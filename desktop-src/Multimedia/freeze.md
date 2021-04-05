---
title: Freeze (comando)
description: El comando Freeze inmoviliza la entrada de vídeo o la salida de vídeo en un VCR o deshabilita la adquisición de vídeo en el búfer de fotogramas. Los dispositivos digitales-vídeo, superposición de vídeo y VCR reconocen este comando.
ms.assetid: 49f3ab98-e893-402a-be78-6140af3b81df
keywords:
- comando Freeze Windows multimedia
topic_type:
- apiref
api_name:
- freeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b63fbb2d888fc1ca315c0b511bcb18224c8168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078844"
---
# <a name="freeze-command"></a><span data-ttu-id="78aaa-105">Freeze (comando)</span><span class="sxs-lookup"><span data-stu-id="78aaa-105">freeze command</span></span>

<span data-ttu-id="78aaa-106">El comando Freeze inmoviliza la entrada de vídeo o la salida de vídeo en un VCR o deshabilita la adquisición de vídeo en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="78aaa-106">The freeze command freezes video input or video output on a VCR or disables video acquisition to the frame buffer.</span></span> <span data-ttu-id="78aaa-107">Los dispositivos digitales-vídeo, superposición de vídeo y VCR reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="78aaa-107">Digital-video, video-overlay, and VCR devices recognize this command.</span></span>

<span data-ttu-id="78aaa-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="78aaa-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("freeze %s %s %s"), 
  lpszDeviceID, 
  lpszFreezeFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="78aaa-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78aaa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78aaa-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="78aaa-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="78aaa-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="78aaa-111">Identifier of an MCI device.</span></span> <span data-ttu-id="78aaa-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78aaa-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="78aaa-113"><span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*</span><span class="sxs-lookup"><span data-stu-id="78aaa-113"><span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*</span></span>
</dt> <dd>

<span data-ttu-id="78aaa-114">Marca que identifica lo que se va a inmovilizar.</span><span class="sxs-lookup"><span data-stu-id="78aaa-114">Flag that identifies what to freeze.</span></span> <span data-ttu-id="78aaa-115">En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **Freeze** y las marcas usadas por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="78aaa-115">The following table lists device types that recognize the **freeze** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78aaa-116">Value</span><span class="sxs-lookup"><span data-stu-id="78aaa-116">Value</span></span></th>
<th><span data-ttu-id="78aaa-117">Significado</span><span class="sxs-lookup"><span data-stu-id="78aaa-117">Meaning</span></span></th>
<th><span data-ttu-id="78aaa-118">Significado</span><span class="sxs-lookup"><span data-stu-id="78aaa-118">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="78aaa-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="78aaa-119">digitalvideo</span></span></td>
<td><span data-ttu-id="78aaa-120">en el <em>rectángulo</em></span><span class="sxs-lookup"><span data-stu-id="78aaa-120">at <em>rectangle</em></span></span></td>
<td><span data-ttu-id="78aaa-121">ajena</span><span class="sxs-lookup"><span data-stu-id="78aaa-121">outside</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78aaa-122">overlay</span><span class="sxs-lookup"><span data-stu-id="78aaa-122">overlay</span></span></td>
<td><span data-ttu-id="78aaa-123">en el <em>rectángulo</em></span><span class="sxs-lookup"><span data-stu-id="78aaa-123">at <em>rectangle</em></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="78aaa-124">vídeos</span><span class="sxs-lookup"><span data-stu-id="78aaa-124">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="78aaa-125">campo</span><span class="sxs-lookup"><span data-stu-id="78aaa-125">field</span></span></li>
<li><span data-ttu-id="78aaa-126">frame</span><span class="sxs-lookup"><span data-stu-id="78aaa-126">frame</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="78aaa-127">input</span><span class="sxs-lookup"><span data-stu-id="78aaa-127">input</span></span></li>
<li><span data-ttu-id="78aaa-128">output</span><span class="sxs-lookup"><span data-stu-id="78aaa-128">output</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="78aaa-129">En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro *lpszFreezeFlags* y su significado.</span><span class="sxs-lookup"><span data-stu-id="78aaa-129">The following table lists the flags that can be specified in the *lpszFreezeFlags* parameter and their meanings.</span></span>



