---
description: El códec nativo JPEG XR está disponible a través de Windows Imaging Component (WIC). El formato JPEG XR, que el códec admite, está diseñado para la fotografía digital del consumidor y del profesional.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: Información general sobre el códec JPEG XR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32ffa397667b325d4e49eadf4d8ce42d49e8a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706877"
---
# <a name="jpeg-xr-codec-overview"></a><span data-ttu-id="0c645-104">Información general sobre el códec JPEG XR</span><span class="sxs-lookup"><span data-stu-id="0c645-104">JPEG XR Codec Overview</span></span>

<span data-ttu-id="0c645-105">El códec nativo JPEG XR está disponible a través de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="0c645-105">The native JPEG XR codec is available through the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="0c645-106">El formato JPEG XR, que el códec admite, está diseñado para la fotografía digital del consumidor y del profesional.</span><span class="sxs-lookup"><span data-stu-id="0c645-106">The JPEG XR format, which the codec supports, is designed for consumer and professional digital photography.</span></span>

<span data-ttu-id="0c645-107">El formato JPEG XR puede lograr hasta dos veces la eficiencia de compresión del formato JPEG original, con artefactos de compresión menos perceptibles.</span><span class="sxs-lookup"><span data-stu-id="0c645-107">The JPEG XR format can achieve up to twice the compression efficiency of the original JPEG format, with less noticeable compression artifacts.</span></span> <span data-ttu-id="0c645-108">Las características de JPEG XR incluyen:</span><span class="sxs-lookup"><span data-stu-id="0c645-108">Features of JPEG XR include:</span></span>

-   <span data-ttu-id="0c645-109">Compatibilidad con imágenes monocromáticas, RGB, CMYK y n-Channel</span><span class="sxs-lookup"><span data-stu-id="0c645-109">Support for monochrome, RGB, CMYK, and n-channel images</span></span>
-   <span data-ttu-id="0c645-110">formatos enteros de 8, 16 y 32 bits</span><span class="sxs-lookup"><span data-stu-id="0c645-110">8-, 16-, and 32-bit integer formats</span></span>
-   <span data-ttu-id="0c645-111">Alta gama dinámica, formatos anchos, con valores de color de punto fijo o punto flotante</span><span class="sxs-lookup"><span data-stu-id="0c645-111">High dynamic range, wide-gamut formats, using fixed point or floating point color values</span></span>
-   <span data-ttu-id="0c645-112">Descodificación progresiva</span><span class="sxs-lookup"><span data-stu-id="0c645-112">Progressive decoding</span></span>
-   <span data-ttu-id="0c645-113">Codificación con pérdida o sin pérdida mediante el mismo algoritmo de compresión</span><span class="sxs-lookup"><span data-stu-id="0c645-113">Lossy or lossless encoding using the same compression algorithm</span></span>
-   <span data-ttu-id="0c645-114">Compatibilidad con la descodificación de regiones de interés en imágenes de gran tamaño</span><span class="sxs-lookup"><span data-stu-id="0c645-114">Support for decoding of regions of interest in large images</span></span>

<span data-ttu-id="0c645-115">El formato JPEG XR se define en los siguientes documentos de estándares:</span><span class="sxs-lookup"><span data-stu-id="0c645-115">The JPEG XR format is defined in the following standards documents:</span></span>

-   <span data-ttu-id="0c645-116">ITU-T T. 832: *tecnología de la información: JPEG XR Image Coding System – Image codificación Specification*</span><span class="sxs-lookup"><span data-stu-id="0c645-116">ITU-T T.832: *Information technology – JPEG XR image coding system – Image coding specification*</span></span>
-   <span data-ttu-id="0c645-117">ISO/IEC 29199-2:2010: *tecnología de la información: sistema de codificación de imágenes JPEG XR, parte 2: especificación de codificación de imágenes*</span><span class="sxs-lookup"><span data-stu-id="0c645-117">ISO/IEC 29199-2:2010: *Information technology — JPEG XR image coding system — Part 2: Image coding specification*</span></span>

<span data-ttu-id="0c645-118">El estándar JPEG XR se basa en gran medida en el formato de [fotografía HD](hdphoto-format-overview.md) , pero hay algunas diferencias entre los dos formatos.</span><span class="sxs-lookup"><span data-stu-id="0c645-118">The JPEG XR standard is largely based on the [HD Photo](hdphoto-format-overview.md) format, but there are some differences between the two formats.</span></span> <span data-ttu-id="0c645-119">En Windows 8, el códec HD Photo se ha actualizado para que sea compatible con JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="0c645-119">In Windows 8, the HD Photo codec has been updated to support JPEG XR.</span></span> <span data-ttu-id="0c645-120">El codificador ahora siempre genera un flujo de bits compatible con JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="0c645-120">The encoder now always outputs a JPEG XR–compliant bit stream.</span></span> <span data-ttu-id="0c645-121">El descodificador puede descodificar imágenes JPEG XR y HD.</span><span class="sxs-lookup"><span data-stu-id="0c645-121">The decoder can decode both JPEG XR and HD Photo images.</span></span>

<span data-ttu-id="0c645-122">Se han realizado mejoras sustanciales en el rendimiento, en relación con el códec HD Photo, en el códec JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="0c645-122">Substantial performance improvements, in relation to the HD Photo codec, have been made to the JPEG XR codec.</span></span> <span data-ttu-id="0c645-123">Por ejemplo, se ha mejorado la descodificación de imágenes de subresolución, como la generación de miniaturas, así como la descodificación de imágenes de baja resolución.</span><span class="sxs-lookup"><span data-stu-id="0c645-123">For example, sub-resolution image decoding, such as thumbnail generation, has been improved, as well as low-resolution image decoding.</span></span> <span data-ttu-id="0c645-124">Se recomienda usar el formato JPEG XR en lugar del formato HD Photo.</span><span class="sxs-lookup"><span data-stu-id="0c645-124">It is recommended that you use the JPEG XR format instead of the HD Photo format.</span></span>

## <a name="codec-information"></a><span data-ttu-id="0c645-125">Información del códec</span><span class="sxs-lookup"><span data-stu-id="0c645-125">Codec Information</span></span>



|                     |                                                                         |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="0c645-126">Extensión de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="0c645-126">File name extension</span></span> | <span data-ttu-id="0c645-127">"jxr" y "WDP"</span><span class="sxs-lookup"><span data-stu-id="0c645-127">"jxr" and "wdp"</span></span>                                                         |
| <span data-ttu-id="0c645-128">GUID de contenedor</span><span class="sxs-lookup"><span data-stu-id="0c645-128">Container GUID</span></span>      | <span data-ttu-id="0c645-129">**GUID \_ ContainerFormatWmp**</span><span class="sxs-lookup"><span data-stu-id="0c645-129">**GUID\_ContainerFormatWmp**</span></span>                                            |
| <span data-ttu-id="0c645-130">GUID del descodificador</span><span class="sxs-lookup"><span data-stu-id="0c645-130">Decoder GUID</span></span>        | <span data-ttu-id="0c645-131">**CLSID \_ WICWmpDecoder**</span><span class="sxs-lookup"><span data-stu-id="0c645-131">**CLSID\_WICWmpDecoder**</span></span>                                                |
| <span data-ttu-id="0c645-132">GUID del codificador</span><span class="sxs-lookup"><span data-stu-id="0c645-132">Encoder GUID</span></span>        | <span data-ttu-id="0c645-133">**CLSID \_ WICWmpEncoder**</span><span class="sxs-lookup"><span data-stu-id="0c645-133">**CLSID\_WICWmpEncoder**</span></span>                                                |
| <span data-ttu-id="0c645-134">Compatibilidad con perfiles</span><span class="sxs-lookup"><span data-stu-id="0c645-134">Profile Support</span></span>     | <span data-ttu-id="0c645-135">El codificador y el descodificador admiten hasta el perfil principal y hasta el nivel 128.</span><span class="sxs-lookup"><span data-stu-id="0c645-135">The encoder and decoder support up to Main Profile and up to level 128.</span></span> |



 

## <a name="codec-features"></a><span data-ttu-id="0c645-136">Características del códec</span><span class="sxs-lookup"><span data-stu-id="0c645-136">Codec Features</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="0c645-137">Alto rango dinámico</span><span class="sxs-lookup"><span data-stu-id="0c645-137">High Dynamic Range</span></span>

<span data-ttu-id="0c645-138">JPEG XR admite imágenes de rangos más dinámicas, mediante el uso de colores de punto flotante o de punto fijo.</span><span class="sxs-lookup"><span data-stu-id="0c645-138">JPEG XR supports high-dynamic range images, using floating-point or fixed-point colors.</span></span> <span data-ttu-id="0c645-139">En estos formatos de color, el intervalo numérico de un píxel es mayor que el intervalo visible, de modo que puede ajustar los colores por encima o por debajo del rango visible durante las fases de procesamiento intermedios.</span><span class="sxs-lookup"><span data-stu-id="0c645-139">In these color formats, the numerical range of a pixel is larger than the visible range, so you can adjust colors above or below the visible range during intermediate processing stages.</span></span>

-   <span data-ttu-id="0c645-140">Punto fijo: en una representación de punto fijo, 0 representa el negro y 1,0 representa la saturación máxima.</span><span class="sxs-lookup"><span data-stu-id="0c645-140">Fixed-point: In a fixed-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="0c645-141">El códec JPEG XR admite formatos de punto fijo de 16 y 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0c645-141">The JPEG XR codec supports both 16-bit and 32-bit fixed-point formats.</span></span> <span data-ttu-id="0c645-142">Para 16 bits, 1,0 = 0x2000h, que proporciona 13 bits para el intervalo visible \[ 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="0c645-142">For 16-bit, 1.0 = 0x2000h, which gives 13 bits for the visible range \[0...1\].</span></span> <span data-ttu-id="0c645-143">El intervalo total es de – 4,0 a + 3,999 y se asigna linealmente.</span><span class="sxs-lookup"><span data-stu-id="0c645-143">The total range is –4.0 to +3.999, and is mapped linearly.</span></span> <span data-ttu-id="0c645-144">Para 32 bits, 1,0 = 0x01000000h, el intervalo visible es de 24 bits y el intervalo total es – 128 a + 127,999.</span><span class="sxs-lookup"><span data-stu-id="0c645-144">For 32-bit, 1.0 = 0x01000000h, the visible range is 24 bits, and the total range is –128 to +127.999.</span></span>
-   <span data-ttu-id="0c645-145">Punto flotante: en una representación de punto flotante, 0 representa el negro y 1,0 representa la saturación máxima.</span><span class="sxs-lookup"><span data-stu-id="0c645-145">Floating-point: In a floating-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="0c645-146">El códec JPEG XR es compatible con los formatos de punto flotante de 16 y 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0c645-146">The JPEG XR codec supports both 16-bit and 32-bit floating-point formats.</span></span>

