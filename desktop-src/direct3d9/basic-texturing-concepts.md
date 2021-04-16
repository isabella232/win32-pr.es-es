---
description: Imágenes 3D tempranas generadas por el equipo, aunque por lo general son avanzadas para su tiempo, con lo que se tiende a tener un aspecto plástico brillante.
ms.assetid: 548ae140-c746-4fab-8000-421289d4f0a2
title: Conceptos básicos de la texturización (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba8c4971f70cbe5b7b371f71191de6edb4c2be46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696122"
---
# <a name="basic-texturing-concepts-direct3d-9"></a><span data-ttu-id="8094c-103">Conceptos básicos de la texturización (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8094c-103">Basic Texturing Concepts (Direct3D 9)</span></span>

<span data-ttu-id="8094c-104">Imágenes 3D tempranas generadas por el equipo, aunque por lo general son avanzadas para su tiempo, con lo que se tiende a tener un aspecto plástico brillante.</span><span class="sxs-lookup"><span data-stu-id="8094c-104">Early computer-generated 3D images, although generally advanced for their time, tended to have a shiny plastic look.</span></span> <span data-ttu-id="8094c-105">Carecía de los tipos de marcas, como scuffs, grietas, huellas digitales y manchas, que proporcionan a los objetos 3D una complejidad visual realista.</span><span class="sxs-lookup"><span data-stu-id="8094c-105">They lacked the types of markings-such as scuffs, cracks, fingerprints, and smudges-that give 3D objects realistic visual complexity.</span></span> <span data-ttu-id="8094c-106">En los últimos años, las texturas han ganado popularidad entre los desarrolladores como una herramienta para mejorar el realismo de las imágenes 3D generadas por el equipo.</span><span class="sxs-lookup"><span data-stu-id="8094c-106">In recent years, textures have gained popularity among developers as a tool for enhancing the realism of computer-generated 3D images.</span></span>

<span data-ttu-id="8094c-107">En su uso cotidiano, la palabra Texture hace referencia a la suavidad o la rugosidad de un objeto.</span><span class="sxs-lookup"><span data-stu-id="8094c-107">In its everyday use, the word texture refers to an object's smoothness or roughness.</span></span> <span data-ttu-id="8094c-108">En los gráficos de equipos, sin embargo, una textura es un mapa de bits de colores de píxeles que proporcionan a un objeto la apariencia de la textura.</span><span class="sxs-lookup"><span data-stu-id="8094c-108">In computer graphics, however, a texture is a bitmap of pixel colors that give an object the appearance of texture.</span></span>

<span data-ttu-id="8094c-109">Dado que las texturas de Direct3D son mapas de bits, cualquier mapa de bits se puede aplicar a un primitivo de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8094c-109">Because Direct3D textures are bitmaps, any bitmap can be applied to a Direct3D primitive.</span></span> <span data-ttu-id="8094c-110">Por ejemplo, las aplicaciones pueden crear y manipular objetos que parezcan tener un patrón de grano de madera en ellos.</span><span class="sxs-lookup"><span data-stu-id="8094c-110">For instance, applications can create and manipulate objects that appear to have a wood grain pattern in them.</span></span> <span data-ttu-id="8094c-111">Hierba, suciedad y Rocks se pueden aplicar a un conjunto de primitivas 3D que forman un máximo.</span><span class="sxs-lookup"><span data-stu-id="8094c-111">Grass, dirt, and rocks can be applied to a set of 3D primitives that form a hill.</span></span> <span data-ttu-id="8094c-112">El resultado es una Hillside de aspecto realista.</span><span class="sxs-lookup"><span data-stu-id="8094c-112">The result is a realistic-looking hillside.</span></span> <span data-ttu-id="8094c-113">También puede usar la texturización para crear efectos como signos a lo largo de una carretera, Rock estratos en un acantilado o la apariencia de Marble en un piso.</span><span class="sxs-lookup"><span data-stu-id="8094c-113">You can also use texturing to create effects such as signs along a roadside, rock strata in a cliff, or the appearance of marble on a floor.</span></span>

<span data-ttu-id="8094c-114">Además, Direct3D admite técnicas de texturización más avanzadas, como la combinación de texturas, con o sin la asignación de transparencia y ligera.</span><span class="sxs-lookup"><span data-stu-id="8094c-114">In addition, Direct3D supports more advanced texturing techniques such as texture blending-with or without transparency-and light mapping.</span></span> <span data-ttu-id="8094c-115">Para obtener más información, vea [combinación de texturas (Direct3D 9)](texture-blending.md) y [asignación de luz con texturas (Direct3D 9)](light-mapping-with-textures.md).</span><span class="sxs-lookup"><span data-stu-id="8094c-115">For more information, see [Texture Blending (Direct3D 9)](texture-blending.md) and [Light Mapping with Textures (Direct3D 9)](light-mapping-with-textures.md).</span></span>

<span data-ttu-id="8094c-116">Si la aplicación crea un dispositivo de capa de abstracción de hardware (HAL) o un dispositivo de software, puede usar texturas de 8, 16, 24, 32, 64 o 128 bits.</span><span class="sxs-lookup"><span data-stu-id="8094c-116">If your application creates a hardware abstraction layer (HAL) device or a software device, it can use 8, 16, 24, 32, 64, or 128-bit textures.</span></span>

<span data-ttu-id="8094c-117">En los temas siguientes se incluye información adicional.</span><span class="sxs-lookup"><span data-stu-id="8094c-117">Additional information is contained in the following topics.</span></span>

-   [<span data-ttu-id="8094c-118">Modos de direccionamiento de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8094c-118">Texture Addressing Modes (Direct3D 9)</span></span>](texture-addressing-modes.md)
-   [<span data-ttu-id="8094c-119">Regiones desfasadas de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8094c-119">Texture Dirty Regions (Direct3D 9)</span></span>](texture-dirty-regions.md)
-   [<span data-ttu-id="8094c-120">Paletas de texturas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8094c-120">Texture Palettes (Direct3D 9)</span></span>](texture-palettes.md)

## <a name="related-topics"></a><span data-ttu-id="8094c-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8094c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8094c-122">Texturas de Direct3D</span><span class="sxs-lookup"><span data-stu-id="8094c-122">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 



