---
description: En este tema se proporciona información sobre el códec BMP nativo disponible a través Windows Imaging Component (WIC).
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Información general sobre el formato BMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975f27af5b731ed1f62f3571109553848705239
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444966"
---
# <a name="bmp-format-overview"></a><span data-ttu-id="19409-103">Información general sobre el formato BMP</span><span class="sxs-lookup"><span data-stu-id="19409-103">BMP Format Overview</span></span>

<span data-ttu-id="19409-104">En este tema se proporciona información sobre el códec BMP nativo disponible a través Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="19409-104">This topic provides information about the native BMP codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="19409-105">Identidad de códec</span><span class="sxs-lookup"><span data-stu-id="19409-105">Codec Identity</span></span>

<span data-ttu-id="19409-106">En la tabla siguiente se proporciona información de identificación de códecs.</span><span class="sxs-lookup"><span data-stu-id="19409-106">The following table provides codec identification information.</span></span>



| <span data-ttu-id="19409-107">Componente</span><span class="sxs-lookup"><span data-stu-id="19409-107">Component</span></span>              | <span data-ttu-id="19409-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="19409-108">Description</span></span>           |
|------------------------|-----------------------|
| <span data-ttu-id="19409-109">Nombres formales</span><span class="sxs-lookup"><span data-stu-id="19409-109">Formal Name(s)</span></span>         | <span data-ttu-id="19409-110">Formato de mapa de bits de Windows</span><span class="sxs-lookup"><span data-stu-id="19409-110">Windows Bitmap Format</span></span> |
| <span data-ttu-id="19409-111">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="19409-111">File Name Extension(s)</span></span> | <span data-ttu-id="19409-112">bmp, dib</span><span class="sxs-lookup"><span data-stu-id="19409-112">bmp, dib</span></span>              |
| <span data-ttu-id="19409-113">Tipo de MIME</span><span class="sxs-lookup"><span data-stu-id="19409-113">MIME type</span></span>              | <span data-ttu-id="19409-114">image/bmp</span><span class="sxs-lookup"><span data-stu-id="19409-114">image/bmp</span></span>             |
| <span data-ttu-id="19409-115">Compatibilidad con especificaciones</span><span class="sxs-lookup"><span data-stu-id="19409-115">Specification Support</span></span>  | <span data-ttu-id="19409-116">Especificación BMP v5</span><span class="sxs-lookup"><span data-stu-id="19409-116">BMP Specification v5</span></span>  |



 

<span data-ttu-id="19409-117">En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes de códec BMP nativos.</span><span class="sxs-lookup"><span data-stu-id="19409-117">The following table lists the GUIDs used to identify the native BMP codec components.</span></span>



| <span data-ttu-id="19409-118">Componente</span><span class="sxs-lookup"><span data-stu-id="19409-118">Component</span></span>        | <span data-ttu-id="19409-119">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="19409-119">Friendly Name</span></span>            | <span data-ttu-id="19409-120">GUID</span><span class="sxs-lookup"><span data-stu-id="19409-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="19409-121">Formato de contenedor</span><span class="sxs-lookup"><span data-stu-id="19409-121">Container Format</span></span> | <span data-ttu-id="19409-122">GUID \_ ContainerFormatBmp</span><span class="sxs-lookup"><span data-stu-id="19409-122">GUID\_ContainerFormatBmp</span></span> | <span data-ttu-id="19409-123">0af1d87e-fcfe-4188-bdeba7906471cbe3</span><span class="sxs-lookup"><span data-stu-id="19409-123">0af1d87e-fcfe-4188-bdeba7906471cbe3</span></span> |
| <span data-ttu-id="19409-124">Descodificador</span><span class="sxs-lookup"><span data-stu-id="19409-124">Decoder</span></span>          | <span data-ttu-id="19409-125">CLSID \_ WICBmpDecoder</span><span class="sxs-lookup"><span data-stu-id="19409-125">CLSID\_WICBmpDecoder</span></span>     | <span data-ttu-id="19409-126">6b462062-7cbf-400d-9fdb813ddd10f2778</span><span class="sxs-lookup"><span data-stu-id="19409-126">6b462062-7cbf-400d-9fdb813dd10f2778</span></span> |
| <span data-ttu-id="19409-127">Codificador</span><span class="sxs-lookup"><span data-stu-id="19409-127">Encoder</span></span>          | <span data-ttu-id="19409-128">CLSID \_ WICBmpEncoder</span><span class="sxs-lookup"><span data-stu-id="19409-128">CLSID\_WICBmpEncoder</span></span>     | <span data-ttu-id="19409-129">69be8bb4-d66d-47c8-865aed1589433782</span><span class="sxs-lookup"><span data-stu-id="19409-129">69be8bb4-d66d-47c8-865aed1589433782</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="19409-130">Encoding</span><span class="sxs-lookup"><span data-stu-id="19409-130">Encoding</span></span>

