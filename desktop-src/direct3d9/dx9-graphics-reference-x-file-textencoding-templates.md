---
description: 'Las plantillas definen cómo se interpreta el flujo de datos: los datos se modularán mediante la definición de plantilla. En esta sección se analizan los siguientes aspectos de una plantilla y se proporciona una plantilla de ejemplo.'
ms.assetid: f84978a8-8315-4626-be68-f00f3a72e5ac
title: Plantillas (formato de archivo X, codificación de texto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e164b92c6c5738ad98b138941b1b2fda6c332068
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060654"
---
# <a name="templates-x-file-format-text-encoding"></a>Plantillas (formato de archivo X, codificación de texto)

Las plantillas definen cómo se interpreta el flujo de datos: los datos se modularán mediante la definición de plantilla. En esta sección se analizan los siguientes aspectos de una plantilla y se proporciona una plantilla de ejemplo.

Hay una plantilla especial: la plantilla de encabezado. Se recomienda que cada aplicación defina una plantilla de encabezado y la use para definir información específica de la aplicación, como la información de versión. Si está presente, la API de formato de archivo .x lee este encabezado. Si un miembro flags está disponible, se usa para determinar cómo se interpretan los datos siguientes. El miembro flags, si se define, debe ser DWORD. Un bit está definido actualmente: bit 0. Si este bit está claro, los siguientes datos del archivo son binarios. Si se establece, los datos siguientes son texto. Puede usar varios objetos de datos de encabezado para cambiar entre binario y texto dentro del archivo.

## <a name="template-form-name-and-uuid"></a>Formulario de plantilla, nombre y UUID

Una plantilla tiene el siguiente formulario.


```
template <template-name> {
<UUID>
    <member 1>;
...
    <member n>;
[restrictions]
}
```



El nombre de la plantilla es un nombre alfanumérico que puede incluir el carácter de subrayado ( \_ ). No debe comenzar con un dígito. El UUID es un identificador único universal con el formato estándar distributed Computing Environment de Open Software Foundation y entre corchetes angulares (< >). Por ejemplo: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.

## <a name="template-members"></a>Miembros de plantilla

Los miembros de plantilla constan de un tipo de datos con nombre seguido de un nombre opcional o una matriz de un tipo de datos con nombre. Los tipos de datos primitivos válidos se definen en la tabla siguiente.



| Tipo    | Size                               |
|---------|------------------------------------|
| WORD    | 16 bits                            |
| DWORD   | 32 bits                            |
| FLOAT   | IEEE float                         |
| DOUBLE  | 64 bits                            |
| CHAR    | 8 bits                             |
| UCHAR   | 8 bits                             |
| BYTE    | 8 bits                             |
| STRING  | Cadena terminada en NULL             |
| CSTRING | Cadena de C con formato (no compatible) |
| UNICODE | Cadena Unicode (no compatible)     |



 

También se puede hacer referencia a tipos de datos adicionales definidos por plantillas encontradas anteriormente en el flujo de datos dentro de una definición de plantilla. No se permiten referencias adelantadas.

Cualquier tipo de datos válido se puede expresar como una matriz en la definición de plantilla. La sintaxis básica se muestra en el ejemplo siguiente.


```
array <data-type> <name>[<dimension-size>];
```



&lt;dimension-size puede ser un entero o una referencia con nombre a otro miembro de plantilla &gt; cuyo valor se sustituya a continuación. Las matrices pueden ser n dimensionales, donde n viene determinado por el número de corchetes emparejados que se encuentra al final de la instrucción, como en el ejemplo siguiente.


```
array DWORD FixedHerd[24];
array DWORD Herd[nCows];
array FLOAT Matrix4x4[4][4];
```



## <a name="template-restrictions"></a>Restricciones de plantilla

Las plantillas se pueden abrir, cerrar o restringir. Estas restricciones determinan qué tipos de datos pueden aparecer en la jerarquía inmediata de un objeto de datos definido por la plantilla. Una plantilla abierta no tiene restricciones, una plantilla cerrada rechaza todos los tipos de datos y una plantilla restringida permite una lista con nombre de tipos de datos.

La sintaxis para indicar una plantilla abierta es de tres períodos entre corchetes.


```
[ ... ]
```



Una lista separada por comas de tipos de datos con nombre seguidos opcionalmente de sus UUID entre corchetes indica una plantilla restringida.


```
[ { data-type [ UUID ] , } ... ]
```



La ausencia de cualquiera de los elementos anteriores indica una plantilla cerrada.

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

 

 



