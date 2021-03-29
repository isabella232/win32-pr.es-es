---
title: comando de pila
description: El comando de pila se prepara para reproducir o grabar. Los dispositivos de audio digital-vídeo, VCR y de onda y de onda reconocen este comando.
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- comando CUE Windows multimedia
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd71f06a71c8aff4752fc31d750a3612564eb8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905663"
---
# <a name="cue-command"></a><span data-ttu-id="bc464-105">comando de pila</span><span class="sxs-lookup"><span data-stu-id="bc464-105">cue command</span></span>

<span data-ttu-id="bc464-106">El comando de pila se prepara para reproducir o grabar.</span><span class="sxs-lookup"><span data-stu-id="bc464-106">The cue command prepares for playing or recording.</span></span> <span data-ttu-id="bc464-107">Los dispositivos de audio digital-vídeo, VCR y de onda y de onda reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="bc464-107">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="bc464-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="bc464-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cue %s %s %s"), 
  lpszDeviceID, 
  lpszInOutTo, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="bc464-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc464-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc464-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="bc464-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="bc464-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="bc464-111">Identifier of an MCI device.</span></span> <span data-ttu-id="bc464-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc464-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="bc464-113"><span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*</span><span class="sxs-lookup"><span data-stu-id="bc464-113"><span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*</span></span>
</dt> <dd>

<span data-ttu-id="bc464-114">Marca que prepara un dispositivo para la reproducción o grabación.</span><span class="sxs-lookup"><span data-stu-id="bc464-114">Flag that prepares a device for playing or recording.</span></span> <span data-ttu-id="bc464-115">En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando de **pila** y las marcas usadas por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="bc464-115">The following table lists device types that recognize the **cue** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc464-116">Value</span><span class="sxs-lookup"><span data-stu-id="bc464-116">Value</span></span></th>
<th><span data-ttu-id="bc464-117">Pila</span><span class="sxs-lookup"><span data-stu-id="bc464-117">Cue</span></span></th>
<th><span data-ttu-id="bc464-118">Pila</span><span class="sxs-lookup"><span data-stu-id="bc464-118">Cue</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bc464-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="bc464-119">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="bc464-120">input</span><span class="sxs-lookup"><span data-stu-id="bc464-120">input</span></span></li>
<li><span data-ttu-id="bc464-121">nomostrar</span><span class="sxs-lookup"><span data-stu-id="bc464-121">noshow</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="bc464-122">output</span><span class="sxs-lookup"><span data-stu-id="bc464-122">output</span></span></li>
<li><span data-ttu-id="bc464-123">para <em>colocar</em></span><span class="sxs-lookup"><span data-stu-id="bc464-123">to <em>position</em></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc464-124">vídeos</span><span class="sxs-lookup"><span data-stu-id="bc464-124">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="bc464-125">desde la <em>posición</em></span><span class="sxs-lookup"><span data-stu-id="bc464-125">from <em>position</em></span></span></li>
<li><span data-ttu-id="bc464-126">input</span><span class="sxs-lookup"><span data-stu-id="bc464-126">input</span></span></li>
<li><span data-ttu-id="bc464-127">output</span><span class="sxs-lookup"><span data-stu-id="bc464-127">output</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="bc464-128">preprocesará</span><span class="sxs-lookup"><span data-stu-id="bc464-128">preroll</span></span></li>
<li><span data-ttu-id="bc464-129">reverse</span><span class="sxs-lookup"><span data-stu-id="bc464-129">reverse</span></span></li>
<li><span data-ttu-id="bc464-130">para <em>colocar</em></span><span class="sxs-lookup"><span data-stu-id="bc464-130">to <em>position</em></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc464-131">waveaudio</span><span class="sxs-lookup"><span data-stu-id="bc464-131">waveaudio</span></span></td>
<td><span data-ttu-id="bc464-132">input</span><span class="sxs-lookup"><span data-stu-id="bc464-132">input</span></span></td>
<td><span data-ttu-id="bc464-133">output</span><span class="sxs-lookup"><span data-stu-id="bc464-133">output</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bc464-134">En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro *lpszInOutTo* y su significado.</span><span class="sxs-lookup"><span data-stu-id="bc464-134">The following table lists the flags that can be specified in the *lpszInOutTo* parameter and their meanings.</span></span>



