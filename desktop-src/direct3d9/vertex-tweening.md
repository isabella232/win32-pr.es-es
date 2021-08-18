---
description: La interpolación de vértices combina dos posiciones (o normales) proporcionadas por el usuario.
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: Interpolación de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8486f53e4eb1a3a003b15255baeb50d30f0ed205f4259625d7d66ba33e8274c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519226"
---
# <a name="vertex-tweening-direct3d-9"></a>Interpolación de vértices (Direct3D 9)

La interpolación de vértices combina dos posiciones (o normales) proporcionadas por el usuario. La interpolación es mutuamente excluyente de la combinación de vértices con pesos. La interpolación se realiza antes de la iluminación y el recorte, y se habilita estableciendo D3DRS \_ VERTEXBLEND en D3DVBF \_ TWEENING. La posición del vértice resultante se calcula mediante:


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



Se usa el mismo enfoque para calcular las normales. Para obtener más información, [vea Usar la interpolación de vértices (Direct3D 9).](using-vertex-tweening.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación de geometría](geometry-blending.md)
</dt> </dl>

 

 



