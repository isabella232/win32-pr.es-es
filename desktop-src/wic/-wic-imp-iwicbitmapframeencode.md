---
description: Implementar IWICBitmapFrameEncode
ms.assetid: 509fa49c-c90d-4270-a338-6ce638ccd89a
title: Implementar IWICBitmapFrameEncode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d2a5ea0412ea4a45ea329618d00443c1755391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278190"
---
# <a name="implementing-iwicbitmapframeencode"></a><span data-ttu-id="ebbca-103">Implementar IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="ebbca-103">Implementing IWICBitmapFrameEncode</span></span>

## <a name="iwicbitmapframeencode"></a><span data-ttu-id="ebbca-104">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="ebbca-104">IWICBitmapFrameEncode</span></span>

<span data-ttu-id="ebbca-105">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) es el homólogo del codificador de la interfaz [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="ebbca-105">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) is the encoder’s counterpart to the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface.</span></span> <span data-ttu-id="ebbca-106">Puede implementar esta interfaz en la clase de codificación de nivel de marco, que es la clase que realiza la codificación real de los bits de imagen para cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="ebbca-106">You can implement this interface on your frame-level encoding class, which is the class that does the actual encoding of the image bits for each frame.</span></span>


```C++
interface IWICBitmapFrameEncode : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IPropertyBag2 *pIEncoderOptions );
   HRESULT SetSize ( UINT width,
               UINT height );
   HRESULT SetResolution ( double dpiX,
               double dpiY );
   HRESULT SetPixelFormat (WICPixelFormatGUID *pPixelFormat);
   HRESULT SetColorContexts ( UINT cCount,
               IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
               **ppIMetadataQueryWriter );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT WritePixels ( UINT lineCount,
               UINT cbStride,
               UINT cbBufferSize,
               BYTE *pbPixels );
   HRESULT WriteSource ( IWICBitmapSource *pIWICBitmapSource,
               WICRect *prc );
   HRESULT Commit ( void );

// Optional method
   HRESULT SetPalette ( IWICPalette *pIPalette );
};
```



