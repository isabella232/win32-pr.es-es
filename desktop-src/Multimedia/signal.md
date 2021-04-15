---
title: Signal (comando)
description: El comando Signal identifica una posición especificada en el área de trabajo enviando a la aplicación un \_ mensaje mm MCISIGNAL. Los dispositivos de vídeo digital reconocen este comando. MCIAVI solo admite una señal activa a la vez.
ms.assetid: 3d10eac0-fd1a-41ee-98fa-2518642c7339
keywords:
- comando Signal Windows multimedia
topic_type:
- apiref
api_name:
- signal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd96b8970ebbb6502306c6d2d5fd8c49f172cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676798"
---
# <a name="signal-command"></a><span data-ttu-id="148dd-106">Signal (comando)</span><span class="sxs-lookup"><span data-stu-id="148dd-106">signal command</span></span>

<span data-ttu-id="148dd-107">El comando Signal identifica una posición especificada en el área de trabajo enviando a la aplicación un mensaje [mm \_ MCISIGNAL](mm-mcisignal.md) .</span><span class="sxs-lookup"><span data-stu-id="148dd-107">The signal command identifies a specified position in the workspace by sending the application an [MM\_MCISIGNAL](mm-mcisignal.md) message.</span></span> <span data-ttu-id="148dd-108">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="148dd-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="148dd-109">MCIAVI solo admite una señal activa a la vez.</span><span class="sxs-lookup"><span data-stu-id="148dd-109">MCIAVI supports only one active signal at a time.</span></span>

<span data-ttu-id="148dd-110">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="148dd-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("signal %s %s %s"), 
  lpszDeviceID, 
  lpszSignalFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="148dd-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="148dd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="148dd-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="148dd-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="148dd-113">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="148dd-113">Identifier of an MCI device.</span></span> <span data-ttu-id="148dd-114">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="148dd-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="148dd-115"><span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*</span><span class="sxs-lookup"><span data-stu-id="148dd-115"><span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*</span></span>
</dt> <dd>

<span data-ttu-id="148dd-116">Una de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="148dd-116">One of the following flags.</span></span>



