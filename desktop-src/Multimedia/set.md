---
title: Set (comando)
description: El comando set establece la configuración del control para el dispositivo. Los dispositivos de audio de CD, vídeo digital, secuencia de MIDI, VCR, vídeo, superposición de vídeo y de audio y de onda reconocen este comando.
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- comando set Windows multimedia
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914743db038b0cae32b53fa79b7696ddba1ad05b
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2021
ms.locfileid: "105678604"
---
# <a name="set-command"></a><span data-ttu-id="d7666-105">Set (comando)</span><span class="sxs-lookup"><span data-stu-id="d7666-105">set command</span></span>

> [!NOTE]
> <span data-ttu-id="d7666-106">Comunicación sin polarización: Microsoft admite un entorno diverso y de inclusión.</span><span class="sxs-lookup"><span data-stu-id="d7666-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="d7666-107">Dentro de este documento, hay referencias a la palabra ' Slave '.</span><span class="sxs-lookup"><span data-stu-id="d7666-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="d7666-108">La guía de estilo de Microsoft [para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo reconoce como una palabra de exclusión.</span><span class="sxs-lookup"><span data-stu-id="d7666-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="d7666-109">Este texto se usa tal como está actualmente el texto que se usa en los comandos.</span><span class="sxs-lookup"><span data-stu-id="d7666-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="d7666-110">Para mantener la coherencia, este documento contiene esta palabra.</span><span class="sxs-lookup"><span data-stu-id="d7666-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="d7666-111">Cuando se modifique esta palabra en los comandos, se corregirá este documento para que esté alineado.</span><span class="sxs-lookup"><span data-stu-id="d7666-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>


<span data-ttu-id="d7666-112">El comando set establece la configuración del control para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7666-112">The set command establishes control settings for the device.</span></span> <span data-ttu-id="d7666-113">Los dispositivos de audio de CD, vídeo digital, secuencia de MIDI, VCR, vídeo, superposición de vídeo y de audio y de onda reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="d7666-113">CD audio, digital-video, MIDI sequencer, VCR, videodisc, video-overlay, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="d7666-114">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="d7666-114">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("set %s %s %s"),
  lpszDeviceID,
  lpszSetting,
  lpszFlags
);
      
