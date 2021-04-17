---
description: En este tema se proporciona información sobre el códec JPEG nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Información general sobre el formato JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953d1d6a02e47b41d1b7cf872f3381cd640151
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687547"
---
# <a name="jpeg-format-overview"></a><span data-ttu-id="46909-103">Información general sobre el formato JPEG</span><span class="sxs-lookup"><span data-stu-id="46909-103">JPEG Format Overview</span></span>

<span data-ttu-id="46909-104">En este tema se proporciona información sobre el códec JPEG nativo disponible a través de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="46909-104">This topic provides information about the native JPEG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="46909-105">Identidad del códec</span><span class="sxs-lookup"><span data-stu-id="46909-105">Codec Identity</span></span>

<span data-ttu-id="46909-106">En la tabla siguiente se proporciona información de identificación del códec.</span><span class="sxs-lookup"><span data-stu-id="46909-106">The following table provides codec identification information.</span></span>



|                        |                                         |
|------------------------|-----------------------------------------|
| <span data-ttu-id="46909-107">Nombres formales</span><span class="sxs-lookup"><span data-stu-id="46909-107">Formal Name(s)</span></span>         | <span data-ttu-id="46909-108">Formato JPEG (Joint Photographic Experts Group)</span><span class="sxs-lookup"><span data-stu-id="46909-108">Joint Photographic Experts Group (JPEG)</span></span> |
| <span data-ttu-id="46909-109">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="46909-109">File Name Extension(s)</span></span> | <span data-ttu-id="46909-110">JPE, JPEG, jpg</span><span class="sxs-lookup"><span data-stu-id="46909-110">jpe, jpeg, jpg</span></span>                          |
| <span data-ttu-id="46909-111">Tipo de MIME</span><span class="sxs-lookup"><span data-stu-id="46909-111">MIME type</span></span>              | <span data-ttu-id="46909-112">image/JPEG, Image/JPE, Image/jpg</span><span class="sxs-lookup"><span data-stu-id="46909-112">image/jpeg, image/jpe, image/jpg</span></span>        |
| <span data-ttu-id="46909-113">Compatibilidad con las especificaciones</span><span class="sxs-lookup"><span data-stu-id="46909-113">Specification Support</span></span>  | <span data-ttu-id="46909-114">Especificación JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="46909-114">JFIF Specification 1.02</span></span>                 |



 

<span data-ttu-id="46909-115">En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes nativos del códec JPEG.</span><span class="sxs-lookup"><span data-stu-id="46909-115">The following table lists the GUIDs used to identify the native JPEG codec components.</span></span>



| <span data-ttu-id="46909-116">Componente</span><span class="sxs-lookup"><span data-stu-id="46909-116">Component</span></span>        | <span data-ttu-id="46909-117">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="46909-117">Friendly Name</span></span>             | <span data-ttu-id="46909-118">GUID</span><span class="sxs-lookup"><span data-stu-id="46909-118">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="46909-119">Formato de contenedor</span><span class="sxs-lookup"><span data-stu-id="46909-119">Container Format</span></span> | <span data-ttu-id="46909-120">GUID \_ ContainerFormatJpeg</span><span class="sxs-lookup"><span data-stu-id="46909-120">GUID\_ContainerFormatJpeg</span></span> | <span data-ttu-id="46909-121">19e4a5aa-5662-4fc5-a0c01758028e1057</span><span class="sxs-lookup"><span data-stu-id="46909-121">19e4a5aa-5662-4fc5-a0c01758028e1057</span></span> |
| <span data-ttu-id="46909-122">Descodificador</span><span class="sxs-lookup"><span data-stu-id="46909-122">Decoder</span></span>          | <span data-ttu-id="46909-123">CLSID \_ WICJpegDecoder</span><span class="sxs-lookup"><span data-stu-id="46909-123">CLSID\_WICJpegDecoder</span></span>     | <span data-ttu-id="46909-124">9456a480-e88b-43ea-9e730b2d9b71b1ca</span><span class="sxs-lookup"><span data-stu-id="46909-124">9456a480-e88b-43ea-9e730b2d9b71b1ca</span></span> |
| <span data-ttu-id="46909-125">Codificador</span><span class="sxs-lookup"><span data-stu-id="46909-125">Encoder</span></span>          | <span data-ttu-id="46909-126">CLSID \_ WICJpegEncoder</span><span class="sxs-lookup"><span data-stu-id="46909-126">CLSID\_WICJpegEncoder</span></span>     | <span data-ttu-id="46909-127">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span><span class="sxs-lookup"><span data-stu-id="46909-127">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="46909-128">Encoding</span><span class="sxs-lookup"><span data-stu-id="46909-128">Encoding</span></span>

