---
description: En este tema se proporciona información sobre el códec TIFF nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Información general sobre el formato TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db603857da892d4b699bb7df7d8b3e2ee5566326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706997"
---
# <a name="tiff-format-overview"></a><span data-ttu-id="75119-103">Información general sobre el formato TIFF</span><span class="sxs-lookup"><span data-stu-id="75119-103">TIFF Format Overview</span></span>

<span data-ttu-id="75119-104">En este tema se proporciona información sobre el códec TIFF nativo disponible a través de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="75119-104">This topic provides information about the native TIFF codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="75119-105">Identidad del códec</span><span class="sxs-lookup"><span data-stu-id="75119-105">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="75119-106">Encoding</span><span class="sxs-lookup"><span data-stu-id="75119-106">Encoding</span></span>](#encoding)
    -   [<span data-ttu-id="75119-107">Opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="75119-107">Encoder Options</span></span>](#encoder-options)
-   [<span data-ttu-id="75119-108">Descodificación</span><span class="sxs-lookup"><span data-stu-id="75119-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="75119-109">Identidad del códec</span><span class="sxs-lookup"><span data-stu-id="75119-109">Codec Identity</span></span>

<span data-ttu-id="75119-110">En la tabla siguiente se proporciona información de identificación del códec.</span><span class="sxs-lookup"><span data-stu-id="75119-110">The following table provides codec identification information.</span></span>



|                        |                                 |
|------------------------|---------------------------------|
| <span data-ttu-id="75119-111">Nombres formales</span><span class="sxs-lookup"><span data-stu-id="75119-111">Formal Name(s)</span></span>         | <span data-ttu-id="75119-112">Tagged Image File Format (TIFF)</span><span class="sxs-lookup"><span data-stu-id="75119-112">Tagged Image File Format (TIFF)</span></span> |
| <span data-ttu-id="75119-113">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="75119-113">File Name Extension(s)</span></span> | <span data-ttu-id="75119-114">TIFF, TIF</span><span class="sxs-lookup"><span data-stu-id="75119-114">tiff, tif</span></span>                       |
| <span data-ttu-id="75119-115">Tipos MIME</span><span class="sxs-lookup"><span data-stu-id="75119-115">MIME type(s)</span></span>           | <span data-ttu-id="75119-116">imagen/TIFF, imagen/TIF</span><span class="sxs-lookup"><span data-stu-id="75119-116">image/tiff, image/tif</span></span>           |
| <span data-ttu-id="75119-117">Compatibilidad con las especificaciones</span><span class="sxs-lookup"><span data-stu-id="75119-117">Specification Support</span></span>  | <span data-ttu-id="75119-118">Especificación TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="75119-118">TIFF Specification 6.0</span></span>          |



 

<span data-ttu-id="75119-119">En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes del códec TIFF nativo.</span><span class="sxs-lookup"><span data-stu-id="75119-119">The following table lists the GUIDs used to identify the native TIFF codec components.</span></span>



| <span data-ttu-id="75119-120">Componente</span><span class="sxs-lookup"><span data-stu-id="75119-120">Component</span></span>        | <span data-ttu-id="75119-121">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="75119-121">Friendly Name</span></span>             | <span data-ttu-id="75119-122">GUID</span><span class="sxs-lookup"><span data-stu-id="75119-122">GUID</span></span>                                 |
|------------------|---------------------------|--------------------------------------|
| <span data-ttu-id="75119-123">Formato de contenedor</span><span class="sxs-lookup"><span data-stu-id="75119-123">Container Format</span></span> | <span data-ttu-id="75119-124">GUID \_ ContainerFormatTiff</span><span class="sxs-lookup"><span data-stu-id="75119-124">GUID\_ContainerFormatTiff</span></span> | <span data-ttu-id="75119-125">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span><span class="sxs-lookup"><span data-stu-id="75119-125">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span></span>  |
| <span data-ttu-id="75119-126">Descodificador</span><span class="sxs-lookup"><span data-stu-id="75119-126">Decoder</span></span>          | <span data-ttu-id="75119-127">CLSID \_ WICTiffDecoder</span><span class="sxs-lookup"><span data-stu-id="75119-127">CLSID\_WICTiffDecoder</span></span>     | <span data-ttu-id="75119-128">b54e85d9-fe23-499f-8b886acea7137502b</span><span class="sxs-lookup"><span data-stu-id="75119-128">b54e85d9-fe23-499f-8b886acea7137502b</span></span> |
| <span data-ttu-id="75119-129">Codificador</span><span class="sxs-lookup"><span data-stu-id="75119-129">Encoder</span></span>          | <span data-ttu-id="75119-130">CLSID \_ WICTiffEncoder</span><span class="sxs-lookup"><span data-stu-id="75119-130">CLSID\_WICTiffEncoder</span></span>     | <span data-ttu-id="75119-131">0131be10-2001-4c5f-a9b0cc88fab64ce8</span><span class="sxs-lookup"><span data-stu-id="75119-131">0131be10-2001-4c5f-a9b0cc88fab64ce8</span></span>  |



 

## <a name="encoding"></a><span data-ttu-id="75119-132">Encoding</span><span class="sxs-lookup"><span data-stu-id="75119-132">Encoding</span></span>

<span data-ttu-id="75119-133">La API de codificación WIC está diseñada para ser independiente del códec y la codificación de imágenes para los códecs habilitados para WIC es esencialmente la misma.</span><span class="sxs-lookup"><span data-stu-id="75119-133">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="75119-134">Para obtener más información sobre la codificación de imágenes mediante la API de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.</span><span class="sxs-lookup"><span data-stu-id="75119-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="75119-135">Opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="75119-135">Encoder Options</span></span>

<span data-ttu-id="75119-136">Los códecs habilitados para WIC difieren en el nivel de opción de codificación.</span><span class="sxs-lookup"><span data-stu-id="75119-136">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="75119-137">Las opciones del codificador reflejan las capacidades de un codificador de imágenes y cada códec nativo admite un conjunto de estas opciones de codificador.</span><span class="sxs-lookup"><span data-stu-id="75119-137">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="75119-138">Las opciones del codificador pueden ser opciones básicas de WIC compatibles disponibles para todos los códigos habilitados para WIC (aunque no se admiten necesariamente) o las opciones específicas del códec diseñadas con el códec formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="75119-138">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="75119-139">Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la interfaz [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="75119-139">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="75119-140">Para obtener más información sobre el uso de la interfaz **IPropertyBag2** para la codificación de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.</span><span class="sxs-lookup"><span data-stu-id="75119-140">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="75119-141">El códec TIFF usa las opciones básicas de WIC.</span><span class="sxs-lookup"><span data-stu-id="75119-141">The TIFF codec uses basic WIC options.</span></span> <span data-ttu-id="75119-142">En la tabla siguiente se enumeran las opciones del codificador WIC admitidas por el códec TIFF nativo.</span><span class="sxs-lookup"><span data-stu-id="75119-142">The following table lists the WIC encoder options supported by the native TIFF codec.</span></span>

| <span data-ttu-id="75119-143">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="75119-143">Property Name</span></span>         | <span data-ttu-id="75119-144">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="75119-144">VARTYPE</span></span> | <span data-ttu-id="75119-145">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="75119-145">Value Range</span></span> | <span data-ttu-id="75119-146">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="75119-146">Default Value</span></span>    |
|-----------------------|---------|-------------|------------------|
| <span data-ttu-id="75119-147">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="75119-147">CompressionQuality</span></span>    | <span data-ttu-id="75119-148">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="75119-148">VT\_R4</span></span>  | <span data-ttu-id="75119-149">0-1,0</span><span class="sxs-lookup"><span data-stu-id="75119-149">0 - 1.0</span></span>     | <span data-ttu-id="75119-150">0</span><span class="sxs-lookup"><span data-stu-id="75119-150">0</span></span>                |
| <span data-ttu-id="75119-151">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="75119-151">TiffCompressionMethod</span></span> | <span data-ttu-id="75119-152">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="75119-152">VT\_UI1</span></span> | [<span data-ttu-id="75119-153">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="75119-153">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [<span data-ttu-id="75119-154">**WICTiffCompressionDontCare**</span><span class="sxs-lookup"><span data-stu-id="75119-154">**WICTiffCompressionDontCare**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

<span data-ttu-id="75119-155">Si una opción de codificador está presente en la lista de opciones [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que el códec no admite, se omite.</span><span class="sxs-lookup"><span data-stu-id="75119-155">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="compressionquality-option"></a><span data-ttu-id="75119-156">Opción CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="75119-156">CompressionQuality Option</span></span>

<span data-ttu-id="75119-157">Especifica la calidad de compresión deseada.</span><span class="sxs-lookup"><span data-stu-id="75119-157">Specifies the desired compression quality.</span></span> <span data-ttu-id="75119-158">0,0 indica el esquema de compresión menos eficaz disponible.</span><span class="sxs-lookup"><span data-stu-id="75119-158">0.0 indicates the least efficient compression scheme available.</span></span> <span data-ttu-id="75119-159">Normalmente, este esquema da como resultado una codificación más rápida pero una salida más grande.</span><span class="sxs-lookup"><span data-stu-id="75119-159">Typically, this scheme results in a faster encode but larger output.</span></span> <span data-ttu-id="75119-160">Un valor de 1,0 especifica el esquema de compresión más eficaz disponible.</span><span class="sxs-lookup"><span data-stu-id="75119-160">A value of 1.0 specifies the most efficient compression scheme available.</span></span> <span data-ttu-id="75119-161">Normalmente, este esquema da como resultado una codificación más larga, pero genera una salida más pequeña.</span><span class="sxs-lookup"><span data-stu-id="75119-161">Typically, this scheme results in a longer encode but produces smaller output.</span></span>

<span data-ttu-id="75119-162">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="75119-162">The default value is 0.</span></span>

### <a name="tiffcompressionmethod-option"></a><span data-ttu-id="75119-163">Opción TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="75119-163">TiffCompressionMethod Option</span></span>

<span data-ttu-id="75119-164">Especifica el método de compresión TIFF.</span><span class="sxs-lookup"><span data-stu-id="75119-164">Specifies the TIFF compression method.</span></span>

<span data-ttu-id="75119-165">El valor predeterminado es [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span><span class="sxs-lookup"><span data-stu-id="75119-165">The default value is [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span></span>

## <a name="decoding"></a><span data-ttu-id="75119-166">Descodificación</span><span class="sxs-lookup"><span data-stu-id="75119-166">Decoding</span></span>

<span data-ttu-id="75119-167">Las API de descodificación de WIC están diseñadas para ser independientes del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma.</span><span class="sxs-lookup"><span data-stu-id="75119-167">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="75119-168">Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="75119-168">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="75119-169">Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="75119-169">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
