---
description: En este tema se presenta la compatibilidad con metadatos de imágenes que proporciona el componente de creación de imágenes de Windows (WIC).
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: Información general sobre metadatos de WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f00e3a77eb74a3fb4a00db05ef9e00028f02ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570512"
---
# <a name="wic-metadata-overview"></a><span data-ttu-id="03bae-103">Información general sobre metadatos de WIC</span><span class="sxs-lookup"><span data-stu-id="03bae-103">WIC Metadata Overview</span></span>

<span data-ttu-id="03bae-104">En este tema se presenta la compatibilidad con metadatos de imágenes que proporciona el componente de creación de imágenes de Windows (WIC).</span><span class="sxs-lookup"><span data-stu-id="03bae-104">This topic introduces the imaging metadata support provided by the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="03bae-105">Proporciona una introducción a la lectura y la escritura de metadatos de imagen, el lenguaje de consulta de metadatos y la extensibilidad del controlador de metadatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-105">It provides an introduction to reading and writing image metadata, the metadata query language, and metadata handler extensibility.</span></span>

<span data-ttu-id="03bae-106">Los metadatos de la imagen son datos incrustados dentro de un archivo de imagen que proporciona información adicional sobre la imagen, como el dispositivo que se usa para capturar la imagen o las dimensiones de la imagen.</span><span class="sxs-lookup"><span data-stu-id="03bae-106">Image metadata is data embedded inside an image file that provides additional information about the image, such as the device used to capture the image or the dimensions of the image.</span></span> <span data-ttu-id="03bae-107">Aunque se encuentra dentro del propio archivo de imagen, estos metadatos no forman parte de los datos de representación.</span><span class="sxs-lookup"><span data-stu-id="03bae-107">Although it is contained within the image file itself, this metadata is not part of the rendering data.</span></span> <span data-ttu-id="03bae-108">WIC proporciona interfaces que permiten leer y escribir estos metadatos para varios formatos de metadatos comunes, entre los que se incluyen la plataforma de metadatos extensible (XMP), el archivo de imagen intercambiable (EXIF) y los datos de texto PNG (texto).</span><span class="sxs-lookup"><span data-stu-id="03bae-108">WIC provides interfaces that enable you to read and write this metadata for several common metadata formats including Extensible Metadata Platform (XMP), Exchangeable Image File (EXIF), and Png Textual Data (tEXt).</span></span>

