---
description: El motor de iluminación de Direct3D puede usar los datos de color por vértice al realizar la iluminación si se indica al tiempo de ejecución que los datos están presentes.
ms.assetid: acb43921-f0d4-4151-9371-1b99e5d30c0e
title: Per-Vertex estado de color (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0104b427753fa3d7b7cf5a0a5a10cfeb5d10f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422748"
---
# <a name="per-vertex-color-state-direct3d-9"></a>Per-Vertex estado de color (Direct3D 9)

El motor de iluminación de Direct3D puede usar los datos de color por vértice al realizar la iluminación si se indica al tiempo de ejecución que los datos están presentes. Esto se realiza activando el siguiente estado de representación:


```
// disable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, FALSE);

// enable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, TRUE);
```



Si el color por vértice está habilitado, las aplicaciones pueden configurar el origen desde el que el sistema recupera la información de color de un vértice. Los \_ Estados de representación D3DRS AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE y D3DRS \_ SPECULARMATERIALSOURCE controlan los orígenes de componentes de color ambiente, difuso, emisor y especular, respectivamente. Cada Estado se puede establecer en los miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) , que define las constantes que indican al sistema que utilice el material actual, el color difuso o el color especular como origen para el componente de color especificado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estados de representación](render-states.md)
</dt> </dl>

 

 
