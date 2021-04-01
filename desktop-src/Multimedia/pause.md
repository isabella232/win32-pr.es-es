---
title: Pausar (comando)
description: El comando PAUSE pausa la reproducción o grabación.
ms.assetid: 8fa1a40d-fdb1-4c9f-a8db-9dd6a0d83b87
keywords:
- comando pausar de Windows multimedia
topic_type:
- apiref
api_name:
- pause
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25957defa4db514ce84f2e013dcc3751e21779b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905655"
---
# <a name="pause-command"></a><span data-ttu-id="c2885-104">Pausar (comando)</span><span class="sxs-lookup"><span data-stu-id="c2885-104">pause command</span></span>

<span data-ttu-id="c2885-105">El comando PAUSE pausa la reproducción o grabación.</span><span class="sxs-lookup"><span data-stu-id="c2885-105">The pause command pauses playing or recording.</span></span> <span data-ttu-id="c2885-106">La mayoría de los controladores conservan la posición actual y finalmente reanudan la reproducción o grabación en esta posición.</span><span class="sxs-lookup"><span data-stu-id="c2885-106">Most drivers retain the current position and eventually resume playback or recording at this position.</span></span> <span data-ttu-id="c2885-107">Los dispositivos de audio de CD, digital-video, MIDI Sequencer, VCR, Videodisc y de onda-audio reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="c2885-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="c2885-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="c2885-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("pause %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c2885-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2885-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2885-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c2885-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c2885-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="c2885-111">Identifier of an MCI device.</span></span> <span data-ttu-id="c2885-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2885-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c2885-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c2885-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c2885-114">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="c2885-114">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="c2885-115">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="c2885-115">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="c2885-116">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c2885-116">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2885-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2885-117">Return Value</span></span>

<span data-ttu-id="c2885-118">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c2885-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2885-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2885-119">Remarks</span></span>

<span data-ttu-id="c2885-120">Con los controladores MCICDA, MCISEQ y MCIPIONR, el comando PAUSE funciona igual que el comando [Stop](stop.md) .</span><span class="sxs-lookup"><span data-stu-id="c2885-120">With the MCICDA, MCISEQ, and MCIPIONR drivers, the pause command works the same as the [stop](stop.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="c2885-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c2885-121">Examples</span></span>

<span data-ttu-id="c2885-122">El siguiente comando pausa el dispositivo "de".</span><span class="sxs-lookup"><span data-stu-id="c2885-122">The following command pauses the "mysound" device.</span></span>

``` syntax
pause mysound
```

## <a name="requirements"></a><span data-ttu-id="c2885-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2885-123">Requirements</span></span>



| <span data-ttu-id="c2885-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2885-124">Requirement</span></span> | <span data-ttu-id="c2885-125">Value</span><span class="sxs-lookup"><span data-stu-id="c2885-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c2885-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2885-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c2885-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c2885-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c2885-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2885-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c2885-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c2885-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c2885-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2885-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2885-131">MCI</span><span class="sxs-lookup"><span data-stu-id="c2885-131">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c2885-132">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="c2885-132">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="c2885-133">stop</span><span class="sxs-lookup"><span data-stu-id="c2885-133">stop</span></span>](stop.md)
</dt> </dl>

 

