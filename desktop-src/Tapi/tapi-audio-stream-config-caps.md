---
description: La estructura de los límites de la configuración de la \_ secuencia de audio TAPI \_ \_ \_ está contenida en la estructura de la configuración de la secuencia de TAPI \_ \_ \_ Cap cuando el miembro CapsType se establece en el miembro AudioCap de la Unión StreamConfigCapsType.
ms.assetid: 61575839-4604-4c8b-ae4d-fe796c3c5314
title: TAPI_AUDIO_STREAM_CONFIG_CAPS estructura (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daec587a8e760bedd3ab9c6b3469ef8f70b72383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679487"
---
# <a name="tapi_audio_stream_config_caps-structure"></a><span data-ttu-id="a05de-103">Estructura de los límites de configuración de la \_ secuencia de audio TAPI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a05de-103">TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="a05de-104">\[ Esta estructura no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a05de-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a05de-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="a05de-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a05de-106">La estructura de los límites de la configuración de la **\_ secuencia de audio \_ \_ \_ TAPI** está contenida en la estructura de la configuración de la [**secuencia de TAPI \_ \_ \_ Cap**](tapi-stream-config-caps.md) cuando el miembro **CapsType** se establece en el miembro **AudioCap** de la Unión [**StreamConfigCapsType**](streamconfigcapstype.md) .</span><span class="sxs-lookup"><span data-stu-id="a05de-106">The **TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS** structure is contained by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure when the **CapsType** member is set to the **AudioCap** member of the [**StreamConfigCapsType**](streamconfigcapstype.md) union.</span></span>

## <a name="syntax"></a><span data-ttu-id="a05de-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a05de-107">Syntax</span></span>


```C++
} TAPI_AUDIO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="a05de-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a05de-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a05de-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a05de-109">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a05de-110">Descripción detallada del tipo de configuración de la secuencia de audio que se va a mostrar a los usuarios de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a05de-110">A friendly description of the audio stream configuration type for display to application users.</span></span>

</dd> <dt>

<span data-ttu-id="a05de-111">**MinimumChannels**</span><span class="sxs-lookup"><span data-stu-id="a05de-111">**MinimumChannels**</span></span>
</dt> <dd>

<span data-ttu-id="a05de-112">Número mínimo de canales asociados a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="a05de-112">The minimum number of channels associated with the stream.</span></span>

</dd> <dt>

<span data-ttu-id="a05de-113">**MaximumChannels**</span><span class="sxs-lookup"><span data-stu-id="a05de-113">**MaximumChannels**</span></span>
</dt> <dd>

<span data-ttu-id="a05de-114">Número máximo de canales asociados a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="a05de-114">The maximum number of channels associated with the stream.</span></span>

</dd> <dt>

<span data-ttu-id="a05de-115">**ChannelsGranularity**</span><span class="sxs-lookup"><span data-stu-id="a05de-115">**ChannelsGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="a05de-116">La granularidad del número de canales.</span><span class="sxs-lookup"><span data-stu-id="a05de-116">The granularity of the channel count.</span></span>

</dd> <dt>

<span data-ttu-id="a05de-117">**MinimumBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="a05de-117">**MinimumBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="a05de-118">Número mínimo de bits por muestra.</span><span class="sxs-lookup"><span data-stu-id="a05de-118">The minimum number of bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="a05de-119">**MaximumBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="a05de-119">**MaximumBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="a05de-120">Número máximo de bits por muestra.</span><span class="sxs-lookup"><span data-stu-id="a05de-120">The maximum number of bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="a05de-121">**BitsPerSampleGranularity**</span><span class="sxs-lookup"><span data-stu-id="a05de-121">**BitsPerSampleGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="a05de-122">La granularidad de los bits por los valores de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a05de-122">The granularity of the bits per sample values.</span></span>

</dd> <dt>

<span data-ttu-id="a05de-123">**MinimumSampleFrequency**</span><span class="sxs-lookup"><span data-stu-id="a05de-123">**MinimumSampleFrequency**</span></span>
</dt> <dd>

<span data-ttu-id="a05de-124">La frecuencia de muestreo mínima.</span><span class="sxs-lookup"><span data-stu-id="a05de-124">The minimum sampling frequency.</span></span>

</dd> <dt>

<span data-ttu-id="a05de-125">**MaximumSampleFrequency**</span><span class="sxs-lookup"><span data-stu-id="a05de-125">**MaximumSampleFrequency**</span></span>
</dt> <dd>

<span data-ttu-id="a05de-126">La frecuencia de muestreo máxima.</span><span class="sxs-lookup"><span data-stu-id="a05de-126">The maximum sampling frequency.</span></span>

</dd> <dt>

<span data-ttu-id="a05de-127">**SampleFrequencyGranularity**</span><span class="sxs-lookup"><span data-stu-id="a05de-127">**SampleFrequencyGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="a05de-128">La granularidad de los valores de frecuencia de muestreo.</span><span class="sxs-lookup"><span data-stu-id="a05de-128">The granularity of the sampling frequency values.</span></span>

</dd> <dt>

<span data-ttu-id="a05de-129">**MinimumAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="a05de-129">**MinimumAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="a05de-130">Promedio mínimo de bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="a05de-130">The minimum average bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="a05de-131">**MaximumAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="a05de-131">**MaximumAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="a05de-132">Promedio máximo de bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="a05de-132">The maximum average bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="a05de-133">**AvgBytesPerSecGranularity**</span><span class="sxs-lookup"><span data-stu-id="a05de-133">**AvgBytesPerSecGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="a05de-134">La granularidad de los valores de bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="a05de-134">The granularity of the bytes per second values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a05de-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a05de-135">Requirements</span></span>



| <span data-ttu-id="a05de-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a05de-136">Requirement</span></span> | <span data-ttu-id="a05de-137">Value</span><span class="sxs-lookup"><span data-stu-id="a05de-137">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a05de-138">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="a05de-138">TAPI version</span></span><br/> | <span data-ttu-id="a05de-139">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="a05de-139">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="a05de-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a05de-140">Header</span></span><br/>       | <dl> <span data-ttu-id="a05de-141"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a05de-141"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a05de-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="a05de-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a05de-143">**\_Cap de \_ configuración de secuencia TAPI \_**</span><span class="sxs-lookup"><span data-stu-id="a05de-143">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




