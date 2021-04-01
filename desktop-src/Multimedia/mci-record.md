---
title: Comando MCI_RECORD (mmsystem. h)
description: El \_ comando MCI record inicia la grabación desde la posición actual o desde una ubicación especificada hasta otra ubicación especificada.
ms.assetid: d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02
keywords:
- Comando de MCI_RECORD de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_RECORD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cd15974753b8f40abd87b8d93622c090e2a57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150396"
---
# <a name="mci_record-command"></a><span data-ttu-id="34eeb-104">\_Comando MCI record</span><span class="sxs-lookup"><span data-stu-id="34eeb-104">MCI\_RECORD command</span></span>

<span data-ttu-id="34eeb-105">El comando [**MCI \_ Record**](mci-record-parms.md) inicia la grabación desde la posición actual o desde una ubicación especificada hasta otra ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="34eeb-105">The [**MCI\_RECORD**](mci-record-parms.md) command starts recording from the current position or from one specified location to another specified location.</span></span> <span data-ttu-id="34eeb-106">Los dispositivos VCR y de onda-audio reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="34eeb-106">VCR and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="34eeb-107">Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo implementan.</span><span class="sxs-lookup"><span data-stu-id="34eeb-107">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="34eeb-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="34eeb-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RECORD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_RECORD_PARMS) lpRecord
);
```



## <a name="parameters"></a><span data-ttu-id="34eeb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34eeb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34eeb-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="34eeb-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="34eeb-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="34eeb-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="34eeb-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="34eeb-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="34eeb-113">MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="34eeb-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="34eeb-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="34eeb-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="34eeb-115"><span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*</span><span class="sxs-lookup"><span data-stu-id="34eeb-115"><span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*</span></span>
</dt> <dd>

<span data-ttu-id="34eeb-116">Puntero a una [**estructura \_ \_ parms del registro MCI**](mci-record-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="34eeb-116">Pointer to an [**MCI\_RECORD\_PARMS**](mci-record-parms.md) structure.</span></span> <span data-ttu-id="34eeb-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="34eeb-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34eeb-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34eeb-118">Return Value</span></span>

<span data-ttu-id="34eeb-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="34eeb-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="34eeb-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34eeb-120">Remarks</span></span>

<span data-ttu-id="34eeb-121">Este comando es compatible con los dispositivos que devuelven **true** cuando se llama al comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con el \_ marcador MCI GETDEVCAPS \_ Can \_ Record.</span><span class="sxs-lookup"><span data-stu-id="34eeb-121">This command is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_CAN\_RECORD flag.</span></span> <span data-ttu-id="34eeb-122">En el caso del controlador MCIWAVE, todos los datos registrados después de abrir un archivo se descartan si el archivo se cierra sin guardarlo.</span><span class="sxs-lookup"><span data-stu-id="34eeb-122">For the MCIWAVE driver, all data recorded after a file is opened is discarded if the file is closed without saving it.</span></span>

<span data-ttu-id="34eeb-123">Las siguientes marcas adicionales se aplican a todos los dispositivos que admiten el registro de MCI \_ :</span><span class="sxs-lookup"><span data-stu-id="34eeb-123">The following additional flags apply to all devices supporting MCI\_RECORD:</span></span>

<dl> <dt>

<span data-ttu-id="34eeb-124"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ desde</span><span class="sxs-lookup"><span data-stu-id="34eeb-124"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="34eeb-125">Una ubicación de inicio se incluye en el miembro **dwFrom** de la estructura identificada por *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="34eeb-125">A starting location is included in the **dwFrom** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="34eeb-126">Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI del comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="34eeb-126">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="34eeb-127">Si \_ no se especifica MCI desde, la ubicación inicial toma como valor predeterminado la posición actual.</span><span class="sxs-lookup"><span data-stu-id="34eeb-127">If MCI\_FROM is not specified, the starting location defaults to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="34eeb-128"><span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>\_inserción de registros MCI \_</span><span class="sxs-lookup"><span data-stu-id="34eeb-128"><span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>MCI\_RECORD\_INSERT</span></span>
</dt> <dd>

<span data-ttu-id="34eeb-129">La información que se acaba de grabar se debe insertar o pegar en los datos existentes.</span><span class="sxs-lookup"><span data-stu-id="34eeb-129">Newly recorded information should be inserted or pasted into the existing data.</span></span> <span data-ttu-id="34eeb-130">Es posible que algunos dispositivos no lo admitan.</span><span class="sxs-lookup"><span data-stu-id="34eeb-130">Some devices might not support this.</span></span> <span data-ttu-id="34eeb-131">Si se admite, este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="34eeb-131">If supported, this is the default.</span></span>

</dd> <dt>

<span data-ttu-id="34eeb-132"><span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>\_sobrescritura del registro de MCI \_</span><span class="sxs-lookup"><span data-stu-id="34eeb-132"><span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>MCI\_RECORD\_OVERWRITE</span></span>
</dt> <dd>

<span data-ttu-id="34eeb-133">Los datos deben sobrescribir los datos existentes.</span><span class="sxs-lookup"><span data-stu-id="34eeb-133">Data should overwrite existing data.</span></span> <span data-ttu-id="34eeb-134">MCIWAVE. El dispositivo DRV devuelve \_ la función no admitida MCIERR \_ en respuesta a esta marca.</span><span class="sxs-lookup"><span data-stu-id="34eeb-134">The MCIWAVE.DRV device returns MCIERR\_UNSUPPORTED\_FUNCTION in response to this flag.</span></span>

</dd> <dt>

<span data-ttu-id="34eeb-135"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a</span><span class="sxs-lookup"><span data-stu-id="34eeb-135"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="34eeb-136">Una ubicación final se incluye en el miembro **dwTo** de la estructura identificada por *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="34eeb-136">An ending location is included in the **dwTo** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="34eeb-137">Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI del comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="34eeb-137">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="34eeb-138">Si \_ no se especifica MCI en, la ubicación final toma como valor predeterminado el final del contenido.</span><span class="sxs-lookup"><span data-stu-id="34eeb-138">If MCI\_TO is not specified, the ending location defaults to the end of the content.</span></span>

</dd> </dl>

<span data-ttu-id="34eeb-139">Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:</span><span class="sxs-lookup"><span data-stu-id="34eeb-139">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="34eeb-140"><span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>\_secuencia de \_ audio de registro DGV \_ de MCI \_</span><span class="sxs-lookup"><span data-stu-id="34eeb-140"><span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>MCI\_DGV\_RECORD\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="34eeb-141">Un número de secuencia de audio se incluye en el miembro **dwAudioStream** de la estructura identificada por *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="34eeb-141">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="34eeb-142">Si omite esta marca, los datos de audio se registran en la primera secuencia física.</span><span class="sxs-lookup"><span data-stu-id="34eeb-142">If you omit this flag, audio data is recorded into the first physical stream.</span></span>

</dd> <dt>

<span data-ttu-id="34eeb-143"><span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>retención de registro de MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="34eeb-143"><span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>MCI\_DGV\_RECORD\_HOLD</span></span>
</dt> <dd>

<span data-ttu-id="34eeb-144">Cuando se detiene la grabación, la pantalla contendrá la última imagen y no se reanudará mostrando el vídeo hasta que se emita un comando del [ \_ monitor MCI](mci-monitor.md) .</span><span class="sxs-lookup"><span data-stu-id="34eeb-144">When recording stops, the screen will hold the last image and will not resume showing the video until an [MCI\_MONITOR](mci-monitor.md) command is issued.</span></span>

</dd> <dt>

<span data-ttu-id="34eeb-145"><span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>\_secuencia de \_ vídeo de registro \_ \_ de MCI DGV</span><span class="sxs-lookup"><span data-stu-id="34eeb-145"><span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>MCI\_DGV\_RECORD\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="34eeb-146">Un número de secuencia de vídeo se incluye en el miembro **dwVideoStream** de la estructura identificada por *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="34eeb-146">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="34eeb-147">Si omite esta marca, los datos de vídeo se registran en la primera secuencia física.</span><span class="sxs-lookup"><span data-stu-id="34eeb-147">If you omit this flag, video data is recorded into the first physical stream.</span></span>

</dd> <dt>

<span data-ttu-id="34eeb-148"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV \_ Rect</span><span class="sxs-lookup"><span data-stu-id="34eeb-148"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="34eeb-149">Se especifica un rectángulo en el miembro **RC** de la estructura identificada por *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="34eeb-149">A rectangle is specified in the **rc** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="34eeb-150">El rectángulo especifica la región de la entrada externa usada como origen para los píxeles comprimidos y guardados.</span><span class="sxs-lookup"><span data-stu-id="34eeb-150">The rectangle specifies the region of the external input used as the source for the pixels compressed and saved.</span></span> <span data-ttu-id="34eeb-151">Este rectángulo tiene como valor predeterminado el rectángulo especificado (o predeterminado) por la \_ \_ \_ marca de vídeo de DGV de MCI Put para el comando [MCI \_ Put](mci-put.md) .</span><span class="sxs-lookup"><span data-stu-id="34eeb-151">This rectangle defaults to the rectangle specified (or defaulted) by the MCI\_DGV\_PUT\_VIDEO flag for the [MCI\_PUT](mci-put.md) command.</span></span> <span data-ttu-id="34eeb-152">Cuando se establece de manera diferente que el rectángulo de vídeo, lo que se muestra no es lo que se registra</span><span class="sxs-lookup"><span data-stu-id="34eeb-152">When it is set differently than the video rectangle, what is displayed is not what is recorded</span></span>

</dd> </dl>

<span data-ttu-id="34eeb-153">En el caso de los dispositivos de vídeo digital, *lpRecord* apunta a una estructura [**parms de \_ \_ Registro \_ MCI DGV**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) .</span><span class="sxs-lookup"><span data-stu-id="34eeb-153">For digital-video devices, *lpRecord* points to an [**MCI\_DGV\_RECORD\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) structure.</span></span>

<span data-ttu-id="34eeb-154">Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="34eeb-154">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="34eeb-155"><span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>\_ \_ grabación de VCR MCI \_ en</span><span class="sxs-lookup"><span data-stu-id="34eeb-155"><span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>MCI\_VCR\_RECORD\_AT</span></span>
</dt> <dd>

<span data-ttu-id="34eeb-156">El miembro **dwAt** de la estructura identificada por *lpRecord* contiene la hora a la que comienza el comando completo, o bien, si el dispositivo está preparado, cuando el dispositivo llega a la posición a partir del comando CUE.</span><span class="sxs-lookup"><span data-stu-id="34eeb-156">The **dwAt** member of the structure identified by *lpRecord* contains a time when the entire command begins, or if the device is cued, when the device reaches the from position given by the cue command.</span></span>

</dd> <dt>

<span data-ttu-id="34eeb-157"><span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>\_ \_ inicialización del registro de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="34eeb-157"><span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>MCI\_VCR\_RECORD\_INITIALIZE</span></span>
</dt> <dd>

<span data-ttu-id="34eeb-158">Busque el dispositivo en el principio del medio, empiece a grabar vídeo y audio en blanco y grabe el código de tiempo, si es posible.</span><span class="sxs-lookup"><span data-stu-id="34eeb-158">Seek the device to the start of the media, begin recording blank video and audio, and record timecode, if possible.</span></span>

</dd> </dl>

<span data-ttu-id="34eeb-159">En el caso de los dispositivos VCR, *lpRecord* apunta a una estructura [**\_ \_ \_ parms de registro VCR de MCI**](mci-vcr-record-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="34eeb-159">For VCR devices, *lpRecord* points to an [**MCI\_VCR\_RECORD\_PARMS**](mci-vcr-record-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="34eeb-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34eeb-160">Requirements</span></span>



| <span data-ttu-id="34eeb-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="34eeb-161">Requirement</span></span> | <span data-ttu-id="34eeb-162">Value</span><span class="sxs-lookup"><span data-stu-id="34eeb-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34eeb-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34eeb-163">Minimum supported client</span></span><br/> | <span data-ttu-id="34eeb-164">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="34eeb-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="34eeb-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34eeb-165">Minimum supported server</span></span><br/> | <span data-ttu-id="34eeb-166">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="34eeb-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="34eeb-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34eeb-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="34eeb-168"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34eeb-168"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34eeb-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="34eeb-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34eeb-170">MCI</span><span class="sxs-lookup"><span data-stu-id="34eeb-170">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="34eeb-171">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="34eeb-171">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

