---
description: La estructura de los límites de la configuración de la \_ secuencia de vídeo TAPI \_ \_ \_ está contenida en la estructura de la configuración de la secuencia de TAPI \_ \_ \_ Cap cuando el miembro CapsType se establece en el miembro VideoCap de la Unión StreamConfigCapsType.
ms.assetid: 8812755a-50e8-4d8e-ab67-7a3a4b2a4a67
title: TAPI_VIDEO_STREAM_CONFIG_CAPS estructura (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525a35cb7c7332aa4e80fe8d5e2436e75e2d5c08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680931"
---
# <a name="tapi_video_stream_config_caps-structure"></a><span data-ttu-id="69fc8-103">Estructura de los límites de la configuración de la \_ secuencia de vídeo TAPI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="69fc8-103">TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="69fc8-104">\[ Esta estructura no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="69fc8-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="69fc8-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="69fc8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="69fc8-106">La estructura de los límites de la configuración de la **\_ secuencia de vídeo \_ \_ \_ TAPI** está contenida en la estructura de la configuración de la [**secuencia de TAPI \_ \_ \_ Cap**](tapi-stream-config-caps.md) cuando el miembro **CapsType** se establece en el miembro **VideoCap** de la Unión [**StreamConfigCapsType**](streamconfigcapstype.md) .</span><span class="sxs-lookup"><span data-stu-id="69fc8-106">The **TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS** structure is contained by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure when the **CapsType** member is set to the **VideoCap** member of the [**StreamConfigCapsType**](streamconfigcapstype.md) union.</span></span>

## <a name="syntax"></a><span data-ttu-id="69fc8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69fc8-107">Syntax</span></span>


```C++
} TAPI_VIDEO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="69fc8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="69fc8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="69fc8-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69fc8-109">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-110">Descripción detallada del tipo de configuración de la secuencia de audio que se va a mostrar a los usuarios de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69fc8-110">A friendly description of the audio stream configuration type for display to application users.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-111">**Videoestándar**</span><span class="sxs-lookup"><span data-stu-id="69fc8-111">**VideoStandard**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-112">Estándar de vídeo que se está usando.</span><span class="sxs-lookup"><span data-stu-id="69fc8-112">Video standard being used.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-113">**Inlocate**</span><span class="sxs-lookup"><span data-stu-id="69fc8-113">**InputSize**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-114">Tamaño de entrada del marco.</span><span class="sxs-lookup"><span data-stu-id="69fc8-114">Input size of frame.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-115">**MinCroppingSize**</span><span class="sxs-lookup"><span data-stu-id="69fc8-115">**MinCroppingSize**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-116">Tamaño mínimo de recorte.</span><span class="sxs-lookup"><span data-stu-id="69fc8-116">Minimum cropping size.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-117">**MaxCroppingSize**</span><span class="sxs-lookup"><span data-stu-id="69fc8-117">**MaxCroppingSize**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-118">Tamaño máximo de recorte.</span><span class="sxs-lookup"><span data-stu-id="69fc8-118">Maximum cropping size.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-119">**CropGranularityX**</span><span class="sxs-lookup"><span data-stu-id="69fc8-119">**CropGranularityX**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-120">Granularidad del recorte que se permite a lo largo del eje x.</span><span class="sxs-lookup"><span data-stu-id="69fc8-120">Granularity of cropping allowed along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-121">**CropGranularityY**</span><span class="sxs-lookup"><span data-stu-id="69fc8-121">**CropGranularityY**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-122">Granularidad del recorte que se permite a lo largo del eje y.</span><span class="sxs-lookup"><span data-stu-id="69fc8-122">Granularity of cropping allowed along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-123">**CropAlignX**</span><span class="sxs-lookup"><span data-stu-id="69fc8-123">**CropAlignX**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-124">Alineación del recorte del eje x.</span><span class="sxs-lookup"><span data-stu-id="69fc8-124">Alignment of x-axis cropping.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-125">**CropAlignY**</span><span class="sxs-lookup"><span data-stu-id="69fc8-125">**CropAlignY**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-126">Alineación del recorte del eje y.</span><span class="sxs-lookup"><span data-stu-id="69fc8-126">Alignment of y-axis cropping.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-127">**MinOutputSize**</span><span class="sxs-lookup"><span data-stu-id="69fc8-127">**MinOutputSize**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-128">Tamaño mínimo resultante de la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="69fc8-128">Minimum resultant size of video window.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-129">**MaxOutputSize**</span><span class="sxs-lookup"><span data-stu-id="69fc8-129">**MaxOutputSize**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-130">Tamaño máximo resultante de la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="69fc8-130">Maximum resultant size of video window.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-131">**OutputGranularityX**</span><span class="sxs-lookup"><span data-stu-id="69fc8-131">**OutputGranularityX**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-132">Granularidad del tamaño de salida a lo largo del eje x.</span><span class="sxs-lookup"><span data-stu-id="69fc8-132">Granularity of output size along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-133">**OutputGranularityY**</span><span class="sxs-lookup"><span data-stu-id="69fc8-133">**OutputGranularityY**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-134">Granularidad del tamaño de salida a lo largo del eje y.</span><span class="sxs-lookup"><span data-stu-id="69fc8-134">Granularity of output size along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-135">**StretchTapsX**</span><span class="sxs-lookup"><span data-stu-id="69fc8-135">**StretchTapsX**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-136">Estire a lo largo del eje x.</span><span class="sxs-lookup"><span data-stu-id="69fc8-136">Stretch along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-137">**StretchTapsY**</span><span class="sxs-lookup"><span data-stu-id="69fc8-137">**StretchTapsY**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-138">Ajustar a lo largo del eje y.</span><span class="sxs-lookup"><span data-stu-id="69fc8-138">Stretch along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-139">**ShrinkTapsX**</span><span class="sxs-lookup"><span data-stu-id="69fc8-139">**ShrinkTapsX**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-140">Reducir a lo largo del eje x.</span><span class="sxs-lookup"><span data-stu-id="69fc8-140">Shrink along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-141">**ShrinkTapsY**</span><span class="sxs-lookup"><span data-stu-id="69fc8-141">**ShrinkTapsY**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-142">Reducir a lo largo del eje y.</span><span class="sxs-lookup"><span data-stu-id="69fc8-142">Shrink along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-143">**MinFrameInterval**</span><span class="sxs-lookup"><span data-stu-id="69fc8-143">**MinFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-144">Intervalo mínimo de trama de vídeo.</span><span class="sxs-lookup"><span data-stu-id="69fc8-144">Minimum video frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-145">**MaxFrameInterval**</span><span class="sxs-lookup"><span data-stu-id="69fc8-145">**MaxFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-146">Intervalo máximo de trama de vídeo.</span><span class="sxs-lookup"><span data-stu-id="69fc8-146">Maximum video frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-147">**MinBitsPerSecond**</span><span class="sxs-lookup"><span data-stu-id="69fc8-147">**MinBitsPerSecond**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-148">Mínimo de bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="69fc8-148">Minimum bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="69fc8-149">**MaxBitsPerSecond**</span><span class="sxs-lookup"><span data-stu-id="69fc8-149">**MaxBitsPerSecond**</span></span>
</dt> <dd>

<span data-ttu-id="69fc8-150">Número máximo de bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="69fc8-150">Maximum bits per second.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="69fc8-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69fc8-151">Requirements</span></span>



| <span data-ttu-id="69fc8-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="69fc8-152">Requirement</span></span> | <span data-ttu-id="69fc8-153">Value</span><span class="sxs-lookup"><span data-stu-id="69fc8-153">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69fc8-154">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="69fc8-154">TAPI version</span></span><br/> | <span data-ttu-id="69fc8-155">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="69fc8-155">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="69fc8-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69fc8-156">Header</span></span><br/>       | <dl> <span data-ttu-id="69fc8-157"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="69fc8-157"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69fc8-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="69fc8-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69fc8-159">**\_Cap de \_ configuración de secuencia TAPI \_**</span><span class="sxs-lookup"><span data-stu-id="69fc8-159">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




