---
title: pegar (comando)
description: El comando pegar copia el contenido del portapapeles en el área de trabajo. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: c09418e1-2535-40d1-8912-e5ece91ee673
keywords:
- pegar comandos de Windows multimedia
topic_type:
- apiref
api_name:
- paste
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482fd744d7e6e163059330148b6e3f081d435880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079058"
---
# <a name="paste-command"></a><span data-ttu-id="3618c-105">pegar (comando)</span><span class="sxs-lookup"><span data-stu-id="3618c-105">paste command</span></span>

<span data-ttu-id="3618c-106">El comando pegar copia el contenido del portapapeles en el área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="3618c-106">The paste command copies the contents of the clipboard into the workspace.</span></span> <span data-ttu-id="3618c-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="3618c-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="3618c-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="3618c-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("paste %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="3618c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3618c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3618c-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="3618c-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="3618c-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="3618c-111">Identifier of an MCI device.</span></span> <span data-ttu-id="3618c-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3618c-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="3618c-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span><span class="sxs-lookup"><span data-stu-id="3618c-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="3618c-114">Una o varias de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="3618c-114">One or more of the following flags.</span></span>



| <span data-ttu-id="3618c-115">Value</span><span class="sxs-lookup"><span data-stu-id="3618c-115">Value</span></span>                 | <span data-ttu-id="3618c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="3618c-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3618c-117">en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="3618c-117">at *rectangle*</span></span>        | <span data-ttu-id="3618c-118">Especifica la ubicación dentro del marco donde se pegan los datos.</span><span class="sxs-lookup"><span data-stu-id="3618c-118">Specifies the location within the frame where the data is pasted.</span></span> <span data-ttu-id="3618c-119">La esquina superior izquierda del *rectángulo* corresponde a la esquina superior izquierda de los datos agregados.</span><span class="sxs-lookup"><span data-stu-id="3618c-119">The upper left corner of the *rectangle* corresponds to the upper left corner of the added data.</span></span> <span data-ttu-id="3618c-120">Si el rectángulo tiene un tamaño distinto de cero en X o Y, el contenido del portapapeles se escala en esas dimensiones cuando se pegan en el marco.</span><span class="sxs-lookup"><span data-stu-id="3618c-120">If the rectangle has a nonzero size in X or Y, the contents of the clipboard are scaled in those dimensions when they are pasted into the frame.</span></span> <span data-ttu-id="3618c-121">Si se omite, el *rectángulo* tiene como valor predeterminado el marco completo.</span><span class="sxs-lookup"><span data-stu-id="3618c-121">If omitted, the *rectangle* defaults to the entire frame.</span></span> <span data-ttu-id="3618c-122">Si esta marca se especifica en el modo "Insertar" (valor predeterminado), cualquier región fuera del rectángulo se dibuja como un color sólido.</span><span class="sxs-lookup"><span data-stu-id="3618c-122">If this flag is specified in "insert" mode (the default), any region outside the rectangle is painted a solid color.</span></span>                       |
| <span data-ttu-id="3618c-123">*secuencia* de flujo de audio</span><span class="sxs-lookup"><span data-stu-id="3618c-123">audio stream *stream*</span></span> | <span data-ttu-id="3618c-124">Especifica la secuencia de audio en el área de trabajo afectada por el comando.</span><span class="sxs-lookup"><span data-stu-id="3618c-124">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="3618c-125">Si solo existe una secuencia de audio en el portapapeles, los datos de audio se pegan en la *secuencia* designada.</span><span class="sxs-lookup"><span data-stu-id="3618c-125">If only one audio stream exists on the clipboard, the audio data is pasted into the designated *stream*.</span></span> <span data-ttu-id="3618c-126">Si existe más de una secuencia de audio en el portapapeles, la *secuencia* indica el número de inicio de las secuencias de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="3618c-126">If more than one audio stream exists on the clipboard, the *stream* indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="3618c-127">Si usa esta marca y también quiere pegar vídeo, también debe usar la marca "secuencia de vídeo".</span><span class="sxs-lookup"><span data-stu-id="3618c-127">If you use this flag and also want to paste video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="3618c-128">(Si no se especifica ninguna marca, se pegan todas las secuencias de audio y vídeo y se conservan los números de secuencia originales).</span><span class="sxs-lookup"><span data-stu-id="3618c-128">(If neither flag is specified, all audio and video streams are pasted and retain their original stream numbers.)</span></span> |
| <span data-ttu-id="3618c-129">insert</span><span class="sxs-lookup"><span data-stu-id="3618c-129">insert</span></span>                | <span data-ttu-id="3618c-130">Especifica que los datos se insertan en el área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="3618c-130">Specifies that the data is inserted into the workspace.</span></span> <span data-ttu-id="3618c-131">Los datos después del punto de inserción se mueven hacia delante en el área de trabajo para dejar espacio.</span><span class="sxs-lookup"><span data-stu-id="3618c-131">Any data after the insertion point is moved forward in the workspace to make room.</span></span> <span data-ttu-id="3618c-132">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3618c-132">This is the default value.</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3618c-133">sobrescribir</span><span class="sxs-lookup"><span data-stu-id="3618c-133">overwrite</span></span>             | <span data-ttu-id="3618c-134">Especifica que los datos se copian en el área de trabajo escribiendo los datos existentes después del punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="3618c-134">Specifies that the data is copied into the workspace by writing over any existing data after the insertion point.</span></span> <span data-ttu-id="3618c-135">Las marcas "Insertar" y "Sobrescribir" afectan a si los marcos se destruyen o se mueven durante la operación de pegar, no al modo en que los datos se pegan dentro de cada marco.</span><span class="sxs-lookup"><span data-stu-id="3618c-135">The "insert" and "overwrite" flags affect whether frames are destroyed or moved during the paste operation, not how the data is pasted within each frame.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="3618c-136">para *colocar*</span><span class="sxs-lookup"><span data-stu-id="3618c-136">to *position*</span></span>         | <span data-ttu-id="3618c-137">Especifica la posición en el área de trabajo en la que se pegan los datos.</span><span class="sxs-lookup"><span data-stu-id="3618c-137">Specifies the position in the workspace at which the data is pasted.</span></span> <span data-ttu-id="3618c-138">Si se omite, el valor predeterminado es la posición actual.</span><span class="sxs-lookup"><span data-stu-id="3618c-138">If omitted, it defaults to the current position.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3618c-139">*secuencia* de flujo de vídeo</span><span class="sxs-lookup"><span data-stu-id="3618c-139">video stream *stream*</span></span> | <span data-ttu-id="3618c-140">Especifica la secuencia de vídeo en el área de trabajo afectada por el comando.</span><span class="sxs-lookup"><span data-stu-id="3618c-140">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="3618c-141">Si solo existe una secuencia de vídeo en el portapapeles, los datos de vídeo se pegan en la *secuencia* designada.</span><span class="sxs-lookup"><span data-stu-id="3618c-141">If only one video stream exists on the clipboard, the video data is pasted into the designated *stream*.</span></span> <span data-ttu-id="3618c-142">Si existe más de una secuencia de vídeo en el portapapeles, la *secuencia* indica el número de inicio de las secuencias de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="3618c-142">If more than one video stream exists on the clipboard, the *stream* indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="3618c-143">Si usa esta marca y también desea pegar audio, también debe usar la marca de "secuencia de audio".</span><span class="sxs-lookup"><span data-stu-id="3618c-143">If you use this flag and also want to paste audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="3618c-144">(Si no se especifica ninguna marca, se pegan todas las secuencias de audio y vídeo y se conservan los números de secuencia originales).</span><span class="sxs-lookup"><span data-stu-id="3618c-144">(If neither flag is specified, all audio and video streams are pasted and retain their original stream numbers.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="3618c-145"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="3618c-145"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3618c-146">Puede ser "Wait", "Notify", "Test" o una combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="3618c-146">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="3618c-147">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="3618c-147">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3618c-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3618c-148">Return Value</span></span>

<span data-ttu-id="3618c-149">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3618c-149">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3618c-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3618c-150">Remarks</span></span>

<span data-ttu-id="3618c-151">No hay señales en los datos copiados desde el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="3618c-151">No signals are present in the data copied from the clipboard.</span></span> <span data-ttu-id="3618c-152">El cambio solo se convierte en permanente cuando se guardan los datos explícitamente; sin embargo, la reproducción actúa como si se agregaran los datos.</span><span class="sxs-lookup"><span data-stu-id="3618c-152">The change becomes permanent only when the data is explicitly saved; however, playback acts as if the data has been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="3618c-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3618c-153">Requirements</span></span>



| <span data-ttu-id="3618c-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="3618c-154">Requirement</span></span> | <span data-ttu-id="3618c-155">Value</span><span class="sxs-lookup"><span data-stu-id="3618c-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3618c-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3618c-156">Minimum supported client</span></span><br/> | <span data-ttu-id="3618c-157">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3618c-157">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3618c-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3618c-158">Minimum supported server</span></span><br/> | <span data-ttu-id="3618c-159">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3618c-159">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3618c-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="3618c-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3618c-161">MCI</span><span class="sxs-lookup"><span data-stu-id="3618c-161">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3618c-162">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="3618c-162">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

