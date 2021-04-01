---
description: En este tema se proporciona información sobre el códec BMP nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Información general sobre el formato BMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3492189f80b43915bab94a7ea8359f2e5950f7c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814238"
---
# <a name="bmp-format-overview"></a><span data-ttu-id="ef4c7-103">Información general sobre el formato BMP</span><span class="sxs-lookup"><span data-stu-id="ef4c7-103">BMP Format Overview</span></span>

<span data-ttu-id="ef4c7-104">En este tema se proporciona información sobre el códec BMP nativo disponible a través de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="ef4c7-104">This topic provides information about the native BMP codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="ef4c7-105">Identidad del códec</span><span class="sxs-lookup"><span data-stu-id="ef4c7-105">Codec Identity</span></span>

<span data-ttu-id="ef4c7-106">En la tabla siguiente se proporciona información de identificación del códec.</span><span class="sxs-lookup"><span data-stu-id="ef4c7-106">The following table provides codec identification information.</span></span>



|                        |                       |
|------------------------|-----------------------|
| <span data-ttu-id="ef4c7-107">Nombres formales</span><span class="sxs-lookup"><span data-stu-id="ef4c7-107">Formal Name(s)</span></span>         | <span data-ttu-id="ef4c7-108">Formato de mapa de bits de Windows</span><span class="sxs-lookup"><span data-stu-id="ef4c7-108">Windows Bitmap Format</span></span> |
| <span data-ttu-id="ef4c7-109">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="ef4c7-109">File Name Extension(s)</span></span> | <span data-ttu-id="ef4c7-110">BMP, DIB</span><span class="sxs-lookup"><span data-stu-id="ef4c7-110">bmp, dib</span></span>              |
| <span data-ttu-id="ef4c7-111">Tipo de MIME</span><span class="sxs-lookup"><span data-stu-id="ef4c7-111">MIME type</span></span>              | <span data-ttu-id="ef4c7-112">image/bmp</span><span class="sxs-lookup"><span data-stu-id="ef4c7-112">image/bmp</span></span>             |
| <span data-ttu-id="ef4c7-113">Compatibilidad con las especificaciones</span><span class="sxs-lookup"><span data-stu-id="ef4c7-113">Specification Support</span></span>  | <span data-ttu-id="ef4c7-114">Especificación de BMP V5</span><span class="sxs-lookup"><span data-stu-id="ef4c7-114">BMP Specification v5</span></span>  |



 

<span data-ttu-id="ef4c7-115">En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes nativos del códec BMP.</span><span class="sxs-lookup"><span data-stu-id="ef4c7-115">The following table lists the GUIDs used to identify the native BMP codec components.</span></span>



| <span data-ttu-id="ef4c7-116">Componente</span><span class="sxs-lookup"><span data-stu-id="ef4c7-116">Component</span></span>        | <span data-ttu-id="ef4c7-117">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="ef4c7-117">Friendly Name</span></span>            | <span data-ttu-id="ef4c7-118">GUID</span><span class="sxs-lookup"><span data-stu-id="ef4c7-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="ef4c7-119">Formato de contenedor</span><span class="sxs-lookup"><span data-stu-id="ef4c7-119">Container Format</span></span> | <span data-ttu-id="ef4c7-120">GUID \_ ContainerFormatBmp</span><span class="sxs-lookup"><span data-stu-id="ef4c7-120">GUID\_ContainerFormatBmp</span></span> | <span data-ttu-id="ef4c7-121">0af1d87e-fcfe-4188-bdeba7906471cbe3</span><span class="sxs-lookup"><span data-stu-id="ef4c7-121">0af1d87e-fcfe-4188-bdeba7906471cbe3</span></span> |
| <span data-ttu-id="ef4c7-122">Descodificador</span><span class="sxs-lookup"><span data-stu-id="ef4c7-122">Decoder</span></span>          | <span data-ttu-id="ef4c7-123">CLSID \_ WICBmpDecoder</span><span class="sxs-lookup"><span data-stu-id="ef4c7-123">CLSID\_WICBmpDecoder</span></span>     | <span data-ttu-id="ef4c7-124">6b462062-7cbf-400d-9fdb813dd10f2778</span><span class="sxs-lookup"><span data-stu-id="ef4c7-124">6b462062-7cbf-400d-9fdb813dd10f2778</span></span> |
| <span data-ttu-id="ef4c7-125">Codificador</span><span class="sxs-lookup"><span data-stu-id="ef4c7-125">Encoder</span></span>          | <span data-ttu-id="ef4c7-126">CLSID \_ WICBmpEncoder</span><span class="sxs-lookup"><span data-stu-id="ef4c7-126">CLSID\_WICBmpEncoder</span></span>     | <span data-ttu-id="ef4c7-127">69be8bb4-d66d-47c8-865aed1589433782</span><span class="sxs-lookup"><span data-stu-id="ef4c7-127">69be8bb4-d66d-47c8-865aed1589433782</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="ef4c7-128">Encoding</span><span class="sxs-lookup"><span data-stu-id="ef4c7-128">Encoding</span></span>

<span data-ttu-id="ef4c7-129">La API de codificación WIC está diseñada para ser independiente del códec y, por lo tanto, la codificación de imágenes para códecs habilitados para WIC es esencialmente la misma.</span><span class="sxs-lookup"><span data-stu-id="ef4c7-129">The WIC encoding API are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="ef4c7-130">Para obtener más información sobre la codificación de imágenes mediante la API de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.</span><span class="sxs-lookup"><span data-stu-id="ef4c7-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="ef4c7-131">Opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="ef4c7-131">Encoder Options</span></span>

