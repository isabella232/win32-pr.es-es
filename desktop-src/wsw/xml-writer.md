---
title: Escritor XML
description: Xml Writer es una API para emitir XML. En esencia, un escritor XML escribe un nodo XML a la vez, pero hay API auxiliares adicionales para facilitar la escritura de una secuencia de nodos.
ms.assetid: 69d50793-1d5b-4fc7-bf69-128f8e23a98d
keywords:
- Servicios web del escritor XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085a02b3aca33ffa3b31e4579d47068a683ee4d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571961"
---
# <a name="xml-writer"></a>Escritor XML

Xml Writer es una API para emitir XML. En esencia, un escritor XML escribe un nodo [XML](xml-node.md) a la vez, pero hay API auxiliares adicionales para facilitar la escritura de una secuencia de nodos.


Se admiten los siguientes tipos de salida de escritor:

-   [**Búfer en memoria de bytes codificados**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**Una secuencia**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   Un [búfer XML](xml-buffer.md)

Las devoluciones de llamada siguientes se usan con el sistema de escritura XML:

-   [**WS \_ DYNAMIC \_ STRING \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**DEVOLUCIÓN DE LLAMADA \_ \_ DE BYTES DE \_ EXTRACCIÓN DE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**WS \_ PUSH \_ BYTES \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**WS \_ WRITE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

Las enumeraciones siguientes se usan con el sistema de escritura XML:

-   [**WS \_ CHARSET**](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [**TIPO DE \_ \_ CODIFICACIÓN WS XML WRITER \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [**TIPO DE SALIDA DE WS \_ XML \_ WRITER \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [**ID. \_ DE PROPIEDAD DE WS XML \_ WRITER \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

Las siguientes funciones se usan con el sistema de escritura XML:

-   [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode)
-   [**WsCreateWriter**](/windows/desktop/api/WebServices/nf-webservices-wscreatewriter)
-   [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter)
-   [**WsFreeWriter**](/windows/desktop/api/WebServices/nf-webservices-wsfreewriter)
-   [**WsGetPrefixFromNamespace**](/windows/desktop/api/WebServices/nf-webservices-wsgetprefixfromnamespace)
-   [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition)
-   [**WsGetWriterProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterproperty)
-   [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter)
-   [**WsPullBytes**](/windows/desktop/api/WebServices/nf-webservices-wspullbytes)
-   [**WsPushBytes**](/windows/desktop/api/WebServices/nf-webservices-wspushbytes)
-   [**WsSetOutput**](/windows/desktop/api/WebServices/nf-webservices-wssetoutput)
-   [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer)
-   [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition)
-   [**WsWriteArray**](/windows/desktop/api/WebServices/nf-webservices-wswritearray)
-   [**WsWriteBytes**](/windows/desktop/api/WebServices/nf-webservices-wswritebytes)
-   [**WsWriteChars**](/windows/desktop/api/WebServices/nf-webservices-wswritechars)
-   [**WsWriteCharsUtf8**](/windows/desktop/api/WebServices/nf-webservices-wswritecharsutf8)
-   [**WsWriteEndAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteendattribute)
-   [**WsWriteEndCData**](/windows/desktop/api/WebServices/nf-webservices-wswriteendcdata)
-   [**WsWriteEndElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteendelement)
-   [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode)
-   [**WsWriteQualifiedName**](/windows/desktop/api/WebServices/nf-webservices-wswritequalifiedname)
-   [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute)
-   [**WsWriteStartCData**](/windows/desktop/api/WebServices/nf-webservices-wswritestartcdata)
-   [**WsWriteStartElement**](/windows/desktop/api/WebServices/nf-webservices-wswritestartelement)
-   [**WsWriteText**](/windows/desktop/api/WebServices/nf-webservices-wswritetext)
-   [**WsWriteValue**](/windows/desktop/api/WebServices/nf-webservices-wswritevalue)
-   [**WsWriteXmlnsAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritexmlnsattribute)

El siguiente identificador se usa con el sistema de escritura XML:

-   [WS \_ XML \_ WRITER](ws-xml-writer.md)

Las estructuras siguientes se usan con el sistema de escritura XML:

-   [**CODIFICACIÓN BINARIA DE WS \_ XML \_ WRITER \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [**SALIDA DEL \_ BÚFER DE WS XML \_ WRITER \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**CODIFICACIÓN \_ WS XML \_ WRITER \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [**WS \_ XML \_ WRITER \_ MTOM \_ ENCODING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [**SALIDA DE WS \_ XML \_ WRITER \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [**PROPIEDADES DE \_ WS XML \_ WRITER \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [**WS \_ XML \_ WRITER \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [**SALIDA DE SECUENCIA DE \_ WS XML \_ WRITER \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [**CODIFICACIÓN DE TEXTO DE WS \_ XML \_ WRITER \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 




