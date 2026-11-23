# Sitio web · Auto Repuestos MAZA (Flask)

## Cómo abrirlo en Visual Studio Code

1. Descomprime el ZIP y abre la carpeta `maza_web` en VS Code (*Archivo › Abrir carpeta*).
2. Abre una terminal (*Terminal › Nueva terminal*) y ejecuta:

```bash
python -m venv venv
# Windows:
venv\Scripts\activate
# Mac / Linux:
source venv/bin/activate

pip install -r requirements.txt
python app.py
```

3. Abre en el navegador: http://127.0.0.1:5000

## Estructura

```
maza_web/
├── app.py                 ← rutas y datos de la empresa (teléfonos, direcciones, redes)
├── requirements.txt
├── data/destacados.json   ← piezas destacadas que se muestran
├── templates/             ← páginas HTML (Jinja)
│   ├── base.html          ← cabecera, menú y pie de página
│   ├── index.html         ← inicio
│   ├── catalogo.html      ← piezas destacadas y demás líneas
│   ├── nosotros.html      ← historia, misión, visión y equipo
│   ├── contacto.html      ← formulario que abre WhatsApp
│   └── 404.html
└── static/
    ├── css/styles.css     ← colores y diseño
    ├── js/main.js         ← menú móvil y menú desplegable
    └── img/               ← logo, fotos de bobinas y fondo
```

## Qué editar

- **Teléfonos, direcciones y WhatsApp:** diccionario `EMPRESA` en `app.py`.
- **TikTok e Instagram:** en `EMPRESA["redes"]` cambia `"#"` por el enlace de cada cuenta.
- **Piezas destacadas:** agrega, quita o cambia piezas en `data/destacados.json` (código, vehículos, pines e imagen de `static/img`).
- **Colores:** variables al inicio de `static/css/styles.css` (`--rojo`, `--negro`, etc.).
