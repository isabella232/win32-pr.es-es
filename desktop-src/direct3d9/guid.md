---
description: Define un GUID que se puede usar en otras plantillas.
ms.assetid: dbfdd307-310f-4c80-b4aa-f16a81a9a372
title: GUID (DirectX 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e83e45d6e993153cf293a2ad55080c74f2e6049d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537227"
---
# <a name="guid-directx-9"></a>GUID (DirectX 9)

Define un GUID que se puede usar en otras plantillas.

``` syntax
template Guid
{
    < a42790e0-7810-11cf-8f52-0040333594a3 >
    DWORD data1;
    WORD data2;
    WORD data3;
    array UCHAR data4[8];
} 
```

Donde los parámetros forman el formato de almacenamiento binario para un GUID:

-   valor de datos de entero de 32 bits sin signo de Data1
-   data2: valor de datos de entero sin signo de 16 bits
-   valor de datos de entero de 16 bits sin signo de data3
-   data4: una matriz de caracteres sin signo

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



