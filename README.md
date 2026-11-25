# Tu Menú — cartas digitales interactivas

Aplicación web adaptable a cafeterías, bares y restaurantes, con la carta de **Monti** como demostración. La marca general es **Tu Menú**; al cargar el logo de un local, se cambia su identidad visual, plantilla, nombre e ícono de pestaña sin modificar el sistema base.

## Funciones de la demo
- QR por mesa; carta pública y carrito habilitado desde el panel del mostrador
- Pedidos, personalizaciones, seguimiento, solicitud de cuenta y cierre manual sin pasarela de pago
- Panel de mesas, precios, disponibilidad, stock y estadísticas de ejemplo
- Fotos por producto o ilustraciones lineales propias cuando no hay foto
- **Comandas individuales de cocina**: botón de impresión en Mesas y cuentas / Pedidos; vista previa con mesa, número, hora, cantidad, variantes y observaciones
- Anchos de **58 mm** y **80 mm**, con ejemplo imprimible

## Impresión de comandas
La impresión actual es **manual con el diálogo del navegador** (seleccionar la impresora instalada). El sistema **no imprime automáticamente ni confirma impresión física**.

Para impresión automática al llegar pedidos se requiere backend compartido y un agente de impresión local o un servicio como QZ Tray/PrintNode, con una cola confiable por identificador de pedido y control de reimpresiones.

## Importante antes de lanzar
La demo guarda datos en el navegador. No conecta PC y celulares entre sí, ni protege todavía el panel de administración; no debe utilizarse con pedidos reales. Se necesita autenticación, autorización por local, sesiones de mesa comprobadas desde el servidor y sincronización de pedidos/impresión.

Los logos de cada restaurante y las fotografías que se agreguen deberán almacenarse centralmente al conectar la base de datos. `branding/` contiene la marca Tu Menú.

## Actualización V9 — Carta genérica
- Catálogo de **35 productos ficticios** distribuidos en Restaurante, Cafetería y Para llevar. No son los platos ni los precios de Monti ni de otro negocio real.
- Los textos de la portada son genéricos y editables desde Personalización junto al logo, la paleta y la plantilla.
- Las categorías se generan desde los datos del catálogo. Referencia: `data/catalogo-ejemplo.json`.
- **iPhone:** los campos de entrada, listas y áreas de texto tienen como mínimo 16px en pantallas móviles para evitar el zoom automático al escribir. Se mantiene el zoom manual.
- La demo usa una clave nueva (`menu-demo-v9-tumenu-demo`) para no importar consumos, precios ni pedidos de antiguas pruebas.
- La gestión y los pedidos son simulados hasta conectar un backend central y proteger el panel administrativo.


## Actualización V10 — Instalación e identidad de app

- `branding/apple-touch-icon.png`: PNG de **180×180** para iPhone/iPad (ya no muestra la inicial genérica si se agrega después de publicar).
- `branding/icon-192.png` y `branding/icon-512.png`: íconos para Android/Chromium, declarados en `manifest.webmanifest`.
- El ícono y nombre de la pestaña siguen la identidad del local en el navegador donde se cargó el logo.
- La demo convierte el logo cargado en un ícono táctil PNG de vista local. **iOS puede ignorar los íconos personalizados expresados como URL de datos**; en ese caso se muestra el ícono general Tu Menú al instalar. Para asegurar el del local en cualquier dispositivo se requiere alojamiento público del logo, manifiesto por local y configuración central.
- Si un acceso ya está instalado en iPhone, puede ser necesario borrarlo de Inicio y volver a usar *Compartir → Añadir a pantalla de inicio*; no se modifica de forma garantizada el ícono existente.
- La subida de logos continúa siendo local a ese navegador hasta la futura integración con Supabase. No se modifican los productos, las mesas, las cuentas ni las comandas.
