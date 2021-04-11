---
description: Un codificador escribe datos de imagen en una secuencia. Los codificadores pueden comprimir, cifrar y modificar los píxeles de la imagen de varias maneras antes de escribirlos en la secuencia.
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: Información general sobre la codificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be46aa73082071deb69fdd402f42866b18ef0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278844"
---
# <a name="encoding-overview"></a><span data-ttu-id="5c76a-104">Información general sobre la codificación</span><span class="sxs-lookup"><span data-stu-id="5c76a-104">Encoding Overview</span></span>

<span data-ttu-id="5c76a-105">Un codificador escribe datos de imagen en una secuencia.</span><span class="sxs-lookup"><span data-stu-id="5c76a-105">An encoder writes image data to a stream.</span></span> <span data-ttu-id="5c76a-106">Los codificadores pueden comprimir, cifrar y modificar los píxeles de la imagen de varias maneras antes de escribirlos en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="5c76a-106">Encoders can compress, encrypt, and alter the image pixels in a number of ways prior to writing them to the stream.</span></span> <span data-ttu-id="5c76a-107">El uso de algunos codificadores produce contrapartidas (por ejemplo, JPEG), que compensa la información de color para una mejor compresión.</span><span class="sxs-lookup"><span data-stu-id="5c76a-107">Using some encoders results in tradeoffs—for example, JPEG, which trades off color information for better compression.</span></span> <span data-ttu-id="5c76a-108">Otros codificadores no producen tales pérdidas, por ejemplo, mapa de bits (BMP).</span><span class="sxs-lookup"><span data-stu-id="5c76a-108">Other encoders do not result in such losses—for example, bitmap (BMP).</span></span> <span data-ttu-id="5c76a-109">Dado que muchos códecs usan tecnología propietaria para lograr una mejor compresión y una fidelidad de imagen, los detalles sobre cómo se codifica una imagen son el desarrollador de códecs.</span><span class="sxs-lookup"><span data-stu-id="5c76a-109">Because many codecs use proprietary technology to achieve better compression and image fidelity, the details on how an image gets encoded are up to the codec developer.</span></span>

