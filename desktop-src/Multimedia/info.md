---
title: info (comando)
description: El comando info recupera una descripción de hardware de un dispositivo. Todos los dispositivos MCI reconocen este comando.
ms.assetid: cdd6628b-bff8-4a0d-9dad-a63321f584ea
keywords:
- comando info Windows multimedia
topic_type:
- apiref
api_name:
- info
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d401efca6a59d1ed3cbf433d7c33311678705d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422554"
---
# <a name="info-command"></a><span data-ttu-id="c1fda-105">info (comando)</span><span class="sxs-lookup"><span data-stu-id="c1fda-105">info command</span></span>

<span data-ttu-id="c1fda-106">El comando info recupera una descripción de hardware de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c1fda-106">The info command retrieves a hardware description from a device.</span></span> <span data-ttu-id="c1fda-107">Todos los dispositivos MCI reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="c1fda-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="c1fda-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="c1fda-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("info %s %s %s"), 
  lpszDeviceID, 
  lpszInfoType, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c1fda-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1fda-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1fda-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c1fda-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c1fda-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="c1fda-111">Identifier of an MCI device.</span></span> <span data-ttu-id="c1fda-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c1fda-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c1fda-113"><span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*</span><span class="sxs-lookup"><span data-stu-id="c1fda-113"><span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*</span></span>
</dt> <dd>

<span data-ttu-id="c1fda-114">Marca que identifica el tipo de información necesaria.</span><span class="sxs-lookup"><span data-stu-id="c1fda-114">Flag that identifies the type of information required.</span></span> <span data-ttu-id="c1fda-115">En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **info** y las marcas usadas por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="c1fda-115">The following table lists device types that recognize the **info** command and the flags used by each type.</span></span>



| <span data-ttu-id="c1fda-116">Value</span><span class="sxs-lookup"><span data-stu-id="c1fda-116">Value</span></span>        | <span data-ttu-id="c1fda-117">Significado</span><span class="sxs-lookup"><span data-stu-id="c1fda-117">Meaning</span></span>                                                             | <span data-ttu-id="c1fda-118">Significado</span><span class="sxs-lookup"><span data-stu-id="c1fda-118">Meaning</span></span>                                             |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="c1fda-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="c1fda-119">cdaudio</span></span>      | <span data-ttu-id="c1fda-120">info identityinfo UPC</span><span class="sxs-lookup"><span data-stu-id="c1fda-120">info identityinfo upc</span></span>                                               | <span data-ttu-id="c1fda-121">product</span><span class="sxs-lookup"><span data-stu-id="c1fda-121">product</span></span>                                             |
| <span data-ttu-id="c1fda-122">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="c1fda-122">digitalvideo</span></span> | <span data-ttu-id="c1fda-123">audio algorithmaudio qualityfileproductstill algorithmstill Quality</span><span class="sxs-lookup"><span data-stu-id="c1fda-123">audio algorithmaudio qualityfileproductstill algorithmstill quality</span></span> | <span data-ttu-id="c1fda-124">usageversionvideo algorithmvideo qualitywindow Text</span><span class="sxs-lookup"><span data-stu-id="c1fda-124">usageversionvideo algorithmvideo qualitywindow text</span></span> |
| <span data-ttu-id="c1fda-125">overlay</span><span class="sxs-lookup"><span data-stu-id="c1fda-125">overlay</span></span>      | <span data-ttu-id="c1fda-126">fileproduct</span><span class="sxs-lookup"><span data-stu-id="c1fda-126">fileproduct</span></span>                                                         | <span data-ttu-id="c1fda-127">texto de la ventana</span><span class="sxs-lookup"><span data-stu-id="c1fda-127">window text</span></span>                                         |
| <span data-ttu-id="c1fda-128">sequencer</span><span class="sxs-lookup"><span data-stu-id="c1fda-128">sequencer</span></span>    | <span data-ttu-id="c1fda-129">copyrightfile</span><span class="sxs-lookup"><span data-stu-id="c1fda-129">copyrightfile</span></span>                                                       | <span data-ttu-id="c1fda-130">nameproduct</span><span class="sxs-lookup"><span data-stu-id="c1fda-130">nameproduct</span></span>                                         |
| <span data-ttu-id="c1fda-131">vídeos</span><span class="sxs-lookup"><span data-stu-id="c1fda-131">vcr</span></span>          | <span data-ttu-id="c1fda-132">product</span><span class="sxs-lookup"><span data-stu-id="c1fda-132">product</span></span>                                                             | <span data-ttu-id="c1fda-133">version</span><span class="sxs-lookup"><span data-stu-id="c1fda-133">version</span></span>                                             |
| <span data-ttu-id="c1fda-134">videodisco</span><span class="sxs-lookup"><span data-stu-id="c1fda-134">videodisk</span></span>    | <span data-ttu-id="c1fda-135">product</span><span class="sxs-lookup"><span data-stu-id="c1fda-135">product</span></span>                                                             |                                                     |
| <span data-ttu-id="c1fda-136">waveaudio</span><span class="sxs-lookup"><span data-stu-id="c1fda-136">waveaudio</span></span>    | <span data-ttu-id="c1fda-137">fileinput</span><span class="sxs-lookup"><span data-stu-id="c1fda-137">fileinput</span></span>                                                           | <span data-ttu-id="c1fda-138">outputproduct</span><span class="sxs-lookup"><span data-stu-id="c1fda-138">outputproduct</span></span>                                       |



 

