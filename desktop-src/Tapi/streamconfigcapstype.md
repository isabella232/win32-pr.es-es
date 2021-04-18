---
description: La estructura de la configuración de la secuencia de TAPI usa el tipo de enumeración StreamConfigCapsType \_ \_ \_ para indicar si está implicado el streaming de audio o vídeo.
ms.assetid: c3eec6b2-ce3b-49b1-a0ba-f450d60a1477
title: Enumeración StreamConfigCapsType (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14649edb7e451cdc7d955f2028a77c247148182b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681277"
---
# <a name="streamconfigcapstype-enumeration"></a><span data-ttu-id="dbc9a-103">Enumeración StreamConfigCapsType</span><span class="sxs-lookup"><span data-stu-id="dbc9a-103">StreamConfigCapsType enumeration</span></span>

<span data-ttu-id="dbc9a-104">\[ Esta enumeración no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dbc9a-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dbc9a-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="dbc9a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="dbc9a-106">La estructura de la configuración de la [**secuencia de \_ TAPI \_ \_**](tapi-stream-config-caps.md) usa el tipo de enumeración **StreamConfigCapsType** para indicar si está implicado el streaming de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="dbc9a-106">The **StreamConfigCapsType** enumeration type is used by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure as a switch to indicate whether audio or video streaming is involved.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbc9a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbc9a-107">Syntax</span></span>


```C++
} StreamConfigCapsType;
```



## <a name="constants"></a><span data-ttu-id="dbc9a-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="dbc9a-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dbc9a-109"><span id="AudioStreamConfigCaps"></span><span id="audiostreamconfigcaps"></span><span id="AUDIOSTREAMCONFIGCAPS"></span>**AudioStreamConfigCaps**</span><span class="sxs-lookup"><span data-stu-id="dbc9a-109"><span id="AudioStreamConfigCaps"></span><span id="audiostreamconfigcaps"></span><span id="AUDIOSTREAMCONFIGCAPS"></span>**AudioStreamConfigCaps**</span></span>
</dt> <dd>

<span data-ttu-id="dbc9a-110">Configuración de transmisión por secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="dbc9a-110">Audio streaming configuration.</span></span>

</dd> <dt>

<span data-ttu-id="dbc9a-111"><span id="VideoStreamConfigCaps"></span><span id="videostreamconfigcaps"></span><span id="VIDEOSTREAMCONFIGCAPS"></span>**VideoStreamConfigCaps**</span><span class="sxs-lookup"><span data-stu-id="dbc9a-111"><span id="VideoStreamConfigCaps"></span><span id="videostreamconfigcaps"></span><span id="VIDEOSTREAMCONFIGCAPS"></span>**VideoStreamConfigCaps**</span></span>
</dt> <dd>

<span data-ttu-id="dbc9a-112">Configuración de streaming de vídeo.</span><span class="sxs-lookup"><span data-stu-id="dbc9a-112">Video streaming configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dbc9a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbc9a-113">Requirements</span></span>



| <span data-ttu-id="dbc9a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbc9a-114">Requirement</span></span> | <span data-ttu-id="dbc9a-115">Value</span><span class="sxs-lookup"><span data-stu-id="dbc9a-115">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc9a-116">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="dbc9a-116">TAPI version</span></span><br/> | <span data-ttu-id="dbc9a-117">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="dbc9a-117">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="dbc9a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dbc9a-118">Header</span></span><br/>       | <dl> <span data-ttu-id="dbc9a-119"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbc9a-119"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbc9a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="dbc9a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc9a-121">**\_Cap de \_ configuración de secuencia TAPI \_**</span><span class="sxs-lookup"><span data-stu-id="dbc9a-121">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




