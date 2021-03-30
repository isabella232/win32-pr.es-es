---
title: Comando MCI_PAUSE (mmsystem. h)
description: El comando de pausa de MCI \_ detiene la acción actual. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, VCR, Videodisc y de onda-audio reconocen este comando.
ms.assetid: c4d0b0a2-cd7b-4641-a318-eb4b4e88b70f
keywords:
- Comando de MCI_PAUSE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_PAUSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076397ca9ab770d6f9c23cc5b64853bdd2f07ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801016"
---
# <a name="mci_pause-command"></a><span data-ttu-id="f9be1-105">Comando de pausa de MCI \_</span><span class="sxs-lookup"><span data-stu-id="f9be1-105">MCI\_PAUSE command</span></span>

<span data-ttu-id="f9be1-106">El comando de pausa de MCI \_ detiene la acción actual.</span><span class="sxs-lookup"><span data-stu-id="f9be1-106">The MCI\_PAUSE command pauses the current action.</span></span> <span data-ttu-id="f9be1-107">Los dispositivos de audio de CD, digital-video, MIDI Sequencer, VCR, Videodisc y de onda-audio reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="f9be1-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="f9be1-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="f9be1-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PAUSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpPause
);
```



## <a name="parameters"></a><span data-ttu-id="f9be1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9be1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9be1-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f9be1-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f9be1-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="f9be1-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="f9be1-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f9be1-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f9be1-113">MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="f9be1-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="f9be1-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f9be1-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9be1-115"><span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lpPause*</span><span class="sxs-lookup"><span data-stu-id="f9be1-115"><span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lpPause*</span></span>
</dt> <dd>

<span data-ttu-id="f9be1-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f9be1-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="f9be1-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="f9be1-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9be1-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9be1-118">Return Value</span></span>

<span data-ttu-id="f9be1-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f9be1-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9be1-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9be1-120">Remarks</span></span>

<span data-ttu-id="f9be1-121">La diferencia entre los comandos [MCI \_ Stop](mci-stop.md) y MCI \_ PAUSE depende del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9be1-121">The difference between the [MCI\_STOP](mci-stop.md) and MCI\_PAUSE commands depends on the device.</span></span> <span data-ttu-id="f9be1-122">Si es posible, \_ la pausa de MCI suspende el funcionamiento del dispositivo pero deja el dispositivo listo para reanudar la reproducción inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f9be1-122">If possible, MCI\_PAUSE suspends device operation but leaves the device ready to resume play immediately.</span></span> <span data-ttu-id="f9be1-123">Con los controladores MCICDA, MCISEQ y MCIPIONR, el comando de \_ pausa de MCI funciona igual que el comando de detención de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="f9be1-123">With the MCICDA, MCISEQ, and MCIPIONR drivers, the MCI\_PAUSE command works the same as the MCI\_STOP command.</span></span>

<span data-ttu-id="f9be1-124">En el caso de los dispositivos de vídeo digital, el parámetro *lpPause* apunta a una estructura [**MCI \_ DGV \_ PAUSE \_ parms**](/previous-versions//dd743395(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f9be1-124">For digital-video devices, the *lpPause* parameter points to an [**MCI\_DGV\_PAUSE\_PARMS**](/previous-versions//dd743395(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9be1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9be1-125">Requirements</span></span>



| <span data-ttu-id="f9be1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9be1-126">Requirement</span></span> | <span data-ttu-id="f9be1-127">Value</span><span class="sxs-lookup"><span data-stu-id="f9be1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9be1-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9be1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f9be1-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f9be1-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f9be1-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9be1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f9be1-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f9be1-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f9be1-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9be1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9be1-133"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9be1-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9be1-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9be1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9be1-135">MCI</span><span class="sxs-lookup"><span data-stu-id="f9be1-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f9be1-136">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="f9be1-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

