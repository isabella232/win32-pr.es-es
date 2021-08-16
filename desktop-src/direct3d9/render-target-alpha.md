---
description: Ahora, la mezcla de búfer de fotogramas puede combinar canales alfa independientemente de la combinación de canales de color en los destinos de representación. Este control está habilitado con un nuevo estado de representación, D3DRS \_ SEPARATEALPHABLENDENABLE.
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: Representar destino alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5d4701b2d09334d605cf2c90ef0e03b06ea7886ea875ce8ec8ff9cbc428ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797940"
---
# <a name="render-target-alpha-direct3d-9"></a>Representar destino alfa (Direct3D 9)

Ahora, la mezcla de búfer de fotogramas puede combinar canales alfa independientemente de la combinación de canales de color en los destinos de representación. Este control está habilitado con un nuevo estado de representación, D3DRS \_ SEPARATEALPHABLENDENABLE.

Cuando D3DRS \_ SEPARATEALPHABLENDENABLE se establece en **FALSE** (que es la condición predeterminada), los factores de combinación de destino de representación y las operaciones aplicadas a alfa son los mismos que los definidos para combinar canales de color. Un controlador debe establecer el límite D3DPMISCCAPS SEPARATEALPHABLEND para indicar que puede admitir la mezcla alfa de destino \_ de representación. Asegúrese de habilitar D3DRS ALPHABLEND para que le diga a la canalización que se necesita la \_ combinación alfa.

Para controlar los factores en el canal alfa de las mezclas render-target, se definen dos nuevos estados de representación de la siguiente manera:


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



Al igual que D3DRS \_ SRCBLEND y D3DRS DESTBLEND, se pueden establecer en uno de los valores de la enumeración \_ [**D3DBLEND.**](./d3dblend.md) La configuración de mezcla de origen y destino se puede combinar de varias maneras, dependiendo de la configuración de los miembros SrcBlendCaps y DestBlendCaps de [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

La combinación alfa se realiza de la siguiente manera:

renderTargetAlpha = (alpha<sub>in</sub> \* srcBlendOp) BlendOp (alpha<sub>rt</sub> \* destBlendOp)

Donde:

-   alpha<sub>in</sub> es el valor alfa de entrada.
-   srcBlendOp es uno de los factores de mezcla de [**D3DBLEND.**](./d3dblend.md)
-   BlendOp es uno de los factores de mezcla de [**D3DBLENDOP.**](./d3dblendop.md)
-   alpha<sub>rt</sub> es el valor alfa de destino de representación.
-   destBlendOp es uno de los factores de mezcla de [**D3DBLEND.**](./d3dblend.md)
-   renderTargetAlpha es el valor alfa combinado final.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación alfa](alpha-blending.md)
</dt> </dl>

 

 
