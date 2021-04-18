---
description: Las \_ constantes de marcador de bits PHONEHOOKSWITCHMODE describen los componentes de micrófono y altavoz de un dispositivo conmutador.
ms.assetid: 532bf089-d5ca-4a04-847d-69e48990ff5c
title: Constantes de PHONEHOOKSWITCHMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8028cb531d5b38185edf75ae58e4c3c855398f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681288"
---
# <a name="phonehookswitchmode_-constants"></a><span data-ttu-id="d1948-103">Constantes de PHONEHOOKSWITCHMODE \_</span><span class="sxs-lookup"><span data-stu-id="d1948-103">PHONEHOOKSWITCHMODE\_ Constants</span></span>

<span data-ttu-id="d1948-104">Las constantes de marcador de bits **PHONEHOOKSWITCHMODE \_** describen los componentes de micrófono y altavoz de un dispositivo conmutador.</span><span class="sxs-lookup"><span data-stu-id="d1948-104">The **PHONEHOOKSWITCHMODE\_** bit-flag constants describe the microphone and speaker components of a hookswitch device.</span></span>

<dl> <dt>

<span data-ttu-id="d1948-105"><span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**MIC de PHONEHOOKSWITCHMODE \_**</span><span class="sxs-lookup"><span data-stu-id="d1948-105"><span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**PHONEHOOKSWITCHMODE\_MIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d1948-106">El micrófono del dispositivo está activo, el altavoz es silenciado.</span><span class="sxs-lookup"><span data-stu-id="d1948-106">The device's microphone is active, the speaker is mute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1948-107"><span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**PHONEHOOKSWITCHMODE \_ MICSPEAKER**</span><span class="sxs-lookup"><span data-stu-id="d1948-107"><span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**PHONEHOOKSWITCHMODE\_MICSPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d1948-108">El micrófono y el altavoz del dispositivo están activos.</span><span class="sxs-lookup"><span data-stu-id="d1948-108">The device's microphone and speaker are both active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1948-109"><span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**PHONEHOOKSWITCHMODE de \_ enlace**</span><span class="sxs-lookup"><span data-stu-id="d1948-109"><span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**PHONEHOOKSWITCHMODE\_ONHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d1948-110">El micrófono y el altavoz del dispositivo están conectados.</span><span class="sxs-lookup"><span data-stu-id="d1948-110">The device's microphone and speaker are both onhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1948-111"><span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**altavoz de PHONEHOOKSWITCHMODE \_**</span><span class="sxs-lookup"><span data-stu-id="d1948-111"><span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**PHONEHOOKSWITCHMODE\_SPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d1948-112">El altavoz del dispositivo está activo y el micrófono es silenciado.</span><span class="sxs-lookup"><span data-stu-id="d1948-112">The device's speaker is active, the microphone is mute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1948-113"><span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**PHONEHOOKSWITCHMODE \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="d1948-113"><span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**PHONEHOOKSWITCHMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d1948-114">El modo conmutador del dispositivo es desconocido actualmente.</span><span class="sxs-lookup"><span data-stu-id="d1948-114">The device's hookswitch mode is currently unknown.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1948-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1948-115">Remarks</span></span>

<span data-ttu-id="d1948-116">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="d1948-116">No extensibility.</span></span> <span data-ttu-id="d1948-117">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="d1948-117">All 32 bits are reserved.</span></span>

<span data-ttu-id="d1948-118">Estas constantes se utilizan para proporcionar un nivel de control individual sobre los componentes del micrófono y el altavoz de un dispositivo de teléfono.</span><span class="sxs-lookup"><span data-stu-id="d1948-118">These constants are used to provide an individual level of control over the microphone and speaker components of a phone device.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1948-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1948-119">Requirements</span></span>



| <span data-ttu-id="d1948-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1948-120">Requirement</span></span> | <span data-ttu-id="d1948-121">Value</span><span class="sxs-lookup"><span data-stu-id="d1948-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d1948-122">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="d1948-122">TAPI version</span></span><br/> | <span data-ttu-id="d1948-123">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="d1948-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d1948-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1948-124">Header</span></span><br/>       | <dl> <span data-ttu-id="d1948-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1948-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




