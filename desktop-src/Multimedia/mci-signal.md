---
title: Comando MCI_SIGNAL (mmsystem. h)
description: El \_ comando MCI Signal establece una posición especificada en el área de trabajo. Los dispositivos de vídeo digital reconocen este comando. MCIAVI solo admite una señal activa a la vez.
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- Comando de MCI_SIGNAL de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711238d73ee40f5809f15a2d6df93183fb17bf67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422222"
---
# <a name="mci_signal-command"></a><span data-ttu-id="21673-106">Comando de señal de MCI \_</span><span class="sxs-lookup"><span data-stu-id="21673-106">MCI\_SIGNAL command</span></span>

<span data-ttu-id="21673-107">El \_ comando MCI Signal establece una posición especificada en el área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="21673-107">The MCI\_SIGNAL command sets a specified position in the workspace.</span></span> <span data-ttu-id="21673-108">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="21673-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="21673-109">MCIAVI solo admite una señal activa a la vez.</span><span class="sxs-lookup"><span data-stu-id="21673-109">MCIAVI supports only one active signal at a time.</span></span>

<span data-ttu-id="21673-110">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="21673-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SIGNAL, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_SIGNAL_PARMS) lpSignal
);
```



## <a name="parameters"></a><span data-ttu-id="21673-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21673-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21673-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="21673-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="21673-113">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="21673-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="21673-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="21673-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="21673-115">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="21673-115">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="21673-116">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="21673-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="21673-117"><span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*</span><span class="sxs-lookup"><span data-stu-id="21673-117"><span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*</span></span>
</dt> <dd>

<span data-ttu-id="21673-118">Puntero a una estructura de parms de DGV de la [**\_ \_ señal \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) .</span><span class="sxs-lookup"><span data-stu-id="21673-118">Pointer to an [**MCI\_DGV\_SIGNAL\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21673-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21673-119">Return Value</span></span>

<span data-ttu-id="21673-120">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="21673-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="21673-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21673-121">Remarks</span></span>

<span data-ttu-id="21673-122">La ventana cuyo identificador se especifica en el miembro **dwCallback** de la estructura [**MCI \_ DGV \_ Signal \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) recibe el mensaje mm \_ MCISIGNAL.</span><span class="sxs-lookup"><span data-stu-id="21673-122">The window whose handle you specify in the **dwCallback** member of the [**MCI\_DGV\_SIGNAL\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) structure receives the MM\_MCISIGNAL message.</span></span>

<span data-ttu-id="21673-123">Las marcas siguientes se aplican a los dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="21673-123">The following flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="21673-124"><span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>\_ \_ señal de MCI DGV \_ en</span><span class="sxs-lookup"><span data-stu-id="21673-124"><span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>MCI\_DGV\_SIGNAL\_AT</span></span>
</dt> <dd>

<span data-ttu-id="21673-125">Una posición de la señal se incluye en el miembro **dwPosition** de la estructura identificada por *lpSignal*.</span><span class="sxs-lookup"><span data-stu-id="21673-125">A signal position is included in the **dwPosition** member of the structure identified by *lpSignal*.</span></span>

</dd> <dt>

<span data-ttu-id="21673-126"><span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>\_cancelación de \_ señal de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="21673-126"><span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>MCI\_DGV\_SIGNAL\_CANCEL</span></span>
</dt> <dd>

<span data-ttu-id="21673-127">Quita la posición de la señal especificada por el valor asociado a MCI \_ DGV \_ Signal \_ USERVAL.</span><span class="sxs-lookup"><span data-stu-id="21673-127">Removes the signal position specified by the value associated with MCI\_DGV\_SIGNAL\_USERVAL.</span></span>

</dd> <dt>

<span data-ttu-id="21673-128"><span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>señal de MCI \_ DGV \_ \_ cada</span><span class="sxs-lookup"><span data-stu-id="21673-128"><span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>MCI\_DGV\_SIGNAL\_EVERY</span></span>
</dt> <dd>

<span data-ttu-id="21673-129">Un valor de período de señal se incluye en el miembro **dwPeriod** de la estructura identificada por *lpSignal*.</span><span class="sxs-lookup"><span data-stu-id="21673-129">A signal-period value is included in the **dwPeriod** member of the structure identified by *lpSignal*.</span></span>

</dd> <dt>

<span data-ttu-id="21673-130"><span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>posición de la señal de MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="21673-130"><span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>MCI\_DGV\_SIGNAL\_POSITION</span></span>
</dt> <dd>

<span data-ttu-id="21673-131">El dispositivo enviará el valor de posición con el mensaje de Windows en lugar del valor especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="21673-131">The device will send the position value with the Windows message instead of the user-specified value.</span></span>

</dd> <dt>

<span data-ttu-id="21673-132"><span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>\_USERVAL de \_ señal MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="21673-132"><span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>MCI\_DGV\_SIGNAL\_USERVAL</span></span>
</dt> <dd>

<span data-ttu-id="21673-133">Un valor de datos se incluye en el miembro **dwUserParm** de la estructura identificada por *lpSignal*.</span><span class="sxs-lookup"><span data-stu-id="21673-133">A data value is included in the **dwUserParm** member of the structure identified by *lpSignal*.</span></span> <span data-ttu-id="21673-134">El valor de datos asociado a esta solicitud se devuelve con el mensaje de Windows.</span><span class="sxs-lookup"><span data-stu-id="21673-134">The data value associated with this request is reported back with the Windows message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21673-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21673-135">Requirements</span></span>



| <span data-ttu-id="21673-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="21673-136">Requirement</span></span> | <span data-ttu-id="21673-137">Value</span><span class="sxs-lookup"><span data-stu-id="21673-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21673-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21673-138">Minimum supported client</span></span><br/> | <span data-ttu-id="21673-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="21673-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="21673-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21673-140">Minimum supported server</span></span><br/> | <span data-ttu-id="21673-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="21673-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="21673-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21673-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="21673-143"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21673-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21673-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="21673-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21673-145">MCI</span><span class="sxs-lookup"><span data-stu-id="21673-145">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="21673-146">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="21673-146">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

