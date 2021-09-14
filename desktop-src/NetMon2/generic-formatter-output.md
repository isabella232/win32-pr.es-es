---
description: Las listas y tablas de esta sección muestran la salida del formateador genérico. Tenga en cuenta que el formateador genérico usa los miembros DataType y DataQualifier de la estructura PROPERTYINFO para determinar cómo dar formato a los datos mostrados.
ms.assetid: cf3dc6cd-7b24-464a-9d2b-5e35c4e8825e
title: Salida de formateador genérico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf4b334dd717c7ff332c3b730afb57d4be611ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171490"
---
# <a name="generic-formatter-output"></a>Salida de formateador genérico

Las listas y tablas de esta sección muestran la salida del [*formateador genérico*](g.md). Tenga en cuenta que el formateador genérico usa los miembros **DataType** y **DataQualifier** de la [**estructura PROPERTYINFO**](propertyinfo.md) para determinar cómo dar formato a los datos mostrados.

Para obtener más información y un ejemplo de la salida de un tipo de datos de propiedad específico, vea:

-   [PROP \_ TYPE \_ VOID](/windows)
-   [RESUMEN \_ DE TIPO \_ PROP](/windows)
-   [BYTE \_ DE TIPO \_ PROP](/windows)
-   [PROP \_ TYPE \_ WORD](/windows)
-   [PROP \_ TYPE \_ DWORD](/windows)
-   PROP \_ TYPE \_ LARGEINT (el formateador genérico no admite)
-   PROP \_ TYPE \_ ADDR (el formateador genérico no admite)
-   [PROP \_ TYPE \_ TIME](/windows)
-   [PROP \_ TYPE \_ STRING](/windows)
-   [DIRECCIÓN \_ IP DE TIPO \_ PROP \_](/windows)
-   PROP \_ TYPE \_ BYTESWAPPED \_ WORD (Obsoleto. Para obtener más información, vea [PROP \_ TYPE \_ WORD](/windows))
-   TIPO \_ PROP \_ BYTESWAPPED \_ DWORD (obsoleto. Para obtener más información, [vea PROP \_ TYPE \_ DWORD](/windows))
-   PROP \_ TYPE \_ TYPED STRING \_ (obsoleto)
-   [DATOS SIN \_ \_ PROCESAR DE TIPO \_ PROP](/windows)
-   [COMENTARIO \_ DE TIPO \_ PROP](/windows)
-   PROP \_ TYPE \_ SRCFRIENDLYNAME (el formateador genérico no admite)
-   PROP \_ TYPE \_ DSTFRIENDLYNAME (el formateador genérico no admite)
-   PROP \_ TYPE \_ TOKENRING ADDRESS \_ (el formateador genérico no admite)
-   PROP \_ TYPE \_ FDDI ADDRESS \_ (el formateador genérico no admite)
-   PROP \_ TYPE ETHERNET ADDRESS \_ \_ (el formateador genérico no admite)
-   PROP \_ TYPE OBJECT IDENTIFIER \_ \_ (el formateador genérico no admite)
-   PROP \_ TYPE \_ SARS IP ADDRESS \_ \_ (el formateador genérico no admite)
-   PROP \_ TYPE \_ VAR \_ LEN SMALL INT \_ \_ (el formateador genérico no admite)

## <a name="prop_type_void-and-prop_type_comment"></a>PROP \_ TYPE VOID y PROP TYPE \_ \_ \_ COMMENT

En la tabla siguiente se muestra la salida de formato genérico para las propiedades de tipo de datos **PROP \_ TYPE \_ VOID** **y PROP TYPE \_ \_ COMMENT.**

En la columna de salida del formateador, el valor de los datos de la captura es XYZ.



| Calificador de propiedad            | Salida del formateador                                      |
|-------------------------------|-------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | XYZ                                                   |
| PROP \_ QUAL \_ RANGE             | XYZ                                                   |
| CAMPO DE \_ BITS DE PROP QUAL \_          | Obsoletos                                              |
| PROP \_ QUAL \_ LABELED \_ SET      | XYZ                                                   |
| CAMPO \_ DE BITS CON ETIQUETA \_ PROP QUAL \_ | Obsoleto. Para más información, consulte PROP \_ QUAL \_ FLAGS |
| PROP \_ QUAL \_ CONST             | XYZ                                                   |
| MARCAS \_ DE PROP \_ QUAL             | XYZ                                                   |
| PROP \_ QUAL \_ ARRAY             | XYZ                                                   |



 

