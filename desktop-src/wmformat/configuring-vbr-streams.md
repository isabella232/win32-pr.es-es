---
title: Configuración de secuencias VBR
description: Configuración de secuencias VBR
ms.assetid: 83caabb7-b7fa-4b0a-a608-d5a86e4101b8
keywords:
- flujos, configurar secuencias VBR
- secuencias, velocidad de bits variable (VBR)
- velocidad de bits variable (VBR), secuencias
- VBR (velocidad de bits variable), secuencias
- streams, interfaz IWMPropertyVault
- IWMPropertyVault
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6667dc9cf66932cf8af90da0b0e59ad27860ab3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994940"
---
# <a name="configuring-vbr-streams"></a><span data-ttu-id="7809d-109">Configuración de secuencias VBR</span><span class="sxs-lookup"><span data-stu-id="7809d-109">Configuring VBR Streams</span></span>

<span data-ttu-id="7809d-110">Puede usar la codificación de velocidad de bits variable (VBR) para generar secuencias de alta calidad para archivos locales o para descargar y reproducir.</span><span class="sxs-lookup"><span data-stu-id="7809d-110">You can use variable bit rate (VBR) encoding to produce high quality streams for local files or for downloading and playing.</span></span> <span data-ttu-id="7809d-111">Hay tres opciones para VBR: basado en la calidad (un paso), sin restricciones (dos pasos) y restringido (dos pasos).</span><span class="sxs-lookup"><span data-stu-id="7809d-111">There are three options for VBR: quality-based (one-pass), unconstrained (two-pass), and constrained (two-pass).</span></span> <span data-ttu-id="7809d-112">Para obtener más información sobre los tipos de codificación VBR, consulte [codificación de velocidad de bits variable (VBR)](variable-bit-rate--vbr--encoding.md).</span><span class="sxs-lookup"><span data-stu-id="7809d-112">For more information about the types of VBR encoding, see [Variable Bit Rate (VBR) Encoding](variable-bit-rate--vbr--encoding.md).</span></span>

<span data-ttu-id="7809d-113">Para configurar la codificación VBR en un perfil, establezca las propiedades con la interfaz [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) .</span><span class="sxs-lookup"><span data-stu-id="7809d-113">You can configure VBR encoding in a profile by setting properties with the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface.</span></span> <span data-ttu-id="7809d-114">En la tabla siguiente se describen las propiedades que se usan para configurar la codificación VBR.</span><span class="sxs-lookup"><span data-stu-id="7809d-114">The following table describes the properties used to configure VBR encoding.</span></span>



| <span data-ttu-id="7809d-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7809d-115">Property</span></span>                     | <span data-ttu-id="7809d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="7809d-116">Description</span></span>                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7809d-117">**g \_ wszVBREnabled**</span><span class="sxs-lookup"><span data-stu-id="7809d-117">**g\_wszVBREnabled**</span></span>         | <span data-ttu-id="7809d-118">Valor booleano.</span><span class="sxs-lookup"><span data-stu-id="7809d-118">Boolean value.</span></span> <span data-ttu-id="7809d-119">Establézcalo en true para usar la codificación VBR.</span><span class="sxs-lookup"><span data-stu-id="7809d-119">Set to True to use VBR encoding.</span></span>                                                   |
| <span data-ttu-id="7809d-120">**g \_ wszVBRQuality**</span><span class="sxs-lookup"><span data-stu-id="7809d-120">**g\_wszVBRQuality**</span></span>         | <span data-ttu-id="7809d-121">Valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7809d-121">**DWORD** value.</span></span> <span data-ttu-id="7809d-122">Se establece en el nivel de calidad deseado (de 1 a 100) para la codificación VBR basada en la calidad.</span><span class="sxs-lookup"><span data-stu-id="7809d-122">Set to the desired quality level (1 to 100) for quality-based VBR encoding.</span></span>      |
| <span data-ttu-id="7809d-123">**g \_ wszVBRBitrateMax**</span><span class="sxs-lookup"><span data-stu-id="7809d-123">**g\_wszVBRBitrateMax**</span></span>      | <span data-ttu-id="7809d-124">Valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7809d-124">**DWORD** value.</span></span> <span data-ttu-id="7809d-125">Se establece en la velocidad de bits máxima, en bits por segundo, para la codificación VBR restringida.</span><span class="sxs-lookup"><span data-stu-id="7809d-125">Set to the maximum bit rate, in bits per second, for constrained VBR encoding.</span></span>   |
| <span data-ttu-id="7809d-126">**g \_ wszVBRBufferWindowMax**</span><span class="sxs-lookup"><span data-stu-id="7809d-126">**g\_wszVBRBufferWindowMax**</span></span> | <span data-ttu-id="7809d-127">Valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7809d-127">**DWORD** value.</span></span> <span data-ttu-id="7809d-128">Se establece en la ventana del búfer máximo, en milisegundos, para la codificación VBR restringida.</span><span class="sxs-lookup"><span data-stu-id="7809d-128">Set to the maximum buffer window, in milliseconds, for constrained VBR encoding.</span></span> |



 

<span data-ttu-id="7809d-129">En las secciones siguientes se describe cómo usar los distintos tipos de codificación de velocidad de bits variable.</span><span class="sxs-lookup"><span data-stu-id="7809d-129">The following sections describe how to use the different types of variable bit rate encoding.</span></span>



| <span data-ttu-id="7809d-130">Sección</span><span class="sxs-lookup"><span data-stu-id="7809d-130">Section</span></span>                                                              | <span data-ttu-id="7809d-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="7809d-131">Description</span></span>                                                                                                        |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7809d-132">Para configurar Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="7809d-132">To Configure Quality-Based VBR</span></span>](to-configure-quality-based-vbr.md) | <span data-ttu-id="7809d-133">Describe cómo usar la codificación de velocidad de bits variable basada en un nivel de calidad estático.</span><span class="sxs-lookup"><span data-stu-id="7809d-133">Describes how to use variable bit rate encoding based on a static quality level.</span></span>                                   |
| [<span data-ttu-id="7809d-134">Para configurar una VBR sin restricciones</span><span class="sxs-lookup"><span data-stu-id="7809d-134">To Configure Unconstrained VBR</span></span>](to-configure-unconstrained-vbr.md) | <span data-ttu-id="7809d-135">Describe cómo usar la codificación de velocidad de bits variable basada en una velocidad de bits media de destino sin un valor de pico explícito.</span><span class="sxs-lookup"><span data-stu-id="7809d-135">Describes how to use variable bit rate encoding based on a target average bit rate without an explicit peak value.</span></span> |
| [<span data-ttu-id="7809d-136">Para configurar una VBR restringida</span><span class="sxs-lookup"><span data-stu-id="7809d-136">To Configure Constrained VBR</span></span>](to-configure-constrained-vbr.md)     | <span data-ttu-id="7809d-137">Describe cómo usar la codificación de velocidad de bits variable basada en una velocidad de bits media de destino y un valor máximo explícito.</span><span class="sxs-lookup"><span data-stu-id="7809d-137">Describes how to use variable bit rate encoding based on a target average bit rate and an explicit peak value.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="7809d-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7809d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7809d-139">**Configuración de secuencias**</span><span class="sxs-lookup"><span data-stu-id="7809d-139">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




