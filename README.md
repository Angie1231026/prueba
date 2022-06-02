# prueba
prueba tecnica cafeteria

CREATE DATABASE cafeteria; 

use cafeteria; 

CREATE TABLE producto
 (
 id INT primary key not null AUTO_INCREMENT,
 nombre VARCHAR (50),
 referencia VARCHAR (25),
 precio INT,
 peso INT,
 categoria VARCHAR (50),
 stock INT,
 fechaCreacion DATE
 );
 
 CREATE TABLE venta
 (
 idVenta INT primary key not null AUTO_INCREMENT,
 cantidad VARCHAR (50),
 id_producto INT,
 CONSTRAINT fk_producto FOREIGN KEY (id_producto)  
REFERENCES producto(id)  
 );


Consultas

Stock

SELECT id FROM producto WHERE id = @id ) UPDATE producto SET stock = stock - @cantidad WHERE id = @id

Mayor cantidad en stock

SELECT nombre, MAX(stock) edad FROM producto GROUP BY nombre

Más vendido

SELECT producto.nombre, SUM(venta.cantidad) as cantidad FROM ventas JOIN producto ON venta.id_producto = producto.id GROUP BY producto.id ORDER BY SUM(venta.cantidad) DESC LIMIT 1
