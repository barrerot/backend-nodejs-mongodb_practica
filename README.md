
# Nodepop

Esta API ha sido Consiste en un backend construido con Express, NodeJS y MongoDB.

# Nodepop

Website and API application.

## Install

Install dependencies:

```sh
$ npm install
```

Review database connection on /lib/connectMongoose.js (see "Start a MongoDB Server in MacOS or Linux")

Load initial data:

```sh
# this command deletes all the data in the database and create default data
$ npm run init-db
```

## Start
In production:

```sh
npm start
```

In development:

```sh
npm run dev
```

## Start a MongoDB Server in MacOS or Linux

From the folder of the server:

```sh
./bin/mongod --dbpath ./data
```

## API Endpoints

## ### Parámetros de consulta

Ambas vías de consulta admiten los mismos parámetros. Un ejemplo de consulta seria:
```
localhost:3000/anuncios?type=compra&type=venta&tags=work&range=10-100&limit=3&skip=3&sort=nombre
```

Los parámetros aceptados son:
- **Name**: El nombre de un artículo. No distingue minúsculas de mayúsculas.
- **Tags**: El nombre de un tag o categoría.
- **Type**: Venta o Compra según el tipo de anuncio.
- **Range**: Precio mínimo y máximo separado por un guión.
- **Limit**: Número máximo de anuncios a devolver.
- **Skip**: Número de anuncios a saltar. En caso de paginación.
- **Sort**: Campo por el cu

### GET /api/anuncios/
### GET /api/anuncios/tags

```json
{
    "results": [
        {
            "_id": "6511d779c0d44ab041a37592",
            "name": "Smith",
            "age": 24
        }
    ]
}
```
