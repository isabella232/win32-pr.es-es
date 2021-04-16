---
title: Comando MCI_SET (mmsystem. h)
description: El \_ comando set de MCI establece la información del dispositivo. Los dispositivos de audio de CD, vídeo digital, secuencia de MIDI, VCR, vídeo, superposición de vídeo y de audio y de onda reconocen este comando.
ms.assetid: c527f9d6-2119-4274-98b7-dc892e9b70f9
keywords:
- Comando de MCI_SET de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SET
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1da0da94c0d970b607a29548c773fa9302d26d
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2021
ms.locfileid: "105678605"
---
# <a name="mci_set-command"></a><span data-ttu-id="2bf70-105">\_Comando MCI set</span><span class="sxs-lookup"><span data-stu-id="2bf70-105">MCI\_SET command</span></span>

> [!NOTE]
> <span data-ttu-id="2bf70-106">Comunicación sin polarización: Microsoft admite un entorno diverso y de inclusión.</span><span class="sxs-lookup"><span data-stu-id="2bf70-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="2bf70-107">Dentro de este documento, hay referencias a la palabra ' Slave '.</span><span class="sxs-lookup"><span data-stu-id="2bf70-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="2bf70-108">La guía de estilo de Microsoft [para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo reconoce como una palabra de exclusión.</span><span class="sxs-lookup"><span data-stu-id="2bf70-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="2bf70-109">Este texto se usa tal como está actualmente el texto que se usa en los comandos.</span><span class="sxs-lookup"><span data-stu-id="2bf70-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="2bf70-110">Para mantener la coherencia, este documento contiene esta palabra.</span><span class="sxs-lookup"><span data-stu-id="2bf70-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="2bf70-111">Cuando se modifique esta palabra en los comandos, se corregirá este documento para que esté alineado.</span><span class="sxs-lookup"><span data-stu-id="2bf70-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="2bf70-112">El \_ comando set de MCI establece la información del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bf70-112">The MCI\_SET command sets device information.</span></span> <span data-ttu-id="2bf70-113">Los dispositivos de audio de CD, vídeo digital, secuencia de MIDI, VCR, vídeo, superposición de vídeo y de audio y de onda reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="2bf70-113">CD audio, digital-video, MIDI sequencer, VCR, videodisc, video-overlay, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="2bf70-114">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="2bf70-114">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SET, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SET_PARMS) lpSet
);
```



## <a name="parameters"></a><span data-ttu-id="2bf70-115">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bf70-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bf70-116"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="2bf70-116"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-117">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="2bf70-117">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-118"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="2bf70-118"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-119">MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="2bf70-119">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="2bf70-120">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="2bf70-120">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-121"><span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*</span><span class="sxs-lookup"><span data-stu-id="2bf70-121"><span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-122">Puntero a una [**estructura \_ \_ parms de set MCI**](mci-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="2bf70-122">Pointer to an [**MCI\_SET\_PARMS**](mci-set-parms.md) structure.</span></span> <span data-ttu-id="2bf70-123">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="2bf70-123">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bf70-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bf70-124">Return Value</span></span>

<span data-ttu-id="2bf70-125">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2bf70-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bf70-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2bf70-126">Remarks</span></span>

<span data-ttu-id="2bf70-127">Las siguientes marcas adicionales se aplican a todos los dispositivos que admiten MCI \_ set:</span><span class="sxs-lookup"><span data-stu-id="2bf70-127">The following additional flags apply to all devices supporting MCI\_SET:</span></span>

<dl> <dt>

<span data-ttu-id="2bf70-128"><span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI \_ set \_ audio</span><span class="sxs-lookup"><span data-stu-id="2bf70-128"><span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI\_SET\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-129">Un número de canal de audio se incluye en el miembro dwAudio de la estructura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="2bf70-129">An audio channel number is included in the dwAudio member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="2bf70-130">Esta marca debe usarse con MCI \_ establecido \_ en o MCI \_ \_ desactivado.</span><span class="sxs-lookup"><span data-stu-id="2bf70-130">This flag must be used with MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="2bf70-131">Use una de las siguientes constantes para indicar el número de canal:</span><span class="sxs-lookup"><span data-stu-id="2bf70-131">Use one of the following constants to indicate the channel number:</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-132"><span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI \_ set \_ audio \_ All</span><span class="sxs-lookup"><span data-stu-id="2bf70-132"><span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI\_SET\_AUDIO\_ALL</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-133">Todos los canales de audio.</span><span class="sxs-lookup"><span data-stu-id="2bf70-133">All audio channels.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-134"><span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI \_ set \_ audio \_ izquierda</span><span class="sxs-lookup"><span data-stu-id="2bf70-134"><span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI\_SET\_AUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-135">Canal izquierdo.</span><span class="sxs-lookup"><span data-stu-id="2bf70-135">Left channel.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-136"><span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI \_ establecer \_ audio a la \_ derecha</span><span class="sxs-lookup"><span data-stu-id="2bf70-136"><span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI\_SET\_AUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-137">Canal derecho.</span><span class="sxs-lookup"><span data-stu-id="2bf70-137">Right channel.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-138"><span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>\_cerrar la \_ puerta del conjunto de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-138"><span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>MCI\_SET\_DOOR\_CLOSED</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-139">Cierra la cubierta multimedia (si existe).</span><span class="sxs-lookup"><span data-stu-id="2bf70-139">Closes the media cover (if any).</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-140"><span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>\_abrir la \_ puerta del conjunto de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-140"><span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>MCI\_SET\_DOOR\_OPEN</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-141">Abre la cubierta multimedia (si existe).</span><span class="sxs-lookup"><span data-stu-id="2bf70-141">Opens the media cover (if any).</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-142"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>Desactivación de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-142"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-143">Deshabilita el canal de audio o vídeo especificado.</span><span class="sxs-lookup"><span data-stu-id="2bf70-143">Disables the specified video or audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-144"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activado \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-144"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-145">Habilita el canal de audio o vídeo especificado.</span><span class="sxs-lookup"><span data-stu-id="2bf70-145">Enables the specified video or audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-146"><span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>\_formato de \_ hora del conjunto de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-146"><span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>MCI\_SET\_TIME\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-147">Un parámetro de formato de hora se incluye en el miembro **dwTimeFormat** de la estructura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="2bf70-147">A time format parameter is included in the **dwTimeFormat** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="2bf70-148">Las marcas siguientes se usan con esta marca:</span><span class="sxs-lookup"><span data-stu-id="2bf70-148">The following flags are used with this flag:</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-149"><span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>\_bytes de formato de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-149"><span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>MCI\_FORMAT\_BYTES</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-150">Dentro de un formato de datos PCM (modulación por pulsos de código), cambia la descripción del miembro de hora a bytes para la entrada o salida.</span><span class="sxs-lookup"><span data-stu-id="2bf70-150">Within a PCM (Pulse Code Modulation) data format, changes the time member description to bytes for input or output.</span></span> <span data-ttu-id="2bf70-151">Reconocido por el tipo de dispositivo **WaveAudio** .</span><span class="sxs-lookup"><span data-stu-id="2bf70-151">Recognized by the **waveaudio** device type.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-152"><span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>\_marcos de formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-152"><span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>MCI\_FORMAT\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-153">Los comandos subsiguientes usarán los marcos.</span><span class="sxs-lookup"><span data-stu-id="2bf70-153">Subsequent commands will use frames.</span></span> <span data-ttu-id="2bf70-154">Reconocido por los tipos de dispositivo **DigitalVideo**, **VCR** y **VideoDisc** .</span><span class="sxs-lookup"><span data-stu-id="2bf70-154">Recognized by the **digitalvideo**, **vcr**, and **videodisc** device types.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-155"><span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>\_formato MCI \_ HMS</span><span class="sxs-lookup"><span data-stu-id="2bf70-155"><span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>MCI\_FORMAT\_HMS</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-156">Cambia el formato de hora a horas, minutos y segundos.</span><span class="sxs-lookup"><span data-stu-id="2bf70-156">Changes the time format to hours, minutes, and seconds.</span></span> <span data-ttu-id="2bf70-157">Reconocido por los tipos de dispositivo **VCR** y **VideoDisc** .</span><span class="sxs-lookup"><span data-stu-id="2bf70-157">Recognized by the **vcr** and **videodisc** device types.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-158"><span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>formato MCI en \_ \_ milisegundos</span><span class="sxs-lookup"><span data-stu-id="2bf70-158"><span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>MCI\_FORMAT\_MILLISECONDS</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-159">Cambia el formato de hora a milisegundos.</span><span class="sxs-lookup"><span data-stu-id="2bf70-159">Changes the time format to milliseconds.</span></span> <span data-ttu-id="2bf70-160">Reconocido por todos los tipos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2bf70-160">Recognized by all device types.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-161"><span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>\_formato MCI \_ MSF</span><span class="sxs-lookup"><span data-stu-id="2bf70-161"><span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>MCI\_FORMAT\_MSF</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-162">Cambia el formato de hora a minutos, segundos y fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2bf70-162">Changes the time format to minutes, seconds, and frames.</span></span> <span data-ttu-id="2bf70-163">Reconocido por los tipos de dispositivo **cdaudio** y **VCR** .</span><span class="sxs-lookup"><span data-stu-id="2bf70-163">Recognized by the **cdaudio** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-164"><span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>\_ejemplos de formato de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-164"><span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>MCI\_FORMAT\_SAMPLES</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-165">Cambia el formato de hora a los ejemplos de entrada o salida.</span><span class="sxs-lookup"><span data-stu-id="2bf70-165">Changes the time format to samples for input or output.</span></span> <span data-ttu-id="2bf70-166">Reconocido por el tipo de dispositivo **WaveAudio** .</span><span class="sxs-lookup"><span data-stu-id="2bf70-166">Recognized by the **waveaudio** device type.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-167"><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>\_Formato MCI \_ SMPTE \_ 24, \_ formato MCI \_ SMPTE \_ 25 y formato MCI \_ \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="2bf70-167"><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>MCI\_FORMAT\_SMPTE\_24, MCI\_FORMAT\_SMPTE\_25, and MCI\_FORMAT\_SMPTE\_30</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-168">Establece el formato de hora en 24, 25 y 30 fotogramas SMPTE (sociedad de los ingenieros de cine y televisión), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2bf70-168">Sets the time format to 24, 25, and 30 frame SMPTE (Society of Motion Picture and Television Engineers), respectively.</span></span> <span data-ttu-id="2bf70-169">Reconocido por los tipos de dispositivo **secuenciador** y **VCR** .</span><span class="sxs-lookup"><span data-stu-id="2bf70-169">Recognized by the **sequencer** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-170"><span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>\_Formato MCI \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="2bf70-170"><span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>MCI\_FORMAT\_SMPTE\_30DROP</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-171">Establece el formato de hora en 30 fotograma eliminado SMPTE.</span><span class="sxs-lookup"><span data-stu-id="2bf70-171">Sets the time format to 30 drop-frame SMPTE.</span></span> <span data-ttu-id="2bf70-172">Reconocido por los tipos de dispositivo **secuenciador** y **VCR** .</span><span class="sxs-lookup"><span data-stu-id="2bf70-172">Recognized by the **sequencer** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-173"><span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>\_formato MCI \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="2bf70-173"><span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>MCI\_FORMAT\_TMSF</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-174">Cambia el formato de hora a pistas, minutos, segundos y fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2bf70-174">Changes the time format to tracks, minutes, seconds, and frames.</span></span> <span data-ttu-id="2bf70-175">(MCI usa números de pista continuos). Reconocido por los tipos de dispositivo **cdaudio** y **VCR** .</span><span class="sxs-lookup"><span data-stu-id="2bf70-175">(MCI uses continuous track numbers.) Recognized by the **cdaudio** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-176"><span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>\_vídeo de set MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-176"><span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>MCI\_SET\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-177">Establece la señal de vídeo activada o desactivada.</span><span class="sxs-lookup"><span data-stu-id="2bf70-177">Sets the video signal on or off.</span></span> <span data-ttu-id="2bf70-178">Esta marca debe usarse con MCI \_ establecido \_ en o MCI \_ establecido en \_ OFF.</span><span class="sxs-lookup"><span data-stu-id="2bf70-178">This flag must be used with either MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="2bf70-179">Los dispositivos que no tienen vídeo devuelven MCIERR \_ función no admitida \_ .</span><span class="sxs-lookup"><span data-stu-id="2bf70-179">Devices that do not have video return MCIERR\_UNSUPPORTED\_FUNCTION.</span></span>

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="2bf70-180">Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:</span><span class="sxs-lookup"><span data-stu-id="2bf70-180">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="2bf70-181"><span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI \_ DGV \_ set \_ FILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="2bf70-181"><span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI\_DGV\_SET\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-182">En el miembro **dwFileFormat** de la estructura identificada por *lpSet* se incluye un parámetro de formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="2bf70-182">A file format parameter is included in the **dwFileFormat** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="2bf70-183">En el caso de los dispositivos de vídeo digital, el formato de archivo se usa para los comandos guardar o capturar.</span><span class="sxs-lookup"><span data-stu-id="2bf70-183">For digital-video devices, the file format is used for save or capture commands.</span></span> <span data-ttu-id="2bf70-184">Si se omite, puede que el valor predeterminado sea un formato definido por el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bf70-184">If omitted, this might default to a device driver defined format.</span></span> <span data-ttu-id="2bf70-185">Si el formato de archivo especificado entra en conflicto con el algoritmo y la calidad seleccionados actualmente, se cambian a los valores predeterminados para el formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="2bf70-185">If the specified file format conflicts with the currently selected algorithm and quality, then they are changed to the defaults for the file format.</span></span> <span data-ttu-id="2bf70-186">Se definen las siguientes constantes de formato de archivo:</span><span class="sxs-lookup"><span data-stu-id="2bf70-186">The following file format constants are defined:</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-187"><span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI \_ DGV \_ FF \_ AVI</span><span class="sxs-lookup"><span data-stu-id="2bf70-187"><span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI\_DGV\_FF\_AVI</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-188">Formato AVI.</span><span class="sxs-lookup"><span data-stu-id="2bf70-188">AVI format.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-189"><span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI \_ DGV \_ FF \_ AVSS</span><span class="sxs-lookup"><span data-stu-id="2bf70-189"><span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI\_DGV\_FF\_AVSS</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-190">Formato AVSS.</span><span class="sxs-lookup"><span data-stu-id="2bf70-190">AVSS format.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-191"><span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>\_DGV MCI \_ FF \_ DIB</span><span class="sxs-lookup"><span data-stu-id="2bf70-191"><span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI\_DGV\_FF\_DIB</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-192">Formato DIB.</span><span class="sxs-lookup"><span data-stu-id="2bf70-192">DIB format.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-193"><span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI \_ DGV \_ FF \_ JFIF</span><span class="sxs-lookup"><span data-stu-id="2bf70-193"><span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI\_DGV\_FF\_JFIF</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-194">Formato JFIF.</span><span class="sxs-lookup"><span data-stu-id="2bf70-194">JFIF format.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-195"><span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI \_ DGV \_ FF \_ JPEG</span><span class="sxs-lookup"><span data-stu-id="2bf70-195"><span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI\_DGV\_FF\_JPEG</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-196">Formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="2bf70-196">JPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-197"><span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI \_ DGV \_ FF \_ MPEG</span><span class="sxs-lookup"><span data-stu-id="2bf70-197"><span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI\_DGV\_FF\_MPEG</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-198">Formato MPEG.</span><span class="sxs-lookup"><span data-stu-id="2bf70-198">MPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-199"><span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI \_ DGV \_ FF \_ RDIB</span><span class="sxs-lookup"><span data-stu-id="2bf70-199"><span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI\_DGV\_FF\_RDIB</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-200">Formato DIB de RLE.</span><span class="sxs-lookup"><span data-stu-id="2bf70-200">RLE DIB format.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-201"><span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI \_ DGV \_ FF \_ RJPEG</span><span class="sxs-lookup"><span data-stu-id="2bf70-201"><span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI\_DGV\_FF\_RJPEG</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-202">Formato RJPEG.</span><span class="sxs-lookup"><span data-stu-id="2bf70-202">RJPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-203"><span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>\_DGV MCI \_ set \_ Seek \_ exactly</span><span class="sxs-lookup"><span data-stu-id="2bf70-203"><span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>MCI\_DGV\_SET\_SEEK\_EXACTLY</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-204">Establece el formato utilizado para la posición.</span><span class="sxs-lookup"><span data-stu-id="2bf70-204">Sets the format used for positioning.</span></span> <span data-ttu-id="2bf70-205">Esta marca debe usarse con MCI \_ establecido \_ en o MCI \_ \_ desactivado.</span><span class="sxs-lookup"><span data-stu-id="2bf70-205">This flag must be used with MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="2bf70-206">Si \_ \_ se especifica MCI SET ON, la reproducción o grabación tiene acceso con precisión al marco especificado con la \_ marca MCI from.</span><span class="sxs-lookup"><span data-stu-id="2bf70-206">If MCI\_SET\_ON is specified, playing or recording precisely accesses the frame specified with the MCI\_FROM flag.</span></span> <span data-ttu-id="2bf70-207">Esto podría agregar algún retraso adicional si el fotograma solicitado no es un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="2bf70-207">This might add some extra delay if the requested frame is not a key frame.</span></span> <span data-ttu-id="2bf70-208">Si \_ \_ se especifica MCI SET OFF, el dispositivo buscará una imagen de fotogramas clave que preceda a la trama solicitada.</span><span class="sxs-lookup"><span data-stu-id="2bf70-208">If MCI\_SET\_OFF is specified, the device will seek to a key-frame image that precedes the requested frame.</span></span> <span data-ttu-id="2bf70-209">En algunos archivos y dispositivos, este podría ser el primer fotograma del archivo.</span><span class="sxs-lookup"><span data-stu-id="2bf70-209">For some files and devices, this might be the first frame of the file.</span></span> <span data-ttu-id="2bf70-210">El valor predeterminado para esta marca depende del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bf70-210">The default for this flag is device dependent.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-211"><span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>\_velocidad del \_ conjunto de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-211"><span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>MCI\_DGV\_SET\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-212">Un parámetro de velocidad se incluye en el miembro **dwSpeed** de la estructura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="2bf70-212">A speed parameter is included in the **dwSpeed** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="2bf70-213">La velocidad se especifica como una relación entre la velocidad de fotogramas nominal y la velocidad de fotogramas deseada, donde la velocidad de fotogramas nominal se designa como 1000.</span><span class="sxs-lookup"><span data-stu-id="2bf70-213">Speed is specified as a ratio between the nominal frame rate and the desired frame rate where the nominal frame rate is designated as 1000.</span></span> <span data-ttu-id="2bf70-214">La velocidad media es 500 y la velocidad doble es 2000.</span><span class="sxs-lookup"><span data-stu-id="2bf70-214">Half speed is 500 and double speed is 2000.</span></span> <span data-ttu-id="2bf70-215">El intervalo de velocidad permitido depende también del dispositivo y, posiblemente, del archivo.</span><span class="sxs-lookup"><span data-stu-id="2bf70-215">The allowable speed range is dependent on the device and possibly the file, too.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-216"><span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>\_DGV MCI \_ set \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-216"><span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>MCI\_DGV\_SET\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-217">Cuando se usa con MCI \_ DGV \_ set \_ FILEFORMAT, \_ el conjunto de MCI establece el formato de archivo utilizado para los comandos de captura.</span><span class="sxs-lookup"><span data-stu-id="2bf70-217">When used with MCI\_DGV\_SET\_FILEFORMAT, MCI\_SET sets the file format used for capture commands.</span></span>

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="2bf70-218">En el caso de los dispositivos de vídeo digital, el parámetro *lpSet* apunta a una estructura [**parms de MCI \_ DGV \_ set \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) .</span><span class="sxs-lookup"><span data-stu-id="2bf70-218">For digital-video devices, the *lpSet* parameter points to an [**MCI\_DGV\_SET\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) structure.</span></span>

<span data-ttu-id="2bf70-219">Se usan las siguientes marcas adicionales con el tipo de dispositivo **Sequencer** :</span><span class="sxs-lookup"><span data-stu-id="2bf70-219">The following additional flags are used with the **sequencer** device type:</span></span>

<dl> <dt>

<span data-ttu-id="2bf70-220"><span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>\_ \_ formato \_ SONGPTR de MCI SEQ</span><span class="sxs-lookup"><span data-stu-id="2bf70-220"><span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>MCI\_SEQ\_FORMAT\_SONGPTR</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-221">Establece el formato de hora para las unidades del puntero de la canción.</span><span class="sxs-lookup"><span data-stu-id="2bf70-221">Sets the time format to song pointer units.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-222"><span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>MCI \_ Seq \_ set \_ Master</span><span class="sxs-lookup"><span data-stu-id="2bf70-222"><span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>MCI\_SEQ\_SET\_MASTER</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-223">Establece Sequencer como un origen de datos de sincronización e indica que el tipo de sincronización se especifica en el miembro **dwMaster** de la estructura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="2bf70-223">Sets the sequencer as a source of synchronization data and indicates that the type of synchronization is specified in the **dwMaster** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="2bf70-224">MCISEQ devuelve MCIERR \_ función no admitida \_ .</span><span class="sxs-lookup"><span data-stu-id="2bf70-224">MCISEQ returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="2bf70-225">Las siguientes constantes se definen para el tipo de sincronización:</span><span class="sxs-lookup"><span data-stu-id="2bf70-225">The following constants are defined for the synchronization type:</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-226"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ Seq \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="2bf70-226"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI\_SEQ\_MIDI</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-227">Sequencer enviará los datos de sincronización de formato MIDI.</span><span class="sxs-lookup"><span data-stu-id="2bf70-227">The sequencer will send MIDI format synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-228"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ Seq \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="2bf70-228"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI\_SEQ\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-229">Sequencer enviará los datos de sincronización de formato SMPTE.</span><span class="sxs-lookup"><span data-stu-id="2bf70-229">The sequencer will send SMPTE format synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-230"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ Seq \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="2bf70-230"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-231">Sequencer no enviará los datos de sincronización.</span><span class="sxs-lookup"><span data-stu-id="2bf70-231">The sequencer will not send synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-232"><span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>desplazamiento de set de MCI \_ Seq \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-232"><span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>MCI\_SEQ\_SET\_OFFSET</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-233">Cambia el desplazamiento SMPTE de una secuencia a la especificada por el miembro **dwOffset** de la estructura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="2bf70-233">Changes the SMPTE offset of a sequence to that specified by the **dwOffset** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="2bf70-234">Esto solo afecta a las secuencias con un tipo de división SMPTE.</span><span class="sxs-lookup"><span data-stu-id="2bf70-234">This affects only sequences with a SMPTE division type.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-235"><span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>\_ \_ Puerto set de MCI SEQ \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-235"><span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>MCI\_SEQ\_SET\_PORT</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-236">Establece el puerto MIDI de salida de una secuencia en el especificado por el identificador de dispositivo MIDI en el miembro **dwPort** de la estructura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="2bf70-236">Sets the output MIDI port of a sequence to that specified by the MIDI device identifier in the **dwPort** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="2bf70-237">El dispositivo cierra el puerto anterior (si existe) e intenta abrir y usar el nuevo puerto.</span><span class="sxs-lookup"><span data-stu-id="2bf70-237">The device closes the previous port (if any), and attempts to open and use the new port.</span></span> <span data-ttu-id="2bf70-238">Si se produce un error, devuelve un error y vuelve a abrir el puerto usado previamente (si existe).</span><span class="sxs-lookup"><span data-stu-id="2bf70-238">If it fails, it returns an error and reopens the previously used port (if any).</span></span> <span data-ttu-id="2bf70-239">Las siguientes constantes se definen para los puertos:</span><span class="sxs-lookup"><span data-stu-id="2bf70-239">The following constants are defined for the ports:</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-240"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ Seq \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="2bf70-240"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-241">Cierra el puerto usado previamente (si existe).</span><span class="sxs-lookup"><span data-stu-id="2bf70-241">Closes the previously used port (if any).</span></span> <span data-ttu-id="2bf70-242">Sequencer se comporta exactamente igual que si se hubiese abierto un puerto, excepto en que no se envía ningún mensaje MIDI.</span><span class="sxs-lookup"><span data-stu-id="2bf70-242">The sequencer behaves exactly the same as if a port were open, except no MIDI message is sent.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-243"><span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>\_asignador MIDI</span><span class="sxs-lookup"><span data-stu-id="2bf70-243"><span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>MIDI\_MAPPER</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-244">Establece el puerto abierto en el asignador MIDI.</span><span class="sxs-lookup"><span data-stu-id="2bf70-244">Sets the port opened to the MIDI mapper.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-245"><span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI \_ Seq \_ set \_ Slave</span><span class="sxs-lookup"><span data-stu-id="2bf70-245"><span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI\_SEQ\_SET\_SLAVE</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-246">Establece el secuenciador para recibir los datos de sincronización e indica que el tipo de sincronización se especifica en el miembro **dwSlave** de la estructura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="2bf70-246">Sets the sequencer to receive synchronization data and indicates that the type of synchronization is specified in the **dwSlave** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="2bf70-247">MCISEQ devuelve MCIERR \_ función no admitida \_ .</span><span class="sxs-lookup"><span data-stu-id="2bf70-247">MCISEQ returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="2bf70-248">Las siguientes constantes se definen para el tipo de sincronización:</span><span class="sxs-lookup"><span data-stu-id="2bf70-248">The following constants are defined for the synchronization type:</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-249"><span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>\_archivo de SEQ de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-249"><span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>MCI\_SEQ\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-250">Establece Sequencer para recibir los datos de sincronización contenidos en el archivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="2bf70-250">Sets the sequencer to receive synchronization data contained in the MIDI file.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-251"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ Seq \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="2bf70-251"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI\_SEQ\_MIDI</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-252">Establece el secuenciador para recibir los datos de sincronización MIDI.</span><span class="sxs-lookup"><span data-stu-id="2bf70-252">Sets the sequencer to receive MIDI synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-253"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ Seq \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="2bf70-253"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-254">Establece el secuenciador para omitir los datos de sincronización en una secuencia MIDI.</span><span class="sxs-lookup"><span data-stu-id="2bf70-254">Sets the sequencer to ignore synchronization data in a MIDI stream.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-255"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ Seq \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="2bf70-255"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI\_SEQ\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-256">Establece el secuenciador para recibir los datos de sincronización de SMPTE.</span><span class="sxs-lookup"><span data-stu-id="2bf70-256">Sets the sequencer to receive SMPTE synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-257"><span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>\_ \_ tempo set de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-257"><span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>MCI\_SEQ\_SET\_TEMPO</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-258">Cambia el tempo de la secuencia MIDI a la especificada por el miembro **dwTempo** de la estructura a la que apunta *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="2bf70-258">Changes the tempo of the MIDI sequence to that specified by the **dwTempo** member of the structure pointed to by *lpSet*.</span></span> <span data-ttu-id="2bf70-259">En el caso de las secuencias con el tipo de división PPQN, el tempo se especifica en pulsaciones por minuto. en el caso de las secuencias con el tipo de división SMPTE, el tempo se especifica en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="2bf70-259">For sequences with division type PPQN, tempo is specified in beats per minute; for sequences with division type SMPTE, tempo is specified in frames per second.</span></span>

</dd> </dl>

<span data-ttu-id="2bf70-260">En el caso de los dispositivos del secuenciador, el parámetro *lpSet* apunta a una estructura [**MCI \_ Seq \_ set \_ parms**](mci-seq-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="2bf70-260">For sequencer devices, the *lpSet* parameter points to an [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure.</span></span>

<span data-ttu-id="2bf70-261">Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="2bf70-261">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="2bf70-262"><span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>\_registro de \_ montaje del conjunto de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-262"><span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>MCI\_VCR\_SET\_ASSEMBLE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-263">Establece el dispositivo para grabar en los modos de montaje o inserción (cuando el ensamblado está desactivado, INSERT es on y viceversa).</span><span class="sxs-lookup"><span data-stu-id="2bf70-263">Sets the device to record in assemble or insert modes (when assemble is off, insert is on, and vice-versa).</span></span> <span data-ttu-id="2bf70-264">Use con una de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="2bf70-264">Use with one of the following flag:</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-265"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activado \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-265"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-266">Establece el registro de ensamblado en y activa la opción insertar registro.</span><span class="sxs-lookup"><span data-stu-id="2bf70-266">Sets assemble record on, and turns insert record off.</span></span> <span data-ttu-id="2bf70-267">Registra todas las pistas de vídeo, audio y código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2bf70-267">Records all video, audio and timecode tracks.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-268"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>Desactivación de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-268"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-269">Establece el conjunto de registros en OFF y activa insertar registro.</span><span class="sxs-lookup"><span data-stu-id="2bf70-269">Sets assemble record off, and turns insert record on.</span></span> <span data-ttu-id="2bf70-270">Cuando el registro de ensamblado está desactivado, se pueden seleccionar pistas individuales de vídeo, audio y código de tiempo para la grabación.</span><span class="sxs-lookup"><span data-stu-id="2bf70-270">When assemble record is off, individual tracks of video, audio, and timecode can be selected for recording.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-271"><span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>\_reloj del \_ conjunto de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-271"><span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>MCI\_VCR\_SET\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-272">El miembro **dwClock** de la estructura identificada por *lpSet* contiene la nueva hora de reloj.</span><span class="sxs-lookup"><span data-stu-id="2bf70-272">The **dwClock** member of the structure identified by *lpSet* contains the new clock time.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-273"><span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>forma de \_ contador de VCR MCI \_ set \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-273"><span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>MCI\_VCR\_SET\_COUNTER\_FORMA</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-274">El miembro **dwCounterFormat** de la estructura identificada por *lpSet* contiene una constante que especifica el nuevo formato de tiempo de contador que va a usar el contador de estado.</span><span class="sxs-lookup"><span data-stu-id="2bf70-274">The **dwCounterFormat** member of the structure identified by *lpSet* contains a constant specifying the new counter-time format to be used by the status counter.</span></span> <span data-ttu-id="2bf70-275">Para obtener una lista de constantes válidas, consulte \_ formato de hora del conjunto de MCI \_ \_ en la lista de marcas adicionales para este comando.</span><span class="sxs-lookup"><span data-stu-id="2bf70-275">For a list of valid constants, see MCI\_SET\_TIME\_FORMAT in the list of additional flags for this command.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-276"><span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>\_valor de \_ contador del conjunto de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-276"><span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>MCI\_VCR\_SET\_COUNTER\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-277">El miembro **dwCounterValue** de la estructura identificada por *lpSet* contiene el nuevo valor de contador.</span><span class="sxs-lookup"><span data-stu-id="2bf70-277">The **dwCounterValue** member of the structure identified by *lpSet* contains the new counter value.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-278"><span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>\_Índice del \_ conjunto de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-278"><span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>MCI\_VCR\_SET\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-279">El miembro **dwIndex** de la estructura identificada por *lpSet* contiene una constante que indica el contenido de la presentación en pantalla y debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2bf70-279">The **dwIndex** member of the structure identified by *lpSet* contains a constant indicating the contents of the on-screen display and must be one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-280"><span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>\_contador de \_ Índice de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-280"><span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>MCI\_VCR\_INDEX\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-281">Muestra Counter.</span><span class="sxs-lookup"><span data-stu-id="2bf70-281">Displays counter.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-282"><span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>\_fecha de \_ Índice de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-282"><span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>MCI\_VCR\_INDEX\_DATE</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-283">Muestra la fecha.</span><span class="sxs-lookup"><span data-stu-id="2bf70-283">Displays date.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-284"><span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>\_tiempo de \_ Índice de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-284"><span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>MCI\_VCR\_INDEX\_TIME</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-285">Muestra la hora.</span><span class="sxs-lookup"><span data-stu-id="2bf70-285">Displays time.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-286"><span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>\_código de \_ tiempo del índice de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-286"><span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>MCI\_VCR\_INDEX\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-287">Muestra el código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2bf70-287">Displays timecode.</span></span>

<span data-ttu-id="2bf70-288">Para obtener más información, consulte el comando [MCI \_ index](mci-index.md) .</span><span class="sxs-lookup"><span data-stu-id="2bf70-288">For more information, see the [MCI\_INDEX](mci-index.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-289"><span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>\_tiempo de \_ espera de pausa de conjunto de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-289"><span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>MCI\_VCR\_SET\_PAUSE\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-290">El miembro **dwPauseTimeout** de la estructura identificada por *lpSet* contiene la duración máxima, en milisegundos, de un comando PAUSE.</span><span class="sxs-lookup"><span data-stu-id="2bf70-290">The **dwPauseTimeout** member of the structure identified by *lpSet* contains the maximum duration, in milliseconds, of a pause command.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-291"><span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>\_duración de \_ PostRoll de conjunto de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-291"><span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>MCI\_VCR\_SET\_POSTROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-292">El miembro **dwPostrollDuration** de la estructura identificada por *lpSet* contiene la longitud de la cinta de vídeo, en el formato de hora actual, necesaria para frenar el transporte de VCR cuando se emite un comando de detención o pausa.</span><span class="sxs-lookup"><span data-stu-id="2bf70-292">The **dwPostrollDuration** member of the structure identified by *lpSet* contains the videotape length, in the current time format, needed to brake the VCR transport when a stop or pause command is issued.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-293"><span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>\_energía del \_ juego de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-293"><span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>MCI\_VCR\_SET\_POWER</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-294">Permite activar o desactivar la alimentación.</span><span class="sxs-lookup"><span data-stu-id="2bf70-294">Sets the power on or off.</span></span> <span data-ttu-id="2bf70-295">Debe usarse con una de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="2bf70-295">Must be used with one of the following flags:</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-296"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>Desactivación de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-296"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-297">Desactiva el apagado.</span><span class="sxs-lookup"><span data-stu-id="2bf70-297">Turns power off.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-298"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activado \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-298"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-299">Activa el encendido.</span><span class="sxs-lookup"><span data-stu-id="2bf70-299">Turns power on.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-300"><span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>\_duración del \_ preajuste del vídeo de \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-300"><span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>MCI\_VCR\_SET\_PREROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-301">El miembro **dwPrerollDuration** de la estructura identificada por *lpSet* contiene la longitud de la cinta de vídeo, en el formato de hora actual, necesaria para estabilizar la salida del VCR.</span><span class="sxs-lookup"><span data-stu-id="2bf70-301">The **dwPrerollDuration** member of the structure identified by *lpSet* contains the videotape length, in the current time format, needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-302"><span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>\_formato de \_ registro del conjunto de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-302"><span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>MCI\_VCR\_SET\_RECORD\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-303">El miembro **dwRecordFormat** de la estructura identificada por *lpSet* contiene una constante que describe la velocidad del registro, que debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2bf70-303">The **dwRecordFormat** member of the structure identified by *lpSet* contains a constant describing the record speed, which must be one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-304"><span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>formato de VCR de MCI \_ \_ \_ EP</span><span class="sxs-lookup"><span data-stu-id="2bf70-304"><span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>MCI\_VCR\_FORMAT\_EP</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-305">Registros a velocidad lenta.</span><span class="sxs-lookup"><span data-stu-id="2bf70-305">Records at slow speed.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-306"><span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>formato de VCR de MCI \_ \_ \_ LP</span><span class="sxs-lookup"><span data-stu-id="2bf70-306"><span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>MCI\_VCR\_FORMAT\_LP</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-307">Registros a velocidad lenta.</span><span class="sxs-lookup"><span data-stu-id="2bf70-307">Records at medium-slow speed.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-308"><span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>\_SP de \_ formato \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="2bf70-308"><span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>MCI\_VCR\_FORMAT\_SP</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-309">Registros a velocidad estándar.</span><span class="sxs-lookup"><span data-stu-id="2bf70-309">Records at standard speed.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-310"><span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>\_velocidad del \_ conjunto de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-310"><span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>MCI\_VCR\_SET\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-311">El miembro **dwSpeed** de la estructura identificada por *lpSet* contiene la nueva configuración de velocidad, donde 1000 es la velocidad normal, 2000 es la velocidad doble y 500 es la velocidad media, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="2bf70-311">The **dwSpeed** member of the structure identified by *lpSet* contains the new speed setting, where 1000 is normal speed, 2000 is double speed, and 500 is half speed, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-312"><span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>\_longitud de \_ cinta del conjunto de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-312"><span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>MCI\_VCR\_SET\_TAPE\_LENGTH</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-313">El miembro **dwTapeLength** de la estructura identificada por *lpSet* contiene la nueva longitud de la cinta, siempre que no se detecte la longitud de la cinta.</span><span class="sxs-lookup"><span data-stu-id="2bf70-313">The **dwTapeLength** member of the structure identified by *lpSet* contains the new length of the tape, provided that the length of the tape is undetectable.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-314"><span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>\_modo de \_ tiempo de conjunto de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-314"><span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>MCI\_VCR\_SET\_TIME\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-315">El miembro **dwTimeMode** de la estructura identificada por *lpSet* contiene una constante que indica el nuevo modo de hora posicional.</span><span class="sxs-lookup"><span data-stu-id="2bf70-315">The **dwTimeMode** member of the structure identified by *lpSet* contains a constant indicating the new positional time mode.</span></span> <span data-ttu-id="2bf70-316">Las constantes siguientes son válidas:</span><span class="sxs-lookup"><span data-stu-id="2bf70-316">The following constants are valid:</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-317"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_contador de \_ tiempo de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-317"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI\_VCR\_TIME\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-318">Obliga al dispositivo a usar el contador de forma exclusiva.</span><span class="sxs-lookup"><span data-stu-id="2bf70-318">Forces the device to use counter exclusively.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-319"><span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>\_detección de \_ tiempo de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-319"><span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>MCI\_VCR\_TIME\_DETECT</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-320">Cada vez que se inserta una nueva cinta de vídeo en el dispositivo o el modo cambia de no está listo a listo, el dispositivo debe intentar determinar si hay código de tiempo disponible en la cinta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2bf70-320">Each time a new videotape is inserted into the device, or the mode changes from not ready to ready, the device should attempt to determine if there is timecode available on the videotape.</span></span> <span data-ttu-id="2bf70-321">Si el código de tiempo está disponible, use el código de tiempo en todos los comandos subsiguientes que especifiquen posiciones.</span><span class="sxs-lookup"><span data-stu-id="2bf70-321">If timecode is available, use timecode in all subsequent commands that specify positions.</span></span> <span data-ttu-id="2bf70-322">De lo contrario, use el contador.</span><span class="sxs-lookup"><span data-stu-id="2bf70-322">Otherwise, use the counter.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-323"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>\_código de \_ tiempo de vídeo de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-323"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI\_VCR\_TIME\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-324">Obliga al dispositivo a usar el código de tiempo exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="2bf70-324">Forces the device to use timecode exclusively.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-325"><span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>\_seguimiento del \_ conjunto de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-325"><span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>MCI\_VCR\_SET\_TRACKING</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-326">Ajusta la velocidad del transporte de cinta de VCR con un ajuste fino y debe usarse con una de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="2bf70-326">Tunes the speed of the VCR tape transport with a fine adjustment, and must be used with one of the following flags:</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-327"><span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>VCR de MCI \_ \_ Plus</span><span class="sxs-lookup"><span data-stu-id="2bf70-327"><span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>MCI\_VCR\_PLUS</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-328">Aumenta la velocidad de transporte de la cinta.</span><span class="sxs-lookup"><span data-stu-id="2bf70-328">Increases the tape transport speed.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-329"><span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>VCR de MCI \_ \_ menos</span><span class="sxs-lookup"><span data-stu-id="2bf70-329"><span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>MCI\_VCR\_MINUS</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-330">Disminuye la velocidad de transporte de cinta.</span><span class="sxs-lookup"><span data-stu-id="2bf70-330">Decreases the tape transport speed.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-331"><span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>\_restablecimiento de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-331"><span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>MCI\_VCR\_RESET</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-332">Devuelve el ajuste de seguimiento a cero.</span><span class="sxs-lookup"><span data-stu-id="2bf70-332">Returns the tracking adjustment to zero.</span></span>

</dd> </dl>

<span data-ttu-id="2bf70-333">En el caso de los dispositivos VCR, el parámetro *lpSet* apunta a una estructura [**\_ parms de VCR VCR \_ set \_**](mci-vcr-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="2bf70-333">For VCR devices, the *lpSet* parameter points to an [**MCI\_VCR\_SET\_PARMS**](mci-vcr-set-parms.md) structure.</span></span>

<span data-ttu-id="2bf70-334">La siguiente marca adicional se usa con el tipo de dispositivo de **videodisco** :</span><span class="sxs-lookup"><span data-stu-id="2bf70-334">The following additional flag is used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="2bf70-335"><span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>pista de formato de MCI \_ Vd \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-335"><span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>MCI\_VD\_FORMAT\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-336">Cambia el formato de hora a las pistas.</span><span class="sxs-lookup"><span data-stu-id="2bf70-336">Changes the time format to tracks.</span></span> <span data-ttu-id="2bf70-337">MCI usa números de pista continuos.</span><span class="sxs-lookup"><span data-stu-id="2bf70-337">MCI uses continuous track numbers.</span></span>

</dd> </dl>

<span data-ttu-id="2bf70-338">Con el tipo de dispositivo **WaveAudio** se usan las siguientes marcas adicionales:</span><span class="sxs-lookup"><span data-stu-id="2bf70-338">The following additional flags are used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="2bf70-339"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrada de onda de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-339"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-340">Establece la entrada que se usa para la grabación en el miembro **WInput** de la estructura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="2bf70-340">Sets the input used for recording to the **wInput** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-341"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_salida de onda de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-341"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-342">Establece la salida usada para reproducirla en el miembro **wOutput** de la estructura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="2bf70-342">Sets the output used for playing to the **wOutput** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-343"><span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>ANYINPUT de onda de MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-343"><span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>MCI\_WAVE\_SET\_ANYINPUT</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-344">Cualquier entrada de onda compatible con el formato actual se puede usar para la grabación.</span><span class="sxs-lookup"><span data-stu-id="2bf70-344">Any wave input compatible with the current format can be used for recording.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-345"><span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>ANYOUTPUT de onda de MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-345"><span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>MCI\_WAVE\_SET\_ANYOUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-346">Cualquier salida de onda compatible con el formato actual se puede usar para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="2bf70-346">Any wave output compatible with the current format can be used for playing.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-347"><span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>AVGBYTESPERSEC de onda de MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-347"><span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>MCI\_WAVE\_SET\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-348">Establece los bytes por segundo que se usan para reproducir, grabar y guardar en el miembro **nAvgBytesPerSec** de la estructura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="2bf70-348">Sets the bytes per second used for playing, recording, and saving to the **nAvgBytesPerSec** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-349"><span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>BitsPerSample de onda de MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-349"><span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>MCI\_WAVE\_SET\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-350">Establece los bits por muestra que se usan para reproducir, grabar y guardar en el miembro **nBitsPerSample** del formato de datos PCM identificado por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="2bf70-350">Sets the bits per sample used for playing, recording, and saving to the **nBitsPerSample** member of the PCM data format identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-351"><span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>BLOCKALIGN de onda de MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-351"><span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>MCI\_WAVE\_SET\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-352">Establece la alineación de bloque utilizada para reproducir, grabar y guardar en el miembro **nBlockAlign** de la estructura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="2bf70-352">Sets the block alignment used for playing, recording, and saving to the **nBlockAlign** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-353"><span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>\_canales de \_ conjunto de ondas MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-353"><span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>MCI\_WAVE\_SET\_CHANNELS</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-354">El número de canales se indica en el miembro **nChannels** de la estructura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="2bf70-354">The number of channels is indicated in the **nChannels** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-355"><span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>FORMATTAG de onda de MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-355"><span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>MCI\_WAVE\_SET\_FORMATTAG</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-356">Establece el tipo de formato usado para reproducir, grabar y guardar en el miembro **wFormatTag** de la estructura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="2bf70-356">Sets the format type used for playing, recording, and saving to the **wFormatTag** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="2bf70-357">Especificar \_ \_ el formato de onda PCM cambia el formato a PCM.</span><span class="sxs-lookup"><span data-stu-id="2bf70-357">Specifying WAVE\_FORMAT\_PCM changes the format to PCM.</span></span>

</dd> <dt>

<span data-ttu-id="2bf70-358"><span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>SAMPLESPERSEC de onda de MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-358"><span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>MCI\_WAVE\_SET\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="2bf70-359">Establece las muestras por segundo que se usan para reproducir, grabar y guardar en el miembro **nSamplesPerSec** de la estructura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="2bf70-359">Sets the samples per second used for playing, recording, and saving to the **nSamplesPerSec** member of the structure identified by *lpSet*.</span></span>

</dd> </dl>

<span data-ttu-id="2bf70-360">En el caso de los dispositivos de audio de onda, el parámetro *lpSet* apunta a una estructura de [**\_ \_ \_ parms de onda de MCI**](mci-wave-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="2bf70-360">For waveform-audio devices, the *lpSet* parameter points to an [**MCI\_WAVE\_SET\_PARMS**](mci-wave-set-parms.md) structure.</span></span>

<span data-ttu-id="2bf70-361">Se definen varias propiedades de los datos de audio de forma de onda cuando se crea el archivo en el que se almacenan los datos.</span><span class="sxs-lookup"><span data-stu-id="2bf70-361">Several properties of waveform-audio data are defined when the file to store the data is created.</span></span> <span data-ttu-id="2bf70-362">Estas propiedades describen cómo se estructuran los datos en el archivo y no se pueden cambiar una vez que se inicia la grabación.</span><span class="sxs-lookup"><span data-stu-id="2bf70-362">These properties describe how the data is structured within the file and cannot be changed once recording begins.</span></span> <span data-ttu-id="2bf70-363">La siguiente lista de marcas identifica estas propiedades:</span><span class="sxs-lookup"><span data-stu-id="2bf70-363">The following list of flags identifies these properties:</span></span>

-   <span data-ttu-id="2bf70-364">AVGBYTESPERSEC de onda de MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-364">MCI\_WAVE\_SET\_AVGBYTESPERSEC</span></span>
-   <span data-ttu-id="2bf70-365">BitsPerSample de onda de MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-365">MCI\_WAVE\_SET\_BITSPERSAMPLE</span></span>
-   <span data-ttu-id="2bf70-366">BLOCKALIGN de onda de MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-366">MCI\_WAVE\_SET\_BLOCKALIGN</span></span>
-   <span data-ttu-id="2bf70-367">\_canales de \_ conjunto de ondas MCI \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-367">MCI\_WAVE\_SET\_CHANNELS</span></span>
-   <span data-ttu-id="2bf70-368">FORMATTAG de onda de MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-368">MCI\_WAVE\_SET\_FORMATTAG</span></span>
-   <span data-ttu-id="2bf70-369">SAMPLESPERSEC de onda de MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="2bf70-369">MCI\_WAVE\_SET\_SAMPLESPERSEC</span></span>

## <a name="requirements"></a><span data-ttu-id="2bf70-370">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bf70-370">Requirements</span></span>



| <span data-ttu-id="2bf70-371">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bf70-371">Requirement</span></span> | <span data-ttu-id="2bf70-372">Value</span><span class="sxs-lookup"><span data-stu-id="2bf70-372">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bf70-373">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bf70-373">Minimum supported client</span></span><br/> | <span data-ttu-id="2bf70-374">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2bf70-374">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2bf70-375">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bf70-375">Minimum supported server</span></span><br/> | <span data-ttu-id="2bf70-376">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2bf70-376">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2bf70-377">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bf70-377">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bf70-378"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2bf70-378"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bf70-379">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bf70-379">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bf70-380">MCI</span><span class="sxs-lookup"><span data-stu-id="2bf70-380">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2bf70-381">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="2bf70-381">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

