---
title: Estado (comando)
description: El comando de estado solicita información de estado de un dispositivo. Todos los dispositivos reconocen este comando.
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- comando de estado Windows multimedia
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ab184ddaca16d0ea96b86a6b062f1e66e2eee2
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2021
ms.locfileid: "105678603"
---
# <a name="status-command"></a><span data-ttu-id="a4d79-105">Estado (comando)</span><span class="sxs-lookup"><span data-stu-id="a4d79-105">status command</span></span>

> [!NOTE]
> <span data-ttu-id="a4d79-106">Comunicación sin polarización: Microsoft admite un entorno diverso y de inclusión.</span><span class="sxs-lookup"><span data-stu-id="a4d79-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="a4d79-107">Dentro de este documento, hay referencias a la palabra ' Slave '.</span><span class="sxs-lookup"><span data-stu-id="a4d79-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="a4d79-108">La guía de estilo de Microsoft [para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo reconoce como una palabra de exclusión.</span><span class="sxs-lookup"><span data-stu-id="a4d79-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="a4d79-109">Este texto se usa tal como está actualmente el texto que se usa en los comandos.</span><span class="sxs-lookup"><span data-stu-id="a4d79-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="a4d79-110">Para mantener la coherencia, este documento contiene esta palabra.</span><span class="sxs-lookup"><span data-stu-id="a4d79-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="a4d79-111">Cuando se modifique esta palabra en los comandos, se corregirá este documento para que esté alineado.</span><span class="sxs-lookup"><span data-stu-id="a4d79-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="a4d79-112">El comando de estado solicita información de estado de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-112">The status command requests status information from a device.</span></span> <span data-ttu-id="a4d79-113">Todos los dispositivos reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="a4d79-113">All devices recognize this command.</span></span>

<span data-ttu-id="a4d79-114">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="a4d79-114">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("status %s %s %s"),
  lpszDeviceID,
  lpszRequest,
  lpszFlags
);
      