### <a name="tiles"></a><span data-ttu-id="0c645-147">Iconos</span><span class="sxs-lookup"><span data-stu-id="0c645-147">Tiles</span></span>

<span data-ttu-id="0c645-148">Un marco se puede particionar en subregiones rectangulares denominadas *mosaicos*.</span><span class="sxs-lookup"><span data-stu-id="0c645-148">A frame can be partitioned into rectangular subregions called *tiles*.</span></span> <span data-ttu-id="0c645-149">Un icono es un área de una imagen que contiene matrices rectangulares de macrobloques.</span><span class="sxs-lookup"><span data-stu-id="0c645-149">A tile is an area of a image that contains rectangular arrays of macroblocks.</span></span> <span data-ttu-id="0c645-150">Los mosaicos permiten descodificar las regiones de la imagen sin procesar toda la imagen.</span><span class="sxs-lookup"><span data-stu-id="0c645-150">Tiles enable regions of the image to be decoded without processing the entire image.</span></span>

<span data-ttu-id="0c645-151">Durante la codificación, seleccione el número de mosaicos mediante el establecimiento de las propiedades **HorizontalTileSlices** y **VerticalTileSlices** .</span><span class="sxs-lookup"><span data-stu-id="0c645-151">During encoding, select the number of tiles by setting the **HorizontalTileSlices** and **VerticalTileSlices** properties.</span></span> <span data-ttu-id="0c645-152">El tamaño mínimo del mosaico es de 16 × 16 píxeles.</span><span class="sxs-lookup"><span data-stu-id="0c645-152">The minimum tile size is 16 × 16 pixels.</span></span> <span data-ttu-id="0c645-153">El codificador ajusta el número de mosaicos para mantener esta restricción.</span><span class="sxs-lookup"><span data-stu-id="0c645-153">The encoder adjusts the number of tiles to maintain this restriction.</span></span> <span data-ttu-id="0c645-154">Hay una sobrecarga de almacenamiento y procesamiento asociada a cada mosaico, por lo que debe tener en cuenta el número de mosaicos necesarios para determinados escenarios.</span><span class="sxs-lookup"><span data-stu-id="0c645-154">There is storage and processing overhead associated with each tile, so you should consider the number of tiles that are needed for particular scenarios.</span></span>

### <a name="image-stream-output"></a><span data-ttu-id="0c645-155">Salida de flujo de imagen</span><span class="sxs-lookup"><span data-stu-id="0c645-155">Image Stream Output</span></span>

<span data-ttu-id="0c645-156">El estándar JPEG-XR define dos partes de un archivo JPEG-XR:</span><span class="sxs-lookup"><span data-stu-id="0c645-156">The JPEG-XR standard defines two parts of a JPEG-XR file:</span></span>

-   <span data-ttu-id="0c645-157">Flujo de bits de imagen, definido en el cuerpo del estándar.</span><span class="sxs-lookup"><span data-stu-id="0c645-157">The image bit stream, defined in the body of the standard.</span></span>
-   <span data-ttu-id="0c645-158">Contenedor de la imagen.</span><span class="sxs-lookup"><span data-stu-id="0c645-158">The image container.</span></span> <span data-ttu-id="0c645-159">El archivo contiene metadatos Exif y XMP, y se define en el anexo A del estándar.</span><span class="sxs-lookup"><span data-stu-id="0c645-159">The file contains Exif and XMP metadata, and is defined in Annex A of the standard.</span></span>

<span data-ttu-id="0c645-160">Es posible, y permitido por el estándar, incrustar el flujo de imágenes dentro de otro tipo de contenedor de archivos.</span><span class="sxs-lookup"><span data-stu-id="0c645-160">It is possible, and allowed by the standard, to embed the image stream inside another type of file container.</span></span> <span data-ttu-id="0c645-161">El codificador admite un modo de solo transmisión, que genera la secuencia de bits de imagen sin procesar sin contenedor de imágenes.</span><span class="sxs-lookup"><span data-stu-id="0c645-161">The encoder supports a stream-only mode, which outputs the raw image bit stream with no image container.</span></span> <span data-ttu-id="0c645-162">Una aplicación puede almacenar el flujo de bits en otro formato de contenedor.</span><span class="sxs-lookup"><span data-stu-id="0c645-162">An application can store the bit stream in some other container format.</span></span>

<span data-ttu-id="0c645-163">Para habilitar el modo de solo transmisión, establezca la propiedad **StreamOnly** .</span><span class="sxs-lookup"><span data-stu-id="0c645-163">To enable stream-only mode, set the **StreamOnly** property.</span></span>

### <a name="image-quality-settings"></a><span data-ttu-id="0c645-164">Configuración de calidad de imagen</span><span class="sxs-lookup"><span data-stu-id="0c645-164">Image Quality Settings</span></span>

<span data-ttu-id="0c645-165">Varias propiedades de códec controlan la calidad de la imagen de salida del codificador.</span><span class="sxs-lookup"><span data-stu-id="0c645-165">Several codec properties control the quality of the output image from the encoder.</span></span>

