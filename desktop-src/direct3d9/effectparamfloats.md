---
description: Define números de punto flotante de efecto. Esta plantilla reemplaza a la plantilla EffectFloats.
ms.assetid: 7b41d0dc-209f-4ade-a7ed-aa54f421e520
title: EffectParamFloats
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f34f60c16f583021d0e7f01482941fa31d12861d4a59c07c26c7aa89a96e3d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122394"
---
# <a name="effectparamfloats"></a>EffectParamFloats

Define números de punto flotante de efecto. Esta plantilla reemplaza a la [**plantilla EffectFloats.**](effectfloats.md)

``` syntax
template EffectParamFloats
{
    < 3014B9A0-62F5-478c-9B86-E4AC9F4E418B >
    STRING ParamName;
    DWORD nFloats;
    array float Floats[nFloats];
} 
```

Donde:

-   ParamName: nombre de la matriz de elementos float.
-   nFloats: número de valores de punto flotante en la matriz.
-   Floats \[ nFloats: \] matriz de valores de punto flotante.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



