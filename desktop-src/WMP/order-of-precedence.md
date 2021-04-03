---
title: Orden de precedencia
description: Orden de precedencia
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Metaarchivos de Windows Media, orden de prioridad
- Metaarchivos de Windows Media, prioridad
- metaarchivos, orden de prioridad
- metaarchivos, prioridad
- Windows Media, metaarchivos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9161d1e43f61ae1b1a7231c640e33c4c6ec6527f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075375"
---
# <a name="order-of-precedence"></a><span data-ttu-id="e50ca-108">Orden de precedencia</span><span class="sxs-lookup"><span data-stu-id="e50ca-108">Order of Precedence</span></span>

<span data-ttu-id="e50ca-109">No todos los atributos de elemento de metarchivo se crean igual.</span><span class="sxs-lookup"><span data-stu-id="e50ca-109">Not all metafile element attributes are created equal.</span></span> <span data-ttu-id="e50ca-110">Algunos atributos de elemento de metarchivo invalidan otros atributos de elemento.</span><span class="sxs-lookup"><span data-stu-id="e50ca-110">Some metafile element attributes override other element attributes.</span></span> <span data-ttu-id="e50ca-111">Los atributos de elemento pueden reemplazarse por atributos de elemento similares en función de la posición y el orden.</span><span class="sxs-lookup"><span data-stu-id="e50ca-111">Element attributes can be overridden by similar element attributes depending on position and order.</span></span> <span data-ttu-id="e50ca-112">Los atributos de una lista de reproducción de metarchivo invalidan los contenidos en un archivo de Windows Media al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="e50ca-112">Any attributes of a metafile playlist override those contained in a referenced Windows Media file.</span></span> <span data-ttu-id="e50ca-113">Un atributo que reemplaza a otro tiene mayor precedencia.</span><span class="sxs-lookup"><span data-stu-id="e50ca-113">An attribute that overrides another has higher precedence.</span></span>

<span data-ttu-id="e50ca-114">En la tabla siguiente se muestra la jerarquía de prioridad más alta a la más baja.</span><span class="sxs-lookup"><span data-stu-id="e50ca-114">The hierarchy, highest precedence to lowest, is shown in the following table.</span></span> <span data-ttu-id="e50ca-115">El elemento de prioridad más alto nunca se invalida.</span><span class="sxs-lookup"><span data-stu-id="e50ca-115">The highest precedence item is never overridden.</span></span>



| <span data-ttu-id="e50ca-116">Ámbito</span><span class="sxs-lookup"><span data-stu-id="e50ca-116">Scope</span></span>                    | <span data-ttu-id="e50ca-117">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="e50ca-117">Hierarchy</span></span>                                   |
|--------------------------|---------------------------------------------|
| <span data-ttu-id="e50ca-118">"Contenido DRM firmado"</span><span class="sxs-lookup"><span data-stu-id="e50ca-118">"Signed DRM content"</span></span>     | <span data-ttu-id="e50ca-119">Nunca se invalida.</span><span class="sxs-lookup"><span data-stu-id="e50ca-119">Never overridden.</span></span>                           |
| <span data-ttu-id="e50ca-120">Ámbito del elemento **ref**</span><span class="sxs-lookup"><span data-stu-id="e50ca-120">**REF** element scope</span></span>    | <span data-ttu-id="e50ca-121">Solo se reemplaza por contenido DRM firmado.</span><span class="sxs-lookup"><span data-stu-id="e50ca-121">Only overridden by signed DRM content.</span></span>      |
| <span data-ttu-id="e50ca-122">Ámbito del elemento de **entrada**</span><span class="sxs-lookup"><span data-stu-id="e50ca-122">**ENTRY** element scope</span></span>  | <span data-ttu-id="e50ca-123">Reemplaza los elementos de las categorías siguientes.</span><span class="sxs-lookup"><span data-stu-id="e50ca-123">Overrides elements of the categories below.</span></span> |
| <span data-ttu-id="e50ca-124">Ámbito de **ASX**</span><span class="sxs-lookup"><span data-stu-id="e50ca-124">**ASX** scope</span></span>            | <span data-ttu-id="e50ca-125">Invalida los elementos de archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="e50ca-125">Overrides media file elements.</span></span>              |
| <span data-ttu-id="e50ca-126">Ámbito de archivo de Windows Media</span><span class="sxs-lookup"><span data-stu-id="e50ca-126">Windows Media file scope</span></span> | <span data-ttu-id="e50ca-127">Reemplazado por todo lo anterior.</span><span class="sxs-lookup"><span data-stu-id="e50ca-127">Overridden by all of the above.</span></span>             |



 

