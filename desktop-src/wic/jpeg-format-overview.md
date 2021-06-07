---
description: En este tema se proporciona información sobre el códec JPEG nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Introducción al formato JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2acc7fcd71fc962d3321112d342f675b878188
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444196"
---
# <a name="jpeg-format-overview"></a><span data-ttu-id="20c91-103">Introducción al formato JPEG</span><span class="sxs-lookup"><span data-stu-id="20c91-103">JPEG Format Overview</span></span>

<span data-ttu-id="20c91-104">En este tema se proporciona información sobre el códec JPEG nativo disponible a través de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="20c91-104">This topic provides information about the native JPEG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="20c91-105">Identidad de códec</span><span class="sxs-lookup"><span data-stu-id="20c91-105">Codec Identity</span></span>

<span data-ttu-id="20c91-106">En la tabla siguiente se proporciona información de identificación de códecs.</span><span class="sxs-lookup"><span data-stu-id="20c91-106">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="20c91-107">Componente</span><span class="sxs-lookup"><span data-stu-id="20c91-107">Component</span></span>            | <span data-ttu-id="20c91-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="20c91-108">Description</span></span>                             |
|------------------------|-----------------------------------------|
| <span data-ttu-id="20c91-109">Nombres formales</span><span class="sxs-lookup"><span data-stu-id="20c91-109">Formal Name(s)</span></span>         | <span data-ttu-id="20c91-110">Formato JPEG (Joint Photographic Experts Group)</span><span class="sxs-lookup"><span data-stu-id="20c91-110">Joint Photographic Experts Group (JPEG)</span></span> |
| <span data-ttu-id="20c91-111">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="20c91-111">File Name Extension(s)</span></span> | <span data-ttu-id="20c91-112">jpe, jpeg, jpg</span><span class="sxs-lookup"><span data-stu-id="20c91-112">jpe, jpeg, jpg</span></span>                          |
| <span data-ttu-id="20c91-113">Tipo de MIME</span><span class="sxs-lookup"><span data-stu-id="20c91-113">MIME type</span></span>              | <span data-ttu-id="20c91-114">image/jpeg, image/jpe, image/jpg</span><span class="sxs-lookup"><span data-stu-id="20c91-114">image/jpeg, image/jpe, image/jpg</span></span>        |
| <span data-ttu-id="20c91-115">Compatibilidad con especificaciones</span><span class="sxs-lookup"><span data-stu-id="20c91-115">Specification Support</span></span>  | <span data-ttu-id="20c91-116">Especificación JFIF 1.02</span><span class="sxs-lookup"><span data-stu-id="20c91-116">JFIF Specification 1.02</span></span>                 |



 

<span data-ttu-id="20c91-117">En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes de códec JPEG nativos.</span><span class="sxs-lookup"><span data-stu-id="20c91-117">The following table lists the GUIDs used to identify the native JPEG codec components.</span></span>



