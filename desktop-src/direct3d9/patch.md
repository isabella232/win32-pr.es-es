---
description: Define un control B&\# 233;zier. La matriz define los puntos de control para la revisión.
ms.assetid: vs|directx_sdk|~\patch.htm
title: Revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f57ac0cec68a1e8d1651c0e6ad2aabde6f1f6b949b085aa0dc35bd6e02c82a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118644"
---
# <a name="patch"></a>Revisión

Define una revisión de control de Bézier. La matriz define los puntos de control para la revisión.

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
-   array DWORD controlIndices \[ nControlIndices: \] matriz de índices de punto de control.

El tipo de revisión se define por el número de puntos de control, como se muestra en la tabla siguiente.



| Número de puntos de control | Tipo                              |
|--------------------------|-----------------------------------|
| 10                       | Revisión triangular de Bézier cúbica     |
| 15                       | Revisión triangular de Bézier cuartico   |
| 16                       | Revisión de rectángulo cuadrado de Bézier cúbica |



 

El orden de los puntos de control se indica en un patrón de patrón de patrón, como se muestra en los diagramas siguientes para las revisiones triangulares y rectangulares.

Las revisiones triangulares usan el siguiente patrón.

![diagrama del patrón para las revisiones triangulares](images/tripatch.png)

Las revisiones rectangulares usan el siguiente patrón.

![diagrama del patrón para revisiones rectangulares](images/quadpatch.png)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