| <span data-ttu-id="bc464-135">Value</span><span class="sxs-lookup"><span data-stu-id="bc464-135">Value</span></span>           | <span data-ttu-id="bc464-136">Significado</span><span class="sxs-lookup"><span data-stu-id="bc464-136">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc464-137">desde la *posición*</span><span class="sxs-lookup"><span data-stu-id="bc464-137">from *position*</span></span> | <span data-ttu-id="bc464-138">Indica dónde comenzar.</span><span class="sxs-lookup"><span data-stu-id="bc464-138">Indicates where to start.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="bc464-139">input</span><span class="sxs-lookup"><span data-stu-id="bc464-139">input</span></span>           | <span data-ttu-id="bc464-140">Se prepara para la grabación.</span><span class="sxs-lookup"><span data-stu-id="bc464-140">Prepares for recording.</span></span> <span data-ttu-id="bc464-141">En el caso de los dispositivos de vídeo digital, esta marca se puede omitir si el origen de presentación actual ya es la entrada externa.</span><span class="sxs-lookup"><span data-stu-id="bc464-141">For digital-video devices, this flag can be omitted if the current presentation source is already the external input.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="bc464-142">nomostrar</span><span class="sxs-lookup"><span data-stu-id="bc464-142">noshow</span></span>          | <span data-ttu-id="bc464-143">Prepara para reproducir un marco sin mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="bc464-143">Prepares for playing a frame without displaying it.</span></span> <span data-ttu-id="bc464-144">Cuando se especifica esta marca, la pantalla continúa mostrando la imagen en el búfer de fotogramas aunque su fotograma correspondiente no sea la posición actual.</span><span class="sxs-lookup"><span data-stu-id="bc464-144">When this flag is specified, the display continues to show the image in the frame buffer even though its corresponding frame is not the current position.</span></span> <span data-ttu-id="bc464-145">Un comando de pila subsiguiente sin esta marca y sin la marca "para" muestra el marco actual.</span><span class="sxs-lookup"><span data-stu-id="bc464-145">A subsequent cue command without this flag and without the "to" flag displays the current frame.</span></span> |
| <span data-ttu-id="bc464-146">output</span><span class="sxs-lookup"><span data-stu-id="bc464-146">output</span></span>          | <span data-ttu-id="bc464-147">Se prepara para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="bc464-147">Prepares for playing.</span></span> <span data-ttu-id="bc464-148">Si no se especifica "Input" ni "Output", el valor predeterminado es "Output".</span><span class="sxs-lookup"><span data-stu-id="bc464-148">If neither "input" nor "output" is specified, the default setting is "output".</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="bc464-149">preprocesará</span><span class="sxs-lookup"><span data-stu-id="bc464-149">preroll</span></span>         | <span data-ttu-id="bc464-150">Mueve la distancia de predesplazamiento desde el *punto*.</span><span class="sxs-lookup"><span data-stu-id="bc464-150">Moves the preroll distance from the *in-point*.</span></span> <span data-ttu-id="bc464-151">El en el punto es la posición actual o la posición especificada por el indicador "desde".</span><span class="sxs-lookup"><span data-stu-id="bc464-151">The in-point is the current position, or the position specified by the "from" flag.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="bc464-152">reverse</span><span class="sxs-lookup"><span data-stu-id="bc464-152">reverse</span></span>         | <span data-ttu-id="bc464-153">Indica que la dirección de reproducción está en orden inverso (hacia atrás).</span><span class="sxs-lookup"><span data-stu-id="bc464-153">Indicates play direction is in reverse (backward).</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="bc464-154">para *colocar*</span><span class="sxs-lookup"><span data-stu-id="bc464-154">to *position*</span></span>   | <span data-ttu-id="bc464-155">Mueve el área de trabajo a la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="bc464-155">Moves the workspace to the specified position.</span></span> <span data-ttu-id="bc464-156">En el caso de los dispositivos VCR, esta marca indica dónde debe detenerse.</span><span class="sxs-lookup"><span data-stu-id="bc464-156">For VCR devices, this flag indicates where to stop.</span></span>                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="bc464-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="bc464-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="bc464-158">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="bc464-158">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="bc464-159">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="bc464-159">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="bc464-160">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="bc464-160">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc464-161">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc464-161">Return Value</span></span>

<span data-ttu-id="bc464-162">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bc464-162">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc464-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc464-163">Remarks</span></span>

<span data-ttu-id="bc464-164">Aunque no es necesario, la emisión del comando de pila antes de reproducir o grabar en algunos dispositivos podría reducir el retraso antes de que el dispositivo inicie la acción.</span><span class="sxs-lookup"><span data-stu-id="bc464-164">Although it is not necessary, issuing the cue command before playing or recording on some devices might reduce the delay before the device starts the action.</span></span>

<span data-ttu-id="bc464-165">Este comando produce un error si la reproducción o grabación está en curso o si el dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="bc464-165">This command fails if playing or recording is in progress or if the device is paused.</span></span>

<span data-ttu-id="bc464-166">Cuando se cueing para la reproducción (mediante la indicación "Output"), la emisión del comando [Play](play.md) con la marca "from", "to" o "REVERSE" cancela el comando CUE.</span><span class="sxs-lookup"><span data-stu-id="bc464-166">When cueing for playback (using cue "output"), issuing the [play](play.md) command with the "from", "to", or "reverse" flag cancels the cue command.</span></span>

<span data-ttu-id="bc464-167">Cuando se cueing para grabar (mediante la entrada "Input"), la emisión del comando [Record](record.md) con la marca "from", "to" o "Initialize" cancela el comando CUE.</span><span class="sxs-lookup"><span data-stu-id="bc464-167">When cueing for recording (using cue "input"), issuing the [record](record.md) command with the "from", "to", or "initialize" flag cancels the cue command.</span></span>

## <a name="examples"></a><span data-ttu-id="bc464-168">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bc464-168">Examples</span></span>

<span data-ttu-id="bc464-169">El siguiente comando prepara el dispositivo "" de "" para grabar.</span><span class="sxs-lookup"><span data-stu-id="bc464-169">The following command prepares the "mysound" device for recording.</span></span>

``` syntax
cue mysound input
```

## <a name="requirements"></a><span data-ttu-id="bc464-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc464-170">Requirements</span></span>



| <span data-ttu-id="bc464-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc464-171">Requirement</span></span> | <span data-ttu-id="bc464-172">Value</span><span class="sxs-lookup"><span data-stu-id="bc464-172">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="bc464-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc464-173">Minimum supported client</span></span><br/> | <span data-ttu-id="bc464-174">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bc464-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bc464-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc464-175">Minimum supported server</span></span><br/> | <span data-ttu-id="bc464-176">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bc464-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="bc464-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc464-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc464-178">MCI</span><span class="sxs-lookup"><span data-stu-id="bc464-178">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bc464-179">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="bc464-179">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="bc464-180">reproducción</span><span class="sxs-lookup"><span data-stu-id="bc464-180">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="bc464-181">record</span><span class="sxs-lookup"><span data-stu-id="bc464-181">record</span></span>](record.md)
</dt> </dl>

 