-   [<span data-ttu-id="ebbca-107">Inicialización</span><span class="sxs-lookup"><span data-stu-id="ebbca-107">Initialize</span></span>](#initialize)
-   [<span data-ttu-id="ebbca-108">SetSize y SetResolution</span><span class="sxs-lookup"><span data-stu-id="ebbca-108">SetSize and SetResolution</span></span>](#setsize-and-setresolution)
-   [<span data-ttu-id="ebbca-109">SetPixelFormat</span><span class="sxs-lookup"><span data-stu-id="ebbca-109">SetPixelFormat</span></span>](#setpixelformat)
-   [<span data-ttu-id="ebbca-110">SetColorContexts</span><span class="sxs-lookup"><span data-stu-id="ebbca-110">SetColorContexts</span></span>](#setcolorcontexts)
-   [<span data-ttu-id="ebbca-111">GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="ebbca-111">GetMetadataQueryWriter</span></span>](#getmetadataquerywriter)
-   [<span data-ttu-id="ebbca-112">SetThumbnail</span><span class="sxs-lookup"><span data-stu-id="ebbca-112">SetThumbnail</span></span>](#setthumbnail)
-   [<span data-ttu-id="ebbca-113">WritePixels</span><span class="sxs-lookup"><span data-stu-id="ebbca-113">WritePixels</span></span>](#writepixels)
-   [<span data-ttu-id="ebbca-114">WriteSource</span><span class="sxs-lookup"><span data-stu-id="ebbca-114">WriteSource</span></span>](#writesource)
-   [<span data-ttu-id="ebbca-115">Confirmar</span><span class="sxs-lookup"><span data-stu-id="ebbca-115">Commit</span></span>](#commit)
-   [<span data-ttu-id="ebbca-116">SetPalette</span><span class="sxs-lookup"><span data-stu-id="ebbca-116">SetPalette</span></span>](#setpalette)

### <a name="initialize"></a><span data-ttu-id="ebbca-117">Inicialización</span><span class="sxs-lookup"><span data-stu-id="ebbca-117">Initialize</span></span>

<span data-ttu-id="ebbca-118">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) es el primer método invocado en un objeto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) después del que se ha creado una instancia.</span><span class="sxs-lookup"><span data-stu-id="ebbca-118">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) is the first method invoked on an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object after it has been instantiated.</span></span> <span data-ttu-id="ebbca-119">Este método tiene un parámetro, que se puede establecer en **null**.</span><span class="sxs-lookup"><span data-stu-id="ebbca-119">This method has one parameter, which may be set to **NULL**.</span></span> <span data-ttu-id="ebbca-120">Este parámetro representa las opciones del codificador y es la misma instancia de [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que se creó en el método [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) en el descodificador de nivel de contenedor y se devuelve al llamador en el parámetro pIEncoderOptions de ese método.</span><span class="sxs-lookup"><span data-stu-id="ebbca-120">This parameter represents the encoder options, and is the same [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) instance that you created in the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method on the container-level decoder, and passed back to the caller in the pIEncoderOptions parameter of that method.</span></span> <span data-ttu-id="ebbca-121">En ese momento, ha rellenado el struct IPropertyBag2 con propiedades que representan las opciones de codificación que admite el codificador de nivel de marco.</span><span class="sxs-lookup"><span data-stu-id="ebbca-121">At that time, you populated the IPropertyBag2 struct with properties that represent the encoding options supported by your frame-level encoder.</span></span> <span data-ttu-id="ebbca-122">Ahora, el autor de la llamada ha proporcionado valores para esas propiedades para indicar determinados parámetros de opción de codificación y está pasando el mismo objeto a usted para inicializar el objeto **IWICBitmapFrameEncode** .</span><span class="sxs-lookup"><span data-stu-id="ebbca-122">The caller has now provided values for those properties to indicate certain encoding option parameters, and is passing the same object back to you to initialize the **IWICBitmapFrameEncode** object.</span></span> <span data-ttu-id="ebbca-123">Debe aplicar las opciones especificadas al codificar los bits de la imagen.</span><span class="sxs-lookup"><span data-stu-id="ebbca-123">You should apply the specified options when encoding the image bits.</span></span>

### <a name="setsize-and-setresolution"></a><span data-ttu-id="ebbca-124">SetSize y SetResolution</span><span class="sxs-lookup"><span data-stu-id="ebbca-124">SetSize and SetResolution</span></span>

<span data-ttu-id="ebbca-125">[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) y [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) se explican por sí solos.</span><span class="sxs-lookup"><span data-stu-id="ebbca-125">[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) and [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) are self-explanatory.</span></span> <span data-ttu-id="ebbca-126">El autor de la llamada utiliza estos métodos para especificar el tamaño y la resolución de la imagen codificada.</span><span class="sxs-lookup"><span data-stu-id="ebbca-126">The caller uses these methods to specify the size and resolution for the encoded image.</span></span>

### <a name="setpixelformat"></a><span data-ttu-id="ebbca-127">SetPixelFormat</span><span class="sxs-lookup"><span data-stu-id="ebbca-127">SetPixelFormat</span></span>

<span data-ttu-id="ebbca-128">[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) se usa para solicitar un formato de píxel en el que codificar la imagen.</span><span class="sxs-lookup"><span data-stu-id="ebbca-128">[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) is used to request a pixel format in which to encode the image.</span></span> <span data-ttu-id="ebbca-129">Si el formato de píxel solicitado no es compatible, debe devolver el GUID del formato de píxel más cercano que se admite en *pPixelFormat*, que es un parámetro in/out.</span><span class="sxs-lookup"><span data-stu-id="ebbca-129">If the requested pixel format is not supported, you should return the GUID of the closest pixel format that is supported in *pPixelFormat*, which is an in/out parameter.</span></span>

### <a name="setcolorcontexts"></a><span data-ttu-id="ebbca-130">SetColorContexts</span><span class="sxs-lookup"><span data-stu-id="ebbca-130">SetColorContexts</span></span>

<span data-ttu-id="ebbca-131">[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) se usa para especificar uno o más contextos de color válidos (también conocidos como perfiles de color) para esta imagen.</span><span class="sxs-lookup"><span data-stu-id="ebbca-131">[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) is used to specify one or more valid color contexts (also known as color profiles) for this image.</span></span> <span data-ttu-id="ebbca-132">Es importante especificar los contextos de color, de modo que una aplicación que descodifica la imagen más tarde puede convertir el perfil de color de origen en el perfil de destino del dispositivo que se usa para mostrar o imprimir la imagen.</span><span class="sxs-lookup"><span data-stu-id="ebbca-132">It’s important to specify the color contexts, so an application that decodes the image at a later time can convert from the source color profile to the destination profile of the device being used to display or print the image.</span></span> <span data-ttu-id="ebbca-133">Sin un perfil de color, no es posible obtener colores coherentes en distintos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ebbca-133">Without a color profile, it is not possible to get consistent colors across different devices.</span></span> <span data-ttu-id="ebbca-134">Esto puede resultar frustrante para los usuarios finales cuando sus fotografías tienen un aspecto diferente en diferentes monitores y no pueden hacer que las copias coincidan con lo que ven en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="ebbca-134">This can be frustrating for end users when their photos look different on different monitors, and they can’t get the prints to match what they see on screen.</span></span>

### <a name="getmetadataquerywriter"></a><span data-ttu-id="ebbca-135">GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="ebbca-135">GetMetadataQueryWriter</span></span>

<span data-ttu-id="ebbca-136">[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) devuelve un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) que una aplicación puede usar para insertar o editar propiedades de metadatos específicas en un bloque de metadatos en el marco de imagen.</span><span class="sxs-lookup"><span data-stu-id="ebbca-136">[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) returns an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) that an application can use to insert or edit specific metadata properties in a metadata block on the image frame.</span></span>

<span data-ttu-id="ebbca-137">Puede crear instancias de un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) desde [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="ebbca-137">You can instantiate an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) from the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) in several ways.</span></span> <span data-ttu-id="ebbca-138">Puede crearlo desde el [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), de la misma manera que [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) se creó a partir de un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) en el método [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) de la interfaz [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="ebbca-138">You can either create it from your [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), the same way [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) was created from an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) in the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) method on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface.</span></span>


```C++
IWICMetadataQueryWriter* piMetadataQueryWriter = NULL;
HRESULT hr;

hr = m_piComponentFactory->CreateQueryWriterFromBlockWriter( 
      static_cast<IWICMetadataBlockWriter*>(this), 
      &piMetadataQueryWriter);

```



<span data-ttu-id="ebbca-139">También se puede crear a partir de un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)existente, como el obtenido con el método anterior.</span><span class="sxs-lookup"><span data-stu-id="ebbca-139">You can also create it from an existing [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), such as the one obtained using the previous method.</span></span>


```C++
hr = m_piComponentFactory->CreateQueryWriterFromReader( 
      piMetadataQueryReader, pguidVendor, &piMetadataQueryWriter);
```



<span data-ttu-id="ebbca-140">El parámetro *pguidVendor* permite especificar un proveedor determinado para que lo use el escritor de consultas al crear instancias de un escritor de metadatos.</span><span class="sxs-lookup"><span data-stu-id="ebbca-140">The *pguidVendor* parameter allows you to specify a particular vendor for the query writer to use when instantiating a metadata writer.</span></span> <span data-ttu-id="ebbca-141">Por ejemplo, si proporciona sus propios escritores de metadatos, puede especificar su propio GUID de proveedor.</span><span class="sxs-lookup"><span data-stu-id="ebbca-141">For example, if you provide your own metadata writers, you may want to specify your own vendor GUID.</span></span> <span data-ttu-id="ebbca-142">Puede pasar **null** a este parámetro si no tiene ninguna preferencia.</span><span class="sxs-lookup"><span data-stu-id="ebbca-142">You can pass **NULL** to this parameter if you don’t have a preference.</span></span>

### <a name="setthumbnail"></a><span data-ttu-id="ebbca-143">SetThumbnail</span><span class="sxs-lookup"><span data-stu-id="ebbca-143">SetThumbnail</span></span>

<span data-ttu-id="ebbca-144">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) se usa para proporcionar una miniatura.</span><span class="sxs-lookup"><span data-stu-id="ebbca-144">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) is used to provide a thumbnail.</span></span> <span data-ttu-id="ebbca-145">Todas las imágenes deben proporcionar una miniatura, ya sea globalmente, en cada fotograma o en ambas.</span><span class="sxs-lookup"><span data-stu-id="ebbca-145">All images should provide a thumbnail either globally, on each frame, or both.</span></span> <span data-ttu-id="ebbca-146">Los métodos **GetThumbnail** y **SetThumbnail** son opcionales en el nivel de contenedor pero, si un códec devuelve WINCODEC \_ Err \_ CODECNOTHUMBNAIL del método [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) , Windows Imaging Component (WIC) invocará el método [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) para el marco 0.</span><span class="sxs-lookup"><span data-stu-id="ebbca-146">The **GetThumbnail** and **SetThumbnail** methods are optional at the container-level but, if a codec returns WINCODEC\_ERR\_CODECNOTHUMBNAIL from the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) method, Windows Imaging Component (WIC) will invoke the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method for Frame 0.</span></span> <span data-ttu-id="ebbca-147">Si no se encuentra ninguna miniatura en ningún lugar, WIC debe descodificar la imagen completa y escalarla a un tamaño de miniatura, lo que podría suponer una gran penalización del rendimiento para imágenes más grandes.</span><span class="sxs-lookup"><span data-stu-id="ebbca-147">If no thumbnail is found in either place, WIC must decode the full image and scale it to thumbnail size, which could incur a large performance penalty for larger images.</span></span>