<span data-ttu-id="19409-131">La API de codificación WIC está diseñada para ser independiente del códec y, por tanto, la codificación de imágenes para códecs habilitados para WIC es básicamente la misma.</span><span class="sxs-lookup"><span data-stu-id="19409-131">The WIC encoding API are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="19409-132">Para más información sobre la codificación de imágenes mediante la API de WIC, consulte Información general [sobre codificación.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="19409-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="19409-133">Opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="19409-133">Encoder Options</span></span>

<span data-ttu-id="19409-134">Los códecs habilitados para WIC difieren en el nivel de opción de codificación.</span><span class="sxs-lookup"><span data-stu-id="19409-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="19409-135">Las opciones del codificador reflejan las funcionalidades de un codificador de imagen y cada códec nativo admite un conjunto de estas opciones de codificador.</span><span class="sxs-lookup"><span data-stu-id="19409-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="19409-136">Las opciones del codificador pueden ser opciones básicas compatibles con WIC disponibles para todos los códigos habilitados para WIC (aunque no necesariamente admitidos) o opciones específicas del códec diseñadas por el códec de formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="19409-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="19409-137">Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la [**interfaz IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="19409-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="19409-138">Para obtener más información sobre el uso de la **interfaz IPropertyBag2** para la codificación WIC, vea Información general [sobre codificación](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="19409-138">For more information about using the **IPropertyBag2** interface for WIC encoding see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="19409-139">En la tabla siguiente se enumeran las opciones del codificador WIC compatibles con el códec BMP nativo.</span><span class="sxs-lookup"><span data-stu-id="19409-139">The following table lists the WIC encoder options supported by the native BMP codec.</span></span>



| <span data-ttu-id="19409-140">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="19409-140">Property Name</span></span>               | <span data-ttu-id="19409-141">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="19409-141">VARTYPE</span></span>      | <span data-ttu-id="19409-142">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="19409-142">Value Range</span></span>                      | <span data-ttu-id="19409-143">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="19409-143">Default Value</span></span>      |
|-----------------------------|--------------|----------------------------------|--------------------|
| <span data-ttu-id="19409-144">**EnableV5Header32bppBGRA**</span><span class="sxs-lookup"><span data-stu-id="19409-144">**EnableV5Header32bppBGRA**</span></span> | <span data-ttu-id="19409-145">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="19409-145">**VT\_BOOL**</span></span> | <span data-ttu-id="19409-146">**VARIANT \_ TRUE/VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="19409-146">**VARIANT\_TRUE/VARIANT\_FALSE**</span></span> | <span data-ttu-id="19409-147">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="19409-147">**VARIANT\_FALSE**</span></span> |



 

### <a name="enablev5header32bppbgra"></a><span data-ttu-id="19409-148">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="19409-148">EnableV5Header32bppBGRA</span></span>

<span data-ttu-id="19409-149">Especifica si se permiten los datos de codificación en el formato de píxel \_ WICPixelFormat32bppBGRA guid.</span><span class="sxs-lookup"><span data-stu-id="19409-149">Specifies whether to allow encoding data in the GUID\_WICPixelFormat32bppBGRA pixel format.</span></span> <span data-ttu-id="19409-150">Si esta opción se establece en **VARIANT \_ TRUE,** bmp se escribirá con un encabezado BITMAPV5HEADER.</span><span class="sxs-lookup"><span data-stu-id="19409-150">If this option is set to **VARIANT\_TRUE**, the BMP will be written out with a BITMAPV5HEADER header.</span></span>

<span data-ttu-id="19409-151">El valor predeterminado es **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="19409-151">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="19409-152">Si hay una opción de codificador en la lista de opciones IPropertyBag2 que el códec no admite, se omite.</span><span class="sxs-lookup"><span data-stu-id="19409-152">If an encoder option is present in the IPropertyBag2 option list that the codec does not support, it is ignored.</span></span>

<span data-ttu-id="19409-153">Tenga en cuenta que para los archivos BMP de Windows de 16 y 32 bits, el códec BMP omite cualquier canal alfa, ya que muchos archivos de imagen heredados contienen datos no válidos en este canal adicional.</span><span class="sxs-lookup"><span data-stu-id="19409-153">Note for 16-bit and 32-bit Windows BMP files, the BMP codec ignores any alpha channel, as many legacy image files contain invalid data in this extra channel.</span></span> <span data-ttu-id="19409-154">A partir Windows 8, los archivos BMP de Windows de 32 bits escritos con **BITMAPV5HEADER** con contenido de canal alfa válido se leen como WICPixelFormat32bppBGRA.</span><span class="sxs-lookup"><span data-stu-id="19409-154">Starting with Windows 8, 32-bit Windows BMP files written using the **BITMAPV5HEADER** with valid alpha channel content are read as WICPixelFormat32bppBGRA</span></span>

## <a name="decoding"></a><span data-ttu-id="19409-155">Descodificación</span><span class="sxs-lookup"><span data-stu-id="19409-155">Decoding</span></span>

<span data-ttu-id="19409-156">La API de decoding de WIC está diseñada para ser independiente del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma.</span><span class="sxs-lookup"><span data-stu-id="19409-156">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="19409-157">Para obtener más información sobre lacodación de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="19409-157">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="19409-158">Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="19409-158">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
