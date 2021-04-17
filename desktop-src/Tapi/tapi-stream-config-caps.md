---
description: La estructura de los Cap de configuración de la \_ secuencia TAPI \_ \_ contiene información de configuración de flujo de audio o vídeo.
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: TAPI_STREAM_CONFIG_CAPS estructura (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379ca481d3bebaf8ceb11bfc2dbdab6642ca20b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680360"
---
# <a name="tapi_stream_config_caps-structure"></a><span data-ttu-id="f404c-103">Estructura de los límites de configuración de la \_ secuencia TAPI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f404c-103">TAPI\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="f404c-104">\[ Esta estructura no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f404c-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f404c-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="f404c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f404c-106">La estructura de los **\_ \_ \_ Cap** de configuración de la secuencia TAPI contiene información de configuración de flujo de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="f404c-106">The **TAPI\_STREAM\_CONFIG\_CAPS** structure contains either video or audio stream configuration information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f404c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f404c-107">Syntax</span></span>


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="f404c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f404c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f404c-109">**CapsType**</span><span class="sxs-lookup"><span data-stu-id="f404c-109">**CapsType**</span></span>
</dt> <dd>

<span data-ttu-id="f404c-110">Define si el miembro de Unión contiene información de vídeo o de audio.</span><span class="sxs-lookup"><span data-stu-id="f404c-110">Defines whether the union member contains video or audio information.</span></span>

</dd> <dt>

<span data-ttu-id="f404c-111">**VideoCap**</span><span class="sxs-lookup"><span data-stu-id="f404c-111">**VideoCap**</span></span>
</dt> <dd>

<span data-ttu-id="f404c-112">Una estructura de [**vídeo de configuración de \_ secuencia de vídeo \_ \_ \_ TAPI**](tapi-video-stream-config-caps.md) que contiene las capacidades de flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f404c-112">A [**TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS**](tapi-video-stream-config-caps.md) structure containing the video stream capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="f404c-113">**AudioCap**</span><span class="sxs-lookup"><span data-stu-id="f404c-113">**AudioCap**</span></span>
</dt> <dd>

<span data-ttu-id="f404c-114">Una estructura de [**\_ configuración de flujo de audio \_ \_ \_ TAPI**](tapi-audio-stream-config-caps.md) que contiene las capacidades de secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="f404c-114">A [**TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS**](tapi-audio-stream-config-caps.md) structure containing the audio stream capabilities.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f404c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f404c-115">Requirements</span></span>



| <span data-ttu-id="f404c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f404c-116">Requirement</span></span> | <span data-ttu-id="f404c-117">Value</span><span class="sxs-lookup"><span data-stu-id="f404c-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f404c-118">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f404c-118">TAPI version</span></span><br/> | <span data-ttu-id="f404c-119">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="f404c-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="f404c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f404c-120">Header</span></span><br/>       | <dl> <span data-ttu-id="f404c-121"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f404c-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f404c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f404c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f404c-123">**ITFormatControl::GetStreamCaps**</span><span class="sxs-lookup"><span data-stu-id="f404c-123">**ITFormatControl::GetStreamCaps**</span></span>](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[<span data-ttu-id="f404c-124">**StreamConfigCapsType**</span><span class="sxs-lookup"><span data-stu-id="f404c-124">**StreamConfigCapsType**</span></span>](streamconfigcapstype.md)
</dt> <dt>

[<span data-ttu-id="f404c-125">**\_Cap de \_ configuración de secuencia de vídeo TAPI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f404c-125">**TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-video-stream-config-caps.md)
</dt> <dt>

[<span data-ttu-id="f404c-126">**\_Cap de \_ configuración de secuencia de audio TAPI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f404c-126">**TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




