---
description: La \_ enumeración de eventos participante describe los eventos de los participantes.
ms.assetid: 678165f2-ad0b-415f-86bf-8c4e3bd8d793
title: Enumeración PARTICIPANT_EVENT (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225b1b9901efa5648dfaa326c53ed69cff2c4295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690328"
---
# <a name="participant_event-enumeration"></a><span data-ttu-id="baf56-103">\_Enumeración de eventos de participantes</span><span class="sxs-lookup"><span data-stu-id="baf56-103">PARTICIPANT\_EVENT enumeration</span></span>

<span data-ttu-id="baf56-104">\[ Esta enumeración no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="baf56-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="baf56-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="baf56-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="baf56-106">La enumeración de **\_ eventos participante** describe los eventos de los participantes.</span><span class="sxs-lookup"><span data-stu-id="baf56-106">The **PARTICIPANT\_EVENT** enum describes participant events.</span></span> <span data-ttu-id="baf56-107">El método de [**\_ evento ITParticipantEvent:: get**](itparticipantevent-get-event.md) devuelve un miembro de esta enumeración para indicar el tipo de evento de participante de conferencia que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="baf56-107">The [**ITParticipantEvent::get\_Event**](itparticipantevent-get-event.md) method returns a member of this enum to indicate the type of conference participant event that occurred.</span></span> <span data-ttu-id="baf56-108">Esta enumeración la usan las aplicaciones que acceden a [IPCONF MSP](ipconf-msp.md).</span><span class="sxs-lookup"><span data-stu-id="baf56-108">This enum is used by applications that access the [IPConf MSP](ipconf-msp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="baf56-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="baf56-109">Syntax</span></span>


```C++
} PARTICIPANT_EVENT;
```



## <a name="constants"></a><span data-ttu-id="baf56-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="baf56-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="baf56-111"><span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**\_nuevo \_ participante de PE**</span><span class="sxs-lookup"><span data-stu-id="baf56-111"><span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**PE\_NEW\_PARTICIPANT**</span></span>
</dt> <dd>

<span data-ttu-id="baf56-112">Se ha agregado un nuevo participante a la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="baf56-112">A new participant has been added to the conference.</span></span>

</dd> <dt>

<span data-ttu-id="baf56-113"><span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**\_cambio de información de PE \_**</span><span class="sxs-lookup"><span data-stu-id="baf56-113"><span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**PE\_INFO\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="baf56-114">La información sobre un participante ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="baf56-114">Information on a participant has changed.</span></span>

</dd> <dt>

<span data-ttu-id="baf56-115"><span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**\_ausencia de participante de PE \_**</span><span class="sxs-lookup"><span data-stu-id="baf56-115"><span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**PE\_PARTICIPANT\_LEAVE**</span></span>
</dt> <dd>

<span data-ttu-id="baf56-116">Un participante ha abandonado la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="baf56-116">A participant has left the conference.</span></span>

</dd> <dt>

<span data-ttu-id="baf56-117"><span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**\_nuevo \_ subflujo de PE**</span><span class="sxs-lookup"><span data-stu-id="baf56-117"><span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**PE\_NEW\_SUBSTREAM**</span></span>
</dt> <dd>

<span data-ttu-id="baf56-118">Se ha agregado un subflujo nuevo al participante.</span><span class="sxs-lookup"><span data-stu-id="baf56-118">A new substream has been added to the participant.</span></span>

</dd> <dt>

<span data-ttu-id="baf56-119"><span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**\_SUBFLUJO PE \_ quitado**</span><span class="sxs-lookup"><span data-stu-id="baf56-119"><span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**PE\_SUBSTREAM\_REMOVED**</span></span>
</dt> <dd>

<span data-ttu-id="baf56-120">Se ha quitado un subflujo nuevo del participante.</span><span class="sxs-lookup"><span data-stu-id="baf56-120">A new substream has been removed from the participant.</span></span>

</dd> <dt>

<span data-ttu-id="baf56-121"><span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**subsecuencia de PE \_ \_ asignada**</span><span class="sxs-lookup"><span data-stu-id="baf56-121"><span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**PE\_SUBSTREAM\_MAPPED**</span></span>
</dt> <dd>

<span data-ttu-id="baf56-122">Un participante se ha asignado a un subflujo.</span><span class="sxs-lookup"><span data-stu-id="baf56-122">A participant has been mapped to a substream.</span></span>

</dd> <dt>

<span data-ttu-id="baf56-123"><span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**subsecuencia PE sin \_ \_ asignar**</span><span class="sxs-lookup"><span data-stu-id="baf56-123"><span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**PE\_SUBSTREAM\_UNMAPPED**</span></span>
</dt> <dd>

<span data-ttu-id="baf56-124">Un participante se ha desasignado de un subflujo.</span><span class="sxs-lookup"><span data-stu-id="baf56-124">A participant has been unmapped from a substream.</span></span>

</dd> <dt>

<span data-ttu-id="baf56-125"><span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**tiempo de espera de \_ participante de PE \_**</span><span class="sxs-lookup"><span data-stu-id="baf56-125"><span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**PE\_PARTICIPANT\_TIMEOUT**</span></span>
</dt> <dd>

<span data-ttu-id="baf56-126">Se ha quitado un participante de la Conferencia debido a un tiempo de espera agotado.</span><span class="sxs-lookup"><span data-stu-id="baf56-126">A participant has been removed from the conference due to a timeout.</span></span>

</dd> <dt>

<span data-ttu-id="baf56-127"><span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**participante de PE \_ \_ recuperado**</span><span class="sxs-lookup"><span data-stu-id="baf56-127"><span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**PE\_PARTICIPANT\_RECOVERED**</span></span>
</dt> <dd>

<span data-ttu-id="baf56-128">Un participante quitado vuelve a estar visible.</span><span class="sxs-lookup"><span data-stu-id="baf56-128">A removed participant is again visible.</span></span> <span data-ttu-id="baf56-129">Normalmente, es un participante que ha agotado el tiempo de espera, pero ahora se están recibiendo señales.</span><span class="sxs-lookup"><span data-stu-id="baf56-129">Usually, this is a participant who timed out but signals are now being received.</span></span>

</dd> <dt>

<span data-ttu-id="baf56-130"><span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**participante de PE \_ \_ activo**</span><span class="sxs-lookup"><span data-stu-id="baf56-130"><span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**PE\_PARTICIPANT\_ACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="baf56-131">El participante se ha vuelto activo en la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="baf56-131">The participant has become active in the conference.</span></span>

</dd> <dt>

<span data-ttu-id="baf56-132"><span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**participante de PE \_ \_ inactivo**</span><span class="sxs-lookup"><span data-stu-id="baf56-132"><span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**PE\_PARTICIPANT\_INACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="baf56-133">El participante ha dejado de estar activo en la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="baf56-133">The participant has become inactive in the conference.</span></span>

</dd> <dt>

<span data-ttu-id="baf56-134"><span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**\_comunicación local de PE \_**</span><span class="sxs-lookup"><span data-stu-id="baf56-134"><span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**PE\_LOCAL\_TALKING**</span></span>
</dt> <dd>

<span data-ttu-id="baf56-135">El participante local ha empezado a hablar.</span><span class="sxs-lookup"><span data-stu-id="baf56-135">The local participant has started to talk.</span></span>

</dd> <dt>

<span data-ttu-id="baf56-136"><span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE \_ local \_ silenciosa**</span><span class="sxs-lookup"><span data-stu-id="baf56-136"><span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE\_LOCAL\_SILENT**</span></span>
</dt> <dd>

<span data-ttu-id="baf56-137">El participante local se ha vuelto silencioso en la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="baf56-137">The local participant has become silent in the conference.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="baf56-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baf56-138">Requirements</span></span>



| <span data-ttu-id="baf56-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="baf56-139">Requirement</span></span> | <span data-ttu-id="baf56-140">Value</span><span class="sxs-lookup"><span data-stu-id="baf56-140">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="baf56-141">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="baf56-141">TAPI version</span></span><br/> | <span data-ttu-id="baf56-142">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="baf56-142">Requires TAPI 3.0 or later</span></span><br/>                                              |
| <span data-ttu-id="baf56-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="baf56-143">Header</span></span><br/>       | <dl> <span data-ttu-id="baf56-144"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="baf56-144"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baf56-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="baf56-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baf56-146">**ITParticipantEvent:: get ( \_ evento)**</span><span class="sxs-lookup"><span data-stu-id="baf56-146">**ITParticipantEvent::get\_Event**</span></span>](itparticipantevent-get-event.md)
</dt> <dt>

[<span data-ttu-id="baf56-147">IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="baf56-147">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="baf56-148">Interfaces de IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="baf56-148">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




