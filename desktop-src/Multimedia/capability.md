---
title: funcionalidad (comando)
description: El comando Capability solicita información acerca de una funcionalidad determinada de un dispositivo. Todos los dispositivos MCI reconocen este comando.
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- comando de funcionalidad multimedia de Windows
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a6ac87b98fb8d748a5baf2665cc5a63230b6a98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489599"
---
# <a name="capability-command"></a><span data-ttu-id="e6be2-105">funcionalidad (comando)</span><span class="sxs-lookup"><span data-stu-id="e6be2-105">capability command</span></span>

<span data-ttu-id="e6be2-106">El comando Capability solicita información acerca de una funcionalidad determinada de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6be2-106">The capability command requests information about a particular capability of a device.</span></span> <span data-ttu-id="e6be2-107">Todos los dispositivos MCI reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="e6be2-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="e6be2-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="e6be2-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capability %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="e6be2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6be2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6be2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="e6be2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e6be2-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="e6be2-111">Identifier of an MCI device.</span></span> <span data-ttu-id="e6be2-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6be2-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="e6be2-113"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span><span class="sxs-lookup"><span data-stu-id="e6be2-113"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span></span>
</dt> <dd>

<span data-ttu-id="e6be2-114">Marca que identifica una funcionalidad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6be2-114">Flag that identifies a device capability.</span></span> <span data-ttu-id="e6be2-115">En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando de **funcionalidad** y las marcas usadas por cada tipo:</span><span class="sxs-lookup"><span data-stu-id="e6be2-115">The following table lists device types that recognize the **capability** command and the flags used by each type:</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6be2-116">Value</span><span class="sxs-lookup"><span data-stu-id="e6be2-116">Value</span></span></th>
<th><span data-ttu-id="e6be2-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6be2-117">Type</span></span></th>
<th><span data-ttu-id="e6be2-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6be2-118">Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6be2-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="e6be2-119">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="e6be2-120">puede expulsar</span><span class="sxs-lookup"><span data-stu-id="e6be2-120">can eject</span></span></li>
<li><span data-ttu-id="e6be2-121">puede jugar</span><span class="sxs-lookup"><span data-stu-id="e6be2-121">can play</span></span></li>
<li><span data-ttu-id="e6be2-122">puede grabar</span><span class="sxs-lookup"><span data-stu-id="e6be2-122">can record</span></span></li>
<li><span data-ttu-id="e6be2-123">puede guardar</span><span class="sxs-lookup"><span data-stu-id="e6be2-123">can save</span></span></li>
<li><span data-ttu-id="e6be2-124">dispositivo compuesto</span><span class="sxs-lookup"><span data-stu-id="e6be2-124">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e6be2-125">tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e6be2-125">device type</span></span></li>
<li><span data-ttu-id="e6be2-126">tiene audio</span><span class="sxs-lookup"><span data-stu-id="e6be2-126">has audio</span></span></li>
<li><span data-ttu-id="e6be2-127">tiene vídeo</span><span class="sxs-lookup"><span data-stu-id="e6be2-127">has video</span></span></li>
<li><span data-ttu-id="e6be2-128">utiliza archivos</span><span class="sxs-lookup"><span data-stu-id="e6be2-128">uses files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-129">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="e6be2-129">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="e6be2-130">puede expulsar</span><span class="sxs-lookup"><span data-stu-id="e6be2-130">can eject</span></span></li>
<li><span data-ttu-id="e6be2-131">puede inmovilizar</span><span class="sxs-lookup"><span data-stu-id="e6be2-131">can freeze</span></span></li>
<li><span data-ttu-id="e6be2-132">puede bloquear</span><span class="sxs-lookup"><span data-stu-id="e6be2-132">can lock</span></span></li>
<li><span data-ttu-id="e6be2-133">puede jugar</span><span class="sxs-lookup"><span data-stu-id="e6be2-133">can play</span></span></li>
<li><span data-ttu-id="e6be2-134">puede grabar</span><span class="sxs-lookup"><span data-stu-id="e6be2-134">can record</span></span></li>
<li><span data-ttu-id="e6be2-135">puede invertir</span><span class="sxs-lookup"><span data-stu-id="e6be2-135">can reverse</span></span></li>
<li><span data-ttu-id="e6be2-136">puede guardar</span><span class="sxs-lookup"><span data-stu-id="e6be2-136">can save</span></span></li>
<li><span data-ttu-id="e6be2-137">se puede extender</span><span class="sxs-lookup"><span data-stu-id="e6be2-137">can stretch</span></span></li>
<li><span data-ttu-id="e6be2-138">puede extender la entrada</span><span class="sxs-lookup"><span data-stu-id="e6be2-138">can stretch input</span></span></li>
<li><span data-ttu-id="e6be2-139">puede probar</span><span class="sxs-lookup"><span data-stu-id="e6be2-139">can test</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e6be2-140">dispositivo compuesto</span><span class="sxs-lookup"><span data-stu-id="e6be2-140">compound device</span></span></li>
<li><span data-ttu-id="e6be2-141">tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e6be2-141">device type</span></span></li>
<li><span data-ttu-id="e6be2-142">tiene audio</span><span class="sxs-lookup"><span data-stu-id="e6be2-142">has audio</span></span></li>
<li><span data-ttu-id="e6be2-143">todavía</span><span class="sxs-lookup"><span data-stu-id="e6be2-143">has still</span></span></li>
<li><span data-ttu-id="e6be2-144">tiene vídeo</span><span class="sxs-lookup"><span data-stu-id="e6be2-144">has video</span></span></li>
<li><span data-ttu-id="e6be2-145">velocidad máxima de reproducción</span><span class="sxs-lookup"><span data-stu-id="e6be2-145">maximum play rate</span></span></li>
<li><span data-ttu-id="e6be2-146">velocidad de reproducción mínima</span><span class="sxs-lookup"><span data-stu-id="e6be2-146">minimum play rate</span></span></li>
<li><span data-ttu-id="e6be2-147">utiliza archivos</span><span class="sxs-lookup"><span data-stu-id="e6be2-147">uses files</span></span></li>
<li><span data-ttu-id="e6be2-148">usar paletas</span><span class="sxs-lookup"><span data-stu-id="e6be2-148">uses palettes</span></span></li>
<li><span data-ttu-id="e6be2-149">Windows</span><span class="sxs-lookup"><span data-stu-id="e6be2-149">windows</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-150">overlay</span><span class="sxs-lookup"><span data-stu-id="e6be2-150">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="e6be2-151">puede expulsar</span><span class="sxs-lookup"><span data-stu-id="e6be2-151">can eject</span></span></li>
<li><span data-ttu-id="e6be2-152">puede inmovilizar</span><span class="sxs-lookup"><span data-stu-id="e6be2-152">can freeze</span></span></li>
<li><span data-ttu-id="e6be2-153">puede jugar</span><span class="sxs-lookup"><span data-stu-id="e6be2-153">can play</span></span></li>
<li><span data-ttu-id="e6be2-154">puede grabar</span><span class="sxs-lookup"><span data-stu-id="e6be2-154">can record</span></span></li>
<li><span data-ttu-id="e6be2-155">puede guardar</span><span class="sxs-lookup"><span data-stu-id="e6be2-155">can save</span></span></li>
<li><span data-ttu-id="e6be2-156">se puede extender</span><span class="sxs-lookup"><span data-stu-id="e6be2-156">can stretch</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e6be2-157">dispositivo compuesto</span><span class="sxs-lookup"><span data-stu-id="e6be2-157">compound device</span></span></li>
<li><span data-ttu-id="e6be2-158">tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e6be2-158">device type</span></span></li>
<li><span data-ttu-id="e6be2-159">tiene audio</span><span class="sxs-lookup"><span data-stu-id="e6be2-159">has audio</span></span></li>
<li><span data-ttu-id="e6be2-160">tiene vídeo</span><span class="sxs-lookup"><span data-stu-id="e6be2-160">has video</span></span></li>
<li><span data-ttu-id="e6be2-161">utiliza archivos</span><span class="sxs-lookup"><span data-stu-id="e6be2-161">uses files</span></span></li>
<li><span data-ttu-id="e6be2-162">Windows</span><span class="sxs-lookup"><span data-stu-id="e6be2-162">windows</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-163">sequencer</span><span class="sxs-lookup"><span data-stu-id="e6be2-163">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="e6be2-164">puede expulsar</span><span class="sxs-lookup"><span data-stu-id="e6be2-164">can eject</span></span></li>
<li><span data-ttu-id="e6be2-165">puede jugar</span><span class="sxs-lookup"><span data-stu-id="e6be2-165">can play</span></span></li>
<li><span data-ttu-id="e6be2-166">puede grabar</span><span class="sxs-lookup"><span data-stu-id="e6be2-166">can record</span></span></li>
<li><span data-ttu-id="e6be2-167">puede guardar</span><span class="sxs-lookup"><span data-stu-id="e6be2-167">can save</span></span></li>
<li><span data-ttu-id="e6be2-168">dispositivo compuesto</span><span class="sxs-lookup"><span data-stu-id="e6be2-168">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e6be2-169">tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e6be2-169">device type</span></span></li>
<li><span data-ttu-id="e6be2-170">tiene audio</span><span class="sxs-lookup"><span data-stu-id="e6be2-170">has audio</span></span></li>
<li><span data-ttu-id="e6be2-171">tiene vídeo</span><span class="sxs-lookup"><span data-stu-id="e6be2-171">has video</span></span></li>
<li><span data-ttu-id="e6be2-172">utiliza archivos</span><span class="sxs-lookup"><span data-stu-id="e6be2-172">uses files</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-173">vídeos</span><span class="sxs-lookup"><span data-stu-id="e6be2-173">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="e6be2-174">puede detectar la longitud</span><span class="sxs-lookup"><span data-stu-id="e6be2-174">can detect length</span></span></li>
<li><span data-ttu-id="e6be2-175">puede expulsar</span><span class="sxs-lookup"><span data-stu-id="e6be2-175">can eject</span></span></li>
<li><span data-ttu-id="e6be2-176">puede inmovilizar</span><span class="sxs-lookup"><span data-stu-id="e6be2-176">can freeze</span></span></li>
<li><span data-ttu-id="e6be2-177">puede supervisar orígenes</span><span class="sxs-lookup"><span data-stu-id="e6be2-177">can monitor sources</span></span></li>
<li><span data-ttu-id="e6be2-178">puede jugar</span><span class="sxs-lookup"><span data-stu-id="e6be2-178">can play</span></span></li>
<li><span data-ttu-id="e6be2-179">puede prevertir</span><span class="sxs-lookup"><span data-stu-id="e6be2-179">can preroll</span></span></li>
<li><span data-ttu-id="e6be2-180">puede obtener una vista previa</span><span class="sxs-lookup"><span data-stu-id="e6be2-180">can preview</span></span></li>
<li><span data-ttu-id="e6be2-181">puede grabar</span><span class="sxs-lookup"><span data-stu-id="e6be2-181">can record</span></span></li>
<li><span data-ttu-id="e6be2-182">puede invertir</span><span class="sxs-lookup"><span data-stu-id="e6be2-182">can reverse</span></span></li>
<li><span data-ttu-id="e6be2-183">puede guardar</span><span class="sxs-lookup"><span data-stu-id="e6be2-183">can save</span></span></li>
<li><span data-ttu-id="e6be2-184">puede probar</span><span class="sxs-lookup"><span data-stu-id="e6be2-184">can test</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e6be2-185">tasa de incremento de reloj</span><span class="sxs-lookup"><span data-stu-id="e6be2-185">clock increment rate</span></span></li>
<li><span data-ttu-id="e6be2-186">dispositivo compuesto</span><span class="sxs-lookup"><span data-stu-id="e6be2-186">compound device</span></span></li>
<li><span data-ttu-id="e6be2-187">tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e6be2-187">device type</span></span></li>
<li><span data-ttu-id="e6be2-188">tiene audio</span><span class="sxs-lookup"><span data-stu-id="e6be2-188">has audio</span></span></li>
<li><span data-ttu-id="e6be2-189">tiene reloj</span><span class="sxs-lookup"><span data-stu-id="e6be2-189">has clock</span></span></li>
<li><span data-ttu-id="e6be2-190">tiene código de tiempo</span><span class="sxs-lookup"><span data-stu-id="e6be2-190">has timecode</span></span></li>
<li><span data-ttu-id="e6be2-191">tiene vídeo</span><span class="sxs-lookup"><span data-stu-id="e6be2-191">has video</span></span></li>
<li><span data-ttu-id="e6be2-192">número de marcas</span><span class="sxs-lookup"><span data-stu-id="e6be2-192">number of marks</span></span></li>
<li><span data-ttu-id="e6be2-193">precisión de búsqueda</span><span class="sxs-lookup"><span data-stu-id="e6be2-193">seek accuracy</span></span></li>
<li><span data-ttu-id="e6be2-194">utiliza archivos</span><span class="sxs-lookup"><span data-stu-id="e6be2-194">uses files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-195">videodisco</span><span class="sxs-lookup"><span data-stu-id="e6be2-195">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="e6be2-196">puede expulsar</span><span class="sxs-lookup"><span data-stu-id="e6be2-196">can eject</span></span></li>
<li><span data-ttu-id="e6be2-197">puede jugar</span><span class="sxs-lookup"><span data-stu-id="e6be2-197">can play</span></span></li>
<li><span data-ttu-id="e6be2-198">puede grabar</span><span class="sxs-lookup"><span data-stu-id="e6be2-198">can record</span></span></li>
<li><span data-ttu-id="e6be2-199">puede invertir</span><span class="sxs-lookup"><span data-stu-id="e6be2-199">can reverse</span></span></li>
<li><span data-ttu-id="e6be2-200">puede guardar</span><span class="sxs-lookup"><span data-stu-id="e6be2-200">can save</span></span></li>
<li><span data-ttu-id="e6be2-201">CAV</span><span class="sxs-lookup"><span data-stu-id="e6be2-201">CAV</span></span></li>
<li><span data-ttu-id="e6be2-202">CLV</span><span class="sxs-lookup"><span data-stu-id="e6be2-202">CLV</span></span></li>
<li><span data-ttu-id="e6be2-203">dispositivo compuesto</span><span class="sxs-lookup"><span data-stu-id="e6be2-203">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e6be2-204">tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e6be2-204">device type</span></span></li>
<li><span data-ttu-id="e6be2-205">velocidad de reproducción rápida</span><span class="sxs-lookup"><span data-stu-id="e6be2-205">fast play rate</span></span></li>
<li><span data-ttu-id="e6be2-206">tiene audio</span><span class="sxs-lookup"><span data-stu-id="e6be2-206">has audio</span></span></li>
<li><span data-ttu-id="e6be2-207">tiene vídeo</span><span class="sxs-lookup"><span data-stu-id="e6be2-207">has video</span></span></li>
<li><span data-ttu-id="e6be2-208">velocidad de reproducción normal</span><span class="sxs-lookup"><span data-stu-id="e6be2-208">normal play rate</span></span></li>
<li><span data-ttu-id="e6be2-209">velocidad de reproducción lenta</span><span class="sxs-lookup"><span data-stu-id="e6be2-209">slow play rate</span></span></li>
<li><span data-ttu-id="e6be2-210">utiliza archivos</span><span class="sxs-lookup"><span data-stu-id="e6be2-210">uses files</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-211">waveaudio</span><span class="sxs-lookup"><span data-stu-id="e6be2-211">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="e6be2-212">puede expulsar</span><span class="sxs-lookup"><span data-stu-id="e6be2-212">can eject</span></span></li>
<li><span data-ttu-id="e6be2-213">puede jugar</span><span class="sxs-lookup"><span data-stu-id="e6be2-213">can play</span></span></li>
<li><span data-ttu-id="e6be2-214">puede grabar</span><span class="sxs-lookup"><span data-stu-id="e6be2-214">can record</span></span></li>
<li><span data-ttu-id="e6be2-215">puede guardar</span><span class="sxs-lookup"><span data-stu-id="e6be2-215">can save</span></span></li>
<li><span data-ttu-id="e6be2-216">dispositivo compuesto</span><span class="sxs-lookup"><span data-stu-id="e6be2-216">compound device</span></span></li>
<li><span data-ttu-id="e6be2-217">tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e6be2-217">device type</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e6be2-218">tiene audio</span><span class="sxs-lookup"><span data-stu-id="e6be2-218">has audio</span></span></li>
<li><span data-ttu-id="e6be2-219">tiene vídeo</span><span class="sxs-lookup"><span data-stu-id="e6be2-219">has video</span></span></li>
<li><span data-ttu-id="e6be2-220">inputs</span><span class="sxs-lookup"><span data-stu-id="e6be2-220">inputs</span></span></li>
<li><span data-ttu-id="e6be2-221">outputs</span><span class="sxs-lookup"><span data-stu-id="e6be2-221">outputs</span></span></li>
<li><span data-ttu-id="e6be2-222">utiliza archivos</span><span class="sxs-lookup"><span data-stu-id="e6be2-222">uses files</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e6be2-223">En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro *lpszRequest* y su significado:</span><span class="sxs-lookup"><span data-stu-id="e6be2-223">The following table lists the flags that can be specified in the *lpszRequest* parameter and their meanings:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6be2-224">Marcas</span><span class="sxs-lookup"><span data-stu-id="e6be2-224">Flags</span></span></th>
<th><span data-ttu-id="e6be2-225">Significado</span><span class="sxs-lookup"><span data-stu-id="e6be2-225">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6be2-226">puede detectar la longitud</span><span class="sxs-lookup"><span data-stu-id="e6be2-226">can detect length</span></span></td>
<td><span data-ttu-id="e6be2-227">Devuelve <strong>true</strong> si el dispositivo puede detectar la longitud del medio.</span><span class="sxs-lookup"><span data-stu-id="e6be2-227">Returns <strong>TRUE</strong> if the device can detect the length of the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-228">puede expulsar</span><span class="sxs-lookup"><span data-stu-id="e6be2-228">can eject</span></span></td>
<td><span data-ttu-id="e6be2-229">Devuelve <strong>true</strong> si el dispositivo puede expulsar los medios.</span><span class="sxs-lookup"><span data-stu-id="e6be2-229">Returns <strong>TRUE</strong> if the device can eject the media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-230">puede inmovilizar</span><span class="sxs-lookup"><span data-stu-id="e6be2-230">can freeze</span></span></td>
<td><span data-ttu-id="e6be2-231">Devuelve <strong>true</strong> si el dispositivo puede inmovilizar los datos en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="e6be2-231">Returns <strong>TRUE</strong> if the device can freeze data in the frame buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-232">puede bloquear</span><span class="sxs-lookup"><span data-stu-id="e6be2-232">can lock</span></span></td>
<td><span data-ttu-id="e6be2-233">Devuelve <strong>true</strong> si el dispositivo puede bloquear los datos.</span><span class="sxs-lookup"><span data-stu-id="e6be2-233">Returns <strong>TRUE</strong> if the device can lock data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-234">puede supervisar orígenes</span><span class="sxs-lookup"><span data-stu-id="e6be2-234">can monitor sources</span></span></td>
<td><span data-ttu-id="e6be2-235">Devuelve <strong>true</strong> si el dispositivo puede pasar una entrada (origen) a la salida supervisada, independientemente de la selección de entrada actual.</span><span class="sxs-lookup"><span data-stu-id="e6be2-235">Returns <strong>TRUE</strong> if the device can pass an input (source) to the monitored output, independent of the current input selection.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-236">puede jugar</span><span class="sxs-lookup"><span data-stu-id="e6be2-236">can play</span></span></td>
<td><span data-ttu-id="e6be2-237">Devuelve <strong>true</strong> si el dispositivo puede reproducirse.</span><span class="sxs-lookup"><span data-stu-id="e6be2-237">Returns <strong>TRUE</strong> if the device can play.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-238">puede prevertir</span><span class="sxs-lookup"><span data-stu-id="e6be2-238">can preroll</span></span></td>
<td><span data-ttu-id="e6be2-239">Devuelve <strong>true</strong> si el dispositivo admite la &quot; marca de preroll &quot; con el comando <a href="cue.md">CUE</a> .</span><span class="sxs-lookup"><span data-stu-id="e6be2-239">Returns <strong>TRUE</strong> if the device supports the &quot;preroll&quot; flag with the <a href="cue.md">cue</a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-240">puede obtener una vista previa</span><span class="sxs-lookup"><span data-stu-id="e6be2-240">can preview</span></span></td>
<td><span data-ttu-id="e6be2-241">Devuelve <strong>true</strong> si el dispositivo admite versiones preliminares.</span><span class="sxs-lookup"><span data-stu-id="e6be2-241">Returns <strong>TRUE</strong> if the device supports previews.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-242">puede grabar</span><span class="sxs-lookup"><span data-stu-id="e6be2-242">can record</span></span></td>
<td><span data-ttu-id="e6be2-243">Devuelve <strong>true</strong> si el dispositivo admite la grabación.</span><span class="sxs-lookup"><span data-stu-id="e6be2-243">Returns <strong>TRUE</strong> if the device supports recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-244">puede invertir</span><span class="sxs-lookup"><span data-stu-id="e6be2-244">can reverse</span></span></td>
<td><span data-ttu-id="e6be2-245">Devuelve <strong>true</strong> si el dispositivo puede reproducirse en orden inverso.</span><span class="sxs-lookup"><span data-stu-id="e6be2-245">Returns <strong>TRUE</strong> if the device can play in reverse.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-246">puede guardar</span><span class="sxs-lookup"><span data-stu-id="e6be2-246">can save</span></span></td>
<td><span data-ttu-id="e6be2-247">Devuelve <strong>true</strong> si el dispositivo puede guardar datos.</span><span class="sxs-lookup"><span data-stu-id="e6be2-247">Returns <strong>TRUE</strong> if the device can save data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-248">se puede extender</span><span class="sxs-lookup"><span data-stu-id="e6be2-248">can stretch</span></span></td>
<td><span data-ttu-id="e6be2-249">Devuelve <strong>true</strong> si el dispositivo puede expandir fotogramas para rellenar un rectángulo de presentación determinado.</span><span class="sxs-lookup"><span data-stu-id="e6be2-249">Returns <strong>TRUE</strong> if the device can stretch frames to fill a given display rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-250">puede extender la entrada</span><span class="sxs-lookup"><span data-stu-id="e6be2-250">can stretch input</span></span></td>
<td><span data-ttu-id="e6be2-251">Devuelve <strong>true</strong> si el dispositivo puede cambiar el tamaño de una imagen en el proceso de digitalización en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="e6be2-251">Returns <strong>TRUE</strong> if the device can resize an image in the process of digitizing it into the frame buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-252">puede probar</span><span class="sxs-lookup"><span data-stu-id="e6be2-252">can test</span></span></td>
<td><span data-ttu-id="e6be2-253">Devuelve <strong>true</strong> si el dispositivo reconoce la palabra clave de prueba.</span><span class="sxs-lookup"><span data-stu-id="e6be2-253">Returns <strong>TRUE</strong> if the device recognizes the test keyword.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-254">cav</span><span class="sxs-lookup"><span data-stu-id="e6be2-254">cav</span></span></td>
<td><span data-ttu-id="e6be2-255">Cuando se combina con otros elementos, esta marca especifica que la información de devolución se aplica al formato CAV de los videodiscos.</span><span class="sxs-lookup"><span data-stu-id="e6be2-255">When combined with other items, this flag specifies that the return information applies to CAV format videodiscs.</span></span> <span data-ttu-id="e6be2-256">Este es el valor predeterminado si no se inserta ningún CD.</span><span class="sxs-lookup"><span data-stu-id="e6be2-256">This is the default if no videodisc is inserted.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-257">tasa de incremento de reloj</span><span class="sxs-lookup"><span data-stu-id="e6be2-257">clock increment rate</span></span></td>
<td><span data-ttu-id="e6be2-258">Devuelve el número de subdivisiones que admite el reloj externo por segundo.</span><span class="sxs-lookup"><span data-stu-id="e6be2-258">Returns the number of subdivisions the external clock supports per second.</span></span> <span data-ttu-id="e6be2-259">Si el reloj externo es un reloj de milisegundos, el valor devuelto es 1000.</span><span class="sxs-lookup"><span data-stu-id="e6be2-259">If the external clock is a millisecond clock, the return value is 1000.</span></span> <span data-ttu-id="e6be2-260">Si el valor devuelto es 0, no se admite ningún reloj.</span><span class="sxs-lookup"><span data-stu-id="e6be2-260">If the return value is 0, no clock is supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-261">clv</span><span class="sxs-lookup"><span data-stu-id="e6be2-261">clv</span></span></td>
<td><span data-ttu-id="e6be2-262">Cuando se combina con otros elementos, esta marca especifica que la información de devolución se aplica al formato CLV de los videodiscos.</span><span class="sxs-lookup"><span data-stu-id="e6be2-262">When combined with other items, this flag specifies that the return information applies to CLV format videodiscs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-263">dispositivo compuesto</span><span class="sxs-lookup"><span data-stu-id="e6be2-263">compound device</span></span></td>
<td><span data-ttu-id="e6be2-264">Devuelve <strong>true</strong> si el dispositivo admite un nombre de elemento (nombre de archivo).</span><span class="sxs-lookup"><span data-stu-id="e6be2-264">Returns <strong>TRUE</strong> if the device supports an element name (filename).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-265">tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e6be2-265">device type</span></span></td>
<td><span data-ttu-id="e6be2-266">Devuelve un nombre de tipo de dispositivo, que puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e6be2-266">Returns a device type name, which can be one of the following:</span></span>
<ul>
<li><span data-ttu-id="e6be2-267">cdaudio</span><span class="sxs-lookup"><span data-stu-id="e6be2-267">cdaudio</span></span></li>
<li><span data-ttu-id="e6be2-268">incrementa</span><span class="sxs-lookup"><span data-stu-id="e6be2-268">dat</span></span></li>
<li><span data-ttu-id="e6be2-269">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="e6be2-269">digitalvideo</span></span></li>
<li><span data-ttu-id="e6be2-270">Otros</span><span class="sxs-lookup"><span data-stu-id="e6be2-270">other</span></span></li>
<li><span data-ttu-id="e6be2-271">overlay</span><span class="sxs-lookup"><span data-stu-id="e6be2-271">overlay</span></span></li>
<li><span data-ttu-id="e6be2-272">escáner</span><span class="sxs-lookup"><span data-stu-id="e6be2-272">scanner</span></span></li>
<li><span data-ttu-id="e6be2-273">sequencer</span><span class="sxs-lookup"><span data-stu-id="e6be2-273">sequencer</span></span></li>
<li><span data-ttu-id="e6be2-274">vídeos</span><span class="sxs-lookup"><span data-stu-id="e6be2-274">vcr</span></span></li>
<li><span data-ttu-id="e6be2-275">videodisco</span><span class="sxs-lookup"><span data-stu-id="e6be2-275">videodisc</span></span></li>
<li><span data-ttu-id="e6be2-276">waveaudio</span><span class="sxs-lookup"><span data-stu-id="e6be2-276">waveaudio</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-277">velocidad de reproducción rápida</span><span class="sxs-lookup"><span data-stu-id="e6be2-277">fast play rate</span></span></td>
<td><span data-ttu-id="e6be2-278">Devuelve la velocidad de reproducción rápida en fotogramas por segundo o cero si el dispositivo no se puede reproducir rápidamente.</span><span class="sxs-lookup"><span data-stu-id="e6be2-278">Returns the fast play rate in frames per second, or zero if the device cannot play fast.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-279">tiene audio</span><span class="sxs-lookup"><span data-stu-id="e6be2-279">has audio</span></span></td>
<td><span data-ttu-id="e6be2-280">Devuelve <strong>true</strong> si el dispositivo admite la reproducción de audio.</span><span class="sxs-lookup"><span data-stu-id="e6be2-280">Returns <strong>TRUE</strong> if the device supports audio playback.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-281">tiene reloj</span><span class="sxs-lookup"><span data-stu-id="e6be2-281">has clock</span></span></td>
<td><span data-ttu-id="e6be2-282">Devuelve <strong>true</strong> si el dispositivo tiene un reloj.</span><span class="sxs-lookup"><span data-stu-id="e6be2-282">Returns <strong>TRUE</strong> if the device has a clock.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-283">todavía</span><span class="sxs-lookup"><span data-stu-id="e6be2-283">has still</span></span></td>
<td><span data-ttu-id="e6be2-284">Devuelve <strong>true</strong> si el dispositivo trata los archivos con una sola imagen de forma más eficaz que los archivos de vídeo de movimiento.</span><span class="sxs-lookup"><span data-stu-id="e6be2-284">Returns <strong>TRUE</strong> if the device treats files with a single image more efficiently than motion video files.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-285">tiene código de tiempo</span><span class="sxs-lookup"><span data-stu-id="e6be2-285">has timecode</span></span></td>
<td><span data-ttu-id="e6be2-286">Devuelve <strong>true</strong> si el dispositivo es capaz de admitir el código de tiempo, o si se desconoce.</span><span class="sxs-lookup"><span data-stu-id="e6be2-286">Returns <strong>TRUE</strong> if the device is capable of supporting timecode, or if it is unknown.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-287">tiene vídeo</span><span class="sxs-lookup"><span data-stu-id="e6be2-287">has video</span></span></td>
<td><span data-ttu-id="e6be2-288">Devuelve <strong>true</strong> si el dispositivo admite vídeo.</span><span class="sxs-lookup"><span data-stu-id="e6be2-288">Returns <strong>TRUE</strong> if the device supports video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-289">inputs</span><span class="sxs-lookup"><span data-stu-id="e6be2-289">inputs</span></span></td>
<td><span data-ttu-id="e6be2-290">Devuelve el número total de dispositivos de entrada.</span><span class="sxs-lookup"><span data-stu-id="e6be2-290">Returns the total number of input devices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-291">velocidad máxima de reproducción</span><span class="sxs-lookup"><span data-stu-id="e6be2-291">maximum play rate</span></span></td>
<td><span data-ttu-id="e6be2-292">Devuelve la velocidad de reproducción máxima, en fotogramas por segundo, del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6be2-292">Returns the maximum play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-293">velocidad de reproducción mínima</span><span class="sxs-lookup"><span data-stu-id="e6be2-293">minimum play rate</span></span></td>
<td><span data-ttu-id="e6be2-294">Devuelve la velocidad de reproducción mínima, en fotogramas por segundo, del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6be2-294">Returns the minimum play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-295">velocidad de reproducción normal</span><span class="sxs-lookup"><span data-stu-id="e6be2-295">normal play rate</span></span></td>
<td><span data-ttu-id="e6be2-296">Devuelve la velocidad de reproducción normal, en fotogramas por segundo, del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6be2-296">Returns the normal play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-297">número de marcas</span><span class="sxs-lookup"><span data-stu-id="e6be2-297">number of marks</span></span></td>
<td><span data-ttu-id="e6be2-298">Devuelve el número máximo de marcas que se pueden usar; cero indica que no se admiten las marcas.</span><span class="sxs-lookup"><span data-stu-id="e6be2-298">Returns the maximum number of marks that can be used; zero indicates that marks are unsupported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-299">outputs</span><span class="sxs-lookup"><span data-stu-id="e6be2-299">outputs</span></span></td>
<td><span data-ttu-id="e6be2-300">Devuelve el número total de dispositivos de salida.</span><span class="sxs-lookup"><span data-stu-id="e6be2-300">Returns the total number of output devices.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-301">precisión de búsqueda</span><span class="sxs-lookup"><span data-stu-id="e6be2-301">seek accuracy</span></span></td>
<td><span data-ttu-id="e6be2-302">Devuelve la precisión esperada de una búsqueda en marcos; 0 indica que el dispositivo es preciso fotograma, 1 indica que el dispositivo espera estar dentro de un fotograma de la posición de búsqueda indicada, etc.</span><span class="sxs-lookup"><span data-stu-id="e6be2-302">Returns the expected accuracy of a search in frames; 0 indicates that the device is frame accurate, 1 indicates that the device expects to be within one frame of the indicated seek position, and so on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-303">velocidad de reproducción lenta</span><span class="sxs-lookup"><span data-stu-id="e6be2-303">slow play rate</span></span></td>
<td><span data-ttu-id="e6be2-304">Devuelve la velocidad de reproducción lenta en fotogramas por segundo, o bien cero si el dispositivo no se puede reproducir lentamente.</span><span class="sxs-lookup"><span data-stu-id="e6be2-304">Returns the slow play rate in frames per second, or zero if the device cannot play slowly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-305">utiliza archivos</span><span class="sxs-lookup"><span data-stu-id="e6be2-305">uses files</span></span></td>
<td><span data-ttu-id="e6be2-306">Devuelve <strong>true</strong> si el almacenamiento de datos utilizado por un dispositivo compuesto es un archivo.</span><span class="sxs-lookup"><span data-stu-id="e6be2-306">Returns <strong>TRUE</strong> if the data storage used by a compound device is a file.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6be2-307">usar paletas</span><span class="sxs-lookup"><span data-stu-id="e6be2-307">uses palettes</span></span></td>
<td><span data-ttu-id="e6be2-308">Devuelve <strong>true</strong> si el dispositivo usa las paletas.</span><span class="sxs-lookup"><span data-stu-id="e6be2-308">Returns <strong>TRUE</strong> if the device uses palettes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6be2-309">Windows</span><span class="sxs-lookup"><span data-stu-id="e6be2-309">windows</span></span></td>
<td><span data-ttu-id="e6be2-310">Devuelve el número de ventanas de pantalla simultáneas que el dispositivo puede admitir.</span><span class="sxs-lookup"><span data-stu-id="e6be2-310">Returns the number of simultaneous display windows the device can support.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="e6be2-311"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="e6be2-311"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e6be2-312">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="e6be2-312">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="e6be2-313">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="e6be2-313">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="e6be2-314">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e6be2-314">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6be2-315">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6be2-315">Return Value</span></span>

