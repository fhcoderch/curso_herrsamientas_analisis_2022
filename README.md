#diplomado en analisis de datos

## curso_herrsamientas_analisis_2022

repositorio para aprender del curso de herramienta de analisis datos

docuento dxe prueba para comenzar a usar Github

esto es una prueba 


# tercert subtitulo 
dentro de Git veremos como crear un repositoris, como modificar un archivo y crear una rama


#primer ejercicio en SQL

use jarvis;

CREATE TABLE FHC_CLIENTES (
ID INT AUTO_INCREMENT AUTO_INCREMENT KEY
, NOMBRE VARCHAR(25)
,PAIS VARCHAR (25)
,CATEGORIA VARCHAR (30)
, NUM_VENTA INT);

use jarvis

-- SELECCIONANDO LA BASE DE DATOS JARVIS LOS 
-- "--" SON LA FORMA DE ESCRIBOR COMENTARIOS	
use jarvis;
	-- CREANDO TABLA PERSONALIZADA FHC_CLIENTES 

   CREATE TABLE FHC_CLIENTES (
	ID INT AUTO_INCREMENT AUTO_INCREMENT KEY
	,NOMBRE VARCHAR(25)
	,PAIS VARCHAR (25)
	,CATEGORIA VARCHAR (30)
	,NUM_VENTA INT);


-- MODIFINCANDO  LA FHC_CLIENTES, 
-- AGREGANDO COLUMNA TELEFONO 
	ALTER TABLE FHC_CLIENTES ADD TELEFONO INT;

-- AGREGANDO LA COLUMNA BORRADO 
	ALTER TABLE FHC_CLIENTES ADD BORRADO BOOLEAN;

-- ELIMINANDO LA COLUMNA NUM_VENTA
ALTER TABLE FHC_CLIENTES DROP NUM_VENTA;

-- MODIFICANDO LA COLUMNA TELEFONOS
ALTER TABLE FHC_CLIENTES MODIFY COLUMN TELEFONO VARCHAR(15);

-- ELIMINANDO LA TABLA FHCTMP
DROP TABLE FHCTMP;


-- %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%5

-- AGREGANDO DATOS 
INSERT INTO FHC_CLIENTES (NOMBRE, PAIS, CATEGORIA, TELEFONO ) VALUES ('Felipe Hernandez, Chile, Premium,+56968621330')


-- 
use jarvis;

CREATE TABLE FHC_CLIENTES (
ID INT AUTO_INCREMENT AUTO_INCREMENT KEY
,NOMBRE VARCHAR(25)
,PAIS VARCHAR (25)
,CATEGORIA VARCHAR (30)
,NUM_VENTA INT);
USE jarvis;
DROP TABLE FHC_CLIENTES;

--%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

-- REVISANDO LA TABLA CLINETES

SELECT * FROM DETALLE_COMPRA

-- CONSULTAS A LA TABLA

-- MAX
SELECT MAX(NUM_VENTA)  
FROM CLIENTES 

-- CONSULTA ANIDADA
SELECT * FROM CLIENTES WHERE NUM_VENTA =(
SELECT  MAX(NUM_VENTA) FROM CLIENTES)

SELECT CATEGORIA, NOMBRE
FROM CLIENTES
WHERE NUM_VENTA = (
SELECT MAX(NUM_VENTA)
FROM CLIENTES)