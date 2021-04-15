---
title: Tipos percibidos (características heredadas del entorno de Windows)
description: PerceivedType es una propiedad que clasifica un elemento en el índice.
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afaf7d8b827495a94b441e5504762dd53dbe733c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695840"
---
# <a name="perceived-types-legacy-windows-environment-features"></a><span data-ttu-id="66b9e-103">Tipos percibidos (características heredadas del entorno de Windows)</span><span class="sxs-lookup"><span data-stu-id="66b9e-103">Perceived Types (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="66b9e-104">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="66b9e-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="66b9e-105">En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="66b9e-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="66b9e-106">`PerceivedType` es una propiedad que clasifica un elemento en el índice.</span><span class="sxs-lookup"><span data-stu-id="66b9e-106">`PerceivedType` is a property that classifies an item in the index.</span></span> <span data-ttu-id="66b9e-107">Esta clasificación es diferente de la clasificación "Kind" utilizada por la [Sintaxis de consulta avanzada](-search-2x-wds-aqsreference.md) , pero también permite a los usuarios refinar los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="66b9e-107">This classification is different from the "kind" classification used by the [Advanced Query Syntax](-search-2x-wds-aqsreference.md) but similarly lets users refine their search results.</span></span> <span data-ttu-id="66b9e-108">El tipo de AQS permite a los usuarios limitar su consulta de búsqueda, mientras que la propiedad PerceivedType permite a los usuarios filtrar el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="66b9e-108">The AQS kind lets users limit their search query while the PerceivedType property lets users filter their result set.</span></span>

## <a name="types"></a><span data-ttu-id="66b9e-109">Tipos</span><span class="sxs-lookup"><span data-stu-id="66b9e-109">Types</span></span>

<span data-ttu-id="66b9e-110">Use la propiedad PerceivedType para clasificar el tipo de archivo de forma que los usuarios puedan filtrar sus resultados de búsqueda por tipo.</span><span class="sxs-lookup"><span data-stu-id="66b9e-110">Use the PerceivedType property to classify your file type so that users can filter their search results by type.</span></span> <span data-ttu-id="66b9e-111">La salida debe ser una de las cadenas siguientes:</span><span class="sxs-lookup"><span data-stu-id="66b9e-111">The output must be one of the following strings:</span></span>

-   <span data-ttu-id="66b9e-112">contact</span><span class="sxs-lookup"><span data-stu-id="66b9e-112">contact</span></span>
-   <span data-ttu-id="66b9e-113">comunicaciones</span><span class="sxs-lookup"><span data-stu-id="66b9e-113">communications</span></span>
-   <span data-ttu-id="66b9e-114">comunicaciones/correo electrónico</span><span class="sxs-lookup"><span data-stu-id="66b9e-114">communications/email</span></span>
-   <span data-ttu-id="66b9e-115">comunicaciones/calendario</span><span class="sxs-lookup"><span data-stu-id="66b9e-115">communications/calendar</span></span>
-   <span data-ttu-id="66b9e-116">comunicaciones/tarea</span><span class="sxs-lookup"><span data-stu-id="66b9e-116">communications/task</span></span>
-   <span data-ttu-id="66b9e-117">comunicaciones/im</span><span class="sxs-lookup"><span data-stu-id="66b9e-117">communications/im</span></span>
-   <span data-ttu-id="66b9e-118">documento</span><span class="sxs-lookup"><span data-stu-id="66b9e-118">document</span></span>
-   <span data-ttu-id="66b9e-119">documento/Nota</span><span class="sxs-lookup"><span data-stu-id="66b9e-119">document/note</span></span>
-   <span data-ttu-id="66b9e-120">documento/texto</span><span class="sxs-lookup"><span data-stu-id="66b9e-120">document/text</span></span>
-   <span data-ttu-id="66b9e-121">documento/hoja de cálculo</span><span class="sxs-lookup"><span data-stu-id="66b9e-121">document/spreadsheet</span></span>
-   <span data-ttu-id="66b9e-122">documento/presentación</span><span class="sxs-lookup"><span data-stu-id="66b9e-122">document/presentation</span></span>
-   <span data-ttu-id="66b9e-123">music</span><span class="sxs-lookup"><span data-stu-id="66b9e-123">music</span></span>
-   <span data-ttu-id="66b9e-124">images</span><span class="sxs-lookup"><span data-stu-id="66b9e-124">images</span></span>
-   <span data-ttu-id="66b9e-125">imágenes/imagen</span><span class="sxs-lookup"><span data-stu-id="66b9e-125">images/picture</span></span>
-   <span data-ttu-id="66b9e-126">imágenes/vídeo</span><span class="sxs-lookup"><span data-stu-id="66b9e-126">images/video</span></span>
-   <span data-ttu-id="66b9e-127">folder</span><span class="sxs-lookup"><span data-stu-id="66b9e-127">folder</span></span>
-   <span data-ttu-id="66b9e-128">programa</span><span class="sxs-lookup"><span data-stu-id="66b9e-128">program</span></span>

<span data-ttu-id="66b9e-129">Por ejemplo, si desea crear un complemento de filtro para un nuevo tipo de archivo de imagen, debe implementar lo siguiente en la interfaz de [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter):</span><span class="sxs-lookup"><span data-stu-id="66b9e-129">For example, when you want to create a filter add-in for a new picture file type, you need to implement the following in your [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface:</span></span>

-   <span data-ttu-id="66b9e-130">**GetChunk** para devolver un FULLPROPSPEC que incluye: D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType</span><span class="sxs-lookup"><span data-stu-id="66b9e-130">**GetChunk** to return a FULLPROPSPEC that includes: D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType</span></span>
-   <span data-ttu-id="66b9e-131">**GetValue** para devolver un PROPVARIANT que incluye: VT \_ LPWStr = "images/Picture"</span><span class="sxs-lookup"><span data-stu-id="66b9e-131">**GetValue** to return a PROPVARIANT that includes: VT\_LPWSTR = "images/picture"</span></span>

## <a name="related-topics"></a><span data-ttu-id="66b9e-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66b9e-132">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="66b9e-133">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="66b9e-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="66b9e-134">Desarrollo de complementos de IFilter</span><span class="sxs-lookup"><span data-stu-id="66b9e-134">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="66b9e-135">Desarrollar controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="66b9e-135">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="66b9e-136">Sintaxis de consulta avanzada</span><span class="sxs-lookup"><span data-stu-id="66b9e-136">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="66b9e-137">SchemaTable</span><span class="sxs-lookup"><span data-stu-id="66b9e-137">SchemaTable</span></span>](-search-2x-wds-schematable.md)
</dt> </dl>

 

 
