---
title: Comando MCI_PUT (mmsystem. h)
description: El \_ comando MCI Put establece los rectángulos de origen, de destino y de marco. Los dispositivos de vídeo digital y de superposición reconocen este comando.
ms.assetid: 9d81682b-6546-4e6d-a6df-e2de8c013b66
keywords:
- Comando de MCI_PUT de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_PUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fa4af30aa2b3aa6f7cdd50f453bc8edca83334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151238"
---
# <a name="mci_put-command"></a><span data-ttu-id="787ae-105">\_Comando MCI Put</span><span class="sxs-lookup"><span data-stu-id="787ae-105">MCI\_PUT command</span></span>

<span data-ttu-id="787ae-106">El \_ comando MCI Put establece los rectángulos de origen, de destino y de marco.</span><span class="sxs-lookup"><span data-stu-id="787ae-106">The MCI\_PUT command sets the source, destination, and frame rectangles.</span></span> <span data-ttu-id="787ae-107">Los dispositivos de vídeo digital y de superposición reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="787ae-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="787ae-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="787ae-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
);
```



## <a name="parameters"></a><span data-ttu-id="787ae-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="787ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="787ae-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="787ae-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="787ae-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="787ae-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="787ae-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="787ae-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="787ae-113">\_La notificación de MCI, la espera de MCI \_ o, para dispositivos de vídeo digital, la prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="787ae-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="787ae-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="787ae-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="787ae-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span><span class="sxs-lookup"><span data-stu-id="787ae-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span></span>
</dt> <dd>

<span data-ttu-id="787ae-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="787ae-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="787ae-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="787ae-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="787ae-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="787ae-118">Return Value</span></span>

<span data-ttu-id="787ae-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="787ae-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="787ae-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="787ae-120">Remarks</span></span>

<span data-ttu-id="787ae-121">Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:</span><span class="sxs-lookup"><span data-stu-id="787ae-121">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="787ae-122"><span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>\_cliente de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="787ae-122"><span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>MCI\_DGV\_PUT\_CLIENT</span></span>
</dt> <dd>

<span data-ttu-id="787ae-123">El rectángulo definido para MCI \_ DGV \_ Rect se aplica a la posición de la ventana del cliente.</span><span class="sxs-lookup"><span data-stu-id="787ae-123">The rectangle defined for MCI\_DGV\_RECT applies to the position of the client window.</span></span> <span data-ttu-id="787ae-124">El rectángulo especificado es relativo a la ventana primaria de la ventana de presentación.</span><span class="sxs-lookup"><span data-stu-id="787ae-124">The rectangle specified is relative to the parent window of the display window.</span></span> <span data-ttu-id="787ae-125">\_ \_ \_ La ventana de colocación de MCI DGV debe establecerse simultáneamente con esta marca.</span><span class="sxs-lookup"><span data-stu-id="787ae-125">MCI\_DGV\_PUT\_WINDOW must be set concurrently with this flag.</span></span>

</dd> <dt>

<span data-ttu-id="787ae-126"><span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>\_ \_ destino put de MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="787ae-126"><span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>MCI\_DGV\_PUT\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="787ae-127">El rectángulo definido para MCI \_ DGV \_ Rect especifica un rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="787ae-127">The rectangle defined for MCI\_DGV\_RECT specifies a destination rectangle.</span></span> <span data-ttu-id="787ae-128">El rectángulo de destino especifica la parte de la ventana de cliente asociada a esta instancia de controlador de dispositivo que muestra la imagen o el vídeo.</span><span class="sxs-lookup"><span data-stu-id="787ae-128">The destination rectangle specifies the portion of the client window associated with this device driver instance that shows the image or video.</span></span>

</dd> <dt>

<span data-ttu-id="787ae-129"><span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>fotograma de DGV de MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="787ae-129"><span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>MCI\_DGV\_PUT\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="787ae-130">El rectángulo definido para MCI \_ DGV \_ Rect se aplica al rectángulo del marco.</span><span class="sxs-lookup"><span data-stu-id="787ae-130">The rectangle defined for MCI\_DGV\_RECT applies to the frame rectangle.</span></span> <span data-ttu-id="787ae-131">El rectángulo de marco especifica la parte del búfer de fotogramas que se usa como destino de las imágenes de vídeo obtenidas del rectángulo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="787ae-131">The frame rectangle specifies the portion of the frame buffer used as the destination of the video images obtained from the video rectangle.</span></span> <span data-ttu-id="787ae-132">El vídeo se debe escalar para ajustarse al rectángulo de búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="787ae-132">The video should be scaled to fit within the frame buffer rectangle.</span></span>

<span data-ttu-id="787ae-133">El rectángulo se especifica en coordenadas de búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="787ae-133">The rectangle is specified in frame buffer coordinates.</span></span> <span data-ttu-id="787ae-134">El rectángulo predeterminado es el búfer de marco completo.</span><span class="sxs-lookup"><span data-stu-id="787ae-134">The default rectangle is the full frame buffer.</span></span> <span data-ttu-id="787ae-135">Especificar este rectángulo permite que el dispositivo escale la imagen a medida que digitaliza los datos.</span><span class="sxs-lookup"><span data-stu-id="787ae-135">Specifying this rectangle lets the device scale the image as it digitizes the data.</span></span> <span data-ttu-id="787ae-136">Los dispositivos que no pueden escalar la imagen rechazan este comando con la \_ función MCIERR no admitida \_ .</span><span class="sxs-lookup"><span data-stu-id="787ae-136">Devices that cannot scale the image reject this command with MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="787ae-137">Puede usar la marca MCI \_ GETDEVCAPS \_ Can \_ Stretch con el comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) para determinar si un dispositivo escala la imagen.</span><span class="sxs-lookup"><span data-stu-id="787ae-137">You can use the MCI\_GETDEVCAPS\_CAN\_STRETCH flag with the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command to determine if a device scales the image.</span></span> <span data-ttu-id="787ae-138">Un dispositivo devuelve **false** si no puede escalar la imagen.</span><span class="sxs-lookup"><span data-stu-id="787ae-138">A device returns **FALSE** if it cannot scale the image.</span></span>

</dd> <dt>

<span data-ttu-id="787ae-139"><span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>\_origen de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="787ae-139"><span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>MCI\_DGV\_PUT\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="787ae-140">El rectángulo definido para MCI \_ DGV \_ Rect especifica un rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="787ae-140">The rectangle defined for MCI\_DGV\_RECT specifies a source rectangle.</span></span> <span data-ttu-id="787ae-141">El rectángulo de origen especifica qué parte del búfer de fotogramas se va a escalar para ajustarse al rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="787ae-141">The source rectangle specifies which portion of the frame buffer is to be scaled to fit into the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="787ae-142"><span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>\_vídeo de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="787ae-142"><span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>MCI\_DGV\_PUT\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="787ae-143">El rectángulo definido para MCI \_ DGV \_ Rect se aplica al rectángulo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="787ae-143">The rectangle defined for MCI\_DGV\_RECT applies to the video rectangle.</span></span> <span data-ttu-id="787ae-144">El rectángulo de vídeo especifica qué parte del origen de presentación actual se almacena en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="787ae-144">The video rectangle specifies which portion of the current presentation source is stored in the frame buffer.</span></span> <span data-ttu-id="787ae-145">El rectángulo se especifica mediante las coordenadas naturales del origen de presentación.</span><span class="sxs-lookup"><span data-stu-id="787ae-145">The rectangle is specified using the natural coordinates of the presentation source.</span></span> <span data-ttu-id="787ae-146">Permite la especificación del recorte que se produce antes de almacenar imágenes y vídeo en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="787ae-146">It allows the specification of cropping that occurs prior to storing images and video in the frame buffer.</span></span> <span data-ttu-id="787ae-147">El rectángulo predeterminado es el área de análisis activa completa o las imágenes y el vídeo descomprimidos completos.</span><span class="sxs-lookup"><span data-stu-id="787ae-147">The default rectangle is the full active scan area or the full decompressed images and video.</span></span>

</dd> <dt>

<span data-ttu-id="787ae-148"><span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>\_ventana de \_ colocación de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="787ae-148"><span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>MCI\_DGV\_PUT\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="787ae-149">El rectángulo definido para MCI \_ DGV \_ Rect se aplica a la ventana de presentación.</span><span class="sxs-lookup"><span data-stu-id="787ae-149">The rectangle defined for MCI\_DGV\_RECT applies to the display window.</span></span> <span data-ttu-id="787ae-150">Este rectángulo es relativo a la ventana primaria de la ventana de presentación (normalmente el escritorio).</span><span class="sxs-lookup"><span data-stu-id="787ae-150">This rectangle is relative to the parent window of the display window (usually the desktop).</span></span> <span data-ttu-id="787ae-151">Si no se especifica la ventana, se toma como valor predeterminado el tamaño y la posición de la ventana inicial.</span><span class="sxs-lookup"><span data-stu-id="787ae-151">If the window is not specified, it defaults to the initial window size and position.</span></span>

</dd> <dt>

<span data-ttu-id="787ae-152"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV \_ Rect</span><span class="sxs-lookup"><span data-stu-id="787ae-152"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="787ae-153">El miembro **RC** de la estructura identificada por *lpDest* contiene un rectángulo válido.</span><span class="sxs-lookup"><span data-stu-id="787ae-153">The **rc** member of the structure identified by *lpDest* contains a valid rectangle.</span></span>

</dd> </dl>

<span data-ttu-id="787ae-154">En el caso de los dispositivos de vídeo digital, *lpDest* apunta a una estructura [**MCI \_ DGV \_ Put \_ parms**](/previous-versions//dd743397(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="787ae-154">For digital-video devices, *lpDest* points to an [**MCI\_DGV\_PUT\_PARMS**](/previous-versions//dd743397(v=vs.85)) structure.</span></span>

<span data-ttu-id="787ae-155">Se usan las siguientes marcas adicionales con el tipo de dispositivo **superpuesto** :</span><span class="sxs-lookup"><span data-stu-id="787ae-155">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="787ae-156"><span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>\_ \_ destino put de MCI OVLY \_</span><span class="sxs-lookup"><span data-stu-id="787ae-156"><span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>MCI\_OVLY\_PUT\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="787ae-157">El rectángulo definido para MCI \_ OVLY \_ Rect especifica el área de la ventana de cliente que se usa para mostrar una imagen.</span><span class="sxs-lookup"><span data-stu-id="787ae-157">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the client window used to display an image.</span></span> <span data-ttu-id="787ae-158">El rectángulo contiene el desplazamiento y la extensión visible de la imagen en relación con el origen de la ventana.</span><span class="sxs-lookup"><span data-stu-id="787ae-158">The rectangle contains the offset and visible extent of the image relative to the window origin.</span></span> <span data-ttu-id="787ae-159">Si se va a estirar el marco, el origen se ajusta al rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="787ae-159">If the frame is being stretched, the source is stretched to the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="787ae-160"><span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>fotograma de OVLY de MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="787ae-160"><span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>MCI\_OVLY\_PUT\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="787ae-161">El rectángulo definido para MCI \_ OVLY \_ Rect especifica el área del búfer de vídeo que se usa para recibir la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="787ae-161">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video buffer used to receive the video image.</span></span> <span data-ttu-id="787ae-162">El rectángulo contiene el desplazamiento y la extensión del área del búfer en relación con el origen del búfer de vídeo.</span><span class="sxs-lookup"><span data-stu-id="787ae-162">The rectangle contains the offset and extent of the buffer area relative to the video buffer origin.</span></span>

</dd> <dt>

<span data-ttu-id="787ae-163"><span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>\_origen de OVLY de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="787ae-163"><span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>MCI\_OVLY\_PUT\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="787ae-164">El rectángulo definido para MCI \_ OVLY \_ Rect especifica el área del búfer de vídeo que se usa como origen de la imagen digital.</span><span class="sxs-lookup"><span data-stu-id="787ae-164">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video buffer used as the source of the digital image.</span></span> <span data-ttu-id="787ae-165">El rectángulo contiene el desplazamiento y la extensión del rectángulo de recorte para el búfer de vídeo en relación con su origen.</span><span class="sxs-lookup"><span data-stu-id="787ae-165">The rectangle contains the offset and extent of the clipping rectangle for the video buffer relative to its origin.</span></span>

</dd> <dt>

<span data-ttu-id="787ae-166"><span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>\_vídeo de OVLY de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="787ae-166"><span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>MCI\_OVLY\_PUT\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="787ae-167">El rectángulo definido para MCI \_ OVLY \_ Rect especifica el área de la captura de origen de vídeo por el búfer de vídeo.</span><span class="sxs-lookup"><span data-stu-id="787ae-167">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video source capture by the video buffer.</span></span> <span data-ttu-id="787ae-168">El rectángulo contiene el desplazamiento y la extensión del rectángulo de recorte para el origen de vídeo en relación con su origen.</span><span class="sxs-lookup"><span data-stu-id="787ae-168">The rectangle contains the offset and extent of the clipping rectangle for the video source relative to its origin.</span></span>

</dd> <dt>

<span data-ttu-id="787ae-169"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect</span><span class="sxs-lookup"><span data-stu-id="787ae-169"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="787ae-170">El miembro **RC** de la estructura identificada por *lpDest* contiene un rectángulo de presentación válido.</span><span class="sxs-lookup"><span data-stu-id="787ae-170">The **rc** member of the structure identified by *lpDest* contains a valid display rectangle.</span></span> <span data-ttu-id="787ae-171">Si no se especifica esta marca, el rectángulo predeterminado coincide con las coordenadas del búfer de vídeo o de la ventana que se va a recortar.</span><span class="sxs-lookup"><span data-stu-id="787ae-171">If this flag is not specified, the default rectangle matches the coordinates of the video buffer or window being clipped.</span></span>

</dd> </dl>

<span data-ttu-id="787ae-172">En el caso de los dispositivos de superposición de vídeo, *lpDest* apunta a una estructura [**MCI \_ OVLY \_ Rect \_ parms**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="787ae-172">For video-overlay devices, *lpDest* points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="787ae-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="787ae-173">Requirements</span></span>



| <span data-ttu-id="787ae-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="787ae-174">Requirement</span></span> | <span data-ttu-id="787ae-175">Value</span><span class="sxs-lookup"><span data-stu-id="787ae-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="787ae-176">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="787ae-176">Minimum supported client</span></span><br/> | <span data-ttu-id="787ae-177">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="787ae-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="787ae-178">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="787ae-178">Minimum supported server</span></span><br/> | <span data-ttu-id="787ae-179">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="787ae-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="787ae-180">Encabezado</span><span class="sxs-lookup"><span data-stu-id="787ae-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="787ae-181"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="787ae-181"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="787ae-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="787ae-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="787ae-183">MCI</span><span class="sxs-lookup"><span data-stu-id="787ae-183">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="787ae-184">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="787ae-184">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