```

## <a name="parameters"></a><span data-ttu-id="d7666-115">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7666-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7666-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d7666-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d7666-117">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="d7666-117">Identifier of an MCI device.</span></span> <span data-ttu-id="d7666-118">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7666-118">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d7666-119"><span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*</span><span class="sxs-lookup"><span data-stu-id="d7666-119"><span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*</span></span>
</dt> <dd>

<span data-ttu-id="d7666-120">Marca para establecer la configuración del control.</span><span class="sxs-lookup"><span data-stu-id="d7666-120">Flag for establishing control settings.</span></span> <span data-ttu-id="d7666-121">En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **set** y las marcas usadas por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="d7666-121">The following table lists device types that recognize the **set** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7666-122">Tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d7666-122">Device Type</span></span></th>
<th><span data-ttu-id="d7666-123">Marcas de comandos</span><span class="sxs-lookup"><span data-stu-id="d7666-123">Command Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d7666-124">cdaudio</span><span class="sxs-lookup"><span data-stu-id="d7666-124">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="d7666-125">todo desactivado de audio</span><span class="sxs-lookup"><span data-stu-id="d7666-125">audio all off</span></span></li>
<li><span data-ttu-id="d7666-126">audio todo activado</span><span class="sxs-lookup"><span data-stu-id="d7666-126">audio all on</span></span></li>
<li><span data-ttu-id="d7666-127">audio abandonado</span><span class="sxs-lookup"><span data-stu-id="d7666-127">audio left off</span></span></li>
<li><span data-ttu-id="d7666-128">audio a la izquierda</span><span class="sxs-lookup"><span data-stu-id="d7666-128">audio left on</span></span></li>
<li><span data-ttu-id="d7666-129">audio a la derecha</span><span class="sxs-lookup"><span data-stu-id="d7666-129">audio right off</span></span></li>
<li><span data-ttu-id="d7666-130">audio a la derecha</span><span class="sxs-lookup"><span data-stu-id="d7666-130">audio right on</span></span></li>
<li><span data-ttu-id="d7666-131">puerta cerrada</span><span class="sxs-lookup"><span data-stu-id="d7666-131">door closed</span></span></li>
<li><span data-ttu-id="d7666-132">puerta abierta</span><span class="sxs-lookup"><span data-stu-id="d7666-132">door open</span></span></li>
<li><span data-ttu-id="d7666-133">milisegundos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-133">time format milliseconds</span></span></li>
<li><span data-ttu-id="d7666-134">formato de hora MSF</span><span class="sxs-lookup"><span data-stu-id="d7666-134">time format msf</span></span></li>
<li><span data-ttu-id="d7666-135">formato de hora TMSF</span><span class="sxs-lookup"><span data-stu-id="d7666-135">time format tmsf</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-136">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="d7666-136">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="d7666-137">todo desactivado de audio</span><span class="sxs-lookup"><span data-stu-id="d7666-137">audio all off</span></span></li>
<li><span data-ttu-id="d7666-138">audio todo activado</span><span class="sxs-lookup"><span data-stu-id="d7666-138">audio all on</span></span></li>
<li><span data-ttu-id="d7666-139">audio abandonado</span><span class="sxs-lookup"><span data-stu-id="d7666-139">audio left off</span></span></li>
<li><span data-ttu-id="d7666-140">audio a la izquierda</span><span class="sxs-lookup"><span data-stu-id="d7666-140">audio left on</span></span></li>
<li><span data-ttu-id="d7666-141">audio a la derecha</span><span class="sxs-lookup"><span data-stu-id="d7666-141">audio right off</span></span></li>
<li><span data-ttu-id="d7666-142">audio a la derecha</span><span class="sxs-lookup"><span data-stu-id="d7666-142">audio right on</span></span></li>
<li><span data-ttu-id="d7666-143">puerta cerrada</span><span class="sxs-lookup"><span data-stu-id="d7666-143">door closed</span></span></li>
<li><span data-ttu-id="d7666-144">puerta abierta</span><span class="sxs-lookup"><span data-stu-id="d7666-144">door open</span></span></li>
<li><span data-ttu-id="d7666-145"><em>formato</em> de formato de archivo</span><span class="sxs-lookup"><span data-stu-id="d7666-145">file format <em>format</em></span></span></li>
<li><span data-ttu-id="d7666-146">Buscar exactamente</span><span class="sxs-lookup"><span data-stu-id="d7666-146">seek exactly on</span></span></li>
<li><span data-ttu-id="d7666-147">Buscar exactamente desactivado</span><span class="sxs-lookup"><span data-stu-id="d7666-147">seek exactly off</span></span></li>
<li><span data-ttu-id="d7666-148"><em>factor</em> de velocidad</span><span class="sxs-lookup"><span data-stu-id="d7666-148">speed <em>factor</em></span></span></li>
<li><span data-ttu-id="d7666-149"><em>formato</em> de formato de archivo todavía</span><span class="sxs-lookup"><span data-stu-id="d7666-149">still file format <em>format</em></span></span></li>
<li><span data-ttu-id="d7666-150">marcos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-150">time format frames</span></span></li>
<li><span data-ttu-id="d7666-151">milisegundos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-151">time format milliseconds</span></span></li>
<li><span data-ttu-id="d7666-152">vídeo desactivado</span><span class="sxs-lookup"><span data-stu-id="d7666-152">video off</span></span></li>
<li><span data-ttu-id="d7666-153">vídeo sobre</span><span class="sxs-lookup"><span data-stu-id="d7666-153">video on</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-154">overlay</span><span class="sxs-lookup"><span data-stu-id="d7666-154">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="d7666-155">todo desactivado de audio</span><span class="sxs-lookup"><span data-stu-id="d7666-155">audio all off</span></span></li>
<li><span data-ttu-id="d7666-156">audio todo activado</span><span class="sxs-lookup"><span data-stu-id="d7666-156">audio all on</span></span></li>
<li><span data-ttu-id="d7666-157">audio abandonado</span><span class="sxs-lookup"><span data-stu-id="d7666-157">audio left off</span></span></li>
<li><span data-ttu-id="d7666-158">audio a la izquierda</span><span class="sxs-lookup"><span data-stu-id="d7666-158">audio left on</span></span></li>
<li><span data-ttu-id="d7666-159">audio a la derecha</span><span class="sxs-lookup"><span data-stu-id="d7666-159">audio right off</span></span></li>
<li><span data-ttu-id="d7666-160">audio a la derecha</span><span class="sxs-lookup"><span data-stu-id="d7666-160">audio right on</span></span></li>
<li><span data-ttu-id="d7666-161">puerta cerrada</span><span class="sxs-lookup"><span data-stu-id="d7666-161">door closed</span></span></li>
<li><span data-ttu-id="d7666-162">puerta abierta</span><span class="sxs-lookup"><span data-stu-id="d7666-162">door open</span></span></li>
<li><span data-ttu-id="d7666-163">vídeo desactivado</span><span class="sxs-lookup"><span data-stu-id="d7666-163">video off</span></span></li>
<li><span data-ttu-id="d7666-164">vídeo sobre</span><span class="sxs-lookup"><span data-stu-id="d7666-164">video on</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-165">sequencer</span><span class="sxs-lookup"><span data-stu-id="d7666-165">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="d7666-166">todo desactivado de audio</span><span class="sxs-lookup"><span data-stu-id="d7666-166">audio all off</span></span></li>
<li><span data-ttu-id="d7666-167">audio todo activado</span><span class="sxs-lookup"><span data-stu-id="d7666-167">audio all on</span></span></li>
<li><span data-ttu-id="d7666-168">audio abandonado</span><span class="sxs-lookup"><span data-stu-id="d7666-168">audio left off</span></span></li>
<li><span data-ttu-id="d7666-169">audio a la izquierda</span><span class="sxs-lookup"><span data-stu-id="d7666-169">audio left on</span></span></li>
<li><span data-ttu-id="d7666-170">audio a la derecha</span><span class="sxs-lookup"><span data-stu-id="d7666-170">audio right off</span></span></li>
<li><span data-ttu-id="d7666-171">audio a la derecha</span><span class="sxs-lookup"><span data-stu-id="d7666-171">audio right on</span></span></li>
<li><span data-ttu-id="d7666-172">puerta cerrada</span><span class="sxs-lookup"><span data-stu-id="d7666-172">door closed</span></span></li>
<li><span data-ttu-id="d7666-173">puerta abierta</span><span class="sxs-lookup"><span data-stu-id="d7666-173">door open</span></span></li>
<li><span data-ttu-id="d7666-174">MIDI maestro</span><span class="sxs-lookup"><span data-stu-id="d7666-174">master MIDI</span></span></li>
<li><span data-ttu-id="d7666-175">ninguno principal</span><span class="sxs-lookup"><span data-stu-id="d7666-175">master none</span></span></li>
<li><span data-ttu-id="d7666-176">SMPTE maestro</span><span class="sxs-lookup"><span data-stu-id="d7666-176">master SMPTE</span></span></li>
<li><span data-ttu-id="d7666-177"><em>tiempo</em> de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="d7666-177">offset <em>time</em></span></span></li>
<li><span data-ttu-id="d7666-178">Asignador de puertos</span><span class="sxs-lookup"><span data-stu-id="d7666-178">port mapper</span></span></li>
<li><span data-ttu-id="d7666-179">Puerto ninguno</span><span class="sxs-lookup"><span data-stu-id="d7666-179">port none</span></span></li>
<li><span data-ttu-id="d7666-180"><em>port_number</em> de Puerto</span><span class="sxs-lookup"><span data-stu-id="d7666-180">port <em>port_number</em></span></span></li>
<li><span data-ttu-id="d7666-181">archivo esclavo</span><span class="sxs-lookup"><span data-stu-id="d7666-181">slave file</span></span></li>
<li><span data-ttu-id="d7666-182">MIDI esclavo</span><span class="sxs-lookup"><span data-stu-id="d7666-182">slave MIDI</span></span></li>
<li><span data-ttu-id="d7666-183">ninguno subordinado</span><span class="sxs-lookup"><span data-stu-id="d7666-183">slave none</span></span></li>
<li><span data-ttu-id="d7666-184">SMPTE esclavo</span><span class="sxs-lookup"><span data-stu-id="d7666-184">slave SMPTE</span></span></li>
<li><span data-ttu-id="d7666-185"><em>tempo_value</em> de tempo</span><span class="sxs-lookup"><span data-stu-id="d7666-185">tempo <em>tempo_value</em></span></span></li>
<li><span data-ttu-id="d7666-186">milisegundos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-186">time format milliseconds</span></span></li>
<li><span data-ttu-id="d7666-187">formato de hora SMPTE <em>fps</em></span><span class="sxs-lookup"><span data-stu-id="d7666-187">time format SMPTE <em>fps</em></span></span></li>
<li><span data-ttu-id="d7666-188">formato de hora SMPTE 30 Drop</span><span class="sxs-lookup"><span data-stu-id="d7666-188">time format SMPTE 30 drop</span></span></li>
<li><span data-ttu-id="d7666-189">formato de hora, puntero de canción</span><span class="sxs-lookup"><span data-stu-id="d7666-189">time format song pointer</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-190"><strong>vídeos</strong></span><span class="sxs-lookup"><span data-stu-id="d7666-190"><strong>vcr</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="d7666-191">ensamblar registro en</span><span class="sxs-lookup"><span data-stu-id="d7666-191">assemble record on</span></span></li>
<li><span data-ttu-id="d7666-192">Ensamblaje de registro desactivado</span><span class="sxs-lookup"><span data-stu-id="d7666-192">assemble record off</span></span></li>
<li><span data-ttu-id="d7666-193">todo desactivado de audio</span><span class="sxs-lookup"><span data-stu-id="d7666-193">audio all off</span></span></li>
<li><span data-ttu-id="d7666-194">audio todo activado</span><span class="sxs-lookup"><span data-stu-id="d7666-194">audio all on</span></span></li>
<li><span data-ttu-id="d7666-195">audio abandonado</span><span class="sxs-lookup"><span data-stu-id="d7666-195">audio left off</span></span></li>
<li><span data-ttu-id="d7666-196">audio a la izquierda</span><span class="sxs-lookup"><span data-stu-id="d7666-196">audio left on</span></span></li>
<li><span data-ttu-id="d7666-197">audio a la derecha</span><span class="sxs-lookup"><span data-stu-id="d7666-197">audio right off</span></span></li>
<li><span data-ttu-id="d7666-198">audio a la derecha</span><span class="sxs-lookup"><span data-stu-id="d7666-198">audio right on</span></span></li>
<li><span data-ttu-id="d7666-199"><em>hora</em> del reloj</span><span class="sxs-lookup"><span data-stu-id="d7666-199">clock <em>time</em></span></span></li>
<li><span data-ttu-id="d7666-200">formato del contador</span><span class="sxs-lookup"><span data-stu-id="d7666-200">counter format</span></span></li>
<li><span data-ttu-id="d7666-201"><em>valor</em> del contador</span><span class="sxs-lookup"><span data-stu-id="d7666-201">counter <em>value</em></span></span></li>
<li><span data-ttu-id="d7666-202">puerta cerrada</span><span class="sxs-lookup"><span data-stu-id="d7666-202">door closed</span></span></li>
<li><span data-ttu-id="d7666-203">puerta abierta</span><span class="sxs-lookup"><span data-stu-id="d7666-203">door open</span></span></li>
<li><span data-ttu-id="d7666-204">contador de índice</span><span class="sxs-lookup"><span data-stu-id="d7666-204">index counter</span></span></li>
<li><span data-ttu-id="d7666-205">fecha de índice</span><span class="sxs-lookup"><span data-stu-id="d7666-205">index date</span></span></li>
<li><span data-ttu-id="d7666-206">tiempo de índice</span><span class="sxs-lookup"><span data-stu-id="d7666-206">index time</span></span></li>
<li><span data-ttu-id="d7666-207">tiempo de índice</span><span class="sxs-lookup"><span data-stu-id="d7666-207">index time</span></span></li>
<li><span data-ttu-id="d7666-208"><em>duración</em> de CodeLength</span><span class="sxs-lookup"><span data-stu-id="d7666-208">codelength <em>duration</em></span></span></li>
<li><span data-ttu-id="d7666-209"><em>tiempo de espera</em> de pausa</span><span class="sxs-lookup"><span data-stu-id="d7666-209">pause <em>timeout</em></span></span></li>
<li><span data-ttu-id="d7666-210">duración de PostRoll-</span><span class="sxs-lookup"><span data-stu-id="d7666-210">postroll duration -</span></span></li>
<li><span data-ttu-id="d7666-211"><em>duration</em></span><span class="sxs-lookup"><span data-stu-id="d7666-211"><em>duration</em></span></span></li>
<li><span data-ttu-id="d7666-212">encendido</span><span class="sxs-lookup"><span data-stu-id="d7666-212">power on</span></span></li>
<li><span data-ttu-id="d7666-213">desconectar</span><span class="sxs-lookup"><span data-stu-id="d7666-213">power off</span></span></li>
<li><span data-ttu-id="d7666-214"><em>duración</em> de la duración del prelanzamiento</span><span class="sxs-lookup"><span data-stu-id="d7666-214">preroll duration <em>duration</em></span></span></li>
<li><span data-ttu-id="d7666-215">formato de registro SP</span><span class="sxs-lookup"><span data-stu-id="d7666-215">record format SP</span></span></li>
<li><span data-ttu-id="d7666-216">formato de registro LP</span><span class="sxs-lookup"><span data-stu-id="d7666-216">record format LP</span></span></li>
<li><span data-ttu-id="d7666-217">formato de registro EP</span><span class="sxs-lookup"><span data-stu-id="d7666-217">record format EP</span></span></li>
<li><span data-ttu-id="d7666-218"><em>factor</em> de velocidad</span><span class="sxs-lookup"><span data-stu-id="d7666-218">speed <em>factor</em></span></span></li>
<li><span data-ttu-id="d7666-219">marcos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-219">time format frames</span></span></li>
<li><span data-ttu-id="d7666-220">formato de hora HMS</span><span class="sxs-lookup"><span data-stu-id="d7666-220">time format hms</span></span></li>
<li><span data-ttu-id="d7666-221">milisegundos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-221">time format milliseconds</span></span></li>
<li><span data-ttu-id="d7666-222">formato de hora MSF</span><span class="sxs-lookup"><span data-stu-id="d7666-222">time format msf</span></span></li>
<li><span data-ttu-id="d7666-223">formato de hora SMPTE <em>fps</em></span><span class="sxs-lookup"><span data-stu-id="d7666-223">time format SMPTE <em>fps</em></span></span></li>
<li><span data-ttu-id="d7666-224">formato de hora SMPTE 30 Drop</span><span class="sxs-lookup"><span data-stu-id="d7666-224">time format SMPTE 30 drop</span></span></li>
<li><span data-ttu-id="d7666-225">formato de hora TMSF</span><span class="sxs-lookup"><span data-stu-id="d7666-225">time format tmsf</span></span></li>
<li><span data-ttu-id="d7666-226">contador de modo de tiempo</span><span class="sxs-lookup"><span data-stu-id="d7666-226">time mode counter</span></span></li>
<li><span data-ttu-id="d7666-227">detección del modo de tiempo</span><span class="sxs-lookup"><span data-stu-id="d7666-227">time mode detect</span></span></li>
<li><span data-ttu-id="d7666-228">código de tiempo del modo de tiempo</span><span class="sxs-lookup"><span data-stu-id="d7666-228">time mode timecode</span></span></li>
<li><span data-ttu-id="d7666-229">más seguimiento</span><span class="sxs-lookup"><span data-stu-id="d7666-229">tracking plus</span></span></li>
<li><span data-ttu-id="d7666-230">seguimiento menos</span><span class="sxs-lookup"><span data-stu-id="d7666-230">tracking minus</span></span></li>
<li><span data-ttu-id="d7666-231">restablecimiento de seguimiento</span><span class="sxs-lookup"><span data-stu-id="d7666-231">tracking reset</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-232">videodisco</span><span class="sxs-lookup"><span data-stu-id="d7666-232">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="d7666-233">todo desactivado de audio</span><span class="sxs-lookup"><span data-stu-id="d7666-233">audio all off</span></span></li>
<li><span data-ttu-id="d7666-234">audio todo activado</span><span class="sxs-lookup"><span data-stu-id="d7666-234">audio all on</span></span></li>
<li><span data-ttu-id="d7666-235">audio abandonado</span><span class="sxs-lookup"><span data-stu-id="d7666-235">audio left off</span></span></li>
<li><span data-ttu-id="d7666-236">audio a la izquierda</span><span class="sxs-lookup"><span data-stu-id="d7666-236">audio left on</span></span></li>
<li><span data-ttu-id="d7666-237">audio a la derecha</span><span class="sxs-lookup"><span data-stu-id="d7666-237">audio right off</span></span></li>
<li><span data-ttu-id="d7666-238">audio a la derecha</span><span class="sxs-lookup"><span data-stu-id="d7666-238">audio right on</span></span></li>
<li><span data-ttu-id="d7666-239">puerta cerrada</span><span class="sxs-lookup"><span data-stu-id="d7666-239">door closed</span></span></li>
<li><span data-ttu-id="d7666-240">puerta abierta</span><span class="sxs-lookup"><span data-stu-id="d7666-240">door open</span></span></li>
<li><span data-ttu-id="d7666-241">marcos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-241">time format frames</span></span></li>
<li><span data-ttu-id="d7666-242">formato de hora HMS</span><span class="sxs-lookup"><span data-stu-id="d7666-242">time format hms</span></span></li>
<li><span data-ttu-id="d7666-243">milisegundos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-243">time format milliseconds</span></span></li>
<li><span data-ttu-id="d7666-244">seguimiento de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-244">time format track</span></span></li>
<li><span data-ttu-id="d7666-245">vídeo desactivado</span><span class="sxs-lookup"><span data-stu-id="d7666-245">video off</span></span></li>
<li><span data-ttu-id="d7666-246">vídeo sobre</span><span class="sxs-lookup"><span data-stu-id="d7666-246">video on</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-247">waveaudio</span><span class="sxs-lookup"><span data-stu-id="d7666-247">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="d7666-248"><em>entero</em> de alineación</span><span class="sxs-lookup"><span data-stu-id="d7666-248">alignment <em>integer</em></span></span></li>
<li><span data-ttu-id="d7666-249">cualquier entrada</span><span class="sxs-lookup"><span data-stu-id="d7666-249">any input</span></span></li>
<li><span data-ttu-id="d7666-250">cualquier salida</span><span class="sxs-lookup"><span data-stu-id="d7666-250">any output</span></span></li>
<li><span data-ttu-id="d7666-251">todo desactivado de audio</span><span class="sxs-lookup"><span data-stu-id="d7666-251">audio all off</span></span></li>
<li><span data-ttu-id="d7666-252">audio todo activado</span><span class="sxs-lookup"><span data-stu-id="d7666-252">audio all on</span></span></li>
<li><span data-ttu-id="d7666-253">audio abandonado</span><span class="sxs-lookup"><span data-stu-id="d7666-253">audio left off</span></span></li>
<li><span data-ttu-id="d7666-254">audio a la izquierda</span><span class="sxs-lookup"><span data-stu-id="d7666-254">audio left on</span></span></li>
<li><span data-ttu-id="d7666-255">audio a la derecha</span><span class="sxs-lookup"><span data-stu-id="d7666-255">audio right off</span></span></li>
<li><span data-ttu-id="d7666-256">audio a la derecha</span><span class="sxs-lookup"><span data-stu-id="d7666-256">audio right on</span></span></li>
<li><span data-ttu-id="d7666-257"><em>BIT_COUNT</em> BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="d7666-257">bitspersample <em>bit_count</em></span></span></li>
<li><span data-ttu-id="d7666-258"><em>byte_rate</em> bytespersec</span><span class="sxs-lookup"><span data-stu-id="d7666-258">bytespersec <em>byte_rate</em></span></span></li>
<li><span data-ttu-id="d7666-259">canales <em>channel_count</em></span><span class="sxs-lookup"><span data-stu-id="d7666-259">channels <em>channel_count</em></span></span></li>
<li><span data-ttu-id="d7666-260">puerta cerrada</span><span class="sxs-lookup"><span data-stu-id="d7666-260">door closed</span></span></li>
<li><span data-ttu-id="d7666-261">puerta abierta</span><span class="sxs-lookup"><span data-stu-id="d7666-261">door open</span></span></li>
<li><span data-ttu-id="d7666-262">PCM de etiqueta de formato</span><span class="sxs-lookup"><span data-stu-id="d7666-262">format tag pcm</span></span></li>
<li><span data-ttu-id="d7666-263"><em>etiqueta</em> de etiqueta de formato</span><span class="sxs-lookup"><span data-stu-id="d7666-263">format tag <em>tag</em></span></span></li>
<li><span data-ttu-id="d7666-264"><em>entero</em> de entrada</span><span class="sxs-lookup"><span data-stu-id="d7666-264">input <em>integer</em></span></span></li>
<li><span data-ttu-id="d7666-265"><em>entero</em> de salida</span><span class="sxs-lookup"><span data-stu-id="d7666-265">output <em>integer</em></span></span></li>
<li><span data-ttu-id="d7666-266"><em>entero</em> SamplesPerSec</span><span class="sxs-lookup"><span data-stu-id="d7666-266">samplespersec <em>integer</em></span></span></li>
<li><span data-ttu-id="d7666-267">bytes de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-267">time format bytes</span></span></li>
<li><span data-ttu-id="d7666-268">milisegundos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-268">time format milliseconds</span></span></li>
<li><span data-ttu-id="d7666-269">ejemplos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-269">time format samples</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d7666-270">En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszSetting** y su significado.</span><span class="sxs-lookup"><span data-stu-id="d7666-270">The following table lists the flags that can be specified in the **lpszSetting** parameter and their meanings.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7666-271">Value</span><span class="sxs-lookup"><span data-stu-id="d7666-271">Value</span></span></th>
<th><span data-ttu-id="d7666-272">Significado</span><span class="sxs-lookup"><span data-stu-id="d7666-272">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d7666-273"><em>entero</em> de alineación</span><span class="sxs-lookup"><span data-stu-id="d7666-273">alignment <em>integer</em></span></span></td>
<td><span data-ttu-id="d7666-274">Establece la alineación de los bloques de datos en relación con el inicio de los datos pasados al dispositivo de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="d7666-274">Sets the alignment of data blocks relative to the start of data passed to the waveform-audio device.</span></span> <span data-ttu-id="d7666-275">El archivo se guarda en este formato.</span><span class="sxs-lookup"><span data-stu-id="d7666-275">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-276">cualquier entrada</span><span class="sxs-lookup"><span data-stu-id="d7666-276">any input</span></span></td>
<td><span data-ttu-id="d7666-277">Use cualquier entrada que admita el formato actual al grabar.</span><span class="sxs-lookup"><span data-stu-id="d7666-277">Use any input that supports the current format when recording.</span></span> <span data-ttu-id="d7666-278">Esta es la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d7666-278">This is the default setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-279">cualquier salida</span><span class="sxs-lookup"><span data-stu-id="d7666-279">any output</span></span></td>
<td><span data-ttu-id="d7666-280">Use cualquier salida que admita el formato actual al reproducirlo.</span><span class="sxs-lookup"><span data-stu-id="d7666-280">Use any output that supports the current format when playing.</span></span> <span data-ttu-id="d7666-281">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d7666-281">This is the default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-282">ensamblar registro en</span><span class="sxs-lookup"><span data-stu-id="d7666-282">assemble record on</span></span> <br/> <span data-ttu-id="d7666-283">Ensamblaje de registro desactivado</span><span class="sxs-lookup"><span data-stu-id="d7666-283">assemble record off</span></span> <br/></td>
<td><span data-ttu-id="d7666-284">En el modo de ensamblado, todas las pistas se registran tal y como se define en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7666-284">In assemble mode, all tracks are recorded as defined by the device.</span></span> <span data-ttu-id="d7666-285">La mayoría de los VCR están en modo de ensamblado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d7666-285">Most VCRs are in assemble mode by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-286">todo desactivado de audio</span><span class="sxs-lookup"><span data-stu-id="d7666-286">audio all off</span></span> <br/> <span data-ttu-id="d7666-287">audio todo activado</span><span class="sxs-lookup"><span data-stu-id="d7666-287">audio all on</span></span> <br/></td>
<td><span data-ttu-id="d7666-288">Deshabilita o habilita la salida de audio.</span><span class="sxs-lookup"><span data-stu-id="d7666-288">Disables or enables audio output.</span></span> <span data-ttu-id="d7666-289">Los dispositivos de superposición de vídeo, el secuenciador MCISEQ y el dispositivo de audio de onda MCIWAVE no admiten esta marca.</span><span class="sxs-lookup"><span data-stu-id="d7666-289">Video-overlay devices, the MCISEQ sequencer, and the MCIWAVE waveform-audio device do not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-290">audio abandonado</span><span class="sxs-lookup"><span data-stu-id="d7666-290">audio left off</span></span> <br/> <span data-ttu-id="d7666-291">audio a la izquierda</span><span class="sxs-lookup"><span data-stu-id="d7666-291">audio left on</span></span> <br/> <span data-ttu-id="d7666-292">audio a la derecha</span><span class="sxs-lookup"><span data-stu-id="d7666-292">audio right off</span></span> <br/> <span data-ttu-id="d7666-293">audio a la derecha</span><span class="sxs-lookup"><span data-stu-id="d7666-293">audio right on</span></span> <br/></td>
<td><span data-ttu-id="d7666-294">Deshabilita o habilita la salida en el canal de audio izquierdo o derecho.</span><span class="sxs-lookup"><span data-stu-id="d7666-294">Disables or enables output to either the left or the right audio channel.</span></span> <span data-ttu-id="d7666-295">Los dispositivos de superposición de vídeo, el secuenciador MCISEQ y el dispositivo de audio de onda MCIWAVE no admiten esta marca.</span><span class="sxs-lookup"><span data-stu-id="d7666-295">Video-overlay devices, the MCISEQ sequencer, and the MCIWAVE waveform-audio device do not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-296"><em>BIT_COUNT</em> BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="d7666-296">bitspersample <em>bit_count</em></span></span></td>
<td><span data-ttu-id="d7666-297">Establece el número de bits por muestra de código PCM (modulación por pulsos) reproducido o grabado.</span><span class="sxs-lookup"><span data-stu-id="d7666-297">Sets the number of bits per PCM (Pulse Code Modulation) sample played or recorded.</span></span> <span data-ttu-id="d7666-298">El archivo se guarda en este formato.</span><span class="sxs-lookup"><span data-stu-id="d7666-298">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-299"><em>byte_rate</em> bytespersec</span><span class="sxs-lookup"><span data-stu-id="d7666-299">bytespersec <em>byte_rate</em></span></span></td>
<td><span data-ttu-id="d7666-300">Establece el número medio de bytes por segundo que se reproducen o registran.</span><span class="sxs-lookup"><span data-stu-id="d7666-300">Sets the average number of bytes per second played or recorded.</span></span> <span data-ttu-id="d7666-301">El archivo se guarda en este formato.</span><span class="sxs-lookup"><span data-stu-id="d7666-301">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-302">canales <em>channel_count</em></span><span class="sxs-lookup"><span data-stu-id="d7666-302">channels <em>channel_count</em></span></span></td>
<td><span data-ttu-id="d7666-303">Establece los canales para reproducir y grabar.</span><span class="sxs-lookup"><span data-stu-id="d7666-303">Sets the channels for playing and recording.</span></span> <span data-ttu-id="d7666-304">El archivo se guarda en este formato.</span><span class="sxs-lookup"><span data-stu-id="d7666-304">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-305"><em>hora</em> del reloj</span><span class="sxs-lookup"><span data-stu-id="d7666-305">clock <em>time</em></span></span></td>
<td><span data-ttu-id="d7666-306">Establece la hora del reloj externo a la <em>hora.</em></span><span class="sxs-lookup"><span data-stu-id="d7666-306">Sets time on the external clock to <em>time.</em></span></span> <span data-ttu-id="d7666-307">El formato se especifica como un entero largo sin signo.</span><span class="sxs-lookup"><span data-stu-id="d7666-307">The format is specified as a long unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-308">formato del contador</span><span class="sxs-lookup"><span data-stu-id="d7666-308">counter format</span></span></td>
<td><span data-ttu-id="d7666-309">Establezca el formato de hora para el contador, devuelto por el contador de <a href="status.md">Estado</a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="d7666-309">Set the time format for the counter, as returned by <a href="status.md">status</a> &quot;counter&quot;.</span></span> <span data-ttu-id="d7666-310">Para obtener información sobre los tipos aplicables, consulte el comando <strong>set</strong> &quot; Time format &quot; .</span><span class="sxs-lookup"><span data-stu-id="d7666-310">For information about applicable types, see the <strong>set</strong> &quot;time format&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-311"><em>valor</em> del contador</span><span class="sxs-lookup"><span data-stu-id="d7666-311">counter <em>value</em></span></span></td>
<td><span data-ttu-id="d7666-312">Establece el contador VCR en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="d7666-312">Sets the VCR counter to the specified value.</span></span> <span data-ttu-id="d7666-313">El valor debe especificarse en el formato del contador actual.</span><span class="sxs-lookup"><span data-stu-id="d7666-313">The value must be specified in the current counter format.</span></span> <span data-ttu-id="d7666-314">Para obtener más información, consulte el comando <strong>set</strong> &quot; Counter format &quot; .</span><span class="sxs-lookup"><span data-stu-id="d7666-314">For more information, see the <strong>set</strong> &quot;counter format&quot; command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-315">puerta cerrada</span><span class="sxs-lookup"><span data-stu-id="d7666-315">door closed</span></span></td>
<td><span data-ttu-id="d7666-316">Retira la bandeja y cierra la puerta, si es posible.</span><span class="sxs-lookup"><span data-stu-id="d7666-316">Retracts the tray and closes the door, if possible.</span></span> <span data-ttu-id="d7666-317">Para VCR, carga la cinta automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d7666-317">For VCRs, loads the tape automatically.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-318">puerta abierta</span><span class="sxs-lookup"><span data-stu-id="d7666-318">door open</span></span></td>
<td><span data-ttu-id="d7666-319">Abre la puerta y expulsa la bandeja o la cinta, si es posible.</span><span class="sxs-lookup"><span data-stu-id="d7666-319">Opens the door and ejects the tray or tape, if possible.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-320"><em>formato</em> de formato de archivo</span><span class="sxs-lookup"><span data-stu-id="d7666-320">file format <em>format</em></span></span></td>
<td><span data-ttu-id="d7666-321">Especifica un formato de archivo que se usa para los comandos <a href="save.md">Guardar</a> o <a href="capture.md">capturar</a> .</span><span class="sxs-lookup"><span data-stu-id="d7666-321">Specifies a file format that is used for <a href="save.md">save</a> or <a href="capture.md">capture</a> commands.</span></span> <span data-ttu-id="d7666-322">Si se omite, puede que el valor predeterminado sea un formato definido por el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7666-322">If omitted, this might default to a device driver defined format.</span></span> <span data-ttu-id="d7666-323">Si el formato de archivo especificado entra en conflicto con el algoritmo y la calidad seleccionados actualmente, se cambian a los valores predeterminados para el formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="d7666-323">If the specified file format conflicts with the currently selected algorithm and quality, then they are changed to the defaults for the file format.</span></span> <span data-ttu-id="d7666-324">Se definen los siguientes formatos de archivo:</span><span class="sxs-lookup"><span data-stu-id="d7666-324">The following file formats are defined:</span></span>
<ul>
<li><span data-ttu-id="d7666-325">AVI: especifica el formato AVI.</span><span class="sxs-lookup"><span data-stu-id="d7666-325">avi: Specifies AVI format.</span></span></li>
<li><span data-ttu-id="d7666-326">AVSS: especifica el formato de AVSS.</span><span class="sxs-lookup"><span data-stu-id="d7666-326">avss: Specifies AVSS format.</span></span></li>
<li><span data-ttu-id="d7666-327">DIB: especifica el formato DIB.</span><span class="sxs-lookup"><span data-stu-id="d7666-327">dib: Specifies DIB format.</span></span></li>
<li><span data-ttu-id="d7666-328">JFIF: especifica el formato JFIF.</span><span class="sxs-lookup"><span data-stu-id="d7666-328">jfif: Specifies JFIF format.</span></span></li>
<li><span data-ttu-id="d7666-329">JPEG: especifica el formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="d7666-329">jpeg: Specifies JPEG format.</span></span></li>
<li><span data-ttu-id="d7666-330">MPEG: especifica el formato MPEG.</span><span class="sxs-lookup"><span data-stu-id="d7666-330">mpeg: Specifies MPEG format.</span></span></li>
<li><span data-ttu-id="d7666-331">RDIB: especifica el formato DIB de RLE.</span><span class="sxs-lookup"><span data-stu-id="d7666-331">rdib: Specifies RLE DIB format.</span></span></li>
<li><span data-ttu-id="d7666-332">RJPEG: especifica el formato de RJPEG.</span><span class="sxs-lookup"><span data-stu-id="d7666-332">rjpeg: Specifies RJPEG format.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-333">PCM de etiqueta de formato</span><span class="sxs-lookup"><span data-stu-id="d7666-333">format tag pcm</span></span></td>
<td><span data-ttu-id="d7666-334">Establece el tipo de formato en PCM para reproducir y grabar.</span><span class="sxs-lookup"><span data-stu-id="d7666-334">Sets the format type to PCM for playing and recording.</span></span> <span data-ttu-id="d7666-335">El archivo se guarda en este formato.</span><span class="sxs-lookup"><span data-stu-id="d7666-335">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-336"><em>etiqueta</em> de etiqueta de formato</span><span class="sxs-lookup"><span data-stu-id="d7666-336">format tag <em>tag</em></span></span></td>
<td><span data-ttu-id="d7666-337">Establece el tipo de formato para reproducir y grabar.</span><span class="sxs-lookup"><span data-stu-id="d7666-337">Sets the format type for playing and recording.</span></span> <span data-ttu-id="d7666-338">El archivo se guarda en este formato.</span><span class="sxs-lookup"><span data-stu-id="d7666-338">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-339">código de tiempo de índice</span><span class="sxs-lookup"><span data-stu-id="d7666-339">index timecode</span></span> <br/> <span data-ttu-id="d7666-340">contador de índice</span><span class="sxs-lookup"><span data-stu-id="d7666-340">index counter</span></span> <br/> <span data-ttu-id="d7666-341">fecha de índice</span><span class="sxs-lookup"><span data-stu-id="d7666-341">index date</span></span> <br/> <span data-ttu-id="d7666-342">tiempo de índice</span><span class="sxs-lookup"><span data-stu-id="d7666-342">index time</span></span> <br/></td>
<td><span data-ttu-id="d7666-343">Establece la pantalla de presentación actual en el VCR.</span><span class="sxs-lookup"><span data-stu-id="d7666-343">Sets the current display screen on the VCR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-344"><em>entero</em> de entrada</span><span class="sxs-lookup"><span data-stu-id="d7666-344">input <em>integer</em></span></span></td>
<td><span data-ttu-id="d7666-345">Establece el canal de audio que se usa como entrada.</span><span class="sxs-lookup"><span data-stu-id="d7666-345">Sets the audio channel used as the input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-346"><em>duración</em> de la longitud</span><span class="sxs-lookup"><span data-stu-id="d7666-346">length <em>duration</em></span></span></td>
<td><span data-ttu-id="d7666-347">Establece la longitud especificada por el usuario de la cinta en el VCR.</span><span class="sxs-lookup"><span data-stu-id="d7666-347">Sets the user-specified length of the tape in the VCR.</span></span> <span data-ttu-id="d7666-348">Este valor lo devuelve el <a href="status.md"></a> &quot; comando de longitud &quot; de estado y se proporciona para ofrecer compatibilidad con las aplicaciones que requieren este comando para devolver una longitud válida.</span><span class="sxs-lookup"><span data-stu-id="d7666-348">This length is returned by the <a href="status.md">status</a> &quot;length&quot; command and is provided for compatibility with applications that require this command to return a valid length.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-349">MIDI maestro</span><span class="sxs-lookup"><span data-stu-id="d7666-349">master midi</span></span></td>
<td><span data-ttu-id="d7666-350">Establece el secuenciador MIDI como el origen de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="d7666-350">Sets the MIDI sequencer as the synchronization source.</span></span> <span data-ttu-id="d7666-351">Los datos de sincronización se envían en formato MIDI.</span><span class="sxs-lookup"><span data-stu-id="d7666-351">Synchronization data is sent in MIDI format.</span></span> <span data-ttu-id="d7666-352">El secuenciador MCISEQ no admite esta marca.</span><span class="sxs-lookup"><span data-stu-id="d7666-352">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-353">ninguno principal</span><span class="sxs-lookup"><span data-stu-id="d7666-353">master none</span></span></td>
<td><span data-ttu-id="d7666-354">Impide que el secuenciador MIDI envíe datos de sincronización.</span><span class="sxs-lookup"><span data-stu-id="d7666-354">Inhibits the MIDI sequencer from sending synchronization data.</span></span> <span data-ttu-id="d7666-355">El secuenciador MCISEQ no admite esta marca.</span><span class="sxs-lookup"><span data-stu-id="d7666-355">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-356">SMPTE maestro</span><span class="sxs-lookup"><span data-stu-id="d7666-356">master smpte</span></span></td>
<td><span data-ttu-id="d7666-357">Establece el secuenciador MIDI como el origen de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="d7666-357">Sets the MIDI sequencer as the synchronization source.</span></span> <span data-ttu-id="d7666-358">Los datos de sincronización se envían en formato SMPTE (sociedad de los ingenieros de películas y televisión).</span><span class="sxs-lookup"><span data-stu-id="d7666-358">Synchronization data is sent in SMPTE (Society of Motion Picture and Television Engineers) format.</span></span> <span data-ttu-id="d7666-359">El secuenciador MCISEQ no admite esta marca.</span><span class="sxs-lookup"><span data-stu-id="d7666-359">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-360"><em>tiempo</em> de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="d7666-360">offset <em>time</em></span></span></td>
<td><span data-ttu-id="d7666-361">Establece el <em>tiempo</em>de desplazamiento de SMPTE.</span><span class="sxs-lookup"><span data-stu-id="d7666-361">Sets the SMPTE offset <em>time</em>.</span></span> <span data-ttu-id="d7666-362">El desplazamiento es la hora de inicio de una secuencia basada en SMPTE.</span><span class="sxs-lookup"><span data-stu-id="d7666-362">The offset is the beginning time of a SMPTE based sequence.</span></span> <span data-ttu-id="d7666-363">La <em>hora</em> se expresa como <em>HH</em>: <em>mm</em>: <em>SS</em>: <em>FF</em>, donde <em>HH</em> es hours, <em>mm</em> es minutes, <em>SS</em> is seconds y <em>FF</em> es frames.</span><span class="sxs-lookup"><span data-stu-id="d7666-363">The <em>time</em> is expressed as <em>hh</em>: <em>mm</em>: <em>ss</em>: <em>ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-364"><em>entero</em> de salida</span><span class="sxs-lookup"><span data-stu-id="d7666-364">output <em>integer</em></span></span></td>
<td><span data-ttu-id="d7666-365">Establece el canal de audio que se usa como salida.</span><span class="sxs-lookup"><span data-stu-id="d7666-365">Sets the audio channel used as the output.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-366"><em>tiempo de espera</em> de pausa</span><span class="sxs-lookup"><span data-stu-id="d7666-366">pause <em>timeout</em></span></span></td>
<td><span data-ttu-id="d7666-367">Establece la duración máxima, en milisegundos, de un comando <a href="pause.md">PAUSE</a> .</span><span class="sxs-lookup"><span data-stu-id="d7666-367">Sets the maximum duration, in milliseconds, of a <a href="pause.md">pause</a> command.</span></span> <span data-ttu-id="d7666-368">Un valor de tiempo de <em>espera</em> cero indica que no se producirá ningún tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="d7666-368">A <em>timeout</em> value of zero indicates that no time-out will occur.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-369"><em>duración</em> de la duración de PostRoll</span><span class="sxs-lookup"><span data-stu-id="d7666-369">postroll duration <em>duration</em></span></span></td>
<td><span data-ttu-id="d7666-370">Establece la longitud, en el formato de hora actual, necesaria para frenar el transporte del VCR cuando se emite un comando <a href="stop.md">detener</a> o <strong>pausar</strong> .</span><span class="sxs-lookup"><span data-stu-id="d7666-370">Sets the length, in the current time format, needed to brake the VCR transport when a <a href="stop.md">stop</a> or <strong>pause</strong> command is issued.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-371">Asignador de puertos</span><span class="sxs-lookup"><span data-stu-id="d7666-371">port mapper</span></span></td>
<td><span data-ttu-id="d7666-372">Establece el asignador MIDI como el puerto que recibe los mensajes MIDI.</span><span class="sxs-lookup"><span data-stu-id="d7666-372">Sets the MIDI mapper as the port receiving the MIDI messages.</span></span> <span data-ttu-id="d7666-373">Este comando genera un error si otra aplicación está usando el asignador de MIDI o un puerto que necesita.</span><span class="sxs-lookup"><span data-stu-id="d7666-373">This command fails if the MIDI mapper or a port it needs is being used by another application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-374">Puerto ninguno</span><span class="sxs-lookup"><span data-stu-id="d7666-374">port none</span></span></td>
<td><span data-ttu-id="d7666-375">Deshabilita el envío de mensajes MIDI.</span><span class="sxs-lookup"><span data-stu-id="d7666-375">Disables the sending of MIDI messages.</span></span> <span data-ttu-id="d7666-376">Este comando también cierra un puerto MIDI.</span><span class="sxs-lookup"><span data-stu-id="d7666-376">This command also closes a MIDI port.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-377"><em>port_number</em> de Puerto</span><span class="sxs-lookup"><span data-stu-id="d7666-377">port <em>port_number</em></span></span></td>
<td><span data-ttu-id="d7666-378">Establece el puerto MIDI que recibe los mensajes MIDI.</span><span class="sxs-lookup"><span data-stu-id="d7666-378">Sets the MIDI port receiving the MIDI messages.</span></span> <span data-ttu-id="d7666-379">Este comando produce un error si otra aplicación está usando el puerto que está intentando abrir.</span><span class="sxs-lookup"><span data-stu-id="d7666-379">This command fails if the port you are trying to open is being used by another application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-380">encendido</span><span class="sxs-lookup"><span data-stu-id="d7666-380">power on</span></span> <br/> <span data-ttu-id="d7666-381">desconectar</span><span class="sxs-lookup"><span data-stu-id="d7666-381">power off</span></span> <br/></td>
<td><span data-ttu-id="d7666-382">Establece la capacidad del dispositivo en ON u OFF.</span><span class="sxs-lookup"><span data-stu-id="d7666-382">Sets the device power to on or off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-383"><em>duración</em> de la duración del prelanzamiento</span><span class="sxs-lookup"><span data-stu-id="d7666-383">preroll duration <em>duration</em></span></span></td>
<td><span data-ttu-id="d7666-384">Establece la longitud, en el formato de hora actual, necesaria para estabilizar la salida del VCR.</span><span class="sxs-lookup"><span data-stu-id="d7666-384">Sets the length, in the current time format, needed to stabilize the VCR output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-385">formato de registro SP</span><span class="sxs-lookup"><span data-stu-id="d7666-385">record format SP</span></span> <br/> <span data-ttu-id="d7666-386">formato de registro LP</span><span class="sxs-lookup"><span data-stu-id="d7666-386">record format LP</span></span> <br/> <span data-ttu-id="d7666-387">formato de registro EP</span><span class="sxs-lookup"><span data-stu-id="d7666-387">record format EP</span></span> <br/></td>
<td><span data-ttu-id="d7666-388">Establece el modo de grabación para el VCR en SP para reproducción estándar, EP para reproducción extendida o LP para larga reproducción.</span><span class="sxs-lookup"><span data-stu-id="d7666-388">Sets the recording mode for the VCR to SP for standard play, EP for extended play, or LP for long play.</span></span> <span data-ttu-id="d7666-389">Estos valores no pretenden ser específicos de VHS.</span><span class="sxs-lookup"><span data-stu-id="d7666-389">These values are not intended to be VHS specific.</span></span> <span data-ttu-id="d7666-390">Se asignan a tres modos adecuados con otros formatos de cinta.</span><span class="sxs-lookup"><span data-stu-id="d7666-390">They map to any three appropriate modes with other tape formats.</span></span> <span data-ttu-id="d7666-391">Por ejemplo, SP se asigna a la grabación más rápida y de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="d7666-391">For example, SP maps to the fastest, highest quality recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-392"><em>entero</em> SamplesPerSec</span><span class="sxs-lookup"><span data-stu-id="d7666-392">samplespersec <em>integer</em></span></span></td>
<td><span data-ttu-id="d7666-393">Establece la velocidad de muestreo para reproducir y grabar.</span><span class="sxs-lookup"><span data-stu-id="d7666-393">Sets the sample rate for playing and recording.</span></span> <span data-ttu-id="d7666-394">El archivo se guarda en este formato.</span><span class="sxs-lookup"><span data-stu-id="d7666-394">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-395">Buscar exactamente</span><span class="sxs-lookup"><span data-stu-id="d7666-395">seek exactly on</span></span><br/> <span data-ttu-id="d7666-396">Buscar exactamente desactivado</span><span class="sxs-lookup"><span data-stu-id="d7666-396">seek exactly off</span></span> <br/></td>
<td><span data-ttu-id="d7666-397">Selecciona uno de dos modos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d7666-397">Selects one of two seek modes.</span></span> <span data-ttu-id="d7666-398">Con &quot; Seek exactamente en &quot; , Seek siempre se moverá al marco especificado.</span><span class="sxs-lookup"><span data-stu-id="d7666-398">With &quot;seek exactly on&quot;, seek will always move to the frame specified.</span></span> <span data-ttu-id="d7666-399">Con &quot; Seek exactamente OFF &quot; , Seek se moverá al fotograma clave más cercano antes del marco especificado.</span><span class="sxs-lookup"><span data-stu-id="d7666-399">With &quot;seek exactly off&quot;, seek will move to the closest key frame prior to the frame specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-400">archivo esclavo</span><span class="sxs-lookup"><span data-stu-id="d7666-400">slave file</span></span></td>
<td><span data-ttu-id="d7666-401">Establece que el secuenciador MIDI Use los datos de archivo como origen de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="d7666-401">Sets the MIDI sequencer to use file data as the synchronization source.</span></span> <span data-ttu-id="d7666-402">Esta es la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d7666-402">This is the default setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-403">MIDI esclavo</span><span class="sxs-lookup"><span data-stu-id="d7666-403">slave midi</span></span></td>
<td><span data-ttu-id="d7666-404">Establece que el secuenciador MIDI Use los datos MIDI entrantes para el origen de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="d7666-404">Sets the MIDI sequencer to use incoming MIDI data for the synchronization source.</span></span> <span data-ttu-id="d7666-405">Sequencer reconoce los datos de sincronización con el formato MIDI.</span><span class="sxs-lookup"><span data-stu-id="d7666-405">The sequencer recognizes synchronization data with the MIDI format.</span></span> <span data-ttu-id="d7666-406">El secuenciador MCISEQ no admite esta marca.</span><span class="sxs-lookup"><span data-stu-id="d7666-406">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-407">ninguno subordinado</span><span class="sxs-lookup"><span data-stu-id="d7666-407">slave none</span></span></td>
<td><span data-ttu-id="d7666-408">Establece que el secuenciador MIDI omita la sincronización</span><span class="sxs-lookup"><span data-stu-id="d7666-408">Sets the MIDI sequencer to ignore synchronization</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-409">SMPTE esclavo</span><span class="sxs-lookup"><span data-stu-id="d7666-409">slave smpte</span></span></td>
<td><span data-ttu-id="d7666-410">Establece que el secuenciador MIDI Use los datos MIDI entrantes para el origen de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="d7666-410">Sets the MIDI sequencer to use incoming MIDI data for the synchronization source.</span></span> <span data-ttu-id="d7666-411">Sequencer reconoce los datos de sincronización con el formato SMPTE.</span><span class="sxs-lookup"><span data-stu-id="d7666-411">The sequencer recognizes synchronization data with the SMPTE format.</span></span> <span data-ttu-id="d7666-412">El secuenciador MCISEQ no admite esta marca.</span><span class="sxs-lookup"><span data-stu-id="d7666-412">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-413">factor de velocidad</span><span class="sxs-lookup"><span data-stu-id="d7666-413">speed factor</span></span></td>
<td><span data-ttu-id="d7666-414">Establece la velocidad relativa de reproducción de vídeo y audio desde el área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d7666-414">Sets the relative speed of video and audio playback from the workspace.</span></span> <span data-ttu-id="d7666-415">Factor es la proporción entre la velocidad de fotogramas nominal y la velocidad de fotogramas deseada, donde la velocidad de fotogramas nominal se designa como 1000.</span><span class="sxs-lookup"><span data-stu-id="d7666-415">Factor is the ratio between the nominal frame rate and the desired frame rate, where the nominal frame rate is designated as 1000.</span></span> <span data-ttu-id="d7666-416">(Una tasa de 500 es la velocidad media normal, 2000 es el doble de velocidad normal, etc.). Al establecer la velocidad en cero, el vídeo se reproduce lo más rápido posible sin quitar fotogramas y sin audio.</span><span class="sxs-lookup"><span data-stu-id="d7666-416">(A rate of 500 is half normal speed, 2000 is twice normal speed, and so on.) Setting the speed to zero plays the video as fast as possible without dropping frames and without audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-417"><em>formato</em> de formato de archivo todavía</span><span class="sxs-lookup"><span data-stu-id="d7666-417">still file format <em>format</em></span></span></td>
<td><span data-ttu-id="d7666-418">Especifica el formato de archivo utilizado para los comandos de captura.</span><span class="sxs-lookup"><span data-stu-id="d7666-418">Specifies the file format used for capture commands.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-419">tempo_value de tempo</span><span class="sxs-lookup"><span data-stu-id="d7666-419">tempo tempo_value</span></span></td>
<td><span data-ttu-id="d7666-420">Establece el tempo de la secuencia de acuerdo con el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="d7666-420">Sets the tempo of the sequence according to the current time format.</span></span> <span data-ttu-id="d7666-421">Para un archivo basado en PPQN, el tempo_value se interpreta como pulsaciones por minuto.</span><span class="sxs-lookup"><span data-stu-id="d7666-421">For a PPQN-based file, the tempo_value is interpreted as beats per minute.</span></span> <span data-ttu-id="d7666-422">Para un archivo basado en SMPTE, el tempo_value se interpreta como fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="d7666-422">For a SMPTE-based file, the tempo_value is interpreted as frames per second.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-423">bytes de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-423">time format bytes</span></span></td>
<td><span data-ttu-id="d7666-424">En un formato de archivo PCM, establece el formato de hora en bytes.</span><span class="sxs-lookup"><span data-stu-id="d7666-424">In a PCM file format, sets the time format to bytes.</span></span> <span data-ttu-id="d7666-425">Toda la información de posición se especifica como bytes después de este comando.</span><span class="sxs-lookup"><span data-stu-id="d7666-425">All position information is specified as bytes following this command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-426">marcos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-426">time format frames</span></span></td>
<td><span data-ttu-id="d7666-427">Establece el formato de hora en fotogramas.</span><span class="sxs-lookup"><span data-stu-id="d7666-427">Sets the time format to frames.</span></span> <span data-ttu-id="d7666-428">Todos los comandos que usan valores de posición asumirán fotogramas.</span><span class="sxs-lookup"><span data-stu-id="d7666-428">All commands that use position values will assume frames.</span></span> <span data-ttu-id="d7666-429">Cuando el dispositivo está abierto, el modo predeterminado es tramas.</span><span class="sxs-lookup"><span data-stu-id="d7666-429">When the device is opened, frames is the default mode.</span></span> <span data-ttu-id="d7666-430">Compatible con los discos de videodisco con el formato CAV.</span><span class="sxs-lookup"><span data-stu-id="d7666-430">Supported by videodiscs using CAV format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-431">formato de hora HMS</span><span class="sxs-lookup"><span data-stu-id="d7666-431">time format hms</span></span></td>
<td><span data-ttu-id="d7666-432">Establece el formato de hora en horas, minutos y segundos.</span><span class="sxs-lookup"><span data-stu-id="d7666-432">Sets the time format to hours, minutes, and seconds.</span></span> <span data-ttu-id="d7666-433">Todos los comandos que usan valores de posición asumirán HMS.</span><span class="sxs-lookup"><span data-stu-id="d7666-433">All commands that use position values will assume HMS.</span></span> <span data-ttu-id="d7666-434">HMS es el formato predeterminado para los videodiscos de CLV.</span><span class="sxs-lookup"><span data-stu-id="d7666-434">HMS is the default format for CLV videodiscs.</span></span> <span data-ttu-id="d7666-435">Especifique un valor de HMS como HH: mm: SS, donde HH es horas, mm son minutos y SS es segundos.</span><span class="sxs-lookup"><span data-stu-id="d7666-435">Specify an HMS value as hh:mm:ss, where hh is hours, mm is minutes, and ss is seconds.</span></span> <span data-ttu-id="d7666-436">Puede omitir un campo si este y todos los campos siguientes son cero.</span><span class="sxs-lookup"><span data-stu-id="d7666-436">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="d7666-437">Por ejemplo, 3, 3:0 y 3:0:0 son formas válidas de expresar 3 horas.</span><span class="sxs-lookup"><span data-stu-id="d7666-437">For example, 3, 3:0, and 3:0:0 are all valid ways to express 3 hours.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-438">milisegundos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-438">time format milliseconds</span></span></td>
<td><span data-ttu-id="d7666-439">Establece el formato de hora en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="d7666-439">Sets the time format to milliseconds.</span></span> <span data-ttu-id="d7666-440">Todos los comandos que usan valores de posición supondrán milisegundos.</span><span class="sxs-lookup"><span data-stu-id="d7666-440">All commands that use position values will assume milliseconds.</span></span> <span data-ttu-id="d7666-441">Puede abreviar los milisegundos como &quot; MS &quot; .</span><span class="sxs-lookup"><span data-stu-id="d7666-441">You can abbreviate milliseconds as &quot;ms&quot;.</span></span> <span data-ttu-id="d7666-442">En el caso de los dispositivos del secuenciador, el archivo de secuencia establece el formato predeterminado en PPQN o SMPTE.</span><span class="sxs-lookup"><span data-stu-id="d7666-442">For sequencer devices, the sequence file sets the default format to PPQN or SMPTE.</span></span> <span data-ttu-id="d7666-443">Los dispositivos de superposición de vídeo no admiten esta marca.</span><span class="sxs-lookup"><span data-stu-id="d7666-443">Video-overlay devices do not support this flag.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-444">formato de hora MSF</span><span class="sxs-lookup"><span data-stu-id="d7666-444">time format msf</span></span></td>
<td><span data-ttu-id="d7666-445">Establece el formato de hora en minutos, segundos y fotogramas.</span><span class="sxs-lookup"><span data-stu-id="d7666-445">Sets the time format to minutes, seconds, and frames.</span></span> <span data-ttu-id="d7666-446">Todos los comandos que usan valores de posición asumirán MSF (el formato predeterminado para el audio de CD).</span><span class="sxs-lookup"><span data-stu-id="d7666-446">All commands that use position values will assume MSF (the default format for CD audio).</span></span> <span data-ttu-id="d7666-447">Especifique un valor de MSF como mm: SS: FF, donde mm es minutos, SS es segundos y FF es fotogramas.</span><span class="sxs-lookup"><span data-stu-id="d7666-447">Specify an MSF value as mm:ss:ff, where mm is minutes, ss is seconds, and ff is frames.</span></span> <span data-ttu-id="d7666-448">Puede omitir un campo si este y todos los campos siguientes son cero.</span><span class="sxs-lookup"><span data-stu-id="d7666-448">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="d7666-449">Por ejemplo, 3, 3:0 y 3:0:0 son formas válidas de expresar 3 minutos.</span><span class="sxs-lookup"><span data-stu-id="d7666-449">For example, 3, 3:0, and 3:0:0 are valid ways to express 3 minutes.</span></span><br/> <span data-ttu-id="d7666-450">Los campos de MSF tienen los siguientes valores máximos:</span><span class="sxs-lookup"><span data-stu-id="d7666-450">The MSF fields have the following maximum values:</span></span><br/>
<ul>
<li><span data-ttu-id="d7666-451">Minutos 99</span><span class="sxs-lookup"><span data-stu-id="d7666-451">Minutes 99</span></span></li>
<li><span data-ttu-id="d7666-452">Segundos 59</span><span class="sxs-lookup"><span data-stu-id="d7666-452">Seconds 59</span></span></li>
<li><span data-ttu-id="d7666-453">Marcos 74</span><span class="sxs-lookup"><span data-stu-id="d7666-453">Frames 74</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-454">ejemplos de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-454">time format samples</span></span></td>
<td><span data-ttu-id="d7666-455">Establece el formato de hora en samples.</span><span class="sxs-lookup"><span data-stu-id="d7666-455">Sets the time format to samples.</span></span> <span data-ttu-id="d7666-456">Toda la información de posición se especifica como ejemplos que siguen este comando.</span><span class="sxs-lookup"><span data-stu-id="d7666-456">All position information is specified as samples following this command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-457">formato de hora SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="d7666-457">time format smpte 24</span></span><br/> <span data-ttu-id="d7666-458">formato de hora SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="d7666-458">time format smpte 25</span></span><br/> <span data-ttu-id="d7666-459">formato de hora SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="d7666-459">time format smpte 30</span></span><br/></td>
<td><span data-ttu-id="d7666-460">Establece el formato de hora en una velocidad de fotogramas SMPTE.</span><span class="sxs-lookup"><span data-stu-id="d7666-460">Sets the time format to an SMPTE frame rate.</span></span> <span data-ttu-id="d7666-461">Para VCR, establece el formato de hora en HH: mm: SS: FF, donde los valores válidos son de 00:00:00:00 a 23:59:59: XX y XX es uno menos que los fotogramas por segundo, según se especifica en el número 24, 25 o 30, tal y como se especifica en la marca.</span><span class="sxs-lookup"><span data-stu-id="d7666-461">For VCRs, sets the time format to hh:mm:ss:ff, where the legal values are 00:00:00:00 through 23:59:59:xx, and xx is one less than the frames per second as specified by the number 24, 25, or 30 as specified in the flag.</span></span> <span data-ttu-id="d7666-462">En la entrada, dos puntos (:) se requieren para separar los componentes.</span><span class="sxs-lookup"><span data-stu-id="d7666-462">On input, colons (:) are required to separate the components.</span></span> <span data-ttu-id="d7666-463">Las unidades menos significativas se pueden omitir si son 00; por ejemplo, 02:00 es igual que 02:00:00:00.</span><span class="sxs-lookup"><span data-stu-id="d7666-463">The least significant units can be omitted if they are 00; for example, 02:00 is the same as 02:00:00:00.</span></span> <span data-ttu-id="d7666-464">Todos los comandos que usan valores de posición adoptarán el formato SMPTE.</span><span class="sxs-lookup"><span data-stu-id="d7666-464">All commands that use position values will assume SMPTE format.</span></span><br/> <span data-ttu-id="d7666-465">El archivo de secuencia establece el formato predeterminado en PPQN o SMPTE.</span><span class="sxs-lookup"><span data-stu-id="d7666-465">The sequence file sets the default format to PPQN or SMPTE.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-466">formato de hora SMPTE 30 Drop</span><span class="sxs-lookup"><span data-stu-id="d7666-466">time format smpte 30 drop</span></span></td>
<td><span data-ttu-id="d7666-467">Establece el formato de hora en la velocidad de fotogramas de eliminación SMPTE 30.</span><span class="sxs-lookup"><span data-stu-id="d7666-467">Sets the time format to SMPTE 30 drop frame rate.</span></span> <span data-ttu-id="d7666-468">Para VCR, igual que SMPTE 30, con la excepción de que ciertas posiciones de código de tiempo se quitan del formato para que las posiciones de código de tiempo grabadas para cada fotograma (en la velocidad de fotogramas NTSC de 29,97 fps) se correspondan a tiempo real (30 fps).</span><span class="sxs-lookup"><span data-stu-id="d7666-468">For VCRs, same as SMPTE 30, except that certain timecode positions are dropped from the format to have the recorded timecode positions for each frame (at the NTSC frame rate of 29.97 fps) correspond to real time (at 30 fps).</span></span> <span data-ttu-id="d7666-469">Las posiciones de código de tiempo que se quitan son las siguientes: dos cada minuto, por minuto, durante los primeros nueve de cada diez minutos de contenido grabado.</span><span class="sxs-lookup"><span data-stu-id="d7666-469">Timecode positions that are dropped are as follows: two every minute, on the minute, for the first nine of every ten minutes of recorded content.</span></span> <span data-ttu-id="d7666-470">Por ejemplo, en 01:04:59:29, la siguiente posición del código de tiempo sería 01:05:00:02, no 01:05:00:00.</span><span class="sxs-lookup"><span data-stu-id="d7666-470">For example, at 01:04:59:29, the next timecode position would be 01:05:00:02, not 01:05:00:00.</span></span> <span data-ttu-id="d7666-471">Todos los comandos que usan valores de posición adoptarán el formato SMPTE.</span><span class="sxs-lookup"><span data-stu-id="d7666-471">All commands that use position values will assume SMPTE format.</span></span><br/> <span data-ttu-id="d7666-472">El archivo de secuencia establece el formato predeterminado en PPQN o SMPTE.</span><span class="sxs-lookup"><span data-stu-id="d7666-472">The sequence file sets the default format to PPQN or SMPTE.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-473">formato de hora, puntero de canción</span><span class="sxs-lookup"><span data-stu-id="d7666-473">time format song pointer</span></span></td>
<td><span data-ttu-id="d7666-474">Establece el formato de hora en el puntero de canción (decimosexto notas).</span><span class="sxs-lookup"><span data-stu-id="d7666-474">Sets the time format to song pointer (sixteenth notes).</span></span> <span data-ttu-id="d7666-475">Todos los comandos que usan valores de posición asumirán las unidades de puntero de la canción.</span><span class="sxs-lookup"><span data-stu-id="d7666-475">All commands that use position values will assume song pointer units.</span></span> <span data-ttu-id="d7666-476">Esta marca solo es válida para una secuencia de tipo de división PPQN.</span><span class="sxs-lookup"><span data-stu-id="d7666-476">This flag is valid only for a sequence of division type PPQN.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-477">formato de hora TMSF</span><span class="sxs-lookup"><span data-stu-id="d7666-477">time format tmsf</span></span></td>
<td><span data-ttu-id="d7666-478">Establece el formato de hora en pistas, minutos, segundos y fotogramas.</span><span class="sxs-lookup"><span data-stu-id="d7666-478">Sets the time format to tracks, minutes, seconds, and frames.</span></span> <span data-ttu-id="d7666-479">Todos los comandos que usan valores de posición asumirán TMSF.</span><span class="sxs-lookup"><span data-stu-id="d7666-479">All commands that use position values will assume TMSF.</span></span> <span data-ttu-id="d7666-480">Especifique un valor de TMSF como TT: mm: SS: FF, donde TT es pistas, mm es minutos, SS es segundos y FF es fotogramas.</span><span class="sxs-lookup"><span data-stu-id="d7666-480">Specify a TMSF value as tt:mm:ss:ff, where tt is tracks, mm is minutes, ss is seconds, and ff is frames.</span></span> <span data-ttu-id="d7666-481">Puede omitir un campo si este y todos los campos siguientes son cero.</span><span class="sxs-lookup"><span data-stu-id="d7666-481">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="d7666-482">Por ejemplo, 3, 3:0, 3:0:0 y 3:0:0:0 son formas válidas de expresar el seguimiento 3.</span><span class="sxs-lookup"><span data-stu-id="d7666-482">For example, 3, 3:0, 3:0:0, and 3:0:0:0 are all valid ways to express track 3.</span></span> <br/> <span data-ttu-id="d7666-483">Los campos TMSF tienen los siguientes valores máximos:</span><span class="sxs-lookup"><span data-stu-id="d7666-483">The TMSF fields have the following maximum values:</span></span><br/>
<ul>
<li><span data-ttu-id="d7666-484">Realiza un seguimiento de 99</span><span class="sxs-lookup"><span data-stu-id="d7666-484">Tracks 99</span></span></li>
<li><span data-ttu-id="d7666-485">Minutos 90</span><span class="sxs-lookup"><span data-stu-id="d7666-485">Minutes 90</span></span></li>
<li><span data-ttu-id="d7666-486">Segundos 59</span><span class="sxs-lookup"><span data-stu-id="d7666-486">Seconds 59</span></span></li>
<li><span data-ttu-id="d7666-487">Marcos 74</span><span class="sxs-lookup"><span data-stu-id="d7666-487">Frames 74</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-488">seguimiento de formato de hora</span><span class="sxs-lookup"><span data-stu-id="d7666-488">time format track</span></span></td>
<td><span data-ttu-id="d7666-489">Establece el formato de posición en las pistas.</span><span class="sxs-lookup"><span data-stu-id="d7666-489">Sets the position format to tracks.</span></span> <span data-ttu-id="d7666-490">Todos los comandos que usan valores de posición asumirán pistas.</span><span class="sxs-lookup"><span data-stu-id="d7666-490">All commands that use position values will assume tracks.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-491">contador de modo de tiempo</span><span class="sxs-lookup"><span data-stu-id="d7666-491">time mode counter</span></span></td>
<td><span data-ttu-id="d7666-492">Establece el modo de información de posición para utilizar los contadores de VCR.</span><span class="sxs-lookup"><span data-stu-id="d7666-492">Sets the position-information mode to use the VCR counters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-493">detección del modo de tiempo</span><span class="sxs-lookup"><span data-stu-id="d7666-493">time mode detect</span></span></td>
<td><span data-ttu-id="d7666-494">Establece el modo de información de posición en función de la detección de información de código de tiempo en la cinta.</span><span class="sxs-lookup"><span data-stu-id="d7666-494">Sets the position information mode based on detection of timecode information on the tape.</span></span> <span data-ttu-id="d7666-495">Si se detecta información de código de tiempo, el tipo de tiempo se establece en código de tiempo &quot; &quot; ; de lo contrario, el tipo de hora se establece en &quot; Counter &quot; .</span><span class="sxs-lookup"><span data-stu-id="d7666-495">If timecode information is detected, the time type is set to &quot;timecode&quot;; otherwise, the time type is set to &quot;counter&quot;.</span></span> <span data-ttu-id="d7666-496">&quot;&quot;La detección es un modo especial.</span><span class="sxs-lookup"><span data-stu-id="d7666-496">&quot;Detect&quot; is a special mode.</span></span> <span data-ttu-id="d7666-497">Cada vez que se abre el controlador, se inserta una nueva cinta o &quot; se emite el comando de modo de hora &quot; , el controlador comprueba el modo de hora actual disponible en la cinta y establece el &quot; tipo de hora &quot; en código de tiempo &quot; &quot; o &quot; contador &quot; .</span><span class="sxs-lookup"><span data-stu-id="d7666-497">Whenever the driver is opened, a new tape is inserted, or the &quot;time mode&quot; command is issued, the driver checks the current time mode available on the tape and sets &quot;time type&quot; to either &quot;timecode&quot; or &quot;counter&quot;.</span></span> <span data-ttu-id="d7666-498">Una vez &quot; establecido el tipo de tiempo &quot; , el controlador no lo cambia hasta que no se produce una de las condiciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="d7666-498">Once &quot;time type&quot; is set, the driver doesn't change it until one of the above conditions occurs again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-499">código de tiempo del modo de tiempo</span><span class="sxs-lookup"><span data-stu-id="d7666-499">time mode timecode</span></span></td>
<td><span data-ttu-id="d7666-500">Establece el modo de información de posición para utilizar &quot; &quot; la información de código de tiempo de la cinta.</span><span class="sxs-lookup"><span data-stu-id="d7666-500">Sets the position information mode to use &quot;timecode&quot; information on the tape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-501">más seguimiento</span><span class="sxs-lookup"><span data-stu-id="d7666-501">tracking plus</span></span> <br/> <span data-ttu-id="d7666-502">seguimiento menos</span><span class="sxs-lookup"><span data-stu-id="d7666-502">tracking minus</span></span> <br/> <span data-ttu-id="d7666-503">restablecimiento de seguimiento</span><span class="sxs-lookup"><span data-stu-id="d7666-503">tracking reset</span></span> <br/></td>
<td><span data-ttu-id="d7666-504">Ajusta la velocidad del transporte de cinta de vídeo en incrementos precisos.</span><span class="sxs-lookup"><span data-stu-id="d7666-504">Adjusts the speed of the videotape transport in fine increments.</span></span> <span data-ttu-id="d7666-505">Use las &quot; &quot; marcas de seguimiento cuando se obtenga una imagen ruidosa de un VCR.</span><span class="sxs-lookup"><span data-stu-id="d7666-505">Use the &quot;tracking&quot; flags when a noisy picture is obtained from a VCR.</span></span> <span data-ttu-id="d7666-506">&quot;El seguimiento más &quot; aumenta la velocidad de transporte.</span><span class="sxs-lookup"><span data-stu-id="d7666-506">&quot;Tracking plus&quot; increases the transport speed.</span></span> <span data-ttu-id="d7666-507">&quot;El seguimiento menos &quot; disminuye la velocidad de transporte.</span><span class="sxs-lookup"><span data-stu-id="d7666-507">&quot;Tracking minus&quot; decreases the transport speed.</span></span> <span data-ttu-id="d7666-508">&quot;El restablecimiento de seguimiento &quot; devuelve el ajuste de seguimiento a cero.</span><span class="sxs-lookup"><span data-stu-id="d7666-508">&quot;Tracking reset&quot; returns the tracking adjustment to zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7666-509">vídeo desactivado</span><span class="sxs-lookup"><span data-stu-id="d7666-509">video off</span></span></td>
<td><span data-ttu-id="d7666-510">Deshabilita la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d7666-510">Disables video output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7666-511">vídeo sobre</span><span class="sxs-lookup"><span data-stu-id="d7666-511">video on</span></span></td>
<td><span data-ttu-id="d7666-512">Habilita la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d7666-512">Enables video output.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="d7666-513"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="d7666-513"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d7666-514">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="d7666-514">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="d7666-515">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="d7666-515">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="d7666-516">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d7666-516">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7666-517">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7666-517">Return Value</span></span>

<span data-ttu-id="d7666-518">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d7666-518">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7666-519">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7666-519">Remarks</span></span>

<span data-ttu-id="d7666-520">Se definen varias propiedades de los datos de audio de forma de onda cuando se crea el archivo en el que se almacenan los datos.</span><span class="sxs-lookup"><span data-stu-id="d7666-520">Several properties of waveform-audio data are defined when the file to store the data is created.</span></span> <span data-ttu-id="d7666-521">Estas propiedades describen cómo se estructuran los datos en el archivo y no se pueden cambiar una vez que se inicia la grabación.</span><span class="sxs-lookup"><span data-stu-id="d7666-521">These properties describe how the data is structured within the file and cannot be changed once recording begins.</span></span> <span data-ttu-id="d7666-522">En la lista siguiente se identifican estas propiedades:</span><span class="sxs-lookup"><span data-stu-id="d7666-522">The following list identifies these properties:</span></span>

-   <span data-ttu-id="d7666-523">alineación</span><span class="sxs-lookup"><span data-stu-id="d7666-523">alignment</span></span>
-   <span data-ttu-id="d7666-524">bitspersample</span><span class="sxs-lookup"><span data-stu-id="d7666-524">bitspersample</span></span>
-   <span data-ttu-id="d7666-525">bytespersec</span><span class="sxs-lookup"><span data-stu-id="d7666-525">bytespersec</span></span>
-   <span data-ttu-id="d7666-526">canales nueva</span><span class="sxs-lookup"><span data-stu-id="d7666-526">channels</span></span>
-   <span data-ttu-id="d7666-527">etiqueta de formato</span><span class="sxs-lookup"><span data-stu-id="d7666-527">format tag</span></span>
-   <span data-ttu-id="d7666-528">samplespersec</span><span class="sxs-lookup"><span data-stu-id="d7666-528">samplespersec</span></span>

## <a name="examples"></a><span data-ttu-id="d7666-529">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d7666-529">Examples</span></span>

<span data-ttu-id="d7666-530">El siguiente comando establece el formato de hora en milisegundos y establece el formato de audio de forma de onda en 8 bits, mono, 11 kHz.</span><span class="sxs-lookup"><span data-stu-id="d7666-530">The following command sets the time format to milliseconds and sets the waveform-audio format to 8 bit, mono, 11 kHz.</span></span>

``` syntax
set mysound time format ms bitspersample 8 channels 1 samplespersec 11025
```

## <a name="requirements"></a><span data-ttu-id="d7666-531">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7666-531">Requirements</span></span>



| <span data-ttu-id="d7666-532">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7666-532">Requirement</span></span> | <span data-ttu-id="d7666-533">Value</span><span class="sxs-lookup"><span data-stu-id="d7666-533">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d7666-534">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7666-534">Minimum supported client</span></span><br/> | <span data-ttu-id="d7666-535">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d7666-535">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d7666-536">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7666-536">Minimum supported server</span></span><br/> | <span data-ttu-id="d7666-537">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d7666-537">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d7666-538">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7666-538">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7666-539">MCI</span><span class="sxs-lookup"><span data-stu-id="d7666-539">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d7666-540">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="d7666-540">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="d7666-541">grabar</span><span class="sxs-lookup"><span data-stu-id="d7666-541">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="d7666-542">pause</span><span class="sxs-lookup"><span data-stu-id="d7666-542">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="d7666-543">guardar</span><span class="sxs-lookup"><span data-stu-id="d7666-543">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="d7666-544">stop</span><span class="sxs-lookup"><span data-stu-id="d7666-544">stop</span></span>](stop.md)
</dt> </dl>

 

