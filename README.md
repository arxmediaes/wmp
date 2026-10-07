# Propuesta WMP — Ricardo

## Subir a GitHub Pages
1. Crea un repositorio en GitHub.
2. Descomprime este ZIP y sube su contenido a la raíz del repositorio. index.html debe quedar en la raíz, junto a assets y los demás archivos.
3. En Settings → Pages, selecciona Deploy from a branch, la rama main y la carpeta / (root). Guarda.
4. GitHub mostrará el enlace cuando termine la publicación.

No requiere npm, instalación ni compilación. No subas el ZIP como un único archivo: sube los archivos descomprimidos.

## Funcionamiento
Los cinco proyectos y sus recorridos viven en la misma web. Los datos de prueba se conservan en el navegador; exportarlos permite guardar una copia. Los perfiles, producciones y accesos de ejemplo no crean pagos, reservas ni contactos reales.

## IA, n8n y Excel
La opción Conexiones permite configurar webhooks HTTPS de n8n. La clave del modelo de IA va en n8n, nunca en el repositorio. El token de acceso al webhook se conserva solo durante la sesión.

IA recibe {project, message, history} y devuelve {reply}.
Datos recibe {project, action: "load"} y devuelve {data}, o recibe {project, action: "save", data} y devuelve {ok: true}.
El workflow debe permitir el origen de tu GitHub Pages mediante CORS. El guardado local funciona sin conectar esos servicios.

## Actualizar
Edita o reemplaza los archivos y haz commit en la rama publicada. Conserva las rutas relativas y la carpeta assets. No necesita un dominio propio.
