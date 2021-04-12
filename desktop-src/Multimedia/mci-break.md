---
title: Comando MCI_BREAK (mmsystem. h)
description: El \_ comando de interrupción de MCI establece una tecla de interrupción para un dispositivo MCI. MCI admite este comando directamente en lugar de pasarlo al dispositivo. Cualquier aplicación MCI puede usar este comando.
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- Comando de MCI_BREAK de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_BREAK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b17e3796192344ef974fed1af7229d41746aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490132"
---
# <a name="mci_break-command"></a><span data-ttu-id="a3026-106">Comando de interrupción de MCI \_</span><span class="sxs-lookup"><span data-stu-id="a3026-106">MCI\_BREAK command</span></span>

<span data-ttu-id="a3026-107">El \_ comando de interrupción de MCI establece una tecla de interrupción para un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="a3026-107">The MCI\_BREAK command sets a break key for an MCI device.</span></span> <span data-ttu-id="a3026-108">MCI admite este comando directamente en lugar de pasarlo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3026-108">MCI supports this command directly rather than passing it to the device.</span></span> <span data-ttu-id="a3026-109">Cualquier aplicación MCI puede usar este comando.</span><span class="sxs-lookup"><span data-stu-id="a3026-109">Any MCI application can use this command.</span></span>

<span data-ttu-id="a3026-110">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="a3026-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_BREAK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_BREAK_PARMS) lpBreak
);
```



## <a name="parameters"></a><span data-ttu-id="a3026-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3026-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3026-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a3026-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a3026-113">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="a3026-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="a3026-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a3026-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a3026-115">Las \_ notificaciones de MCI, espera de MCI \_ o, para dispositivos de grabadora de vídeo digital y vídeo (VCR), prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="a3026-115">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and video-cassette recorder (VCR) devices, MCI\_TEST.</span></span> <span data-ttu-id="a3026-116">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a3026-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3026-117"><span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*</span><span class="sxs-lookup"><span data-stu-id="a3026-117"><span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*</span></span>
</dt> <dd>

<span data-ttu-id="a3026-118">Puntero a una [**estructura \_ \_ parms de interrupción de MCI**](mci-break-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a3026-118">Pointer to an [**MCI\_ BREAK\_PARMS**](mci-break-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3026-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3026-119">Return Value</span></span>

<span data-ttu-id="a3026-120">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a3026-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3026-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3026-121">Remarks</span></span>

<span data-ttu-id="a3026-122">Es posible que tenga que presionar la tecla interrumpir varias veces para interrumpir una operación de espera.</span><span class="sxs-lookup"><span data-stu-id="a3026-122">You might have to press the break key multiple times to interrupt a wait operation.</span></span> <span data-ttu-id="a3026-123">Al presionar la tecla interrumpir después de que se cancele un dispositivo, puede enviar la interrupción a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="a3026-123">Pressing the break key after a device wait is canceled can send the break to an application.</span></span> <span data-ttu-id="a3026-124">Si una aplicación tiene una acción definida para el código de tecla virtual, puede responder accidentalmente a la interrupción.</span><span class="sxs-lookup"><span data-stu-id="a3026-124">If an application has an action defined for the virtual-key code, then it can inadvertently respond to the break.</span></span> <span data-ttu-id="a3026-125">Por ejemplo, una aplicación que use VK \_ Cancel para una tecla de aceleración puede responder a la tecla Ctrl + Inter predeterminada si se presiona después de que se cancele la espera.</span><span class="sxs-lookup"><span data-stu-id="a3026-125">For example, an application using VK\_CANCEL for an accelerator key can respond to the default CTRL+BREAK key if it is pressed after a wait is canceled.</span></span>

<span data-ttu-id="a3026-126">Las siguientes marcas adicionales se aplican a todos los dispositivos:</span><span class="sxs-lookup"><span data-stu-id="a3026-126">The following additional flags apply to all devices:</span></span>

<dl> <dt>

<span data-ttu-id="a3026-127"><span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>\_hWnd de interrupción de MCI \_</span><span class="sxs-lookup"><span data-stu-id="a3026-127"><span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>MCI\_BREAK\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="a3026-128">El miembro **hwndBreak** de la estructura identificada por *lpBreak* contiene un identificador de ventana que debe ser la ventana actual para habilitar la detección de interrupciones para ese dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="a3026-128">The **hwndBreak** member of the structure identified by *lpBreak* contains a window handle that must be the current window in order to enable break detection for that MCI device.</span></span> <span data-ttu-id="a3026-129">Esta suele ser la ventana principal de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a3026-129">This is usually the application's main window.</span></span> <span data-ttu-id="a3026-130">Si se omite, MCI no comprueba el identificador de ventana de la ventana actual.</span><span class="sxs-lookup"><span data-stu-id="a3026-130">If omitted, MCI does not check the window handle of the current window.</span></span>

</dd> <dt>

<span data-ttu-id="a3026-131"><span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>\_tecla de interrupción de MCI \_</span><span class="sxs-lookup"><span data-stu-id="a3026-131"><span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>MCI\_BREAK\_KEY</span></span>
</dt> <dd>

<span data-ttu-id="a3026-132">El miembro **nVirtKey** de la estructura identificada por *lpBreak* especifica el código de la clave virtual que se usa para la tecla interrumpir.</span><span class="sxs-lookup"><span data-stu-id="a3026-132">The **nVirtKey** member of the structure identified by *lpBreak* specifies the virtual-key code used for the break key.</span></span> <span data-ttu-id="a3026-133">De forma predeterminada, MCI asigna CTRL + INTER como tecla de salto.</span><span class="sxs-lookup"><span data-stu-id="a3026-133">By default, MCI assigns CTRL+BREAK as the break key.</span></span> <span data-ttu-id="a3026-134">Esta marca es necesaria si \_ no se especifica la interrupción de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="a3026-134">This flag is required if MCI\_BREAK\_OFF is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="a3026-135"><span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>interrupción de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="a3026-135"><span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>MCI\_BREAK\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="a3026-136">Deshabilita cualquier clave de interrupción existente para el dispositivo indicado.</span><span class="sxs-lookup"><span data-stu-id="a3026-136">Disables any existing break key for the indicated device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3026-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3026-137">Requirements</span></span>



| <span data-ttu-id="a3026-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3026-138">Requirement</span></span> | <span data-ttu-id="a3026-139">Value</span><span class="sxs-lookup"><span data-stu-id="a3026-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3026-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3026-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a3026-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a3026-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a3026-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3026-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a3026-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a3026-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a3026-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3026-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3026-145"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3026-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3026-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3026-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3026-147">MCI</span><span class="sxs-lookup"><span data-stu-id="a3026-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a3026-148">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="a3026-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

