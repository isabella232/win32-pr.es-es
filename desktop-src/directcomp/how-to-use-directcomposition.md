---
title: Cómo usar DirectComposition
description: En esta sección se describen los procedimientos recomendados para usar Microsoft DirectComposition \ 32; Y muestra cómo usar la API para realizar varias tareas comunes.
ms.assetid: 49F6E356-90C7-423A-A31A-AEE41F882D3B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0658a9693567dfd88e9a986893048fa1d0fa1e5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105695498"
---
# <a name="how-to-use-directcomposition"></a><span data-ttu-id="47aed-103">Cómo usar DirectComposition</span><span class="sxs-lookup"><span data-stu-id="47aed-103">How to use DirectComposition</span></span>

> [!NOTE]
> <span data-ttu-id="47aed-104">En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="47aed-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="47aed-105">Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="47aed-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="47aed-106">En esta sección se describen los procedimientos recomendados para usar la API de Microsoft DirectComposition y se muestra cómo usar la API para realizar varias tareas comunes.</span><span class="sxs-lookup"><span data-stu-id="47aed-106">This section describes best practices for using the Microsoft DirectComposition API, and demonstrates how to use the API to accomplish several common tasks.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="47aed-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="47aed-107">In this section</span></span>



| <span data-ttu-id="47aed-108">Tema</span><span class="sxs-lookup"><span data-stu-id="47aed-108">Topic</span></span>                                                                                                                      | <span data-ttu-id="47aed-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="47aed-109">Description</span></span>                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47aed-110">Prácticas recomendadas para DirectComposition</span><span class="sxs-lookup"><span data-stu-id="47aed-110">Best practices for DirectComposition</span></span>](best-practices-for-directcomposition.md)<br/>                                | <span data-ttu-id="47aed-111">En este tema se describen los procedimientos recomendados para usar DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="47aed-111">This topic describes best practices for using DirectComposition.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="47aed-112">Cómo inicializar DirectComposition</span><span class="sxs-lookup"><span data-stu-id="47aed-112">How to initialize DirectComposition</span></span>](initialize-directcomposition.md)<br/>                                         | <span data-ttu-id="47aed-113">En este tema se muestra cómo crear e inicializar el conjunto mínimo de objetos DirectComposition necesarios para crear una composición simple.</span><span class="sxs-lookup"><span data-stu-id="47aed-113">This topic demonstrates how to create and initialize the minimum set of DirectComposition objects needed to create a simple composition.</span></span><br/>                                                          |
| [<span data-ttu-id="47aed-114">Cómo compilar un árbol visual sencillo</span><span class="sxs-lookup"><span data-stu-id="47aed-114">How to build a simple visual tree</span></span>](how-to--build-a-visual-tree.md)<br/>                                            | <span data-ttu-id="47aed-115">En este tema se muestra cómo crear un árbol visual DirectComposition simple.</span><span class="sxs-lookup"><span data-stu-id="47aed-115">This topic demonstrates how to build a simple DirectComposition visual tree.</span></span> <span data-ttu-id="47aed-116">En el ejemplo de este tema se crea y se compone un árbol visual que consta de un elemento visual raíz y tres objetos visuales secundarios.</span><span class="sxs-lookup"><span data-stu-id="47aed-116">The example in this topic builds and composes a visual tree that consists of a root visual and three child visuals.</span></span> <br/> |
| [<span data-ttu-id="47aed-117">Cómo recortar con un objeto de recorte de rectángulo</span><span class="sxs-lookup"><span data-stu-id="47aed-117">How to clip with a rectangle clip object</span></span>](how-to--set-the-clip-rectangle-for-a-visual.md)<br/>                     | <span data-ttu-id="47aed-118">En este tema se muestra cómo usar un objeto de clip de rectángulo para recortar un árbol visual o visual.</span><span class="sxs-lookup"><span data-stu-id="47aed-118">This topic demonstrates how to use a rectangle clip object to clip a visual or visual tree.</span></span> <br/>                                                                                                      |
| [<span data-ttu-id="47aed-119">Cómo aplicar transformaciones 2D</span><span class="sxs-lookup"><span data-stu-id="47aed-119">How to apply 2D transforms</span></span>](apply-2d-transforms.md)<br/>                                                           | <span data-ttu-id="47aed-120">En este tema se muestra cómo aplicar transformaciones 2D a un visual mediante DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="47aed-120">This topic demonstrates how to apply 2D transforms to a visual by using DirectComposition.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="47aed-121">Cómo aplicar efectos</span><span class="sxs-lookup"><span data-stu-id="47aed-121">How to apply effects</span></span>](how-to--apply-transforms-and-effects-to-a-visual.md)<br/>                                    | <span data-ttu-id="47aed-122">En este tema se muestra cómo usar DirectComposition para aplicar efectos y transformaciones 3D a un visual.</span><span class="sxs-lookup"><span data-stu-id="47aed-122">This topic demonstrates how to use DirectComposition to apply effects and 3D transformations to a visual.</span></span><br/>                                                                                         |
| [<span data-ttu-id="47aed-123">Cómo aplicar animaciones</span><span class="sxs-lookup"><span data-stu-id="47aed-123">How to apply animations</span></span>](how-to--animate-a-visual.md)<br/>                                                         | <span data-ttu-id="47aed-124">En este tema se muestra cómo animar las propiedades de un visual mediante DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="47aed-124">This topic demonstrates how to animate the properties of a visual by using DirectComposition.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="47aed-125">Cómo animar el mapa de bits de una ventana secundaria superpuesta</span><span class="sxs-lookup"><span data-stu-id="47aed-125">How to animate the bitmap of a layered child window</span></span>](how-to--animate-the-bitmap-of-a-layered-child-window.md)<br/> | <span data-ttu-id="47aed-126">En este tema se describe cómo crear y animar un elemento visual que utiliza el mapa de bits de una ventana secundaria superpuesta como contenido del elemento visual.</span><span class="sxs-lookup"><span data-stu-id="47aed-126">This topic describes how to create and animate a visual that uses the bitmap of a layered child window as the visual's content.</span></span> <br/>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="47aed-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="47aed-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47aed-128">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="47aed-128">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





