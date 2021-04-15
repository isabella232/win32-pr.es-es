---
title: Contenedores de contenido
description: Contenedores de contenido
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Windows Media Player tiendas en línea, contenedores de contenido
- tiendas en línea, contenedores de contenido
- tipo 1 almacenes en línea, contenedores de contenido
- Windows Media Player tiendas en línea, interfaz IWMPContentContainer
- tiendas en línea, interfaz IWMPContentContainer
- tipo 1 tiendas en línea, interfaz IWMPContentContainer
- Windows Media Player, contenedores de contenido
- Windows Media Player, interfaz IWMPContentContainer
- contenedores de contenido
- IWMPContentContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801816c3e26920f3d0869190fc1101d6017a524e
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "105695570"
---
# <a name="content-containers"></a><span data-ttu-id="e6681-113">Contenedores de contenido</span><span class="sxs-lookup"><span data-stu-id="e6681-113">Content Containers</span></span>

<span data-ttu-id="e6681-114">Windows Media Player utiliza contenedores de contenido para representar el contenido multimedia digital en una transacción de descarga o compra de suscripción.</span><span class="sxs-lookup"><span data-stu-id="e6681-114">Windows Media Player uses content containers to represent digital media content in a subscription download or purchase transaction.</span></span> <span data-ttu-id="e6681-115">Un contenedor de contenido se representa mediante la interfaz **IWMPContentContainer** .</span><span class="sxs-lookup"><span data-stu-id="e6681-115">A content container is represented by the **IWMPContentContainer** interface.</span></span> <span data-ttu-id="e6681-116">Un contenedor de contenido podría contener una lista de contenido relacionado, como un álbum, o un conjunto de elementos de contenido no relacionados o *pistas*.</span><span class="sxs-lookup"><span data-stu-id="e6681-116">A content container might contain a list of related content, such as an album, or a set of unrelated content items, or *tracks*.</span></span> <span data-ttu-id="e6681-117">Puede usar la interfaz **IWMPContentContainer** para enumerar las pistas del contenedor de contenido y recuperar el precio de cada pista. También puede recuperar información sobre el propio contenedor de contenido, como el identificador del contenedor, el tipo de contenido del contenedor y el precio total de las pistas del contenedor (que podrían diferir de la suma de los precios de las pistas individuales, como en el caso de una compra de álbum).</span><span class="sxs-lookup"><span data-stu-id="e6681-117">You can use the **IWMPContentContainer** interface to enumerate the tracks of the content container and retrieve the price of each track. You can also retrieve information about the content container itself, such as the container ID, the type of content in the container, and the total price for the tracks in the container (which might differ from the sum of the prices of the individual tracks, as in the case of an album purchase).</span></span>

<span data-ttu-id="e6681-118">Para proporcionar un mecanismo para empaquetar varios contenedores de contenido en un único objeto, Windows Media Player admite la interfaz **IWMPContentContainerList** .</span><span class="sxs-lookup"><span data-stu-id="e6681-118">To provide a mechanism for packaging multiple content containers into a single object, Windows Media Player supports the **IWMPContentContainerList** interface.</span></span> <span data-ttu-id="e6681-119">**IWMPContentContainerList** proporciona métodos para enumerar y recuperar los contenedores de contenido de la lista.</span><span class="sxs-lookup"><span data-stu-id="e6681-119">**IWMPContentContainerList** provides methods to enumerate and retrieve the content containers in the list.</span></span> <span data-ttu-id="e6681-120">Para detectar si la lista de contenedores de contenido representa una descarga de compra o de suscripción, llame a [IWMPContentContainerList:: GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) para recuperar un valor de [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) .</span><span class="sxs-lookup"><span data-stu-id="e6681-120">To discover whether the content container list represents a purchase or a subscription download, call [IWMPContentContainerList::GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) to retrieve a [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6681-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e6681-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6681-122">**Acerca de las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="e6681-122">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e6681-123">**Interfaz IWMPContentContainer**</span><span class="sxs-lookup"><span data-stu-id="e6681-123">**IWMPContentContainer Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[<span data-ttu-id="e6681-124">**Interfaz IWMPContentContainerList**</span><span class="sxs-lookup"><span data-stu-id="e6681-124">**IWMPContentContainerList Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 




