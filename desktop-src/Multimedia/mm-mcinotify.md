---
title: Mensaje de MM_MCINOTIFY (mmsystem. h)
description: El \_ mensaje mm MCINOTIFY notifica a una aplicación que un dispositivo MCI ha completado una operación. Los dispositivos MCI envían este mensaje solo cuando \_ se usa la marca de notificación de MCI.
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- Mensaje de MM_MCINOTIFY de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MCINOTIFY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ee62c4a2b6e17bf5ad6d719dcb7d6e992a2f2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150629"
---
# <a name="mm_mcinotify-message"></a><span data-ttu-id="823d5-105">\_Mensaje MCINOTIFY mm</span><span class="sxs-lookup"><span data-stu-id="823d5-105">MM\_MCINOTIFY message</span></span>

<span data-ttu-id="823d5-106">El mensaje **mm \_ MCINOTIFY** notifica a una aplicación que un dispositivo MCI ha completado una operación.</span><span class="sxs-lookup"><span data-stu-id="823d5-106">The **MM\_MCINOTIFY** message notifies an application that an MCI device has completed an operation.</span></span> <span data-ttu-id="823d5-107">Los dispositivos MCI envían este mensaje solo cuando \_ se usa la marca de notificación de MCI.</span><span class="sxs-lookup"><span data-stu-id="823d5-107">MCI devices send this message only when the MCI\_NOTIFY flag is used.</span></span>


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a><span data-ttu-id="823d5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="823d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="823d5-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span><span class="sxs-lookup"><span data-stu-id="823d5-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span></span>
</dt> <dd>

<span data-ttu-id="823d5-110">Motivo de la notificación.</span><span class="sxs-lookup"><span data-stu-id="823d5-110">Reason for the notification.</span></span> <span data-ttu-id="823d5-111">Se definen los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="823d5-111">The following values are defined:</span></span>



| <span data-ttu-id="823d5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="823d5-112">Requirement</span></span> | <span data-ttu-id="823d5-113">Value</span><span class="sxs-lookup"><span data-stu-id="823d5-113">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="823d5-114">la notificación de MCI se \_ \_ anuló</span><span class="sxs-lookup"><span data-stu-id="823d5-114">MCI\_NOTIFY\_ABORTED</span></span>    | <span data-ttu-id="823d5-115">El dispositivo recibió un comando que impidió que se cumplieran las condiciones actuales para iniciar la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="823d5-115">The device received a command that prevented the current conditions for initiating the callback function from being met.</span></span> <span data-ttu-id="823d5-116">Si un comando nuevo interrumpe el comando actual y también solicita la notificación, el dispositivo solo envía este mensaje y no \_ la notificación de MCI. \_</span><span class="sxs-lookup"><span data-stu-id="823d5-116">If a new command interrupts the current command and it also requests notification, the device sends this message only and not MCI\_NOTIFY\_SUPERSEDED</span></span> |
| <span data-ttu-id="823d5-117">\_error de notificación de MCI \_</span><span class="sxs-lookup"><span data-stu-id="823d5-117">MCI\_NOTIFY\_FAILURE</span></span>    | <span data-ttu-id="823d5-118">Se produjo un error de dispositivo mientras el dispositivo estaba ejecutando el comando.</span><span class="sxs-lookup"><span data-stu-id="823d5-118">A device error occurred while the device was executing the command.</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="823d5-119">la notificación de MCI se \_ \_ realizó correctamente</span><span class="sxs-lookup"><span data-stu-id="823d5-119">MCI\_NOTIFY\_SUCCESSFUL</span></span> | <span data-ttu-id="823d5-120">Se han cumplido las condiciones que inician la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="823d5-120">The conditions initiating the callback function have been met.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="823d5-121">notificación de MCI \_ \_ sustituida</span><span class="sxs-lookup"><span data-stu-id="823d5-121">MCI\_NOTIFY\_SUPERSEDED</span></span> | <span data-ttu-id="823d5-122">El dispositivo ha recibido otro comando con el indicador "Notify" establecido y se han reemplazado las condiciones actuales para iniciar la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="823d5-122">The device received another command with the "notify" flag set and the current conditions for initiating the callback function have been superseded.</span></span>                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="823d5-123"><span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*</span><span class="sxs-lookup"><span data-stu-id="823d5-123"><span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*</span></span>
</dt> <dd>

<span data-ttu-id="823d5-124">Identificador del dispositivo que inicia la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="823d5-124">Identifier of the device initiating the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="823d5-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="823d5-125">Return Value</span></span>

<span data-ttu-id="823d5-126">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="823d5-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="823d5-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="823d5-127">Remarks</span></span>

<span data-ttu-id="823d5-128">Para obtener más información acerca de la marca de notificación de MCI \_ , vea [la marca de notificación](the-notify-flag.md).</span><span class="sxs-lookup"><span data-stu-id="823d5-128">For more information about the MCI\_NOTIFY flag, see [The Notify Flag](the-notify-flag.md).</span></span>

