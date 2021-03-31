---
description: Implementación de IWICBitmapFrameDecode
ms.assetid: 7dc626ad-1158-4b67-8ca7-47b4cf88e278
title: Implementación de IWICBitmapFrameDecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394b5858ec5eee37ef1c7f52b766806c4a0c1a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816094"
---
# <a name="implementing-iwicbitmapframedecode"></a><span data-ttu-id="2e74c-103">Implementación de IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="2e74c-103">Implementing IWICBitmapFrameDecode</span></span>

## <a name="iwicbitmapframedecode"></a><span data-ttu-id="2e74c-104">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="2e74c-104">IWICBitmapFrameDecode</span></span>

<span data-ttu-id="2e74c-105">[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) es la interfaz de nivel de marco que proporciona acceso a los bits de imagen reales.</span><span class="sxs-lookup"><span data-stu-id="2e74c-105">[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) is the frame-level interface that provides access to the actual image bits.</span></span> <span data-ttu-id="2e74c-106">Esta interfaz se implementa en la clase de descodificación de nivel de marco.</span><span class="sxs-lookup"><span data-stu-id="2e74c-106">You implement this interface on your frame-level decoding class.</span></span> <span data-ttu-id="2e74c-107">Dado que se deriva de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), la implementación de **IWICBitmapFrameDecode** incluirá una implementación de los métodos de **IWICBitmapSource** .</span><span class="sxs-lookup"><span data-stu-id="2e74c-107">Because it’s derived from [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), your implementation of **IWICBitmapFrameDecode** will include an implementation of the **IWICBitmapSource** methods.</span></span> <span data-ttu-id="2e74c-108">Los métodos adicionales en **IWICBitmapFrameDecode** proporcionan acceso a la miniatura de nivel de marco, a los contextos de color de la imagen y al lector de consultas de metadatos para el marco.</span><span class="sxs-lookup"><span data-stu-id="2e74c-108">The additional methods on **IWICBitmapFrameDecode** provide access to the frame-level thumbnail, any color contexts for the image, and the metadata query reader for the frame.</span></span>

