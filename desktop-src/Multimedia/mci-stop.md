---
title: Comando MCI_STOP (mmsystem. h)
description: El comando de detención de MCI \_ detiene todas las secuencias de reproducción y grabación, descarga todos los búferes de reproducción y deja de mostrar las imágenes de vídeo. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, Videodisc, VCR y de onda-audio reconocen este comando.
ms.assetid: e5ae20b3-7439-4314-8354-d06e83b29729
keywords:
- Comando de MCI_STOP de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_STOP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea5f2acbe39b0be64ebc640ae31ceede7591c7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422368"
---
# <a name="mci_stop-command"></a><span data-ttu-id="fcd42-105">Comando de detención de MCI \_</span><span class="sxs-lookup"><span data-stu-id="fcd42-105">MCI\_STOP command</span></span>

<span data-ttu-id="fcd42-106">El comando de detención de MCI \_ detiene todas las secuencias de reproducción y grabación, descarga todos los búferes de reproducción y deja de mostrar las imágenes de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fcd42-106">The MCI\_STOP command stops all play and record sequences, unloads all play buffers, and ceases display of video images.</span></span> <span data-ttu-id="fcd42-107">Los dispositivos de audio de CD, digital-video, MIDI Sequencer, Videodisc, VCR y de onda-audio reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="fcd42-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="fcd42-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="fcd42-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STOP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStop
);
```



## <a name="parameters"></a><span data-ttu-id="fcd42-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcd42-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcd42-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="fcd42-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="fcd42-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="fcd42-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="fcd42-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="fcd42-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="fcd42-113">MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="fcd42-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="fcd42-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="fcd42-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="fcd42-115"><span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*</span><span class="sxs-lookup"><span data-stu-id="fcd42-115"><span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*</span></span>
</dt> <dd>

<span data-ttu-id="fcd42-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="fcd42-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="fcd42-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="fcd42-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcd42-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcd42-118">Return Value</span></span>

<span data-ttu-id="fcd42-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fcd42-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcd42-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcd42-120">Remarks</span></span>

<span data-ttu-id="fcd42-121">La diferencia entre los \_ comandos MCI STOP y [MCI \_ PAUSE](mci-pause.md) depende del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fcd42-121">The difference between the MCI\_STOP and [MCI\_PAUSE](mci-pause.md) commands depends on the device.</span></span> <span data-ttu-id="fcd42-122">Si es posible, \_ la pausa de MCI suspende el funcionamiento del dispositivo pero deja el dispositivo listo para reanudar la reproducción inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="fcd42-122">If possible, MCI\_PAUSE suspends device operation but leaves the device ready to resume play immediately.</span></span>

<span data-ttu-id="fcd42-123">En el caso del dispositivo de audio de CD, MCI \_ Stop restablece la posición de pista actual a cero; por el contrario, la [ \_ pausa de MCI](mci-pause.md) mantiene la posición de pista actual, lo que prevé que el dispositivo se reanudará la reproducción.</span><span class="sxs-lookup"><span data-stu-id="fcd42-123">For the CD audio device, MCI\_STOP resets the current track position to zero; in contrast, [MCI\_PAUSE](mci-pause.md) maintains the current track position, anticipating that the device will resume playing.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcd42-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcd42-124">Requirements</span></span>



| <span data-ttu-id="fcd42-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcd42-125">Requirement</span></span> | <span data-ttu-id="fcd42-126">Value</span><span class="sxs-lookup"><span data-stu-id="fcd42-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcd42-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcd42-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fcd42-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fcd42-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fcd42-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcd42-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fcd42-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fcd42-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fcd42-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fcd42-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcd42-132"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fcd42-132"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcd42-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcd42-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcd42-134">MCI</span><span class="sxs-lookup"><span data-stu-id="fcd42-134">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="fcd42-135">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="fcd42-135">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

