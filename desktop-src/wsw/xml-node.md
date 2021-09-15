---
title: Nodo XML
description: Un nodo XML representa un único fragmento de XML, por ejemplo, un elemento start y sus atributos, un elemento final, texto o \ 0034;typed \ 0034; contenido de texto, como un entero o una matriz de bytes. Los datos de un nodo varían según el tipo de nodo \_ XML de WS. \_ \_
ms.assetid: c514c542-029b-46d1-a796-1f132a41b2ad
keywords:
- Servicios web de nodo XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac212205fac02db0ee87d8acbe0b123ffcead921
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571140"
---
# <a name="xml-node"></a>Nodo XML

Un nodo XML representa un único fragmento de XML, por ejemplo, un elemento de inicio y sus atributos, un elemento final, texto o contenido de texto "con tipo", como un entero o una matriz de bytes. Los datos de un nodo varían según el tipo de [**nodo \_ XML \_ de \_ WS.**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)


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

Las enumeraciones siguientes se usan con nodos XML:

-   [**TIPO DE \_ VALOR WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [**TIPO DE \_ NODO XML \_ DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [**WS \_ XML \_ TEXT \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

Las siguientes funciones se usan con nodos XML:

-   [**WsTrimXmlWhitespace**](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [**WsVerifyXmlNCName**](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [**WsXmlStringEquals**](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

Las macros siguientes se usan con nodos XML:

-   [**VALOR DEL \_ DICCIONARIO DE CADENAS XML \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   [**WS \_ XML \_ STRING \_ NULL**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))
-   [**WS \_ XML \_ STRING \_ VALUE**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

Las estructuras siguientes se usan con nodos XML:

-   [**ATRIBUTO XML de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [**TEXTO DE WS \_ XML \_ BASE64 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [**WS \_ XML \_ BOOL \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [**NODO DE \_ COMENTARIO XML \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [**TEXTO \_ \_ DATETIME DE WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [**TEXTO \_ DECIMAL XML WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [**DICCIONARIO XML de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [**WS \_ XML \_ DOUBLE \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [**NODO DE \_ ELEMENTO XML \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [**TEXTO FLOTANTE DE WS \_ XML \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [**TEXTO GUID \_ DE WS XML \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [**WS \_ XML \_ INT32 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [**TEXTO \_ INT64 DE WS XML \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [**TEXTO DE LA \_ LISTA XML \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [**NODO XML de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [**WS \_ XML \_ QNAME**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [**WS \_ XML \_ QNAME \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [**CADENA XML de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [**TEXTO XML DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [**NODO DE \_ TEXTO XML \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [**TEXTO DE \_ \_ TIMESPAN DE WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [**WS \_ XML \_ UINT64 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [**TEXTO DE IDENTIFICADOR ÚNICO DE WS \_ XML \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [**TEXTO \_ \_ UTF16 DE WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [**TEXTO \_ \_ UTF8 DE WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 