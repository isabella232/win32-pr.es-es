---
title: Objeto DownloadCollection
description: Objeto DownloadCollection
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Windows Media Player tiendas en línea, objeto DownloadCollection
- tiendas en línea, objeto DownloadCollection
- tipo 2 tiendas en línea, objeto DownloadCollection
- DownloadCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8275cbd2661bdce9c428800206c14b9c55942c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695388"
---
# <a name="downloadcollection-object"></a><span data-ttu-id="4224a-107">Objeto DownloadCollection</span><span class="sxs-lookup"><span data-stu-id="4224a-107">DownloadCollection Object</span></span>

> [!Note]  
> <span data-ttu-id="4224a-108">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="4224a-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="4224a-109">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="4224a-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="4224a-110">El objeto **DownloadCollection** contiene propiedades y métodos para controlar las colecciones de elementos de descarga.</span><span class="sxs-lookup"><span data-stu-id="4224a-110">The **DownloadCollection** object contains properties and methods to handle collections of download items.</span></span> <span data-ttu-id="4224a-111">Las páginas web que se hospedan en el modo completo de Windows Media Player y que tienen acceso al objeto **externo** , como las tiendas en línea, pueden usarlas.</span><span class="sxs-lookup"><span data-stu-id="4224a-111">It can be used by webpages that are hosted in the full mode Windows Media Player and that have access to the **External** object, such as online stores.</span></span>

<span data-ttu-id="4224a-112">El objeto **DownloadCollection** admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="4224a-112">The **DownloadCollection** object supports the following properties.</span></span>



| <span data-ttu-id="4224a-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4224a-113">Property</span></span>                              | <span data-ttu-id="4224a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4224a-114">Description</span></span>                                  |
|---------------------------------------|----------------------------------------------|
| [<span data-ttu-id="4224a-115">count</span><span class="sxs-lookup"><span data-stu-id="4224a-115">count</span></span>](downloadcollection-count.md) | <span data-ttu-id="4224a-116">Recupera el número de descargas pendientes.</span><span class="sxs-lookup"><span data-stu-id="4224a-116">Retrieves the number of pending downloads.</span></span>   |
| [<span data-ttu-id="4224a-117">id</span><span class="sxs-lookup"><span data-stu-id="4224a-117">id</span></span>](downloadcollection-id.md)       | <span data-ttu-id="4224a-118">Recupera el identificador de la colección de descargas.</span><span class="sxs-lookup"><span data-stu-id="4224a-118">Retrieves the ID of the download collection.</span></span> |



 

<span data-ttu-id="4224a-119">El objeto **DownloadCollection** admite los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="4224a-119">The **DownloadCollection** object supports the following methods.</span></span>



| <span data-ttu-id="4224a-120">Método</span><span class="sxs-lookup"><span data-stu-id="4224a-120">Method</span></span>                                                | <span data-ttu-id="4224a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="4224a-121">Description</span></span>                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="4224a-122">Borrar</span><span class="sxs-lookup"><span data-stu-id="4224a-122">Clear</span></span>](downloadcollection-clear.md)                 | <span data-ttu-id="4224a-123">Quita todos los elementos de una colección de descarga.</span><span class="sxs-lookup"><span data-stu-id="4224a-123">Removes all items from a download collection.</span></span> |
| [<span data-ttu-id="4224a-124">item</span><span class="sxs-lookup"><span data-stu-id="4224a-124">item</span></span>](downloadcollection-item.md)                   | <span data-ttu-id="4224a-125">Recupera un objeto de descarga pendiente.</span><span class="sxs-lookup"><span data-stu-id="4224a-125">Retrieves a pending download object.</span></span>          |
| [<span data-ttu-id="4224a-126">removeItem</span><span class="sxs-lookup"><span data-stu-id="4224a-126">removeItem</span></span>](downloadcollection-removeitem.md)       | <span data-ttu-id="4224a-127">Quita un elemento de descarga de una colección.</span><span class="sxs-lookup"><span data-stu-id="4224a-127">Removes a download item from a collection.</span></span>    |
| [<span data-ttu-id="4224a-128">startDownload</span><span class="sxs-lookup"><span data-stu-id="4224a-128">startDownload</span></span>](downloadcollection-startdownload.md) | <span data-ttu-id="4224a-129">Pone en cola una descarga.</span><span class="sxs-lookup"><span data-stu-id="4224a-129">Queues a download.</span></span>                            |



 

<span data-ttu-id="4224a-130">Se tiene acceso al objeto **DownloadCollection** a través de los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="4224a-130">The **DownloadCollection** object is accessed through the following methods.</span></span>



| <span data-ttu-id="4224a-131">Object</span><span class="sxs-lookup"><span data-stu-id="4224a-131">Object</span></span>                                        | <span data-ttu-id="4224a-132">Método</span><span class="sxs-lookup"><span data-stu-id="4224a-132">Method</span></span>                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="4224a-133">DownloadManager</span><span class="sxs-lookup"><span data-stu-id="4224a-133">DownloadManager</span></span>](downloadmanager-object.md) | [<span data-ttu-id="4224a-134">createDownloadCollection</span><span class="sxs-lookup"><span data-stu-id="4224a-134">createDownloadCollection</span></span>](downloadmanager-createdownloadcollection.md) |
| [<span data-ttu-id="4224a-135">DownloadManager</span><span class="sxs-lookup"><span data-stu-id="4224a-135">DownloadManager</span></span>](downloadmanager-object.md) | [<span data-ttu-id="4224a-136">getDownloadCollection</span><span class="sxs-lookup"><span data-stu-id="4224a-136">getDownloadCollection</span></span>](downloadmanager-getdownloadcollection.md)       |



 

<span data-ttu-id="4224a-137">A efectos de Ilustración, **Downloadmanager**. **getDownloadCollection**(*collectionId*) se usa en las secciones de sintaxis de referencia.</span><span class="sxs-lookup"><span data-stu-id="4224a-137">For purposes of illustration, **DownloadManager**.**getDownloadCollection**(*collectionId*) is used in the reference syntax sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4224a-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4224a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4224a-139">**Referencia de las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="4224a-139">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




