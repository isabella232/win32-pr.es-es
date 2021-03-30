---
description: En el fragmento de código siguiente se muestra cómo solicitar y establecer una dirección de multidifusión para una conferencia.
ms.assetid: faff57a9-88b3-45ce-bf9e-3f7087dfd1fd
title: Adquisición de una dirección de multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb451bb403002a4b2dc347abf51e587d8ea02a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154052"
---
# <a name="acquiring-a-multicast-address"></a><span data-ttu-id="da9ff-103">Adquisición de una dirección de multidifusión</span><span class="sxs-lookup"><span data-stu-id="da9ff-103">Acquiring a Multicast Address</span></span>

<span data-ttu-id="da9ff-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="da9ff-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="da9ff-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="da9ff-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="da9ff-106">En el fragmento de código siguiente se muestra cómo solicitar y establecer una dirección de multidifusión para una conferencia.</span><span class="sxs-lookup"><span data-stu-id="da9ff-106">The following code fragment illustrates how to request and set a multicast address for a conference.</span></span>

<span data-ttu-id="da9ff-107">Por motivos de simplicidad, este fragmento muestra la asignación de una dirección de multidifusión a un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="da9ff-107">For the sake of simplicity, this fragment shows the assignment of one multicast address to one media item.</span></span> <span data-ttu-id="da9ff-108">En realidad, la selección de un ámbito, la solicitud de dirección de multidifusión y la asignación se realizarán para cada elemento multimedia implicado en la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="da9ff-108">In actuality, the selection of a scope, the multicast address request, and the assignment will be performed for every media item involved in the conference.</span></span>

<span data-ttu-id="da9ff-109">Este fragmento supone que ya se ha realizado la [conexión a un servidor ILS](connecting-to-an-ils-server.md) .</span><span class="sxs-lookup"><span data-stu-id="da9ff-109">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span> <span data-ttu-id="da9ff-110">Las operaciones que se muestran aquí se realizarían en la sección "modificar la configuración si es necesario" de [creación de un anuncio de conferencia](creating-a-conference-announcement.md).</span><span class="sxs-lookup"><span data-stu-id="da9ff-110">The operations shown here would be performed in the "Modify the settings if necessary" section of [Creating a Conference Announcement](creating-a-conference-announcement.md).</span></span>


```C++
// If ( hr != S_OK ) process the error here.
```



## <a name="related-topics"></a><span data-ttu-id="da9ff-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="da9ff-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da9ff-112">Interfaces COM multidifusión</span><span class="sxs-lookup"><span data-stu-id="da9ff-112">Multicast COM Interfaces</span></span>](multicast-com-interfaces.md)
</dt> <dt>

[<span data-ttu-id="da9ff-113">**IMcastAddressAllocation**</span><span class="sxs-lookup"><span data-stu-id="da9ff-113">**IMcastAddressAllocation**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)
</dt> <dt>

[<span data-ttu-id="da9ff-114">**IMcastScope**</span><span class="sxs-lookup"><span data-stu-id="da9ff-114">**IMcastScope**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)
</dt> <dt>

[<span data-ttu-id="da9ff-115">**IMcastLeaseInfo**</span><span class="sxs-lookup"><span data-stu-id="da9ff-115">**IMcastLeaseInfo**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)
</dt> <dt>

[<span data-ttu-id="da9ff-116">**IEnumMcastScope**</span><span class="sxs-lookup"><span data-stu-id="da9ff-116">**IEnumMcastScope**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)
</dt> <dt>

[<span data-ttu-id="da9ff-117">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="da9ff-117">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="da9ff-118">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="da9ff-118">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="da9ff-119">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="da9ff-119">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> <dt>

[<span data-ttu-id="da9ff-120">**IEnumBstr**</span><span class="sxs-lookup"><span data-stu-id="da9ff-120">**IEnumBstr**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr)
</dt> <dt>

[<span data-ttu-id="da9ff-121">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="da9ff-121">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="da9ff-122">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="da9ff-122">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 