-   <span data-ttu-id="0c645-166">[ImageQuality](#imagequality) es una propiedad común a través de los códecs WIC.</span><span class="sxs-lookup"><span data-stu-id="0c645-166">[ImageQuality](#imagequality) is a property common across WIC codecs.</span></span> <span data-ttu-id="0c645-167">Especifica la calidad de la imagen como un valor de punto flotante único entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="0c645-167">It specifies image quality as a single floating-point value from 0.0–1.0,</span></span>
-   <span data-ttu-id="0c645-168">Las propiedades [calidad](#image-quality-settings), [superposición](#overlap)y [submuestreo](#subsampling) proporcionan más control sobre la configuración de calidad.</span><span class="sxs-lookup"><span data-stu-id="0c645-168">The [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties give more control over the quality settings.</span></span>

<span data-ttu-id="0c645-169">Para usar las propiedades [calidad](#image-quality-settings), [superposición](#overlap)y [submuestreo](#subsampling) , establezca la propiedad [UseCodecOptions](#usecodecoptions) en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0c645-169">To use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties, set the [UseCodecOptions](#usecodecoptions) property to **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="0c645-170">Si [UseCodecOptions](#usecodecoptions) es **Variant \_ false** (**Variant \_ false** es el valor predeterminado), el codificador utiliza la propiedad [ImageQuality](#imagequality) .</span><span class="sxs-lookup"><span data-stu-id="0c645-170">If [UseCodecOptions](#usecodecoptions) is **VARIANT\_FALSE** (**VARIANT\_FALSE** is the default) the encoder uses the [ImageQuality](#imagequality) property.</span></span> <span data-ttu-id="0c645-171">El codificador asigna el valor de ImageQuality a la [calidad](#image-quality-settings), la [superposición](#overlap)y el [submuestreo](#subsampling) a través de una tabla de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="0c645-171">The encoder maps the value of ImageQuality to [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) through a lookup table.</span></span>

<span data-ttu-id="0c645-172">El codificador no admite la propiedad **CompressionQuality** .</span><span class="sxs-lookup"><span data-stu-id="0c645-172">The encoder does not support the **CompressionQuality** property.</span></span>

### <a name="compressed-domain-transcode"></a><span data-ttu-id="0c645-173">Transcodificación de dominios comprimidos</span><span class="sxs-lookup"><span data-stu-id="0c645-173">Compressed Domain Transcode</span></span>

<span data-ttu-id="0c645-174">El códec JPEG XR puede realizar ciertas transformaciones de imágenes sin descodificar realmente los datos comprimidos y volver a codificarlos.</span><span class="sxs-lookup"><span data-stu-id="0c645-174">The JPEG XR codec can perform certain image transformations without actually decoding the compressed data and re-encoding it.</span></span> <span data-ttu-id="0c645-175">Las operaciones de dominio comprimido son muy eficaces y evitan cualquier pérdida de calidad adicional que sea habitual al descodificar y volver a codificar una imagen comprimida con pérdida.</span><span class="sxs-lookup"><span data-stu-id="0c645-175">Compressed domain operations are very efficient and avoid any additional quality loss that is typical when you decode and re-encode a lossy-compressed image.</span></span>

<span data-ttu-id="0c645-176">Se admiten las siguientes operaciones de dominio comprimido:</span><span class="sxs-lookup"><span data-stu-id="0c645-176">The following compressed domain operations are supported:</span></span>

-   <span data-ttu-id="0c645-177">Recortar una región de la imagen.</span><span class="sxs-lookup"><span data-stu-id="0c645-177">Crop a region of the image.</span></span>
-   <span data-ttu-id="0c645-178">Girar o voltear la imagen.</span><span class="sxs-lookup"><span data-stu-id="0c645-178">Rotate or flip the image.</span></span>
-   <span data-ttu-id="0c645-179">Descarte los datos de frecuencia para crear un archivo de imagen más pequeño.</span><span class="sxs-lookup"><span data-stu-id="0c645-179">Discard frequency data to create a smaller image file.</span></span>
-   <span data-ttu-id="0c645-180">Reorganice la imagen entre el orden espacial y el orden de las frecuencias.</span><span class="sxs-lookup"><span data-stu-id="0c645-180">Reorganize the image between spatial and frequency order.</span></span>

<span data-ttu-id="0c645-181">El codificador de JPEG XR usa la transcodificación de dominios comprimidos, si es posible, cuando la imagen de origen es una imagen de JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="0c645-181">The JPEG XR encoder uses compressed domain transcoding, if possible, when the source image is a JPEG XR image.</span></span> <span data-ttu-id="0c645-182">Cuando el codificador realiza una operación de dominio comprimido, omite las siguientes propiedades de códec: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha),[superposición](#overlap)sin [pérdida](#lossless)y [calidad](#image-quality-settings).</span><span class="sxs-lookup"><span data-stu-id="0c645-182">When the encoder performs a compressed domain operation, it ignores the following codec properties: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha), [Lossless](#lossless)[Overlap](#overlap), and [Quality](#image-quality-settings).</span></span> <span data-ttu-id="0c645-183">Si las propiedades [HorizontalTileSlices](/windows) y [VerticalTileSlices](/windows) están presentes, debe establecerlas en cero.</span><span class="sxs-lookup"><span data-stu-id="0c645-183">If the [HorizontalTileSlices](/windows) and [VerticalTileSlices](/windows) properties are present, you must set them to zero.</span></span> <span data-ttu-id="0c645-184">No se puede cambiar el tamaño de mosaico de una imagen como parte de un transcodificación de dominios comprimidos.</span><span class="sxs-lookup"><span data-stu-id="0c645-184">You cannot change the tile size of an image as part of a compressed domain transcode.</span></span>

<span data-ttu-id="0c645-185">En la lista siguiente se describe cómo realizar las transformaciones de imagen.</span><span class="sxs-lookup"><span data-stu-id="0c645-185">The follow list describes how to perform the image transformations.</span></span>

-   <span data-ttu-id="0c645-186">Para recortar la imagen, establezca la región deseada en el parámetro [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) del método **WriteSource** .</span><span class="sxs-lookup"><span data-stu-id="0c645-186">To crop the image, set the desired region in the [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) parameter of the **WriteSource** method.</span></span>
-   <span data-ttu-id="0c645-187">Para girar o voltear la imagen, establezca la propiedad [BitmapTransform](#bitmaptransform) .</span><span class="sxs-lookup"><span data-stu-id="0c645-187">To rotate or flip the image, set the [BitmapTransform](#bitmaptransform) property.</span></span>
-   <span data-ttu-id="0c645-188">Para descartar los datos de frecuencia de la imagen, establezca la propiedad [ImageDataDiscard](#imagedatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="0c645-188">To discard frequency data in the image, set the [ImageDataDiscard](#imagedatadiscard) property.</span></span> <span data-ttu-id="0c645-189">Para descartar los datos de frecuencia en el canal alfa, establezca la propiedad [AlphaDataDiscard](#alphadatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="0c645-189">To discard frequency data in the alpha channel, set the [AlphaDataDiscard](#alphadatadiscard) property.</span></span> <span data-ttu-id="0c645-190">Descartar los datos de frecuencia reduce el tamaño del archivo codificado y puede reducir la resolución.</span><span class="sxs-lookup"><span data-stu-id="0c645-190">Discarding frequency data reduces the encoded file size and can reduce the resolution.</span></span>
-   <span data-ttu-id="0c645-191">Para cambiar la organización de la imagen entre la frecuencia y la ordenación espacial, establezca la propiedad [FrequencyOrdering](/windows) .</span><span class="sxs-lookup"><span data-stu-id="0c645-191">To change the image organization between frequency and spatial ordering, set the [FrequencyOrdering](/windows) property.</span></span>

<span data-ttu-id="0c645-192">Para deshabilitar el transcodificación de dominios comprimidos y forzar que el codificador vuelva a codificar la imagen, establezca [UseCodecOptions](#usecodecoptions) en **Variant \_ true** y establezca [CompressedDomainTranscode](#compresseddomaintranscode) en **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="0c645-192">To disable compressed domain transcode and force the encoder to re-encode the image, set the [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE** and set [CompressedDomainTranscode](#compresseddomaintranscode) to **VARIANT\_FALSE**.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="0c645-193">Opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="0c645-193">Encoder Options</span></span>

<span data-ttu-id="0c645-194">Para establecer las propiedades de codificación, use la interfaz [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0c645-194">To set encoding properties, use the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface.</span></span> <span data-ttu-id="0c645-195">Para obtener más información, vea [información general sobre la codificación](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="0c645-195">For more information, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="0c645-196">En la lista siguiente se especifican las opciones del codificador.</span><span class="sxs-lookup"><span data-stu-id="0c645-196">The following list specifies the encoder options.</span></span>

-   [<span data-ttu-id="0c645-197">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="0c645-197">AlphaDataDiscard</span></span>](#alphadatadiscard)
-   [<span data-ttu-id="0c645-198">AlphaQuality</span><span class="sxs-lookup"><span data-stu-id="0c645-198">AlphaQuality</span></span>](#alphaquality)
-   [<span data-ttu-id="0c645-199">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="0c645-199">BitmapTransform</span></span>](#bitmaptransform)
-   [<span data-ttu-id="0c645-200">CompressedDomainTranscode</span><span class="sxs-lookup"><span data-stu-id="0c645-200">CompressedDomainTranscode</span></span>](#compresseddomaintranscode)
-   [<span data-ttu-id="0c645-201">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="0c645-201">FrequencyOrder</span></span>](#frequencyorder)
-   [<span data-ttu-id="0c645-202">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="0c645-202">HorizontalTileSlices</span></span>](#horizontaltileslices)
-   [<span data-ttu-id="0c645-203">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="0c645-203">IgnoreOverlap</span></span>](#ignoreoverlap)
-   [<span data-ttu-id="0c645-204">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="0c645-204">ImageDataDiscard</span></span>](#imagedatadiscard)
-   [<span data-ttu-id="0c645-205">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="0c645-205">ImageQuality</span></span>](#imagequality)
-   [<span data-ttu-id="0c645-206">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="0c645-206">InterleavedAlpha</span></span>](#interleavedalpha)
-   [<span data-ttu-id="0c645-207">Lossless</span><span class="sxs-lookup"><span data-stu-id="0c645-207">Lossless</span></span>](#lossless)
-   [<span data-ttu-id="0c645-208">Superpone</span><span class="sxs-lookup"><span data-stu-id="0c645-208">Overlap</span></span>](#overlap)
-   [<span data-ttu-id="0c645-209">ProgressiveMode</span><span class="sxs-lookup"><span data-stu-id="0c645-209">ProgressiveMode</span></span>](#progressivemode)
-   [<span data-ttu-id="0c645-210">Quality</span><span class="sxs-lookup"><span data-stu-id="0c645-210">Quality</span></span>](#image-quality-settings)
-   [<span data-ttu-id="0c645-211">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="0c645-211">StreamOnly</span></span>](#streamonly)
-   [<span data-ttu-id="0c645-212">Un submuestreo</span><span class="sxs-lookup"><span data-stu-id="0c645-212">Subsampling</span></span>](#subsampling)
-   [<span data-ttu-id="0c645-213">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="0c645-213">UseCodecOptions</span></span>](#usecodecoptions)
-   [<span data-ttu-id="0c645-214">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="0c645-214">VerticalTileSlices</span></span>](#verticaltileslices)

### <a name="alphadatadiscard"></a><span data-ttu-id="0c645-215">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="0c645-215">AlphaDataDiscard</span></span>

<span data-ttu-id="0c645-216">Establece la cantidad de datos de frecuencia alfa que se va a descartar durante la transcodificación de un dominio comprimido.</span><span class="sxs-lookup"><span data-stu-id="0c645-216">Sets the amount of alpha frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="0c645-217">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-217">Data type</span></span> | <span data-ttu-id="0c645-218">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-218">VARTYPE</span></span>     | <span data-ttu-id="0c645-219">Intervalo</span><span class="sxs-lookup"><span data-stu-id="0c645-219">Range</span></span> | <span data-ttu-id="0c645-220">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-220">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="0c645-221">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="0c645-221">**UCHAR**</span></span> | <span data-ttu-id="0c645-222">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="0c645-222">**VT\_UI1**</span></span> | <span data-ttu-id="0c645-223">de 0 a 4</span><span class="sxs-lookup"><span data-stu-id="0c645-223">0–4</span></span>   | <span data-ttu-id="0c645-224">None</span><span class="sxs-lookup"><span data-stu-id="0c645-224">None</span></span>    |



 

<span data-ttu-id="0c645-225">Esta propiedad solo se aplica si la propiedad [CompressedDomainTranscode](#compresseddomaintranscode) está establecida en **Variant \_ true** y la imagen contiene un canal alfa plano o un canal alfa intercalado; de lo contrario, se omite.</span><span class="sxs-lookup"><span data-stu-id="0c645-225">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and the image contains either a planar alpha channel or interleaved alpha channel; otherwise it is ignored.</span></span>

<span data-ttu-id="0c645-226">En el caso de las imágenes que contienen un canal alfa plano, los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="0c645-226">For images that contain a planar alpha channel, the following values are valid.</span></span>



| <span data-ttu-id="0c645-227">Value</span><span class="sxs-lookup"><span data-stu-id="0c645-227">Value</span></span> | <span data-ttu-id="0c645-228">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c645-228">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c645-229">0</span><span class="sxs-lookup"><span data-stu-id="0c645-229">0</span></span>     | <span data-ttu-id="0c645-230">No se descartan datos de frecuencia de la imagen.</span><span class="sxs-lookup"><span data-stu-id="0c645-230">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="0c645-231">1</span><span class="sxs-lookup"><span data-stu-id="0c645-231">1</span></span>     | <span data-ttu-id="0c645-232">Se descartan los flexbits.</span><span class="sxs-lookup"><span data-stu-id="0c645-232">The flexbits are discarded.</span></span> <span data-ttu-id="0c645-233">Esto reduce arbitrariamente la calidad del canal alfa plano para la imagen transcodificada.</span><span class="sxs-lookup"><span data-stu-id="0c645-233">This arbitrarily reduces the quality of the planar alpha channel for the transcoded image.</span></span> <span data-ttu-id="0c645-234">, sin un cambio en la resolución efectiva.</span><span class="sxs-lookup"><span data-stu-id="0c645-234">, without a change in the effective resolution.</span></span> <span data-ttu-id="0c645-235">La reducción exacta del tamaño y la calidad de los archivos depende de numerosos factores y no se puede especificar exactamente.</span><span class="sxs-lookup"><span data-stu-id="0c645-235">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="0c645-236">2</span><span class="sxs-lookup"><span data-stu-id="0c645-236">2</span></span>     | <span data-ttu-id="0c645-237">La banda de datos de frecuencia de paso alto se descarta, incluido el flexbits.</span><span class="sxs-lookup"><span data-stu-id="0c645-237">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="0c645-238">Esto reduce eficazmente la resolución del canal alfa plano en un factor de 4 en ambas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="0c645-238">This effectively reduces the resolution of the planar alpha channel by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="0c645-239">Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles en cada bloque 4x4 de píxeles de canal alfa.</span><span class="sxs-lookup"><span data-stu-id="0c645-239">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of alpha-channel pixels.</span></span> <span data-ttu-id="0c645-240">Normalmente, solo debe establecer este valor cuando la propiedad [ImageDataDiscard](#imagedatadiscard) tiene el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="0c645-240">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span>                            |
| <span data-ttu-id="0c645-241">3</span><span class="sxs-lookup"><span data-stu-id="0c645-241">3</span></span>     | <span data-ttu-id="0c645-242">Se descartan las bandas de datos de frecuencia alta y de baja pasada, incluido el flexbits.</span><span class="sxs-lookup"><span data-stu-id="0c645-242">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="0c645-243">Este ffectively reduce la resolución del canal alfa plano en un factor de 16 en ambas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="0c645-243">This ffectively reduces the resolution of the planar alpha channel by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="0c645-244">Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles en cada adaptativo macrobloque de 16x16 de píxeles de canal alfa.</span><span class="sxs-lookup"><span data-stu-id="0c645-244">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of alpha-channel pixels.</span></span> <span data-ttu-id="0c645-245">Normalmente, solo debe establecer este valor cuando la propiedad [ImageDataDiscard](#imagedatadiscard) tiene el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="0c645-245">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span> |
| <span data-ttu-id="0c645-246">4</span><span class="sxs-lookup"><span data-stu-id="0c645-246">4</span></span>     | <span data-ttu-id="0c645-247">Se descarta totalmente el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="0c645-247">The alpha channel is completely discarded.</span></span> <span data-ttu-id="0c645-248">El formato de píxel de la imagen transcodificada se cambia para reflejar la eliminación del canal alfa.</span><span class="sxs-lookup"><span data-stu-id="0c645-248">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="0c645-249">En el caso de las imágenes que contienen un canal alfa intercalado, el valor siguiente es válido.</span><span class="sxs-lookup"><span data-stu-id="0c645-249">For images that contain an interleaved alpha channel, the following value is valid.</span></span>



| <span data-ttu-id="0c645-250">Value</span><span class="sxs-lookup"><span data-stu-id="0c645-250">Value</span></span> | <span data-ttu-id="0c645-251">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c645-251">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c645-252">4</span><span class="sxs-lookup"><span data-stu-id="0c645-252">4</span></span>     | <span data-ttu-id="0c645-253">Se descarta totalmente el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="0c645-253">The alpha channel is completely discarded.</span></span> <span data-ttu-id="0c645-254">El formato de píxel de la imagen transcodificada se cambia para reflejar la eliminación del canal alfa.</span><span class="sxs-lookup"><span data-stu-id="0c645-254">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span> |



 

<span data-ttu-id="0c645-255">En el caso de alfa intercalado, a menos que esta propiedad esté establecida en 4, el canal alfa se procesa igual que los datos de la imagen, de acuerdo con el valor de la propiedad [ImageDataDiscard](#imagedatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="0c645-255">For interleaved alpha, unless this property is set to 4, the alpha channel is processed the same as the image data, according to the value of the [ImageDataDiscard](#imagedatadiscard) property.</span></span>

### <a name="alphaquality"></a><span data-ttu-id="0c645-256">AlphaQuality</span><span class="sxs-lookup"><span data-stu-id="0c645-256">AlphaQuality</span></span>

<span data-ttu-id="0c645-257">Establece la calidad de compresión para la imagen del canal alfa plana.</span><span class="sxs-lookup"><span data-stu-id="0c645-257">Sets the compression quality for the planar alpha channel image.</span></span>



| <span data-ttu-id="0c645-258">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-258">Data type</span></span> | <span data-ttu-id="0c645-259">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-259">VARTYPE</span></span>     | <span data-ttu-id="0c645-260">Intervalo</span><span class="sxs-lookup"><span data-stu-id="0c645-260">Range</span></span> | <span data-ttu-id="0c645-261">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-261">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="0c645-262">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="0c645-262">**UCHAR**</span></span> | <span data-ttu-id="0c645-263">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="0c645-263">**VT\_UI1**</span></span> | <span data-ttu-id="0c645-264">de 1 a 255</span><span class="sxs-lookup"><span data-stu-id="0c645-264">1–255</span></span> | <span data-ttu-id="0c645-265">1</span><span class="sxs-lookup"><span data-stu-id="0c645-265">1</span></span>       |



 

<span data-ttu-id="0c645-266">Esta propiedad se aplica cuando la imagen tiene un canal alfa y la propiedad [InterleavedAlpha](#interleavedalpha) es una **variante \_ falsa**.</span><span class="sxs-lookup"><span data-stu-id="0c645-266">This property applies when the image has an alpha channel and the [InterleavedAlpha](#interleavedalpha) property is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="0c645-267">El valor 1 indica el modo sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="0c645-267">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="0c645-268">Aumentar los valores produce mayores proporciones de compresión y una calidad de imagen inferior.</span><span class="sxs-lookup"><span data-stu-id="0c645-268">Increasing values result in higher compression ratios and lower image quality.</span></span>

### <a name="bitmaptransform"></a><span data-ttu-id="0c645-269">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="0c645-269">BitmapTransform</span></span>

<span data-ttu-id="0c645-270">Especifica si la imagen se gira o voltea al descodificar.</span><span class="sxs-lookup"><span data-stu-id="0c645-270">Specifies whether the image is rotated or flipped when decoded.</span></span>



| <span data-ttu-id="0c645-271">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-271">Data type</span></span> | <span data-ttu-id="0c645-272">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-272">VARTYPE</span></span>     | <span data-ttu-id="0c645-273">Intervalo</span><span class="sxs-lookup"><span data-stu-id="0c645-273">Range</span></span>                                                                     | <span data-ttu-id="0c645-274">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-274">Default</span></span>                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="0c645-275">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="0c645-275">**UCHAR**</span></span> | <span data-ttu-id="0c645-276">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="0c645-276">**VT\_UI1**</span></span> | [<span data-ttu-id="0c645-277">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="0c645-277">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="0c645-278">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="0c645-278">**WICBitmapTransformRotate0**</span></span> |



 

### <a name="compresseddomaintranscode"></a><span data-ttu-id="0c645-279">CompressedDomainTranscode</span><span class="sxs-lookup"><span data-stu-id="0c645-279">CompressedDomainTranscode</span></span>

<span data-ttu-id="0c645-280">Habilita o deshabilita la transcodificación de dominios comprimidos.</span><span class="sxs-lookup"><span data-stu-id="0c645-280">Enables or disables compressed domain transcoding.</span></span>



| <span data-ttu-id="0c645-281">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-281">Data type</span></span>         | <span data-ttu-id="0c645-282">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-282">VARTYPE</span></span>      | <span data-ttu-id="0c645-283">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-283">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="0c645-284">**VARIANTE \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c645-284">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="0c645-285">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c645-285">**VT\_BOOL**</span></span> | <span data-ttu-id="0c645-286">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="0c645-286">**VARIANT\_TRUE**</span></span> |



 

<span data-ttu-id="0c645-287">Para deshabilitar las operaciones de dominio comprimido, establezca esta propiedad en **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="0c645-287">To disable compressed domain operations, set this property to **VARIANT\_FALSE**.</span></span>

### <a name="frequencyorder"></a><span data-ttu-id="0c645-288">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="0c645-288">FrequencyOrder</span></span>

<span data-ttu-id="0c645-289">Habilita la codificación en orden de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="0c645-289">Enables encoding in frequency order.</span></span> <span data-ttu-id="0c645-290">Las implementaciones de dispositivos de los codificadores JPEG XR pueden organizar un archivo en orden espacial para reducir la memoria necesaria durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="0c645-290">Device implementations of JPEG XR encoders can organize a file in spatial order to reduce the memory required during encoding.</span></span>



| <span data-ttu-id="0c645-291">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-291">Data type</span></span>         | <span data-ttu-id="0c645-292">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-292">VARTYPE</span></span>      | <span data-ttu-id="0c645-293">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-293">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="0c645-294">**VARIANTE \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c645-294">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="0c645-295">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c645-295">**VT\_BOOL**</span></span> | <span data-ttu-id="0c645-296">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="0c645-296">**VARIANT\_TRUE**</span></span> |



 

-   <span data-ttu-id="0c645-297">**Variante \_ TRUE**: orden de la frecuencia.</span><span class="sxs-lookup"><span data-stu-id="0c645-297">**VARIANT\_TRUE**: Frequency order.</span></span> <span data-ttu-id="0c645-298">Los datos de la frecuencia más baja aparecen en primer lugar en el archivo y el contenido de la imagen se agrupa por su frecuencia en lugar de su orientación espacial.</span><span class="sxs-lookup"><span data-stu-id="0c645-298">The lowest frequency data appears first in the file, and image content is grouped by its frequency rather than its spatial orientation.</span></span> <span data-ttu-id="0c645-299">La organización de un archivo por orden de frecuencia proporciona el mejor rendimiento para cualquier descodificación basada en frecuencias.</span><span class="sxs-lookup"><span data-stu-id="0c645-299">Organizing a file by frequency order provides the best performance for any frequency-based decoding.</span></span>
-   <span data-ttu-id="0c645-300">**Variante \_ FALSE**: orden espacial.</span><span class="sxs-lookup"><span data-stu-id="0c645-300">**VARIANT\_FALSE**: Spatial order.</span></span> <span data-ttu-id="0c645-301">El orden espacial reduce la memoria necesaria durante la codificación</span><span class="sxs-lookup"><span data-stu-id="0c645-301">Spatial order reduces the memory required during encoding</span></span>

<span data-ttu-id="0c645-302">Se recomienda el orden de las frecuencias a menos que tenga razones de rendimiento o específicas de la aplicación para usar el orden espacial.</span><span class="sxs-lookup"><span data-stu-id="0c645-302">Frequency order is recommended unless you have performance or application-specific reasons to use spatial order.</span></span>

### <a name="horizontaltileslices"></a><span data-ttu-id="0c645-303">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="0c645-303">HorizontalTileSlices</span></span>

<span data-ttu-id="0c645-304">Establece el número de mosaicos horizontales.</span><span class="sxs-lookup"><span data-stu-id="0c645-304">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="0c645-305">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-305">Data type</span></span>  | <span data-ttu-id="0c645-306">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-306">VARTYPE</span></span>     | <span data-ttu-id="0c645-307">Intervalo</span><span class="sxs-lookup"><span data-stu-id="0c645-307">Range</span></span>  | <span data-ttu-id="0c645-308">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-308">Default</span></span>                      |
|------------|-------------|--------|------------------------------|
| <span data-ttu-id="0c645-309">**USHORT**</span><span class="sxs-lookup"><span data-stu-id="0c645-309">**USHORT**</span></span> | <span data-ttu-id="0c645-310">**VT \_ UI2**</span><span class="sxs-lookup"><span data-stu-id="0c645-310">**VT\_UI2**</span></span> | <span data-ttu-id="0c645-311">0 – 4095</span><span class="sxs-lookup"><span data-stu-id="0c645-311">0–4095</span></span> | <span data-ttu-id="0c645-312">(ancho de imagen – 1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="0c645-312">(image width – 1) >> 8</span></span> |



 

<span data-ttu-id="0c645-313">El valor es el número de subdivisiones horizontales; es decir, el número de mosaicos horizontales: 1.</span><span class="sxs-lookup"><span data-stu-id="0c645-313">The value is the number of horizontal subdivisions; that is, the number of horizontal tiles – 1.</span></span>

### <a name="ignoreoverlap"></a><span data-ttu-id="0c645-314">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="0c645-314">IgnoreOverlap</span></span>

<span data-ttu-id="0c645-315">Especifica cómo el codificador controla los límites del mosaico durante la transcodificación de un dominio comprimido.</span><span class="sxs-lookup"><span data-stu-id="0c645-315">Specifies how the encoder handles tile boundaries during a compressed domain transcode.</span></span>



| <span data-ttu-id="0c645-316">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-316">Data type</span></span>         | <span data-ttu-id="0c645-317">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-317">VARTYPE</span></span>      | <span data-ttu-id="0c645-318">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-318">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="0c645-319">**VARIANTE \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c645-319">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="0c645-320">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c645-320">**VT\_BOOL**</span></span> | <span data-ttu-id="0c645-321">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="0c645-321">**VARIANT\_FALSE**</span></span> |



 

<span data-ttu-id="0c645-322">Esta propiedad solo se aplica si la propiedad [CompressedDomainTranscode](#compresseddomaintranscode) se establece en **Variant \_ true** y se realiza una subcodificación de una subregión de exactamente uno o más mosaicos.</span><span class="sxs-lookup"><span data-stu-id="0c645-322">This property is applied only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and a sub-region transcode of exactly one or more tiles is performed.</span></span>

<span data-ttu-id="0c645-323">La operación predeterminada para una región Transcode es expandir la región solicitada para incluir los píxeles circundantes necesarios para la descodificación de superposiciones de los bordes de la región.</span><span class="sxs-lookup"><span data-stu-id="0c645-323">The default operation for a region transcode is to expand the requested region to include the surrounding pixels that are required for overlap decoding of the region edges.</span></span> <span data-ttu-id="0c645-324">Si esta propiedad se establece en **Variant \_ true**, el códec omite los píxeles circundantes y solo se extraen el mosaico o los mosaicos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="0c645-324">If this property is set to **VARIANT\_TRUE**, the codec ignores the surrounding pixels, and only the selected tile or tiles are extracted.</span></span> <span data-ttu-id="0c645-325">Si la imagen de origen no está en mosaico o si la región solicitada incluye mosaicos parciales, se omite este parámetro.</span><span class="sxs-lookup"><span data-stu-id="0c645-325">If the source image is not tiled or if the requested region includes partial tiles, this parameter is ignored.</span></span>

### <a name="imagedatadiscard"></a><span data-ttu-id="0c645-326">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="0c645-326">ImageDataDiscard</span></span>

<span data-ttu-id="0c645-327">Establece la cantidad de datos de frecuencia de la imagen que se van a descartar durante una transcodificación de dominio comprimido.</span><span class="sxs-lookup"><span data-stu-id="0c645-327">Sets the amount of image frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="0c645-328">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-328">Data type</span></span> | <span data-ttu-id="0c645-329">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-329">VARTYPE</span></span>     | <span data-ttu-id="0c645-330">Intervalo</span><span class="sxs-lookup"><span data-stu-id="0c645-330">Range</span></span> | <span data-ttu-id="0c645-331">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-331">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="0c645-332">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="0c645-332">**UCHAR**</span></span> | <span data-ttu-id="0c645-333">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="0c645-333">**VT\_UI1**</span></span> | <span data-ttu-id="0c645-334">0 – 3</span><span class="sxs-lookup"><span data-stu-id="0c645-334">0–3</span></span>   | <span data-ttu-id="0c645-335">0</span><span class="sxs-lookup"><span data-stu-id="0c645-335">0</span></span>       |



 

<span data-ttu-id="0c645-336">Esta propiedad solo se aplica si la propiedad [CompressedDomainTranscode](#compresseddomaintranscode) está establecida en **Variant \_ true**; en caso contrario, se omite.</span><span class="sxs-lookup"><span data-stu-id="0c645-336">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE**; otherwise it is ignored.</span></span>



| <span data-ttu-id="0c645-337">Value</span><span class="sxs-lookup"><span data-stu-id="0c645-337">Value</span></span> | <span data-ttu-id="0c645-338">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c645-338">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c645-339">0</span><span class="sxs-lookup"><span data-stu-id="0c645-339">0</span></span>     | <span data-ttu-id="0c645-340">No se descartan datos de frecuencia de la imagen.</span><span class="sxs-lookup"><span data-stu-id="0c645-340">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="0c645-341">1</span><span class="sxs-lookup"><span data-stu-id="0c645-341">1</span></span>     | <span data-ttu-id="0c645-342">Se descartan los flexbits.</span><span class="sxs-lookup"><span data-stu-id="0c645-342">The flexbits are discarded.</span></span> <span data-ttu-id="0c645-343">Esto reduce arbitrariamente la calidad de la imagen transcodificada sin cambiar la resolución efectiva de la imagen.</span><span class="sxs-lookup"><span data-stu-id="0c645-343">This arbitrarily reduces the quality of the transcoded image without changing the effective resolution of the image.</span></span> <span data-ttu-id="0c645-344">La reducción exacta del tamaño y la calidad de los archivos depende de numerosos factores y no se puede especificar exactamente.</span><span class="sxs-lookup"><span data-stu-id="0c645-344">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span> <span data-ttu-id="0c645-345">Este valor devuelve un error especificado para un canal alfa intercalado.</span><span class="sxs-lookup"><span data-stu-id="0c645-345">This value returns an error specified for an interleaved alpha channel.</span></span>                                                                                |
| <span data-ttu-id="0c645-346">2</span><span class="sxs-lookup"><span data-stu-id="0c645-346">2</span></span>     | <span data-ttu-id="0c645-347">La banda de datos de frecuencia de paso alto se descarta, incluido el flexbits.</span><span class="sxs-lookup"><span data-stu-id="0c645-347">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="0c645-348">Esto reduce la resolución de la imagen transcodificada en un factor de 4 en ambas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="0c645-348">This reduces the resolution of the transcoded image by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="0c645-349">Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles en cada bloque 4x4 de píxeles.</span><span class="sxs-lookup"><span data-stu-id="0c645-349">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of pixels.</span></span> <span data-ttu-id="0c645-350">Por lo tanto, la imagen transcodificada debe downsampledse en consecuencia cada vez que se descodifica.</span><span class="sxs-lookup"><span data-stu-id="0c645-350">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span>                             |
| <span data-ttu-id="0c645-351">3</span><span class="sxs-lookup"><span data-stu-id="0c645-351">3</span></span>     | <span data-ttu-id="0c645-352">Se descartan las bandas de datos de frecuencia alta y de baja pasada, incluido el flexbits.</span><span class="sxs-lookup"><span data-stu-id="0c645-352">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="0c645-353">Esto reduce la resolución de la imagen transcodificada en un factor de 16 en ambas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="0c645-353">This reduces the resolution of the transcoded image by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="0c645-354">Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles en cada adaptativo macrobloque de 16x16 de píxeles.</span><span class="sxs-lookup"><span data-stu-id="0c645-354">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of pixels.</span></span> <span data-ttu-id="0c645-355">Por lo tanto, la imagen transcodificada debe downsampledse en consecuencia cada vez que se descodifica.</span><span class="sxs-lookup"><span data-stu-id="0c645-355">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span> |



 

<span data-ttu-id="0c645-356">Si la imagen contiene un canal alfa intercalado, el valor de [ImageDataDiscard](#imagedatadiscard) se aplica al canal alfa a menos que la propiedad [AlphaDataDiscard](#alphadatadiscard) esté establecida en 4, en cuyo caso se descarta el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="0c645-356">If the image contains an interleaved alpha channel, the value of [ImageDataDiscard](#imagedatadiscard) is applied to the alpha channel unless the [AlphaDataDiscard](#alphadatadiscard) property is set to 4, in which case the alpha channel is discarded.</span></span>

<span data-ttu-id="0c645-357">En el caso del alfa plano, los datos de frecuencia que se descartan se controlan mediante la propiedad [AlphaDataDiscard](#alphadatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="0c645-357">For planar alpha, the frequency data that is discarded is controlled by the [AlphaDataDiscard](#alphadatadiscard) property.</span></span>

### <a name="imagequality"></a><span data-ttu-id="0c645-358">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="0c645-358">ImageQuality</span></span>

<span data-ttu-id="0c645-359">Establece la calidad de la imagen.</span><span class="sxs-lookup"><span data-stu-id="0c645-359">Sets the image quality.</span></span>



| <span data-ttu-id="0c645-360">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-360">Data type</span></span> | <span data-ttu-id="0c645-361">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-361">VARTYPE</span></span>    | <span data-ttu-id="0c645-362">Intervalo</span><span class="sxs-lookup"><span data-stu-id="0c645-362">Range</span></span> | <span data-ttu-id="0c645-363">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-363">Default</span></span> |
|-----------|------------|-------|---------|
| <span data-ttu-id="0c645-364">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="0c645-364">**FLOAT**</span></span> | <span data-ttu-id="0c645-365">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="0c645-365">**VT\_R4**</span></span> | <span data-ttu-id="0c645-366">0 – 1,0</span><span class="sxs-lookup"><span data-stu-id="0c645-366">0–1.0</span></span> | <span data-ttu-id="0c645-367">0.9</span><span class="sxs-lookup"><span data-stu-id="0c645-367">0.9</span></span>     |



 

<span data-ttu-id="0c645-368">El nivel 1,0 proporciona una compresión matemática sin pérdida de los mismos.</span><span class="sxs-lookup"><span data-stu-id="0c645-368">Level 1.0 gives mathematically lossless compression.</span></span>

<span data-ttu-id="0c645-369">El nivel 0,0 es el valor de la calidad más baja.</span><span class="sxs-lookup"><span data-stu-id="0c645-369">Level 0.0 is the lowest quality setting.</span></span>

### <a name="interleavedalpha"></a><span data-ttu-id="0c645-370">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="0c645-370">InterleavedAlpha</span></span>

<span data-ttu-id="0c645-371">Especifica si se va a codificar un alfa plano o alfa intercalado.</span><span class="sxs-lookup"><span data-stu-id="0c645-371">Specifies whether to encode interleaved alpha or planar alpha.</span></span>



| <span data-ttu-id="0c645-372">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-372">Data type</span></span>         | <span data-ttu-id="0c645-373">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-373">VARTYPE</span></span>      | <span data-ttu-id="0c645-374">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-374">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="0c645-375">**VARIANTE \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c645-375">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="0c645-376">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c645-376">**VT\_BOOL**</span></span> | <span data-ttu-id="0c645-377">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="0c645-377">**VARIANT\_FALSE**</span></span> |



 

-   <span data-ttu-id="0c645-378">**Variante \_ TRUE**: alfa intercalado.</span><span class="sxs-lookup"><span data-stu-id="0c645-378">**VARIANT\_TRUE**: Interleaved alpha.</span></span> <span data-ttu-id="0c645-379">La información del canal alfa se codifica como un canal intercalado adicional, sin correlación con los canales de contenido de la imagen.</span><span class="sxs-lookup"><span data-stu-id="0c645-379">Alpha channel information is encoded as an additional interleaved channel, with no correlation to the image content channels.</span></span> <span data-ttu-id="0c645-380">Este modo es útil para descodificar alfa simultáneamente con la imagen cuando la imagen se transmite por secuencias.</span><span class="sxs-lookup"><span data-stu-id="0c645-380">This mode is useful for decoding alpha simultaneously with the image when the image is streaming.</span></span>
-   <span data-ttu-id="0c645-381">VARIANT \_ false: alfa plana.</span><span class="sxs-lookup"><span data-stu-id="0c645-381">VARIANT\_FALSE: Planar alpha.</span></span> <span data-ttu-id="0c645-382">Un canal alfa plano se codifica como una imagen independiente.</span><span class="sxs-lookup"><span data-stu-id="0c645-382">A planar alpha channel is encoded as a separate image.</span></span> <span data-ttu-id="0c645-383">Los datos de la imagen y el canal alfa se descodifican de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="0c645-383">The image data and the alpha channel are decoded independently.</span></span> <span data-ttu-id="0c645-384">Opcionalmente, puede establecer el nivel de calidad del canal alfa estableciendo la propiedad [AlphaQuality](#alphaquality) .</span><span class="sxs-lookup"><span data-stu-id="0c645-384">Optionally, you can set the quality level of the alpha channel by setting the [AlphaQuality](#alphaquality) property.</span></span>

<span data-ttu-id="0c645-385">El alfa intercalado solo se admite para determinados formatos de píxeles RGB.</span><span class="sxs-lookup"><span data-stu-id="0c645-385">Interleaved alpha is supported only for certain RGB pixel formats.</span></span> <span data-ttu-id="0c645-386">El alfa plano es compatible con cualquier formato de imagen que defina un canal alfa.</span><span class="sxs-lookup"><span data-stu-id="0c645-386">Planar alpha is supported for any image format that defines an alpha channel.</span></span>

### <a name="lossless"></a><span data-ttu-id="0c645-387">Lossless</span><span class="sxs-lookup"><span data-stu-id="0c645-387">Lossless</span></span>

<span data-ttu-id="0c645-388">Habilita la compresión de pérdidas.</span><span class="sxs-lookup"><span data-stu-id="0c645-388">Enables losses compression.</span></span>



| <span data-ttu-id="0c645-389">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-389">Data type</span></span>         | <span data-ttu-id="0c645-390">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-390">VARTYPE</span></span>      | <span data-ttu-id="0c645-391">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-391">Default</span></span>        |
|-------------------|--------------|----------------|
| <span data-ttu-id="0c645-392">**VARIANTE \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c645-392">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="0c645-393">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c645-393">**VT\_BOOL**</span></span> | <span data-ttu-id="0c645-394">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="0c645-394">VARIANT\_FALSE</span></span> |



 

<span data-ttu-id="0c645-395">Si el valor es **Variant \_ true**, el codificador utiliza la compresión sin pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="0c645-395">If the value is **VARIANT\_TRUE**, the encoder uses lossless compression.</span></span> <span data-ttu-id="0c645-396">Cuando se establece en **Variant \_ true**, esta propiedad invalida la propiedad [ImageQuality](#imagequality) .</span><span class="sxs-lookup"><span data-stu-id="0c645-396">When set to **VARIANT\_TRUE**, this property overrides the [ImageQuality](#imagequality) property.</span></span>

### <a name="overlap"></a><span data-ttu-id="0c645-397">Superposición</span><span class="sxs-lookup"><span data-stu-id="0c645-397">Overlap</span></span>

<span data-ttu-id="0c645-398">Establece el nivel de filtrado de superposición.</span><span class="sxs-lookup"><span data-stu-id="0c645-398">Sets the level of overlap filtering.</span></span> <span data-ttu-id="0c645-399">Con el filtrado de superposición, los coeficientes de transformación se aplican en los límites de bloque y adaptativo macrobloque.</span><span class="sxs-lookup"><span data-stu-id="0c645-399">With overlap filtering, transform coefficients are applied across block and macroblock boundaries.</span></span> <span data-ttu-id="0c645-400">Esto puede reducir los artefactos de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="0c645-400">This can reduce blocking artifacts.</span></span>



| <span data-ttu-id="0c645-401">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-401">Data type</span></span> | <span data-ttu-id="0c645-402">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-402">VARTYPE</span></span>     | <span data-ttu-id="0c645-403">Intervalo</span><span class="sxs-lookup"><span data-stu-id="0c645-403">Range</span></span> | <span data-ttu-id="0c645-404">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-404">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="0c645-405">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="0c645-405">**UCHAR**</span></span> | <span data-ttu-id="0c645-406">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="0c645-406">**VT\_UI1**</span></span> | <span data-ttu-id="0c645-407">de 0 a 4</span><span class="sxs-lookup"><span data-stu-id="0c645-407">0–4</span></span>   | <span data-ttu-id="0c645-408">1</span><span class="sxs-lookup"><span data-stu-id="0c645-408">1</span></span>       |



 



| <span data-ttu-id="0c645-409">Value</span><span class="sxs-lookup"><span data-stu-id="0c645-409">Value</span></span> | <span data-ttu-id="0c645-410">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c645-410">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="0c645-411">0</span><span class="sxs-lookup"><span data-stu-id="0c645-411">0</span></span>     | <span data-ttu-id="0c645-412">No superponerse.</span><span class="sxs-lookup"><span data-stu-id="0c645-412">No overlap.</span></span>                                   |
| <span data-ttu-id="0c645-413">1</span><span class="sxs-lookup"><span data-stu-id="0c645-413">1</span></span>     | <span data-ttu-id="0c645-414">Un nivel de superposición, mosaico flexible.</span><span class="sxs-lookup"><span data-stu-id="0c645-414">One level of overlap, soft tiling.</span></span> <span data-ttu-id="0c645-415">(Valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="0c645-415">(Default.)</span></span> |
| <span data-ttu-id="0c645-416">2</span><span class="sxs-lookup"><span data-stu-id="0c645-416">2</span></span>     | <span data-ttu-id="0c645-417">Dos niveles de superposición, mosaico flexible.</span><span class="sxs-lookup"><span data-stu-id="0c645-417">Two levels of overlap, soft tiling.</span></span>           |
| <span data-ttu-id="0c645-418">3</span><span class="sxs-lookup"><span data-stu-id="0c645-418">3</span></span>     | <span data-ttu-id="0c645-419">Un nivel de superposición, mosaico fuerte</span><span class="sxs-lookup"><span data-stu-id="0c645-419">One level of overlap, hard tiling</span></span>             |
| <span data-ttu-id="0c645-420">4</span><span class="sxs-lookup"><span data-stu-id="0c645-420">4</span></span>     | <span data-ttu-id="0c645-421">Dos niveles de superposición, mosaico fuerte.</span><span class="sxs-lookup"><span data-stu-id="0c645-421">Two levels of overlap, hard tiling.</span></span>           |



 

<span data-ttu-id="0c645-422">Definiciones:</span><span class="sxs-lookup"><span data-stu-id="0c645-422">Definitions:</span></span>

-   <span data-ttu-id="0c645-423">Un nivel de superposición: los valores codificados de los bloques 4x4 se modifican en función de los bloques vecinos.</span><span class="sxs-lookup"><span data-stu-id="0c645-423">One level of overlap: The encoded values of 4x4 blocks are modified based on neighboring blocks.</span></span>
-   <span data-ttu-id="0c645-424">Dos niveles de superposición: se aplica el primer nivel de superposición.</span><span class="sxs-lookup"><span data-stu-id="0c645-424">Two levels of overlap: The first level of overlap is applied.</span></span> <span data-ttu-id="0c645-425">Además, los valores codificados de 16x16 macrobloques se modifican en función de la macrobloques vecina.</span><span class="sxs-lookup"><span data-stu-id="0c645-425">In addition, the encoded values of 16x16 macroblocks are modified based on the neighboring macroblocks.</span></span>
-   <span data-ttu-id="0c645-426">Mosaico flexible: el filtrado de superposición se aplica a través de los límites del mosaico.</span><span class="sxs-lookup"><span data-stu-id="0c645-426">Soft tiling: Overlap filtering is applied across tile boundaries.</span></span>
-   <span data-ttu-id="0c645-427">Mosaico fuerte: el filtrado de superposición no se aplica a través de los límites del mosaico.</span><span class="sxs-lookup"><span data-stu-id="0c645-427">Hard tiling: Overlap filtering is not applied across tile boundaries.</span></span> <span data-ttu-id="0c645-428">Los mosaicos fuertes pueden introducir algunos artefactos visuales a lo largo de los límites del mosaico.</span><span class="sxs-lookup"><span data-stu-id="0c645-428">Hard tiles can introduce some visual artifacts along tile boundaries.</span></span>

<span data-ttu-id="0c645-429">Si establece esta propiedad, establezca también [UseCodecOptions](#usecodecoptions) en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0c645-429">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="progressivemode"></a><span data-ttu-id="0c645-430">ProgressiveMode</span><span class="sxs-lookup"><span data-stu-id="0c645-430">ProgressiveMode</span></span>

<span data-ttu-id="0c645-431">Habilita o deshabilita la codificación progresiva.</span><span class="sxs-lookup"><span data-stu-id="0c645-431">Enables or disables progressive encoding.</span></span>



| <span data-ttu-id="0c645-432">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-432">Data type</span></span>         | <span data-ttu-id="0c645-433">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-433">VARTYPE</span></span>      | <span data-ttu-id="0c645-434">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-434">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="0c645-435">**VARIANTE \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c645-435">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="0c645-436">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c645-436">**VT\_BOOL**</span></span> | <span data-ttu-id="0c645-437">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="0c645-437">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="0c645-438">Value</span><span class="sxs-lookup"><span data-stu-id="0c645-438">Value</span></span>              | <span data-ttu-id="0c645-439">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c645-439">Description</span></span>                |
|--------------------|----------------------------|
| <span data-ttu-id="0c645-440">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="0c645-440">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="0c645-441">Modo secuencial (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="0c645-441">Sequential mode (default).</span></span> |
| <span data-ttu-id="0c645-442">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="0c645-442">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="0c645-443">Modo progresivo.</span><span class="sxs-lookup"><span data-stu-id="0c645-443">Progressive mode.</span></span>          |



 

### <a name="quality"></a><span data-ttu-id="0c645-444">Calidad</span><span class="sxs-lookup"><span data-stu-id="0c645-444">Quality</span></span>

<span data-ttu-id="0c645-445">Establece la calidad de compresión.</span><span class="sxs-lookup"><span data-stu-id="0c645-445">Sets the compression quality.</span></span>



| <span data-ttu-id="0c645-446">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-446">Data type</span></span> | <span data-ttu-id="0c645-447">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-447">VARTYPE</span></span>     | <span data-ttu-id="0c645-448">Intervalo</span><span class="sxs-lookup"><span data-stu-id="0c645-448">Range</span></span> | <span data-ttu-id="0c645-449">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-449">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="0c645-450">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="0c645-450">**UCHAR**</span></span> | <span data-ttu-id="0c645-451">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="0c645-451">**VT\_UI1**</span></span> | <span data-ttu-id="0c645-452">de 1 a 255</span><span class="sxs-lookup"><span data-stu-id="0c645-452">1–255</span></span> | <span data-ttu-id="0c645-453">1</span><span class="sxs-lookup"><span data-stu-id="0c645-453">1</span></span>       |



 

<span data-ttu-id="0c645-454">El valor 1 indica el modo sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="0c645-454">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="0c645-455">Aumentar los valores produce mayores proporciones de compresión y una calidad de imagen inferior.</span><span class="sxs-lookup"><span data-stu-id="0c645-455">Increasing values result in higher compression ratios and lower image quality.</span></span>

<span data-ttu-id="0c645-456">Si establece esta propiedad, establezca también [UseCodecOptions](#usecodecoptions) en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0c645-456">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="streamonly"></a><span data-ttu-id="0c645-457">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="0c645-457">StreamOnly</span></span>

<span data-ttu-id="0c645-458">Habilita o deshabilita el modo de solo transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="0c645-458">Enables or disables stream-only mode.</span></span>



| <span data-ttu-id="0c645-459">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-459">Data type</span></span>         | <span data-ttu-id="0c645-460">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-460">VARTYPE</span></span>      | <span data-ttu-id="0c645-461">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-461">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="0c645-462">**VARIANTE \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c645-462">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="0c645-463">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c645-463">**VT\_BOOL**</span></span> | <span data-ttu-id="0c645-464">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="0c645-464">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="0c645-465">Value</span><span class="sxs-lookup"><span data-stu-id="0c645-465">Value</span></span>              | <span data-ttu-id="0c645-466">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c645-466">Description</span></span>                                                            |
|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="0c645-467">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="0c645-467">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="0c645-468">El codificador genera el flujo de imágenes sin formato sin metadatos.</span><span class="sxs-lookup"><span data-stu-id="0c645-468">The encoder outputs the raw image stream without metadata.</span></span>             |
| <span data-ttu-id="0c645-469">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="0c645-469">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="0c645-470">El codificador genera el formato de contenedor (flujo de imagen más metadatos).</span><span class="sxs-lookup"><span data-stu-id="0c645-470">The encoder outputs the container format (image stream plus metadata).</span></span> |



 

### <a name="subsampling"></a><span data-ttu-id="0c645-471">Un submuestreo</span><span class="sxs-lookup"><span data-stu-id="0c645-471">Subsampling</span></span>

<span data-ttu-id="0c645-472">Establece el submuestreo de croma.</span><span class="sxs-lookup"><span data-stu-id="0c645-472">Sets the chroma subsampling.</span></span> <span data-ttu-id="0c645-473">Esta propiedad solo se aplica a las imágenes RGB.</span><span class="sxs-lookup"><span data-stu-id="0c645-473">This property applies only to RGB images.</span></span>



| <span data-ttu-id="0c645-474">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-474">Data type</span></span> | <span data-ttu-id="0c645-475">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-475">VARTYPE</span></span>     | <span data-ttu-id="0c645-476">Intervalo</span><span class="sxs-lookup"><span data-stu-id="0c645-476">Range</span></span> | <span data-ttu-id="0c645-477">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-477">Default</span></span>                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| <span data-ttu-id="0c645-478">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="0c645-478">**UCHAR**</span></span> | <span data-ttu-id="0c645-479">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="0c645-479">**VT\_UI1**</span></span> | <span data-ttu-id="0c645-480">0 – 3</span><span class="sxs-lookup"><span data-stu-id="0c645-480">0–3</span></span>   | <span data-ttu-id="0c645-481">3 Si [ImageQuality](#imagequality) > 0,8; de lo contrario 1</span><span class="sxs-lookup"><span data-stu-id="0c645-481">3 if [ImageQuality](#imagequality) > 0.8; otherwise 1</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c645-482">Value</span><span class="sxs-lookup"><span data-stu-id="0c645-482">Value</span></span></th>
<th><span data-ttu-id="0c645-483">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c645-483">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c645-484">3</span><span class="sxs-lookup"><span data-stu-id="0c645-484">3</span></span></td>
<td><span data-ttu-id="0c645-485">codificación 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="0c645-485">4:4:4 encoding.</span></span> <span data-ttu-id="0c645-486">Conserva la resolución de croma completa.</span><span class="sxs-lookup"><span data-stu-id="0c645-486">Preserves full chroma resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c645-487">2</span><span class="sxs-lookup"><span data-stu-id="0c645-487">2</span></span></td>
<td><span data-ttu-id="0c645-488">codificación 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="0c645-488">4:2:2 encoding.</span></span> <span data-ttu-id="0c645-489">La resolución de croma es 1/2 de la resolución de luminancia.</span><span class="sxs-lookup"><span data-stu-id="0c645-489">Chroma resolution is ½ of luminance resolution.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c645-490">1</span><span class="sxs-lookup"><span data-stu-id="0c645-490">1</span></span></td>
<td><span data-ttu-id="0c645-491">codificación 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="0c645-491">4:2:0 encoding.</span></span> <span data-ttu-id="0c645-492">La resolución de croma es 1/4 de la resolución de luminancia.</span><span class="sxs-lookup"><span data-stu-id="0c645-492">Chroma resolution is ¼ of luminance resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c645-493">0</span><span class="sxs-lookup"><span data-stu-id="0c645-493">0</span></span></td>
<td><span data-ttu-id="0c645-494">Codificación 4:0:0.</span><span class="sxs-lookup"><span data-stu-id="0c645-494">4:0:0 encoding.</span></span> <span data-ttu-id="0c645-495">Descarta todos los valores de croma y conserva solo la luminancia.</span><span class="sxs-lookup"><span data-stu-id="0c645-495">Discards all chroma values and preserves luminance only.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="0c645-496">No se recomienda este modo, ya que el códec utiliza una definición ligeramente modificada de luminancia para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0c645-496">This mode is not recommended, because the codec uses a slightly modified definition of luminance to improve performance.</span></span> <span data-ttu-id="0c645-497">En su lugar, es mejor convertir la imagen en monocromo antes de la codificación.</span><span class="sxs-lookup"><span data-stu-id="0c645-497">Instead, it is better to convert the image to monochrome before encoding.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0c645-498">4:2:2 y 4:2:0 conservar el detalle de luminancia a costa de los detalles de color.</span><span class="sxs-lookup"><span data-stu-id="0c645-498">4:2:2 and 4:2:0 preserve luminance detail at the expense of color detail.</span></span>

<span data-ttu-id="0c645-499">Si establece esta propiedad, establezca también [UseCodecOptions](#usecodecoptions) en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0c645-499">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="usecodecoptions"></a><span data-ttu-id="0c645-500">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="0c645-500">UseCodecOptions</span></span>

<span data-ttu-id="0c645-501">Especifica si se deben usar las propiedades de [calidad](#image-quality-settings), [superposición](#overlap)y [submuestreo](#subsampling) en lugar de la propiedad [ImageQuality](#imagequality) genérica.</span><span class="sxs-lookup"><span data-stu-id="0c645-501">Specifies whether to use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties instead of the generic [ImageQuality](#imagequality) property.</span></span>



| <span data-ttu-id="0c645-502">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-502">Data type</span></span>         | <span data-ttu-id="0c645-503">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-503">VARTYPE</span></span>      | <span data-ttu-id="0c645-504">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-504">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="0c645-505">**VARIANTE \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c645-505">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="0c645-506">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0c645-506">**VT\_BOOL**</span></span> | <span data-ttu-id="0c645-507">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="0c645-507">**VARIANT\_FALSE**</span></span> |



 

### <a name="verticaltileslices"></a><span data-ttu-id="0c645-508">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="0c645-508">VerticalTileSlices</span></span>

<span data-ttu-id="0c645-509">Establece el número de mosaicos horizontales.</span><span class="sxs-lookup"><span data-stu-id="0c645-509">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="0c645-510">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c645-510">Data type</span></span>  | <span data-ttu-id="0c645-511">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c645-511">VARTYPE</span></span>     | <span data-ttu-id="0c645-512">Intervalo</span><span class="sxs-lookup"><span data-stu-id="0c645-512">Range</span></span>  | <span data-ttu-id="0c645-513">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c645-513">Default</span></span>                       |
|------------|-------------|--------|-------------------------------|
| <span data-ttu-id="0c645-514">**USHORT**</span><span class="sxs-lookup"><span data-stu-id="0c645-514">**USHORT**</span></span> | <span data-ttu-id="0c645-515">**VT \_ UI2**</span><span class="sxs-lookup"><span data-stu-id="0c645-515">**VT\_UI2**</span></span> | <span data-ttu-id="0c645-516">0 – 4095</span><span class="sxs-lookup"><span data-stu-id="0c645-516">0–4095</span></span> | <span data-ttu-id="0c645-517">(alto de imagen – 1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="0c645-517">(image height – 1) >> 8</span></span> |



 

<span data-ttu-id="0c645-518">El valor es el número de subdivisiones verticales; es decir, el número de mosaicos verticales-1.</span><span class="sxs-lookup"><span data-stu-id="0c645-518">The value is the number of vertical subdivisions; that is, the number of vertical tiles – 1.</span></span>

## <a name="supported-color-formats"></a><span data-ttu-id="0c645-519">Formatos de color admitidos</span><span class="sxs-lookup"><span data-stu-id="0c645-519">Supported Color Formats</span></span>

<span data-ttu-id="0c645-520">Para obtener más información sobre estos formatos, vea [formatos de píxeles nativos](-wic-codec-native-pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="0c645-520">For more information about these formats, see [Native Pixel Formats](-wic-codec-native-pixel-formats.md).</span></span>

-   <span data-ttu-id="0c645-521">**Formatos RGB enteros**</span><span class="sxs-lookup"><span data-stu-id="0c645-521">**Integer RGB formats**</span></span>
    -   <span data-ttu-id="0c645-522">GUID \_ WICPixelFormat24bppRGB</span><span class="sxs-lookup"><span data-stu-id="0c645-522">GUID\_WICPixelFormat24bppRGB</span></span>
    -   <span data-ttu-id="0c645-523">GUID \_ WICPixelFormat24bppBGR</span><span class="sxs-lookup"><span data-stu-id="0c645-523">GUID\_WICPixelFormat24bppBGR</span></span>
    -   <span data-ttu-id="0c645-524">GUID \_ WICPixelFormat32bppBGR</span><span class="sxs-lookup"><span data-stu-id="0c645-524">GUID\_WICPixelFormat32bppBGR</span></span>
    -   <span data-ttu-id="0c645-525">GUID \_ WICPixelFormat48bppRGB</span><span class="sxs-lookup"><span data-stu-id="0c645-525">GUID\_WICPixelFormat48bppRGB</span></span>
    -   <span data-ttu-id="0c645-526">GUID \_ WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="0c645-526">GUID\_WICPixelFormat32bppBGRA</span></span>
    -   <span data-ttu-id="0c645-527">GUID \_ WICPixelFormat64bppRGBA</span><span class="sxs-lookup"><span data-stu-id="0c645-527">GUID\_WICPixelFormat64bppRGBA</span></span>
    -   <span data-ttu-id="0c645-528">GUID \_ WICPixelFormat32bppPBGRA</span><span class="sxs-lookup"><span data-stu-id="0c645-528">GUID\_WICPixelFormat32bppPBGRA</span></span>
    -   <span data-ttu-id="0c645-529">GUID \_ WICPixelFormat64bppPRGBA</span><span class="sxs-lookup"><span data-stu-id="0c645-529">GUID\_WICPixelFormat64bppPRGBA</span></span>
-   <span data-ttu-id="0c645-530">**Formatos RGB de punto fijo**</span><span class="sxs-lookup"><span data-stu-id="0c645-530">**Fixed-point RGB formats**</span></span>
    -   <span data-ttu-id="0c645-531">GUID \_ WICPixelFormat48bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="0c645-531">GUID\_WICPixelFormat48bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="0c645-532">GUID \_ WICPixelFormat64bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="0c645-532">GUID\_WICPixelFormat64bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="0c645-533">GUID \_ WICPixelFormat96bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="0c645-533">GUID\_WICPixelFormat96bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="0c645-534">GUID \_ WICPixelFormat128bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="0c645-534">GUID\_WICPixelFormat128bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="0c645-535">GUID \_ WICPixelFormat128bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="0c645-535">GUID\_WICPixelFormat128bppRGBAFixedPoint</span></span>
-   <span data-ttu-id="0c645-536">**Formatos RGB de punto flotante**</span><span class="sxs-lookup"><span data-stu-id="0c645-536">**Floating-point RGB formats**</span></span>
    -   <span data-ttu-id="0c645-537">GUID \_ WICPixelFormat48bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="0c645-537">GUID\_WICPixelFormat48bppRGBHalf</span></span>
    -   <span data-ttu-id="0c645-538">GUID \_ WICPixelFormat64bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="0c645-538">GUID\_WICPixelFormat64bppRGBHalf</span></span>
    -   <span data-ttu-id="0c645-539">GUID \_ WICPixelFormat128bppRGBFloat</span><span class="sxs-lookup"><span data-stu-id="0c645-539">GUID\_WICPixelFormat128bppRGBFloat</span></span>
    -   <span data-ttu-id="0c645-540">GUID \_ WICPixelFormat64bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="0c645-540">GUID\_WICPixelFormat64bppRGBAFixedPoint</span></span>
    -   <span data-ttu-id="0c645-541">GUID \_ WICPixelFormat64bppRGBAHalf</span><span class="sxs-lookup"><span data-stu-id="0c645-541">GUID\_WICPixelFormat64bppRGBAHalf</span></span>
    -   <span data-ttu-id="0c645-542">GUID \_ WICPixelFormat128bppRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="0c645-542">GUID\_WICPixelFormat128bppRGBAFloat</span></span>
    -   <span data-ttu-id="0c645-543">GUID \_ WICPixelFormat128bppPRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="0c645-543">GUID\_WICPixelFormat128bppPRGBAFloat</span></span>
-   <span data-ttu-id="0c645-544">**Formatos de escala de grises**</span><span class="sxs-lookup"><span data-stu-id="0c645-544">**Grayscale formats**</span></span>
    -   <span data-ttu-id="0c645-545">GUID \_ WICPixelFormat8bppGray</span><span class="sxs-lookup"><span data-stu-id="0c645-545">GUID\_WICPixelFormat8bppGray</span></span>
    -   <span data-ttu-id="0c645-546">GUID \_ WICPixelFormat16bppGray</span><span class="sxs-lookup"><span data-stu-id="0c645-546">GUID\_WICPixelFormat16bppGray</span></span>
    -   <span data-ttu-id="0c645-547">GUID \_ WICPixelFormat16bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="0c645-547">GUID\_WICPixelFormat16bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="0c645-548">GUID \_ WICPixelFormat16bppGrayHalf</span><span class="sxs-lookup"><span data-stu-id="0c645-548">GUID\_WICPixelFormat16bppGrayHalf</span></span>
    -   <span data-ttu-id="0c645-549">GUID \_ WICPixelFormat32bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="0c645-549">GUID\_WICPixelFormat32bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="0c645-550">GUID \_ WICPixelFormat32bppGrayFloat</span><span class="sxs-lookup"><span data-stu-id="0c645-550">GUID\_WICPixelFormat32bppGrayFloat</span></span>
-   <span data-ttu-id="0c645-551">**Formatos empaquetados**</span><span class="sxs-lookup"><span data-stu-id="0c645-551">**Packed formats**</span></span>
    -   <span data-ttu-id="0c645-552">GUID \_ WICPixelFormat16bppBGR555</span><span class="sxs-lookup"><span data-stu-id="0c645-552">GUID\_WICPixelFormat16bppBGR555</span></span>
    -   <span data-ttu-id="0c645-553">GUID \_ WICPixelFormat16bppBGR565</span><span class="sxs-lookup"><span data-stu-id="0c645-553">GUID\_WICPixelFormat16bppBGR565</span></span>
    -   <span data-ttu-id="0c645-554">GUID \_ WICPixelFormat32bppBGR101010</span><span class="sxs-lookup"><span data-stu-id="0c645-554">GUID\_WICPixelFormat32bppBGR101010</span></span>
    -   <span data-ttu-id="0c645-555">GUID \_ WICPixelFormat32bppRGBE</span><span class="sxs-lookup"><span data-stu-id="0c645-555">GUID\_WICPixelFormat32bppRGBE</span></span>
-   <span data-ttu-id="0c645-556">**Formatos CMYK**</span><span class="sxs-lookup"><span data-stu-id="0c645-556">**CMYK formats**</span></span>
    -   <span data-ttu-id="0c645-557">GUID \_ WICPixelFormat40bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="0c645-557">GUID\_WICPixelFormat40bppCMYKAlpha</span></span>
    -   <span data-ttu-id="0c645-558">GUID \_ WICPixelFormat64bppCMYK</span><span class="sxs-lookup"><span data-stu-id="0c645-558">GUID\_WICPixelFormat64bppCMYK</span></span>
    -   <span data-ttu-id="0c645-559">GUID \_ WICPixelFormat80bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="0c645-559">GUID\_WICPixelFormat80bppCMYKAlpha</span></span>
-   <span data-ttu-id="0c645-560">**Formatos de N canales**</span><span class="sxs-lookup"><span data-stu-id="0c645-560">**N-channel formats**</span></span>
    -   <span data-ttu-id="0c645-561">GUID \_ WICPixelFormat32bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="0c645-561">GUID\_WICPixelFormat32bpp4Channels</span></span>
    -   <span data-ttu-id="0c645-562">GUID \_ WICPixelFormat40bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="0c645-562">GUID\_WICPixelFormat40bpp5Channels</span></span>
    -   <span data-ttu-id="0c645-563">GUID \_ WICPixelFormat48bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="0c645-563">GUID\_WICPixelFormat48bpp6Channels</span></span>
    -   <span data-ttu-id="0c645-564">GUID \_ WICPixelFormat56bpp7Channels</span><span class="sxs-lookup"><span data-stu-id="0c645-564">GUID\_WICPixelFormat56bpp7Channels</span></span>
    -   <span data-ttu-id="0c645-565">GUID \_ WICPixelFormat64bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="0c645-565">GUID\_WICPixelFormat64bpp8Channels</span></span>
    -   <span data-ttu-id="0c645-566">GUID \_ WICPixelFormat32bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0c645-566">GUID\_WICPixelFormat32bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="0c645-567">GUID \_ WICPixelFormat40bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0c645-567">GUID\_WICPixelFormat40bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="0c645-568">GUID \_ WICPixelFormat48bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0c645-568">GUID\_WICPixelFormat48bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="0c645-569">GUID \_ WICPixelFormat56bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0c645-569">GUID\_WICPixelFormat56bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="0c645-570">GUID \_ WICPixelFormat64bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0c645-570">GUID\_WICPixelFormat64bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="0c645-571">GUID \_ WICPixelFormat72bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0c645-571">GUID\_WICPixelFormat72bpp8ChannelsAlpha</span></span>
    -   <span data-ttu-id="0c645-572">GUID \_ WICPixelFormat48bpp3Channels</span><span class="sxs-lookup"><span data-stu-id="0c645-572">GUID\_WICPixelFormat48bpp3Channels</span></span>
    -   <span data-ttu-id="0c645-573">GUID \_ WICPixelFormat64bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="0c645-573">GUID\_WICPixelFormat64bpp4Channels</span></span>
    -   <span data-ttu-id="0c645-574">GUID \_ WICPixelFormat80bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="0c645-574">GUID\_WICPixelFormat80bpp5Channels</span></span>
    -   <span data-ttu-id="0c645-575">GUID \_ WICPixelFormat96bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="0c645-575">GUID\_WICPixelFormat96bpp6Channels</span></span>
    -   <span data-ttu-id="0c645-576">GUID \_ WICPixelFormat128bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="0c645-576">GUID\_WICPixelFormat128bpp8Channels</span></span>
    -   <span data-ttu-id="0c645-577">GUID \_ WICPixelFormat64bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0c645-577">GUID\_WICPixelFormat64bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="0c645-578">GUID \_ WICPixelFormat80bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0c645-578">GUID\_WICPixelFormat80bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="0c645-579">GUID \_ WICPixelFormat96bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0c645-579">GUID\_WICPixelFormat96bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="0c645-580">GUID \_ WICPixelFormat112bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0c645-580">GUID\_WICPixelFormat112bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="0c645-581">GUID \_ WICPixelFormat128bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0c645-581">GUID\_WICPixelFormat128bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="0c645-582">GUID \_ WICPixelFormat144bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0c645-582">GUID\_WICPixelFormat144bpp8ChannelsAlpha</span></span>

 

 
