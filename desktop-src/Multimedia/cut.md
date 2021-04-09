---
title: cortar (comando)
description: El comando CUT quita los datos del área de trabajo y los copia en el portapapeles. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: f42c7364-49cb-41be-b601-bda6e97d1e76
keywords:
- cortar comando de Windows multimedia
topic_type:
- apiref
api_name:
- cut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33571309e1dd249f20e577c97b8c6e1b950eda09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996899"
---
# <a name="cut-command"></a><span data-ttu-id="e04be-105">cortar (comando)</span><span class="sxs-lookup"><span data-stu-id="e04be-105">cut command</span></span>

<span data-ttu-id="e04be-106">El comando CUT quita los datos del área de trabajo y los copia en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="e04be-106">The cut command removes data from the workspace and copies it to the clipboard.</span></span> <span data-ttu-id="e04be-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="e04be-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="e04be-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="e04be-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cut %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="e04be-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e04be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e04be-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="e04be-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e04be-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="e04be-111">Identifier of an MCI device.</span></span> <span data-ttu-id="e04be-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e04be-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="e04be-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span><span class="sxs-lookup"><span data-stu-id="e04be-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="e04be-114">Una de las marcas siguientes que identifican el elemento que se va a cortar.</span><span class="sxs-lookup"><span data-stu-id="e04be-114">One of the following flags identifying the item to cut.</span></span>



| <span data-ttu-id="e04be-115">Value</span><span class="sxs-lookup"><span data-stu-id="e04be-115">Value</span></span>                 | <span data-ttu-id="e04be-116">Significado</span><span class="sxs-lookup"><span data-stu-id="e04be-116">Meaning</span></span>                                                                                                                                                                                                                               |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e04be-117">en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="e04be-117">at *rectangle*</span></span>        | <span data-ttu-id="e04be-118">Especifica la parte de cada corte del marco.</span><span class="sxs-lookup"><span data-stu-id="e04be-118">Specifies the portion of each frame cut.</span></span> <span data-ttu-id="e04be-119">Si se omite, el valor predeterminado es todo el marco.</span><span class="sxs-lookup"><span data-stu-id="e04be-119">If omitted, it defaults to the entire frame.</span></span> <span data-ttu-id="e04be-120">Cuando se especifica este elemento, no se eliminan los marcos.</span><span class="sxs-lookup"><span data-stu-id="e04be-120">When this item is specified, frames are not deleted.</span></span> <span data-ttu-id="e04be-121">En su lugar, el área dentro del rectángulo se vuelve negra.</span><span class="sxs-lookup"><span data-stu-id="e04be-121">Instead the area inside the rectangle becomes black.</span></span>                                       |
| <span data-ttu-id="e04be-122">*secuencia* de flujo de audio</span><span class="sxs-lookup"><span data-stu-id="e04be-122">audio stream *stream*</span></span> | <span data-ttu-id="e04be-123">Especifica la secuencia de audio en el área de trabajo afectada por el comando.</span><span class="sxs-lookup"><span data-stu-id="e04be-123">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="e04be-124">Si usa esta marca y también desea cortar vídeo, también debe usar la marca "secuencia de vídeo".</span><span class="sxs-lookup"><span data-stu-id="e04be-124">If you use this flag and also want to cut video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="e04be-125">(Si no se especifica ninguna marca, se cortan todas las secuencias de audio y vídeo).</span><span class="sxs-lookup"><span data-stu-id="e04be-125">(If neither flag is specified, all audio and video streams are cut.)</span></span> |
| <span data-ttu-id="e04be-126">desde la *posición*</span><span class="sxs-lookup"><span data-stu-id="e04be-126">from *position*</span></span>       | <span data-ttu-id="e04be-127">Especifica el inicio del corte del intervalo.</span><span class="sxs-lookup"><span data-stu-id="e04be-127">Specifies the start of the range cut.</span></span> <span data-ttu-id="e04be-128">Si se omite, el valor predeterminado es la posición actual.</span><span class="sxs-lookup"><span data-stu-id="e04be-128">If omitted, it defaults to the current position.</span></span>                                                                                                                                                |
| <span data-ttu-id="e04be-129">para *colocar*</span><span class="sxs-lookup"><span data-stu-id="e04be-129">to *position*</span></span>         | <span data-ttu-id="e04be-130">Especifica el final del corte del intervalo.</span><span class="sxs-lookup"><span data-stu-id="e04be-130">Specifies the end of the range cut.</span></span> <span data-ttu-id="e04be-131">El corte de datos de audio y vídeo es exclusivo de esta posición.</span><span class="sxs-lookup"><span data-stu-id="e04be-131">The audio and video data cut are exclusive of this position.</span></span> <span data-ttu-id="e04be-132">Si se omite, el valor predeterminado es el final del área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e04be-132">If omitted it defaults to the end of the workspace.</span></span>                                                                                  |
| <span data-ttu-id="e04be-133">*secuencia* de flujo de vídeo</span><span class="sxs-lookup"><span data-stu-id="e04be-133">video stream *stream*</span></span> | <span data-ttu-id="e04be-134">Especifica la secuencia de vídeo en el área de trabajo afectada por el comando.</span><span class="sxs-lookup"><span data-stu-id="e04be-134">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="e04be-135">Si usa esta marca y también desea cortar audio, también debe usar la marca de "secuencia de audio".</span><span class="sxs-lookup"><span data-stu-id="e04be-135">If you use this flag and also want to cut audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="e04be-136">(Si no se especifica ninguna marca, se cortan todas las secuencias de audio y vídeo).</span><span class="sxs-lookup"><span data-stu-id="e04be-136">(If neither flag is specified, all audio and video streams are cut.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="e04be-137"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="e04be-137"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e04be-138">Puede ser "Wait", "Notify", "Test" o una combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="e04be-138">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="e04be-139">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e04be-139">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e04be-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e04be-140">Return Value</span></span>

<span data-ttu-id="e04be-141">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e04be-141">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e04be-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e04be-142">Remarks</span></span>

<span data-ttu-id="e04be-143">El cambio solo se convierte en permanente cuando se guardan los datos explícitamente; sin embargo, la reproducción actúa como si se hubieran quitado los datos.</span><span class="sxs-lookup"><span data-stu-id="e04be-143">The change becomes permanent only when the data is explicitly saved; however, playback acts as if the data has been removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e04be-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e04be-144">Requirements</span></span>



| <span data-ttu-id="e04be-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="e04be-145">Requirement</span></span> | <span data-ttu-id="e04be-146">Value</span><span class="sxs-lookup"><span data-stu-id="e04be-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e04be-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e04be-147">Minimum supported client</span></span><br/> | <span data-ttu-id="e04be-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e04be-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e04be-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e04be-149">Minimum supported server</span></span><br/> | <span data-ttu-id="e04be-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e04be-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e04be-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="e04be-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e04be-152">MCI</span><span class="sxs-lookup"><span data-stu-id="e04be-152">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e04be-153">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="e04be-153">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

