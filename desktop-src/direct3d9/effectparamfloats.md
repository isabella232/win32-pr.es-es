---
description: Define los números de punto flotante de efecto. Esta plantilla reemplaza la plantilla EffectFloats.
ms.assetid: 7b41d0dc-209f-4ade-a7ed-aa54f421e520
title: EffectParamFloats
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0954ce7679691920c2e104277d12a48f7a34ddf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079949"
---
# <a name="effectparamfloats"></a>EffectParamFloats

Define los números de punto flotante de efecto. Esta plantilla reemplaza la plantilla [**EffectFloats**](effectfloats.md) .

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

-   ParamName: nombre de la matriz de floats.
-   nFloats: número de valores de punto flotante de la matriz.
-   Flota \[ nFloats \] : matriz de valores de punto flotante.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