| <span data-ttu-id="78aaa-130">Value</span><span class="sxs-lookup"><span data-stu-id="78aaa-130">Value</span></span>          | <span data-ttu-id="78aaa-131">Significado</span><span class="sxs-lookup"><span data-stu-id="78aaa-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78aaa-132">en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="78aaa-132">at *rectangle*</span></span> | <span data-ttu-id="78aaa-133">Especifica la región que se va a inmovilizar.</span><span class="sxs-lookup"><span data-stu-id="78aaa-133">Specifies the region that will be frozen.</span></span> <span data-ttu-id="78aaa-134">En el caso de los dispositivos de superposición de vídeo, esta región tendrá deshabilitada la adquisición de vídeo.</span><span class="sxs-lookup"><span data-stu-id="78aaa-134">For video-overlay devices, this region will have video acquisition disabled.</span></span> <span data-ttu-id="78aaa-135">En el caso de los dispositivos de vídeo digital, los píxeles del rectángulo tendrán el bit de máscara de bloqueo activado (a menos que se especifique la marca "exterior").</span><span class="sxs-lookup"><span data-stu-id="78aaa-135">For digital-video devices, the pixels within the rectangle will have their lock mask bit turned on (unless the "outside" flag is specified).</span></span> <span data-ttu-id="78aaa-136">El rectángulo es relativo al origen del búfer de vídeo y se especifica como *x1 Y1 x2 Y2*.</span><span class="sxs-lookup"><span data-stu-id="78aaa-136">The rectangle is relative to the video buffer origin and is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="78aaa-137">Las coordenadas *x1 Y1* especifican la esquina superior izquierda del rectángulo y las coordenadas *x2 Y2* especifican el ancho y el alto.</span><span class="sxs-lookup"><span data-stu-id="78aaa-137">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span> |
| <span data-ttu-id="78aaa-138">campo</span><span class="sxs-lookup"><span data-stu-id="78aaa-138">field</span></span>          | <span data-ttu-id="78aaa-139">Inmoviliza el primer campo.</span><span class="sxs-lookup"><span data-stu-id="78aaa-139">Freezes the first field.</span></span> <span data-ttu-id="78aaa-140">El campo se supone de forma predeterminada (si no se especifica ningún marco ni campo).</span><span class="sxs-lookup"><span data-stu-id="78aaa-140">Field is assumed by default (if neither frame nor field is specified).</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="78aaa-141">frame</span><span class="sxs-lookup"><span data-stu-id="78aaa-141">frame</span></span>          | <span data-ttu-id="78aaa-142">Inmoviliza todo el marco, mostrando ambos campos.</span><span class="sxs-lookup"><span data-stu-id="78aaa-142">Freezes the entire frame, displaying both fields.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="78aaa-143">input</span><span class="sxs-lookup"><span data-stu-id="78aaa-143">input</span></span>          | <span data-ttu-id="78aaa-144">Inmoviliza el marco actual de la imagen de entrada, si está en pausa o en ejecución.</span><span class="sxs-lookup"><span data-stu-id="78aaa-144">Freezes the current frame of the input image, whether it is paused or running.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="78aaa-145">output</span><span class="sxs-lookup"><span data-stu-id="78aaa-145">output</span></span>         | <span data-ttu-id="78aaa-146">Inmoviliza el marco actual de la salida del VCR.</span><span class="sxs-lookup"><span data-stu-id="78aaa-146">Freezes the current frame of the output from the VCR.</span></span> <span data-ttu-id="78aaa-147">Si el VCR se está reproduciendo cuando se emite la inmovilización, el fotograma actual se congela y el VCR está en pausa.</span><span class="sxs-lookup"><span data-stu-id="78aaa-147">If the VCR is playing when freeze is issued, the current frame is frozen and the VCR is paused.</span></span> <span data-ttu-id="78aaa-148">Si el VCR está en pausa cuando se emite este comando, se inmoviliza el marco actual.</span><span class="sxs-lookup"><span data-stu-id="78aaa-148">If the VCR is paused when this command is issued, the current frame is frozen.</span></span> <span data-ttu-id="78aaa-149">La imagen inmovilizada permanece en el dispositivo de salida hasta que se emite un comando [unfreeze](unfreeze.md) .</span><span class="sxs-lookup"><span data-stu-id="78aaa-149">The frozen image remains on the output device until an [unfreeze](unfreeze.md) command is issued.</span></span> <span data-ttu-id="78aaa-150">Si no se especifica "Input" ni "Output", se asume "Output".</span><span class="sxs-lookup"><span data-stu-id="78aaa-150">If neither "input" nor "output" is specified, "output" is assumed.</span></span>                                                                                    |
| <span data-ttu-id="78aaa-151">ajena</span><span class="sxs-lookup"><span data-stu-id="78aaa-151">outside</span></span>        | <span data-ttu-id="78aaa-152">Indica que el área fuera de la región especificada mediante la marca "at" está inmovilizada.</span><span class="sxs-lookup"><span data-stu-id="78aaa-152">Indicates that the area outside the region specified using the "at" flag is frozen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="78aaa-153"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="78aaa-153"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="78aaa-154">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="78aaa-154">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="78aaa-155">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="78aaa-155">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="78aaa-156">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="78aaa-156">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78aaa-157">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78aaa-157">Return Value</span></span>

