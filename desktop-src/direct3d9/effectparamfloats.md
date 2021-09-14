---
description: Define números de punto flotante de efecto. Esta plantilla reemplaza a la plantilla EffectFloats.
ms.assetid: 7b41d0dc-209f-4ade-a7ed-aa54f421e520
title: EffectParamFloats
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0954ce7679691920c2e104277d12a48f7a34ddf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969688"
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

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



