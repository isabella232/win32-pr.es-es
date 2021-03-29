---
description: Requisitos del método de interfaz
ms.assetid: 8c2afeb3-3e0b-4f8a-a2f4-df7c9ce4b098
title: Requisitos del método de interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9cabe02900fa789773f4104cf282ab326bd4930
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648569"
---
# <a name="interface-method-requirements"></a><span data-ttu-id="cd00c-103">Requisitos del método de interfaz</span><span class="sxs-lookup"><span data-stu-id="cd00c-103">Interface Method Requirements</span></span>

<span data-ttu-id="cd00c-104">No todos los métodos de cada interfaz deben tener una implementación de.</span><span class="sxs-lookup"><span data-stu-id="cd00c-104">Not every method on every interface must have an implementation.</span></span> <span data-ttu-id="cd00c-105">Por ejemplo, algunos códecs tienen metadatos globales, miniaturas o contextos de color, mientras que otros códecs los proporcionan únicamente en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="cd00c-105">For example, some codecs have global metadata, thumbnails, or color contexts, whereas other codecs provide these only on a per-frame basis.</span></span> <span data-ttu-id="cd00c-106">Si los autores de códecs proporcionan estos solo en cada fotograma, solo necesitan [**implementar el**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) o ColorContexts, o bien implementar los métodos [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) o [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) en [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) y [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) en lugar de en [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) y [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span><span class="sxs-lookup"><span data-stu-id="cd00c-106">If codec authors provide these only on a per-frame basis, they need only implement the [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)/[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) or ColorContexts, or implement the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) or [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) methods on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) rather than on the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span></span> <span data-ttu-id="cd00c-107">Del mismo modo, algunos códecs no usan formatos indexados, por lo que no son necesarios para implementar los métodos [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) y [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="cd00c-107">Likewise, some codecs do not use indexed formats and so are not required to implement the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) and [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) methods.</span></span> <span data-ttu-id="cd00c-108">Por lo tanto, estos métodos son opcionales y se dejan a la discreción del creador del códec.</span><span class="sxs-lookup"><span data-stu-id="cd00c-108">These methods are therefore optional and are left to the discretion of the codec creator.</span></span> <span data-ttu-id="cd00c-109">La mayoría de los demás métodos son necesarios.</span><span class="sxs-lookup"><span data-stu-id="cd00c-109">Most other methods are required.</span></span>

<span data-ttu-id="cd00c-110">Para Windows 7 [](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview), / se necesitan Get [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) y [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) y se deben implementar en las clases de nivel de contenido o en las clases de nivel de marco.</span><span class="sxs-lookup"><span data-stu-id="cd00c-110">For Windows 7 [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)/[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) and [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)/[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) are required and must be implemented on either the contain-level classes or on the frame-level classes.</span></span> <span data-ttu-id="cd00c-111">Si el formato de archivo de imagen no admite vistas previas ni vistas en miniatura en ninguna de estas ubicaciones, debe revisar el formato del archivo de imagen para proporcionar dicha compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="cd00c-111">If your image file format doesn't support previews or thumbnails in either of these locations, then you should revise your image file format to provide such support.</span></span>