<span data-ttu-id="03bae-109">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="03bae-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="03bae-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="03bae-110">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="03bae-111">Introducción</span><span class="sxs-lookup"><span data-stu-id="03bae-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="03bae-112">Leer metadatos de imagen</span><span class="sxs-lookup"><span data-stu-id="03bae-112">Reading Image Metadata</span></span>](#reading-image-metadata)
-   [<span data-ttu-id="03bae-113">Escribir metadatos de imagen</span><span class="sxs-lookup"><span data-stu-id="03bae-113">Writing Image Metadata</span></span>](#writing-image-metadata)
-   [<span data-ttu-id="03bae-114">Extensibilidad de metadatos</span><span class="sxs-lookup"><span data-stu-id="03bae-114">Metadata Extensibility</span></span>](#metadata-extensibility)
-   [<span data-ttu-id="03bae-115">Formatos de metadatos admitidos</span><span class="sxs-lookup"><span data-stu-id="03bae-115">Supported Metadata Formats</span></span>](#supported-metadata-formats)
-   [<span data-ttu-id="03bae-116">Resumen de los componentes de metadatos</span><span class="sxs-lookup"><span data-stu-id="03bae-116">Metadata Component Summary</span></span>](#metadata-component-summary)
-   [<span data-ttu-id="03bae-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="03bae-117">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="03bae-118">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="03bae-118">Prerequisites</span></span>

<span data-ttu-id="03bae-119">Para entender este tema, debe estar familiarizado con las interfaces del codificador y el descodificador de WIC y con sus componentes de modelo de objetos componentes (COM) relacionados, tal como se describe en [información general sobre el componente de creación de imágenes de Windows](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="03bae-119">To understand this topic, you should be familiar with the WIC encoder and decoder interfaces and their related Component Object Model (COM) components, as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> <span data-ttu-id="03bae-120">También ayuda a tener una familiaridad general con algunos de los formatos de metadatos de imágenes que se usan hoy en día.</span><span class="sxs-lookup"><span data-stu-id="03bae-120">It also helps to have a general familiarity with some of the imaging metadata formats in use today.</span></span>

## <a name="introduction"></a><span data-ttu-id="03bae-121">Introducción</span><span class="sxs-lookup"><span data-stu-id="03bae-121">Introduction</span></span>

<span data-ttu-id="03bae-122">Los metadatos proporcionan información extendida sobre una imagen.</span><span class="sxs-lookup"><span data-stu-id="03bae-122">Metadata provides extended information about an image.</span></span> <span data-ttu-id="03bae-123">Esta información se puede usar de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="03bae-123">This information can be used in several ways.</span></span> <span data-ttu-id="03bae-124">Una imagen puede contener metadatos como una descripción, clasificación, etiquetas de categoría e información de copyright.</span><span class="sxs-lookup"><span data-stu-id="03bae-124">An image might contain metadata such as a description, rating, category tags, and copyright information.</span></span> <span data-ttu-id="03bae-125">El acceso a los metadatos facilita la realización de tareas como la administración de recursos, la ubicación de los archivos o la determinación de la información de copyright.</span><span class="sxs-lookup"><span data-stu-id="03bae-125">Accessing the metadata makes it easier to perform tasks such as asset management, file location, or determining copyright information.</span></span> <span data-ttu-id="03bae-126">Por ejemplo, la Galería fotográfica de Windows de Windows Vista permite agregar descripciones y etiquetas de categoría a las imágenes.</span><span class="sxs-lookup"><span data-stu-id="03bae-126">For example, the Windows Photo Gallery in Windows Vista enables you to add descriptions and category tags to images.</span></span> <span data-ttu-id="03bae-127">Esto permite una mejor detectabilidad de las imágenes y una manera cómoda de clasificar las imágenes.</span><span class="sxs-lookup"><span data-stu-id="03bae-127">This allows for better discoverability of images and a convenient way to categorize images.</span></span> <span data-ttu-id="03bae-128">Con las API de WIC y los formatos de metadatos comunes, las aplicaciones pueden escribir o leer fácilmente este tipo de metadatos en imágenes o desde ellas.</span><span class="sxs-lookup"><span data-stu-id="03bae-128">Using the WIC APIs and common metadata formats, applications can easily write or read this type of metadata to or from images.</span></span>

<span data-ttu-id="03bae-129">En el diagrama siguiente se muestra el contenido de un archivo JPEG que incluye bloques de metadatos incrustados y elementos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-129">The following diagram illustrates the contents of a JPEG file that includes embedded metadata blocks and metadata items.</span></span>

![imagen JPEG con metadatos de clasificación](graphics/jpeg.png)

<span data-ttu-id="03bae-131">En esta imagen de ejemplo, los metadatos se insertan en el archivo de imagen dentro de un marco de imagen.</span><span class="sxs-lookup"><span data-stu-id="03bae-131">In this example image, the metadata is embedded in the image file within an image frame.</span></span> <span data-ttu-id="03bae-132">El formato JPEG no admite varios fotogramas de imagen, por lo que los metadatos se adjuntan conceptualmente a este único fotograma.</span><span class="sxs-lookup"><span data-stu-id="03bae-132">The JPEG format does not support multiple image frames, so the metadata is conceptually attached to this single frame.</span></span> <span data-ttu-id="03bae-133">Los formatos que admiten varios marcos, como TIFF, pueden tener metadatos adjuntos a cada fotograma de imagen como se muestra en este diagrama.</span><span class="sxs-lookup"><span data-stu-id="03bae-133">Formats that support multiple frames, such as TIFF, may have metadata attached to each image frame as this diagram shows.</span></span> <span data-ttu-id="03bae-134">Aunque no es habitual hoy y no es compatible con los códecs de imagen nativa, algunos formatos de imagen también pueden admitir metadatos fuera de un marco de imagen.</span><span class="sxs-lookup"><span data-stu-id="03bae-134">Though not common today and not supported by the native image codecs, some image formats may also support metadata outside of an image frame.</span></span> <span data-ttu-id="03bae-135">WIC es lo suficientemente flexible como para controlar metadatos y metadatos de nivel de marco fuera del marco individual de una imagen.</span><span class="sxs-lookup"><span data-stu-id="03bae-135">WIC is flexible enough to handle both frame-level metadata and metadata outside of an image's individual frame.</span></span>

## <a name="reading-image-metadata"></a><span data-ttu-id="03bae-136">Leer metadatos de imagen</span><span class="sxs-lookup"><span data-stu-id="03bae-136">Reading Image Metadata</span></span>

<span data-ttu-id="03bae-137">Las API de WIC proporcionan componentes COM que facilitan a las aplicaciones la lectura y escritura de metadatos de imágenes.</span><span class="sxs-lookup"><span data-stu-id="03bae-137">The WIC APIs provide COM components that make it easy for applications to read and write image metadata.</span></span>

<span data-ttu-id="03bae-138">La forma principal de leer los metadatos es usar un lector de consultas de metadatos ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) para tener acceso a los elementos de metadatos específicos.</span><span class="sxs-lookup"><span data-stu-id="03bae-138">The primary way to read metadata is to use a metadata query reader ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) to access specific metadata items.</span></span> <span data-ttu-id="03bae-139">El códec implementa el componente lector de consultas de metadatos y se puede tener acceso a él en el nivel de descodificador o a través de fotogramas de imagen individuales, que es el método más común.</span><span class="sxs-lookup"><span data-stu-id="03bae-139">The metadata query reader component is implemented by the codec and can be accessed at the decoder level or through individual image frames, which is the more common method.</span></span> <span data-ttu-id="03bae-140">En el código siguiente se muestra cómo obtener acceso a un lector de consultas para un marco individual mediante el método **GetMetadataQueryReader** del lector de consultas.</span><span class="sxs-lookup"><span data-stu-id="03bae-140">The following code demonstrates how to access a query reader for an individual frame by using the query reader's **GetMetadataQueryReader** method.</span></span>


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



<span data-ttu-id="03bae-141">Un lector de consultas proporciona métodos para obtener información sobre metadatos específicos y un medio para especificar un elemento de metadatos que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="03bae-141">A query reader provides methods to obtain information about specific metadata, and a means to specify a metadata item to retrieve.</span></span> <span data-ttu-id="03bae-142">En el código siguiente se usa una expresión de consulta para solicitar un elemento de metadatos específico dentro del bloque de directorio de archivos de imagen anidada (IFD) de app1.</span><span class="sxs-lookup"><span data-stu-id="03bae-142">The following code uses a query expression to request a specific metadata item within the App1 nested image file directory (IFD) block.</span></span> <span data-ttu-id="03bae-143">Esto se hace mediante el método **GetMetadataByName** del lector de consultas.</span><span class="sxs-lookup"><span data-stu-id="03bae-143">This is done by using the query reader's **GetMetadataByName** method.</span></span> <span data-ttu-id="03bae-144">En el código siguiente se muestra cómo utilizar el lector de consultas para obtener el valor de clasificación MicrosoftPhoto.</span><span class="sxs-lookup"><span data-stu-id="03bae-144">The following code demonstrates using the query reader to obtain the MicrosoftPhoto rating value.</span></span>


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



<span data-ttu-id="03bae-145">La variable pwzRatingQuery del ejemplo anterior es la cadena de consulta para tener acceso al elemento de metadatos MicrosoftPhoto rating.</span><span class="sxs-lookup"><span data-stu-id="03bae-145">The pwzRatingQuery variable in the preceding example is the query string to access the metadata item MicrosoftPhoto rating.</span></span> <span data-ttu-id="03bae-146">Esta cadena se crea mediante el lenguaje de consulta de metadatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-146">This string is created by using the metadata query language.</span></span> <span data-ttu-id="03bae-147">Para crear esta cadena, es necesario conocer el formato de metadatos y el lenguaje de consulta de metadatos para recuperar los elementos de metadatos individuales.</span><span class="sxs-lookup"><span data-stu-id="03bae-147">To create this string, knowledge of the metadata format and the metadata query language is needed to retrieve individual metadata items.</span></span> <span data-ttu-id="03bae-148">Para obtener más información sobre el lenguaje de consulta de metadatos, vea [información general sobre el lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="03bae-148">For more information about the metadata query language, see the [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

<span data-ttu-id="03bae-149">En segundo plano, un lector de consultas usa un lector de metadatos ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) para tener acceso a los metadatos descritos por la expresión de consulta.</span><span class="sxs-lookup"><span data-stu-id="03bae-149">Behind the scenes, a query reader uses a metadata reader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) to access the metadata described by the query expression.</span></span> <span data-ttu-id="03bae-150">Además de usar un lector de consultas, también puede tener acceso a un lector de metadatos directamente para leer los metadatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-150">In addition to using a query reader, you can also access a metadata reader directly to read metadata.</span></span> <span data-ttu-id="03bae-151">Puede obtener un lector de metadatos del descodificador o de los marcos individuales consultando una interfaz de lectura de bloques ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)).</span><span class="sxs-lookup"><span data-stu-id="03bae-151">You can obtain a metadata reader from the decoder or individual frames by querying for a block reader ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) interface.</span></span>

## <a name="writing-image-metadata"></a><span data-ttu-id="03bae-152">Escribir metadatos de imagen</span><span class="sxs-lookup"><span data-stu-id="03bae-152">Writing Image Metadata</span></span>

<span data-ttu-id="03bae-153">El proceso de escritura de metadatos es similar a la forma en que se lee, salvo que se usa un escritor de consultas de metadatos ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="03bae-153">The process of writing metadata is similar to the way it is read except that a metadata query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) is used.</span></span> <span data-ttu-id="03bae-154">El codificador de imágenes implementa la interfaz del escritor de consultas y, como en el lector de consultas, se tiene acceso a los metadatos tanto en el codificador como en los marcos individuales (dependiendo de la compatibilidad con el formato de imagen).</span><span class="sxs-lookup"><span data-stu-id="03bae-154">The query writer interface is implemented by the image encoder and, as in the query reader, metadata is accessed both on the encoder and on individual frames (depending on image format support).</span></span>

<span data-ttu-id="03bae-155">En el código siguiente se muestra cómo obtener un escritor de consultas de un marco de codificador y cómo quitar el valor de clasificación que se leyó previamente.</span><span class="sxs-lookup"><span data-stu-id="03bae-155">The following code demonstrates how to obtain a query writer from an encoder frame and remove the rating value that was previously read.</span></span>


```
// Get the frame's query writer
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/app1/ifd/{ushort=18249}");
}
```



<span data-ttu-id="03bae-156">Otra manera de escribir metadatos es a través de actualizaciones rápidas de metadatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-156">Another way to write metadata is through fast metadata updates.</span></span> <span data-ttu-id="03bae-157">La codificación rápida de metadatos es una manera de escribir metadatos de imagen sin tener que volver a codificar un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="03bae-157">Fast metadata encoding is a way to write image metadata without having to re-encode an image file.</span></span> <span data-ttu-id="03bae-158">Para ello, se escribe una nueva información de metadatos en una región rellenada del formato de metadatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-158">This is done by writing new metadata information to a padded region of the metadata format.</span></span> <span data-ttu-id="03bae-159">El codificador rápido de metadatos ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) se obtiene del generador de componentes, basado en el descodificador de imágenes.</span><span class="sxs-lookup"><span data-stu-id="03bae-159">The fast metadata encoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) is obtained from the component factory, based on the image decoder.</span></span> <span data-ttu-id="03bae-160">A continuación, el codificador de metadatos rápido obtiene un escritor de consultas que se utiliza para escribir los metadatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-160">The fast metadata encoder then obtains a query writer that is used to write the metadata.</span></span> <span data-ttu-id="03bae-161">Por último, el codificador rápido confirma el cambio.</span><span class="sxs-lookup"><span data-stu-id="03bae-161">Finally, the fast encoder commits the change.</span></span>

