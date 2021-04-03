---
title: Información general sobre capas XML
description: La API XML en WWSAPI se basa en los objetos lector XML y escritor XML, que permiten leer o escribir documentos XML en un modo de solo avance. El nivel XML proporciona a la aplicación acceso completo y control sobre el contenido de los mensajes.
ms.assetid: 938ca257-fbb8-4569-b791-2148abb1a5a5
keywords:
- Información general de la capa XML servicios web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9b5d062754adea7b48bd42a6a501ce17d0e332b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776243"
---
# <a name="xml-layer-overview"></a><span data-ttu-id="ed347-107">Información general sobre capas XML</span><span class="sxs-lookup"><span data-stu-id="ed347-107">XML Layer Overview</span></span>

<span data-ttu-id="ed347-108">La API XML en WWSAPI se basa en los objetos [lector](xml-reader.md) XML y [escritor XML](xml-writer.md) , que permiten leer o escribir documentos XML en un modo de solo avance.</span><span class="sxs-lookup"><span data-stu-id="ed347-108">The XML API in WWSAPI is based on the [XML Reader](xml-reader.md) and [XML Writer](xml-writer.md) objects, which allow reading or writing of XML documents in a forward only fashion.</span></span> <span data-ttu-id="ed347-109">El nivel XML proporciona a la aplicación acceso completo y control sobre el contenido de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="ed347-109">The XML Layer give the application full access to and control over the content of messages.</span></span>

## <a name="encoding"></a><span data-ttu-id="ed347-110">Encoding</span><span class="sxs-lookup"><span data-stu-id="ed347-110">Encoding</span></span>

<span data-ttu-id="ed347-111">La API XML admite documentos codificados como:</span><span class="sxs-lookup"><span data-stu-id="ed347-111">The XML API supports documents encoded as:</span></span>

-   <span data-ttu-id="ed347-112">Texto (UTF-8, UTF-16LE, UTF-16BE)</span><span class="sxs-lookup"><span data-stu-id="ed347-112">Text (UTF-8, UTF-16LE, UTF-16BE)</span></span>
-   <span data-ttu-id="ed347-113">Binary</span><span class="sxs-lookup"><span data-stu-id="ed347-113">Binary</span></span>
-   <span data-ttu-id="ed347-114">MTOM</span><span class="sxs-lookup"><span data-stu-id="ed347-114">MTOM</span></span>

## <a name="storage"></a><span data-ttu-id="ed347-115">Almacenamiento</span><span class="sxs-lookup"><span data-stu-id="ed347-115">Storage</span></span>

<span data-ttu-id="ed347-116">La API XML admite el procesamiento de documentos almacenados como:</span><span class="sxs-lookup"><span data-stu-id="ed347-116">The XML API supports processing documents stored as:</span></span>

