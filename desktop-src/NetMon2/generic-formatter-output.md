---
description: En las listas y tablas de esta sección se muestra el resultado del formateador genérico. Tenga en cuenta que el formateador genérico usa los miembros DataType y Qualifier de la estructura PROPERTYINFO para determinar cómo se da formato a los datos mostrados.
ms.assetid: cf3dc6cd-7b24-464a-9d2b-5e35c4e8825e
title: Salida del formateador genérico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf4b334dd717c7ff332c3b730afb57d4be611ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677285"
---
# <a name="generic-formatter-output"></a>Salida del formateador genérico

En las listas y tablas de esta sección se muestra el resultado del [*formateador genérico*](g.md). Tenga en cuenta que el formateador genérico usa los miembros **DataType** y **Qualifier** de la estructura [**PROPERTYINFO**](propertyinfo.md) para determinar cómo se da formato a los datos mostrados.

Para obtener más información y un ejemplo de la salida de un tipo de datos de propiedad concreto, vea:

-   [PROP \_ Type \_ void](/windows)
-   [\_Resumen de tipo de prop \_](/windows)
-   [tipo de PROP \_ \_ byte](/windows)
-   [PROP ( \_ tipo de \_ palabra)](/windows)
-   [PROP ( \_ tipo \_ DWORD)](/windows)
-   PROP \_ Type \_ LARGEINT (el formateador genérico no admite)
-   PROP \_ Type \_ addr (el formateador genérico no admite)
-   [\_hora del tipo de prop \_](/windows)
-   [PROP \_ Type ( \_ cadena)](/windows)
-   [PROP \_ Type \_ IP \_ Address](/windows)
-   PROP \_ Type \_ BYTESWAPPED \_ Word (obsoleto. Para obtener más información, vea [prop \_ Type \_ Word](/windows))
-   PROP \_ Type \_ BYTESWAPPED \_ DWORD (obsoleto. Para obtener más información, vea [prop \_ Type \_ DWORD](/windows))
-   Tipo de PROP \_ \_ cadena con tipo \_ (obsoleto)
-   [\_ \_ datos sin procesar de tipo prop \_](/windows)
-   [PROP ( \_ Comentario de tipo) \_](/windows)
-   PROP \_ Type \_ SRCFRIENDLYNAME (el formateador genérico no admite)
-   PROP \_ Type \_ DSTFRIENDLYNAME (el formateador genérico no admite)
-   PROP \_ Type \_ TOKENRING \_ Address (el formateador genérico no admite)
-   PROP \_ Type \_ FDDI \_ Address (el formateador genérico no admite)
-   \_ \_ Dirección Ethernet del tipo de Prop (el \_ formateador genérico no admite)
-   Identificador de objeto de tipo de PROP \_ (el \_ \_ formateador genérico no admite)
-   PROP \_ Type \_ \_ \_ (dirección IP) (el formateador genérico no admite)
-   PROP \_ Type \_ var \_ Len \_ Small \_ int (el formateador genérico no admite)

## <a name="prop_type_void-and-prop_type_comment"></a>PROP \_ Type \_ void y prop \_ Type \_ comment

En la tabla siguiente se muestra la salida de formato genérico para las propiedades de tipo de datos de tipo **\_ \_ void** y **prop \_ \_** Type.

En la columna de salida del formateador, el valor de los datos de la captura es XYZ.



| Calificador de propiedad            | Salida del formateador                                      |
|-------------------------------|-------------------------------------------------------|
| PROP \_ . \_ ninguno              | XYZ                                                   |
| PROPal \_ \_ Range             | XYZ                                                   |
| PROP \_ . \_          | Obsoletos                                              |
| PROPia con \_ \_ etiqueta \_ establecido      | XYZ                                                   |
| PROPia con la etiqueta de campo de \_ \_ \_ bits | Obsoleto. Para obtener más información, vea PROPness \_ \_ Flags. |
| PROPia \_ \_ const             | XYZ                                                   |
| marcas PROPn \_ \_             | XYZ                                                   |
| PROPy ( \_ \_ matriz)             | XYZ                                                   |



 

