# Sistema de Gestión de Inventario y Mantenimiento — Bomberos de San Bernardo

Aplicación web desarrollada para centralizar la gestión de inventario, alertas de vencimiento, mantenciones, gastos, checklist, pérdidas y respaldo en Excel para una compañía de Bomberos de San Bernardo, reemplazando el manejo disperso en planillas Excel[cite: 35]. Permite operar de forma local o mediante contenedor en el puerto 5000 (`http://127.0.0.1:5000`)[cite: 35].

## Tecnologías y prerrequisitos

- Lenguaje/framework: Python 3, Flask, HTML, CSS y JavaScript[cite: 35]
- Base de datos: SQLite[cite: 35]
- Otras dependencias relevantes: librerías indicadas en `Aplicacion/backend/requirements.txt` y Docker (para ejecución en contenedor)[cite: 32, 34]

## Instalación

```bash
git clone [https://github.com/usuario/proyecto-bomberos-san-bernardo.git](https://github.com/usuario/proyecto-bomberos-san-bernardo.git)
cd proyecto-bomberos-san-bernardo
py -m pip install -r Aplicacion/backend/requirements.txt
```

## Configuración

El sistema emplea una base de datos SQLite local y la creación inicial de usuario administrador mediante script local[cite: 32, 35]. No se deben incluir contraseñas, tokens ni datos reales en el repositorio ni en archivos de configuración versionados.

```bash
cd Aplicacion/backend
py crear_admin.py
```

## Uso

Para ejecutar la aplicación en entorno local[cite: 35]:

```bash
cd Aplicacion/backend
py app.py
```

Luego abre `http://127.0.0.1:5000` en el navegador para acceder al sistema[cite: 35]. Para ejecutar las pruebas automatizadas en el backend[cite: 32, 35]:

```bash
cd Aplicacion/backend
py -m unittest discover
```

Para ejecutar con Docker desde la carpeta `Aplicacion`[cite: 32, 34]:

```bash
cd Aplicacion
mkdir data -Force
docker compose up --build -d
docker compose ps
```

## Enfoque de trabajo en equipo

Crystal Clear · Desarrollo individual · Entregas incrementales por hito[cite: 34, 35].

## Estructura del proyecto

```text
Aplicacion/
├── backend/          # Servidor Flask, lógica de alertas/Excel, SQLite y pruebas
├── frontend/         # Interfaz HTML, CSS y JavaScript
├── README_CIERRE.md  # Notas de cierre de la aplicación
└── LEER_PRIMERO.txt  # Indicaciones iniciales
```
[cite: 32]

## Autores

- Benjamín Sandoval — Desarrollo individual (análisis, diseño, implementación, pruebas y documentación)[cite: 35]

Sección: CAPSTONE_002D · Docente guía: Mallén González — elia.gonzalezg@profesor.duoc.cl (contacto alternativo: mallen@mallen.cl)[cite: 34]

## Licencia

no aplica
