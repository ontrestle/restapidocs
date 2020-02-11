# Comradery API Docs

Base URL: https://api.comradery.io/v2

## Authentication

On your Admin Panel, you should be able to generate an Admin-scoped API key. Be _very_ careful with this API key, it can do everything you can including creating, reading, editing, and deleting users, posts, and more.

To authenticate you must include an `Authorization: Token <api_key_here>` header on each request.

## Analytics

We have integrated with Segment for analytics. Please read the documentation [here](analytics/segment.md) for more information.

## Custom CSS

We allow you to upload custom CSS! Please read the documentation [here](customization/css.md) for more information.

## Endpoints

### Communities

Each endpoint manipulates or displays information related to the provided community. Note that your API key will only work on communities that you control.

* [Retrieve a Community](communities/get.md) : `GET /community/<community_url>`
* [Edit a Community](communities/edit.md) : `POST /community/<community_url>`

### Users

Endpoints for viewing and manipulating profiles.

* [Create a User](users/create.md) : `POST /create_user`
* [Retrieve a List of Users](users/list.md) : `GET /community/<community_url>/people`
* [Retrieve a User](users/get.md) : `GET /person/<person_email>`
* [Edit a User](users/edit.md) : `POST /person/<person_email>`
* [Login a User](users/login.md) : `POST /login/<person_email>`

### Posts

Endpoints for viewing and manipulating posts.

* [Create a Post](posts/create.md) : `POST /post/create`
* [Retrieve a List of Posts](posts/list.md) : `GET /community/<community_url>/posts
* [Retrieve a Post](posts/get.md) : `GET /post/<post_id>`
* [Edit a Post](posts/edit.md) : `POST /post/<post_id>`

### Comments

Endpoints for viewing and manipulation comments.

* [Create a Comment](comments/create.md) : `POST /post/<post_id>/comment`
* [Retrieve a Comment](comments/get.md) : `GET /comment/<comment_id>`
* [Edit a Comment](comments/edit.md) : `POST /comment/<comment_id>`
