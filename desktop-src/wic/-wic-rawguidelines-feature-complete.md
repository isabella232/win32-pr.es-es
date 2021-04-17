---
description: 'Integridad de características: interfaces recomendadas'
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 'Integridad de características: interfaces recomendadas'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1dba4bcc029b2205985afb443526376c0eecb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697490"
---
# <a name="feature-completeness-recommended-interfaces"></a><span data-ttu-id="90c60-103">Integridad de características: interfaces recomendadas</span><span class="sxs-lookup"><span data-stu-id="90c60-103">Feature Completeness: Recommended Interfaces</span></span>

<span data-ttu-id="90c60-104">En la tabla siguiente se enumeran los códecs sin formato de Windows Imaging Component (WIC) que deben implementar.</span><span class="sxs-lookup"><span data-stu-id="90c60-104">The following table lists the Windows Imaging Component (WIC) interfaces RAW codecs should implement.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90c60-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="90c60-105">Interface</span></span></th>
<th><span data-ttu-id="90c60-106">Requerido para</span><span class="sxs-lookup"><span data-stu-id="90c60-106">Required for</span></span></th>
<th><span data-ttu-id="90c60-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="90c60-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="90c60-108"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="90c60-108"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></span></span></td>
<td><span data-ttu-id="90c60-109">Descodificadores</span><span class="sxs-lookup"><span data-stu-id="90c60-109">Decoders</span></span></td>
<td><span data-ttu-id="90c60-110">Representa el punto inicial para descodificar un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="90c60-110">Represents the starting point for decoding an image file.</span></span> <span data-ttu-id="90c60-111">Proporciona acceso a las propiedades de nivel de contenedor como miniaturas, fotogramas y paleta.</span><span class="sxs-lookup"><span data-stu-id="90c60-111">Provides access to container-level properties like thumbnails, frames, and palette.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90c60-112"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></span><span class="sxs-lookup"><span data-stu-id="90c60-112"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></span></span></td>
<td><span data-ttu-id="90c60-113">Descodificadores</span><span class="sxs-lookup"><span data-stu-id="90c60-113">Decoders</span></span></td>
<td><span data-ttu-id="90c60-114">Representa un marco de imagen específico dentro del contenedor que proporciona acceso a las propiedades de nivel de marco.</span><span class="sxs-lookup"><span data-stu-id="90c60-114">Represents a specific image frame within the container that provides access to frame-level properties.</span></span> <span data-ttu-id="90c60-115">Esta es la interfaz que descodifica los bits de imagen reales.</span><span class="sxs-lookup"><span data-stu-id="90c60-115">This is the interface that decodes the actual image bits.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90c60-116"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></span><span class="sxs-lookup"><span data-stu-id="90c60-116"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></span></span></td>
<td><span data-ttu-id="90c60-117">Descodificadores</span><span class="sxs-lookup"><span data-stu-id="90c60-117">Decoders</span></span></td>
<td><span data-ttu-id="90c60-118">Se requiere para enumerar y recorrer en iteración los bloques de metadatos e invocar los lectores de metadatos adecuados al leer de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="90c60-118">Required for enumerating and iterating through metadata blocks and invoking the appropriate metadata readers when reading from an image file.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90c60-119">Si el formato de contenedor sin formato es compatible con TIFF o usa IFDs estándar o IRBs para almacenar metadatos EXIF o XMP, los creadores de códecs pueden optar por invocar los lectores de metadatos integrados en lugar de escribir los suyos propios.</span><span class="sxs-lookup"><span data-stu-id="90c60-119">If the RAW container format is TIFF compatible or uses standard IFDs or IRBs to store EXIF or XMP metadata, codec authors can choose to invoke the built-in metadata readers rather than writing their own.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90c60-120"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></span><span class="sxs-lookup"><span data-stu-id="90c60-120"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></span></span></td>
<td><span data-ttu-id="90c60-121">Descodificadores</span><span class="sxs-lookup"><span data-stu-id="90c60-121">Decoders</span></span></td>
<td><span data-ttu-id="90c60-122">Permite al llamador especificar el escalado, el recorte, la rotación o el formato de píxel deseado para la imagen descodificada, lo que puede mejorar significativamente el rendimiento del descodificador.</span><span class="sxs-lookup"><span data-stu-id="90c60-122">Allows the caller to specify desired scaling, cropping, rotation, or pixel format for the decoded image, which can significantly improve decoder performance.</span></span> <span data-ttu-id="90c60-123">Por ejemplo, los descodificadores JPEG y Protocolo de datagramas inalámbricos (WDP) de Microsoft usan un esquema de optimización piramidal para lograr una descodificación más rápida cuando el mapa de bits de destino es menor que el mapa de bits de origen.</span><span class="sxs-lookup"><span data-stu-id="90c60-123">For example, Microsoft's JPEG and Wireless Datagram Protocol (WDP) decoders use a pyramid optimization scheme to achieve faster decoding when the target bitmap is smaller than the source bitmap.</span></span> <span data-ttu-id="90c60-124">Windows Vista (y versiones posteriores) intentará usar esta interfaz para extraer una &quot; &quot; vista previa rápida de una imagen sin procesar siempre que falte la vista previa incrustada o menos de 1.024 píxeles en su dimensión más grande.</span><span class="sxs-lookup"><span data-stu-id="90c60-124">Windows Vista (and later) will attempt to use this interface to extract a &quot;fast&quot; preview from a RAW image whenever the embedded preview is missing or less than 1,024 pixels in its largest dimension.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90c60-125"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></span><span class="sxs-lookup"><span data-stu-id="90c60-125"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></span></span></td>
<td><span data-ttu-id="90c60-126">Descodificadores</span><span class="sxs-lookup"><span data-stu-id="90c60-126">Decoders</span></span></td>
<td><span data-ttu-id="90c60-127">Se requiere para los formatos sin formato.</span><span class="sxs-lookup"><span data-stu-id="90c60-127">Required for RAW formats.</span></span> <span data-ttu-id="90c60-128">Expone parámetros que son específicos del procesamiento de imágenes sin procesar.</span><span class="sxs-lookup"><span data-stu-id="90c60-128">Exposes parameters that are specific to RAW image processing.</span></span> <span data-ttu-id="90c60-129">Los códecs sin formato deben admitir todos los parámetros que se aplican al códec.</span><span class="sxs-lookup"><span data-stu-id="90c60-129">RAW codecs should support as many of these parameters as apply to the codec.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90c60-130"><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="90c60-130"><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></span></span></td>
<td><span data-ttu-id="90c60-131">Codificadores</span><span class="sxs-lookup"><span data-stu-id="90c60-131">Encoders</span></span></td>
<td><span data-ttu-id="90c60-132">Representa el punto inicial para codificar un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="90c60-132">Represents the starting point for encoding an image file.</span></span> <span data-ttu-id="90c60-133">Esta interfaz se usa para establecer las propiedades de nivel de contenedor, como miniaturas, fotogramas y paleta.</span><span class="sxs-lookup"><span data-stu-id="90c60-133">This interface is used for setting container-level properties, such as thumbnails, frames, and palette.</span></span> <span data-ttu-id="90c60-134">También es necesario invocar un escritor de metadatos para habilitar la persistencia de metadatos en el archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="90c60-134">It is also required to invoke a metadata writer to enable metadata persistence to the image file.</span></span> <span data-ttu-id="90c60-135">Por estos motivos, esta interfaz es necesaria incluso si no se admite la codificación del mapa de bits principal en el formato sin procesar.</span><span class="sxs-lookup"><span data-stu-id="90c60-135">For these reasons, this interface is necessary even if encoding the primary bitmap to the RAW format is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90c60-136"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></span><span class="sxs-lookup"><span data-stu-id="90c60-136"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></span></span></td>
<td><span data-ttu-id="90c60-137">Codificadores</span><span class="sxs-lookup"><span data-stu-id="90c60-137">Encoders</span></span></td>
<td><span data-ttu-id="90c60-138">Representa un marco de imagen específico dentro del contenedor.</span><span class="sxs-lookup"><span data-stu-id="90c60-138">Represents a specific image frame within the container.</span></span> <span data-ttu-id="90c60-139">Esta interfaz se usa para codificar los bits de imagen reales y para establecer las propiedades y los metadatos de cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="90c60-139">This interface is used to encode the actual image bits and to set per-frame metadata and properties.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90c60-140"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></span><span class="sxs-lookup"><span data-stu-id="90c60-140"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></span></span></td>
<td><span data-ttu-id="90c60-141">Codificadores</span><span class="sxs-lookup"><span data-stu-id="90c60-141">Encoders</span></span></td>
<td><span data-ttu-id="90c60-142">Necesario para recorrer en iteración los bloques de metadatos e invocar los escritores de metadatos adecuados al serializar un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="90c60-142">Required for iterating through metadata blocks and invoking the appropriate metadata writers when serializing an image file.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90c60-143">Si el formato de contenedor sin formato es compatible con TIFF, los creadores de códecs pueden optar por invocar los escritores de metadatos integrados en lugar de escribir los suyos propios.</span><span class="sxs-lookup"><span data-stu-id="90c60-143">If the RAW container format is TIFF-compatible, codec authors can choose to invoke the built-in metadata writers rather than writing their own.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="90c60-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90c60-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="90c60-145">**Vista**</span><span class="sxs-lookup"><span data-stu-id="90c60-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="90c60-146">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="90c60-146">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="90c60-147">Instrucciones de WIC para formatos de imagen RAW de cámara</span><span class="sxs-lookup"><span data-stu-id="90c60-147">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="90c60-148">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="90c60-148">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




