---
description: Un metarchivo mejorado es una matriz de registros.
ms.assetid: af3261c7-2113-4777-97c0-504f23022550
title: Registros de metarchivo mejorados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2097fd59497838c2a77a0209f6ae715dff2e1cf9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474332"
---
# <a name="enhanced-metafile-records"></a>Registros de metarchivo mejorados

Un metarchivo mejorado es una matriz de registros. Un registro de metarchivo es una estructura [**ENHMETARECORD de**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) longitud variable. Al principio de cada registro de metarchivo mejorado hay una [**estructura DER,**](/windows/win32/api/wingdi/ns-wingdi-emr) que contiene dos miembros. El primer miembro, iType, identifica el tipo de registro, es decir, la función GDI cuyos parámetros están contenidos en el registro. Dado que las estructuras tienen una longitud variable, el otro miembro, nSize, contiene el tamaño del registro. Inmediatamente después del miembro nSize se encuentran los parámetros restantes, si existen, de la función GDI. El resto de la estructura contiene datos adicionales que dependen del tipo de registro.

El primer registro de un metarchivo mejorado es siempre la estructura [**ENHMETAHEADER,**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) que es el encabezado enhanced-metafile. El encabezado especifica la siguiente información:

-   Tamaño del metarchivo, en bytes
-   Dimensiones del marco de imagen, en unidades de dispositivo
-   Dimensiones del marco de imagen, en unidades de .01 milímetros
-   Número de registros del metarchivo
-   Desplazamiento a una descripción de texto opcional
-   Tamaño de la paleta opcional
-   Resolución del dispositivo original, en píxeles
-   Resolución del dispositivo original, en milímetros

Una descripción de texto opcional puede seguir el registro de encabezado. La descripción del texto describe la imagen y el nombre del autor. La paleta opcional especifica los colores usados para crear el metarchivo mejorado. Los registros restantes identifican las funciones GDI usadas para crear la imagen. La siguiente salida hexadecimal corresponde a un registro generado para una llamada a la [**función SetMapMode.**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)


```C++
00000011 0000000C 00000004 
```



El valor 0x00000011 especifica el tipo de registro (corresponde a la constante SETMAPMODE de EMR definida en el \_ archivo Wingdi.h). El valor 0x0000000C especifica la longitud del registro, en bytes. El valor 0x00000004 el modo de asignación (corresponde a la constante \_ MM LOENGLISH definida en la función [**SetMapMode).**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)

Para obtener una lista de tipos de registro adicionales, vea [Estructuras de metarchivo.](metafile-structures.md)

 

 



