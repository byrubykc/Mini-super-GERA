# Mini-super-GERA
*Proyecto de Ingeniería de Software*

---------ESPECIFICACIÓN DE REQUISITOS---------

-Objetivo-
Este documento define los requisitos funcionales y no funcionales para el desarrollo de una aplicación de escritorio que permita gestionar y controlar los procesos de un mini-super, incluyendo el control de inventario, usuarios, cuentas de crédito de clientes, cobro de caja, etc.

-Alcance-
El sistema estará dirigido a abarrotes medianos y mini-supers, y será utilizado por el personal de la sucursal en caja. No incluirá funcionalidades para usuarios finales externos (ej. consulta web o móvil).


---------Descripción General---------

-Objetivos del Sistema-
Digitalizar el registro de productos, precios, usuarios (tanto de personal, como cuentas de crédito para clientes)
Automatizar el proceso de cobro y fiado.
Gestionar cuentas de crédito de clientes.

-Actores-
Administrador: Gestiona usuarios (personal), cuentas (clientes) y controla entrada y salida en el inventario.
Cajero (Personal): Escanea productos de los clientes, realiza cobros, de contado y crédito, gestiona los abonos a cuentas de crédito y liquidaciones.


---------Requisitos Funcionales---------

-Gestión de productos-

RF-01
El sistema debe permitir al administrador agregar nuevos productos al inventario con los datos (id_prod, cod_barras, descripcion, cantidad, precio_unidad)
RF-02
El sistema debe permitir al administrador editar información de productos existentes.
RF-03
El sistema debe permitir al administrador eliminar productos del inventario
RF-04
El sistema debe permitir al usuario buscar productos por descripcion, id o código de barras


-Gestión de usuarios (personal)-

RF-05
El sistema debe permitir al administrador agregar usuarios con los datos (id_user ,nombre, num_celular)
RF-06
El sistema debe permitir al administrador eliminar usuarios (Ej. Un trabajador renunció o lo despidieron, por lo que ya no debe tener cuenta con acceso)


-Cuentas de crédito-

RF-07
El sistema debe permitir al administrador registrar cuentas de crédito para los clientes frecuentes con id_cliente y nombre
RF-08
El sistema debe permitir al usuario agregar la cantidad de la compra a crédito y los últimos 5 productos adquiridos a la cuenta del cliente
RF-09
El sistema debe permitir al administrador eliminar cuentas de clientes (solo si esta cuenta ya ha sido liquidada)


-Autenticación y Seguridad-

RF-05
El sistema debe permitir al empleado iniciar sesión con usuario y contraseña correspondiente (cajero, administrador)
RF-06
El sistema debe permitir al usuario o administrador finalizar su sesión 


---------Requisitos No Funcionales---------

-Usabilidad-

RNF-01
El sistema debe permitir usar atajos de teclado


-Rendimiento-

RNF-02
El sistema debe tener un tiempo de respuesta menor de 3 segundos en todas las operaciones
RNF-03
El sistema debe tener capacidad para gestionar 5000 productos y 50 cuentas como mínimo


-Seguridad-

RNF-04
El sistema debe poder almacenar las contraseñas encriptadas usando la función hash (SHA-256) 
RNF-05
El sistema debe tener obtener respaldos automáticos de la información todos los días a las 22:15 horas


-Compatibilidad-

RNF-06
El sistema debe ser compatible para su operación con Windows 10/11 y Linux (Ubuntu)
RNF-07
El sistema debe utilizar PostgreSQL como manejador de base de datos
RNF-08
El Sistema debe ser desarrollado en Java o Python
