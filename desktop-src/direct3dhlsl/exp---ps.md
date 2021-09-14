---
title: exp - ps
description: Proporciona una precisión total exponencial de 2x. | exp - ps
ms.assetid: 09e4446f-4149-4ec8-b3e3-2045b55bd591
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acd7c50c1f0d6ff08ee5d66e50fdd3e56939f0d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974676"
---
# <a name="exp---ps"></a>exp - ps

Proporciona una precisión total exponencial de 2<sup>x</sup>.

## <a name="syntax"></a>Sintaxis



| exp dst, src |
|--------------|



 

, donde

-   dst es el registro de destino.
-   src es un registro de origen. El registro de origen requiere el uso explícito de replicate swzzle; Es decir, se debe especificar exactamente uno de los componentes .x, .y, .z, .w swzzle (o .r, .g, .b, .a equivalentes). Consulte [Source Register Swlingling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| exp                   |      |      |      |      | x    | x    | x     | x    | x     |



 

El fragmento de código siguiente muestra las operaciones realizadas:


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




