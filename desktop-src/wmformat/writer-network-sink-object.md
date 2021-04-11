---
title: Objeto de receptor de red del escritor
description: Objeto de receptor de red del escritor
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- SDK de Windows Media Format, objetos de receptor de red del escritor
- Advanced Systems Format (ASF), objetos de receptor de red del escritor
- ASF (formato de sistemas avanzados), objetos de receptor de red del sistema de escritura
- objetos, objetos de receptor de red del escritor
- objetos de receptor de red del escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85af356c1d326ddaaf3703ca87c3b7bdd1628b9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104149129"
---
# <a name="writer-network-sink-object"></a><span data-ttu-id="50e53-108">Objeto de receptor de red del escritor</span><span class="sxs-lookup"><span data-stu-id="50e53-108">Writer Network Sink Object</span></span>

<span data-ttu-id="50e53-109">El objeto de receptor de red del escritor se utiliza para escribir medios digitales en una red.</span><span class="sxs-lookup"><span data-stu-id="50e53-109">The writer network sink object is used to write digital media to a network.</span></span>

<span data-ttu-id="50e53-110">La función [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)crea el objeto de receptor de red del escritor, que establece un puntero a una interfaz **IWMWriterNetworkSink** .</span><span class="sxs-lookup"><span data-stu-id="50e53-110">The writer network sink object is created by the function [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink), which sets a pointer to an **IWMWriterNetworkSink** interface.</span></span> <span data-ttu-id="50e53-111">Las demás interfaces del objeto de receptor de red del escritor se pueden obtener llamando al método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="50e53-111">The other interfaces of the writer network sink object can be obtained by calling the **QueryInterface** method.</span></span>



| <span data-ttu-id="50e53-112">Interfaz</span><span class="sxs-lookup"><span data-stu-id="50e53-112">Interface</span></span>                                              | <span data-ttu-id="50e53-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="50e53-113">Description</span></span>                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50e53-114">**IWMClientConnections**</span><span class="sxs-lookup"><span data-stu-id="50e53-114">**IWMClientConnections**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | <span data-ttu-id="50e53-115">Recopila información sobre los clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="50e53-115">Collects information on connected clients.</span></span>                                                                                                                                                                      |
| [<span data-ttu-id="50e53-116">**IWMClientConnections2**</span><span class="sxs-lookup"><span data-stu-id="50e53-116">**IWMClientConnections2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | <span data-ttu-id="50e53-117">Recupera información de cliente avanzada.</span><span class="sxs-lookup"><span data-stu-id="50e53-117">Retrieves advanced client information.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="50e53-118">**IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="50e53-118">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | <span data-ttu-id="50e53-119">Permite que la aplicación obtenga mensajes de estado del objeto.</span><span class="sxs-lookup"><span data-stu-id="50e53-119">Enables the application to get status messages from the object.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="50e53-120">**IWMWriterNetworkSink**</span><span class="sxs-lookup"><span data-stu-id="50e53-120">**IWMWriterNetworkSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | <span data-ttu-id="50e53-121">Abre y cierra los puertos, establece y recupera el número máximo de clientes que pueden conectarse al objeto de receptor, establece el protocolo de red que va a usar el objeto de escritor y realiza otras funciones avanzadas.</span><span class="sxs-lookup"><span data-stu-id="50e53-121">Opens and closes ports, sets and retrieves the maximum number of clients that can connect to the sink object, sets the network protocol to be used by the writer object, and performs other advanced functions.</span></span> |
| [<span data-ttu-id="50e53-122">**IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="50e53-122">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | <span data-ttu-id="50e53-123">Asigna memoria, determina si el receptor está funcionando en tiempo real y controla varias funciones de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="50e53-123">Allocates memory, determines whether the sink is operating in real time, and handles several callback functions.</span></span>                                                                                                |



 

<span data-ttu-id="50e53-124">La aplicación puede implementar la siguiente interfaz de devolución de llamada para realizar el seguimiento del progreso de un objeto de receptor de red del escritor.</span><span class="sxs-lookup"><span data-stu-id="50e53-124">The following callback interface can be implemented by the application to track the progress of a writer network sink object.</span></span>



| <span data-ttu-id="50e53-125">Interfaz</span><span class="sxs-lookup"><span data-stu-id="50e53-125">Interface</span></span>                                      | <span data-ttu-id="50e53-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="50e53-126">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="50e53-127">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="50e53-127">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="50e53-128">Obligatorio cuando la información de estado se debe comunicar a la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="50e53-128">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="50e53-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50e53-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50e53-130">**Difusión de datos de ASF**</span><span class="sxs-lookup"><span data-stu-id="50e53-130">**Broadcasting ASF Data**</span></span>](broadcasting-asf-data.md)
</dt> <dt>

[<span data-ttu-id="50e53-131">**de la empresa**</span><span class="sxs-lookup"><span data-stu-id="50e53-131">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="50e53-132">**Trabajar con receptores de escritor**</span><span class="sxs-lookup"><span data-stu-id="50e53-132">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




