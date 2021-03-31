---
title: Objeto DownloadManager
description: Objeto DownloadManager
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Windows Media Player tiendas en línea, objeto DownloadManager
- tiendas en línea, objeto DownloadManager
- tipo 2 tiendas en línea, objeto DownloadManager
- DownloadManager
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3555ee7b99c97e85ce856766bd9f670aac4229b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903575"
---
# <a name="downloadmanager-object"></a><span data-ttu-id="4d456-107">Objeto DownloadManager</span><span class="sxs-lookup"><span data-stu-id="4d456-107">DownloadManager Object</span></span>

> [!Note]  
> <span data-ttu-id="4d456-108">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="4d456-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="4d456-109">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="4d456-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="4d456-110">El objeto **Downloadmanager** es el objeto raíz para el administrador de descargas de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4d456-110">The **DownloadManager** object is the root object for the Windows Media Player Download Manager.</span></span> <span data-ttu-id="4d456-111">Lo pueden usar las páginas web que se hospedan en los paneles de tareas de servicio de tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="4d456-111">It can be used by webpages that are hosted in online store service task panes.</span></span>

<span data-ttu-id="4d456-112">El objeto **Downloadmanager** admite los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="4d456-112">The **DownloadManager** object supports the following methods.</span></span>



| <span data-ttu-id="4d456-113">Método</span><span class="sxs-lookup"><span data-stu-id="4d456-113">Method</span></span>                                                                   | <span data-ttu-id="4d456-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d456-114">Description</span></span>                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="4d456-115">createDownloadCollection</span><span class="sxs-lookup"><span data-stu-id="4d456-115">createDownloadCollection</span></span>](downloadmanager-createdownloadcollection.md) | <span data-ttu-id="4d456-116">Crea una colección de descargas vacía.</span><span class="sxs-lookup"><span data-stu-id="4d456-116">Creates an empty download collection.</span></span>        |
| [<span data-ttu-id="4d456-117">getDownloadCollection</span><span class="sxs-lookup"><span data-stu-id="4d456-117">getDownloadCollection</span></span>](downloadmanager-getdownloadcollection.md)       | <span data-ttu-id="4d456-118">Recupera la colección de descarga especificada.</span><span class="sxs-lookup"><span data-stu-id="4d456-118">Retrieves the specified download collection.</span></span> |



 

<span data-ttu-id="4d456-119">Se tiene acceso al objeto **Downloadmanager** mediante **external. DownloadManager**.</span><span class="sxs-lookup"><span data-stu-id="4d456-119">The **DownloadManager** object is accessed by using **external.DownloadManager**.</span></span> <span data-ttu-id="4d456-120">A efectos de Ilustración, se supone que este valor se ha asignado a una variable denominada "DownloadManager", que se usará para identificar este objeto en las secciones de sintaxis de referencia.</span><span class="sxs-lookup"><span data-stu-id="4d456-120">For illustration purposes, it is assumed that this value has been assigned to a variable named "DownloadManager", which will be used to identify this object in the reference syntax sections.</span></span>

<span data-ttu-id="4d456-121">En Windows Media Player 10 o versiones posteriores, solo se puede tener acceso a la propiedad y el objeto **Downloadmanager** desde los paneles de tareas servicio de tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="4d456-121">In Windows Media Player 10 or later, the **DownloadManager** property and object are accessible only from online store service task panes.</span></span> <span data-ttu-id="4d456-122">No se puede usar el **Downloadmanager** de otras características en las que el objeto **externo** está disponible, como HTMLView, la vista del centro de información y la información del álbum.</span><span class="sxs-lookup"><span data-stu-id="4d456-122">You cannot use the **DownloadManager** from other features where the **External** object is available, such as HTMLView, Info Center View, and album information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d456-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d456-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d456-124">**Referencia de las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="4d456-124">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




