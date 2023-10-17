# BD_Zapateria

## Creacion tabla fabricante
![Fabricante](fabricantes.png)

![tabla](estructura.png)

## Creacion tabla Articulo
![articulo](articulo.png)

## Relación uno a muchos
![relacion](relacion.png)



# Consultas BD Zapatería

## 1. Obtener los nombres de los productos de la Zapateria
![consultas](nombre.png)

## 2. Obtener los nombres y los precios de los productos de la Zapatería.
![consultas](2.png)

## 3. Obtener el nombre de los productos cuyo precio sea menor o igual a 50000

`SELECT nombre FROM `Articulo` WHERE precio <= 50000;`

![ Consulta 3](3.png)


 ## 4. Obtener todos los datos de los artículos cuyo precio esté entre 5000 y 40000 (ambas canditades incluidas).

`SELECT * FROM `Articulo` WHERE precio BETWEEN 5000 AND 40000;`


![ Consulta 4](4.png)

## 5. Obtener el nombre y el precio de cada artículo, en dolares.

`SELECT nombre, precio / 4242 AS precio_dolares FROM  Articulo;`

![ Consulta 5](/5.png)

## 6. Obtener el precio promedio de todos los artículos

`SELECT AVG (precio) AS precio_promedio FROM  Articulo;`

![ Consulta 6](6.png)

## 7. Obtener el precio medio de los artículos cuyo codigo de fabricante sea 2.

`SELECT AVG(precio) AS precio_medio FROM Articulo WHERE codigo_fab = 2;`


![ Consulta 7](7.png)

## 8. Obtener el número de artículos cuyo precio sea mayor o igual a 50000

`SELECT COUNT(*) AS numero_de_articulos FROM Articulo WHERE precio >= 50000;`

![ Consulta 8](8.png)

## 9. Obtener el nombre y precio de los artículos cuyo precio sea mayor o igual a 50000 y ordenarlos descendentemente por precio, y luego ascendentemente por nombre.

`SELECT nombre, precio FROM Articulo WHERE precio>= 50000  
ORDER BY `Articulo`nombre``


![ Consulta 9](9.png)


![ Consulta 9_2](9_2.png)

## 10. Obtener un listado completo de artículos, incluyendo por cada articulo los datos del artículo y de su fabricante.

`SELECT Articulo.*, Fabricante.* FROM Fabricante INNER JOIN Articulo ON Fabricante.codigo=Articulo.codigo_fab;`

![ Consulta 10](10.png)