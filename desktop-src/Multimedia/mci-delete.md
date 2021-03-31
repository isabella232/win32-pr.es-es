---
title: Comando MCI_DELETE (mmsystem. h)
description: El \_ comando de eliminación de MCI quita los datos del archivo. Los dispositivos de audio digital y de onda-vídeo reconocen este comando.
ms.assetid: cf7fae86-e81e-4006-9755-fd01f81aeb62
keywords:
- Comando de MCI_DELETE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_DELETE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c1b9f81712c842e06085c323ca2110c8e06784
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996701"
---
# <a name="mci_delete-command"></a><span data-ttu-id="033db-105">Comando de eliminación de MCI \_</span><span class="sxs-lookup"><span data-stu-id="033db-105">MCI\_DELETE command</span></span>

<span data-ttu-id="033db-106">El \_ comando de eliminación de MCI quita los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="033db-106">The MCI\_DELETE command removes data from the file.</span></span> <span data-ttu-id="033db-107">Los dispositivos de audio digital y de onda-vídeo reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="033db-107">Digital-video and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="033db-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="033db-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_DELETE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDelete
);
```



## <a name="parameters"></a><span data-ttu-id="033db-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="033db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="033db-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="033db-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="033db-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="033db-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="033db-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="033db-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="033db-113">\_La notificación de MCI, la espera de MCI \_ o, para dispositivos de vídeo digital, la prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="033db-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="033db-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="033db-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="033db-115"><span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*</span><span class="sxs-lookup"><span data-stu-id="033db-115"><span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*</span></span>
</dt> <dd>

<span data-ttu-id="033db-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="033db-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="033db-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="033db-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="033db-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="033db-118">Return Value</span></span>

<span data-ttu-id="033db-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="033db-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="033db-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="033db-120">Remarks</span></span>

<span data-ttu-id="033db-121">Las marcas siguientes se aplican al tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="033db-121">The following flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="033db-122"><span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI \_ DGV \_ eliminar \_ en</span><span class="sxs-lookup"><span data-stu-id="033db-122"><span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI\_DGV\_DELETE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="033db-123">Se incluye un rectángulo en el miembro **RC** de la estructura identificada por *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="033db-123">A rectangle is included in the **rc** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="033db-124">El rectángulo especifica la parte de cada fotograma que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="033db-124">The rectangle specifies the portion of each frame to delete.</span></span> <span data-ttu-id="033db-125">Cuando se usa esta marca, el marco se conserva en el área de trabajo y el área especificada por el rectángulo se vuelve negra.</span><span class="sxs-lookup"><span data-stu-id="033db-125">When this flag is used, the frame is retained in the workspace and the area specified by the rectangle becomes black.</span></span> <span data-ttu-id="033db-126">Si se omite la marca, la \_ eliminación de los valores predeterminados de MCI es todo el marco y quita el marco del área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="033db-126">If the flag is omitted, MCI\_DELETE defaults to the entire frame and removes the frame from the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="033db-127"><span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI \_ DGV \_ eliminar \_ secuencia de audio \_</span><span class="sxs-lookup"><span data-stu-id="033db-127"><span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI\_DGV\_DELETE\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="033db-128">Un número de secuencia de audio se incluye en el miembro **dwAudioStream** de la estructura identificada por *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="033db-128">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="033db-129">Si usa esta marca y también quiere eliminar vídeo, también debe usar la \_ marca MCI DGV \_ Delete \_ video \_ Stream.</span><span class="sxs-lookup"><span data-stu-id="033db-129">If you use this flag and also want to delete video, you must also use the MCI\_DGV\_DELETE\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="033db-130">(Si no se especifica ninguna marca, se eliminarán los datos de todas las secuencias de audio y vídeo).</span><span class="sxs-lookup"><span data-stu-id="033db-130">(If neither flag is specified, data from all audio and video streams is deleted.)</span></span>

</dd> <dt>

<span data-ttu-id="033db-131"><span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>\_secuencia de \_ vídeo de eliminación de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="033db-131"><span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>MCI\_DGV\_DELETE\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="033db-132">Un número de secuencia de vídeo se incluye en el miembro **dwVideoStream** de la estructura identificada por *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="033db-132">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="033db-133">Si usa esta marca y también quiere eliminar audio, también debe usar la \_ marca MCI DGV \_ Delete \_ audio \_ Stream.</span><span class="sxs-lookup"><span data-stu-id="033db-133">If you use this flag and also want to delete audio, you must also use the MCI\_DGV\_DELETE\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="033db-134">(Si no se especifica ninguna marca, se eliminarán los datos de todas las secuencias de audio y vídeo).</span><span class="sxs-lookup"><span data-stu-id="033db-134">(If neither flag is specified, data from all audio and video streams is deleted.)</span></span>

</dd> <dt>

<span data-ttu-id="033db-135"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ desde</span><span class="sxs-lookup"><span data-stu-id="033db-135"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="033db-136">Una ubicación de inicio se incluye en el miembro **dwFrom** de la estructura identificada por *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="033db-136">A starting location is included in the **dwFrom** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="033db-137">Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI del comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="033db-137">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="033db-138"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a</span><span class="sxs-lookup"><span data-stu-id="033db-138"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="033db-139">Una ubicación final se incluye en el miembro **dwTo** de la estructura identificada por *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="033db-139">An ending location is included in the **dwTo** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="033db-140">Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI de MCI \_ set.</span><span class="sxs-lookup"><span data-stu-id="033db-140">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

<span data-ttu-id="033db-141">En el caso de los dispositivos de vídeo digital, el parámetro *lpDelete* apunta a una estructura [**MCI \_ DGV \_ Delete \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) .</span><span class="sxs-lookup"><span data-stu-id="033db-141">For digital-video devices, the *lpDelete* parameter points to an [**MCI\_DGV\_DELETE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) structure.</span></span>

<span data-ttu-id="033db-142">Las marcas siguientes se aplican al tipo de dispositivo **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="033db-142">The following flags apply to the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="033db-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ desde</span><span class="sxs-lookup"><span data-stu-id="033db-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="033db-144">Una ubicación de inicio se incluye en el miembro **dwFrom** de la estructura identificada por *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="033db-144">A starting location is included in the **dwFrom** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="033db-145">Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI de [MCI \_ set](mci-set.md).</span><span class="sxs-lookup"><span data-stu-id="033db-145">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of [MCI\_SET](mci-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="033db-146"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a</span><span class="sxs-lookup"><span data-stu-id="033db-146"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="033db-147">Una ubicación final se incluye en el miembro **dwTo** de la estructura identificada por *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="033db-147">An ending location is included in the **dwTo** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="033db-148">Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI de MCI \_ set.</span><span class="sxs-lookup"><span data-stu-id="033db-148">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

<span data-ttu-id="033db-149">En el caso de los dispositivos de audio de onda, el parámetro *lpDelete* apunta a una estructura parms de la [**\_ \_ eliminación \_ de onda MCI**](mci-wave-delete-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="033db-149">For waveform-audio devices, the *lpDelete* parameter points to an [**MCI\_WAVE\_DELETE\_PARMS**](mci-wave-delete-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="033db-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="033db-150">Requirements</span></span>



| <span data-ttu-id="033db-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="033db-151">Requirement</span></span> | <span data-ttu-id="033db-152">Value</span><span class="sxs-lookup"><span data-stu-id="033db-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="033db-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="033db-153">Minimum supported client</span></span><br/> | <span data-ttu-id="033db-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="033db-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="033db-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="033db-155">Minimum supported server</span></span><br/> | <span data-ttu-id="033db-156">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="033db-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="033db-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="033db-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="033db-158"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="033db-158"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="033db-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="033db-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="033db-160">MCI</span><span class="sxs-lookup"><span data-stu-id="033db-160">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="033db-161">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="033db-161">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

