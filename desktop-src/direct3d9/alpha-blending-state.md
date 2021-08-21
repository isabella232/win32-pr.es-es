---
description: El valor alfa de un color controla su transparencia. La habilitación de la mezcla alfa permite combinar colores, materiales y texturas de una superficie con transparencia en otra superficie.
ms.assetid: e8e925d5-262d-45c0-be9f-21c9a103d7b7
title: Estado de mezcla alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4bd012340fae9e7597479d846d18db37c32d6f95a42118ba7444ad63a2e1cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045213"
---
# <a name="alpha-blending-state-direct3d-9"></a>Estado de mezcla alfa (Direct3D 9)

El valor alfa de un color controla su transparencia. La habilitación de la mezcla alfa permite combinar colores, materiales y texturas de una superficie con transparencia en otra superficie.

Para obtener más información, vea [Alpha Texture Blending (Direct3D 9)](alpha-texture-blending.md) y [Texture Blending (Direct3D 9).](texture-blending.md)

Las aplicaciones escritas en C++ usan el estado de representación [**D3DRS \_ ALPHABLENDENABLE**](./d3drenderstatetype.md) para habilitar la combinación de transparencia alfa. La API de Direct3D permite muchos tipos de mezcla alfa. Sin embargo, es importante tener en cuenta que es posible que el hardware 3D del usuario no admita todos los estados de mezcla permitidos por Direct3D.

El tipo de combinación alfa que se realiza depende de los estados de representación [**D3DRS \_ SRCBLEND**](./d3drenderstatetype.md) y **D3DRS \_ DESTBLEND.** Los estados de mezcla de origen y destino se usan en pares. En el ejemplo de código siguiente se muestra cómo el estado de mezcla de origen se establece en D3DBLEND SRCCOLOR y el estado de mezcla de destino se establece en \_ D3DBLEND \_ INVSRCCOLOR.


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the source blend state.
d3dDevice->SetRenderState(D3DRS_SRCBLEND, D3DBLEND_SRCCOLOR);

// Set the destination blend state.

d3dDevice->SetRenderState(D3DRS_DESTBLEND, D3DBLEND_INVSRCCOLOR);
```



La modificación de los estados de combinación de origen y destino puede dar la apariencia de objetos emisivos en un ambiente desenlomendido o con mucha humedad. Por ejemplo, si la aplicación modela las llamas, fuerza campos, haces de calor u objetos similares en un entorno desenmascarado, establezca los estados de mezcla de origen y destino en D3DBLEND \_ ONE.

Otra aplicación de mezcla alfa es controlar la iluminación en una escena 3D, también denominada asignación de luz. Al establecer el estado de mezcla de origen en D3DBLEND ZERO y el estado de mezcla de destino en \_ D3DBLEND SRCALPHA, se oscuro una escena según la información \_ alfa de origen. La primitiva de origen se usa como un mapa claro que escala el contenido del búfer de fotogramas para oscuro cuando sea necesario. Esto genera una asignación de luz monocromática.

Puede lograr la asignación de luz de color estableciendo el estado de mezcla alfa de origen en D3DBLEND ZERO y el estado de mezcla de destino \_ en D3DBLEND \_ SRCCOLOR.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar estados](render-states.md)
</dt> </dl>

 

 
