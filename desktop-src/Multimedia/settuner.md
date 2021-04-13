---
title: comando settuner
description: El comando settuner cambia el sintonizador actual o la configuración de canal del sintonizador actual. Los dispositivos VCR reconocen este comando.
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- comando settuner de Windows multimedia
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51150043a68f3cd34525eb74a64237fc4dc150e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493259"
---
# <a name="settuner-command"></a><span data-ttu-id="35dad-105">comando settuner</span><span class="sxs-lookup"><span data-stu-id="35dad-105">settuner command</span></span>

<span data-ttu-id="35dad-106">El comando settuner cambia el sintonizador actual o la configuración de canal del sintonizador actual.</span><span class="sxs-lookup"><span data-stu-id="35dad-106">The settuner command changes the current tuner or the channel setting of the current tuner.</span></span> <span data-ttu-id="35dad-107">Los dispositivos VCR reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="35dad-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="35dad-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="35dad-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settuner %s %s %s"), 
  lpszDeviceID, 
  lpszTuner, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="35dad-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35dad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35dad-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="35dad-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="35dad-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="35dad-111">Identifier of an MCI device.</span></span> <span data-ttu-id="35dad-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35dad-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="35dad-113"><span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*</span><span class="sxs-lookup"><span data-stu-id="35dad-113"><span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*</span></span>
</dt> <dd>

<span data-ttu-id="35dad-114">Una de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="35dad-114">One of the following flags.</span></span>



| <span data-ttu-id="35dad-115">Value</span><span class="sxs-lookup"><span data-stu-id="35dad-115">Value</span></span>                            | <span data-ttu-id="35dad-116">Significado</span><span class="sxs-lookup"><span data-stu-id="35dad-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35dad-117">*canal* de canal</span><span class="sxs-lookup"><span data-stu-id="35dad-117">channel *channel*</span></span>                | <span data-ttu-id="35dad-118">Establece el sintonizador en el *canal*.</span><span class="sxs-lookup"><span data-stu-id="35dad-118">Sets the tuner to *channel*.</span></span> <span data-ttu-id="35dad-119">Es posible que no pueda cambiar el canal durante la grabación, según el VCR.</span><span class="sxs-lookup"><span data-stu-id="35dad-119">You might not be able to change the channel while recording, depending on the VCR.</span></span> <span data-ttu-id="35dad-120">Un canal mayor que el máximo establece el sintonizador en el canal máximo.</span><span class="sxs-lookup"><span data-stu-id="35dad-120">A channel larger than the maximum sets the tuner to the maximum channel.</span></span>                                                                                                                    |
| <span data-ttu-id="35dad-121">búsqueda de canal activo de búsqueda de canal</span><span class="sxs-lookup"><span data-stu-id="35dad-121">channel seek upchannel seek down</span></span> | <span data-ttu-id="35dad-122">Busca el siguiente canal con una señal válida.</span><span class="sxs-lookup"><span data-stu-id="35dad-122">Seeks the next channel with a valid signal.</span></span> <span data-ttu-id="35dad-123">"Buscar" incrementa el número de canal en su búsqueda.</span><span class="sxs-lookup"><span data-stu-id="35dad-123">"Seek up" increments the channel number in its search.</span></span> <span data-ttu-id="35dad-124">"Buscar hacia abajo" disminuye el número de canal en su búsqueda.</span><span class="sxs-lookup"><span data-stu-id="35dad-124">"Seek down" decrements the channel number in its search.</span></span> <span data-ttu-id="35dad-125">El sintonizador se ajusta al canal 1 cuando se supera el número de canal máximo.</span><span class="sxs-lookup"><span data-stu-id="35dad-125">The tuner wraps to channel 1 when the maximum channel number is exceeded.</span></span> <span data-ttu-id="35dad-126">Del mismo modo, al buscar hacia abajo, el sintonizador se ajusta al canal máximo.</span><span class="sxs-lookup"><span data-stu-id="35dad-126">Similarly, when seeking down, the tuner wraps to the maximum channel.</span></span> |
| <span data-ttu-id="35dad-127">canal inferior del canal</span><span class="sxs-lookup"><span data-stu-id="35dad-127">channel upchannel down</span></span>           | <span data-ttu-id="35dad-128">Incrementa o disminuye el canal del sintonizador.</span><span class="sxs-lookup"><span data-stu-id="35dad-128">Increments or decrements the tuner channel.</span></span> <span data-ttu-id="35dad-129">Es posible que no pueda cambiar el canal durante la grabación, según el VCR.</span><span class="sxs-lookup"><span data-stu-id="35dad-129">You might not be able to change the channel while recording, depending on the VCR.</span></span> <span data-ttu-id="35dad-130">El sintonizador se ajusta al canal 1 cuando se supera el número de canal máximo.</span><span class="sxs-lookup"><span data-stu-id="35dad-130">The tuner wraps to channel 1 when the maximum channel number is exceeded.</span></span> <span data-ttu-id="35dad-131">Del mismo modo, al buscar hacia abajo, el sintonizador se ajusta al canal máximo.</span><span class="sxs-lookup"><span data-stu-id="35dad-131">Similarly, when seeking down, the tuner wraps to the maximum channel.</span></span>                              |
| <span data-ttu-id="35dad-132">*número* de número</span><span class="sxs-lookup"><span data-stu-id="35dad-132">number *number*</span></span>                  | <span data-ttu-id="35dad-133">Especifica el sintonizador que debe verse afectado por el comando settuner.</span><span class="sxs-lookup"><span data-stu-id="35dad-133">Specifies the tuner to be affected by the settuner command.</span></span> <span data-ttu-id="35dad-134">Si no se proporciona el *número* , se asume el valor predeterminado de 1.</span><span class="sxs-lookup"><span data-stu-id="35dad-134">If *number* is not given, the default value of 1 is assumed.</span></span>                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="35dad-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="35dad-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="35dad-136">Puede ser "Wait", "Notify", "Test" o una combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="35dad-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="35dad-137">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="35dad-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35dad-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35dad-138">Return Value</span></span>

<span data-ttu-id="35dad-139">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="35dad-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="35dad-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35dad-140">Requirements</span></span>



| <span data-ttu-id="35dad-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="35dad-141">Requirement</span></span> | <span data-ttu-id="35dad-142">Value</span><span class="sxs-lookup"><span data-stu-id="35dad-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="35dad-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35dad-143">Minimum supported client</span></span><br/> | <span data-ttu-id="35dad-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="35dad-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="35dad-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35dad-145">Minimum supported server</span></span><br/> | <span data-ttu-id="35dad-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="35dad-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="35dad-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="35dad-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35dad-148">MCI</span><span class="sxs-lookup"><span data-stu-id="35dad-148">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="35dad-149">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="35dad-149">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

