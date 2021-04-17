---
title: Objeto DownloadItem
description: Objeto DownloadItem
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Windows Media Player tiendas en línea, objeto DownloadItem
- tiendas en línea, objeto DownloadItem
- tipo 2 tiendas en línea, objeto DownloadItem
- DownloadItem
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c367eee37f2f4d8329d71f3d42a3c78771a50a6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695472"
---
# <a name="downloaditem-object"></a><span data-ttu-id="a5598-107">Objeto DownloadItem</span><span class="sxs-lookup"><span data-stu-id="a5598-107">DownloadItem Object</span></span>

> [!Note]  
> <span data-ttu-id="a5598-108">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="a5598-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="a5598-109">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="a5598-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="a5598-110">El objeto **DownloadItem** representa una solicitud de descarga de archivos.</span><span class="sxs-lookup"><span data-stu-id="a5598-110">The **DownloadItem** object represents a file download request.</span></span> <span data-ttu-id="a5598-111">Las páginas web que se hospedan en el modo completo de Windows Media Player y que tienen acceso al objeto **externo** , como los servicios Premium, pueden usarlas.</span><span class="sxs-lookup"><span data-stu-id="a5598-111">It can be used by webpages that are hosted in the full mode Windows Media Player and that have access to the **External** object, such as premium services.</span></span>

<span data-ttu-id="a5598-112">El objeto **DownloadItem** admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="a5598-112">The **DownloadItem** object supports the following properties.</span></span>



| <span data-ttu-id="a5598-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a5598-113">Property</span></span>                                        | <span data-ttu-id="a5598-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5598-114">Description</span></span>                                      |
|-------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="a5598-115">downloadState</span><span class="sxs-lookup"><span data-stu-id="a5598-115">downloadState</span></span>](downloaditem-downloadstate.md) | <span data-ttu-id="a5598-116">Recupera el estado de la descarga.</span><span class="sxs-lookup"><span data-stu-id="a5598-116">Retrieves the state of the download.</span></span>             |
| [<span data-ttu-id="a5598-117">progreso</span><span class="sxs-lookup"><span data-stu-id="a5598-117">progress</span></span>](downloaditem-progress.md)           | <span data-ttu-id="a5598-118">Recupera el progreso de la descarga en bytes.</span><span class="sxs-lookup"><span data-stu-id="a5598-118">Retrieves the progress of the download in bytes.</span></span> |
| [<span data-ttu-id="a5598-119">size</span><span class="sxs-lookup"><span data-stu-id="a5598-119">size</span></span>](downloaditem-size.md)                   | <span data-ttu-id="a5598-120">Recupera el tamaño de la descarga.</span><span class="sxs-lookup"><span data-stu-id="a5598-120">Retrieves the size of the download.</span></span>              |
| [<span data-ttu-id="a5598-121">sourceURL</span><span class="sxs-lookup"><span data-stu-id="a5598-121">sourceURL</span></span>](downloaditem-sourceurl.md)         | <span data-ttu-id="a5598-122">Recupera la dirección URL de origen de la descarga.</span><span class="sxs-lookup"><span data-stu-id="a5598-122">Retrieves the source URL of the download.</span></span>        |
| [<span data-ttu-id="a5598-123">type</span><span class="sxs-lookup"><span data-stu-id="a5598-123">type</span></span>](downloaditem-type.md)                   | <span data-ttu-id="a5598-124">Recupera el tipo de la descarga.</span><span class="sxs-lookup"><span data-stu-id="a5598-124">Retrieves the type of the download.</span></span>              |



 

<span data-ttu-id="a5598-125">El objeto **DownloadItem** admite los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="a5598-125">The **DownloadItem** object supports the following methods.</span></span>



| <span data-ttu-id="a5598-126">Método</span><span class="sxs-lookup"><span data-stu-id="a5598-126">Method</span></span>                                      | <span data-ttu-id="a5598-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5598-127">Description</span></span>                                                |
|---------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="a5598-128">cancel</span><span class="sxs-lookup"><span data-stu-id="a5598-128">cancel</span></span>](downloaditem-cancel.md)           | <span data-ttu-id="a5598-129">Cancela la descarga.</span><span class="sxs-lookup"><span data-stu-id="a5598-129">Cancels the download.</span></span>                                      |
| [<span data-ttu-id="a5598-130">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="a5598-130">getItemInfo</span></span>](downloaditem-getiteminfo.md) | <span data-ttu-id="a5598-131">Recupera el valor de un atributo para el elemento de descarga.</span><span class="sxs-lookup"><span data-stu-id="a5598-131">Retrieves the value of an attribute for the download item.</span></span> |
| [<span data-ttu-id="a5598-132">pause</span><span class="sxs-lookup"><span data-stu-id="a5598-132">pause</span></span>](downloaditem-pause.md)             | <span data-ttu-id="a5598-133">Pausa la descarga.</span><span class="sxs-lookup"><span data-stu-id="a5598-133">Pauses the download.</span></span>                                       |
| [<span data-ttu-id="a5598-134">Recuper</span><span class="sxs-lookup"><span data-stu-id="a5598-134">resume</span></span>](downloaditem-resume.md)           | <span data-ttu-id="a5598-135">Reanuda la descarga.</span><span class="sxs-lookup"><span data-stu-id="a5598-135">Resumes the download.</span></span>                                      |



 

<span data-ttu-id="a5598-136">Se tiene acceso al objeto **DownloadItem** a través de la propiedad siguiente.</span><span class="sxs-lookup"><span data-stu-id="a5598-136">The **DownloadItem** object is accessed through the following property.</span></span>



| <span data-ttu-id="a5598-137">Object</span><span class="sxs-lookup"><span data-stu-id="a5598-137">Object</span></span>                                              | <span data-ttu-id="a5598-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a5598-138">Property</span></span>                            |
|-----------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="a5598-139">DownloadCollection</span><span class="sxs-lookup"><span data-stu-id="a5598-139">DownloadCollection</span></span>](downloadcollection-object.md) | [<span data-ttu-id="a5598-140">item</span><span class="sxs-lookup"><span data-stu-id="a5598-140">item</span></span>](downloadcollection-item.md) |



 

<span data-ttu-id="a5598-141">A efectos de Ilustración, **Downloadmanager**. **getDownloadCollection**(*collectionId*). **Item**(*Itemid*) se usa en las secciones de sintaxis de referencia.</span><span class="sxs-lookup"><span data-stu-id="a5598-141">For purposes of illustration, **DownloadManager**.**getDownloadCollection**(*collectionId*).**item**(*itemId*) is used in the reference syntax sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5598-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5598-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5598-143">**Referencia de las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="a5598-143">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