<span data-ttu-id="ebbca-148">La miniatura debe tener un tamaño y una resolución que permita descodificar y mostrar rápidamente.</span><span class="sxs-lookup"><span data-stu-id="ebbca-148">The thumbnail should be of a size and resolution that makes it quick to decode and display.</span></span> <span data-ttu-id="ebbca-149">Por este motivo, las miniaturas suelen ser imágenes JPEG.</span><span class="sxs-lookup"><span data-stu-id="ebbca-149">For this reason, thumbnails are most commonly JPEG images.</span></span> <span data-ttu-id="ebbca-150">Tenga en cuenta que, si usa JPEG para las miniaturas, no tiene que escribir un codificador JPEG para codificarlos o un descodificador JPEG para descodificarlos.</span><span class="sxs-lookup"><span data-stu-id="ebbca-150">Note that, if you use JPEG for your thumbnails, you don’t have to write a JPEG encoder to encode them, or a JPEG decoder to decode them.</span></span> <span data-ttu-id="ebbca-151">Siempre debe delegar en el códec JPEG que se suministra con la plataforma WIC para codificar y descodificar las miniaturas.</span><span class="sxs-lookup"><span data-stu-id="ebbca-151">You should always delegate to the JPEG codec that ships with the WIC platform for encoding and decoding thumbnails.</span></span>

