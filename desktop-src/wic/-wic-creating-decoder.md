---
description: En este tema se presenta el descodificador de mapas de bits, un componente de códec básico de Windows Imaging Component (WIC) que se usa para descodificar archivos de imagen de una secuencia.
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: Información general sobre descodificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a15e6a9c914cfa220e1aad5bff4badeb8fc8cc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361573"
---
# <a name="decoding-overview"></a><span data-ttu-id="417a5-103">Información general sobre descodificación</span><span class="sxs-lookup"><span data-stu-id="417a5-103">Decoding Overview</span></span>

<span data-ttu-id="417a5-104">En este tema se presenta el descodificador de mapas de bits, un componente de códec básico de Windows Imaging Component (WIC) que se usa para descodificar archivos de imagen de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="417a5-104">The topic introduces the bitmap decoder, a core Windows Imaging Component (WIC) codec component used to decode image files from a stream.</span></span>

<span data-ttu-id="417a5-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="417a5-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="417a5-106">Introducción</span><span class="sxs-lookup"><span data-stu-id="417a5-106">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="417a5-107">Descodificadores de mapas de bits nativos</span><span class="sxs-lookup"><span data-stu-id="417a5-107">Native Bitmap Decoders</span></span>](#native-bitmap-decoders)
-   [<span data-ttu-id="417a5-108">Crear un descodificador de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="417a5-108">Creating a Bitmap Decoder</span></span>](#creating-a-bitmap-decoder)
-   [<span data-ttu-id="417a5-109">Extensibilidad del descodificador</span><span class="sxs-lookup"><span data-stu-id="417a5-109">Decoder Extensibility</span></span>](#decoder-extensibility)
-   [<span data-ttu-id="417a5-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="417a5-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="417a5-111">Introducción</span><span class="sxs-lookup"><span data-stu-id="417a5-111">Introduction</span></span>

<span data-ttu-id="417a5-112">Los descodificadores de mapas de bits se pueden ver como el contenedor exterior de una imagen digital y proporcionan acceso a las propiedades globales y a los fotogramas de imagen.</span><span class="sxs-lookup"><span data-stu-id="417a5-112">Bitmap decoders can be viewed as the outer container of a digital image and provides access to global properties and image frames.</span></span> <span data-ttu-id="417a5-113">Algunos formatos de imagen admiten miniaturas globales, vistas previas, contextos de color o metadatos, mientras que otros proporcionan estas propiedades solo en el nivel de marco.</span><span class="sxs-lookup"><span data-stu-id="417a5-113">Some image formats support global thumbnails, previews, color contexts, or metadata, while others provide these properties only at the frame level.</span></span> <span data-ttu-id="417a5-114">Sin embargo, tenga en cuenta que muchos de los formatos de imagen estándar no admiten estas propiedades globales.</span><span class="sxs-lookup"><span data-stu-id="417a5-114">Note, however, many of the standard image formats do not support these global properties.</span></span> <span data-ttu-id="417a5-115">Como tal, muchas de las implementaciones de códecs nativas proporcionadas por WIC no admiten la mayoría de estas propiedades globales.</span><span class="sxs-lookup"><span data-stu-id="417a5-115">As such, many of the native codec implementations provided by WIC do not support the majority of these global properties.</span></span> <span data-ttu-id="417a5-116">Vea la tabla de la sección descodificadores de mapas de bits nativos de este tema para obtener información sobre la compatibilidad de propiedades globales.</span><span class="sxs-lookup"><span data-stu-id="417a5-116">See the table in the Native Bitmap Decoders section of this topic for information about global property support.</span></span>

<span data-ttu-id="417a5-117">En WIC, los descodificadores de mapas de bits se representan mediante la interfaz [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) y proporcionan acceso a estas propiedades globales del mapa de bits y, lo que es más importante, los fotogramas que contiene.</span><span class="sxs-lookup"><span data-stu-id="417a5-117">In WIC, bitmap decoders are represented by the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface and provides access to these global properties of the bitmap and, more importantly, the frames it contains.</span></span> <span data-ttu-id="417a5-118">La interfaz [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) representa un marco de mapa de bits individual y se describe en detalle en la [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="417a5-118">The [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface represents an individual bitmap frame and is discussed in detail in the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="native-bitmap-decoders"></a><span data-ttu-id="417a5-119">Descodificadores de mapas de bits nativos</span><span class="sxs-lookup"><span data-stu-id="417a5-119">Native Bitmap Decoders</span></span>

<span data-ttu-id="417a5-120">WIC proporciona varias implementaciones nativas de la interfaz [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) para los formatos de imagen web estándar y el formato HD de alta calidad HD.</span><span class="sxs-lookup"><span data-stu-id="417a5-120">WIC provides several native implementations of the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface for the standard web image formats and the high dynamic range HD Photo format.</span></span> <span data-ttu-id="417a5-121">En la tabla siguiente se enumeran los descodificadores nativos disponibles, el nombre del identificador de clase y la compatibilidad con las propiedades globales.</span><span class="sxs-lookup"><span data-stu-id="417a5-121">The following table lists the available native decoders, class identifier name, and support for global properties.</span></span> <span data-ttu-id="417a5-122">Aunque es posible que una característica no admita una propiedad como miniaturas en el nivel global, el formato de la imagen puede admitir tales propiedades en el nivel de marco individual.</span><span class="sxs-lookup"><span data-stu-id="417a5-122">Though a feature may not support a property such as thumbnails at the global level, the image format may support such properties at the individual frame level.</span></span>



| <span data-ttu-id="417a5-123">Formato de imágenes</span><span class="sxs-lookup"><span data-stu-id="417a5-123">Image Format</span></span> | <span data-ttu-id="417a5-124">Nombre CLSID</span><span class="sxs-lookup"><span data-stu-id="417a5-124">CLSID Name</span></span>            | <span data-ttu-id="417a5-125">Miniaturas</span><span class="sxs-lookup"><span data-stu-id="417a5-125">Thumbnails</span></span> | <span data-ttu-id="417a5-126">Vistas previas</span><span class="sxs-lookup"><span data-stu-id="417a5-126">Previews</span></span> | <span data-ttu-id="417a5-127">Contextos de color</span><span class="sxs-lookup"><span data-stu-id="417a5-127">Color Contexts</span></span> | <span data-ttu-id="417a5-128">Metadatos</span><span class="sxs-lookup"><span data-stu-id="417a5-128">Metadata</span></span> |
|--------------|-----------------------|------------|----------|----------------|----------|
| <span data-ttu-id="417a5-129">BMP</span><span class="sxs-lookup"><span data-stu-id="417a5-129">BMP</span></span>          | <span data-ttu-id="417a5-130">CLSID \_ WICBmpDecoder</span><span class="sxs-lookup"><span data-stu-id="417a5-130">CLSID\_WICBmpDecoder</span></span>  | <span data-ttu-id="417a5-131">No</span><span class="sxs-lookup"><span data-stu-id="417a5-131">No</span></span>         | <span data-ttu-id="417a5-132">No</span><span class="sxs-lookup"><span data-stu-id="417a5-132">No</span></span>       | <span data-ttu-id="417a5-133">No</span><span class="sxs-lookup"><span data-stu-id="417a5-133">No</span></span>             | <span data-ttu-id="417a5-134">No</span><span class="sxs-lookup"><span data-stu-id="417a5-134">No</span></span>       |
| <span data-ttu-id="417a5-135">GIF</span><span class="sxs-lookup"><span data-stu-id="417a5-135">GIF</span></span>          | <span data-ttu-id="417a5-136">CLSID \_ WICGifDecoder</span><span class="sxs-lookup"><span data-stu-id="417a5-136">CLSID\_WICGifDecoder</span></span>  | <span data-ttu-id="417a5-137">No</span><span class="sxs-lookup"><span data-stu-id="417a5-137">No</span></span>         | <span data-ttu-id="417a5-138">No</span><span class="sxs-lookup"><span data-stu-id="417a5-138">No</span></span>       | <span data-ttu-id="417a5-139">No</span><span class="sxs-lookup"><span data-stu-id="417a5-139">No</span></span>             | <span data-ttu-id="417a5-140">Sí</span><span class="sxs-lookup"><span data-stu-id="417a5-140">Yes</span></span>      |
| <span data-ttu-id="417a5-141">ICO</span><span class="sxs-lookup"><span data-stu-id="417a5-141">ICO</span></span>          | <span data-ttu-id="417a5-142">CLSID \_ WICIcoDecoder</span><span class="sxs-lookup"><span data-stu-id="417a5-142">CLSID\_WICIcoDecoder</span></span>  | <span data-ttu-id="417a5-143">No</span><span class="sxs-lookup"><span data-stu-id="417a5-143">No</span></span>         | <span data-ttu-id="417a5-144">No</span><span class="sxs-lookup"><span data-stu-id="417a5-144">No</span></span>       | <span data-ttu-id="417a5-145">No</span><span class="sxs-lookup"><span data-stu-id="417a5-145">No</span></span>             | <span data-ttu-id="417a5-146">No</span><span class="sxs-lookup"><span data-stu-id="417a5-146">No</span></span>       |
| <span data-ttu-id="417a5-147">JPEG</span><span class="sxs-lookup"><span data-stu-id="417a5-147">JPEG</span></span>         | <span data-ttu-id="417a5-148">CLSID \_ WICJpegDecoder</span><span class="sxs-lookup"><span data-stu-id="417a5-148">CLSID\_WICJpegDecoder</span></span> | <span data-ttu-id="417a5-149">No</span><span class="sxs-lookup"><span data-stu-id="417a5-149">No</span></span>         | <span data-ttu-id="417a5-150">No</span><span class="sxs-lookup"><span data-stu-id="417a5-150">No</span></span>       | <span data-ttu-id="417a5-151">No</span><span class="sxs-lookup"><span data-stu-id="417a5-151">No</span></span>             | <span data-ttu-id="417a5-152">No</span><span class="sxs-lookup"><span data-stu-id="417a5-152">No</span></span>       |
| <span data-ttu-id="417a5-153">PNG</span><span class="sxs-lookup"><span data-stu-id="417a5-153">PNG</span></span>          | <span data-ttu-id="417a5-154">CLSID \_ WICPngDecoder</span><span class="sxs-lookup"><span data-stu-id="417a5-154">CLSID\_WICPngDecoder</span></span>  | <span data-ttu-id="417a5-155">No</span><span class="sxs-lookup"><span data-stu-id="417a5-155">No</span></span>         | <span data-ttu-id="417a5-156">No</span><span class="sxs-lookup"><span data-stu-id="417a5-156">No</span></span>       | <span data-ttu-id="417a5-157">No</span><span class="sxs-lookup"><span data-stu-id="417a5-157">No</span></span>             | <span data-ttu-id="417a5-158">No</span><span class="sxs-lookup"><span data-stu-id="417a5-158">No</span></span>       |
| <span data-ttu-id="417a5-159">TIFF</span><span class="sxs-lookup"><span data-stu-id="417a5-159">TIFF</span></span>         | <span data-ttu-id="417a5-160">CLSID \_ WICTiffDecoder</span><span class="sxs-lookup"><span data-stu-id="417a5-160">CLSID\_WICTiffDecoder</span></span> | <span data-ttu-id="417a5-161">No</span><span class="sxs-lookup"><span data-stu-id="417a5-161">No</span></span>         | <span data-ttu-id="417a5-162">No</span><span class="sxs-lookup"><span data-stu-id="417a5-162">No</span></span>       | <span data-ttu-id="417a5-163">No</span><span class="sxs-lookup"><span data-stu-id="417a5-163">No</span></span>             | <span data-ttu-id="417a5-164">No</span><span class="sxs-lookup"><span data-stu-id="417a5-164">No</span></span>       |
| <span data-ttu-id="417a5-165">Foto HD</span><span class="sxs-lookup"><span data-stu-id="417a5-165">HD Photo</span></span>     | <span data-ttu-id="417a5-166">CLSID \_ WICWmpDecoder</span><span class="sxs-lookup"><span data-stu-id="417a5-166">CLSID\_WICWmpDecoder</span></span>  | <span data-ttu-id="417a5-167">No</span><span class="sxs-lookup"><span data-stu-id="417a5-167">No</span></span>         | <span data-ttu-id="417a5-168">Sí</span><span class="sxs-lookup"><span data-stu-id="417a5-168">Yes</span></span>      | <span data-ttu-id="417a5-169">No</span><span class="sxs-lookup"><span data-stu-id="417a5-169">No</span></span>             | <span data-ttu-id="417a5-170">No</span><span class="sxs-lookup"><span data-stu-id="417a5-170">No</span></span>       |



 

## <a name="creating-a-bitmap-decoder"></a><span data-ttu-id="417a5-171">Crear un descodificador de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="417a5-171">Creating a Bitmap Decoder</span></span>

<span data-ttu-id="417a5-172">Para descodificar una imagen mediante WIC, primero debe crear una instancia de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) para el formato de imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="417a5-172">To decode an image using WIC, you first need to create an instance of the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) for the targeted image format.</span></span> <span data-ttu-id="417a5-173">La instancia del descodificador permite tener acceso a las propiedades globales y a los metadatos, si se admiten, así como a los fotogramas de imagen.</span><span class="sxs-lookup"><span data-stu-id="417a5-173">The decoder instance enables you to access the global properties and metadata, if supported, as well as the image frames.</span></span> <span data-ttu-id="417a5-174">El generador de imágenes WIC, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), proporciona varios métodos para crear descodificadores de mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="417a5-174">The WIC imaging factory, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), provides several methods for creating bitmap decoders.</span></span> <span data-ttu-id="417a5-175">Se proporcionan los siguientes métodos de generador para crear descodificadores de mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="417a5-175">The following factory methods are provided to create bitmap decoders.</span></span>

-   [<span data-ttu-id="417a5-176">**CreateDecoder**</span><span class="sxs-lookup"><span data-stu-id="417a5-176">**CreateDecoder**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [<span data-ttu-id="417a5-177">**CreateDecoderFromFileHandle**</span><span class="sxs-lookup"><span data-stu-id="417a5-177">**CreateDecoderFromFileHandle**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [<span data-ttu-id="417a5-178">**CreateDecoderFromFilename**</span><span class="sxs-lookup"><span data-stu-id="417a5-178">**CreateDecoderFromFilename**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [<span data-ttu-id="417a5-179">**CreateDecoderFromStream**</span><span class="sxs-lookup"><span data-stu-id="417a5-179">**CreateDecoderFromStream**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

<span data-ttu-id="417a5-180">En el código siguiente se muestra cómo crear un descodificador de mapa de bits con un nombre de archivo de imagen y recuperar el primer fotograma de la imagen.</span><span class="sxs-lookup"><span data-stu-id="417a5-180">The following code demonstrates the how to create a bitmap decoder using an image filename and retrieve the first frame of the image.</span></span>


```C++
   // Create a decoder
   IWICBitmapDecoder *pDecoder = NULL;

   hr = m_pIWICFactory->CreateDecoderFromFilename(
       szFileName,                      // Image to be decoded
       NULL,                            // Do not prefer a particular vendor
       GENERIC_READ,                    // Desired read access to the file
       WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
       &pDecoder                        // Pointer to the decoder
       );

   // Retrieve the first frame of the image from the decoder
   IWICBitmapFrameDecode *pFrame = NULL;

   if (SUCCEEDED(hr))
   {
       hr = pDecoder->GetFrame(0, &pFrame);
   }
```



## <a name="decoder-extensibility"></a><span data-ttu-id="417a5-181">Extensibilidad del descodificador</span><span class="sxs-lookup"><span data-stu-id="417a5-181">Decoder Extensibility</span></span>

<span data-ttu-id="417a5-182">Una de las características principales de WIC es un marco de extensibilidad que permite a los desarrolladores de códec desarrollar sus propios códecs de imagen y obtener la misma compatibilidad con la plataforma que las implementaciones nativas de códecs de imagen.</span><span class="sxs-lookup"><span data-stu-id="417a5-182">One of the core features of WIC is an extensibility framework that enables codec developers to develop their own image codecs and get the same platform support as the native implementations of image codecs.</span></span> <span data-ttu-id="417a5-183">Se usa un único conjunto coherente de interfaces para todo el procesamiento de imágenes, independientemente del formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="417a5-183">A single, consistent set of interfaces is used for all image processing, regardless of image format.</span></span> <span data-ttu-id="417a5-184">Cualquier aplicación que use WIC obtiene la compatibilidad automática con los nuevos formatos de imagen en cuanto se instala el códec.</span><span class="sxs-lookup"><span data-stu-id="417a5-184">Any application using WIC gets automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="417a5-185">Para obtener más información sobre el desarrollo de códecs, vea los temas del [desarrollo de componentes](-wic-component-development.md).</span><span class="sxs-lookup"><span data-stu-id="417a5-185">For more information on codec development, see the topics in [Component Development](-wic-component-development.md).</span></span> <span data-ttu-id="417a5-186">Para obtener más información sobre el desarrollo del descodificador, vea [implementar un descodificador de WIC-Enabled](-wic-implementingwicdecoder.md).</span><span class="sxs-lookup"><span data-stu-id="417a5-186">For more information on decoder development, see [Implementing a WIC-Enabled Decoder](-wic-implementingwicdecoder.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="417a5-187">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="417a5-187">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="417a5-188">**Vista**</span><span class="sxs-lookup"><span data-stu-id="417a5-188">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="417a5-189">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="417a5-189">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="417a5-190">Información general sobre la codificación</span><span class="sxs-lookup"><span data-stu-id="417a5-190">Encoding Overview</span></span>](-wic-creating-encoder.md)
</dt> <dt>

[<span data-ttu-id="417a5-191">Desarrollo de componentes</span><span class="sxs-lookup"><span data-stu-id="417a5-191">Component Development</span></span>](-wic-component-development.md)
</dt> </dl>

 

 



