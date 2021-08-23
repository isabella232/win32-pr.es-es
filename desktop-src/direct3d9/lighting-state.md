---
description: Si no se enciende con un sombreador de vértices o un sombreador de píxeles, puede optar por usar el motor de iluminación en tiempo de ejecución.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: Estado de iluminación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5935590c46776c621535968f4d457f3738d83d02342ffddf832cbf0278bbd9ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674275"
---
# <a name="lighting-state-direct3d-9"></a>Estado de iluminación (Direct3D 9)

Si no se enciende con un sombreador de vértices o un sombreador de píxeles, puede optar por usar el motor de iluminación en tiempo de ejecución. El motor de iluminación requiere que los datos del vértice contengan normales por vértice; Los vértices sin datos normales generarán un producto de punto cero en todos los cálculos de iluminación. Los cálculos de iluminación se tratan con más detalle en Matemáticas de iluminación [(Direct3D 9).](mathematics-of-lighting.md)

Para habilitar el motor de iluminación, use:


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar estados](render-states.md)
</dt> </dl>

 

 



