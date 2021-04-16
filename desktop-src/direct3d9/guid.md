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
# <a name="guid-directx-9"></a><span data-ttu-id="8e761-103">GUID (DirectX 9)</span><span class="sxs-lookup"><span data-stu-id="8e761-103">Guid (DirectX 9)</span></span>

<span data-ttu-id="8e761-104">Define un GUID que se puede usar en otras plantillas.</span><span class="sxs-lookup"><span data-stu-id="8e761-104">Defines a GUID that can be used in other templates.</span></span>

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

<span data-ttu-id="8e761-105">Donde los parámetros forman el formato de almacenamiento binario para un GUID:</span><span class="sxs-lookup"><span data-stu-id="8e761-105">Where the parameters together form the binary storage format for a GUID:</span></span>

-   <span data-ttu-id="8e761-106">valor de datos de entero de 32 bits sin signo de Data1</span><span class="sxs-lookup"><span data-stu-id="8e761-106">data1 - 32-bit unsigned integer data value</span></span>
-   <span data-ttu-id="8e761-107">data2: valor de datos de entero sin signo de 16 bits</span><span class="sxs-lookup"><span data-stu-id="8e761-107">data2 - 16-bit unsigned integer data value</span></span>
-   <span data-ttu-id="8e761-108">valor de datos de entero de 16 bits sin signo de data3</span><span class="sxs-lookup"><span data-stu-id="8e761-108">data3 - 16-bit unsigned integer data value</span></span>
-   <span data-ttu-id="8e761-109">data4: una matriz de caracteres sin signo</span><span class="sxs-lookup"><span data-stu-id="8e761-109">data4 - An array of unsigned characters</span></span>

## <a name="see-also"></a><span data-ttu-id="8e761-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e761-110">See also</span></span>

<dl> <dt>

<span data-ttu-id="8e761-111">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="8e761-111">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



