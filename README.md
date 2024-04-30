<h1 align="center">
Assessment for Junior Laravel Developer
</h1>

**Output**: All tasks should be committed to a Github repo, using best practices for commits. Once complete, please email a link to the repository to mbowyer@tariffcom.com. If you have created a private repository, please add mchlbwyr as a contributor.

## Level 1

### Goals

- [ ] Implement Laravel’s default login features using Laravel Breeze
- [ ] Develop User CRUD functionalities using Tailwind styling
- [ ] Add Validation rules to the User CRUD

### Prerequisites

Base the user migration file on the following table:

```mysql
mysql> show columns from users;
+-------------------+-----------------+------+-----+---------+----------------+
| Field             | Type            | Null | Key | Default | Extra          |
+-------------------+-----------------+------+-----+---------+----------------+
| id                | bigint unsigned | NO   | PRI | NULL    | auto_increment |
| prefixname        | varchar(255)    | YES  |     | NULL    |                |
| firstname         | varchar(255)    | NO   |     | NULL    |                |
| middlename        | varchar(255)    | YES  |     | NULL    |                |
| lastname          | varchar(255)    | NO   |     | NULL    |                |
| suffixname        | varchar(255)    | YES  |     | NULL    |                |
| email             | varchar(255)    | NO   | UNI | NULL    |                |
| password          | varchar(255)    | NO   |     | NULL    |                |
| photo             | text            | YES  |     | NULL    |                |
| type              | varchar(255)    | YES  | MUL | user    |                |
| remember_token    | varchar(100)    | YES  |     | NULL    |                |
| email_verified_at | timestamp       | YES  |     | NULL    |                |
| created_at        | timestamp       | YES  |     | NULL    |                |
| updated_at        | timestamp       | YES  |     | NULL    |                |
| deleted_at        | timestamp       | YES  |     | NULL    |                |
+-------------------+-----------------+------+-----+---------+----------------+
```

<br>

### Instructions

#### Initial Tasks

1. Start a new project in Laravel 10
1. Implement the default login feature using the [laravel/breeze](https://laravel.com/docs/10.x/starter-kits#laravel-breeze) package using the Inertia stack with Vue.
1. Add a page to list all users (users.index) in a table.
1. Add a page to display a single user (users.show).
1. Add a page to display the form to create a new user (users.create).
1. Add a page to edit a user (users.edit / users.update).
1. Add a button to delete a user (users.destroy).

#### Extended Tasks

1. Use your best judgment to add validation rules for the fields (for both creating and deleting a user).
1. Create a new migration to alter the `prefixname` so it can only be one of `[Mr, Mrs, Ms]`.
1. Add a page to list all soft deleted users (users.trashed).
1. Add a button to restore a soft deleted user (users.restore).
1. Add a button to permanently delete a soft deleted user (users.delete).
1. Use TailwindCSS to style any pages and components you have created.
