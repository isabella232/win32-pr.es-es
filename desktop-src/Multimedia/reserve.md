---
title: Reserve (comando)
description: El comando Reserve asigna espacio en disco contiguo para el área de trabajo de la instancia del dispositivo. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: ac4fc75e-82d0-4817-a5cf-a77996bc69e2
keywords:
- comando Reserve de Windows multimedia
topic_type:
- apiref
api_name:
- reserve
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f71889af552b9040777394047a0facfc6c81366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995955"
---
# <a name="reserve-command"></a><span data-ttu-id="0ff5d-105">Reserve (comando)</span><span class="sxs-lookup"><span data-stu-id="0ff5d-105">reserve command</span></span>

<span data-ttu-id="0ff5d-106">El comando Reserve asigna espacio en disco contiguo para el área de trabajo de la instancia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-106">The reserve command allocates contiguous disk space for the device instance's workspace.</span></span> <span data-ttu-id="0ff5d-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="0ff5d-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("reserve %s %s %s"), 
  lpszDeviceID, 
  lpszReserve, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="0ff5d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ff5d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ff5d-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="0ff5d-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0ff5d-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-111">Identifier of an MCI device.</span></span> <span data-ttu-id="0ff5d-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="0ff5d-113"><span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*</span><span class="sxs-lookup"><span data-stu-id="0ff5d-113"><span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*</span></span>
</dt> <dd>

<span data-ttu-id="0ff5d-114">Una o varias de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-114">One or more of the following flags.</span></span>



| <span data-ttu-id="0ff5d-115">Value</span><span class="sxs-lookup"><span data-stu-id="0ff5d-115">Value</span></span>           | <span data-ttu-id="0ff5d-116">Significado</span><span class="sxs-lookup"><span data-stu-id="0ff5d-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ff5d-117">en *ruta de acceso*</span><span class="sxs-lookup"><span data-stu-id="0ff5d-117">in *path*</span></span>       | <span data-ttu-id="0ff5d-118">Especifica la unidad y la ruta de acceso del directorio (pero no el nombre) de un archivo temporal que se usa para almacenar los datos registrados.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-118">Specifies the drive and directory path (but not the name) of a temporary file used to hold recorded data.</span></span> <span data-ttu-id="0ff5d-119">El dispositivo especifica el nombre de este archivo.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-119">The name of this file is specified by the device.</span></span> <span data-ttu-id="0ff5d-120">El archivo temporal se elimina cuando se cierra el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-120">The temporary file is deleted when the device is closed.</span></span> <span data-ttu-id="0ff5d-121">Si se omite esta marca, el dispositivo especifica la ubicación del espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-121">If this flag is omitted, the device specifies the location of the disk space.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="0ff5d-122">*duración* del tamaño</span><span class="sxs-lookup"><span data-stu-id="0ff5d-122">size *duration*</span></span> | <span data-ttu-id="0ff5d-123">Especifica la cantidad aproximada de espacio en disco que se va a reservar en el área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-123">Specifies the approximate amount of disk space to reserve in the workspace.</span></span> <span data-ttu-id="0ff5d-124">El valor *Duration* se especifica en el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-124">The *duration* value is specified in the current time format.</span></span> <span data-ttu-id="0ff5d-125">El dispositivo basa su estimación del espacio en disco necesario en los parámetros siguientes: la hora solicitada, el formato de archivo, el algoritmo de compresión de audio y vídeo, y los valores de calidad de compresión en vigor.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-125">The device bases its estimate of the required disk space on the following parameters: the requested time, the file format, the video and audio compression algorithm, and the compression quality values in effect.</span></span> <span data-ttu-id="0ff5d-126">Si [setvideo](setvideo.md) "registro" es "desactivado", el espacio solo se reserva para el audio.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-126">If [setvideo](setvideo.md) "record" is "off", then space is reserved only for audio.</span></span> <span data-ttu-id="0ff5d-127">Si [SetAudio](setaudio.md) "registro" es "desactivado", el espacio solo se reserva para vídeo.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-127">If [setaudio](setaudio.md) "record" is "off", then space is reserved only for video.</span></span> <span data-ttu-id="0ff5d-128">Si ambos son "OFF", o si *Duration* es cero, no se reserva ningún espacio y se cancela la asignación de cualquier espacio reservado existente.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-128">If both are "off", or if *duration* is zero, then no space is reserved and any existing reserved space is deallocated.</span></span> <span data-ttu-id="0ff5d-129">Si se omite esta marca, el dispositivo usará un valor predeterminado definido por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-129">If this flag is omitted, the device will use a device-defined default.</span></span> |



 

