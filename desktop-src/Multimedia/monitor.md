---
title: monitor (comando)
description: El comando monitor especifica el origen de la presentación. (El origen de presentación predeterminado es el área de trabajo). Al cambiar el origen de la presentación, se cambian todas las secuencias de audio y vídeo del origen. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 5cacbe88-b94e-4101-badf-2bb4796b19cf
keywords:
- comando supervisar Windows multimedia
topic_type:
- apiref
api_name:
- monitor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ccbe1d8919c232ab88d04081dad242944868893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802221"
---
# <a name="monitor-command"></a><span data-ttu-id="7a0e4-106">monitor (comando)</span><span class="sxs-lookup"><span data-stu-id="7a0e4-106">monitor command</span></span>

<span data-ttu-id="7a0e4-107">El comando monitor especifica el origen de la presentación.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-107">The monitor command specifies the presentation source.</span></span> <span data-ttu-id="7a0e4-108">(El origen de presentación predeterminado es el área de trabajo). Al cambiar el origen de la presentación, se cambian todas las secuencias de audio y vídeo del origen.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-108">(The default presentation source is the workspace.) Switching the presentation source switches all audio and video streams in the source.</span></span> <span data-ttu-id="7a0e4-109">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-109">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="7a0e4-110">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("monitor %s %s %s"), 
  lpszDeviceID, 
  lpszMonitor, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="7a0e4-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a0e4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a0e4-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="7a0e4-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7a0e4-113">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-113">Identifier of an MCI device.</span></span> <span data-ttu-id="7a0e4-114">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="7a0e4-115"><span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*</span><span class="sxs-lookup"><span data-stu-id="7a0e4-115"><span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*</span></span>
</dt> <dd>

<span data-ttu-id="7a0e4-116">Una o varias de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-116">One or more of the following flags.</span></span>



| <span data-ttu-id="7a0e4-117">Value</span><span class="sxs-lookup"><span data-stu-id="7a0e4-117">Value</span></span>           | <span data-ttu-id="7a0e4-118">Significado</span><span class="sxs-lookup"><span data-stu-id="7a0e4-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a0e4-119">archivo</span><span class="sxs-lookup"><span data-stu-id="7a0e4-119">file</span></span>            | <span data-ttu-id="7a0e4-120">Especifica que el área de trabajo es el origen de la presentación.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-120">Specifies that the workspace is the presentation source.</span></span> <span data-ttu-id="7a0e4-121">Este es el origen predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-121">This is the default source.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="7a0e4-122">input</span><span class="sxs-lookup"><span data-stu-id="7a0e4-122">input</span></span>           | <span data-ttu-id="7a0e4-123">Especifica que la entrada externa es el origen de la presentación.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-123">Specifies that the external input is the presentation source.</span></span> <span data-ttu-id="7a0e4-124">Si un comando de [reproducción](play.md) está en curso, se pausa primero.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-124">If a [play](play.md) command is in progress, it is first paused.</span></span> <span data-ttu-id="7a0e4-125">Si [setvideo](setvideo.md) es "ON", esta marca muestra una ventana oculta predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-125">If [setvideo](setvideo.md) is "on", this flag displays a default hidden window.</span></span> <span data-ttu-id="7a0e4-126">Los dispositivos pueden limitar lo que pueden hacer otras instancias del dispositivo mientras se supervisa la entrada.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-126">Devices might limit what other device instances can do while monitoring input.</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="7a0e4-127">método *Method*</span><span class="sxs-lookup"><span data-stu-id="7a0e4-127">method *method*</span></span> | <span data-ttu-id="7a0e4-128">Cuando se usa con el **monitor** "Input", esta marca selecciona el método de supervisión.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-128">When used with **monitor** "input", this flag selects the method of monitoring.</span></span> <span data-ttu-id="7a0e4-129">El *método* es "pre", "post" o "Direct".</span><span class="sxs-lookup"><span data-stu-id="7a0e4-129">The *method* is either "pre", "post", or "direct".</span></span> <span data-ttu-id="7a0e4-130">La supervisión directa solicita que el dispositivo esté configurado para una calidad de visualización óptima durante la supervisión.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-130">Direct monitoring requests that the device be configured for optimum display quality during monitoring.</span></span> <span data-ttu-id="7a0e4-131">El método de supervisión directa podría ser incompatible con la grabación de vídeo de movimiento. La supervisión previa y posterior permite la grabación de vídeo en movimiento.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-131">The direct monitoring method might be incompatible with motion video recording.Pre- and post-monitoring allow motion video recording.</span></span> <span data-ttu-id="7a0e4-132">La supervisión previa muestra la entrada externa antes de la compresión, mientras que la supervisión posterior muestra la entrada externa después de la compresión.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-132">Pre-monitoring shows the external input prior to compression, while post-monitoring shows the external input after compression.</span></span> <span data-ttu-id="7a0e4-133">Normalmente, los distintos métodos de supervisión tienen implicaciones de hardware diferentes.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-133">Typically, different monitoring methods have different hardware implications.</span></span> <span data-ttu-id="7a0e4-134">El dispositivo selecciona el método de supervisión predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-134">The default monitoring method is selected by the device.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7a0e4-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="7a0e4-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7a0e4-136">Puede ser "Wait", "Notify", "Test" o una combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="7a0e4-137">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7a0e4-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a0e4-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a0e4-138">Return Value</span></span>

