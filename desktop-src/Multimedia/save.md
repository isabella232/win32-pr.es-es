---
title: guardar (comando)
description: El comando Guardar guarda un archivo MCI. Los dispositivos de audio y la superposición de vídeo y de onda reconocen este comando. Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo admiten.
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- comando guardar de Windows multimedia
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0029ad03c1b7fe855e8485b2719b11628fac1103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676569"
---
# <a name="save-command"></a><span data-ttu-id="4802c-106">guardar (comando)</span><span class="sxs-lookup"><span data-stu-id="4802c-106">save command</span></span>

<span data-ttu-id="4802c-107">El comando Guardar guarda un archivo MCI.</span><span class="sxs-lookup"><span data-stu-id="4802c-107">The save command saves an MCI file.</span></span> <span data-ttu-id="4802c-108">Los dispositivos de audio y la superposición de vídeo y de onda reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="4802c-108">Video-overlay and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="4802c-109">Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo admiten.</span><span class="sxs-lookup"><span data-stu-id="4802c-109">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not support it.</span></span>

<span data-ttu-id="4802c-110">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="4802c-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("save %s %s %s"), 
  lpszDeviceID, 
  lpszFilename, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="4802c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4802c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4802c-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="4802c-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4802c-113">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="4802c-113">Identifier of an MCI device.</span></span> <span data-ttu-id="4802c-114">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4802c-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="4802c-115"><span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*</span><span class="sxs-lookup"><span data-stu-id="4802c-115"><span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*</span></span>
</dt> <dd>

<span data-ttu-id="4802c-116">Marca que especifica el nombre del archivo que se va a guardar y, opcionalmente, marcas adicionales que modifican la operación de guardar.</span><span class="sxs-lookup"><span data-stu-id="4802c-116">Flag specifying the name of the file being saved and, optionally, additional flags modifying the save operation.</span></span> <span data-ttu-id="4802c-117">En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **Save** y las marcas usadas por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="4802c-117">The following table lists device types that recognize the **save** command and the flags used by each type.</span></span>



| <span data-ttu-id="4802c-118">Value</span><span class="sxs-lookup"><span data-stu-id="4802c-118">Value</span></span>        | <span data-ttu-id="4802c-119">Significado</span><span class="sxs-lookup"><span data-stu-id="4802c-119">Meaning</span></span>              | <span data-ttu-id="4802c-120">Significado</span><span class="sxs-lookup"><span data-stu-id="4802c-120">Meaning</span></span>               |
|--------------|----------------------|-----------------------|
| <span data-ttu-id="4802c-121">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="4802c-121">digitalvideo</span></span> | <span data-ttu-id="4802c-122">anular en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="4802c-122">abort at *rectangle*</span></span> | <span data-ttu-id="4802c-123">*nombre de archivo* keepreserve</span><span class="sxs-lookup"><span data-stu-id="4802c-123">*filename* keepreserve</span></span> |
| <span data-ttu-id="4802c-124">overlay</span><span class="sxs-lookup"><span data-stu-id="4802c-124">overlay</span></span>      | <span data-ttu-id="4802c-125">en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="4802c-125">at *rectangle*</span></span>       | <span data-ttu-id="4802c-126">*filename*</span><span class="sxs-lookup"><span data-stu-id="4802c-126">*filename*</span></span>            |
| <span data-ttu-id="4802c-127">sequencer</span><span class="sxs-lookup"><span data-stu-id="4802c-127">sequencer</span></span>    | <span data-ttu-id="4802c-128">*filename*</span><span class="sxs-lookup"><span data-stu-id="4802c-128">*filename*</span></span>           |                       |
| <span data-ttu-id="4802c-129">waveaudio</span><span class="sxs-lookup"><span data-stu-id="4802c-129">waveaudio</span></span>    | <span data-ttu-id="4802c-130">*filename*</span><span class="sxs-lookup"><span data-stu-id="4802c-130">*filename*</span></span>           |                       |



 

<span data-ttu-id="4802c-131">En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszFilename** y su significado.</span><span class="sxs-lookup"><span data-stu-id="4802c-131">The following table lists the flags that can be specified in the **lpszFilename** parameter and their meanings.</span></span>



