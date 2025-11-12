# FPMI Library API Specification

This folder contains an example of an **OpenAPI 3.0.3 specification** built with an *API-first mindset*.
The goal is to demonstrate how a clean, modular, and readable specification can guide implementation, rather than being generated after the code.

## Key principles

- **API-first** – the design starts with defining the contract, not the code
- **Reusable components** – all schemas, parameters, and responses are centralized
- **Consistency** – naming, status codes, and data structures follow a unified pattern
- **Clarity** – examples and descriptions are written for humans, not just machines
- **Extensibility** – the spec can grow as new endpoints and roles are added

## Files

| File                | Description                                        |
|---------------------|----------------------------------------------------|
| `fpmi-library.yaml` | The main OpenAPI 3.0.3 specification               |
| `README.md`         | This file                                          |

## How to view

You can visualize and test this spec using any OpenAPI viewer:

- [Swagger Editor](https://editor.swagger.io)
- [Redocly](https://redocly.github.io/redoc/)
- [Stoplight Studio](https://stoplight.io/studio)

Just copy the YAML file content and paste it into your tool of choice.

## Quick example

```yaml
  /books:
    get:
      tags:
        - Books
      summary: Get All Books
      description: Retrieves a paginated list of all books in the library, with filtering options.
      operationId: Books_RetrieveList
      security:
        - oAuth2:
            - Library.Manage
      x-required-roles:
        - '#/components/x-roles/Library.Books.View'
      parameters:
        - $ref: '#/components/parameters/SearchQuery'
        - $ref: '#/components/parameters/Limit'
        - $ref: '#/components/parameters/Offset'
      responses:
        '200':
          $ref: '#/components/responses/BooksList200'
```
