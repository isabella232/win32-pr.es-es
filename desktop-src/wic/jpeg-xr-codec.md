---
description: El códec XR JPEG nativo está disponible a través de Windows Imaging Component (WIC). El formato JPEG XR, compatible con el códec, está diseñado para la fotografía digital profesional y de consumidor.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: Introducción al códec JPEG XR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d39608535f9be09821d8db3615641a84fd95a6
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444475"
---
# <a name="jpeg-xr-codec-overview"></a><span data-ttu-id="969de-104">Introducción al códec JPEG XR</span><span class="sxs-lookup"><span data-stu-id="969de-104">JPEG XR Codec Overview</span></span>

<span data-ttu-id="969de-105">El códec XR JPEG nativo está disponible a través de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="969de-105">The native JPEG XR codec is available through the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="969de-106">El formato JPEG XR, compatible con el códec, está diseñado para la fotografía digital profesional y de consumidor.</span><span class="sxs-lookup"><span data-stu-id="969de-106">The JPEG XR format, which the codec supports, is designed for consumer and professional digital photography.</span></span>

<span data-ttu-id="969de-107">El formato JPEG XR puede lograr hasta el doble de eficacia de compresión del formato JPEG original, con artefactos de compresión menos evidentes.</span><span class="sxs-lookup"><span data-stu-id="969de-107">The JPEG XR format can achieve up to twice the compression efficiency of the original JPEG format, with less noticeable compression artifacts.</span></span> <span data-ttu-id="969de-108">Las características de JPEG XR incluyen:</span><span class="sxs-lookup"><span data-stu-id="969de-108">Features of JPEG XR include:</span></span>

-   <span data-ttu-id="969de-109">Compatibilidad con imágenes monocromáticas, RGB, GRAMA y n canales</span><span class="sxs-lookup"><span data-stu-id="969de-109">Support for monochrome, RGB, CMYK, and n-channel images</span></span>
-   <span data-ttu-id="969de-110">Formatos enteros de 8, 16 y 32 bits</span><span class="sxs-lookup"><span data-stu-id="969de-110">8-, 16-, and 32-bit integer formats</span></span>
-   <span data-ttu-id="969de-111">Rango dinámico alto, formatos de gama ancha, con valores de color de punto fijo o punto flotante</span><span class="sxs-lookup"><span data-stu-id="969de-111">High dynamic range, wide-gamut formats, using fixed point or floating point color values</span></span>
-   <span data-ttu-id="969de-112">Decoding progresiva</span><span class="sxs-lookup"><span data-stu-id="969de-112">Progressive decoding</span></span>
-   <span data-ttu-id="969de-113">Codificación sin pérdida o pérdida de datos con el mismo algoritmo de compresión</span><span class="sxs-lookup"><span data-stu-id="969de-113">Lossy or lossless encoding using the same compression algorithm</span></span>
-   <span data-ttu-id="969de-114">Compatibilidad con la decodificación de regiones de interés en imágenes de gran tamaño</span><span class="sxs-lookup"><span data-stu-id="969de-114">Support for decoding of regions of interest in large images</span></span>

<span data-ttu-id="969de-115">El formato JPEG XR se define en los siguientes documentos de estándar:</span><span class="sxs-lookup"><span data-stu-id="969de-115">The JPEG XR format is defined in the following standards documents:</span></span>

-   <span data-ttu-id="969de-116">ITU-T T.832: tecnología de la información: sistema de codificación de imágenes *JPEG XR: especificación de codificación de imágenes*</span><span class="sxs-lookup"><span data-stu-id="969de-116">ITU-T T.832: *Information technology – JPEG XR image coding system – Image coding specification*</span></span>
-   <span data-ttu-id="969de-117">ISO/IEC 29199-2:2010: Tecnología de la información: sistema de codificación de imágenes *JPEG XR, parte 2:* Especificación de codificación de imágenes</span><span class="sxs-lookup"><span data-stu-id="969de-117">ISO/IEC 29199-2:2010: *Information technology — JPEG XR image coding system — Part 2: Image coding specification*</span></span>

<span data-ttu-id="969de-118">El estándar JPEG XR se basa en gran medida en el formato [HD Photo,](hdphoto-format-overview.md) pero hay algunas diferencias entre los dos formatos.</span><span class="sxs-lookup"><span data-stu-id="969de-118">The JPEG XR standard is largely based on the [HD Photo](hdphoto-format-overview.md) format, but there are some differences between the two formats.</span></span> <span data-ttu-id="969de-119">En Windows 8, el códec HD Photo se ha actualizado para admitir JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="969de-119">In Windows 8, the HD Photo codec has been updated to support JPEG XR.</span></span> <span data-ttu-id="969de-120">El codificador ahora siempre genera una secuencia de bits compatible con JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="969de-120">The encoder now always outputs a JPEG XR–compliant bit stream.</span></span> <span data-ttu-id="969de-121">El descodificador puede descodificar imágenes JPEG XR y HD Photo.</span><span class="sxs-lookup"><span data-stu-id="969de-121">The decoder can decode both JPEG XR and HD Photo images.</span></span>

<span data-ttu-id="969de-122">Se han realizado mejoras sustanciales de rendimiento en relación con el códec HD Photo con el códec JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="969de-122">Substantial performance improvements, in relation to the HD Photo codec, have been made to the JPEG XR codec.</span></span> <span data-ttu-id="969de-123">Por ejemplo, se ha mejorado la decodificación de imágenes de sub resolución, como la generación de miniaturas, así como lacoding de imágenes de baja resolución.</span><span class="sxs-lookup"><span data-stu-id="969de-123">For example, sub-resolution image decoding, such as thumbnail generation, has been improved, as well as low-resolution image decoding.</span></span> <span data-ttu-id="969de-124">Se recomienda usar el formato JPEG XR en lugar del formato HD Photo.</span><span class="sxs-lookup"><span data-stu-id="969de-124">It is recommended that you use the JPEG XR format instead of the HD Photo format.</span></span>

## <a name="codec-information"></a><span data-ttu-id="969de-125">Información del códec</span><span class="sxs-lookup"><span data-stu-id="969de-125">Codec Information</span></span>



|      <span data-ttu-id="969de-126">Componente</span><span class="sxs-lookup"><span data-stu-id="969de-126">Component</span></span>      |    <span data-ttu-id="969de-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="969de-127">Description</span></span>                                                          |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="969de-128">Extensión de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="969de-128">File name extension</span></span> | <span data-ttu-id="969de-129">"jxr" y "wdp"</span><span class="sxs-lookup"><span data-stu-id="969de-129">"jxr" and "wdp"</span></span>                                                         |
| <span data-ttu-id="969de-130">GUID de contenedor</span><span class="sxs-lookup"><span data-stu-id="969de-130">Container GUID</span></span>      | <span data-ttu-id="969de-131">**GUID \_ ContainerFormatWmp**</span><span class="sxs-lookup"><span data-stu-id="969de-131">**GUID\_ContainerFormatWmp**</span></span>                                            |
| <span data-ttu-id="969de-132">GUID del descodificador</span><span class="sxs-lookup"><span data-stu-id="969de-132">Decoder GUID</span></span>        | <span data-ttu-id="969de-133">**CLSID \_ WICWmpDecoder**</span><span class="sxs-lookup"><span data-stu-id="969de-133">**CLSID\_WICWmpDecoder**</span></span>                                                |
| <span data-ttu-id="969de-134">GUID del codificador</span><span class="sxs-lookup"><span data-stu-id="969de-134">Encoder GUID</span></span>        | <span data-ttu-id="969de-135">**CLSID \_ WICWmpEncoder**</span><span class="sxs-lookup"><span data-stu-id="969de-135">**CLSID\_WICWmpEncoder**</span></span>                                                |
| <span data-ttu-id="969de-136">Compatibilidad con perfiles</span><span class="sxs-lookup"><span data-stu-id="969de-136">Profile Support</span></span>     | <span data-ttu-id="969de-137">El codificador y el descodificador admiten hasta el perfil principal y hasta el nivel 128.</span><span class="sxs-lookup"><span data-stu-id="969de-137">The encoder and decoder support up to Main Profile and up to level 128.</span></span> |



 

## <a name="codec-features"></a><span data-ttu-id="969de-138">Características del códec</span><span class="sxs-lookup"><span data-stu-id="969de-138">Codec Features</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="969de-139">Alto rango dinámico</span><span class="sxs-lookup"><span data-stu-id="969de-139">High Dynamic Range</span></span>

<span data-ttu-id="969de-140">JPEG XR admite imágenes de rango altamente dinámicas, mediante colores de punto flotante o de punto fijo.</span><span class="sxs-lookup"><span data-stu-id="969de-140">JPEG XR supports high-dynamic range images, using floating-point or fixed-point colors.</span></span> <span data-ttu-id="969de-141">En estos formatos de color, el intervalo numérico de un píxel es mayor que el intervalo visible, por lo que puede ajustar los colores por encima o por debajo del intervalo visible durante las fases de procesamiento intermedio.</span><span class="sxs-lookup"><span data-stu-id="969de-141">In these color formats, the numerical range of a pixel is larger than the visible range, so you can adjust colors above or below the visible range during intermediate processing stages.</span></span>

-   <span data-ttu-id="969de-142">Punto fijo: en una representación de punto fijo, 0 representa el negro y 1,0 representa la saturación máxima.</span><span class="sxs-lookup"><span data-stu-id="969de-142">Fixed-point: In a fixed-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="969de-143">El códec JPEG XR admite formatos de punto fijo de 16 y 32 bits.</span><span class="sxs-lookup"><span data-stu-id="969de-143">The JPEG XR codec supports both 16-bit and 32-bit fixed-point formats.</span></span> <span data-ttu-id="969de-144">Para 16 bits, 1,0 = 0x2000h, que proporciona 13 bits para el intervalo visible \[ 0...1. \]</span><span class="sxs-lookup"><span data-stu-id="969de-144">For 16-bit, 1.0 = 0x2000h, which gives 13 bits for the visible range \[0...1\].</span></span> <span data-ttu-id="969de-145">El intervalo total es de –4,0 a +3,999 y se asigna linealmente.</span><span class="sxs-lookup"><span data-stu-id="969de-145">The total range is –4.0 to +3.999, and is mapped linearly.</span></span> <span data-ttu-id="969de-146">Para 32 bits, 1,0 = 0x01000000 h, el intervalo visible es de 24 bits y el intervalo total es de -128 a +127,999.</span><span class="sxs-lookup"><span data-stu-id="969de-146">For 32-bit, 1.0 = 0x01000000h, the visible range is 24 bits, and the total range is –128 to +127.999.</span></span>
-   <span data-ttu-id="969de-147">Punto flotante: en una representación de punto flotante, 0 representa el negro y 1,0 representa la saturación máxima.</span><span class="sxs-lookup"><span data-stu-id="969de-147">Floating-point: In a floating-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="969de-148">El códec JPEG XR admite formatos de punto flotante de 16 y 32 bits.</span><span class="sxs-lookup"><span data-stu-id="969de-148">The JPEG XR codec supports both 16-bit and 32-bit floating-point formats.</span></span>

