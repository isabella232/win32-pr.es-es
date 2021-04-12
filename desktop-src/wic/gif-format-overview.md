---
description: En este tema se proporciona información sobre el códec GIF nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Información general sobre el formato GIF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f592b50300edf79c71ff4050a2c0d5aeba8b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277770"
---
# <a name="gif-format-overview"></a><span data-ttu-id="988ac-103">Información general sobre el formato GIF</span><span class="sxs-lookup"><span data-stu-id="988ac-103">GIF Format Overview</span></span>

<span data-ttu-id="988ac-104">En este tema se proporciona información sobre el códec GIF nativo disponible a través de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="988ac-104">This topic provides information about the native GIF codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="988ac-105">Identidad del códec</span><span class="sxs-lookup"><span data-stu-id="988ac-105">Codec Identity</span></span>

<span data-ttu-id="988ac-106">En la tabla siguiente se proporciona información de identificación del códec.</span><span class="sxs-lookup"><span data-stu-id="988ac-106">The following table provides codec identification information.</span></span>



|                        |                                       |
|------------------------|---------------------------------------|
| <span data-ttu-id="988ac-107">Nombres formales</span><span class="sxs-lookup"><span data-stu-id="988ac-107">Formal Name(s)</span></span>         | <span data-ttu-id="988ac-108">Formato de intercambio de gráficos 89A (GIF)</span><span class="sxs-lookup"><span data-stu-id="988ac-108">Graphics Interchange Format 89a (GIF)</span></span> |
| <span data-ttu-id="988ac-109">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="988ac-109">File Name Extension(s)</span></span> | <span data-ttu-id="988ac-110">GIF</span><span class="sxs-lookup"><span data-stu-id="988ac-110">gif</span></span>                                   |
| <span data-ttu-id="988ac-111">Tipo de MIME</span><span class="sxs-lookup"><span data-stu-id="988ac-111">MIME type</span></span>              | <span data-ttu-id="988ac-112">image/gif</span><span class="sxs-lookup"><span data-stu-id="988ac-112">image/gif</span></span>                             |
| <span data-ttu-id="988ac-113">Compatibilidad con las especificaciones</span><span class="sxs-lookup"><span data-stu-id="988ac-113">Specification Support</span></span>  | <span data-ttu-id="988ac-114">Especificación de GIF 89A/89m</span><span class="sxs-lookup"><span data-stu-id="988ac-114">GIF Specification 89a/89m</span></span>             |



 

<span data-ttu-id="988ac-115">En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes del códec GIF nativo.</span><span class="sxs-lookup"><span data-stu-id="988ac-115">The following table lists the GUIDs used to identify the native GIF codec components.</span></span>



| <span data-ttu-id="988ac-116">Componente</span><span class="sxs-lookup"><span data-stu-id="988ac-116">Component</span></span>        | <span data-ttu-id="988ac-117">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="988ac-117">Friendly Name</span></span>            | <span data-ttu-id="988ac-118">GUID</span><span class="sxs-lookup"><span data-stu-id="988ac-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="988ac-119">Formato de contenedor</span><span class="sxs-lookup"><span data-stu-id="988ac-119">Container Format</span></span> | <span data-ttu-id="988ac-120">GUID \_ ContainerFormatGif</span><span class="sxs-lookup"><span data-stu-id="988ac-120">GUID\_ContainerFormatGif</span></span> | <span data-ttu-id="988ac-121">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span><span class="sxs-lookup"><span data-stu-id="988ac-121">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span></span> |
| <span data-ttu-id="988ac-122">Descodificador</span><span class="sxs-lookup"><span data-stu-id="988ac-122">Decoder</span></span>          | <span data-ttu-id="988ac-123">CLSID \_ WICGifDecoder</span><span class="sxs-lookup"><span data-stu-id="988ac-123">CLSID\_WICGifDecoder</span></span>     | <span data-ttu-id="988ac-124">381dda3c-9ce9-4834-a23e1f98f8fc52be</span><span class="sxs-lookup"><span data-stu-id="988ac-124">381dda3c-9ce9-4834-a23e1f98f8fc52be</span></span> |
| <span data-ttu-id="988ac-125">Codificador</span><span class="sxs-lookup"><span data-stu-id="988ac-125">Encoder</span></span>          | <span data-ttu-id="988ac-126">CLSID \_ WICGifEncoder</span><span class="sxs-lookup"><span data-stu-id="988ac-126">CLSID\_WICGifEncoder</span></span>     | <span data-ttu-id="988ac-127">114f5598-0b22-40a0-86a1c83ea495adbd</span><span class="sxs-lookup"><span data-stu-id="988ac-127">114f5598-0b22-40a0-86a1c83ea495adbd</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="988ac-128">Encoding</span><span class="sxs-lookup"><span data-stu-id="988ac-128">Encoding</span></span>

<span data-ttu-id="988ac-129">La API de codificación WIC está diseñada para ser independiente del códec y la codificación de imágenes para los códecs habilitados para WIC es esencialmente la misma.</span><span class="sxs-lookup"><span data-stu-id="988ac-129">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="988ac-130">Para obtener más información sobre la codificación de imágenes mediante la API de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.</span><span class="sxs-lookup"><span data-stu-id="988ac-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="988ac-131">Opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="988ac-131">Encoder Options</span></span>

<span data-ttu-id="988ac-132">Los códecs habilitados para WIC difieren en el nivel de opción de codificación.</span><span class="sxs-lookup"><span data-stu-id="988ac-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="988ac-133">Las opciones del codificador reflejan las capacidades de un codificador de imágenes y cada códec nativo admite un conjunto de estas opciones de codificador.</span><span class="sxs-lookup"><span data-stu-id="988ac-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="988ac-134">Las opciones del codificador pueden ser opciones básicas de WIC compatibles disponibles para todos los códigos habilitados para WIC (aunque no se admiten necesariamente) o las opciones específicas del códec diseñadas con el códec formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="988ac-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="988ac-135">Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la interfaz [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="988ac-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="988ac-136">Para obtener más información sobre el uso de la interfaz **IPropertyBag2** para la codificación de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.</span><span class="sxs-lookup"><span data-stu-id="988ac-136">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="988ac-137">El codificador GIF no es compatible con las opciones básicas de WIC y no proporciona opciones de codificador personalizadas.</span><span class="sxs-lookup"><span data-stu-id="988ac-137">The GIF encoder does not support any basic WIC options and does not provide custom encoder options.</span></span> <span data-ttu-id="988ac-138">Si una opción de codificador está en la lista de opciones [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) , se omite.</span><span class="sxs-lookup"><span data-stu-id="988ac-138">If an encoder option is in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list, it is ignored.</span></span>

## <a name="decoding"></a><span data-ttu-id="988ac-139">Descodificación</span><span class="sxs-lookup"><span data-stu-id="988ac-139">Decoding</span></span>

<span data-ttu-id="988ac-140">La API de descodificación de WIC está diseñada para ser independiente del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma.</span><span class="sxs-lookup"><span data-stu-id="988ac-140">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="988ac-141">Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="988ac-141">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="988ac-142">Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="988ac-142">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