<span data-ttu-id="5c76a-110">En este tema se incluyen las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="5c76a-110">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="5c76a-111">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="5c76a-111">IWICBitmapEncoder</span></span>](#iwicbitmapencoder)
-   [<span data-ttu-id="5c76a-112">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="5c76a-112">IWICBitmapFrameEncode</span></span>](#iwicbitmapframeencode)
-   [<span data-ttu-id="5c76a-113">Ejemplo de codificación TIFF</span><span class="sxs-lookup"><span data-stu-id="5c76a-113">TIFF Encoding Example</span></span>](#tiff-encoding-example)
-   [<span data-ttu-id="5c76a-114">Uso de las opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="5c76a-114">Encoder Options Usage</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="5c76a-115">Opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="5c76a-115">Encoder Options</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="5c76a-116">Ejemplos de opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="5c76a-116">Encoder Options Examples</span></span>](#encoder-options-examples)
-   [<span data-ttu-id="5c76a-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c76a-117">Related topics</span></span>](#related-topics)

## <a name="iwicbitmapencoder"></a><span data-ttu-id="5c76a-118">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="5c76a-118">IWICBitmapEncoder</span></span>

<span data-ttu-id="5c76a-119">[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) es la interfaz principal para codificar una imagen en el formato de destino y usarse para serializar los componentes de una imagen, como miniatura ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) y marcos ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), en el archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="5c76a-119">[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) is the main interface for encoding an image to the target format and used to serialize an image's components, such as thumbnail ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) and frames ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), to the image file.</span></span>

<span data-ttu-id="5c76a-120">Cómo y cuándo se produce la serialización se dejan al desarrollador de códecs.</span><span class="sxs-lookup"><span data-stu-id="5c76a-120">How and when serialization occurs is left up to the codec developer.</span></span> <span data-ttu-id="5c76a-121">Cada bloque de datos individual en el formato de archivo de destino debe poder establecerse de forma independiente del orden, pero de nuevo es la decisión del desarrollador de códecs.</span><span class="sxs-lookup"><span data-stu-id="5c76a-121">Each individual block of data within the target file format should be able to set independent of order, but again, this is the codec developer's decision.</span></span> <span data-ttu-id="5c76a-122">Sin embargo, una vez que se llama al método [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) , no se deben permitir los cambios en la imagen y se debe cerrar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="5c76a-122">Once the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method is called however, changes to the image should not be allowed and the stream should be closed.</span></span>

## <a name="iwicbitmapframeencode"></a><span data-ttu-id="5c76a-123">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="5c76a-123">IWICBitmapFrameEncode</span></span>

<span data-ttu-id="5c76a-124">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) es la interfaz para codificar los marcos individuales de una imagen.</span><span class="sxs-lookup"><span data-stu-id="5c76a-124">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) is the interface for encoding the individual frames of an image.</span></span> <span data-ttu-id="5c76a-125">Proporciona métodos para establecer componentes de creación de imágenes de fotogramas individuales, como miniaturas y fotogramas, así como dimensiones de imagen, PPP y formatos de píxel.</span><span class="sxs-lookup"><span data-stu-id="5c76a-125">It provides methods for setting individual frame imaging components, such as thumbnails and frames, as well as image dimensions, DPI, and pixel formats.</span></span>

<span data-ttu-id="5c76a-126">Los fotogramas individuales se pueden codificar con metadatos específicos del marco para que [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) proporcione acceso a un escritor de metadatos mediante el método [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="5c76a-126">Individual frames may be encoded with frame-specific metadata so [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) provides access to a metadata writer through the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

<span data-ttu-id="5c76a-127">El método [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) del marco confirma todos los cambios en el marco individual e indica que ya no se deben aceptar los cambios en ese marco.</span><span class="sxs-lookup"><span data-stu-id="5c76a-127">The frame's [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method commits all changes to the individual frame and indicates that changes to that frame should no longer be accepted.</span></span>

## <a name="tiff-encoding-example"></a><span data-ttu-id="5c76a-128">Ejemplo de codificación TIFF</span><span class="sxs-lookup"><span data-stu-id="5c76a-128">TIFF Encoding Example</span></span>

<span data-ttu-id="5c76a-129">En el ejemplo siguiente, una imagen de Tagged Image File Format (TIFF) se codifica mediante [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) y [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span><span class="sxs-lookup"><span data-stu-id="5c76a-129">In the following example, a Tagged Image File Format (TIFF) image is encoded using [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) and an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span> <span data-ttu-id="5c76a-130">La salida TIFF se personaliza mediante [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) y el marco de mapa de bits se inicializa con las opciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="5c76a-130">The TIFF output is customized using the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) and the bitmap frame is initialized using the given options.</span></span> <span data-ttu-id="5c76a-131">Una vez que la imagen se ha creado con [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), el marco se confirma mediante la [**confirmación**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) y la imagen se guarda con [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).</span><span class="sxs-lookup"><span data-stu-id="5c76a-131">Once the image has been created using [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), the frame is committed by way of [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) and the image is saved using [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).</span></span>


```C++
IWICImagingFactory *piFactory = NULL;
IWICBitmapEncoder *piEncoder = NULL;
IWICBitmapFrameEncode *piBitmapFrame = NULL;
IPropertyBag2 *pPropertybag = NULL;

IWICStream *piStream = NULL;
UINT uiWidth = 640;
UINT uiHeight = 480;

HRESULT hr = CoCreateInstance(
                CLSID_WICImagingFactory,
                NULL,
                CLSCTX_INPROC_SERVER,
                IID_IWICImagingFactory,
                (LPVOID*) &piFactory);

if (SUCCEEDED(hr))
{
    hr = piFactory->CreateStream(&piStream);
}

if (SUCCEEDED(hr))
{
    hr = piStream->InitializeFromFilename(L"output.tif", GENERIC_WRITE);
}

if (SUCCEEDED(hr))
{
   hr = piFactory->CreateEncoder(GUID_ContainerFormatTiff, NULL, &piEncoder);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->Initialize(piStream, WICBitmapEncoderNoCache);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetSize(uiWidth, uiHeight);
}

WICPixelFormatGUID formatGUID = GUID_WICPixelFormat24bppBGR;
if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetPixelFormat(&formatGUID);
}

if (SUCCEEDED(hr))
{
    // We're expecting to write out 24bppRGB. Fail if the encoder cannot do it.
    hr = IsEqualGUID(formatGUID, GUID_WICPixelFormat24bppBGR) ? S_OK : E_FAIL;
}

if (SUCCEEDED(hr))
{
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride**_/;
    UINT cbBufferSize = uiHeight _ cbStride;

    BYTE *pbBuffer = new BYTE[cbBufferSize];

    if (pbBuffer != NULL)
    {
        for (UINT i = 0; i < cbBufferSize; i++)
        {
            pbBuffer[i] = static_cast<BYTE>(rand());
        }

        hr = piBitmapFrame->WritePixels(uiHeight, cbStride, cbBufferSize, pbBuffer);

        delete[] pbBuffer;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->Commit();
}    

if (SUCCEEDED(hr))
{
    hr = piEncoder->Commit();
}

if (piFactory)
    piFactory->Release();

if (piEncoder)
    piEncoder->Release();

if (piBitmapFrame)
    piBitmapFrame->Release();

if (pPropertybag)
    pPropertybag->Release();

if (piStream)
    piStream->Release();

return hr;
```



## <a name="encoder-options-usage"></a><span data-ttu-id="5c76a-132">Uso de las opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="5c76a-132">Encoder Options Usage</span></span>

<span data-ttu-id="5c76a-133">Los distintos codificadores para distintos formatos deben exponer distintas opciones para la codificación de una imagen.</span><span class="sxs-lookup"><span data-stu-id="5c76a-133">Different encoders for different formats need to expose different options for how an image is encoded.</span></span> <span data-ttu-id="5c76a-134">El componente de creación de imágenes de Windows (WIC) proporciona un mecanismo coherente para expresar si se requieren opciones de codificación mientras se sigue permitiendo que las aplicaciones funcionen con varios codificadores sin necesidad de conocer un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="5c76a-134">Windows Imaging Component (WIC) provides a consistent mechanism for expressing whether encoding options are required while still enabling applications to work with multiple encoders without requiring knowledge of a particular format.</span></span> <span data-ttu-id="5c76a-135">Esto se consigue proporcionando un parámetro [IPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) en el método [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) y el método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) .</span><span class="sxs-lookup"><span data-stu-id="5c76a-135">This is accomplished by providing an [IPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) parameter on the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method and the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

<span data-ttu-id="5c76a-136">El generador de componentes proporciona un punto de creación fácil para crear un contenedor de propiedades de opciones de codificador.</span><span class="sxs-lookup"><span data-stu-id="5c76a-136">The component factory provides an easy creation point for creating an encoder options property bag.</span></span> <span data-ttu-id="5c76a-137">Los códecs pueden usar este servicio si necesitan proporcionar un conjunto simple, intuitivo y no conflictivo de opciones de codificador.</span><span class="sxs-lookup"><span data-stu-id="5c76a-137">Codecs can use this service if they need to provide a simple, intuitive and non-conflicting set of encoder options.</span></span> <span data-ttu-id="5c76a-138">La bolsa de propiedades de imágenes debe inicializarse durante la creación con todas las opciones de codificador relevantes para ese códec.</span><span class="sxs-lookup"><span data-stu-id="5c76a-138">The imaging property bag must be initialized during creation with all the encoder options relevant to that codec.</span></span> <span data-ttu-id="5c76a-139">En el caso de las opciones del codificador del conjunto canónico, el intervalo de valores se aplicará en la escritura.</span><span class="sxs-lookup"><span data-stu-id="5c76a-139">For encoder options from the canonical set, the value range will be enforced on Write.</span></span> <span data-ttu-id="5c76a-140">En el caso de las necesidades más avanzadas, los códecs deben escribir su propia implementación de contenedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="5c76a-140">For more advanced needs, codecs should write their own property bag implementation.</span></span>

<span data-ttu-id="5c76a-141">A una aplicación se le asigna el contenedor de opciones del codificador durante la creación del marco y debe configurar los valores antes de inicializar el marco del codificador.</span><span class="sxs-lookup"><span data-stu-id="5c76a-141">An application is given the encoder options bag during frame creation and must configure any values prior to initializing the encoder frame.</span></span> <span data-ttu-id="5c76a-142">En el caso de una aplicación controlada por la interfaz de usuario, puede ofrecer una interfaz de usuario fija para las opciones canónicas del codificador y una vista avanzada para las opciones restantes.</span><span class="sxs-lookup"><span data-stu-id="5c76a-142">For a UI-driven application, it can offer a fixed UI for the canonical encoder options and an advanced view for remaining options.</span></span> <span data-ttu-id="5c76a-143">Los cambios se pueden realizar de una en una a través del método Write y cualquier error se informará a través de IErrorLog.</span><span class="sxs-lookup"><span data-stu-id="5c76a-143">Changes can be made one at a time through the Write method and any error will be reported through IErrorLog.</span></span> <span data-ttu-id="5c76a-144">La aplicación de interfaz de usuario siempre debe volver a leer y mostrar todas las opciones después de realizar un cambio en caso de que el cambio provocó un efecto en cascada.</span><span class="sxs-lookup"><span data-stu-id="5c76a-144">The UI application should always re-read and display all options after making a change in case the change caused a cascade effect.</span></span> <span data-ttu-id="5c76a-145">Una aplicación debe estar preparada para controlar la inicialización de fotogramas con errores para códecs que solo proporcionan informes de errores mínimos a través de su contenedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="5c76a-145">An application should be prepared to handle failed frame initialization for codecs that only provide minimal error reporting through their property bag.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="5c76a-146">Opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="5c76a-146">Encoder Options</span></span>

<span data-ttu-id="5c76a-147">Una aplicación puede esperar encontrar el siguiente conjunto de opciones de codificador.</span><span class="sxs-lookup"><span data-stu-id="5c76a-147">An application can expect to encounter the following set of encoder options.</span></span> <span data-ttu-id="5c76a-148">Las opciones del codificador reflejan las capacidades de un codificador y el formato del contenedor subyacente y, por tanto, son por su naturaleza no es independiente del códec.</span><span class="sxs-lookup"><span data-stu-id="5c76a-148">Encoder options reflect the capabilities of an encoder and the underlying container format, and therefore are by their nature not really codec-agnostic.</span></span> <span data-ttu-id="5c76a-149">Cuando sea posible, se deben normalizar las nuevas opciones para que se puedan aplicar a los nuevos códecs que surjan.</span><span class="sxs-lookup"><span data-stu-id="5c76a-149">When possible, new options should be normalized so they can be applied to new codecs that emerge.</span></span>



| <span data-ttu-id="5c76a-150">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="5c76a-150">Property Name</span></span>      | <span data-ttu-id="5c76a-151">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5c76a-151">VARTYPE</span></span>  | <span data-ttu-id="5c76a-152">Value</span><span class="sxs-lookup"><span data-stu-id="5c76a-152">Value</span></span>                                                                     | <span data-ttu-id="5c76a-153">Códecs aplicables</span><span class="sxs-lookup"><span data-stu-id="5c76a-153">Applicable Codecs</span></span> |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="5c76a-154">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="5c76a-154">ImageQuality</span></span>       | <span data-ttu-id="5c76a-155">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="5c76a-155">VT\_R4</span></span>   | <span data-ttu-id="5c76a-156">0-1,0</span><span class="sxs-lookup"><span data-stu-id="5c76a-156">0-1.0</span></span>                                                                     | <span data-ttu-id="5c76a-157">JPEG, HDPhoto</span><span class="sxs-lookup"><span data-stu-id="5c76a-157">JPEG, HDPhoto</span></span>     |
| <span data-ttu-id="5c76a-158">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="5c76a-158">CompressionQuality</span></span> | <span data-ttu-id="5c76a-159">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="5c76a-159">VT\_R4</span></span>   | <span data-ttu-id="5c76a-160">0-1,0</span><span class="sxs-lookup"><span data-stu-id="5c76a-160">0-1.0</span></span>                                                                     | <span data-ttu-id="5c76a-161">TIFF</span><span class="sxs-lookup"><span data-stu-id="5c76a-161">TIFF</span></span>              |
| <span data-ttu-id="5c76a-162">Lossless</span><span class="sxs-lookup"><span data-stu-id="5c76a-162">Lossless</span></span>           | <span data-ttu-id="5c76a-163">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="5c76a-163">VT\_BOOL</span></span> | <span data-ttu-id="5c76a-164">**true**, **false**</span><span class="sxs-lookup"><span data-stu-id="5c76a-164">**TRUE**, **FALSE**</span></span>                                                       | <span data-ttu-id="5c76a-165">HDPhoto</span><span class="sxs-lookup"><span data-stu-id="5c76a-165">HDPhoto</span></span>           |
| <span data-ttu-id="5c76a-166">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="5c76a-166">BitmapTransform</span></span>    | <span data-ttu-id="5c76a-167">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="5c76a-167">VT\_UI1</span></span>  | [<span data-ttu-id="5c76a-168">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="5c76a-168">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="5c76a-169">JPEG</span><span class="sxs-lookup"><span data-stu-id="5c76a-169">JPEG</span></span>              |



 

<span data-ttu-id="5c76a-170">El valor de ImageQualty de 0,0 significa que la última copia de fidelidad posible y 1,0 significa la mayor fidelidad, que también puede implicar pérdida de pérdida según el códec.</span><span class="sxs-lookup"><span data-stu-id="5c76a-170">ImageQualty of 0.0 means the lowest possible fidelity rendition and 1.0 means the highest fidelity, which may also imply lossless depending on the codec.</span></span>

<span data-ttu-id="5c76a-171">CompressionQuality es el esquema 0,0 de compresión menos eficaz disponible, que normalmente produce una codificación rápida pero una salida más grande.</span><span class="sxs-lookup"><span data-stu-id="5c76a-171">CompressionQuality of 0.0 means the least efficient compression scheme available, typically resulting in a fast encode but larger output.</span></span> <span data-ttu-id="5c76a-172">Un valor de 1,0 significa que el esquema más eficaz disponible, normalmente tarda más tiempo en codificarse, pero generando una salida más pequeña.</span><span class="sxs-lookup"><span data-stu-id="5c76a-172">A value of 1.0 means the most efficient scheme available, typically taking more time to encode but producing smaller output.</span></span> <span data-ttu-id="5c76a-173">En función de las capacidades del códec, este intervalo se puede asignar a un conjunto discreto de métodos de compresión disponibles.</span><span class="sxs-lookup"><span data-stu-id="5c76a-173">Depending on the capabilities of the codec, this range may be mapped onto a discrete set of available compression methods.</span></span>

<span data-ttu-id="5c76a-174">Sin pérdida significa que el códec codifica la imagen como Lossless sin pérdida de datos de imagen.</span><span class="sxs-lookup"><span data-stu-id="5c76a-174">Lossless means that the codec encodes the image as lossless with no image data loss.</span></span> <span data-ttu-id="5c76a-175">Si se habilita Lossless, se omite ImageQuality.</span><span class="sxs-lookup"><span data-stu-id="5c76a-175">If Lossless is enabled, ImageQuality is ignored.</span></span>

<span data-ttu-id="5c76a-176">Además de las opciones de codificador genéricas anteriores, los códecs suministrados con WIC admiten las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="5c76a-176">In addition to the above generic encoder options, codecs supplied with WIC support the following options.</span></span> <span data-ttu-id="5c76a-177">Si un códec tiene la necesidad de admitir una opción coherente con el uso de estos códecs suministrados, se recomienda hacerlo.</span><span class="sxs-lookup"><span data-stu-id="5c76a-177">If a codec has a need to support an option that is consistent with the usage in these supplied codecs, it is encouraged to do so.</span></span>



| <span data-ttu-id="5c76a-178">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="5c76a-178">Property Name</span></span>           | <span data-ttu-id="5c76a-179">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5c76a-179">VARTYPE</span></span>           | <span data-ttu-id="5c76a-180">Value</span><span class="sxs-lookup"><span data-stu-id="5c76a-180">Value</span></span>                                                                             | <span data-ttu-id="5c76a-181">Códecs aplicables</span><span class="sxs-lookup"><span data-stu-id="5c76a-181">Applicable Codecs</span></span> |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="5c76a-182">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="5c76a-182">InterlaceOption</span></span>         | <span data-ttu-id="5c76a-183">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="5c76a-183">VT\_BOOL</span></span>          | <span data-ttu-id="5c76a-184">Activado/Desactivado</span><span class="sxs-lookup"><span data-stu-id="5c76a-184">On/Off</span></span>                                                                            | <span data-ttu-id="5c76a-185">PNG</span><span class="sxs-lookup"><span data-stu-id="5c76a-185">PNG</span></span>               |
| <span data-ttu-id="5c76a-186">FilterOption</span><span class="sxs-lookup"><span data-stu-id="5c76a-186">FilterOption</span></span>            | <span data-ttu-id="5c76a-187">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="5c76a-187">VT\_UI1</span></span>           | [<span data-ttu-id="5c76a-188">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="5c76a-188">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | <span data-ttu-id="5c76a-189">PNG</span><span class="sxs-lookup"><span data-stu-id="5c76a-189">PNG</span></span>               |
| <span data-ttu-id="5c76a-190">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="5c76a-190">TiffCompressionMethod</span></span>   | <span data-ttu-id="5c76a-191">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="5c76a-191">VT\_UI1</span></span>           | [<span data-ttu-id="5c76a-192">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="5c76a-192">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | <span data-ttu-id="5c76a-193">TIFF</span><span class="sxs-lookup"><span data-stu-id="5c76a-193">TIFF</span></span>              |
| <span data-ttu-id="5c76a-194">Luminance</span><span class="sxs-lookup"><span data-stu-id="5c76a-194">Luminance</span></span>               | <span data-ttu-id="5c76a-195">Matriz de VT \_ UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="5c76a-195">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="5c76a-196">64 entradas (DCT)</span><span class="sxs-lookup"><span data-stu-id="5c76a-196">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="5c76a-197">JPEG</span><span class="sxs-lookup"><span data-stu-id="5c76a-197">JPEG</span></span>              |
| <span data-ttu-id="5c76a-198">Chrominance</span><span class="sxs-lookup"><span data-stu-id="5c76a-198">Chrominance</span></span>             | <span data-ttu-id="5c76a-199">Matriz de VT \_ UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="5c76a-199">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="5c76a-200">64 entradas (DCT)</span><span class="sxs-lookup"><span data-stu-id="5c76a-200">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="5c76a-201">JPEG</span><span class="sxs-lookup"><span data-stu-id="5c76a-201">JPEG</span></span>              |
| <span data-ttu-id="5c76a-202">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="5c76a-202">JpegYCrCbSubsampling</span></span>    | <span data-ttu-id="5c76a-203">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="5c76a-203">VT\_UI1</span></span>           | [<span data-ttu-id="5c76a-204">**WICJpegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="5c76a-204">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | <span data-ttu-id="5c76a-205">JPEG</span><span class="sxs-lookup"><span data-stu-id="5c76a-205">JPEG</span></span>              |
| <span data-ttu-id="5c76a-206">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="5c76a-206">SuppressApp0</span></span>            | <span data-ttu-id="5c76a-207">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="5c76a-207">VT\_BOOL</span></span>          |                                                                                   | <span data-ttu-id="5c76a-208">JPEG</span><span class="sxs-lookup"><span data-stu-id="5c76a-208">JPEG</span></span>              |
| <span data-ttu-id="5c76a-209">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="5c76a-209">EnableV5Header32bppBGRA</span></span> | <span data-ttu-id="5c76a-210">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="5c76a-210">VT\_BOOL</span></span>          | <span data-ttu-id="5c76a-211">Activado/Desactivado</span><span class="sxs-lookup"><span data-stu-id="5c76a-211">On/Off</span></span>                                                                            | <span data-ttu-id="5c76a-212">BMP</span><span class="sxs-lookup"><span data-stu-id="5c76a-212">BMP</span></span>               |



 

<span data-ttu-id="5c76a-213">Use **VT \_ vacío** para indicar que **\* no \* se ha establecido** como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5c76a-213">Use **VT\_EMPTY** to indicate **\*not set\*** as the default.</span></span> <span data-ttu-id="5c76a-214">Si se establecen propiedades adicionales pero no se admiten, el codificador debe omitirlas. Esto permite que las aplicaciones codifiquen menos lógica si desean una funcionalidad que puede estar presente o no.</span><span class="sxs-lookup"><span data-stu-id="5c76a-214">If additional properties are set but not supported, the encoder should ignore them; this allows applications to code less logic if they want a capability that may or may not be present.</span></span>

## <a name="encoder-options-examples"></a><span data-ttu-id="5c76a-215">Ejemplos de opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="5c76a-215">Encoder Options Examples</span></span>

<span data-ttu-id="5c76a-216">En el [ejemplo de codificación TIFF](#tiff-encoding-example) anterior, se establece una opción de codificador específica.</span><span class="sxs-lookup"><span data-stu-id="5c76a-216">In the [TIFF Encoding Example](#tiff-encoding-example) above, a specific encoder option is set.</span></span> <span data-ttu-id="5c76a-217">El miembro *pstrName* de la estructura PROPBAG2 se establece en el nombre de propiedad adecuado y la variante se establece en el VARTYPE correspondiente y en el valor deseado (en este caso, un miembro de la enumeración [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) ).</span><span class="sxs-lookup"><span data-stu-id="5c76a-217">The *pstrName* member of the PROPBAG2 structure is set to the appropriate property name, and the VARIANT is set to the corresponding VARTYPE and the desired value—in this case, a member of the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) enumeration.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



<span data-ttu-id="5c76a-218">Para usar las opciones predeterminadas del codificador, solo tiene que inicializar el marco de mapa de bits con el contenedor de propiedades devuelto cuando se creó el marco.</span><span class="sxs-lookup"><span data-stu-id="5c76a-218">To use the default encoder options, simply initialize the bitmap frame with the property bag returned when the frame was created.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // Accept the default encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



<span data-ttu-id="5c76a-219">También es posible eliminar el contenedor de propiedades cuando no se están considerando opciones de codificador.</span><span class="sxs-lookup"><span data-stu-id="5c76a-219">It is also possible to eliminate the property bag when no encoder options are being considered.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, 0);
}

if (SUCCEEDED(hr))
{        
    // No encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(0);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="5c76a-220">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c76a-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5c76a-221">**Vista**</span><span class="sxs-lookup"><span data-stu-id="5c76a-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5c76a-222">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="5c76a-222">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="5c76a-223">Información general sobre descodificación</span><span class="sxs-lookup"><span data-stu-id="5c76a-223">Decoding Overview</span></span>](-wic-creating-decoder.md)
</dt> <dt>

<span data-ttu-id="5c76a-224">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="5c76a-224">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5c76a-225">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="5c76a-225">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
