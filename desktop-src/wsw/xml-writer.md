---
title: Escritor XML
description: El escritor XML es una API para emitir XML. En esencia, un escritor XML escribe un nodo XML a la vez, pero hay otras API auxiliares para facilitar la escritura de una secuencia de nodos.
ms.assetid: 69d50793-1d5b-4fc7-bf69-128f8e23a98d
keywords:
- Servicios web del escritor XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085a02b3aca33ffa3b31e4579d47068a683ee4d8
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "105714495"
---
# <a name="xml-writer"></a><span data-ttu-id="5d59f-107">Escritor XML</span><span class="sxs-lookup"><span data-stu-id="5d59f-107">XML Writer</span></span>

<span data-ttu-id="5d59f-108">El escritor XML es una API para emitir XML.</span><span class="sxs-lookup"><span data-stu-id="5d59f-108">XML Writer is an API for emitting XML.</span></span> <span data-ttu-id="5d59f-109">En esencia, un escritor XML escribe un [nodo XML](xml-node.md) a la vez, pero hay otras API auxiliares para facilitar la escritura de una secuencia de nodos.</span><span class="sxs-lookup"><span data-stu-id="5d59f-109">At its core, an XML Writer writes one [XML Node](xml-node.md) at a time, but there are additional helper APIs to make writing a sequence of nodes easier.</span></span>


<span data-ttu-id="5d59f-110">Se admiten los siguientes tipos de salida de escritor:</span><span class="sxs-lookup"><span data-stu-id="5d59f-110">The following types of writer output are supported:</span></span>

