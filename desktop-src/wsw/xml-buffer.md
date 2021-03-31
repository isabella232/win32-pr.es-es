---
title: Búfer XML
description: Un búfer XML proporciona un almacenamiento en memoria eficaz para los datos XML arbitrarios.
ms.assetid: e379628b-c6f8-48b1-8109-59fb604f2bcb
keywords:
- Servicios Web de búfer de XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab71121dc451c9ccb186c754d537836f9e899fa9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995747"
---
# <a name="xml-buffer"></a><span data-ttu-id="49cfb-106">Búfer XML</span><span class="sxs-lookup"><span data-stu-id="49cfb-106">XML Buffer</span></span>

<span data-ttu-id="49cfb-107">Un búfer XML proporciona un almacenamiento en memoria eficaz para los datos XML arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="49cfb-107">An XML Buffer provides efficient in-memory storage for arbitrary XML data.</span></span>


<span data-ttu-id="49cfb-108">Para leer datos de un búfer XML, use un [lector XML](xml-reader.md) y llame a [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) con el búfer XML.</span><span class="sxs-lookup"><span data-stu-id="49cfb-108">To read data from an XML Buffer, use a [XML Reader](xml-reader.md) and call [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) with the XML Buffer.</span></span> <span data-ttu-id="49cfb-109">El lector se colocará al principio del documento.</span><span class="sxs-lookup"><span data-stu-id="49cfb-109">The reader will be positioned at the start of the document.</span></span>

<span data-ttu-id="49cfb-110">Para insertar datos en un búfer, utilice un [escritor de XML](xml-writer.md) y llame a [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) con el búfer XML.</span><span class="sxs-lookup"><span data-stu-id="49cfb-110">To insert data into a buffer, use a [XML Writer](xml-writer.md) and call [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) with the XML Buffer.</span></span> <span data-ttu-id="49cfb-111">El escritor se colocará al final del documento.</span><span class="sxs-lookup"><span data-stu-id="49cfb-111">The writer will be positioned at the end of the document.</span></span>

<span data-ttu-id="49cfb-112">Una vez que se ha establecido un lector en un búfer XML, además de todas las API de lector de XML, se puede usar [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) para navegar por el lector a través del documento.</span><span class="sxs-lookup"><span data-stu-id="49cfb-112">Once a reader has been set to an XML Buffer, in addition to all of the XML Reader APIs, [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) may be used to navigate the reader through the document.</span></span> <span data-ttu-id="49cfb-113">[**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) y [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) también se pueden usar para registrar una posición en el documento y volver a ella más adelante.</span><span class="sxs-lookup"><span data-stu-id="49cfb-113">[**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) and [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) may also be used to record a position in the document and return to it later.</span></span>

<span data-ttu-id="49cfb-114">Una vez que se ha establecido un escritor en un búfer XML, además de todas las API del escritor de XML, se puede usar [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) para navegar por el escritor a través del documento.</span><span class="sxs-lookup"><span data-stu-id="49cfb-114">Once a writer has been set to an XML Buffer, in addition to all of the XML Writer APIs, [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) may be used to navigate the writer through the document.</span></span> <span data-ttu-id="49cfb-115">[**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) y [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) también se pueden usar para registrar una posición en el documento y volver a ella más adelante.</span><span class="sxs-lookup"><span data-stu-id="49cfb-115">[**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) and [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) may also be used to record a position in the document and return to it later.</span></span> <span data-ttu-id="49cfb-116">El escritor siempre inserta los datos antes del nodo en el que se coloca.</span><span class="sxs-lookup"><span data-stu-id="49cfb-116">The writer always inserts data before the node to which it is positioned.</span></span>

<span data-ttu-id="49cfb-117">Los nodos se pueden eliminar del búfer XML obteniendo la posición del nodo mediante [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) o [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) y llamando a [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) con esa posición.</span><span class="sxs-lookup"><span data-stu-id="49cfb-117">Nodes may be deleted from the XML Buffer by obtaining the position of the node using [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) or [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) and then calling [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) with that position.</span></span> <span data-ttu-id="49cfb-118">En el caso de los elementos, se eliminará el elemento y todos sus elementos secundarios, incluido el elemento final correspondiente.</span><span class="sxs-lookup"><span data-stu-id="49cfb-118">For elements, this will delete the element, all its children including its matching end element.</span></span>

<span data-ttu-id="49cfb-119">Una posición se representa mediante el valor de la [**\_ \_ \_ posición del nodo XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position).</span><span class="sxs-lookup"><span data-stu-id="49cfb-119">A position is represented by the value [**WS\_XML\_NODE\_POSITION**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position).</span></span> <span data-ttu-id="49cfb-120">Las posiciones son específicas de un búfer XML determinado y solo son válidas siempre que el búfer XML sea válido.</span><span class="sxs-lookup"><span data-stu-id="49cfb-120">Positions are specific to a particular XML Buffer, and are only valid as long as the XML Buffer is valid.</span></span>

<span data-ttu-id="49cfb-121">Las enumeraciones siguientes se utilizan con búferes XML:</span><span class="sxs-lookup"><span data-stu-id="49cfb-121">The following enumerations are used with XML buffers:</span></span>

-   [<span data-ttu-id="49cfb-122">**\_pasar \_ de WS a**</span><span class="sxs-lookup"><span data-stu-id="49cfb-122">**WS\_MOVE\_TO**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [<span data-ttu-id="49cfb-123">**identificador de la \_ \_ propiedad de búfer XML \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="49cfb-123">**WS\_XML\_BUFFER\_PROPERTY\_ID**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

<span data-ttu-id="49cfb-124">Las siguientes funciones se usan con búferes XML:</span><span class="sxs-lookup"><span data-stu-id="49cfb-124">The following functions are used with XML buffers:</span></span>

-   [<span data-ttu-id="49cfb-125">**WsCreateXmlBuffer**</span><span class="sxs-lookup"><span data-stu-id="49cfb-125">**WsCreateXmlBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [<span data-ttu-id="49cfb-126">**WsRemoveNode**</span><span class="sxs-lookup"><span data-stu-id="49cfb-126">**WsRemoveNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

<span data-ttu-id="49cfb-127">El siguiente identificador se utiliza con los búferes XML:</span><span class="sxs-lookup"><span data-stu-id="49cfb-127">The following handle is used with XML buffers:</span></span>

-   [<span data-ttu-id="49cfb-128">búfer de WS \_ XML \_</span><span class="sxs-lookup"><span data-stu-id="49cfb-128">WS\_XML\_BUFFER</span></span>](ws-xml-buffer.md)

<span data-ttu-id="49cfb-129">Las siguientes estructuras se utilizan con búferes XML:</span><span class="sxs-lookup"><span data-stu-id="49cfb-129">The following structures are used with XML buffers:</span></span>

-   [<span data-ttu-id="49cfb-130">**\_propiedad de \_ búfer \_ XML de WS**</span><span class="sxs-lookup"><span data-stu-id="49cfb-130">**WS\_XML\_BUFFER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [<span data-ttu-id="49cfb-131">**\_posición del \_ nodo \_ XML de WS**</span><span class="sxs-lookup"><span data-stu-id="49cfb-131">**WS\_XML\_NODE\_POSITION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




