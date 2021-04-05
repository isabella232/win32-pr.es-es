---
title: Comando MCI_FREEZE (mmsystem. h)
description: El \_ comando MCI Freeze inmoviliza el movimiento en la pantalla. Los dispositivos digitales-vídeo, superposición de vídeo y VCR reconocen este comando.
ms.assetid: 6f90984a-24dc-4046-8234-986b2125bab4
keywords:
- Comando de MCI_FREEZE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_FREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705117aef85fe69382657c647240849b515afa07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079066"
---
# <a name="mci_freeze-command"></a><span data-ttu-id="c5225-105">\_Comando MCI Freeze</span><span class="sxs-lookup"><span data-stu-id="c5225-105">MCI\_FREEZE command</span></span>

<span data-ttu-id="c5225-106">El \_ comando MCI Freeze inmoviliza el movimiento en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="c5225-106">The MCI\_FREEZE command freezes motion on the display.</span></span> <span data-ttu-id="c5225-107">Los dispositivos digitales-vídeo, superposición de vídeo y VCR reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="c5225-107">Digital-video, video-overlay, and VCR devices recognize this command.</span></span>

<span data-ttu-id="c5225-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="c5225-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_FREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpFreeze
);
```



## <a name="parameters"></a><span data-ttu-id="c5225-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5225-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5225-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c5225-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c5225-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="c5225-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="c5225-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c5225-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c5225-113">MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="c5225-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="c5225-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c5225-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5225-115"><span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*</span><span class="sxs-lookup"><span data-stu-id="c5225-115"><span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*</span></span>
</dt> <dd>

<span data-ttu-id="c5225-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="c5225-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="c5225-117">(Los dispositivos con parámetros adicionales podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="c5225-117">(Devices with additional parameters might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5225-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5225-118">Return Value</span></span>

<span data-ttu-id="c5225-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c5225-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5225-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5225-120">Remarks</span></span>

<span data-ttu-id="c5225-121">El tipo de dispositivo **DigitalVideo** usa las siguientes marcas adicionales:</span><span class="sxs-lookup"><span data-stu-id="c5225-121">The following additional flags are used by the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="c5225-122"><span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>\_DGV \_ de MCI congelado \_ en</span><span class="sxs-lookup"><span data-stu-id="c5225-122"><span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>MCI\_DGV\_FREEZE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="c5225-123">El miembro **RC** de la estructura identificada por *lpFreeze* contiene un rectángulo válido.</span><span class="sxs-lookup"><span data-stu-id="c5225-123">The **rc** member of the structure identified by *lpFreeze* contains a valid rectangle.</span></span> <span data-ttu-id="c5225-124">El rectángulo especifica una región en el búfer de fotogramas que tendrá el bit de máscara de bloqueo para cada píxel activado.</span><span class="sxs-lookup"><span data-stu-id="c5225-124">The rectangle specifies a region within the frame buffer that will have the lock mask bit for each pixel turned on.</span></span> <span data-ttu-id="c5225-125">Los píxeles especificados no se actualizarán hasta que el bit de la máscara de bloqueo esté desactivado.</span><span class="sxs-lookup"><span data-stu-id="c5225-125">The specified pixels will not be updated until their lock mask bit is turned off.</span></span> <span data-ttu-id="c5225-126">Si no se especifica esta marca, el rectángulo tiene como valor predeterminado el búfer de fotogramas completo.</span><span class="sxs-lookup"><span data-stu-id="c5225-126">If this flag is not specified, the rectangle defaults to the entire frame buffer.</span></span> <span data-ttu-id="c5225-127">Esta marca solo se admite si el comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) devuelve **true** para la \_ marca MCI DGV \_ GETDEVCAPS \_ Can \_ Lock.</span><span class="sxs-lookup"><span data-stu-id="c5225-127">This flag is supported only if the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command returns **TRUE** for the MCI\_DGV\_GETDEVCAPS\_CAN\_LOCK flag.</span></span>

</dd> <dt>

<span data-ttu-id="c5225-128"><span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>desbloqueo de DGV de MCI \_ \_ \_ fuera de</span><span class="sxs-lookup"><span data-stu-id="c5225-128"><span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>MCI\_DGV\_FREEZE\_OUTSIDE</span></span>
</dt> <dd>

<span data-ttu-id="c5225-129">El área fuera de la región especificada para la \_ marca MCI DGV \_ Freeze \_ at está inmovilizada.</span><span class="sxs-lookup"><span data-stu-id="c5225-129">The area outside the region specified for the MCI\_DGV\_FREEZE\_AT flag is frozen.</span></span>

</dd> </dl>

<span data-ttu-id="c5225-130">En el caso de los dispositivos de vídeo digital, el parámetro *lpFreeze* apunta a una estructura de [**\_ DGV \_ Freeze \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) .</span><span class="sxs-lookup"><span data-stu-id="c5225-130">For digital-video devices, the *lpFreeze* parameter points to an [**MCI\_DGV\_FREEZE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="c5225-131">El tipo de dispositivo **VCR** usa las siguientes marcas adicionales:</span><span class="sxs-lookup"><span data-stu-id="c5225-131">The following additional flags are used by the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="c5225-132"><span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>\_campo MCI VCR \_ Freeze \_</span><span class="sxs-lookup"><span data-stu-id="c5225-132"><span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>MCI\_VCR\_FREEZE\_FIELD</span></span>
</dt> <dd>

<span data-ttu-id="c5225-133">Inmoviliza solo un miembro del marco actual.</span><span class="sxs-lookup"><span data-stu-id="c5225-133">Freeze only one member of the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="c5225-134"><span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>\_marco de \_ desbloqueo de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="c5225-134"><span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>MCI\_VCR\_FREEZE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="c5225-135">Inmoviliza ambos campos del marco actual.</span><span class="sxs-lookup"><span data-stu-id="c5225-135">Freeze both fields of the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="c5225-136"><span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>\_entrada de \_ inmovilización de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="c5225-136"><span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>MCI\_VCR\_FREEZE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="c5225-137">Inmoviliza el marco actual en la pantalla (se usa para la grabación).</span><span class="sxs-lookup"><span data-stu-id="c5225-137">Freeze the current frame on the screen (used for recording).</span></span>

</dd> <dt>

<span data-ttu-id="c5225-138"><span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>\_salida de \_ desbloqueo de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="c5225-138"><span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>MCI\_VCR\_FREEZE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="c5225-139">Inmovilizar el fotograma actual del VCR (usado con la captura de fotogramas).</span><span class="sxs-lookup"><span data-stu-id="c5225-139">Freeze the current frame from the VCR (used with frame capture).</span></span>

</dd> </dl>

<span data-ttu-id="c5225-140">En el caso de los dispositivos VCR, el parámetro *lpFreeze* apunta a una estructura [**\_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="c5225-140">For VCR devices, the *lpFreeze* parameter points to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span>

<span data-ttu-id="c5225-141">El tipo de dispositivo **superpuesto** usa la siguiente marca adicional:</span><span class="sxs-lookup"><span data-stu-id="c5225-141">The following additional flag is used by the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="c5225-142"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect</span><span class="sxs-lookup"><span data-stu-id="c5225-142"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="c5225-143">El miembro **RC** de la estructura identificada por *lpFreeze* contiene un rectángulo válido.</span><span class="sxs-lookup"><span data-stu-id="c5225-143">The **rc** member of the structure identified by *lpFreeze* contains a valid rectangle.</span></span> <span data-ttu-id="c5225-144">Si no se especifica esta marca, el controlador de dispositivo inmovilizará todo el marco.</span><span class="sxs-lookup"><span data-stu-id="c5225-144">If this flag is not specified, the device driver will freeze the entire frame.</span></span>

</dd> </dl>

<span data-ttu-id="c5225-145">En el caso de los dispositivos de superposición de vídeo, el parámetro *lpFreeze* apunta a una estructura [**MCI \_ OVLY \_ Rect \_ parms**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="c5225-145">For video-overlay devices, the *lpFreeze* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5225-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5225-146">Requirements</span></span>



| <span data-ttu-id="c5225-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5225-147">Requirement</span></span> | <span data-ttu-id="c5225-148">Value</span><span class="sxs-lookup"><span data-stu-id="c5225-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5225-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5225-149">Minimum supported client</span></span><br/> | <span data-ttu-id="c5225-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c5225-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c5225-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5225-151">Minimum supported server</span></span><br/> | <span data-ttu-id="c5225-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c5225-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c5225-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5225-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5225-154"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5225-154"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5225-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5225-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5225-156">MCI</span><span class="sxs-lookup"><span data-stu-id="c5225-156">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c5225-157">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="c5225-157">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