## <a name="prop_type_summary"></a>RESUMEN \_ DE TIPO \_ PROP

En la tabla siguiente se muestra la salida de formato genérico para las propiedades del tipo de datos **\_ PROP TYPE \_ SUMMARY.**

En la columna de salida de ejemplo, el valor de los datos de la captura es XYZ.



| Calificador de propiedad            | Salida de ejemplo                                        |
|-------------------------------|-------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | XYZ                                                   |
| PROP \_ QUAL \_ RANGE             | XYZ                                                   |
| CAMPO DE \_ BITS DE PROP QUAL \_          | Obsoletos                                              |
| PROP \_ QUAL \_ LABELED \_ SET      | XYZ                                                   |
| CAMPO \_ DE BITS CON ETIQUETA \_ PROP QUAL \_ | Obsoleto. Para más información, consulte PROP \_ QUAL \_ FLAGS |
| PROP \_ QUAL \_ CONST             | XYZ                                                   |
| MARCAS \_ DE PROP \_ QUAL             | XYZ                                                   |
| PROP \_ QUAL \_ ARRAY             | XYZ                                                   |



 

## <a name="prop_type_byte"></a>BYTE \_ DE TIPO \_ PROP

En la tabla siguiente se muestra la salida de formato genérico para las propiedades del tipo de **\_ datos BYTE \_ PROP TYPE.**

En la columna de salida de ejemplo, el valor de los datos de la captura es 10.



| Calificador de propiedad            | Salida de ejemplo                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | 10 (0xa)"                                                                                                     |
| PROP \_ QUAL \_ RANGE             | Intervalo de 10 (0xa): (1 (0x1) - 20 (0x14))                                                                          |
| PROP \_ QUAL \_ SET               | 10 (0xa) coincide con el valor establecido o<br/> 10 (0xa) Valor de conjunto desconocido<br/>                                |
| CAMPO DE \_ BITS DE PROP QUAL \_          | Obsoleto.                                                                                                     |
| PROP \_ QUAL \_ LABELED \_ SET      | Etiqueta correspondiente en un conjunto de etiquetas o número.                                                                 |
| CAMPO \_ DE BITS CON ETIQUETA \_ PROP QUAL \_ | Obsoleto. Para obtener más información, vea PROP \_ QUAL \_ FLAGS.                                                        |
| PROP \_ QUAL \_ CONST             | Sin salida. No se muestra ningún dato en el panel de detalles.                                                           |
| MARCAS \_ DE PROP \_ QUAL             | ....... 0 = Etiquetar cadena desactivada ...... 1. = Etiqueta en la cadena ...... 0.. = Etiquetar cadena desactivada... 1... = Etiqueta en cadena |
| PROP \_ QUAL \_ ARRAY             | 0a ff ...                                                                                                     |



 

## <a name="prop_type_word"></a>PROP \_ TYPE \_ WORD

En la tabla siguiente se muestra la salida de formato genérico para una **propiedad de tipo de datos PROP TYPE \_ \_ WORD.**

> [!Note]  
> En el caso de las propiedades DWORD que no son intel y intercambiadas por bytes, debe cambiar los datos a un formato Intel. Para cambiar el formato, establezca el parámetro *IFlags* de la función de instancia de propiedad **Attach** IFLAG SWAPPED al asignar la instancia de \_ propiedad a una ubicación.

 

En la columna de salida de ejemplo, el valor de los datos de la captura es 10.