### <a name="writepixels"></a><span data-ttu-id="ebbca-152">WritePixels</span><span class="sxs-lookup"><span data-stu-id="ebbca-152">WritePixels</span></span>

<span data-ttu-id="ebbca-153">[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) es el método que se usa para pasar líneas de análisis de un mapa de bits en memoria para la codificación.</span><span class="sxs-lookup"><span data-stu-id="ebbca-153">[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) is the method used to pass in scan lines from a bitmap in memory for encoding.</span></span> <span data-ttu-id="ebbca-154">Se llamará al método varias veces hasta que se hayan pasado todas las líneas de recorrido.</span><span class="sxs-lookup"><span data-stu-id="ebbca-154">The method will be called repeatedly until all of the scan lines have been passed in.</span></span> <span data-ttu-id="ebbca-155">El parámetro *lineCount* indica el número de líneas de análisis que se van a escribir en esta llamada.</span><span class="sxs-lookup"><span data-stu-id="ebbca-155">The *lineCount* parameter indicates how many scan lines are to be written in this call.</span></span> <span data-ttu-id="ebbca-156">El parámetro *cbStride* indica el número de bytes por línea de examen.</span><span class="sxs-lookup"><span data-stu-id="ebbca-156">The *cbStride* parameter indicates the number of bytes per scan line.</span></span> <span data-ttu-id="ebbca-157">*cbBufferSize* indica el tamaño del búfer pasado en el parámetro pbPixels, que contiene los bits de imagen reales que se van a codificar.</span><span class="sxs-lookup"><span data-stu-id="ebbca-157">*cbBufferSize* indicates the size of the buffer passed in the pbPixels parameter, which contains the actual image bits to be encoded.</span></span> <span data-ttu-id="ebbca-158">Si el alto combinado de las líneas de análisis de las llamadas acumulativas es mayor que el alto especificado en el método [**setSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) , se devuelve WINCODEC \_ Err \_ TOOMANYSCANLINES.</span><span class="sxs-lookup"><span data-stu-id="ebbca-158">If the combined height of the scan lines from cumulative calls is greater than the height specified in [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) method, return WINCODEC\_ERR\_TOOMANYSCANLINES.</span></span>

