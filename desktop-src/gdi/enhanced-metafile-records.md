---
description: Un metarchivo mejorado es una matriz de registros.
ms.assetid: af3261c7-2113-4777-97c0-504f23022550
title: Registros de metarchivos mejorados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2097fd59497838c2a77a0209f6ae715dff2e1cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984970"
---
# <a name="enhanced-metafile-records"></a>Registros de metarchivos mejorados

Un metarchivo mejorado es una matriz de registros. Un registro de metarchivo es una estructura [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) de longitud variable. Al principio de cada registro de metarchivo mejorado se encuentra una estructura [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) , que contiene dos miembros. El primer miembro, iType, identifica el tipo de registro que es, la función GDI cuyos parámetros se incluyen en el registro. Dado que las estructuras son de longitud variable, el otro miembro, nSize, contiene el tamaño del registro. Inmediatamente después del miembro nSize se encuentran los parámetros restantes de la función GDI, si existen. El resto de la estructura contiene datos adicionales que dependen del tipo de registro.

El primer registro de un metarchivo mejorado siempre es la estructura [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) , que es el encabezado Enhanced-Metafile. El encabezado especifica la siguiente información:

-   Tamaño del metarchivo, en bytes
-   Dimensiones del marco de imagen, en unidades de dispositivo
-   Dimensiones del marco de imagen, en unidades. 01-milímetros
-   Número de registros del metarchivo
-   Desplazamiento a una descripción de texto opcional
-   Tamaño de la paleta opcional
-   Resolución del dispositivo original, en píxeles
-   Resolución del dispositivo original, en milímetros

Una descripción de texto opcional puede seguir el registro de encabezado. La descripción del texto describe la imagen y el nombre del autor. La paleta opcional especifica los colores usados para crear el metarchivo mejorado. Los registros restantes identifican las funciones GDI utilizadas para crear la imagen. La siguiente salida hexadecimal corresponde a un registro generado para una llamada a la función [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) .


```C++
00000011 0000000C 00000004 
```



El valor 0x00000011 especifica el tipo de registro (corresponde a la \_ constante SETMAPMODE de EMR definida en el archivo WinGDI. h). El valor 0x0000000C especifica la longitud del registro, en bytes. El valor 0x00000004 identifica el modo de asignación (corresponde a la \_ constante LOENGLISH de mm definida en la función [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) ).

Para obtener una lista de tipos de registros adicionales, vea [estructuras de metarchivo](metafile-structures.md).

 

 