<span data-ttu-id="7a0e4-139">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a0e4-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a0e4-140">Remarks</span></span>

<span data-ttu-id="7a0e4-141">El origen de la presentación cambia automáticamente al área de trabajo después de un comando de [reproducción](play.md), [paso](step.md), [pausa](pause.md), [indicación](cue.md) "salida" o [búsqueda](seek.md) .</span><span class="sxs-lookup"><span data-stu-id="7a0e4-141">The presentation source automatically switches to the workspace after a [play](play.md), [step](step.md), [pause](pause.md), [cue](cue.md) "output", or [seek](seek.md) command.</span></span> <span data-ttu-id="7a0e4-142">El comando [grabar](record.md) no cambia automáticamente los orígenes de presentación, lo que proporciona a la aplicación la opción de no mostrar vídeo mientras se graba.</span><span class="sxs-lookup"><span data-stu-id="7a0e4-142">The [record](record.md) command does not automatically switch presentation sources, which gives your application the option of not showing video while it is being recorded.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a0e4-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a0e4-143">Requirements</span></span>



| <span data-ttu-id="7a0e4-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a0e4-144">Requirement</span></span> | <span data-ttu-id="7a0e4-145">Value</span><span class="sxs-lookup"><span data-stu-id="7a0e4-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7a0e4-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a0e4-146">Minimum supported client</span></span><br/> | <span data-ttu-id="7a0e4-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7a0e4-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7a0e4-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a0e4-148">Minimum supported server</span></span><br/> | <span data-ttu-id="7a0e4-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7a0e4-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7a0e4-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a0e4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a0e4-151">MCI</span><span class="sxs-lookup"><span data-stu-id="7a0e4-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7a0e4-152">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="7a0e4-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="7a0e4-153">indicación</span><span class="sxs-lookup"><span data-stu-id="7a0e4-153">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="7a0e4-154">pause</span><span class="sxs-lookup"><span data-stu-id="7a0e4-154">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="7a0e4-155">reproducción</span><span class="sxs-lookup"><span data-stu-id="7a0e4-155">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="7a0e4-156">record</span><span class="sxs-lookup"><span data-stu-id="7a0e4-156">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="7a0e4-157">desean</span><span class="sxs-lookup"><span data-stu-id="7a0e4-157">seek</span></span>](seek.md)
</dt> <dt>

[<span data-ttu-id="7a0e4-158">pasar</span><span class="sxs-lookup"><span data-stu-id="7a0e4-158">step</span></span>](step.md)
</dt> </dl>

 