<span data-ttu-id="ebbca-159">Cuando [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) es **WICBitmapEncoderCacheInMemory**, las líneas de análisis deben almacenarse en la memoria caché hasta que se hayan pasado todas las líneas de examen.</span><span class="sxs-lookup"><span data-stu-id="ebbca-159">When the [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) is **WICBitmapEncoderCacheInMemory**, the scan lines should be cached in memory until all scan lines have been passed in.</span></span> <span data-ttu-id="ebbca-160">Si la opción de caché del codificador es **WICBitmapEncoderCacheTempFile**, las líneas de análisis deben almacenarse en caché en un archivo temporal, que se crea al inicializar el objeto.</span><span class="sxs-lookup"><span data-stu-id="ebbca-160">If the encoder cache option is **WICBitmapEncoderCacheTempFile**, the scan lines should be cached in a temporary file, created when initializing the object.</span></span> <span data-ttu-id="ebbca-161">En cualquiera de estos casos, la imagen no se debe codificar hasta que el autor de la llamada llame a [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).</span><span class="sxs-lookup"><span data-stu-id="ebbca-161">In either of these cases, the image should not be encoded until the caller calls [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).</span></span> <span data-ttu-id="ebbca-162">En el caso de que la opción de caché sea **WICBitmapEncoderNoCache**, el codificador debe codificar las líneas de análisis a medida que se reciben, si es posible.</span><span class="sxs-lookup"><span data-stu-id="ebbca-162">In the case where the cache option is **WICBitmapEncoderNoCache**, the encoder should encode the scan lines as they’re received, if possible.</span></span> <span data-ttu-id="ebbca-163">(En algunos formatos, esto no es posible y las líneas de recorrido deben almacenarse en caché hasta que se llame a commit).</span><span class="sxs-lookup"><span data-stu-id="ebbca-163">(In some formats, this is not possible, and the scan lines must be cached until Commit is called.)</span></span>

<span data-ttu-id="ebbca-164">La mayoría de los códecs sin formato no implementarán [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), ya que no admiten la modificación de los bits de imagen en el archivo sin formato.</span><span class="sxs-lookup"><span data-stu-id="ebbca-164">Most raw codecs will not implement [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), because they don’t support altering the image bits in the raw file.</span></span> <span data-ttu-id="ebbca-165">Sin embargo, los códecs sin formato deben implementar **WritePixels**, porque cuando se agregan metadatos, puede aumentar el tamaño del archivo, lo que requiere que el archivo se vuelva a escribir en el disco.</span><span class="sxs-lookup"><span data-stu-id="ebbca-165">Raw codecs should still implement **WritePixels**, however, because when metadata is added, it may increase the size of the file, requiring the file to be rewritten on the disk.</span></span> <span data-ttu-id="ebbca-166">En ese caso, es necesario poder copiar los bits de imagen existentes, que es lo que hace el método **WritePixels** .</span><span class="sxs-lookup"><span data-stu-id="ebbca-166">In that case, it’s necessary to be able to copy the existing image bits, which is what the **WritePixels** method does.</span></span>

