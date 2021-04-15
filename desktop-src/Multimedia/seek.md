---
title: comando de búsqueda
description: El comando Seek se desplaza a la posición y se detiene especificados. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, VCR, Videodisc y de onda-audio reconocen este comando.
ms.assetid: e9e8ca14-d181-4f29-b4d3-c7f5b0301164
keywords:
- comando Buscar multimedia de Windows
topic_type:
- apiref
api_name:
- seek
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40f3467d328e161245e77217b4ce6edfa9665ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421946"
---
# <a name="seek-command"></a><span data-ttu-id="e11f9-105">comando de búsqueda</span><span class="sxs-lookup"><span data-stu-id="e11f9-105">seek command</span></span>

<span data-ttu-id="e11f9-106">El comando Seek se desplaza a la posición y se detiene especificados.</span><span class="sxs-lookup"><span data-stu-id="e11f9-106">The seek command moves to the specified position and stops.</span></span> <span data-ttu-id="e11f9-107">Los dispositivos de audio de CD, digital-video, MIDI Sequencer, VCR, Videodisc y de onda-audio reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="e11f9-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="e11f9-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="e11f9-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("seek %s %s %s"), 
  lpszDeviceID, 
  lpszSeekFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="e11f9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e11f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e11f9-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="e11f9-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e11f9-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="e11f9-111">Identifier of an MCI device.</span></span> <span data-ttu-id="e11f9-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e11f9-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="e11f9-113"><span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*</span><span class="sxs-lookup"><span data-stu-id="e11f9-113"><span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e11f9-114">Marca que se va a mover a una posición especificada.</span><span class="sxs-lookup"><span data-stu-id="e11f9-114">Flag for moving to a specified position.</span></span> <span data-ttu-id="e11f9-115">En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **Seek** y las marcas usadas por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="e11f9-115">The following table lists device types that recognize the **seek** command and the flags used by each type.</span></span>



| <span data-ttu-id="e11f9-116">Value</span><span class="sxs-lookup"><span data-stu-id="e11f9-116">Value</span></span>        | <span data-ttu-id="e11f9-117">Significado</span><span class="sxs-lookup"><span data-stu-id="e11f9-117">Meaning</span></span>                          | <span data-ttu-id="e11f9-118">Significado</span><span class="sxs-lookup"><span data-stu-id="e11f9-118">Meaning</span></span>                      |
|--------------|----------------------------------|------------------------------|
| <span data-ttu-id="e11f9-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="e11f9-119">cdaudio</span></span>      | <span data-ttu-id="e11f9-120">hasta el final de la *posición*</span><span class="sxs-lookup"><span data-stu-id="e11f9-120">to end to *position*</span></span>             | <span data-ttu-id="e11f9-121">para iniciar</span><span class="sxs-lookup"><span data-stu-id="e11f9-121">to start</span></span>                     |
| <span data-ttu-id="e11f9-122">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="e11f9-122">digitalvideo</span></span> | <span data-ttu-id="e11f9-123">hasta el final de la *posición*</span><span class="sxs-lookup"><span data-stu-id="e11f9-123">to end to *position*</span></span>             | <span data-ttu-id="e11f9-124">para iniciar</span><span class="sxs-lookup"><span data-stu-id="e11f9-124">to start</span></span>                     |
| <span data-ttu-id="e11f9-125">sequencer</span><span class="sxs-lookup"><span data-stu-id="e11f9-125">sequencer</span></span>    | <span data-ttu-id="e11f9-126">hasta el final de la *posición*</span><span class="sxs-lookup"><span data-stu-id="e11f9-126">to end to *position*</span></span>             | <span data-ttu-id="e11f9-127">para iniciar</span><span class="sxs-lookup"><span data-stu-id="e11f9-127">to start</span></span>                     |
| <span data-ttu-id="e11f9-128">vídeos</span><span class="sxs-lookup"><span data-stu-id="e11f9-128">vcr</span></span>          | <span data-ttu-id="e11f9-129">en marca de marca de *tiempo* *\_ número* inverso</span><span class="sxs-lookup"><span data-stu-id="e11f9-129">at *time* mark *mark\_num* reverse</span></span> | <span data-ttu-id="e11f9-130">para finalizar la *posición* de inicio</span><span class="sxs-lookup"><span data-stu-id="e11f9-130">to end to *position* to start</span></span> |
| <span data-ttu-id="e11f9-131">videodisco</span><span class="sxs-lookup"><span data-stu-id="e11f9-131">videodisc</span></span>    | <span data-ttu-id="e11f9-132">invertir hasta el final</span><span class="sxs-lookup"><span data-stu-id="e11f9-132">reverse to end</span></span>                   | <span data-ttu-id="e11f9-133">para *colocar* en Start</span><span class="sxs-lookup"><span data-stu-id="e11f9-133">to *position* to start</span></span>        |
| <span data-ttu-id="e11f9-134">waveaudio</span><span class="sxs-lookup"><span data-stu-id="e11f9-134">waveaudio</span></span>    | <span data-ttu-id="e11f9-135">hasta el final de la *posición*</span><span class="sxs-lookup"><span data-stu-id="e11f9-135">to end to *position*</span></span>             | <span data-ttu-id="e11f9-136">para iniciar</span><span class="sxs-lookup"><span data-stu-id="e11f9-136">to start</span></span>                     |



 