-   <span data-ttu-id="e50ca-128">"Contenido DRM firmado": objeto de firma digital.</span><span class="sxs-lookup"><span data-stu-id="e50ca-128">"Signed DRM content" - Digital signature object.</span></span>

    <span data-ttu-id="e50ca-129">Los atributos de contenido DRM firmado reemplazarán a todos los demás.</span><span class="sxs-lookup"><span data-stu-id="e50ca-129">Attributes of Signed DRM content will override all others.</span></span> <span data-ttu-id="e50ca-130">Por ejemplo, la información de copyright de "contenido DRM firmado" no se invalidará.</span><span class="sxs-lookup"><span data-stu-id="e50ca-130">For example, the Copyright information of "Signed DRM content" will not be overridden.</span></span> <span data-ttu-id="e50ca-131">Siempre se transmitirá por secuencias y se presentará.</span><span class="sxs-lookup"><span data-stu-id="e50ca-131">It will always be streamed and presented.</span></span>

-   <span data-ttu-id="e50ca-132">Ámbito del elemento **ref**</span><span class="sxs-lookup"><span data-stu-id="e50ca-132">**REF** element scope</span></span>

    <span data-ttu-id="e50ca-133">Los atributos del elemento **ref** reemplazarán a otros atributos de elemento, pero no a contenido DRM firmado.</span><span class="sxs-lookup"><span data-stu-id="e50ca-133">Attributes of the **REF** element will override other element attributes, but not signed DRM content.</span></span>

-   <span data-ttu-id="e50ca-134">Ámbito de **entrada**</span><span class="sxs-lookup"><span data-stu-id="e50ca-134">**ENTRY** scope</span></span>

    <span data-ttu-id="e50ca-135">El atributo de elemento de **referencia** invalidará los atributos del elemento de **entrada** , pero invalidará otros atributos de elemento.</span><span class="sxs-lookup"><span data-stu-id="e50ca-135">Attributes of the **ENTRY** element will be overridden by the **REF** element attribute but will override other element attributes.</span></span> <span data-ttu-id="e50ca-136">Los metadatos de **título** del elemento de **entrada** se muestran en lugar de la información de título del archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="e50ca-136">**TITLE** metadata from the **ENTRY** element is displayed instead of the title information from the media file.</span></span>

-   <span data-ttu-id="e50ca-137">Ámbito de **ASX**</span><span class="sxs-lookup"><span data-stu-id="e50ca-137">**ASX** scope</span></span>

    <span data-ttu-id="e50ca-138">Las propiedades que se escriban en el metarchivo invalidarán las contenidas en el archivo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e50ca-138">Any properties that are entered in the metafile override those contained in the Windows Media file.</span></span> <span data-ttu-id="e50ca-139">Los atributos del elemento de **entrada** reemplazan los atributos del elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="e50ca-139">Attributes of the **ENTRY** element override **ASX** element attributes.</span></span> <span data-ttu-id="e50ca-140">Mientras se reproduce el clip multimedia al que se hace referencia del elemento de **entrada** , se muestran los metadatos del **título** del elemento de **entrada** en lugar de la información de título del elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="e50ca-140">While the **ENTRY** element's referenced media clip is playing, **TITLE** metadata from the **ENTRY** element is displayed instead of title information from the **ASX** element.</span></span>

-   <span data-ttu-id="e50ca-141">Ámbito de archivo de Windows Media</span><span class="sxs-lookup"><span data-stu-id="e50ca-141">Windows Media file scope</span></span>

    <span data-ttu-id="e50ca-142">Los atributos de metarchivo reemplazan a los atributos del archivo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e50ca-142">Attributes of the Windows Media file are overridden by any metafile attributes.</span></span> <span data-ttu-id="e50ca-143">Los metadatos del archivo multimedia se muestran solo si no hay metadatos definidos para ese elemento en el metarchivo.</span><span class="sxs-lookup"><span data-stu-id="e50ca-143">Media file metadata is displayed only if there is no metadata defined for that element in the metafile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e50ca-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e50ca-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e50ca-145">**Crear listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="e50ca-145">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="e50ca-146">**Listas de reproducción de metarchivos**</span><span class="sxs-lookup"><span data-stu-id="e50ca-146">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="e50ca-147">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e50ca-147">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="e50ca-148">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e50ca-148">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




