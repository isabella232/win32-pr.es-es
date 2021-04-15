---
description: En este tema se describen los detalles internos del modo en que la resolución de origen crea un origen de medios.
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: Controladores de esquema y controladores de Byte-Stream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54976f45c7f07e12b6f095297231d306d0644704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715498"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a><span data-ttu-id="d5143-103">Controladores de esquema y controladores de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="d5143-103">Scheme Handlers and Byte-Stream Handlers</span></span>

<span data-ttu-id="d5143-104">En este tema se describen los detalles internos del modo en que la resolución de origen crea un origen de medios.</span><span class="sxs-lookup"><span data-stu-id="d5143-104">This topic describes the internal details of how the source resolver creates a media source.</span></span> <span data-ttu-id="d5143-105">Lea este tema si va a implementar un origen multimedia personalizado para Media Foundation y desea que el origen de medios esté disponible para las aplicaciones a través de la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="d5143-105">Read this topic if you are implementing a custom media source for Media Foundation, and you want the media source to be available to applications via the source resolver.</span></span>

<span data-ttu-id="d5143-106">La resolución de origen puede crear un origen multimedia a partir de una dirección URL o de una secuencia de bytes (es decir, un puntero [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) ).</span><span class="sxs-lookup"><span data-stu-id="d5143-106">The source resolver can create a media source from a URL or from a byte stream (that is, an [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) pointer).</span></span> <span data-ttu-id="d5143-107">Para ello, usa objetos auxiliares denominados *Controladores*.</span><span class="sxs-lookup"><span data-stu-id="d5143-107">To do so, it uses helper objects called *handlers*.</span></span> <span data-ttu-id="d5143-108">En el caso de las direcciones URL, la resolución de origen usa *controladores de esquema*.</span><span class="sxs-lookup"><span data-stu-id="d5143-108">For URLs, the source resolver uses *scheme handlers*.</span></span> <span data-ttu-id="d5143-109">En el caso de secuencias de bytes, usa *controladores de secuencia de bytes*.</span><span class="sxs-lookup"><span data-stu-id="d5143-109">For byte streams, it uses *byte-stream handlers*.</span></span>

<span data-ttu-id="d5143-110">Un controlador de esquema toma una dirección URL como entrada y crea un origen multimedia o un flujo de bytes.</span><span class="sxs-lookup"><span data-stu-id="d5143-110">A scheme handler takes a URL as input and creates either a media source or a byte stream.</span></span> <span data-ttu-id="d5143-111">Si crea una secuencia de bytes, la resolución de origen la pasará a un controlador de flujo de bytes, que crea el origen de los medios.</span><span class="sxs-lookup"><span data-stu-id="d5143-111">If it creates a byte stream, the source resolver will pass that to a byte-stream handler, which creates the media source.</span></span> <span data-ttu-id="d5143-112">En la imagen siguiente se ilustra este proceso.</span><span class="sxs-lookup"><span data-stu-id="d5143-112">The following image illustrates this process.</span></span>

