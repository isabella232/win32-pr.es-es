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
# <a name="xml-node"></a><span data-ttu-id="e7a8e-107">Nodo XML</span><span class="sxs-lookup"><span data-stu-id="e7a8e-107">XML Node</span></span>

<span data-ttu-id="e7a8e-108">Un nodo XML representa un único fragmento de XML, por ejemplo, un elemento de inicio y sus atributos, un elemento final, texto o contenido de texto "con tipo", como un entero o una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="e7a8e-108">An XML Node represents a single piece of XML, for example, a start element and its attributes, an end element, text, or "typed" text content such as an integer or byte array.</span></span> <span data-ttu-id="e7a8e-109">Los datos de un nodo varían según el [**tipo de \_ \_ nodo XML \_ de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).</span><span class="sxs-lookup"><span data-stu-id="e7a8e-109">The data in a node varies according to the [**WS\_XML\_NODE\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).</span></span>


<span data-ttu-id="e7a8e-110">A continuación se muestra un ejemplo de un documento XML específico de codificación representado con estructuras independientes de codificación.</span><span class="sxs-lookup"><span data-stu-id="e7a8e-110">The following shows an example of an encoding specific xml document represented with encoding independent structures.</span></span>

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

<span data-ttu-id="e7a8e-111">Las enumeraciones siguientes se utilizan con nodos XML:</span><span class="sxs-lookup"><span data-stu-id="e7a8e-111">The following enumerations are used with XML nodes:</span></span>

-   [<span data-ttu-id="e7a8e-112">**\_tipo de valor WS \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-112">**WS\_VALUE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [<span data-ttu-id="e7a8e-113">**\_tipo de \_ nodo \_ XML de WS**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-113">**WS\_XML\_NODE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [<span data-ttu-id="e7a8e-114">**\_tipo de \_ texto \_ XML de WS**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-114">**WS\_XML\_TEXT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

<span data-ttu-id="e7a8e-115">Las siguientes funciones se usan con nodos XML:</span><span class="sxs-lookup"><span data-stu-id="e7a8e-115">The following functions are used with XML nodes:</span></span>

-   [<span data-ttu-id="e7a8e-116">**WsTrimXmlWhitespace**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-116">**WsTrimXmlWhitespace**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [<span data-ttu-id="e7a8e-117">**WsVerifyXmlNCName**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-117">**WsVerifyXmlNCName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [<span data-ttu-id="e7a8e-118">**WsXmlStringEquals**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-118">**WsXmlStringEquals**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

<span data-ttu-id="e7a8e-119">Las macros siguientes se utilizan con nodos XML:</span><span class="sxs-lookup"><span data-stu-id="e7a8e-119">The following macros are used with XML nodes:</span></span>

-   [<span data-ttu-id="e7a8e-120">**\_valor del \_ Diccionario de cadenas XML \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-120">**WS\_XML\_STRING\_DICTIONARY\_VALUE**</span></span>](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   <span data-ttu-id="e7a8e-121">[**\_ \_ cadena \_ null de WS XML**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e7a8e-121">[**WS\_XML\_STRING\_NULL**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))</span></span>
-   [<span data-ttu-id="e7a8e-122">**\_valor de \_ cadena \_ XML de WS**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-122">**WS\_XML\_STRING\_VALUE**</span></span>](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

<span data-ttu-id="e7a8e-123">Las siguientes estructuras se utilizan con nodos XML:</span><span class="sxs-lookup"><span data-stu-id="e7a8e-123">The following structures are used with XML nodes:</span></span>

-   [<span data-ttu-id="e7a8e-124">**\_atributo XML de WS \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-124">**WS\_XML\_ATTRIBUTE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [<span data-ttu-id="e7a8e-125">**Texto de WS \_ XML \_ Base64 \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-125">**WS\_XML\_BASE64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [<span data-ttu-id="e7a8e-126">**\_ \_ texto BOOLEANO de WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-126">**WS\_XML\_BOOL\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [<span data-ttu-id="e7a8e-127">**nodo de comentario de WS \_ XML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-127">**WS\_XML\_COMMENT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [<span data-ttu-id="e7a8e-128">**\_texto de \_ fecha y hora XML de WS \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-128">**WS\_XML\_DATETIME\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [<span data-ttu-id="e7a8e-129">**\_ \_ texto decimal de WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-129">**WS\_XML\_DECIMAL\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [<span data-ttu-id="e7a8e-130">**Diccionario de WS \_ XML \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-130">**WS\_XML\_DICTIONARY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [<span data-ttu-id="e7a8e-131">**\_ \_ texto Double de WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-131">**WS\_XML\_DOUBLE\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [<span data-ttu-id="e7a8e-132">**\_nodo de \_ elemento \_ XML de WS**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-132">**WS\_XML\_ELEMENT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [<span data-ttu-id="e7a8e-133">**\_ \_ texto flotante de WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-133">**WS\_XML\_FLOAT\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [<span data-ttu-id="e7a8e-134">**texto del GUID de WS \_ XML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-134">**WS\_XML\_GUID\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [<span data-ttu-id="e7a8e-135">**\_Texto XML \_ INT32 de WS \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-135">**WS\_XML\_INT32\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [<span data-ttu-id="e7a8e-136">**\_ \_ Texto INT64 XML de WS \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-136">**WS\_XML\_INT64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [<span data-ttu-id="e7a8e-137">**\_texto de \_ lista \_ XML de WS**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-137">**WS\_XML\_LIST\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [<span data-ttu-id="e7a8e-138">**\_nodo XML de WS \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-138">**WS\_XML\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [<span data-ttu-id="e7a8e-139">**\_QNAME XML de WS \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-139">**WS\_XML\_QNAME**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [<span data-ttu-id="e7a8e-140">**\_ \_ texto QNAME XML de WS \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-140">**WS\_XML\_QNAME\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [<span data-ttu-id="e7a8e-141">**\_cadena XML de WS \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-141">**WS\_XML\_STRING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [<span data-ttu-id="e7a8e-142">**\_texto XML de WS \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-142">**WS\_XML\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [<span data-ttu-id="e7a8e-143">**\_nodo de \_ texto \_ XML de WS**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-143">**WS\_XML\_TEXT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [<span data-ttu-id="e7a8e-144">**\_texto de \_ TIMESPAN \_ XML de WS**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-144">**WS\_XML\_TIMESPAN\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [<span data-ttu-id="e7a8e-145">**\_ \_ Texto UINT64 XML de WS \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-145">**WS\_XML\_UINT64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [<span data-ttu-id="e7a8e-146">**\_texto de \_ \_ identificador único \_ de WS XML**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-146">**WS\_XML\_UNIQUE\_ID\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [<span data-ttu-id="e7a8e-147">**\_ \_ Texto UTF16 XML de WS \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-147">**WS\_XML\_UTF16\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [<span data-ttu-id="e7a8e-148">**\_ \_ Texto UTF8 de WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="e7a8e-148">**WS\_XML\_UTF8\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 