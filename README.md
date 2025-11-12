# API-First Example: SU FPMI Library API

This repository demonstrates an **API-first approach** to designing and documenting REST APIs using OpenAPI 3.0.3.  
Instead of generating the specification *after* the code, the API contract is defined *first* - guiding the implementation that follows.

### Key ideas
- **Specification-driven design**: Define the API contract before development.
- **Reusable components**: All schemas, headers, and responses are modular and centralized.
- **Improved readability**: Examples and patterns make the specification more human-friendly.
- **Security and roles**: OAuth2 and role-based access are clearly defined in the spec.

### Example spec
See [`/openapi/fpmi-library.yaml`](openapi/fpmi-library.yaml).

### Preview
You can visualize it using:
- [Swagger Editor](https://editor.swagger.io)
- [Redocly](https://redocly.github.io/redoc/)

---

© 2025 Andrei Golovistikov — Licensed under MIT