## <a name="prop_type_summary"></a>\_Resumen de tipo de prop \_

En la tabla siguiente se muestra la salida de formato genérico para las propiedades de tipo de datos de **\_ \_ Resumen de tipo prop** .

En la columna de salida de ejemplo, el valor de los datos de la captura es XYZ.



| Calificador de propiedad            | Salida de ejemplo                                        |
|-------------------------------|-------------------------------------------------------|
| PROP \_ . \_ ninguno              | XYZ                                                   |
| PROPal \_ \_ Range             | XYZ                                                   |
| PROP \_ . \_          | Obsoletos                                              |
| PROPia con \_ \_ etiqueta \_ establecido      | XYZ                                                   |
| PROPia con la etiqueta de campo de \_ \_ \_ bits | Obsoleto. Para obtener más información, vea PROPness \_ \_ Flags. |
| PROPia \_ \_ const             | XYZ                                                   |
| marcas PROPn \_ \_             | XYZ                                                   |
| PROPy ( \_ \_ matriz)             | XYZ                                                   |



 

## <a name="prop_type_byte"></a>tipo de PROP \_ \_ byte

En la tabla siguiente se muestra la salida de formato genérico para las propiedades de tipo de datos **\_ \_ byte de tipo prop** .

En la columna de salida de ejemplo, el valor de los datos de la captura es 10.



| Calificador de propiedad            | Salida de ejemplo                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------|
| PROP \_ . \_ ninguno              | 10 (0xA) "                                                                                                     |
| PROPal \_ \_ Range             | 10 (0xA) intervalo:(1 (0x1)-20 (0x14))                                                                          |
| PROPia \_ \_ set               | 10 (0xA) coincide con el valor establecido o<br/> 10 (0xA) valor de conjunto desconocido<br/>                                |
| PROP \_ . \_          | Obsoleto.                                                                                                     |
| PROPia con \_ \_ etiqueta \_ establecido      | Etiqueta correspondiente en un conjunto o un número de etiqueta.                                                                 |
| PROPia con la etiqueta de campo de \_ \_ \_ bits | Obsoleto. Para obtener más información, vea PROPness \_ \_ Flags.                                                        |
| PROPia \_ \_ const             | Ninguna salida. No se muestra ningún dato en el panel de detalles.                                                           |
| marcas PROPn \_ \_             | ....... 0 = etiqueta fuera de la cadena...... dimensional. = Etiqueta en la cadena..... 0.. = Etiqueta fuera de la cadena.... 1... = etiqueta en la cadena |
| PROPy ( \_ \_ matriz)             | 0A FF...                                                                                                     |



 

## <a name="prop_type_word"></a>PROP ( \_ tipo de \_ palabra)

En la tabla siguiente se muestra la salida de formato genérico para una propiedad de tipo de datos **\_ \_ Word de tipo prop** .

> [!Note]  
> En el caso de las propiedades DWORD de intercambio de bytes que no son de Intel, debe cambiar los datos a un formato de Intel. Para cambiar el formato, establezca el parámetro *IFlags* de la función de instancia de propiedad **Attach** IFLAG \_ intercambiada al asignar la instancia de la propiedad a una ubicación.

 

En la columna de salida de ejemplo, el valor de los datos de la captura es 10.



