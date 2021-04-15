---
title: reproducir comando
description: El comando PLAY comienza a reproducir un dispositivo. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, Videodisc, VCR y de onda-audio reconocen este comando.
ms.assetid: 3ee707d6-6af4-494d-a887-d91ea5666ac4
keywords:
- comando PLAY Windows multimedia
topic_type:
- apiref
api_name:
- play
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf262db152677ef5a2f29de9526152c1d48d4c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676700"
---
# <a name="play-command"></a><span data-ttu-id="4fd24-105">reproducir comando</span><span class="sxs-lookup"><span data-stu-id="4fd24-105">play command</span></span>

<span data-ttu-id="4fd24-106">El comando PLAY comienza a reproducir un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4fd24-106">The play command starts playing a device.</span></span> <span data-ttu-id="4fd24-107">Los dispositivos de audio de CD, digital-video, MIDI Sequencer, Videodisc, VCR y de onda-audio reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="4fd24-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="4fd24-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="4fd24-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("play %s %s %s"), 
  lpszDeviceID, 
  lpszPlayFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="4fd24-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4fd24-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fd24-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="4fd24-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4fd24-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="4fd24-111">Identifier of an MCI device.</span></span> <span data-ttu-id="4fd24-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4fd24-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="4fd24-113"><span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*</span><span class="sxs-lookup"><span data-stu-id="4fd24-113"><span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4fd24-114">Marca para reproducir un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4fd24-114">Flag for playing a device.</span></span> <span data-ttu-id="4fd24-115">En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **Play** y las marcas usadas por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="4fd24-115">The following table lists device types that recognize the **play** command and the flags used by each type.</span></span>



| <span data-ttu-id="4fd24-116">Value</span><span class="sxs-lookup"><span data-stu-id="4fd24-116">Value</span></span>        | <span data-ttu-id="4fd24-117">Significado</span><span class="sxs-lookup"><span data-stu-id="4fd24-117">Meaning</span></span>                          | <span data-ttu-id="4fd24-118">Significado</span><span class="sxs-lookup"><span data-stu-id="4fd24-118">Meaning</span></span>                           |
|--------------|----------------------------------|-----------------------------------|
| <span data-ttu-id="4fd24-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="4fd24-119">cdaudio</span></span>      | <span data-ttu-id="4fd24-120">desde la *posición*</span><span class="sxs-lookup"><span data-stu-id="4fd24-120">from *position*</span></span>                  | <span data-ttu-id="4fd24-121">para *colocar*</span><span class="sxs-lookup"><span data-stu-id="4fd24-121">to *position*</span></span>                     |
| <span data-ttu-id="4fd24-122">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="4fd24-122">digitalvideo</span></span> | <span data-ttu-id="4fd24-123">repetir desde la *posición* de pantalla completa</span><span class="sxs-lookup"><span data-stu-id="4fd24-123">from *position* fullscreen repeat</span></span> | <span data-ttu-id="4fd24-124">invertir en la ventana de *posición*</span><span class="sxs-lookup"><span data-stu-id="4fd24-124">reverse to *position* window</span></span>       |
| <span data-ttu-id="4fd24-125">sequencer</span><span class="sxs-lookup"><span data-stu-id="4fd24-125">sequencer</span></span>    | <span data-ttu-id="4fd24-126">desde la *posición*</span><span class="sxs-lookup"><span data-stu-id="4fd24-126">from *position*</span></span>                  | <span data-ttu-id="4fd24-127">para *colocar*</span><span class="sxs-lookup"><span data-stu-id="4fd24-127">to *position*</span></span>                     |
| <span data-ttu-id="4fd24-128">vídeos</span><span class="sxs-lookup"><span data-stu-id="4fd24-128">vcr</span></span>          | <span data-ttu-id="4fd24-129">en *el tiempo* desde la *posición* inversa</span><span class="sxs-lookup"><span data-stu-id="4fd24-129">at *time* from *position* reverse</span></span>  | <span data-ttu-id="4fd24-130">Buscar en *posición*</span><span class="sxs-lookup"><span data-stu-id="4fd24-130">scan to *position*</span></span>                |
| <span data-ttu-id="4fd24-131">videodisco</span><span class="sxs-lookup"><span data-stu-id="4fd24-131">videodisc</span></span>    | <span data-ttu-id="4fd24-132">exploración inversa rápida desde la *posición*</span><span class="sxs-lookup"><span data-stu-id="4fd24-132">fast from *position* reverse scan</span></span> | <span data-ttu-id="4fd24-133">*entero* de velocidad lenta que se va a *colocar*</span><span class="sxs-lookup"><span data-stu-id="4fd24-133">slow speed *integer* to *position*</span></span> |
| <span data-ttu-id="4fd24-134">waveaudio</span><span class="sxs-lookup"><span data-stu-id="4fd24-134">waveaudio</span></span>    | <span data-ttu-id="4fd24-135">desde la *posición*</span><span class="sxs-lookup"><span data-stu-id="4fd24-135">from *position*</span></span>                  | <span data-ttu-id="4fd24-136">para *colocar*</span><span class="sxs-lookup"><span data-stu-id="4fd24-136">to *position*</span></span>                     |



 

