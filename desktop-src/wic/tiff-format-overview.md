---
description: En este tema se proporciona información sobre el códec TIFF nativo disponible a través Windows Imaging Component (WIC).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Información general sobre el formato TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28dfcc85dac21e95e6c76118d2db57cb74a08
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444426"
---
# <a name="tiff-format-overview"></a><span data-ttu-id="5f869-103">Información general sobre el formato TIFF</span><span class="sxs-lookup"><span data-stu-id="5f869-103">TIFF Format Overview</span></span>

<span data-ttu-id="5f869-104">En este tema se proporciona información sobre el códec TIFF nativo disponible a través Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="5f869-104">This topic provides information about the native TIFF codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="5f869-105">Identidad de códec</span><span class="sxs-lookup"><span data-stu-id="5f869-105">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="5f869-106">Encoding</span><span class="sxs-lookup"><span data-stu-id="5f869-106">Encoding</span></span>](#encoding)
    -   [<span data-ttu-id="5f869-107">Opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="5f869-107">Encoder Options</span></span>](#encoder-options)
-   [<span data-ttu-id="5f869-108">Descodificación</span><span class="sxs-lookup"><span data-stu-id="5f869-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="5f869-109">Identidad de códec</span><span class="sxs-lookup"><span data-stu-id="5f869-109">Codec Identity</span></span>

<span data-ttu-id="5f869-110">En la tabla siguiente se proporciona información de identificación de códecs.</span><span class="sxs-lookup"><span data-stu-id="5f869-110">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="5f869-111">Componente</span><span class="sxs-lookup"><span data-stu-id="5f869-111">Component</span></span>            |   <span data-ttu-id="5f869-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f869-112">Description</span></span>                   |
|------------------------|---------------------------------|
| <span data-ttu-id="5f869-113">Nombres formales</span><span class="sxs-lookup"><span data-stu-id="5f869-113">Formal Name(s)</span></span>         | <span data-ttu-id="5f869-114">Tagged Image File Format (TIFF)</span><span class="sxs-lookup"><span data-stu-id="5f869-114">Tagged Image File Format (TIFF)</span></span> |
| <span data-ttu-id="5f869-115">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="5f869-115">File Name Extension(s)</span></span> | <span data-ttu-id="5f869-116">tiff, tif</span><span class="sxs-lookup"><span data-stu-id="5f869-116">tiff, tif</span></span>                       |
| <span data-ttu-id="5f869-117">Tipos MIME</span><span class="sxs-lookup"><span data-stu-id="5f869-117">MIME type(s)</span></span>           | <span data-ttu-id="5f869-118">image/tiff, image/tif</span><span class="sxs-lookup"><span data-stu-id="5f869-118">image/tiff, image/tif</span></span>           |
| <span data-ttu-id="5f869-119">Compatibilidad con especificaciones</span><span class="sxs-lookup"><span data-stu-id="5f869-119">Specification Support</span></span>  | <span data-ttu-id="5f869-120">Especificación TIFF 6.0</span><span class="sxs-lookup"><span data-stu-id="5f869-120">TIFF Specification 6.0</span></span>          |



 

<span data-ttu-id="5f869-121">En la tabla siguiente se enumeran los GUID usados para identificar los componentes de códec TIFF nativos.</span><span class="sxs-lookup"><span data-stu-id="5f869-121">The following table lists the GUIDs used to identify the native TIFF codec components.</span></span>



| <span data-ttu-id="5f869-122">Componente</span><span class="sxs-lookup"><span data-stu-id="5f869-122">Component</span></span>        | <span data-ttu-id="5f869-123">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="5f869-123">Friendly Name</span></span>             | <span data-ttu-id="5f869-124">GUID</span><span class="sxs-lookup"><span data-stu-id="5f869-124">GUID</span></span>                                 |
|------------------|---------------------------|--------------------------------------|
| <span data-ttu-id="5f869-125">Formato de contenedor</span><span class="sxs-lookup"><span data-stu-id="5f869-125">Container Format</span></span> | <span data-ttu-id="5f869-126">GUID \_ ContainerFormatTiff</span><span class="sxs-lookup"><span data-stu-id="5f869-126">GUID\_ContainerFormatTiff</span></span> | <span data-ttu-id="5f869-127">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span><span class="sxs-lookup"><span data-stu-id="5f869-127">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span></span>  |
| <span data-ttu-id="5f869-128">Descodificador</span><span class="sxs-lookup"><span data-stu-id="5f869-128">Decoder</span></span>          | <span data-ttu-id="5f869-129">CLSID \_ WICTiffDecoder</span><span class="sxs-lookup"><span data-stu-id="5f869-129">CLSID\_WICTiffDecoder</span></span>     | <span data-ttu-id="5f869-130">b54e85d9-fe23-499f-8b886acea7137502b</span><span class="sxs-lookup"><span data-stu-id="5f869-130">b54e85d9-fe23-499f-8b886acea7137502b</span></span> |
| <span data-ttu-id="5f869-131">Codificador</span><span class="sxs-lookup"><span data-stu-id="5f869-131">Encoder</span></span>          | <span data-ttu-id="5f869-132">CLSID \_ WICTiffEncoder</span><span class="sxs-lookup"><span data-stu-id="5f869-132">CLSID\_WICTiffEncoder</span></span>     | <span data-ttu-id="5f869-133">0131be10-2001-4c5f-a9b0cc88fab64ce8</span><span class="sxs-lookup"><span data-stu-id="5f869-133">0131be10-2001-4c5f-a9b0cc88fab64ce8</span></span>  |



 

## <a name="encoding"></a><span data-ttu-id="5f869-134">Encoding</span><span class="sxs-lookup"><span data-stu-id="5f869-134">Encoding</span></span>

<span data-ttu-id="5f869-135">La API de codificación WIC está diseñada para ser independiente del códec y la codificación de imágenes para códecs habilitados para WIC es básicamente la misma.</span><span class="sxs-lookup"><span data-stu-id="5f869-135">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="5f869-136">Para obtener más información sobre la codificación de imágenes mediante la API de WIC, vea Información general [sobre la codificación.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="5f869-136">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="5f869-137">Opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="5f869-137">Encoder Options</span></span>

<span data-ttu-id="5f869-138">Los códecs habilitados para WIC difieren en el nivel de opción de codificación.</span><span class="sxs-lookup"><span data-stu-id="5f869-138">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="5f869-139">Las opciones del codificador reflejan las funcionalidades de un codificador de imágenes y cada códec nativo admite un conjunto de estas opciones de codificador.</span><span class="sxs-lookup"><span data-stu-id="5f869-139">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="5f869-140">Las opciones de codificador pueden ser opciones básicas compatibles con WIC disponibles para todos los códigos habilitados para WIC (aunque no necesariamente admitidos) o opciones específicas del códec diseñadas por el códec de formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="5f869-140">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="5f869-141">Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la [**interfaz IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5f869-141">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="5f869-142">Para obtener más información sobre el uso de la **interfaz IPropertyBag2** para la codificación WIC , vea Información general [sobre la codificación.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="5f869-142">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="5f869-143">El códec TIFF usa opciones básicas de WIC.</span><span class="sxs-lookup"><span data-stu-id="5f869-143">The TIFF codec uses basic WIC options.</span></span> <span data-ttu-id="5f869-144">En la tabla siguiente se enumeran las opciones del codificador WIC compatibles con el códec TIFF nativo.</span><span class="sxs-lookup"><span data-stu-id="5f869-144">The following table lists the WIC encoder options supported by the native TIFF codec.</span></span>

| <span data-ttu-id="5f869-145">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="5f869-145">Property Name</span></span>         | <span data-ttu-id="5f869-146">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5f869-146">VARTYPE</span></span> | <span data-ttu-id="5f869-147">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="5f869-147">Value Range</span></span> | <span data-ttu-id="5f869-148">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="5f869-148">Default Value</span></span>    |
|-----------------------|---------|-------------|------------------|
| <span data-ttu-id="5f869-149">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="5f869-149">CompressionQuality</span></span>    | <span data-ttu-id="5f869-150">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="5f869-150">VT\_R4</span></span>  | <span data-ttu-id="5f869-151">0 - 1.0</span><span class="sxs-lookup"><span data-stu-id="5f869-151">0 - 1.0</span></span>     | <span data-ttu-id="5f869-152">0</span><span class="sxs-lookup"><span data-stu-id="5f869-152">0</span></span>                |
| <span data-ttu-id="5f869-153">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="5f869-153">TiffCompressionMethod</span></span> | <span data-ttu-id="5f869-154">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="5f869-154">VT\_UI1</span></span> | [<span data-ttu-id="5f869-155">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="5f869-155">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [<span data-ttu-id="5f869-156">**WICTiffCompressionDontCare**</span><span class="sxs-lookup"><span data-stu-id="5f869-156">**WICTiffCompressionDontCare**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

<span data-ttu-id="5f869-157">Si hay una opción de codificador en la lista [**de opciones IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que el códec no admite, se omite.</span><span class="sxs-lookup"><span data-stu-id="5f869-157">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="compressionquality-option"></a><span data-ttu-id="5f869-158">CompressionQuality (opción)</span><span class="sxs-lookup"><span data-stu-id="5f869-158">CompressionQuality Option</span></span>

<span data-ttu-id="5f869-159">Especifica la calidad de compresión deseada.</span><span class="sxs-lookup"><span data-stu-id="5f869-159">Specifies the desired compression quality.</span></span> <span data-ttu-id="5f869-160">0.0 indica el esquema de compresión menos eficaz disponible.</span><span class="sxs-lookup"><span data-stu-id="5f869-160">0.0 indicates the least efficient compression scheme available.</span></span> <span data-ttu-id="5f869-161">Normalmente, este esquema da como resultado una codificación más rápida, pero una salida mayor.</span><span class="sxs-lookup"><span data-stu-id="5f869-161">Typically, this scheme results in a faster encode but larger output.</span></span> <span data-ttu-id="5f869-162">Un valor de 1,0 especifica el esquema de compresión más eficaz disponible.</span><span class="sxs-lookup"><span data-stu-id="5f869-162">A value of 1.0 specifies the most efficient compression scheme available.</span></span> <span data-ttu-id="5f869-163">Normalmente, este esquema da como resultado una codificación más larga, pero genera una salida más pequeña.</span><span class="sxs-lookup"><span data-stu-id="5f869-163">Typically, this scheme results in a longer encode but produces smaller output.</span></span>

<span data-ttu-id="5f869-164">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="5f869-164">The default value is 0.</span></span>

### <a name="tiffcompressionmethod-option"></a><span data-ttu-id="5f869-165">Opción TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="5f869-165">TiffCompressionMethod Option</span></span>

<span data-ttu-id="5f869-166">Especifica el método de compresión TIFF.</span><span class="sxs-lookup"><span data-stu-id="5f869-166">Specifies the TIFF compression method.</span></span>

<span data-ttu-id="5f869-167">El valor predeterminado es [**WICTiffCompressionDontCare.**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)</span><span class="sxs-lookup"><span data-stu-id="5f869-167">The default value is [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span></span>

## <a name="decoding"></a><span data-ttu-id="5f869-168">Descodificación</span><span class="sxs-lookup"><span data-stu-id="5f869-168">Decoding</span></span>

<span data-ttu-id="5f869-169">Las API de decodificación de WIC están diseñadas para ser independientes del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma.</span><span class="sxs-lookup"><span data-stu-id="5f869-169">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="5f869-170">Para obtener más información sobre lacoding de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="5f869-170">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="5f869-171">Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="5f869-171">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