| Calificador de propiedad            | Salida de ejemplo                                                                                                                                                                                                                |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | 10 (0xa)                                                                                                                                                                                                                      |
| PROP \_ QUAL \_ RANGE             | Intervalo de 10 (0xa): (1 (0x1) - 20 (0x14))                                                                                                                                                                                          |
| PROP \_ QUAL \_ SET               | 10 (0xa) coincide con el valor establecido o<br/> 10 (0xa) Valor de conjunto desconocido<br/>                                                                                                                                                |
| CAMPO DE \_ BITS DE PROP QUAL \_          | Obsoleto.                                                                                                                                                                                                                     |
| PROP \_ QUAL \_ LABELED \_ SET      | Etiqueta correspondiente en el conjunto de etiquetas o número.                                                                                                                                                                               |
| CAMPO \_ DE BITS CON LA ETIQUETA \_ PROP QUAL \_ | Obsoleto. Para obtener más información, vea PROP \_ QUAL \_ FLAGS.                                                                                                                                                                        |
| PROP \_ QUAL \_ CONST             | Sin salida. No se muestra ningún dato en el panel de detalles.                                                                                                                                                                           |
| MARCAS \_ DE PROP QUAL \_             | ....... 0 = Etiquetar cadena desactivada ...... 0. = Etiquetar cadena desactivada ...... 0.. = Etiquetar cadena desactivada... 0... = Etiquetar cadena desactivada... 0.... = Etiquetar cadena desactivada . 1..... = Etiqueta en la cadena .0...... = Etiqueta desactivada Cadena 1...... = Etiqueta en cadena |
| PROP \_ QUAL \_ ARRAY             | 000a ffff ...                                                                                                                                                                                                                 |



 

## <a name="prop_type_dword"></a>TIPO \_ DE \_ PROP DWORD

En la tabla siguiente se muestra la salida de formato genérico para las propiedades del tipo de datos **\_ PROP TYPE \_ DWORD.**

> [!Note]  
> En el caso de las propiedades DWORD que no son intel y intercambiadas por bytes, debe cambiar los datos a un formato Intel. Para cambiar el formato, establezca el parámetro *IFlags* de la función de instancia de propiedad **Attach** IFLAG SWAPPED al asignar la instancia de \_ propiedad a una ubicación.

 

En la columna de salida de ejemplo, el valor de los datos de la captura es 10.



| Calificador de propiedad            | Salida de ejemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | 10 (0xa)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PROP \_ QUAL \_ RANGE             | Intervalo de 10 (0xa): (1 (0x1) - 20 (0x14))                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| PROP \_ QUAL \_ SET               | 10 (0xa) coincide con el valor establecido o<br/> 10 (0xa) Valor de conjunto desconocido<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| CAMPO DE \_ BITS DE PROP QUAL \_          | Obsoleto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| PROP \_ QUAL \_ LABELED \_ SET      | Etiqueta correspondiente en el número o conjunto de etiquetas.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| CAMPO \_ DE BITS CON LA ETIQUETA \_ PROP QUAL \_ | Obsoleto. Para obtener más información, vea PROP \_ QUAL \_ FLAGS.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| PROP \_ QUAL \_ CONST             | Sin salida. No se muestra ningún dato en el panel de detalles.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| MARCAS \_ DE PROP QUAL \_             | ............... 0 = Etiquetar cadena desactivada ............... 0. = Etiquetar cadena desactivada .................. 0.. = Etiquetar cadena desactivada ............ 0... = Etiquetar cadena desactivada ............ 0.... = Etiquetar cadena desactivada ............. 0..... = Etiquetar cadena desactivada ......... 0...... = Etiquetar cadena desactivada ......... 0....... = Etiquetar cadena desactivada ...... 0........ = Etiquetar cadena desactivada ...... 0......... = Etiquetar cadena desactivada ..... 0.......... = Etiquetar cadena desactivada ...... 0........... = Etiquetar cadena desactivada... 0............ = Etiquetar cadena desactivada . 1.................. = Etiqueta en la cadena .0................ = Etiquetar cadena desactivada 1............... = Etiqueta en cadena |
| PROP \_ QUAL \_ ARRAY             | 0000000a ffffffff ...                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="prop_type_raw_data"></a>DATOS \_ SIN PROCESAR DE TIPO \_ \_ PROP

En la tabla siguiente se muestra la salida de formato genérico para una propiedad de tipo de **datos PROP TYPE RAW \_ \_ \_ DATA.** Tenga en cuenta que la salida del formateador no muestra los datos sin procesar, pero muestra la etiqueta de propiedad.



| Calificador de propiedad            | Salida del formateador |
|-------------------------------|------------------|
| PROP \_ QUAL \_ NONE              | Etiqueta de propiedad.  |
| PROP \_ QUAL \_ RANGE             | Etiqueta de propiedad.  |
| CAMPO DE \_ BITS DE PROP QUAL \_          | Etiqueta de propiedad.  |
| PROP \_ QUAL \_ LABELED \_ SET      | Etiqueta de propiedad.  |
| CAMPO \_ DE BITS CON LA ETIQUETA \_ PROP QUAL \_ | Etiqueta de propiedad.  |
| PROP \_ QUAL \_ CONST             | Etiqueta de propiedad.  |
| MARCAS \_ DE PROP QUAL \_             | Etiqueta de propiedad.  |
| PROP \_ QUAL \_ ARRAY             | Etiqueta de propiedad.  |



 

