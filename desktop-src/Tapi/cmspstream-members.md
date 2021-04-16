---
description: La lista siguiente contiene los miembros de CMSPStream.
ms.assetid: 792a29ac-ebbb-4bb2-bebf-fbf870b18e84
title: Miembros de CMSPStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacee41ff95cdf16c7cd50c2e39017d9dfa7e83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156565"
---
# <a name="cmspstream-members"></a><span data-ttu-id="1ea48-103">Miembros de CMSPStream</span><span class="sxs-lookup"><span data-stu-id="1ea48-103">CMSPStream Members</span></span>



| <span data-ttu-id="1ea48-104">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="1ea48-104">Member type</span></span>                     | <span data-ttu-id="1ea48-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="1ea48-105">Name</span></span>                | <span data-ttu-id="1ea48-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ea48-106">Description</span></span>                                                                                                                                |
|---------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ea48-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="1ea48-107">IUnknown</span></span>                        | <span data-ttu-id="1ea48-108">\*m \_ pFTM</span><span class="sxs-lookup"><span data-stu-id="1ea48-108">\*m\_pFTM</span></span>           | <span data-ttu-id="1ea48-109">Puntero al serializador de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="1ea48-109">Pointer to the free threaded marshaller.</span></span>                                                                                                   |
| <span data-ttu-id="1ea48-110">DWORD</span><span class="sxs-lookup"><span data-stu-id="1ea48-110">DWORD</span></span>                           | <span data-ttu-id="1ea48-111">m \_ dwState</span><span class="sxs-lookup"><span data-stu-id="1ea48-111">m\_dwState</span></span>          | <span data-ttu-id="1ea48-112">Estado actual de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1ea48-112">The current state of the stream.</span></span>                                                                                                           |
| <span data-ttu-id="1ea48-113">HANDLE</span><span class="sxs-lookup"><span data-stu-id="1ea48-113">HANDLE</span></span>                          | <span data-ttu-id="1ea48-114">m \_ hAddress</span><span class="sxs-lookup"><span data-stu-id="1ea48-114">m\_hAddress</span></span>         | <span data-ttu-id="1ea48-115">Dirección en la que se usa esta secuencia.</span><span class="sxs-lookup"><span data-stu-id="1ea48-115">The address on which this stream is being used.</span></span>                                                                                            |
| <span data-ttu-id="1ea48-116">DWORD</span><span class="sxs-lookup"><span data-stu-id="1ea48-116">DWORD</span></span>                           | <span data-ttu-id="1ea48-117">m \_ dwMediaType</span><span class="sxs-lookup"><span data-stu-id="1ea48-117">m\_dwMediaType</span></span>      | <span data-ttu-id="1ea48-118">El [**tipo de medio**](tapimediatype--constants.md) de este flujo (audio, vídeo, etc.).</span><span class="sxs-lookup"><span data-stu-id="1ea48-118">The [**media type**](tapimediatype--constants.md) of this stream (audio, video, etc.).</span></span>                                                    |
| <span data-ttu-id="1ea48-119">Dirección del TERMINAL \_</span><span class="sxs-lookup"><span data-stu-id="1ea48-119">TERMINAL\_DIRECTION</span></span>             | <span data-ttu-id="1ea48-120">\_Dirección m</span><span class="sxs-lookup"><span data-stu-id="1ea48-120">m\_Direction</span></span>        | <span data-ttu-id="1ea48-121">[**Dirección**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) de este flujo (entrante o saliente).</span><span class="sxs-lookup"><span data-stu-id="1ea48-121">The [**direction**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) of this stream (incoming or outgoing).</span></span>                                                         |
| <span data-ttu-id="1ea48-122">CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="1ea48-122">CMSPCallBase</span></span>                    | <span data-ttu-id="1ea48-123">\*m \_ pMSPCall</span><span class="sxs-lookup"><span data-stu-id="1ea48-123">\*m\_pMSPCall</span></span>       | <span data-ttu-id="1ea48-124">Puntero al objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="1ea48-124">Pointer to the call object.</span></span>                                                                                                                |
| <span data-ttu-id="1ea48-125">IGraphBuilder</span><span class="sxs-lookup"><span data-stu-id="1ea48-125">IGraphBuilder</span></span>                   | <span data-ttu-id="1ea48-126">\*m \_ pIGraphBuilder</span><span class="sxs-lookup"><span data-stu-id="1ea48-126">\*m\_pIGraphBuilder</span></span> | <span data-ttu-id="1ea48-127">Puntero a las interfaces del objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="1ea48-127">Pointer to graph object interfaces.</span></span>                                                                                                        |
| <span data-ttu-id="1ea48-128">IMediaControl</span><span class="sxs-lookup"><span data-stu-id="1ea48-128">IMediaControl</span></span>                   | <span data-ttu-id="1ea48-129">\*m \_ pIMediaControl</span><span class="sxs-lookup"><span data-stu-id="1ea48-129">\*m\_pIMediaControl</span></span> | <span data-ttu-id="1ea48-130">Puntero a la interfaz de control de medios.</span><span class="sxs-lookup"><span data-stu-id="1ea48-130">Pointer to the media control interface.</span></span>                                                                                                    |
| <span data-ttu-id="1ea48-131">CMSPArray <ITTerminal \*></span><span class="sxs-lookup"><span data-stu-id="1ea48-131">CMSPArray <ITTerminal \*></span></span> | <span data-ttu-id="1ea48-132">m \_ terminales</span><span class="sxs-lookup"><span data-stu-id="1ea48-132">m\_Terminals</span></span>        | <span data-ttu-id="1ea48-133">Lista de terminales del flujo.</span><span class="sxs-lookup"><span data-stu-id="1ea48-133">The list of terminals on the stream.</span></span>                                                                                                       |
| <span data-ttu-id="1ea48-134">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="1ea48-134">CMSPCritSection</span></span>                 | <span data-ttu-id="1ea48-135">\_bloqueo m</span><span class="sxs-lookup"><span data-stu-id="1ea48-135">m\_lock</span></span>             | <span data-ttu-id="1ea48-136">El bloqueo que protege el objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="1ea48-136">The lock that protects the stream object.</span></span> <span data-ttu-id="1ea48-137">El objeto de secuencia nunca debe adquirir el bloqueo y llamar a un método MSPCall que podría bloquearse.</span><span class="sxs-lookup"><span data-stu-id="1ea48-137">The stream object should never acquire the lock and then call an MSPCall method that might lock.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1ea48-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1ea48-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ea48-139">**CMSPStream**</span><span class="sxs-lookup"><span data-stu-id="1ea48-139">**CMSPStream**</span></span>](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



