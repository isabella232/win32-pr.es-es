---
description: La asignación de entorno es una técnica que simula superficies muy reflectantes sin usar el seguimiento de Ray.
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: Asignación de entorno (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686f15b2f097550206f9c02cfc4104e7c9f6c030
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805612"
---
# <a name="environment-mapping-direct3d-9"></a><span data-ttu-id="5eb46-103">Asignación de entorno (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5eb46-103">Environment Mapping (Direct3D 9)</span></span>

<span data-ttu-id="5eb46-104">La asignación de entorno es una técnica que simula superficies muy reflectantes sin usar el seguimiento de Ray.</span><span class="sxs-lookup"><span data-stu-id="5eb46-104">Environment mapping is a technique that simulates highly reflective surfaces without using ray tracing.</span></span> <span data-ttu-id="5eb46-105">En la práctica, la asignación de entorno aplica un mapa de textura especial que contiene una imagen de la escena que rodea un objeto al propio objeto.</span><span class="sxs-lookup"><span data-stu-id="5eb46-105">In practice, environment mapping applies a special texture map that contains an image of the scene surrounding an object to the object itself.</span></span> <span data-ttu-id="5eb46-106">El resultado se aproxima a la apariencia de una superficie reflectante, lo suficientemente cerca como para engañar, sin incurrir en ningún cálculo complejo implicado en el seguimiento de Ray.</span><span class="sxs-lookup"><span data-stu-id="5eb46-106">The result approximates the appearance of a reflective surface, close enough to fool the eye, without incurring any of the complex computations involved in ray tracing.</span></span>

<span data-ttu-id="5eb46-107">En la ilustración siguiente se muestra un tipo de asignación de entorno denominada asignación de entorno esférico.</span><span class="sxs-lookup"><span data-stu-id="5eb46-107">The following illustration demonstrates a type of environment mapping called spherical environment mapping.</span></span> <span data-ttu-id="5eb46-108">Para obtener más información, consulte [asignación de entorno esférico](spherical-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="5eb46-108">For details, see [Spherical Environment Mapping](spherical-environment-mapping.md).</span></span>

![Ilustración de un tetera con una textura aplicada que refleja el entorno](images/spheremapped-teapot.png)

<span data-ttu-id="5eb46-110">El tetera de esta imagen parece reflejar su entorno; en realidad, se aplica una textura al objeto.</span><span class="sxs-lookup"><span data-stu-id="5eb46-110">The teapot in this image appears to reflect its surroundings; this is actually a texture being applied to the object.</span></span> <span data-ttu-id="5eb46-111">Dado que la asignación de entorno utiliza una textura, combinada con coordenadas de textura de cálculo especial, se puede realizar en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="5eb46-111">Because environment mapping uses a texture, combined with specially computed texture coordinates, it can be performed in real-time.</span></span>

<span data-ttu-id="5eb46-112">En esta sección se proporciona información sobre cómo realizar dos tipos comunes de asignación de entorno con Direct3D.</span><span class="sxs-lookup"><span data-stu-id="5eb46-112">This section provides information about performing two common types of environment mapping with Direct3D.</span></span> <span data-ttu-id="5eb46-113">Hay muchos tipos de asignación de entorno en uso en toda la industria de gráficos, pero los temas siguientes se destinan a las dos formas más comunes: asignación de entorno cúbica y asignación de entorno esférico.</span><span class="sxs-lookup"><span data-stu-id="5eb46-113">There are many types of environment mapping in use throughout the graphics industry, but the following topics target the two most common forms: cubic environment mapping and spherical environment mapping.</span></span>

-   [<span data-ttu-id="5eb46-114">Asignación de entorno cúbica</span><span class="sxs-lookup"><span data-stu-id="5eb46-114">Cubic Environment Mapping</span></span>](cubic-environment-mapping.md)
-   [<span data-ttu-id="5eb46-115">Asignación de entorno esférico</span><span class="sxs-lookup"><span data-stu-id="5eb46-115">Spherical Environment Mapping</span></span>](spherical-environment-mapping.md)

## <a name="related-topics"></a><span data-ttu-id="5eb46-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5eb46-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eb46-117">Canalización de píxeles</span><span class="sxs-lookup"><span data-stu-id="5eb46-117">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 



