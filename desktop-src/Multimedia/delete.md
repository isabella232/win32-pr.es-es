---
title: eliminar comando
description: El comando DELETE elimina un segmento de datos de un archivo. Los dispositivos de audio digital y de onda-vídeo reconocen este comando.
ms.assetid: 9cf084f6-d64e-4487-9407-b68502b7cec9
keywords:
- comando DELETE de Windows multimedia
topic_type:
- apiref
api_name:
- delete
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e356d4972384e676f2e521bd2ca102bb21d7ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905573"
---
# <a name="delete-command"></a><span data-ttu-id="04ad4-105">eliminar comando</span><span class="sxs-lookup"><span data-stu-id="04ad4-105">delete command</span></span>

<span data-ttu-id="04ad4-106">El comando DELETE elimina un segmento de datos de un archivo.</span><span class="sxs-lookup"><span data-stu-id="04ad4-106">The delete command deletes a data segment from a file.</span></span> <span data-ttu-id="04ad4-107">Los dispositivos de audio digital y de onda-vídeo reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="04ad4-107">Digital-video and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="04ad4-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="04ad4-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("delete %s %s %s"), 
  lpszDeviceID, 
  lpszPosition, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="04ad4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04ad4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04ad4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="04ad4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="04ad4-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="04ad4-111">Identifier of an MCI device.</span></span> <span data-ttu-id="04ad4-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="04ad4-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="04ad4-113"><span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*</span><span class="sxs-lookup"><span data-stu-id="04ad4-113"><span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*</span></span>
</dt> <dd>

<span data-ttu-id="04ad4-114">Marca que identifica un segmento de datos que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="04ad4-114">Flag that identifies a data segment to delete.</span></span> <span data-ttu-id="04ad4-115">En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **Delete** y las marcas usadas por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="04ad4-115">The following table lists device types that recognize the **delete** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04ad4-116">Value</span><span class="sxs-lookup"><span data-stu-id="04ad4-116">Value</span></span></th>
<th><span data-ttu-id="04ad4-117">Significado</span><span class="sxs-lookup"><span data-stu-id="04ad4-117">Meaning</span></span></th>
<th><span data-ttu-id="04ad4-118">Significado</span><span class="sxs-lookup"><span data-stu-id="04ad4-118">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="04ad4-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="04ad4-119">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="04ad4-120">en el <em>rectángulo</em></span><span class="sxs-lookup"><span data-stu-id="04ad4-120">at <em>rectangle</em></span></span></li>
<li><span data-ttu-id="04ad4-121"><em>secuencia</em> de flujo de audio</span><span class="sxs-lookup"><span data-stu-id="04ad4-121">audio stream <em>stream</em></span></span></li>
<li><span data-ttu-id="04ad4-122">desde la <em>posición</em></span><span class="sxs-lookup"><span data-stu-id="04ad4-122">from <em>position</em></span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="04ad4-123">para <em>colocar</em></span><span class="sxs-lookup"><span data-stu-id="04ad4-123">to <em>position</em></span></span></li>
<li><span data-ttu-id="04ad4-124"><em>secuencia</em> de flujo de vídeo</span><span class="sxs-lookup"><span data-stu-id="04ad4-124">video stream <em>stream</em></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04ad4-125">waveaudio</span><span class="sxs-lookup"><span data-stu-id="04ad4-125">waveaudio</span></span></td>
<td><span data-ttu-id="04ad4-126">desde la <em>posición</em></span><span class="sxs-lookup"><span data-stu-id="04ad4-126">from <em>position</em></span></span></td>
<td><span data-ttu-id="04ad4-127">para <em>colocar</em></span><span class="sxs-lookup"><span data-stu-id="04ad4-127">to <em>position</em></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="04ad4-128">En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro *lpszPosition* y su significado.</span><span class="sxs-lookup"><span data-stu-id="04ad4-128">The following table lists the flags that can be specified in the *lpszPosition* parameter and their meanings.</span></span>



