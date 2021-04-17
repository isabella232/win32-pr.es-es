---
description: Las \_ constantes LINECALLPARAMFLAGS describen varias marcas de estado sobre una llamada.
ms.assetid: f323ec9f-5bab-4b5d-93ef-8a552ee0d591
title: Constantes de LINECALLPARAMFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e70fe2721e6fce0ac509b50290b1ec3788f3c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678990"
---
# <a name="linecallparamflags_-constants"></a><span data-ttu-id="02fb7-103">Constantes de LINECALLPARAMFLAGS \_</span><span class="sxs-lookup"><span data-stu-id="02fb7-103">LINECALLPARAMFLAGS\_ Constants</span></span>

<span data-ttu-id="02fb7-104">Las **constantes \_ LINECALLPARAMFLAGS** describen varias marcas de estado sobre una llamada.</span><span class="sxs-lookup"><span data-stu-id="02fb7-104">The **LINECALLPARAMFLAGS\_** constants describe various status flags about a call.</span></span>

<dl> <dt>

<span data-ttu-id="02fb7-105"><span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**LINECALLPARAMFLAGS \_ BLOCKID**</span><span class="sxs-lookup"><span data-stu-id="02fb7-105"><span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**LINECALLPARAMFLAGS\_BLOCKID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02fb7-106">La identidad del originador debe ocultarse (identificador del llamador de bloque).</span><span class="sxs-lookup"><span data-stu-id="02fb7-106">The originator identity should be concealed (block caller ID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02fb7-107"><span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**LINECALLPARAMFLAGS \_ DESTOFFHOOK**</span><span class="sxs-lookup"><span data-stu-id="02fb7-107"><span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**LINECALLPARAMFLAGS\_DESTOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02fb7-108">El teléfono de la entidad a la que se llama debe tomarse automáticamente OffHook.</span><span class="sxs-lookup"><span data-stu-id="02fb7-108">The called party's phone should be automatically taken offhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02fb7-109"><span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS \_ inactivo**</span><span class="sxs-lookup"><span data-stu-id="02fb7-109"><span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS\_IDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02fb7-110">La llamada se debe originar en el aspecto de una llamada inactiva y no unirse a una llamada en curso.</span><span class="sxs-lookup"><span data-stu-id="02fb7-110">The call should be originated on an idle call appearance and not join a call in progress.</span></span> <span data-ttu-id="02fb7-111">Cuando se usa la función [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) , si \_ no se establece el valor inactivo de LINECALLPARAMFLAGS y hay una llamada existente en la línea, la función se interrumpe en la llamada existente si es necesario para realizar la nueva llamada.</span><span class="sxs-lookup"><span data-stu-id="02fb7-111">When using the [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) function, if the LINECALLPARAMFLAGS\_IDLE value is not set and there is an existing call on the line, the function breaks into the existing call if necessary to make the new call.</span></span> <span data-ttu-id="02fb7-112">Si no hay ninguna llamada existente, la función realiza la nueva llamada según lo especificado.</span><span class="sxs-lookup"><span data-stu-id="02fb7-112">If there is no existing call, the function makes the new call as specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02fb7-113"><span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**LINECALLPARAMFLAGS \_ NOHOLDCONFERENCE**</span><span class="sxs-lookup"><span data-stu-id="02fb7-113"><span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**LINECALLPARAMFLAGS\_NOHOLDCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02fb7-114">Este bit solo se usa junto con [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) y [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference).</span><span class="sxs-lookup"><span data-stu-id="02fb7-114">This bit is used only in conjunction with [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) and [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference).</span></span> <span data-ttu-id="02fb7-115">La dirección que se va a incluir en la Conferencia con la llamada actual se especifica en el miembro **targetAddress** de [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span><span class="sxs-lookup"><span data-stu-id="02fb7-115">The address to be conferenced with the current call is specified in the **TargetAddress** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span></span> <span data-ttu-id="02fb7-116">La llamada de consulta no dibuja físicamente el tono de marcado desde el conmutador, pero progresará a través de varios Estados del establecimiento de llamadas (por ejemplo, marcado y continuación).</span><span class="sxs-lookup"><span data-stu-id="02fb7-116">The consultation call does not physically draw dial tone from the switch, but will progress through various call establishment states (for example, dialing, proceeding).</span></span> <span data-ttu-id="02fb7-117">Cuando la llamada de consulta alcanza el estado conectado, la Conferencia se establece automáticamente. la llamada original, que permaneció en estado conectado, entra en el estado de conferencia; la llamada de consulta entra en el estado de conferencia; el hConfCall entra en el estado conectado.</span><span class="sxs-lookup"><span data-stu-id="02fb7-117">When the consultation call reaches the connected state, the conference is automatically established; the original call, which had remained in the connected state, enters the conferenced state; the consultation call enters the conferenced state; the hConfCall enters the connected state.</span></span> <span data-ttu-id="02fb7-118">Si se produce un error en la llamada de consulta (entra en el estado disconnected seguido de idle), el hConfCall también entra en el estado inactivo y la llamada original (que puede haber sido una conferencia existente, en el caso de **linePrepareAddToConference**) permanece en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="02fb7-118">If the consultation call fails (enters the disconnected state followed by idle), the hConfCall also enters the idle state, and the original call (which may have been an existing conference, in the case of **linePrepareAddToConference**) remains in the connected state.</span></span> <span data-ttu-id="02fb7-119">La entidad original (o entidades) nunca percibe que la llamada ha desaparecido.</span><span class="sxs-lookup"><span data-stu-id="02fb7-119">The original party (or parties) never perceive the call has having gone onhold.</span></span> <span data-ttu-id="02fb7-120">Esta característica se usa a menudo para agregar un supervisor a una llamada del agente ACD cuando sea necesario para supervisar las interacciones con un llamador Irate.</span><span class="sxs-lookup"><span data-stu-id="02fb7-120">This feature is often used to add a supervisor to an ACD agent call when necessary to monitor interactions with an irate caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02fb7-121"><span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**LINECALLPARAMFLAGS \_ ONESTEPTRANSFER**</span><span class="sxs-lookup"><span data-stu-id="02fb7-121"><span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**LINECALLPARAMFLAGS\_ONESTEPTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02fb7-122">Este bit solo se usa junto con [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span><span class="sxs-lookup"><span data-stu-id="02fb7-122">This bit is used only in conjunction with [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span></span> <span data-ttu-id="02fb7-123">Combina el funcionamiento de **lineSetupTransfer** seguido de la llamada de [**consulta en un**](/windows/desktop/api/Tapi/nf-tapi-linedial) solo paso.</span><span class="sxs-lookup"><span data-stu-id="02fb7-123">It combines the operation of **lineSetupTransfer** followed by [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) on the consultation call into a single step.</span></span> <span data-ttu-id="02fb7-124">La dirección que se va a marcar se especifica en el miembro **targetAddress** de [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span><span class="sxs-lookup"><span data-stu-id="02fb7-124">The address to be dialed is specified in the **TargetAddress** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span></span> <span data-ttu-id="02fb7-125">La llamada original se coloca en el estado *onholdpendingtransfer* , al igual que si se llamara a **lineSetupTransfer** normalmente, y la llamada de consulta se establece normalmente.</span><span class="sxs-lookup"><span data-stu-id="02fb7-125">The original call is placed in *onholdpendingtransfer* state, just as if **lineSetupTransfer** were called normally, and the consultation call is established normally.</span></span> <span data-ttu-id="02fb7-126">La aplicación debe seguir llamando a [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) para que afecte a la transferencia.</span><span class="sxs-lookup"><span data-stu-id="02fb7-126">The application must still call [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) to effect the transfer.</span></span> <span data-ttu-id="02fb7-127">Esta característica se usa a menudo al invocar una transferencia desde un servidor a través de un vínculo de control de llamadas de terceros, ya que estos vínculos no admiten con frecuencia el proceso normal de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="02fb7-127">This feature is often used when invoking a transfer from a server over a third-party call control link, because such links frequently do not support the normal two-step process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02fb7-128"><span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**LINECALLPARAMFLAGS \_ ORIGOFFHOOK**</span><span class="sxs-lookup"><span data-stu-id="02fb7-128"><span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**LINECALLPARAMFLAGS\_ORIGOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02fb7-129">El teléfono del autor debe tomarse automáticamente OffHook.</span><span class="sxs-lookup"><span data-stu-id="02fb7-129">The originator's phone should be automatically taken offhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02fb7-130"><span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**LINECALLPARAMFLAGS \_ PREDICTIVEDIAL**</span><span class="sxs-lookup"><span data-stu-id="02fb7-130"><span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**LINECALLPARAMFLAGS\_PREDICTIVEDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02fb7-131">Este bit solo se usa cuando se realiza una llamada en una dirección con funcionalidad de marcado de predicción (LINEADDRCAPFLAGS \_ PREDICTIVEDIALER está activada en el miembro **DwAddrCapFlags** de [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)).</span><span class="sxs-lookup"><span data-stu-id="02fb7-131">This bit is used only when placing a call on an address with predictive dialing capability (LINEADDRCAPFLAGS\_PREDICTIVEDIALER is on in the **dwAddrCapFlags** member in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)).</span></span> <span data-ttu-id="02fb7-132">El bit debe estar activado para habilitar el progreso de llamada mejorado y/o las capacidades de supervisión de dispositivos multimedia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="02fb7-132">The bit must be on to enable the enhanced call progress and/or media device monitoring capabilities of the device.</span></span> <span data-ttu-id="02fb7-133">Si este bit no está activado, la llamada se realizará sin el progreso de llamada mejorado o la supervisión de tipo de medio, y no se iniciará ninguna transferencia automática en función del estado de la llamada.</span><span class="sxs-lookup"><span data-stu-id="02fb7-133">If this bit is not on, the call will be placed without enhanced call progress or media type monitoring, and no automatic transfer will be initiated based on call state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02fb7-134"><span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**LINECALLPARAMFLAGS \_ seguro**</span><span class="sxs-lookup"><span data-stu-id="02fb7-134"><span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**LINECALLPARAMFLAGS\_SECURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02fb7-135">La llamada debe estar configurada como segura.</span><span class="sxs-lookup"><span data-stu-id="02fb7-135">The call should be set up as secure.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02fb7-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02fb7-136">Remarks</span></span>

<span data-ttu-id="02fb7-137">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="02fb7-137">No extensibility.</span></span> <span data-ttu-id="02fb7-138">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="02fb7-138">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="02fb7-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02fb7-139">Requirements</span></span>



| <span data-ttu-id="02fb7-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="02fb7-140">Requirement</span></span> | <span data-ttu-id="02fb7-141">Value</span><span class="sxs-lookup"><span data-stu-id="02fb7-141">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="02fb7-142">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="02fb7-142">TAPI version</span></span><br/> | <span data-ttu-id="02fb7-143">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="02fb7-143">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="02fb7-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02fb7-144">Header</span></span><br/>       | <dl> <span data-ttu-id="02fb7-145"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="02fb7-145"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02fb7-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="02fb7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02fb7-147">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="02fb7-147">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="02fb7-148">**LINECALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="02fb7-148">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="02fb7-149">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="02fb7-149">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="02fb7-150">**Fino**</span><span class="sxs-lookup"><span data-stu-id="02fb7-150">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[<span data-ttu-id="02fb7-151">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="02fb7-151">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="02fb7-152">**linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="02fb7-152">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[<span data-ttu-id="02fb7-153">**lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="02fb7-153">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[<span data-ttu-id="02fb7-154">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="02fb7-154">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




