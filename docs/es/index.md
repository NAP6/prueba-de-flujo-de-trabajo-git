# Alpaca-Security

### Servicio de vigilancia con reconocimiento biométrico facial

## Antecedentes

Segun el [informe de cifras de robos en el periodo Enero-Septiembre del 2021 (corte 8 de octubre del 2021)](https://www.fiscalia.gob.ec/estadisticas-de-robos/) los robos reportados por unidades economicas (locales comerciales), para el periodo mencionado es de 3.423, lo que implica un incremento del 17.3% comparado con el año 2020.

Con un promedio de 376.5 robos por mes, el horario de 06h00-05h59 ha registrado un 32.7% de los robos en esta categoria.

<img src="https://user-images.githubusercontent.com/43932822/141213683-6fc76c4d-1ed5-483c-a1c8-3af94d1d503d.png" alt="fig 1" style="width:400px;"/>

Ademas en este informe se endica que 47% corresponden ha asaltos.

<img src="https://user-images.githubusercontent.com/43932822/141213822-836c637d-5f17-4351-8541-8f73b07148d7.png" alt="fig 1" style="width:400px;"/>

Es bueno considerar tambien que los lugares que nececitan solucionar con mas urgencia este problema, son las provincias de Pichincha, Guayas y Manabí

<img src="https://user-images.githubusercontent.com/43932822/141214113-2ca447c8-6e72-4996-9cca-7cde4e230677.png" alt="fig 1" style="width:400px;"/>

## Solucion

La empresa Alpaca S.A.S ha propuesto el desarrollo de un sistema de seguridad por video vigilacia, que implemente reconocimiento facial, para poder alertar a los dueños de negocios cuando un antisocial registrado entre ha alguno de sus negocios comerciales.

El sistema deberiía además permitir al personal del negocio, reconocer a la persona que ha realizado alguna fechoria, esto alimentará al sistema de alpaca para brindar un mejor servicio con el tiempo.

> Alpaca-Security pretende ser el eje central de una red de locales comerciales en Ecuador, que reporten a los delincuentes, y se ayuden entre sí.

---

## Descripcion

Alpaca-Security es un sistema de seguridad, cuyo modelo de negocio, es por un lado, vender un sistema de video vigilancia que permita identificar los rostros captados por las camaras; por otro lado, busca vender la información almacenada en este, para determinar si alguna de las personas reconocidas por el sistema de video vigilancia es un delincuente, y asi alertar a los subscriptores.

## Características.

El sistema se comercializará como servicio a locales comerciales, oficinas, instituciones, etc.

El paquete de servicio estará compuesto por:

- Cámara de video con lectura biométrica.
- Software de reconocimiento biométrico.
- Base de datos para almacenamiento de imágenes y metadata.
- Instancia general de propiedad de Alpaca I.S. en AWS(Para alojamiento de la base de datos).

## Funcionalidades

- La cámara estará instalada en el punto de ingreso estratégico del cliente(Persona natural o jurídica que ha contratado el servicio con Alpaca I.S.) que ha contratado el cliente.
- El rostro de la persona que ingresa a la localidad del cliente será captado por la cámara.
- Una vez captado el rostro de la persona, el software de Alpaca Security tomará la imagen capturada y la buscará dentro de la base de datos de imágenes.
- Si la imagen no existe en la base, esta se almacenará en la misma con un estado de SIN ALERTA más la metadata necesaria.
- Si la imagen existe en la base, se verificará el estado de dicha imagen:
  - Estado SIN ALERTA.- Cuando la imagen está con este estado, el sistema no dará ningún tipo de alerta al cliente.
    - En caso de que se haya presentado algún percance entre la persona y el cliente, dicho percance será analizado entre el cliente y personal experto de Alpaca SECURITY.
    - Si se determina y comprueba que en efecto hubo un percance(Robo, estafa). La imagen almacenada de la persona cambiara a estado CON ALERTA.
  - Estado CON ALERTA.- Cuando la imagen está con este estado, el sistema mostrará en la pantalla del computador del cliente un mensaje de alerta: ALERTA PERSONA REPORTADA. Adicionalmente deberá enviar un mensaje vía celular a las personas de contacto del cliente.
  - Si el cliente tiene contratado el servicio de BOTON DE PANICO, el sistema enviará un mensaje de ALERTA PERSONA REPORTADA DONDE EL CLIENTE XXXX, a los clientes cercanos al local del cliente en riesgo.
