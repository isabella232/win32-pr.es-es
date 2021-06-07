---
description: En este tema se proporciona información sobre el códec PNG nativo disponible a través Windows Imaging Component (WIC).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Información general sobre el formato PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb00b7530a22fcdbcce112053431ace5e553383
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444446"
---
# <a name="png-format-overview"></a><span data-ttu-id="24903-103">Información general sobre el formato PNG</span><span class="sxs-lookup"><span data-stu-id="24903-103">PNG Format Overview</span></span>

<span data-ttu-id="24903-104">En este tema se proporciona información sobre el códec PNG nativo disponible a través Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="24903-104">This topic provides information about the native PNG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="24903-105">Identidad de códec</span><span class="sxs-lookup"><span data-stu-id="24903-105">Codec Identity</span></span>

<span data-ttu-id="24903-106">En la tabla siguiente se proporciona información de identificación de códecs.</span><span class="sxs-lookup"><span data-stu-id="24903-106">The following table provides codec identification information.</span></span>



|     <span data-ttu-id="24903-107">Componente</span><span class="sxs-lookup"><span data-stu-id="24903-107">Component</span></span>          | <span data-ttu-id="24903-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="24903-108">Description</span></span>                     |
|------------------------|---------------------------------|
| <span data-ttu-id="24903-109">Nombres formales</span><span class="sxs-lookup"><span data-stu-id="24903-109">Formal Name(s)</span></span>         | <span data-ttu-id="24903-110">Formato PNG (Portable Network Graphics)</span><span class="sxs-lookup"><span data-stu-id="24903-110">Portable Network Graphics (PNG)</span></span> |
| <span data-ttu-id="24903-111">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="24903-111">File Name Extension(s)</span></span> | <span data-ttu-id="24903-112">png</span><span class="sxs-lookup"><span data-stu-id="24903-112">png</span></span>                             |
| <span data-ttu-id="24903-113">Tipo de MIME</span><span class="sxs-lookup"><span data-stu-id="24903-113">MIME type</span></span>              | <span data-ttu-id="24903-114">image/png</span><span class="sxs-lookup"><span data-stu-id="24903-114">image/png</span></span>                       |
| <span data-ttu-id="24903-115">Compatibilidad con especificaciones</span><span class="sxs-lookup"><span data-stu-id="24903-115">Specification Support</span></span>  | <span data-ttu-id="24903-116">Especificación PNG 1.2</span><span class="sxs-lookup"><span data-stu-id="24903-116">PNG Specification 1.2</span></span>           |



 

<span data-ttu-id="24903-117">En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes de códec PNG nativos.</span><span class="sxs-lookup"><span data-stu-id="24903-117">The following table lists the GUIDs used to identify the native PNG codec components.</span></span>



| <span data-ttu-id="24903-118">Componente</span><span class="sxs-lookup"><span data-stu-id="24903-118">Component</span></span>        | <span data-ttu-id="24903-119">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="24903-119">Friendly Name</span></span>            | <span data-ttu-id="24903-120">GUID</span><span class="sxs-lookup"><span data-stu-id="24903-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="24903-121">Formato de contenedor</span><span class="sxs-lookup"><span data-stu-id="24903-121">Container Format</span></span> | <span data-ttu-id="24903-122">GUID \_ ContainerFormatPng</span><span class="sxs-lookup"><span data-stu-id="24903-122">GUID\_ContainerFormatPng</span></span> | <span data-ttu-id="24903-123">1b7cfaf4-713f-473c-qued6137425faeaf</span><span class="sxs-lookup"><span data-stu-id="24903-123">1b7cfaf4-713f-473c-bbcd6137425faeaf</span></span> |
| <span data-ttu-id="24903-124">Descodificador</span><span class="sxs-lookup"><span data-stu-id="24903-124">Decoder</span></span>          | <span data-ttu-id="24903-125">CLSID \_ WICPngDecoder</span><span class="sxs-lookup"><span data-stu-id="24903-125">CLSID\_WICPngDecoder</span></span>     | <span data-ttu-id="24903-126">389ea17b-5078-4cde-b6ef25c15175c751</span><span class="sxs-lookup"><span data-stu-id="24903-126">389ea17b-5078-4cde-b6ef25c15175c751</span></span> |
| <span data-ttu-id="24903-127">Codificador</span><span class="sxs-lookup"><span data-stu-id="24903-127">Encoder</span></span>          | <span data-ttu-id="24903-128">CLSID \_ WICPngEncoder</span><span class="sxs-lookup"><span data-stu-id="24903-128">CLSID\_WICPngEncoder</span></span>     | <span data-ttu-id="24903-129">27949969-876a-41d7-9447568f6a35a4dc</span><span class="sxs-lookup"><span data-stu-id="24903-129">27949969-876a-41d7-9447568f6a35a4dc</span></span> |



 

### <a name="windows-8-and-later"></a><span data-ttu-id="24903-130">Windows 8 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="24903-130">Windows 8 and later</span></span>

<span data-ttu-id="24903-131">A partir de Windows 8 WIC proporciona un descodificador PNG adicional</span><span class="sxs-lookup"><span data-stu-id="24903-131">Starting with Windows 8 WIC provides an additional PNG decoder</span></span>

