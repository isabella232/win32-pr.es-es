---
description: La combinación alfa se usa para mostrar una imagen que tiene píxeles transparentes o semitransparentes.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Combinación alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f4ae2883c7a9a92ba1b62306dc26bf09d0d9947
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153307"
---
# <a name="alpha-blending-direct3d-9"></a><span data-ttu-id="2b8ed-103">Combinación alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b8ed-103">Alpha Blending (Direct3D 9)</span></span>

<span data-ttu-id="2b8ed-104">La combinación alfa se usa para mostrar una imagen que tiene píxeles transparentes o semitransparentes.</span><span class="sxs-lookup"><span data-stu-id="2b8ed-104">Alpha blending is used to display an image that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="2b8ed-105">Además de un canal de color rojo, verde y azul, cada píxel de un mapa de bits alfa tiene un componente de transparencia conocido como canal alfa.</span><span class="sxs-lookup"><span data-stu-id="2b8ed-105">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its alpha channel.</span></span> <span data-ttu-id="2b8ed-106">Normalmente, el canal alfa contiene tantos bits como un canal de color.</span><span class="sxs-lookup"><span data-stu-id="2b8ed-106">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="2b8ed-107">Por ejemplo, un canal alfa de 8 bits puede representar 256 niveles de transparencia, desde 0 (todo el píxel es transparente) hasta 255 (todo el píxel es opaco).</span><span class="sxs-lookup"><span data-stu-id="2b8ed-107">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire pixel is transparent) to 255 (the entire pixel is opaque).</span></span> <span data-ttu-id="2b8ed-108">En la siguiente lista se muestran algunos efectos especiales que se pueden crear mediante la combinación alfa.</span><span class="sxs-lookup"><span data-stu-id="2b8ed-108">The list below shows some special effects you can create using alpha blending.</span></span>

<span data-ttu-id="2b8ed-109">El color puede definirse con o sin valores alfa.</span><span class="sxs-lookup"><span data-stu-id="2b8ed-109">Color can be defined with or without alpha values.</span></span> <span data-ttu-id="2b8ed-110">El color sin alfa es un color RGB con alfa almacenado como ARGB.</span><span class="sxs-lookup"><span data-stu-id="2b8ed-110">Color without alpha is RGB color with alpha is stored as ARGB.</span></span> <span data-ttu-id="2b8ed-111">Los datos de vértices, datos de materiales y datos de textura se pueden usar para proporcionar transparencia del objeto.</span><span class="sxs-lookup"><span data-stu-id="2b8ed-111">Vertex data, material data and texture data can be used to give object's transparency.</span></span> <span data-ttu-id="2b8ed-112">El búfer de fotogramas también se puede utilizar para generar efectos de transparencia.</span><span class="sxs-lookup"><span data-stu-id="2b8ed-112">The frame buffer can also be used to generate transparency effects.</span></span>

-   [<span data-ttu-id="2b8ed-113">Vértice alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b8ed-113">Vertex Alpha (Direct3D 9)</span></span>](vertex-alpha.md)
-   [<span data-ttu-id="2b8ed-114">Material alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b8ed-114">Material Alpha (Direct3D 9)</span></span>](material-alpha.md)
-   [<span data-ttu-id="2b8ed-115">Textura alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b8ed-115">Texture Alpha (Direct3D 9)</span></span>](texture-alpha.md)
-   [<span data-ttu-id="2b8ed-116">Búfer de trama alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b8ed-116">Frame Buffer Alpha (Direct3D 9)</span></span>](frame-buffer-alpha.md)
-   [<span data-ttu-id="2b8ed-117">Alfa de destino de representación (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b8ed-117">Render Target Alpha (Direct3D 9)</span></span>](render-target-alpha.md)

<span data-ttu-id="2b8ed-118">Los ejemplos que muestran Alpha incluyen:</span><span class="sxs-lookup"><span data-stu-id="2b8ed-118">Samples that demonstrate alpha include:</span></span>

-   [<span data-ttu-id="2b8ed-119">Cartelera (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b8ed-119">Billboarding (Direct3D 9)</span></span>](billboarding.md)
-   [<span data-ttu-id="2b8ed-120">Nubes, humo y rastros de vapor (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b8ed-120">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>](clouds--smoke--and-vapor-trails.md)
-   [<span data-ttu-id="2b8ed-121">Fuego, destellos y explosiones (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b8ed-121">Fire, Flares, and Explosions (Direct3D 9)</span></span>](fire--flares--and-explosions.md)

## <a name="related-topics"></a><span data-ttu-id="2b8ed-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2b8ed-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b8ed-123">Representación en Direct3D</span><span class="sxs-lookup"><span data-stu-id="2b8ed-123">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



