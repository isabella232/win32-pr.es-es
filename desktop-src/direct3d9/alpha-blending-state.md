---
description: El valor alfa de un color controla su transparencia. La habilitación de la combinación alfa permite mezclar colores, materiales y texturas en una superficie con la transparencia en otra superficie.
ms.assetid: e8e925d5-262d-45c0-be9f-21c9a103d7b7
title: Estado de mezcla alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884ecad07fb9aefba08a0abbab92969937ec6361
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423391"
---
# <a name="alpha-blending-state-direct3d-9"></a>Estado de mezcla alfa (Direct3D 9)

El valor alfa de un color controla su transparencia. La habilitación de la combinación alfa permite mezclar colores, materiales y texturas en una superficie con la transparencia en otra superficie.

Para obtener más información, vea [combinación de texturas alfa (Direct3D 9)](alpha-texture-blending.md) y [combinación de texturas (Direct3D 9)](texture-blending.md).

Las aplicaciones escritas en C++ usan el estado de representación de [**\_ ALPHABLENDENABLE de D3DRS**](./d3drenderstatetype.md) para habilitar la combinación de transparencia alfa. La API de Direct3D permite muchos tipos de combinación alfa. Sin embargo, es importante tener en cuenta que es posible que el hardware 3D del usuario no admita todos los Estados de mezcla permitidos por Direct3D.

El tipo de combinación alfa que se realiza depende de los Estados de representación [**D3DRS \_ SRCBLEND**](./d3drenderstatetype.md) y **D3DRS \_ DESTBLEND** . Los Estados de mezcla de origen y destino se usan en pares. En el ejemplo de código siguiente se muestra cómo se establece el estado de Blend de origen en D3DBLEND \_ SRCCOLOR y el estado de Blend de destino se establece en D3DBLEND \_ INVSRCCOLOR.


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the source blend state.
d3dDevice->SetRenderState(D3DRS_SRCBLEND, D3DBLEND_SRCCOLOR);

// Set the destination blend state.

d3dDevice->SetRenderState(D3DRS_DESTBLEND, D3DBLEND_INVSRCCOLOR);
```



La modificación de los Estados de mezcla de origen y de destino puede dar la apariencia de los objetos emisor en una atmósfera de Foggy o suciedad. Por ejemplo, si la aplicación modela llamas, fuerza campos, vigas de plasma o objetos de umbrales similares en un entorno de Foggy, establezca los Estados de mezcla de origen y de destino en D3DBLEND \_ uno.

Otra aplicación de la combinación alfa es controlar la iluminación en una escena 3D, también denominada asignación ligera. Al establecer el estado de Blend de origen en D3DBLEND \_ cero y el estado de mezcla de destino en D3DBLEND \_ SRCALPHA se oscurece una escena según la información alfa de origen. El primitivo de origen se usa como mapa de luz que escala el contenido del búfer de fotogramas para oscurecerlo cuando sea necesario. Esto produce una asignación ligera monocroma.

Puede lograr la asignación de luz de color si establece el estado de la mezcla alfa de origen en D3DBLEND \_ cero y el estado de mezcla de destino en D3DBLEND \_ SRCCOLOR.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estados de representación](render-states.md)
</dt> </dl>

 

 
