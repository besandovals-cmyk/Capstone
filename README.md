# Sistema de Gestión de Inventario y Mantenimiento — Bomberos de San Bernardo

Aplicación web desarrollada para centralizar la gestión de inventario, alertas de vencimiento, mantenciones, gastos, checklist, pérdidas y respaldo en Excel para una compañía de Bomberos de San Bernardo, reemplazando el manejo disperso en planillas Excel. Permite operar de forma local o mediante contenedor en el puerto 5000 (`http://127.0.0.1:5000`).

## Tecnologías y prerrequisitos

- Lenguaje/framework: Python 3, Flask, HTML, CSS y JavaScript
- Base de datos: SQLite
- Otras dependencias relevantes: librerías indicadas en `requirements.txt` dentro de `Sistema_Bomberos_Multicompania.zip` y Docker (para ejecución en contenedor)

## Instalación

```bash
git clone https://github.com/besandovals-cmyk/Capstone.git
cd Capstone
```

Extrae `Fase 2/Evidencias Proyecto/Sistema_Bomberos_Multicompania.zip` en tu carpeta de trabajo e instala las dependencias desde `Aplicacion/backend/requirements.txt`:

```bash
py -m pip install -r Aplicacion/backend/requirements.txt
```

## Configuración

El sistema emplea una base de datos SQLite local y la creación inicial de usuario administrador mediante script local. No se deben incluir contraseñas, tokens ni datos reales en el repositorio ni en archivos de configuración versionados.

```bash
py Aplicacion/backend/crear_admin.py
```

## Uso

Para ejecutar la aplicación en entorno local:

```bash
py Aplicacion/backend/app.py
```

Luego abre `http://127.0.0.1:5000` en el navegador para acceder al sistema. Para ejecutar las pruebas automatizadas en el backend:

```bash
py -m unittest discover -s Aplicacion/backend
```

Para ejecutar con Docker desde la carpeta `Aplicacion`:

```bash
cd Aplicacion
mkdir data -Force
docker compose up --build -d
docker compose ps
```

## Enfoque de trabajo en equipo

Crystal Clear · Desarrollo individual · Entregas incrementales por hito.

## Estructura del proyecto

```text
Capstone/
├── Fase 1/
├── Fase 2/
│   ├── Evidencias Individuales/
│   ├── Evidencias Grupales/
│   └── Evidencias Proyecto/
│       ├── Evidencias De Documentacion/
│       ├── Presentación_Proyecto.pptx
│       └── Sistema_Bomberos_Multicompania.zip
├── Fase 3/
└── README.md
```

## Autores

- Benjamín Sandoval — Desarrollo individual (análisis, diseño, implementación, pruebas y documentación)

Sección: CAPSTONE_002D · Docente guía: Mallén González — elia.gonzalezg@profesor.duoc.cl (contacto alternativo: mallen@mallen.cl)

## Licencia

no aplica