<span data-ttu-id="823d5-129">Un dispositivo devuelve la \_ marca MCI Notify \_ Successful with **mm \_ MCINOTIFY** cuando finaliza la acción de un comando.</span><span class="sxs-lookup"><span data-stu-id="823d5-129">A device returns the MCI\_NOTIFY\_SUCCESSFUL flag with **MM\_MCINOTIFY** when the action for a command finishes.</span></span> <span data-ttu-id="823d5-130">Por ejemplo, un dispositivo de audio de CD usa esta marca para la notificación del comando [**Play**](play.md) ( [**MCI \_ Play**](mci-play.md)) cuando el dispositivo finaliza la reproducción.</span><span class="sxs-lookup"><span data-stu-id="823d5-130">For example, a CD audio device uses this flag for notification for the [**play**](play.md) ( [**MCI\_PLAY**](mci-play.md)) command when the device finishes playing.</span></span> <span data-ttu-id="823d5-131">El comando **Play** solo se ejecuta correctamente cuando llega a la posición final especificada o alcanza el final del medio.</span><span class="sxs-lookup"><span data-stu-id="823d5-131">The **play** command is successful only when it reaches the specified end position or reaches the end of the media.</span></span> <span data-ttu-id="823d5-132">Del mismo modo, los comandos [**Buscar**](seek.md) ( [**MCI \_ Seek**](mci-seek.md)) y [**registro**](record.md) ( [**\_ registro de MCI**](mci-record.md)) no devuelven la \_ notificación de MCI \_ correctamente hasta que llegan a la posición final especificada o alcanzan el final del medio.</span><span class="sxs-lookup"><span data-stu-id="823d5-132">Similarly, the [**seek**](seek.md) ( [**MCI\_SEEK**](mci-seek.md)) and [**record**](record.md) ( [**MCI\_RECORD**](mci-record.md)) commands do not return MCI\_NOTIFY\_SUCCESSFUL until they reach the specified end position or reach the end of the media.</span></span>

<span data-ttu-id="823d5-133">Un dispositivo devuelve la \_ marca MCI Notify \_ Aborted con **mm \_ MCINOTIFY** solo cuando recibe un comando que le impide cumplir las condiciones de notificación.</span><span class="sxs-lookup"><span data-stu-id="823d5-133">A device returns the MCI\_NOTIFY\_ABORTED flag with **MM\_MCINOTIFY** only when it receives a command that prevents it from meeting the notification conditions.</span></span> <span data-ttu-id="823d5-134">Por ejemplo, el comando [**Play**](play.md) no anulará la notificación de un comando **Play** anterior siempre que el comando nuevo no cambie la dirección de reproducción ni cambie la posición final.</span><span class="sxs-lookup"><span data-stu-id="823d5-134">For example, the [**play**](play.md) command would not abort notification for a previous **play** command provided that the new command does not change the play direction or change the ending position.</span></span> <span data-ttu-id="823d5-135">Los comandos de [**búsqueda**](seek.md) y [**registro**](record.md) se comportan de forma similar.</span><span class="sxs-lookup"><span data-stu-id="823d5-135">The [**seek**](seek.md) and [**record**](record.md) commands behave similarly.</span></span> <span data-ttu-id="823d5-136">MCI tampoco envía una notificación de \_ MCI \_ anulada cuando la reproducción o grabación se detiene con el comando [**pausar**](pause.md) ( [**MCI \_ PAUSE**](mci-pause.md)).</span><span class="sxs-lookup"><span data-stu-id="823d5-136">MCI also does not send MCI\_NOTIFY\_ABORTED when playback or recording is paused with the [**pause**](pause.md) ( [**MCI\_PAUSE**](mci-pause.md)) command.</span></span> <span data-ttu-id="823d5-137">El envío del comando de [**reanudación**](resume.md) ( [**\_ reanudación de MCI**](mci-resume.md)) permite que sigan cumpliendo las condiciones de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="823d5-137">Sending the [**resume**](resume.md) ( [**MCI\_RESUME**](mci-resume.md)) command allows them to continue to meet the callback conditions.</span></span>

<span data-ttu-id="823d5-138">Cuando la aplicación solicite una notificación para un comando, compruebe el error devuelto por las funciones [**mciSendString**](/previous-versions//dd757161(v=vs.85)) o [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="823d5-138">When your application requests notification for a command, check the error return of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) or [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) functions.</span></span> <span data-ttu-id="823d5-139">Si estas funciones encuentran un error y devuelven un valor distinto de cero, MCI no establecerá la notificación para el comando.</span><span class="sxs-lookup"><span data-stu-id="823d5-139">If these functions encounter an error and return a nonzero value, MCI will not set notification for the command.</span></span>

## <a name="requirements"></a><span data-ttu-id="823d5-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="823d5-140">Requirements</span></span>



| <span data-ttu-id="823d5-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="823d5-141">Requirement</span></span> | <span data-ttu-id="823d5-142">Value</span><span class="sxs-lookup"><span data-stu-id="823d5-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="823d5-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="823d5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="823d5-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="823d5-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="823d5-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="823d5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="823d5-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="823d5-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="823d5-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="823d5-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="823d5-148"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="823d5-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="823d5-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="823d5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="823d5-150">MCI</span><span class="sxs-lookup"><span data-stu-id="823d5-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="823d5-151">Mensajes de MCI</span><span class="sxs-lookup"><span data-stu-id="823d5-151">MCI Messages</span></span>](mci-messages.md)
</dt> <dt>

[<span data-ttu-id="823d5-152">**temporalmente**</span><span class="sxs-lookup"><span data-stu-id="823d5-152">**pause**</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="823d5-153">**reproducción**</span><span class="sxs-lookup"><span data-stu-id="823d5-153">**play**</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="823d5-154">**registro**</span><span class="sxs-lookup"><span data-stu-id="823d5-154">**record**</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="823d5-155">**Recuper**</span><span class="sxs-lookup"><span data-stu-id="823d5-155">**resume**</span></span>](resume.md)
</dt> <dt>

[<span data-ttu-id="823d5-156">**desean**</span><span class="sxs-lookup"><span data-stu-id="823d5-156">**seek**</span></span>](seek.md)
</dt> </dl>

 

