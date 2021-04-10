---
description: Define una revisión de \# control de Bézier B&233;. La matriz define los puntos de control para la revisión.
ms.assetid: vs|directx_sdk|~\patch.htm
title: Revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480457b3dd3800aca8b23210e3fe653b4e713e94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906327"
---
# <a name="patch"></a>Revisión

Define una revisión de control Bezier. La matriz define los puntos de control para la revisión.

``` syntax
template Patch
{
    < A3EB5D44-FC22-429D-9AFB-3221CB9719A6 >
    DWORD nControlIndices;
    array DWORD controlIndices[nControlIndices];
} 
```

Donde:

-   nControlIndices: número de índices de punto de control.
-   array DWORD controlIndices \[ nControlIndices \] : matriz de índices de punto de control.

El tipo de revisión se define por el número de puntos de control, como se muestra en la tabla siguiente.



| Número de puntos de control | Tipo                              |
|--------------------------|-----------------------------------|
| 10                       | Revisión triangular Bézier cúbica     |
| 15                       | Revisión triangular de Bézier de cuartil   |
| 16                       | Revisión Bézier cúbica de rectángulo cuádruple |



 

El orden de los puntos de control se proporciona en un patrón de espiral, tal como se muestra en los diagramas siguientes para las revisiones triangulares y rectangulares.

Las revisiones triangulares usan el siguiente patrón.

![diagrama del patrón para las revisiones triangulares](images/tripatch.png)

Las revisiones rectangulares usan el siguiente patrón.

![diagrama del patrón para las revisiones rectangulares](images/quadpatch.png)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



