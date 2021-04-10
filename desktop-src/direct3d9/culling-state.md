---
description: Para mejorar el rendimiento de la representación, puede desechar (o quitar) un primitivo que se encuentre enfrente de la cámara.
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: Estado de selección (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86e71fd7c6543f0d232e32a630d73e0ebbadae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153250"
---
# <a name="culling-state-direct3d-9"></a>Estado de selección (Direct3D 9)

Para mejorar el rendimiento de la representación, puede desechar (o quitar) un primitivo que se encuentre enfrente de la cámara. En el caso de las primitivas de una sola cara, se ahorra tiempo de representación porque no está visible la cara posterior. Para habilitar el reactivado, debe conocer el orden de bobinado de los vértices (normalmente en el sentido contrario a las agujas del reloj). En este ejemplo se quitará cualquier primitiva cuya cara trasera esté mirando hacia delante (dado un orden de bobinado en el sentido contrario a las agujas del reloj):


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estados de representación](render-states.md)
</dt> </dl>

 

 



