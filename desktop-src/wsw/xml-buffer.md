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
# <a name="xml-buffer"></a>Búfer XML

Un búfer XML proporciona un almacenamiento en memoria eficaz para los datos XML arbitrarios.


Para leer datos de un búfer XML, use un [lector XML](xml-reader.md) y llame a [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) con el búfer XML. El lector se colocará al principio del documento.

Para insertar datos en un búfer, utilice un [escritor de XML](xml-writer.md) y llame a [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) con el búfer XML. El escritor se colocará al final del documento.

Una vez que se ha establecido un lector en un búfer XML, además de todas las API de lector de XML, se puede usar [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) para navegar por el lector a través del documento. [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) y [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) también se pueden usar para registrar una posición en el documento y volver a ella más adelante.

Una vez que se ha establecido un escritor en un búfer XML, además de todas las API del escritor de XML, se puede usar [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) para navegar por el escritor a través del documento. [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) y [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) también se pueden usar para registrar una posición en el documento y volver a ella más adelante. El escritor siempre inserta los datos antes del nodo en el que se coloca.

Los nodos se pueden eliminar del búfer XML obteniendo la posición del nodo mediante [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) o [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) y llamando a [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) con esa posición. En el caso de los elementos, se eliminará el elemento y todos sus elementos secundarios, incluido el elemento final correspondiente.

Una posición se representa mediante el valor de la [**\_ \_ \_ posición del nodo XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position). Las posiciones son específicas de un búfer XML determinado y solo son válidas siempre que el búfer XML sea válido.

Las enumeraciones siguientes se utilizan con búferes XML:

-   [**\_pasar \_ de WS a**](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [**identificador de la \_ \_ propiedad de búfer XML \_ de WS \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

Las siguientes funciones se usan con búferes XML:

-   [**WsCreateXmlBuffer**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

El siguiente identificador se utiliza con los búferes XML:

-   [búfer de WS \_ XML \_](ws-xml-buffer.md)

Las siguientes estructuras se utilizan con búferes XML:

-   [**\_propiedad de \_ búfer \_ XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [**\_posición del \_ nodo \_ XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




