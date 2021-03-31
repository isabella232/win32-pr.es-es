---
title: Comando MCI_WINDOW (mmsystem. h)
description: El \_ comando MCI Window especifica la ventana y las características de la ventana para los dispositivos gráficos. Los dispositivos de vídeo digital y de superposición reconocen este comando.
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- Comando de MCI_WINDOW de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_WINDOW
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41b4d630dbc9dbc7403e93cd0bda3de2eef1e5cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996538"
---
# <a name="mci_window-command"></a><span data-ttu-id="88d4d-105">\_Comando de ventana MCI</span><span class="sxs-lookup"><span data-stu-id="88d4d-105">MCI\_WINDOW command</span></span>

<span data-ttu-id="88d4d-106">El \_ comando MCI Window especifica la ventana y las características de la ventana para los dispositivos gráficos.</span><span class="sxs-lookup"><span data-stu-id="88d4d-106">The MCI\_WINDOW command specifies the window and the window characteristics for graphic devices.</span></span> <span data-ttu-id="88d4d-107">Los dispositivos de vídeo digital y de superposición reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="88d4d-107">Digital-video, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="88d4d-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="88d4d-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WINDOW, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpWindow
);
```



## <a name="parameters"></a><span data-ttu-id="88d4d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88d4d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88d4d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="88d4d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="88d4d-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="88d4d-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="88d4d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="88d4d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="88d4d-113">\_La notificación de MCI, la espera de MCI \_ o, para dispositivos de vídeo digital, la prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="88d4d-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="88d4d-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="88d4d-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="88d4d-115"><span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*</span><span class="sxs-lookup"><span data-stu-id="88d4d-115"><span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*</span></span>
</dt> <dd>

<span data-ttu-id="88d4d-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="88d4d-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="88d4d-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="88d4d-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88d4d-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88d4d-118">Return Value</span></span>

<span data-ttu-id="88d4d-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="88d4d-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="88d4d-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88d4d-120">Remarks</span></span>

<span data-ttu-id="88d4d-121">Los dispositivos gráficos deben crear una ventana predeterminada cuando se abre un dispositivo, pero no se debe mostrar hasta que reciban el comando de [ \_ reproducción de MCI](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="88d4d-121">Graphic devices should create a default window when a device is opened but should not display it until they receive the [MCI\_PLAY](mci-play.md) command.</span></span> <span data-ttu-id="88d4d-122">El \_ comando MCI Window se usa para proporcionar una ventana creada por la aplicación al dispositivo y para cambiar las características de presentación de una ventana de visualización definida por la aplicación o predeterminada.</span><span class="sxs-lookup"><span data-stu-id="88d4d-122">The MCI\_WINDOW command is used to supply an application-created window to the device and to change the display characteristics of an application-defined or default display window.</span></span> <span data-ttu-id="88d4d-123">Si la aplicación proporciona la ventana de presentación, debe estar preparada para actualizar un rectángulo no válido en la ventana.</span><span class="sxs-lookup"><span data-stu-id="88d4d-123">If the application supplies the display window, it should be prepared to update an invalid rectangle on the window.</span></span>

<span data-ttu-id="88d4d-124">Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:</span><span class="sxs-lookup"><span data-stu-id="88d4d-124">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="88d4d-125"><span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>\_ventana DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="88d4d-125"><span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>MCI\_DGV\_WINDOW\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="88d4d-126">El identificador de la ventana necesaria para su uso como destino se incluye en el miembro **hWnd** de la estructura identificada por *lpWindow*.</span><span class="sxs-lookup"><span data-stu-id="88d4d-126">The handle of the window needed for use as the destination is included in the **hWnd** member of the structure identified by *lpWindow*.</span></span>

</dd> <dt>

<span data-ttu-id="88d4d-127"><span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>Estado de la ventana de MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="88d4d-127"><span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>MCI\_DGV\_WINDOW\_STATE</span></span>
</dt> <dd>

<span data-ttu-id="88d4d-128">El miembro **nCmdShow** de la estructura identificada por *lpWindow* contiene parámetros para establecer el estado de la ventana.</span><span class="sxs-lookup"><span data-stu-id="88d4d-128">The **nCmdShow** member of the structure identified by *lpWindow* contains parameters for setting the window state.</span></span>

</dd> <dt>

<span data-ttu-id="88d4d-129"><span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>texto de la ventana de DGV de MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="88d4d-129"><span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>MCI\_DGV\_WINDOW\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="88d4d-130">El miembro **lpstrText** de la estructura identificada por *lpWindow* contiene una dirección de un búfer que contiene el título usado en la barra de título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="88d4d-130">The **lpstrText** member of the structure identified by *lpWindow* contains an address of a buffer containing the caption used in the window title bar.</span></span>

</dd> </dl>

<span data-ttu-id="88d4d-131">En el caso de los dispositivos de vídeo digital, el parámetro *lpWindow* apunta a una estructura [**parms de DGV de \_ \_ ventana \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="88d4d-131">For digital-video devices, the *lpWindow* parameter points to an [**MCI\_DGV\_WINDOW\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) structure.</span></span>

<span data-ttu-id="88d4d-132">Se usan las siguientes marcas adicionales con el tipo de dispositivo **superpuesto** :</span><span class="sxs-lookup"><span data-stu-id="88d4d-132">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="88d4d-133"><span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>ventana de OVLY de MCI \_ \_ \_ deshabilitar \_ Stretch</span><span class="sxs-lookup"><span data-stu-id="88d4d-133"><span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>MCI\_OVLY\_WINDOW\_DISABLE\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="88d4d-134">Deshabilita la expansión de la imagen.</span><span class="sxs-lookup"><span data-stu-id="88d4d-134">Disables stretching of the image.</span></span>

</dd> <dt>

<span data-ttu-id="88d4d-135"><span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>ventana de OVLY de MCI \_ \_ \_ habilitar \_ Stretch</span><span class="sxs-lookup"><span data-stu-id="88d4d-135"><span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>MCI\_OVLY\_WINDOW\_ENABLE\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="88d4d-136">Habilita la expansión de la imagen.</span><span class="sxs-lookup"><span data-stu-id="88d4d-136">Enables stretching of the image.</span></span>

</dd> <dt>

<span data-ttu-id="88d4d-137"><span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>\_ventana OVLY de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="88d4d-137"><span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>MCI\_OVLY\_WINDOW\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="88d4d-138">El identificador de la ventana que se usa para el destino se incluye en el miembro **hWnd** de la estructura identificada por *lpWindow*.</span><span class="sxs-lookup"><span data-stu-id="88d4d-138">The handle of the window used for the destination is included in the **hWnd** member of the structure identified by *lpWindow*.</span></span> <span data-ttu-id="88d4d-139">Establezca esta marca en \_ \_ \_ el valor predeterminado de la ventana MCI OVLY para volver a la ventana predeterminada.</span><span class="sxs-lookup"><span data-stu-id="88d4d-139">Set this flag to MCI\_OVLY\_WINDOW\_DEFAULT to return to the default window.</span></span>

</dd> <dt>

<span data-ttu-id="88d4d-140"><span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>Estado de la ventana de MCI \_ OVLY \_ \_</span><span class="sxs-lookup"><span data-stu-id="88d4d-140"><span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>MCI\_OVLY\_WINDOW\_STATE</span></span>
</dt> <dd>

<span data-ttu-id="88d4d-141">El miembro **nCmdShow** de la estructura *lpWindow* contiene parámetros para establecer el estado de la ventana.</span><span class="sxs-lookup"><span data-stu-id="88d4d-141">The **nCmdShow** member of the *lpWindow* structure contains parameters for setting the window state.</span></span> <span data-ttu-id="88d4d-142">Esta marca es equivalente a llamar a [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) con el parámetro *State* .</span><span class="sxs-lookup"><span data-stu-id="88d4d-142">This flag is equivalent to calling [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) with the *state* parameter.</span></span> <span data-ttu-id="88d4d-143">Las constantes son las mismas que las definidas en WINDOWS. H (como SW \_ Hide, SW \_ minimizar o SW \_ SHOWNORMAL).</span><span class="sxs-lookup"><span data-stu-id="88d4d-143">The constants are the same as those defined in WINDOWS.H (such as SW\_HIDE, SW\_MINIMIZE, or SW\_SHOWNORMAL).</span></span>

</dd> <dt>

<span data-ttu-id="88d4d-144"><span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>texto de la ventana de OVLY de MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="88d4d-144"><span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>MCI\_OVLY\_WINDOW\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="88d4d-145">El miembro **lpstrText** de la estructura identificada por *lpWindow* contiene una dirección de un búfer que contiene el título que se usa para la ventana.</span><span class="sxs-lookup"><span data-stu-id="88d4d-145">The **lpstrText** member of the structure identified by *lpWindow* contains an address of a buffer containing the caption used for the window.</span></span>

</dd> </dl>

<span data-ttu-id="88d4d-146">En el caso de los dispositivos de superposición de vídeo, el parámetro *lpWindow* apunta a una estructura [**parms de OVLY de \_ \_ ventana \_ MCI**](mci-ovly-window-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="88d4d-146">For video-overlay devices, the *lpWindow* parameter points to an [**MCI\_OVLY\_WINDOW\_PARMS**](mci-ovly-window-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="88d4d-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88d4d-147">Requirements</span></span>



| <span data-ttu-id="88d4d-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="88d4d-148">Requirement</span></span> | <span data-ttu-id="88d4d-149">Value</span><span class="sxs-lookup"><span data-stu-id="88d4d-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88d4d-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88d4d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="88d4d-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="88d4d-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="88d4d-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88d4d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="88d4d-153">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="88d4d-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="88d4d-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88d4d-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="88d4d-155"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88d4d-155"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88d4d-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="88d4d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88d4d-157">MCI</span><span class="sxs-lookup"><span data-stu-id="88d4d-157">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="88d4d-158">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="88d4d-158">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

