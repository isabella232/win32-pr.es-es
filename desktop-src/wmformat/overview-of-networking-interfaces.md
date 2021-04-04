---
title: Información general de las interfaces de red
description: Información general de las interfaces de red
ms.assetid: 7aa7ff1b-9c81-4fee-afa9-2a9eed457360
keywords:
- SDK de Windows Media Format, interfaces de red
- SDK de Windows Media Format, interfaces
- Advanced Systems Format (ASF), interfaces de red
- ASF (formato de sistemas avanzados), interfaces de red
- Advanced Systems Format (ASF), lista de interfaces para características de red
- ASF (formato de sistemas avanzados), lista de interfaces para características de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd1c235e7e8b36964993bb24ce30977446d9af8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789244"
---
# <a name="overview-of-networking-interfaces"></a><span data-ttu-id="b9b18-109">Información general de las interfaces de red</span><span class="sxs-lookup"><span data-stu-id="b9b18-109">Overview of Networking Interfaces</span></span>

<span data-ttu-id="b9b18-110">Las características de red de este SDK se admiten a través de métodos de las interfaces siguientes.</span><span class="sxs-lookup"><span data-stu-id="b9b18-110">The networking features of this SDK are supported through methods of the following interfaces.</span></span>



| <span data-ttu-id="b9b18-111">Interfaz</span><span class="sxs-lookup"><span data-stu-id="b9b18-111">Interface</span></span>                                                  | <span data-ttu-id="b9b18-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9b18-112">Description</span></span>                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9b18-113">**IWMClientConnections**</span><span class="sxs-lookup"><span data-stu-id="b9b18-113">**IWMClientConnections**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)       | <span data-ttu-id="b9b18-114">Obtiene información acerca de los clientes conectados a un receptor de red.</span><span class="sxs-lookup"><span data-stu-id="b9b18-114">Gets information about the clients connected to a network sink.</span></span>                                                                                       |
| [<span data-ttu-id="b9b18-115">**IWMClientConnections2**</span><span class="sxs-lookup"><span data-stu-id="b9b18-115">**IWMClientConnections2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2)     | <span data-ttu-id="b9b18-116">Proporciona un método para obtener información acerca de un cliente conectado a un receptor de red del escritor.</span><span class="sxs-lookup"><span data-stu-id="b9b18-116">Provides a method to get information about a client attached to a writer network sink.</span></span> <span data-ttu-id="b9b18-117">Esta interfaz extiende la interfaz **IWMClientConnections** .</span><span class="sxs-lookup"><span data-stu-id="b9b18-117">This interface extends the **IWMClientConnections** interface.</span></span> |
| [<span data-ttu-id="b9b18-118">**IWMCredentialCallback**</span><span class="sxs-lookup"><span data-stu-id="b9b18-118">**IWMCredentialCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)     | <span data-ttu-id="b9b18-119">Proporciona un método de devolución de llamada para adquirir las credenciales de usuario al obtener acceso a un sitio remoto.</span><span class="sxs-lookup"><span data-stu-id="b9b18-119">Provides a callback method to acquire user credentials when accessing a remote site.</span></span>                                                                  |
| [<span data-ttu-id="b9b18-120">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="b9b18-120">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)           | <span data-ttu-id="b9b18-121">Proporciona métodos avanzados en el objeto de lector.</span><span class="sxs-lookup"><span data-stu-id="b9b18-121">Provides advanced methods on the reader object.</span></span>                                                                                                       |
| [<span data-ttu-id="b9b18-122">**IWMReaderAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="b9b18-122">**IWMReaderAdvanced3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)           | <span data-ttu-id="b9b18-123">Extiende la interfaz **IWMReaderAdvanced2** .</span><span class="sxs-lookup"><span data-stu-id="b9b18-123">Extends the **IWMReaderAdvanced2** interface.</span></span>                                                                                                         |
| [<span data-ttu-id="b9b18-124">**IWMReaderAdvanced4**</span><span class="sxs-lookup"><span data-stu-id="b9b18-124">**IWMReaderAdvanced4**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)           | <span data-ttu-id="b9b18-125">Extiende la interfaz **IWMReaderAdvanced3** .</span><span class="sxs-lookup"><span data-stu-id="b9b18-125">Extends the **IWMReaderAdvanced3** interface.</span></span>                                                                                                         |
| [<span data-ttu-id="b9b18-126">**IWMReaderNetworkConfig**</span><span class="sxs-lookup"><span data-stu-id="b9b18-126">**IWMReaderNetworkConfig**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)   | <span data-ttu-id="b9b18-127">Configura las opciones de red en el objeto de lector.</span><span class="sxs-lookup"><span data-stu-id="b9b18-127">Configures the network settings on the reader object.</span></span>                                                                                                 |
| [<span data-ttu-id="b9b18-128">**IWMReaderNetworkConfig2**</span><span class="sxs-lookup"><span data-stu-id="b9b18-128">**IWMReaderNetworkConfig2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) | <span data-ttu-id="b9b18-129">Configura opciones de red adicionales en el objeto de lector.</span><span class="sxs-lookup"><span data-stu-id="b9b18-129">Configures additional network settings on the reader object.</span></span> <span data-ttu-id="b9b18-130">Esta interfaz extiende la interfaz **IWMReaderNetworkConfig** .</span><span class="sxs-lookup"><span data-stu-id="b9b18-130">This interface extends the **IWMReaderNetworkConfig** interface.</span></span>                         |
| [<span data-ttu-id="b9b18-131">**IWMWriterNetworkSink**</span><span class="sxs-lookup"><span data-stu-id="b9b18-131">**IWMWriterNetworkSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)       | <span data-ttu-id="b9b18-132">Configura el objeto de receptor de red, que se utiliza para escribir medios digitales en una red.</span><span class="sxs-lookup"><span data-stu-id="b9b18-132">Configures the network sink object, which is used to write digital media to a network.</span></span>                                                                |
| [<span data-ttu-id="b9b18-133">**IWMWriterPushSink**</span><span class="sxs-lookup"><span data-stu-id="b9b18-133">**IWMWriterPushSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)             | <span data-ttu-id="b9b18-134">Configura el objeto de receptor de la extracción, que se utiliza para distribuir medios digitales a puntos de publicación.</span><span class="sxs-lookup"><span data-stu-id="b9b18-134">Configures the push sink object, which is used to distribute digital media to publishing points.</span></span>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="b9b18-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9b18-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9b18-136">**Implementación de la funcionalidad de red**</span><span class="sxs-lookup"><span data-stu-id="b9b18-136">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> </dl>

 

 




