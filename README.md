# IngSoftware

### Informacion sobre el negocio
 
#### Detalles de la organizacion

-Actualmente trabajan los dueños, dos personas con acceso total a los sistemas de inventario y boletas y caja.

-No descartan la posibilidad de contratar personal adicional una vez normalizada la situacion del covid, pero no para caja.

### ¿Que servicios ofrecen?

-Venta en el local y despacho a domicilio por pedido telefonico o por whatsapp.

-Alimentos, bebidas, productos de limpieza, etc. ropa, juguetes y otras cosas

### Sistemas que poseen actualmente

Se tiene un punto de venta que funciona pero se encuentra obsoleto. Este punto de venta tiene inventario y 1 pistola, pero solo se usa para revisar los precios de productos de venta ocasional (precios que no se saben de memoria).

### ¿Como se hace una venta?

1- El cliente pide sus productos y/o los lleva al meson
2- se van sumando los precios en una calculadura
3-	si no se sabe el precio, se busca en el sistema

- En el punto de venta, en una ventana de chrome con la pagina del sii, se genera la boleta con el monto total y se imprime o se envia por whatsapp

- En un celular con la app del sii? se genera la boleta con el monto total y se envia por whatsapp

### ¿Como se actualiza el inventario?

El procedimiento para actualizar el inventario con una factura recien llegada:
	for producto in factura:
		- pistolear el codigo de barra de producto
		- ingresar datos del producto
			* nombre
			* cantidad
			* precio unitario
			* precio de venta
		- ok

### Propuesta de mejora
propuesta inicial: leer version pdf de la factura que se puede encontrar en su cuenta en el SII, de modo que el procedimiento pase a ser:
	load factura
	for producto in factura:
		- solicitar pistloear producto.name
		- mostrar datos en pantalla y pedir confirmacion

posible problema: las facturas de distintos proveedores tienen distintas columnas

posible mejora: los proveedores tienen o existe una tabla de equivalencia entre codigo producto  y su codigo de barra
