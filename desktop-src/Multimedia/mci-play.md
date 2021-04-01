---
title: Comando MCI_PLAY (mmsystem. h)
description: El \_ comando MCI Play indica al dispositivo que empiece a transmitir los datos de salida. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, Videodisc, VCR y de onda-audio reconocen este comando.
ms.assetid: d912ab49-63f0-40a9-aa4c-f9463782b54c
keywords:
- Comando de MCI_PLAY de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_PLAY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f985a8d5d6be7ad42702afc898b3aaf437ef320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905660"
---
# <a name="mci_play-command"></a><span data-ttu-id="26a25-105">Comando de reproducción de MCI \_</span><span class="sxs-lookup"><span data-stu-id="26a25-105">MCI\_PLAY command</span></span>

<span data-ttu-id="26a25-106">El \_ comando MCI Play indica al dispositivo que empiece a transmitir los datos de salida.</span><span class="sxs-lookup"><span data-stu-id="26a25-106">The MCI\_PLAY command signals the device to begin transmitting output data.</span></span> <span data-ttu-id="26a25-107">Los dispositivos de audio de CD, digital-video, MIDI Sequencer, Videodisc, VCR y de onda-audio reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="26a25-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="26a25-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="26a25-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PLAY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_PLAY_PARMS ) lpPlay
);
```



## <a name="parameters"></a><span data-ttu-id="26a25-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26a25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26a25-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="26a25-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="26a25-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="26a25-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="26a25-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="26a25-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="26a25-113">MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="26a25-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="26a25-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="26a25-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="26a25-115"><span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*</span><span class="sxs-lookup"><span data-stu-id="26a25-115"><span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*</span></span>
</dt> <dd>

<span data-ttu-id="26a25-116">Puntero a una estructura de [**\_ \_ parms de reproducción de MCI**](mci-play-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="26a25-116">Pointer to an [**MCI\_PLAY\_PARMS**](mci-play-parms.md) structure.</span></span> <span data-ttu-id="26a25-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="26a25-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26a25-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26a25-118">Return Value</span></span>

<span data-ttu-id="26a25-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="26a25-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="26a25-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26a25-120">Remarks</span></span>

<span data-ttu-id="26a25-121">Las siguientes marcas adicionales se aplican a todos los dispositivos que admiten MCI \_ Play:</span><span class="sxs-lookup"><span data-stu-id="26a25-121">The following additional flags apply to all devices supporting MCI\_PLAY:</span></span>

<dl> <dt>

<span data-ttu-id="26a25-122"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ desde</span><span class="sxs-lookup"><span data-stu-id="26a25-122"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="26a25-123">Una ubicación de inicio se incluye en el miembro **dwFrom** de la estructura identificada por *lpPlay*.</span><span class="sxs-lookup"><span data-stu-id="26a25-123">A starting location is included in the **dwFrom** member of the structure identified by *lpPlay*.</span></span> <span data-ttu-id="26a25-124">Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI del comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="26a25-124">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="26a25-125">Si \_ no se especifica MCI desde, la ubicación inicial toma como valor predeterminado la posición actual.</span><span class="sxs-lookup"><span data-stu-id="26a25-125">If MCI\_FROM is not specified, the starting location defaults to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="26a25-126"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a</span><span class="sxs-lookup"><span data-stu-id="26a25-126"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="26a25-127">Una ubicación final se incluye en el miembro **dwTo** de la estructura identificada por *lpPlay*.</span><span class="sxs-lookup"><span data-stu-id="26a25-127">An ending location is included in the **dwTo** member of the structure identified by *lpPlay*.</span></span> <span data-ttu-id="26a25-128">Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI de MCI \_ set.</span><span class="sxs-lookup"><span data-stu-id="26a25-128">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span> <span data-ttu-id="26a25-129">Si \_ no se especifica MCI en, el valor predeterminado de la ubicación final es el final del medio.</span><span class="sxs-lookup"><span data-stu-id="26a25-129">If MCI\_TO is not specified, the ending location defaults to the end of the media.</span></span>

</dd> </dl>

<span data-ttu-id="26a25-130">Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:</span><span class="sxs-lookup"><span data-stu-id="26a25-130">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="26a25-131"><span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>\_reproducción de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="26a25-131"><span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>MCI\_DGV\_PLAY\_REPEAT</span></span>
</dt> <dd>

<span data-ttu-id="26a25-132">La reproducción debe comenzar de nuevo al principio cuando se alcanza el final del contenido.</span><span class="sxs-lookup"><span data-stu-id="26a25-132">Playback should start again at the beginning when the end of the content is reached.</span></span>

</dd> <dt>

<span data-ttu-id="26a25-133"><span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>MCI \_ DGV \_ Play \_ Reverse</span><span class="sxs-lookup"><span data-stu-id="26a25-133"><span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>MCI\_DGV\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="26a25-134">La reproducción debe realizarse en orden inverso.</span><span class="sxs-lookup"><span data-stu-id="26a25-134">Playback should occur in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="26a25-135"><span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>ventana de reproducción de MCI \_ MCIAVI \_ \_</span><span class="sxs-lookup"><span data-stu-id="26a25-135"><span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>MCI\_MCIAVI\_PLAY\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="26a25-136">La reproducción debe realizarse en la ventana asociada a una instancia de dispositivo (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="26a25-136">Playback should occur in the window associated with a device instance (the default).</span></span> <span data-ttu-id="26a25-137">(Esta marca es específica de MCIAVI. DRV).</span><span class="sxs-lookup"><span data-stu-id="26a25-137">(This flag is specific to MCIAVI.DRV.)</span></span>

</dd> <dt>

<span data-ttu-id="26a25-138"><span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>MCI \_ MCIAVI \_ Play \_ Fullscreen</span><span class="sxs-lookup"><span data-stu-id="26a25-138"><span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>MCI\_MCIAVI\_PLAY\_FULLSCREEN</span></span>
</dt> <dd>

<span data-ttu-id="26a25-139">La reproducción debe usar una presentación en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="26a25-139">Playback should use a full-screen display.</span></span> <span data-ttu-id="26a25-140">Use esta marca solo cuando se reproduzcan archivos comprimidos u de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="26a25-140">Use this flag only when playing compressed or 8-bit files.</span></span>

</dd> </dl>

<span data-ttu-id="26a25-141">En el caso de los dispositivos de vídeo digital, *lpPlay* apunta a una estructura [**MCI \_ DGV \_ Play \_ parms**](/previous-versions//dd743396(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="26a25-141">For digital-video devices, *lpPlay* points to an [**MCI\_DGV\_PLAY\_PARMS**](/previous-versions//dd743396(v=vs.85)) structure.</span></span>

<span data-ttu-id="26a25-142">Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="26a25-142">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="26a25-143"><span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>\_ \_ reproducción de VCR \_ de MCI en</span><span class="sxs-lookup"><span data-stu-id="26a25-143"><span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>MCI\_VCR\_PLAY\_AT</span></span>
</dt> <dd>

<span data-ttu-id="26a25-144">El miembro **dwAt** de la estructura identificada por *lpPlay* contiene la hora a la que comienza el comando completo, o bien, si el dispositivo está preparado, cuando el dispositivo llega a la posición a partir del comando [MCI \_ CUE](mci-cue.md) .</span><span class="sxs-lookup"><span data-stu-id="26a25-144">The **dwAt** member of the structure identified by *lpPlay* contains a time when the entire command begins, or if the device is cued, when the device reaches the from position given by the [MCI\_CUE](mci-cue.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="26a25-145"><span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>reproducción de VCR de MCI \_ \_ \_ inverso</span><span class="sxs-lookup"><span data-stu-id="26a25-145"><span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>MCI\_VCR\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="26a25-146">La reproducción debe realizarse en orden inverso.</span><span class="sxs-lookup"><span data-stu-id="26a25-146">Playback should occur in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="26a25-147"><span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>\_recorrido de \_ reproducción de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="26a25-147"><span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>MCI\_VCR\_PLAY\_SCAN</span></span>
</dt> <dd>

<span data-ttu-id="26a25-148">La reproducción debe ser lo más rápida posible mientras se mantiene la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="26a25-148">Playback should be as fast as possible while maintaining video output.</span></span>

</dd> </dl>

<span data-ttu-id="26a25-149">En el caso de los dispositivos VCR, *lpPlay* apunta a una estructura [**MCI \_ VCR \_ Play \_ parms**](mci-vcr-play-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="26a25-149">For VCR devices, *lpPlay* points to an [**MCI\_VCR\_PLAY\_PARMS**](mci-vcr-play-parms.md) structure.</span></span>

<span data-ttu-id="26a25-150">Se usan las siguientes marcas adicionales con el tipo de dispositivo de **videodisco** :</span><span class="sxs-lookup"><span data-stu-id="26a25-150">The following additional flags are used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="26a25-151"><span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>MCI \_ Vd \_ Play \_ Fast</span><span class="sxs-lookup"><span data-stu-id="26a25-151"><span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>MCI\_VD\_PLAY\_FAST</span></span>
</dt> <dd>

<span data-ttu-id="26a25-152">Reproducción rápida.</span><span class="sxs-lookup"><span data-stu-id="26a25-152">Play fast.</span></span>

</dd> <dt>

<span data-ttu-id="26a25-153"><span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>MCI \_ Vd \_ Play \_ Reverse</span><span class="sxs-lookup"><span data-stu-id="26a25-153"><span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>MCI\_VD\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="26a25-154">Reproducir en orden inverso.</span><span class="sxs-lookup"><span data-stu-id="26a25-154">Play in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="26a25-155"><span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>examen de reproducción de MCI \_ Vd \_ \_</span><span class="sxs-lookup"><span data-stu-id="26a25-155"><span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>MCI\_VD\_PLAY\_SCAN</span></span>
</dt> <dd>

<span data-ttu-id="26a25-156">Digitalice rápidamente.</span><span class="sxs-lookup"><span data-stu-id="26a25-156">Scan quickly.</span></span>

</dd> <dt>

<span data-ttu-id="26a25-157"><span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>MCI \_ Vd \_ play reproducción \_ lenta</span><span class="sxs-lookup"><span data-stu-id="26a25-157"><span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>MCI\_VD\_PLAY\_SLOW</span></span>
</dt> <dd>

<span data-ttu-id="26a25-158">Reproducir lentamente.</span><span class="sxs-lookup"><span data-stu-id="26a25-158">Play slowly.</span></span>

</dd> <dt>

<span data-ttu-id="26a25-159"><span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>velocidad de reproducción de MCI \_ Vd \_ \_</span><span class="sxs-lookup"><span data-stu-id="26a25-159"><span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>MCI\_VD\_PLAY\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="26a25-160">La velocidad de reproducción se incluye en el miembro **dwSpeed** de la estructura identificada por *lpPlay*.</span><span class="sxs-lookup"><span data-stu-id="26a25-160">The play speed is included in the **dwSpeed** member in the structure identified by *lpPlay*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26a25-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26a25-161">Requirements</span></span>



| <span data-ttu-id="26a25-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="26a25-162">Requirement</span></span> | <span data-ttu-id="26a25-163">Value</span><span class="sxs-lookup"><span data-stu-id="26a25-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26a25-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26a25-164">Minimum supported client</span></span><br/> | <span data-ttu-id="26a25-165">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="26a25-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="26a25-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26a25-166">Minimum supported server</span></span><br/> | <span data-ttu-id="26a25-167">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="26a25-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="26a25-168">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26a25-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="26a25-169"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26a25-169"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26a25-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="26a25-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26a25-171">MCI</span><span class="sxs-lookup"><span data-stu-id="26a25-171">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="26a25-172">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="26a25-172">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