<span data-ttu-id="cd00c-112">Cuando no se implementa un método, es importante devolver un error adecuado para que el autor de la llamada pueda determinar que la característica solicitada no se admite.</span><span class="sxs-lookup"><span data-stu-id="cd00c-112">When a method is not implemented, it is important to return an appropriate error so the caller can determine that the requested feature is not supported.</span></span> <span data-ttu-id="cd00c-113">Por ejemplo, si los autores de códecs no admiten miniaturas de nivel de contenedor, deben devolver [WINCODEC \_ Err \_ CODECNOTHUMBNAIL](-wic-codec-error-codes.md) cuando una aplicación llama a [**GetThumbnail**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md)y, si no tienen una paleta, deben devolver [WINCODEC \_ Err \_ PALETTEUNAVAILABLE](-wic-codec-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cd00c-113">For example, if codec authors do not support container-level thumbnails, they should return [WINCODEC\_ERR\_CODECNOTHUMBNAIL](-wic-codec-error-codes.md) when an application calls [**GetThumbnail**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md), and if they don't have a palette, they should return [WINCODEC\_ERR\_PALETTEUNAVAILABLE](-wic-codec-error-codes.md).</span></span> <span data-ttu-id="cd00c-114">Si no existe ningún código de [ \_ error WINCODEC](-wic-codec-error-codes.md) adecuado, el códec debe devolver E \_ NOTIMPL para los métodos no implementados.</span><span class="sxs-lookup"><span data-stu-id="cd00c-114">If no suitable [WINCODEC\_ERR](-wic-codec-error-codes.md) code exists, then the codec should return E\_NOTIMPL for unimplemented methods.</span></span>

<span data-ttu-id="cd00c-115">En las tablas siguientes se enumeran los métodos obligatorios y opcionales para cada interfaz de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="cd00c-115">The following tables list the required and optional methods for each Windows Imaging Component (WIC) interfaces.</span></span>

[<span data-ttu-id="cd00c-116">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="cd00c-116">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)



<span data-ttu-id="cd00c-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="cd00c-117">Required</span></span>

[<span data-ttu-id="cd00c-118">**QueryCapability**</span><span class="sxs-lookup"><span data-stu-id="cd00c-118">**QueryCapability**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability)

[<span data-ttu-id="cd00c-119">**Inicialización**</span><span class="sxs-lookup"><span data-stu-id="cd00c-119">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize)

[<span data-ttu-id="cd00c-120">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="cd00c-120">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)

[<span data-ttu-id="cd00c-121">**GetDecoderInfo**</span><span class="sxs-lookup"><span data-stu-id="cd00c-121">**GetDecoderInfo**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo)

[<span data-ttu-id="cd00c-122">**GetFrameCount**</span><span class="sxs-lookup"><span data-stu-id="cd00c-122">**GetFrameCount**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)

[<span data-ttu-id="cd00c-123">**GetFrame**</span><span class="sxs-lookup"><span data-stu-id="cd00c-123">**GetFrame**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe)

<span data-ttu-id="cd00c-124">Opcionales</span><span class="sxs-lookup"><span data-stu-id="cd00c-124">Optional</span></span>

<span data-ttu-id="cd00c-125">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹</span><span class="sxs-lookup"><span data-stu-id="cd00c-125">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹</span></span>

<span data-ttu-id="cd00c-126">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²</span><span class="sxs-lookup"><span data-stu-id="cd00c-126">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²</span></span>

[<span data-ttu-id="cd00c-127">**GetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="cd00c-127">**GetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)

[<span data-ttu-id="cd00c-128">**GetMetadataQueryReader**</span><span class="sxs-lookup"><span data-stu-id="cd00c-128">**GetMetadataQueryReader**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)

[<span data-ttu-id="cd00c-129">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="cd00c-129">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

<span data-ttu-id="cd00c-130">¹ se requiere si el formato de archivo de imagen admite las vistas previas de nivel de contenedor.</span><span class="sxs-lookup"><span data-stu-id="cd00c-130">¹Required if your image file format supports container-level previews.</span></span> <span data-ttu-id="cd00c-131">Si no es así, le recomendamos encarecidamente que revise el formato del archivo de imagen para que sea compatible.</span><span class="sxs-lookup"><span data-stu-id="cd00c-131">If this is not the case you are strongly encouraged to revise your image file format to support this.</span></span> <span data-ttu-id="cd00c-132">Si se implementa aquí, se requiere un [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) correspondiente en la clase de codificación de nivel de contenedor.</span><span class="sxs-lookup"><span data-stu-id="cd00c-132">If implemented here, then a corresponding [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) is required on the container-level encode class.</span></span>

<span data-ttu-id="cd00c-133">² se requiere aquí o en la clase de descodificación en el nivel de marco, en función del lugar en el que el formato de archivo de imagen almacena las miniaturas.</span><span class="sxs-lookup"><span data-stu-id="cd00c-133">²Required either here, or on the frame-level decode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="cd00c-134">Si se implementa aquí, se requiere un [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) correspondiente en la clase de codificación de nivel de contenedor.</span><span class="sxs-lookup"><span data-stu-id="cd00c-134">If implemented here, then a corresponding [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) is required on the container-level encode class.</span></span>

[<span data-ttu-id="cd00c-135">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="cd00c-135">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)



<span data-ttu-id="cd00c-136">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="cd00c-136">Required</span></span>

[<span data-ttu-id="cd00c-137">**GetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="cd00c-137">**GetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)

[<span data-ttu-id="cd00c-138">**GetMetadataQueryReader**</span><span class="sxs-lookup"><span data-stu-id="cd00c-138">**GetMetadataQueryReader**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)

[<span data-ttu-id="cd00c-139">**GetSize (**</span><span class="sxs-lookup"><span data-stu-id="cd00c-139">**GetSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)

[<span data-ttu-id="cd00c-140">**GetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="cd00c-140">**GetPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)

[<span data-ttu-id="cd00c-141">**GetResolution**</span><span class="sxs-lookup"><span data-stu-id="cd00c-141">**GetResolution**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution)

[<span data-ttu-id="cd00c-142">**CopyPixels**</span><span class="sxs-lookup"><span data-stu-id="cd00c-142">**CopyPixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)

<span data-ttu-id="cd00c-143">Opcionales</span><span class="sxs-lookup"><span data-stu-id="cd00c-143">Optional</span></span>

<span data-ttu-id="cd00c-144">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹</span><span class="sxs-lookup"><span data-stu-id="cd00c-144">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹</span></span>

[<span data-ttu-id="cd00c-145">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="cd00c-145">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

<span data-ttu-id="cd00c-146">¹ se requiere aquí o en la clase de descodificación de nivel de contenedor, en función del lugar en el que el formato de archivo de imagen almacena las miniaturas.</span><span class="sxs-lookup"><span data-stu-id="cd00c-146">¹Required either here, or on the container-level decode class, depending on where you image file format stores thumbnails.</span></span> <span data-ttu-id="cd00c-147">Si se implementa aquí, se requiere un [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) correspondiente en la clase de codificador de nivel de marco.</span><span class="sxs-lookup"><span data-stu-id="cd00c-147">If implemented here, then a corresponding [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) is required on the frame-level encoder class.</span></span>

[<span data-ttu-id="cd00c-148">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="cd00c-148">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



<span data-ttu-id="cd00c-149">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="cd00c-149">Required</span></span>

[<span data-ttu-id="cd00c-150">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="cd00c-150">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat)

[<span data-ttu-id="cd00c-151">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="cd00c-151">**GetCount**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount)

[<span data-ttu-id="cd00c-152">**GetReaderByIndex**</span><span class="sxs-lookup"><span data-stu-id="cd00c-152">**GetReaderByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex)

[<span data-ttu-id="cd00c-153">**GetEnumerator**</span><span class="sxs-lookup"><span data-stu-id="cd00c-153">**GetEnumerator**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator)



 

[<span data-ttu-id="cd00c-154">**IWICBitmapSourceTransform**</span><span class="sxs-lookup"><span data-stu-id="cd00c-154">**IWICBitmapSourceTransform**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)



<span data-ttu-id="cd00c-155">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="cd00c-155">Required</span></span>

[<span data-ttu-id="cd00c-156">**DoesSupportTransform**</span><span class="sxs-lookup"><span data-stu-id="cd00c-156">**DoesSupportTransform**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)

[<span data-ttu-id="cd00c-157">**CopyPixels**</span><span class="sxs-lookup"><span data-stu-id="cd00c-157">**CopyPixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)

<span data-ttu-id="cd00c-158">Opcionales</span><span class="sxs-lookup"><span data-stu-id="cd00c-158">Optional</span></span>

[<span data-ttu-id="cd00c-159">**GetClosestSize**</span><span class="sxs-lookup"><span data-stu-id="cd00c-159">**GetClosestSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize)

[<span data-ttu-id="cd00c-160">**GetClosestPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="cd00c-160">**GetClosestPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)



 

[<span data-ttu-id="cd00c-161">**IWICDevelopRaw**</span><span class="sxs-lookup"><span data-stu-id="cd00c-161">**IWICDevelopRaw**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)

<span data-ttu-id="cd00c-162">Consulte [compatibilidad con IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md), más adelante en este documento.</span><span class="sxs-lookup"><span data-stu-id="cd00c-162">See [Support for IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md), later in this document.</span></span>

[<span data-ttu-id="cd00c-163">**IWICBitmapEncoder**</span><span class="sxs-lookup"><span data-stu-id="cd00c-163">**IWICBitmapEncoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)



<span data-ttu-id="cd00c-164">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="cd00c-164">Required</span></span>

[<span data-ttu-id="cd00c-165">**Inicialización**</span><span class="sxs-lookup"><span data-stu-id="cd00c-165">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[<span data-ttu-id="cd00c-166">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="cd00c-166">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat)

[<span data-ttu-id="cd00c-167">**GetEncoderInfo**</span><span class="sxs-lookup"><span data-stu-id="cd00c-167">**GetEncoderInfo**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo)

[<span data-ttu-id="cd00c-168">**CreateNewFrame**</span><span class="sxs-lookup"><span data-stu-id="cd00c-168">**CreateNewFrame**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)

[<span data-ttu-id="cd00c-169">**Promete**</span><span class="sxs-lookup"><span data-stu-id="cd00c-169">**Commit**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

<span data-ttu-id="cd00c-170">Opcionales</span><span class="sxs-lookup"><span data-stu-id="cd00c-170">Optional</span></span>

<span data-ttu-id="cd00c-171">[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹</span><span class="sxs-lookup"><span data-stu-id="cd00c-171">[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹</span></span>

<span data-ttu-id="cd00c-172">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²</span><span class="sxs-lookup"><span data-stu-id="cd00c-172">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²</span></span>

[<span data-ttu-id="cd00c-173">**SetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="cd00c-173">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setcolorcontexts)

[<span data-ttu-id="cd00c-174">**GetMetadataQueryWriter**</span><span class="sxs-lookup"><span data-stu-id="cd00c-174">**GetMetadataQueryWriter**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)

[<span data-ttu-id="cd00c-175">**SetPalette**</span><span class="sxs-lookup"><span data-stu-id="cd00c-175">**SetPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)



 

<span data-ttu-id="cd00c-176">¹ se requiere si el formato de archivo de imagen admite vistas previas de nivel de marco.</span><span class="sxs-lookup"><span data-stu-id="cd00c-176">¹Required if your image file format supports frame-level previews.</span></span>

<span data-ttu-id="cd00c-177">² se requiere aquí o bien, en la clase de codificación en el nivel de marco, en función del lugar en el que el formato de archivo de imagen almacena las miniaturas.</span><span class="sxs-lookup"><span data-stu-id="cd00c-177">²Required either here, or on the frame-level encode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="cd00c-178">Si se implementa aquí, se requiere un [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) correspondiente en la clase de descodificación de nivel de contenedor.</span><span class="sxs-lookup"><span data-stu-id="cd00c-178">If implemented here, then a corresponding [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) is required on the container-level decode class.</span></span>

[<span data-ttu-id="cd00c-179">**IWICBitmapFrameEncode**</span><span class="sxs-lookup"><span data-stu-id="cd00c-179">**IWICBitmapFrameEncode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)



<span data-ttu-id="cd00c-180">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="cd00c-180">Required</span></span>

[<span data-ttu-id="cd00c-181">**Inicialización**</span><span class="sxs-lookup"><span data-stu-id="cd00c-181">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[<span data-ttu-id="cd00c-182">**SetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="cd00c-182">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[<span data-ttu-id="cd00c-183">**SetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="cd00c-183">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[<span data-ttu-id="cd00c-184">**SetSize**</span><span class="sxs-lookup"><span data-stu-id="cd00c-184">**SetSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize)

[<span data-ttu-id="cd00c-185">**SetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="cd00c-185">**SetPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat)

[<span data-ttu-id="cd00c-186">**SetResolution**</span><span class="sxs-lookup"><span data-stu-id="cd00c-186">**SetResolution**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)

[<span data-ttu-id="cd00c-187">**WritePixels**</span><span class="sxs-lookup"><span data-stu-id="cd00c-187">**WritePixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)

[<span data-ttu-id="cd00c-188">**WriteSource**</span><span class="sxs-lookup"><span data-stu-id="cd00c-188">**WriteSource**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)

[<span data-ttu-id="cd00c-189">**Promete**</span><span class="sxs-lookup"><span data-stu-id="cd00c-189">**Commit**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

<span data-ttu-id="cd00c-190">Opcionales</span><span class="sxs-lookup"><span data-stu-id="cd00c-190">Optional</span></span>

<span data-ttu-id="cd00c-191">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹</span><span class="sxs-lookup"><span data-stu-id="cd00c-191">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹</span></span>

[<span data-ttu-id="cd00c-192">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="cd00c-192">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)



 

<span data-ttu-id="cd00c-193">¹ se requiere aquí o en la clase de codificación de nivel de contenedor, en función del lugar en el que el formato de archivo de imagen almacena las miniaturas.</span><span class="sxs-lookup"><span data-stu-id="cd00c-193">¹Required either here, or on the container-level encode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="cd00c-194">Si se implementa aquí, se requiere un [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) correspondiente en la clase de descodificación en el nivel de marco.</span><span class="sxs-lookup"><span data-stu-id="cd00c-194">If implemented here, then a corresponding [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) is required on the frame-level decode class.</span></span>

[<span data-ttu-id="cd00c-195">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="cd00c-195">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



<span data-ttu-id="cd00c-196">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="cd00c-196">Required</span></span>

[<span data-ttu-id="cd00c-197">**InitializeFromBlockReader**</span><span class="sxs-lookup"><span data-stu-id="cd00c-197">**InitializeFromBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader)

[<span data-ttu-id="cd00c-198">**AddWriter**</span><span class="sxs-lookup"><span data-stu-id="cd00c-198">**AddWriter**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter)

[<span data-ttu-id="cd00c-199">**GetWriterByIndex**</span><span class="sxs-lookup"><span data-stu-id="cd00c-199">**GetWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex)

[<span data-ttu-id="cd00c-200">**SetWriterByIndex**</span><span class="sxs-lookup"><span data-stu-id="cd00c-200">**SetWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex)

[<span data-ttu-id="cd00c-201">**RemoveWriterByIndex**</span><span class="sxs-lookup"><span data-stu-id="cd00c-201">**RemoveWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex)



 

## <a name="related-topics"></a><span data-ttu-id="cd00c-202">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cd00c-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="cd00c-203">**Vista**</span><span class="sxs-lookup"><span data-stu-id="cd00c-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cd00c-204">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="cd00c-204">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="cd00c-205">Instrucciones de WIC para formatos de imagen RAW de cámara</span><span class="sxs-lookup"><span data-stu-id="cd00c-205">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="cd00c-206">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="cd00c-206">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