<span data-ttu-id="c1fda-139">En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszInfoType** y su significado.</span><span class="sxs-lookup"><span data-stu-id="c1fda-139">The following table lists the flags that can be specified in the **lpszInfoType** parameter and their meanings.</span></span>



| <span data-ttu-id="c1fda-140">Value</span><span class="sxs-lookup"><span data-stu-id="c1fda-140">Value</span></span>           | <span data-ttu-id="c1fda-141">Significado</span><span class="sxs-lookup"><span data-stu-id="c1fda-141">Meaning</span></span>                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1fda-142">algoritmo de audio</span><span class="sxs-lookup"><span data-stu-id="c1fda-142">audio algorithm</span></span> | <span data-ttu-id="c1fda-143">Devuelve el nombre del algoritmo de compresión de audio actual.</span><span class="sxs-lookup"><span data-stu-id="c1fda-143">Returns the name of the current audio compression algorithm.</span></span>                                                                                                                                       |
| <span data-ttu-id="c1fda-144">calidad de audio</span><span class="sxs-lookup"><span data-stu-id="c1fda-144">audio quality</span></span>   | <span data-ttu-id="c1fda-145">Devuelve el nombre del descriptor de calidad de audio actual.</span><span class="sxs-lookup"><span data-stu-id="c1fda-145">Returns the name for the current audio quality descriptor.</span></span> <span data-ttu-id="c1fda-146">Esto podría devolver "Unknown" si la aplicación tiene parámetros establecidos en valores específicos que no se corresponden con calidades definidas.</span><span class="sxs-lookup"><span data-stu-id="c1fda-146">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span>       |
| <span data-ttu-id="c1fda-147">copyright</span><span class="sxs-lookup"><span data-stu-id="c1fda-147">copyright</span></span>       | <span data-ttu-id="c1fda-148">Recupera el aviso de copyright del archivo MIDI del evento meta de copyright.</span><span class="sxs-lookup"><span data-stu-id="c1fda-148">Retrieves the MIDI file copyright notice from the copyright meta event.</span></span>                                                                                                                            |
| <span data-ttu-id="c1fda-149">archivo</span><span class="sxs-lookup"><span data-stu-id="c1fda-149">file</span></span>            | <span data-ttu-id="c1fda-150">Recupera el nombre del archivo utilizado por el dispositivo compuesto.</span><span class="sxs-lookup"><span data-stu-id="c1fda-150">Retrieves the name of the file used by the compound device.</span></span> <span data-ttu-id="c1fda-151">Si el dispositivo se abre sin un archivo y no se ha usado el comando [Load](load.md) , se devuelve una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="c1fda-151">If the device is opened without a file and the [load](load.md) command has not been used, a null string is returned.</span></span>                  |
| <span data-ttu-id="c1fda-152">identidad de información</span><span class="sxs-lookup"><span data-stu-id="c1fda-152">info identity</span></span>   | <span data-ttu-id="c1fda-153">Genera un identificador único para el CD de audio cargado actualmente en el reproductor que se consulta.</span><span class="sxs-lookup"><span data-stu-id="c1fda-153">Produces a unique identifier for the audio CD currently loaded in the player being queried.</span></span>                                                                                                        |
| <span data-ttu-id="c1fda-154">UPC de información</span><span class="sxs-lookup"><span data-stu-id="c1fda-154">info upc</span></span>        | <span data-ttu-id="c1fda-155">Genera el código universal de producto (UPC) que está codificado en un CD de audio.</span><span class="sxs-lookup"><span data-stu-id="c1fda-155">Produces the Universal Product Code (UPC) that is encoded on an audio CD.</span></span> <span data-ttu-id="c1fda-156">UPC es una cadena de dígitos.</span><span class="sxs-lookup"><span data-stu-id="c1fda-156">The UPC is a string of digits.</span></span> <span data-ttu-id="c1fda-157">Es posible que no esté disponible para todos los CD.</span><span class="sxs-lookup"><span data-stu-id="c1fda-157">It might not be available for all CDs.</span></span>                                                    |
| <span data-ttu-id="c1fda-158">input</span><span class="sxs-lookup"><span data-stu-id="c1fda-158">input</span></span>           | <span data-ttu-id="c1fda-159">Recupera la descripción del dispositivo de entrada actual.</span><span class="sxs-lookup"><span data-stu-id="c1fda-159">Retrieves the description of the current input device.</span></span> <span data-ttu-id="c1fda-160">Devuelve "none" si no se ha establecido un dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="c1fda-160">Returns "none" if an input device is not set.</span></span>                                                                                               |
| <span data-ttu-id="c1fda-161">name</span><span class="sxs-lookup"><span data-stu-id="c1fda-161">name</span></span>            | <span data-ttu-id="c1fda-162">Recupera el nombre de secuencia del evento meta de nombre de secuencia/pista.</span><span class="sxs-lookup"><span data-stu-id="c1fda-162">Retrieves the sequence name from the sequence/track name meta event.</span></span>                                                                                                                               |
| <span data-ttu-id="c1fda-163">output</span><span class="sxs-lookup"><span data-stu-id="c1fda-163">output</span></span>          | <span data-ttu-id="c1fda-164">Recupera la descripción del dispositivo de salida actual.</span><span class="sxs-lookup"><span data-stu-id="c1fda-164">Retrieves the description of the current output device.</span></span> <span data-ttu-id="c1fda-165">Devuelve "none" si no se ha establecido un dispositivo de salida.</span><span class="sxs-lookup"><span data-stu-id="c1fda-165">Returns "none" if an output device is not set.</span></span>                                                                                             |
| <span data-ttu-id="c1fda-166">product</span><span class="sxs-lookup"><span data-stu-id="c1fda-166">product</span></span>         | <span data-ttu-id="c1fda-167">Recupera una descripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c1fda-167">Retrieves a description of the device.</span></span> <span data-ttu-id="c1fda-168">Esta información suele incluir el nombre del producto y el modelo.</span><span class="sxs-lookup"><span data-stu-id="c1fda-168">This information often includes the product name and model.</span></span> <span data-ttu-id="c1fda-169">La longitud de la cadena será de 31 caracteres como máximo.</span><span class="sxs-lookup"><span data-stu-id="c1fda-169">The string length will be 31 characters or fewer.</span></span>                                               |
| <span data-ttu-id="c1fda-170">algoritmo de todavía</span><span class="sxs-lookup"><span data-stu-id="c1fda-170">still algorithm</span></span> | <span data-ttu-id="c1fda-171">Devuelve el nombre del algoritmo de compresión de imagen fija actual.</span><span class="sxs-lookup"><span data-stu-id="c1fda-171">Returns the name of the current still image compression algorithm.</span></span>                                                                                                                                 |
| <span data-ttu-id="c1fda-172">calidad todavía</span><span class="sxs-lookup"><span data-stu-id="c1fda-172">still quality</span></span>   | <span data-ttu-id="c1fda-173">Devuelve el nombre del descriptor de calidad de imagen todavía actual.</span><span class="sxs-lookup"><span data-stu-id="c1fda-173">Returns the name for the current still image quality descriptor.</span></span> <span data-ttu-id="c1fda-174">Esto podría devolver "Unknown" si la aplicación tiene parámetros establecidos en valores específicos que no se corresponden con calidades definidas.</span><span class="sxs-lookup"><span data-stu-id="c1fda-174">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span> |
| <span data-ttu-id="c1fda-175">usage</span><span class="sxs-lookup"><span data-stu-id="c1fda-175">usage</span></span>           | <span data-ttu-id="c1fda-176">Devuelve una cadena que describe las restricciones de uso que puede imponer el propietario de los datos visuales o de audio en el área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="c1fda-176">Returns a string describing usage restrictions that might be imposed by the owner of the visual or audio data in the workspace.</span></span>                                                                    |
| <span data-ttu-id="c1fda-177">version</span><span class="sxs-lookup"><span data-stu-id="c1fda-177">version</span></span>         | <span data-ttu-id="c1fda-178">Devuelve el nivel de versión del controlador de dispositivo y el hardware.</span><span class="sxs-lookup"><span data-stu-id="c1fda-178">Returns the release level of the device driver and hardware.</span></span>                                                                                                                                       |
| <span data-ttu-id="c1fda-179">algoritmo de vídeo</span><span class="sxs-lookup"><span data-stu-id="c1fda-179">video algorithm</span></span> | <span data-ttu-id="c1fda-180">Devuelve el nombre del algoritmo de compresión de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="c1fda-180">Returns the name of the current video compression algorithm.</span></span>                                                                                                                                       |
| <span data-ttu-id="c1fda-181">calidad del vídeo</span><span class="sxs-lookup"><span data-stu-id="c1fda-181">video quality</span></span>   | <span data-ttu-id="c1fda-182">Devuelve el nombre del descriptor de calidad de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="c1fda-182">Returns the name for the current video quality descriptor.</span></span> <span data-ttu-id="c1fda-183">Esto podría devolver "Unknown" si la aplicación tiene parámetros establecidos en valores específicos que no se corresponden con calidades definidas.</span><span class="sxs-lookup"><span data-stu-id="c1fda-183">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span>       |
| <span data-ttu-id="c1fda-184">texto de la ventana</span><span class="sxs-lookup"><span data-stu-id="c1fda-184">window text</span></span>     | <span data-ttu-id="c1fda-185">Recupera el título de la ventana que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c1fda-185">Retrieves the caption of the window used by the device.</span></span>                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="c1fda-186"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c1fda-186"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c1fda-187">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="c1fda-187">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="c1fda-188">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="c1fda-188">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="c1fda-189">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c1fda-189">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1fda-190">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1fda-190">Return Value</span></span>