``` syntax
interface IWICBitmapFrameDecode : IWICBitmapSource
{
// Required methods
HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
HRESULT GetColorContexts ( UINT cCount, 
IWICColorContext **ppIColorContexts, UINT *pcActualCount );
HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader );

// Methods inherited from IWICBitmapSource
HRESULT GetSize ( UINT *puiWidth, UINT *puiHeight );
HRESULT GetPixelFormat ( WICPixelFormatGUID *pPixelFormat );
HRESULT GetResolution ( double *pDpiX, double *pDpiY );
HRESULT CopyPixels ( const WICRect *prc, 
   UINT cbStride,
   UINT cbBufferSize, 
   BYTE *pbBuffer );
// Optional method
HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

-   [<span data-ttu-id="2e74c-109">GetThumbnail</span><span class="sxs-lookup"><span data-stu-id="2e74c-109">GetThumbnail</span></span>](#getthumbnail)
-   [<span data-ttu-id="2e74c-110">GetColorContexts</span><span class="sxs-lookup"><span data-stu-id="2e74c-110">GetColorContexts</span></span>](#getcolorcontexts)
-   [<span data-ttu-id="2e74c-111">GetMetadataQueryReader</span><span class="sxs-lookup"><span data-stu-id="2e74c-111">GetMetadataQueryReader</span></span>](#getmetadataqueryreader)
-   [<span data-ttu-id="2e74c-112">GetPixelFormat, y GetResolution</span><span class="sxs-lookup"><span data-stu-id="2e74c-112">GetSize, GetPixelFormat, and GetResolution</span></span>](#getsize-getpixelformat-and-getresolution)
-   [<span data-ttu-id="2e74c-113">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="2e74c-113">CopyPixels</span></span>](#copypixels)
-   [<span data-ttu-id="2e74c-114">CopyPalette</span><span class="sxs-lookup"><span data-stu-id="2e74c-114">CopyPalette</span></span>](#copypalette)

### <a name="getthumbnail"></a><span data-ttu-id="2e74c-115">GetThumbnail</span><span class="sxs-lookup"><span data-stu-id="2e74c-115">GetThumbnail</span></span>

<span data-ttu-id="2e74c-116">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) devuelve la miniatura del fotograma actual.</span><span class="sxs-lookup"><span data-stu-id="2e74c-116">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) returns the thumbnail for the current frame.</span></span> <span data-ttu-id="2e74c-117">Por motivos de rendimiento, las miniaturas se codifican normalmente en formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="2e74c-117">For performance reasons, thumbnails are most commonly encoded in a JPEG format.</span></span> <span data-ttu-id="2e74c-118">Del mismo modo que con la vista previa en el descodificador, no es necesario ni se recomienda proporcionar su propio descodificador JPEG para las miniaturas.</span><span class="sxs-lookup"><span data-stu-id="2e74c-118">Just as with the Preview on the decoder, it is not necessary or recommended to provide your own JPEG decoder for thumbnails.</span></span> <span data-ttu-id="2e74c-119">En su lugar, debe delegar en el descodificador JPEG proporcionado por el componente de creación de imágenes de Windows (WIC).</span><span class="sxs-lookup"><span data-stu-id="2e74c-119">Instead, you should delegate to the JPEG decoder provided by Windows Imaging Component (WIC).</span></span>

<span data-ttu-id="2e74c-120">Para obtener más información sobre las miniaturas, vea el método [SetThumbnail](-wic-imp-iwicbitmapframeencode.md) en [implementar IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).</span><span class="sxs-lookup"><span data-stu-id="2e74c-120">For more information on thumbnails, see the [SetThumbnail](-wic-imp-iwicbitmapframeencode.md) method on [Implementing IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).</span></span>

### <a name="getcolorcontexts"></a><span data-ttu-id="2e74c-121">GetColorContexts</span><span class="sxs-lookup"><span data-stu-id="2e74c-121">GetColorContexts</span></span>

<span data-ttu-id="2e74c-122">[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) devuelve los contextos de color válidos (también conocidos como perfiles de color) asociados a la imagen de este marco.</span><span class="sxs-lookup"><span data-stu-id="2e74c-122">[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) returns the valid color contexts (also known as color profiles) associated with the image in this frame.</span></span> <span data-ttu-id="2e74c-123">En la mayoría de los casos, esto solo será uno, pero puede haber casos en los que haya dos o, en raras ocasiones, más.</span><span class="sxs-lookup"><span data-stu-id="2e74c-123">In most cases, this will only be one, but there could be cases where there are two or, rarely, more.</span></span> <span data-ttu-id="2e74c-124">El autor de la llamada pasará uno o más objetos [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) , estableciendo el parámetro *enta* para indicar cuántos pasan.</span><span class="sxs-lookup"><span data-stu-id="2e74c-124">The caller will pass in one or more [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects, setting the *cCount* parameter to indicate how many they are passing in.</span></span> <span data-ttu-id="2e74c-125">Este método rellena los objetos **IWICColorContext** con los datos de contexto de color reales de los perfiles de color asociados a la imagen.</span><span class="sxs-lookup"><span data-stu-id="2e74c-125">This method populates the **IWICColorContext** objects with the actual color context data for the color profiles associated with the image.</span></span> <span data-ttu-id="2e74c-126">Establezca el parámetro *pcActualCount* en el número real de contextos de color asociado a la imagen, incluso si es mayor que el número que se puede devolver.</span><span class="sxs-lookup"><span data-stu-id="2e74c-126">Set the *pcActualCount* parameter to the actual number of color contexts associated with the image, even if this is greater than the number you can return.</span></span> <span data-ttu-id="2e74c-127">(En caso de que haya más contextos de color disponibles que el número de objetos **IWICColorContext** pasados por el autor de la llamada, esto indica al llamador que hay uno o más usuarios disponibles).</span><span class="sxs-lookup"><span data-stu-id="2e74c-127">(In the case where more color contexts are available than the number of **IWICColorContext** objects passed in by the caller, this tells the caller there are one or more others available.)</span></span>

### <a name="getmetadataqueryreader"></a><span data-ttu-id="2e74c-128">GetMetadataQueryReader</span><span class="sxs-lookup"><span data-stu-id="2e74c-128">GetMetadataQueryReader</span></span>

<span data-ttu-id="2e74c-129">[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) devuelve un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) que una aplicación puede usar para recuperar metadatos del marco de imagen.</span><span class="sxs-lookup"><span data-stu-id="2e74c-129">[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) returns an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) that an application can use to retrieve metadata from the image frame.</span></span> <span data-ttu-id="2e74c-130">Esta interfaz se implementa mediante un controlador de metadatos y permite que una aplicación consulte propiedades de metadatos específicas pertenecientes a un formato de metadatos determinado.</span><span class="sxs-lookup"><span data-stu-id="2e74c-130">This interface is implemented by a metadata handler, and allows an application to query for specific metadata properties belonging to a particular metadata format.</span></span> <span data-ttu-id="2e74c-131">Para obtener más información, vea [implementar IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).</span><span class="sxs-lookup"><span data-stu-id="2e74c-131">For more information, see [Implementing IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).</span></span>

<span data-ttu-id="2e74c-132">Para crear una instancia de [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), llame a [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) en [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).</span><span class="sxs-lookup"><span data-stu-id="2e74c-132">To instantiate an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), call [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) on the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).</span></span>


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a><span data-ttu-id="2e74c-133">GetPixelFormat, y GetResolution</span><span class="sxs-lookup"><span data-stu-id="2e74c-133">GetSize, GetPixelFormat, and GetResolution</span></span>

<span data-ttu-id="2e74c-134">Se explican por sí solos, [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)y [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) [**, y**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)se devuelven las propiedades solicitadas de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2e74c-134">[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize), [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat), and [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) are self-explanatory, and return the requested properties of the image.</span></span>

### <a name="copypixels"></a><span data-ttu-id="2e74c-135">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="2e74c-135">CopyPixels</span></span>

<span data-ttu-id="2e74c-136">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) es el método al que llama una aplicación cuando desea crear un mapa de bits en memoria que se puede representar en la pantalla o la impresora.</span><span class="sxs-lookup"><span data-stu-id="2e74c-136">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) is the method an application calls when it wants to create a bitmap in memory that can be rendered to the display or printer.</span></span> <span data-ttu-id="2e74c-137">Este es el método que realiza la descodificación real de los bits de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2e74c-137">This is the method that does the actual decoding of the image bits.</span></span> <span data-ttu-id="2e74c-138">Los parámetros son un rectángulo, que representa la región de interés de la imagen de origen que se va a copiar en la memoria; STRIDE, que especifica el número de bytes en una línea de recorrido; tamaño del búfer en memoria asignado por la aplicación; y un puntero al búfer en el que se deben copiar los bits de imagen solicitados.</span><span class="sxs-lookup"><span data-stu-id="2e74c-138">The parameters are a rectangle, which represents the region of interest in the source image to copy into memory; the stride, which specifies the number of bytes in one scan line; the size of the buffer in memory that has been allocated by the application; and a pointer to the buffer into which the requested image bits should be copied.</span></span> <span data-ttu-id="2e74c-139">(Para evitar que las saturaciones de búfer potenciales introduzcan vulnerabilidades de seguridad, asegúrese de copiar solo los datos de imagen en el búfer que especifica el parámetro *cbBufferSize* ).</span><span class="sxs-lookup"><span data-stu-id="2e74c-139">(To prevent potential buffer overruns from introducing security vulnerabilities, be sure to copy only as much image data into the buffer as the *cbBufferSize* parameter specifies.)</span></span>

### <a name="copypalette"></a><span data-ttu-id="2e74c-140">CopyPalette</span><span class="sxs-lookup"><span data-stu-id="2e74c-140">CopyPalette</span></span>

<span data-ttu-id="2e74c-141">Solo los códecs que tienen formatos de píxel indexados deben implementar el método [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="2e74c-141">Only codecs that have indexed pixel formats must implement the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span> <span data-ttu-id="2e74c-142">Si una imagen usa un formato indizado, use este método para devolver la paleta de colores utilizada en la imagen.</span><span class="sxs-lookup"><span data-stu-id="2e74c-142">If an image uses an indexed format, use this method to return the palette of colors used in the image.</span></span> <span data-ttu-id="2e74c-143">Si el códec no tiene un formato indizado, devuelva WINCODEC \_ Err \_ PALETTEUNAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="2e74c-143">If your codec doesn’t have an indexed format, return WINCODEC\_ERR\_PALETTEUNAVAILABLE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e74c-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e74c-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2e74c-145">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="2e74c-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2e74c-146">**IWICBitmapSource**</span><span class="sxs-lookup"><span data-stu-id="2e74c-146">**IWICBitmapSource**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[<span data-ttu-id="2e74c-147">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="2e74c-147">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="2e74c-148">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="2e74c-148">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="2e74c-149">**Vista**</span><span class="sxs-lookup"><span data-stu-id="2e74c-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2e74c-150">Implementación de IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="2e74c-150">Implementing IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[<span data-ttu-id="2e74c-151">Implementar IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="2e74c-151">Implementing IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[<span data-ttu-id="2e74c-152">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="2e74c-152">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="2e74c-153">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="2e74c-153">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



