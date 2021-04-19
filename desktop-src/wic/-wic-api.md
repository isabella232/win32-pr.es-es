---
description: El componente de creación de imágenes de Windows (WIC) proporciona una API basada en el modelo de objetos componentes (COM) para su uso en C y C++.
ms.assetid: 74b14b5e-70e9-410f-a6e6-d8873a5f4fa4
title: Información general sobre la API WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86e5a876010e52489adac9baa7ce57fdfdf80f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720566"
---
# <a name="wic-api-overview"></a><span data-ttu-id="f9d87-103">Información general sobre la API WIC</span><span class="sxs-lookup"><span data-stu-id="f9d87-103">WIC API Overview</span></span>

<span data-ttu-id="f9d87-104">El componente de creación de imágenes de Windows (WIC) proporciona una API basada en el modelo de objetos componentes (COM) para su uso en C y C++.</span><span class="sxs-lookup"><span data-stu-id="f9d87-104">The Windows Imaging Component (WIC) provides a Component Object Model (COM) based API for use in C and C++.</span></span> <span data-ttu-id="f9d87-105">La API de WIC expone una variedad de funcionalidades relacionadas con la imagen, entre las que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="f9d87-105">The WIC API exposes a variety of image-related functionality, including:</span></span>

-   <span data-ttu-id="f9d87-106">Códecs integrados para los formatos de imagen web estándar.</span><span class="sxs-lookup"><span data-stu-id="f9d87-106">Built-in codecs for the standard web image formats.</span></span>
-   <span data-ttu-id="f9d87-107">Compatibilidad integrada con formatos de metadatos estándar.</span><span class="sxs-lookup"><span data-stu-id="f9d87-107">Built-in support for standard metadata formats.</span></span>
-   <span data-ttu-id="f9d87-108">Gran variedad de compatibilidad con el formato de píxeles.</span><span class="sxs-lookup"><span data-stu-id="f9d87-108">Wide range of pixel format support.</span></span>
-   <span data-ttu-id="f9d87-109">Compatibilidad de alto color; incluye formatos de intervalo extendido de 30 bits, alta precisión de 30 bits y alta precisión de 48 bits y de gama ancha.</span><span class="sxs-lookup"><span data-stu-id="f9d87-109">High-color support; including 30-bit extended range, 30-bit high precision, and 48-bit high precision and wide gamut pixel formats.</span></span>
-   <span data-ttu-id="f9d87-110">Marco extensible para códecs de imagen, formatos de píxeles y formatos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="f9d87-110">Extensible framework for image codecs, pixel formats, and metadata formats.</span></span>

<span data-ttu-id="f9d87-111">Este tema contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="f9d87-111">This topic contains the following topics.</span></span>