| <span data-ttu-id="4802c-132">Value</span><span class="sxs-lookup"><span data-stu-id="4802c-132">Value</span></span>          | <span data-ttu-id="4802c-133">Significado</span><span class="sxs-lookup"><span data-stu-id="4802c-133">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4802c-134">anular</span><span class="sxs-lookup"><span data-stu-id="4802c-134">abort</span></span>          | <span data-ttu-id="4802c-135">Detiene una operación de **Guardar** en curso.</span><span class="sxs-lookup"><span data-stu-id="4802c-135">Stops a **save** operation in progress.</span></span> <span data-ttu-id="4802c-136">Si se utiliza, debe ser el único elemento presente.</span><span class="sxs-lookup"><span data-stu-id="4802c-136">If used, this must be the only item present.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="4802c-137">en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="4802c-137">at *rectangle*</span></span> | <span data-ttu-id="4802c-138">Especifica un rectángulo con respecto al origen de búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="4802c-138">Specifies a rectangle relative to the frame buffer origin.</span></span> <span data-ttu-id="4802c-139">El *rectángulo* se especifica como *x1 Y1 x2 Y2*.</span><span class="sxs-lookup"><span data-stu-id="4802c-139">The *rectangle* is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="4802c-140">Las coordenadas *x1 Y1* especifican la esquina superior izquierda y las coordenadas *x2 Y2* especifican el ancho y el alto. En el caso de los dispositivos de vídeo digital, el comando [Capture](capture.md) se usa para capturar el contenido del búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="4802c-140">The coordinates *X1 Y1* specify the upper left corner and the coordinates *X2 Y2* specify the width and height.For digital-video devices, the [capture](capture.md) command is used to capture the contents of the frame buffer.</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="4802c-141">*filename*</span><span class="sxs-lookup"><span data-stu-id="4802c-141">*filename*</span></span>     | <span data-ttu-id="4802c-142">Especifica el nombre de archivo que se va a asignar al archivo de datos.</span><span class="sxs-lookup"><span data-stu-id="4802c-142">Specifies the filename to assign to the data file.</span></span> <span data-ttu-id="4802c-143">Si no se especifica una ruta de acceso, el archivo se colocará en el disco y en el directorio especificado anteriormente en el comando de [reserva](reserve.md) explícito o implícito.</span><span class="sxs-lookup"><span data-stu-id="4802c-143">If a path is not specified, the file will be placed on the disk and in the directory previously specified on the explicit or implicit [reserve](reserve.md) command.</span></span> <span data-ttu-id="4802c-144">Si no se ha emitido **Reserve** , la unidad y el directorio predeterminados son los asociados a la tarea de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4802c-144">If **reserve** has not been issued, the default drive and directory are those associated with the application's task.</span></span> <span data-ttu-id="4802c-145">Si se especifica una ruta de acceso, el dispositivo podría requerir que esté en la unidad de disco especificada por la **reserva** explícita o implícita.</span><span class="sxs-lookup"><span data-stu-id="4802c-145">If a path is specified, the device might require it to be on the disk drive specified by the explicit or implicit **reserve**.</span></span> <span data-ttu-id="4802c-146">Esta marca es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="4802c-146">This flag is required.</span></span> |
| <span data-ttu-id="4802c-147">keepreserve</span><span class="sxs-lookup"><span data-stu-id="4802c-147">keepreserve</span></span>    | <span data-ttu-id="4802c-148">Especifica que no se cancela la asignación del espacio en disco no utilizado que queda del comando de **reserva** original.</span><span class="sxs-lookup"><span data-stu-id="4802c-148">Specifies that unused disk space left over from the original **reserve** command is not deallocated.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="4802c-149"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="4802c-149"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4802c-150">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="4802c-150">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="4802c-151">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="4802c-151">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="4802c-152">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4802c-152">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4802c-153">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4802c-153">Return Value</span></span>

<span data-ttu-id="4802c-154">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4802c-154">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4802c-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4802c-155">Remarks</span></span>

<span data-ttu-id="4802c-156">La variable *filename* es necesaria si el dispositivo se abrió con el identificador de dispositivo "nuevo".</span><span class="sxs-lookup"><span data-stu-id="4802c-156">The *filename* variable is required if the device was opened using the "new" device identifier.</span></span>

## <a name="examples"></a><span data-ttu-id="4802c-157">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4802c-157">Examples</span></span>

<span data-ttu-id="4802c-158">El siguiente comando guarda el búfer de vídeo completo en un archivo denominado VCAPFILE. TGA.</span><span class="sxs-lookup"><span data-stu-id="4802c-158">The following command saves the entire video buffer to a file named VCAPFILE.TGA.</span></span>

``` syntax
save vboard c:\vcap\vcapfile.tga
```

## <a name="requirements"></a><span data-ttu-id="4802c-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4802c-159">Requirements</span></span>



| <span data-ttu-id="4802c-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="4802c-160">Requirement</span></span> | <span data-ttu-id="4802c-161">Value</span><span class="sxs-lookup"><span data-stu-id="4802c-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4802c-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4802c-162">Minimum supported client</span></span><br/> | <span data-ttu-id="4802c-163">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4802c-163">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4802c-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4802c-164">Minimum supported server</span></span><br/> | <span data-ttu-id="4802c-165">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4802c-165">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4802c-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="4802c-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4802c-167">MCI</span><span class="sxs-lookup"><span data-stu-id="4802c-167">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4802c-168">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="4802c-168">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="4802c-169">grabar</span><span class="sxs-lookup"><span data-stu-id="4802c-169">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="4802c-170">reserva</span><span class="sxs-lookup"><span data-stu-id="4802c-170">reserve</span></span>](reserve.md)
</dt> </dl>

 