### <a name="tiles"></a><span data-ttu-id="969de-149">Iconos</span><span class="sxs-lookup"><span data-stu-id="969de-149">Tiles</span></span>

<span data-ttu-id="969de-150">Un marco se puede particionar en subregiones rectangulares *denominadas iconos*.</span><span class="sxs-lookup"><span data-stu-id="969de-150">A frame can be partitioned into rectangular subregions called *tiles*.</span></span> <span data-ttu-id="969de-151">Un icono es un área de una imagen que contiene matrices rectangulares de macrobloqueos.</span><span class="sxs-lookup"><span data-stu-id="969de-151">A tile is an area of a image that contains rectangular arrays of macroblocks.</span></span> <span data-ttu-id="969de-152">Los iconos permiten descodificar las regiones de la imagen sin procesar toda la imagen.</span><span class="sxs-lookup"><span data-stu-id="969de-152">Tiles enable regions of the image to be decoded without processing the entire image.</span></span>

<span data-ttu-id="969de-153">Durante la codificación, seleccione el número de iconos estableciendo las propiedades **HorizontalTileSlices** y **VerticalTileSlices.**</span><span class="sxs-lookup"><span data-stu-id="969de-153">During encoding, select the number of tiles by setting the **HorizontalTileSlices** and **VerticalTileSlices** properties.</span></span> <span data-ttu-id="969de-154">El tamaño mínimo del icono es de 16 × 16 píxeles.</span><span class="sxs-lookup"><span data-stu-id="969de-154">The minimum tile size is 16 × 16 pixels.</span></span> <span data-ttu-id="969de-155">El codificador ajusta el número de iconos para mantener esta restricción.</span><span class="sxs-lookup"><span data-stu-id="969de-155">The encoder adjusts the number of tiles to maintain this restriction.</span></span> <span data-ttu-id="969de-156">Hay una sobrecarga de almacenamiento y procesamiento asociada a cada icono, por lo que debe tener en cuenta el número de iconos necesarios para escenarios concretos.</span><span class="sxs-lookup"><span data-stu-id="969de-156">There is storage and processing overhead associated with each tile, so you should consider the number of tiles that are needed for particular scenarios.</span></span>

### <a name="image-stream-output"></a><span data-ttu-id="969de-157">Salida del flujo de imagen</span><span class="sxs-lookup"><span data-stu-id="969de-157">Image Stream Output</span></span>

<span data-ttu-id="969de-158">El estándar JPEG-XR define dos partes de un archivo JPEG-XR:</span><span class="sxs-lookup"><span data-stu-id="969de-158">The JPEG-XR standard defines two parts of a JPEG-XR file:</span></span>

-   <span data-ttu-id="969de-159">Secuencia de bits de imagen, definida en el cuerpo del estándar.</span><span class="sxs-lookup"><span data-stu-id="969de-159">The image bit stream, defined in the body of the standard.</span></span>
-   <span data-ttu-id="969de-160">Contenedor de imágenes.</span><span class="sxs-lookup"><span data-stu-id="969de-160">The image container.</span></span> <span data-ttu-id="969de-161">El archivo contiene metadatos Exif y XMP, y se define en el anexo A del estándar.</span><span class="sxs-lookup"><span data-stu-id="969de-161">The file contains Exif and XMP metadata, and is defined in Annex A of the standard.</span></span>

<span data-ttu-id="969de-162">Es posible, y lo permite el estándar, insertar la secuencia de imágenes dentro de otro tipo de contenedor de archivos.</span><span class="sxs-lookup"><span data-stu-id="969de-162">It is possible, and allowed by the standard, to embed the image stream inside another type of file container.</span></span> <span data-ttu-id="969de-163">El codificador admite un modo de solo secuencia, que genera la secuencia de bits de imagen sin procesar sin contenedor de imágenes.</span><span class="sxs-lookup"><span data-stu-id="969de-163">The encoder supports a stream-only mode, which outputs the raw image bit stream with no image container.</span></span> <span data-ttu-id="969de-164">Una aplicación puede almacenar la secuencia de bits en algún otro formato de contenedor.</span><span class="sxs-lookup"><span data-stu-id="969de-164">An application can store the bit stream in some other container format.</span></span>

<span data-ttu-id="969de-165">Para habilitar el modo de solo secuencia, establezca **la propiedad StreamOnly.**</span><span class="sxs-lookup"><span data-stu-id="969de-165">To enable stream-only mode, set the **StreamOnly** property.</span></span>

### <a name="image-quality-settings"></a><span data-ttu-id="969de-166">Configuración de calidad de imagen</span><span class="sxs-lookup"><span data-stu-id="969de-166">Image Quality Settings</span></span>

<span data-ttu-id="969de-167">Varias propiedades de códec controlan la calidad de la imagen de salida del codificador.</span><span class="sxs-lookup"><span data-stu-id="969de-167">Several codec properties control the quality of the output image from the encoder.</span></span>

