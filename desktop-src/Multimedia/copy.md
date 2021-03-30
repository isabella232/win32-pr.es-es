---
title: copiar comando
description: El comando copiar copia los datos en el portapapeles. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- copiar comando de Windows multimedia
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f08c764cb12b1cdca4c1876e6a22220a5c7522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801525"
---
# <a name="copy-command"></a><span data-ttu-id="78ccd-105">copiar comando</span><span class="sxs-lookup"><span data-stu-id="78ccd-105">copy command</span></span>

<span data-ttu-id="78ccd-106">El comando copiar copia los datos en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="78ccd-106">The copy command copies data to the clipboard.</span></span> <span data-ttu-id="78ccd-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="78ccd-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="78ccd-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="78ccd-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("copy %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="78ccd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78ccd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78ccd-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="78ccd-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="78ccd-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="78ccd-111">Identifier of an MCI device.</span></span> <span data-ttu-id="78ccd-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78ccd-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="78ccd-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span><span class="sxs-lookup"><span data-stu-id="78ccd-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="78ccd-114">Una de las marcas siguientes que identifican el elemento que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="78ccd-114">One of the following flags identifying the item to copy.</span></span>



| <span data-ttu-id="78ccd-115">Value</span><span class="sxs-lookup"><span data-stu-id="78ccd-115">Value</span></span>                 | <span data-ttu-id="78ccd-116">Significado</span><span class="sxs-lookup"><span data-stu-id="78ccd-116">Meaning</span></span>                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78ccd-117">en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="78ccd-117">at *rectangle*</span></span>        | <span data-ttu-id="78ccd-118">Especifica la parte de cada fotograma que se copiará.</span><span class="sxs-lookup"><span data-stu-id="78ccd-118">Specifies the portion of each frame that will be copied.</span></span> <span data-ttu-id="78ccd-119">Si se omite, el valor predeterminado es todo el marco.</span><span class="sxs-lookup"><span data-stu-id="78ccd-119">If omitted, the default setting is the entire frame.</span></span>                                                                                                                             |
| <span data-ttu-id="78ccd-120">*secuencia* de flujo de audio</span><span class="sxs-lookup"><span data-stu-id="78ccd-120">audio stream *stream*</span></span> | <span data-ttu-id="78ccd-121">Especifica la secuencia de audio en el área de trabajo afectada por el comando.</span><span class="sxs-lookup"><span data-stu-id="78ccd-121">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="78ccd-122">Si usa esta marca y también quiere copiar vídeo, también debe usar la marca "secuencia de vídeo".</span><span class="sxs-lookup"><span data-stu-id="78ccd-122">If you use this flag and also want to copy video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="78ccd-123">(Si no se especifica ninguna marca, se copian todas las secuencias de audio y vídeo).</span><span class="sxs-lookup"><span data-stu-id="78ccd-123">(If neither flag is specified, all audio and video streams are copied.)</span></span> |
| <span data-ttu-id="78ccd-124">desde la *posición*</span><span class="sxs-lookup"><span data-stu-id="78ccd-124">from *position*</span></span>       | <span data-ttu-id="78ccd-125">Especifica el inicio del intervalo copiado.</span><span class="sxs-lookup"><span data-stu-id="78ccd-125">Specifies the start of the range copied.</span></span> <span data-ttu-id="78ccd-126">Si se omite, el valor predeterminado es la posición actual.</span><span class="sxs-lookup"><span data-stu-id="78ccd-126">If omitted, the default setting is the current position.</span></span>                                                                                                                                         |
| <span data-ttu-id="78ccd-127">para *colocar*</span><span class="sxs-lookup"><span data-stu-id="78ccd-127">to *position*</span></span>         | <span data-ttu-id="78ccd-128">Especifica el final del intervalo copiado.</span><span class="sxs-lookup"><span data-stu-id="78ccd-128">Specifies the end of the range copied.</span></span> <span data-ttu-id="78ccd-129">Los datos de audio y vídeo copiados son exclusivos de esta posición.</span><span class="sxs-lookup"><span data-stu-id="78ccd-129">The audio and video data copied are exclusive of this position.</span></span> <span data-ttu-id="78ccd-130">Si se omite, el valor predeterminado es el final del área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="78ccd-130">If omitted, the default setting is the end of the workspace.</span></span>                                                                       |
| <span data-ttu-id="78ccd-131">*secuencia* de flujo de vídeo</span><span class="sxs-lookup"><span data-stu-id="78ccd-131">video stream *stream*</span></span> | <span data-ttu-id="78ccd-132">Especifica la secuencia de vídeo en el área de trabajo afectada por el comando.</span><span class="sxs-lookup"><span data-stu-id="78ccd-132">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="78ccd-133">Si usa esta marca y también quiere copiar audio, también debe usar la marca de "secuencia de audio".</span><span class="sxs-lookup"><span data-stu-id="78ccd-133">If you use this flag and also want to copy audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="78ccd-134">(Si no se especifica ninguna marca, se copian todas las secuencias de audio y vídeo).</span><span class="sxs-lookup"><span data-stu-id="78ccd-134">(If neither flag is specified, all audio and video streams are copied.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="78ccd-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="78ccd-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="78ccd-136">Puede ser "Wait", "Notify", "Test" o una combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="78ccd-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="78ccd-137">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="78ccd-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78ccd-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78ccd-138">Return Value</span></span>

<span data-ttu-id="78ccd-139">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="78ccd-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="78ccd-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78ccd-140">Requirements</span></span>



| <span data-ttu-id="78ccd-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="78ccd-141">Requirement</span></span> | <span data-ttu-id="78ccd-142">Value</span><span class="sxs-lookup"><span data-stu-id="78ccd-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="78ccd-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78ccd-143">Minimum supported client</span></span><br/> | <span data-ttu-id="78ccd-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="78ccd-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="78ccd-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78ccd-145">Minimum supported server</span></span><br/> | <span data-ttu-id="78ccd-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="78ccd-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="78ccd-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="78ccd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78ccd-148">MCI</span><span class="sxs-lookup"><span data-stu-id="78ccd-148">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="78ccd-149">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="78ccd-149">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

