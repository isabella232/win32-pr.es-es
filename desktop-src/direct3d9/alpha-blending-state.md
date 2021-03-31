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
# <a name="alpha-blending-state-direct3d-9"></a><span data-ttu-id="76196-104">Estado de mezcla alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="76196-104">Alpha Blending State (Direct3D 9)</span></span>

<span data-ttu-id="76196-105">El valor alfa de un color controla su transparencia.</span><span class="sxs-lookup"><span data-stu-id="76196-105">The alpha value of a color controls its transparency.</span></span> <span data-ttu-id="76196-106">La habilitación de la combinación alfa permite mezclar colores, materiales y texturas en una superficie con la transparencia en otra superficie.</span><span class="sxs-lookup"><span data-stu-id="76196-106">Enabling alpha blending allows colors, materials, and textures on a surface to be blended with transparency onto another surface.</span></span>

<span data-ttu-id="76196-107">Para obtener más información, vea [combinación de texturas alfa (Direct3D 9)](alpha-texture-blending.md) y [combinación de texturas (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="76196-107">For more information, see [Alpha Texture Blending (Direct3D 9)](alpha-texture-blending.md) and [Texture Blending (Direct3D 9)](texture-blending.md).</span></span>

<span data-ttu-id="76196-108">Las aplicaciones escritas en C++ usan el estado de representación de [**\_ ALPHABLENDENABLE de D3DRS**](./d3drenderstatetype.md) para habilitar la combinación de transparencia alfa.</span><span class="sxs-lookup"><span data-stu-id="76196-108">Applications written in C++ use the [**D3DRS\_ALPHABLENDENABLE**](./d3drenderstatetype.md) render state to enable alpha transparency blending.</span></span> <span data-ttu-id="76196-109">La API de Direct3D permite muchos tipos de combinación alfa.</span><span class="sxs-lookup"><span data-stu-id="76196-109">The Direct3D API allows many types of alpha blending.</span></span> <span data-ttu-id="76196-110">Sin embargo, es importante tener en cuenta que es posible que el hardware 3D del usuario no admita todos los Estados de mezcla permitidos por Direct3D.</span><span class="sxs-lookup"><span data-stu-id="76196-110">However, it is important to note the user's 3D hardware might not support all the blending states allowed by Direct3D.</span></span>

<span data-ttu-id="76196-111">El tipo de combinación alfa que se realiza depende de los Estados de representación [**D3DRS \_ SRCBLEND**](./d3drenderstatetype.md) y **D3DRS \_ DESTBLEND** .</span><span class="sxs-lookup"><span data-stu-id="76196-111">The type of alpha blending that is done depends on the [**D3DRS\_SRCBLEND**](./d3drenderstatetype.md) And **D3DRS\_DESTBLEND** render states.</span></span> <span data-ttu-id="76196-112">Los Estados de mezcla de origen y destino se usan en pares.</span><span class="sxs-lookup"><span data-stu-id="76196-112">Source and destination blend states are used in pairs.</span></span> <span data-ttu-id="76196-113">En el ejemplo de código siguiente se muestra cómo se establece el estado de Blend de origen en D3DBLEND \_ SRCCOLOR y el estado de Blend de destino se establece en D3DBLEND \_ INVSRCCOLOR.</span><span class="sxs-lookup"><span data-stu-id="76196-113">The following code example demonstrates how the source blend state is set to D3DBLEND\_SRCCOLOR and the destination blend state is set to D3DBLEND\_INVSRCCOLOR.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the source blend state.
d3dDevice->SetRenderState(D3DRS_SRCBLEND, D3DBLEND_SRCCOLOR);

// Set the destination blend state.

d3dDevice->SetRenderState(D3DRS_DESTBLEND, D3DBLEND_INVSRCCOLOR);
```



<span data-ttu-id="76196-114">La modificación de los Estados de mezcla de origen y de destino puede dar la apariencia de los objetos emisor en una atmósfera de Foggy o suciedad.</span><span class="sxs-lookup"><span data-stu-id="76196-114">Altering the source and destination blend states can give the appearance of emissive objects in a foggy or dusty atmosphere.</span></span> <span data-ttu-id="76196-115">Por ejemplo, si la aplicación modela llamas, fuerza campos, vigas de plasma o objetos de umbrales similares en un entorno de Foggy, establezca los Estados de mezcla de origen y de destino en D3DBLEND \_ uno.</span><span class="sxs-lookup"><span data-stu-id="76196-115">For instance, if your application models flames, force fields, plasma beams, or similarly radiant objects in a foggy environment, set the source and destination blend states to D3DBLEND\_ONE.</span></span>

<span data-ttu-id="76196-116">Otra aplicación de la combinación alfa es controlar la iluminación en una escena 3D, también denominada asignación ligera.</span><span class="sxs-lookup"><span data-stu-id="76196-116">Another application of alpha blending is to control the lighting in a 3D scene, also called light mapping.</span></span> <span data-ttu-id="76196-117">Al establecer el estado de Blend de origen en D3DBLEND \_ cero y el estado de mezcla de destino en D3DBLEND \_ SRCALPHA se oscurece una escena según la información alfa de origen.</span><span class="sxs-lookup"><span data-stu-id="76196-117">Setting the source blend state to D3DBLEND\_ZERO and the destination blend state to D3DBLEND\_SRCALPHA darkens a scene according to the source alpha information.</span></span> <span data-ttu-id="76196-118">El primitivo de origen se usa como mapa de luz que escala el contenido del búfer de fotogramas para oscurecerlo cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="76196-118">The source primitive is used as a light map that scales the contents of the frame buffer to darken it when appropriate.</span></span> <span data-ttu-id="76196-119">Esto produce una asignación ligera monocroma.</span><span class="sxs-lookup"><span data-stu-id="76196-119">This produces monochrome light mapping.</span></span>

<span data-ttu-id="76196-120">Puede lograr la asignación de luz de color si establece el estado de la mezcla alfa de origen en D3DBLEND \_ cero y el estado de mezcla de destino en D3DBLEND \_ SRCCOLOR.</span><span class="sxs-lookup"><span data-stu-id="76196-120">You can achieve color light mapping by setting the source alpha blending state to D3DBLEND\_ZERO and the destination blend state to D3DBLEND\_SRCCOLOR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76196-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76196-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76196-122">Estados de representación</span><span class="sxs-lookup"><span data-stu-id="76196-122">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
