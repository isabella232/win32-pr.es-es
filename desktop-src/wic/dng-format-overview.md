---
description: En este tema se proporciona información sobre el códec DNG nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Información general sobre el formato DNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f766356f7c13d7b2bb25adab5411ae55c2735f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360762"
---
# <a name="dng-format-overview"></a><span data-ttu-id="72db7-103">Información general sobre el formato DNG</span><span class="sxs-lookup"><span data-stu-id="72db7-103">DNG Format Overview</span></span>

<span data-ttu-id="72db7-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="72db7-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="72db7-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="72db7-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="72db7-106">En este tema se proporciona información sobre el códec DNG nativo disponible a través de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="72db7-106">This topic provides information about the native DNG codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="72db7-107">Identidad del códec</span><span class="sxs-lookup"><span data-stu-id="72db7-107">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="72db7-108">Descodificación</span><span class="sxs-lookup"><span data-stu-id="72db7-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="72db7-109">Identidad del códec</span><span class="sxs-lookup"><span data-stu-id="72db7-109">Codec Identity</span></span>

<span data-ttu-id="72db7-110">En la tabla siguiente se proporciona información de identificación del códec.</span><span class="sxs-lookup"><span data-stu-id="72db7-110">The following table provides codec identification information.</span></span>



|                        |                                                      |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="72db7-111">Nombres formales</span><span class="sxs-lookup"><span data-stu-id="72db7-111">Formal Name(s)</span></span>         | <span data-ttu-id="72db7-112">Negativo digital (DNG)</span><span class="sxs-lookup"><span data-stu-id="72db7-112">Digital Negative (DNG)</span></span>                               |
| <span data-ttu-id="72db7-113">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="72db7-113">File Name Extension(s)</span></span> | <span data-ttu-id="72db7-114">.dng</span><span class="sxs-lookup"><span data-stu-id="72db7-114">.dng</span></span>                                                 |
| <span data-ttu-id="72db7-115">Tipos MIME</span><span class="sxs-lookup"><span data-stu-id="72db7-115">MIME type(s)</span></span>           | <span data-ttu-id="72db7-116">imagen/DNG</span><span class="sxs-lookup"><span data-stu-id="72db7-116">image/DNG</span></span>                                            |
| <span data-ttu-id="72db7-117">Compatibilidad con las especificaciones</span><span class="sxs-lookup"><span data-stu-id="72db7-117">Specification Support</span></span>  | <span data-ttu-id="72db7-118">Versión de especificación negativa digital (DNG) 1.4.0.0</span><span class="sxs-lookup"><span data-stu-id="72db7-118">Digital Negative (DNG) Specification Version 1.4.0.0</span></span> |



 

<span data-ttu-id="72db7-119">En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes del códec DNG nativo.</span><span class="sxs-lookup"><span data-stu-id="72db7-119">The following table lists the GUIDs used to identify the native DNG codec components.</span></span>



| <span data-ttu-id="72db7-120">Componente</span><span class="sxs-lookup"><span data-stu-id="72db7-120">Component</span></span>        | <span data-ttu-id="72db7-121">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="72db7-121">Friendly Name</span></span>             | <span data-ttu-id="72db7-122">GUID</span><span class="sxs-lookup"><span data-stu-id="72db7-122">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="72db7-123">Formato de contenedor</span><span class="sxs-lookup"><span data-stu-id="72db7-123">Container Format</span></span> | <span data-ttu-id="72db7-124">GUID \_ ContainerFormatAdng</span><span class="sxs-lookup"><span data-stu-id="72db7-124">GUID\_ContainerFormatAdng</span></span> | <span data-ttu-id="72db7-125">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span><span class="sxs-lookup"><span data-stu-id="72db7-125">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span></span> |
| <span data-ttu-id="72db7-126">Descodificador</span><span class="sxs-lookup"><span data-stu-id="72db7-126">Decoder</span></span>          | <span data-ttu-id="72db7-127">CLSID \_ WICAdngDecoder</span><span class="sxs-lookup"><span data-stu-id="72db7-127">CLSID\_WICAdngDecoder</span></span>     | <span data-ttu-id="72db7-128">981d9411-909e-42a7-8f5da747ff052edb</span><span class="sxs-lookup"><span data-stu-id="72db7-128">981d9411-909e-42a7-8f5da747ff052edb</span></span> |



 

## <a name="decoding"></a><span data-ttu-id="72db7-129">Descodificación</span><span class="sxs-lookup"><span data-stu-id="72db7-129">Decoding</span></span>

<span data-ttu-id="72db7-130">La API de descodificación de WIC está diseñada para ser independiente del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma.</span><span class="sxs-lookup"><span data-stu-id="72db7-130">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="72db7-131">Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="72db7-131">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="72db7-132">Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="72db7-132">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="72db7-133">El descodificador no admite la descodificación de datos de sensor sin procesar y solo admite archivos con una representación de imagen sin formato insertada en una IFD con NewSubFileType igual a 1.</span><span class="sxs-lookup"><span data-stu-id="72db7-133">The decoder does not support decoding raw sensor data and only supports files with a non-raw image representation embedded in an IFD with NewSubFileType equal to 1.</span></span>

 

 