-   [<span data-ttu-id="5d59f-111">**Búfer en memoria de bytes codificados**</span><span class="sxs-lookup"><span data-stu-id="5d59f-111">**An in-memory buffer of encoded bytes**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [<span data-ttu-id="5d59f-112">**Un flujo**</span><span class="sxs-lookup"><span data-stu-id="5d59f-112">**A stream**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   <span data-ttu-id="5d59f-113">Un [búfer XML](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="5d59f-113">An [XML Buffer](xml-buffer.md)</span></span>

<span data-ttu-id="5d59f-114">Las siguientes devoluciones de llamada se utilizan con el escritor de XML:</span><span class="sxs-lookup"><span data-stu-id="5d59f-114">The following callbacks are used with the XML writer:</span></span>

-   [<span data-ttu-id="5d59f-115">**\_devolución de \_ llamada de cadena dinámica de WS \_**</span><span class="sxs-lookup"><span data-stu-id="5d59f-115">**WS\_DYNAMIC\_STRING\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [<span data-ttu-id="5d59f-116">**\_devolución de \_ llamada de bytes de extracción de WS \_**</span><span class="sxs-lookup"><span data-stu-id="5d59f-116">**WS\_PULL\_BYTES\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [<span data-ttu-id="5d59f-117">**\_devolución de \_ llamada de bytes de inserciones de WS \_**</span><span class="sxs-lookup"><span data-stu-id="5d59f-117">**WS\_PUSH\_BYTES\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [<span data-ttu-id="5d59f-118">**devolución de llamada de WS- \_ Write \_**</span><span class="sxs-lookup"><span data-stu-id="5d59f-118">**WS\_WRITE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

<span data-ttu-id="5d59f-119">Las enumeraciones siguientes se utilizan con el escritor de XML:</span><span class="sxs-lookup"><span data-stu-id="5d59f-119">The following enumerations are used with the XML writer:</span></span>

-   [<span data-ttu-id="5d59f-120">**juego de caracteres de WS \_**</span><span class="sxs-lookup"><span data-stu-id="5d59f-120">**WS\_CHARSET**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [<span data-ttu-id="5d59f-121">**\_tipo de \_ codificación del escritor XML \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="5d59f-121">**WS\_XML\_WRITER\_ENCODING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [<span data-ttu-id="5d59f-122">**\_tipo de \_ salida del escritor XML \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="5d59f-122">**WS\_XML\_WRITER\_OUTPUT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [<span data-ttu-id="5d59f-123">**\_identificador de \_ propiedad del escritor XML \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="5d59f-123">**WS\_XML\_WRITER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

<span data-ttu-id="5d59f-124">Las siguientes funciones se usan con el escritor de XML:</span><span class="sxs-lookup"><span data-stu-id="5d59f-124">The following functions are used with the XML writer:</span></span>

-   [<span data-ttu-id="5d59f-125">**WsCopyNode**</span><span class="sxs-lookup"><span data-stu-id="5d59f-125">**WsCopyNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscopynode)
-   [<span data-ttu-id="5d59f-126">**WsCreateWriter**</span><span class="sxs-lookup"><span data-stu-id="5d59f-126">**WsCreateWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatewriter)
-   [<span data-ttu-id="5d59f-127">**WsFlushWriter**</span><span class="sxs-lookup"><span data-stu-id="5d59f-127">**WsFlushWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter)
-   [<span data-ttu-id="5d59f-128">**WsFreeWriter**</span><span class="sxs-lookup"><span data-stu-id="5d59f-128">**WsFreeWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreewriter)
-   [<span data-ttu-id="5d59f-129">**WsGetPrefixFromNamespace**</span><span class="sxs-lookup"><span data-stu-id="5d59f-129">**WsGetPrefixFromNamespace**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetprefixfromnamespace)
-   [<span data-ttu-id="5d59f-130">**WsGetWriterPosition**</span><span class="sxs-lookup"><span data-stu-id="5d59f-130">**WsGetWriterPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition)
-   [<span data-ttu-id="5d59f-131">**WsGetWriterProperty**</span><span class="sxs-lookup"><span data-stu-id="5d59f-131">**WsGetWriterProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterproperty)
-   [<span data-ttu-id="5d59f-132">**WsMoveWriter**</span><span class="sxs-lookup"><span data-stu-id="5d59f-132">**WsMoveWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter)
-   [<span data-ttu-id="5d59f-133">**WsPullBytes**</span><span class="sxs-lookup"><span data-stu-id="5d59f-133">**WsPullBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wspullbytes)
-   [<span data-ttu-id="5d59f-134">**WsPushBytes**</span><span class="sxs-lookup"><span data-stu-id="5d59f-134">**WsPushBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wspushbytes)
-   [<span data-ttu-id="5d59f-135">**WsSetOutput**</span><span class="sxs-lookup"><span data-stu-id="5d59f-135">**WsSetOutput**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetoutput)
-   [<span data-ttu-id="5d59f-136">**WsSetOutputToBuffer**</span><span class="sxs-lookup"><span data-stu-id="5d59f-136">**WsSetOutputToBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer)
-   [<span data-ttu-id="5d59f-137">**WsSetWriterPosition**</span><span class="sxs-lookup"><span data-stu-id="5d59f-137">**WsSetWriterPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition)
-   [<span data-ttu-id="5d59f-138">**WsWriteArray**</span><span class="sxs-lookup"><span data-stu-id="5d59f-138">**WsWriteArray**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritearray)
-   [<span data-ttu-id="5d59f-139">**WsWriteBytes**</span><span class="sxs-lookup"><span data-stu-id="5d59f-139">**WsWriteBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritebytes)
-   [<span data-ttu-id="5d59f-140">**WsWriteChars**</span><span class="sxs-lookup"><span data-stu-id="5d59f-140">**WsWriteChars**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritechars)
-   [<span data-ttu-id="5d59f-141">**WsWriteCharsUtf8**</span><span class="sxs-lookup"><span data-stu-id="5d59f-141">**WsWriteCharsUtf8**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritecharsutf8)
-   [<span data-ttu-id="5d59f-142">**WsWriteEndAttribute**</span><span class="sxs-lookup"><span data-stu-id="5d59f-142">**WsWriteEndAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendattribute)
-   [<span data-ttu-id="5d59f-143">**WsWriteEndCData**</span><span class="sxs-lookup"><span data-stu-id="5d59f-143">**WsWriteEndCData**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendcdata)
-   [<span data-ttu-id="5d59f-144">**WsWriteEndElement**</span><span class="sxs-lookup"><span data-stu-id="5d59f-144">**WsWriteEndElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendelement)
-   [<span data-ttu-id="5d59f-145">**WsWriteNode**</span><span class="sxs-lookup"><span data-stu-id="5d59f-145">**WsWriteNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritenode)
-   [<span data-ttu-id="5d59f-146">**WsWriteQualifiedName**</span><span class="sxs-lookup"><span data-stu-id="5d59f-146">**WsWriteQualifiedName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritequalifiedname)
-   [<span data-ttu-id="5d59f-147">**WsWriteStartAttribute**</span><span class="sxs-lookup"><span data-stu-id="5d59f-147">**WsWriteStartAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute)
-   [<span data-ttu-id="5d59f-148">**WsWriteStartCData**</span><span class="sxs-lookup"><span data-stu-id="5d59f-148">**WsWriteStartCData**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartcdata)
-   [<span data-ttu-id="5d59f-149">**WsWriteStartElement**</span><span class="sxs-lookup"><span data-stu-id="5d59f-149">**WsWriteStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartelement)
-   [<span data-ttu-id="5d59f-150">**WsWriteText**</span><span class="sxs-lookup"><span data-stu-id="5d59f-150">**WsWriteText**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritetext)
-   [<span data-ttu-id="5d59f-151">**WsWriteValue**</span><span class="sxs-lookup"><span data-stu-id="5d59f-151">**WsWriteValue**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritevalue)
-   [<span data-ttu-id="5d59f-152">**WsWriteXmlnsAttribute**</span><span class="sxs-lookup"><span data-stu-id="5d59f-152">**WsWriteXmlnsAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritexmlnsattribute)

<span data-ttu-id="5d59f-153">El siguiente identificador se utiliza con el escritor de XML:</span><span class="sxs-lookup"><span data-stu-id="5d59f-153">The following handle is used with the XML writer:</span></span>

-   [<span data-ttu-id="5d59f-154">\_escritor de XML de WS \_</span><span class="sxs-lookup"><span data-stu-id="5d59f-154">WS\_XML\_WRITER</span></span>](ws-xml-writer.md)

<span data-ttu-id="5d59f-155">Las siguientes estructuras se utilizan con el escritor de XML:</span><span class="sxs-lookup"><span data-stu-id="5d59f-155">The following structures are used with the XML writer:</span></span>

-   [<span data-ttu-id="5d59f-156">**\_ \_ \_ codificación binaria de la escritura de WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="5d59f-156">**WS\_XML\_WRITER\_BINARY\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [<span data-ttu-id="5d59f-157">**\_salida del \_ búfer del escritor XML \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="5d59f-157">**WS\_XML\_WRITER\_BUFFER\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [<span data-ttu-id="5d59f-158">**\_codificación del \_ escritor \_ XML de WS**</span><span class="sxs-lookup"><span data-stu-id="5d59f-158">**WS\_XML\_WRITER\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [<span data-ttu-id="5d59f-159">**\_ \_ codificación MTOM del escritor XML \_ de \_ WS**</span><span class="sxs-lookup"><span data-stu-id="5d59f-159">**WS\_XML\_WRITER\_MTOM\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [<span data-ttu-id="5d59f-160">**\_salida del \_ escritor \_ XML de WS**</span><span class="sxs-lookup"><span data-stu-id="5d59f-160">**WS\_XML\_WRITER\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [<span data-ttu-id="5d59f-161">**\_propiedades del \_ escritor de XML de WS \_**</span><span class="sxs-lookup"><span data-stu-id="5d59f-161">**WS\_XML\_WRITER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [<span data-ttu-id="5d59f-162">**\_propiedad del \_ escritor \_ XML de WS**</span><span class="sxs-lookup"><span data-stu-id="5d59f-162">**WS\_XML\_WRITER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [<span data-ttu-id="5d59f-163">**\_salida de \_ flujo del escritor XML \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="5d59f-163">**WS\_XML\_WRITER\_STREAM\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [<span data-ttu-id="5d59f-164">**\_codificación de \_ texto del escritor XML \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="5d59f-164">**WS\_XML\_WRITER\_TEXT\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 




