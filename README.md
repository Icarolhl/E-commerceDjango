# E-commerce Django Project

This repository contains a Django-based e-commerce application (project root: `loja`). It's a small online store with product listing, cart, orders, user profiles, and admin features.

## Disclaimer

This project was created for study purposes and is not ready for production use.

## Features

- Product listing with variations and images
- Shopping cart and checkout flow
- Order management (`pedido` app)
- User profile management (`perfil` app)
- Media handling for product images

## Tech stack

- Python 3.x
- Django (project apps: `produto`, `pedido`, `perfil`, `loja` settings)
- SQLite (default `db.sqlite3`) for development

## Quickstart (Windows)

1. Create and activate a virtual environment:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install dependencies (add a `requirements.txt` if needed):

```powershell
pip install -r requirements.txt
```

3. Apply migrations and run the development server:

```powershell
python manage.py migrate
python manage.py runserver
```

4. Access the site at `http://127.0.0.1:8000/`.

## Media and Static files

- User-uploaded product images are stored under the `media/` directory (`media/produto_imagens/...`).
- Static assets are in the `templates/static/` and top-level `static/` folders. Configure `MEDIA_ROOT` and `STATIC_ROOT` in `loja/settings.py` for production.

## Database

- The project ships with `db.sqlite3` for development. For production, switch to PostgreSQL or another production-ready DB and update `loja/settings.py`.


## Project structure (high level)

- `loja/` — Django project settings and URLs
- `produto/` — product models, views, templates, templatetags
- `pedido/` — order models, views, templates
- `perfil/` — user profile forms and views
- `media/` — uploaded images

## Contributing

- Open an issue for bugs or feature requests.
- Create a branch, add tests when applicable, and submit a pull request.
