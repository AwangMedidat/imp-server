# IMP REST API

CRUD for office needs, such as inputting, displaying, editing, and deleting data. And this includes the REST API

## Installation

Clone the repository.

Change Directory `cd/imp-server`

Install dependencies: `composer install`

Create a copy of the `.env.example` file and name it `.env`

Configure the `.env` file with your database and other settings.

Migrate the database: `php artisan migrate`

Seed the Database: `php artisan db:seed --class=PostSeeder`

## Usage

To deploy this project run

```bash
  php artisan serve
```

## API Reference

#### Get all items

```http
  GET /api/v1/posts
```

| Parameter | Type | Description                |
| :-------- | :--- | :------------------------- |
| `-`       | `-`  | **Required**. Your API key |

#### Get item

```http
  GET /api/v1/posts/${id}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of item to fetch |

#### Create item

```http
  POST /api/v1/posts
```

| Body      | Type     | Description   |
| :-------- | :------- | :------------ |
| `name`    | `string` | **Required**. |
| `divisi`  | `string` | **Required**. |
| `jabatan` | `string` | **Required**. |

#### Update item

```http
  PUT /api/v1/posts
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of item to fetch |

| Body      | Type     | Description   |
| :-------- | :------- | :------------ |
| `name`    | `string` | **Required**. |
| `divisi`  | `string` | **Required**. |
| `jabatan` | `string` | **Required**. |

#### Delete item

```http
  DELETE /api/v1/posts/${id}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of item to fetch |