<span data-ttu-id="e11f9-137">En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszSeekFlags** y su significado.</span><span class="sxs-lookup"><span data-stu-id="e11f9-137">The following table lists the flags that can be specified in the **lpszSeekFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="e11f9-138">Value</span><span class="sxs-lookup"><span data-stu-id="e11f9-138">Value</span></span>            | <span data-ttu-id="e11f9-139">Significado</span><span class="sxs-lookup"><span data-stu-id="e11f9-139">Meaning</span></span>                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e11f9-140">a la *hora*</span><span class="sxs-lookup"><span data-stu-id="e11f9-140">at *time*</span></span>        | <span data-ttu-id="e11f9-141">Indica que el dispositivo debe comenzar a ejecutar este comando, o bien, si el dispositivo está preparado, cuando comienza el comando de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="e11f9-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="e11f9-142">Para obtener más información, consulte el comando [CUE](cue.md) .</span><span class="sxs-lookup"><span data-stu-id="e11f9-142">For more information, see the [cue](cue.md) command.</span></span>                             |
| <span data-ttu-id="e11f9-143">marcar *\_ núm* .</span><span class="sxs-lookup"><span data-stu-id="e11f9-143">mark *mark\_num*</span></span> | <span data-ttu-id="e11f9-144">Busca la marca relativa indicada por *Mark \_ NUM*, que debe ser un valor entero positivo.</span><span class="sxs-lookup"><span data-stu-id="e11f9-144">Seeks to the relative mark indicated by *mark\_num*, which must be a positive integer value.</span></span> <span data-ttu-id="e11f9-145">Las marcas son señales escritas en la cinta VCR con el comando [Mark](mark.md) y se usan para la búsqueda de alta velocidad.</span><span class="sxs-lookup"><span data-stu-id="e11f9-145">Marks are signals written to the VCR tape using the [mark](mark.md) command and are used for high-speed searching.</span></span> |
| <span data-ttu-id="e11f9-146">reverse</span><span class="sxs-lookup"><span data-stu-id="e11f9-146">reverse</span></span>          | <span data-ttu-id="e11f9-147">Indica que la dirección de búsqueda en los videodiscos VCR y CAV está hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="e11f9-147">Indicates that the seek direction on VCRs and CAV videodiscs is backward.</span></span> <span data-ttu-id="e11f9-148">Esta marca no es válida si se especifica la marca "to".</span><span class="sxs-lookup"><span data-stu-id="e11f9-148">This flag is invalid if the "to" flag is specified.</span></span> <span data-ttu-id="e11f9-149">En el caso de los VCR, esta marca se debe usar con el marcador "Mark".</span><span class="sxs-lookup"><span data-stu-id="e11f9-149">For VCRs, this flag must be used with the "mark" flag.</span></span>                             |
| <span data-ttu-id="e11f9-150">hasta el final</span><span class="sxs-lookup"><span data-stu-id="e11f9-150">to end</span></span>           | <span data-ttu-id="e11f9-151">Busca el final del contenido.</span><span class="sxs-lookup"><span data-stu-id="e11f9-151">Seeks to the end of the content.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="e11f9-152">para *colocar*</span><span class="sxs-lookup"><span data-stu-id="e11f9-152">to *position*</span></span>    | <span data-ttu-id="e11f9-153">Especifica la posición para detener la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e11f9-153">Specifies the position to stop the seek.</span></span> <span data-ttu-id="e11f9-154">En el caso de los dispositivos **cdaudio** , MCI devuelve un error fuera de intervalo si la posición especificada es mayor que la longitud del disco.</span><span class="sxs-lookup"><span data-stu-id="e11f9-154">For **cdaudio** devices, MCI returns an out-of-range error if the specified position is greater than the length of the disc.</span></span>                                            |
| <span data-ttu-id="e11f9-155">para iniciar</span><span class="sxs-lookup"><span data-stu-id="e11f9-155">to start</span></span>         | <span data-ttu-id="e11f9-156">Busca el inicio del contenido.</span><span class="sxs-lookup"><span data-stu-id="e11f9-156">Seeks to the start of the content.</span></span>                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="e11f9-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="e11f9-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e11f9-158">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="e11f9-158">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="e11f9-159">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="e11f9-159">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="e11f9-160">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e11f9-160">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e11f9-161">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e11f9-161">Return Value</span></span>

