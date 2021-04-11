---
title: Comando MCI_SETAUDIO (mmsystem. h)
description: El \_ comando MCI SETAUDIO establece los valores asociados a la reproducción y la captura de audio. Los dispositivos digitales-vídeo y VCR reconocen este comando.
ms.assetid: 78624596-e465-4ef1-8988-edcfe9a46f89
keywords:
- Comando de MCI_SETAUDIO de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SETAUDIO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20605ff78c62a8e688778692d5ca8f8e1342a968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274542"
---
# <a name="mci_setaudio-command"></a><span data-ttu-id="0549a-105">\_Comando MCI SETAUDIO</span><span class="sxs-lookup"><span data-stu-id="0549a-105">MCI\_SETAUDIO command</span></span>

<span data-ttu-id="0549a-106">El \_ comando MCI SETAUDIO establece los valores asociados a la reproducción y la captura de audio.</span><span class="sxs-lookup"><span data-stu-id="0549a-106">The MCI\_SETAUDIO command sets values associated with audio playback and capture.</span></span> <span data-ttu-id="0549a-107">Los dispositivos digitales-vídeo y VCR reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="0549a-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="0549a-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="0549a-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETAUDIO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetAudio
);
```



## <a name="parameters"></a><span data-ttu-id="0549a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0549a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0549a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="0549a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0549a-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="0549a-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="0549a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0549a-113">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="0549a-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="0549a-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0549a-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="0549a-115"><span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*</span><span class="sxs-lookup"><span data-stu-id="0549a-115"><span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*</span></span>
</dt> <dd>

<span data-ttu-id="0549a-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="0549a-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="0549a-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="0549a-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0549a-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0549a-118">Return Value</span></span>

<span data-ttu-id="0549a-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0549a-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0549a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0549a-120">Remarks</span></span>

<span data-ttu-id="0549a-121">Las marcas siguientes se aplican al tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="0549a-121">The following flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="0549a-122"><span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>\_DGV MCI \_ SETAUDIO \_ alg</span><span class="sxs-lookup"><span data-stu-id="0549a-122"><span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI\_DGV\_SETAUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="0549a-123">El miembro **lpstrAlgorithm** de la estructura identificada por *lpSetAudio* contiene una dirección de un búfer que contiene el nombre de un algoritmo de compresión de audio.</span><span class="sxs-lookup"><span data-stu-id="0549a-123">The **lpstrAlgorithm** member of the structure identified by *lpSetAudio* contains an address of a buffer containing the name of an audio compression algorithm.</span></span> <span data-ttu-id="0549a-124">El algoritmo de compresión lo usan los comandos de [ \_ reserva de MCI](mci-reserve.md) o de [ \_ registro MCI](mci-record.md) posteriores.</span><span class="sxs-lookup"><span data-stu-id="0549a-124">The compression algorithm is used by subsequent [MCI\_RESERVE](mci-reserve.md) or [MCI\_RECORD](mci-record.md) commands.</span></span> <span data-ttu-id="0549a-125">Los algoritmos disponibles dependen del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0549a-125">The available algorithms are device dependent.</span></span> <span data-ttu-id="0549a-126">Si el algoritmo es incompatible con el formato de archivo actual, el formato de archivo se cambia al formato predeterminado para el algoritmo.</span><span class="sxs-lookup"><span data-stu-id="0549a-126">If the algorithm is incompatible with the current file format, the file format is changed to the default format for the algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-127"><span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI \_ DGV \_ SETAUDIO \_ CLOCKTIME</span><span class="sxs-lookup"><span data-stu-id="0549a-127"><span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI\_DGV\_SETAUDIO\_CLOCKTIME</span></span>
</dt> <dd>

<span data-ttu-id="0549a-128">La hora especificada se encuentra en milisegundos y es la hora absoluta cuando se usa con MCI \_ DGV \_ SETAUDIO \_ over.</span><span class="sxs-lookup"><span data-stu-id="0549a-128">The time specified is in milliseconds and is absolute time when used with MCI\_DGV\_SETAUDIO\_OVER.</span></span> <span data-ttu-id="0549a-129">(Esta vez no está en el paso con la reproducción del área de trabajo).</span><span class="sxs-lookup"><span data-stu-id="0549a-129">(This time is not in step with the playing of the workspace.)</span></span>

</dd> <dt>

<span data-ttu-id="0549a-130"><span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>\_ \_ entrada SETAUDIO de MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="0549a-130"><span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>MCI\_DGV\_SETAUDIO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="0549a-131">Modifica la marca de graves, agudos o de volumen para que afecte a la señal de entrada y modifique lo que se registra.</span><span class="sxs-lookup"><span data-stu-id="0549a-131">Modifies the bass, treble, or volume flag so that it affects the input signal and modifies what is recorded.</span></span> <span data-ttu-id="0549a-132">Si es posible, es el valor predeterminado al supervisar la entrada.</span><span class="sxs-lookup"><span data-stu-id="0549a-132">If possible, this is the default when monitoring the input.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-133"><span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>\_ \_ elemento SETAUDIO de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="0549a-133"><span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>MCI\_DGV\_SETAUDIO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="0549a-134">Una constante de audio se especifica en el miembro **dwItem** de la estructura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="0549a-134">An audio constant is specified in the **dwItem** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="0549a-135">La constante identifica el valor que se establece.</span><span class="sxs-lookup"><span data-stu-id="0549a-135">The constant identifies the value that is being set.</span></span> <span data-ttu-id="0549a-136">Se definen las constantes siguientes:</span><span class="sxs-lookup"><span data-stu-id="0549a-136">The following constants are defined:</span></span>

</dd> <dt>

<span data-ttu-id="0549a-137"><span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI \_ DGV \_ SETAUDIO \_ AVGBYTESPERSEC</span><span class="sxs-lookup"><span data-stu-id="0549a-137"><span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI\_DGV\_SETAUDIO\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="0549a-138">El número promedio de bytes se especifica en el miembro **dwValue** de la estructura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="0549a-138">The average number of bytes is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="0549a-139">Este valor establece el número medio de bytes por segundo para reproducir o grabar en los formatos PCM (modulación por pulsos de código) y ADPCM (modulación de código de impulso diferencial adaptativo).</span><span class="sxs-lookup"><span data-stu-id="0549a-139">This value sets the average number of bytes per second for playing or recording in the PCM (Pulse Code Modulation) and ADPCM (Adaptive Differential Pulse Code Modulation) formats.</span></span> <span data-ttu-id="0549a-140">El archivo se guarda en este formato.</span><span class="sxs-lookup"><span data-stu-id="0549a-140">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-141"><span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>\_DGV MCI \_ SETAUDIO \_ Bass</span><span class="sxs-lookup"><span data-stu-id="0549a-141"><span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI\_DGV\_SETAUDIO\_BASS</span></span>
</dt> <dd>

<span data-ttu-id="0549a-142">El nivel de baja frecuencia de audio se especifica como un factor en el miembro **dwValue** de la estructura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="0549a-142">The audio low frequency level is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-143"><span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI \_ DGV \_ SETAUDIO \_ BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="0549a-143"><span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI\_DGV\_SETAUDIO\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="0549a-144">El número de bits por muestra se especifica en el miembro **dwValue** de la estructura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="0549a-144">The number of bits per sample is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="0549a-145">Este valor establece el número de bits por muestra reproducido o grabado en el formato PCM.</span><span class="sxs-lookup"><span data-stu-id="0549a-145">This value sets the number of bits per sample played or recorded in the PCM format.</span></span> <span data-ttu-id="0549a-146">El archivo se guarda en este formato.</span><span class="sxs-lookup"><span data-stu-id="0549a-146">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-147"><span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI \_ DGV \_ SETAUDIO \_ BLOCKALIGN</span><span class="sxs-lookup"><span data-stu-id="0549a-147"><span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI\_DGV\_SETAUDIO\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="0549a-148">La alineación del bloque de datos se especifica en el miembro **dwValue** de la estructura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="0549a-148">The data block alignment is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="0549a-149">Este valor establece la alineación de los bloques de datos en relación con el inicio de los datos de la manera de onda de entrada.</span><span class="sxs-lookup"><span data-stu-id="0549a-149">This value sets the alignment of data blocks relative to the start of input waveform data.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-150"><span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI \_ DGV \_ SETAUDIO \_ SAMPLESPERSEC</span><span class="sxs-lookup"><span data-stu-id="0549a-150"><span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI\_DGV\_SETAUDIO\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="0549a-151">La frecuencia de muestreo se especifica en el miembro **dwValue** de la estructura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="0549a-151">The sample rate is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="0549a-152">Este valor establece la velocidad de muestreo para reproducir y grabar con los algoritmos PCM y ADPCM.</span><span class="sxs-lookup"><span data-stu-id="0549a-152">This value sets the sample rate for playing and recording with the PCM and ADPCM algorithms.</span></span> <span data-ttu-id="0549a-153">El archivo se guarda en este formato.</span><span class="sxs-lookup"><span data-stu-id="0549a-153">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-154"><span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>origen de DGV de MCI \_ \_ SETAUDIO \_</span><span class="sxs-lookup"><span data-stu-id="0549a-154"><span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>MCI\_DGV\_SETAUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="0549a-155">Una constante que especifica el origen de la entrada de audio se incluye en el miembro **dwValue** de la estructura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="0549a-155">A constant specifying the source of audio input is included in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="0549a-156">Las siguientes constantes se definen para los orígenes de entrada de audio:</span><span class="sxs-lookup"><span data-stu-id="0549a-156">The following constants are defined for the audio input sources:</span></span>

<span data-ttu-id="0549a-157">media de origen de DGV de MCI \_ \_ SETAUDIO \_ \_</span><span class="sxs-lookup"><span data-stu-id="0549a-157">MCI\_DGV\_SETAUDIO\_SOURCE\_AVERAGE</span></span>

<span data-ttu-id="0549a-158">Promedio de los canales de audio izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="0549a-158">The average of the left and right audio channels.</span></span>

<span data-ttu-id="0549a-159">\_DGV MCI \_ SETAUDIO \_ source \_ left</span><span class="sxs-lookup"><span data-stu-id="0549a-159">MCI\_DGV\_SETAUDIO\_SOURCE\_LEFT</span></span>

<span data-ttu-id="0549a-160">Canal de audio izquierdo.</span><span class="sxs-lookup"><span data-stu-id="0549a-160">Left audio channel.</span></span>

<span data-ttu-id="0549a-161">MCI \_ DGV \_ SETAUDIO \_ source \_ right</span><span class="sxs-lookup"><span data-stu-id="0549a-161">MCI\_DGV\_SETAUDIO\_SOURCE\_RIGHT</span></span>

<span data-ttu-id="0549a-162">Canal de audio derecho.</span><span class="sxs-lookup"><span data-stu-id="0549a-162">Right audio channel.</span></span>

<span data-ttu-id="0549a-163">estéreo de origen de DGV de MCI \_ \_ SETAUDIO \_ \_</span><span class="sxs-lookup"><span data-stu-id="0549a-163">MCI\_DGV\_SETAUDIO\_SOURCE\_STEREO</span></span>

<span data-ttu-id="0549a-164">Casa.</span><span class="sxs-lookup"><span data-stu-id="0549a-164">Stereo.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-165"><span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>\_flujo de \_ SETAUDIO de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="0549a-165"><span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>MCI\_DGV\_SETAUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="0549a-166">Se especifica una secuencia de audio en el miembro **dwValue** de la estructura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="0549a-166">An audio-stream is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="0549a-167">El valor entero especifica la secuencia de audio que se reproduce desde el área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="0549a-167">The integer value specifies the audio stream played back from the workspace.</span></span> <span data-ttu-id="0549a-168">Si no se especifica la secuencia, se reproduce la primera secuencia de audio intercalada físicamente.</span><span class="sxs-lookup"><span data-stu-id="0549a-168">If the stream is not specified, the first physically interleaved audio stream is played.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-169"><span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI \_ DGV \_ SETAUDIO \_ agudos</span><span class="sxs-lookup"><span data-stu-id="0549a-169"><span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI\_DGV\_SETAUDIO\_TREBLE</span></span>
</dt> <dd>

<span data-ttu-id="0549a-170">El nivel de alta frecuencia de audio se especifica como un factor en el miembro **dwValue** de la estructura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="0549a-170">The audio high-frequency level is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-171"><span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>\_volumen de \_ SETAUDIO de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="0549a-171"><span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>MCI\_DGV\_SETAUDIO\_VOLUME</span></span>
</dt> <dd>

<span data-ttu-id="0549a-172">El nivel de audio de uno o ambos canales de audio se especifica como factor en el miembro **dwValue** de la estructura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="0549a-172">The audio level for one or both audio channels is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="0549a-173">Si los volúmenes izquierdo y derecho se han establecido en valores diferentes, la relación entre el volumen de izquierda a derecha es prácticamente inalterada.</span><span class="sxs-lookup"><span data-stu-id="0549a-173">If the left and right volumes have been set to different values, then the ratio of left to right volume is approximately unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-174"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>\_DGV MCI \_ SETAUDIO \_ izquierda</span><span class="sxs-lookup"><span data-stu-id="0549a-174"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI\_DGV\_SETAUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="0549a-175">Habilita el canal de audio izquierdo cuando se usa con MCI \_ establecido \_ en.</span><span class="sxs-lookup"><span data-stu-id="0549a-175">Enables the left audio channel when used with MCI\_SET\_ON.</span></span> <span data-ttu-id="0549a-176">Deshabilita el canal de audio izquierdo cuando se usa con MCI \_ establecido en \_ OFF.</span><span class="sxs-lookup"><span data-stu-id="0549a-176">Disables the left audio channel when used with MCI\_SET\_OFF.</span></span> <span data-ttu-id="0549a-177">Cuando esta marca se usa con la combinación de MCI \_ DGV \_ SETAUDIO \_ value y MCI \_ DGV \_ SETAUDIO \_ Volume, establece el volumen del canal de audio izquierdo.</span><span class="sxs-lookup"><span data-stu-id="0549a-177">When this flag is used with the combination of MCI\_DGV\_SETAUDIO\_VALUE and MCI\_DGV\_SETAUDIO\_VOLUME, it sets the volume of the left audio channel.</span></span> <span data-ttu-id="0549a-178">Cuando esta marca se usa con el \_ origen MCI DGV \_ SETAUDIO \_ , especifica el canal de audio izquierdo como el origen del digitalizador de entrada de audio.</span><span class="sxs-lookup"><span data-stu-id="0549a-178">When this flag is used with MCI\_DGV\_SETAUDIO\_SOURCE, it specifies the left audio channel as the source for the audio input digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-179"><span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI \_ DGV \_ SETAUDIO \_</span><span class="sxs-lookup"><span data-stu-id="0549a-179"><span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI\_DGV\_SETAUDIO\_OVER</span></span>
</dt> <dd>

<span data-ttu-id="0549a-180">Un parámetro de longitud de transición se incluye en el miembro **dwOver** de la estructura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="0549a-180">A transition length parameter is included in the **dwOver** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="0549a-181">El valor de longitud especifica cuánto tiempo (en unidades del formato de hora actual) debe tardar en realizar un cambio que use un factor.</span><span class="sxs-lookup"><span data-stu-id="0549a-181">The length value specifies how long (in units of the current time format) it should take to make a change that uses a factor.</span></span> <span data-ttu-id="0549a-182">Si no se usa esta marca, los cambios se producen inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="0549a-182">If this flag is not used, changes occur immediately.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-183"><span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>calidad de SETAUDIO de MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="0549a-183"><span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>MCI\_DGV\_SETAUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="0549a-184">El miembro **lpstrQuality** de la estructura identificada por *lpSetAudio* contiene una dirección de un búfer que define la calidad del audio.</span><span class="sxs-lookup"><span data-stu-id="0549a-184">The **lpstrQuality** member of the structure identified by *lpSetAudio* contains an address of a buffer defining the audio quality.</span></span> <span data-ttu-id="0549a-185">Una cadena de texto dentro del búfer especifica las características del algoritmo de compresión de audio.</span><span class="sxs-lookup"><span data-stu-id="0549a-185">A text-string within the buffer specifies the characteristics of the audio compression algorithm.</span></span>

<span data-ttu-id="0549a-186">La \_ marca MCI DGV \_ SETAUDIO \_ alg se puede usar para seleccionar un descriptor de calidad para el algoritmo especificado.</span><span class="sxs-lookup"><span data-stu-id="0549a-186">The MCI\_DGV\_SETAUDIO\_ALG flag can be used to select a quality descriptor for the specified algorithm.</span></span> <span data-ttu-id="0549a-187">Si se omite esta marca, se utiliza el algoritmo actual.</span><span class="sxs-lookup"><span data-stu-id="0549a-187">If this flag is omitted, then the current algorithm is used.</span></span>

<span data-ttu-id="0549a-188">Los algoritmos y los nombres de descriptor disponibles dependen del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0549a-188">The algorithms and descriptor names available depend on the device.</span></span> <span data-ttu-id="0549a-189">Cada dispositivo proporciona documentación para los algoritmos disponibles y una descripción de los nombres de descriptor aplicables.</span><span class="sxs-lookup"><span data-stu-id="0549a-189">Each device supplies documentation for the available algorithms and a description of the applicable descriptor names.</span></span> <span data-ttu-id="0549a-190">El comando [MCI \_ Quality](mci-quality.md) puede definir nombres de descriptores adicionales.</span><span class="sxs-lookup"><span data-stu-id="0549a-190">The [MCI\_QUALITY](mci-quality.md) command can define additional descriptor names.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-191"><span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>registro de DGV de MCI \_ \_ SETAUDIO \_</span><span class="sxs-lookup"><span data-stu-id="0549a-191"><span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>MCI\_DGV\_SETAUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="0549a-192">Especifica si la grabación incluye o excluye datos de audio.</span><span class="sxs-lookup"><span data-stu-id="0549a-192">Specifies whether recording includes or excludes audio data.</span></span> <span data-ttu-id="0549a-193">Cuando se combina con MCI \_ establecido \_ en, se registran los datos de audio.</span><span class="sxs-lookup"><span data-stu-id="0549a-193">When combined with MCI\_SET\_ON, audio data is recorded.</span></span> <span data-ttu-id="0549a-194">Cuando se combina con MCI \_ establecido en \_ OFF, se excluyen los datos de audio.</span><span class="sxs-lookup"><span data-stu-id="0549a-194">When combined with MCI\_SET\_OFF, audio data is excluded.</span></span> <span data-ttu-id="0549a-195">El valor predeterminado incluye datos de audio.</span><span class="sxs-lookup"><span data-stu-id="0549a-195">The default includes audio data.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-196"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>\_DGV MCI \_ SETAUDIO \_ derecha</span><span class="sxs-lookup"><span data-stu-id="0549a-196"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI\_DGV\_SETAUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="0549a-197">Habilita el canal de audio adecuado cuando se usa con MCI \_ establecido \_ en.</span><span class="sxs-lookup"><span data-stu-id="0549a-197">Enables the right audio channel when used with MCI\_SET\_ON.</span></span> <span data-ttu-id="0549a-198">Deshabilita el canal de audio derecho cuando se usa con MCI \_ establecido en \_ OFF.</span><span class="sxs-lookup"><span data-stu-id="0549a-198">Disables the right audio channel when used with MCI\_SET\_OFF.</span></span> <span data-ttu-id="0549a-199">Cuando esta marca se usa con la combinación de MCI \_ DGV \_ SETAUDIO \_ value y MCI \_ DGV \_ SETAUDIO \_ Volume, establece el volumen del canal de audio adecuado.</span><span class="sxs-lookup"><span data-stu-id="0549a-199">When this flag is used with the combination of MCI\_DGV\_SETAUDIO\_VALUE and MCI\_DGV\_SETAUDIO\_VOLUME, it sets the volume of the right audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-200"><span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>\_ \_ valor SETAUDIO de MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="0549a-200"><span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>MCI\_DGV\_SETAUDIO\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="0549a-201">Se especifica un valor en el miembro **dwValue** de la estructura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="0549a-201">A value is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="0549a-202">El significado del valor se especifica mediante la constante definida para la marca MCI \_ DGV \_ SETAUDIO \_ Item.</span><span class="sxs-lookup"><span data-stu-id="0549a-202">The meaning of the value is specified by the constant defined for the MCI\_DGV\_SETAUDIO\_ITEM flag.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-203"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>Desactivación de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="0549a-203"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="0549a-204">Deshabilita el canal de audio especificado.</span><span class="sxs-lookup"><span data-stu-id="0549a-204">Disables the specified audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-205"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activado \_</span><span class="sxs-lookup"><span data-stu-id="0549a-205"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="0549a-206">Habilita el canal de audio especificado.</span><span class="sxs-lookup"><span data-stu-id="0549a-206">Enables the specified audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="0549a-207"><span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>salida de MCI \_ SETAUDIO \_</span><span class="sxs-lookup"><span data-stu-id="0549a-207"><span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>MCI\_SETAUDIO\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="0549a-208">Modifica la marca de graves, agudos o de volumen para que solo modifique la señal de reproducción y no lo que se grabe.</span><span class="sxs-lookup"><span data-stu-id="0549a-208">Modifies the bass, treble, or volume flag so that it modifies only the played signal and not what is recorded.</span></span> <span data-ttu-id="0549a-209">Si es posible, es el valor predeterminado al supervisar la entrada.</span><span class="sxs-lookup"><span data-stu-id="0549a-209">If possible, this is the default when monitoring the input.</span></span>

</dd> </dl>

<span data-ttu-id="0549a-210">En el caso de los dispositivos de vídeo digital, el parámetro *lpSetAudio* apunta a una estructura [**MCI \_ DGV \_ SETAUDIO \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="0549a-210">For digital-video devices, the *lpSetAudio* parameter points to an [**MCI\_DGV\_SETAUDIO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) structure.</span></span>

<span data-ttu-id="0549a-211">Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="0549a-211">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="0549a-212"><span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>\_registro de \_ SETAUDIO de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="0549a-212"><span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>MCI\_VCR\_SETAUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="0549a-213">Establece la grabación de audio en activado o desactivado, que se usa junto con una de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="0549a-213">Sets the audio recording to on or off, which is used in conjunction with one of following flags:</span></span>

<span data-ttu-id="0549a-214">MCI \_ activado \_</span><span class="sxs-lookup"><span data-stu-id="0549a-214">MCI\_SET\_ON</span></span>

<span data-ttu-id="0549a-215">Grabación de audio activada.</span><span class="sxs-lookup"><span data-stu-id="0549a-215">Audio recording on.</span></span>

<span data-ttu-id="0549a-216">Desactivación de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="0549a-216">MCI\_SET\_OFF</span></span>

<span data-ttu-id="0549a-217">Grabación de audio desactivada.</span><span class="sxs-lookup"><span data-stu-id="0549a-217">Audio recording off.</span></span> <span data-ttu-id="0549a-218">Es posible que sea necesario desactivar primero la grabación de ensamblados (con el comando [MCI \_ set](mci-set.md) con la \_ marca de montaje del conjunto de VCR de MCI \_ \_ \_ establecida en OFF) antes de que se pueda desactivar la grabación de audio.</span><span class="sxs-lookup"><span data-stu-id="0549a-218">It might be necessary to first turn off the assemble recording (using the [MCI\_SET](mci-set.md) command with the MCI\_VCR\_SET\_ASSEMBLE\_RECORD flag set to off) before the audio recording can be turned off.</span></span>

<span data-ttu-id="0549a-219">pista de MCI \_</span><span class="sxs-lookup"><span data-stu-id="0549a-219">MCI\_TRACK</span></span>

<span data-ttu-id="0549a-220">El miembro **dwTrack** de la estructura identificada por *lpSetAudio* especifica qué pista se ve afectada por el comando.</span><span class="sxs-lookup"><span data-stu-id="0549a-220">The **dwTrack** member of the structure identified by *lpSetAudio* specifies which track is affected by the command.</span></span>

<span data-ttu-id="0549a-221">\_origen de \_ SETAUDIO de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="0549a-221">MCI\_VCR\_SETAUDIO\_SOURCE</span></span>

<span data-ttu-id="0549a-222">Establece el origen de audio.</span><span class="sxs-lookup"><span data-stu-id="0549a-222">Sets the audio source.</span></span> <span data-ttu-id="0549a-223">Esta marca debe usarse con la SETAUDIO de VCR de MCI \_ \_ \_ para marcar.</span><span class="sxs-lookup"><span data-stu-id="0549a-223">This flag must be used with the MCI\_VCR\_SETAUDIO\_TO flag.</span></span>

<span data-ttu-id="0549a-224">\_monitor de \_ SETAUDIO de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="0549a-224">MCI\_VCR\_SETAUDIO\_MONITOR</span></span>

<span data-ttu-id="0549a-225">Establece el monitor de origen de audio.</span><span class="sxs-lookup"><span data-stu-id="0549a-225">Sets the audio source monitor.</span></span> <span data-ttu-id="0549a-226">Esta marca debe usarse con la SETAUDIO de VCR de MCI \_ \_ \_ para marcar.</span><span class="sxs-lookup"><span data-stu-id="0549a-226">This flag must be used with the MCI\_VCR\_SETAUDIO\_TO flag.</span></span>

<span data-ttu-id="0549a-227">MCI \_ VCR \_ SETAUDIO \_</span><span class="sxs-lookup"><span data-stu-id="0549a-227">MCI\_VCR\_SETAUDIO\_TO</span></span>

<span data-ttu-id="0549a-228">El miembro **dwTo** de la estructura identificada por *lpSetAudio* contiene una constante que describe el tipo de entrada o entrada supervisada.</span><span class="sxs-lookup"><span data-stu-id="0549a-228">The **dwTo** member of the structure identified by *lpSetAudio* contains a constant describing the type of input or monitored input.</span></span> <span data-ttu-id="0549a-229">Debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="0549a-229">It must be one of the following:</span></span>

<span data-ttu-id="0549a-230"><dl> <dd></span><span class="sxs-lookup"><span data-stu-id="0549a-230"><dl> <dd></span></span>

<span data-ttu-id="0549a-231">\_ \_ \_ sintonizador de tipo \_ src VCR de MCI</span><span class="sxs-lookup"><span data-stu-id="0549a-231">MCI\_VCR\_SRC\_TYPE\_TUNER</span></span>

<span data-ttu-id="0549a-232">El tipo es sintonizador.</span><span class="sxs-lookup"><span data-stu-id="0549a-232">Type is tuner.</span></span>

</dd> <dd>

<span data-ttu-id="0549a-233">\_línea de \_ \_ tipo src VCR de \_ MCI</span><span class="sxs-lookup"><span data-stu-id="0549a-233">MCI\_VCR\_SRC\_TYPE\_LINE</span></span>

<span data-ttu-id="0549a-234">El tipo es line.</span><span class="sxs-lookup"><span data-stu-id="0549a-234">Type is line.</span></span>

</dd> <dd>

<span data-ttu-id="0549a-235">tipo de origen de VCR de MCI \_ \_ \_ \_ AUX</span><span class="sxs-lookup"><span data-stu-id="0549a-235">MCI\_VCR\_SRC\_TYPE\_AUX</span></span>

<span data-ttu-id="0549a-236">El tipo es auxiliar.</span><span class="sxs-lookup"><span data-stu-id="0549a-236">Type is auxiliary.</span></span>

</dd> <dd>

<span data-ttu-id="0549a-237">tipo de origen de VCR de MCI \_ \_ \_ \_ genérico</span><span class="sxs-lookup"><span data-stu-id="0549a-237">MCI\_VCR\_SRC\_TYPE\_GENERIC</span></span>

<span data-ttu-id="0549a-238">El tipo es genérico.</span><span class="sxs-lookup"><span data-stu-id="0549a-238">Type is generic.</span></span>

</dd> <dd>

<span data-ttu-id="0549a-239">Desactivación de \_ \_ tipo src VCR \_ de MCI \_</span><span class="sxs-lookup"><span data-stu-id="0549a-239">MCI\_VCR\_SRC\_TYPE\_MUTE</span></span>

<span data-ttu-id="0549a-240">El tipo es MUTE.</span><span class="sxs-lookup"><span data-stu-id="0549a-240">Type is mute.</span></span> <span data-ttu-id="0549a-241">Esto solo se puede usar con la \_ marca de \_ origen SETAUDIO VCR VCR \_ .</span><span class="sxs-lookup"><span data-stu-id="0549a-241">This can be used only with the MCI\_VCR\_SETAUDIO\_SOURCE flag.</span></span>

</dd> <dd>

<span data-ttu-id="0549a-242">\_salida de \_ tipo de origen de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="0549a-242">MCI\_VCR\_SRC\_TYPE\_OUTPUT</span></span>

<span data-ttu-id="0549a-243">El tipo es output.</span><span class="sxs-lookup"><span data-stu-id="0549a-243">Type is output.</span></span>

</dd> <dd>

<span data-ttu-id="0549a-244">\_ \_ número SETAUDIO de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="0549a-244">MCI\_VCR\_SETAUDIO\_NUMBER</span></span>

<span data-ttu-id="0549a-245">El miembro dwNumber de la estructura identificada por lpSetAudio contiene la entrada de audio (del tipo especificado en el miembro dwTo) que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="0549a-245">The dwNumber member of the structure identified by lpSetAudio contains the audio input (of the type specified in the dwTo member) to use.</span></span>

</dd> </dl> </dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="0549a-246">En el caso de los dispositivos VCR, el parámetro *lpSetAudio* apunta a una estructura [**MCI \_ VCR \_ SETAUDIO \_ parms**](mci-vcr-setaudio-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="0549a-246">For VCR devices, the *lpSetAudio* parameter points to an [**MCI\_VCR\_SETAUDIO\_PARMS**](mci-vcr-setaudio-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0549a-247">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0549a-247">Requirements</span></span>



| <span data-ttu-id="0549a-248">Requisito</span><span class="sxs-lookup"><span data-stu-id="0549a-248">Requirement</span></span> | <span data-ttu-id="0549a-249">Value</span><span class="sxs-lookup"><span data-stu-id="0549a-249">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0549a-250">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0549a-250">Minimum supported client</span></span><br/> | <span data-ttu-id="0549a-251">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0549a-251">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0549a-252">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0549a-252">Minimum supported server</span></span><br/> | <span data-ttu-id="0549a-253">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0549a-253">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0549a-254">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0549a-254">Header</span></span><br/>                   | <dl> <span data-ttu-id="0549a-255"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0549a-255"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0549a-256">Vea también</span><span class="sxs-lookup"><span data-stu-id="0549a-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0549a-257">MCI</span><span class="sxs-lookup"><span data-stu-id="0549a-257">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0549a-258">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="0549a-258">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

