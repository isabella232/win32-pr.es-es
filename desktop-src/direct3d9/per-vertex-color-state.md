---
description: El motor de iluminación de Direct3D puede usar datos de color por vértice al realizar la iluminación si se le dice al tiempo de ejecución que los datos están presentes.
ms.assetid: acb43921-f0d4-4151-9371-1b99e5d30c0e
title: Per-Vertex de color (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6efd227c64785f7399ae3ba56d4623342c0910d901c3cfc404fc4a37f0d233
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727995"
---
# <a name="per-vertex-color-state-direct3d-9"></a>Per-Vertex de color (Direct3D 9)

El motor de iluminación de Direct3D puede usar datos de color por vértice al realizar la iluminación si se le dice al tiempo de ejecución que los datos están presentes. Para ello, se activará el siguiente estado de representación:


```
// disable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, FALSE);

// enable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, TRUE);
```



Si el color por vértice está habilitado, las aplicaciones pueden configurar el origen desde el que el sistema recupera información de color para un vértice. D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS EMISSIVEMATERIALSOURCE y D3DRS SPECULARMATERIALSOURCE representan los estados que controlan los orígenes de componentes de \_ \_ color ambiente, difuso, emisivo y especular, respectivamente. Cada estado se puede establecer en miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE,**](./d3dmaterialcolorsource.md) que define constantes que indiquen al sistema que use el material actual, el color difuso o el color especular como origen del componente de color especificado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar estados](render-states.md)
</dt> </dl>

 

 
