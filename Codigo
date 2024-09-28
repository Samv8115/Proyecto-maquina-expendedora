CREATE DATABASE maquina_expendedora;
USE maquina_expendedora;
CREATE TABLE Productos (
    id_productos INT AUTO_INCREMENT PRIMARY KEY,
    nombre ENUM('papas', 'gaseosa', 'jugo', 'galleta') NOT NULL,
    cantidad_actual INT NOT NULL,
    precio DECIMAL(10, 2) NOT NULL
);
CREATE TABLE Cliente (
    id_cliente INT AUTO_INCREMENT PRIMARY KEY,
    credito INT
);
CREATE TABLE Compra (
    id_compra INT AUTO_INCREMENT PRIMARY KEY,
    id_cliente INT,
    fecha DATETIME,
    total_compra DECIMAL(10, 2),
    FOREIGN KEY (id_cliente) REFERENCES Cliente(id_cliente)
);

CREATE TABLE Info_compra (
    id_info_compra INT AUTO_INCREMENT PRIMARY KEY,
    id_productos INT,
    id_cliente INT,
    cantidad INT NOT NULL,
    FOREIGN KEY (id_productos) REFERENCES Productos(id_productos),
    FOREIGN KEY (id_cliente) REFERENCES Cliente(id_cliente)
);
INSERT INTO Productos (nombre, cantidad_actual, precio)
VALUES
	('papas',34,2.34),
    ('gaseosa',25,4.19),
    ('jugo',27,2.58),
    ('galleta',16,3.44);
    
CREATE INDEX idx_nombre_producto ON Productos(nombre);
CREATE INDEX idx_cantidad_actual_producto ON Productos(cantidad_actual);
CREATE INDEX idx_precio_producto ON Productos(precio);

CREATE INDEX idx_credito_cliente ON Cliente(credito);

CREATE INDEX idx_fecha_compra ON Compra(fecha);
CREATE INDEX idx_total_compra_compra ON Compra(total_compra);

CREATE INDEX idx_cantidad_info_compra ON Info_compra(cantidad);