<span data-ttu-id="c1fda-191">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c1fda-191">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="c1fda-192">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c1fda-192">Examples</span></span>

<span data-ttu-id="c1fda-193">El siguiente comando recupera una descripción del hardware asociado al dispositivo "".</span><span class="sxs-lookup"><span data-stu-id="c1fda-193">The following command retrieves a description of the hardware associated with the "mysound" device.</span></span>

``` syntax
info mysound product
```

## <a name="requirements"></a><span data-ttu-id="c1fda-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1fda-194">Requirements</span></span>



| <span data-ttu-id="c1fda-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1fda-195">Requirement</span></span> | <span data-ttu-id="c1fda-196">Value</span><span class="sxs-lookup"><span data-stu-id="c1fda-196">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c1fda-197">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1fda-197">Minimum supported client</span></span><br/> | <span data-ttu-id="c1fda-198">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c1fda-198">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c1fda-199">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1fda-199">Minimum supported server</span></span><br/> | <span data-ttu-id="c1fda-200">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c1fda-200">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c1fda-201">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1fda-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1fda-202">MCI</span><span class="sxs-lookup"><span data-stu-id="c1fda-202">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c1fda-203">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="c1fda-203">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="c1fda-204">carga</span><span class="sxs-lookup"><span data-stu-id="c1fda-204">load</span></span>](load.md)
</dt> </dl>

 

