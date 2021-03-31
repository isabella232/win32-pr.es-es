---
title: comando Step
description: El comando Step le indica cómo reproducir una o más tramas hacia delante o hacia atrás. La acción predeterminada es avanzar un fotograma. Los dispositivos de vídeo digital-video, VCR y CAV-Format reconocen este comando.
ms.assetid: 6017ace5-cde9-42a0-bb2f-f85d7847adc5
keywords:
- comando Step multimedia de Windows
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6203d0b2d5dea401e8197e1261946955cd28618a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490475"
---
# <a name="step-command"></a><span data-ttu-id="fd323-106">comando Step</span><span class="sxs-lookup"><span data-stu-id="fd323-106">step command</span></span>

<span data-ttu-id="fd323-107">El comando Step le indica cómo reproducir una o más tramas hacia delante o hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="fd323-107">The step command steps the play one or more frames forward or reverse.</span></span> <span data-ttu-id="fd323-108">La acción predeterminada es avanzar un fotograma.</span><span class="sxs-lookup"><span data-stu-id="fd323-108">The default action is to step forward one frame.</span></span> <span data-ttu-id="fd323-109">Los dispositivos de vídeo digital-video, VCR y CAV-Format reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="fd323-109">Digital-video, VCR, and CAV-format videodisc devices recognize this command.</span></span>

<span data-ttu-id="fd323-110">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="fd323-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("step %s %s %s"), 
  lpszDeviceID, 
  lpszStepFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="fd323-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd323-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd323-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="fd323-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="fd323-113">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="fd323-113">Identifier of an MCI device.</span></span> <span data-ttu-id="fd323-114">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fd323-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="fd323-115"><span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*</span><span class="sxs-lookup"><span data-stu-id="fd323-115"><span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*</span></span>
</dt> <dd>

<span data-ttu-id="fd323-116">Una o ambas de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="fd323-116">One or both of the following flags.</span></span>



| <span data-ttu-id="fd323-117">Value</span><span class="sxs-lookup"><span data-stu-id="fd323-117">Value</span></span>       | <span data-ttu-id="fd323-118">Significado</span><span class="sxs-lookup"><span data-stu-id="fd323-118">Meaning</span></span>                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd323-119">por *fotogramas*</span><span class="sxs-lookup"><span data-stu-id="fd323-119">by *frames*</span></span> | <span data-ttu-id="fd323-120">Indica el número de fotogramas que se van a recorrer.</span><span class="sxs-lookup"><span data-stu-id="fd323-120">Indicates the number of frames to step.</span></span> <span data-ttu-id="fd323-121">Si especifica un valor de *fotogramas* negativos, no puede especificar la marca "REVERSE".</span><span class="sxs-lookup"><span data-stu-id="fd323-121">If you specify a negative *frames* value, you cannot specify the "reverse" flag.</span></span> |
| <span data-ttu-id="fd323-122">reverse</span><span class="sxs-lookup"><span data-stu-id="fd323-122">reverse</span></span>     | <span data-ttu-id="fd323-123">Desplazar los fotogramas en orden inverso.</span><span class="sxs-lookup"><span data-stu-id="fd323-123">Step the frames in reverse.</span></span>                                                                                              |



 

</dd> <dt>

<span data-ttu-id="fd323-124"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="fd323-124"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="fd323-125">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="fd323-125">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="fd323-126">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="fd323-126">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="fd323-127">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="fd323-127">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd323-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd323-128">Return Value</span></span>

<span data-ttu-id="fd323-129">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fd323-129">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd323-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd323-130">Requirements</span></span>



| <span data-ttu-id="fd323-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd323-131">Requirement</span></span> | <span data-ttu-id="fd323-132">Value</span><span class="sxs-lookup"><span data-stu-id="fd323-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="fd323-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd323-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fd323-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fd323-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fd323-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd323-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fd323-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fd323-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="fd323-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd323-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd323-138">MCI</span><span class="sxs-lookup"><span data-stu-id="fd323-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="fd323-139">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="fd323-139">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

