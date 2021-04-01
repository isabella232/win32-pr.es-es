---
title: Comando MCI_RESUME (mmsystem. h)
description: El \_ comando de reanudación de MCI hace que un dispositivo en pausa reanude la operación en pausa.
ms.assetid: 2df712c1-5005-4e89-a439-a651076bbb73
keywords:
- Comando de MCI_RESUME de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_RESUME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd83b6d753cd223235b8b11f2d4b0be4c828ec28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996050"
---
# <a name="mci_resume-command"></a><span data-ttu-id="5b268-104">\_Comando de reanudación de MCI</span><span class="sxs-lookup"><span data-stu-id="5b268-104">MCI\_RESUME command</span></span>

<span data-ttu-id="5b268-105">El \_ comando de reanudación de MCI hace que un dispositivo en pausa reanude la operación en pausa.</span><span class="sxs-lookup"><span data-stu-id="5b268-105">The MCI\_RESUME command causes a paused device to resume the paused operation.</span></span> <span data-ttu-id="5b268-106">Los dispositivos de audio digital-vídeo, VCR y de onda y de onda reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="5b268-106">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="5b268-107">Aunque los dispositivos de audio de CD, secuenciador MIDI y VideoDisc también reconocen este comando, los controladores de dispositivos MCICDA, MCISEQ y MCIPIONR no lo admiten.</span><span class="sxs-lookup"><span data-stu-id="5b268-107">Although CD audio, MIDI sequencer, and videodisc devices also recognize this command, the MCICDA, MCISEQ, and MCIPIONR device drivers do not support it.</span></span>

<span data-ttu-id="5b268-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="5b268-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESUME, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpResume
);
```



## <a name="parameters"></a><span data-ttu-id="5b268-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b268-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b268-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="5b268-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5b268-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="5b268-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="5b268-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="5b268-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5b268-113">MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="5b268-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="5b268-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5b268-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b268-115"><span id="lpResume"></span><span id="lpresume"></span><span id="LPRESUME"></span>*lpResume*</span><span class="sxs-lookup"><span data-stu-id="5b268-115"><span id="lpResume"></span><span id="lpresume"></span><span id="LPRESUME"></span>*lpResume*</span></span>
</dt> <dd>

<span data-ttu-id="5b268-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="5b268-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="5b268-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="5b268-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b268-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b268-118">Return Value</span></span>

<span data-ttu-id="5b268-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5b268-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b268-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b268-120">Remarks</span></span>

<span data-ttu-id="5b268-121">Este comando reanuda la reproducción y grabación sin cambiar la posición de seguimiento actual establecida con [MCI \_ Play](mci-play.md) o [MCI \_ Record](mci-record.md).</span><span class="sxs-lookup"><span data-stu-id="5b268-121">This command resumes playing and recording without changing the current track position set with [MCI\_PLAY](mci-play.md) or [MCI\_RECORD](mci-record.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b268-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b268-122">Requirements</span></span>



| <span data-ttu-id="5b268-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b268-123">Requirement</span></span> | <span data-ttu-id="5b268-124">Value</span><span class="sxs-lookup"><span data-stu-id="5b268-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b268-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b268-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5b268-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5b268-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5b268-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b268-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5b268-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5b268-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5b268-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b268-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b268-130"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b268-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b268-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b268-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b268-132">MCI</span><span class="sxs-lookup"><span data-stu-id="5b268-132">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5b268-133">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="5b268-133">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

