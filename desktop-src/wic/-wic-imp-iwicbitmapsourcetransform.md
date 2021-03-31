---
description: Implementación de IWICBitmapSourceTransform
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: Implementación de IWICBitmapSourceTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0809e1e56fe3c05c8803bb70106c4a24a466eafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361036"
---
# <a name="implementing-iwicbitmapsourcetransform"></a><span data-ttu-id="7f792-103">Implementación de IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="7f792-103">Implementing IWICBitmapSourceTransform</span></span>

## <a name="iwicbitmapsourcetransform"></a><span data-ttu-id="7f792-104">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="7f792-104">IWICBitmapSourceTransform</span></span>

<span data-ttu-id="7f792-105">Aunque es opcional, se recomienda encarecidamente que cada descodificador implemente esta interfaz en la clase de descodificación de nivel de marco, ya que puede proporcionar ventajas de rendimiento importantes.</span><span class="sxs-lookup"><span data-stu-id="7f792-105">Though optional, we highly recommend that every decoder implement this interface on your frame-level decoding class, because it can provide major performance benefits.</span></span> <span data-ttu-id="7f792-106">Cuando una aplicación solicita una región específica de interés, tamaño, orientación o formato de píxeles, en lugar de simplemente descodificar toda la imagen a resolución completa y, a continuación, aplicar las transformaciones solicitadas, Windows Imaging Component (WIC) llama a [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para esta interfaz en el objeto [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="7f792-106">When an application requests a specific region of interest, size, orientation, or pixel format, instead of just decoding the whole image at full resolution and then applying the requested transforms, Windows Imaging Component (WIC) calls [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for this interface on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span> <span data-ttu-id="7f792-107">Si el descodificador de fotogramas lo admite, WIC llama al método o métodos adecuados para determinar si el descodificador de fotogramas puede realizar la transformación solicitada o determinar el tamaño o el formato de píxel más cercano que el descodificador puede proporcionar al solicitado.</span><span class="sxs-lookup"><span data-stu-id="7f792-107">If the frame decoder supports it, WIC calls the appropriate method or methods to determine whether the frame decoder can perform the requested transform or determine the closest size or pixel format the decoder can provide to the one requested.</span></span> <span data-ttu-id="7f792-108">Si el descodificador puede realizar la transformación o transformaciones solicitadas, WIC invoca [**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) con los parámetros adecuados.</span><span class="sxs-lookup"><span data-stu-id="7f792-108">If the decoder can perform the requested transform or transforms, WIC invokes [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) with the appropriate parameters.</span></span> <span data-ttu-id="7f792-109">Si el descodificador puede realizar algunas, pero no todas las transformaciones solicitadas, WIC pide al descodificador que realice las transformaciones que se pueden realizar y usa los objetos de transformación de WIC ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)y [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) para realizar las transformaciones restantes que el descodificador de marcos no pudo realizar en el resultado de la llamada de **copyPixels** .</span><span class="sxs-lookup"><span data-stu-id="7f792-109">If the decoder can perform some, but not all of the requested transforms, WIC asks the decoder to perform those that it can, and uses the WIC transform objects ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator), and [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) to perform the remaining transforms that could not be performed by the frame decoder on the result of the **CopyPixels** call.</span></span> <span data-ttu-id="7f792-110">Si el descodificador no admite [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), WIC debe utilizar los objetos de transformación para realizar todas las transformaciones.</span><span class="sxs-lookup"><span data-stu-id="7f792-110">If the decoder doesn’t support [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), then WIC must use the transform objects to perform all of the transforms.</span></span> <span data-ttu-id="7f792-111">Normalmente, es mucho más eficaz para el descodificador realizar transformaciones durante el proceso de descodificación que descodificar toda la imagen y, a continuación, realizar las transformaciones.</span><span class="sxs-lookup"><span data-stu-id="7f792-111">It’s usually much more efficient for the decoder to perform transforms during the decoding process than it is to decode the entire image and then perform the transforms.</span></span> <span data-ttu-id="7f792-112">Esto es especialmente cierto para las operaciones como el escalado a un tamaño mucho menor o a las conversiones de formato de píxel.</span><span class="sxs-lookup"><span data-stu-id="7f792-112">This is especially true for operations such as scaling to a much smaller size or pixel format conversions.</span></span>


```C++
interface IWICBitmapSourceTransform : IUnknown
{
   // Required methods
   HRESULT DoesSupportTransform ( WICTransformOptions dstTransform,
              BOOL *pfIsSupported);
   HRESULT CopyPixels ( WICRect *prcSrc, 
      UINT uiWidth, 
      UINT uiHeight,
      WICPixelFormatGUID * pguidDstFormat,
      WICBitmapTransformOptions dstTransform, 
      UINT nStride, 
      UINT cbBufferSize, 
      BYTE *pbBuffer );

   // Optional methods
   HRESULT GetClosestSize ( UINT *puiWidth,
              UINT *puiHeight);
   HRESULT GetClosestPixelFormat ( WICPixelFormatGUID *pguidDstFormat);
}
```



-   [<span data-ttu-id="7f792-113">DoesSupportTransform</span><span class="sxs-lookup"><span data-stu-id="7f792-113">DoesSupportTransform</span></span>](#doessupporttransform)
-   [<span data-ttu-id="7f792-114">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="7f792-114">CopyPixels</span></span>](#copypixels)
-   [<span data-ttu-id="7f792-115">GetClosestSize</span><span class="sxs-lookup"><span data-stu-id="7f792-115">GetClosestSize</span></span>](#getclosestsize)
-   [<span data-ttu-id="7f792-116">GetClosestPixelFormat</span><span class="sxs-lookup"><span data-stu-id="7f792-116">GetClosestPixelFormat</span></span>](#getclosestpixelformat)

### <a name="doessupporttransform"></a><span data-ttu-id="7f792-117">DoesSupportTransform</span><span class="sxs-lookup"><span data-stu-id="7f792-117">DoesSupportTransform</span></span>

<span data-ttu-id="7f792-118">[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) pregunta si el descodificador admite la rotación solicitada o la operación de volteo.</span><span class="sxs-lookup"><span data-stu-id="7f792-118">[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) asks whether the decoder supports the requested rotation or flipping operation.</span></span> <span data-ttu-id="7f792-119">Los [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) que se pueden solicitar son:</span><span class="sxs-lookup"><span data-stu-id="7f792-119">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) that may be requested are:</span></span>


```C++
enum WICBitmapTransformOptions
{   
   WICBitmapTransformRotate0,
   WICBitmapTransformRotate90,
   WICBitmapTransformRotate180,
   WICBitmapTransformRotate270,
   WICBitmapTransformFlipHorizontal,
   WICBitmapTransformFlipVertical
}
```



### <a name="copypixels"></a><span data-ttu-id="7f792-120">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="7f792-120">CopyPixels</span></span>

<span data-ttu-id="7f792-121">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) realiza el trabajo real de descodificar los bits de imagen, como el método [**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) en la interfaz [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , pero el método [**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) en [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) es mucho más eficaz y puede mejorar significativamente el rendimiento del procesamiento de imágenes.</span><span class="sxs-lookup"><span data-stu-id="7f792-121">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) performs the actual work of decoding the image bits, such as the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method on the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) interface, but the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) method on [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) is much more powerful, and can improve image processing performance significantly.</span></span>

<span data-ttu-id="7f792-122">Cuando se solicitan varias operaciones de transformación, el resultado depende del orden en el que se realizan las operaciones.</span><span class="sxs-lookup"><span data-stu-id="7f792-122">When multiple transform operations are requested, the result is dependent on the order in which the operations are performed.</span></span> <span data-ttu-id="7f792-123">Para garantizar la previsibilidad y la coherencia entre los códecs, es importante que todos los códecs realicen estas operaciones en el mismo orden.</span><span class="sxs-lookup"><span data-stu-id="7f792-123">To ensure predictability and consistency across codecs, it’s important that all codecs perform these operations in the same order.</span></span> <span data-ttu-id="7f792-124">Este es el orden canónico para realizar estas operaciones.</span><span class="sxs-lookup"><span data-stu-id="7f792-124">This is the canonical order for performing these operations.</span></span>

1.  <span data-ttu-id="7f792-125">Escala</span><span class="sxs-lookup"><span data-stu-id="7f792-125">Scale</span></span>
2.  <span data-ttu-id="7f792-126">Recortar</span><span class="sxs-lookup"><span data-stu-id="7f792-126">Crop</span></span>
3.  <span data-ttu-id="7f792-127">Girar</span><span class="sxs-lookup"><span data-stu-id="7f792-127">Rotate</span></span>

<span data-ttu-id="7f792-128">La conversión de formato de píxeles se puede realizar en cualquier momento, ya que no tiene ningún efecto en las otras transformaciones.</span><span class="sxs-lookup"><span data-stu-id="7f792-128">Pixel format conversion can be performed at any time, because it has no effect on the other transforms.</span></span>

<span data-ttu-id="7f792-129">El primer parámetro, *prcSrc*, se usa para especificar la región de interés para recortar la imagen.</span><span class="sxs-lookup"><span data-stu-id="7f792-129">The first parameter, *prcSrc*, is used to specify the region of interest for clipping the image.</span></span> <span data-ttu-id="7f792-130">Dado que el escalado se realiza antes del recorte por Convención, si la imagen se va a escalar y recortar, la región de interés debe determinarse después de que la imagen se haya escalado.</span><span class="sxs-lookup"><span data-stu-id="7f792-130">Because scaling is performed before clipping by convention, if the image is to be scaled as well as clipped, the region of interest should be determined after the image has been scaled.</span></span>

<span data-ttu-id="7f792-131">Los parámetros segundo y tercero indican el tamaño al que se va a escalar la imagen.</span><span class="sxs-lookup"><span data-stu-id="7f792-131">The second and third parameters indicate the size to which to scale the image.</span></span>

<span data-ttu-id="7f792-132">El parámetro *pguidDstFormat* indica el formato de píxel solicitado para la imagen descodificada.</span><span class="sxs-lookup"><span data-stu-id="7f792-132">The *pguidDstFormat* parameter indicates the requested pixel format for the decoded image.</span></span> <span data-ttu-id="7f792-133">Dado que WIC ya ha llamado a [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), debe ser un formato de píxel que el descodificador haya indicado que admite.</span><span class="sxs-lookup"><span data-stu-id="7f792-133">Because WIC has already called [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), this should be a pixel format that the decoder has indicated that it supports.</span></span>

<span data-ttu-id="7f792-134">El parámetro *dstTransform* indica el ángulo de giro solicitado y si se va a voltear la imagen verticalmente, horizontalmente o ambos.</span><span class="sxs-lookup"><span data-stu-id="7f792-134">The *dstTransform* parameter indicates the requested rotation angle, and whether to flip the image vertically, horizontally, or both.</span></span> <span data-ttu-id="7f792-135">De nuevo, dado que WIC ya habrá llamado a [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), la transformación solicitada debe ser una que el descodificador ya haya indicado que admite.</span><span class="sxs-lookup"><span data-stu-id="7f792-135">Again, because WIC will have already called [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), the requested transform should be one that the decoder has already indicated that it supports.</span></span> <span data-ttu-id="7f792-136">Recuerde que el giro siempre debe realizarse después de ajustar el tamaño y el recorte.</span><span class="sxs-lookup"><span data-stu-id="7f792-136">Remember that rotation should always be performed after scaling and clipping.</span></span>

### <a name="getclosestsize"></a><span data-ttu-id="7f792-137">GetClosestSize</span><span class="sxs-lookup"><span data-stu-id="7f792-137">GetClosestSize</span></span>

<span data-ttu-id="7f792-138">[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) toma dos parámetros in/out.</span><span class="sxs-lookup"><span data-stu-id="7f792-138">[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) takes two in/out parameters.</span></span> <span data-ttu-id="7f792-139">El autor de la llamada utiliza los parámetros *puiWidth* y *puiHeight* para especificar el tamaño en el que el llamador prefiere la descodificación de la imagen.</span><span class="sxs-lookup"><span data-stu-id="7f792-139">The caller uses the *puiWidth* and *puiHeight* parameters to specify the size at which that the caller prefers the image to be decoded.</span></span> <span data-ttu-id="7f792-140">Sin embargo, un descodificador puede descodificar una imagen solo en un tamaño que es múltiplo de su tamaño DCT y distintos formatos de imagen pueden tener distintos tamaños DCT.</span><span class="sxs-lookup"><span data-stu-id="7f792-140">However, a decoder can decode an image only to a size that’s a multiple of its DCT size, and different image formats can have different DCT sizes.</span></span> <span data-ttu-id="7f792-141">El descodificador debe determinar, en función de su propio tamaño DCT, el más cercano puede ser el tamaño solicitado y establecer *puiWidth* y *puiHeight* en esas dimensiones en la devolución.</span><span class="sxs-lookup"><span data-stu-id="7f792-141">The decoder should determine, based on its own DCT size, the closest it can come to the requested size, and set the *puiWidth* and *puiHeight* to those dimensions on return.</span></span> <span data-ttu-id="7f792-142">Si se solicita un tamaño mayor, pero el códec no admite el escalado, se debe devolver el original.</span><span class="sxs-lookup"><span data-stu-id="7f792-142">If a larger size is requested, but the codec doesn’t support upscaling, the original should be returned.</span></span>

### <a name="getclosestpixelformat"></a><span data-ttu-id="7f792-143">GetClosestPixelFormat</span><span class="sxs-lookup"><span data-stu-id="7f792-143">GetClosestPixelFormat</span></span>

<span data-ttu-id="7f792-144">[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) se usa para determinar el formato de píxel más cercano al formato de píxel solicitado que el descodificador puede proporcionar sin pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="7f792-144">[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) is used to determine the closest pixel format to the requested pixel format that the decoder can provide without loss of data.</span></span> <span data-ttu-id="7f792-145">Siempre es preferible convertir a un formato de píxel más ancho que un más estrecho, aunque aumente el tamaño de la imagen, ya que siempre se puede volver a convertir a un formato más restrictivo si es necesario.</span><span class="sxs-lookup"><span data-stu-id="7f792-145">It’s always preferable to convert to a wider pixel format than a narrower one, even though it will increase the size of the image, because it can always be reconverted to a more restrictive format if necessary.</span></span> <span data-ttu-id="7f792-146">Sin embargo, después de que se pierdan los datos, no se pueden recuperar.</span><span class="sxs-lookup"><span data-stu-id="7f792-146">However, after the data is lost, it can’t be recovered.</span></span>

## <a name="continued-reading"></a><span data-ttu-id="7f792-147">Lectura continua</span><span class="sxs-lookup"><span data-stu-id="7f792-147">Continued Reading</span></span>

<span data-ttu-id="7f792-148">Para obtener más información sobre cómo crear un códec habilitado para WIC, consulte [implementación de IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).</span><span class="sxs-lookup"><span data-stu-id="7f792-148">To learn more about how to create a WIC-enabled codec, see [Implementing IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f792-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7f792-149">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7f792-150">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="7f792-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7f792-151">**IWICBitmapSourceTransform**</span><span class="sxs-lookup"><span data-stu-id="7f792-151">**IWICBitmapSourceTransform**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[<span data-ttu-id="7f792-152">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="7f792-152">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

<span data-ttu-id="7f792-153">**Vista**</span><span class="sxs-lookup"><span data-stu-id="7f792-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7f792-154">Implementar IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="7f792-154">Implementing IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[<span data-ttu-id="7f792-155">Implementación de IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="7f792-155">Implementing IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[<span data-ttu-id="7f792-156">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="7f792-156">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="7f792-157">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="7f792-157">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
