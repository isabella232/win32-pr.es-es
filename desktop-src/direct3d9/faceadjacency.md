---
description: Se crea una instancia de esta plantilla por malla, que contiene información sobre qué vértices de la malla son duplicados entre sí.
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: FaceAdjacency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2fd0f0b2bb328aa8b5ec39e7481c0b7fd766fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805329"
---
# <a name="faceadjacency"></a>FaceAdjacency

Se crea una instancia de esta plantilla por malla, que contiene información sobre qué vértices de la malla son duplicados entre sí. Los duplicados se producen cuando un vértice se encuentra en un grupo de suavizado o en un límite de materiales. La finalidad de esta plantilla es permitir que el cargador determine qué vértices que presentan distintos parámetros periféricos son en realidad los mismos vértices en el modelo. Ciertas aplicaciones (por ejemplo, la simplificación de la malla) pueden hacer uso de esta información.

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

Donde:

-   nIndices: número de índices en la malla.
-   índices \[ nIndices \] : matriz de índices.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