### <a name="writesource"></a><span data-ttu-id="ebbca-167">WriteSource</span><span class="sxs-lookup"><span data-stu-id="ebbca-167">WriteSource</span></span>

<span data-ttu-id="ebbca-168">[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) se usa para codificar un objeto [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="ebbca-168">[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) is used to encode an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span> <span data-ttu-id="ebbca-169">El primer parámetro es un puntero a un objeto **IWICBitmapSource** .</span><span class="sxs-lookup"><span data-stu-id="ebbca-169">The first parameter is a pointer to an **IWICBitmapSource** object.</span></span> <span data-ttu-id="ebbca-170">El segundo parámetro es un WICRect que especifica la región de interés que se va a codificar.</span><span class="sxs-lookup"><span data-stu-id="ebbca-170">The second parameter is a WICRect that specifies the region of interest to encode.</span></span> <span data-ttu-id="ebbca-171">Se puede llamar a este método varias veces consecutivas, siempre que el ancho de cada rectángulo tenga el mismo ancho que la imagen final que se va a codificar.</span><span class="sxs-lookup"><span data-stu-id="ebbca-171">This method may be called multiple times in succession, as long as the width of each rectangle is the same width of the final image to be encoded.</span></span> <span data-ttu-id="ebbca-172">Si el ancho del rectángulo pasado en el parámetro PRC es diferente del ancho especificado en el método setSize, devuelva WINCODEC \_ Err \_ SOURCERECTDOESNOTMATCHDIMENSIONS.</span><span class="sxs-lookup"><span data-stu-id="ebbca-172">If the width of the rectangle passed in the prc parameter is different than the width specified in the SetSize method, return WINCODEC\_ERR\_SOURCERECTDOESNOTMATCHDIMENSIONS.</span></span> <span data-ttu-id="ebbca-173">Si el alto combinado de las líneas de análisis de las llamadas acumulativas es mayor que el alto especificado en el método setSize, se devuelve WINCODEC \_ Err \_ TOOMANYSCANLINES.</span><span class="sxs-lookup"><span data-stu-id="ebbca-173">If the combined height of the scan lines from cumulative calls is greater than the height specified in SetSize method, return WINCODEC\_ERR\_TOOMANYSCANLINES.</span></span>

<span data-ttu-id="ebbca-174">Las opciones de caché funcionan de la misma manera con este método que con el método [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ebbca-174">The cache options work the same way with this method as with the [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) method described previously.</span></span>

### <a name="commit"></a><span data-ttu-id="ebbca-175">Commit</span><span class="sxs-lookup"><span data-stu-id="ebbca-175">Commit</span></span>

<span data-ttu-id="ebbca-176">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) es el método que serializa los bits de imagen codificados en la secuencia de archivos y recorre en iteración todos los escritores de metadatos para el marco que los solicita para serializar los metadatos en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="ebbca-176">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) is the method that serializes the encoded image bits to the file stream, and iterates through all the metadata writers for the frame requesting them to serialize their metadata to the stream.</span></span> <span data-ttu-id="ebbca-177">En el caso de que la opción de caché del codificador sea WICBitmapEncoderCacheInMemory o WICBitmapEncoderCacheTempFile, este método también es responsable de codificar la imagen y, cuando la opción de caché es WICBitmapEncoderCacheTempFile, el método **commit** también debe eliminar el archivo temporal que se usa para almacenar en caché los datos de la imagen antes de la codificación.</span><span class="sxs-lookup"><span data-stu-id="ebbca-177">In the case where the encoder cache option is WICBitmapEncoderCacheInMemory or WICBitmapEncoderCacheTempFile, this method is also responsible for encoding the image, and when the cache option is WICBitmapEncoderCacheTempFile, the **Commit** method should also delete the temporary file used to cache the image data before encoding.</span></span>

