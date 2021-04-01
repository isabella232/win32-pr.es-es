---
title: comando grabar
description: El comando grabar inicia la grabación de datos. Los dispositivos VCR y de onda-audio reconocen este comando. Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo implementan.
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- comando grabar Windows multimedia
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39d3659d4577517726260f948563cd31ecc07bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905018"
---
# <a name="record-command"></a><span data-ttu-id="5d18a-106">comando grabar</span><span class="sxs-lookup"><span data-stu-id="5d18a-106">record command</span></span>

<span data-ttu-id="5d18a-107">El comando grabar inicia la grabación de datos.</span><span class="sxs-lookup"><span data-stu-id="5d18a-107">The record command starts recording data.</span></span> <span data-ttu-id="5d18a-108">Los dispositivos VCR y de onda-audio reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="5d18a-108">VCR and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="5d18a-109">Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo implementan.</span><span class="sxs-lookup"><span data-stu-id="5d18a-109">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="5d18a-110">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="5d18a-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("record %s %s %s"), 
  lpszDeviceID, 
  lpszRecordFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="5d18a-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d18a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d18a-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="5d18a-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5d18a-113">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="5d18a-113">Identifier of an MCI device.</span></span> <span data-ttu-id="5d18a-114">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d18a-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="5d18a-115"><span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*</span><span class="sxs-lookup"><span data-stu-id="5d18a-115"><span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5d18a-116">Marca para la grabación de datos.</span><span class="sxs-lookup"><span data-stu-id="5d18a-116">Flag for recording data.</span></span> <span data-ttu-id="5d18a-117">En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **registro** y las marcas usadas por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="5d18a-117">The following table lists device types that recognize the **record** command and the flags used by each type.</span></span>



| <span data-ttu-id="5d18a-118">Value</span><span class="sxs-lookup"><span data-stu-id="5d18a-118">Value</span></span>        | <span data-ttu-id="5d18a-119">Significado</span><span class="sxs-lookup"><span data-stu-id="5d18a-119">Meaning</span></span>                                                | <span data-ttu-id="5d18a-120">Significado</span><span class="sxs-lookup"><span data-stu-id="5d18a-120">Meaning</span></span>                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="5d18a-121">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="5d18a-121">digitalvideo</span></span> | <span data-ttu-id="5d18a-122">*secuencia* de flujo de audio de *rectángulo* desde la *posición* de espera</span><span class="sxs-lookup"><span data-stu-id="5d18a-122">at *rectangle* audio stream *stream* from *position* hold</span></span> | <span data-ttu-id="5d18a-123">insertar la *secuencia* de flujo de vídeo sobrescribir en la *posición*</span><span class="sxs-lookup"><span data-stu-id="5d18a-123">insert overwrite to *position* video stream *stream*</span></span> |
| <span data-ttu-id="5d18a-124">sequencer</span><span class="sxs-lookup"><span data-stu-id="5d18a-124">sequencer</span></span>    | <span data-ttu-id="5d18a-125">desde la *posición* Insert</span><span class="sxs-lookup"><span data-stu-id="5d18a-125">from *position* insert</span></span>                                  | <span data-ttu-id="5d18a-126">sobrescribir en *posición*</span><span class="sxs-lookup"><span data-stu-id="5d18a-126">overwrite to *position*</span></span>                             |
| <span data-ttu-id="5d18a-127">vídeos</span><span class="sxs-lookup"><span data-stu-id="5d18a-127">vcr</span></span>          | <span data-ttu-id="5d18a-128">en *el momento* de la inicialización de la *posición*</span><span class="sxs-lookup"><span data-stu-id="5d18a-128">at *time* from *position* initialize</span></span>                     | <span data-ttu-id="5d18a-129">Insertar Sobrescribir en *posición*</span><span class="sxs-lookup"><span data-stu-id="5d18a-129">insert overwrite to *position*</span></span>                      |
| <span data-ttu-id="5d18a-130">waveaudio</span><span class="sxs-lookup"><span data-stu-id="5d18a-130">waveaudio</span></span>    | <span data-ttu-id="5d18a-131">desde la *posición* Insert</span><span class="sxs-lookup"><span data-stu-id="5d18a-131">from *position* insert</span></span>                                  | <span data-ttu-id="5d18a-132">sobrescribir en *posición*</span><span class="sxs-lookup"><span data-stu-id="5d18a-132">overwrite to *position*</span></span>                             |



 