<span data-ttu-id="46909-129">La API de codificación WIC está diseñada para ser independiente del códec y la codificación de imágenes para los códecs habilitados para WIC es esencialmente la misma.</span><span class="sxs-lookup"><span data-stu-id="46909-129">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="46909-130">Para obtener más información sobre la codificación de imágenes mediante la API de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.</span><span class="sxs-lookup"><span data-stu-id="46909-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="46909-131">Opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="46909-131">Encoder Options</span></span>

<span data-ttu-id="46909-132">Los códecs habilitados para WIC difieren en el nivel de opción de codificación.</span><span class="sxs-lookup"><span data-stu-id="46909-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="46909-133">Las opciones del codificador reflejan las capacidades de un codificador de imágenes y cada códec nativo admite un conjunto de estas opciones de codificador.</span><span class="sxs-lookup"><span data-stu-id="46909-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="46909-134">Las opciones del codificador pueden ser opciones básicas de WIC compatibles disponibles para todos los códigos habilitados para WIC (aunque no se admiten necesariamente) o las opciones específicas del códec diseñadas con el códec formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="46909-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="46909-135">Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la interfaz [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="46909-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="46909-136">Para obtener más información sobre el uso de la interfaz **IPropertyBag2** para la codificación de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.</span><span class="sxs-lookup"><span data-stu-id="46909-136">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="46909-137">El códec JPEG usa las opciones básicas de WIC.</span><span class="sxs-lookup"><span data-stu-id="46909-137">The JPEG codec uses basic WIC options.</span></span> <span data-ttu-id="46909-138">En la tabla siguiente se enumeran las opciones del codificador WIC admitidas por el códec JPEG nativo.</span><span class="sxs-lookup"><span data-stu-id="46909-138">The following table lists the WIC encoder options supported by the native JPEG codec.</span></span>