-   <span data-ttu-id="ed347-117">Búfer en memoria de bytes codificados</span><span class="sxs-lookup"><span data-stu-id="ed347-117">An in-memory buffer of encoded bytes</span></span>
-   <span data-ttu-id="ed347-118">Un flujo</span><span class="sxs-lookup"><span data-stu-id="ed347-118">A stream</span></span>
-   <span data-ttu-id="ed347-119">Un [búfer XML](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="ed347-119">An [XML Buffer](xml-buffer.md)</span></span>

<span data-ttu-id="ed347-120">Un [búfer XML](xml-buffer.md) es una representación en memoria estructurada de un documento XML.</span><span class="sxs-lookup"><span data-stu-id="ed347-120">An [XML Buffer](xml-buffer.md) is a structured in-memory representation of an XML document.</span></span> <span data-ttu-id="ed347-121">Se trata de una representación más eficaz que un documento codificado como bytes.</span><span class="sxs-lookup"><span data-stu-id="ed347-121">This is a more efficient representation than a document encoded as bytes.</span></span> <span data-ttu-id="ed347-122">Se puede navegar, leer o escribir un documento XML almacenado en un búfer XML.</span><span class="sxs-lookup"><span data-stu-id="ed347-122">An XML document stored in an An XML Buffer can be navigated, read, or written.</span></span>

## <a name="io"></a><span data-ttu-id="ed347-123">E/S</span><span class="sxs-lookup"><span data-stu-id="ed347-123">I/O</span></span>

<span data-ttu-id="ed347-124">La API XML nunca realizará la e/s a menos que se solicite específicamente.</span><span class="sxs-lookup"><span data-stu-id="ed347-124">The XML API will never perform I/O unless specifically requested.</span></span> <span data-ttu-id="ed347-125">Además, cualquier e/s se puede iniciar de manera asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ed347-125">Furthermore, any I/O may be initiated in an asynchronous fashion.</span></span> <span data-ttu-id="ed347-126">Vea [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader) y [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter) para obtener información detallada sobre el procesamiento asincrónico con la API de XML.</span><span class="sxs-lookup"><span data-stu-id="ed347-126">See [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader) and [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter) for details on asynchronous processing with the XML API.</span></span>

## <a name="processing"></a><span data-ttu-id="ed347-127">Processing</span><span class="sxs-lookup"><span data-stu-id="ed347-127">Processing</span></span>

<span data-ttu-id="ed347-128">La API XML tiene tres niveles distintos en los que se puede procesar el documento.</span><span class="sxs-lookup"><span data-stu-id="ed347-128">The XML API has three distinct levels at which the document may be processed.</span></span>

<span data-ttu-id="ed347-129">Un documento se puede procesar en un [**nodo**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node) a la vez.</span><span class="sxs-lookup"><span data-stu-id="ed347-129">A document may be processed a [**node**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node) at a time.</span></span> <span data-ttu-id="ed347-130">Esto ofrece la administración más específica del contenido XML y proporciona una fidelidad completa de los datos del documento.</span><span class="sxs-lookup"><span data-stu-id="ed347-130">This offers the most fine-grained handling of the XML content, and provides complete fidelity of data from the document.</span></span> <span data-ttu-id="ed347-131">En este nivel, se utilizarán las funciones [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode) y [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode) y [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode) .</span><span class="sxs-lookup"><span data-stu-id="ed347-131">At this level, the functions [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode) and [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode) and [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode) would be used.</span></span>

<span data-ttu-id="ed347-132">El siguiente nivel de control son las API como [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement), [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue) y [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement).</span><span class="sxs-lookup"><span data-stu-id="ed347-132">The next level of control are APIs like [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement), [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue) and [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement).</span></span> <span data-ttu-id="ed347-133">Estas API proporcionan numerosos tipos de validación, omiten el espacio en blanco y los comentarios, y normalizan el texto y CDATA para presentar al consumidor una vista más sencilla del XML.</span><span class="sxs-lookup"><span data-stu-id="ed347-133">These APIs provide numerous kinds of validation, skip whitespace and comments, and normalize text and CDATA to present the consumer with a simpler view of the xml.</span></span>

<span data-ttu-id="ed347-134">El nivel más alto de control consiste en usar la API de serialización.</span><span class="sxs-lookup"><span data-stu-id="ed347-134">The highest level of control is to use the Serialization API.</span></span> <span data-ttu-id="ed347-135">Estas API se impulsan de una asignación entre los tipos de datos de C y XML, y pueden leer o escribir una estructura compleja en memoria en XML y volver con una sola función como [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement) y [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement).</span><span class="sxs-lookup"><span data-stu-id="ed347-135">These APIs are driven off a mapping between C data types and XML, and can read or write a complex in-memory structure to xml and back with a single function like [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement) and [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement).</span></span>

<span data-ttu-id="ed347-136">Las API de canonización XML se pueden usar para generar una forma canónica de XML que, a su vez, se puede usar para generar firmas criptográficas sobre contenido XML.</span><span class="sxs-lookup"><span data-stu-id="ed347-136">The XML Canonicalization APIs may be used to generate a canonical form of XML which may in turn be used for generating cryptographic signatures over XML content.</span></span>

## <a name="creating-a-writer"></a><span data-ttu-id="ed347-137">Creación de un escritor</span><span class="sxs-lookup"><span data-stu-id="ed347-137">Creating a writer</span></span>

<span data-ttu-id="ed347-138">Para crear y usar un escritor para escribir en un búfer en memoria:</span><span class="sxs-lookup"><span data-stu-id="ed347-138">To create and use a writer to write to an in-memory buffer:</span></span>

``` syntax
WsCreateWriter              // Create an instance of a WS_XML_WRITER
// Initialize a WS_XML_WRITER_BUFFER_OUTPUT
WsSetOutput                 // Set the encoding and output of the writer along with any other writer properties
// Write Elements
WsGetWriterProperty(..., WS_XML_WRITER_PROPERTY_BYTES, ...)  // Get the generated bytes as a single byte array
// Use the generated bytes
WsFreeWriter                // Free the writer
```

<span data-ttu-id="ed347-139">Para crear y usar un escritor para escribir en una secuencia:</span><span class="sxs-lookup"><span data-stu-id="ed347-139">To create and use a writer to write to a stream:</span></span>

``` syntax
WsCreateWriter              // Create an instance of a WS_XML_WRITER
// Initialize a WS_XML_WRITER_STREAM_OUTPUT
WsSetOutput                 // Set the encoding and output of the writer along with any other writer properties
// Write Elements
WsFlushWriter               // Force any buffered data to be written
WsFreeWriter                // Free the writer
```

<span data-ttu-id="ed347-140">Para crear y usar un escritor para escribir en un [ \_ \_ búfer de WS XML](ws-xml-buffer.md):</span><span class="sxs-lookup"><span data-stu-id="ed347-140">To create and use a writer to write to a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax
WsCreateXmlBuffer           // Create the buffer to write to
WsCreateWriter              // Create an instance of a WS_XML_WRITER
WsSetOutputToBuffer         // Set the output buffer along with any other writer properties
// Write Elements
WsFreeWriter                // Free the writer
// The buffer has the generated document
```

<span data-ttu-id="ed347-141">En todos los casos, se puede incluir la propiedad de la propiedad del [**\_ \_ escritor \_ \_ XML de WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id) para dar formato al XML.</span><span class="sxs-lookup"><span data-stu-id="ed347-141">In all cases, the property [**WS\_XML\_WRITER\_PROPERTY\_INDENT**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id) may be included to format the xml.</span></span>

## <a name="writing-elements"></a><span data-ttu-id="ed347-142">Escritura de elementos</span><span class="sxs-lookup"><span data-stu-id="ed347-142">Writing Elements</span></span>

<span data-ttu-id="ed347-143">Para escribir un elemento en un escritor:</span><span class="sxs-lookup"><span data-stu-id="ed347-143">To write an element to a writer:</span></span>

``` syntax
WsWriteStartElement          // Write a start element
for each attribute
{
// Write an attribute using either
WsWriteStartAttribute    // Write a start attribute
// Write Content
WsWriteEndAttribute      // Write an end attribute
// Or one of the following
WsWriteXmlnsAttribute    // Write an explicit xmlns attribute
}
// Write Elements or Content
WsWriteEndElement
```

<span data-ttu-id="ed347-144">También se puede utilizar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ed347-144">The following may also be used:</span></span>

``` syntax
WsWriteArray                 // Write an array of primitive values as a series of repeated elements
```

## <a name="writing-content"></a><span data-ttu-id="ed347-145">Escribir contenido</span><span class="sxs-lookup"><span data-stu-id="ed347-145">Writing Content</span></span>

<span data-ttu-id="ed347-146">Para escribir contenido en un elemento o atributo, se puede utilizar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ed347-146">To write content to an element or attribute, the following may be used:</span></span>

``` syntax
WsWriteChars                 // Write unicode characters from memory
WsWriteCharsUtf8             // Write UTF-8 encoded characters from memory
WsWriteBytes                 // Write binary data encoded as base64
WsPushBytes                  // Direct the writer to request that bytes be written
WsPullBytes                  // Direct the writer to read the bytes to be written
WsWriteValue                 // Write primitive values such as ints and BOOLs
WsWriteText                  // Write an WS_XML_TEXT
WsWriteQualifiedName         // Write a qualified name
```

<span data-ttu-id="ed347-147">Se puede utilizar lo siguiente para escribir en un documento, pero no se puede usar cuando está dentro de un atributo.</span><span class="sxs-lookup"><span data-stu-id="ed347-147">The following can be used to write to a document, but may not be used when within an attribute.</span></span>

``` syntax
WsWriteNode                  // Write a single WS_XML_NODE
WsCopyNode                   // Copy a single node, or an entire WS_XML_ELEMENT_NODE and children from an WS_XML_READER
```

<span data-ttu-id="ed347-148">Puede usar lo siguiente para escribir una sección CDATA en un documento de texto:</span><span class="sxs-lookup"><span data-stu-id="ed347-148">The following may be used to write a CDATA section in a text document:</span></span>

``` syntax
WsWriteStartCData            // Start a CDATA section in a text encoding
// Write Content
WsWriteEndCData              // End a CDATA section in text encoding
```

## <a name="miscellaneous"></a><span data-ttu-id="ed347-149">Varios</span><span class="sxs-lookup"><span data-stu-id="ed347-149">Miscellaneous</span></span>

``` syntax
WsGetPrefixFromNamespace     // Find a prefix bound to a namespace
```

## <a name="creating-a-reader"></a><span data-ttu-id="ed347-150">Crear un lector</span><span class="sxs-lookup"><span data-stu-id="ed347-150">Creating a reader</span></span>

<span data-ttu-id="ed347-151">Para crear y usar un lector para leer desde un búfer en memoria:</span><span class="sxs-lookup"><span data-stu-id="ed347-151">To create and use a reader to read from an in-memory buffer:</span></span>

``` syntax
WsCreateReader              // Create an instance of a WS_XML_READER
// Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput                  // Set the encoding and input of the reader along with any other reader properties
// Read Elements
WsFreeReader                // Free the reader
```

<span data-ttu-id="ed347-152">Para crear y usar un lector para el lector de una secuencia:</span><span class="sxs-lookup"><span data-stu-id="ed347-152">To create and use a reader to reader from a stream:</span></span>

``` syntax
WsCreateReader              // Create an instance of a WS_XML_READER
// Initialize a WS_XML_READER_STREAM_INPUT
WsSetInput                  // Set the encoding and input of the reader along with any other reader properties
WsFillReader                // Populate the reader with data from the underlying stream
// Read Elements
WsFreeReader                // Free the reader
```

<span data-ttu-id="ed347-153">Para crear y usar un lector para leer desde un [ \_ \_ búfer de WS XML](ws-xml-buffer.md):</span><span class="sxs-lookup"><span data-stu-id="ed347-153">To create and use a reader to read from a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax
WsCreateXmlBuffer           // Create the buffer to write to
WsCreateReader              // Create an instance of a WS_XML_READER
WsSetInputToBuffer          // Set the input buffer along with any other reader properties
// Read Elements
WsFreeReader                // Free the reader
```

## <a name="reading-elements"></a><span data-ttu-id="ed347-154">Lectura de elementos</span><span class="sxs-lookup"><span data-stu-id="ed347-154">Reading Elements</span></span>

<span data-ttu-id="ed347-155">Para leer un elemento de un lector:</span><span class="sxs-lookup"><span data-stu-id="ed347-155">To read an element from a reader:</span></span>

``` syntax
WsReadToStartElement         // Skip whitespace and comments to position the reader on a specific element
for each attribute of interest
{
WsFindAttribute          // Try Locate the attribute
if (found)
{
WsReadStartAttribute // Set the reader to read the attribute
// Read Content
WsReadEndAttribute   // Return the reader to the element
}
}
WsReadStartElement           // Advance the reader past the current element
// Read Elements or Content
WsWriteEndElement            // Advance the reader past the corresponding end element
```

<span data-ttu-id="ed347-156">También se puede utilizar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ed347-156">The following may also be used:</span></span>

``` syntax
WsReadArray                  // Read an array of primitive values as a series of repeated elements
```

## <a name="reading-content"></a><span data-ttu-id="ed347-157">Lectura de contenido</span><span class="sxs-lookup"><span data-stu-id="ed347-157">Reading Content</span></span>

<span data-ttu-id="ed347-158">Para leer el contenido de un elemento o atributo, se puede utilizar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ed347-158">To read content from an element or attribute, the following may be used:</span></span>

``` syntax
WsReadChars                 // Read characters to memory as unicode
WsReadCharsUtf8             // Read characters to memory encoded as UTF-8
WsReadBytes                 // Read binary data encoded as base64
WsReadValue                 // Read primitive values such as ints and BOOLs
WsReadQualifiedName         // Read a qualified name
```

<span data-ttu-id="ed347-159">Se puede utilizar lo siguiente para inspeccionar el nodo actual en el que está situado el lector:</span><span class="sxs-lookup"><span data-stu-id="ed347-159">The following may be used to inspect the current node the reader is positioned on:</span></span>

``` syntax
WsGetReaderNode             // Get the current node
```

## <a name="using-a-buffer"></a><span data-ttu-id="ed347-160">Usar un búfer</span><span class="sxs-lookup"><span data-stu-id="ed347-160">Using a buffer</span></span>

<span data-ttu-id="ed347-161">Al escribir en un [ \_ \_ búfer de WS XML](ws-xml-buffer.md) , se puede utilizar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ed347-161">When writing to a [WS\_XML\_BUFFER](ws-xml-buffer.md) the following may be used:</span></span>

``` syntax
WsGetWriterPosition          // Get the current position of the writer in the document
WsSetWriterPosition          // Set the current position of the writer in the document
WsMoveWriter                 // Move relative to the current position in the document
WsRemoveNode                 // Delete an element or text from a document
```

<span data-ttu-id="ed347-162">Al leer desde un [ \_ \_ búfer de WS XML](ws-xml-buffer.md) , se puede utilizar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ed347-162">When reading from a [WS\_XML\_BUFFER](ws-xml-buffer.md) the following may be used:</span></span>

``` syntax
WsGetReaderPosition          // Get the current position of the reader in the document
WsSetReaderPosition          // Set the current position of the reader in the document
WsMoveReader                 // Move relative to the current position in the document
```

<span data-ttu-id="ed347-163">Se puede utilizar lo siguiente para modificar un [ \_ \_ búfer de WS XML](ws-xml-buffer.md):</span><span class="sxs-lookup"><span data-stu-id="ed347-163">The following may be used to modify a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax

WsRemoveNode                 // Delete an element or text from a document
```

## <a name="other"></a><span data-ttu-id="ed347-164">Otros</span><span class="sxs-lookup"><span data-stu-id="ed347-164">Other</span></span>

``` syntax
WsGetNamespaceFromPrefix     // Find a namespace bound to a prefix
WsGetXmlAttribute            // Find an "xml:space" or "xml:lang" attribute in scope
```

 

 