| <span data-ttu-id="148dd-117">Value</span><span class="sxs-lookup"><span data-stu-id="148dd-117">Value</span></span>            | <span data-ttu-id="148dd-118">Significado</span><span class="sxs-lookup"><span data-stu-id="148dd-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="148dd-119">en la posición</span><span class="sxs-lookup"><span data-stu-id="148dd-119">at position</span></span>      | <span data-ttu-id="148dd-120">Especifica el marco en el que se va a invocar una señal.</span><span class="sxs-lookup"><span data-stu-id="148dd-120">Specifies the frame to invoke a signal.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="148dd-121">cancel</span><span class="sxs-lookup"><span data-stu-id="148dd-121">cancel</span></span>           | <span data-ttu-id="148dd-122">Quita las señales del área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="148dd-122">Removes signals from the workspace.</span></span> <span data-ttu-id="148dd-123">Una señal individual se especifica mediante la marca "uservalue".</span><span class="sxs-lookup"><span data-stu-id="148dd-123">An individual signal is specified by using the "uservalue" flag.</span></span> <span data-ttu-id="148dd-124">Si no se especifica la marca "uservalue" mediante "Cancelar", el dispositivo cancela todas las señales.</span><span class="sxs-lookup"><span data-stu-id="148dd-124">If the "uservalue" flag is not specified by using "cancel", the device cancels all signals.</span></span> <span data-ttu-id="148dd-125">La marca "Cancelar" es incompatible con las marcas "at", "cada" y "posición de retorno".</span><span class="sxs-lookup"><span data-stu-id="148dd-125">The "cancel" flag is incompatible with the "at", "every", and "return position" flags.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="148dd-126">cada *intervalo*</span><span class="sxs-lookup"><span data-stu-id="148dd-126">every *interval*</span></span> | <span data-ttu-id="148dd-127">Especifica el período de las señales.</span><span class="sxs-lookup"><span data-stu-id="148dd-127">Specifies the period of the signals.</span></span> <span data-ttu-id="148dd-128">El valor de *intervalo* se especifica en el formato de hora actual. Si se usa con la *posición*"at", las señales se colocan en el área de trabajo con una marca de señal colocada en la *posición*.</span><span class="sxs-lookup"><span data-stu-id="148dd-128">The *interval* value is specified in the current time format.If used with "at" *position*, signals are placed throughout the workspace with one signal mark placed at *position*.</span></span><br/> <span data-ttu-id="148dd-129">Sin la marca "at", las señales se colocan en el área de trabajo con una señal en la posición actual.</span><span class="sxs-lookup"><span data-stu-id="148dd-129">Without the "at" flag, signals are placed throughout the workspace with one signal at the current position.</span></span><br/> <span data-ttu-id="148dd-130">Si se omite esta marca, solo se marca la posición indicada por la marca "at".</span><span class="sxs-lookup"><span data-stu-id="148dd-130">If this flag is omitted, only the position indicated by the "at" flag is marked.</span></span><br/> <span data-ttu-id="148dd-131">Si el valor del *intervalo* es menor que la frecuencia mínima admitida por un dispositivo, utilizará su valor mínimo.</span><span class="sxs-lookup"><span data-stu-id="148dd-131">If the *interval* value is less than the minimum frequency supported by a device, it will use its minimum value.</span></span><br/> |
| <span data-ttu-id="148dd-132">posición de retorno</span><span class="sxs-lookup"><span data-stu-id="148dd-132">return position</span></span>  | <span data-ttu-id="148dd-133">Indica que el dispositivo debe enviar el valor de posición en lugar del identificador "uservalue" en el mensaje de señalización.</span><span class="sxs-lookup"><span data-stu-id="148dd-133">Indicates the device should send the position value instead of the "uservalue" identifier in the signaling message.</span></span> <span data-ttu-id="148dd-134">El identificador "uservalue" puede seguir utilizándose para cancelar o volver a definir las marcas de señal.</span><span class="sxs-lookup"><span data-stu-id="148dd-134">The "uservalue" identifier can still be used to cancel or to redefine the signal marks.</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="148dd-135">*identificador* de uservalue</span><span class="sxs-lookup"><span data-stu-id="148dd-135">uservalue *id*</span></span>   | <span data-ttu-id="148dd-136">Especifica un identificador que se devuelve con el mensaje de señalización.</span><span class="sxs-lookup"><span data-stu-id="148dd-136">Specifies an identifier that is reported back with the signaling message.</span></span> <span data-ttu-id="148dd-137">Este identificador actúa como un identificador que se puede usar con otros comandos de **señal** para hacer referencia a esta configuración de la **señal** .</span><span class="sxs-lookup"><span data-stu-id="148dd-137">This identifier acts as an identifier that can be used with other **signal** commands to reference this **signal** setting.</span></span> <span data-ttu-id="148dd-138">Si se omite, el valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="148dd-138">If omitted, the default value is zero.</span></span>                                                                                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="148dd-139"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="148dd-139"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="148dd-140">Puede ser "Wait", "Notify", "Test" o una combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="148dd-140">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="148dd-141">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="148dd-141">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="148dd-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="148dd-142">Return Value</span></span>

<span data-ttu-id="148dd-143">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="148dd-143">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="148dd-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="148dd-144">Remarks</span></span>

<span data-ttu-id="148dd-145">El identificador de ventana que se usa para la notificación de mensajes de finalización de comandos también se usa para la señalización.</span><span class="sxs-lookup"><span data-stu-id="148dd-145">The window handle used for notification of command completion messages is also used for signaling.</span></span>

## <a name="requirements"></a><span data-ttu-id="148dd-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="148dd-146">Requirements</span></span>



| <span data-ttu-id="148dd-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="148dd-147">Requirement</span></span> | <span data-ttu-id="148dd-148">Value</span><span class="sxs-lookup"><span data-stu-id="148dd-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="148dd-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="148dd-149">Minimum supported client</span></span><br/> | <span data-ttu-id="148dd-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="148dd-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="148dd-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="148dd-151">Minimum supported server</span></span><br/> | <span data-ttu-id="148dd-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="148dd-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="148dd-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="148dd-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="148dd-154">MCI</span><span class="sxs-lookup"><span data-stu-id="148dd-154">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="148dd-155">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="148dd-155">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="148dd-156">MM \_ MCISIGNAL</span><span class="sxs-lookup"><span data-stu-id="148dd-156">MM\_MCISIGNAL</span></span>](mm-mcisignal.md)
</dt> </dl>

 