| <span data-ttu-id="20c91-118">Componente</span><span class="sxs-lookup"><span data-stu-id="20c91-118">Component</span></span>        | <span data-ttu-id="20c91-119">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="20c91-119">Friendly Name</span></span>             | <span data-ttu-id="20c91-120">GUID</span><span class="sxs-lookup"><span data-stu-id="20c91-120">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="20c91-121">Formato de contenedor</span><span class="sxs-lookup"><span data-stu-id="20c91-121">Container Format</span></span> | <span data-ttu-id="20c91-122">GUID \_ ContainerFormatFormatFormateg</span><span class="sxs-lookup"><span data-stu-id="20c91-122">GUID\_ContainerFormatJpeg</span></span> | <span data-ttu-id="20c91-123">19e4a5aa-5662-4fc5-a0c01758028e1057</span><span class="sxs-lookup"><span data-stu-id="20c91-123">19e4a5aa-5662-4fc5-a0c01758028e1057</span></span> |
| <span data-ttu-id="20c91-124">Descodificador</span><span class="sxs-lookup"><span data-stu-id="20c91-124">Decoder</span></span>          | <span data-ttu-id="20c91-125">CLSID \_ WICShuegDecoder</span><span class="sxs-lookup"><span data-stu-id="20c91-125">CLSID\_WICJpegDecoder</span></span>     | <span data-ttu-id="20c91-126">9456a480-e88b-43ea-9e730b2d9b71b1ca</span><span class="sxs-lookup"><span data-stu-id="20c91-126">9456a480-e88b-43ea-9e730b2d9b71b1ca</span></span> |
| <span data-ttu-id="20c91-127">Codificador</span><span class="sxs-lookup"><span data-stu-id="20c91-127">Encoder</span></span>          | <span data-ttu-id="20c91-128">CLSID \_ WICShuegEncoder</span><span class="sxs-lookup"><span data-stu-id="20c91-128">CLSID\_WICJpegEncoder</span></span>     | <span data-ttu-id="20c91-129">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span><span class="sxs-lookup"><span data-stu-id="20c91-129">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="20c91-130">Encoding</span><span class="sxs-lookup"><span data-stu-id="20c91-130">Encoding</span></span>

<span data-ttu-id="20c91-131">La API de codificación WIC está diseñada para ser independiente del códec y la codificación de imágenes para códecs habilitados para WIC es básicamente la misma.</span><span class="sxs-lookup"><span data-stu-id="20c91-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="20c91-132">Para obtener más información sobre la codificación de imágenes mediante la API de WIC, vea Información general [sobre la codificación.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="20c91-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="20c91-133">Opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="20c91-133">Encoder Options</span></span>