<span data-ttu-id="4fd24-137">En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszPlayFlags** y su significado.</span><span class="sxs-lookup"><span data-stu-id="4fd24-137">The following table lists the flags that can be specified in the **lpszPlayFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="4fd24-138">Value</span><span class="sxs-lookup"><span data-stu-id="4fd24-138">Value</span></span>           | <span data-ttu-id="4fd24-139">Significado</span><span class="sxs-lookup"><span data-stu-id="4fd24-139">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd24-140">a la *hora*</span><span class="sxs-lookup"><span data-stu-id="4fd24-140">at *time*</span></span>       | <span data-ttu-id="4fd24-141">Indica que el dispositivo debe comenzar a ejecutar este comando, o bien, si el dispositivo está preparado, cuando comienza el comando de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="4fd24-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="4fd24-142">Para obtener más información, consulte el comando [CUE](cue.md) .</span><span class="sxs-lookup"><span data-stu-id="4fd24-142">For more information, see the [cue](cue.md) command.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="4fd24-143">fast</span><span class="sxs-lookup"><span data-stu-id="4fd24-143">fast</span></span>            | <span data-ttu-id="4fd24-144">Indica que el dispositivo debe reproducirse más rápido que el normal.</span><span class="sxs-lookup"><span data-stu-id="4fd24-144">Indicates that the device should play faster than normal.</span></span> <span data-ttu-id="4fd24-145">Para determinar la velocidad exacta en un reproductor de videodisco, use la marca "Speed" del comando [status](status.md) .</span><span class="sxs-lookup"><span data-stu-id="4fd24-145">To determine the exact speed on a videodisc player, use the "speed" flag of the [status](status.md) command.</span></span> <span data-ttu-id="4fd24-146">Para especificar la velocidad de forma más precisa, use la marca "Speed" de este comando.</span><span class="sxs-lookup"><span data-stu-id="4fd24-146">To specify the speed more precisely, use the "speed" flag of this command.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="4fd24-147">desde la *posición*</span><span class="sxs-lookup"><span data-stu-id="4fd24-147">from *position*</span></span> | <span data-ttu-id="4fd24-148">Especifica una posición inicial para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="4fd24-148">Specifies a starting position for the playback.</span></span> <span data-ttu-id="4fd24-149">Si no se especifica la marca "from", la reproducción comienza en la posición actual.</span><span class="sxs-lookup"><span data-stu-id="4fd24-149">If the "from" flag is not specified, playback begins at the current position.</span></span> <span data-ttu-id="4fd24-150">En el caso de los dispositivos **cdaudio** , si la posición "desde" es mayor que la posición final del disco o si la posición "desde" es mayor que la posición "hasta", el controlador devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="4fd24-150">For **cdaudio** devices, if the "from" position is greater than the end position of the disc, or if the "from" position is greater than the "to" position, the driver returns an error.</span></span> <span data-ttu-id="4fd24-151">En el caso de los dispositivos de **videodisco** , las posiciones predeterminadas están en fotogramas para los discos CAV y en horas, minutos y segundos para los discos CLV.</span><span class="sxs-lookup"><span data-stu-id="4fd24-151">For **videodisc** devices, the default positions are in frames for CAV discs and in hours, minutes, and seconds for CLV discs.</span></span> |
| <span data-ttu-id="4fd24-152">completa</span><span class="sxs-lookup"><span data-stu-id="4fd24-152">fullscreen</span></span>      | <span data-ttu-id="4fd24-153">Especifica que debe usarse una presentación en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="4fd24-153">Specifies that a full-screen display should be used.</span></span> <span data-ttu-id="4fd24-154">Use esta marca solo cuando se reproduzcan archivos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="4fd24-154">Use this flag only when playing compressed files.</span></span> <span data-ttu-id="4fd24-155">(Los archivos sin comprimir no se reproducirán en pantalla completa).</span><span class="sxs-lookup"><span data-stu-id="4fd24-155">(Uncompressed files won't play full-screen.)</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="4fd24-156">pueden</span><span class="sxs-lookup"><span data-stu-id="4fd24-156">repeat</span></span>          | <span data-ttu-id="4fd24-157">Especifica que la reproducción debe reiniciarse cuando se alcanza el final del contenido.</span><span class="sxs-lookup"><span data-stu-id="4fd24-157">Specifies that playback should restart when the end of the content is reached.</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="4fd24-158">reverse</span><span class="sxs-lookup"><span data-stu-id="4fd24-158">reverse</span></span>         | <span data-ttu-id="4fd24-159">Especifica que la dirección de reproducción está hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="4fd24-159">Specifies that the play direction is backward.</span></span> <span data-ttu-id="4fd24-160">No se puede especificar una ubicación final con el marcador "REVERSE".</span><span class="sxs-lookup"><span data-stu-id="4fd24-160">You cannot specify an ending location with the "reverse" flag.</span></span> <span data-ttu-id="4fd24-161">En el caso de los videodisco, "SCAN" solo se aplica al formato CAV.</span><span class="sxs-lookup"><span data-stu-id="4fd24-161">For videodiscs, "scan" applies only to CAV format.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="4fd24-162">revisar</span><span class="sxs-lookup"><span data-stu-id="4fd24-162">scan</span></span>            | <span data-ttu-id="4fd24-163">Se reproduce lo más rápido posible sin deshabilitar el vídeo (aunque es posible que el audio esté deshabilitado).</span><span class="sxs-lookup"><span data-stu-id="4fd24-163">Plays as fast as possible without disabling video (although audio might be disabled).</span></span> <span data-ttu-id="4fd24-164">En el caso de los videodisco, "SCAN" solo se aplica al formato CAV.</span><span class="sxs-lookup"><span data-stu-id="4fd24-164">For videodiscs, "scan" applies only to CAV format.</span></span>                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="4fd24-165">lento</span><span class="sxs-lookup"><span data-stu-id="4fd24-165">slow</span></span>            | <span data-ttu-id="4fd24-166">Se reproduce lentamente.</span><span class="sxs-lookup"><span data-stu-id="4fd24-166">Plays slowly.</span></span> <span data-ttu-id="4fd24-167">Para determinar la velocidad exacta en un reproductor de videodisco, use la marca "Speed" del comando [status](status.md) .</span><span class="sxs-lookup"><span data-stu-id="4fd24-167">To determine the exact speed on a videodisc player, use the "speed" flag of the [status](status.md) command.</span></span> <span data-ttu-id="4fd24-168">Para especificar la velocidad de forma más precisa, use la marca "Speed" de este comando.</span><span class="sxs-lookup"><span data-stu-id="4fd24-168">To specify the speed more precisely, use the "speed" flag of this command.</span></span> <span data-ttu-id="4fd24-169">En el caso de los videodisco, "slow" solo se aplica al formato CAV.</span><span class="sxs-lookup"><span data-stu-id="4fd24-169">For videodiscs, "slow" applies only to CAV format.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="4fd24-170">*entero* de velocidad</span><span class="sxs-lookup"><span data-stu-id="4fd24-170">speed *integer*</span></span> | <span data-ttu-id="4fd24-171">Reproduce un CD a la velocidad especificada, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="4fd24-171">Plays a videodisc at the specified speed, in frames per second.</span></span> <span data-ttu-id="4fd24-172">Esta marca solo se aplica a discos CAV.</span><span class="sxs-lookup"><span data-stu-id="4fd24-172">This flag applies only to CAV discs.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="4fd24-173">para *colocar*</span><span class="sxs-lookup"><span data-stu-id="4fd24-173">to *position*</span></span>   | <span data-ttu-id="4fd24-174">Especifica una posición final para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="4fd24-174">Specifies an ending position for the playback.</span></span> <span data-ttu-id="4fd24-175">Si no se especifica la marca "to", la reproducción se detiene al final del contenido.</span><span class="sxs-lookup"><span data-stu-id="4fd24-175">If the "to" flag is not specified, playback stops at the end of the content.</span></span> <span data-ttu-id="4fd24-176">En el caso de los dispositivos **cdaudio** , si la posición "para" es mayor que la posición final del disco, el controlador devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="4fd24-176">For **cdaudio** devices, if the "to" position is greater than the end position of the disc, the driver returns an error.</span></span> <span data-ttu-id="4fd24-177">En el caso de los dispositivos de **videodisco** , las posiciones predeterminadas están en fotogramas para los discos CAV y en horas, minutos y segundos para los discos CLV.</span><span class="sxs-lookup"><span data-stu-id="4fd24-177">For **videodisc** devices, the default positions are in frames for CAV discs and in hours, minutes, and seconds for CLV discs.</span></span>                                                                  |
| <span data-ttu-id="4fd24-178">periodo</span><span class="sxs-lookup"><span data-stu-id="4fd24-178">window</span></span>          | <span data-ttu-id="4fd24-179">Especifica que la reproducción debe usar la ventana asociada a la instancia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4fd24-179">Specifies that playing should use the window associated with the device instance.</span></span> <span data-ttu-id="4fd24-180">Esta es la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4fd24-180">This is the default setting.</span></span>                                                                                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="4fd24-181"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="4fd24-181"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4fd24-182">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="4fd24-182">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="4fd24-183">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="4fd24-183">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="4fd24-184">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4fd24-184">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fd24-185">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4fd24-185">Return Value</span></span>

<span data-ttu-id="4fd24-186">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4fd24-186">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fd24-187">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fd24-187">Remarks</span></span>

<span data-ttu-id="4fd24-188">Antes de emitir comandos que usan valores de posición, debe establecer el formato de hora deseado mediante el comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="4fd24-188">Before issuing commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span> <span data-ttu-id="4fd24-189">Este comando empieza a reproducirse en la velocidad actual, como se establece con el comando SET "Speed".</span><span class="sxs-lookup"><span data-stu-id="4fd24-189">This command begins playing at the current speed, as set with the set "speed" command.</span></span> <span data-ttu-id="4fd24-190">La dirección es inversa si se especifica la marca "REVERSE", o si la marca "to" se especifica como un valor menor que la marca "from".</span><span class="sxs-lookup"><span data-stu-id="4fd24-190">The direction is reverse if the "reverse" flag is specified, or if the "to" flag is specified as a value less than the "from" flag.</span></span> <span data-ttu-id="4fd24-191">Si no se especifica la marca "from", la reproducción comienza en la posición actual.</span><span class="sxs-lookup"><span data-stu-id="4fd24-191">If the "from" flag is not specified, playback begins at the current position.</span></span> <span data-ttu-id="4fd24-192">Las marcas "to" y "REVERSE" no se pueden usar juntas.</span><span class="sxs-lookup"><span data-stu-id="4fd24-192">The "to" and "reverse" flags cannot be used together.</span></span>

## <a name="examples"></a><span data-ttu-id="4fd24-193">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4fd24-193">Examples</span></span>

<span data-ttu-id="4fd24-194">El siguiente comando reproduce el dispositivo "" de "" de la posición 1000 a la posición 2000 y envía un mensaje de notificación cuando se completa la reproducción.</span><span class="sxs-lookup"><span data-stu-id="4fd24-194">The following command plays the "mysound" device from position 1000 through position 2000, sending a notification message when the playback completes.</span></span>

``` syntax
play mysound from 1000 to 2000 notify
```

## <a name="requirements"></a><span data-ttu-id="4fd24-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fd24-195">Requirements</span></span>



| <span data-ttu-id="4fd24-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fd24-196">Requirement</span></span> | <span data-ttu-id="4fd24-197">Value</span><span class="sxs-lookup"><span data-stu-id="4fd24-197">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4fd24-198">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fd24-198">Minimum supported client</span></span><br/> | <span data-ttu-id="4fd24-199">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4fd24-199">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4fd24-200">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fd24-200">Minimum supported server</span></span><br/> | <span data-ttu-id="4fd24-201">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4fd24-201">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4fd24-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fd24-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fd24-203">MCI</span><span class="sxs-lookup"><span data-stu-id="4fd24-203">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4fd24-204">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="4fd24-204">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="4fd24-205">indicación</span><span class="sxs-lookup"><span data-stu-id="4fd24-205">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="4fd24-206">set</span><span class="sxs-lookup"><span data-stu-id="4fd24-206">set</span></span>](set.md)
</dt> </dl>

 