<span data-ttu-id="e6be2-316">Devuelve información en el parámetro *lpszReturnString* de la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e6be2-316">Returns information in the *lpszReturnString* parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="e6be2-317">La información depende del tipo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="e6be2-317">The information is dependent on the request type.</span></span>

## <a name="examples"></a><span data-ttu-id="e6be2-318">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e6be2-318">Examples</span></span>

<span data-ttu-id="e6be2-319">El siguiente comando devuelve el tipo de dispositivo del dispositivo "".</span><span class="sxs-lookup"><span data-stu-id="e6be2-319">The following command returns the device type of the "mysound" device.</span></span>

``` syntax
capability mysound device type
```

## <a name="requirements"></a><span data-ttu-id="e6be2-320">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6be2-320">Requirements</span></span>



| <span data-ttu-id="e6be2-321">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6be2-321">Requirement</span></span> | <span data-ttu-id="e6be2-322">Value</span><span class="sxs-lookup"><span data-stu-id="e6be2-322">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e6be2-323">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6be2-323">Minimum supported client</span></span><br/> | <span data-ttu-id="e6be2-324">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e6be2-324">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e6be2-325">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6be2-325">Minimum supported server</span></span><br/> | <span data-ttu-id="e6be2-326">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e6be2-326">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e6be2-327">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6be2-327">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6be2-328">MCI</span><span class="sxs-lookup"><span data-stu-id="e6be2-328">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e6be2-329">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="e6be2-329">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="e6be2-330">indicación</span><span class="sxs-lookup"><span data-stu-id="e6be2-330">cue</span></span>](cue.md)
</dt> </dl>

 