<span data-ttu-id="5d18a-133">En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszRecordFlags** y su significado.</span><span class="sxs-lookup"><span data-stu-id="5d18a-133">The following table lists the flags that can be specified in the **lpszRecordFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="5d18a-134">Value</span><span class="sxs-lookup"><span data-stu-id="5d18a-134">Value</span></span>                 | <span data-ttu-id="5d18a-135">Significado</span><span class="sxs-lookup"><span data-stu-id="5d18a-135">Meaning</span></span>                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d18a-136">en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="5d18a-136">at *rectangle*</span></span>        | <span data-ttu-id="5d18a-137">Especifica una región rectangular de la entrada externa usada como origen para los píxeles comprimidos y guardados.</span><span class="sxs-lookup"><span data-stu-id="5d18a-137">Specifies a rectangular region of the external input used as the source for the pixels compressed and saved.</span></span> <span data-ttu-id="5d18a-138">Si no se especifica, el rectángulo tiene como valor predeterminado el rectángulo especificado para [Put](put.md) "vídeo".</span><span class="sxs-lookup"><span data-stu-id="5d18a-138">If not specified, the rectangle defaults to the rectangle specified for [put](put.md) "video".</span></span> <span data-ttu-id="5d18a-139">Cuando se establece de manera diferente del rectángulo de "vídeo", la imagen mostrada no es lo que se graba.</span><span class="sxs-lookup"><span data-stu-id="5d18a-139">When it is set differently from the "video" rectangle, the displayed image is not what is recorded.</span></span> |
| <span data-ttu-id="5d18a-140">a la *hora*</span><span class="sxs-lookup"><span data-stu-id="5d18a-140">at *time*</span></span>             | <span data-ttu-id="5d18a-141">Indica que el dispositivo debe comenzar a ejecutar este comando, o bien, si el dispositivo está preparado, cuando comienza el comando de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="5d18a-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="5d18a-142">Para obtener más información, consulte el comando [CUE](cue.md) .</span><span class="sxs-lookup"><span data-stu-id="5d18a-142">For more information, see the [cue](cue.md) command.</span></span>                                                                                                                             |
| <span data-ttu-id="5d18a-143">*secuencia* de flujo de audio</span><span class="sxs-lookup"><span data-stu-id="5d18a-143">audio stream *stream*</span></span> | <span data-ttu-id="5d18a-144">Especifica la secuencia de audio utilizada para la grabación.</span><span class="sxs-lookup"><span data-stu-id="5d18a-144">Specifies the audio stream used for recording.</span></span> <span data-ttu-id="5d18a-145">Si no se especifica esta marca y el formato de archivo no define un valor predeterminado, se registra en el flujo que es físicamente primero.</span><span class="sxs-lookup"><span data-stu-id="5d18a-145">If this flag is not specified and the file format does not define a default, it is recorded into the stream that is physically first.</span></span>                                                                                                                             |
| <span data-ttu-id="5d18a-146">desde la *posición*</span><span class="sxs-lookup"><span data-stu-id="5d18a-146">from *position*</span></span>       | <span data-ttu-id="5d18a-147">Especifica una posición inicial para la grabación.</span><span class="sxs-lookup"><span data-stu-id="5d18a-147">Specifies a starting position for the recording.</span></span> <span data-ttu-id="5d18a-148">Si no se especifica la marca "desde", el dispositivo inicia la grabación en la posición actual.</span><span class="sxs-lookup"><span data-stu-id="5d18a-148">If the "from" flag is not specified, the device starts recording at the current position.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="5d18a-149">contener</span><span class="sxs-lookup"><span data-stu-id="5d18a-149">hold</span></span>                  | <span data-ttu-id="5d18a-150">Inmoviliza la imagen cuando ha terminado la grabación en lugar de mostrar vídeo en directo.</span><span class="sxs-lookup"><span data-stu-id="5d18a-150">Freezes the image when recording has finished instead of showing live video.</span></span> <span data-ttu-id="5d18a-151">Cuando se detiene la grabación, se realiza un comando de [supervisión](monitor.md) automática del "archivo".</span><span class="sxs-lookup"><span data-stu-id="5d18a-151">When recording stops, an automatic [monitor](monitor.md) "file" command is performed.</span></span> <span data-ttu-id="5d18a-152">Para volver a vídeo en directo, emita el comando **supervisar** "entrada".</span><span class="sxs-lookup"><span data-stu-id="5d18a-152">To return to live video, issue the **monitor** "input" command.</span></span>                                                                              |
| <span data-ttu-id="5d18a-153">initialize</span><span class="sxs-lookup"><span data-stu-id="5d18a-153">initialize</span></span>            | <span data-ttu-id="5d18a-154">Inicialice la cinta (multimedia), que implica el registro del código de tiempo (si es posible) para vídeo y audio en blanco.</span><span class="sxs-lookup"><span data-stu-id="5d18a-154">Initialize the tape (media), which involves recording timecode (if possible) for blank video and audio.</span></span> <span data-ttu-id="5d18a-155">Este comando puede tardar varias horas si se debe inicializar toda la cinta.</span><span class="sxs-lookup"><span data-stu-id="5d18a-155">This command might take several hours if the entire tape must be initialized.</span></span>                                                                                                                            |
| <span data-ttu-id="5d18a-156">insert</span><span class="sxs-lookup"><span data-stu-id="5d18a-156">insert</span></span>                | <span data-ttu-id="5d18a-157">Especifica que los nuevos datos se agregan al archivo en la posición actual.</span><span class="sxs-lookup"><span data-stu-id="5d18a-157">Specifies that new data is added to the file at the current position.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="5d18a-158">sobrescribir</span><span class="sxs-lookup"><span data-stu-id="5d18a-158">overwrite</span></span>             | <span data-ttu-id="5d18a-159">Especifica que los nuevos datos reemplazarán los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="5d18a-159">Specifies that new data will replace data in the file.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="5d18a-160">para *colocar*</span><span class="sxs-lookup"><span data-stu-id="5d18a-160">to *position*</span></span>         | <span data-ttu-id="5d18a-161">Especifica una posición final para la grabación.</span><span class="sxs-lookup"><span data-stu-id="5d18a-161">Specifies an ending position for the recording.</span></span> <span data-ttu-id="5d18a-162">Si no se especifica la marca "para", el dispositivo registra hasta que recibe un comando [detener](stop.md) o [pausar](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="5d18a-162">If the "to" flag is not specified, the device records until it receives a [stop](stop.md) or [pause](pause.md) command.</span></span>                                                                                                                                        |
| <span data-ttu-id="5d18a-163">*secuencia* de flujo de vídeo</span><span class="sxs-lookup"><span data-stu-id="5d18a-163">video stream *stream*</span></span> | <span data-ttu-id="5d18a-164">Especifica la secuencia de vídeo que se usa para la grabación.</span><span class="sxs-lookup"><span data-stu-id="5d18a-164">Specifies the video stream used for recording.</span></span> <span data-ttu-id="5d18a-165">Si no se especifica y el formato de archivo no define un valor predeterminado, se registra en el flujo que es físicamente primero.</span><span class="sxs-lookup"><span data-stu-id="5d18a-165">If this is not specified and the file format does not define a default, then it is recorded into the stream that is physically first.</span></span>                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="5d18a-166"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="5d18a-166"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5d18a-167">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="5d18a-167">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="5d18a-168">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="5d18a-168">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="5d18a-169">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5d18a-169">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d18a-170">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d18a-170">Return Value</span></span>

<span data-ttu-id="5d18a-171">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5d18a-171">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d18a-172">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d18a-172">Remarks</span></span>

<span data-ttu-id="5d18a-173">La grabación se detiene cuando se emite un comando [detener](stop.md) o [pausar](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="5d18a-173">The recording stops when a [stop](stop.md) or [pause](pause.md) command is issued.</span></span> <span data-ttu-id="5d18a-174">En el caso del controlador MCIWAVE, todos los datos registrados después de abrir un archivo se descartan si el archivo se cierra sin guardarlo.</span><span class="sxs-lookup"><span data-stu-id="5d18a-174">For the MCIWAVE driver, all data recorded after a file is opened is discarded if the file is closed without saving it.</span></span>

<span data-ttu-id="5d18a-175">Antes de emitir cualquier comando que use valores de posición, debe establecer el formato de hora deseado mediante el comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="5d18a-175">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span> <span data-ttu-id="5d18a-176">Las pistas que se van a grabar se especifican mediante los comandos [settimecode](settimecode.md) "registro", "ensamblar registro", [setvideo](setvideo.md) "registro" y [SetAudio](setaudio.md) "registro".</span><span class="sxs-lookup"><span data-stu-id="5d18a-176">The tracks to be recorded are specified by the [settimecode](settimecode.md) "record", set "assemble record", [setvideo](setvideo.md) "record", and [setaudio](setaudio.md) "record" commands.</span></span>

## <a name="examples"></a><span data-ttu-id="5d18a-177">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5d18a-177">Examples</span></span>

<span data-ttu-id="5d18a-178">El comando siguiente inicia la grabación en la posición actual.</span><span class="sxs-lookup"><span data-stu-id="5d18a-178">The following command starts recording at the current position.</span></span>

``` syntax
record mysound
```

## <a name="requirements"></a><span data-ttu-id="5d18a-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d18a-179">Requirements</span></span>



| <span data-ttu-id="5d18a-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d18a-180">Requirement</span></span> | <span data-ttu-id="5d18a-181">Value</span><span class="sxs-lookup"><span data-stu-id="5d18a-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="5d18a-182">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d18a-182">Minimum supported client</span></span><br/> | <span data-ttu-id="5d18a-183">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5d18a-183">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5d18a-184">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d18a-184">Minimum supported server</span></span><br/> | <span data-ttu-id="5d18a-185">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5d18a-185">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5d18a-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d18a-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d18a-187">MCI</span><span class="sxs-lookup"><span data-stu-id="5d18a-187">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5d18a-188">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="5d18a-188">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="5d18a-189">indicación</span><span class="sxs-lookup"><span data-stu-id="5d18a-189">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="5d18a-190">control</span><span class="sxs-lookup"><span data-stu-id="5d18a-190">monitor</span></span>](monitor.md)
</dt> <dt>

[<span data-ttu-id="5d18a-191">pause</span><span class="sxs-lookup"><span data-stu-id="5d18a-191">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="5d18a-192">pondrán</span><span class="sxs-lookup"><span data-stu-id="5d18a-192">put</span></span>](put.md)
</dt> <dt>

[<span data-ttu-id="5d18a-193">set</span><span class="sxs-lookup"><span data-stu-id="5d18a-193">set</span></span>](set.md)
</dt> <dt>

[<span data-ttu-id="5d18a-194">setaudio</span><span class="sxs-lookup"><span data-stu-id="5d18a-194">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="5d18a-195">settimecode</span><span class="sxs-lookup"><span data-stu-id="5d18a-195">settimecode</span></span>](settimecode.md)
</dt> <dt>

[<span data-ttu-id="5d18a-196">setvideo</span><span class="sxs-lookup"><span data-stu-id="5d18a-196">setvideo</span></span>](setvideo.md)
</dt> <dt>

[<span data-ttu-id="5d18a-197">stop</span><span class="sxs-lookup"><span data-stu-id="5d18a-197">stop</span></span>](stop.md)
</dt> </dl>

 

