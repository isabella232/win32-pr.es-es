---
description: Algunas placas de aceleradores 3D anteriores no admiten la combinación de texturas mediante el valor alfa del píxel de destino.
ms.assetid: 77d3b9fd-3232-4955-9df2-d4763d3eed6f
title: Mapas de luz monocroma (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ca63c2e7bb3ed51f1c6c5184536aa51e0a11e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696070"
---
# <a name="monochrome-light-maps-direct3d-9"></a><span data-ttu-id="1df9b-103">Mapas de luz monocroma (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1df9b-103">Monochrome Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="1df9b-104">Algunas placas de aceleradores 3D anteriores no admiten la combinación de texturas mediante el valor alfa del píxel de destino.</span><span class="sxs-lookup"><span data-stu-id="1df9b-104">Some older 3D accelerator boards do not support texture blending using the alpha value of the destination pixel.</span></span> <span data-ttu-id="1df9b-105">Consulte [combinación de texturas alfa (Direct3D 9)](alpha-texture-blending.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="1df9b-105">See [Alpha Texture Blending (Direct3D 9)](alpha-texture-blending.md) for more information.</span></span> <span data-ttu-id="1df9b-106">Normalmente, estos adaptadores no admiten la combinación de texturas múltiples.</span><span class="sxs-lookup"><span data-stu-id="1df9b-106">These adapters also generally do not support multiple texture blending.</span></span> <span data-ttu-id="1df9b-107">Si la aplicación se ejecuta en un adaptador como este, puede usar la combinación de texturas Multipass para realizar la asignación de luz monocromática.</span><span class="sxs-lookup"><span data-stu-id="1df9b-107">If your application is running on an adapter such as this, it can use multipass texture blending to perform monochrome light mapping.</span></span>

<span data-ttu-id="1df9b-108">Para realizar la asignación de luz monocromática, una aplicación almacena la información de iluminación en los datos alfa de sus texturas de mapa ligero.</span><span class="sxs-lookup"><span data-stu-id="1df9b-108">To perform monochrome light mapping, an application stores the lighting information in the alpha data of its light map textures.</span></span> <span data-ttu-id="1df9b-109">La aplicación utiliza las capacidades de filtrado de texturas de Direct3D para realizar una asignación desde cada píxel de la imagen de primitiva a un textura correspondiente en el mapa de luz.</span><span class="sxs-lookup"><span data-stu-id="1df9b-109">The application uses the texture filtering capabilities of Direct3D to perform a mapping from each pixel in the primitive's image to a corresponding texel in the light map.</span></span> <span data-ttu-id="1df9b-110">Establece el factor de fusión de origen en el valor alfa del textura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1df9b-110">It sets the source blending factor to the alpha value of the corresponding texel.</span></span>

<span data-ttu-id="1df9b-111">En el ejemplo siguiente se muestra cómo una aplicación puede usar una textura como mapa de luz monocroma:</span><span class="sxs-lookup"><span data-stu-id="1df9b-111">The following example illustrates how an application can use a texture as a monochrome light map:</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains monochrome light map data.

// Set the light map texture as the current texture.
d3dDevice->SetTexture(0, lptexLightMap);

// Set the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_SELECTARG1);

// Set argument 1 to the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1,
                                D3DTA_TEXTURE | D3DTA_ALPHAREPLICATE);
```



<span data-ttu-id="1df9b-112">Dado que los adaptadores de pantalla que no admiten la combinación alfa de destino normalmente no admiten la combinación de texturas múltiples, este ejemplo establece el mapa de luz como la primera textura, que está disponible en todas las tarjetas aceleradoras 3D.</span><span class="sxs-lookup"><span data-stu-id="1df9b-112">Because display adapters that do not support destination alpha blending usually do not support multiple texture blending, this example sets the light map as the first texture, which is available on all 3D accelerator cards.</span></span> <span data-ttu-id="1df9b-113">El código de ejemplo establece la operación de color para que la fase de fusión de la textura mezcle los datos de textura con el color existente del primitivo.</span><span class="sxs-lookup"><span data-stu-id="1df9b-113">The sample code sets the color operation for the texture's blending stage to blend the texture data with the primitive's existing color.</span></span> <span data-ttu-id="1df9b-114">A continuación, selecciona la primera textura y el color existente del primitivo como los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="1df9b-114">It then selects the first texture and the primitive's existing color as the input data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1df9b-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1df9b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1df9b-116">Asignación de luz con texturas</span><span class="sxs-lookup"><span data-stu-id="1df9b-116">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



