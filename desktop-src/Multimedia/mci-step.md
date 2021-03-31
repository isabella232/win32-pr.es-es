---
title: Comando MCI_STEP (mmsystem. h)
description: El comando de paso de MCI \_ indica al reproductor uno o varios fotogramas. Los dispositivos de vídeo digital-video, VCR y CAV-Format reconocen este comando.
ms.assetid: 8d976840-fe9d-4393-b9fc-10f847166b1b
keywords:
- Comando de MCI_STEP de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_STEP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd81b3ad0e1f10c14d68df12399045149f686a8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149876"
---
# <a name="mci_step-command"></a><span data-ttu-id="1fc08-105">Comando de paso de MCI \_</span><span class="sxs-lookup"><span data-stu-id="1fc08-105">MCI\_STEP command</span></span>

<span data-ttu-id="1fc08-106">El comando de paso de MCI \_ indica al reproductor uno o varios fotogramas.</span><span class="sxs-lookup"><span data-stu-id="1fc08-106">The MCI\_STEP command steps the player one or more frames.</span></span> <span data-ttu-id="1fc08-107">Los dispositivos de vídeo digital-video, VCR y CAV-Format reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="1fc08-107">Digital-video, VCR, and CAV-format videodisc devices recognize this command.</span></span>

<span data-ttu-id="1fc08-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="1fc08-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STEP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStep
);
```



## <a name="parameters"></a><span data-ttu-id="1fc08-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1fc08-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fc08-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="1fc08-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="1fc08-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="1fc08-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="1fc08-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="1fc08-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1fc08-113">MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="1fc08-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="1fc08-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="1fc08-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc08-115"><span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*</span><span class="sxs-lookup"><span data-stu-id="1fc08-115"><span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*</span></span>
</dt> <dd>

<span data-ttu-id="1fc08-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="1fc08-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="1fc08-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="1fc08-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fc08-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1fc08-118">Return Value</span></span>

<span data-ttu-id="1fc08-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1fc08-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fc08-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1fc08-120">Remarks</span></span>

<span data-ttu-id="1fc08-121">Este comando admite dispositivos que devuelven **true** a \_ la \_ \_ marca de vídeo MCI GETDEVCAPS tiene el comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="1fc08-121">This command supports devices that return **TRUE** to the MCI\_GETDEVCAPS\_HAS\_VIDEO flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

<span data-ttu-id="1fc08-122">Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:</span><span class="sxs-lookup"><span data-stu-id="1fc08-122">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="1fc08-123"><span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>\_marcos de \_ paso de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="1fc08-123"><span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>MCI\_DGV\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="1fc08-124">El miembro **dwFrames** de la estructura identificada por *lpStep* especifica el número de fotogramas que se van a avanzar antes de mostrar otra imagen.</span><span class="sxs-lookup"><span data-stu-id="1fc08-124">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to advance before displaying another image.</span></span>

</dd> <dt>

<span data-ttu-id="1fc08-125"><span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>paso de DGV de MCI \_ \_ \_ inverso</span><span class="sxs-lookup"><span data-stu-id="1fc08-125"><span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>MCI\_DGV\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="1fc08-126">Pasos en orden inverso.</span><span class="sxs-lookup"><span data-stu-id="1fc08-126">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="1fc08-127">En el caso de los dispositivos de vídeo digital, el parámetro *lpStep* apunta a una estructura [**parms de MCI \_ DGV \_ Step \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) .</span><span class="sxs-lookup"><span data-stu-id="1fc08-127">For digital-video devices, the *lpStep* parameter points to an [**MCI\_DGV\_STEP\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) structure.</span></span>

<span data-ttu-id="1fc08-128">Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="1fc08-128">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="1fc08-129"><span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>fotogramas de VCR de MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="1fc08-129"><span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>MCI\_VCR\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="1fc08-130">El miembro **dwFrames** de la estructura identificada por *lpStep* especifica el número de fotogramas que se van a avanzar antes de mostrar otra imagen.</span><span class="sxs-lookup"><span data-stu-id="1fc08-130">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to advance before displaying another image.</span></span>

</dd> <dt>

<span data-ttu-id="1fc08-131"><span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>desplazar VCR de MCI hacia \_ \_ \_ atrás</span><span class="sxs-lookup"><span data-stu-id="1fc08-131"><span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>MCI\_VCR\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="1fc08-132">Pasos en orden inverso.</span><span class="sxs-lookup"><span data-stu-id="1fc08-132">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="1fc08-133">En el caso de los dispositivos VCR, el parámetro *lpStep* apunta a una estructura [**MCI \_ VCR \_ Step \_ parms**](mci-vcr-step-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="1fc08-133">For VCR devices, the *lpStep* parameter points to an [**MCI\_VCR\_STEP\_PARMS**](mci-vcr-step-parms.md) structure.</span></span>

<span data-ttu-id="1fc08-134">Se usan las siguientes marcas adicionales con el tipo de dispositivo de **videodisco** :</span><span class="sxs-lookup"><span data-stu-id="1fc08-134">The following additional flags are used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="1fc08-135"><span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>marcos de paso de MCI \_ Vd \_ \_</span><span class="sxs-lookup"><span data-stu-id="1fc08-135"><span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>MCI\_VD\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="1fc08-136">El miembro **dwFrames** de la estructura identificada por *lpStep* especifica el número de fotogramas que se van a recorrer.</span><span class="sxs-lookup"><span data-stu-id="1fc08-136">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to step.</span></span>

</dd> <dt>

<span data-ttu-id="1fc08-137"><span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>paso de MCI \_ Vd \_ \_ inverso</span><span class="sxs-lookup"><span data-stu-id="1fc08-137"><span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>MCI\_VD\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="1fc08-138">Pasos en orden inverso.</span><span class="sxs-lookup"><span data-stu-id="1fc08-138">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="1fc08-139">En el caso de los dispositivos de videodisco, el parámetro *lpStep* apunta a una estructura [**parms de MCI \_ Vd \_ Step \_**](mci-vd-step-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="1fc08-139">For videodisc devices, the *lpStep* parameter points to an [**MCI\_VD\_STEP\_PARMS**](mci-vd-step-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fc08-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fc08-140">Requirements</span></span>



| <span data-ttu-id="1fc08-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fc08-141">Requirement</span></span> | <span data-ttu-id="1fc08-142">Value</span><span class="sxs-lookup"><span data-stu-id="1fc08-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc08-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fc08-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1fc08-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1fc08-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1fc08-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fc08-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1fc08-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1fc08-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1fc08-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fc08-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fc08-148"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fc08-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fc08-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fc08-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fc08-150">MCI</span><span class="sxs-lookup"><span data-stu-id="1fc08-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1fc08-151">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="1fc08-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

