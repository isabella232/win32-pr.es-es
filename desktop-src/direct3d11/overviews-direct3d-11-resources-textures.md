---
title: Texturas
description: En esta sección se describen las texturas que se usan en Direct3D 11 y se proporcionan vínculos a la documentación basada en tareas para escenarios comunes.
ms.assetid: ec833431-a7b4-4aea-91c8-e99b718de2c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc3909f354b0709e82ffd2bdffafe6cdb35516
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269091"
---
# <a name="textures"></a><span data-ttu-id="af1ba-103">Texturas</span><span class="sxs-lookup"><span data-stu-id="af1ba-103">Textures</span></span>

<span data-ttu-id="af1ba-104">Una textura almacena información de textura.</span><span class="sxs-lookup"><span data-stu-id="af1ba-104">A texture stores texel information.</span></span> <span data-ttu-id="af1ba-105">En esta sección se describen las texturas que se usan en Direct3D 11 y se proporcionan vínculos a la documentación basada en tareas para escenarios comunes.</span><span class="sxs-lookup"><span data-stu-id="af1ba-105">This section describes textures that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="af1ba-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="af1ba-106">In this section</span></span>



| <span data-ttu-id="af1ba-107">Tema</span><span class="sxs-lookup"><span data-stu-id="af1ba-107">Topic</span></span>                                                                                                    | <span data-ttu-id="af1ba-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="af1ba-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af1ba-109">Introducción a las texturas en Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="af1ba-109">Introduction To Textures in Direct3D 11</span></span>](overviews-direct3d-11-resources-textures-intro.md)<br/> | <span data-ttu-id="af1ba-110">Un recurso de textura es una colección estructurada de datos diseñada para almacenar textura.</span><span class="sxs-lookup"><span data-stu-id="af1ba-110">A texture resource is a structured collection of data designed to store texels.</span></span> <span data-ttu-id="af1ba-111">Un textura representa la unidad más pequeña de una textura que se puede leer o escribir en la canalización.</span><span class="sxs-lookup"><span data-stu-id="af1ba-111">A texel represents the smallest unit of a texture that can be read or written to by the pipeline.</span></span> <span data-ttu-id="af1ba-112">A diferencia de los búferes, las texturas se pueden filtrar por muestras de texturas, ya que las unidades de sombreador las leen.</span><span class="sxs-lookup"><span data-stu-id="af1ba-112">Unlike buffers, textures can be filtered by texture samplers as they are read by shader units.</span></span> <span data-ttu-id="af1ba-113">El tipo de textura afecta al modo en que se filtra la textura.</span><span class="sxs-lookup"><span data-stu-id="af1ba-113">The type of texture impacts how the texture is filtered.</span></span> <span data-ttu-id="af1ba-114">Cada textura contiene de 1 a 4 componentes, organizados en uno de los formatos de DXGI definidos por la \_ enumeración de formato de dxgi.</span><span class="sxs-lookup"><span data-stu-id="af1ba-114">Each texel contains 1 to 4 components, arranged in one of the DXGI formats defined by the DXGI\_FORMAT enumeration.</span></span><br/> |
| [<span data-ttu-id="af1ba-115">Compresión de bloque de textura en Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="af1ba-115">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)<br/>      | <span data-ttu-id="af1ba-116">La compatibilidad con la compresión de bloques (BC) para las texturas se ha ampliado en Direct3D 11 para incluir los algoritmos BC6H y BC7.</span><span class="sxs-lookup"><span data-stu-id="af1ba-116">Block Compression (BC) support for textures has been extended in Direct3D 11 to include the BC6H and BC7 algorithms.</span></span> <span data-ttu-id="af1ba-117">BC6H es compatible con los datos de origen de color de alto nivel dinámico y BC7 proporciona una compresión de calidad mejor que la media con menos artefactos para los datos de origen RGB estándar.</span><span class="sxs-lookup"><span data-stu-id="af1ba-117">BC6H supports high-dynamic range color source data, and BC7 provides better-than-average quality compression with less artifacts for standard RGB source data.</span></span><br/>                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="af1ba-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af1ba-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af1ba-119">Cómo: crear una textura</span><span class="sxs-lookup"><span data-stu-id="af1ba-119">How to: Create a Texture</span></span>](overviews-direct3d-11-resources-textures-create.md)
</dt> <dt>

[<span data-ttu-id="af1ba-120">Cómo: inicializar una textura mediante programación</span><span class="sxs-lookup"><span data-stu-id="af1ba-120">How to: Initialize a Texture Programmatically</span></span>](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
</dt> <dt>

[<span data-ttu-id="af1ba-121">Cómo: inicializar una textura desde un archivo</span><span class="sxs-lookup"><span data-stu-id="af1ba-121">How to: Initialize a Texture From a File</span></span>](overviews-direct3d-11-resources-textures-how-to.md)
</dt> <dt>

[<span data-ttu-id="af1ba-122">Recursos</span><span class="sxs-lookup"><span data-stu-id="af1ba-122">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