| <span data-ttu-id="46909-139">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="46909-139">Property Name</span></span>                                        | <span data-ttu-id="46909-140">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="46909-140">VARTYPE</span></span>           | <span data-ttu-id="46909-141">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="46909-141">Value Range</span></span>                                                                       | <span data-ttu-id="46909-142">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="46909-142">Default Value</span></span>                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="46909-143">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="46909-143">ImageQuality</span></span>](#imagequality-option)                 | <span data-ttu-id="46909-144">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="46909-144">VT\_R4</span></span>            | <span data-ttu-id="46909-145">0-1,0</span><span class="sxs-lookup"><span data-stu-id="46909-145">0 - 1.0</span></span>                                                                           | <span data-ttu-id="46909-146">0.9</span><span class="sxs-lookup"><span data-stu-id="46909-146">0.9</span></span>                                                                            |
| [<span data-ttu-id="46909-147">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="46909-147">BitmapTransform</span></span>](#bitmaptransform-option)           | <span data-ttu-id="46909-148">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="46909-148">VT\_UI1</span></span>           | [<span data-ttu-id="46909-149">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="46909-149">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [<span data-ttu-id="46909-150">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="46909-150">**WICBitmapTransformRotate0**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [<span data-ttu-id="46909-151">Luminancia</span><span class="sxs-lookup"><span data-stu-id="46909-151">Luminance</span></span>](#luminance-option)                       | <span data-ttu-id="46909-152">Matriz de VT \_ UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="46909-152">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="46909-153">64 entradas (DCT)</span><span class="sxs-lookup"><span data-stu-id="46909-153">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="46909-154">Tabla de luminancia predeterminada.</span><span class="sxs-lookup"><span data-stu-id="46909-154">Default luminance table.</span></span>                                                       |
| [<span data-ttu-id="46909-155">Chrominance</span><span class="sxs-lookup"><span data-stu-id="46909-155">Chrominance</span></span>](#chrominance-option)                   | <span data-ttu-id="46909-156">Matriz de VT \_ UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="46909-156">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="46909-157">64 entradas (DCT)</span><span class="sxs-lookup"><span data-stu-id="46909-157">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="46909-158">Tabla de crominancia predeterminada.</span><span class="sxs-lookup"><span data-stu-id="46909-158">Default chrominance table.</span></span>                                                     |
| [<span data-ttu-id="46909-159">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="46909-159">JpegYCrCbSubsampling</span></span>](#jpegycrcbsubsampling-option) | <span data-ttu-id="46909-160">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="46909-160">VT\_UI1</span></span>           | [<span data-ttu-id="46909-161">**WICJpegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="46909-161">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [<span data-ttu-id="46909-162">**WICJpegYCrCbSubsampling420**</span><span class="sxs-lookup"><span data-stu-id="46909-162">**WICJpegYCrCbSubsampling420**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [<span data-ttu-id="46909-163">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="46909-163">SuppressApp0</span></span>](/windows)                       | <span data-ttu-id="46909-164">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="46909-164">VT\_BOOL</span></span>          | <span data-ttu-id="46909-165">**True** / **False**</span><span class="sxs-lookup"><span data-stu-id="46909-165">**TRUE**/**FALSE**</span></span>                                                                | <span data-ttu-id="46909-166">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="46909-166">**FALSE**</span></span>                                                                      |



 

<span data-ttu-id="46909-167">Si una opción de codificador está presente en la lista de opciones [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que el códec no admite, se omite.</span><span class="sxs-lookup"><span data-stu-id="46909-167">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="imagequality-option"></a><span data-ttu-id="46909-168">Opción ImageQuality</span><span class="sxs-lookup"><span data-stu-id="46909-168">ImageQuality Option</span></span>

<span data-ttu-id="46909-169">Especifica la fidelidad de imagen deseada.</span><span class="sxs-lookup"><span data-stu-id="46909-169">Specifies the desired image fidelity.</span></span> <span data-ttu-id="46909-170">0,0 indica la fidelidad más baja posible y 1,0 especifica la fidelidad más alta.</span><span class="sxs-lookup"><span data-stu-id="46909-170">0.0 indicates the lowest possible fidelity and 1.0 specifies the highest fidelity.</span></span>

<span data-ttu-id="46909-171">El valor predeterminado es 0,9.</span><span class="sxs-lookup"><span data-stu-id="46909-171">The default value is 0.9.</span></span>

### <a name="bitmaptransform-option"></a><span data-ttu-id="46909-172">Opción BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="46909-172">BitmapTransform Option</span></span>

<span data-ttu-id="46909-173">Especifica cómo se transformará la imagen durante la descodificación de imágenes.</span><span class="sxs-lookup"><span data-stu-id="46909-173">Specifies how the image is to be transformed during image decoding.</span></span> <span data-ttu-id="46909-174">Esta opción debe establecerse en uno de los valores de enumeración [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .</span><span class="sxs-lookup"><span data-stu-id="46909-174">This option must be set to one of the [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) enumeration values.</span></span>

<span data-ttu-id="46909-175">El valor predeterminado es [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span><span class="sxs-lookup"><span data-stu-id="46909-175">The default value is [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span></span>

### <a name="luminance-option"></a><span data-ttu-id="46909-176">Opción de luminancia</span><span class="sxs-lookup"><span data-stu-id="46909-176">Luminance Option</span></span>

<span data-ttu-id="46909-177">Especifica la tabla de nivel de brillo de escala de grises que se va a usar para la codificación.</span><span class="sxs-lookup"><span data-stu-id="46909-177">Specifies the grayscale brightness level table to use for encoding.</span></span>

### <a name="chrominance-option"></a><span data-ttu-id="46909-178">Opción de crominancia</span><span class="sxs-lookup"><span data-stu-id="46909-178">Chrominance Option</span></span>

<span data-ttu-id="46909-179">Especifica la tabla de crominancia que se va a utilizar para la codificación.</span><span class="sxs-lookup"><span data-stu-id="46909-179">Specifies the chrominance table to use for encoding.</span></span>

### <a name="jpegycrcbsubsampling-option"></a><span data-ttu-id="46909-180">Opción JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="46909-180">JpegYCrCbSubsampling Option</span></span>

<span data-ttu-id="46909-181">Especifica la proporción de submuestreo que se va a usar para la codificación YCrCb.</span><span class="sxs-lookup"><span data-stu-id="46909-181">Specifies the subsampling ratio to use for YCrCb encoding.</span></span>

<span data-ttu-id="46909-182">El valor predeterminado es [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span><span class="sxs-lookup"><span data-stu-id="46909-182">The default value is [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span></span>

### <a name="suppressapp0-option"></a><span data-ttu-id="46909-183">Opción SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="46909-183">SuppressApp0 Option</span></span>

<span data-ttu-id="46909-184">Especifica si se va a suprimir la escritura de metadatos de App0 mientras se codifican los datos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="46909-184">Specifies whether to suppress the write of App0 metadata while encoding the image data.</span></span>

<span data-ttu-id="46909-185">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="46909-185">The default value is **FALSE**.</span></span>

## <a name="decoding"></a><span data-ttu-id="46909-186">Descodificación</span><span class="sxs-lookup"><span data-stu-id="46909-186">Decoding</span></span>

<span data-ttu-id="46909-187">La API de descodificación de WIC está diseñada para ser independiente del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma.</span><span class="sxs-lookup"><span data-stu-id="46909-187">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="46909-188">Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="46909-188">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="46909-189">Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="46909-189">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="46909-190">El códec JPEG nativo también admite [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) en la descodificación de fotogramas agregar opciones de avanzada para descodificar una secuencia de imágenes.</span><span class="sxs-lookup"><span data-stu-id="46909-190">The native JPEG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advaced options for decoding an image stream.</span></span> <span data-ttu-id="46909-191">Para obtener más información acerca de estas opciones avanzadas, consulte la [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="46909-191">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
