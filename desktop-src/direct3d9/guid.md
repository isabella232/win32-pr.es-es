---
description: Define un GUID que se puede usar en otras plantillas.
ms.assetid: dbfdd307-310f-4c80-b4aa-f16a81a9a372
title: Guid (DirectX 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e83e45d6e993153cf293a2ad55080c74f2e6049d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060641"
---
# <a name="guid-directx-9"></a>Guid (DirectX 9)

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

Donde los parámetros forman juntos el formato de almacenamiento binario para un GUID:

-   data1: valor de datos enteros de 32 bits sin signo
-   data2: valor de datos enteros de 16 bits sin signo
-   data3: valor de datos enteros de 16 bits sin signo
-   data4: una matriz de caracteres sin signo

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



