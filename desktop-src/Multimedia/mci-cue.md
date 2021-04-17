---
title: Comando MCI_CUE (mmsystem. h)
description: El \_ comando MCI CUE señala un dispositivo para que la reproducción o grabación comience con un retraso mínimo. Los dispositivos de audio digital-vídeo, VCR y de onda y de onda reconocen este comando.
ms.assetid: 22da4a84-a7af-42df-b950-8d1184fff9ba
keywords:
- Comando de MCI_CUE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_CUE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8463c68f304fe216049568e0df518cbe1d0090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676862"
---
# <a name="mci_cue-command"></a><span data-ttu-id="ee9ce-105">\_Comando MCI CUE</span><span class="sxs-lookup"><span data-stu-id="ee9ce-105">MCI\_CUE command</span></span>

<span data-ttu-id="ee9ce-106">El \_ comando MCI CUE señala un dispositivo para que la reproducción o grabación comience con un retraso mínimo.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-106">The MCI\_CUE command cues a device so that playback or recording begins with minimum delay.</span></span> <span data-ttu-id="ee9ce-107">Los dispositivos de audio digital-vídeo, VCR y de onda y de onda reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-107">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="ee9ce-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpCue
);
```



## <a name="parameters"></a><span data-ttu-id="ee9ce-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee9ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee9ce-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ee9ce-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ee9ce-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ee9ce-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ee9ce-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ee9ce-113">MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="ee9ce-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="ee9ce-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ee9ce-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee9ce-115"><span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*</span><span class="sxs-lookup"><span data-stu-id="ee9ce-115"><span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*</span></span>
</dt> <dd>

<span data-ttu-id="ee9ce-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ee9ce-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="ee9ce-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="ee9ce-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee9ce-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee9ce-118">Return Value</span></span>

<span data-ttu-id="ee9ce-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee9ce-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee9ce-120">Remarks</span></span>

<span data-ttu-id="ee9ce-121">Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:</span><span class="sxs-lookup"><span data-stu-id="ee9ce-121">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ee9ce-122"><span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>\_entrada de \_ indicación MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="ee9ce-122"><span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>MCI\_DGV\_CUE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="ee9ce-123">Una instancia de vídeo digital debe prepararse para la grabación.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-123">A digital-video instance should prepare for recording.</span></span> <span data-ttu-id="ee9ce-124">Si la aplicación no ha reservado espacio en disco, el dispositivo reserva el espacio en disco con sus parámetros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-124">If the application has not reserved disk space, the device reserves the disk space using its default parameters.</span></span> <span data-ttu-id="ee9ce-125">La aplicación puede omitir esta marca si el origen de presentación actual ya es la entrada externa.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-125">The application can omit this flag if the current presentation source is already the external input.</span></span> <span data-ttu-id="ee9ce-126">(Esta marca no tiene ningún efecto en la selección del origen de presentación).</span><span class="sxs-lookup"><span data-stu-id="ee9ce-126">(This flag has no effect on selecting the presentation source.)</span></span>

</dd> <dt>

<span data-ttu-id="ee9ce-127"><span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>DGV de la señal de MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ee9ce-127"><span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>MCI\_DGV\_CUE\_NOSHOW</span></span>
</dt> <dd>

<span data-ttu-id="ee9ce-128">Una instancia de vídeo digital debe prepararse para reproducir el marco especificado con el comando sin mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-128">A digital-video instance should prepare for playing the frame specified with the command without displaying it.</span></span> <span data-ttu-id="ee9ce-129">Cuando se especifica esta marca, la pantalla continúa mostrando la imagen en el búfer de fotogramas aunque su fotograma correspondiente no sea la posición actual.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-129">When this flag is specified, the display continues to show the image in the frame buffer even though its corresponding frame is not the current position.</span></span> <span data-ttu-id="ee9ce-130">Por ejemplo, si el búfer de fotogramas contiene la imagen del fotograma 7, el dispositivo continúa mostrando el fotograma 7 cuando se usa esta marca para señalar el dispositivo a cualquier otra posición.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-130">For example, if the frame buffer contains the image from frame 7, the device continues to show frame 7 when this flag is used to cue the device to any other position.</span></span> <span data-ttu-id="ee9ce-131">Un comando de pila subsiguiente sin esta marca y sin la \_ marca MCI to muestra el marco actual.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-131">A subsequent cue command without this flag and without the MCI\_TO flag displays the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="ee9ce-132"><span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>salida de indicación de MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="ee9ce-132"><span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>MCI\_DGV\_CUE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="ee9ce-133">Una instancia de vídeo digital debe prepararse para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-133">A digital-video instance should prepare for playing.</span></span> <span data-ttu-id="ee9ce-134">Si el área de trabajo está en pausa, no se produce ninguna posición.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-134">If the workspace is paused, no positioning occurs.</span></span> <span data-ttu-id="ee9ce-135">Si el área de trabajo está detenida, la posición puede cambiar a una imagen de fotograma clave anterior.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-135">If the workspace is stopped, the position might change to a previous key-frame image.</span></span> <span data-ttu-id="ee9ce-136">La aplicación puede omitir esta marca si el origen de presentación actual ya es el área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-136">The application can omit this flag if the current presentation source is already the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="ee9ce-137"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a</span><span class="sxs-lookup"><span data-stu-id="ee9ce-137"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="ee9ce-138">Una posición en el área de trabajo se incluye en el miembro **dwTo** de la estructura identificada por *lpCue*.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-138">A workspace position is included in the **dwTo** member of the structure identified by *lpCue*.</span></span> <span data-ttu-id="ee9ce-139">Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo de conjunto de MCI del comando [ \_ set de MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="ee9ce-139">The units assigned to position values are specified using the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="ee9ce-140">Esto es equivalente a buscar en una posición, excepto que el dispositivo se pausa después del comando.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-140">This is equivalent to seeking to a position, except the device is paused after the command.</span></span>

</dd> </dl>

<span data-ttu-id="ee9ce-141">En el caso de los dispositivos **DigitalVideo** , el parámetro *lpCue* apunta a una estructura de parms de DGV de la [**\_ \_ señal \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) .</span><span class="sxs-lookup"><span data-stu-id="ee9ce-141">For **digitalvideo** devices, the *lpCue* parameter points to an [**MCI\_DGV\_CUE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) structure.</span></span>

<span data-ttu-id="ee9ce-142">Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="ee9ce-142">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ee9ce-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ desde</span><span class="sxs-lookup"><span data-stu-id="ee9ce-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="ee9ce-144">El miembro **dwFrom** de la estructura a la que apunta *lpCue* contiene la ubicación de inicio especificada en el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-144">The **dwFrom** member of the structure pointed to by *lpCue* contains the starting location specified in the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="ee9ce-145"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a</span><span class="sxs-lookup"><span data-stu-id="ee9ce-145"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="ee9ce-146">El miembro **dwTo** de la estructura a la que apunta *lpCue* contiene la ubicación final (en pausa) especificada en el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-146">The **dwTo** member of the structure pointed to by *lpCue* contains the ending (pausing) location specified in the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="ee9ce-147"><span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>\_entrada de \_ pista de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="ee9ce-147"><span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>MCI\_VCR\_CUE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="ee9ce-148">Preparación para la grabación.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-148">Prepare for recording.</span></span>

</dd> <dt>

<span data-ttu-id="ee9ce-149"><span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>salida de la señal de VCR de MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ee9ce-149"><span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>MCI\_VCR\_CUE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="ee9ce-150">Preparación para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-150">Prepare for playing.</span></span> <span data-ttu-id="ee9ce-151">Si \_ \_ \_ no se especifica ninguna entrada de pila de VCR de MCI ni \_ \_ salida de señal de VCR MCI \_ , \_ \_ se presupone la salida de la señal de VCR de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="ee9ce-151">If neither MCI\_VCR\_CUE\_INPUT nor MCI\_VCR\_CUE\_OUTPUT is specified, MCI\_VCR\_CUE\_OUTPUT is assumed.</span></span>

</dd> <dt>

<span data-ttu-id="ee9ce-152"><span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>prelanzamiento de pista de VCR de MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ee9ce-152"><span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>MCI\_VCR\_CUE\_PREROLL</span></span>
</dt> <dd>

<span data-ttu-id="ee9ce-153">Señale el dispositivo a la posición actual, o la posición **dwFrom** , menos la duración del preroll.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-153">Cue the device to the current position, or the **dwFrom** position, minus the preroll duration.</span></span> <span data-ttu-id="ee9ce-154">Esto permitirá que el dispositivo se prepare antes de entrar en el modo de grabación o reproducción.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-154">This will allow the device to prepare itself before entering record or playback mode.</span></span>

</dd> <dt>

<span data-ttu-id="ee9ce-155"><span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>pista de VCR de MCI \_ \_ \_ inverso</span><span class="sxs-lookup"><span data-stu-id="ee9ce-155"><span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>MCI\_VCR\_CUE\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="ee9ce-156">La dirección del comando siguiente reproducir o grabar es inversa.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-156">The direction of the next play or record command is reverse.</span></span>

</dd> </dl>

<span data-ttu-id="ee9ce-157">Cuando cueing para la reproducción mediante el uso del \_ comando MCI CUE con la marca de salida de la \_ señal de VCR MCI \_ \_ , puede cancelar \_ la pila de MCI emitiendo el comando de [ \_ reproducción de MCI](mci-play.md) con MCI \_ de, MCI \_ a o MCI \_ VCR \_ Play \_ REVERSE.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-157">When cueing for playback by using the MCI\_CUE command with the MCI\_VCR\_CUE\_OUTPUT flag, you can cancel MCI\_CUE by issuing the [MCI\_PLAY](mci-play.md) command with MCI\_FROM, MCI\_TO, or MCI\_VCR\_PLAY\_REVERSE.</span></span>

<span data-ttu-id="ee9ce-158">Cuando cueing para la grabación mediante el uso de \_ la señal de MCI con la marca de entrada de vídeo de MCI \_ \_ \_ , puede cancelar \_ la señal de MCI emitiendo el comando [MCI \_ Record](mci-record.md) con MCI \_ de, MCI \_ a o el registro de VCR de MCI \_ \_ \_ Initialize.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-158">When cueing for recording by using MCI\_CUE with the MCI\_VCR\_CUE\_INPUT flag, you can cancel MCI\_CUE by issuing the [MCI\_RECORD](mci-record.md) command with MCI\_FROM, MCI\_TO, or MCI\_VCR\_RECORD\_INITIALIZE.</span></span>

<span data-ttu-id="ee9ce-159">En el caso de los dispositivos **VCR** , el parámetro *lpCue* apunta a una estructura [**MCI \_ VCR \_ CUE \_ parms**](mci-vcr-cue-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ee9ce-159">For **vcr** devices, the *lpCue* parameter points to an [**MCI\_VCR\_CUE\_PARMS**](mci-vcr-cue-parms.md) structure.</span></span>

<span data-ttu-id="ee9ce-160">Con el tipo de dispositivo **WaveAudio** se usan las siguientes marcas adicionales:</span><span class="sxs-lookup"><span data-stu-id="ee9ce-160">The following additional flags are used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ee9ce-161"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrada de onda de MCI \_</span><span class="sxs-lookup"><span data-stu-id="ee9ce-161"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="ee9ce-162">Un dispositivo de entrada de onda-audio debe estar preparado.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-162">A waveform-audio input device should be cued.</span></span>

</dd> <dt>

<span data-ttu-id="ee9ce-163"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_salida de onda de MCI \_</span><span class="sxs-lookup"><span data-stu-id="ee9ce-163"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="ee9ce-164">Un dispositivo de salida de onda-audio debe estar preparado.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-164">A waveform-audio output device should be cued.</span></span> <span data-ttu-id="ee9ce-165">Esta es la marca predeterminada si no se especifica una marca.</span><span class="sxs-lookup"><span data-stu-id="ee9ce-165">This is the default flag if a flag is not specified.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee9ce-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee9ce-166">Requirements</span></span>



| <span data-ttu-id="ee9ce-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee9ce-167">Requirement</span></span> | <span data-ttu-id="ee9ce-168">Value</span><span class="sxs-lookup"><span data-stu-id="ee9ce-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee9ce-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee9ce-169">Minimum supported client</span></span><br/> | <span data-ttu-id="ee9ce-170">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ee9ce-170">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ee9ce-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee9ce-171">Minimum supported server</span></span><br/> | <span data-ttu-id="ee9ce-172">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ee9ce-172">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ee9ce-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee9ce-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee9ce-174"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee9ce-174"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee9ce-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee9ce-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee9ce-176">MCI</span><span class="sxs-lookup"><span data-stu-id="ee9ce-176">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ee9ce-177">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="ee9ce-177">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

