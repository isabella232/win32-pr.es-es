---
description: Interfaces del descodificador
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Interfaces del descodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef90ca2dd521c15460295505a6d5b7ea451c4dba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278843"
---
# <a name="decoder-interfaces"></a><span data-ttu-id="0913b-103">Interfaces del descodificador</span><span class="sxs-lookup"><span data-stu-id="0913b-103">Decoder Interfaces</span></span>

<span data-ttu-id="0913b-104">En las tablas siguientes se muestran las interfaces implementadas por descodificadores de componentes de Windows Imaging (WIC) y el diagrama de clases muestra la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="0913b-104">The following tables show the interfaces implemented by Windows Imaging Component (WIC) decoders, and the class diagram shows the inheritance hierarchy.</span></span>

<span data-ttu-id="0913b-105">Container-Level interfaces del descodificador</span><span class="sxs-lookup"><span data-stu-id="0913b-105">Container-Level Decoder Interfaces</span></span>



| <span data-ttu-id="0913b-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="0913b-106">Interface</span></span>                                                                                       | <span data-ttu-id="0913b-107">Responsabilidades</span><span class="sxs-lookup"><span data-stu-id="0913b-107">Responsibilities</span></span>                             | <span data-ttu-id="0913b-108">Implementación</span><span class="sxs-lookup"><span data-stu-id="0913b-108">Implementation</span></span>                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="0913b-109">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="0913b-109">IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)                                             | <span data-ttu-id="0913b-110">Servicios de nivel de contenedor</span><span class="sxs-lookup"><span data-stu-id="0913b-110">Container-level services</span></span>                     | <span data-ttu-id="0913b-111">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="0913b-111">Required</span></span>                                                                   |
| [<span data-ttu-id="0913b-112">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="0913b-112">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | <span data-ttu-id="0913b-113">Compatibilidad con la cancelación de notificación de progreso &</span><span class="sxs-lookup"><span data-stu-id="0913b-113">Progress notification & cancellation support</span></span> | <span data-ttu-id="0913b-114">Recomendado</span><span class="sxs-lookup"><span data-stu-id="0913b-114">Recommended</span></span>                                                                |
| [<span data-ttu-id="0913b-115">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="0913b-115">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)                                 | <span data-ttu-id="0913b-116">Enumeración de metadatos</span><span class="sxs-lookup"><span data-stu-id="0913b-116">Metadata enumeration</span></span>                         | <span data-ttu-id="0913b-117">Opcional (solo es necesario para los formatos que admiten metadatos de nivel de contenedor)</span><span class="sxs-lookup"><span data-stu-id="0913b-117">Optional (Required only for formats that support container-level metadata)</span></span> |



 

<span data-ttu-id="0913b-118">Frame-Level interfaces del descodificador</span><span class="sxs-lookup"><span data-stu-id="0913b-118">Frame-Level Decoder Interfaces</span></span>



| <span data-ttu-id="0913b-119">Interfaz</span><span class="sxs-lookup"><span data-stu-id="0913b-119">Interface</span></span>                                                           | <span data-ttu-id="0913b-120">Responsabilidades</span><span class="sxs-lookup"><span data-stu-id="0913b-120">Responsibilities</span></span>          | <span data-ttu-id="0913b-121">Implementación</span><span class="sxs-lookup"><span data-stu-id="0913b-121">Implementation</span></span>                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [<span data-ttu-id="0913b-122">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="0913b-122">IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)         | <span data-ttu-id="0913b-123">Servicios de nivel de marco</span><span class="sxs-lookup"><span data-stu-id="0913b-123">Frame-level services</span></span>      | <span data-ttu-id="0913b-124">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="0913b-124">Required</span></span>                      |
| [<span data-ttu-id="0913b-125">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="0913b-125">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)     | <span data-ttu-id="0913b-126">Enumeración de metadatos</span><span class="sxs-lookup"><span data-stu-id="0913b-126">Metadata enumeration</span></span>      | <span data-ttu-id="0913b-127">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="0913b-127">Required</span></span>                      |
| [<span data-ttu-id="0913b-128">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="0913b-128">IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md) | <span data-ttu-id="0913b-129">Transformaciones nativas del descodificador</span><span class="sxs-lookup"><span data-stu-id="0913b-129">Native decoder transforms</span></span> | <span data-ttu-id="0913b-130">Recomendado</span><span class="sxs-lookup"><span data-stu-id="0913b-130">Recommended</span></span>                   |
| [<span data-ttu-id="0913b-131">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="0913b-131">IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)                       | <span data-ttu-id="0913b-132">Servicios de procesamiento sin procesar</span><span class="sxs-lookup"><span data-stu-id="0913b-132">Raw processing services</span></span>   | <span data-ttu-id="0913b-133">Necesario solo para formatos RAW</span><span class="sxs-lookup"><span data-stu-id="0913b-133">Required for Raw formats only</span></span> |



 

![jerarquía de herencia de la interfaz WIC](graphics/wicinterfaces.png)

## <a name="related-topics"></a><span data-ttu-id="0913b-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0913b-135">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0913b-136">**Vista**</span><span class="sxs-lookup"><span data-stu-id="0913b-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0913b-137">Implementar un descodificador de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="0913b-137">Implementing a WIC-Enabled Decoder</span></span>](-wic-implementingwicdecoder.md)
</dt> <dt>

[<span data-ttu-id="0913b-138">Implementar IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="0913b-138">Implementing IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[<span data-ttu-id="0913b-139">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="0913b-139">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="0913b-140">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="0913b-140">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