| <span data-ttu-id="04ad4-129">Value</span><span class="sxs-lookup"><span data-stu-id="04ad4-129">Value</span></span>                 | <span data-ttu-id="04ad4-130">Significado</span><span class="sxs-lookup"><span data-stu-id="04ad4-130">Meaning</span></span>                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04ad4-131">en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="04ad4-131">at *rectangle*</span></span>        | <span data-ttu-id="04ad4-132">Especifica la parte de cada fotograma eliminada.</span><span class="sxs-lookup"><span data-stu-id="04ad4-132">Specifies the portion of each frame deleted.</span></span> <span data-ttu-id="04ad4-133">Si se omite, el valor predeterminado es todo el marco.</span><span class="sxs-lookup"><span data-stu-id="04ad4-133">If omitted, it defaults to the entire frame.</span></span> <span data-ttu-id="04ad4-134">Cuando se especifica este elemento, no se eliminan los marcos.</span><span class="sxs-lookup"><span data-stu-id="04ad4-134">When this item is specified, frames are not deleted.</span></span> <span data-ttu-id="04ad4-135">En su lugar, el área dentro del rectángulo se vuelve negra.</span><span class="sxs-lookup"><span data-stu-id="04ad4-135">Instead the area inside the rectangle becomes black.</span></span>                                          |
| <span data-ttu-id="04ad4-136">*secuencia* de flujo de audio</span><span class="sxs-lookup"><span data-stu-id="04ad4-136">audio stream *stream*</span></span> | <span data-ttu-id="04ad4-137">Especifica la secuencia de audio en el área de trabajo afectada por el comando.</span><span class="sxs-lookup"><span data-stu-id="04ad4-137">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="04ad4-138">Si usa esta marca y también desea eliminar vídeo, también debe usar la marca de "secuencia de vídeo".</span><span class="sxs-lookup"><span data-stu-id="04ad4-138">If you use this flag and also want to delete video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="04ad4-139">(Si no se especifica ninguna marca, se eliminan todas las secuencias de audio y vídeo).</span><span class="sxs-lookup"><span data-stu-id="04ad4-139">(If neither flag is specified, all audio and video streams are deleted.)</span></span> |
| <span data-ttu-id="04ad4-140">desde la *posición*</span><span class="sxs-lookup"><span data-stu-id="04ad4-140">from *position*</span></span>       | <span data-ttu-id="04ad4-141">Especifica la posición en la que comienza la eliminación.</span><span class="sxs-lookup"><span data-stu-id="04ad4-141">Specifies the position at which deletion begins.</span></span> <span data-ttu-id="04ad4-142">Si se omite esta marca, la eliminación comienza en la posición actual.</span><span class="sxs-lookup"><span data-stu-id="04ad4-142">If this flag is omitted, the deletion begins at the current position.</span></span>                                                                                                                       |
| <span data-ttu-id="04ad4-143">para *colocar*</span><span class="sxs-lookup"><span data-stu-id="04ad4-143">to *position*</span></span>         | <span data-ttu-id="04ad4-144">Especifica la posición en la que finaliza la eliminación.</span><span class="sxs-lookup"><span data-stu-id="04ad4-144">Specifies the position at which deletion ends.</span></span> <span data-ttu-id="04ad4-145">Si se omite esta marca, la eliminación continúa hasta el final del contenido o del área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="04ad4-145">If this flag is omitted, the deletion continues to the end of the content or workspace.</span></span>                                                                                                       |
| <span data-ttu-id="04ad4-146">*secuencia* de flujo de vídeo</span><span class="sxs-lookup"><span data-stu-id="04ad4-146">video stream *stream*</span></span> | <span data-ttu-id="04ad4-147">Especifica la secuencia de vídeo en el área de trabajo afectada por el comando.</span><span class="sxs-lookup"><span data-stu-id="04ad4-147">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="04ad4-148">Si usa esta marca y también desea eliminar audio, también debe usar la marca de "secuencia de audio".</span><span class="sxs-lookup"><span data-stu-id="04ad4-148">If you use this flag and also want to delete audio, you must also use "audio stream" flag.</span></span> <span data-ttu-id="04ad4-149">(Si no se especifica ninguna marca, se eliminan todas las secuencias de audio y vídeo).</span><span class="sxs-lookup"><span data-stu-id="04ad4-149">(If neither flag is specified, all audio and video streams are deleted.)</span></span>     |



 

</dd> <dt>

<span data-ttu-id="04ad4-150"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="04ad4-150"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="04ad4-151">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="04ad4-151">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="04ad4-152">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="04ad4-152">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="04ad4-153">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="04ad4-153">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04ad4-154">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04ad4-154">Return Value</span></span>

<span data-ttu-id="04ad4-155">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="04ad4-155">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="04ad4-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04ad4-156">Remarks</span></span>

<span data-ttu-id="04ad4-157">Antes de emitir cualquier comando que use valores de posición, debe establecer el formato de hora deseado mediante el comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="04ad4-157">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="04ad4-158">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="04ad4-158">Examples</span></span>

<span data-ttu-id="04ad4-159">El siguiente comando elimina los datos de audio de forma de onda de 1 milisegundo a 900 milisegundos (suponiendo que el formato de hora se establece en milisegundos).</span><span class="sxs-lookup"><span data-stu-id="04ad4-159">The following command deletes the waveform-audio data from 1 millisecond through 900 milliseconds (assuming the time format is set to milliseconds).</span></span>

``` syntax
delete mysound from 1 to 900
```

## <a name="requirements"></a><span data-ttu-id="04ad4-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04ad4-160">Requirements</span></span>



| <span data-ttu-id="04ad4-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="04ad4-161">Requirement</span></span> | <span data-ttu-id="04ad4-162">Value</span><span class="sxs-lookup"><span data-stu-id="04ad4-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="04ad4-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04ad4-163">Minimum supported client</span></span><br/> | <span data-ttu-id="04ad4-164">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="04ad4-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="04ad4-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04ad4-165">Minimum supported server</span></span><br/> | <span data-ttu-id="04ad4-166">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04ad4-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="04ad4-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="04ad4-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04ad4-168">MCI</span><span class="sxs-lookup"><span data-stu-id="04ad4-168">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="04ad4-169">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="04ad4-169">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="04ad4-170">set</span><span class="sxs-lookup"><span data-stu-id="04ad4-170">set</span></span>](set.md)
</dt> </dl>

 

