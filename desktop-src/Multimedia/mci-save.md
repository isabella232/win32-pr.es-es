---
title: Comando MCI_SAVE (mmsystem. h)
description: El \_ comando MCI Save guarda el archivo actual.
ms.assetid: 286e6f31-cb93-443b-8191-8c363b366eae
keywords:
- Comando de MCI_SAVE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SAVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a241c0379731e870940cd676c33ae192efc5d297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489586"
---
# <a name="mci_save-command"></a><span data-ttu-id="3c95e-104">Comando de guardado de MCI \_</span><span class="sxs-lookup"><span data-stu-id="3c95e-104">MCI\_SAVE command</span></span>

<span data-ttu-id="3c95e-105">El \_ comando MCI Save guarda el archivo actual.</span><span class="sxs-lookup"><span data-stu-id="3c95e-105">The MCI\_SAVE command saves the current file.</span></span> <span data-ttu-id="3c95e-106">Los dispositivos que modifican archivos no deben destruir la copia original hasta que reciban el mensaje de guardado.</span><span class="sxs-lookup"><span data-stu-id="3c95e-106">Devices that modify files should not destroy the original copy until they receive the save message.</span></span> <span data-ttu-id="3c95e-107">Los dispositivos de audio y la superposición de vídeo y de onda reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="3c95e-107">Video-overlay and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="3c95e-108">Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo implementan.</span><span class="sxs-lookup"><span data-stu-id="3c95e-108">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="3c95e-109">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="3c95e-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SAVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SAVE_PARMS ) lpSave
);
```



## <a name="parameters"></a><span data-ttu-id="3c95e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c95e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c95e-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="3c95e-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="3c95e-112">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="3c95e-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="3c95e-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="3c95e-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3c95e-114">MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="3c95e-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="3c95e-115">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="3c95e-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c95e-116"><span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*</span><span class="sxs-lookup"><span data-stu-id="3c95e-116"><span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*</span></span>
</dt> <dd>

<span data-ttu-id="3c95e-117">Puntero a una [**estructura \_ \_ parms de guardado de MCI**](mci-save-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="3c95e-117">Pointer to an [**MCI\_SAVE\_PARMS**](mci-save-parms.md) structure.</span></span> <span data-ttu-id="3c95e-118">(Los dispositivos con parámetros adicionales podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="3c95e-118">(Devices with additional parameters might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c95e-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c95e-119">Return Value</span></span>

<span data-ttu-id="3c95e-120">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3c95e-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c95e-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c95e-121">Remarks</span></span>

<span data-ttu-id="3c95e-122">Este comando es compatible con los dispositivos que devuelven **true** cuando se llama al comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con el \_ marcador MCI GETDEVCAPS \_ Can \_ Save.</span><span class="sxs-lookup"><span data-stu-id="3c95e-122">This command is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_CAN\_SAVE flag.</span></span>

<span data-ttu-id="3c95e-123">La marca adicional siguiente se aplica a todos los dispositivos que admiten el [ \_ guardado de MCI](/windows):</span><span class="sxs-lookup"><span data-stu-id="3c95e-123">The following additional flag applies to all devices supporting [MCI\_SAVE](/windows):</span></span>

<dl> <dt>

<span data-ttu-id="3c95e-124"><span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>\_Guardar \_ archivo MCI</span><span class="sxs-lookup"><span data-stu-id="3c95e-124"><span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>MCI\_SAVE\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="3c95e-125">El miembro **lpfilename** de la estructura identificada por *lpSave* contiene una dirección de un búfer que contiene el nombre de archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="3c95e-125">The **lpfilename** member of the structure identified by *lpSave* contains an address of a buffer containing the destination filename.</span></span>

</dd> </dl>

<span data-ttu-id="3c95e-126">Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:</span><span class="sxs-lookup"><span data-stu-id="3c95e-126">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="3c95e-127"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV \_ Rect</span><span class="sxs-lookup"><span data-stu-id="3c95e-127"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="3c95e-128">El miembro **RC** de la estructura identificada por *lpSave* contiene un rectángulo válido.</span><span class="sxs-lookup"><span data-stu-id="3c95e-128">The **rc** member of the structure identified by *lpSave* contains a valid rectangle.</span></span> <span data-ttu-id="3c95e-129">El rectángulo especifica una región del búfer de fotogramas que se guardará en el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="3c95e-129">The rectangle specifies a region of the frame buffer that will be saved to the specified file.</span></span> <span data-ttu-id="3c95e-130">El primer par de coordenadas especifica la esquina superior izquierda del rectángulo; el segundo par especifica el ancho y el alto.</span><span class="sxs-lookup"><span data-stu-id="3c95e-130">The first pair of coordinates specifies the upper left corner of the rectangle; the second pair specifies the width and height.</span></span> <span data-ttu-id="3c95e-131">Los dispositivos de vídeo digital deben usar el comando [MCI \_ Capture](mci-capture.md) para capturar el contenido del búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="3c95e-131">Digital-video devices must use the [MCI\_CAPTURE](mci-capture.md) command to capture the contents of the frame buffer.</span></span> <span data-ttu-id="3c95e-132">(Los dispositivos de superposición de vídeo también deben usar MCI \_ ) CAPTURE). Esta marca es por compatibilidad con el conjunto de comandos de vídeo superposición de MCI existente.</span><span class="sxs-lookup"><span data-stu-id="3c95e-132">(Video-overlay devices should also use MCI\_CAPTURE.) This flag is for compatibility with the existing MCI video-overlay command set.</span></span>

</dd> <dt>

<span data-ttu-id="3c95e-133"><span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>\_DGV de \_ almacenamiento de MCI \_</span><span class="sxs-lookup"><span data-stu-id="3c95e-133"><span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>MCI\_DGV\_SAVE\_ABORT</span></span>
</dt> <dd>

<span data-ttu-id="3c95e-134">Detiene una operación de guardar en curso.</span><span class="sxs-lookup"><span data-stu-id="3c95e-134">Stops a save operation in progress.</span></span> <span data-ttu-id="3c95e-135">Debe ser la única marca presente.</span><span class="sxs-lookup"><span data-stu-id="3c95e-135">This must be the only flag present.</span></span>

</dd> <dt>

<span data-ttu-id="3c95e-136"><span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI \_ DGV \_ Save \_ KEEPRESERVE</span><span class="sxs-lookup"><span data-stu-id="3c95e-136"><span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI\_DGV\_SAVE\_KEEPRESERVE</span></span>
</dt> <dd>

<span data-ttu-id="3c95e-137">No se cancela la asignación del espacio en disco que queda sin usar desde el comando de [ \_ reserva de MCI](mci-reserve.md) original.</span><span class="sxs-lookup"><span data-stu-id="3c95e-137">Unused disk space left over from the original [MCI\_RESERVE](mci-reserve.md) command is not deallocated.</span></span>

</dd> </dl>

<span data-ttu-id="3c95e-138">En el caso de los dispositivos de vídeo digital, el parámetro *lpSave* apunta a una estructura [**MCI \_ DGV \_ Save \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="3c95e-138">For digital-video devices, the *lpSave* parameter points to an [**MCI\_DGV\_SAVE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) structure.</span></span>

<span data-ttu-id="3c95e-139">La siguiente marca adicional se usa con el tipo de dispositivo **superpuesto** :</span><span class="sxs-lookup"><span data-stu-id="3c95e-139">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="3c95e-140"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect</span><span class="sxs-lookup"><span data-stu-id="3c95e-140"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="3c95e-141">El miembro **RC** de la estructura identificada por *lpSave* contiene un rectángulo de presentación válido que indica el área del búfer de vídeo que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="3c95e-141">The **rc** member of the structure identified by *lpSave* contains a valid display rectangle indicating the area of the video buffer to save.</span></span>

</dd> </dl>

<span data-ttu-id="3c95e-142">En el caso de los dispositivos de superposición de vídeo, el parámetro *lpSave* apunta a una estructura [**MCI \_ OVLY \_ Save \_ parms**](/previous-versions//dd743447(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3c95e-142">For video-overlay devices, the *lpSave* parameter points to an [**MCI\_OVLY\_SAVE\_PARMS**](/previous-versions//dd743447(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c95e-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c95e-143">Requirements</span></span>



| <span data-ttu-id="3c95e-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c95e-144">Requirement</span></span> | <span data-ttu-id="3c95e-145">Value</span><span class="sxs-lookup"><span data-stu-id="3c95e-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c95e-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c95e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="3c95e-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3c95e-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3c95e-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c95e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="3c95e-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3c95e-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3c95e-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c95e-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c95e-151"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c95e-151"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c95e-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c95e-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c95e-153">MCI</span><span class="sxs-lookup"><span data-stu-id="3c95e-153">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3c95e-154">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="3c95e-154">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