<span data-ttu-id="78aaa-158">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="78aaa-158">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="78aaa-159">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78aaa-159">Remarks</span></span>

<span data-ttu-id="78aaa-160">Cuando se usa con dispositivos VCR, este comando está pensado para tarjetas que capturan fotogramas.</span><span class="sxs-lookup"><span data-stu-id="78aaa-160">When used with VCR devices, this command is intended for frame-grabbing cards.</span></span>

<span data-ttu-id="78aaa-161">Para especificar regiones de adquisición irregulares con la marca "at", use una serie de comandos Freeze y [unfreeze](unfreeze.md) .</span><span class="sxs-lookup"><span data-stu-id="78aaa-161">To specify irregular acquisition regions with the "at" flag, use a series of freeze and [unfreeze](unfreeze.md) commands.</span></span> <span data-ttu-id="78aaa-162">Algunos dispositivos de superposición de vídeo limitan la complejidad de la región de adquisición.</span><span class="sxs-lookup"><span data-stu-id="78aaa-162">Some video-overlay devices limit the complexity of the acquisition region.</span></span>

<span data-ttu-id="78aaa-163">Este comando solo se admite si una llamada al comando [Capability](capability.md) con la marca "puede inmovilizar" devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="78aaa-163">This command is supported only if a call to the [capability](capability.md) command with the "can freeze" flag returns **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="78aaa-164">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="78aaa-164">Examples</span></span>

<span data-ttu-id="78aaa-165">El siguiente comando deshabilita la adquisición de vídeo en un cuadrado de 100 píxeles en la esquina superior izquierda del búfer de vídeo.</span><span class="sxs-lookup"><span data-stu-id="78aaa-165">The following command disables video acquisition in a 100-pixel square at the upper left corner of the video buffer.</span></span>

``` syntax
freeze vboard at 0 0 100 100
```

## <a name="requirements"></a><span data-ttu-id="78aaa-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78aaa-166">Requirements</span></span>



| <span data-ttu-id="78aaa-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="78aaa-167">Requirement</span></span> | <span data-ttu-id="78aaa-168">Value</span><span class="sxs-lookup"><span data-stu-id="78aaa-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="78aaa-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78aaa-169">Minimum supported client</span></span><br/> | <span data-ttu-id="78aaa-170">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="78aaa-170">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="78aaa-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78aaa-171">Minimum supported server</span></span><br/> | <span data-ttu-id="78aaa-172">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="78aaa-172">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="78aaa-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="78aaa-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78aaa-174">MCI</span><span class="sxs-lookup"><span data-stu-id="78aaa-174">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="78aaa-175">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="78aaa-175">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="78aaa-176">capability</span><span class="sxs-lookup"><span data-stu-id="78aaa-176">capability</span></span>](capability.md)
</dt> <dt>

[<span data-ttu-id="78aaa-177">liberar</span><span class="sxs-lookup"><span data-stu-id="78aaa-177">unfreeze</span></span>](unfreeze.md)
</dt> </dl>

 

