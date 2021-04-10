---
description: Las texturas son una herramienta muy eficaz para dotar de realismo a las imágenes en 3D generadas por PC. Direct3D admite un amplio conjunto de características de texturas y ofrece a los desarrolladores acceso fácil a técnicas avanzadas de texturas.
ms.assetid: 48dcbc86-631e-4bc7-b809-b0e4a0a9ae8e
title: Texturas de Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afebd7217b36ad5f740616e198963314a1d2aca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151979"
---
# <a name="direct3d-textures-direct3d-9"></a><span data-ttu-id="0833f-104">Texturas de Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0833f-104">Direct3D Textures (Direct3D 9)</span></span>

<span data-ttu-id="0833f-105">Las texturas son una herramienta muy eficaz para dotar de realismo a las imágenes en 3D generadas por PC.</span><span class="sxs-lookup"><span data-stu-id="0833f-105">Textures are a powerful tool in creating realism in computer-generated 3D images.</span></span> <span data-ttu-id="0833f-106">Direct3D admite un amplio conjunto de características de texturas y ofrece a los desarrolladores acceso fácil a técnicas avanzadas de texturas.</span><span class="sxs-lookup"><span data-stu-id="0833f-106">Direct3D supports an extensive texturing feature set, providing developers with easy access to advanced texturing techniques.</span></span>

<span data-ttu-id="0833f-107">Esta sección le ayudará a empezar a usar las texturas.</span><span class="sxs-lookup"><span data-stu-id="0833f-107">This section will get you started using textures.</span></span>

-   [<span data-ttu-id="0833f-108">Conceptos básicos de la texturización (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0833f-108">Basic Texturing Concepts (Direct3D 9)</span></span>](basic-texturing-concepts.md)
-   [<span data-ttu-id="0833f-109">Coordenadas de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0833f-109">Texture Coordinates (Direct3D 9)</span></span>](texture-coordinates.md)
-   [<span data-ttu-id="0833f-110">Filtrado de texturas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0833f-110">Texture Filtering (Direct3D 9)</span></span>](texture-filtering.md)
-   [<span data-ttu-id="0833f-111">Recursos de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0833f-111">Texture Resources (Direct3D 9)</span></span>](texture-resources.md)
-   [<span data-ttu-id="0833f-112">Ajuste de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0833f-112">Texture Wrapping (Direct3D 9)</span></span>](texture-wrapping.md)
-   [<span data-ttu-id="0833f-113">Combinación de texturas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0833f-113">Texture Blending (Direct3D 9)</span></span>](texture-blending.md)

<span data-ttu-id="0833f-114">Estos temas incluirán más detalles sobre la funcionalidad de texturas adicional.</span><span class="sxs-lookup"><span data-stu-id="0833f-114">These topics will go into more detail about additional texturing functionality.</span></span>

-   [<span data-ttu-id="0833f-115">Generación automática de mapas MIP (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0833f-115">Automatic Generation of Mipmaps (Direct3D 9)</span></span>](automatic-generation-of-mipmaps.md)
-   [<span data-ttu-id="0833f-116">Administración automática de texturas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0833f-116">Automatic Texture Management (Direct3D 9)</span></span>](automatic-texture-management.md)
-   [<span data-ttu-id="0833f-117">Recursos de textura comprimidos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0833f-117">Compressed Texture Resources (Direct3D 9)</span></span>](compressed-texture-resources.md)
-   [<span data-ttu-id="0833f-118">Consideraciones de hardware para la texturización (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0833f-118">Hardware Considerations for Texturing (Direct3D 9)</span></span>](hardware-considerations-for-texturing.md)
-   [<span data-ttu-id="0833f-119">Recursos de textura de volumen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0833f-119">Volume Texture Resources (Direct3D 9)</span></span>](volume-texture-resources.md)

<span data-ttu-id="0833f-120">Para mejorar el rendimiento, considere la posibilidad de usar texturas dinámicas.</span><span class="sxs-lookup"><span data-stu-id="0833f-120">For improved performance, consider using dynamic textures.</span></span> <span data-ttu-id="0833f-121">Una textura dinámica puede bloquearse, escribirse y desbloquearse en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="0833f-121">A dynamic texture can be locked, written to, and unlocked each frame.</span></span> <span data-ttu-id="0833f-122">Vea [usar texturas dinámicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="0833f-122">See [Using Dynamic Textures](performance-optimizations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0833f-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0833f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0833f-124">Introducción</span><span class="sxs-lookup"><span data-stu-id="0833f-124">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



