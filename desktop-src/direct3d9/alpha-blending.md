---
description: Obtenga información sobre la combinación alfa. La combinación alfa se usa para mostrar una imagen que tiene píxeles transparentes o semitransparentes.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Combinación alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd79c622778e17c5acb9b17d52b6d5db278b1508
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262007"
---
# <a name="alpha-blending-direct3d-9"></a><span data-ttu-id="1cf9b-104">Combinación alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1cf9b-104">Alpha Blending (Direct3D 9)</span></span>

<span data-ttu-id="1cf9b-105">La combinación alfa se usa para mostrar una imagen que tiene píxeles transparentes o semitransparentes.</span><span class="sxs-lookup"><span data-stu-id="1cf9b-105">Alpha blending is used to display an image that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="1cf9b-106">Además de un canal de color rojo, verde y azul, cada píxel de un mapa de bits alfa tiene un componente de transparencia conocido como su canal alfa.</span><span class="sxs-lookup"><span data-stu-id="1cf9b-106">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its alpha channel.</span></span> <span data-ttu-id="1cf9b-107">El canal alfa normalmente contiene tantos bits como un canal de color.</span><span class="sxs-lookup"><span data-stu-id="1cf9b-107">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="1cf9b-108">Por ejemplo, un canal alfa de 8 bits puede representar 256 niveles de transparencia, de 0 (el píxel completo es transparente) a 255 (el píxel completo es opaco).</span><span class="sxs-lookup"><span data-stu-id="1cf9b-108">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire pixel is transparent) to 255 (the entire pixel is opaque).</span></span> <span data-ttu-id="1cf9b-109">En la lista siguiente se muestran algunos efectos especiales que puede crear mediante la combinación alfa.</span><span class="sxs-lookup"><span data-stu-id="1cf9b-109">The list below shows some special effects you can create using alpha blending.</span></span>

<span data-ttu-id="1cf9b-110">El color se puede definir con o sin valores alfa.</span><span class="sxs-lookup"><span data-stu-id="1cf9b-110">Color can be defined with or without alpha values.</span></span> <span data-ttu-id="1cf9b-111">Color sin alfa es color RGB con alfa se almacena como ARGB.</span><span class="sxs-lookup"><span data-stu-id="1cf9b-111">Color without alpha is RGB color with alpha is stored as ARGB.</span></span> <span data-ttu-id="1cf9b-112">Los datos de vértice, los datos de material y los datos de textura se pueden usar para proporcionar transparencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="1cf9b-112">Vertex data, material data and texture data can be used to give object's transparency.</span></span> <span data-ttu-id="1cf9b-113">El búfer de fotogramas también se puede usar para generar efectos de transparencia.</span><span class="sxs-lookup"><span data-stu-id="1cf9b-113">The frame buffer can also be used to generate transparency effects.</span></span>

-   [<span data-ttu-id="1cf9b-114">Vértice alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1cf9b-114">Vertex Alpha (Direct3D 9)</span></span>](vertex-alpha.md)
-   [<span data-ttu-id="1cf9b-115">Material Alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1cf9b-115">Material Alpha (Direct3D 9)</span></span>](material-alpha.md)
-   [<span data-ttu-id="1cf9b-116">Alfa de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1cf9b-116">Texture Alpha (Direct3D 9)</span></span>](texture-alpha.md)
-   [<span data-ttu-id="1cf9b-117">Búfer de fotogramas alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1cf9b-117">Frame Buffer Alpha (Direct3D 9)</span></span>](frame-buffer-alpha.md)
-   [<span data-ttu-id="1cf9b-118">Destino de representación alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1cf9b-118">Render Target Alpha (Direct3D 9)</span></span>](render-target-alpha.md)

<span data-ttu-id="1cf9b-119">Entre los ejemplos que muestran alfa se incluyen:</span><span class="sxs-lookup"><span data-stu-id="1cf9b-119">Samples that demonstrate alpha include:</span></span>

-   [<span data-ttu-id="1cf9b-120">Afición (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1cf9b-120">Billboarding (Direct3D 9)</span></span>](billboarding.md)
-   [<span data-ttu-id="1cf9b-121">Nubes, humo y pistas de Esquí (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1cf9b-121">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>](clouds--smoke--and-vapor-trails.md)
-   [<span data-ttu-id="1cf9b-122">Fire, Fires, and Explosions (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1cf9b-122">Fire, Flares, and Explosions (Direct3D 9)</span></span>](fire--flares--and-explosions.md)

## <a name="related-topics"></a><span data-ttu-id="1cf9b-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1cf9b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cf9b-124">Representación de Direct3D</span><span class="sxs-lookup"><span data-stu-id="1cf9b-124">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