## <a name="prop_type_time"></a>HORA \_ DEL TIPO DE \_ PROP

En la tabla siguiente se muestra la salida de formato genérico para una propiedad de tipo de datos **\_ PROP TYPE \_ TIME.** Tenga en cuenta que la salida con formato puede variar en función del calificador de datos de la propiedad .

El formateador genérico llama a [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) para obtener una hora que se basa en el reloj del sistema del equipo local.



| Calificador de propiedad            | Salida del formateador                                            |
|-------------------------------|-------------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | Muestra la hora del sistema según el reloj del equipo local. |
| PROP \_ QUAL \_ RANGE             | Muestra la hora del sistema según el reloj del equipo local. |
| CAMPO DE \_ BITS DE PROP QUAL \_          | Obsoleto.                                                   |
| PROP \_ QUAL \_ LABELED \_ SET      | Muestra la hora del sistema según el reloj del equipo local. |
| CAMPO \_ DE BITS CON LA ETIQUETA \_ PROP QUAL \_ | Obsoleto. Para obtener más información, vea PROP \_ QUAL \_ FLAGS.      |
| PROP \_ QUAL \_ CONST             | Muestra la hora del sistema según el reloj del equipo local. |
| MARCAS \_ DE PROP QUAL \_             | Muestra la hora del sistema según el reloj del equipo local. |
| PROP \_ QUAL \_ ARRAY             | Muestra la hora del sistema según el reloj del equipo local. |



 

## <a name="prop_type_string"></a>PROP \_ TYPE \_ STRING

En la tabla siguiente se muestra la salida de formato genérico para las propiedades del tipo de datos **\_ PROP TYPE \_ STRING.** Tenga en cuenta que la salida del formateador puede variar en función del calificador de datos de la propiedad .



| Calificador de propiedad            | Salida del formateador                                       |
|-------------------------------|--------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | Cadena adjunta.                                       |
| PROP \_ QUAL \_ RANGE             | Cadena adjunta.                                       |
| CAMPO DE \_ BITS DE PROP QUAL \_          | Obsoleto.                                              |
| PROP \_ QUAL \_ LABELED \_ SET      | Cadena adjunta.                                       |
| CAMPO \_ DE BITS CON LA ETIQUETA \_ PROP QUAL \_ | Obsoleto. Para obtener más información, vea PROP \_ QUAL \_ FLAGS. |
| PROP \_ QUAL \_ CONST             | Cadena adjunta.                                       |
| MARCAS \_ DE PROP QUAL \_             | Cadena adjunta.                                       |
| PROP \_ QUAL \_ ARRAY             | Cadena adjunta.                                       |



 

## <a name="prop_type_ip_address"></a>DIRECCIÓN \_ IP DEL TIPO DE \_ \_ PROP

En la tabla siguiente se muestra la salida de formato genérico para las propiedades del tipo de datos **\_ PROP TYPE IP \_ \_ ADDRESS.** Tenga en cuenta que la salida con formato puede variar en función del calificador de datos de propiedad de la propiedad.

En la columna de salida de ejemplo, el valor de los datos de la captura es "129.65.100.2".



| Calificador de propiedad            | Salida de ejemplo                                         |
|-------------------------------|--------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | 129.65.100.2                                           |
| PROP \_ QUAL \_ RANGE             | 129.65.100.2                                           |
| CAMPO DE \_ BITS DE PROP QUAL \_          | Obsoleto.                                              |
| PROP \_ QUAL \_ LABELED \_ SET      | 129.65.100.2                                           |
| CAMPO \_ DE BITS CON LA ETIQUETA \_ PROP QUAL \_ | Obsoleto. Para obtener más información, vea PROP \_ QUAL \_ FLAGS. |
| PROP \_ QUAL \_ CONST             | 129.65.100.2                                           |
| MARCAS \_ DE PROP QUAL \_             | 129.65.100.2                                           |
| PROP \_ QUAL \_ ARRAY             | 129.65.100.2                                           |



 

 

