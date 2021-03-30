---
description: Implementar IWICBitmapDecoder
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: Implementar IWICBitmapDecoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b31bca377828606fe1beb68d6f1d95d290e01407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082721"
---
# <a name="implementing-iwicbitmapdecoder"></a><span data-ttu-id="ae1ea-103">Implementar IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="ae1ea-103">Implementing IWICBitmapDecoder</span></span>

## <a name="iwicbitmapdecoder"></a><span data-ttu-id="ae1ea-104">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="ae1ea-104">IWICBitmapDecoder</span></span>

<span data-ttu-id="ae1ea-105">Cuando una aplicación solicita un descodificador, el primer punto de interacción con el códec se realiza a través de la interfaz [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="ae1ea-105">When an application requests a decoder, the first point of interaction with the codec is through the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface.</span></span> <span data-ttu-id="ae1ea-106">Esta es la interfaz de nivel de contenedor que proporciona acceso a las propiedades de nivel superior del contenedor y, lo que es más importante, los fotogramas que contiene.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-106">This is the container-level interface that provides access to the top-level properties of the container and, most importantly, the frames it contains.</span></span> <span data-ttu-id="ae1ea-107">Esta es la interfaz principal de la clase descodificador de nivel de contenedor.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-107">This is the primary interface on your container-level decoder class.</span></span>

``` syntax
interface IWICBitmapDecoder : IUnknown
{
// Required methods
   HRESULT QueryCapability (IStream *pIStream, 
      DWORD *pdwCapabilities );
   HRESULT Initialize ( IStream *pIStream,
      WICDecodeOptions cacheOptions );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetDecoderInfo ( IWICBitmapDecoderInfo **pIDecoderInfo );
   HRESULT GetFrameCount ( UINT *pCount );
   HRESULT GetFrame ( UINT index, 
      IWICBitmapFrameDecode **ppIBitmapFrame );

// Optional methods
   HRESULT GetPreview ( IWICBitmapSource **ppIPreview );
   HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
   HRESULT GetColorContexts ( UINT cCount, 
      IWICColorContext **ppIColorContexts, 
      UINT *pcActualCount );
   HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader);
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

<span data-ttu-id="ae1ea-108">Algunos formatos de imagen tienen miniaturas globales, contextos de color o metadatos, mientras que muchos formatos de imagen solo los proporcionan en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-108">Some image formats have global thumbnails, color contexts, or metadata, while many image formats provide these only on a per-frame basis.</span></span> <span data-ttu-id="ae1ea-109">Los métodos para tener acceso a estos elementos son opcionales en [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), pero son necesarios en [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span><span class="sxs-lookup"><span data-stu-id="ae1ea-109">The methods for accessing these items are optional on [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), but are required on [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span></span> <span data-ttu-id="ae1ea-110">Del mismo modo, algunos códecs no usan formatos de píxeles indizados, por lo que no es necesario implementar los métodos [CopyPalette](-wic-imp-iwicbitmapframedecode.md) en ninguna de las interfaces.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-110">Likewise, some codecs do not use indexed pixel formats and so do not need to implement the [CopyPalette](-wic-imp-iwicbitmapframedecode.md) methods on either interface.</span></span> <span data-ttu-id="ae1ea-111">Para obtener más información sobre los métodos **IWICBitmapDecoder** opcionales, vea [implementar IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), donde se implementan con mayor frecuencia.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-111">For more information on the optional **IWICBitmapDecoder** methods, see [Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), where they are most commonly implemented.</span></span>

### <a name="querycapability"></a><span data-ttu-id="ae1ea-112">QueryCapability</span><span class="sxs-lookup"><span data-stu-id="ae1ea-112">QueryCapability</span></span>

<span data-ttu-id="ae1ea-113">[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) es el método que se usa para el arbitraje del códec.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-113">[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) is the method used for codec arbitration.</span></span> <span data-ttu-id="ae1ea-114">(Consulte [detección y arbitraje](-wic-howwicworks.md) en el tema [Cómo funciona el componente de creación de imágenes de Windows](-wic-howwicworks.md) ).</span><span class="sxs-lookup"><span data-stu-id="ae1ea-114">(See [Discovery and Arbitration](-wic-howwicworks.md) in the [How The Windows Imaging Component Works](-wic-howwicworks.md) topic).</span></span> <span data-ttu-id="ae1ea-115">Si dos códecs pueden descodificar el mismo formato de imagen o si se produce una colisión de patrón en la que dos códecs usan el mismo patrón de identificación, este método le permite seleccionar el códec que puede controlar mejor cualquier imagen específica.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-115">If two codecs are capable of decoding the same image format, or if a pattern collision occurs in which two codecs use the same identifying pattern, this method allows you to select the codec that can best handle any specific image.</span></span>

<span data-ttu-id="ae1ea-116">Al invocar este método, el componente de creación de imágenes de Windows (WIC) le pasa la secuencia real que contiene la imagen.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-116">When invoking this method, Windows Imaging Component (WIC) passes you the actual stream containing the image.</span></span> <span data-ttu-id="ae1ea-117">Debe comprobar si puede descodificar cada fotograma de la imagen y enumerar los bloques de metadatos para declarar con precisión qué funcionalidades tiene este descodificador con respecto al flujo de archivo específico que se le ha pasado.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-117">You must verify whether you can decode each frame within the image and enumerate through the metadata blocks, to accurately declare what capabilities this decoder has with respect to the specific file stream passed to it.</span></span> <span data-ttu-id="ae1ea-118">Esto es importante para todos los descodificadores, pero especialmente importante para los formatos de imagen basados en contenedores Tagged Image File Format (TIFF).</span><span class="sxs-lookup"><span data-stu-id="ae1ea-118">This is important for all decoders, but particularly important for image formats based on Tagged Image File Format (TIFF) containers.</span></span> <span data-ttu-id="ae1ea-119">El proceso de detección funciona mediante patrones coincidentes asociados con los descodificadores en el registro con los patrones del archivo de imagen real.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-119">The discovery process works by matching patterns associated with decoders in the registry to patterns in the actual image file.</span></span> <span data-ttu-id="ae1ea-120">Declarar el patrón de identificación en el registro garantiza que el descodificador siempre se detectará para las imágenes en el formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-120">Declaring your identifying pattern in the registry guarantees that your decoder will always be detected for images in your image format.</span></span> <span data-ttu-id="ae1ea-121">Sin embargo, el descodificador todavía podría detectarse para imágenes en otros formatos.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-121">However, your decoder could still be detected for images in other formats.</span></span> <span data-ttu-id="ae1ea-122">Por ejemplo, todos los contenedores TIFF incluyen el patrón TIFF, que es un patrón de identificación válido para el formato de imagen TIFF.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-122">For example, all TIFF containers include the TIFF pattern, which is a valid identifying pattern for the TIFF image format.</span></span> <span data-ttu-id="ae1ea-123">Esto significa que, durante la detección, se encontrarán al menos dos patrones de identificación en los archivos de imagen para cualquier formato de imagen que se base en un contenedor de estilo TIFF.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-123">This means that, during discovery, at least two identifying patterns will be found in image files for any image format that’s based on a TIFF-style container.</span></span> <span data-ttu-id="ae1ea-124">Uno será el patrón TIFF y el otro será el patrón de formato de imagen real.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-124">One will be the TIFF pattern and the other will be the actual image format pattern.</span></span> <span data-ttu-id="ae1ea-125">Aunque es menos probable, también podría haber colisiones de patrón entre otros formatos de imagen no relacionados.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-125">While less likely, there could be pattern collisions between other unrelated image formats as well.</span></span> <span data-ttu-id="ae1ea-126">Este es el motivo por el que la detección y el arbitraje son un proceso de dos fases.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-126">This is why discovery and arbitration is a two-stage process.</span></span> <span data-ttu-id="ae1ea-127">Compruebe siempre que el flujo de imagen pasado a [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) es realmente una instancia válida de su propio formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-127">Always verify that the image stream passed to [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) is actually a valid instance of your own image format.</span></span> <span data-ttu-id="ae1ea-128">Además, si el códec descodifica un formato de imagen para el que no posee la especificación, la implementación de **QueryCapability** debe comprobar la presencia de cualquier característica que pueda ser válida en la especificación de formato de imagen que el códec no implementa.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-128">Also, if your codec decodes an image format for which you don’t own the specification, your **QueryCapability** implementation should check for the presence of any feature that may be valid under the image format specification that your codec doesn’t implement.</span></span> <span data-ttu-id="ae1ea-129">Esto garantizará que los usuarios no experimenten errores de descodificación innecesarios u obtengan resultados inesperados con el códec.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-129">This will ensure that users do not experience unnecessary decoding failures or get unexpected results with your codec.</span></span>

<span data-ttu-id="ae1ea-130">Antes de realizar cualquier operación en la imagen, debe guardar la posición actual de la secuencia, por lo que puede restaurarla a su posición original antes de volver del método.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-130">Before performing any operation on the image, you must save the current position of the stream, so you can restore it to its original position before returning from the method.</span></span> <span data-ttu-id="ae1ea-131">La enumeración [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) que especifica las capacidades se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="ae1ea-131">The [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) enumeration that specifies the capabilities is defined as follows:</span></span>

``` syntax
enum WICBitmapDecoderCapabilities
{   
   WICBitmapDecoderCapabilitySameEncoder,
   WICBitmapDecoderCapabilityCanDecodeAllImages,
   WICBitmapDecoderCapabilityCanDecodeSomeImages,
   WICBitmapDecoderCapabilityCanEnumerateMetadata,
   WICBitmapDecoderCapabilityCanDecodeThumbnail
}
```

<span data-ttu-id="ae1ea-132">Solo debe declarar **WICBitmapDecoderCapabilitySameEncoder** si su codificador era el que codifica la imagen.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-132">You should declare **WICBitmapDecoderCapabilitySameEncoder** only if your encoder was the one that encoded the image.</span></span> <span data-ttu-id="ae1ea-133">Después de comprobar si puede descodificar cada fotograma del contenedor, declare **WICBitmapDecoderCapabilityCanDecodeSomeImages** si puede descodificar algunos, pero no todos, **WICBitmapDecoderCapabilityCanDecodeAllImages** si puede descodificar todos los fotogramas, o ninguno si no puede descodificar ninguno de ellos.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-133">After verifying whether you can decode each frame in the container, declare either **WICBitmapDecoderCapabilityCanDecodeSomeImages** if you can decode some but not all of the frames, **WICBitmapDecoderCapabilityCanDecodeAllImages** if you can decode all of the frames, or neither if you cannot decode any of them.</span></span> <span data-ttu-id="ae1ea-134">(Estas dos enumeraciones son mutuamente excluyentes; si devuelve **WICBitmapDecoderCapabilityCanDecodeAllImages**, **WICBitmapDecoderCapabilityCanDecodeSomeImages** se omitirá). Declare **WICBitmapDecoderCapabilityCanEnumerateMetadata** después de comprobar que puede enumerar los bloques de metadatos en el contenedor de imágenes.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-134">(These two enums are mutually exclusive; if you return **WICBitmapDecoderCapabilityCanDecodeAllImages**, **WICBitmapDecoderCapabilityCanDecodeSomeImages** will be ignored.) Declare **WICBitmapDecoderCapabilityCanEnumerateMetadata** after verifying that you can enumerate through the metadata blocks in the image container.</span></span> <span data-ttu-id="ae1ea-135">No tiene que buscar una miniatura en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-135">You don’t have to check for a thumbnail in every frame.</span></span> <span data-ttu-id="ae1ea-136">Si hay una miniatura global y puede descodificarla, puede declarar **WICBitmapDecoderCapabilityCanDecodeThumbnail**.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-136">If there is a global thumbnail and you can decode it, you can declare **WICBitmapDecoderCapabilityCanDecodeThumbnail**.</span></span> <span data-ttu-id="ae1ea-137">Si no hay ninguna miniatura global, intente descodificar la miniatura del fotograma 0.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-137">If there is no global thumbnail, then attempt to decode the thumbnail for Frame 0.</span></span> <span data-ttu-id="ae1ea-138">Si no hay ninguna miniatura en ninguno de estos lugares, no declare esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-138">If there is no thumbnail in either of these places, do not declare this capability.</span></span>

<span data-ttu-id="ae1ea-139">Después de determinar las capacidades del descodificador con respecto al flujo de imagen pasado a este método, realice una operación OR con el [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) que ha comprobado que este descodificador puede realizar en esta imagen y devuelva el resultado.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-139">After determining the capabilities of the decoder with respect to the image stream passed to this method, perform an OR operation with the [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) you have verified that this decoder can perform on this image, and return the result.</span></span> <span data-ttu-id="ae1ea-140">Recuerde restaurar el flujo a su posición original antes de volver.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-140">Remember to restore the stream to its original position before returning.</span></span>

### <a name="initialize"></a><span data-ttu-id="ae1ea-141">Inicialización</span><span class="sxs-lookup"><span data-stu-id="ae1ea-141">Initialize</span></span>

<span data-ttu-id="ae1ea-142">Una aplicación invoca la [**inicialización**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) una vez que se ha seleccionado un descodificador para descodificar una imagen específica.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-142">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) is invoked by an application after a decoder has been selected to decode a specific image.</span></span> <span data-ttu-id="ae1ea-143">La secuencia de imágenes se pasa al descodificador y un llamador puede especificar opcionalmente la opción de caché [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) para tratar con los metadatos del archivo.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-143">The image stream is passed to the decoder, and a caller may optionally specify the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) cache option for dealing with the metadata in the file.</span></span>

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

<span data-ttu-id="ae1ea-144">Algunas aplicaciones usan metadatos más que otras.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-144">Some applications use metadata more than others.</span></span> <span data-ttu-id="ae1ea-145">La mayoría de las aplicaciones no necesitan tener acceso a todos los metadatos de un archivo de imagen y solicitarán metadatos específicos a medida que lo necesiten.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-145">Most applications don’t need to access all the metadata in an image file, and will request specific metadata as they need it.</span></span> <span data-ttu-id="ae1ea-146">En lugar de ello, otras aplicaciones almacenarán en caché todos los metadatos antes de que mantener la secuencia de archivos abierta y realizar la e/s de disco cada vez que necesiten tener acceso a los metadatos.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-146">Other applications would rather cache all the metadata up front than keep the file stream open and perform disk I/O every time they need to access metadata.</span></span> <span data-ttu-id="ae1ea-147">Si el autor de la llamada no especifica una opción de caché de metadatos, el comportamiento de almacenamiento en caché predeterminado debe ser caché a petición.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-147">If the caller doesn’t specify a metadata cache option, the default caching behavior should be cache on demand.</span></span> <span data-ttu-id="ae1ea-148">Esto significa que no se deben cargar metadatos en memoria hasta que la aplicación realice una solicitud específica para esos metadatos.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-148">This means no metadata should be loaded into memory until the application makes a specific request for that metadata.</span></span> <span data-ttu-id="ae1ea-149">Si la aplicación especifica **WICDecodeMetadataCacheOnLoad**, los metadatos se deben cargar en memoria de inmediato y almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-149">If the application specifies **WICDecodeMetadataCacheOnLoad**, the metadata should be loaded in memory immediately and cached.</span></span> <span data-ttu-id="ae1ea-150">Cuando los metadatos se almacenan en la memoria caché durante la carga, la secuencia de archivos se puede liberar una vez que los metadatos se han almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-150">When metadata is cached on load, the file stream may be released after the metadata has been cached.</span></span>

### <a name="getcontainerformat"></a><span data-ttu-id="ae1ea-151">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="ae1ea-151">GetContainerFormat</span></span>

<span data-ttu-id="ae1ea-152">Para implementar [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), solo tiene que devolver el GUID del formato de imagen de la imagen para la que se crea una instancia del descodificador.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-152">To implement [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), just return the GUID of the image format of the image for which the decoder is instantiated.</span></span> <span data-ttu-id="ae1ea-153">Este método también se implementa en [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) y [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span><span class="sxs-lookup"><span data-stu-id="ae1ea-153">This method is also implemented on [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) and [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span></span>

### <a name="getdecoderinfo"></a><span data-ttu-id="ae1ea-154">GetDecoderInfo</span><span class="sxs-lookup"><span data-stu-id="ae1ea-154">GetDecoderInfo</span></span>

<span data-ttu-id="ae1ea-155">[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) devuelve un objeto [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) .</span><span class="sxs-lookup"><span data-stu-id="ae1ea-155">[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) returns an [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) object.</span></span> <span data-ttu-id="ae1ea-156">Para obtener el objeto **IWICBitmapDecoderInfo** , solo tiene que pasar el GUID del descodificador al método [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) en [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)y, a continuación, solicitar la interfaz **IWICBitmapDecoderInfo** en él, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-156">To get the **IWICBitmapDecoderInfo** object, just pass the GUID of your decoder to the [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) method on [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), and then request the **IWICBitmapDecoderInfo** interface on it, as shown in the following example.</span></span>


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a><span data-ttu-id="ae1ea-157">GetFrameCount</span><span class="sxs-lookup"><span data-stu-id="ae1ea-157">GetFrameCount</span></span>

<span data-ttu-id="ae1ea-158">[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) simplemente devuelve el número de marcos del contenedor.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-158">[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) just returns the number of frames in the container.</span></span> <span data-ttu-id="ae1ea-159">Algunos formatos de contenedor admiten varios marcos y otros solo admiten un marco por contenedor.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-159">Some container formats support multiple frames, and others support only one frame per container.</span></span>

### <a name="getframe"></a><span data-ttu-id="ae1ea-160">GetFrame</span><span class="sxs-lookup"><span data-stu-id="ae1ea-160">GetFrame</span></span>

<span data-ttu-id="ae1ea-161">[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) es un método importante en la interfaz [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) porque el marco contiene los bits de imagen reales y el objeto de descodificador de marco devuelto por este método es el objeto que realiza la descodificación real de la imagen solicitada.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-161">[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) is an important method on the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface because the frame contains the actual image bits, and the frame decoder object returned from this method is the object that does the actual decoding of the requested image.</span></span> <span data-ttu-id="ae1ea-162">Es el otro objeto que debe implementar al escribir un descodificador.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-162">That is the other object you need to implement when writing a decoder.</span></span> <span data-ttu-id="ae1ea-163">Para obtener más información sobre los descodificadores de fotogramas, vea [implementar IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).</span><span class="sxs-lookup"><span data-stu-id="ae1ea-163">For more information on frame decoders, see [Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).</span></span>

### <a name="getpreview"></a><span data-ttu-id="ae1ea-164">GetPreview</span><span class="sxs-lookup"><span data-stu-id="ae1ea-164">GetPreview</span></span>

<span data-ttu-id="ae1ea-165">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) devuelve una vista previa de la imagen.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-165">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) returns a preview of the image.</span></span> <span data-ttu-id="ae1ea-166">Para obtener una explicación detallada de las versiones preliminares, vea el método de [implementación de IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) en la interfaz de [implementación de IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) .</span><span class="sxs-lookup"><span data-stu-id="ae1ea-166">For a detailed discussion of previews, see the [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) method on the [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) interface.</span></span>

<span data-ttu-id="ae1ea-167">Si el formato de imagen contiene una vista previa de JPEG incrustada, se recomienda encarecidamente que, en lugar de escribir un descodificador JPEG, delegue en el descodificador JPEG que se suministra con la plataforma WIC para descodificar vistas previas y vistas en miniatura.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-167">If your image format contains an embedded JPEG preview, it is strongly recommend that, instead of writing a JPEG decoder to decode it, you delegate to the JPEG decoder that ships with the WIC platform for decoding previews and thumbnails.</span></span> <span data-ttu-id="ae1ea-168">Para ello, busque el principio de los datos de la imagen de vista previa en la secuencia e invoque el método [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) en [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="ae1ea-168">To do this, seek to the beginning of the preview image data in the stream and invoke the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method on the [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span>


```C++
IWICBitmapDecoder* pPreviewDecoder = NULL;
IWICBitmapFrameDecode* pPreviewFrame = NULL;
IWICBitmapSource* pPreview = NULL;
HRESULT hr;

hr = m_pImagingFactory->CreateDecoderFromStream(
                               m_pStream, NULL, 
                               WICDecodeMetadataCacheOnDemand, &pPreviewDecoder);
hr = pPreviewDecoder->GetFrame(0, pPreviewFrame);
hr = pPreviewFrame->QueryInterface(IID_IWICBitmapSource, (void**)&pPreview);

```



## <a name="related-topics"></a><span data-ttu-id="ae1ea-169">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae1ea-169">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ae1ea-170">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ae1ea-170">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ae1ea-171">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="ae1ea-171">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="ae1ea-172">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="ae1ea-172">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="ae1ea-173">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ae1ea-173">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ae1ea-174">Interfaces del descodificador</span><span class="sxs-lookup"><span data-stu-id="ae1ea-174">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="ae1ea-175">Implementación de IWICBitmapCodecProgressNotification (descodificador)</span><span class="sxs-lookup"><span data-stu-id="ae1ea-175">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[<span data-ttu-id="ae1ea-176">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="ae1ea-176">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="ae1ea-177">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="ae1ea-177">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



