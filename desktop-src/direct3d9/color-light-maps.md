---
description: Normalmente, la aplicación representará escenas 3D de manera más realista si usa mapas de colores claros. Una asignación de luz en color utiliza los datos RGB en el mapa de luz para su información de iluminación.
ms.assetid: 47760884-7b9f-45de-9d4a-faf822da899f
title: Mapas de luz de color (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 621c5056fe2cbb9e6446adfb5dcad3079c0d90bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496133"
---
# <a name="color-light-maps-direct3d-9"></a><span data-ttu-id="b1d00-104">Mapas de luz de color (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b1d00-104">Color Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="b1d00-105">Normalmente, la aplicación representará escenas 3D de manera más realista si usa mapas de colores claros.</span><span class="sxs-lookup"><span data-stu-id="b1d00-105">Your application will usually render 3D scenes more realistically if it uses colored light maps.</span></span> <span data-ttu-id="b1d00-106">Una asignación de luz en color utiliza los datos RGB en el mapa de luz para su información de iluminación.</span><span class="sxs-lookup"><span data-stu-id="b1d00-106">A colored light map uses the RGB data in the light map for its lighting information.</span></span>

<span data-ttu-id="b1d00-107">En el ejemplo de código de C++ siguiente se muestra la asignación de luz con datos de color RGB.</span><span class="sxs-lookup"><span data-stu-id="b1d00-107">The following C++ code example demonstrates light mapping with RGB color data.</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains RGB light map data.

// Set the light map texture as the first texture.
d3dDevice->SetTexture(0, lptexLightMap);

d3dDevice->SetTextureStageState( 0,D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );
```



<span data-ttu-id="b1d00-108">En este ejemplo se establece el mapa de luz como la primera textura.</span><span class="sxs-lookup"><span data-stu-id="b1d00-108">This example sets the light map as the first texture.</span></span> <span data-ttu-id="b1d00-109">A continuación, establece el estado de la primera fase de mezcla para modular los datos de texturas entrantes.</span><span class="sxs-lookup"><span data-stu-id="b1d00-109">It then sets the state of the first blending stage to modulate the incoming texture data.</span></span> <span data-ttu-id="b1d00-110">Usa la primera textura y el color actual de la primitiva como argumentos para la operación modular.</span><span class="sxs-lookup"><span data-stu-id="b1d00-110">It uses the first texture and the current color of the primitive as the arguments to the modulate operation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1d00-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1d00-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1d00-112">Asignación de luz con texturas</span><span class="sxs-lookup"><span data-stu-id="b1d00-112">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



