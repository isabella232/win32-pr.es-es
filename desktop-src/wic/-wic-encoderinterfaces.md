---
description: Interfaces del codificador
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Interfaces del codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5367a25f1a2a4caf486711f7569312a436f8f474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277624"
---
# <a name="encoder-interfaces"></a><span data-ttu-id="b3a62-103">Interfaces del codificador</span><span class="sxs-lookup"><span data-stu-id="b3a62-103">Encoder Interfaces</span></span>


<span data-ttu-id="b3a62-104">En las tablas siguientes se muestran las interfaces implementadas por los codificadores de componentes de imágenes de Windows (WIC) y el diagrama de clases muestra la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="b3a62-104">The following tables show the interfaces implemented by Windows Imaging Component (WIC) encoders, and the class diagram shows the inheritance hierarchy.</span></span>

<span data-ttu-id="b3a62-105">Interfaces del codificador Container-Level</span><span class="sxs-lookup"><span data-stu-id="b3a62-105">Container-Level Encoder Interfaces</span></span>



| <span data-ttu-id="b3a62-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="b3a62-106">Interface</span></span>                                                                                       | <span data-ttu-id="b3a62-107">Responsabilidades</span><span class="sxs-lookup"><span data-stu-id="b3a62-107">Responsibilities</span></span>                             | <span data-ttu-id="b3a62-108">Implementación</span><span class="sxs-lookup"><span data-stu-id="b3a62-108">Implementation</span></span>                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="b3a62-109">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="b3a62-109">IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)                                             | <span data-ttu-id="b3a62-110">Servicios de nivel de contenedor</span><span class="sxs-lookup"><span data-stu-id="b3a62-110">Container-level services</span></span>                     | <span data-ttu-id="b3a62-111">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b3a62-111">Required</span></span>                                                                   |
| [<span data-ttu-id="b3a62-112">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="b3a62-112">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | <span data-ttu-id="b3a62-113">Compatibilidad con la cancelación de notificación de progreso &</span><span class="sxs-lookup"><span data-stu-id="b3a62-113">Progress notification & cancellation support</span></span> | <span data-ttu-id="b3a62-114">Recomendado</span><span class="sxs-lookup"><span data-stu-id="b3a62-114">Recommended</span></span>                                                                |
| [<span data-ttu-id="b3a62-115">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="b3a62-115">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)                                 | <span data-ttu-id="b3a62-116">Servicios de serialización de metadatos</span><span class="sxs-lookup"><span data-stu-id="b3a62-116">Metadata serialization services</span></span>              | <span data-ttu-id="b3a62-117">Opcional (solo es necesario para los formatos que admiten metadatos de nivel de contenedor)</span><span class="sxs-lookup"><span data-stu-id="b3a62-117">Optional (Required only for formats that support container-level metadata)</span></span> |



 

<span data-ttu-id="b3a62-118">Interfaces del codificador Frame-Level</span><span class="sxs-lookup"><span data-stu-id="b3a62-118">Frame-Level Encoder Interfaces</span></span>



| <span data-ttu-id="b3a62-119">Interfaz</span><span class="sxs-lookup"><span data-stu-id="b3a62-119">Interface</span></span>                                                       | <span data-ttu-id="b3a62-120">Responsabilidades</span><span class="sxs-lookup"><span data-stu-id="b3a62-120">Responsibilities</span></span>                | <span data-ttu-id="b3a62-121">Implementación</span><span class="sxs-lookup"><span data-stu-id="b3a62-121">Implementation</span></span> |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [<span data-ttu-id="b3a62-122">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="b3a62-122">IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)     | <span data-ttu-id="b3a62-123">Servicios de nivel de marco</span><span class="sxs-lookup"><span data-stu-id="b3a62-123">Frame-level services</span></span>            | <span data-ttu-id="b3a62-124">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b3a62-124">Required</span></span>       |
| [<span data-ttu-id="b3a62-125">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="b3a62-125">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md) | <span data-ttu-id="b3a62-126">Servicios de serialización de metadatos</span><span class="sxs-lookup"><span data-stu-id="b3a62-126">Metadata serialization services</span></span> | <span data-ttu-id="b3a62-127">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b3a62-127">Required</span></span>       |



 

![jerarquía de herencia de la interfaz del codificador WIC](graphics/wicencoderinterfaces.png)

<span data-ttu-id="b3a62-129">Observará que las interfaces del codificador son prácticamente imágenes reflejadas de las interfaces del descodificador y que la mayoría de los métodos de estas interfaces se corresponden con los métodos de las interfaces del descodificador relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b3a62-129">You'll notice that the encoder interfaces are almost mirror images of the decoder interfaces, and that most of the methods on these interfaces correspond to methods on the related decoder interfaces.</span></span> <span data-ttu-id="b3a62-130">Ahora que está familiarizado con la implementación de un descodificador habilitado para WIC, la implementación de un codificador habilitado para WIC también resultará familiar.</span><span class="sxs-lookup"><span data-stu-id="b3a62-130">Now that you're familiar with the implementation of a WIC-enabled decoder, the implementation of a WIC-enabled encoder will seem familiar as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3a62-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b3a62-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b3a62-132">**Vista**</span><span class="sxs-lookup"><span data-stu-id="b3a62-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b3a62-133">Implementación de un codificador WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="b3a62-133">Implementing a WIC-Enabled Encoder</span></span>](-wic-implementingwicencoder.md)
</dt> <dt>

[<span data-ttu-id="b3a62-134">Implementación de IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="b3a62-134">Implementing IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[<span data-ttu-id="b3a62-135">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="b3a62-135">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="b3a62-136">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="b3a62-136">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