-   [<span data-ttu-id="f9d87-112">Archivos de encabezado WIC</span><span class="sxs-lookup"><span data-stu-id="f9d87-112">WIC Header Files</span></span>](#wic-header-files)
-   [<span data-ttu-id="f9d87-113">Archivos de biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9d87-113">Library Files</span></span>](#library-files)
-   [<span data-ttu-id="f9d87-114">Generadores de clases</span><span class="sxs-lookup"><span data-stu-id="f9d87-114">Class Factories</span></span>](#class-factories)
-   [<span data-ttu-id="f9d87-115">Componentes de creación de imágenes</span><span class="sxs-lookup"><span data-stu-id="f9d87-115">Imaging Components</span></span>](#imaging-components)
-   [<span data-ttu-id="f9d87-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9d87-116">See Also</span></span>](#see-also)

## <a name="wic-header-files"></a><span data-ttu-id="f9d87-117">Archivos de encabezado WIC</span><span class="sxs-lookup"><span data-stu-id="f9d87-117">WIC Header Files</span></span>

<span data-ttu-id="f9d87-118">Las API de WIC se definen en los siguientes archivos de encabezado y de lenguaje de definición de interfaz (IDL):</span><span class="sxs-lookup"><span data-stu-id="f9d87-118">The WIC APIs are defined in the following header and Interface Definition Language (IDL) files:</span></span>



| <span data-ttu-id="f9d87-119">Archivo</span><span class="sxs-lookup"><span data-stu-id="f9d87-119">File</span></span>              | <span data-ttu-id="f9d87-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9d87-120">Description</span></span>                                          |
|-------------------|------------------------------------------------------|
| <span data-ttu-id="f9d87-121">wincodec. h</span><span class="sxs-lookup"><span data-stu-id="f9d87-121">wincodec.h</span></span>        | <span data-ttu-id="f9d87-122">Define las versiones de C y C++ de las API de WIC principales.</span><span class="sxs-lookup"><span data-stu-id="f9d87-122">Defines C and C++ versions of the primary WIC APIs.</span></span>  |
| <span data-ttu-id="f9d87-123">wincodec. idl</span><span class="sxs-lookup"><span data-stu-id="f9d87-123">wincodec.idl</span></span>      | <span data-ttu-id="f9d87-124">Define las interfaces de WIC principales.</span><span class="sxs-lookup"><span data-stu-id="f9d87-124">Defines the primary WIC interfaces.</span></span>                  |
| <span data-ttu-id="f9d87-125">wincodecsdk. h</span><span class="sxs-lookup"><span data-stu-id="f9d87-125">wincodecsdk.h</span></span>     | <span data-ttu-id="f9d87-126">Define las versiones de C y C++ de las API de WIC de metadatos.</span><span class="sxs-lookup"><span data-stu-id="f9d87-126">Defines C and C++ versions of the metadata WIC APIs.</span></span> |
| <span data-ttu-id="f9d87-127">wincodecsdk. idl</span><span class="sxs-lookup"><span data-stu-id="f9d87-127">wincodecsdk.idl</span></span>   | <span data-ttu-id="f9d87-128">Define las interfaces de metadatos de WIC.</span><span class="sxs-lookup"><span data-stu-id="f9d87-128">Defines the WIC metadata interfaces.</span></span>                 |
| <span data-ttu-id="f9d87-129">wincodec \_ proxy. h</span><span class="sxs-lookup"><span data-stu-id="f9d87-129">wincodec\_proxy.h</span></span> | <span data-ttu-id="f9d87-130">Define las exportaciones del proxy WIC.</span><span class="sxs-lookup"><span data-stu-id="f9d87-130">Defines the WIC proxy exports.</span></span>                       |



 

<span data-ttu-id="f9d87-131">Para usar WIC, las aplicaciones deben incluir wincodec. h y/o wincodecsdk. h, en función de la API que necesite la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f9d87-131">To use WIC, your applications must include wincodec.h and/or wincodecsdk.h, depending on the API your application needs.</span></span>

## <a name="library-files"></a><span data-ttu-id="f9d87-132">Archivos de biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9d87-132">Library Files</span></span>

<span data-ttu-id="f9d87-133">Archivos de la biblioteca WIC:</span><span class="sxs-lookup"><span data-stu-id="f9d87-133">The WIC library files:</span></span>



| <span data-ttu-id="f9d87-134">Archivo</span><span class="sxs-lookup"><span data-stu-id="f9d87-134">File</span></span>              | <span data-ttu-id="f9d87-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9d87-135">Description</span></span>                                                            |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="f9d87-136">WindowsCodecs. lib</span><span class="sxs-lookup"><span data-stu-id="f9d87-136">windowscodecs.lib</span></span> | <span data-ttu-id="f9d87-137">Biblioteca de importación proporcionada por el kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="f9d87-137">Import library provided by the Windows Software Development Kit (SDK).</span></span> |
| <span data-ttu-id="f9d87-138">windowscodecs.dll</span><span class="sxs-lookup"><span data-stu-id="f9d87-138">windowscodecs.dll</span></span> | <span data-ttu-id="f9d87-139">Biblioteca de implementación de acciones proporcionada por el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f9d87-139">Stock implementation library provided by the operating system.</span></span>         |



 

<span data-ttu-id="f9d87-140">Para vincular a las API de WIC, la aplicación debe incluir windowscodec. lib como una dependencia del enlazador adicional.</span><span class="sxs-lookup"><span data-stu-id="f9d87-140">To link to WIC APIs, your application must include windowscodec.lib as an additional linker dependency.</span></span>

## <a name="class-factories"></a><span data-ttu-id="f9d87-141">Generadores de clases</span><span class="sxs-lookup"><span data-stu-id="f9d87-141">Class Factories</span></span>

<span data-ttu-id="f9d87-142">En la tabla siguiente se describen los dos generadores de clases COM que las API de WIC proporcionan para crear componentes de WIC.</span><span class="sxs-lookup"><span data-stu-id="f9d87-142">The following table describes the two COM class factories the WIC APIs provide for creating WIC components.</span></span>



| <span data-ttu-id="f9d87-143">Interfaz de fábrica</span><span class="sxs-lookup"><span data-stu-id="f9d87-143">Factory Interface</span></span>                                               | <span data-ttu-id="f9d87-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9d87-144">Description</span></span>                                                                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9d87-145">**IWICImagingFactory**</span><span class="sxs-lookup"><span data-stu-id="f9d87-145">**IWICImagingFactory**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)     | <span data-ttu-id="f9d87-146">Generador de clases principal para el desarrollo de aplicaciones mediante componentes de WIC.</span><span class="sxs-lookup"><span data-stu-id="f9d87-146">Primary class factory for application development using WIC components.</span></span> <span data-ttu-id="f9d87-147">Este generador crea componentes como descodificadores de imágenes, codificadores y secuencias.</span><span class="sxs-lookup"><span data-stu-id="f9d87-147">This factory creates components such as image decoders, encoders and streams.</span></span>   |
| [<span data-ttu-id="f9d87-148">**IWICComponentFactory**</span><span class="sxs-lookup"><span data-stu-id="f9d87-148">**IWICComponentFactory**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) | <span data-ttu-id="f9d87-149">Generador de clases destinado a desarrolladores de componentes de WIC.</span><span class="sxs-lookup"><span data-stu-id="f9d87-149">Class factory targeted for WIC component developers.</span></span> <span data-ttu-id="f9d87-150">Los componentes creados a partir de este generador se utilizan principalmente en el desarrollo de códecs y controladores de metadatos.</span><span class="sxs-lookup"><span data-stu-id="f9d87-150">Components created from this factory are primarily used in codec and metadata handler development.</span></span> |



 

<span data-ttu-id="f9d87-151">Para crear un generador de clases, utilice la función com [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="f9d87-151">To create either class factory, use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM function.</span></span> <span data-ttu-id="f9d87-152">En el ejemplo siguiente se muestra la creación de la factoría de imágenes WIC.</span><span class="sxs-lookup"><span data-stu-id="f9d87-152">The following example demonstrates the creation of the WIC imaging factory.</span></span>


```C++
// Initialize COM
CoInitialize(NULL);

// The factory pointer
IWICImagingFactory *pFactory = NULL;

// Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&pFactory)
);
```



## <a name="imaging-components"></a><span data-ttu-id="f9d87-153">Componentes de creación de imágenes</span><span class="sxs-lookup"><span data-stu-id="f9d87-153">Imaging Components</span></span>

<span data-ttu-id="f9d87-154">Las API de WIC proporcionan varios tipos de componentes de creación de imágenes.</span><span class="sxs-lookup"><span data-stu-id="f9d87-154">The WIC APIs provide several types of imaging components.</span></span> <span data-ttu-id="f9d87-155">En la tabla siguiente se describen algunos de los componentes de WIC comunes.</span><span class="sxs-lookup"><span data-stu-id="f9d87-155">The following table describes some of the common WIC components.</span></span> <span data-ttu-id="f9d87-156">Para obtener una lista completa de los componentes disponibles, consulte [interfaces de WIC](-wic-codec-ifaces.md).</span><span class="sxs-lookup"><span data-stu-id="f9d87-156">For a full list of available components, see [WIC interfaces](-wic-codec-ifaces.md).</span></span>



| <span data-ttu-id="f9d87-157">Tipo de componente</span><span class="sxs-lookup"><span data-stu-id="f9d87-157">Component Type</span></span>                                                      | <span data-ttu-id="f9d87-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9d87-158">Description</span></span>                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9d87-159">**Bitmap**</span><span class="sxs-lookup"><span data-stu-id="f9d87-159">**Bitmap**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                             | <span data-ttu-id="f9d87-160">Representa una representación en memoria grabable de un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource).</span><span class="sxs-lookup"><span data-stu-id="f9d87-160">Represents a writable in-memory representation of an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource).</span></span> |
| [<span data-ttu-id="f9d87-161">**Descodificador**</span><span class="sxs-lookup"><span data-stu-id="f9d87-161">**Decoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)                     | <span data-ttu-id="f9d87-162">Se usa para descodificar los datos de imagen de una secuencia en un formato útil para el procesamiento de imágenes.</span><span class="sxs-lookup"><span data-stu-id="f9d87-162">Used to decode image data from a stream into a format that is useful for image processing.</span></span>                    |
| [<span data-ttu-id="f9d87-163">**Codificador**</span><span class="sxs-lookup"><span data-stu-id="f9d87-163">**Encoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)                     | <span data-ttu-id="f9d87-164">Escribe datos de imagen en una secuencia.</span><span class="sxs-lookup"><span data-stu-id="f9d87-164">Writes image data to a stream.</span></span>                                                                                |
| [<span data-ttu-id="f9d87-165">**Stream**</span><span class="sxs-lookup"><span data-stu-id="f9d87-165">**Stream**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)                             | <span data-ttu-id="f9d87-166">Se usa para leer y escribir datos de un archivo, un recurso de red, un bloque de memoria, etc.</span><span class="sxs-lookup"><span data-stu-id="f9d87-166">Used to read and write data from a file, network resource, a block of memory, and so on.</span></span>                      |
| [<span data-ttu-id="f9d87-167">**Convertidor de formato**</span><span class="sxs-lookup"><span data-stu-id="f9d87-167">**Format Converter**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)          | <span data-ttu-id="f9d87-168">Se utiliza para convertir de un formato de píxel a otro.</span><span class="sxs-lookup"><span data-stu-id="f9d87-168">Used to convert from one pixel format to another.</span></span>                                                             |
| [<span data-ttu-id="f9d87-169">**Lector de consultas de metadatos**</span><span class="sxs-lookup"><span data-stu-id="f9d87-169">**Metadata Query Reader**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) | <span data-ttu-id="f9d87-170">Se usa para leer los metadatos de un marco de imagen o imagen.</span><span class="sxs-lookup"><span data-stu-id="f9d87-170">Used to read metadata of an image or image frame.</span></span>                                                             |
| [<span data-ttu-id="f9d87-171">**Escritor de consultas de metadatos**</span><span class="sxs-lookup"><span data-stu-id="f9d87-171">**Metadata Query Writer**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) | <span data-ttu-id="f9d87-172">Se usa para escribir metadatos en un marco de imagen o imagen.</span><span class="sxs-lookup"><span data-stu-id="f9d87-172">Used to write metadata to an image or image frame.</span></span>                                                            |



 

## <a name="see-also"></a><span data-ttu-id="f9d87-173">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f9d87-173">See Also</span></span>

[<span data-ttu-id="f9d87-174">Referencias</span><span class="sxs-lookup"><span data-stu-id="f9d87-174">References</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="f9d87-175">Ejemplos y ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="f9d87-175">Samples and Code Examples</span></span>](-wic-samples.md)


 

 
