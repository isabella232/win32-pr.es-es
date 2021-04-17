---
description: En este tema se proporciona información sobre el códec PNG nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Información general sobre el formato PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118d6af831c8fb6f8cacc8407e90f610c0fc426d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706874"
---
# <a name="png-format-overview"></a><span data-ttu-id="3fa9e-103">Información general sobre el formato PNG</span><span class="sxs-lookup"><span data-stu-id="3fa9e-103">PNG Format Overview</span></span>

<span data-ttu-id="3fa9e-104">En este tema se proporciona información sobre el códec PNG nativo disponible a través de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="3fa9e-104">This topic provides information about the native PNG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="3fa9e-105">Identidad del códec</span><span class="sxs-lookup"><span data-stu-id="3fa9e-105">Codec Identity</span></span>

<span data-ttu-id="3fa9e-106">En la tabla siguiente se proporciona información de identificación del códec.</span><span class="sxs-lookup"><span data-stu-id="3fa9e-106">The following table provides codec identification information.</span></span>



|                        |                                 |
|------------------------|---------------------------------|
| <span data-ttu-id="3fa9e-107">Nombres formales</span><span class="sxs-lookup"><span data-stu-id="3fa9e-107">Formal Name(s)</span></span>         | <span data-ttu-id="3fa9e-108">Formato PNG (Portable Network Graphics)</span><span class="sxs-lookup"><span data-stu-id="3fa9e-108">Portable Network Graphics (PNG)</span></span> |
| <span data-ttu-id="3fa9e-109">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="3fa9e-109">File Name Extension(s)</span></span> | <span data-ttu-id="3fa9e-110">png</span><span class="sxs-lookup"><span data-stu-id="3fa9e-110">png</span></span>                             |
| <span data-ttu-id="3fa9e-111">Tipo de MIME</span><span class="sxs-lookup"><span data-stu-id="3fa9e-111">MIME type</span></span>              | <span data-ttu-id="3fa9e-112">image/png</span><span class="sxs-lookup"><span data-stu-id="3fa9e-112">image/png</span></span>                       |
| <span data-ttu-id="3fa9e-113">Compatibilidad con las especificaciones</span><span class="sxs-lookup"><span data-stu-id="3fa9e-113">Specification Support</span></span>  | <span data-ttu-id="3fa9e-114">Especificación PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="3fa9e-114">PNG Specification 1.2</span></span>           |



 

<span data-ttu-id="3fa9e-115">En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes de códec PNG nativos.</span><span class="sxs-lookup"><span data-stu-id="3fa9e-115">The following table lists the GUIDs used to identify the native PNG codec components.</span></span>



| <span data-ttu-id="3fa9e-116">Componente</span><span class="sxs-lookup"><span data-stu-id="3fa9e-116">Component</span></span>        | <span data-ttu-id="3fa9e-117">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="3fa9e-117">Friendly Name</span></span>            | <span data-ttu-id="3fa9e-118">GUID</span><span class="sxs-lookup"><span data-stu-id="3fa9e-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="3fa9e-119">Formato de contenedor</span><span class="sxs-lookup"><span data-stu-id="3fa9e-119">Container Format</span></span> | <span data-ttu-id="3fa9e-120">GUID \_ ContainerFormatPng</span><span class="sxs-lookup"><span data-stu-id="3fa9e-120">GUID\_ContainerFormatPng</span></span> | <span data-ttu-id="3fa9e-121">1b7cfaf4-713f-473c-bbcd6137425faeaf</span><span class="sxs-lookup"><span data-stu-id="3fa9e-121">1b7cfaf4-713f-473c-bbcd6137425faeaf</span></span> |
| <span data-ttu-id="3fa9e-122">Descodificador</span><span class="sxs-lookup"><span data-stu-id="3fa9e-122">Decoder</span></span>          | <span data-ttu-id="3fa9e-123">CLSID \_ WICPngDecoder</span><span class="sxs-lookup"><span data-stu-id="3fa9e-123">CLSID\_WICPngDecoder</span></span>     | <span data-ttu-id="3fa9e-124">389ea17b-5078-4cde-b6ef25c15175c751</span><span class="sxs-lookup"><span data-stu-id="3fa9e-124">389ea17b-5078-4cde-b6ef25c15175c751</span></span> |
| <span data-ttu-id="3fa9e-125">Codificador</span><span class="sxs-lookup"><span data-stu-id="3fa9e-125">Encoder</span></span>          | <span data-ttu-id="3fa9e-126">CLSID \_ WICPngEncoder</span><span class="sxs-lookup"><span data-stu-id="3fa9e-126">CLSID\_WICPngEncoder</span></span>     | <span data-ttu-id="3fa9e-127">27949969-876a-41d7-9447568f6a35a4dc</span><span class="sxs-lookup"><span data-stu-id="3fa9e-127">27949969-876a-41d7-9447568f6a35a4dc</span></span> |



 

### <a name="windows-8-and-later"></a><span data-ttu-id="3fa9e-128">Windows 8 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="3fa9e-128">Windows 8 and later</span></span>

<span data-ttu-id="3fa9e-129">A partir de Windows 8, WIC proporciona un descodificador PNG adicional</span><span class="sxs-lookup"><span data-stu-id="3fa9e-129">Starting with Windows 8 WIC provides an additional PNG decoder</span></span>

## <a name="encoding"></a><span data-ttu-id="3fa9e-130">Encoding</span><span class="sxs-lookup"><span data-stu-id="3fa9e-130">Encoding</span></span>

