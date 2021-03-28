---
title: Recursos
description: En esta sección se describen aspectos de los recursos de Direct3D 11.
ms.assetid: 5b8b1198-73ed-4058-9fc6-a1c43902d732
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9ed73d81d2521fe97b36e6bfc8d71e387f8c9c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078628"
---
# <a name="resources"></a><span data-ttu-id="82da8-103">Recursos</span><span class="sxs-lookup"><span data-stu-id="82da8-103">Resources</span></span>

<span data-ttu-id="82da8-104">Los recursos proporcionan datos a la canalización y definen lo que se representa durante la escena.</span><span class="sxs-lookup"><span data-stu-id="82da8-104">Resources provide data to the pipeline and define what is rendered during your scene.</span></span> <span data-ttu-id="82da8-105">Los recursos se pueden cargar desde el medio de juego o se pueden crear dinámicamente en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="82da8-105">Resources can be loaded from your game media or created dynamically at run time.</span></span> <span data-ttu-id="82da8-106">Normalmente, los recursos incluyen datos de textura, datos de vértices y datos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="82da8-106">Typically, resources include texture data, vertex data, and shader data.</span></span> <span data-ttu-id="82da8-107">La mayoría de las aplicaciones de Direct3D crean y destruyen los recursos mucho a lo largo de su duración.</span><span class="sxs-lookup"><span data-stu-id="82da8-107">Most Direct3D applications create and destroy resources extensively throughout their lifespan.</span></span> <span data-ttu-id="82da8-108">En esta sección se describen aspectos de los recursos de Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="82da8-108">This section describes aspects of Direct3D 11 resources.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="82da8-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="82da8-109">In this section</span></span>



| <span data-ttu-id="82da8-110">Tema</span><span class="sxs-lookup"><span data-stu-id="82da8-110">Topic</span></span>                                                                                             | <span data-ttu-id="82da8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="82da8-111">Description</span></span>                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82da8-112">Introducción a un recurso en Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="82da8-112">Introduction to a Resource in Direct3D 11</span></span>](overviews-direct3d-11-resources-intro.md)<br/> | <span data-ttu-id="82da8-113">En este tema se presentan recursos de Direct3D como búferes y texturas.</span><span class="sxs-lookup"><span data-stu-id="82da8-113">This topic introduces Direct3D resources such as buffers and textures.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="82da8-114">Tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="82da8-114">Types of Resources</span></span>](overviews-direct3d-11-resources-types.md)<br/>                        | <span data-ttu-id="82da8-115">En este tema se describen los tipos de recursos de Direct3D 10, así como los nuevos tipos en Direct3D 11, incluidos los búferes estructurados y las texturas y los búferes de escritura.</span><span class="sxs-lookup"><span data-stu-id="82da8-115">This topic describes the types of resources from Direct3D 10, as well as new types in Direct3D 11 including structured buffers and writable textures and buffers.</span></span><br/>                                                                       |
| [<span data-ttu-id="82da8-116">Límites de recursos</span><span class="sxs-lookup"><span data-stu-id="82da8-116">Resource Limits</span></span>](overviews-direct3d-11-resources-limits.md)<br/>                          | <span data-ttu-id="82da8-117">Este tema contiene una lista de recursos compatibles con Direct3D 11 (concretamente, hardware de [nivel de característica](overviews-direct3d-11-devices-downlevel-intro.md) 11 ó 9. x).</span><span class="sxs-lookup"><span data-stu-id="82da8-117">This topic contains a list of resources that Direct3D 11 supports (specifically [feature level](overviews-direct3d-11-devices-downlevel-intro.md) 11 or 9.x hardware).</span></span><br/>                                 |
| [<span data-ttu-id="82da8-118">Subrecursos</span><span class="sxs-lookup"><span data-stu-id="82da8-118">Subresources</span></span>](overviews-direct3d-11-resources-subresources.md)<br/>                       | <span data-ttu-id="82da8-119">En este tema se describen los Subrecursos de textura o partes de un recurso.</span><span class="sxs-lookup"><span data-stu-id="82da8-119">This topic describes texture subresources, or portions of a resource.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="82da8-120">Búferes</span><span class="sxs-lookup"><span data-stu-id="82da8-120">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)<br/>                                 | <span data-ttu-id="82da8-121">Los búferes contienen datos que se utilizan para describir geometría, indexación de información de geometría y constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="82da8-121">Buffers contain data that is used for describing geometry, indexing geometry information, and shader constants.</span></span> <span data-ttu-id="82da8-122">En esta sección se describen los búferes que se usan en Direct3D 11 y los vínculos a la documentación basada en tareas para escenarios comunes.</span><span class="sxs-lookup"><span data-stu-id="82da8-122">This section describes buffers that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span><br/> |
| [<span data-ttu-id="82da8-123">Texturas</span><span class="sxs-lookup"><span data-stu-id="82da8-123">Textures</span></span>](overviews-direct3d-11-resources-textures.md)<br/>                               | <span data-ttu-id="82da8-124">En esta sección se describen las texturas que se usan en Direct3D 11 y se proporcionan vínculos a la documentación basada en tareas para escenarios comunes.</span><span class="sxs-lookup"><span data-stu-id="82da8-124">This section describes textures that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="82da8-125">Reglas de punto flotante</span><span class="sxs-lookup"><span data-stu-id="82da8-125">Floating-point rules</span></span>](floating-point-rules.md)<br/>                                       | <span data-ttu-id="82da8-126">Direct3D 11 admite varias representaciones de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="82da8-126">Direct3D 11 supports several floating-point representations.</span></span> <span data-ttu-id="82da8-127">Todos los cálculos de punto flotante operan en un subconjunto definido de las reglas de punto flotante de precisión única de IEEE 754 32 bits.</span><span class="sxs-lookup"><span data-stu-id="82da8-127">All floating-point computations operate under a defined subset of the IEEE 754 32-bit single precision floating-point rules.</span></span><br/>                                               |
| [<span data-ttu-id="82da8-128">Recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="82da8-128">Tiled resources</span></span>](tiled-resources.md)<br/>                                                 | <span data-ttu-id="82da8-129">Los recursos en mosaico pueden considerarse como recursos lógicos de gran tamaño que utilizan pequeñas cantidades de memoria física.</span><span class="sxs-lookup"><span data-stu-id="82da8-129">Tiled resources can be thought of as large logical resources that use small amounts of physical memory.</span></span><br/>                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="82da8-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82da8-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82da8-131">Programming Guide for Direct3D 11 (Guía de programación para Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="82da8-131">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

 





