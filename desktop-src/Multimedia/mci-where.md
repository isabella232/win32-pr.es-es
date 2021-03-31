---
title: Comando MCI_WHERE (mmsystem. h)
description: El \_ comando MCI donde obtiene el rectángulo de recorte para el dispositivo de vídeo.
ms.assetid: f64a7e49-4ee1-4836-ba9a-0bbdc47626b3
keywords:
- Comando de MCI_WHERE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_WHERE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6619131319863d1159a3bdb8bb85d366243544a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996450"
---
# <a name="mci_where-command"></a><span data-ttu-id="78844-104">\_Comando MCI Where</span><span class="sxs-lookup"><span data-stu-id="78844-104">MCI\_WHERE command</span></span>

<span data-ttu-id="78844-105">El \_ comando MCI donde obtiene el rectángulo de recorte para el dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="78844-105">The MCI\_WHERE command obtains the clipping rectangle for the video device.</span></span> <span data-ttu-id="78844-106">Los dispositivos de vídeo digital y de superposición reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="78844-106">Digital-video, and video-overlay devices recognize this command.</span></span> <span data-ttu-id="78844-107">Los miembros **superior** e **izquierdo** del [Rect](/previous-versions//ms536136(v=vs.85)) devuelto contienen el origen del rectángulo de recorte y los miembros **derecho** e **inferior** contienen el ancho y el alto del rectángulo de recorte.</span><span class="sxs-lookup"><span data-stu-id="78844-107">The **top** and **left** members of the returned [RECT](/previous-versions//ms536136(v=vs.85)) contain the origin of the clipping rectangle, and the **right** and **bottom** members contain the width and height of the clipping rectangle.</span></span> <span data-ttu-id="78844-108">(Este no es el uso estándar de los miembros **derecho** e **inferior** ).</span><span class="sxs-lookup"><span data-stu-id="78844-108">(This is not the standard use of the **right** and **bottom** members.)</span></span>

<span data-ttu-id="78844-109">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="78844-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WHERE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpQuery
);
```



## <a name="parameters"></a><span data-ttu-id="78844-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78844-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78844-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="78844-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="78844-112">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="78844-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="78844-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="78844-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="78844-114">\_La notificación de MCI, la espera de MCI \_ o, para dispositivos de vídeo digital, la prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="78844-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="78844-115">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="78844-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="78844-116"><span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*</span><span class="sxs-lookup"><span data-stu-id="78844-116"><span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*</span></span>
</dt> <dd>

<span data-ttu-id="78844-117">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="78844-117">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="78844-118">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="78844-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78844-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78844-119">Return Value</span></span>

<span data-ttu-id="78844-120">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="78844-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="78844-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78844-121">Remarks</span></span>

<span data-ttu-id="78844-122">Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:</span><span class="sxs-lookup"><span data-stu-id="78844-122">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="78844-123"><span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>MCI \_ DGV \_ donde \_ destino</span><span class="sxs-lookup"><span data-stu-id="78844-123"><span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>MCI\_DGV\_WHERE\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="78844-124">Obtiene una descripción de la región rectangular utilizada para mostrar vídeo e imágenes en el área cliente de la ventana actual.</span><span class="sxs-lookup"><span data-stu-id="78844-124">Obtains a description of the rectangular region used to display video and images in the client area of the current window.</span></span>

</dd> <dt>

<span data-ttu-id="78844-125"><span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>\_DGV MCI \_ donde \_ marco</span><span class="sxs-lookup"><span data-stu-id="78844-125"><span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>MCI\_DGV\_WHERE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="78844-126">Obtiene una descripción de la región rectangular del búfer de fotogramas en el que se escalan las imágenes del rectángulo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="78844-126">Obtains a description of the rectangular region of the frame buffer into which images from the video rectangle are scaled.</span></span> <span data-ttu-id="78844-127">Las coordenadas del rectángulo se colocan en el miembro **RC** de la estructura identificada por *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="78844-127">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="78844-128"><span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI \_ DGV \_ Where \_ Max</span><span class="sxs-lookup"><span data-stu-id="78844-128"><span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI\_DGV\_WHERE\_MAX</span></span>
</dt> <dd>

<span data-ttu-id="78844-129">Cuando se usa con MCI \_ DGV \_ donde \_ Destination o MCI \_ DGV \_ Where \_ source, el rectángulo devuelto indica el ancho y el alto máximos de la región especificada.</span><span class="sxs-lookup"><span data-stu-id="78844-129">When used with MCI\_DGV\_WHERE\_DESTINATION or MCI\_DGV\_WHERE\_SOURCE, the rectangle returned indicates the maximum width and height of the specified region.</span></span> <span data-ttu-id="78844-130">Cuando se usa con la ventana de MCI \_ DGV \_ Where \_ , el rectángulo devuelto indica el tamaño de la pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="78844-130">When used with MCI\_DGV\_WHERE\_WINDOW, the rectangle returned indicates the size of the entire display.</span></span>

</dd> <dt>

<span data-ttu-id="78844-131"><span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI \_ DGV \_ Where \_ source</span><span class="sxs-lookup"><span data-stu-id="78844-131"><span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI\_DGV\_WHERE\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="78844-132">Obtiene una descripción de la región rectangular (recortada a partir del búfer de fotogramas) que se ajusta para ajustarse al rectángulo de destino de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="78844-132">Obtains a description of the rectangular region (cropped from the frame buffer) that is stretched to fit the destination rectangle on the display.</span></span>

</dd> <dt>

<span data-ttu-id="78844-133"><span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>DGV de MCI \_ \_ donde \_ vídeo</span><span class="sxs-lookup"><span data-stu-id="78844-133"><span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>MCI\_DGV\_WHERE\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="78844-134">Obtiene una descripción de la región rectangular recortada del origen de presentación para rellenar el rectángulo del marco en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="78844-134">Obtains a description of the rectangular region cropped from the presentation source to fill the frame rectangle in the frame buffer.</span></span> <span data-ttu-id="78844-135">Las coordenadas del rectángulo se colocan en el miembro **RC** de la estructura identificada por *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="78844-135">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="78844-136"><span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>\_ventana de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="78844-136"><span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>MCI\_DGV\_WHERE\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="78844-137">Obtiene una descripción del marco de la ventana de presentación.</span><span class="sxs-lookup"><span data-stu-id="78844-137">Obtains a description of the display-window frame.</span></span>

</dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="78844-138">En el caso de los dispositivos de vídeo digital, el parámetro *lpQuery* apunta a una **\_ DGV MCI \_ donde \_ parms** estructura.</span><span class="sxs-lookup"><span data-stu-id="78844-138">For digital-video devices, the *lpQuery* parameter points to an **MCI\_DGV\_WHERE\_PARMS** structure.</span></span> <span data-ttu-id="78844-139">La estructura **MCI \_ DGV \_ donde \_ parms** es idéntica a la estructura [**MCI \_ DGV \_ Rect \_ parms**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .</span><span class="sxs-lookup"><span data-stu-id="78844-139">The **MCI\_DGV\_WHERE\_PARMS** structure is identical to the [**MCI\_DGV\_RECT\_PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="78844-140">Se usan las siguientes marcas adicionales con el tipo de dispositivo **superpuesto** :</span><span class="sxs-lookup"><span data-stu-id="78844-140">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="78844-141"><span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>MCI \_ OVLY \_ donde \_ destino</span><span class="sxs-lookup"><span data-stu-id="78844-141"><span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>MCI\_OVLY\_WHERE\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="78844-142">Obtiene el rectángulo de presentación de destino.</span><span class="sxs-lookup"><span data-stu-id="78844-142">Obtains the destination display rectangle.</span></span> <span data-ttu-id="78844-143">Las coordenadas del rectángulo se colocan en el miembro **RC** de la estructura identificada por *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="78844-143">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="78844-144"><span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>\_OVLY MCI \_ donde \_ marco</span><span class="sxs-lookup"><span data-stu-id="78844-144"><span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>MCI\_OVLY\_WHERE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="78844-145">Obtiene el rectángulo del marco superpuesto.</span><span class="sxs-lookup"><span data-stu-id="78844-145">Obtains the overlay frame rectangle.</span></span> <span data-ttu-id="78844-146">Las coordenadas del rectángulo se colocan en el miembro **RC** de la estructura identificada por *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="78844-146">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="78844-147"><span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI \_ OVLY \_ Where \_ source</span><span class="sxs-lookup"><span data-stu-id="78844-147"><span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI\_OVLY\_WHERE\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="78844-148">Obtiene el rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="78844-148">Obtains the source rectangle.</span></span> <span data-ttu-id="78844-149">Las coordenadas del rectángulo se colocan en el miembro **RC** de la estructura identificada por *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="78844-149">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="78844-150"><span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>OVLY de MCI \_ \_ donde \_ vídeo</span><span class="sxs-lookup"><span data-stu-id="78844-150"><span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>MCI\_OVLY\_WHERE\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="78844-151">Obtiene el rectángulo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="78844-151">Obtains the video rectangle.</span></span> <span data-ttu-id="78844-152">Las coordenadas del rectángulo se colocan en el miembro **RC** de la estructura identificada por *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="78844-152">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> </dl>

<span data-ttu-id="78844-153">En el caso de los dispositivos de superposición de vídeo, el parámetro *lpQuery* apunta a una estructura [**MCI \_ OVLY \_ Rect \_ parms**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="78844-153">For video-overlay devices, the *lpQuery* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="78844-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78844-154">Requirements</span></span>



| <span data-ttu-id="78844-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="78844-155">Requirement</span></span> | <span data-ttu-id="78844-156">Value</span><span class="sxs-lookup"><span data-stu-id="78844-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78844-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78844-157">Minimum supported client</span></span><br/> | <span data-ttu-id="78844-158">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="78844-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="78844-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78844-159">Minimum supported server</span></span><br/> | <span data-ttu-id="78844-160">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="78844-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="78844-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78844-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="78844-162"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78844-162"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78844-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="78844-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78844-164">MCI</span><span class="sxs-lookup"><span data-stu-id="78844-164">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="78844-165">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="78844-165">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