![diagrama que muestra el proceso de resolución de origen](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a><span data-ttu-id="d5143-114">Controladores de esquema</span><span class="sxs-lookup"><span data-stu-id="d5143-114">Scheme Handlers</span></span>

<span data-ttu-id="d5143-115">Los controladores de esquema se usan cuando la aplicación llama a [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) o su equivalente asincrónico, [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span><span class="sxs-lookup"><span data-stu-id="d5143-115">Scheme handlers are used when the application calls [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) or its asynchronous equivalent, [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span>

<span data-ttu-id="d5143-116">La resolución de origen busca controladores de esquema en el registro.</span><span class="sxs-lookup"><span data-stu-id="d5143-116">The source resolver looks up scheme handlers in the registry.</span></span> <span data-ttu-id="d5143-117">Los controladores de esquema se enumeran según el esquema de direcciones URL, con las claves siguientes:</span><span class="sxs-lookup"><span data-stu-id="d5143-117">Scheme handlers are listed by URL scheme, under the following keys:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

<span data-ttu-id="d5143-118">donde *<scheme>* es el esquema de la dirección URL que el controlador está diseñado para analizar.</span><span class="sxs-lookup"><span data-stu-id="d5143-118">where *<scheme>* is the URL scheme that the handler is designed to parse.</span></span> <span data-ttu-id="d5143-119">El esquema incluye el carácter ': ' final; por ejemplo, "http:".</span><span class="sxs-lookup"><span data-stu-id="d5143-119">The scheme includes the trailing ':' character; for example, "http:".</span></span>

<span data-ttu-id="d5143-120">Para registrar un nuevo controlador de esquema, agregue una entrada cuyo nombre sea el CLSID del controlador de esquema, en formato de cadena canónico: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` .</span><span class="sxs-lookup"><span data-stu-id="d5143-120">To register a new scheme handler, add an entry whose name is the CLSID of the scheme handler, in canonical string form: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}`.</span></span> <span data-ttu-id="d5143-121">El valor de la entrada es una cadena (REG \_ SZ) que contiene una breve descripción del controlador, como "mi esquema controlador".</span><span class="sxs-lookup"><span data-stu-id="d5143-121">The value of the entry is a string (REG\_SZ) containing a brief description of the handler, such as "My Scheme Handler."</span></span> <span data-ttu-id="d5143-122">La parte importante de la entrada es el CLSID.</span><span class="sxs-lookup"><span data-stu-id="d5143-122">The important part of the entry is the CLSID.</span></span> <span data-ttu-id="d5143-123">La resolución de origen crea el controlador mediante una llamada a **CoCreateInstance** con este CLSID.</span><span class="sxs-lookup"><span data-stu-id="d5143-123">The source resolver creates the handler by calling **CoCreateInstance** with this CLSID.</span></span>

<span data-ttu-id="d5143-124">Los controladores de esquema exponen la interfaz [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) .</span><span class="sxs-lookup"><span data-stu-id="d5143-124">Scheme handlers expose the [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) interface.</span></span> <span data-ttu-id="d5143-125">Si la resolución de origen encuentra un controlador de esquema que coincide con el esquema de la dirección URL, el solucionador de origen llama a [**IMFSchemeHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), pasando la dirección URL original.</span><span class="sxs-lookup"><span data-stu-id="d5143-125">If the source resolver finds a scheme handler that matches the URL scheme, the source resolver calls [**IMFSchemeHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), passing in the original URL.</span></span> <span data-ttu-id="d5143-126">El controlador de esquema abrirá la dirección URL e intentará analizar el contenido.</span><span class="sxs-lookup"><span data-stu-id="d5143-126">The scheme handler will open the URL and attempt to parse the contents.</span></span> <span data-ttu-id="d5143-127">En ese momento, el controlador de esquema tiene dos opciones:</span><span class="sxs-lookup"><span data-stu-id="d5143-127">At that point, the scheme handler has two options:</span></span>

-   <span data-ttu-id="d5143-128">Cree un origen de medios.</span><span class="sxs-lookup"><span data-stu-id="d5143-128">Create a media source.</span></span>
-   <span data-ttu-id="d5143-129">Cree una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="d5143-129">Create a byte stream.</span></span>

<span data-ttu-id="d5143-130">Si crea un origen de medios, la resolución de origen devuelve el origen de medios a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d5143-130">If it creates a media source, the source resolver returns the media source to the application.</span></span> <span data-ttu-id="d5143-131">Si crea una secuencia de bytes, el solucionador de origen intenta encontrar un controlador de secuencia de bytes adecuado, tal y como se describe en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="d5143-131">If it creates a byte stream, the source resolver attempts to find an appropriate byte-stream handler, as described in the next section.</span></span>

## <a name="byte-stream-handlers"></a><span data-ttu-id="d5143-132">Controladores de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="d5143-132">Byte-Stream Handlers</span></span>

<span data-ttu-id="d5143-133">Los controladores de secuencias de bytes se usan cuando la aplicación llama a [**IMFSourceResolver:: CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) o su equivalente asincrónico, [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream).</span><span class="sxs-lookup"><span data-stu-id="d5143-133">Byte-stream handlers are used when the application calls [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) or its asynchronous equivalent, [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream).</span></span> <span data-ttu-id="d5143-134">También se usan cuando un controlador de esquema devuelve una secuencia de bytes, como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d5143-134">They are also used when a scheme handler returns a byte stream, as described previously.</span></span>

<span data-ttu-id="d5143-135">Al igual que con los controladores de esquema, los controladores de secuencias de bytes se enumeran en el registro.</span><span class="sxs-lookup"><span data-stu-id="d5143-135">As with scheme handlers, byte-stream handlers are listed in the registry.</span></span> <span data-ttu-id="d5143-136">Se enumeran por extensión de nombre de archivo o tipo MIME (o ambos), en las claves siguientes:</span><span class="sxs-lookup"><span data-stu-id="d5143-136">They are listed either by file name extension or MIME type (or both), under the following keys:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

<span data-ttu-id="d5143-137">donde *<ExtensionOrMimeType>* es la extensión de nombre de archivo o el tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="d5143-137">where *<ExtensionOrMimeType>* is the file name extension or MIME type.</span></span> <span data-ttu-id="d5143-138">Las extensiones de archivo incluyen el carácter '. ' inicial; por ejemplo, ". WMV".</span><span class="sxs-lookup"><span data-stu-id="d5143-138">File extensions include the initial '.' character; for example, ".wmv".</span></span>

<span data-ttu-id="d5143-139">La extensión de nombre de archivo forma parte de la dirección URL, proporcionada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d5143-139">The file name extension is part of the URL, provided by the application.</span></span> <span data-ttu-id="d5143-140">El tipo MIME podría estar disponible a través del atributo de [**\_ tipo de \_ contenido \_ MF BYTESTREAM**](mf-bytestream-content-type-attribute.md) en la secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="d5143-140">The MIME type might be available through the [**MF\_BYTESTREAM\_CONTENT\_TYPE**](mf-bytestream-content-type-attribute.md) attribute on the byte stream.</span></span>

<span data-ttu-id="d5143-141">Para registrar un nuevo controlador de flujo de bytes, agregue una entrada cuyo nombre sea el CLSID del controlador, en formato de cadena canónico.</span><span class="sxs-lookup"><span data-stu-id="d5143-141">To register a new byte-stream handler, add an entry whose name is the CLSID of the handler, in canonical string form.</span></span> <span data-ttu-id="d5143-142">El valor de la entrada es una cadena (REG \_ SZ) que contiene una breve descripción del controlador, como "mi controlador de Byte-Stream".</span><span class="sxs-lookup"><span data-stu-id="d5143-142">The value of the entry is a string (REG\_SZ) containing a brief description of the handler, such as "My Byte-Stream Handler."</span></span> <span data-ttu-id="d5143-143">La resolución de origen llama a **CoCreateInstance** para crear el controlador a partir del CLSID.</span><span class="sxs-lookup"><span data-stu-id="d5143-143">The source resolver calls **CoCreateInstance** to create the handler from the CLSID.</span></span> <span data-ttu-id="d5143-144">Puede registrar el mismo controlador en más de una extensión o tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="d5143-144">You can register the same handler under more than one extension or MIME type.</span></span>

<span data-ttu-id="d5143-145">Los controladores de flujo de bytes exponen la interfaz [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .</span><span class="sxs-lookup"><span data-stu-id="d5143-145">Byte-stream handlers expose the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span> <span data-ttu-id="d5143-146">Si la resolución de origen encuentra un controlador de secuencia de bytes coincidente, llama a [**IMFByteStreamHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span><span class="sxs-lookup"><span data-stu-id="d5143-146">If the source resolver finds a matching byte-stream handler, it calls [**IMFByteStreamHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span></span> <span data-ttu-id="d5143-147">La entrada a este método es un puntero a la secuencia de bytes, más la dirección URL original, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="d5143-147">The input to this method is a pointer to the byte stream, plus the original URL, if available.</span></span> <span data-ttu-id="d5143-148">El controlador de flujo de bytes lee el flujo de bytes hasta que analiza los datos suficientes para crear el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="d5143-148">The byte-stream handler reads from the byte stream until it parses enough data to create the media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5143-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5143-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5143-150">Solucionador de origen</span><span class="sxs-lookup"><span data-stu-id="d5143-150">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



