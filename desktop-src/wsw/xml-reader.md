---
title: Lector de XML
description: Lector XML es un cursor sobre un origen de entrada de XML. En esencia, un lector XML lee un nodo XML a la vez, pero hay API auxiliares adicionales para facilitar la lectura de una secuencia de nodos.
ms.assetid: 1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2
keywords:
- Servicios web del Lector XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9d9c91b6594ec569536751751a3efca4c32e08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466629"
---
# <a name="xml-reader"></a>Lector de XML

Lector XML es un cursor sobre un origen de entrada de XML. En esencia, un lector XML lee un nodo [XML](xml-node.md) a la vez, pero hay API auxiliares adicionales para facilitar la lectura de una secuencia de nodos.


Se admiten los siguientes tipos de entrada de lectores:

-   [**Búfer en memoria de bytes codificados**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**Una secuencia**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   Un [búfer XML](xml-buffer.md)

### <a name="security"></a>Seguridad

El lector comprobará que los atributos presentes en un elemento son únicos. El tiempo necesario para realizar esta validación es una función del número de atributos en el elemento que puede ser tan grande como [**WS \_ XML READER PROPERTY MAX \_ \_ \_ \_ ATTRIBUTES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id). Por lo tanto, el procesamiento de documentos grandes cuando **WS \_ XML READER PROPERTY MAX \_ \_ \_ \_ ATTRIBUTES** está establecido en un valor grande puede presentar una oportunidad para un ataque por denegación de servicio.

El lector asignará prefijos a espacios de nombres para cada elemento y atributos. El tiempo necesario para realizar esta asignación es una función del número de atributos xmlns en el ámbito que puede ser tan grande como [**WS \_ XML READER PROPERTY MAX \_ \_ \_ \_ NAMESPACES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id). Por lo tanto, el procesamiento de documentos grandes cuando esta propiedad se establece en un valor grande puede presentar una oportunidad para un ataque por denegación de servicio.

Aunque el lector se asegurará de que el documento sigue la especificación gramatical de xml y, además, que sus aspectos están dentro de las cuotas especificadas, el contenido del documento todavía debe considerarse como no de confianza cuando se trata de un origen que no es de confianza. Los usuarios del lector deben comprobar todos los nombres de elementos y atributos y espacios de nombres mediante [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)o inspeccionando manualmente los [**nodos**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).

Algunas otras situaciones que se deben tener en cuenta incluyen, entre otras:

-   Pueden faltar elementos esperados
-   Pueden aparecer elementos inesperados
-   Los atributos esperados pueden faltar
-   Pueden aparecer atributos inesperados
-   Los elementos pueden aparecer como elementos vacíos
-   El espacio en blanco puede aparecer en lugares inesperados

Los usuarios del lector no deben asignar memoria basándose simplemente en los valores leídos del documento. Por ejemplo, considere el siguiente documento xml:

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

Asignar una matriz basada en la suposición de que algún número de elementos seguirá sería un vector de ataque potencial. En su lugar, el usuario del lector debe asignar incrementalmente la memoria a medida que aparecen los elementos.

El lector XML no admite DTD. El usuario del lector no necesita preocuparse por la comprobación de DTD.

La devolución de llamada siguiente se usa con lectores XML:

-   [**WS \_ READ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

Las enumeraciones siguientes se usan con lectores XML:

-   [**TIPO DE \_ CODIFICACIÓN DEL LECTOR XML \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [**TIPO DE ENTRADA \_ DEL LECTOR XML DE WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [**ID. \_ DE PROPIEDAD DEL LECTOR XML \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

Las siguientes funciones se usan con lectores XML:

-   [**WsCreateReader**](/windows/desktop/api/WebServices/nf-webservices-wscreatereader)
-   [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader)
-   [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)
-   [**WsFreeReader**](/windows/desktop/api/WebServices/nf-webservices-wsfreereader)
-   [**WsGetNamespaceFromPrefix**](/windows/desktop/api/WebServices/nf-webservices-wsgetnamespacefromprefix)
-   [**WsGetReaderNode**](/windows/desktop/api/WebServices/nf-webservices-wsgetreadernode)
-   [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition)
-   [**WsGetReaderProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderproperty)
-   [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute)
-   [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader)
-   [**WsReadArray**](/windows/desktop/api/WebServices/nf-webservices-wsreadarray)
-   [**WsReadBytes**](/windows/desktop/api/WebServices/nf-webservices-wsreadbytes)
-   [**WsReadChars**](/windows/desktop/api/WebServices/nf-webservices-wsreadchars)
-   [**WsReadCharsUtf8**](/windows/desktop/api/WebServices/nf-webservices-wsreadcharsutf8)
-   [**WsReadEndAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadendattribute)
-   [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement)
-   [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode)
-   [**WsReadQualifiedName**](/windows/desktop/api/WebServices/nf-webservices-wsreadqualifiedname)
-   [**WsReadStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartattribute)
-   [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement)
-   [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)
-   [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue)
-   [**WsSetInput**](/windows/desktop/api/WebServices/nf-webservices-wssetinput)
-   [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer)
-   [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition)
-   [**WsSkipNode**](/windows/desktop/api/WebServices/nf-webservices-wsskipnode)

El siguiente identificador se usa con lectores XML:

-   [WS \_ XML \_ READER](ws-xml-reader.md)

Las estructuras siguientes se usan con lectores XML:

-   [**CODIFICACIÓN \_ BINARIA DEL LECTOR XML \_ \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [**ENTRADA DEL \_ BÚFER DEL LECTOR XML \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**CODIFICACIÓN DEL \_ LECTOR XML \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [**ENTRADA DEL \_ LECTOR XML \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [**WS \_ XML \_ READER \_ MTOM \_ ENCODING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [**PROPIEDADES DEL \_ LECTOR XML \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [**WS \_ XML \_ READER \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [**ENTRADA DE \_ FLUJO DEL LECTOR XML \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [**CODIFICACIÓN \_ DE TEXTO DEL LECTOR XML DE WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 