<span data-ttu-id="ebbca-178">Este método siempre se invoca después de que se hayan pasado todas las líneas de recorrido o rectángulos que componen la imagen mediante el método [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) o [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) .</span><span class="sxs-lookup"><span data-stu-id="ebbca-178">This method is always invoked after all the scan lines or rectangles that make up the image have been passed in using either the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) or [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) method.</span></span> <span data-ttu-id="ebbca-179">El tamaño del rectángulo final que se compone a través de las llamadas acumuladas a WritePixels o WriteSource debe tener el mismo tamaño que el que se especificó en el método setSize.</span><span class="sxs-lookup"><span data-stu-id="ebbca-179">The size of the final rectangle that is composed through the accumulated calls to WritePixels or WriteSource must be the same size as was specified in the SetSize method.</span></span> <span data-ttu-id="ebbca-180">Si el tamaño no coincide con el tamaño esperado, este método debe devolver WINCODECERROR \_ UNEXPECTEDSIZE.</span><span class="sxs-lookup"><span data-stu-id="ebbca-180">If the size does not match the expected size, this method should return WINCODECERROR\_UNEXPECTEDSIZE.</span></span>

<span data-ttu-id="ebbca-181">Para recorrer en iteración los escritores de metadatos e indicar a cada escritor de metadatos que serialice sus metadatos, vaya a la secuencia, invoque GetWriterByIndex para recorrer en iteración los escritores de cada bloque e invoque IWICPersistStream. Save en cada escritor de metadatos.</span><span class="sxs-lookup"><span data-stu-id="ebbca-181">To iterate through the metadata writers and tell each metadata writer to serialize its metadata go the stream, invoke GetWriterByIndex to iterate through the writers for each block, and invoke IWICPersistStream.Save on each metadata writer.</span></span>


```C++
IWICMetadataWriter* piMetadataWRiter = NULL;
IWICPersistStream* piPersistStream = NULL;
HRESULT hr;

for (UINT x=0; x < m_blockCount; x++) 
{
    hr = GetWriterByIndex(x, & piMetadataWriter);
hr = piMetadataWriter->QueryInterface(
IID_IWICPersistStream,(void**)&piPersistStream);

hr = piPersistStream->Save(m_piStream, 
WICPersistOptions.WicPersistOptionDefault, 
true);
...
}
```



### <a name="setpalette"></a><span data-ttu-id="ebbca-182">SetPalette</span><span class="sxs-lookup"><span data-stu-id="ebbca-182">SetPalette</span></span>

<span data-ttu-id="ebbca-183">Solo los códecs con formatos indexados deben implementar el método [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="ebbca-183">Only codecs that have indexed formats need to implement the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) method.</span></span> <span data-ttu-id="ebbca-184">Si una imagen usa un formato indizado, use este método para especificar la paleta de colores utilizada en la imagen.</span><span class="sxs-lookup"><span data-stu-id="ebbca-184">If an image uses an indexed format, use this method to specify the palette of colors used in the image.</span></span> <span data-ttu-id="ebbca-185">Si el códec no tiene un formato indizado, devuelva WINCODEC \_ Err \_ PALETTEUNAVAILABLE desde este método.</span><span class="sxs-lookup"><span data-stu-id="ebbca-185">If your codec doesn’t have an indexed format, return WINCODEC\_ERR\_PALETTEUNAVAILABLE from this method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebbca-186">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ebbca-186">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ebbca-187">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ebbca-187">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ebbca-188">Implementación de IWICBitmapCodecProgressNotification (encoder)</span><span class="sxs-lookup"><span data-stu-id="ebbca-188">Implementing IWICBitmapCodecProgressNotification (Encoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[<span data-ttu-id="ebbca-189">Implementación de IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="ebbca-189">Implementing IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[<span data-ttu-id="ebbca-190">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="ebbca-190">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="ebbca-191">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="ebbca-191">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
