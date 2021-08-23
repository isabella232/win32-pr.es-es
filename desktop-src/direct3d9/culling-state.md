---
description: Para mejorar el rendimiento de la representación, puede quitar (o quitar) una primitiva que se aleje de la cámara.
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: Estado de la selección (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bf9d8ed8ecea46dcfee146784dc97a38e42f0261b8f78bfc9d45ffaf99ddd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608035"
---
# <a name="culling-state-direct3d-9"></a>Estado de la selección (Direct3D 9)

Para mejorar el rendimiento de la representación, puede quitar (o quitar) una primitiva que se aleje de la cámara. En el caso de las primitivas de una sola cara, esto ahorra tiempo de representación porque una cara posterior no está visible. Para habilitar la selección, debe conocer el orden de los vértices (normalmente en sentido contrario a las agujas del reloj). En este ejemplo se quitará cualquier primitivo cuya cara posterior esté orientada hacia delante (dado un orden de sinuoso en el sentido contrario a las agujas del reloj):


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar estados](render-states.md)
</dt> </dl>

 

 