<span data-ttu-id="03bae-162">En el código siguiente se muestra cómo obtener un codificador de metadatos rápido y usarlo para escribir el valor de MicrosoftRating.</span><span class="sxs-lookup"><span data-stu-id="03bae-162">The following code demonstrates how to obtain a fast metadata encoder and use it to write the MicrosoftRating value.</span></span>


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode,
        &pFME);

    if (SUCCEEDED(hr))
    {
        hr = pFME->GetMetadataQueryWriter(&pFMEQW);
    }

    if (SUCCEEDED(hr))
    {
        // Add additional metadata
        PROPVARIANT value;

        PropVariantInit(&value);

        value.vt = VT_UI4;
        value.uiVal = 99;
        hr = pFMEQW->SetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);

        PropVariantClear(&value);
    }

    if (SUCCEEDED(hr))
    {
        hr = pFME->Commit();
    }
}
```



<span data-ttu-id="03bae-163">No todos los formatos de metadatos admiten metadatos rápidos.</span><span class="sxs-lookup"><span data-stu-id="03bae-163">Not all metadata formats support fast metadata.</span></span> <span data-ttu-id="03bae-164">Para ver qué formatos compatibles de forma nativa admiten la codificación rápida de metadatos, consulte la tabla de la sección [formatos de metadatos admitidos](#supported-metadata-formats) más adelante en este documento.</span><span class="sxs-lookup"><span data-stu-id="03bae-164">To see which natively supported formats support fast metadata encoding, see the table in the [Supported Metadata Formats](#supported-metadata-formats) section later in this document.</span></span>

<span data-ttu-id="03bae-165">En segundo plano, un escritor de consultas usa un escritor de metadatos ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) para escribir los metadatos descritos por la expresión de consulta.</span><span class="sxs-lookup"><span data-stu-id="03bae-165">Behind the scenes, a query writer uses a metadata writer ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) to write the metadata described by the query expression.</span></span> <span data-ttu-id="03bae-166">Además de usar un lector de consultas, también puede tener acceso a un escritor de metadatos directamente para escribir metadatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-166">In addition to using a query reader, you can also access a metadata writer directly to write metadata.</span></span> <span data-ttu-id="03bae-167">Puede obtener un escritor de metadatos del descodificador o de los fotogramas individuales mediante la consulta de una interfaz de bloqueo de bloques ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span><span class="sxs-lookup"><span data-stu-id="03bae-167">You can obtain a metadata writer from the decoder or individual frames using querying for a block writer ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)) interface.</span></span>

## <a name="metadata-extensibility"></a><span data-ttu-id="03bae-168">Extensibilidad de metadatos</span><span class="sxs-lookup"><span data-stu-id="03bae-168">Metadata Extensibility</span></span>

<span data-ttu-id="03bae-169">Como se mencionó anteriormente, WIC proporciona varios controladores de metadatos para leer y escribir metadatos para formatos de metadatos comunes.</span><span class="sxs-lookup"><span data-stu-id="03bae-169">As mentioned previously, WIC provides several metadata handlers to read and write metadata for common metadata formats.</span></span> <span data-ttu-id="03bae-170">Sin embargo, hay algunos formatos de metadatos que no se admiten de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="03bae-170">However, there are some metadata formats that are not natively supported.</span></span> <span data-ttu-id="03bae-171">Por lo tanto, WIC proporciona API para crear controladores de metadatos adicionales que pueden extender la compatibilidad de metadatos a otros formatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-171">Therefore, WIC provides APIs for creating additional metadata handlers that can extend metadata support to other formats.</span></span>

<span data-ttu-id="03bae-172">Para admitir por completo otros formatos de metadatos, se deben desarrollar dos tipos de controladores: un lector de metadatos para leer metadatos y un escritor de metadatos para escribir metadatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-172">To fully support other metadata formats, two types of handlers must be developed — a metadata reader to read metadata and a metadata writer to write metadata.</span></span> <span data-ttu-id="03bae-173">Aunque estos dos controladores se suelen implementar en pares para un formato específico, no es un requisito.</span><span class="sxs-lookup"><span data-stu-id="03bae-173">Although these two handlers are usually implemented in pairs for a specific format, that is not a requirement.</span></span> <span data-ttu-id="03bae-174">Puede haber algunos casos en los que solo sea necesaria la capacidad de lectura o solo la capacidad de escritura.</span><span class="sxs-lookup"><span data-stu-id="03bae-174">There might be some cases in which only the read ability or only the write ability is needed.</span></span>

<span data-ttu-id="03bae-175">Para obtener más información sobre la extensibilidad de metadatos mediante las API de WIC, vea la [Introducción a la extensibilidad de metadatos](-wic-codec-metadatahandlers.md).</span><span class="sxs-lookup"><span data-stu-id="03bae-175">For more information on metadata extensibility using the WIC APIs, see the [Metadata Extensibility Overview](-wic-codec-metadatahandlers.md).</span></span>

## <a name="supported-metadata-formats"></a><span data-ttu-id="03bae-176">Formatos de metadatos admitidos</span><span class="sxs-lookup"><span data-stu-id="03bae-176">Supported Metadata Formats</span></span>

<span data-ttu-id="03bae-177">WIC proporciona compatibilidad con varios formatos de metadatos comunes.</span><span class="sxs-lookup"><span data-stu-id="03bae-177">WIC provides support for several common metadata formats.</span></span> <span data-ttu-id="03bae-178">En la tabla siguiente se enumeran los formatos de metadatos admitidos, sus versiones, los formatos de imagen que admiten el formato de metadatos y si el formato de metadatos admite la codificación rápida de metadatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-178">The following table lists the supported metadata formats, their versions, the image formats that support the metadata format, and whether the metadata format supports fast metadata encoding.</span></span> <span data-ttu-id="03bae-179">Para obtener más información sobre la codificación rápida de metadatos, vea la sección [escribir metadatos de imagen](#writing-image-metadata) anteriormente en este documento.</span><span class="sxs-lookup"><span data-stu-id="03bae-179">For more information about fast metadata encoding, see the [Writing Image Metadata](#writing-image-metadata) section earlier in this document.</span></span>



| <span data-ttu-id="03bae-180">Formatos de metadatos admitidos</span><span class="sxs-lookup"><span data-stu-id="03bae-180">Supported metadata formats</span></span> | <span data-ttu-id="03bae-181">Versión de especificación de metadatos</span><span class="sxs-lookup"><span data-stu-id="03bae-181">Metadata specification version</span></span> | <span data-ttu-id="03bae-182">Compatibilidad con formato de imagen</span><span class="sxs-lookup"><span data-stu-id="03bae-182">Image format support</span></span> | <span data-ttu-id="03bae-183">Admite codificación rápida de metadatos</span><span class="sxs-lookup"><span data-stu-id="03bae-183">Supports fast metadata encoding</span></span> |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| <span data-ttu-id="03bae-184">App0</span><span class="sxs-lookup"><span data-stu-id="03bae-184">App0</span></span>                       | <span data-ttu-id="03bae-185">JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="03bae-185">JFIF 1.02</span></span>                      | <span data-ttu-id="03bae-186">JPEG</span><span class="sxs-lookup"><span data-stu-id="03bae-186">JPEG</span></span>                 | <span data-ttu-id="03bae-187">No</span><span class="sxs-lookup"><span data-stu-id="03bae-187">No</span></span>                              |
| <span data-ttu-id="03bae-188">Aplicación 1</span><span class="sxs-lookup"><span data-stu-id="03bae-188">App1</span></span>                       | <span data-ttu-id="03bae-189">JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="03bae-189">JFIF 1.02</span></span>                      | <span data-ttu-id="03bae-190">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="03bae-190">JPEG, TIFF</span></span>           | <span data-ttu-id="03bae-191">No</span><span class="sxs-lookup"><span data-stu-id="03bae-191">No</span></span>                              |
| <span data-ttu-id="03bae-192">App13</span><span class="sxs-lookup"><span data-stu-id="03bae-192">App13</span></span>                      | <span data-ttu-id="03bae-193">Unknown</span><span class="sxs-lookup"><span data-stu-id="03bae-193">Unknown</span></span>                        | <span data-ttu-id="03bae-194">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="03bae-194">JPEG, TIFF</span></span>           | <span data-ttu-id="03bae-195">No</span><span class="sxs-lookup"><span data-stu-id="03bae-195">No</span></span>                              |
| <span data-ttu-id="03bae-196">IFD</span><span class="sxs-lookup"><span data-stu-id="03bae-196">IFD</span></span>                        | <span data-ttu-id="03bae-197">TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="03bae-197">TIFF 6.0</span></span>                       | <span data-ttu-id="03bae-198">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="03bae-198">JPEG, TIFF</span></span>           | <span data-ttu-id="03bae-199">Sí</span><span class="sxs-lookup"><span data-stu-id="03bae-199">Yes</span></span>                             |
| <span data-ttu-id="03bae-200">IRB</span><span class="sxs-lookup"><span data-stu-id="03bae-200">IRB</span></span>                        | <span data-ttu-id="03bae-201">Unknown</span><span class="sxs-lookup"><span data-stu-id="03bae-201">Unknown</span></span>                        | <span data-ttu-id="03bae-202">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="03bae-202">JPEG, TIFF</span></span>           | <span data-ttu-id="03bae-203">No</span><span class="sxs-lookup"><span data-stu-id="03bae-203">No</span></span>                              |
| <span data-ttu-id="03bae-204">Exif</span><span class="sxs-lookup"><span data-stu-id="03bae-204">Exif</span></span>                       | <span data-ttu-id="03bae-205">EXIF 2,2</span><span class="sxs-lookup"><span data-stu-id="03bae-205">Exif 2.2</span></span>                       | <span data-ttu-id="03bae-206">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="03bae-206">JPEG, TIFF</span></span>           | <span data-ttu-id="03bae-207">Sí</span><span class="sxs-lookup"><span data-stu-id="03bae-207">Yes</span></span>                             |
| <span data-ttu-id="03bae-208">XMP</span><span class="sxs-lookup"><span data-stu-id="03bae-208">XMP</span></span>                        | <span data-ttu-id="03bae-209">XMP 1,0 (2005 de septiembre)</span><span class="sxs-lookup"><span data-stu-id="03bae-209">XMP 1.0 (Sept 2005)</span></span>            | <span data-ttu-id="03bae-210">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="03bae-210">JPEG, TIFF</span></span>           | <span data-ttu-id="03bae-211">Sí</span><span class="sxs-lookup"><span data-stu-id="03bae-211">Yes</span></span>                             |
| <span data-ttu-id="03bae-212">GPS</span><span class="sxs-lookup"><span data-stu-id="03bae-212">GPS</span></span>                        | <span data-ttu-id="03bae-213">EXIF 2,2</span><span class="sxs-lookup"><span data-stu-id="03bae-213">Exif 2.2</span></span>                       | <span data-ttu-id="03bae-214">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="03bae-214">JPEG, TIFF</span></span>           | <span data-ttu-id="03bae-215">Sí</span><span class="sxs-lookup"><span data-stu-id="03bae-215">Yes</span></span>                             |
| <span data-ttu-id="03bae-216">CREACIÓN</span><span class="sxs-lookup"><span data-stu-id="03bae-216">IPTC</span></span>                       | <span data-ttu-id="03bae-217">IPTC 4,0</span><span class="sxs-lookup"><span data-stu-id="03bae-217">IPTC 4.0</span></span>                       | <span data-ttu-id="03bae-218">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="03bae-218">JPEG, TIFF</span></span>           | <span data-ttu-id="03bae-219">Sí</span><span class="sxs-lookup"><span data-stu-id="03bae-219">Yes</span></span>                             |
| <span data-ttu-id="03bae-220">Negrita</span><span class="sxs-lookup"><span data-stu-id="03bae-220">tEXt</span></span>                       | <span data-ttu-id="03bae-221">PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="03bae-221">PNG 1.2</span></span>                        | <span data-ttu-id="03bae-222">PNG</span><span class="sxs-lookup"><span data-stu-id="03bae-222">PNG</span></span>                  | <span data-ttu-id="03bae-223">No</span><span class="sxs-lookup"><span data-stu-id="03bae-223">No</span></span>                              |



 

> [!Note]  
> <span data-ttu-id="03bae-224">IPTC solo admite FME si los bloques aumentan de tamaño, ya que IPTC no admite el relleno.</span><span class="sxs-lookup"><span data-stu-id="03bae-224">IPTC only supports FME if the blocks grow in size, as IPTC does not support padding.</span></span>

 

## <a name="metadata-component-summary"></a><span data-ttu-id="03bae-225">Resumen de los componentes de metadatos</span><span class="sxs-lookup"><span data-stu-id="03bae-225">Metadata Component Summary</span></span>

<span data-ttu-id="03bae-226">En la tabla siguiente se describen las interfaces de WIC que admiten metadatos y sus componentes correspondientes.</span><span class="sxs-lookup"><span data-stu-id="03bae-226">The following table describes the WIC interfaces that support metadata, and their corresponding components.</span></span> <span data-ttu-id="03bae-227">Estos componentes proporcionan el acceso a los metadatos de una imagen.</span><span class="sxs-lookup"><span data-stu-id="03bae-227">These components provide the access to an image's metadata.</span></span> <span data-ttu-id="03bae-228">Para obtener más información acerca de estos componentes, consulte la [información general](-wic-about-windows-imaging-codec.md)sobre el componente de creación de imágenes de Windows.</span><span class="sxs-lookup"><span data-stu-id="03bae-228">For more information about these components, see the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03bae-229">Componente</span><span class="sxs-lookup"><span data-stu-id="03bae-229">Component</span></span></th>
<th><span data-ttu-id="03bae-230">Descripción</span><span class="sxs-lookup"><span data-stu-id="03bae-230">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03bae-231">Descodificador de mapa de bits (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="03bae-231">Bitmap Decoder (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="03bae-232">Lee una secuencia de imágenes y genera un origen de mapas de bits utilizable.</span><span class="sxs-lookup"><span data-stu-id="03bae-232">Reads an image stream and produces a usable bitmap source.</span></span> <span data-ttu-id="03bae-233">Asociado con un formato de contenedor como Tagged Image File Format (TIFF) o Joint Photographic Experts Group (JPEG).</span><span class="sxs-lookup"><span data-stu-id="03bae-233">Associated with a container format such as Tagged Image File Format (TIFF) or Joint Photographic Experts Group (JPEG).</span></span></li>
<li><span data-ttu-id="03bae-234">Implementa una interfaz <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> para enumerar todos los bloques de metadatos del flujo de datos del descodificador que no están dentro de un marco.</span><span class="sxs-lookup"><span data-stu-id="03bae-234">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> interface to enumerate all of the metadata blocks in the decoder's data stream that are not inside a frame.</span></span></li>
<li><span data-ttu-id="03bae-235">Expone un lector de consultas para leer los metadatos asociados a la imagen que no está dentro de un marco.</span><span class="sxs-lookup"><span data-stu-id="03bae-235">Exposes a query reader to read the metadata associated with the image that is not inside a frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03bae-236">Descodificación de fotogramas de mapa de bits (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="03bae-236">Bitmap Frame Decode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="03bae-237">Accede a fotogramas individuales desde el flujo de imágenes mantenido por el descodificador.</span><span class="sxs-lookup"><span data-stu-id="03bae-237">Accesses individual frames from the image stream held by the decoder.</span></span></li>
<li><span data-ttu-id="03bae-238">Implementa una interfaz <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> para enumerar todos los bloques de metadatos en el flujo de datos del marco.</span><span class="sxs-lookup"><span data-stu-id="03bae-238">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> interface to enumerate all of the metadata blocks in the frame's data stream.</span></span></li>
<li><span data-ttu-id="03bae-239">Expone un lector de consultas para leer los metadatos asociados con el marco, mediante expresiones de consulta.</span><span class="sxs-lookup"><span data-stu-id="03bae-239">Exposes a query reader to read the metadata associated with the frame, using query expressions.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03bae-240">Codificador de mapa de bits (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="03bae-240">Bitmap Encoder (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="03bae-241">Escribe un origen de mapa de bits en una secuencia de imágenes.</span><span class="sxs-lookup"><span data-stu-id="03bae-241">Writes a bitmap source to an image stream.</span></span> <span data-ttu-id="03bae-242">Asociado con un formato de contenedor como TIFF o JPEG.</span><span class="sxs-lookup"><span data-stu-id="03bae-242">Associated with a container format such as TIFF or JPEG.</span></span></li>
<li><span data-ttu-id="03bae-243">Implementa una interfaz <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> para crear una lista de bloques de metadatos que se van a escribir en el flujo de datos del codificador.</span><span class="sxs-lookup"><span data-stu-id="03bae-243">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> interface to build up a list of metadata blocks to write into the data stream of the encoder.</span></span></li>
<li><span data-ttu-id="03bae-244">Expone un escritor de consultas para escribir los metadatos asociados a la imagen mediante expresiones de consulta.</span><span class="sxs-lookup"><span data-stu-id="03bae-244">Exposes a query writer to write the metadata associated with the image, using query expressions.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03bae-245">Código de marco Bitma (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="03bae-245">Bitma Frame Encode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="03bae-246">Crea un marco que se codificará en el flujo mantenido por el codificador.</span><span class="sxs-lookup"><span data-stu-id="03bae-246">Creates a frame that will be encoded into the stream held by the encoder.</span></span></li>
<li><span data-ttu-id="03bae-247">Implementa una interfaz <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> para crear una lista de bloques de metadatos que se van a escribir en el flujo de datos del marco.</span><span class="sxs-lookup"><span data-stu-id="03bae-247">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> interface to build up a list of metadata blocks to write into the frame's data stream.</span></span></li>
<li><span data-ttu-id="03bae-248">Expone un escritor de consultas para escribir los metadatos asociados con el marco, mediante expresiones de consulta.</span><span class="sxs-lookup"><span data-stu-id="03bae-248">Exposes a query writer to write the metadata associated with the frame, using query expressions.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="03bae-249">En la tabla siguiente se describen los componentes de metadatos de WIC.</span><span class="sxs-lookup"><span data-stu-id="03bae-249">The following table describes the WIC metadata components.</span></span> <span data-ttu-id="03bae-250">Estos componentes permiten leer y escribir los metadatos en una imagen expuesta por los componentes enumerados en la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="03bae-250">These components enable you to read and write the metadata in an image exposed by the components listed in the previous table.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03bae-251">Componente</span><span class="sxs-lookup"><span data-stu-id="03bae-251">Component</span></span></th>
<th><span data-ttu-id="03bae-252">Descripción</span><span class="sxs-lookup"><span data-stu-id="03bae-252">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03bae-253">Lector de consultas de metadatos (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="03bae-253">Metadata Query Reader (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="03bae-254">Toma una cadena de consulta y navega por la jerarquía de metadatos subyacentes para obtener los metadatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-254">Takes a query string and navigates the underlying metadata hierarchy to get metadata.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03bae-255">Escritor de consultas de metadatos (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="03bae-255">Metadata Query Writer (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="03bae-256">Toma una cadena de consulta y navega por la jerarquía de metadatos subyacentes para obtener, establecer y quitar metadatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-256">Takes a query string and navigates the underlying metadata hierarchy to get, set, and remove metadata.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03bae-257">Lector de bloques de metadatos (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="03bae-257">Metadata Block Reader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="03bae-258">Administra una colección de solo lectura de objetos <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> en la parte superior de la jerarquía de metadatos y habilita la enumeración de todos los bloques de metadatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-258">Manages a read-only collection of <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> objects at the top of the metadata hierarchy and enables enumeration of all metadata blocks.</span></span></li>
<li><span data-ttu-id="03bae-259">Implementado por un descodificador de mapa de bits y un marco de mapa de bits descodificado.</span><span class="sxs-lookup"><span data-stu-id="03bae-259">Implemented by a bitmap decoder and a decoded bitmap frame.</span></span></li>
<li><span data-ttu-id="03bae-260">Implementado por desarrolladores de componentes de terceros para códecs personalizados.</span><span class="sxs-lookup"><span data-stu-id="03bae-260">Implemented by third-party component developers for custom codecs.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03bae-261">Escritor de bloques de metadatos (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="03bae-261">Metadata Block Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="03bae-262">Administra una colección de lectura y escritura de objetos <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> en la parte superior de la jerarquía de metadatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-262">Manages a read and write collection of <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> objects at the top of the metadata hierarchy.</span></span></li>
<li><span data-ttu-id="03bae-263">Implementado por un codificador de mapa de bits y un código de marco de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="03bae-263">Implemented by a bitmap encoder and a bitmap frame encode.</span></span></li>
<li><span data-ttu-id="03bae-264">Implementado por desarrolladores de componentes de terceros para códecs personalizados.</span><span class="sxs-lookup"><span data-stu-id="03bae-264">Implemented by third-party component developers for custom codecs.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03bae-265">Lector de metadatos (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="03bae-265">Metadata Reader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="03bae-266">Analiza una secuencia de metadatos y administra una colección de solo lectura de los elementos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-266">Parses a stream of metadata and manages a read-only collection of the metadata items.</span></span> <span data-ttu-id="03bae-267">Asociado con un formato de metadatos como EXIF, IFD y XMP.</span><span class="sxs-lookup"><span data-stu-id="03bae-267">Associated with a metadata format such as EXIF, IFD, and XMP.</span></span></li>
<li><span data-ttu-id="03bae-268">Actúa como diccionario y devuelve un valor cuando se proporciona un par de formato y identificador.</span><span class="sxs-lookup"><span data-stu-id="03bae-268">Acts as a dictionary, returning a value when given a format and ID pair.</span></span></li>
<li><span data-ttu-id="03bae-269">Implementado por desarrolladores de componentes de terceros para tipos de metadatos personalizados.</span><span class="sxs-lookup"><span data-stu-id="03bae-269">Implemented by third-party component developers for custom metadata types.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03bae-270">Escritor de metadatos (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="03bae-270">Metadata Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="03bae-271">Analiza y serializa una secuencia de metadatos y administra una colección de lectura/escritura de elementos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="03bae-271">Parses and serializes a stream of metadata and manages a read/write collection of metadata items.</span></span></li>
<li><span data-ttu-id="03bae-272">Implementado por desarrolladores de componentes de terceros para tipos de metadatos personalizados.</span><span class="sxs-lookup"><span data-stu-id="03bae-272">Implemented by third-party component developers for custom metadata types.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03bae-273">Codificador de metadatos rápido<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="03bae-273">Fast Metadata Encoder<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a></span></span></td>
<td><ul>
<li><span data-ttu-id="03bae-274">Expone la semántica para escribir en una jerarquía de metadatos que actualizará los metadatos en su lugar sin volver a codificar la imagen.</span><span class="sxs-lookup"><span data-stu-id="03bae-274">Exposes semantics for writing on a metadata hierarchy that will update metadata in place without re-encoding the image.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="03bae-275">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="03bae-275">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="03bae-276">**Vista**</span><span class="sxs-lookup"><span data-stu-id="03bae-276">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="03bae-277">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="03bae-277">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="03bae-278">Información general del lenguaje de consulta de metadatos</span><span class="sxs-lookup"><span data-stu-id="03bae-278">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="03bae-279">Información general sobre la lectura y escritura de metadatos de imagen</span><span class="sxs-lookup"><span data-stu-id="03bae-279">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="03bae-280">Información general sobre la extensibilidad de metadatos</span><span class="sxs-lookup"><span data-stu-id="03bae-280">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> <dt>

[<span data-ttu-id="03bae-281">Cómo volver a codificar una imagen JPEG con metadatos</span><span class="sxs-lookup"><span data-stu-id="03bae-281">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



