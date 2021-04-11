---
description: La interpolación de vértices mezcla dos posiciones proporcionadas por el usuario (o normales).
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: Interpolación de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a5458e384fa69b91b1eab1623fb526d514591f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274731"
---
# <a name="vertex-tweening-direct3d-9"></a>Interpolación de vértices (Direct3D 9)

La interpolación de vértices mezcla dos posiciones proporcionadas por el usuario (o normales). La intercalación es mutuamente excluyente de la fusión de vértices con pesos. La intercalación se realiza antes de la iluminación y el recorte, y se habilita estableciendo D3DRS \_ VERTEXBLEND en D3DVBF \_ intercalación. La posición del vértice resultante se calcula mediante:


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



Se usa el mismo enfoque para calcular las normales. Para obtener más información, vea [usar la interpolación de vértices (Direct3D 9)](using-vertex-tweening.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación de geometría](geometry-blending.md)
</dt> </dl>

 

 



