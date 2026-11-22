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