<span data-ttu-id="3fa9e-131">La API de codificación WIC está diseñada para ser independiente del códec y la codificación de imágenes para los códecs habilitados para WIC es esencialmente la misma.</span><span class="sxs-lookup"><span data-stu-id="3fa9e-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="3fa9e-132">Para obtener más información sobre la codificación de imágenes mediante la API de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.</span><span class="sxs-lookup"><span data-stu-id="3fa9e-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="3fa9e-133">Opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="3fa9e-133">Encoder Options</span></span>

<span data-ttu-id="3fa9e-134">Los códecs habilitados para WIC difieren en el nivel de opción de codificación.</span><span class="sxs-lookup"><span data-stu-id="3fa9e-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="3fa9e-135">Las opciones del codificador reflejan las capacidades de un codificador de imágenes y cada códec nativo admite un conjunto de estas opciones de codificador.</span><span class="sxs-lookup"><span data-stu-id="3fa9e-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="3fa9e-136">Las opciones del codificador pueden ser opciones básicas de WIC compatibles disponibles para todos los códigos habilitados para WIC (aunque no se admiten necesariamente) o las opciones específicas del códec diseñadas con el códec formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="3fa9e-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="3fa9e-137">Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la interfaz [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3fa9e-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="3fa9e-138">Para obtener más información sobre el uso de la interfaz **IPropertyBag2** para la codificación de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.</span><span class="sxs-lookup"><span data-stu-id="3fa9e-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="3fa9e-139">El códec PNG usa las opciones básicas del codificador WIC.</span><span class="sxs-lookup"><span data-stu-id="3fa9e-139">The PNG codec uses basic WIC encoder options.</span></span> <span data-ttu-id="3fa9e-140">En la tabla siguiente se enumeran las opciones del codificador WIC admitidas por el códec PNG nativo.</span><span class="sxs-lookup"><span data-stu-id="3fa9e-140">The following table lists the WIC encoder options supported by the native PNG codec.</span></span>



| <span data-ttu-id="3fa9e-141">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="3fa9e-141">Property Name</span></span>   | <span data-ttu-id="3fa9e-142">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3fa9e-142">VARTYPE</span></span>  | <span data-ttu-id="3fa9e-143">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="3fa9e-143">Value Range</span></span>                                                 | <span data-ttu-id="3fa9e-144">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="3fa9e-144">Default Value</span></span>                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="3fa9e-145">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="3fa9e-145">InterlaceOption</span></span> | <span data-ttu-id="3fa9e-146">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="3fa9e-146">VT\_BOOL</span></span> | <span data-ttu-id="3fa9e-147">**True** / **False**</span><span class="sxs-lookup"><span data-stu-id="3fa9e-147">**TRUE**/**FALSE**</span></span>                                          | <span data-ttu-id="3fa9e-148">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3fa9e-148">**FALSE**</span></span>                                                        |
| <span data-ttu-id="3fa9e-149">FilterOption</span><span class="sxs-lookup"><span data-stu-id="3fa9e-149">FilterOption</span></span>    | <span data-ttu-id="3fa9e-150">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="3fa9e-150">VT\_UI1</span></span>  | [<span data-ttu-id="3fa9e-151">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="3fa9e-151">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [<span data-ttu-id="3fa9e-152">**WICPngFilterUnspecified**</span><span class="sxs-lookup"><span data-stu-id="3fa9e-152">**WICPngFilterUnspecified**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

<span data-ttu-id="3fa9e-153">Si una opción de codificador está presente en la lista de opciones [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que el códec no admite, se omite.</span><span class="sxs-lookup"><span data-stu-id="3fa9e-153">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="interlaceoption"></a><span data-ttu-id="3fa9e-154">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="3fa9e-154">InterlaceOption</span></span>

<span data-ttu-id="3fa9e-155">Especifica si se codifican los datos de la imagen como entrelazados.</span><span class="sxs-lookup"><span data-stu-id="3fa9e-155">Specifies whether to encode the image data as interlaced.</span></span>

<span data-ttu-id="3fa9e-156">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="3fa9e-156">The default value is **FALSE**.</span></span>

### <a name="filteroption"></a><span data-ttu-id="3fa9e-157">FilterOption</span><span class="sxs-lookup"><span data-stu-id="3fa9e-157">FilterOption</span></span>

<span data-ttu-id="3fa9e-158">Especifica la opción de filtro que se va a utilizar para la compresión de imágenes.</span><span class="sxs-lookup"><span data-stu-id="3fa9e-158">Specifies the filter option to use for image compression.</span></span>

<span data-ttu-id="3fa9e-159">El valor predeterminado es [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span><span class="sxs-lookup"><span data-stu-id="3fa9e-159">The default value is [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span></span>

## <a name="decoding"></a><span data-ttu-id="3fa9e-160">Descodificación</span><span class="sxs-lookup"><span data-stu-id="3fa9e-160">Decoding</span></span>

<span data-ttu-id="3fa9e-161">La API de descodificación de WIC está diseñada para ser independiente del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma.</span><span class="sxs-lookup"><span data-stu-id="3fa9e-161">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="3fa9e-162">Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="3fa9e-162">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="3fa9e-163">Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="3fa9e-163">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="3fa9e-164">El códec PNG nativo también admite [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) en la descodificación de fotogramas agregar opciones avanzadas para descodificar una secuencia de imágenes.</span><span class="sxs-lookup"><span data-stu-id="3fa9e-164">The native PNG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advanced options for decoding an image stream.</span></span> <span data-ttu-id="3fa9e-165">Para obtener más información acerca de estas opciones avanzadas, consulte la [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="3fa9e-165">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
