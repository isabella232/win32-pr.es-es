---
title: Comando MCI_UNFREEZE (mmsystem. h)
description: El \_ comando MCI unfreeze restaura el movimiento en un área del búfer de vídeo inmovilizado con el \_ comando MCI Freeze. Los dispositivos digitales-vídeo, VCR y superposición de vídeo reconocen este comando.
ms.assetid: 79ff1be5-6e30-4ef4-ab81-fc5643e3a72d
keywords:
- Comando de MCI_UNFREEZE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_UNFREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8736e27998330f9337bb21569e145a4395e90020
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151030"
---
# <a name="mci_unfreeze-command"></a><span data-ttu-id="d8bcb-105">\_Comando MCI UNfreeze</span><span class="sxs-lookup"><span data-stu-id="d8bcb-105">MCI\_UNFREEZE command</span></span>

<span data-ttu-id="d8bcb-106">El \_ comando MCI unfreeze restaura el movimiento en un área del búfer de vídeo inmovilizado con el comando [MCI \_ Freeze](mci-freeze.md) .</span><span class="sxs-lookup"><span data-stu-id="d8bcb-106">The MCI\_UNFREEZE command restores motion to an area of the video buffer frozen with the [MCI\_FREEZE](mci-freeze.md) command.</span></span> <span data-ttu-id="d8bcb-107">Los dispositivos digitales-vídeo, VCR y superposición de vídeo reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="d8bcb-107">Digital-video, VCR, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="d8bcb-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="d8bcb-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNFREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUnfreeze
);
```



## <a name="parameters"></a><span data-ttu-id="d8bcb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8bcb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8bcb-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d8bcb-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d8bcb-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="d8bcb-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="d8bcb-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d8bcb-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d8bcb-113">MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="d8bcb-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="d8bcb-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d8bcb-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8bcb-115"><span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*</span><span class="sxs-lookup"><span data-stu-id="d8bcb-115"><span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*</span></span>
</dt> <dd>

<span data-ttu-id="d8bcb-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="d8bcb-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="d8bcb-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="d8bcb-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8bcb-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8bcb-118">Return Value</span></span>

<span data-ttu-id="d8bcb-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d8bcb-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8bcb-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8bcb-120">Remarks</span></span>

<span data-ttu-id="d8bcb-121">Con el tipo de dispositivo **DigitalVideo** se usa la siguiente marca adicional:</span><span class="sxs-lookup"><span data-stu-id="d8bcb-121">The following additional flag is used with the **digitalvideo** device type:</span></span>

<span data-ttu-id="d8bcb-122">\_DGV \_ Rect</span><span class="sxs-lookup"><span data-stu-id="d8bcb-122">MCI\_DGV\_RECT</span></span>

<span data-ttu-id="d8bcb-123">El miembro **RC** de la estructura identificada por *lpUnfreeze* contiene un rectángulo de presentación válido.</span><span class="sxs-lookup"><span data-stu-id="d8bcb-123">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="d8bcb-124">El rectángulo especifica una región en el búfer de fotogramas cuyos píxeles deben tener el bit de máscara de bloqueo desactivado.</span><span class="sxs-lookup"><span data-stu-id="d8bcb-124">The rectangle specifies a region within the frame buffer whose pixels should have their lock mask bit turned off.</span></span> <span data-ttu-id="d8bcb-125">Las regiones rectangulares se especifican como se describe en el comando [MCI \_ Put](mci-put.md) .</span><span class="sxs-lookup"><span data-stu-id="d8bcb-125">Rectangular regions are specified as described for the [MCI\_PUT](mci-put.md) command.</span></span> <span data-ttu-id="d8bcb-126">Si se omite, el rectángulo tiene como valor predeterminado el búfer de fotogramas completo.</span><span class="sxs-lookup"><span data-stu-id="d8bcb-126">If omitted, the rectangle defaults to the entire frame buffer.</span></span> <span data-ttu-id="d8bcb-127">Mediante el uso de una secuencia de comandos Freeze y unfreeze con distintos rectángulos, se pueden describir patrones arbitrarios de bits de máscara de bloqueos.</span><span class="sxs-lookup"><span data-stu-id="d8bcb-127">By using a sequence of freeze and unfreeze commands with different rectangles, arbitrary patterns of lock mask bits can be described.</span></span>

<span data-ttu-id="d8bcb-128">En el caso de los dispositivos de vídeo digital, el parámetro *lpUnfreeze* apunta a una estructura **\_ DGV \_ unfreeze \_ parms de MCI** .</span><span class="sxs-lookup"><span data-stu-id="d8bcb-128">For digital-video devices, the *lpUnfreeze* parameter points to an **MCI\_DGV\_UNFREEZE\_PARMS** structure.</span></span> <span data-ttu-id="d8bcb-129">Para obtener más información, vea los comentarios de la estructura [**MCI \_ DGV \_ Rect \_ parms**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .</span><span class="sxs-lookup"><span data-stu-id="d8bcb-129">For more information, see the comments for the [**MCI\_DGV\_RECT\_PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="d8bcb-130">Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="d8bcb-130">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="d8bcb-131"><span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>\_entrada de \_ desbloqueo de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="d8bcb-131"><span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>MCI\_VCR\_UNFREEZE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="d8bcb-132">Libere la entrada.</span><span class="sxs-lookup"><span data-stu-id="d8bcb-132">Unfreeze the input.</span></span>

</dd> <dt>

<span data-ttu-id="d8bcb-133"><span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>\_salida de \_ desbloqueo de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="d8bcb-133"><span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>MCI\_VCR\_UNFREEZE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="d8bcb-134">Libere la salida.</span><span class="sxs-lookup"><span data-stu-id="d8bcb-134">Unfreeze the output.</span></span>

</dd> </dl>

<span data-ttu-id="d8bcb-135">La siguiente marca adicional se usa con el tipo de dispositivo **superpuesto** :</span><span class="sxs-lookup"><span data-stu-id="d8bcb-135">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="d8bcb-136"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect</span><span class="sxs-lookup"><span data-stu-id="d8bcb-136"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="d8bcb-137">El miembro **RC** de la estructura identificada por *lpUnfreeze* contiene un rectángulo de presentación válido.</span><span class="sxs-lookup"><span data-stu-id="d8bcb-137">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="d8bcb-138">Es un parámetro obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d8bcb-138">This is a required parameter.</span></span>

</dd> </dl>

<span data-ttu-id="d8bcb-139">En el caso de los dispositivos de superposición de vídeo, el parámetro *lpUnfreeze* apunta a una estructura [**MCI \_ OVLY \_ Rect \_ parms**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="d8bcb-139">For video-overlay devices, the *lpUnfreeze* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8bcb-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8bcb-140">Requirements</span></span>



| <span data-ttu-id="d8bcb-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8bcb-141">Requirement</span></span> | <span data-ttu-id="d8bcb-142">Value</span><span class="sxs-lookup"><span data-stu-id="d8bcb-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8bcb-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8bcb-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d8bcb-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d8bcb-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d8bcb-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8bcb-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d8bcb-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d8bcb-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d8bcb-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8bcb-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8bcb-148"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8bcb-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8bcb-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8bcb-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8bcb-150">MCI</span><span class="sxs-lookup"><span data-stu-id="d8bcb-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d8bcb-151">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="d8bcb-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

