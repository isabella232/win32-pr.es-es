---
title: comando resume
description: El comando de reanudación continúa reproduciendo o grabando en un dispositivo que se ha pausado mediante el comando pausar.
ms.assetid: 0a2cdd23-8c1d-4d9e-9b63-3fdcbb13e3a2
keywords:
- comando resume de Windows multimedia
topic_type:
- apiref
api_name:
- resume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f01fd96e2b25e191608c7c6abf70bfd842158d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676570"
---
# <a name="resume-command"></a><span data-ttu-id="14b6c-104">comando resume</span><span class="sxs-lookup"><span data-stu-id="14b6c-104">resume command</span></span>

<span data-ttu-id="14b6c-105">El comando de reanudación continúa reproduciendo o grabando en un dispositivo que se ha pausado mediante el comando [pausar](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="14b6c-105">The resume command continues playing or recording on a device that has been paused using the [pause](pause.md) command.</span></span> <span data-ttu-id="14b6c-106">Los dispositivos de audio digital-vídeo, VCR y de onda y de onda reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="14b6c-106">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="14b6c-107">Aunque los dispositivos de audio de CD, secuenciador MIDI y VideoDisc también reconocen este comando, los controladores de dispositivos MCICDA, MCISEQ y MCIPIONR no lo admiten.</span><span class="sxs-lookup"><span data-stu-id="14b6c-107">Although CD audio, MIDI sequencer, and videodisc devices also recognize this command, the MCICDA, MCISEQ, and MCIPIONR device drivers do not support it.</span></span>

<span data-ttu-id="14b6c-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="14b6c-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("resume %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="14b6c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14b6c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b6c-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="14b6c-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="14b6c-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="14b6c-111">Identifier of an MCI device.</span></span> <span data-ttu-id="14b6c-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14b6c-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="14b6c-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="14b6c-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="14b6c-114">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="14b6c-114">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="14b6c-115">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="14b6c-115">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="14b6c-116">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="14b6c-116">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14b6c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14b6c-117">Return Value</span></span>

<span data-ttu-id="14b6c-118">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="14b6c-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="14b6c-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="14b6c-119">Examples</span></span>

<span data-ttu-id="14b6c-120">El siguiente comando continúa reproduciendo o grabando el dispositivo "Newsound".</span><span class="sxs-lookup"><span data-stu-id="14b6c-120">The following command continues playing or recording the "newsound" device.</span></span>

``` syntax
resume newsound
```

## <a name="requirements"></a><span data-ttu-id="14b6c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14b6c-121">Requirements</span></span>



| <span data-ttu-id="14b6c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="14b6c-122">Requirement</span></span> | <span data-ttu-id="14b6c-123">Value</span><span class="sxs-lookup"><span data-stu-id="14b6c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="14b6c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14b6c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="14b6c-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="14b6c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="14b6c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14b6c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="14b6c-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14b6c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="14b6c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="14b6c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b6c-129">MCI</span><span class="sxs-lookup"><span data-stu-id="14b6c-129">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="14b6c-130">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="14b6c-130">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="14b6c-131">pause</span><span class="sxs-lookup"><span data-stu-id="14b6c-131">pause</span></span>](pause.md)
</dt> </dl>

 

