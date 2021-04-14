---
title: Lector de XML
description: El lector XML es un cursor sobre un origen de entrada de XML. En esencia, un lector XML Lee un nodo XML a la vez, pero hay otras API auxiliares que facilitan la lectura de una secuencia de nodos.
ms.assetid: 1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2
keywords:
- Servicios Web de lector XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9d9c91b6594ec569536751751a3efca4c32e08
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488548"
---
# <a name="xml-reader"></a>Lector de XML

El lector XML es un cursor sobre un origen de entrada de XML. En esencia, un lector XML Lee un [nodo XML](xml-node.md) a la vez, pero hay otras API auxiliares que facilitan la lectura de una secuencia de nodos.


Se admiten los siguientes tipos de entrada de lectores:

-   [**Búfer en memoria de bytes codificados**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**Un flujo**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   Un [búfer XML](xml-buffer.md)

### <a name="security"></a>Seguridad

El lector comprobará que los atributos presentes en un elemento son únicos. El tiempo necesario para realizar esta validación es una función del número de atributos en el elemento que puede ser tan grande como [**\_ \_ atributos Max XML Reader \_ Property \_ Max \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id). Por lo tanto, el procesamiento de documentos grandes cuando la **\_ \_ \_ propiedad Max XML Reader Property \_ Max \_ attributes** está establecida en un valor grande puede presentar una oportunidad para un ataque por denegación de servicio.

El lector asignará prefijos a los espacios de nombres de cada elemento y atributos. El tiempo necesario para realizar esta asignación es una función del número de atributos xmlns en el ámbito, que puede ser tan grande como los [**\_ espacios de \_ \_ \_ \_ nombres Max XML Reader Property Max**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id). Por lo tanto, el procesamiento de documentos grandes cuando esta propiedad se establece en un valor grande puede presentar una oportunidad para un ataque por denegación de servicio.

Aunque el lector se asegurará de que el documento sigue la especificación gramatical de XML y de que sus aspectos estén dentro de las cuotas especificadas, el contenido del documento se debe considerar como no de confianza cuando proceda de un origen que no es de confianza. Los usuarios del lector deben comprobar todos los nombres de elementos y atributos, así como los espacios de nombres que usan [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)o mediante la inspección manual de los [**nodos**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).

Algunas otras situaciones a tener en cuenta son, entre otras:

-   Puede que falten elementos esperados
-   Pueden aparecer elementos inesperados
-   Puede que falten los atributos esperados
-   Pueden aparecer atributos inesperados
-   Los elementos pueden aparecer como elementos vacíos
-   Puede aparecer un espacio en blanco en lugares inesperados

Los usuarios del lector no deben asignar memoria basándose simplemente en los valores leídos del documento. Por ejemplo, considere el siguiente documento XML:

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

Asignar una matriz basada exclusivamente en la suposición de que un número de elementos seguirá un posible vector de ataque. En este caso, el usuario del lector debe asignar incrementalmente la memoria a medida que aparezcan los elementos.

El lector XML no admite DTD. No es necesario que el usuario del lector tenga que preocuparse por la comprobación de DTD.

La siguiente devolución de llamada se utiliza con los lectores XML:

-   [**devolución de llamada de \_ lectura de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

Las enumeraciones siguientes se usan con los lectores XML:

-   [**\_tipo de \_ codificación del lector XML \_ de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [**\_tipo de \_ entrada del lector XML \_ de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [**\_identificador de \_ propiedad del lector de XML de WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

Las siguientes funciones se usan con los lectores XML:

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

El siguiente identificador se usa con los lectores XML:

-   [\_lector de XML de WS \_](ws-xml-reader.md)

Las siguientes estructuras se utilizan con los lectores XML:

-   [**\_ \_ \_ codificación binaria del lector de WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [**\_entrada de \_ búfer de lector XML \_ de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**\_codificación del \_ lector \_ XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [**\_entrada de \_ lector \_ XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [**\_ \_ codificación MTOM del lector XML \_ de \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [**\_propiedades del \_ lector de XML de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [**\_propiedad del \_ lector de XML de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [**\_entrada de \_ flujo del lector XML \_ de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [**\_codificación de \_ texto del lector XML \_ de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 




