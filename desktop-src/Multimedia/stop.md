---
title: detener (comando)
description: El comando Stop detiene la reproducción o grabación. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, Videodisc, VCR y de onda-audio reconocen este comando.
ms.assetid: 82b2da63-f1ac-48f3-a206-6c5cfe00f5be
keywords:
- detener comando de Windows multimedia
topic_type:
- apiref
api_name:
- stop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79d70aa150c01bd4c0ceab10332b4eca8b15d041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422304"
---
# <a name="stop-command"></a><span data-ttu-id="20a0c-105">detener (comando)</span><span class="sxs-lookup"><span data-stu-id="20a0c-105">stop command</span></span>

<span data-ttu-id="20a0c-106">El comando Stop detiene la reproducción o grabación.</span><span class="sxs-lookup"><span data-stu-id="20a0c-106">The stop command stops playback or recording.</span></span> <span data-ttu-id="20a0c-107">Los dispositivos de audio de CD, digital-video, MIDI Sequencer, Videodisc, VCR y de onda-audio reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="20a0c-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="20a0c-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="20a0c-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("stop %s %s %s"), 
  lpszDeviceID, 
  lpszStopFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="20a0c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20a0c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20a0c-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="20a0c-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="20a0c-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="20a0c-111">Identifier of an MCI device.</span></span> <span data-ttu-id="20a0c-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20a0c-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="20a0c-113"><span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*</span><span class="sxs-lookup"><span data-stu-id="20a0c-113"><span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*</span></span>
</dt> <dd>

<span data-ttu-id="20a0c-114">En el caso de los dispositivos de vídeo digital, puede ser la marca siguiente.</span><span class="sxs-lookup"><span data-stu-id="20a0c-114">For digital-video devices, it can be the following flag.</span></span>



| <span data-ttu-id="20a0c-115">Value</span><span class="sxs-lookup"><span data-stu-id="20a0c-115">Value</span></span> | <span data-ttu-id="20a0c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="20a0c-116">Meaning</span></span>                                                                                                                                                                                      |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20a0c-117">contener</span><span class="sxs-lookup"><span data-stu-id="20a0c-117">hold</span></span>  | <span data-ttu-id="20a0c-118">Impide que se liberen los recursos necesarios para volver a dibujar una imagen fija en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="20a0c-118">Prevents the release of resources required to redraw a still image on the screen.</span></span> <span data-ttu-id="20a0c-119">El búfer de marco sigue estando disponible para su uso en la actualización de la pantalla cuando, por ejemplo, la ventana se mueve.</span><span class="sxs-lookup"><span data-stu-id="20a0c-119">The frame buffer remains available for use in updating the display when, for example, the window is moved.</span></span> |



 

</dd> <dt>

<span data-ttu-id="20a0c-120"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="20a0c-120"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="20a0c-121">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="20a0c-121">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="20a0c-122">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="20a0c-122">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="20a0c-123">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="20a0c-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20a0c-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20a0c-124">Return Value</span></span>

<span data-ttu-id="20a0c-125">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="20a0c-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="20a0c-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20a0c-126">Remarks</span></span>

<span data-ttu-id="20a0c-127">En el caso de los dispositivos de audio de CD, el comando Stop detiene la reproducción y restablece la posición de pista actual en cero.</span><span class="sxs-lookup"><span data-stu-id="20a0c-127">For CD audio devices, the stop command stops playback and resets the current track position to zero.</span></span>

## <a name="examples"></a><span data-ttu-id="20a0c-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="20a0c-128">Examples</span></span>

<span data-ttu-id="20a0c-129">El comando siguiente detiene la reproducción o grabación en el dispositivo "".</span><span class="sxs-lookup"><span data-stu-id="20a0c-129">The following command stops playback or recording on the "mysound" device.</span></span>

``` syntax
stop mysound
```

## <a name="requirements"></a><span data-ttu-id="20a0c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20a0c-130">Requirements</span></span>



| <span data-ttu-id="20a0c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="20a0c-131">Requirement</span></span> | <span data-ttu-id="20a0c-132">Value</span><span class="sxs-lookup"><span data-stu-id="20a0c-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="20a0c-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20a0c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="20a0c-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="20a0c-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="20a0c-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20a0c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="20a0c-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="20a0c-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="20a0c-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="20a0c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20a0c-138">MCI</span><span class="sxs-lookup"><span data-stu-id="20a0c-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="20a0c-139">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="20a0c-139">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

