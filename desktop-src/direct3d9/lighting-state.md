---
description: Si no se enciende con un sombreador de vértices o un sombreador de píxeles, puede optar por usar el motor de iluminación en el tiempo de ejecución.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: Estado de iluminación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f0e7b7ec4a8bcf0ee27c9bc1e643536819d8fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705193"
---
# <a name="lighting-state-direct3d-9"></a>Estado de iluminación (Direct3D 9)

Si no se enciende con un sombreador de vértices o un sombreador de píxeles, puede optar por usar el motor de iluminación en el tiempo de ejecución. El motor de iluminación requiere que los datos del vértice contengan normales por vértice; los vértices sin datos normales generarán un producto DOT de cero en todos los cálculos de iluminación. Los cálculos de iluminación se describen con más detalle en [matemáticas de iluminación (Direct3D 9)](mathematics-of-lighting.md).

Para habilitar el motor de iluminación, use:


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estados de representación](render-states.md)
</dt> </dl>

 

 



