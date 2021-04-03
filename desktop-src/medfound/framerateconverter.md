---
description: Cambia la velocidad de fotogramas de una secuencia de vídeo.
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: Convertidor de velocidad de fotogramas DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6197c29e9e753db6f327aa8b2797ba04131448d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808072"
---
# <a name="frame-rate-converter-dsp"></a><span data-ttu-id="34a22-103">DSP de convertidor de velocidad de fotogramas</span><span class="sxs-lookup"><span data-stu-id="34a22-103">Frame Rate Converter DSP</span></span>

<span data-ttu-id="34a22-104">Cambia la velocidad de fotogramas de una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="34a22-104">Changes the frame rate of a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="34a22-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="34a22-105">CLSID</span></span>

<span data-ttu-id="34a22-106">CLSID \_ CFrameRateConvertDmo</span><span class="sxs-lookup"><span data-stu-id="34a22-106">CLSID\_CFrameRateConvertDmo</span></span>

## <a name="interfaces"></a><span data-ttu-id="34a22-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="34a22-107">Interfaces</span></span>

-   <span data-ttu-id="34a22-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="34a22-108">**IMediaObject**</span></span>
-   <span data-ttu-id="34a22-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="34a22-109">**IMFTransform**</span></span>
-   <span data-ttu-id="34a22-110">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="34a22-110">**IPropertyStore**</span></span>

## <a name="formats"></a><span data-ttu-id="34a22-111">Formatos</span><span class="sxs-lookup"><span data-stu-id="34a22-111">Formats</span></span>

-   <span data-ttu-id="34a22-112">ARGB 32</span><span class="sxs-lookup"><span data-stu-id="34a22-112">ARGB 32</span></span>
-   <span data-ttu-id="34a22-113">RGB 24</span><span class="sxs-lookup"><span data-stu-id="34a22-113">RGB 24</span></span>
-   <span data-ttu-id="34a22-114">RGB 32</span><span class="sxs-lookup"><span data-stu-id="34a22-114">RGB 32</span></span>
-   <span data-ttu-id="34a22-115">RGB 555</span><span class="sxs-lookup"><span data-stu-id="34a22-115">RGB 555</span></span>
-   <span data-ttu-id="34a22-116">RGB 565</span><span class="sxs-lookup"><span data-stu-id="34a22-116">RGB 565</span></span>
-   <span data-ttu-id="34a22-117">AYUV</span><span class="sxs-lookup"><span data-stu-id="34a22-117">AYUV</span></span>
-   <span data-ttu-id="34a22-118">IYUV</span><span class="sxs-lookup"><span data-stu-id="34a22-118">IYUV</span></span>
-   <span data-ttu-id="34a22-119">UYVY</span><span class="sxs-lookup"><span data-stu-id="34a22-119">UYVY</span></span>
-   <span data-ttu-id="34a22-120">Y211</span><span class="sxs-lookup"><span data-stu-id="34a22-120">Y211</span></span>
-   <span data-ttu-id="34a22-121">Y411</span><span class="sxs-lookup"><span data-stu-id="34a22-121">Y411</span></span>
-   <span data-ttu-id="34a22-122">Y41P</span><span class="sxs-lookup"><span data-stu-id="34a22-122">Y41P</span></span>
-   <span data-ttu-id="34a22-123">YUY2</span><span class="sxs-lookup"><span data-stu-id="34a22-123">YUY2</span></span>
-   <span data-ttu-id="34a22-124">YUYV</span><span class="sxs-lookup"><span data-stu-id="34a22-124">YUYV</span></span>
-   <span data-ttu-id="34a22-125">YV12</span><span class="sxs-lookup"><span data-stu-id="34a22-125">YV12</span></span>
-   <span data-ttu-id="34a22-126">YVYU</span><span class="sxs-lookup"><span data-stu-id="34a22-126">YVYU</span></span>

## <a name="properties"></a><span data-ttu-id="34a22-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="34a22-127">Properties</span></span>

-   [<span data-ttu-id="34a22-128">MFPKEY \_ conv \_ INPUTFRAMERATE</span><span class="sxs-lookup"><span data-stu-id="34a22-128">MFPKEY\_CONV\_INPUTFRAMERATE</span></span>](mfpkey-conv-inputframerate.md)
-   [<span data-ttu-id="34a22-129">MFPKEY \_ conv \_ OUTPUTFRAMERATE</span><span class="sxs-lookup"><span data-stu-id="34a22-129">MFPKEY\_CONV\_OUTPUTFRAMERATE</span></span>](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a><span data-ttu-id="34a22-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34a22-130">Remarks</span></span>

<span data-ttu-id="34a22-131">Este DSP cambia la velocidad de fotogramas repitiendo o colocando fotogramas.</span><span class="sxs-lookup"><span data-stu-id="34a22-131">This DSP changes the frame rate by repeating or dropping frames.</span></span>

<span data-ttu-id="34a22-132">De forma predeterminada, el DSP obtiene las velocidades de fotogramas de los tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="34a22-132">By default, the DSP gets the frame rates from the media types.</span></span> <span data-ttu-id="34a22-133">Opcionalmente, puede especificar las velocidades de fotogramas mediante el establecimiento de las \_ propiedades MFPKEY CONV \_ INPUTFRAMERATE y MFPKEY \_ conv \_ OUTPUTFRAMERATE.</span><span class="sxs-lookup"><span data-stu-id="34a22-133">Optionally, you can specify the frame rates by setting the MFPKEY\_CONV\_INPUTFRAMERATE and MFPKEY\_CONV\_OUTPUTFRAMERATE properties.</span></span> <span data-ttu-id="34a22-134">Estos valores invalidan la velocidad de fotogramas proporcionada en el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="34a22-134">These values override the frame rate given in the media type.</span></span> <span data-ttu-id="34a22-135">Sin embargo, si usa este DSP dentro de la canalización de Media Foundation, no debe establecer estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="34a22-135">However, if you are using this DSP within the Media Foundation pipeline, you should not set these properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="34a22-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34a22-136">Requirements</span></span>



| <span data-ttu-id="34a22-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="34a22-137">Requirement</span></span> | <span data-ttu-id="34a22-138">Value</span><span class="sxs-lookup"><span data-stu-id="34a22-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34a22-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34a22-139">Minimum supported client</span></span><br/> | <span data-ttu-id="34a22-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="34a22-140">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="34a22-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34a22-141">Minimum supported server</span></span><br/> | <span data-ttu-id="34a22-142">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="34a22-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="34a22-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34a22-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="34a22-144"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="34a22-144"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="34a22-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="34a22-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34a22-146"><dt>Mfvdsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34a22-146"><dt>Mfvdsp.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="34a22-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="34a22-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34a22-148">Procesadores de señal digital</span><span class="sxs-lookup"><span data-stu-id="34a22-148">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




