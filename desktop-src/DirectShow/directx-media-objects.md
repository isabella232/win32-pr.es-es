---
description: Objetos multimedia de DirectX
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: Objetos multimedia de DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2119fc8cce602bc1cc085886edd6852320aca180
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678622"
---
# <a name="directx-media-objects"></a><span data-ttu-id="27c71-103">Objetos multimedia de DirectX</span><span class="sxs-lookup"><span data-stu-id="27c71-103">DirectX Media Objects</span></span>

> [!Note]  
> <span data-ttu-id="27c71-104">DMOs se han sustituido por [transformaciones de Media Foundation](/windows/desktop/medfound/media-foundation-transforms) (MFTs).</span><span class="sxs-lookup"><span data-stu-id="27c71-104">DMOs have been superseded by [Media Foundation Transforms](/windows/desktop/medfound/media-foundation-transforms) (MFTs).</span></span> <span data-ttu-id="27c71-105">Todavía se admiten las interfaces de DMO.</span><span class="sxs-lookup"><span data-stu-id="27c71-105">The DMO interfaces are still supported.</span></span> <span data-ttu-id="27c71-106">Sin embargo, si está escribiendo un códec personalizado o un complemento de procesamiento de audio y vídeo, considere la posibilidad de implementarlo como MFT.</span><span class="sxs-lookup"><span data-stu-id="27c71-106">However, if you are writing a custom codec or audio/video processing plug-in, you should consider implementing it as an MFT.</span></span>

 

<span data-ttu-id="27c71-107">Los objetos multimedia de DirectX (DMOs) son componentes de streaming de datos basados en COM.</span><span class="sxs-lookup"><span data-stu-id="27c71-107">DirectX Media Objects (DMOs) are COM-based data-streaming components.</span></span> <span data-ttu-id="27c71-108">En algunos aspectos, DMOs son similares a los filtros de Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="27c71-108">In some respects, DMOs are similar to Microsoft DirectShow filters.</span></span> <span data-ttu-id="27c71-109">Como los filtros de DirectShow, DMOs toma los datos de entrada y los usa para generar datos de salida.</span><span class="sxs-lookup"><span data-stu-id="27c71-109">Like DirectShow filters, DMOs take input data and use it to produce output data.</span></span> <span data-ttu-id="27c71-110">Sin embargo, las interfaces de programación de aplicaciones (API) para DMOs son mucho más sencillas que las API correspondientes para DirectShow.</span><span class="sxs-lookup"><span data-stu-id="27c71-110">However, the application programming interfaces (APIs) for DMOs are much simpler than the corresponding APIs for DirectShow.</span></span> <span data-ttu-id="27c71-111">Como resultado, DMOs son más fáciles de crear, probar y usar.</span><span class="sxs-lookup"><span data-stu-id="27c71-111">As a result, DMOs are easier to create, test, and use.</span></span> <span data-ttu-id="27c71-112">DMOs se puede usar en muchos escenarios:</span><span class="sxs-lookup"><span data-stu-id="27c71-112">DMOs can be used in many scenarios:</span></span>

-   <span data-ttu-id="27c71-113">Las aplicaciones basadas en DirectShow pueden usar DMOs a través de un filtro de DirectShow denominado filtro de [contenedor de DMO](dmo-wrapper-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="27c71-113">Applications based on DirectShow can use DMOs through a DirectShow filter called the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="27c71-114">La distinción entre filtros y DMOs es transparente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="27c71-114">The distinction between filters and DMOs is transparent to the application.</span></span> <span data-ttu-id="27c71-115">La aplicación no llama directamente a las API de DMO.</span><span class="sxs-lookup"><span data-stu-id="27c71-115">The application does not directly call the DMO APIs.</span></span>
-   <span data-ttu-id="27c71-116">Las aplicaciones basadas en Microsoft DirectSound pueden usar el efecto de audio DMOs.</span><span class="sxs-lookup"><span data-stu-id="27c71-116">Applications based on Microsoft DirectSound can use audio effect DMOs.</span></span> <span data-ttu-id="27c71-117">De nuevo, la aplicación se protege de las API de DMO de bajo nivel mediante las API de DirectSound de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="27c71-117">Again, the application is shielded from the low-level DMO APIs by the higher-level DirectSound APIs.</span></span>
-   <span data-ttu-id="27c71-118">Las aplicaciones pueden usar DMOs directamente.</span><span class="sxs-lookup"><span data-stu-id="27c71-118">Applications can use DMOs directly.</span></span>

<span data-ttu-id="27c71-119">Por lo tanto, al escribir un DMO, se crea un componente que se puede usar en una amplia gama de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="27c71-119">Thus, by writing a DMO, you create a component that can be used in a wide range of applications.</span></span> <span data-ttu-id="27c71-120">Esta documentación contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="27c71-120">This documentation contains the following sections:</span></span>

-   [<span data-ttu-id="27c71-121">Acerca de DMOs</span><span class="sxs-lookup"><span data-stu-id="27c71-121">About DMOs</span></span>](about-dmos.md)
-   [<span data-ttu-id="27c71-122">Usar DMOs</span><span class="sxs-lookup"><span data-stu-id="27c71-122">Using DMOs</span></span>](using-dmos.md)
-   [<span data-ttu-id="27c71-123">Escritura de DMO</span><span class="sxs-lookup"><span data-stu-id="27c71-123">Writing a DMO</span></span>](writing-a-dmo.md)
-   [<span data-ttu-id="27c71-124">Parámetros multimedia</span><span class="sxs-lookup"><span data-stu-id="27c71-124">Media Parameters</span></span>](media-parameters.md)
-   [<span data-ttu-id="27c71-125">Referencia de DMO</span><span class="sxs-lookup"><span data-stu-id="27c71-125">DMO Reference</span></span>](dmo-reference.md)

## <a name="related-topics"></a><span data-ttu-id="27c71-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="27c71-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27c71-127">DirectShow</span><span class="sxs-lookup"><span data-stu-id="27c71-127">DirectShow</span></span>](directshow.md)
</dt> </dl>

 

 
