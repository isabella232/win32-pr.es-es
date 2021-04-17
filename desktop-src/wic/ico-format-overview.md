---
description: En este tema se proporciona información sobre el códec ICO nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Información general sobre el formato ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d370497e9231d6deb8d1793a26a53565b5cd99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707133"
---
# <a name="ico-format-overview"></a><span data-ttu-id="3c0cb-103">Información general sobre el formato ICO</span><span class="sxs-lookup"><span data-stu-id="3c0cb-103">ICO Format Overview</span></span>

<span data-ttu-id="3c0cb-104">En este tema se proporciona información sobre el códec ICO nativo disponible a través de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="3c0cb-104">This topic provides information about the native ICO codec available through Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="3c0cb-105">Identidad del códec</span><span class="sxs-lookup"><span data-stu-id="3c0cb-105">Codec Identity</span></span>

<span data-ttu-id="3c0cb-106">En la tabla siguiente se proporciona información de identificación del códec.</span><span class="sxs-lookup"><span data-stu-id="3c0cb-106">The following table provides codec identification information.</span></span>



|                        |                   |
|------------------------|-------------------|
| <span data-ttu-id="3c0cb-107">Nombres formales</span><span class="sxs-lookup"><span data-stu-id="3c0cb-107">Formal Name(s)</span></span>         | <span data-ttu-id="3c0cb-108">Formato de icono (ICO)</span><span class="sxs-lookup"><span data-stu-id="3c0cb-108">Icon Format (ICO)</span></span> |
| <span data-ttu-id="3c0cb-109">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="3c0cb-109">File Name Extension(s)</span></span> | <span data-ttu-id="3c0cb-110">ICO</span><span class="sxs-lookup"><span data-stu-id="3c0cb-110">ico</span></span>               |
| <span data-ttu-id="3c0cb-111">Tipo de MIME</span><span class="sxs-lookup"><span data-stu-id="3c0cb-111">MIME type</span></span>              | <span data-ttu-id="3c0cb-112">imagen/ICO</span><span class="sxs-lookup"><span data-stu-id="3c0cb-112">image/ico</span></span>         |
| <span data-ttu-id="3c0cb-113">Compatibilidad con las especificaciones</span><span class="sxs-lookup"><span data-stu-id="3c0cb-113">Specification Support</span></span>  |                   |



 

<span data-ttu-id="3c0cb-114">En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes del códec ICO nativo.</span><span class="sxs-lookup"><span data-stu-id="3c0cb-114">The following table lists the GUIDs used to identify the native ICO codec components.</span></span>



| <span data-ttu-id="3c0cb-115">Componente</span><span class="sxs-lookup"><span data-stu-id="3c0cb-115">Component</span></span>        | <span data-ttu-id="3c0cb-116">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="3c0cb-116">Friendly Name</span></span>            | <span data-ttu-id="3c0cb-117">GUID</span><span class="sxs-lookup"><span data-stu-id="3c0cb-117">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="3c0cb-118">Formato de contenedor</span><span class="sxs-lookup"><span data-stu-id="3c0cb-118">Container Format</span></span> | <span data-ttu-id="3c0cb-119">GUID \_ ContainerFormatIco</span><span class="sxs-lookup"><span data-stu-id="3c0cb-119">GUID\_ContainerFormatIco</span></span> | <span data-ttu-id="3c0cb-120">a3a860c4-338f-4c17-919afba4b5628f21</span><span class="sxs-lookup"><span data-stu-id="3c0cb-120">a3a860c4-338f-4c17-919afba4b5628f21</span></span> |
| <span data-ttu-id="3c0cb-121">Descodificador</span><span class="sxs-lookup"><span data-stu-id="3c0cb-121">Decoder</span></span>          | <span data-ttu-id="3c0cb-122">CLSID \_ WICIcoDecoder</span><span class="sxs-lookup"><span data-stu-id="3c0cb-122">CLSID\_WICIcoDecoder</span></span>     | <span data-ttu-id="3c0cb-123">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span><span class="sxs-lookup"><span data-stu-id="3c0cb-123">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span></span> |
| <span data-ttu-id="3c0cb-124">Codificador</span><span class="sxs-lookup"><span data-stu-id="3c0cb-124">Encoder</span></span>          | <span data-ttu-id="3c0cb-125">NO DISPONIBLE</span><span class="sxs-lookup"><span data-stu-id="3c0cb-125">NOT AVAILABLE</span></span>            | <span data-ttu-id="3c0cb-126">NO DISPONIBLE</span><span class="sxs-lookup"><span data-stu-id="3c0cb-126">NOT AVAILABLE</span></span>                       |



 

## <a name="encoding"></a><span data-ttu-id="3c0cb-127">Encoding</span><span class="sxs-lookup"><span data-stu-id="3c0cb-127">Encoding</span></span>

<span data-ttu-id="3c0cb-128">WIC no proporciona un codificador de imágenes ICO nativo.</span><span class="sxs-lookup"><span data-stu-id="3c0cb-128">WIC does not provide a native ICO image encoder.</span></span>

## <a name="decoding"></a><span data-ttu-id="3c0cb-129">Descodificación</span><span class="sxs-lookup"><span data-stu-id="3c0cb-129">Decoding</span></span>

<span data-ttu-id="3c0cb-130">La API de descodificación de WIC está diseñada para ser independiente del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma.</span><span class="sxs-lookup"><span data-stu-id="3c0cb-130">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="3c0cb-131">Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="3c0cb-131">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="3c0cb-132">Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="3c0cb-132">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 



