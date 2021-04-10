---
description: La asignación de rugosidad es una forma especial de asignación de entorno especular o difusor que simula los reflejos de objetos con una teselación precisa sin necesidad de recuentos de polígonos extremadamente altos.
ms.assetid: 3e195e4f-3fa9-43c4-b2e5-42a6b3aaccf2
title: Asignación de rugosidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dba4621568f595eae965941168ad6930e183f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153382"
---
# <a name="bump-mapping-direct3d-9"></a><span data-ttu-id="402eb-103">Asignación de rugosidad (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="402eb-103">Bump Mapping (Direct3D 9)</span></span>

<span data-ttu-id="402eb-104">La asignación de rugosidad es una forma especial de asignación de entorno especular o difusor que simula los reflejos de objetos con una teselación precisa sin necesidad de recuentos de polígonos extremadamente altos.</span><span class="sxs-lookup"><span data-stu-id="402eb-104">Bump mapping is a special form of specular or diffuse environment mapping that simulates the reflections of finely tessellated objects without requiring extremely high polygon counts.</span></span> <span data-ttu-id="402eb-105">La asignación de rugosidad implementada por Direct3D se puede describir con precisión como Perturbation de coordenadas de textura por píxel de las asignaciones de entorno especulares o difusas, ya que proporciona información sobre el contorno del mapa de rugosidad en términos de valores Delta, que el sistema aplica a las coordenadas de textura de ti y v de un mapa de entorno en la siguiente fase de textura.</span><span class="sxs-lookup"><span data-stu-id="402eb-105">Bump mapping implemented by Direct3D can be accurately described as per-pixel texture coordinate perturbation of specular or diffuse environment maps, because you provide information about the contour of the bump map in terms of delta values, which the system applies to the u and v texture coordinates of an environment map in the next texture stage.</span></span> <span data-ttu-id="402eb-106">Los valores Delta se codifican en el formato de píxel de la superficie del mapa de rugosidad (vea [formatos de píxeles de mapa de rugosidad](bump-map-pixel-formats.md)).</span><span class="sxs-lookup"><span data-stu-id="402eb-106">The delta values are encoded in the pixel format of the bump map surface (see [Bump Map Pixel Formats](bump-map-pixel-formats.md)).</span></span>

<span data-ttu-id="402eb-107">La asignación de rugosidad se basa en la combinación de varias texturas.</span><span class="sxs-lookup"><span data-stu-id="402eb-107">Bump mapping relies on blending multiple textures.</span></span> <span data-ttu-id="402eb-108">Esto significa que el dispositivo debe admitir al menos dos fases de fusión; uno para el mapa de rugosidad y otro para un mapa de entorno.</span><span class="sxs-lookup"><span data-stu-id="402eb-108">This means the device must support at least two blending stages; one for the bump map and another for an environment map.</span></span> <span data-ttu-id="402eb-109">Se requiere un mínimo de tres fases de fusión de texturas para aplicar un mapa de textura base adicional, que es el caso más común.</span><span class="sxs-lookup"><span data-stu-id="402eb-109">A minimum of three texture blending stages are required to apply an additional base texture map, which is the most common case.</span></span> <span data-ttu-id="402eb-110">En el diagrama siguiente se muestran las relaciones entre la textura base, el mapa de rugosidad y el mapa de entorno en cascada de fusión de texturas.</span><span class="sxs-lookup"><span data-stu-id="402eb-110">The following diagram shows the relationships between the base texture, the bump map, and the environment map in the texture blending cascade.</span></span>

![diagrama de la mezcla en cascada de la combinación de texturas](images/bumpmap-tcascade.png)

<span data-ttu-id="402eb-112">Debe preparar las fases de textura correctamente para habilitar la asignación de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="402eb-112">You must prepare the texture stages appropriately to enable bump mapping.</span></span> <span data-ttu-id="402eb-113">En los siguientes temas se presenta la asignación de rugosidad y se proporcionan detalles sobre cómo se puede usar en las aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="402eb-113">The following topics introduce bump mapping, and provide details about how you can use it in your applications:</span></span>

-   [<span data-ttu-id="402eb-114">Formatos de píxeles de mapa de rugosidad</span><span class="sxs-lookup"><span data-stu-id="402eb-114">Bump Map Pixel Formats</span></span>](bump-map-pixel-formats.md)
-   [<span data-ttu-id="402eb-115">Fórmulas de asignación de rugosidad</span><span class="sxs-lookup"><span data-stu-id="402eb-115">Bump Mapping Formulas</span></span>](bump-mapping-formulas.md)
-   [<span data-ttu-id="402eb-116">Usar la asignación de rugosidad</span><span class="sxs-lookup"><span data-stu-id="402eb-116">Using Bump Mapping</span></span>](using-bump-mapping.md)

<span data-ttu-id="402eb-117">Direct3D no admite de forma nativa mapas de altura; son simplemente un formato cómodo en el que se almacenan y visualizan los datos del perfil.</span><span class="sxs-lookup"><span data-stu-id="402eb-117">Direct3D does not natively support height maps; they are merely a convenient format in which to store and visualize contour data.</span></span> <span data-ttu-id="402eb-118">La aplicación puede almacenar información de perfil en cualquier formato o incluso generar un mapa de rugosidad de procedimientos.</span><span class="sxs-lookup"><span data-stu-id="402eb-118">Your application can store contour information in any format, or even generate a procedural bump map.</span></span>

## <a name="related-topics"></a><span data-ttu-id="402eb-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="402eb-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="402eb-120">Canalización de píxeles</span><span class="sxs-lookup"><span data-stu-id="402eb-120">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 



