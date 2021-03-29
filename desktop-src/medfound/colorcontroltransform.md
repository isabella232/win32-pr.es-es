---
description: Ajusta las características de color de una secuencia de vídeo.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: Transformación de control de color DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b94c8314bfd2be85a3bbc392bfa0e83767ff0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808161"
---
# <a name="color-control-transform-dsp"></a><span data-ttu-id="a15ae-103">DSP de transformación de control de color</span><span class="sxs-lookup"><span data-stu-id="a15ae-103">Color Control Transform DSP</span></span>

<span data-ttu-id="a15ae-104">Ajusta las características de color de una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a15ae-104">Adjusts the color characteristics of a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="a15ae-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="a15ae-105">CLSID</span></span>

<span data-ttu-id="a15ae-106">CLSID \_ CColorControlDmo</span><span class="sxs-lookup"><span data-stu-id="a15ae-106">CLSID\_CColorControlDmo</span></span>

## <a name="interfaces"></a><span data-ttu-id="a15ae-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a15ae-107">Interfaces</span></span>

-   <span data-ttu-id="a15ae-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="a15ae-108">**IMediaObject**</span></span>
-   <span data-ttu-id="a15ae-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="a15ae-109">**IMFTransform**</span></span>
-   <span data-ttu-id="a15ae-110">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="a15ae-110">**IPropertyStore**</span></span>

## <a name="formats"></a><span data-ttu-id="a15ae-111">Formatos</span><span class="sxs-lookup"><span data-stu-id="a15ae-111">Formats</span></span>

-   <span data-ttu-id="a15ae-112">RGB 24</span><span class="sxs-lookup"><span data-stu-id="a15ae-112">RGB 24</span></span>
-   <span data-ttu-id="a15ae-113">RGB 32</span><span class="sxs-lookup"><span data-stu-id="a15ae-113">RGB 32</span></span>
-   <span data-ttu-id="a15ae-114">RGB 555</span><span class="sxs-lookup"><span data-stu-id="a15ae-114">RGB 555</span></span>
-   <span data-ttu-id="a15ae-115">RGB 565</span><span class="sxs-lookup"><span data-stu-id="a15ae-115">RGB 565</span></span>
-   <span data-ttu-id="a15ae-116">AYUV</span><span class="sxs-lookup"><span data-stu-id="a15ae-116">AYUV</span></span>
-   <span data-ttu-id="a15ae-117">UYVY</span><span class="sxs-lookup"><span data-stu-id="a15ae-117">UYVY</span></span>
-   <span data-ttu-id="a15ae-118">YUY2</span><span class="sxs-lookup"><span data-stu-id="a15ae-118">YUY2</span></span>
-   <span data-ttu-id="a15ae-119">YV12</span><span class="sxs-lookup"><span data-stu-id="a15ae-119">YV12</span></span>

## <a name="properties"></a><span data-ttu-id="a15ae-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a15ae-120">Properties</span></span>

-   [<span data-ttu-id="a15ae-121">\_brillo del color de MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="a15ae-121">MFPKEY\_COLOR\_BRIGHTNESS</span></span>](mfpkey-color-brightness.md)
-   [<span data-ttu-id="a15ae-122">\_contraste de color de MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="a15ae-122">MFPKEY\_COLOR\_CONTRAST</span></span>](mfpkey-color-contrast.md)
-   [<span data-ttu-id="a15ae-123">\_matiz de color MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="a15ae-123">MFPKEY\_COLOR\_HUE</span></span>](mfpkey-color-hue.md)
-   [<span data-ttu-id="a15ae-124">\_saturación de color de MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="a15ae-124">MFPKEY\_COLOR\_SATURATION</span></span>](mfpkey-color-saturation.md)

## <a name="remarks"></a><span data-ttu-id="a15ae-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a15ae-125">Remarks</span></span>

<span data-ttu-id="a15ae-126">Este DSP modifica el contenido de la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a15ae-126">This DSP modifies the contents of the video stream.</span></span> <span data-ttu-id="a15ae-127">Para la reproducción, es posible que pueda conseguir efectos similares de forma más eficaz mediante la interfaz **IMFVideoProcessor** , que controla el procesamiento de vídeo en la tarjeta gráfica.</span><span class="sxs-lookup"><span data-stu-id="a15ae-127">For playback, you might be able to achieve similar effects more efficiently by using the **IMFVideoProcessor** interface, which controls video processing in the graphics card.</span></span>

## <a name="requirements"></a><span data-ttu-id="a15ae-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a15ae-128">Requirements</span></span>



| <span data-ttu-id="a15ae-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a15ae-129">Requirement</span></span> | <span data-ttu-id="a15ae-130">Value</span><span class="sxs-lookup"><span data-stu-id="a15ae-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a15ae-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a15ae-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a15ae-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a15ae-132">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a15ae-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a15ae-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a15ae-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a15ae-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a15ae-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a15ae-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a15ae-136"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a15ae-136"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="a15ae-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a15ae-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a15ae-138"><dt>Mfvdsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a15ae-138"><dt>Mfvdsp.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a15ae-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="a15ae-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a15ae-140">Procesadores de señal digital</span><span class="sxs-lookup"><span data-stu-id="a15ae-140">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