</dd> <dt>

<span data-ttu-id="0ff5d-130"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="0ff5d-130"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0ff5d-131">Puede ser "Wait", "Notify", "Test" o una combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-131">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="0ff5d-132">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0ff5d-132">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ff5d-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ff5d-133">Return Value</span></span>

<span data-ttu-id="0ff5d-134">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-134">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ff5d-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ff5d-135">Remarks</span></span>

<span data-ttu-id="0ff5d-136">Si es necesario, los comandos [registro](record.md) o [Guardar](save.md) subsiguientes usan el espacio reservado por este comando.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-136">If needed, subsequent [record](record.md) or [save](save.md) commands use the space reserved by this command.</span></span> <span data-ttu-id="0ff5d-137">Si el área de trabajo contiene datos no guardados, se perderán los datos.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-137">If the workspace contains unsaved data, the data is lost.</span></span> <span data-ttu-id="0ff5d-138">Algunos dispositivos no requieren reserva y lo omiten.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-138">Some devices do not require reserve and ignore it.</span></span> <span data-ttu-id="0ff5d-139">Si no se reserva espacio en disco antes de la grabación, el comando de registro realiza una reserva implícita con las marcas predeterminadas específicas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-139">If disk space is not reserved prior to recording, the record command performs an implied reserve with device-specific default flags.</span></span> <span data-ttu-id="0ff5d-140">Use un comando de reserva explícito si desea tener un mayor control sobre cuándo se produce el retraso de la asignación de disco, el control de cuánto espacio se asigna y el control de dónde se asigna el espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-140">Use an explicit reserve command if you want better control of when the delay for disk allocation occurs, control of how much space is allocated, and control of where the disk space is allocated.</span></span> <span data-ttu-id="0ff5d-141">La aplicación puede cambiar la cantidad y la ubicación del espacio en disco reservado previamente con comandos de reserva posteriores.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-141">Your application can change the amount and location of previously reserved disk space with subsequent reserve commands.</span></span> <span data-ttu-id="0ff5d-142">Cualquier espacio en disco asignado y todavía sin usar no se cancela hasta que se guardan los datos grabados, o hasta que se cierra la instancia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ff5d-142">Any allocated and still unused disk space is not deallocated until any recorded data is saved, or until the device instance is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ff5d-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ff5d-143">Requirements</span></span>



| <span data-ttu-id="0ff5d-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ff5d-144">Requirement</span></span> | <span data-ttu-id="0ff5d-145">Value</span><span class="sxs-lookup"><span data-stu-id="0ff5d-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0ff5d-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ff5d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0ff5d-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0ff5d-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0ff5d-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ff5d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0ff5d-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0ff5d-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0ff5d-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ff5d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff5d-151">MCI</span><span class="sxs-lookup"><span data-stu-id="0ff5d-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0ff5d-152">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="0ff5d-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="0ff5d-153">record</span><span class="sxs-lookup"><span data-stu-id="0ff5d-153">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="0ff5d-154">guardar</span><span class="sxs-lookup"><span data-stu-id="0ff5d-154">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="0ff5d-155">setaudio</span><span class="sxs-lookup"><span data-stu-id="0ff5d-155">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="0ff5d-156">setvideo</span><span class="sxs-lookup"><span data-stu-id="0ff5d-156">setvideo</span></span>](setvideo.md)
</dt> </dl>

 

