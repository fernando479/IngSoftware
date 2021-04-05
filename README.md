# IngSoftware

### Información sobre el negocio
![](https://raw.githubusercontent.com/fernando479/IngSoftware/main/jose.jpeg)


## Botillería rotisería y almacén la Tentación

Inicialmente conocido como Provisiones San Bernardo, sus actuales dueños, que tomaron el mando hace alrededor de dos años, han logrado mantenerse, e incluso crecer, en estos tiempos difíciles, como uno de los puntos comerciales del sector norte de paillaco. 

#### Detalles de la organización

Actualmente trabajan los dueños, dos personas con acceso total a los sistemas de inventario y boletas y caja.

No descartan la posibilidad de contratar personal adicional una vez normalizada la situación del covid, pero no para caja.

### ¿Qué servicios ofrecen?

Venta en el local y despacho a domicilio por pedido telefónico o por whatsapp.

Venta de Alimentos, bebidas, productos de limpieza, etc. ropa, juguetes y otras cosas

### Sistemas que poseen actualmente

Se tiene un punto de venta que funciona pero se encuentra obsoleto. Este punto de venta consiste en un computador personal con 2gb de ram y Windows7, que tiene instalado un software de inventario, 1 pistola de codigos de barra y una impresora conectada. El software solo se usa para revisar los precios de productos de venta ocasional (precios que no se saben de memoria).

### ¿Cómo se hace una venta?

 - El cliente pide sus productos y/o los lleva al mesón
 
 - Se van sumando los precios en una calculadora
	- Si no se sabe el precio, se busca en el sistema

- En el punto de venta, en una ventana de chrome con la página del sii, se genera la boleta con el monto total y se imprime o se envia por whatsapp

- En un celular con la app del sii? se genera la boleta con el monto total y se envia por whatsapp

### ¿Cómo se actualiza el inventario?

El procedimiento para actualizar el inventario con una factura recien llegada:
```
	for producto in factura:
		- pistolear el codigo de barra de producto
		- ingresar datos del producto
			* nombre
			* cantidad
			* precio unitario
			* precio de venta
		- confirmar
```

### Posibles cambios

Tener una caja fija donde lleguen los tickets generados por vendedores con pistolas de códigos, y en esta los clientes cancelen el monto indicado y se emitan e impriman las boletas


### Propuesta de mejora

![](https://github.com/fernando479/IngSoftware/blob/main/factura.jpg?raw=true)

propuesta inicial: leer versión pdf de la factura que se puede encontrar en su cuenta en el SII, de modo que el procedimiento pase a ser:

```
	load factura
	for producto in factura:
		- solicitar pistloear producto.name
		- mostrar campos autocompletados permitiendo la edicion
		- confirmar
```

posible problema: las facturas de distintos proveedores tienen distintas columnas o formato

posible mejora: los proveedores tienen o existe una tabla de equivalencia entre codigo producto y su código de barra (desconocido)

### Sistema adicional

Incorporación de un catálogo web con inventario sincronizado que permita a los clientes realizar pedidos para su posterior retiro o despacho.




