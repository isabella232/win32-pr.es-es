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
# <a name="xml-reader"></a><span data-ttu-id="56bd6-107">Lector de XML</span><span class="sxs-lookup"><span data-stu-id="56bd6-107">XML Reader</span></span>

<span data-ttu-id="56bd6-108">El lector XML es un cursor sobre un origen de entrada de XML.</span><span class="sxs-lookup"><span data-stu-id="56bd6-108">XML Reader is a cursor over an input source of XML.</span></span> <span data-ttu-id="56bd6-109">En esencia, un lector XML Lee un [nodo XML](xml-node.md) a la vez, pero hay otras API auxiliares que facilitan la lectura de una secuencia de nodos.</span><span class="sxs-lookup"><span data-stu-id="56bd6-109">At its core, an XML Reader reads one [XML Node](xml-node.md) at a time, but there are additional helper APIs to make reading a sequence of nodes easier.</span></span>


<span data-ttu-id="56bd6-110">Se admiten los siguientes tipos de entrada de lectores:</span><span class="sxs-lookup"><span data-stu-id="56bd6-110">The following types of readers input are supported:</span></span>

-   [<span data-ttu-id="56bd6-111">**Búfer en memoria de bytes codificados**</span><span class="sxs-lookup"><span data-stu-id="56bd6-111">**An in-memory buffer of encoded bytes**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [<span data-ttu-id="56bd6-112">**Un flujo**</span><span class="sxs-lookup"><span data-stu-id="56bd6-112">**A stream**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   <span data-ttu-id="56bd6-113">Un [búfer XML](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="56bd6-113">An [XML Buffer](xml-buffer.md)</span></span>

### <a name="security"></a><span data-ttu-id="56bd6-114">Seguridad</span><span class="sxs-lookup"><span data-stu-id="56bd6-114">Security</span></span>

<span data-ttu-id="56bd6-115">El lector comprobará que los atributos presentes en un elemento son únicos.</span><span class="sxs-lookup"><span data-stu-id="56bd6-115">The reader will verify that the attributes present on an element are unique.</span></span> <span data-ttu-id="56bd6-116">El tiempo necesario para realizar esta validación es una función del número de atributos en el elemento que puede ser tan grande como [**\_ \_ atributos Max XML Reader \_ Property \_ Max \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span><span class="sxs-lookup"><span data-stu-id="56bd6-116">The time required to perform this validation is a function of the number of attributes on the element which can be as large as [**WS\_XML\_READER\_PROPERTY\_MAX\_ATTRIBUTES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span></span> <span data-ttu-id="56bd6-117">Por lo tanto, el procesamiento de documentos grandes cuando la **\_ \_ \_ propiedad Max XML Reader Property \_ Max \_ attributes** está establecida en un valor grande puede presentar una oportunidad para un ataque por denegación de servicio.</span><span class="sxs-lookup"><span data-stu-id="56bd6-117">Therefore, processing large documents when **WS\_XML\_READER\_PROPERTY\_MAX\_ATTRIBUTES** is set to a large value may present an opportunity for a denial of service attack.</span></span>

<span data-ttu-id="56bd6-118">El lector asignará prefijos a los espacios de nombres de cada elemento y atributos.</span><span class="sxs-lookup"><span data-stu-id="56bd6-118">The reader will map prefixes to namespaces for each element and attributes.</span></span> <span data-ttu-id="56bd6-119">El tiempo necesario para realizar esta asignación es una función del número de atributos xmlns en el ámbito, que puede ser tan grande como los [**\_ espacios de \_ \_ \_ \_ nombres Max XML Reader Property Max**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span><span class="sxs-lookup"><span data-stu-id="56bd6-119">The time required to perform this mapping is a function of the number of xmlns attributes in scope which may be as large as [**WS\_XML\_READER\_PROPERTY\_MAX\_NAMESPACES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span></span> <span data-ttu-id="56bd6-120">Por lo tanto, el procesamiento de documentos grandes cuando esta propiedad se establece en un valor grande puede presentar una oportunidad para un ataque por denegación de servicio.</span><span class="sxs-lookup"><span data-stu-id="56bd6-120">Therefore, processing large documents when this property is set to a large value may present an opportunity for a denial of service attack.</span></span>

<span data-ttu-id="56bd6-121">Aunque el lector se asegurará de que el documento sigue la especificación gramatical de XML y de que sus aspectos estén dentro de las cuotas especificadas, el contenido del documento se debe considerar como no de confianza cuando proceda de un origen que no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="56bd6-121">While the reader will ensure that the document follows the grammatical specification of xml and furthermore that its aspects are within the quotas specified, the content of the document must still be considered untrusted when coming from an untrusted source.</span></span> <span data-ttu-id="56bd6-122">Los usuarios del lector deben comprobar todos los nombres de elementos y atributos, así como los espacios de nombres que usan [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)o mediante la inspección manual de los [**nodos**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).</span><span class="sxs-lookup"><span data-stu-id="56bd6-122">Users of the reader should check all element and attribute names and namespaces using [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute), or by manually inspecting [**nodes**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).</span></span>

<span data-ttu-id="56bd6-123">Algunas otras situaciones a tener en cuenta son, entre otras:</span><span class="sxs-lookup"><span data-stu-id="56bd6-123">Some other situations to consider include, but are not limited to:</span></span>

-   <span data-ttu-id="56bd6-124">Puede que falten elementos esperados</span><span class="sxs-lookup"><span data-stu-id="56bd6-124">Expected elements may be missing</span></span>
-   <span data-ttu-id="56bd6-125">Pueden aparecer elementos inesperados</span><span class="sxs-lookup"><span data-stu-id="56bd6-125">Unexpected elements may appear</span></span>
-   <span data-ttu-id="56bd6-126">Puede que falten los atributos esperados</span><span class="sxs-lookup"><span data-stu-id="56bd6-126">Expected attributes may be missing</span></span>
-   <span data-ttu-id="56bd6-127">Pueden aparecer atributos inesperados</span><span class="sxs-lookup"><span data-stu-id="56bd6-127">Unexpected attributes may appear</span></span>
-   <span data-ttu-id="56bd6-128">Los elementos pueden aparecer como elementos vacíos</span><span class="sxs-lookup"><span data-stu-id="56bd6-128">Elements may appear as empty elements</span></span>
-   <span data-ttu-id="56bd6-129">Puede aparecer un espacio en blanco en lugares inesperados</span><span class="sxs-lookup"><span data-stu-id="56bd6-129">Whitespace may appear in unexpected places</span></span>

<span data-ttu-id="56bd6-130">Los usuarios del lector no deben asignar memoria basándose simplemente en los valores leídos del documento.</span><span class="sxs-lookup"><span data-stu-id="56bd6-130">Users of the reader should not allocate memory based simply on values read from the document.</span></span> <span data-ttu-id="56bd6-131">Por ejemplo, considere el siguiente documento XML:</span><span class="sxs-lookup"><span data-stu-id="56bd6-131">For example, consider the following xml document:</span></span>

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

<span data-ttu-id="56bd6-132">Asignar una matriz basada exclusivamente en la suposición de que un número de elementos seguirá un posible vector de ataque.</span><span class="sxs-lookup"><span data-stu-id="56bd6-132">Allocating an array based soley on the assumption that some number of elements will follow would be a potential attack vector.</span></span> <span data-ttu-id="56bd6-133">En este caso, el usuario del lector debe asignar incrementalmente la memoria a medida que aparezcan los elementos.</span><span class="sxs-lookup"><span data-stu-id="56bd6-133">The user of the reader in this case should instead incrementally allocate the memory as the elements appear.</span></span>

<span data-ttu-id="56bd6-134">El lector XML no admite DTD.</span><span class="sxs-lookup"><span data-stu-id="56bd6-134">XML reader does not support DTD.</span></span> <span data-ttu-id="56bd6-135">No es necesario que el usuario del lector tenga que preocuparse por la comprobación de DTD.</span><span class="sxs-lookup"><span data-stu-id="56bd6-135">The user of the reader does not need to concern about DTD verification.</span></span>

<span data-ttu-id="56bd6-136">La siguiente devolución de llamada se utiliza con los lectores XML:</span><span class="sxs-lookup"><span data-stu-id="56bd6-136">The following callback is used with XML readers:</span></span>

-   [<span data-ttu-id="56bd6-137">**devolución de llamada de \_ lectura de WS \_**</span><span class="sxs-lookup"><span data-stu-id="56bd6-137">**WS\_READ\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

<span data-ttu-id="56bd6-138">Las enumeraciones siguientes se usan con los lectores XML:</span><span class="sxs-lookup"><span data-stu-id="56bd6-138">The following enumerations are used with XML readers:</span></span>

-   [<span data-ttu-id="56bd6-139">**\_tipo de \_ codificación del lector XML \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="56bd6-139">**WS\_XML\_READER\_ENCODING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [<span data-ttu-id="56bd6-140">**\_tipo de \_ entrada del lector XML \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="56bd6-140">**WS\_XML\_READER\_INPUT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [<span data-ttu-id="56bd6-141">**\_identificador de \_ propiedad del lector de XML de WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="56bd6-141">**WS\_XML\_READER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

<span data-ttu-id="56bd6-142">Las siguientes funciones se usan con los lectores XML:</span><span class="sxs-lookup"><span data-stu-id="56bd6-142">The following functions are used with XML readers:</span></span>

-   [<span data-ttu-id="56bd6-143">**WsCreateReader**</span><span class="sxs-lookup"><span data-stu-id="56bd6-143">**WsCreateReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatereader)
-   [<span data-ttu-id="56bd6-144">**WsFillReader**</span><span class="sxs-lookup"><span data-stu-id="56bd6-144">**WsFillReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfillreader)
-   [<span data-ttu-id="56bd6-145">**WsFindAttribute**</span><span class="sxs-lookup"><span data-stu-id="56bd6-145">**WsFindAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)
-   [<span data-ttu-id="56bd6-146">**WsFreeReader**</span><span class="sxs-lookup"><span data-stu-id="56bd6-146">**WsFreeReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreereader)
-   [<span data-ttu-id="56bd6-147">**WsGetNamespaceFromPrefix**</span><span class="sxs-lookup"><span data-stu-id="56bd6-147">**WsGetNamespaceFromPrefix**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetnamespacefromprefix)
-   [<span data-ttu-id="56bd6-148">**WsGetReaderNode**</span><span class="sxs-lookup"><span data-stu-id="56bd6-148">**WsGetReaderNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreadernode)
-   [<span data-ttu-id="56bd6-149">**WsGetReaderPosition**</span><span class="sxs-lookup"><span data-stu-id="56bd6-149">**WsGetReaderPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition)
-   [<span data-ttu-id="56bd6-150">**WsGetReaderProperty**</span><span class="sxs-lookup"><span data-stu-id="56bd6-150">**WsGetReaderProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderproperty)
-   [<span data-ttu-id="56bd6-151">**WsGetXmlAttribute**</span><span class="sxs-lookup"><span data-stu-id="56bd6-151">**WsGetXmlAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute)
-   [<span data-ttu-id="56bd6-152">**WsMoveReader**</span><span class="sxs-lookup"><span data-stu-id="56bd6-152">**WsMoveReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmovereader)
-   [<span data-ttu-id="56bd6-153">**WsReadArray**</span><span class="sxs-lookup"><span data-stu-id="56bd6-153">**WsReadArray**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadarray)
-   [<span data-ttu-id="56bd6-154">**WsReadBytes**</span><span class="sxs-lookup"><span data-stu-id="56bd6-154">**WsReadBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadbytes)
-   [<span data-ttu-id="56bd6-155">**WsReadChars**</span><span class="sxs-lookup"><span data-stu-id="56bd6-155">**WsReadChars**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadchars)
-   [<span data-ttu-id="56bd6-156">**WsReadCharsUtf8**</span><span class="sxs-lookup"><span data-stu-id="56bd6-156">**WsReadCharsUtf8**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadcharsutf8)
-   [<span data-ttu-id="56bd6-157">**WsReadEndAttribute**</span><span class="sxs-lookup"><span data-stu-id="56bd6-157">**WsReadEndAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadendattribute)
-   [<span data-ttu-id="56bd6-158">**WsReadEndElement**</span><span class="sxs-lookup"><span data-stu-id="56bd6-158">**WsReadEndElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement)
-   [<span data-ttu-id="56bd6-159">**WsReadNode**</span><span class="sxs-lookup"><span data-stu-id="56bd6-159">**WsReadNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadnode)
-   [<span data-ttu-id="56bd6-160">**WsReadQualifiedName**</span><span class="sxs-lookup"><span data-stu-id="56bd6-160">**WsReadQualifiedName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadqualifiedname)
-   [<span data-ttu-id="56bd6-161">**WsReadStartAttribute**</span><span class="sxs-lookup"><span data-stu-id="56bd6-161">**WsReadStartAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadstartattribute)
-   [<span data-ttu-id="56bd6-162">**WsReadStartElement**</span><span class="sxs-lookup"><span data-stu-id="56bd6-162">**WsReadStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement)
-   [<span data-ttu-id="56bd6-163">**WsReadToStartElement**</span><span class="sxs-lookup"><span data-stu-id="56bd6-163">**WsReadToStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)
-   [<span data-ttu-id="56bd6-164">**WsReadValue**</span><span class="sxs-lookup"><span data-stu-id="56bd6-164">**WsReadValue**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue)
-   [<span data-ttu-id="56bd6-165">**WsSetInput**</span><span class="sxs-lookup"><span data-stu-id="56bd6-165">**WsSetInput**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetinput)
-   [<span data-ttu-id="56bd6-166">**WsSetInputToBuffer**</span><span class="sxs-lookup"><span data-stu-id="56bd6-166">**WsSetInputToBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer)
-   [<span data-ttu-id="56bd6-167">**WsSetReaderPosition**</span><span class="sxs-lookup"><span data-stu-id="56bd6-167">**WsSetReaderPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition)
-   [<span data-ttu-id="56bd6-168">**WsSkipNode**</span><span class="sxs-lookup"><span data-stu-id="56bd6-168">**WsSkipNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsskipnode)

<span data-ttu-id="56bd6-169">El siguiente identificador se usa con los lectores XML:</span><span class="sxs-lookup"><span data-stu-id="56bd6-169">The following handle is used with XML readers:</span></span>

-   [<span data-ttu-id="56bd6-170">\_lector de XML de WS \_</span><span class="sxs-lookup"><span data-stu-id="56bd6-170">WS\_XML\_READER</span></span>](ws-xml-reader.md)

<span data-ttu-id="56bd6-171">Las siguientes estructuras se utilizan con los lectores XML:</span><span class="sxs-lookup"><span data-stu-id="56bd6-171">The following structures are used with XML readers:</span></span>

-   [<span data-ttu-id="56bd6-172">**\_ \_ \_ codificación binaria del lector de WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="56bd6-172">**WS\_XML\_READER\_BINARY\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [<span data-ttu-id="56bd6-173">**\_entrada de \_ búfer de lector XML \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="56bd6-173">**WS\_XML\_READER\_BUFFER\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [<span data-ttu-id="56bd6-174">**\_codificación del \_ lector \_ XML de WS**</span><span class="sxs-lookup"><span data-stu-id="56bd6-174">**WS\_XML\_READER\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [<span data-ttu-id="56bd6-175">**\_entrada de \_ lector \_ XML de WS**</span><span class="sxs-lookup"><span data-stu-id="56bd6-175">**WS\_XML\_READER\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [<span data-ttu-id="56bd6-176">**\_ \_ codificación MTOM del lector XML \_ de \_ WS**</span><span class="sxs-lookup"><span data-stu-id="56bd6-176">**WS\_XML\_READER\_MTOM\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [<span data-ttu-id="56bd6-177">**\_propiedades del \_ lector de XML de WS \_**</span><span class="sxs-lookup"><span data-stu-id="56bd6-177">**WS\_XML\_READER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [<span data-ttu-id="56bd6-178">**\_propiedad del \_ lector de XML de WS \_**</span><span class="sxs-lookup"><span data-stu-id="56bd6-178">**WS\_XML\_READER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [<span data-ttu-id="56bd6-179">**\_entrada de \_ flujo del lector XML \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="56bd6-179">**WS\_XML\_READER\_STREAM\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [<span data-ttu-id="56bd6-180">**\_codificación de \_ texto del lector XML \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="56bd6-180">**WS\_XML\_READER\_TEXT\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 




