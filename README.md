<h1 align="center">File Upload</h1>
<p align="center">
    <a href="#about">About |</a>
    <a href="#technologies">Technologies |</a>
    <a href="#installation-and-usage">Installation and usage</a>
</p>

## About
Back end of an image upload application. It accepts images of up to 2 MB, stores the image metadata in MongoDB and the image files on Amazon S3.

![0](https://user-images.githubusercontent.com/76854209/189429847-dbc1c146-0c59-49b6-b14a-a8f3738d5962.jpg)
![1](https://user-images.githubusercontent.com/76854209/189429851-61c54467-d893-49f2-8a0a-b2d4f9a68b32.jpg)
![2](https://user-images.githubusercontent.com/76854209/189429853-d64fb2f6-a986-4525-abc3-cf79b82cc407.jpg)
![3](https://user-images.githubusercontent.com/76854209/189429854-81b27679-822a-41e5-bc17-44165f74ef44.jpg)
![5](https://user-images.githubusercontent.com/76854209/189429856-f2197ee9-f3f3-4e42-89f0-64d09ccd731f.jpg)
![6](https://user-images.githubusercontent.com/76854209/189429859-14daa34d-97c0-48da-9d2a-77dcf602ed61.jpg)
![7](https://user-images.githubusercontent.com/76854209/189429860-57d28e44-bda8-4c06-aa1d-62595b1bb1f2.jpg)

The application follows good practices such as configuration through environment variables and a storage switch: images are saved locally during development and on Amazon S3 in production. The server only starts after the database connection is established.

## Technologies
- [Node.js](https://nodejs.org/) and [Express](https://expressjs.com/)
- [MongoDB](https://www.mongodb.com/) with [Mongoose](https://mongoosejs.com/)
- [Multer](https://github.com/expressjs/multer) and multer-s3 for file uploads
- [Amazon S3](https://aws.amazon.com/s3/)

## Installation and usage
> This guide assumes you have Node.js installed, a MongoDB database (on [MongoDB Atlas](https://cloud.mongodb.com/) or local) with its connection details, and an AWS account with an S3 bucket configured.

Create a `.env` file with the environment variables, following the `.env.example` template.

```bash
$ git clone https://github.com/leandro-srl/upload-de-arquivos-backend-node
$ cd upload-de-arquivos-backend-node
```

### Installing dependencies
```bash
$ npm i
```

To start the server, run:
```bash
$ npm run dev
```

## Testing the endpoints

Use an API client such as [Postman](https://www.postman.com/) or [Insomnia](https://insomnia.rest/download).

**Front end:** [upload-de-arquivos-frontend-react](https://github.com/leandro-srl/upload-de-arquivos-frontend-react)

**Deploy:** deployed on Heroku in 2022 (offline since Heroku ended its free tier in November 2022).
