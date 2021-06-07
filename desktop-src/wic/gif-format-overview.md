---
description: En este tema se proporciona información sobre el códec GIF nativo disponible a través Windows Imaging Component (WIC).
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Introducción al formato GIF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf7e9924c921b7944de114f5fe667cb2aa33cae
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444456"
---
# <a name="gif-format-overview"></a><span data-ttu-id="d1008-103">Introducción al formato GIF</span><span class="sxs-lookup"><span data-stu-id="d1008-103">GIF Format Overview</span></span>

<span data-ttu-id="d1008-104">En este tema se proporciona información sobre el códec GIF nativo disponible a través Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="d1008-104">This topic provides information about the native GIF codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="d1008-105">Identidad de códec</span><span class="sxs-lookup"><span data-stu-id="d1008-105">Codec Identity</span></span>

<span data-ttu-id="d1008-106">En la tabla siguiente se proporciona información de identificación de códecs.</span><span class="sxs-lookup"><span data-stu-id="d1008-106">The following table provides codec identification information.</span></span>



|  <span data-ttu-id="d1008-107">Componente</span><span class="sxs-lookup"><span data-stu-id="d1008-107">Component</span></span>             | <span data-ttu-id="d1008-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1008-108">Description</span></span>                           |
|------------------------|---------------------------------------|
| <span data-ttu-id="d1008-109">Nombres formales</span><span class="sxs-lookup"><span data-stu-id="d1008-109">Formal Name(s)</span></span>         | <span data-ttu-id="d1008-110">Formato de intercambio de gráficos 89a (GIF)</span><span class="sxs-lookup"><span data-stu-id="d1008-110">Graphics Interchange Format 89a (GIF)</span></span> |
| <span data-ttu-id="d1008-111">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="d1008-111">File Name Extension(s)</span></span> | <span data-ttu-id="d1008-112">GIF</span><span class="sxs-lookup"><span data-stu-id="d1008-112">gif</span></span>                                   |
| <span data-ttu-id="d1008-113">Tipo de MIME</span><span class="sxs-lookup"><span data-stu-id="d1008-113">MIME type</span></span>              | <span data-ttu-id="d1008-114">image/gif</span><span class="sxs-lookup"><span data-stu-id="d1008-114">image/gif</span></span>                             |
| <span data-ttu-id="d1008-115">Compatibilidad con especificaciones</span><span class="sxs-lookup"><span data-stu-id="d1008-115">Specification Support</span></span>  | <span data-ttu-id="d1008-116">Especificación GIF 89a/89 m</span><span class="sxs-lookup"><span data-stu-id="d1008-116">GIF Specification 89a/89m</span></span>             |



 

<span data-ttu-id="d1008-117">En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes de códec GIF nativos.</span><span class="sxs-lookup"><span data-stu-id="d1008-117">The following table lists the GUIDs used to identify the native GIF codec components.</span></span>



| <span data-ttu-id="d1008-118">Componente</span><span class="sxs-lookup"><span data-stu-id="d1008-118">Component</span></span>        | <span data-ttu-id="d1008-119">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="d1008-119">Friendly Name</span></span>            | <span data-ttu-id="d1008-120">GUID</span><span class="sxs-lookup"><span data-stu-id="d1008-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="d1008-121">Formato de contenedor</span><span class="sxs-lookup"><span data-stu-id="d1008-121">Container Format</span></span> | <span data-ttu-id="d1008-122">GUID \_ ContainerFormatGif</span><span class="sxs-lookup"><span data-stu-id="d1008-122">GUID\_ContainerFormatGif</span></span> | <span data-ttu-id="d1008-123">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span><span class="sxs-lookup"><span data-stu-id="d1008-123">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span></span> |
| <span data-ttu-id="d1008-124">Descodificador</span><span class="sxs-lookup"><span data-stu-id="d1008-124">Decoder</span></span>          | <span data-ttu-id="d1008-125">CLSID \_ WICGifDecoder</span><span class="sxs-lookup"><span data-stu-id="d1008-125">CLSID\_WICGifDecoder</span></span>     | <span data-ttu-id="d1008-126">381dda3c-9ce9-4834-a23e1f98f8fc52be</span><span class="sxs-lookup"><span data-stu-id="d1008-126">381dda3c-9ce9-4834-a23e1f98f8fc52be</span></span> |
| <span data-ttu-id="d1008-127">Codificador</span><span class="sxs-lookup"><span data-stu-id="d1008-127">Encoder</span></span>          | <span data-ttu-id="d1008-128">CLSID \_ WICGifEncoder</span><span class="sxs-lookup"><span data-stu-id="d1008-128">CLSID\_WICGifEncoder</span></span>     | <span data-ttu-id="d1008-129">114f5598-0b22-40a0-86a1c83ea495adbd</span><span class="sxs-lookup"><span data-stu-id="d1008-129">114f5598-0b22-40a0-86a1c83ea495adbd</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="d1008-130">Encoding</span><span class="sxs-lookup"><span data-stu-id="d1008-130">Encoding</span></span>

<span data-ttu-id="d1008-131">La API de codificación WIC está diseñada para ser independiente del códec y la codificación de imágenes para códecs habilitados para WIC es básicamente la misma.</span><span class="sxs-lookup"><span data-stu-id="d1008-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="d1008-132">Para obtener más información sobre la codificación de imágenes mediante la API de WIC, vea Información general [sobre la codificación.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="d1008-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="d1008-133">Opciones del codificador</span><span class="sxs-lookup"><span data-stu-id="d1008-133">Encoder Options</span></span>

<span data-ttu-id="d1008-134">Los códecs habilitados para WIC difieren en el nivel de opción de codificación.</span><span class="sxs-lookup"><span data-stu-id="d1008-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="d1008-135">Las opciones del codificador reflejan las funcionalidades de un codificador de imágenes y cada códec nativo admite un conjunto de estas opciones de codificador.</span><span class="sxs-lookup"><span data-stu-id="d1008-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="d1008-136">Las opciones de codificador pueden ser opciones básicas compatibles con WIC disponibles para todos los códigos habilitados para WIC (aunque no necesariamente admitidos) o opciones específicas del códec diseñadas por el códec de formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="d1008-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="d1008-137">Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la [**interfaz IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d1008-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="d1008-138">Para obtener más información sobre el uso de la **interfaz IPropertyBag2** para la codificación WIC , vea Información general [sobre la codificación.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="d1008-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="d1008-139">El codificador GIF no admite ninguna opción básica de WIC y no proporciona opciones de codificador personalizadas.</span><span class="sxs-lookup"><span data-stu-id="d1008-139">The GIF encoder does not support any basic WIC options and does not provide custom encoder options.</span></span> <span data-ttu-id="d1008-140">Si una opción de codificador está en la [**lista de opciones IPropertyBag2,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) se omite.</span><span class="sxs-lookup"><span data-stu-id="d1008-140">If an encoder option is in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list, it is ignored.</span></span>

## <a name="decoding"></a><span data-ttu-id="d1008-141">Descodificación</span><span class="sxs-lookup"><span data-stu-id="d1008-141">Decoding</span></span>

<span data-ttu-id="d1008-142">La API decoding de WIC está diseñada para ser independiente del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma.</span><span class="sxs-lookup"><span data-stu-id="d1008-142">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="d1008-143">Para obtener más información sobre lacoding de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="d1008-143">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="d1008-144">Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="d1008-144">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
