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
# <a name="xml-writer"></a>Escritor XML

El escritor XML es una API para emitir XML. En esencia, un escritor XML escribe un [nodo XML](xml-node.md) a la vez, pero hay otras API auxiliares para facilitar la escritura de una secuencia de nodos.


Se admiten los siguientes tipos de salida de escritor:

-   [**Búfer en memoria de bytes codificados**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**Un flujo**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   Un [búfer XML](xml-buffer.md)

Las siguientes devoluciones de llamada se utilizan con el escritor de XML:

-   [**\_devolución de \_ llamada de cadena dinámica de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**\_devolución de \_ llamada de bytes de extracción de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**\_devolución de \_ llamada de bytes de inserciones de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**devolución de llamada de WS- \_ Write \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

Las enumeraciones siguientes se utilizan con el escritor de XML:

-   [**juego de caracteres de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [**\_tipo de \_ codificación del escritor XML \_ de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [**\_tipo de \_ salida del escritor XML \_ de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [**\_identificador de \_ propiedad del escritor XML \_ de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

Las siguientes funciones se usan con el escritor de XML:

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

El siguiente identificador se utiliza con el escritor de XML:

-   [\_escritor de XML de WS \_](ws-xml-writer.md)

Las siguientes estructuras se utilizan con el escritor de XML:

-   [**\_ \_ \_ codificación binaria de la escritura de WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [**\_salida del \_ búfer del escritor XML \_ de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**\_codificación del \_ escritor \_ XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [**\_ \_ codificación MTOM del escritor XML \_ de \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [**\_salida del \_ escritor \_ XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [**\_propiedades del \_ escritor de XML de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [**\_propiedad del \_ escritor \_ XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [**\_salida de \_ flujo del escritor XML \_ de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [**\_codificación de \_ texto del escritor XML \_ de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 