-   <span data-ttu-id="969de-168">[ImageQuality es](#imagequality) una propiedad común entre códecs WIC.</span><span class="sxs-lookup"><span data-stu-id="969de-168">[ImageQuality](#imagequality) is a property common across WIC codecs.</span></span> <span data-ttu-id="969de-169">Especifica la calidad de la imagen como un valor de punto flotante único entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="969de-169">It specifies image quality as a single floating-point value from 0.0–1.0,</span></span>
-   <span data-ttu-id="969de-170">Las [propiedades Calidad,](#image-quality-settings) [Superposición](#overlap) [y Submuestreo](#subsampling) dan más control sobre la configuración de calidad.</span><span class="sxs-lookup"><span data-stu-id="969de-170">The [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties give more control over the quality settings.</span></span>

<span data-ttu-id="969de-171">Para usar las [propiedades Quality](#image-quality-settings), [Overlap](#overlap)y [Subsampling,](#subsampling) establezca la [propiedad UseCodecOptions](#usecodecoptions) en **VARIANT \_ TRUE.**</span><span class="sxs-lookup"><span data-stu-id="969de-171">To use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties, set the [UseCodecOptions](#usecodecoptions) property to **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="969de-172">Si [UseCodecOptions](#usecodecoptions) es **VARIANT \_ FALSE** **(VARIANT \_ FALSE** es el valor predeterminado), el codificador usa la [propiedad ImageQuality.](#imagequality)</span><span class="sxs-lookup"><span data-stu-id="969de-172">If [UseCodecOptions](#usecodecoptions) is **VARIANT\_FALSE** (**VARIANT\_FALSE** is the default) the encoder uses the [ImageQuality](#imagequality) property.</span></span> <span data-ttu-id="969de-173">El codificador asigna el valor de ImageQuality a [Quality](#image-quality-settings), [Overlap](#overlap)y [Subsampling](#subsampling) a través de una tabla de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="969de-173">The encoder maps the value of ImageQuality to [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) through a lookup table.</span></span>

<span data-ttu-id="969de-174">El codificador no admite la **propiedad CompressionQuality.**</span><span class="sxs-lookup"><span data-stu-id="969de-174">The encoder does not support the **CompressionQuality** property.</span></span>

### <a name="compressed-domain-transcode"></a><span data-ttu-id="969de-175">Transcodificación de dominio comprimido</span><span class="sxs-lookup"><span data-stu-id="969de-175">Compressed Domain Transcode</span></span>

<span data-ttu-id="969de-176">El códec JPEG XR puede realizar determinadas transformaciones de imagen sin realmente decodir los datos comprimidos y volver a codificar.</span><span class="sxs-lookup"><span data-stu-id="969de-176">The JPEG XR codec can perform certain image transformations without actually decoding the compressed data and re-encoding it.</span></span> <span data-ttu-id="969de-177">Las operaciones de dominio comprimido son muy eficaces y evitan cualquier pérdida de calidad adicional que sea típica al descodificar y volver a codificar una imagen comprimida por pérdida.</span><span class="sxs-lookup"><span data-stu-id="969de-177">Compressed domain operations are very efficient and avoid any additional quality loss that is typical when you decode and re-encode a lossy-compressed image.</span></span>

<span data-ttu-id="969de-178">Se admiten las siguientes operaciones de dominio comprimido:</span><span class="sxs-lookup"><span data-stu-id="969de-178">The following compressed domain operations are supported:</span></span>

-   <span data-ttu-id="969de-179">Recortar una región de la imagen.</span><span class="sxs-lookup"><span data-stu-id="969de-179">Crop a region of the image.</span></span>
-   <span data-ttu-id="969de-180">Girar o voltear la imagen.</span><span class="sxs-lookup"><span data-stu-id="969de-180">Rotate or flip the image.</span></span>
-   <span data-ttu-id="969de-181">Descarte los datos de frecuencia para crear un archivo de imagen más pequeño.</span><span class="sxs-lookup"><span data-stu-id="969de-181">Discard frequency data to create a smaller image file.</span></span>
-   <span data-ttu-id="969de-182">Reorganizar la imagen entre el orden espacial y el orden de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="969de-182">Reorganize the image between spatial and frequency order.</span></span>

<span data-ttu-id="969de-183">El codificador JPEG XR usa la transcodificación de dominios comprimidos, si es posible, cuando la imagen de origen es una imagen JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="969de-183">The JPEG XR encoder uses compressed domain transcoding, if possible, when the source image is a JPEG XR image.</span></span> <span data-ttu-id="969de-184">Cuando el codificador realiza una operación de dominio comprimido, omite las siguientes propiedades de códec: [AlphaQuality,](#alphaquality) [ImageQuality,](#imagequality) [InterleavedAlpha,](#interleavedalpha) [Lossless](#lossless)[Overlap](#overlap)y [Quality](#image-quality-settings).</span><span class="sxs-lookup"><span data-stu-id="969de-184">When the encoder performs a compressed domain operation, it ignores the following codec properties: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha), [Lossless](#lossless)[Overlap](#overlap), and [Quality](#image-quality-settings).</span></span> <span data-ttu-id="969de-185">Si las [propiedades HorizontalTileSlices](/windows) y [VerticalTileSlices están presentes,](/windows) debe establecerlas en cero.</span><span class="sxs-lookup"><span data-stu-id="969de-185">If the [HorizontalTileSlices](/windows) and [VerticalTileSlices](/windows) properties are present, you must set them to zero.</span></span> <span data-ttu-id="969de-186">No se puede cambiar el tamaño de mosaico de una imagen como parte de una transcodificación de dominio comprimido.</span><span class="sxs-lookup"><span data-stu-id="969de-186">You cannot change the tile size of an image as part of a compressed domain transcode.</span></span>

<span data-ttu-id="969de-187">En la lista siguiente se describe cómo realizar las transformaciones de imagen.</span><span class="sxs-lookup"><span data-stu-id="969de-187">The follow list describes how to perform the image transformations.</span></span>

-   <span data-ttu-id="969de-188">Para recortar la imagen, establezca la región deseada en el [**parámetro WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) del **método WriteSource.**</span><span class="sxs-lookup"><span data-stu-id="969de-188">To crop the image, set the desired region in the [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) parameter of the **WriteSource** method.</span></span>
-   <span data-ttu-id="969de-189">Para girar o voltear la imagen, establezca la [propiedad BitmapTransform.](#bitmaptransform)</span><span class="sxs-lookup"><span data-stu-id="969de-189">To rotate or flip the image, set the [BitmapTransform](#bitmaptransform) property.</span></span>
-   <span data-ttu-id="969de-190">Para descartar los datos de frecuencia de la imagen, establezca [la propiedad ImageDataDiscard.](#imagedatadiscard)</span><span class="sxs-lookup"><span data-stu-id="969de-190">To discard frequency data in the image, set the [ImageDataDiscard](#imagedatadiscard) property.</span></span> <span data-ttu-id="969de-191">Para descartar los datos de frecuencia en el canal alfa, establezca la [propiedad AlphaDataDiscard.](#alphadatadiscard)</span><span class="sxs-lookup"><span data-stu-id="969de-191">To discard frequency data in the alpha channel, set the [AlphaDataDiscard](#alphadatadiscard) property.</span></span> <span data-ttu-id="969de-192">Descartar los datos de frecuencia reduce el tamaño del archivo codificado y puede reducir la resolución.</span><span class="sxs-lookup"><span data-stu-id="969de-192">Discarding frequency data reduces the encoded file size and can reduce the resolution.</span></span>
-   <span data-ttu-id="969de-193">Para cambiar la organización de la imagen entre la frecuencia y el orden espacial, establezca la [propiedad FrequencyOrdering.](/windows)</span><span class="sxs-lookup"><span data-stu-id="969de-193">To change the image organization between frequency and spatial ordering, set the [FrequencyOrdering](/windows) property.</span></span>

<span data-ttu-id="969de-194">Para deshabilitar la transcodificación de dominio comprimido y forzar al codificador a volver a codificar la imagen, establezca [UseCodecOptions](#usecodecoptions) en **VARIANT \_ TRUE** y [establezca CompressedDomainTranscode](#compresseddomaintranscode) en **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="969de-194">To disable compressed domain transcode and force the encoder to re-encode the image, set the [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE** and set [CompressedDomainTranscode](#compresseddomaintranscode) to **VARIANT\_FALSE**.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="969de-195">Opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="969de-195">Encoder Options</span></span>

<span data-ttu-id="969de-196">Para establecer las propiedades de codificación, use la [**interfaz IPropertyBag2.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="969de-196">To set encoding properties, use the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface.</span></span> <span data-ttu-id="969de-197">Para obtener más información, vea Información general [sobre codificación.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="969de-197">For more information, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="969de-198">En la lista siguiente se especifican las opciones del codificador.</span><span class="sxs-lookup"><span data-stu-id="969de-198">The following list specifies the encoder options.</span></span>

-   [<span data-ttu-id="969de-199">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="969de-199">AlphaDataDiscard</span></span>](#alphadatadiscard)
-   [<span data-ttu-id="969de-200">AlphaQuality</span><span class="sxs-lookup"><span data-stu-id="969de-200">AlphaQuality</span></span>](#alphaquality)
-   [<span data-ttu-id="969de-201">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="969de-201">BitmapTransform</span></span>](#bitmaptransform)
-   [<span data-ttu-id="969de-202">CompressedDomainTranscode</span><span class="sxs-lookup"><span data-stu-id="969de-202">CompressedDomainTranscode</span></span>](#compresseddomaintranscode)
-   [<span data-ttu-id="969de-203">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="969de-203">FrequencyOrder</span></span>](#frequencyorder)
-   [<span data-ttu-id="969de-204">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="969de-204">HorizontalTileSlices</span></span>](#horizontaltileslices)
-   [<span data-ttu-id="969de-205">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="969de-205">IgnoreOverlap</span></span>](#ignoreoverlap)
-   [<span data-ttu-id="969de-206">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="969de-206">ImageDataDiscard</span></span>](#imagedatadiscard)
-   [<span data-ttu-id="969de-207">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="969de-207">ImageQuality</span></span>](#imagequality)
-   [<span data-ttu-id="969de-208">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="969de-208">InterleavedAlpha</span></span>](#interleavedalpha)
-   [<span data-ttu-id="969de-209">Lossless</span><span class="sxs-lookup"><span data-stu-id="969de-209">Lossless</span></span>](#lossless)
-   [<span data-ttu-id="969de-210">Traslapo</span><span class="sxs-lookup"><span data-stu-id="969de-210">Overlap</span></span>](#overlap)
-   [<span data-ttu-id="969de-211">ProgressiveMode</span><span class="sxs-lookup"><span data-stu-id="969de-211">ProgressiveMode</span></span>](#progressivemode)
-   [<span data-ttu-id="969de-212">Quality</span><span class="sxs-lookup"><span data-stu-id="969de-212">Quality</span></span>](#image-quality-settings)
-   [<span data-ttu-id="969de-213">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="969de-213">StreamOnly</span></span>](#streamonly)
-   [<span data-ttu-id="969de-214">Submuestreo</span><span class="sxs-lookup"><span data-stu-id="969de-214">Subsampling</span></span>](#subsampling)
-   [<span data-ttu-id="969de-215">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="969de-215">UseCodecOptions</span></span>](#usecodecoptions)
-   [<span data-ttu-id="969de-216">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="969de-216">VerticalTileSlices</span></span>](#verticaltileslices)

### <a name="alphadatadiscard"></a><span data-ttu-id="969de-217">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="969de-217">AlphaDataDiscard</span></span>

<span data-ttu-id="969de-218">Establece la cantidad de datos de frecuencia alfa que se descartarán durante una transcodificación de dominio comprimido.</span><span class="sxs-lookup"><span data-stu-id="969de-218">Sets the amount of alpha frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="969de-219">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-219">Data type</span></span> | <span data-ttu-id="969de-220">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-220">VARTYPE</span></span>     | <span data-ttu-id="969de-221">Intervalo</span><span class="sxs-lookup"><span data-stu-id="969de-221">Range</span></span> | <span data-ttu-id="969de-222">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-222">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="969de-223">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="969de-223">**UCHAR**</span></span> | <span data-ttu-id="969de-224">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="969de-224">**VT\_UI1**</span></span> | <span data-ttu-id="969de-225">0–4</span><span class="sxs-lookup"><span data-stu-id="969de-225">0–4</span></span>   | <span data-ttu-id="969de-226">Ninguno</span><span class="sxs-lookup"><span data-stu-id="969de-226">None</span></span>    |



 

<span data-ttu-id="969de-227">Esta propiedad solo se aplica si la propiedad [CompressedDomainTranscode](#compresseddomaintranscode) está establecida en **VARIANT \_ TRUE** y la imagen contiene un canal alfa plano o un canal alfa intercalado; de lo contrario, se omite.</span><span class="sxs-lookup"><span data-stu-id="969de-227">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and the image contains either a planar alpha channel or interleaved alpha channel; otherwise it is ignored.</span></span>

<span data-ttu-id="969de-228">En el caso de las imágenes que contienen un canal alfa plana, los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="969de-228">For images that contain a planar alpha channel, the following values are valid.</span></span>



| <span data-ttu-id="969de-229">Valor</span><span class="sxs-lookup"><span data-stu-id="969de-229">Value</span></span> | <span data-ttu-id="969de-230">Descripción</span><span class="sxs-lookup"><span data-stu-id="969de-230">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="969de-231">0</span><span class="sxs-lookup"><span data-stu-id="969de-231">0</span></span>     | <span data-ttu-id="969de-232">No se descartan datos de frecuencia de la imagen.</span><span class="sxs-lookup"><span data-stu-id="969de-232">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="969de-233">1</span><span class="sxs-lookup"><span data-stu-id="969de-233">1</span></span>     | <span data-ttu-id="969de-234">Los flexbits se descartan.</span><span class="sxs-lookup"><span data-stu-id="969de-234">The flexbits are discarded.</span></span> <span data-ttu-id="969de-235">Esto reduce arbitrariamente la calidad del canal alfa planar para la imagen transcodificada.</span><span class="sxs-lookup"><span data-stu-id="969de-235">This arbitrarily reduces the quality of the planar alpha channel for the transcoded image.</span></span> <span data-ttu-id="969de-236">, sin un cambio en la resolución efectiva.</span><span class="sxs-lookup"><span data-stu-id="969de-236">, without a change in the effective resolution.</span></span> <span data-ttu-id="969de-237">La reducción exacta del tamaño y la calidad del archivo depende de numerosos factores y no se puede especificar exactamente.</span><span class="sxs-lookup"><span data-stu-id="969de-237">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="969de-238">2</span><span class="sxs-lookup"><span data-stu-id="969de-238">2</span></span>     | <span data-ttu-id="969de-239">Se descarta la banda de datos de frecuencia de paso alto, incluidos los flexbits.</span><span class="sxs-lookup"><span data-stu-id="969de-239">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="969de-240">Esto reduce eficazmente la resolución del canal alfa plana en un factor de 4 en ambas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="969de-240">This effectively reduces the resolution of the planar alpha channel by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="969de-241">Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles de cada bloque 4x4 de píxeles de canal alfa.</span><span class="sxs-lookup"><span data-stu-id="969de-241">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of alpha-channel pixels.</span></span> <span data-ttu-id="969de-242">Normalmente, debe establecer este valor solo cuando la [propiedad ImageDataDiscard](#imagedatadiscard) tenga el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="969de-242">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span>                            |
| <span data-ttu-id="969de-243">3</span><span class="sxs-lookup"><span data-stu-id="969de-243">3</span></span>     | <span data-ttu-id="969de-244">Se descartan las bandas de datos de frecuencia de paso alto y baja, incluidos los flexbits.</span><span class="sxs-lookup"><span data-stu-id="969de-244">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="969de-245">Esto reduce de forma ffectively la resolución del canal alfa planar en un factor de 16 en ambas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="969de-245">This ffectively reduces the resolution of the planar alpha channel by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="969de-246">Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles en cada macrobloqueo de 16 x 16 píxeles de píxeles de canal alfa.</span><span class="sxs-lookup"><span data-stu-id="969de-246">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of alpha-channel pixels.</span></span> <span data-ttu-id="969de-247">Normalmente, debe establecer este valor solo cuando la [propiedad ImageDataDiscard](#imagedatadiscard) tenga el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="969de-247">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span> |
| <span data-ttu-id="969de-248">4</span><span class="sxs-lookup"><span data-stu-id="969de-248">4</span></span>     | <span data-ttu-id="969de-249">Se descarta totalmente el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="969de-249">The alpha channel is completely discarded.</span></span> <span data-ttu-id="969de-250">El formato de píxel de la imagen transcodificada cambia para reflejar la eliminación del canal alfa.</span><span class="sxs-lookup"><span data-stu-id="969de-250">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="969de-251">Para las imágenes que contienen un canal alfa intercalado, el siguiente valor es válido.</span><span class="sxs-lookup"><span data-stu-id="969de-251">For images that contain an interleaved alpha channel, the following value is valid.</span></span>



| <span data-ttu-id="969de-252">Valor</span><span class="sxs-lookup"><span data-stu-id="969de-252">Value</span></span> | <span data-ttu-id="969de-253">Descripción</span><span class="sxs-lookup"><span data-stu-id="969de-253">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="969de-254">4</span><span class="sxs-lookup"><span data-stu-id="969de-254">4</span></span>     | <span data-ttu-id="969de-255">Se descarta totalmente el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="969de-255">The alpha channel is completely discarded.</span></span> <span data-ttu-id="969de-256">El formato de píxel de la imagen transcodificada cambia para reflejar la eliminación del canal alfa.</span><span class="sxs-lookup"><span data-stu-id="969de-256">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span> |



 

<span data-ttu-id="969de-257">Para alfa intercalado, a menos que esta propiedad esté establecida en 4, el canal alfa se procesa igual que los datos de imagen, según el valor de la [propiedad ImageDataDiscard.](#imagedatadiscard)</span><span class="sxs-lookup"><span data-stu-id="969de-257">For interleaved alpha, unless this property is set to 4, the alpha channel is processed the same as the image data, according to the value of the [ImageDataDiscard](#imagedatadiscard) property.</span></span>

### <a name="alphaquality"></a><span data-ttu-id="969de-258">AlphaQuality</span><span class="sxs-lookup"><span data-stu-id="969de-258">AlphaQuality</span></span>

<span data-ttu-id="969de-259">Establece la calidad de compresión de la imagen de canal alfa plana.</span><span class="sxs-lookup"><span data-stu-id="969de-259">Sets the compression quality for the planar alpha channel image.</span></span>



| <span data-ttu-id="969de-260">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-260">Data type</span></span> | <span data-ttu-id="969de-261">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-261">VARTYPE</span></span>     | <span data-ttu-id="969de-262">Intervalo</span><span class="sxs-lookup"><span data-stu-id="969de-262">Range</span></span> | <span data-ttu-id="969de-263">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-263">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="969de-264">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="969de-264">**UCHAR**</span></span> | <span data-ttu-id="969de-265">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="969de-265">**VT\_UI1**</span></span> | <span data-ttu-id="969de-266">1–255</span><span class="sxs-lookup"><span data-stu-id="969de-266">1–255</span></span> | <span data-ttu-id="969de-267">1</span><span class="sxs-lookup"><span data-stu-id="969de-267">1</span></span>       |



 

<span data-ttu-id="969de-268">Esta propiedad se aplica cuando la imagen tiene un canal alfa y la [propiedad InterleavedAlpha](#interleavedalpha) es **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="969de-268">This property applies when the image has an alpha channel and the [InterleavedAlpha](#interleavedalpha) property is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="969de-269">El valor 1 indica el modo sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="969de-269">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="969de-270">Al aumentar los valores, se aumentan las relaciones de compresión y se reduce la calidad de la imagen.</span><span class="sxs-lookup"><span data-stu-id="969de-270">Increasing values result in higher compression ratios and lower image quality.</span></span>

### <a name="bitmaptransform"></a><span data-ttu-id="969de-271">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="969de-271">BitmapTransform</span></span>

<span data-ttu-id="969de-272">Especifica si la imagen se gira o se voltear cuando se descodifica.</span><span class="sxs-lookup"><span data-stu-id="969de-272">Specifies whether the image is rotated or flipped when decoded.</span></span>



| <span data-ttu-id="969de-273">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-273">Data type</span></span> | <span data-ttu-id="969de-274">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-274">VARTYPE</span></span>     | <span data-ttu-id="969de-275">Intervalo</span><span class="sxs-lookup"><span data-stu-id="969de-275">Range</span></span>                                                                     | <span data-ttu-id="969de-276">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-276">Default</span></span>                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="969de-277">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="969de-277">**UCHAR**</span></span> | <span data-ttu-id="969de-278">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="969de-278">**VT\_UI1**</span></span> | [<span data-ttu-id="969de-279">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="969de-279">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="969de-280">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="969de-280">**WICBitmapTransformRotate0**</span></span> |



 

### <a name="compresseddomaintranscode"></a><span data-ttu-id="969de-281">CompressedDomainTranscode</span><span class="sxs-lookup"><span data-stu-id="969de-281">CompressedDomainTranscode</span></span>

<span data-ttu-id="969de-282">Habilita o deshabilita la transcodificación de dominios comprimidos.</span><span class="sxs-lookup"><span data-stu-id="969de-282">Enables or disables compressed domain transcoding.</span></span>



| <span data-ttu-id="969de-283">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-283">Data type</span></span>         | <span data-ttu-id="969de-284">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-284">VARTYPE</span></span>      | <span data-ttu-id="969de-285">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-285">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="969de-286">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="969de-286">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="969de-287">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="969de-287">**VT\_BOOL**</span></span> | <span data-ttu-id="969de-288">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="969de-288">**VARIANT\_TRUE**</span></span> |



 

<span data-ttu-id="969de-289">Para deshabilitar las operaciones de dominio comprimido, establezca esta propiedad en **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="969de-289">To disable compressed domain operations, set this property to **VARIANT\_FALSE**.</span></span>

### <a name="frequencyorder"></a><span data-ttu-id="969de-290">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="969de-290">FrequencyOrder</span></span>

<span data-ttu-id="969de-291">Habilita la codificación en orden de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="969de-291">Enables encoding in frequency order.</span></span> <span data-ttu-id="969de-292">Las implementaciones de dispositivos de codificadores JPEG XR pueden organizar un archivo en orden espacial para reducir la memoria necesaria durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="969de-292">Device implementations of JPEG XR encoders can organize a file in spatial order to reduce the memory required during encoding.</span></span>



| <span data-ttu-id="969de-293">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-293">Data type</span></span>         | <span data-ttu-id="969de-294">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-294">VARTYPE</span></span>      | <span data-ttu-id="969de-295">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-295">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="969de-296">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="969de-296">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="969de-297">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="969de-297">**VT\_BOOL**</span></span> | <span data-ttu-id="969de-298">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="969de-298">**VARIANT\_TRUE**</span></span> |



 

-   <span data-ttu-id="969de-299">**VARIANT \_ TRUE:** orden de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="969de-299">**VARIANT\_TRUE**: Frequency order.</span></span> <span data-ttu-id="969de-300">Los datos de frecuencia más baja aparecen primero en el archivo y el contenido de la imagen se agrupa por su frecuencia en lugar de por su orientación espacial.</span><span class="sxs-lookup"><span data-stu-id="969de-300">The lowest frequency data appears first in the file, and image content is grouped by its frequency rather than its spatial orientation.</span></span> <span data-ttu-id="969de-301">La organización de un archivo por orden de frecuencia proporciona el mejor rendimiento para cualquier decodificación basada en frecuencia.</span><span class="sxs-lookup"><span data-stu-id="969de-301">Organizing a file by frequency order provides the best performance for any frequency-based decoding.</span></span>
-   <span data-ttu-id="969de-302">**VARIANT \_ FALSE:** orden espacial.</span><span class="sxs-lookup"><span data-stu-id="969de-302">**VARIANT\_FALSE**: Spatial order.</span></span> <span data-ttu-id="969de-303">El orden espacial reduce la memoria necesaria durante la codificación</span><span class="sxs-lookup"><span data-stu-id="969de-303">Spatial order reduces the memory required during encoding</span></span>

<span data-ttu-id="969de-304">Se recomienda el orden de frecuencia a menos que tenga razones específicas del rendimiento o de la aplicación para usar el orden espacial.</span><span class="sxs-lookup"><span data-stu-id="969de-304">Frequency order is recommended unless you have performance or application-specific reasons to use spatial order.</span></span>

### <a name="horizontaltileslices"></a><span data-ttu-id="969de-305">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="969de-305">HorizontalTileSlices</span></span>

<span data-ttu-id="969de-306">Establece el número de iconos horizontales.</span><span class="sxs-lookup"><span data-stu-id="969de-306">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="969de-307">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-307">Data type</span></span>  | <span data-ttu-id="969de-308">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-308">VARTYPE</span></span>     | <span data-ttu-id="969de-309">Intervalo</span><span class="sxs-lookup"><span data-stu-id="969de-309">Range</span></span>  | <span data-ttu-id="969de-310">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-310">Default</span></span>                      |
|------------|-------------|--------|------------------------------|
| <span data-ttu-id="969de-311">**USHORT**</span><span class="sxs-lookup"><span data-stu-id="969de-311">**USHORT**</span></span> | <span data-ttu-id="969de-312">**VT \_ UI2**</span><span class="sxs-lookup"><span data-stu-id="969de-312">**VT\_UI2**</span></span> | <span data-ttu-id="969de-313">0–4095</span><span class="sxs-lookup"><span data-stu-id="969de-313">0–4095</span></span> | <span data-ttu-id="969de-314">(ancho de imagen – 1) >> 8</span><span class="sxs-lookup"><span data-stu-id="969de-314">(image width – 1) >> 8</span></span> |



 

<span data-ttu-id="969de-315">El valor es el número de subdivisiones horizontales; es decir, el número de iconos horizontales: 1.</span><span class="sxs-lookup"><span data-stu-id="969de-315">The value is the number of horizontal subdivisions; that is, the number of horizontal tiles – 1.</span></span>

### <a name="ignoreoverlap"></a><span data-ttu-id="969de-316">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="969de-316">IgnoreOverlap</span></span>

<span data-ttu-id="969de-317">Especifica cómo el codificador controla los límites de mosaico durante una transcodificación de dominio comprimido.</span><span class="sxs-lookup"><span data-stu-id="969de-317">Specifies how the encoder handles tile boundaries during a compressed domain transcode.</span></span>



| <span data-ttu-id="969de-318">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-318">Data type</span></span>         | <span data-ttu-id="969de-319">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-319">VARTYPE</span></span>      | <span data-ttu-id="969de-320">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-320">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="969de-321">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="969de-321">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="969de-322">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="969de-322">**VT\_BOOL**</span></span> | <span data-ttu-id="969de-323">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="969de-323">**VARIANT\_FALSE**</span></span> |



 

<span data-ttu-id="969de-324">Esta propiedad solo se aplica si la propiedad [CompressedDomainTranscode](#compresseddomaintranscode) está establecida en **VARIANT \_ TRUE** y se realiza una transcodificación de subr regiones de exactamente uno o varios iconos.</span><span class="sxs-lookup"><span data-stu-id="969de-324">This property is applied only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and a sub-region transcode of exactly one or more tiles is performed.</span></span>

<span data-ttu-id="969de-325">La operación predeterminada para una transcodificación de región es expandir la región solicitada para incluir los píxeles circundantes necesarios para la descodificación superpuesta de los bordes de la región.</span><span class="sxs-lookup"><span data-stu-id="969de-325">The default operation for a region transcode is to expand the requested region to include the surrounding pixels that are required for overlap decoding of the region edges.</span></span> <span data-ttu-id="969de-326">Si esta propiedad se establece en **VARIANT \_ TRUE,** el códec omite los píxeles circundantes y solo se extraen los mosaicos o iconos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="969de-326">If this property is set to **VARIANT\_TRUE**, the codec ignores the surrounding pixels, and only the selected tile or tiles are extracted.</span></span> <span data-ttu-id="969de-327">Si la imagen de origen no está en mosaico o si la región solicitada incluye iconos parciales, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="969de-327">If the source image is not tiled or if the requested region includes partial tiles, this parameter is ignored.</span></span>

### <a name="imagedatadiscard"></a><span data-ttu-id="969de-328">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="969de-328">ImageDataDiscard</span></span>

<span data-ttu-id="969de-329">Establece la cantidad de datos de frecuencia de imagen que se descartarán durante una transcodificación de dominio comprimido.</span><span class="sxs-lookup"><span data-stu-id="969de-329">Sets the amount of image frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="969de-330">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-330">Data type</span></span> | <span data-ttu-id="969de-331">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-331">VARTYPE</span></span>     | <span data-ttu-id="969de-332">Intervalo</span><span class="sxs-lookup"><span data-stu-id="969de-332">Range</span></span> | <span data-ttu-id="969de-333">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-333">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="969de-334">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="969de-334">**UCHAR**</span></span> | <span data-ttu-id="969de-335">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="969de-335">**VT\_UI1**</span></span> | <span data-ttu-id="969de-336">0–3</span><span class="sxs-lookup"><span data-stu-id="969de-336">0–3</span></span>   | <span data-ttu-id="969de-337">0</span><span class="sxs-lookup"><span data-stu-id="969de-337">0</span></span>       |



 

<span data-ttu-id="969de-338">Esta propiedad solo se aplica si la propiedad [CompressedDomainTranscode](#compresseddomaintranscode) está establecida en **VARIANT \_ TRUE;** de lo contrario, se omite.</span><span class="sxs-lookup"><span data-stu-id="969de-338">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE**; otherwise it is ignored.</span></span>



| <span data-ttu-id="969de-339">Valor</span><span class="sxs-lookup"><span data-stu-id="969de-339">Value</span></span> | <span data-ttu-id="969de-340">Descripción</span><span class="sxs-lookup"><span data-stu-id="969de-340">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="969de-341">0</span><span class="sxs-lookup"><span data-stu-id="969de-341">0</span></span>     | <span data-ttu-id="969de-342">No se descartan datos de frecuencia de la imagen.</span><span class="sxs-lookup"><span data-stu-id="969de-342">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="969de-343">1</span><span class="sxs-lookup"><span data-stu-id="969de-343">1</span></span>     | <span data-ttu-id="969de-344">Los flexbits se descartan.</span><span class="sxs-lookup"><span data-stu-id="969de-344">The flexbits are discarded.</span></span> <span data-ttu-id="969de-345">Esto reduce arbitrariamente la calidad de la imagen transcodificada sin cambiar la resolución efectiva de la imagen.</span><span class="sxs-lookup"><span data-stu-id="969de-345">This arbitrarily reduces the quality of the transcoded image without changing the effective resolution of the image.</span></span> <span data-ttu-id="969de-346">La reducción exacta del tamaño y la calidad del archivo depende de numerosos factores y no se puede especificar exactamente.</span><span class="sxs-lookup"><span data-stu-id="969de-346">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span> <span data-ttu-id="969de-347">Este valor devuelve un error especificado para un canal alfa intercalado.</span><span class="sxs-lookup"><span data-stu-id="969de-347">This value returns an error specified for an interleaved alpha channel.</span></span>                                                                                |
| <span data-ttu-id="969de-348">2</span><span class="sxs-lookup"><span data-stu-id="969de-348">2</span></span>     | <span data-ttu-id="969de-349">Se descarta la banda de datos de frecuencia de paso alto, incluidos los flexbits.</span><span class="sxs-lookup"><span data-stu-id="969de-349">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="969de-350">Esto reduce la resolución de la imagen transcodificada en un factor de 4 en ambas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="969de-350">This reduces the resolution of the transcoded image by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="969de-351">Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles de cada bloque de 4 x 4 píxeles.</span><span class="sxs-lookup"><span data-stu-id="969de-351">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of pixels.</span></span> <span data-ttu-id="969de-352">Por lo tanto, la imagen transcodificada se debe degradar en consecuencia cada vez que se descodifica.</span><span class="sxs-lookup"><span data-stu-id="969de-352">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span>                             |
| <span data-ttu-id="969de-353">3</span><span class="sxs-lookup"><span data-stu-id="969de-353">3</span></span>     | <span data-ttu-id="969de-354">Se descartan las bandas de datos de frecuencia de paso alto y baja, incluidos los flexbits.</span><span class="sxs-lookup"><span data-stu-id="969de-354">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="969de-355">Esto reduce la resolución de la imagen transcodificada en un factor de 16 en ambas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="969de-355">This reduces the resolution of the transcoded image by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="969de-356">Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles en cada macrobloque de 16 x 16 píxeles de píxeles.</span><span class="sxs-lookup"><span data-stu-id="969de-356">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of pixels.</span></span> <span data-ttu-id="969de-357">Por lo tanto, la imagen transcodificada se debe degradar en consecuencia cada vez que se descodifica.</span><span class="sxs-lookup"><span data-stu-id="969de-357">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span> |



 

<span data-ttu-id="969de-358">Si la imagen contiene un canal alfa intercalado, el valor de [ImageDataDiscard](#imagedatadiscard) se aplica al canal alfa a menos que la propiedad [AlphaDataDiscard](#alphadatadiscard) esté establecida en 4, en cuyo caso se descarta el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="969de-358">If the image contains an interleaved alpha channel, the value of [ImageDataDiscard](#imagedatadiscard) is applied to the alpha channel unless the [AlphaDataDiscard](#alphadatadiscard) property is set to 4, in which case the alpha channel is discarded.</span></span>

<span data-ttu-id="969de-359">En el caso de alfa plano, los datos de frecuencia descartados se controlan mediante la [propiedad AlphaDataDiscard.](#alphadatadiscard)</span><span class="sxs-lookup"><span data-stu-id="969de-359">For planar alpha, the frequency data that is discarded is controlled by the [AlphaDataDiscard](#alphadatadiscard) property.</span></span>

### <a name="imagequality"></a><span data-ttu-id="969de-360">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="969de-360">ImageQuality</span></span>

<span data-ttu-id="969de-361">Establece la calidad de la imagen.</span><span class="sxs-lookup"><span data-stu-id="969de-361">Sets the image quality.</span></span>



| <span data-ttu-id="969de-362">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-362">Data type</span></span> | <span data-ttu-id="969de-363">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-363">VARTYPE</span></span>    | <span data-ttu-id="969de-364">Intervalo</span><span class="sxs-lookup"><span data-stu-id="969de-364">Range</span></span> | <span data-ttu-id="969de-365">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-365">Default</span></span> |
|-----------|------------|-------|---------|
| <span data-ttu-id="969de-366">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="969de-366">**FLOAT**</span></span> | <span data-ttu-id="969de-367">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="969de-367">**VT\_R4**</span></span> | <span data-ttu-id="969de-368">0–1.0</span><span class="sxs-lookup"><span data-stu-id="969de-368">0–1.0</span></span> | <span data-ttu-id="969de-369">0.9</span><span class="sxs-lookup"><span data-stu-id="969de-369">0.9</span></span>     |



 

<span data-ttu-id="969de-370">El nivel 1.0 proporciona compresión matemáticamente sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="969de-370">Level 1.0 gives mathematically lossless compression.</span></span>

<span data-ttu-id="969de-371">El nivel 0.0 es la configuración de calidad más baja.</span><span class="sxs-lookup"><span data-stu-id="969de-371">Level 0.0 is the lowest quality setting.</span></span>

### <a name="interleavedalpha"></a><span data-ttu-id="969de-372">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="969de-372">InterleavedAlpha</span></span>

<span data-ttu-id="969de-373">Especifica si se debe codificar alfa intercalado o alfa planar.</span><span class="sxs-lookup"><span data-stu-id="969de-373">Specifies whether to encode interleaved alpha or planar alpha.</span></span>



| <span data-ttu-id="969de-374">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-374">Data type</span></span>         | <span data-ttu-id="969de-375">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-375">VARTYPE</span></span>      | <span data-ttu-id="969de-376">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-376">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="969de-377">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="969de-377">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="969de-378">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="969de-378">**VT\_BOOL**</span></span> | <span data-ttu-id="969de-379">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="969de-379">**VARIANT\_FALSE**</span></span> |



 

-   <span data-ttu-id="969de-380">**VARIANT \_ TRUE:** alfa intercalado.</span><span class="sxs-lookup"><span data-stu-id="969de-380">**VARIANT\_TRUE**: Interleaved alpha.</span></span> <span data-ttu-id="969de-381">La información del canal alfa se codifica como un canal intercalado adicional, sin correlación con los canales de contenido de la imagen.</span><span class="sxs-lookup"><span data-stu-id="969de-381">Alpha channel information is encoded as an additional interleaved channel, with no correlation to the image content channels.</span></span> <span data-ttu-id="969de-382">Este modo es útil para la decodificación alfa simultáneamente con la imagen cuando la imagen se transmite por secuencias.</span><span class="sxs-lookup"><span data-stu-id="969de-382">This mode is useful for decoding alpha simultaneously with the image when the image is streaming.</span></span>
-   <span data-ttu-id="969de-383">VARIANT \_ FALSE: alfa planar.</span><span class="sxs-lookup"><span data-stu-id="969de-383">VARIANT\_FALSE: Planar alpha.</span></span> <span data-ttu-id="969de-384">Un canal alfa planar se codifica como una imagen independiente.</span><span class="sxs-lookup"><span data-stu-id="969de-384">A planar alpha channel is encoded as a separate image.</span></span> <span data-ttu-id="969de-385">Los datos de imagen y el canal alfa se descodifican de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="969de-385">The image data and the alpha channel are decoded independently.</span></span> <span data-ttu-id="969de-386">Opcionalmente, puede establecer el nivel de calidad del canal alfa estableciendo la [propiedad AlphaQuality.](#alphaquality)</span><span class="sxs-lookup"><span data-stu-id="969de-386">Optionally, you can set the quality level of the alpha channel by setting the [AlphaQuality](#alphaquality) property.</span></span>

<span data-ttu-id="969de-387">Alfa intercalado solo se admite para determinados formatos de píxel RGB.</span><span class="sxs-lookup"><span data-stu-id="969de-387">Interleaved alpha is supported only for certain RGB pixel formats.</span></span> <span data-ttu-id="969de-388">Se admite alfa plana para cualquier formato de imagen que defina un canal alfa.</span><span class="sxs-lookup"><span data-stu-id="969de-388">Planar alpha is supported for any image format that defines an alpha channel.</span></span>

### <a name="lossless"></a><span data-ttu-id="969de-389">Lossless</span><span class="sxs-lookup"><span data-stu-id="969de-389">Lossless</span></span>

<span data-ttu-id="969de-390">Habilita la compresión de pérdidas.</span><span class="sxs-lookup"><span data-stu-id="969de-390">Enables losses compression.</span></span>



| <span data-ttu-id="969de-391">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-391">Data type</span></span>         | <span data-ttu-id="969de-392">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-392">VARTYPE</span></span>      | <span data-ttu-id="969de-393">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-393">Default</span></span>        |
|-------------------|--------------|----------------|
| <span data-ttu-id="969de-394">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="969de-394">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="969de-395">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="969de-395">**VT\_BOOL**</span></span> | <span data-ttu-id="969de-396">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="969de-396">VARIANT\_FALSE</span></span> |



 

<span data-ttu-id="969de-397">Si el valor es **VARIANT \_ TRUE,** el codificador usa la compresión sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="969de-397">If the value is **VARIANT\_TRUE**, the encoder uses lossless compression.</span></span> <span data-ttu-id="969de-398">Cuando se establece **en VARIANT \_ TRUE**, esta propiedad invalida la [propiedad ImageQuality.](#imagequality)</span><span class="sxs-lookup"><span data-stu-id="969de-398">When set to **VARIANT\_TRUE**, this property overrides the [ImageQuality](#imagequality) property.</span></span>

### <a name="overlap"></a><span data-ttu-id="969de-399">Superposición</span><span class="sxs-lookup"><span data-stu-id="969de-399">Overlap</span></span>

<span data-ttu-id="969de-400">Establece el nivel de filtrado de superposición.</span><span class="sxs-lookup"><span data-stu-id="969de-400">Sets the level of overlap filtering.</span></span> <span data-ttu-id="969de-401">Con el filtrado de superposición, los coeficientes de transformación se aplican a través de los límites de bloque y macrobloqueo.</span><span class="sxs-lookup"><span data-stu-id="969de-401">With overlap filtering, transform coefficients are applied across block and macroblock boundaries.</span></span> <span data-ttu-id="969de-402">Esto puede reducir los artefactos de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="969de-402">This can reduce blocking artifacts.</span></span>



| <span data-ttu-id="969de-403">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-403">Data type</span></span> | <span data-ttu-id="969de-404">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-404">VARTYPE</span></span>     | <span data-ttu-id="969de-405">Intervalo</span><span class="sxs-lookup"><span data-stu-id="969de-405">Range</span></span> | <span data-ttu-id="969de-406">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-406">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="969de-407">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="969de-407">**UCHAR**</span></span> | <span data-ttu-id="969de-408">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="969de-408">**VT\_UI1**</span></span> | <span data-ttu-id="969de-409">0–4</span><span class="sxs-lookup"><span data-stu-id="969de-409">0–4</span></span>   | <span data-ttu-id="969de-410">1</span><span class="sxs-lookup"><span data-stu-id="969de-410">1</span></span>       |



 



| <span data-ttu-id="969de-411">Valor</span><span class="sxs-lookup"><span data-stu-id="969de-411">Value</span></span> | <span data-ttu-id="969de-412">Descripción</span><span class="sxs-lookup"><span data-stu-id="969de-412">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="969de-413">0</span><span class="sxs-lookup"><span data-stu-id="969de-413">0</span></span>     | <span data-ttu-id="969de-414">Sin superposición.</span><span class="sxs-lookup"><span data-stu-id="969de-414">No overlap.</span></span>                                   |
| <span data-ttu-id="969de-415">1</span><span class="sxs-lookup"><span data-stu-id="969de-415">1</span></span>     | <span data-ttu-id="969de-416">Un nivel de superposición, tiling suave.</span><span class="sxs-lookup"><span data-stu-id="969de-416">One level of overlap, soft tiling.</span></span> <span data-ttu-id="969de-417">(Valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="969de-417">(Default.)</span></span> |
| <span data-ttu-id="969de-418">2</span><span class="sxs-lookup"><span data-stu-id="969de-418">2</span></span>     | <span data-ttu-id="969de-419">Dos niveles de superposición, tiling suave.</span><span class="sxs-lookup"><span data-stu-id="969de-419">Two levels of overlap, soft tiling.</span></span>           |
| <span data-ttu-id="969de-420">3</span><span class="sxs-lookup"><span data-stu-id="969de-420">3</span></span>     | <span data-ttu-id="969de-421">Un nivel de superposición, tiling duro</span><span class="sxs-lookup"><span data-stu-id="969de-421">One level of overlap, hard tiling</span></span>             |
| <span data-ttu-id="969de-422">4</span><span class="sxs-lookup"><span data-stu-id="969de-422">4</span></span>     | <span data-ttu-id="969de-423">Dos niveles de superposición, tiling duro.</span><span class="sxs-lookup"><span data-stu-id="969de-423">Two levels of overlap, hard tiling.</span></span>           |



 

<span data-ttu-id="969de-424">Definiciones:</span><span class="sxs-lookup"><span data-stu-id="969de-424">Definitions:</span></span>

-   <span data-ttu-id="969de-425">Un nivel de superposición: los valores codificados de los bloques 4x4 se modifican en función de los bloques vecinos.</span><span class="sxs-lookup"><span data-stu-id="969de-425">One level of overlap: The encoded values of 4x4 blocks are modified based on neighboring blocks.</span></span>
-   <span data-ttu-id="969de-426">Dos niveles de superposición: se aplica el primer nivel de superposición.</span><span class="sxs-lookup"><span data-stu-id="969de-426">Two levels of overlap: The first level of overlap is applied.</span></span> <span data-ttu-id="969de-427">Además, los valores codificados de macrobloques de 16 x 16 se modifican en función de los bloques de macro vecinos.</span><span class="sxs-lookup"><span data-stu-id="969de-427">In addition, the encoded values of 16x16 macroblocks are modified based on the neighboring macroblocks.</span></span>
-   <span data-ttu-id="969de-428">Mosaico flexible: el filtrado de superposición se aplica a través de los límites de los mosaicos.</span><span class="sxs-lookup"><span data-stu-id="969de-428">Soft tiling: Overlap filtering is applied across tile boundaries.</span></span>
-   <span data-ttu-id="969de-429">Mosaicos duros: el filtrado de superposición no se aplica a través de los límites de mosaico.</span><span class="sxs-lookup"><span data-stu-id="969de-429">Hard tiling: Overlap filtering is not applied across tile boundaries.</span></span> <span data-ttu-id="969de-430">Los iconos duros pueden introducir algunos artefactos visuales a lo largo de los límites de los iconos.</span><span class="sxs-lookup"><span data-stu-id="969de-430">Hard tiles can introduce some visual artifacts along tile boundaries.</span></span>

<span data-ttu-id="969de-431">Si establece esta propiedad, establezca también [UseCodecOptions](#usecodecoptions) en **VARIANT \_ TRUE.**</span><span class="sxs-lookup"><span data-stu-id="969de-431">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="progressivemode"></a><span data-ttu-id="969de-432">ProgressiveMode</span><span class="sxs-lookup"><span data-stu-id="969de-432">ProgressiveMode</span></span>

<span data-ttu-id="969de-433">Habilita o deshabilita la codificación progresiva.</span><span class="sxs-lookup"><span data-stu-id="969de-433">Enables or disables progressive encoding.</span></span>



| <span data-ttu-id="969de-434">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-434">Data type</span></span>         | <span data-ttu-id="969de-435">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-435">VARTYPE</span></span>      | <span data-ttu-id="969de-436">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-436">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="969de-437">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="969de-437">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="969de-438">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="969de-438">**VT\_BOOL**</span></span> | <span data-ttu-id="969de-439">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="969de-439">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="969de-440">Valor</span><span class="sxs-lookup"><span data-stu-id="969de-440">Value</span></span>              | <span data-ttu-id="969de-441">Descripción</span><span class="sxs-lookup"><span data-stu-id="969de-441">Description</span></span>                |
|--------------------|----------------------------|
| <span data-ttu-id="969de-442">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="969de-442">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="969de-443">Modo secuencial (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="969de-443">Sequential mode (default).</span></span> |
| <span data-ttu-id="969de-444">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="969de-444">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="969de-445">Modo progresiva.</span><span class="sxs-lookup"><span data-stu-id="969de-445">Progressive mode.</span></span>          |



 

### <a name="quality"></a><span data-ttu-id="969de-446">Calidad</span><span class="sxs-lookup"><span data-stu-id="969de-446">Quality</span></span>

<span data-ttu-id="969de-447">Establece la calidad de compresión.</span><span class="sxs-lookup"><span data-stu-id="969de-447">Sets the compression quality.</span></span>



| <span data-ttu-id="969de-448">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-448">Data type</span></span> | <span data-ttu-id="969de-449">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-449">VARTYPE</span></span>     | <span data-ttu-id="969de-450">Intervalo</span><span class="sxs-lookup"><span data-stu-id="969de-450">Range</span></span> | <span data-ttu-id="969de-451">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-451">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="969de-452">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="969de-452">**UCHAR**</span></span> | <span data-ttu-id="969de-453">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="969de-453">**VT\_UI1**</span></span> | <span data-ttu-id="969de-454">1–255</span><span class="sxs-lookup"><span data-stu-id="969de-454">1–255</span></span> | <span data-ttu-id="969de-455">1</span><span class="sxs-lookup"><span data-stu-id="969de-455">1</span></span>       |



 

<span data-ttu-id="969de-456">El valor 1 indica el modo sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="969de-456">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="969de-457">Al aumentar los valores, se aumentan las relaciones de compresión y se reduce la calidad de la imagen.</span><span class="sxs-lookup"><span data-stu-id="969de-457">Increasing values result in higher compression ratios and lower image quality.</span></span>

<span data-ttu-id="969de-458">Si establece esta propiedad, establezca también [UseCodecOptions](#usecodecoptions) en **VARIANT \_ TRUE.**</span><span class="sxs-lookup"><span data-stu-id="969de-458">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="streamonly"></a><span data-ttu-id="969de-459">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="969de-459">StreamOnly</span></span>

<span data-ttu-id="969de-460">Habilita o deshabilita el modo de solo secuencia.</span><span class="sxs-lookup"><span data-stu-id="969de-460">Enables or disables stream-only mode.</span></span>



| <span data-ttu-id="969de-461">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-461">Data type</span></span>         | <span data-ttu-id="969de-462">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-462">VARTYPE</span></span>      | <span data-ttu-id="969de-463">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-463">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="969de-464">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="969de-464">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="969de-465">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="969de-465">**VT\_BOOL**</span></span> | <span data-ttu-id="969de-466">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="969de-466">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="969de-467">Valor</span><span class="sxs-lookup"><span data-stu-id="969de-467">Value</span></span>              | <span data-ttu-id="969de-468">Descripción</span><span class="sxs-lookup"><span data-stu-id="969de-468">Description</span></span>                                                            |
|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="969de-469">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="969de-469">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="969de-470">El codificador genera la secuencia de imagen sin procesar sin metadatos.</span><span class="sxs-lookup"><span data-stu-id="969de-470">The encoder outputs the raw image stream without metadata.</span></span>             |
| <span data-ttu-id="969de-471">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="969de-471">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="969de-472">El codificador genera el formato de contenedor (secuencia de imágenes más metadatos).</span><span class="sxs-lookup"><span data-stu-id="969de-472">The encoder outputs the container format (image stream plus metadata).</span></span> |



 

### <a name="subsampling"></a><span data-ttu-id="969de-473">Submuestreo</span><span class="sxs-lookup"><span data-stu-id="969de-473">Subsampling</span></span>

<span data-ttu-id="969de-474">Establece el submuestreo de croma.</span><span class="sxs-lookup"><span data-stu-id="969de-474">Sets the chroma subsampling.</span></span> <span data-ttu-id="969de-475">Esta propiedad solo se aplica a las imágenes RGB.</span><span class="sxs-lookup"><span data-stu-id="969de-475">This property applies only to RGB images.</span></span>



| <span data-ttu-id="969de-476">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-476">Data type</span></span> | <span data-ttu-id="969de-477">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-477">VARTYPE</span></span>     | <span data-ttu-id="969de-478">Intervalo</span><span class="sxs-lookup"><span data-stu-id="969de-478">Range</span></span> | <span data-ttu-id="969de-479">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-479">Default</span></span>                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| <span data-ttu-id="969de-480">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="969de-480">**UCHAR**</span></span> | <span data-ttu-id="969de-481">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="969de-481">**VT\_UI1**</span></span> | <span data-ttu-id="969de-482">0–3</span><span class="sxs-lookup"><span data-stu-id="969de-482">0–3</span></span>   | <span data-ttu-id="969de-483">3 si [ImageQuality](#imagequality) > 0.8; de lo contrario, 1</span><span class="sxs-lookup"><span data-stu-id="969de-483">3 if [ImageQuality](#imagequality) > 0.8; otherwise 1</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="969de-484">Valor</span><span class="sxs-lookup"><span data-stu-id="969de-484">Value</span></span></th>
<th><span data-ttu-id="969de-485">Descripción</span><span class="sxs-lookup"><span data-stu-id="969de-485">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="969de-486">3</span><span class="sxs-lookup"><span data-stu-id="969de-486">3</span></span></td>
<td><span data-ttu-id="969de-487">Codificación 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="969de-487">4:4:4 encoding.</span></span> <span data-ttu-id="969de-488">Conserva la resolución completa de los conflictos.</span><span class="sxs-lookup"><span data-stu-id="969de-488">Preserves full chroma resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="969de-489">2</span><span class="sxs-lookup"><span data-stu-id="969de-489">2</span></span></td>
<td><span data-ttu-id="969de-490">Codificación 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="969de-490">4:2:2 encoding.</span></span> <span data-ttu-id="969de-491">La resolución de la luminosidad es de 1/2 de resolución de luminosidad.</span><span class="sxs-lookup"><span data-stu-id="969de-491">Chroma resolution is ½ of luminance resolution.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="969de-492">1</span><span class="sxs-lookup"><span data-stu-id="969de-492">1</span></span></td>
<td><span data-ttu-id="969de-493">Codificación 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="969de-493">4:2:0 encoding.</span></span> <span data-ttu-id="969de-494">La resolución de la zona es de 1/4 de resolución de luminosidad.</span><span class="sxs-lookup"><span data-stu-id="969de-494">Chroma resolution is ¼ of luminance resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="969de-495">0</span><span class="sxs-lookup"><span data-stu-id="969de-495">0</span></span></td>
<td><span data-ttu-id="969de-496">Codificación 4:0:0.</span><span class="sxs-lookup"><span data-stu-id="969de-496">4:0:0 encoding.</span></span> <span data-ttu-id="969de-497">Descarta todos los valores de croma y solo conserva la luminosidad.</span><span class="sxs-lookup"><span data-stu-id="969de-497">Discards all chroma values and preserves luminance only.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="969de-498">Este modo no se recomienda, ya que el códec usa una definición ligeramente modificada de la luminosidad para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="969de-498">This mode is not recommended, because the codec uses a slightly modified definition of luminance to improve performance.</span></span> <span data-ttu-id="969de-499">En su lugar, es mejor convertir la imagen en monocromática antes de la codificación.</span><span class="sxs-lookup"><span data-stu-id="969de-499">Instead, it is better to convert the image to monochrome before encoding.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="969de-500">4:2:2 y 4:2:0 conservan los detalles de luminosidad a costa de los detalles de color.</span><span class="sxs-lookup"><span data-stu-id="969de-500">4:2:2 and 4:2:0 preserve luminance detail at the expense of color detail.</span></span>

<span data-ttu-id="969de-501">Si establece esta propiedad, establezca también [UseCodecOptions](#usecodecoptions) en **VARIANT \_ TRUE.**</span><span class="sxs-lookup"><span data-stu-id="969de-501">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="usecodecoptions"></a><span data-ttu-id="969de-502">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="969de-502">UseCodecOptions</span></span>

<span data-ttu-id="969de-503">Especifica si se deben usar las propiedades [Quality](#image-quality-settings), [Overlap](#overlap)y [Subsampling](#subsampling) en lugar de la [propiedad ImageQuality](#imagequality) genérica.</span><span class="sxs-lookup"><span data-stu-id="969de-503">Specifies whether to use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties instead of the generic [ImageQuality](#imagequality) property.</span></span>



| <span data-ttu-id="969de-504">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-504">Data type</span></span>         | <span data-ttu-id="969de-505">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-505">VARTYPE</span></span>      | <span data-ttu-id="969de-506">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-506">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="969de-507">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="969de-507">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="969de-508">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="969de-508">**VT\_BOOL**</span></span> | <span data-ttu-id="969de-509">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="969de-509">**VARIANT\_FALSE**</span></span> |



 

### <a name="verticaltileslices"></a><span data-ttu-id="969de-510">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="969de-510">VerticalTileSlices</span></span>

<span data-ttu-id="969de-511">Establece el número de iconos horizontales.</span><span class="sxs-lookup"><span data-stu-id="969de-511">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="969de-512">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="969de-512">Data type</span></span>  | <span data-ttu-id="969de-513">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="969de-513">VARTYPE</span></span>     | <span data-ttu-id="969de-514">Intervalo</span><span class="sxs-lookup"><span data-stu-id="969de-514">Range</span></span>  | <span data-ttu-id="969de-515">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="969de-515">Default</span></span>                       |
|------------|-------------|--------|-------------------------------|
| <span data-ttu-id="969de-516">**USHORT**</span><span class="sxs-lookup"><span data-stu-id="969de-516">**USHORT**</span></span> | <span data-ttu-id="969de-517">**VT \_ UI2**</span><span class="sxs-lookup"><span data-stu-id="969de-517">**VT\_UI2**</span></span> | <span data-ttu-id="969de-518">0–4095</span><span class="sxs-lookup"><span data-stu-id="969de-518">0–4095</span></span> | <span data-ttu-id="969de-519">(alto de la imagen : 1) >> 8</span><span class="sxs-lookup"><span data-stu-id="969de-519">(image height – 1) >> 8</span></span> |



 

<span data-ttu-id="969de-520">El valor es el número de subdivisiones verticales; es decir, el número de mosaicos verticales: 1.</span><span class="sxs-lookup"><span data-stu-id="969de-520">The value is the number of vertical subdivisions; that is, the number of vertical tiles – 1.</span></span>

## <a name="supported-color-formats"></a><span data-ttu-id="969de-521">Formatos de color admitidos</span><span class="sxs-lookup"><span data-stu-id="969de-521">Supported Color Formats</span></span>

<span data-ttu-id="969de-522">Para obtener más información sobre estos formatos, vea [Formatos de píxeles nativos.](-wic-codec-native-pixel-formats.md)</span><span class="sxs-lookup"><span data-stu-id="969de-522">For more information about these formats, see [Native Pixel Formats](-wic-codec-native-pixel-formats.md).</span></span>

-   <span data-ttu-id="969de-523">**Formatos RGB enteros**</span><span class="sxs-lookup"><span data-stu-id="969de-523">**Integer RGB formats**</span></span>
    -   <span data-ttu-id="969de-524">GUID \_ WICPixelFormat24bppRGB</span><span class="sxs-lookup"><span data-stu-id="969de-524">GUID\_WICPixelFormat24bppRGB</span></span>
    -   <span data-ttu-id="969de-525">GUID \_ WICPixelFormat24bppBGR</span><span class="sxs-lookup"><span data-stu-id="969de-525">GUID\_WICPixelFormat24bppBGR</span></span>
    -   <span data-ttu-id="969de-526">GUID \_ WICPixelFormat32bppBGR</span><span class="sxs-lookup"><span data-stu-id="969de-526">GUID\_WICPixelFormat32bppBGR</span></span>
    -   <span data-ttu-id="969de-527">GUID \_ WICPixelFormat48bppRGB</span><span class="sxs-lookup"><span data-stu-id="969de-527">GUID\_WICPixelFormat48bppRGB</span></span>
    -   <span data-ttu-id="969de-528">GUID \_ WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="969de-528">GUID\_WICPixelFormat32bppBGRA</span></span>
    -   <span data-ttu-id="969de-529">GUID \_ WICPixelFormat64bppRGBA</span><span class="sxs-lookup"><span data-stu-id="969de-529">GUID\_WICPixelFormat64bppRGBA</span></span>
    -   <span data-ttu-id="969de-530">GUID \_ WICPixelFormat32bppPBGRA</span><span class="sxs-lookup"><span data-stu-id="969de-530">GUID\_WICPixelFormat32bppPBGRA</span></span>
    -   <span data-ttu-id="969de-531">GUID \_ WICPixelFormat64bppPRGBA</span><span class="sxs-lookup"><span data-stu-id="969de-531">GUID\_WICPixelFormat64bppPRGBA</span></span>
-   <span data-ttu-id="969de-532">**Formatos RGB de punto fijo**</span><span class="sxs-lookup"><span data-stu-id="969de-532">**Fixed-point RGB formats**</span></span>
    -   <span data-ttu-id="969de-533">GUID \_ WICPixelFormat48bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="969de-533">GUID\_WICPixelFormat48bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="969de-534">GUID \_ WICPixelFormat64bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="969de-534">GUID\_WICPixelFormat64bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="969de-535">GUID \_ WICPixelFormat96bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="969de-535">GUID\_WICPixelFormat96bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="969de-536">GUID \_ WICPixelFormat128bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="969de-536">GUID\_WICPixelFormat128bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="969de-537">GUID \_ WICPixelFormat128bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="969de-537">GUID\_WICPixelFormat128bppRGBAFixedPoint</span></span>
-   <span data-ttu-id="969de-538">**Formatos RGB de punto flotante**</span><span class="sxs-lookup"><span data-stu-id="969de-538">**Floating-point RGB formats**</span></span>
    -   <span data-ttu-id="969de-539">GUID \_ WICPixelFormat48bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="969de-539">GUID\_WICPixelFormat48bppRGBHalf</span></span>
    -   <span data-ttu-id="969de-540">GUID \_ WICPixelFormat64bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="969de-540">GUID\_WICPixelFormat64bppRGBHalf</span></span>
    -   <span data-ttu-id="969de-541">GUID \_ WICPixelFormat128bppRGBFloat</span><span class="sxs-lookup"><span data-stu-id="969de-541">GUID\_WICPixelFormat128bppRGBFloat</span></span>
    -   <span data-ttu-id="969de-542">GUID \_ WICPixelFormat64bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="969de-542">GUID\_WICPixelFormat64bppRGBAFixedPoint</span></span>
    -   <span data-ttu-id="969de-543">GUID \_ WICPixelFormat64bppRGBAHalf</span><span class="sxs-lookup"><span data-stu-id="969de-543">GUID\_WICPixelFormat64bppRGBAHalf</span></span>
    -   <span data-ttu-id="969de-544">GUID \_ WICPixelFormat128bppRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="969de-544">GUID\_WICPixelFormat128bppRGBAFloat</span></span>
    -   <span data-ttu-id="969de-545">GUID \_ WICPixelFormat128bppPRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="969de-545">GUID\_WICPixelFormat128bppPRGBAFloat</span></span>
-   <span data-ttu-id="969de-546">**Formatos de escala de grises**</span><span class="sxs-lookup"><span data-stu-id="969de-546">**Grayscale formats**</span></span>
    -   <span data-ttu-id="969de-547">GUID \_ WICPixelFormat8bppGray</span><span class="sxs-lookup"><span data-stu-id="969de-547">GUID\_WICPixelFormat8bppGray</span></span>
    -   <span data-ttu-id="969de-548">GUID \_ WICPixelFormat16bppGray</span><span class="sxs-lookup"><span data-stu-id="969de-548">GUID\_WICPixelFormat16bppGray</span></span>
    -   <span data-ttu-id="969de-549">GUID \_ WICPixelFormat16bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="969de-549">GUID\_WICPixelFormat16bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="969de-550">GUID \_ WICPixelFormat16bppGrayHalf</span><span class="sxs-lookup"><span data-stu-id="969de-550">GUID\_WICPixelFormat16bppGrayHalf</span></span>
    -   <span data-ttu-id="969de-551">GUID \_ WICPixelFormat32bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="969de-551">GUID\_WICPixelFormat32bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="969de-552">GUID \_ WICPixelFormat32bppGrayFloat</span><span class="sxs-lookup"><span data-stu-id="969de-552">GUID\_WICPixelFormat32bppGrayFloat</span></span>
-   <span data-ttu-id="969de-553">**Formatos empaquetados**</span><span class="sxs-lookup"><span data-stu-id="969de-553">**Packed formats**</span></span>
    -   <span data-ttu-id="969de-554">GUID \_ WICPixelFormat16bppBGR555</span><span class="sxs-lookup"><span data-stu-id="969de-554">GUID\_WICPixelFormat16bppBGR555</span></span>
    -   <span data-ttu-id="969de-555">GUID \_ WICPixelFormat16bppBGR565</span><span class="sxs-lookup"><span data-stu-id="969de-555">GUID\_WICPixelFormat16bppBGR565</span></span>
    -   <span data-ttu-id="969de-556">GUID \_ WICPixelFormat32bppBGR101010</span><span class="sxs-lookup"><span data-stu-id="969de-556">GUID\_WICPixelFormat32bppBGR101010</span></span>
    -   <span data-ttu-id="969de-557">GUID \_ WICPixelFormat32bppRGBE</span><span class="sxs-lookup"><span data-stu-id="969de-557">GUID\_WICPixelFormat32bppRGBE</span></span>
-   <span data-ttu-id="969de-558">**Formatos TIFF**</span><span class="sxs-lookup"><span data-stu-id="969de-558">**CMYK formats**</span></span>
    -   <span data-ttu-id="969de-559">GUID \_ WICPixelFormat40bppALEAlpha</span><span class="sxs-lookup"><span data-stu-id="969de-559">GUID\_WICPixelFormat40bppCMYKAlpha</span></span>
    -   <span data-ttu-id="969de-560">GUID \_ WICPixelFormat64bppYUN</span><span class="sxs-lookup"><span data-stu-id="969de-560">GUID\_WICPixelFormat64bppCMYK</span></span>
    -   <span data-ttu-id="969de-561">GUID \_ WICPixelFormat80bppALEAlpha</span><span class="sxs-lookup"><span data-stu-id="969de-561">GUID\_WICPixelFormat80bppCMYKAlpha</span></span>
-   <span data-ttu-id="969de-562">**Formatos de N canales**</span><span class="sxs-lookup"><span data-stu-id="969de-562">**N-channel formats**</span></span>
    -   <span data-ttu-id="969de-563">GUID \_ WICPixelFormat32bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="969de-563">GUID\_WICPixelFormat32bpp4Channels</span></span>
    -   <span data-ttu-id="969de-564">GUID \_ WICPixelFormat40bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="969de-564">GUID\_WICPixelFormat40bpp5Channels</span></span>
    -   <span data-ttu-id="969de-565">GUID \_ WICPixelFormat48bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="969de-565">GUID\_WICPixelFormat48bpp6Channels</span></span>
    -   <span data-ttu-id="969de-566">GUID \_ WICPixelFormat56bpp7Channels</span><span class="sxs-lookup"><span data-stu-id="969de-566">GUID\_WICPixelFormat56bpp7Channels</span></span>
    -   <span data-ttu-id="969de-567">GUID \_ WICPixelFormat64bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="969de-567">GUID\_WICPixelFormat64bpp8Channels</span></span>
    -   <span data-ttu-id="969de-568">GUID \_ WICPixelFormat32bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="969de-568">GUID\_WICPixelFormat32bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="969de-569">GUID \_ WICPixelFormat40bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="969de-569">GUID\_WICPixelFormat40bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="969de-570">GUID \_ WICPixelFormat48bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="969de-570">GUID\_WICPixelFormat48bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="969de-571">GUID \_ WICPixelFormat56bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="969de-571">GUID\_WICPixelFormat56bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="969de-572">GUID \_ WICPixelFormat64bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="969de-572">GUID\_WICPixelFormat64bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="969de-573">GUID \_ WICPixelFormat72bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="969de-573">GUID\_WICPixelFormat72bpp8ChannelsAlpha</span></span>
    -   <span data-ttu-id="969de-574">GUID \_ WICPixelFormat48bpp3Channels</span><span class="sxs-lookup"><span data-stu-id="969de-574">GUID\_WICPixelFormat48bpp3Channels</span></span>
    -   <span data-ttu-id="969de-575">GUID \_ WICPixelFormat64bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="969de-575">GUID\_WICPixelFormat64bpp4Channels</span></span>
    -   <span data-ttu-id="969de-576">GUID \_ WICPixelFormat80bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="969de-576">GUID\_WICPixelFormat80bpp5Channels</span></span>
    -   <span data-ttu-id="969de-577">GUID \_ WICPixelFormat96bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="969de-577">GUID\_WICPixelFormat96bpp6Channels</span></span>
    -   <span data-ttu-id="969de-578">GUID \_ WICPixelFormat128bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="969de-578">GUID\_WICPixelFormat128bpp8Channels</span></span>
    -   <span data-ttu-id="969de-579">GUID \_ WICPixelFormat64bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="969de-579">GUID\_WICPixelFormat64bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="969de-580">GUID \_ WICPixelFormat80bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="969de-580">GUID\_WICPixelFormat80bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="969de-581">GUID \_ WICPixelFormat96bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="969de-581">GUID\_WICPixelFormat96bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="969de-582">GUID \_ WICPixelFormat112bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="969de-582">GUID\_WICPixelFormat112bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="969de-583">GUID \_ WICPixelFormat128bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="969de-583">GUID\_WICPixelFormat128bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="969de-584">GUID \_ WICPixelFormat144bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="969de-584">GUID\_WICPixelFormat144bpp8ChannelsAlpha</span></span>

 

 