## <a name="encoding"></a><span data-ttu-id="24903-132">Encoding</span><span class="sxs-lookup"><span data-stu-id="24903-132">Encoding</span></span>

<span data-ttu-id="24903-133">La API de codificación wic está diseñada para ser independiente del códec y la codificación de imágenes para códecs habilitados para WIC es básicamente la misma.</span><span class="sxs-lookup"><span data-stu-id="24903-133">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="24903-134">Para más información sobre la codificación de imágenes mediante la API de WIC, consulte Información general [sobre codificación.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="24903-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="24903-135">Opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="24903-135">Encoder Options</span></span>

<span data-ttu-id="24903-136">Los códecs habilitados para WIC difieren en el nivel de opción de codificación.</span><span class="sxs-lookup"><span data-stu-id="24903-136">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="24903-137">Las opciones del codificador reflejan las funcionalidades de un codificador de imagen y cada códec nativo admite un conjunto de estas opciones de codificador.</span><span class="sxs-lookup"><span data-stu-id="24903-137">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="24903-138">Las opciones del codificador pueden ser opciones básicas compatibles con WIC disponibles para todos los códigos habilitados para WIC (aunque no necesariamente admitidos) o opciones específicas del códec diseñadas por el códec de formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="24903-138">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="24903-139">Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la [**interfaz IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="24903-139">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="24903-140">Para obtener más información sobre el uso de la **interfaz IPropertyBag2** para la codificación WIC , vea Información general [sobre codificación](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="24903-140">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="24903-141">El códec PNG usa opciones básicas del codificador WIC.</span><span class="sxs-lookup"><span data-stu-id="24903-141">The PNG codec uses basic WIC encoder options.</span></span> <span data-ttu-id="24903-142">En la tabla siguiente se enumeran las opciones del codificador WIC compatibles con el códec PNG nativo.</span><span class="sxs-lookup"><span data-stu-id="24903-142">The following table lists the WIC encoder options supported by the native PNG codec.</span></span>



| <span data-ttu-id="24903-143">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="24903-143">Property Name</span></span>   | <span data-ttu-id="24903-144">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="24903-144">VARTYPE</span></span>  | <span data-ttu-id="24903-145">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="24903-145">Value Range</span></span>                                                 | <span data-ttu-id="24903-146">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="24903-146">Default Value</span></span>                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="24903-147">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="24903-147">InterlaceOption</span></span> | <span data-ttu-id="24903-148">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="24903-148">VT\_BOOL</span></span> | <span data-ttu-id="24903-149">**TRUE** / **FALSE**</span><span class="sxs-lookup"><span data-stu-id="24903-149">**TRUE**/**FALSE**</span></span>                                          | <span data-ttu-id="24903-150">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="24903-150">**FALSE**</span></span>                                                        |
| <span data-ttu-id="24903-151">FilterOption</span><span class="sxs-lookup"><span data-stu-id="24903-151">FilterOption</span></span>    | <span data-ttu-id="24903-152">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="24903-152">VT\_UI1</span></span>  | [<span data-ttu-id="24903-153">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="24903-153">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [<span data-ttu-id="24903-154">**WICPngFilterUnspecified**</span><span class="sxs-lookup"><span data-stu-id="24903-154">**WICPngFilterUnspecified**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

<span data-ttu-id="24903-155">Si hay una opción de codificador en la [**lista de opciones IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que el códec no admite, se omite.</span><span class="sxs-lookup"><span data-stu-id="24903-155">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="interlaceoption"></a><span data-ttu-id="24903-156">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="24903-156">InterlaceOption</span></span>

<span data-ttu-id="24903-157">Especifica si se codifican los datos de la imagen como entrelazados.</span><span class="sxs-lookup"><span data-stu-id="24903-157">Specifies whether to encode the image data as interlaced.</span></span>

<span data-ttu-id="24903-158">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="24903-158">The default value is **FALSE**.</span></span>

### <a name="filteroption"></a><span data-ttu-id="24903-159">FilterOption</span><span class="sxs-lookup"><span data-stu-id="24903-159">FilterOption</span></span>

<span data-ttu-id="24903-160">Especifica la opción de filtro que se usará para la compresión de imágenes.</span><span class="sxs-lookup"><span data-stu-id="24903-160">Specifies the filter option to use for image compression.</span></span>

<span data-ttu-id="24903-161">El valor predeterminado es [**WICPngFilterUnspecified.**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)</span><span class="sxs-lookup"><span data-stu-id="24903-161">The default value is [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span></span>

## <a name="decoding"></a><span data-ttu-id="24903-162">Descodificación</span><span class="sxs-lookup"><span data-stu-id="24903-162">Decoding</span></span>

<span data-ttu-id="24903-163">La API de decoding de WIC está diseñada para ser independiente del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma.</span><span class="sxs-lookup"><span data-stu-id="24903-163">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="24903-164">Para obtener más información sobre lacodación de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="24903-164">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="24903-165">Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="24903-165">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="24903-166">El códec PNG nativo también admite [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) en lacodización de fotogramas y agrega opciones avanzadas para la decodización de un flujo de imagen.</span><span class="sxs-lookup"><span data-stu-id="24903-166">The native PNG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advanced options for decoding an image stream.</span></span> <span data-ttu-id="24903-167">Para obtener más información sobre estas opciones avanzadas, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="24903-167">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
