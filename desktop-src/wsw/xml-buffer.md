---
title: Búfer XML
description: Un búfer XML proporciona un almacenamiento en memoria eficaz para datos XML arbitrarios.
ms.assetid: e379628b-c6f8-48b1-8109-59fb604f2bcb
keywords:
- Servicios web de búfer XML para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd4e4725f2ad3345dcef7c33b694a8e327f4d8a6c43fbce39f9c57babfa467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192341"
---
# <a name="xml-buffer"></a>Búfer XML

Un búfer XML proporciona un almacenamiento en memoria eficaz para datos XML arbitrarios.


Para leer datos de un búfer XML, use un Lector [XML](xml-reader.md) y llame a [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) con el búfer XML. El lector se colocará al principio del documento.

Para insertar datos en un búfer, use un sistema de escritura [XML](xml-writer.md) y llame a [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) con el búfer XML. El escritor se colocará al final del documento.

Una vez que un lector se ha establecido en un búfer XML, además de todas las API de lector XML, [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) se puede usar para navegar por el lector a través del documento. [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) y [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) también se pueden usar para registrar una posición en el documento y volver a ella más adelante.

Una vez que un escritor se ha establecido en un búfer XML, además de todas las API de escritor XML, [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) puede usarse para navegar por el escritor a través del documento. [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) y [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) también se pueden usar para registrar una posición en el documento y volver a ella más adelante. El sistema de escritura siempre inserta datos antes del nodo en el que se coloca.

Los nodos se pueden eliminar del búfer XML obteniendo la posición del nodo mediante [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) o [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) y, a continuación, llamando a [**WsRemoveNode con**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) esa posición. En el caso de los elementos , se eliminará el elemento , todos sus elementos secundarios, incluido su elemento final correspondiente.

Una posición se representa mediante el valor [**WS \_ XML NODE \_ \_ POSITION**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position). Las posiciones son específicas de un búfer XML determinado y solo son válidas siempre que el búfer XML sea válido.

Las enumeraciones siguientes se usan con búferes XML:

-   [**WS \_ MOVE \_ TO**](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [**ID. \_ DE PROPIEDAD DEL BÚFER XML \_ \_ DE \_ WS**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

Las siguientes funciones se usan con búferes XML:

-   [**WsCreateXmlBuffer**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

El siguiente identificador se usa con búferes XML:

-   [BÚFER XML DE WS \_ \_](ws-xml-buffer.md)

Las estructuras siguientes se usan con búferes XML:

-   [**WS \_ XML \_ BUFFER \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [**POSICIÓN DEL \_ NODO XML \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




