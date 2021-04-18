---
title: Nodo XML
description: Un nodo XML representa un único fragmento de XML, por ejemplo, un elemento de inicio y sus atributos, un elemento final, texto o \ 0034; escrito \ 0034; contenido de texto como un entero o una matriz de bytes. Los datos de un nodo varían según el tipo de \_ nodo XML de WS \_ \_ .
ms.assetid: c514c542-029b-46d1-a796-1f132a41b2ad
keywords:
- Servicios Web de nodo XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac212205fac02db0ee87d8acbe0b123ffcead921
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "105714496"
---
# <a name="xml-node"></a>Nodo XML

Un nodo XML representa un único fragmento de XML, por ejemplo, un elemento de inicio y sus atributos, un elemento final, texto o contenido de texto "con tipo", como un entero o una matriz de bytes. Los datos de un nodo varían según el [**tipo de \_ \_ nodo XML \_ de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).


A continuación se muestra un ejemplo de un documento XML específico de codificación representado con estructuras independientes de codificación.

``` syntax
<p:PurchaseOrder xmlns:p="http://tempuri.org" p:id="3891">
    <p:Buyer>Joe</p:Buyer>
</p:PurchaseOrder>
```

``` syntax
WS_XML_STRING purchaseOrder = WS_XML_STRING_VALUE("PurchaseOrder");
WS_XML_STRING id            = WS_XML_STRING_VALUE("id");
WS_XML_STRING prefix        = WS_XML_STRING_VALUE("p");
WS_XML_STRING ns            = WS_XML_STRING_VALUE("http://tempuri.org");

WS_XML_ATTRIBUTE xmlnsAttribute =
{
    /* singleQuote */ FALSE,
    /* isXmlNs     */ TRUE,
    /* prefix      */ &prefix,
    /* localName   */ NULL,
    /* ns          */ &ns,
    /* value       */ NULL
};
WS_XML_INT32_TEXT idText =
{
    /* text  */ { WS_XML_TEXT_TYPE_INT32 },
    /* value */ 3891
};
WS_XML_ATTRIBUTE idAttribute =
{
    /* singleQuote */ FALSE,
    /* isXmlNs     */ FALSE,
    /* prefix      */ &prefix,
    /* localName   */ &id,
    /* ns          */ &ns,
    /* value       */ &idText.text,
};
WS_XML_ATTRIBUTE* attributes[2] =
{
    &xmlnsAttribute,
    &idAttribute
};
WS_XML_ELEMENT_NODE elementNode =
{
    /* node           */ { WS_XML_NODE_TYPE_ELEMENT },
    /* prefix         */ &prefix,
    /* localName      */ &purchaseOrder,
    /* ns             */ &ns,
    /* attributeCount */ 2,
    /* attributes     */ attributes,
    /* isEmpty        */ FALSE,
    /* array          */ NULL,
};
WS_XML_UTF8_TEXT joeText =
{
    /* text  */ { WS_XML_TEXT_TYPE_UTF8 },
    /* value */ WS_XML_STRING_VALUE("Joe")
};
WS_XML_TEXT_NODE textNode =
{
    /* node */ { WS_XML_NODE_TYPE_TEXT },
    /* text */ &joeText.text
};
WS_XML_NODE endElementNode =
{
    WS_XML_NODE_TYPE_END_ELEMENT
};
WS_XML_NODE* nodes[3] =
{
    &elementNode.node,
    &textNode.node,
    &endElementNode
};
```

Las enumeraciones siguientes se utilizan con nodos XML:

-   [**\_tipo de valor WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [**\_tipo de \_ nodo \_ XML de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [**\_tipo de \_ texto \_ XML de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

Las siguientes funciones se usan con nodos XML:

-   [**WsTrimXmlWhitespace**](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [**WsVerifyXmlNCName**](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [**WsXmlStringEquals**](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

Las macros siguientes se utilizan con nodos XML:

-   [**\_valor del \_ Diccionario de cadenas XML \_ de WS \_**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   [**\_ \_ cadena \_ null de WS XML**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))
-   [**\_valor de \_ cadena \_ XML de WS**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

Las siguientes estructuras se utilizan con nodos XML:

-   [**\_atributo XML de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [**Texto de WS \_ XML \_ Base64 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [**\_ \_ texto BOOLEANO de WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [**nodo de comentario de WS \_ XML \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [**\_texto de \_ fecha y hora XML de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [**\_ \_ texto decimal de WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [**Diccionario de WS \_ XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [**\_ \_ texto Double de WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [**\_nodo de \_ elemento \_ XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [**\_ \_ texto flotante de WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [**texto del GUID de WS \_ XML \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [**\_Texto XML \_ INT32 de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [**\_ \_ Texto INT64 XML de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [**\_texto de \_ lista \_ XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [**\_nodo XML de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [**\_QNAME XML de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [**\_ \_ texto QNAME XML de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [**\_cadena XML de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [**\_texto XML de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [**\_nodo de \_ texto \_ XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [**\_texto de \_ TIMESPAN \_ XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [**\_ \_ Texto UINT64 XML de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [**\_texto de \_ \_ identificador único \_ de WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [**\_ \_ Texto UTF16 XML de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [**\_ \_ Texto UTF8 de WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 