| Calificador de propiedad            | Salida de ejemplo                                                                                                                                                                                                                |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROP \_ . \_ ninguno              | 10 (0xA)                                                                                                                                                                                                                      |
| PROPal \_ \_ Range             | 10 (0xA) intervalo:(1 (0x1)-20 (0x14))                                                                                                                                                                                          |
| PROPia \_ \_ set               | 10 (0xA) coincide con el valor establecido o<br/> 10 (0xA) valor de conjunto desconocido<br/>                                                                                                                                                |
| PROP \_ . \_          | Obsoleto.                                                                                                                                                                                                                     |
| PROPia con \_ \_ etiqueta \_ establecido      | Etiqueta correspondiente en el conjunto o el número de etiqueta.                                                                                                                                                                               |
| PROPia con la etiqueta de campo de \_ \_ \_ bits | Obsoleto. Para obtener más información, vea PROPness \_ \_ Flags.                                                                                                                                                                        |
| PROPia \_ \_ const             | Ninguna salida. No se muestra ningún dato en el panel de detalles.                                                                                                                                                                           |
| marcas PROPn \_ \_             | ....... 0 = etiqueta fuera de la cadena...... 0,1. = Etiqueta fuera de la cadena..... 0.. = Etiqueta fuera de la cadena.... 0... = etiqueta fuera de la cadena... 0.... = etiqueta fuera de la cadena.. 1.... = Etiqueta en la cadena. 0...... = Etiqueta de la cadena 1....... = Etiqueta en la cadena |
| PROPy ( \_ \_ matriz)             | 000A ffff...                                                                                                                                                                                                                 |



 

## <a name="prop_type_dword"></a>PROP ( \_ tipo \_ DWORD)

En la tabla siguiente se muestra la salida de formato genérico para las propiedades de tipo de datos **\_ \_ DWORD de tipo prop** .

> [!Note]  
> En el caso de las propiedades DWORD de intercambio de bytes que no son de Intel, debe cambiar los datos a un formato de Intel. Para cambiar el formato, establezca el parámetro *IFlags* de la función de instancia de propiedad **Attach** IFLAG \_ intercambiada al asignar la instancia de la propiedad a una ubicación.

 

En la columna de salida de ejemplo, el valor de los datos de la captura es 10.



| Calificador de propiedad            | Salida de ejemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROP \_ . \_ ninguno              | 10 (0xA)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PROPal \_ \_ Range             | 10 (0xA) intervalo:(1 (0x1)-20 (0x14))                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| PROPia \_ \_ set               | 10 (0xA) coincide con el valor establecido o<br/> 10 (0xA) valor de conjunto desconocido<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| PROP \_ . \_          | Obsoleto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| PROPia con \_ \_ etiqueta \_ establecido      | Etiqueta correspondiente en el conjunto o el número de etiqueta.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROPia con la etiqueta de campo de \_ \_ \_ bits | Obsoleto. Para obtener más información, vea PROPness \_ \_ Flags.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| PROPia \_ \_ const             | Ninguna salida. No se muestra ningún dato en el panel de detalles.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| marcas PROPn \_ \_             | ............... 0 = etiqueta fuera de la cadena.............. 0,1. = Etiqueta fuera de la cadena............. 0.. = Etiqueta fuera de la cadena............ 0... = etiqueta fuera de la cadena........... 0.... = etiqueta fuera de la cadena.......... 0..... = Etiqueta fuera de la cadena......... 0...... = etiqueta fuera de la cadena........ 0....... = etiqueta de la cadena....... 0........ = Etiqueta fuera de la cadena...... 0......... = etiqueta fuera de la cadena..... 0.......... = etiqueta de la cadena.... 0........... = Etiqueta fuera de la cadena... 0............ = etiqueta fuera de la cadena.. 1....... la etiqueta en la cadena. 0..................................... = Etiqueta de la cadena 1........... = Etiqueta en la cadena |
| PROPy ( \_ \_ matriz)             | 0000000a FFFFFFFF...                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="prop_type_raw_data"></a>\_ \_ datos sin procesar de tipo prop \_

En la tabla siguiente se muestra la salida de formato genérico para una propiedad tipo de datos de **\_ \_ \_ datos sin formato de tipo prop** . Tenga en cuenta que la salida del formateador no muestra los datos sin procesar, pero muestra la etiqueta de la propiedad.



| Calificador de propiedad            | Salida del formateador |
|-------------------------------|------------------|
| PROP \_ . \_ ninguno              | Etiqueta de la propiedad.  |
| PROPal \_ \_ Range             | Etiqueta de la propiedad.  |
| PROP \_ . \_          | Etiqueta de la propiedad.  |
| PROPia con \_ \_ etiqueta \_ establecido      | Etiqueta de la propiedad.  |
| PROPia con la etiqueta de campo de \_ \_ \_ bits | Etiqueta de la propiedad.  |
| PROPia \_ \_ const             | Etiqueta de la propiedad.  |
| marcas PROPn \_ \_             | Etiqueta de la propiedad.  |
| PROPy ( \_ \_ matriz)             | Etiqueta de la propiedad.  |



 

