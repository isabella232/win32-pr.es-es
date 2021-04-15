---
description: El mezclador de búfer de fotogramas ahora puede mezclar canales alfa independientes de la combinación de canales de color en destinos de representación. Este control se habilita con un nuevo estado de representación, D3DRS \_ SEPARATEALPHABLENDENABLE.
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: Alfa de destino de representación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70f395406559782172448b5555daff056ffd54c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536508"
---
# <a name="render-target-alpha-direct3d-9"></a>Alfa de destino de representación (Direct3D 9)

El mezclador de búfer de fotogramas ahora puede mezclar canales alfa independientes de la combinación de canales de color en destinos de representación. Este control se habilita con un nuevo estado de representación, D3DRS \_ SEPARATEALPHABLENDENABLE.

Cuando D3DRS \_ SEPARATEALPHABLENDENABLE se establece en **false** (que es la condición predeterminada), los factores de mezcla y las operaciones de destino de representación que se aplican a Alpha son los mismos que los definidos para combinar los canales de color. Un controlador debe establecer el límite de \_ SEPARATEALPHABLEND de D3DPMISCCAPS para indicar que puede admitir la combinación alfa de representación y destino. Asegúrese de habilitar D3DRS \_ ALPHABLEND para indicar a la canalización que se necesita la combinación alfa.

Para controlar los factores del canal alfa de los mezcladores de destino de representación, se definen dos nuevos Estados de representación de la siguiente manera:


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



Al igual que D3DRS \_ SRCBLEND y D3DRS \_ DESTBLEND, se pueden establecer en uno de los valores de la enumeración [**D3DBLEND**](./d3dblend.md) . La configuración de Blend de origen y de destino se puede combinar de varias maneras, dependiendo de la configuración de los miembros SrcBlendCaps y DestBlendCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

La combinación alfa se realiza de la siguiente manera:

renderTargetAlpha = (alpha<sub>en</sub> \* srcBlendOp) BlendOp (alpha<sub>RT</sub> \* destBlendOp)

Donde:

-   alfa es el valor alfa<sub>de</sub> entrada.
-   srcBlendOp es uno de los factores de mezcla de [**D3DBLEND**](./d3dblend.md).
-   BlendOp es uno de los factores de mezcla de [**D3DBLENDOP**](./d3dblendop.md).
-   alpha<sub>RT</sub> es el valor alfa de representación-destino.
-   destBlendOp es uno de los factores de mezcla de [**D3DBLEND**](./d3dblend.md).
-   renderTargetAlpha es el valor alfa mezclado final.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación alfa](alpha-blending.md)
</dt> </dl>

 

 
