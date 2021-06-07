---
description: En este tema se proporciona información sobre el códec DNG nativo disponible a través Windows Imaging Component (WIC).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Información general sobre el formato DNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0815d6a24bb8e57e6c64b90f9e9068765838e148
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444936"
---
# <a name="dng-format-overview"></a><span data-ttu-id="524ef-103">Información general sobre el formato DNG</span><span class="sxs-lookup"><span data-stu-id="524ef-103">DNG Format Overview</span></span>

<span data-ttu-id="524ef-104">\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="524ef-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="524ef-105">Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]</span><span class="sxs-lookup"><span data-stu-id="524ef-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="524ef-106">En este tema se proporciona información sobre el códec DNG nativo disponible a través Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="524ef-106">This topic provides information about the native DNG codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="524ef-107">Identidad de códec</span><span class="sxs-lookup"><span data-stu-id="524ef-107">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="524ef-108">Descodificación</span><span class="sxs-lookup"><span data-stu-id="524ef-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="524ef-109">Identidad de códec</span><span class="sxs-lookup"><span data-stu-id="524ef-109">Codec Identity</span></span>

<span data-ttu-id="524ef-110">En la tabla siguiente se proporciona información de identificación de códecs.</span><span class="sxs-lookup"><span data-stu-id="524ef-110">The following table provides codec identification information.</span></span>



|     <span data-ttu-id="524ef-111">Componente</span><span class="sxs-lookup"><span data-stu-id="524ef-111">Component</span></span>          |  <span data-ttu-id="524ef-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="524ef-112">Description</span></span>                                         |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="524ef-113">Nombres formales</span><span class="sxs-lookup"><span data-stu-id="524ef-113">Formal Name(s)</span></span>         | <span data-ttu-id="524ef-114">Negativo digital (DNG)</span><span class="sxs-lookup"><span data-stu-id="524ef-114">Digital Negative (DNG)</span></span>                               |
| <span data-ttu-id="524ef-115">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="524ef-115">File Name Extension(s)</span></span> | <span data-ttu-id="524ef-116">.dng</span><span class="sxs-lookup"><span data-stu-id="524ef-116">.dng</span></span>                                                 |
| <span data-ttu-id="524ef-117">Tipos MIME</span><span class="sxs-lookup"><span data-stu-id="524ef-117">MIME type(s)</span></span>           | <span data-ttu-id="524ef-118">image/DNG</span><span class="sxs-lookup"><span data-stu-id="524ef-118">image/DNG</span></span>                                            |
| <span data-ttu-id="524ef-119">Compatibilidad con especificaciones</span><span class="sxs-lookup"><span data-stu-id="524ef-119">Specification Support</span></span>  | <span data-ttu-id="524ef-120">Especificación negativa digital (DNG) versión 1.4.0.0</span><span class="sxs-lookup"><span data-stu-id="524ef-120">Digital Negative (DNG) Specification Version 1.4.0.0</span></span> |



 

<span data-ttu-id="524ef-121">En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes de códec DNG nativos.</span><span class="sxs-lookup"><span data-stu-id="524ef-121">The following table lists the GUIDs used to identify the native DNG codec components.</span></span>



| <span data-ttu-id="524ef-122">Componente</span><span class="sxs-lookup"><span data-stu-id="524ef-122">Component</span></span>        | <span data-ttu-id="524ef-123">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="524ef-123">Friendly Name</span></span>             | <span data-ttu-id="524ef-124">GUID</span><span class="sxs-lookup"><span data-stu-id="524ef-124">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="524ef-125">Formato de contenedor</span><span class="sxs-lookup"><span data-stu-id="524ef-125">Container Format</span></span> | <span data-ttu-id="524ef-126">GUID \_ ContainerFormatAdng</span><span class="sxs-lookup"><span data-stu-id="524ef-126">GUID\_ContainerFormatAdng</span></span> | <span data-ttu-id="524ef-127">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span><span class="sxs-lookup"><span data-stu-id="524ef-127">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span></span> |
| <span data-ttu-id="524ef-128">Descodificador</span><span class="sxs-lookup"><span data-stu-id="524ef-128">Decoder</span></span>          | <span data-ttu-id="524ef-129">CLSID \_ WICAdngDecoder</span><span class="sxs-lookup"><span data-stu-id="524ef-129">CLSID\_WICAdngDecoder</span></span>     | <span data-ttu-id="524ef-130">981d9411-909e-42a7-8f5da747ff052edb</span><span class="sxs-lookup"><span data-stu-id="524ef-130">981d9411-909e-42a7-8f5da747ff052edb</span></span> |



 

## <a name="decoding"></a><span data-ttu-id="524ef-131">Descodificación</span><span class="sxs-lookup"><span data-stu-id="524ef-131">Decoding</span></span>

<span data-ttu-id="524ef-132">La API de decoding de WIC está diseñada para ser independiente del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma.</span><span class="sxs-lookup"><span data-stu-id="524ef-132">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="524ef-133">Para obtener más información sobre lacodación de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="524ef-133">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="524ef-134">Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="524ef-134">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="524ef-135">El descodificador no admite la descodificación de datos sin procesar del sensor y solo admite archivos con una representación de imagen sin procesar incrustada en un IFD con NewSubFileType igual a 1.</span><span class="sxs-lookup"><span data-stu-id="524ef-135">The decoder does not support decoding raw sensor data and only supports files with a non-raw image representation embedded in an IFD with NewSubFileType equal to 1.</span></span>

 

 