## <a name="prop_type_time"></a>\_hora del tipo de prop \_

En la tabla siguiente se muestra la salida de formato genérico para una propiedad de tipo de datos de tipo **prop \_ \_ Time** . Tenga en cuenta que la salida con formato puede variar según el calificador de datos de la propiedad.

El formateador genérico llama a [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) para obtener una hora basada en el reloj del sistema del equipo local.



| Calificador de propiedad            | Salida del formateador                                            |
|-------------------------------|-------------------------------------------------------------|
| PROP \_ . \_ ninguno              | Muestra la hora del sistema en función del reloj del equipo local. |
| PROPal \_ \_ Range             | Muestra la hora del sistema en función del reloj del equipo local. |
| PROP \_ . \_          | Obsoleto.                                                   |
| PROPia con \_ \_ etiqueta \_ establecido      | Muestra la hora del sistema en función del reloj del equipo local. |
| PROPia con la etiqueta de campo de \_ \_ \_ bits | Obsoleto. Para obtener más información, vea PROPness \_ \_ Flags.      |
| PROPia \_ \_ const             | Muestra la hora del sistema en función del reloj del equipo local. |
| marcas PROPn \_ \_             | Muestra la hora del sistema en función del reloj del equipo local. |
| PROPy ( \_ \_ matriz)             | Muestra la hora del sistema en función del reloj del equipo local. |



 

## <a name="prop_type_string"></a>PROP \_ Type ( \_ cadena)

En la tabla siguiente se muestra la salida de formato genérico para las propiedades de tipo de datos de **\_ \_ cadena de tipo prop** . Tenga en cuenta que la salida del formateador puede variar según el calificador de datos de la propiedad.



| Calificador de propiedad            | Salida del formateador                                       |
|-------------------------------|--------------------------------------------------------|
| PROP \_ . \_ ninguno              | Cadena adjunta.                                       |
| PROPal \_ \_ Range             | Cadena adjunta.                                       |
| PROP \_ . \_          | Obsoleto.                                              |
| PROPia con \_ \_ etiqueta \_ establecido      | Cadena adjunta.                                       |
| PROPia con la etiqueta de campo de \_ \_ \_ bits | Obsoleto. Para obtener más información, vea PROPness \_ \_ Flags. |
| PROPia \_ \_ const             | Cadena adjunta.                                       |
| marcas PROPn \_ \_             | Cadena adjunta.                                       |
| PROPy ( \_ \_ matriz)             | Cadena adjunta.                                       |



 

## <a name="prop_type_ip_address"></a>PROP \_ Type \_ IP \_ Address

En la tabla siguiente se muestra la salida de formato genérico para las propiedades de tipo de datos de **\_ \_ \_ dirección IP de tipo prop** . Tenga en cuenta que la salida con formato puede variar según el calificador de datos de propiedad de la propiedad.

En la columna de salida de ejemplo, el valor de los datos de la captura es "129.65.100.2".



| Calificador de propiedad            | Salida de ejemplo                                         |
|-------------------------------|--------------------------------------------------------|
| PROP \_ . \_ ninguno              | 129.65.100.2                                           |
| PROPal \_ \_ Range             | 129.65.100.2                                           |
| PROP \_ . \_          | Obsoleto.                                              |
| PROPia con \_ \_ etiqueta \_ establecido      | 129.65.100.2                                           |
| PROPia con la etiqueta de campo de \_ \_ \_ bits | Obsoleto. Para obtener más información, vea PROPness \_ \_ Flags. |
| PROPia \_ \_ const             | 129.65.100.2                                           |
| marcas PROPn \_ \_             | 129.65.100.2                                           |
| PROPy ( \_ \_ matriz)             | 129.65.100.2                                           |



 

 

