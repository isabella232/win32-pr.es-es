---
title: Conceptos de DirectComposition
description: En esta sección se proporciona información general conceptual de DirectComposition.
ms.assetid: 7839C264-C15F-4E89-82B6-2963A5C61CEC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea823d2edd27b2c725cefdd73cd053e94124d7f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076528"
---
# <a name="directcomposition-concepts"></a><span data-ttu-id="d2ba1-103">Conceptos de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="d2ba1-103">DirectComposition concepts</span></span>

> [!NOTE]
> <span data-ttu-id="d2ba1-104">En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="d2ba1-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="d2ba1-105">Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="d2ba1-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="d2ba1-106">En esta sección se proporciona información general conceptual de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="d2ba1-106">This section provides a conceptual overview of DirectComposition.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d2ba1-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d2ba1-107">In this section</span></span>



| <span data-ttu-id="d2ba1-108">Tema</span><span class="sxs-lookup"><span data-stu-id="d2ba1-108">Topic</span></span>                                                                     | <span data-ttu-id="d2ba1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2ba1-109">Description</span></span>                                                                                                                                                                            |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2ba1-110">Conceptos básicos</span><span class="sxs-lookup"><span data-stu-id="d2ba1-110">Basic concepts</span></span>](basic-concepts.md)<br/>                           | <span data-ttu-id="d2ba1-111">En este tema se proporciona información general sobre los conceptos básicos de Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="d2ba1-111">This topic provides an overview of the basic concepts of Microsoft DirectComposition.</span></span><br/>                                                                                       |
| [<span data-ttu-id="d2ba1-112">Objetos Bitmap</span><span class="sxs-lookup"><span data-stu-id="d2ba1-112">Bitmap objects</span></span>](bitmap-surfaces.md)<br/>                          | <span data-ttu-id="d2ba1-113">En este tema se describen los tipos de contenido de mapa de bits que DirectComposition admite.</span><span class="sxs-lookup"><span data-stu-id="d2ba1-113">This topic describes the types of bitmap content that DirectComposition supports.</span></span><br/>                                                                                           |
| [<span data-ttu-id="d2ba1-114">Superficie de composición</span><span class="sxs-lookup"><span data-stu-id="d2ba1-114">Composition surface</span></span>](composition-surface.md)<br/>                 | <span data-ttu-id="d2ba1-115">En este tema se describen los tipos de tipos de superficies que admite DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="d2ba1-115">This topic describes the types of types of surfaces that DirectComposition supports.</span></span><br/>                                                                                        |
| [<span data-ttu-id="d2ba1-116">Transformaciones</span><span class="sxs-lookup"><span data-stu-id="d2ba1-116">Transforms</span></span>](transforms.md)<br/>                                   | <span data-ttu-id="d2ba1-117">En este tema se describe la compatibilidad de DirectComposition con las transformaciones de afinidad bidimensionales (2D) y se describen los tipos de transformaciones que admite DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="d2ba1-117">This topic discusses DirectComposition support for two-dimensional (2D) affine (linear) transforms, and describes the types of transforms that DirectComposition supports.</span></span> <br/> |
| [<span data-ttu-id="d2ba1-118">Efectos</span><span class="sxs-lookup"><span data-stu-id="d2ba1-118">Effects</span></span>](effects.md)<br/>                                         | <span data-ttu-id="d2ba1-119">En este tema se describen los aspectos básicos de los efectos de DirectComposition y se describen los tipos de efectos que DirectComposition admite.</span><span class="sxs-lookup"><span data-stu-id="d2ba1-119">This topic discusses the basics of DirectComposition effects, and describes the types of effects that DirectComposition supports.</span></span> <br/>                                          |
| [<span data-ttu-id="d2ba1-120">Animación</span><span class="sxs-lookup"><span data-stu-id="d2ba1-120">Animation</span></span>](animation.md)<br/>                                     | <span data-ttu-id="d2ba1-121">En este tema se describen los conceptos básicos de la animación DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="d2ba1-121">This topic discusses the basics of DirectComposition animation.</span></span> <br/>                                                                                                            |
| [<span data-ttu-id="d2ba1-122">Recorte</span><span class="sxs-lookup"><span data-stu-id="d2ba1-122">Clipping</span></span>](clipping.md)<br/>                                       | <span data-ttu-id="d2ba1-123">En este tema se describe la compatibilidad de DirectComposition con objetos visuales de recorte.</span><span class="sxs-lookup"><span data-stu-id="d2ba1-123">This topic describes DirectComposition support for clipping visuals.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="d2ba1-124">Arquitectura y componentes</span><span class="sxs-lookup"><span data-stu-id="d2ba1-124">Architecture and components</span></span>](architecture-and-components.md)<br/> | <span data-ttu-id="d2ba1-125">En este tema se describen los componentes que componen DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="d2ba1-125">This topic describes the components that make up DirectComposition.</span></span><br/>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="d2ba1-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d2ba1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2ba1-127">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="d2ba1-127">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





