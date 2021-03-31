---
description: 'Las plantillas definen cómo se interpreta el flujo de datos: los datos se modulan mediante la definición de plantilla. En esta sección se describen los siguientes aspectos de una plantilla y se proporciona una plantilla de ejemplo.'
ms.assetid: f84978a8-8315-4626-be68-f00f3a72e5ac
title: Plantillas (formato de archivo X, codificación de texto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fccec46e72a73bb5ed4434fd252595e1b072ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805192"
---
# <a name="templates-x-file-format-text-encoding"></a>Plantillas (formato de archivo X, codificación de texto)

Las plantillas definen cómo se interpreta el flujo de datos: los datos se modulan mediante la definición de plantilla. En esta sección se describen los siguientes aspectos de una plantilla y se proporciona una plantilla de ejemplo.

Hay una plantilla especial: la plantilla de encabezado. Se recomienda que cada aplicación defina una plantilla de encabezado y la use para definir información específica de la aplicación, como la información de versión. Si está presente, la API de formato de archivo. x Lee este encabezado. Si un miembro de marcas está disponible, se utiliza para determinar cómo se interpretan los datos siguientes. El miembro Flags, si está definido, debe ser un valor DWORD. Un bit está definido actualmente como bit 0. Si este bit está claro, los siguientes datos del archivo son binarios. Si se establece, los datos siguientes son texto. Puede usar varios objetos de datos de encabezado para cambiar entre el texto binario y el texto dentro del archivo.

## <a name="template-form-name-and-uuid"></a>Formulario de plantilla, nombre y UUID

Una plantilla tiene el formato siguiente.


```
template <template-name> {
<UUID>
    <member 1>;
...
    <member n>;
[restrictions]
}
```



El nombre de la plantilla es un nombre alfanumérico que puede incluir el carácter de subrayado ( \_ ). No debe comenzar con un dígito. El UUID es un identificador único universal formateado con el estándar de entorno de informática distribuida de Open Software Foundation y entre corchetes angulares (< >). Por ejemplo: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.

## <a name="template-members"></a>Miembros de plantilla

Los miembros de plantilla se componen de un tipo de datos con nombre seguido de un nombre opcional o una matriz de un tipo de datos con nombre. En la tabla siguiente se definen los tipos de datos primitivos válidos.



| Tipo    | Size                               |
|---------|------------------------------------|
| WORD    | 16 bits                            |
| DWORD   | 32 bits                            |
| FLOAT   | Float de IEEE                         |
| DOUBLE  | 64 bits                            |
| CHAR    | 8 bits                             |
| UCHAR   | 8 bits                             |
| BYTE    | 8 bits                             |
| STRING  | Cadena terminada en NULL             |
| CSTRING | Cadena de C con formato (no se admite) |
| UNICODE | Cadena Unicode (no se admite)     |



 

También se puede hacer referencia a tipos de datos adicionales definidos por plantillas encontradas anteriormente en el flujo de datos dentro de una definición de plantilla. No se permiten referencias adelantadas.

Cualquier tipo de datos válido se puede expresar como una matriz en la definición de plantilla. En el ejemplo siguiente se muestra la sintaxis básica.


```
array <data-type> <name>[<dimension-size>];
```



<> de tamaño de dimensión puede ser un entero o una referencia con nombre a otro miembro de plantilla cuyo valor se sustituirá. Las matrices pueden ser de n dimensiones, donde n viene determinado por el número de corchetes emparejados al final de la instrucción, como en el ejemplo siguiente.


```
array DWORD FixedHerd[24];
array DWORD Herd[nCows];
array FLOAT Matrix4x4[4][4];
```



## <a name="template-restrictions"></a>Restricciones de plantilla

Las plantillas pueden ser abiertas, cerradas o restringidas. Estas restricciones determinan qué tipos de datos pueden aparecer en la jerarquía inmediata de un objeto de datos definido por la plantilla. Una plantilla abierta no tiene restricciones, una plantilla cerrada rechaza todos los tipos de datos y una plantilla restringida permite una lista con nombre de tipos de datos.

La sintaxis para indicar una plantilla abierta es de tres puntos entre corchetes.


```
[ ... ]
```



Una lista separada por comas de tipos de datos con nombre seguido opcionalmente por su UUID entre corchetes indica una plantilla restringida.


```
[ { data-type [ UUID ] , } ... ]
```



La ausencia de una de las anteriores indica una plantilla cerrada.

## <a name="template-example"></a>Ejemplo de plantilla

A continuación se muestra una plantilla de ejemplo.


```
template Mesh {
<3D82AB44-62DA-11cf-AB39-0020AF71E433>
DWORD nVertices;
array Vector vertices[nVertices];
DWORD nFaces;
array MeshFace faces[nFaces];
 [ ... ]                // An open template
}
template Vector {
<3D82AB5E-62DA-11cf-AB39-0020AF71E433>
FLOAT x;
FLOAT y;
FLOAT z;
}                        // A closed template
template FileSystem {
<UUID>
STRING name;
[ Directory <UUID>, File <UUID> ]    // A restricted template
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación de texto](text-encoding.md)
</dt> </dl>

 

 



