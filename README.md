# Lab 31 – Incidencia: Conexión bloqueada por NSG (puerto cerrado)

## Objetivo
Reproducir un fallo de conectividad por NSG y resolverlo creando la regla correcta.

## Qué ha pasado (incidencia)
La VM está encendida y con IP/route bien, pero el puerto está bloqueado por una regla de NSG. El test de conectividad falla.

## Resolución
He identificado el NSG asociado, he creado una regla de entrada permitiendo el puerto y he validado con Test-NetConnection.

## Evidencias

### 01 – Test-NetConnection FAIL
<img src="images/01-testnetconnection-fail.png" width="800">

### 02 – Regla NSG creada/modificada
<img src="images/02-nsg-rule.png" width="800">

### 03 – Test-NetConnection OK
<img src="images/03-testnetconnection-ok.png" width="800">

## Qué diría en entrevista
“Cuando un puerto falla, reviso NSG efectivo, UDR y firewall del SO. Empiezo por el control más común: NSG en NIC/subnet.”