<span data-ttu-id="ef4c7-132">Los códecs habilitados para WIC difieren en el nivel de opción de codificación.</span><span class="sxs-lookup"><span data-stu-id="ef4c7-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="ef4c7-133">Las opciones del codificador reflejan las capacidades de un codificador de imágenes y cada códec nativo admite un conjunto de estas opciones de codificador.</span><span class="sxs-lookup"><span data-stu-id="ef4c7-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="ef4c7-134">Las opciones del codificador pueden ser opciones básicas de WIC compatibles disponibles para todos los códigos habilitados para WIC (aunque no se admiten necesariamente) o las opciones específicas del códec diseñadas con el códec formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="ef4c7-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="ef4c7-135">Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la interfaz [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ef4c7-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="ef4c7-136">Para obtener más información sobre el uso de la interfaz **IPropertyBag2** para la codificación de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.</span><span class="sxs-lookup"><span data-stu-id="ef4c7-136">For more information about using the **IPropertyBag2** interface for WIC encoding see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="ef4c7-137">En la tabla siguiente se enumeran las opciones del codificador WIC admitidas por el códec BMP nativo.</span><span class="sxs-lookup"><span data-stu-id="ef4c7-137">The following table lists the WIC encoder options supported by the native BMP codec.</span></span>



| <span data-ttu-id="ef4c7-138">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="ef4c7-138">Property Name</span></span>               | <span data-ttu-id="ef4c7-139">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ef4c7-139">VARTYPE</span></span>      | <span data-ttu-id="ef4c7-140">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="ef4c7-140">Value Range</span></span>                      | <span data-ttu-id="ef4c7-141">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="ef4c7-141">Default Value</span></span>      |
|-----------------------------|--------------|----------------------------------|--------------------|
| <span data-ttu-id="ef4c7-142">**EnableV5Header32bppBGRA**</span><span class="sxs-lookup"><span data-stu-id="ef4c7-142">**EnableV5Header32bppBGRA**</span></span> | <span data-ttu-id="ef4c7-143">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="ef4c7-143">**VT\_BOOL**</span></span> | <span data-ttu-id="ef4c7-144">**VARIANTE \_ verdadera/variante \_ falsa**</span><span class="sxs-lookup"><span data-stu-id="ef4c7-144">**VARIANT\_TRUE/VARIANT\_FALSE**</span></span> | <span data-ttu-id="ef4c7-145">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="ef4c7-145">**VARIANT\_FALSE**</span></span> |



 

### <a name="enablev5header32bppbgra"></a><span data-ttu-id="ef4c7-146">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="ef4c7-146">EnableV5Header32bppBGRA</span></span>

<span data-ttu-id="ef4c7-147">Especifica si se permite la codificación de datos en el \_ formato de píxel de GUID WICPixelFormat32bppBGRA.</span><span class="sxs-lookup"><span data-stu-id="ef4c7-147">Specifies whether to allow encoding data in the GUID\_WICPixelFormat32bppBGRA pixel format.</span></span> <span data-ttu-id="ef4c7-148">Si esta opción se establece en **Variant \_ true**, el BMP se escribirá con un encabezado BITMAPV5HEADER.</span><span class="sxs-lookup"><span data-stu-id="ef4c7-148">If this option is set to **VARIANT\_TRUE**, the BMP will be written out with a BITMAPV5HEADER header.</span></span>

<span data-ttu-id="ef4c7-149">El valor predeterminado es **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="ef4c7-149">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="ef4c7-150">Si una opción de codificador está presente en la lista de opciones IPropertyBag2 que el códec no admite, se omite.</span><span class="sxs-lookup"><span data-stu-id="ef4c7-150">If an encoder option is present in the IPropertyBag2 option list that the codec does not support, it is ignored.</span></span>

<span data-ttu-id="ef4c7-151">Nota para los archivos BMP de Windows de 16 y 32 bits, el códec BMP omite cualquier canal alfa, ya que muchos archivos de imagen heredados contienen datos no válidos en este canal adicional.</span><span class="sxs-lookup"><span data-stu-id="ef4c7-151">Note for 16-bit and 32-bit Windows BMP files, the BMP codec ignores any alpha channel, as many legacy image files contain invalid data in this extra channel.</span></span> <span data-ttu-id="ef4c7-152">A partir de Windows 8, los archivos BMP de Windows de 32 bits escritos con el **BITMAPV5HEADER** con contenido de canal alfa válido se leen como WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="ef4c7-152">Starting with Windows 8, 32-bit Windows BMP files written using the **BITMAPV5HEADER** with valid alpha channel content are read as WICPixelFormat32bppBGRA</span></span>

## <a name="decoding"></a><span data-ttu-id="ef4c7-153">Descodificación</span><span class="sxs-lookup"><span data-stu-id="ef4c7-153">Decoding</span></span>

<span data-ttu-id="ef4c7-154">La API de descodificación de WIC está diseñada para ser independiente del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma.</span><span class="sxs-lookup"><span data-stu-id="ef4c7-154">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="ef4c7-155">Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="ef4c7-155">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="ef4c7-156">Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="ef4c7-156">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