<span data-ttu-id="e11f9-162">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e11f9-162">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e11f9-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e11f9-163">Remarks</span></span>

<span data-ttu-id="e11f9-164">Antes de emitir cualquier comando que use valores de posición, debe establecer el formato de hora deseado mediante el comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="e11f9-164">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

<span data-ttu-id="e11f9-165">Los dispositivos de vídeo digital admiten dos modos de búsqueda, que se pueden cambiar mediante el comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="e11f9-165">Digital-video devices support two seek modes, which you can change by using the [set](set.md) command.</span></span> <span data-ttu-id="e11f9-166">El modo "Buscar exactamente en" hace que el comando de búsqueda se mueva al marco especificado.</span><span class="sxs-lookup"><span data-stu-id="e11f9-166">The "seek exactly on" mode causes the seek command to move to the specified frame.</span></span> <span data-ttu-id="e11f9-167">El modo "Buscar exactamente desactivado" hace que el comando Buscar se mueva al fotograma clave más cercano antes del marco especificado.</span><span class="sxs-lookup"><span data-stu-id="e11f9-167">The "seek exactly off" mode causes the seek command to move to the closest key frame prior to the specified frame.</span></span>

<span data-ttu-id="e11f9-168">Si se está reproduciendo un dispositivo de audio de CD cuando se emite el comando de búsqueda, se detiene la reproducción.</span><span class="sxs-lookup"><span data-stu-id="e11f9-168">If a CD audio device is playing when the seek command is issued, playback is stopped.</span></span> <span data-ttu-id="e11f9-169">Cuando el comando de búsqueda se emite con un dispositivo de videodisco, el dispositivo realiza búsquedas mediante el uso del avance rápido o el desactivado rápido con vídeo y audio.</span><span class="sxs-lookup"><span data-stu-id="e11f9-169">When the seek command is issued with a videodisc device, the device searches using fast forward or fast reverse with video and audio off.</span></span>

<span data-ttu-id="e11f9-170">Cuando el comando de búsqueda se emite con un dispositivo de audio de forma de onda, el comportamiento depende del tamaño de la muestra.</span><span class="sxs-lookup"><span data-stu-id="e11f9-170">When the seek command is issued with a waveform-audio device, the behavior depends on the sample size.</span></span> <span data-ttu-id="e11f9-171">Si el tamaño de la muestra es de 16 bits o superior, la búsqueda se desplaza al principio del ejemplo más cercano cuando una posición especificada no coincide con el inicio de un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e11f9-171">If the sample size is 16 bits or greater, seek moves to the beginning of the nearest sample when a specified position does not coincide with the start of a sample.</span></span>

## <a name="examples"></a><span data-ttu-id="e11f9-172">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e11f9-172">Examples</span></span>

<span data-ttu-id="e11f9-173">El siguiente comando busca el inicio del archivo multimedia asociado con el dispositivo "de".</span><span class="sxs-lookup"><span data-stu-id="e11f9-173">The following command seeks to the start of the media file associated with the "mysound" device.</span></span>

``` syntax
seek mysound to start
```

## <a name="requirements"></a><span data-ttu-id="e11f9-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e11f9-174">Requirements</span></span>



| <span data-ttu-id="e11f9-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="e11f9-175">Requirement</span></span> | <span data-ttu-id="e11f9-176">Value</span><span class="sxs-lookup"><span data-stu-id="e11f9-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e11f9-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e11f9-177">Minimum supported client</span></span><br/> | <span data-ttu-id="e11f9-178">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e11f9-178">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e11f9-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e11f9-179">Minimum supported server</span></span><br/> | <span data-ttu-id="e11f9-180">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e11f9-180">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e11f9-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="e11f9-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e11f9-182">MCI</span><span class="sxs-lookup"><span data-stu-id="e11f9-182">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e11f9-183">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="e11f9-183">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="e11f9-184">indicación</span><span class="sxs-lookup"><span data-stu-id="e11f9-184">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="e11f9-185">Rasa</span><span class="sxs-lookup"><span data-stu-id="e11f9-185">mark</span></span>](mark.md)
</dt> <dt>

[<span data-ttu-id="e11f9-186">set</span><span class="sxs-lookup"><span data-stu-id="e11f9-186">set</span></span>](set.md)
</dt> </dl>

 

