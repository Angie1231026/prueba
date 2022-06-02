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