```

## <a name="parameters"></a><span data-ttu-id="a4d79-115">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4d79-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4d79-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a4d79-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a4d79-117">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="a4d79-117">Identifier of an MCI device.</span></span> <span data-ttu-id="a4d79-118">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-118">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="a4d79-119"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span><span class="sxs-lookup"><span data-stu-id="a4d79-119"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span></span>
</dt> <dd>

<span data-ttu-id="a4d79-120">Marca para solicitar información de estado.</span><span class="sxs-lookup"><span data-stu-id="a4d79-120">Flag for requesting status information.</span></span> <span data-ttu-id="a4d79-121">En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **status** y las marcas usadas por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-121">The following table lists device types that recognize the **status** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4d79-122">Tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a4d79-122">Device Type</span></span></th>
<th><span data-ttu-id="a4d79-123">Marcas de solicitud</span><span class="sxs-lookup"><span data-stu-id="a4d79-123">Request Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4d79-124">cdaudio</span><span class="sxs-lookup"><span data-stu-id="a4d79-124">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="a4d79-125"><em>número</em> de pista de tipo cdaudio</span><span class="sxs-lookup"><span data-stu-id="a4d79-125">cdaudio type track <em>number</em></span></span></li>
<li><span data-ttu-id="a4d79-126">pista actual</span><span class="sxs-lookup"><span data-stu-id="a4d79-126">current track</span></span></li>
<li><span data-ttu-id="a4d79-127">length</span><span class="sxs-lookup"><span data-stu-id="a4d79-127">length</span></span></li>
<li><span data-ttu-id="a4d79-128"><em>número</em> de pista de longitud</span><span class="sxs-lookup"><span data-stu-id="a4d79-128">length track <em>number</em></span></span></li>
<li><span data-ttu-id="a4d79-129">medio presente</span><span class="sxs-lookup"><span data-stu-id="a4d79-129">media present</span></span></li>
<li><span data-ttu-id="a4d79-130">mode</span><span class="sxs-lookup"><span data-stu-id="a4d79-130">mode</span></span></li>
<li><span data-ttu-id="a4d79-131">número de pistas</span><span class="sxs-lookup"><span data-stu-id="a4d79-131">number of tracks</span></span></li>
<li><span data-ttu-id="a4d79-132">position</span><span class="sxs-lookup"><span data-stu-id="a4d79-132">position</span></span></li>
<li><span data-ttu-id="a4d79-133"><em>número</em> de pista de posición</span><span class="sxs-lookup"><span data-stu-id="a4d79-133">position track <em>number</em></span></span></li>
<li><span data-ttu-id="a4d79-134">ready</span><span class="sxs-lookup"><span data-stu-id="a4d79-134">ready</span></span></li>
<li><span data-ttu-id="a4d79-135">posición inicial</span><span class="sxs-lookup"><span data-stu-id="a4d79-135">start position</span></span></li>
<li><span data-ttu-id="a4d79-136">formato de hora</span><span class="sxs-lookup"><span data-stu-id="a4d79-136">time format</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-137">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="a4d79-137">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="a4d79-138">audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-138">audio</span></span></li>
<li><span data-ttu-id="a4d79-139">alineación de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-139">audio alignment</span></span></li>
<li><span data-ttu-id="a4d79-140">audio BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="a4d79-140">audio bitspersample</span></span></li>
<li><span data-ttu-id="a4d79-141">interrupciones de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-141">audio breaks</span></span></li>
<li><span data-ttu-id="a4d79-142">audio bytespersec</span><span class="sxs-lookup"><span data-stu-id="a4d79-142">audio bytespersec</span></span></li>
<li><span data-ttu-id="a4d79-143">entrada de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-143">audio input</span></span></li>
<li><span data-ttu-id="a4d79-144">registro de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-144">audio record</span></span></li>
<li><span data-ttu-id="a4d79-145">origen de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-145">audio source</span></span></li>
<li><span data-ttu-id="a4d79-146">audio SamplesPerSec</span><span class="sxs-lookup"><span data-stu-id="a4d79-146">audio samplespersec</span></span></li>
<li><span data-ttu-id="a4d79-147">secuencia de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-147">audio stream</span></span></li>
<li><span data-ttu-id="a4d79-148">improvisa</span><span class="sxs-lookup"><span data-stu-id="a4d79-148">bass</span></span></li>
<li><span data-ttu-id="a4d79-149">BitsPerPel</span><span class="sxs-lookup"><span data-stu-id="a4d79-149">bitsperpel</span></span></li>
<li><span data-ttu-id="a4d79-150">luminosidad</span><span class="sxs-lookup"><span data-stu-id="a4d79-150">brightness</span></span></li>
<li><span data-ttu-id="a4d79-151">color</span><span class="sxs-lookup"><span data-stu-id="a4d79-151">color</span></span></li>
<li><span data-ttu-id="a4d79-152">contraste</span><span class="sxs-lookup"><span data-stu-id="a4d79-152">contrast</span></span></li>
<li><span data-ttu-id="a4d79-153">pista actual</span><span class="sxs-lookup"><span data-stu-id="a4d79-153">current track</span></span></li>
<li><span data-ttu-id="a4d79-154"><em>unidad</em> de espacio en disco</span><span class="sxs-lookup"><span data-stu-id="a4d79-154">disk space <em>drive</em></span></span></li>
<li><span data-ttu-id="a4d79-155">finalización de archivos</span><span class="sxs-lookup"><span data-stu-id="a4d79-155">file completion</span></span></li>
<li><span data-ttu-id="a4d79-156">formato del archivo</span><span class="sxs-lookup"><span data-stu-id="a4d79-156">file format</span></span></li>
<li><span data-ttu-id="a4d79-157">modo de archivo</span><span class="sxs-lookup"><span data-stu-id="a4d79-157">file mode</span></span></li>
<li><span data-ttu-id="a4d79-158">forward</span><span class="sxs-lookup"><span data-stu-id="a4d79-158">forward</span></span></li>
<li><span data-ttu-id="a4d79-159">fotogramas omitidos</span><span class="sxs-lookup"><span data-stu-id="a4d79-159">frames skipped</span></span></li>
<li><span data-ttu-id="a4d79-160">gamma</span><span class="sxs-lookup"><span data-stu-id="a4d79-160">gamma</span></span></li>
<li><span data-ttu-id="a4d79-161">input</span><span class="sxs-lookup"><span data-stu-id="a4d79-161">input</span></span></li>
<li><span data-ttu-id="a4d79-162">volumen izquierdo</span><span class="sxs-lookup"><span data-stu-id="a4d79-162">left volume</span></span></li>
<li><span data-ttu-id="a4d79-163">length</span><span class="sxs-lookup"><span data-stu-id="a4d79-163">length</span></span></li>
<li><span data-ttu-id="a4d79-164"><em>número</em> de pista de longitud</span><span class="sxs-lookup"><span data-stu-id="a4d79-164">length track <em>number</em></span></span></li>
<li><span data-ttu-id="a4d79-165">medio presente</span><span class="sxs-lookup"><span data-stu-id="a4d79-165">media present</span></span></li>
<li><span data-ttu-id="a4d79-166">mode</span><span class="sxs-lookup"><span data-stu-id="a4d79-166">mode</span></span></li>
<li><span data-ttu-id="a4d79-167">monitor</span><span class="sxs-lookup"><span data-stu-id="a4d79-167">monitor</span></span></li>
<li><span data-ttu-id="a4d79-168">monitor (método)</span><span class="sxs-lookup"><span data-stu-id="a4d79-168">monitor method</span></span></li>
<li><span data-ttu-id="a4d79-169">tasa</span><span class="sxs-lookup"><span data-stu-id="a4d79-169">nominal</span></span></li>
<li><span data-ttu-id="a4d79-170">velocidad de fotogramas nominal</span><span class="sxs-lookup"><span data-stu-id="a4d79-170">nominal frame rate</span></span></li>
<li><span data-ttu-id="a4d79-171">velocidad de fotogramas de registro nominal</span><span class="sxs-lookup"><span data-stu-id="a4d79-171">nominal record frame rate</span></span></li>
<li><span data-ttu-id="a4d79-172">número de pistas</span><span class="sxs-lookup"><span data-stu-id="a4d79-172">number of tracks</span></span></li>
<li><span data-ttu-id="a4d79-173">output</span><span class="sxs-lookup"><span data-stu-id="a4d79-173">output</span></span></li>
<li><span data-ttu-id="a4d79-174">identificador de paleta</span><span class="sxs-lookup"><span data-stu-id="a4d79-174">palette handle</span></span></li>
<li><span data-ttu-id="a4d79-175">modo de pausa</span><span class="sxs-lookup"><span data-stu-id="a4d79-175">pause mode</span></span></li>
<li><span data-ttu-id="a4d79-176">velocidad de reproducción</span><span class="sxs-lookup"><span data-stu-id="a4d79-176">play speed</span></span></li>
<li><span data-ttu-id="a4d79-177">position</span><span class="sxs-lookup"><span data-stu-id="a4d79-177">position</span></span></li>
<li><span data-ttu-id="a4d79-178"><em>número</em> de pista de posición</span><span class="sxs-lookup"><span data-stu-id="a4d79-178">position track <em>number</em></span></span></li>
<li><span data-ttu-id="a4d79-179">ready</span><span class="sxs-lookup"><span data-stu-id="a4d79-179">ready</span></span></li>
<li><span data-ttu-id="a4d79-180">velocidad de fotogramas de registro</span><span class="sxs-lookup"><span data-stu-id="a4d79-180">record frame rate</span></span></li>
<li><span data-ttu-id="a4d79-181"><em>marco</em> de referencia</span><span class="sxs-lookup"><span data-stu-id="a4d79-181">reference <em>frame</em></span></span></li>
<li><span data-ttu-id="a4d79-182">tamaño reservado</span><span class="sxs-lookup"><span data-stu-id="a4d79-182">reserved size</span></span></li>
<li><span data-ttu-id="a4d79-183">volumen derecho</span><span class="sxs-lookup"><span data-stu-id="a4d79-183">right volume</span></span></li>
<li><span data-ttu-id="a4d79-184">Buscar exactamente</span><span class="sxs-lookup"><span data-stu-id="a4d79-184">seek exactly</span></span></li>
<li><span data-ttu-id="a4d79-185">nitidez</span><span class="sxs-lookup"><span data-stu-id="a4d79-185">sharpness</span></span></li>
<li><span data-ttu-id="a4d79-186">SMPTE</span><span class="sxs-lookup"><span data-stu-id="a4d79-186">smpte</span></span></li>
<li><span data-ttu-id="a4d79-187">velocidad</span><span class="sxs-lookup"><span data-stu-id="a4d79-187">speed</span></span></li>
<li><span data-ttu-id="a4d79-188">posición inicial</span><span class="sxs-lookup"><span data-stu-id="a4d79-188">start position</span></span></li>
<li><span data-ttu-id="a4d79-189">formato de archivo todavía</span><span class="sxs-lookup"><span data-stu-id="a4d79-189">still file format</span></span></li>
<li><span data-ttu-id="a4d79-190">formato de hora</span><span class="sxs-lookup"><span data-stu-id="a4d79-190">time format</span></span></li>
<li><span data-ttu-id="a4d79-191">trama</span><span class="sxs-lookup"><span data-stu-id="a4d79-191">tint</span></span></li>
<li><span data-ttu-id="a4d79-192">agudos</span><span class="sxs-lookup"><span data-stu-id="a4d79-192">treble</span></span></li>
<li><span data-ttu-id="a4d79-193">no guardados</span><span class="sxs-lookup"><span data-stu-id="a4d79-193">unsaved</span></span></li>
<li><span data-ttu-id="a4d79-194">video</span><span class="sxs-lookup"><span data-stu-id="a4d79-194">video</span></span></li>
<li><span data-ttu-id="a4d79-195">Índice de clave de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-195">video key index</span></span></li>
<li><span data-ttu-id="a4d79-196">color de clave de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-196">video key color</span></span></li>
<li><span data-ttu-id="a4d79-197">grabación de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-197">video record</span></span></li>
<li><span data-ttu-id="a4d79-198">origen de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-198">video source</span></span></li>
<li><span data-ttu-id="a4d79-199">número de origen de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-199">video source number</span></span></li>
<li><span data-ttu-id="a4d79-200">secuencia de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-200">video stream</span></span></li>
<li><span data-ttu-id="a4d79-201">volumen</span><span class="sxs-lookup"><span data-stu-id="a4d79-201">volume</span></span></li>
<li><span data-ttu-id="a4d79-202">identificador de ventana</span><span class="sxs-lookup"><span data-stu-id="a4d79-202">window handle</span></span></li>
<li><span data-ttu-id="a4d79-203">ventana visible</span><span class="sxs-lookup"><span data-stu-id="a4d79-203">window visible</span></span></li>
<li><span data-ttu-id="a4d79-204">ventana minimizada</span><span class="sxs-lookup"><span data-stu-id="a4d79-204">window minimized</span></span></li>
<li><span data-ttu-id="a4d79-205">ventana maximizada</span><span class="sxs-lookup"><span data-stu-id="a4d79-205">window maximized</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-206">overlay</span><span class="sxs-lookup"><span data-stu-id="a4d79-206">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="a4d79-207">medio presente</span><span class="sxs-lookup"><span data-stu-id="a4d79-207">media present</span></span></li>
<li><span data-ttu-id="a4d79-208">mode</span><span class="sxs-lookup"><span data-stu-id="a4d79-208">mode</span></span></li>
<li><span data-ttu-id="a4d79-209">número de pistas</span><span class="sxs-lookup"><span data-stu-id="a4d79-209">number of tracks</span></span></li>
<li><span data-ttu-id="a4d79-210">ready</span><span class="sxs-lookup"><span data-stu-id="a4d79-210">ready</span></span></li>
<li><span data-ttu-id="a4d79-211">ajustar</span><span class="sxs-lookup"><span data-stu-id="a4d79-211">stretch</span></span></li>
<li><span data-ttu-id="a4d79-212">identificador de ventana</span><span class="sxs-lookup"><span data-stu-id="a4d79-212">window handle</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-213">sequencer</span><span class="sxs-lookup"><span data-stu-id="a4d79-213">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="a4d79-214">pista actual</span><span class="sxs-lookup"><span data-stu-id="a4d79-214">current track</span></span></li>
<li><span data-ttu-id="a4d79-215">tipo de división</span><span class="sxs-lookup"><span data-stu-id="a4d79-215">division type</span></span></li>
<li><span data-ttu-id="a4d79-216">length</span><span class="sxs-lookup"><span data-stu-id="a4d79-216">length</span></span></li>
<li><span data-ttu-id="a4d79-217">patrón de <em>número</em> de pista de longitud</span><span class="sxs-lookup"><span data-stu-id="a4d79-217">length track <em>number</em> master</span></span></li>
<li><span data-ttu-id="a4d79-218">medio presente</span><span class="sxs-lookup"><span data-stu-id="a4d79-218">media present</span></span></li>
<li><span data-ttu-id="a4d79-219">mode</span><span class="sxs-lookup"><span data-stu-id="a4d79-219">mode</span></span></li>
<li><span data-ttu-id="a4d79-220">número de pistas</span><span class="sxs-lookup"><span data-stu-id="a4d79-220">number of tracks</span></span></li>
<li><span data-ttu-id="a4d79-221">offset</span><span class="sxs-lookup"><span data-stu-id="a4d79-221">offset</span></span></li>
<li><span data-ttu-id="a4d79-222">port</span><span class="sxs-lookup"><span data-stu-id="a4d79-222">port</span></span></li>
<li><span data-ttu-id="a4d79-223">position</span><span class="sxs-lookup"><span data-stu-id="a4d79-223">position</span></span></li>
<li><span data-ttu-id="a4d79-224"><em>número</em> de pista de posición</span><span class="sxs-lookup"><span data-stu-id="a4d79-224">position track <em>number</em></span></span></li>
<li><span data-ttu-id="a4d79-225">ready</span><span class="sxs-lookup"><span data-stu-id="a4d79-225">ready</span></span></li>
<li><span data-ttu-id="a4d79-226">satélite</span><span class="sxs-lookup"><span data-stu-id="a4d79-226">slave</span></span></li>
<li><span data-ttu-id="a4d79-227">posición inicial</span><span class="sxs-lookup"><span data-stu-id="a4d79-227">start position</span></span></li>
<li><span data-ttu-id="a4d79-228">ritmo</span><span class="sxs-lookup"><span data-stu-id="a4d79-228">tempo</span></span></li>
<li><span data-ttu-id="a4d79-229">formato de hora</span><span class="sxs-lookup"><span data-stu-id="a4d79-229">time format</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-230">vídeos</span><span class="sxs-lookup"><span data-stu-id="a4d79-230">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="a4d79-231">ensamblar registro</span><span class="sxs-lookup"><span data-stu-id="a4d79-231">assemble record</span></span></li>
<li><span data-ttu-id="a4d79-232">monitor de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-232">audio monitor</span></span></li>
<li><span data-ttu-id="a4d79-233">número de monitor de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-233">audio monitor number</span></span></li>
<li><span data-ttu-id="a4d79-234">registro de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-234">audio record</span></span></li>
<li><span data-ttu-id="a4d79-235"><em>número</em> de pista de grabación de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-235">audio record track <em>number</em></span></span></li>
<li><span data-ttu-id="a4d79-236">origen de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-236">audio source</span></span></li>
<li><span data-ttu-id="a4d79-237">número de origen de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-237">audio source number</span></span></li>
<li><span data-ttu-id="a4d79-238">canal</span><span class="sxs-lookup"><span data-stu-id="a4d79-238">channel</span></span></li>
<li><span data-ttu-id="a4d79-239"><em>número</em> de sintonizador de canal</span><span class="sxs-lookup"><span data-stu-id="a4d79-239">channel tuner <em>number</em></span></span></li>
<li><span data-ttu-id="a4d79-240">clock</span><span class="sxs-lookup"><span data-stu-id="a4d79-240">clock</span></span></li>
<li><span data-ttu-id="a4d79-241">ID. del reloj</span><span class="sxs-lookup"><span data-stu-id="a4d79-241">clock id</span></span></li>
<li><span data-ttu-id="a4d79-242">counter</span><span class="sxs-lookup"><span data-stu-id="a4d79-242">counter</span></span></li>
<li><span data-ttu-id="a4d79-243">formato del contador</span><span class="sxs-lookup"><span data-stu-id="a4d79-243">counter format</span></span></li>
<li><span data-ttu-id="a4d79-244">resolución de contadores</span><span class="sxs-lookup"><span data-stu-id="a4d79-244">counter resolution</span></span></li>
<li><span data-ttu-id="a4d79-245">pista actual</span><span class="sxs-lookup"><span data-stu-id="a4d79-245">current track</span></span></li>
<li><span data-ttu-id="a4d79-246">velocidad de fotogramas</span><span class="sxs-lookup"><span data-stu-id="a4d79-246">frame rate</span></span></li>
<li><span data-ttu-id="a4d79-247">índice</span><span class="sxs-lookup"><span data-stu-id="a4d79-247">index</span></span></li>
<li><span data-ttu-id="a4d79-248">índice en</span><span class="sxs-lookup"><span data-stu-id="a4d79-248">index on</span></span></li>
<li><span data-ttu-id="a4d79-249">length</span><span class="sxs-lookup"><span data-stu-id="a4d79-249">length</span></span></li>
<li><span data-ttu-id="a4d79-250"><em>número</em> de pista de longitud</span><span class="sxs-lookup"><span data-stu-id="a4d79-250">length track <em>number</em></span></span></li>
<li><span data-ttu-id="a4d79-251">medio presente</span><span class="sxs-lookup"><span data-stu-id="a4d79-251">media present</span></span></li>
<li><span data-ttu-id="a4d79-252">tipo de medio</span><span class="sxs-lookup"><span data-stu-id="a4d79-252">media type</span></span></li>
<li><span data-ttu-id="a4d79-253">mode</span><span class="sxs-lookup"><span data-stu-id="a4d79-253">mode</span></span></li>
<li><span data-ttu-id="a4d79-254">número de pistas de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-254">number of audio tracks</span></span></li>
<li><span data-ttu-id="a4d79-255">número de pistas</span><span class="sxs-lookup"><span data-stu-id="a4d79-255">number of tracks</span></span></li>
<li><span data-ttu-id="a4d79-256">número de pistas de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-256">number of video tracks</span></span></li>
<li><span data-ttu-id="a4d79-257"><em>tiempo de espera</em> de pausa</span><span class="sxs-lookup"><span data-stu-id="a4d79-257">pause <em>timeout</em></span></span></li>
<li><span data-ttu-id="a4d79-258">formato de reproducción</span><span class="sxs-lookup"><span data-stu-id="a4d79-258">play format</span></span></li>
<li><span data-ttu-id="a4d79-259">position</span><span class="sxs-lookup"><span data-stu-id="a4d79-259">position</span></span></li>
<li><span data-ttu-id="a4d79-260">posición inicial</span><span class="sxs-lookup"><span data-stu-id="a4d79-260">position start</span></span></li>
<li><span data-ttu-id="a4d79-261"><em>número</em> de pista de posición</span><span class="sxs-lookup"><span data-stu-id="a4d79-261">position track <em>number</em></span></span></li>
<li><span data-ttu-id="a4d79-262"><em>duración</em> del PostRoll</span><span class="sxs-lookup"><span data-stu-id="a4d79-262">postroll <em>duration</em></span></span></li>
<li><span data-ttu-id="a4d79-263">encendido</span><span class="sxs-lookup"><span data-stu-id="a4d79-263">power on</span></span></li>
<li><span data-ttu-id="a4d79-264"><em>duración</em> del prelanzamiento</span><span class="sxs-lookup"><span data-stu-id="a4d79-264">preroll <em>duration</em></span></span></li>
<li><span data-ttu-id="a4d79-265">ready</span><span class="sxs-lookup"><span data-stu-id="a4d79-265">ready</span></span></li>
<li><span data-ttu-id="a4d79-266">formato de registro</span><span class="sxs-lookup"><span data-stu-id="a4d79-266">record format</span></span></li>
<li><span data-ttu-id="a4d79-267">velocidad</span><span class="sxs-lookup"><span data-stu-id="a4d79-267">speed</span></span></li>
<li><span data-ttu-id="a4d79-268">formato de hora</span><span class="sxs-lookup"><span data-stu-id="a4d79-268">time format</span></span></li>
<li><span data-ttu-id="a4d79-269">modo de tiempo</span><span class="sxs-lookup"><span data-stu-id="a4d79-269">time mode</span></span></li>
<li><span data-ttu-id="a4d79-270">tipo de tiempo</span><span class="sxs-lookup"><span data-stu-id="a4d79-270">time type</span></span></li>
<li><span data-ttu-id="a4d79-271">código de tiempo presente</span><span class="sxs-lookup"><span data-stu-id="a4d79-271">timecode present</span></span></li>
<li><span data-ttu-id="a4d79-272">registro de código de tiempo</span><span class="sxs-lookup"><span data-stu-id="a4d79-272">timecode record</span></span></li>
<li><span data-ttu-id="a4d79-273">tipo de código de tiempo</span><span class="sxs-lookup"><span data-stu-id="a4d79-273">timecode type</span></span></li>
<li><span data-ttu-id="a4d79-274">número de sintonizador</span><span class="sxs-lookup"><span data-stu-id="a4d79-274">tuner number</span></span></li>
<li><span data-ttu-id="a4d79-275">monitor de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-275">video monitor</span></span></li>
<li><span data-ttu-id="a4d79-276">número de monitor de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-276">video monitor number</span></span></li>
<li><span data-ttu-id="a4d79-277">grabación de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-277">video record</span></span></li>
<li><span data-ttu-id="a4d79-278"><em>número</em> de pista de grabación de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-278">video record track <em>number</em></span></span></li>
<li><span data-ttu-id="a4d79-279">origen de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-279">video source</span></span></li>
<li><span data-ttu-id="a4d79-280">número de origen de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-280">video source number</span></span></li>
<li><span data-ttu-id="a4d79-281">protegido contra escritura</span><span class="sxs-lookup"><span data-stu-id="a4d79-281">write protected</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-282">videodisco</span><span class="sxs-lookup"><span data-stu-id="a4d79-282">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="a4d79-283">pista actual</span><span class="sxs-lookup"><span data-stu-id="a4d79-283">current track</span></span></li>
<li><span data-ttu-id="a4d79-284">tamaño del disco</span><span class="sxs-lookup"><span data-stu-id="a4d79-284">disc size</span></span></li>
<li><span data-ttu-id="a4d79-285">forward</span><span class="sxs-lookup"><span data-stu-id="a4d79-285">forward</span></span></li>
<li><span data-ttu-id="a4d79-286">length</span><span class="sxs-lookup"><span data-stu-id="a4d79-286">length</span></span></li>
<li><span data-ttu-id="a4d79-287"><em>número</em> de pista de longitud</span><span class="sxs-lookup"><span data-stu-id="a4d79-287">length track <em>number</em></span></span></li>
<li><span data-ttu-id="a4d79-288">medio presente</span><span class="sxs-lookup"><span data-stu-id="a4d79-288">media present</span></span></li>
<li><span data-ttu-id="a4d79-289">tipo de medio</span><span class="sxs-lookup"><span data-stu-id="a4d79-289">media type</span></span></li>
<li><span data-ttu-id="a4d79-290">mode</span><span class="sxs-lookup"><span data-stu-id="a4d79-290">mode</span></span></li>
<li><span data-ttu-id="a4d79-291">número de pistas</span><span class="sxs-lookup"><span data-stu-id="a4d79-291">number of tracks</span></span></li>
<li><span data-ttu-id="a4d79-292">position</span><span class="sxs-lookup"><span data-stu-id="a4d79-292">position</span></span></li>
<li><span data-ttu-id="a4d79-293"><em>número</em> de pista de posición</span><span class="sxs-lookup"><span data-stu-id="a4d79-293">position track <em>number</em></span></span></li>
<li><span data-ttu-id="a4d79-294">ready</span><span class="sxs-lookup"><span data-stu-id="a4d79-294">ready</span></span></li>
<li><span data-ttu-id="a4d79-295">margen</span><span class="sxs-lookup"><span data-stu-id="a4d79-295">side</span></span></li>
<li><span data-ttu-id="a4d79-296">velocidad</span><span class="sxs-lookup"><span data-stu-id="a4d79-296">speed</span></span></li>
<li><span data-ttu-id="a4d79-297">posición inicial</span><span class="sxs-lookup"><span data-stu-id="a4d79-297">start position</span></span></li>
<li><span data-ttu-id="a4d79-298">formato de hora</span><span class="sxs-lookup"><span data-stu-id="a4d79-298">time format</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-299">waveaudio</span><span class="sxs-lookup"><span data-stu-id="a4d79-299">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="a4d79-300">alineación</span><span class="sxs-lookup"><span data-stu-id="a4d79-300">alignment</span></span></li>
<li><span data-ttu-id="a4d79-301">bitspersample</span><span class="sxs-lookup"><span data-stu-id="a4d79-301">bitspersample</span></span></li>
<li><span data-ttu-id="a4d79-302">bytespersec</span><span class="sxs-lookup"><span data-stu-id="a4d79-302">bytespersec</span></span></li>
<li><span data-ttu-id="a4d79-303">canales nueva</span><span class="sxs-lookup"><span data-stu-id="a4d79-303">channels</span></span></li>
<li><span data-ttu-id="a4d79-304">pista actual</span><span class="sxs-lookup"><span data-stu-id="a4d79-304">current track</span></span></li>
<li><span data-ttu-id="a4d79-305">etiqueta de formato</span><span class="sxs-lookup"><span data-stu-id="a4d79-305">format tag</span></span></li>
<li><span data-ttu-id="a4d79-306">input</span><span class="sxs-lookup"><span data-stu-id="a4d79-306">input</span></span></li>
<li><span data-ttu-id="a4d79-307">length</span><span class="sxs-lookup"><span data-stu-id="a4d79-307">length</span></span></li>
<li><span data-ttu-id="a4d79-308"><em>número</em> de pista de longitud</span><span class="sxs-lookup"><span data-stu-id="a4d79-308">length track <em>number</em></span></span></li>
<li><span data-ttu-id="a4d79-309">Nivel</span><span class="sxs-lookup"><span data-stu-id="a4d79-309">level</span></span></li>
<li><span data-ttu-id="a4d79-310">medio presente</span><span class="sxs-lookup"><span data-stu-id="a4d79-310">media present</span></span></li>
<li><span data-ttu-id="a4d79-311">mode</span><span class="sxs-lookup"><span data-stu-id="a4d79-311">mode</span></span></li>
<li><span data-ttu-id="a4d79-312">número de pistas</span><span class="sxs-lookup"><span data-stu-id="a4d79-312">number of tracks</span></span></li>
<li><span data-ttu-id="a4d79-313">output</span><span class="sxs-lookup"><span data-stu-id="a4d79-313">output</span></span></li>
<li><span data-ttu-id="a4d79-314">position</span><span class="sxs-lookup"><span data-stu-id="a4d79-314">position</span></span></li>
<li><span data-ttu-id="a4d79-315"><em>número</em> de pista de posición</span><span class="sxs-lookup"><span data-stu-id="a4d79-315">position track <em>number</em></span></span></li>
<li><span data-ttu-id="a4d79-316">ready</span><span class="sxs-lookup"><span data-stu-id="a4d79-316">ready</span></span></li>
<li><span data-ttu-id="a4d79-317">samplespersec</span><span class="sxs-lookup"><span data-stu-id="a4d79-317">samplespersec</span></span></li>
<li><span data-ttu-id="a4d79-318">posición inicial</span><span class="sxs-lookup"><span data-stu-id="a4d79-318">start position</span></span></li>
<li><span data-ttu-id="a4d79-319">formato de hora</span><span class="sxs-lookup"><span data-stu-id="a4d79-319">time format</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a4d79-320">En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszRequest** y su significado.</span><span class="sxs-lookup"><span data-stu-id="a4d79-320">The following table lists the flags that can be specified in the **lpszRequest** parameter and their meanings.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4d79-321">Value</span><span class="sxs-lookup"><span data-stu-id="a4d79-321">Value</span></span></th>
<th><span data-ttu-id="a4d79-322">Significado</span><span class="sxs-lookup"><span data-stu-id="a4d79-322">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4d79-323">alineación</span><span class="sxs-lookup"><span data-stu-id="a4d79-323">alignment</span></span></td>
<td><span data-ttu-id="a4d79-324">Devuelve la alineación del bloque de datos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="a4d79-324">Returns the block alignment of data, in bytes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-325">ensamblar registro</span><span class="sxs-lookup"><span data-stu-id="a4d79-325">assemble record</span></span></td>
<td><span data-ttu-id="a4d79-326">Devuelve <strong>true</strong> si el dispositivo está configurado para la grabación en modo de ensamblaje.</span><span class="sxs-lookup"><span data-stu-id="a4d79-326">Returns <strong>TRUE</strong> if the device is set to assemble mode recording.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-327">audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-327">audio</span></span></td>
<td><span data-ttu-id="a4d79-328">Devuelve &quot; on &quot; u &quot; OFF según &quot; el comando <a href="setaudio.md">SetAudio</a> &quot; on &quot; u OFF más reciente &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-328">Returns &quot;on&quot; or &quot;off&quot; depending on the most recent <a href="setaudio.md">setaudio</a> &quot;on&quot; or &quot;off&quot; command.</span></span> <span data-ttu-id="a4d79-329">Devuelve &quot; on &quot; si uno o ambos altavoces están habilitados y &quot; desactivado en &quot; caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a4d79-329">It returns &quot;on&quot; if either or both speakers are enabled, and &quot;off&quot; otherwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-330">alineación de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-330">audio alignment</span></span></td>
<td><span data-ttu-id="a4d79-331">Devuelve la alineación de los bloques de datos en relación con el inicio de los datos de audio de onda de entrada.</span><span class="sxs-lookup"><span data-stu-id="a4d79-331">Returns the alignment of data blocks relative to the start of input waveform-audio data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-332">audio BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="a4d79-332">audio bitspersample</span></span></td>
<td><span data-ttu-id="a4d79-333">Devuelve el número de bits por muestra que el dispositivo usa para la grabación.</span><span class="sxs-lookup"><span data-stu-id="a4d79-333">Returns the number of bits per sample the device uses for recording.</span></span> <span data-ttu-id="a4d79-334">Esta marca solo se aplica a los dispositivos que admiten el &quot; &quot; algoritmo PCM.</span><span class="sxs-lookup"><span data-stu-id="a4d79-334">This flag applies only to devices supporting the &quot;pcm&quot; algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-335">interrupciones de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-335">audio breaks</span></span></td>
<td><span data-ttu-id="a4d79-336">Devuelve el número de veces que se ha interrumpido la parte de audio de la última secuencia de AVI.</span><span class="sxs-lookup"><span data-stu-id="a4d79-336">Returns the number of times the audio portion of the last AVI sequence broke up.</span></span> <span data-ttu-id="a4d79-337">El sistema cuenta una interrupción de audio cada vez que intenta escribir datos de audio en el controlador de dispositivo y detecta que el controlador ya ha reproducido todos los datos disponibles.</span><span class="sxs-lookup"><span data-stu-id="a4d79-337">The system counts an audio break whenever it attempts to write audio data to the device driver and discovers that the driver has already played all of the available data.</span></span> <span data-ttu-id="a4d79-338">Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="a4d79-338">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="a4d79-339">Está pensada solo para la evaluación del rendimiento. el valor devuelto es difícil de interpretar.</span><span class="sxs-lookup"><span data-stu-id="a4d79-339">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-340">audio bytespersec</span><span class="sxs-lookup"><span data-stu-id="a4d79-340">audio bytespersec</span></span></td>
<td><span data-ttu-id="a4d79-341">Devuelve el número medio de bytes por segundo que se usan para la grabación.</span><span class="sxs-lookup"><span data-stu-id="a4d79-341">Returns the average number of bytes per second used for recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-342">entrada de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-342">audio input</span></span></td>
<td><span data-ttu-id="a4d79-343">Devuelve el nivel de audio instantáneo aproximado de la señal de audio de entrada analógica.</span><span class="sxs-lookup"><span data-stu-id="a4d79-343">Returns the approximate instantaneous audio level of the analog input audio signal.</span></span> <span data-ttu-id="a4d79-344">Un valor mayor que 1000 implica una distorsión de recorte.</span><span class="sxs-lookup"><span data-stu-id="a4d79-344">A value greater than 1000 implies clipping distortion.</span></span> <span data-ttu-id="a4d79-345">Algunos dispositivos pueden devolver este valor solo al grabar audio.</span><span class="sxs-lookup"><span data-stu-id="a4d79-345">Some devices can return this value only while recording audio.</span></span> <span data-ttu-id="a4d79-346">El valor no tiene asociado ningún comando <a href="set.md">set</a> o <a href="setaudio.md">SetAudio</a> .</span><span class="sxs-lookup"><span data-stu-id="a4d79-346">The value has no associated <a href="set.md">set</a> or <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-347">monitor de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-347">audio monitor</span></span></td>
<td><span data-ttu-id="a4d79-348">Devuelve &quot; &quot; la salida o uno de los tipos válidos de entrada de origen.</span><span class="sxs-lookup"><span data-stu-id="a4d79-348">Returns &quot;output&quot;, or one of the valid source-input types.</span></span> <span data-ttu-id="a4d79-349">Para obtener más información, consulte el comando monitor de <strong>SetAudio</strong> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-349">For more information, see the <strong>setaudio</strong> &quot;monitor&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-350">número de monitor de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-350">audio monitor number</span></span></td>
<td><span data-ttu-id="a4d79-351">Devuelve el número de vídeo supervisado del tipo especificado por el monitor de audio de <strong>Estado</strong> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-351">Returns the monitored-video number of the type specified by <strong>status</strong> &quot;audio monitor&quot;.</span></span> <span data-ttu-id="a4d79-352">Para obtener más información, consulte el comando <a href="setaudio.md">SetAudio</a> .</span><span class="sxs-lookup"><span data-stu-id="a4d79-352">For more information, see the <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-353">registro de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-353">audio record</span></span></td>
<td><span data-ttu-id="a4d79-354">Devuelve &quot; on &quot; u &quot; OFF &quot; , que refleja el estado establecido por el registro <strong>SetAudio</strong> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-354">Returns &quot;on&quot; or &quot;off&quot;, reflecting the state set by <strong>setaudio</strong> &quot;record&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-355"><em>número</em> de pista de grabación de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-355">audio record track <em>number</em></span></span></td>
<td><span data-ttu-id="a4d79-356">Devuelve <strong>true</strong> si el VCR está establecido para grabar audio.</span><span class="sxs-lookup"><span data-stu-id="a4d79-356">Returns <strong>TRUE</strong> if the VCR is set to record audio.</span></span> <span data-ttu-id="a4d79-357">Si no se proporciona ningún número de pista, se asume el valor predeterminado de 1.</span><span class="sxs-lookup"><span data-stu-id="a4d79-357">If no track number is given, the default value of 1 is assumed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-358">audio SamplesPerSec</span><span class="sxs-lookup"><span data-stu-id="a4d79-358">audio samplespersec</span></span></td>
<td><span data-ttu-id="a4d79-359">Devuelve el número de muestras por segundo grabadas.</span><span class="sxs-lookup"><span data-stu-id="a4d79-359">Returns the number of samples per second recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-360">origen de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-360">audio source</span></span></td>
<td><span data-ttu-id="a4d79-361">Devuelve el origen del digitalizador de audio actual: &quot; izquierda &quot; , &quot; derecha &quot; , &quot; promedio &quot; o &quot; estéreo &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-361">Returns the current audio digitizer source: &quot;left&quot;, &quot;right&quot;, &quot;average&quot;, or &quot;stereo&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-362">número de origen de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-362">audio source number</span></span></td>
<td><span data-ttu-id="a4d79-363">Devuelve el número de origen de audio del tipo devuelto por el <strong>Estado</strong> de &quot; origen de audio &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-363">Returns the audio-source number of the type returned by <strong>status</strong> &quot;audio source&quot;.</span></span> <span data-ttu-id="a4d79-364">Para obtener más información, consulte el comando <a href="setaudio.md">SetAudio</a> .</span><span class="sxs-lookup"><span data-stu-id="a4d79-364">For more information, see the <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-365">secuencia de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-365">audio stream</span></span></td>
<td><span data-ttu-id="a4d79-366">Devuelve el número de secuencia de audio actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-366">Returns the current audio-stream number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-367">improvisa</span><span class="sxs-lookup"><span data-stu-id="a4d79-367">bass</span></span></td>
<td><span data-ttu-id="a4d79-368">Devuelve el nivel de audio-graves actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-368">Returns the current audio-bass level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-369">BitsPerPel</span><span class="sxs-lookup"><span data-stu-id="a4d79-369">bitsperpel</span></span></td>
<td><span data-ttu-id="a4d79-370">Devuelve el número de bits por píxel para guardar los datos capturados o grabados.</span><span class="sxs-lookup"><span data-stu-id="a4d79-370">Returns the number of bits per pixel for saving captured or recorded data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-371">bitspersample</span><span class="sxs-lookup"><span data-stu-id="a4d79-371">bitspersample</span></span></td>
<td><span data-ttu-id="a4d79-372">Devuelve los bits por muestra.</span><span class="sxs-lookup"><span data-stu-id="a4d79-372">Returns the bits per sample.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-373">luminosidad</span><span class="sxs-lookup"><span data-stu-id="a4d79-373">brightness</span></span></td>
<td><span data-ttu-id="a4d79-374">Devuelve el nivel de brillo de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-374">Returns the current video-brightness level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-375">bytespersec</span><span class="sxs-lookup"><span data-stu-id="a4d79-375">bytespersec</span></span></td>
<td><span data-ttu-id="a4d79-376">Devuelve el número medio de bytes por segundo que se reproducen o registran.</span><span class="sxs-lookup"><span data-stu-id="a4d79-376">Returns the average number of bytes per second played or recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-377"><em>número</em> de pista de tipo cdaudio</span><span class="sxs-lookup"><span data-stu-id="a4d79-377">cdaudio type track <em>number</em></span></span></td>
<td><span data-ttu-id="a4d79-378">Devuelve el tipo del número de seguimiento especificado.</span><span class="sxs-lookup"><span data-stu-id="a4d79-378">Returns the type of the specified track number.</span></span> <span data-ttu-id="a4d79-379">Puede ser &quot; audio &quot; u &quot; otro.&quot;</span><span class="sxs-lookup"><span data-stu-id="a4d79-379">This can be &quot;audio&quot; or &quot;other.&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-380">canal</span><span class="sxs-lookup"><span data-stu-id="a4d79-380">channel</span></span></td>
<td><span data-ttu-id="a4d79-381">Devuelve el valor entero del conjunto de canales en el sintonizador.</span><span class="sxs-lookup"><span data-stu-id="a4d79-381">Returns the integer value of the channel set on the tuner.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-382"><em>número</em> de sintonizador de canal</span><span class="sxs-lookup"><span data-stu-id="a4d79-382">channel tuner <em>number</em></span></span></td>
<td><span data-ttu-id="a4d79-383">Si &quot; &quot; se proporciona el <em>número</em> de sintonizador, se devolverá el canal seleccionado actualmente en el <em>número</em> de sintonizador lógico.</span><span class="sxs-lookup"><span data-stu-id="a4d79-383">If &quot;tuner&quot; <em>number</em> is given, then the currently selected channel on the logical tuner <em>number</em> will be returned.</span></span> <span data-ttu-id="a4d79-384">Tenga en cuenta que puede haber varios sintonizadores lógicos.</span><span class="sxs-lookup"><span data-stu-id="a4d79-384">Note that there can be several logical tuners.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-385">canales nueva</span><span class="sxs-lookup"><span data-stu-id="a4d79-385">channels</span></span></td>
<td><span data-ttu-id="a4d79-386">Devuelve el número de canales establecido (1 para mono, 2 para estéreo).</span><span class="sxs-lookup"><span data-stu-id="a4d79-386">Returns the number of channels set (1 for mono, 2 for stereo).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-387">clock</span><span class="sxs-lookup"><span data-stu-id="a4d79-387">clock</span></span></td>
<td><span data-ttu-id="a4d79-388">Devuelve la hora externa.</span><span class="sxs-lookup"><span data-stu-id="a4d79-388">Returns the external time.</span></span> <span data-ttu-id="a4d79-389">El tiempo debe ser un entero largo sin signo que exprese los incrementos totales.</span><span class="sxs-lookup"><span data-stu-id="a4d79-389">The time must be an unsigned long integer expressing total increments.</span></span> <span data-ttu-id="a4d79-390">Para obtener más información, consulte el comando tasa de incremento del reloj de la <a href="capability.md">capacidad</a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-390">For more information, see the <a href="capability.md">capability</a> &quot;clock increment rate&quot; command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-391">ID. del reloj</span><span class="sxs-lookup"><span data-stu-id="a4d79-391">clock id</span></span></td>
<td><span data-ttu-id="a4d79-392">Devuelve un entero único que identifica el reloj.</span><span class="sxs-lookup"><span data-stu-id="a4d79-392">Returns a unique integer identifying the clock.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-393">color</span><span class="sxs-lookup"><span data-stu-id="a4d79-393">color</span></span></td>
<td><span data-ttu-id="a4d79-394">Devuelve el nivel de color actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-394">Returns the current color level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-395">contraste</span><span class="sxs-lookup"><span data-stu-id="a4d79-395">contrast</span></span></td>
<td><span data-ttu-id="a4d79-396">Devuelve el nivel de contraste actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-396">Returns the current contrast level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-397">counter</span><span class="sxs-lookup"><span data-stu-id="a4d79-397">counter</span></span></td>
<td><span data-ttu-id="a4d79-398">Devuelve la posición del contador, en el formato del contador actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-398">Returns the counter position, in the current counter format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-399">formato del contador</span><span class="sxs-lookup"><span data-stu-id="a4d79-399">counter format</span></span></td>
<td><span data-ttu-id="a4d79-400">Devuelve el formato del contador actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-400">Returns the current counter format.</span></span> <span data-ttu-id="a4d79-401">Para obtener más información, consulte el comando <a href="set.md">set</a> &quot; Counter format &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-401">For more information, see the <a href="set.md">set</a> &quot;counter format&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-402">resolución de contadores</span><span class="sxs-lookup"><span data-stu-id="a4d79-402">counter resolution</span></span></td>
<td><span data-ttu-id="a4d79-403">Devuelve &quot; Marcos &quot; o &quot; segundos &quot; , que indican la resolución del contador.</span><span class="sxs-lookup"><span data-stu-id="a4d79-403">Returns &quot;frames&quot; or &quot;seconds&quot;, indicating the counter's resolution.</span></span> <span data-ttu-id="a4d79-404">Esto no es lo mismo que la precisión.</span><span class="sxs-lookup"><span data-stu-id="a4d79-404">This is not the same as accuracy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-405">pista actual</span><span class="sxs-lookup"><span data-stu-id="a4d79-405">current track</span></span></td>
<td><span data-ttu-id="a4d79-406">Devuelve la pista actual. El secuenciador MCISEQ devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="a4d79-406">Returns the current track. The MCISEQ sequencer returns 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-407">tamaño del disco</span><span class="sxs-lookup"><span data-stu-id="a4d79-407">disc size</span></span></td>
<td><span data-ttu-id="a4d79-408">Devuelve 8 o 12, que indica el tamaño del disco cargado en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="a4d79-408">Returns either 8 or 12, indicating the size of the loaded disc in inches.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-409"><em>unidad</em> de espacio en disco</span><span class="sxs-lookup"><span data-stu-id="a4d79-409">disk space <em>drive</em></span></span></td>
<td><span data-ttu-id="a4d79-410">Devuelve el espacio en disco aproximado, en el formato de hora actual, que se puede obtener mediante un comando de <a href="reserve.md">reserva</a> para la unidad de disco especificada <em>.</em></span><span class="sxs-lookup"><span data-stu-id="a4d79-410">Returns the approximate disk space, in the current time format, that can be obtained by a <a href="reserve.md">reserve</a> command for the specified disk <em>drive.</em></span></span> <span data-ttu-id="a4d79-411">Normalmente, la <em>unidad</em> se especifica como una sola letra o una sola letra seguida de dos puntos (:).</span><span class="sxs-lookup"><span data-stu-id="a4d79-411">The <em>drive</em> is usually specified as a single letter or a single letter followed by a colon (:).</span></span> <span data-ttu-id="a4d79-412">Sin embargo, algunos dispositivos pueden usar una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a4d79-412">Some devices, however, might use a path.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-413">tipo de división</span><span class="sxs-lookup"><span data-stu-id="a4d79-413">division type</span></span></td>
<td><span data-ttu-id="a4d79-414">Devuelve uno de los siguientes tipos de división de archivos:</span><span class="sxs-lookup"><span data-stu-id="a4d79-414">Returns one of the following file division types:</span></span>
<ul>
<li><span data-ttu-id="a4d79-415">PPQN</span><span class="sxs-lookup"><span data-stu-id="a4d79-415">PPQN</span></span></li>
<li><span data-ttu-id="a4d79-416">Fotograma SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="a4d79-416">SMPTE 24 frame</span></span></li>
<li><span data-ttu-id="a4d79-417">Fotograma SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="a4d79-417">SMPTE 25 frame</span></span></li>
<li><span data-ttu-id="a4d79-418">Fotograma eliminado SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="a4d79-418">SMPTE 30 drop frame</span></span></li>
<li><span data-ttu-id="a4d79-419">Fotograma SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="a4d79-419">SMPTE 30 frame</span></span></li>
</ul>
<br/> <span data-ttu-id="a4d79-420">Utilice esta información para determinar el formato del archivo MIDI y el significado de la información sobre el tempo y la posición.</span><span class="sxs-lookup"><span data-stu-id="a4d79-420">Use this information to determine the format of the MIDI file and the meaning of tempo and position information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-421">finalización de archivos</span><span class="sxs-lookup"><span data-stu-id="a4d79-421">file completion</span></span></td>
<td><span data-ttu-id="a4d79-422">Devuelve el porcentaje estimado de progreso de una operación de <a href="load.md">carga</a>, <a href="save.md">guardado</a>, <a href="capture.md">captura</a>, <a href="cut.md">cortar</a>, <a href="copy.md">copiar</a>, <a href="delete.md">eliminar</a>, <a href="paste.md">pegar</a>o <a href="undo.md">Deshacer</a> .</span><span class="sxs-lookup"><span data-stu-id="a4d79-422">Returns the estimated percentage a <a href="load.md">load</a>, <a href="save.md">save</a>, <a href="capture.md">capture</a>, <a href="cut.md">cut</a>, <a href="copy.md">copy</a>, <a href="delete.md">delete</a>, <a href="paste.md">paste</a>, or <a href="undo.md">undo</a> operation has progressed.</span></span> <span data-ttu-id="a4d79-423">(Las aplicaciones pueden utilizar esto para proporcionar un indicador visual de progreso).</span><span class="sxs-lookup"><span data-stu-id="a4d79-423">(Applications can use this to provide a visual indicator of progress.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-424">formato del archivo</span><span class="sxs-lookup"><span data-stu-id="a4d79-424">file format</span></span></td>
<td><span data-ttu-id="a4d79-425">Devuelve el formato de archivo actual para los comandos de <a href="record.md">registro</a> o <strong>Guardar</strong> .</span><span class="sxs-lookup"><span data-stu-id="a4d79-425">Returns the current file format for <a href="record.md">record</a> or <strong>save</strong> commands.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-426">modo de archivo</span><span class="sxs-lookup"><span data-stu-id="a4d79-426">file mode</span></span></td>
<td><span data-ttu-id="a4d79-427">Devuelve la &quot; carga &quot; , el &quot; guardado, la &quot; &quot; edición o la &quot; &quot; inactividad &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-427">Returns &quot;loading&quot;, &quot;saving&quot;, &quot;editing&quot;, or &quot;idle&quot;.</span></span> <span data-ttu-id="a4d79-428">Durante una operación de <a href="load.md"><strong>carga</strong></a> , devuelve la &quot; carga &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-428">During a <a href="load.md"><strong>load</strong></a> operation, it returns &quot;loading&quot;.</span></span> <span data-ttu-id="a4d79-429">Durante las operaciones de <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>guardado</strong></a> y <a href="capture.md"><strong>captura</strong></a> , devuelve el &quot; guardado &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-429">During <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>save</strong></a> and <a href="capture.md"><strong>capture</strong></a> operations, it returns &quot;saving&quot;.</span></span> <span data-ttu-id="a4d79-430">Durante las operaciones de <a href="cut.md"><strong>cortar</strong></a>, <a href="copy.md"><strong>copiar</strong></a>, <a href="delete.md"><strong>eliminar</strong></a>, <a href="paste.md"><strong>pegar</strong></a>o <a href="undo.md"><strong>Deshacer</strong></a> , devuelve la &quot; Edición &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-430">During <a href="cut.md"><strong>cut</strong></a>, <a href="copy.md"><strong>copy</strong></a>, <a href="delete.md"><strong>delete</strong></a>, <a href="paste.md"><strong>paste</strong></a>, or <a href="undo.md"><strong>undo</strong></a> operations, it returns &quot;editing&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-431">etiqueta de formato</span><span class="sxs-lookup"><span data-stu-id="a4d79-431">format tag</span></span></td>
<td><span data-ttu-id="a4d79-432">Devuelve la etiqueta de formato.</span><span class="sxs-lookup"><span data-stu-id="a4d79-432">Returns the format tag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-433">forward</span><span class="sxs-lookup"><span data-stu-id="a4d79-433">forward</span></span></td>
<td><span data-ttu-id="a4d79-434">Devuelve <strong>true</strong> si la dirección de reproducción es hacia delante o si el dispositivo no se está reproduciendo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-434">Returns <strong>TRUE</strong> if the play direction is forward or if the device is not playing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-435">velocidad de fotogramas</span><span class="sxs-lookup"><span data-stu-id="a4d79-435">frame rate</span></span></td>
<td><span data-ttu-id="a4d79-436">Devuelve el número de fotogramas por segundo que el dispositivo usará de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a4d79-436">Returns the number of frames per second that the device will use by default.</span></span> <span data-ttu-id="a4d79-437">Los dispositivos NTSC devuelven 30, PAL 25, etc.</span><span class="sxs-lookup"><span data-stu-id="a4d79-437">NTSC devices return 30, PAL 25, and so on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-438">fotogramas omitidos</span><span class="sxs-lookup"><span data-stu-id="a4d79-438">frames skipped</span></span></td>
<td><span data-ttu-id="a4d79-439">Devuelve el número de fotogramas que no se dibujaron cuando se reprodujo la última secuencia AVI.</span><span class="sxs-lookup"><span data-stu-id="a4d79-439">Returns the number of frames that were not drawn when the last AVI sequence was played.</span></span> <span data-ttu-id="a4d79-440">Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="a4d79-440">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="a4d79-441">Está pensada solo para la evaluación del rendimiento. el valor devuelto es difícil de interpretar.</span><span class="sxs-lookup"><span data-stu-id="a4d79-441">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-442">gamma</span><span class="sxs-lookup"><span data-stu-id="a4d79-442">gamma</span></span></td>
<td><span data-ttu-id="a4d79-443">Devuelve el valor establecido con <a href="setvideo.md"><strong></strong></a> el &quot; valor gamma de setvideo &quot; <em></em>.</span><span class="sxs-lookup"><span data-stu-id="a4d79-443">Returns the value set with <a href="setvideo.md"><strong>setvideo</strong></a> &quot;gamma to&quot; <em>value</em>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-444">índice</span><span class="sxs-lookup"><span data-stu-id="a4d79-444">index</span></span></td>
<td><span data-ttu-id="a4d79-445">Devuelve la presentación del índice actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-445">Returns the current index display.</span></span> <span data-ttu-id="a4d79-446">Para obtener más información, consulte el comando <a href="set.md"><strong>set</strong></a> &quot; index &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-446">For more information, see the <a href="set.md"><strong>set</strong></a> &quot;index&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-447">índice en</span><span class="sxs-lookup"><span data-stu-id="a4d79-447">index on</span></span></td>
<td><span data-ttu-id="a4d79-448">Devuelve <strong>true</strong> si el índice está activado.</span><span class="sxs-lookup"><span data-stu-id="a4d79-448">Returns <strong>TRUE</strong> if the index is on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-449">input</span><span class="sxs-lookup"><span data-stu-id="a4d79-449">input</span></span></td>
<td><span data-ttu-id="a4d79-450">Devuelve el conjunto de entrada.</span><span class="sxs-lookup"><span data-stu-id="a4d79-450">Returns the input set.</span></span> <span data-ttu-id="a4d79-451">Si no se establece uno, el error devuelto indica que se puede usar cualquier dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-451">If one is not set, the error returned indicates that any device can be used.</span></span> <span data-ttu-id="a4d79-452">En el caso de los dispositivos de vídeo digital, modifica la &quot; marca de graves &quot; , &quot; agudos &quot; , &quot; volumen &quot; , &quot; brillo &quot; , &quot; color &quot; , &quot; contraste &quot; , &quot; gamma &quot; , &quot; nitidez &quot; o &quot; matiz &quot; para que se aplique solo a la entrada.</span><span class="sxs-lookup"><span data-stu-id="a4d79-452">For digital-video devices, modifies the &quot;bass&quot;, &quot;treble&quot;, &quot;volume&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, or &quot;tint&quot; flag so that it applies only to the input.</span></span> <span data-ttu-id="a4d79-453">Este es el valor predeterminado al supervisar la entrada.</span><span class="sxs-lookup"><span data-stu-id="a4d79-453">This is the default when monitoring the input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-454">volumen izquierdo</span><span class="sxs-lookup"><span data-stu-id="a4d79-454">left volume</span></span></td>
<td><span data-ttu-id="a4d79-455">Devuelve el conjunto de volúmenes para el canal de audio izquierdo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-455">Returns the volume set for the left audio channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-456">length</span><span class="sxs-lookup"><span data-stu-id="a4d79-456">length</span></span></td>
<td><span data-ttu-id="a4d79-457">Devuelve la longitud total del medio, en el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-457">Returns the total length of the media, in the current time format.</span></span> <span data-ttu-id="a4d79-458">En el caso de los archivos PPQN, la longitud se devuelve en unidades de puntero de la canción.</span><span class="sxs-lookup"><span data-stu-id="a4d79-458">For PPQN files, the length is returned in song pointer units.</span></span> <span data-ttu-id="a4d79-459">En el caso de los archivos SMPTE, se devuelve como <em>HH: mm: SS: FF</em>, donde <em>HH</em> es hours, <em>mm</em> es minutes, <em>SS</em> is seconds y <em>FF</em> es frames.</span><span class="sxs-lookup"><span data-stu-id="a4d79-459">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span> <span data-ttu-id="a4d79-460">En el caso de los dispositivos VCR, la longitud es de 2 horas (a menos que la longitud se haya cambiado explícitamente mediante el comando <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> ).</span><span class="sxs-lookup"><span data-stu-id="a4d79-460">For VCR devices, the length is 2 hours (unless the length has been explicitly changed using the <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> command).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-461"><em>número</em> de pista de longitud</span><span class="sxs-lookup"><span data-stu-id="a4d79-461">length track <em>number</em></span></span></td>
<td><span data-ttu-id="a4d79-462">Devuelve la longitud de la pista, en horas o fotogramas, especificada por <em>número</em>. En el caso de los archivos PPQN, la longitud se devuelve en unidades de puntero de la canción.</span><span class="sxs-lookup"><span data-stu-id="a4d79-462">Returns the length of the track, in time or frames, specified by <em>number</em>.For PPQN files, the length is returned in song pointer units.</span></span> <span data-ttu-id="a4d79-463">En el caso de los archivos SMPTE, se devuelve como <em>HH: mm: SS: FF</em>, donde <em>HH</em> es hours, <em>mm</em> es minutes, <em>SS</em> is seconds y <em>FF</em> es frames.</span><span class="sxs-lookup"><span data-stu-id="a4d79-463">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-464">Nivel</span><span class="sxs-lookup"><span data-stu-id="a4d79-464">level</span></span></td>
<td><span data-ttu-id="a4d79-465">Devuelve el valor del ejemplo de audio PCM actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-465">Returns the current PCM audio sample value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-466">maestro</span><span class="sxs-lookup"><span data-stu-id="a4d79-466">master</span></span></td>
<td><span data-ttu-id="a4d79-467">Devuelve &quot; MIDI &quot; , &quot; ninguno &quot; o &quot; SMPTE &quot; según el tipo de conjunto de sincronización.</span><span class="sxs-lookup"><span data-stu-id="a4d79-467">Returns &quot;midi&quot;, &quot;none&quot;, or &quot;smpte&quot; depending on the type of synchronization set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-468">medio presente</span><span class="sxs-lookup"><span data-stu-id="a4d79-468">media present</span></span></td>
<td><span data-ttu-id="a4d79-469">Devuelve <strong>true</strong> si el elemento multimedia se inserta en el dispositivo o <strong>false</strong> en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a4d79-469">Returns <strong>TRUE</strong> if the media is inserted in the device or <strong>FALSE</strong> otherwise.</span></span> <span data-ttu-id="a4d79-470">Los dispositivos Sequencer, vídeo superpuesto, vídeo digital y de audio de onda devuelven <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d79-470">Sequencer, video-overlay, digital-video, and waveform-audio devices return <strong>TRUE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-471">tipo de medio</span><span class="sxs-lookup"><span data-stu-id="a4d79-471">media type</span></span></td>
<td><span data-ttu-id="a4d79-472">Devuelve el tipo de los elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="a4d79-472">Returns the type of the media.</span></span> <span data-ttu-id="a4d79-473">En el caso de los VCR, es &quot; 8mm &quot; , &quot; VHS &quot; , &quot; SVHS &quot; , &quot; beta &quot; , &quot; Hi8 &quot; , &quot; edbeta &quot; u &quot; otros &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-473">For VCRS, this is &quot;8mm&quot;, &quot;vhs&quot;, &quot;svhs&quot;, &quot;beta&quot;, &quot;Hi8&quot;, &quot;edbeta&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="a4d79-474">En el caso de los videodiscos, es &quot; CAV &quot; , &quot; CLV &quot; u &quot; otro &quot; , en función del tipo de VideoDisc.</span><span class="sxs-lookup"><span data-stu-id="a4d79-474">For videodiscs, this is &quot;CAV&quot;, &quot;CLV&quot;, or &quot;other&quot;, depending on the type of videodisc.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-475">mode</span><span class="sxs-lookup"><span data-stu-id="a4d79-475">mode</span></span></td>
<td><span data-ttu-id="a4d79-476">Devuelve el modo actual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-476">Returns the current mode of the device.</span></span> <span data-ttu-id="a4d79-477">Todos los dispositivos pueden devolver los &quot; valores no Ready &quot; , &quot; pausado &quot; , &quot; Playing &quot; y &quot; Stopped &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-477">All devices can return the &quot;not ready&quot;, &quot;paused&quot;, &quot;playing&quot;, and &quot;stopped&quot; values.</span></span> <span data-ttu-id="a4d79-478">Algunos dispositivos pueden devolver los &quot; valores de apertura, de estacionamiento, de &quot; &quot; &quot; &quot; grabación y de búsqueda adicionales &quot; &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-478">Some devices can return the additional &quot;open&quot;, &quot;parked&quot;, &quot;recording&quot;, and &quot;seeking&quot; values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-479">monitor</span><span class="sxs-lookup"><span data-stu-id="a4d79-479">monitor</span></span></td>
<td><span data-ttu-id="a4d79-480">Devuelve el &quot; archivo &quot; o la &quot; entrada &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-480">Returns &quot;file&quot; or &quot;input&quot;.</span></span> <span data-ttu-id="a4d79-481">El valor devuelto indica el origen de presentación actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-481">The returned value indicates the current presentation source.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-482">monitor (método)</span><span class="sxs-lookup"><span data-stu-id="a4d79-482">monitor method</span></span></td>
<td><span data-ttu-id="a4d79-483">Devuelve &quot; pre &quot; , &quot; post &quot; o &quot; Direct &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-483">Returns &quot;pre&quot;, &quot;post&quot;, or &quot;direct&quot;.</span></span> <span data-ttu-id="a4d79-484">El valor devuelto indica el método utilizado para la supervisión de entrada.</span><span class="sxs-lookup"><span data-stu-id="a4d79-484">The returned value indicates the method used for input monitoring.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-485">tasa</span><span class="sxs-lookup"><span data-stu-id="a4d79-485">nominal</span></span></td>
<td><span data-ttu-id="a4d79-486">El elemento modifica las &quot; marcas de graves &quot; , &quot; brillo &quot; , &quot; color &quot; , &quot; contraste &quot; , &quot; gamma &quot; , &quot; nitidez &quot; , &quot; matiz &quot; , &quot; agudos &quot; y &quot; volumen &quot; para devolver el valor nominal en lugar de la configuración actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-486">The item modifies the &quot;bass&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, &quot;tint&quot;, &quot;treble,&quot; and &quot;volume&quot; flags to return the nominal value instead of the current setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-487">velocidad de fotogramas nominal</span><span class="sxs-lookup"><span data-stu-id="a4d79-487">nominal frame rate</span></span></td>
<td><span data-ttu-id="a4d79-488">Devuelve la velocidad de fotogramas nominal asociada al archivo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-488">Returns the nominal frame rate associated with the file.</span></span> <span data-ttu-id="a4d79-489">Las unidades están en fotogramas por segundo multiplicado por 1000.</span><span class="sxs-lookup"><span data-stu-id="a4d79-489">The units are in frames per second multiplied by 1000.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-490">velocidad de fotogramas de registro nominal</span><span class="sxs-lookup"><span data-stu-id="a4d79-490">nominal record frame rate</span></span></td>
<td><span data-ttu-id="a4d79-491">Devuelve la velocidad de fotogramas nominal asociada a la señal de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a4d79-491">Returns the nominal frame rate associated with the input video signal.</span></span> <span data-ttu-id="a4d79-492">Las unidades están en fotogramas por segundo multiplicado por 1000.</span><span class="sxs-lookup"><span data-stu-id="a4d79-492">The units are in frames per second multiplied by 1000.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-493">número de pistas de audio</span><span class="sxs-lookup"><span data-stu-id="a4d79-493">number of audio tracks</span></span></td>
<td><span data-ttu-id="a4d79-494">Devuelve el número de pistas de audio en el medio.</span><span class="sxs-lookup"><span data-stu-id="a4d79-494">Returns the number of audio tracks on the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-495">número de pistas</span><span class="sxs-lookup"><span data-stu-id="a4d79-495">number of tracks</span></span></td>
<td><span data-ttu-id="a4d79-496">Devuelve el número de pistas en el medio.</span><span class="sxs-lookup"><span data-stu-id="a4d79-496">Returns the number of tracks on the media.</span></span> <span data-ttu-id="a4d79-497">Los dispositivos MCISEQ y MCIWAVE devuelven 1, al igual que la mayoría de los dispositivos VCR.</span><span class="sxs-lookup"><span data-stu-id="a4d79-497">The MCISEQ and MCIWAVE devices return 1, as do most VCR devices.</span></span> <span data-ttu-id="a4d79-498">El dispositivo MCIPIONR no admite esta marca.</span><span class="sxs-lookup"><span data-stu-id="a4d79-498">The MCIPIONR device does not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-499">número de pistas de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-499">number of video tracks</span></span></td>
<td><span data-ttu-id="a4d79-500">Devuelve el número de pistas de vídeo en el medio.</span><span class="sxs-lookup"><span data-stu-id="a4d79-500">Returns the number of video tracks on the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-501">offset</span><span class="sxs-lookup"><span data-stu-id="a4d79-501">offset</span></span></td>
<td><span data-ttu-id="a4d79-502">Devuelve el desplazamiento de un archivo basado en SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a4d79-502">Returns the offset of a SMPTE-based file.</span></span> <span data-ttu-id="a4d79-503">El desplazamiento es la hora de inicio de una secuencia basada en SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a4d79-503">The offset is the start time of a SMPTE-based sequence.</span></span> <span data-ttu-id="a4d79-504">La hora se devuelve como <em>HH: mm: SS: FF</em>, donde <em>HH</em> es hours, <em>mm</em> is minutes, <em>SS</em> is seconds y <em>FF</em> is frames.</span><span class="sxs-lookup"><span data-stu-id="a4d79-504">The time is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-505">output</span><span class="sxs-lookup"><span data-stu-id="a4d79-505">output</span></span></td>
<td><span data-ttu-id="a4d79-506">Devuelve la salida establecida actualmente.</span><span class="sxs-lookup"><span data-stu-id="a4d79-506">Returns the currently set output.</span></span> <span data-ttu-id="a4d79-507">Si no se establece ningún resultado, el error devuelto indica que se puede usar cualquier dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-507">If no output is set, the error returned indicates that any device can be used.</span></span> <span data-ttu-id="a4d79-508">En el caso de los dispositivos de vídeo digital, modifica la &quot; marca de graves &quot; , &quot; agudos &quot; , &quot; volumen &quot; , &quot; brillo &quot; , &quot; color &quot; , &quot; contraste &quot; , &quot; gamma &quot; , &quot; nitidez &quot; o &quot; matiz &quot; para que se aplique solo a la salida.</span><span class="sxs-lookup"><span data-stu-id="a4d79-508">For digital-video devices, modifies the &quot;bass&quot;, &quot;treble&quot;, &quot;volume&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, or &quot;tint&quot; flag so that it applies only to the output.</span></span> <span data-ttu-id="a4d79-509">Este es el valor predeterminado al supervisar un archivo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-509">This is the default when monitoring a file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-510">modo de pausa</span><span class="sxs-lookup"><span data-stu-id="a4d79-510">pause mode</span></span></td>
<td><span data-ttu-id="a4d79-511">Devuelve &quot; &quot; la grabación si el dispositivo está en pausa mientras se graba.</span><span class="sxs-lookup"><span data-stu-id="a4d79-511">Returns &quot;recording&quot; if the device is paused while recording.</span></span> <span data-ttu-id="a4d79-512">Devuelve &quot; la reproducción &quot; si el dispositivo está en pausa mientras se reproduce.</span><span class="sxs-lookup"><span data-stu-id="a4d79-512">It returns &quot;playing&quot; if the device is paused while playing.</span></span> <span data-ttu-id="a4d79-513">Devuelve la &quot; acción de error no aplicable en el modo actual &quot; si el dispositivo no está en pausa.</span><span class="sxs-lookup"><span data-stu-id="a4d79-513">It returns the error &quot;Action not applicable in current mode&quot; if the device is not paused.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-514">tiempo de espera de pausa</span><span class="sxs-lookup"><span data-stu-id="a4d79-514">pause timeout</span></span></td>
<td><span data-ttu-id="a4d79-515">Devuelve la duración máxima, en milisegundos, de un comando <a href="pause.md"><strong>PAUSE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a4d79-515">Returns the maximum duration, in milliseconds, of a <a href="pause.md"><strong>pause</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-516">formato de reproducción</span><span class="sxs-lookup"><span data-stu-id="a4d79-516">play format</span></span></td>
<td><span data-ttu-id="a4d79-517">Devuelve un código que indica el formato en el que se reproducirá la cinta de vídeo, si se detecta: &quot; LP &quot; , &quot; EP &quot; , &quot; Sp &quot; u &quot; otros &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-517">Returns a code indicating the format that the videotape will be played back in, if detectable: &quot;lp&quot;, &quot;ep&quot;, &quot;sp&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="a4d79-518">Para obtener más información, vea la &quot; marca de formato de registro &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-518">For more information, see the &quot;record format&quot; flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-519">velocidad de reproducción</span><span class="sxs-lookup"><span data-stu-id="a4d79-519">play speed</span></span></td>
<td><span data-ttu-id="a4d79-520">Devuelve un valor que representa la proximidad del tiempo de reproducción real de la última secuencia de AVI con el tiempo de reproducción del destino.</span><span class="sxs-lookup"><span data-stu-id="a4d79-520">Returns a value representing how closely the actual playing time of the last AVI sequence matched the target playing time.</span></span> <span data-ttu-id="a4d79-521">El valor 1000 indica que la hora de destino y la hora real eran iguales.</span><span class="sxs-lookup"><span data-stu-id="a4d79-521">The value 1000 indicates that the target time and the actual time were the same.</span></span> <span data-ttu-id="a4d79-522">Un valor de 2000, por ejemplo, indicaría que la secuencia AVI tardó dos veces más en ejecutarse que debiera.</span><span class="sxs-lookup"><span data-stu-id="a4d79-522">A value of 2000, for example, would indicate that the AVI sequence took twice as long to play as it should have.</span></span> <span data-ttu-id="a4d79-523">Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="a4d79-523">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="a4d79-524">Está pensada solo para la evaluación del rendimiento. el valor devuelto es difícil de interpretar.</span><span class="sxs-lookup"><span data-stu-id="a4d79-524">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-525">port</span><span class="sxs-lookup"><span data-stu-id="a4d79-525">port</span></span></td>
<td><span data-ttu-id="a4d79-526">Devuelve el número de puerto MIDI asignado a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="a4d79-526">Returns the MIDI port number assigned to the sequence.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-527">position</span><span class="sxs-lookup"><span data-stu-id="a4d79-527">position</span></span></td>
<td><span data-ttu-id="a4d79-528">Devuelve la posición actual. En el caso de los archivos PPQN, la posición se devuelve en unidades del puntero de la canción.</span><span class="sxs-lookup"><span data-stu-id="a4d79-528">Returns the current position.For PPQN files, the position is returned in song pointer units.</span></span> <span data-ttu-id="a4d79-529">En el caso de los archivos SMPTE, se devuelve como <em>HH: mm: SS: FF</em>, donde <em>HH</em> es hours, <em>mm</em> es minutes, SS is seconds y <em>FF</em> es frames.</span><span class="sxs-lookup"><span data-stu-id="a4d79-529">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, ss is seconds, and <em>ff</em> is frames.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-530">posición inicial</span><span class="sxs-lookup"><span data-stu-id="a4d79-530">position start</span></span></td>
<td><span data-ttu-id="a4d79-531">Devuelve la posición del inicio del medio utilizable.</span><span class="sxs-lookup"><span data-stu-id="a4d79-531">Returns the position of the start of the usable media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-532"><em>número</em> de pista de posición</span><span class="sxs-lookup"><span data-stu-id="a4d79-532">position track <em>number</em></span></span></td>
<td><span data-ttu-id="a4d79-533">Devuelve la posición del inicio de la pista especificada por el <em>número</em>.</span><span class="sxs-lookup"><span data-stu-id="a4d79-533">Returns the position of the start of the track specified by <em>number</em>.</span></span> <span data-ttu-id="a4d79-534">En el caso de los archivos PPQN, el formato de hora se devuelve en unidades de puntero de la canción.</span><span class="sxs-lookup"><span data-stu-id="a4d79-534">For PPQN files, the time format is returned in song pointer units.</span></span> <span data-ttu-id="a4d79-535">En el caso de los archivos SMPTE, se devuelve como <em>HH: mm: SS: FF</em>, donde <em>HH</em> es hours, <em>mm</em> es minutes, <em>SS</em> is seconds y <em>FF</em> es frames.</span><span class="sxs-lookup"><span data-stu-id="a4d79-535">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span> <span data-ttu-id="a4d79-536">El secuenciador MCISEQ devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="a4d79-536">The MCISEQ sequencer returns zero.</span></span> <span data-ttu-id="a4d79-537">El dispositivo MCIPIONR no admite esta marca.</span><span class="sxs-lookup"><span data-stu-id="a4d79-537">The MCIPIONR device does not support this flag.</span></span> <span data-ttu-id="a4d79-538">El dispositivo MCIWAVE devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="a4d79-538">The MCIWAVE device returns zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-539">duración del PostRoll</span><span class="sxs-lookup"><span data-stu-id="a4d79-539">postroll duration</span></span></td>
<td><span data-ttu-id="a4d79-540">Devuelve la longitud de la cinta de vídeo, en el formato de hora actual, necesaria para frenar el transporte de VCR cuando se emite un comando de <a href="stop.md"><strong>detención</strong></a> o <a href="pause.md"><strong>pausa</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a4d79-540">Returns the length of videotape, in the current time format, needed to brake the VCR transport when a <a href="stop.md"><strong>stop</strong></a> or <a href="pause.md"><strong>pause</strong></a> command is issued.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-541">encendido</span><span class="sxs-lookup"><span data-stu-id="a4d79-541">power on</span></span></td>
<td><span data-ttu-id="a4d79-542">Devuelve <strong>true</strong> si la alimentación del VCR está activada.</span><span class="sxs-lookup"><span data-stu-id="a4d79-542">Returns <strong>TRUE</strong> if the VCR's power is on.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-543">duración del prelanzamiento</span><span class="sxs-lookup"><span data-stu-id="a4d79-543">preroll duration</span></span></td>
<td><span data-ttu-id="a4d79-544">Devuelve la longitud de la cinta de vídeo, en el formato de hora actual, necesaria para estabilizar la salida del VCR.</span><span class="sxs-lookup"><span data-stu-id="a4d79-544">Returns the length of videotape, in the current time format, needed to stabilize the VCR output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-545">ready</span><span class="sxs-lookup"><span data-stu-id="a4d79-545">ready</span></span></td>
<td><span data-ttu-id="a4d79-546">Devuelve <strong>true</strong> si el dispositivo está listo para aceptar otro comando.</span><span class="sxs-lookup"><span data-stu-id="a4d79-546">Returns <strong>TRUE</strong> if the device is ready to accept another command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-547">formato de registro</span><span class="sxs-lookup"><span data-stu-id="a4d79-547">record format</span></span></td>
<td><span data-ttu-id="a4d79-548">Devuelve un código que indica el formato en el que se grabará la cinta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-548">Returns a code indicating the format that the videotape will be recorded in.</span></span> <span data-ttu-id="a4d79-549">Los tipos de valor devueltos actuales son &quot; LP &quot; , &quot; EP &quot; , &quot; Sp &quot; u &quot; otros &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-549">The current return types are &quot;lp&quot;, &quot;ep&quot;, &quot;sp&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="a4d79-550">Estos formatos no son específicos de VHS y se pueden aplicar a cualquier VCR que tenga varios formatos de grabación seleccionables.</span><span class="sxs-lookup"><span data-stu-id="a4d79-550">These formats are not VHS specific and can be applied to any VCR that has multiple selectable recording formats.</span></span> <span data-ttu-id="a4d79-551">El &quot; &quot; tipo SP es el formato de grabación más rápido y de mayor calidad, y se usa como valor predeterminado en VCR de formato único.</span><span class="sxs-lookup"><span data-stu-id="a4d79-551">The &quot;sp&quot; type is the fastest, highest quality recording format and is used as default on single format VCRs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-552">velocidad de fotogramas de registro</span><span class="sxs-lookup"><span data-stu-id="a4d79-552">record frame rate</span></span></td>
<td><span data-ttu-id="a4d79-553">Devuelve la velocidad de fotogramas, en fotogramas por segundo multiplicada por 1000, que se usa para la compresión.</span><span class="sxs-lookup"><span data-stu-id="a4d79-553">Returns the frame rate, in frames per second multiplied by 1000, used for compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-554"><em>marco</em> de referencia</span><span class="sxs-lookup"><span data-stu-id="a4d79-554">reference <em>frame</em></span></span></td>
<td><span data-ttu-id="a4d79-555">Devuelve el número de marco de la imagen de fotograma clave más cercana que precede al <em>marco</em>especificado.</span><span class="sxs-lookup"><span data-stu-id="a4d79-555">Returns the frame number for the nearest key frame image that precedes the specified <em>frame</em>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-556">tamaño reservado</span><span class="sxs-lookup"><span data-stu-id="a4d79-556">reserved size</span></span></td>
<td><span data-ttu-id="a4d79-557">Devuelve el tamaño, en el formato de hora actual, del área de trabajo reservada.</span><span class="sxs-lookup"><span data-stu-id="a4d79-557">Returns the size, in the current time format, of the reserved workspace.</span></span> <span data-ttu-id="a4d79-558">El tamaño corresponde al tiempo aproximado que se tardaría en reproducir los datos comprimidos desde un área de trabajo completa.</span><span class="sxs-lookup"><span data-stu-id="a4d79-558">The size corresponds to the approximate time it would take to play the compressed data from a full workspace.</span></span> <span data-ttu-id="a4d79-559">Devuelve cero si no hay espacio en disco reservado.</span><span class="sxs-lookup"><span data-stu-id="a4d79-559">It returns zero if there is no reserved disk space.</span></span> <span data-ttu-id="a4d79-560">Esta marca devuelve el tamaño aproximado porque el espacio en disco preciso para los datos comprimidos no se puede predecir en general hasta que se hayan comprimido los datos.</span><span class="sxs-lookup"><span data-stu-id="a4d79-560">This flag returns the approximate size because the precise disk space for compressed data cannot, in general, be predicted until after the data has been compressed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-561">volumen derecho</span><span class="sxs-lookup"><span data-stu-id="a4d79-561">right volume</span></span></td>
<td><span data-ttu-id="a4d79-562">Devuelve el conjunto de volúmenes para el canal de audio derecho.</span><span class="sxs-lookup"><span data-stu-id="a4d79-562">Returns the volume set for the right audio channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-563">samplespersec</span><span class="sxs-lookup"><span data-stu-id="a4d79-563">samplespersec</span></span></td>
<td><span data-ttu-id="a4d79-564">Devuelve el número de muestras por segundo reproducidas o grabadas.</span><span class="sxs-lookup"><span data-stu-id="a4d79-564">Returns the number of samples per second played or recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-565">Buscar exactamente</span><span class="sxs-lookup"><span data-stu-id="a4d79-565">seek exactly</span></span></td>
<td><span data-ttu-id="a4d79-566">Devuelve &quot; on &quot; u &quot; OFF &quot; , que indica si &quot; se establece la marca Seek Exactly &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-566">Returns &quot;on&quot; or &quot;off&quot;, indicating whether or not the &quot;seek exactly&quot; flag is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-567">nitidez</span><span class="sxs-lookup"><span data-stu-id="a4d79-567">sharpness</span></span></td>
<td><span data-ttu-id="a4d79-568">Devuelve el nivel de nitidez actual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-568">Returns the current sharpness level of the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-569">margen</span><span class="sxs-lookup"><span data-stu-id="a4d79-569">side</span></span></td>
<td><span data-ttu-id="a4d79-570">Devuelve 1 o 2 para indicar el lado del CD que se ha cargado.</span><span class="sxs-lookup"><span data-stu-id="a4d79-570">Returns 1 or 2 to indicate which side of the videodisc is loaded.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-571">satélite</span><span class="sxs-lookup"><span data-stu-id="a4d79-571">slave</span></span></td>
<td><span data-ttu-id="a4d79-572">Devuelve &quot; file &quot; , &quot; MIDI &quot; , &quot; None &quot; o &quot; SMPTE &quot; según el tipo de conjunto de sincronización.</span><span class="sxs-lookup"><span data-stu-id="a4d79-572">Returns &quot;file&quot; , &quot;midi&quot;, &quot;none&quot;, or &quot;smpte&quot; depending on the type of synchronization set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-573">SMPTE</span><span class="sxs-lookup"><span data-stu-id="a4d79-573">smpte</span></span></td>
<td><span data-ttu-id="a4d79-574">Devuelve el código de tiempo de SMPTE asociado a la posición actual en el área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-574">Returns the SMPTE timecode associated with the current position in the workspace.</span></span> <span data-ttu-id="a4d79-575">Se trata de una cadena con el formato <em>DD: DD</em>: DD: DD, donde cada <em>d</em> denota un dígito de 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="a4d79-575">This is a string with the form <em>dd:dd:dd:dd</em>, where each <em>d</em> denotes a digit from 0 to 9.</span></span> <span data-ttu-id="a4d79-576">Si los datos del área de trabajo no incluyen datos de código de tiempo, esta marca devuelve 00:00:00:00.</span><span class="sxs-lookup"><span data-stu-id="a4d79-576">If the workspace data does not include timecode data, then this flag returns 00:00:00:00.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-577">velocidad</span><span class="sxs-lookup"><span data-stu-id="a4d79-577">speed</span></span></td>
<td><span data-ttu-id="a4d79-578">Devuelve la velocidad actual del dispositivo en fotogramas por segundo (o en el mismo formato que usa el comando <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> &quot; Speed &quot; ).</span><span class="sxs-lookup"><span data-stu-id="a4d79-578">Returns the current speed of the device in frames per second (or in the same format used by the <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> &quot;speed&quot; command).</span></span> <span data-ttu-id="a4d79-579">El reproductor de videodisco de MCIPIONR no admite esta marca.</span><span class="sxs-lookup"><span data-stu-id="a4d79-579">The MCIPIONR videodisc player does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-580">posición inicial</span><span class="sxs-lookup"><span data-stu-id="a4d79-580">start position</span></span></td>
<td><span data-ttu-id="a4d79-581">Devuelve la posición inicial del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="a4d79-581">Returns the starting position of the media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-582">formato de archivo todavía</span><span class="sxs-lookup"><span data-stu-id="a4d79-582">still file format</span></span></td>
<td><span data-ttu-id="a4d79-583">Devuelve el formato de archivo actual para el comando de <a href="capture.md"><strong>captura</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a4d79-583">Returns the current file format for the <a href="capture.md"><strong>capture</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-584">ajustar</span><span class="sxs-lookup"><span data-stu-id="a4d79-584">stretch</span></span></td>
<td><span data-ttu-id="a4d79-585">Devuelve <strong>true</strong> si está habilitada la expansión.</span><span class="sxs-lookup"><span data-stu-id="a4d79-585">Returns <strong>TRUE</strong> if stretching is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-586">ritmo</span><span class="sxs-lookup"><span data-stu-id="a4d79-586">tempo</span></span></td>
<td><span data-ttu-id="a4d79-587">Devuelve el tempo actual de una secuencia MIDI en el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-587">Returns the current tempo of a MIDI sequence in the current time format.</span></span> <span data-ttu-id="a4d79-588">En el caso de los archivos con el formato PPQN, el tempo está en pulsaciones por minuto.</span><span class="sxs-lookup"><span data-stu-id="a4d79-588">For files with PPQN format, the tempo is in beats per minute.</span></span> <span data-ttu-id="a4d79-589">En el caso de los archivos con el formato SMPTE, el tempo está en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-589">For files with SMPTE format, the tempo is in frames per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-590">formato de hora</span><span class="sxs-lookup"><span data-stu-id="a4d79-590">time format</span></span></td>
<td><span data-ttu-id="a4d79-591">Devuelve el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-591">Returns the current time format.</span></span> <span data-ttu-id="a4d79-592">Para obtener más información, consulte los formatos de hora del comando <a href="set.md"><strong>set</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a4d79-592">For more information, see the time formats in the <a href="set.md"><strong>set</strong></a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-593">modo de tiempo</span><span class="sxs-lookup"><span data-stu-id="a4d79-593">time mode</span></span></td>
<td><span data-ttu-id="a4d79-594">Devuelve el modo de tiempo de la posición actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-594">Returns the current position time mode.</span></span> <span data-ttu-id="a4d79-595">Puede ser &quot; detectada &quot; , &quot; código de tiempo &quot; o &quot; contador &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-595">It can be &quot;detect&quot;, &quot;timecode&quot;, or &quot;counter&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-596">tipo de tiempo</span><span class="sxs-lookup"><span data-stu-id="a4d79-596">time type</span></span></td>
<td><span data-ttu-id="a4d79-597">Devuelve el tiempo de la posición actual en uso: &quot; código de tiempo &quot; o &quot; contador &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-597">Returns the current position time in use: &quot;timecode&quot; or &quot;counter&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-598">código de tiempo presente</span><span class="sxs-lookup"><span data-stu-id="a4d79-598">timecode present</span></span></td>
<td><span data-ttu-id="a4d79-599">Devuelve <strong>true</strong> si el código de tiempo se ha grabado en la posición actual de la cinta.</span><span class="sxs-lookup"><span data-stu-id="a4d79-599">Returns <strong>TRUE</strong> if timecode has been recorded at the current position on the tape.</span></span> <span data-ttu-id="a4d79-600">El código de tiempo debe avanzar desde la posición actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-600">The timecode must advance from the current position.</span></span> <span data-ttu-id="a4d79-601">Es posible que sea necesario reproducir un VCR para comprobar esta condición.</span><span class="sxs-lookup"><span data-stu-id="a4d79-601">A VCR might need to be played to check this condition.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-602">registro de código de tiempo</span><span class="sxs-lookup"><span data-stu-id="a4d79-602">timecode record</span></span></td>
<td><span data-ttu-id="a4d79-603">Devuelve <strong>true</strong> si el VCR está establecido para grabar código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-603">Returns <strong>TRUE</strong> if the VCR is set to record timecode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-604">tipo de código de tiempo</span><span class="sxs-lookup"><span data-stu-id="a4d79-604">timecode type</span></span></td>
<td><span data-ttu-id="a4d79-605">Devuelve &quot; SMPTE &quot; , &quot; eliminación SMPTE &quot; , &quot; otro &quot; o &quot; ninguno &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-605">Returns &quot;smpte&quot;, &quot;smpte drop&quot;, &quot;other&quot;, or &quot;none&quot;.</span></span> <span data-ttu-id="a4d79-606">Tenga en cuenta que los fotogramas por segundo se pueden obtener del &quot; comando tasa de fotogramas de estado &quot; y la precisión del dispositivo puede ser devuelta por el comando precisión de búsqueda de <a href="capability.md"><strong>capacidad</strong></a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-606">Note the frames per second can be obtained from the status &quot;frame rate&quot; command, and the accuracy of the device can be returned by the <a href="capability.md"><strong>capability</strong></a> &quot;seek accuracy&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-607">trama</span><span class="sxs-lookup"><span data-stu-id="a4d79-607">tint</span></span></td>
<td><span data-ttu-id="a4d79-608">Devuelve el nivel de matiz de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-608">Returns the current video-tint level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-609">agudos</span><span class="sxs-lookup"><span data-stu-id="a4d79-609">treble</span></span></td>
<td><span data-ttu-id="a4d79-610">Devuelve el nivel de audio-agudos actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-610">Returns the current audio-treble level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-611">número de sintonizador</span><span class="sxs-lookup"><span data-stu-id="a4d79-611">tuner number</span></span></td>
<td><span data-ttu-id="a4d79-612">Devuelve el número de sintonizador lógico actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-612">Returns the current logical-tuner number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-613">no guardados</span><span class="sxs-lookup"><span data-stu-id="a4d79-613">unsaved</span></span></td>
<td><span data-ttu-id="a4d79-614">Devuelve <strong>true</strong> si hay datos registrados en el área de trabajo que podrían perderse como resultado de un <a href="close.md"><strong>comando cerrar</strong></a>, <a href="load.md"><strong>cargar</strong></a>, <a href="record.md"><strong>grabar</strong></a>, <a href="reserve.md"><strong>reservar</strong></a>, <a href="cut.md"><strong>cortar</strong></a>, <a href="delete.md"><strong>eliminar</strong></a>o <a href="paste.md"><strong>pegar</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a4d79-614">Returns <strong>TRUE</strong> if there is recorded data in the workspace that might be lost as a result of a <a href="close.md"><strong>close</strong></a>, <a href="load.md"><strong>load</strong></a>, <a href="record.md"><strong>record</strong></a>, <a href="reserve.md"><strong>reserve</strong></a>, <a href="cut.md"><strong>cut</strong></a>, <a href="delete.md"><strong>delete</strong></a>, or <a href="paste.md"><strong>paste</strong></a> command.</span></span> <span data-ttu-id="a4d79-615">Devuelve <strong>false</strong> en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a4d79-615">Returns <strong>FALSE</strong> otherwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-616">video</span><span class="sxs-lookup"><span data-stu-id="a4d79-616">video</span></span></td>
<td><span data-ttu-id="a4d79-617">Devuelve &quot; on &quot; u &quot; OFF &quot; , que refleja el estado establecido por el comando <a href="setvideo.md"><strong>setvideo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a4d79-617">Returns &quot;on&quot; or &quot;off&quot;, reflecting the state set by the <a href="setvideo.md"><strong>setvideo</strong></a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-618">color de clave de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-618">video key color</span></span></td>
<td><span data-ttu-id="a4d79-619">Devuelve el valor del color de la clave.</span><span class="sxs-lookup"><span data-stu-id="a4d79-619">Returns the value for the key color.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-620">Índice de clave de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-620">video key index</span></span></td>
<td><span data-ttu-id="a4d79-621">Devuelve el valor del índice de clave.</span><span class="sxs-lookup"><span data-stu-id="a4d79-621">Returns the value for the key index.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-622">monitor de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-622">video monitor</span></span></td>
<td><span data-ttu-id="a4d79-623">Devuelve &quot; &quot; la salida o uno de los tipos válidos de entrada de origen.</span><span class="sxs-lookup"><span data-stu-id="a4d79-623">Returns &quot;output&quot; or one of the valid source-input types.</span></span> <span data-ttu-id="a4d79-624">Para obtener más información, consulte el comando monitor de <a href="setvideo.md"><strong>setvideo</strong></a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-624">For more information, see the <a href="setvideo.md"><strong>setvideo</strong></a> &quot;monitor&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-625">número de monitor de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-625">video monitor number</span></span></td>
<td><span data-ttu-id="a4d79-626">Devuelve el número de vídeo supervisado del tipo devuelto por el monitor de vídeo de estado &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-626">Returns the monitored-video number of the type returned by status &quot;video monitor&quot;.</span></span> <span data-ttu-id="a4d79-627">Para obtener más información, consulte el comando <a href="setvideo.md">setvideo</a> .</span><span class="sxs-lookup"><span data-stu-id="a4d79-627">For more information, see the <a href="setvideo.md">setvideo</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-628">grabación de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-628">video record</span></span></td>
<td><span data-ttu-id="a4d79-629">Devuelve &quot; on &quot; u &quot; OFF &quot; , que refleja el estado actual establecido por el registro <a href="setvideo.md"><strong>setvideo</strong></a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d79-629">Returns &quot;on&quot; or &quot;off&quot;, reflecting the current state set by <a href="setvideo.md"><strong>setvideo</strong></a> &quot;record&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-630"><em>número</em> de pista de grabación de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-630">video record track <em>number</em></span></span></td>
<td><span data-ttu-id="a4d79-631">Devuelve <strong>true</strong> si el VCR está configurado para grabar vídeo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-631">Return <strong>TRUE</strong> if the VCR is set to record video.</span></span> <span data-ttu-id="a4d79-632">Si no se proporciona ningún número de pista, se asume el valor predeterminado de 1.</span><span class="sxs-lookup"><span data-stu-id="a4d79-632">If no track number is given, the default value of 1 is assumed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-633">origen de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-633">video source</span></span></td>
<td><span data-ttu-id="a4d79-634">Devuelve el tipo de origen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a4d79-634">Returns the video-source type.</span></span> <span data-ttu-id="a4d79-635">Para obtener más información, consulte el comando <a href="setvideo.md"><strong>setvideo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a4d79-635">For more information, see the <a href="setvideo.md"><strong>setvideo</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-636">número de origen de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-636">video source number</span></span></td>
<td><span data-ttu-id="a4d79-637">Devuelve un número que corresponde al origen de vídeo del tipo en uso.</span><span class="sxs-lookup"><span data-stu-id="a4d79-637">Returns a number corresponding to the video source of the type in use.</span></span> <span data-ttu-id="a4d79-638">Por ejemplo, devuelve 2 si se usa la segunda entrada de origen de vídeo NTSC.</span><span class="sxs-lookup"><span data-stu-id="a4d79-638">For example, it returns 2 if the second NTSC video source input is being used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-639">secuencia de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4d79-639">video stream</span></span></td>
<td><span data-ttu-id="a4d79-640">Devuelve el número de secuencia de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="a4d79-640">Returns the current video-stream number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-641">volumen</span><span class="sxs-lookup"><span data-stu-id="a4d79-641">volume</span></span></td>
<td><span data-ttu-id="a4d79-642">Devuelve el volumen medio a los altavoces izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="a4d79-642">Returns the average volume to the left and right speaker.</span></span> <span data-ttu-id="a4d79-643">Esto devuelve un error si el dispositivo no se ha reproducido o no se ha establecido el volumen.</span><span class="sxs-lookup"><span data-stu-id="a4d79-643">This returns an error if the device has not been played or volume has not been set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-644">identificador de ventana</span><span class="sxs-lookup"><span data-stu-id="a4d79-644">window handle</span></span></td>
<td><span data-ttu-id="a4d79-645">Devuelve el valor decimal ASCII para el identificador de ventana en la palabra de orden inferior del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="a4d79-645">Returns the ASCII decimal value for the window handle in the low-order word of the return value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-646">ventana maximizada</span><span class="sxs-lookup"><span data-stu-id="a4d79-646">window maximized</span></span></td>
<td><span data-ttu-id="a4d79-647">Devuelve <strong>true</strong> si la ventana está maximizada.</span><span class="sxs-lookup"><span data-stu-id="a4d79-647">Returns <strong>TRUE</strong> if the window is maximized.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-648">ventana minimizada</span><span class="sxs-lookup"><span data-stu-id="a4d79-648">window minimized</span></span></td>
<td><span data-ttu-id="a4d79-649">Devuelve <strong>true</strong> si la ventana está minimizada.</span><span class="sxs-lookup"><span data-stu-id="a4d79-649">Returns <strong>TRUE</strong> if the window is minimized.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d79-650">ventana visible</span><span class="sxs-lookup"><span data-stu-id="a4d79-650">window visible</span></span></td>
<td><span data-ttu-id="a4d79-651">Devuelve <strong>true</strong> si la ventana no está oculta.</span><span class="sxs-lookup"><span data-stu-id="a4d79-651">Returns <strong>TRUE</strong> if the window is not hidden.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d79-652">protegido contra escritura</span><span class="sxs-lookup"><span data-stu-id="a4d79-652">write protected</span></span></td>
<td><span data-ttu-id="a4d79-653">Devuelve <strong>true</strong> si el dispositivo detecta que no puede grabar (es decir, si la protección contra escritura está activada).</span><span class="sxs-lookup"><span data-stu-id="a4d79-653">Returns <strong>TRUE</strong> if the device detects that it cannot record (that is, if the write protect is on).</span></span> <span data-ttu-id="a4d79-654">Si puede grabar, o si no puede determinar si puede grabar (sin escribir realmente), el controlador devuelve <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d79-654">If it can record, or if it is unable to determine whether or not it can record (without actually writing), the driver returns <strong>FALSE</strong>.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="a4d79-655"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="a4d79-655"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a4d79-656">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="a4d79-656">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="a4d79-657">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="a4d79-657">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="a4d79-658">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a4d79-658">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4d79-659">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4d79-659">Return Value</span></span>

<span data-ttu-id="a4d79-660">Devuelve información en el parámetro *lpszReturnString* de [**mciSendString**](/previous-versions//dd757161(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a4d79-660">Returns information in the *lpszReturnString* parameter of [**mciSendString**](/previous-versions//dd757161(v=vs.85)).</span></span> <span data-ttu-id="a4d79-661">La información depende del tipo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="a4d79-661">The information is dependent on the request type.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4d79-662">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4d79-662">Remarks</span></span>

<span data-ttu-id="a4d79-663">Antes de emitir cualquier comando que use valores de posición, debe establecer el formato de hora deseado mediante el comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="a4d79-663">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="a4d79-664">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a4d79-664">Examples</span></span>

<span data-ttu-id="a4d79-665">El siguiente comando devuelve el modo actual del dispositivo "de".</span><span class="sxs-lookup"><span data-stu-id="a4d79-665">The following command returns the current mode of the "mysound" device.</span></span>

``` syntax
status mysound mode
```

## <a name="requirements"></a><span data-ttu-id="a4d79-666">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4d79-666">Requirements</span></span>



| <span data-ttu-id="a4d79-667">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4d79-667">Requirement</span></span> | <span data-ttu-id="a4d79-668">Value</span><span class="sxs-lookup"><span data-stu-id="a4d79-668">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a4d79-669">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4d79-669">Minimum supported client</span></span><br/> | <span data-ttu-id="a4d79-670">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a4d79-670">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a4d79-671">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4d79-671">Minimum supported server</span></span><br/> | <span data-ttu-id="a4d79-672">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a4d79-672">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a4d79-673">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4d79-673">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4d79-674">MCI</span><span class="sxs-lookup"><span data-stu-id="a4d79-674">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a4d79-675">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="a4d79-675">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="a4d79-676">capability</span><span class="sxs-lookup"><span data-stu-id="a4d79-676">capability</span></span>](capability.md)
</dt> <dt>

[<span data-ttu-id="a4d79-677">grabar</span><span class="sxs-lookup"><span data-stu-id="a4d79-677">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="a4d79-678">close</span><span class="sxs-lookup"><span data-stu-id="a4d79-678">close</span></span>](close.md)
</dt> <dt>

[<span data-ttu-id="a4d79-679">límite</span><span class="sxs-lookup"><span data-stu-id="a4d79-679">cut</span></span>](cut.md)
</dt> <dt>

[<span data-ttu-id="a4d79-680">delete</span><span class="sxs-lookup"><span data-stu-id="a4d79-680">delete</span></span>](delete.md)
</dt> <dt>

[<span data-ttu-id="a4d79-681">carga</span><span class="sxs-lookup"><span data-stu-id="a4d79-681">load</span></span>](load.md)
</dt> <dt>

[<span data-ttu-id="a4d79-682">pause</span><span class="sxs-lookup"><span data-stu-id="a4d79-682">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="a4d79-683">copiar</span><span class="sxs-lookup"><span data-stu-id="a4d79-683">paste</span></span>](paste.md)
</dt> <dt>

[<span data-ttu-id="a4d79-684">record</span><span class="sxs-lookup"><span data-stu-id="a4d79-684">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="a4d79-685">reserva</span><span class="sxs-lookup"><span data-stu-id="a4d79-685">reserve</span></span>](reserve.md)
</dt> <dt>

[<span data-ttu-id="a4d79-686">guardar</span><span class="sxs-lookup"><span data-stu-id="a4d79-686">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="a4d79-687">set</span><span class="sxs-lookup"><span data-stu-id="a4d79-687">set</span></span>](set.md)
</dt> <dt>

[<span data-ttu-id="a4d79-688">setaudio</span><span class="sxs-lookup"><span data-stu-id="a4d79-688">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="a4d79-689">setvideo</span><span class="sxs-lookup"><span data-stu-id="a4d79-689">setvideo</span></span>](setvideo.md)
</dt> <dt>

[<span data-ttu-id="a4d79-690">stop</span><span class="sxs-lookup"><span data-stu-id="a4d79-690">stop</span></span>](stop.md)
</dt> <dt>

[<span data-ttu-id="a4d79-691">deshacer</span><span class="sxs-lookup"><span data-stu-id="a4d79-691">undo</span></span>](undo.md)
</dt> </dl>

 