<span data-ttu-id="20c91-134">Los códecs habilitados para WIC difieren en el nivel de opción de codificación.</span><span class="sxs-lookup"><span data-stu-id="20c91-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="20c91-135">Las opciones del codificador reflejan las funcionalidades de un codificador de imágenes y cada códec nativo admite un conjunto de estas opciones de codificador.</span><span class="sxs-lookup"><span data-stu-id="20c91-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="20c91-136">Las opciones de codificador pueden ser opciones básicas compatibles con WIC disponibles para todos los códigos habilitados para WIC (aunque no necesariamente admitidos) o opciones específicas del códec diseñadas por el códec de formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="20c91-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="20c91-137">Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la [**interfaz IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="20c91-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="20c91-138">Para obtener más información sobre el uso de la **interfaz IPropertyBag2** para la codificación WIC , vea Información general [sobre la codificación.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="20c91-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="20c91-139">El códec JPEG usa opciones básicas de WIC.</span><span class="sxs-lookup"><span data-stu-id="20c91-139">The JPEG codec uses basic WIC options.</span></span> <span data-ttu-id="20c91-140">En la tabla siguiente se enumeran las opciones del codificador WIC compatibles con el códec JPEG nativo.</span><span class="sxs-lookup"><span data-stu-id="20c91-140">The following table lists the WIC encoder options supported by the native JPEG codec.</span></span>



| <span data-ttu-id="20c91-141">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="20c91-141">Property Name</span></span>                                        | <span data-ttu-id="20c91-142">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="20c91-142">VARTYPE</span></span>           | <span data-ttu-id="20c91-143">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="20c91-143">Value Range</span></span>                                                                       | <span data-ttu-id="20c91-144">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="20c91-144">Default Value</span></span>                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="20c91-145">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="20c91-145">ImageQuality</span></span>](#imagequality-option)                 | <span data-ttu-id="20c91-146">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="20c91-146">VT\_R4</span></span>            | <span data-ttu-id="20c91-147">0 - 1.0</span><span class="sxs-lookup"><span data-stu-id="20c91-147">0 - 1.0</span></span>                                                                           | <span data-ttu-id="20c91-148">0.9</span><span class="sxs-lookup"><span data-stu-id="20c91-148">0.9</span></span>                                                                            |
| [<span data-ttu-id="20c91-149">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="20c91-149">BitmapTransform</span></span>](#bitmaptransform-option)           | <span data-ttu-id="20c91-150">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="20c91-150">VT\_UI1</span></span>           | [<span data-ttu-id="20c91-151">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="20c91-151">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [<span data-ttu-id="20c91-152">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="20c91-152">**WICBitmapTransformRotate0**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [<span data-ttu-id="20c91-153">Luminancia</span><span class="sxs-lookup"><span data-stu-id="20c91-153">Luminance</span></span>](#luminance-option)                       | <span data-ttu-id="20c91-154">VT \_ UI4/VT \_ ARRAY</span><span class="sxs-lookup"><span data-stu-id="20c91-154">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="20c91-155">64 entradas (DCT)</span><span class="sxs-lookup"><span data-stu-id="20c91-155">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="20c91-156">Tabla de luminosidad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="20c91-156">Default luminance table.</span></span>                                                       |
| [<span data-ttu-id="20c91-157">Chrominance</span><span class="sxs-lookup"><span data-stu-id="20c91-157">Chrominance</span></span>](#chrominance-option)                   | <span data-ttu-id="20c91-158">VT \_ UI4/VT \_ ARRAY</span><span class="sxs-lookup"><span data-stu-id="20c91-158">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="20c91-159">64 entradas (DCT)</span><span class="sxs-lookup"><span data-stu-id="20c91-159">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="20c91-160">Tabla de chrominance predeterminada.</span><span class="sxs-lookup"><span data-stu-id="20c91-160">Default chrominance table.</span></span>                                                     |
| [<span data-ttu-id="20c91-161">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="20c91-161">JpegYCrCbSubsampling</span></span>](#jpegycrcbsubsampling-option) | <span data-ttu-id="20c91-162">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="20c91-162">VT\_UI1</span></span>           | [<span data-ttu-id="20c91-163">**WICOptionegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="20c91-163">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [<span data-ttu-id="20c91-164">**WICCbegYCrCbSubsampling420**</span><span class="sxs-lookup"><span data-stu-id="20c91-164">**WICJpegYCrCbSubsampling420**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [<span data-ttu-id="20c91-165">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="20c91-165">SuppressApp0</span></span>](/windows)                       | <span data-ttu-id="20c91-166">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="20c91-166">VT\_BOOL</span></span>          | <span data-ttu-id="20c91-167">**TRUE** / **FALSE**</span><span class="sxs-lookup"><span data-stu-id="20c91-167">**TRUE**/**FALSE**</span></span>                                                                | <span data-ttu-id="20c91-168">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="20c91-168">**FALSE**</span></span>                                                                      |



 

<span data-ttu-id="20c91-169">Si hay una opción de codificador en la lista [**de opciones IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que el códec no admite, se omite.</span><span class="sxs-lookup"><span data-stu-id="20c91-169">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="imagequality-option"></a><span data-ttu-id="20c91-170">Opción ImageQuality</span><span class="sxs-lookup"><span data-stu-id="20c91-170">ImageQuality Option</span></span>

<span data-ttu-id="20c91-171">Especifica la fidelidad de la imagen deseada.</span><span class="sxs-lookup"><span data-stu-id="20c91-171">Specifies the desired image fidelity.</span></span> <span data-ttu-id="20c91-172">0,0 indica la fidelidad más baja posible y 1,0 especifica la fidelidad más alta.</span><span class="sxs-lookup"><span data-stu-id="20c91-172">0.0 indicates the lowest possible fidelity and 1.0 specifies the highest fidelity.</span></span>

<span data-ttu-id="20c91-173">El valor predeterminado es 0,9.</span><span class="sxs-lookup"><span data-stu-id="20c91-173">The default value is 0.9.</span></span>

### <a name="bitmaptransform-option"></a><span data-ttu-id="20c91-174">Opción BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="20c91-174">BitmapTransform Option</span></span>

<span data-ttu-id="20c91-175">Especifica cómo se va a transformar la imagen durante la decodificación de la imagen.</span><span class="sxs-lookup"><span data-stu-id="20c91-175">Specifies how the image is to be transformed during image decoding.</span></span> <span data-ttu-id="20c91-176">Esta opción debe establecerse en uno de los valores de enumeración [**WICBitmapTransformOptions.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)</span><span class="sxs-lookup"><span data-stu-id="20c91-176">This option must be set to one of the [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) enumeration values.</span></span>

<span data-ttu-id="20c91-177">El valor predeterminado es [**WICBitmapTransformRotate0.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)</span><span class="sxs-lookup"><span data-stu-id="20c91-177">The default value is [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span></span>

### <a name="luminance-option"></a><span data-ttu-id="20c91-178">Opción de luminosidad</span><span class="sxs-lookup"><span data-stu-id="20c91-178">Luminance Option</span></span>

<span data-ttu-id="20c91-179">Especifica la tabla de nivel de brillo de escala de grises que se usará para la codificación.</span><span class="sxs-lookup"><span data-stu-id="20c91-179">Specifies the grayscale brightness level table to use for encoding.</span></span>

### <a name="chrominance-option"></a><span data-ttu-id="20c91-180">Opción chrominance</span><span class="sxs-lookup"><span data-stu-id="20c91-180">Chrominance Option</span></span>

<span data-ttu-id="20c91-181">Especifica la tabla chrominance que se usará para la codificación.</span><span class="sxs-lookup"><span data-stu-id="20c91-181">Specifies the chrominance table to use for encoding.</span></span>

### <a name="jpegycrcbsubsampling-option"></a><span data-ttu-id="20c91-182">JpegYCrCbSubsampling (opción)</span><span class="sxs-lookup"><span data-stu-id="20c91-182">JpegYCrCbSubsampling Option</span></span>

<span data-ttu-id="20c91-183">Especifica la proporción de submuestreo que se usará para la codificación YCrCb.</span><span class="sxs-lookup"><span data-stu-id="20c91-183">Specifies the subsampling ratio to use for YCrCb encoding.</span></span>

<span data-ttu-id="20c91-184">El valor predeterminado [**es WICOmisiónegYCrCbSubsampling420.**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption)</span><span class="sxs-lookup"><span data-stu-id="20c91-184">The default value is [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span></span>

### <a name="suppressapp0-option"></a><span data-ttu-id="20c91-185">Opción SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="20c91-185">SuppressApp0 Option</span></span>

<span data-ttu-id="20c91-186">Especifica si se debe suprimir la escritura de metadatos de App0 al codificar los datos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="20c91-186">Specifies whether to suppress the write of App0 metadata while encoding the image data.</span></span>

<span data-ttu-id="20c91-187">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="20c91-187">The default value is **FALSE**.</span></span>

## <a name="decoding"></a><span data-ttu-id="20c91-188">Descodificación</span><span class="sxs-lookup"><span data-stu-id="20c91-188">Decoding</span></span>

<span data-ttu-id="20c91-189">La API decoding de WIC está diseñada para ser independiente del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma.</span><span class="sxs-lookup"><span data-stu-id="20c91-189">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="20c91-190">Para obtener más información sobre lacoding de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="20c91-190">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="20c91-191">Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="20c91-191">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="20c91-192">El códec JPEG nativo también admite [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) en la codificación de fotogramas agregando opciones avanzadas para la decodización de un flujo de imagen.</span><span class="sxs-lookup"><span data-stu-id="20c91-192">The native JPEG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advaced options for decoding an image stream.</span></span> <span data-ttu-id="20c91-193">Para obtener más información sobre estas opciones avanzadas, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="20c91-193">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
