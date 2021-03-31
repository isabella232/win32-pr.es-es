---
title: Comando MCI_UPDATE (mmsystem. h)
description: El comando de actualización de MCI \_ actualiza el rectángulo de presentación. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- Comando de MCI_UPDATE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_UPDATE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423186096c88a8f1ff74987ff57c6b49dc6c3131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151029"
---
# <a name="mci_update-command"></a><span data-ttu-id="5f91b-105">Comando de actualización de MCI \_</span><span class="sxs-lookup"><span data-stu-id="5f91b-105">MCI\_UPDATE command</span></span>

<span data-ttu-id="5f91b-106">El comando de actualización de MCI \_ actualiza el rectángulo de presentación.</span><span class="sxs-lookup"><span data-stu-id="5f91b-106">The MCI\_UPDATE command updates the display rectangle.</span></span> <span data-ttu-id="5f91b-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="5f91b-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="5f91b-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="5f91b-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UPDATE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
);
```



## <a name="parameters"></a><span data-ttu-id="5f91b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f91b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f91b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="5f91b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5f91b-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="5f91b-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="5f91b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="5f91b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5f91b-113">**MCI \_ NOTIFICAr**, **\_ espera de MCI** o, para dispositivos de vídeo digital **, \_ prueba de MCI**.</span><span class="sxs-lookup"><span data-stu-id="5f91b-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or, for digital-video devices, **MCI\_TEST**.</span></span> <span data-ttu-id="5f91b-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5f91b-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f91b-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span><span class="sxs-lookup"><span data-stu-id="5f91b-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span></span>
</dt> <dd>

<span data-ttu-id="5f91b-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="5f91b-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="5f91b-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="5f91b-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f91b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f91b-118">Return Value</span></span>

<span data-ttu-id="5f91b-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5f91b-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f91b-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f91b-120">Remarks</span></span>

<span data-ttu-id="5f91b-121">Se usan las siguientes marcas adicionales con el tipo de dispositivo "DigitalVideo":</span><span class="sxs-lookup"><span data-stu-id="5f91b-121">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="5f91b-122"><span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>actualización de DGV de MCI \_ \_ \_ HDC</span><span class="sxs-lookup"><span data-stu-id="5f91b-122"><span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>MCI\_DGV\_UPDATE\_HDC</span></span>
</dt> <dd>

<span data-ttu-id="5f91b-123">El miembro **HDC** de la estructura identificada por *lpDest* contiene una ventana válida del controlador de dominio que se va a pintar.</span><span class="sxs-lookup"><span data-stu-id="5f91b-123">The **hDC** member of the structure identified by *lpDest* contains a valid window of the DC to paint.</span></span> <span data-ttu-id="5f91b-124">Esta marca es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="5f91b-124">This flag is required.</span></span>

</dd> <dt>

<span data-ttu-id="5f91b-125"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV \_ Rect</span><span class="sxs-lookup"><span data-stu-id="5f91b-125"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="5f91b-126">El miembro **RC** de la estructura identificada por *lpUnfreeze* contiene un rectángulo de presentación válido.</span><span class="sxs-lookup"><span data-stu-id="5f91b-126">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="5f91b-127">El rectángulo especifica el rectángulo de recorte relativo al rectángulo de cliente.</span><span class="sxs-lookup"><span data-stu-id="5f91b-127">The rectangle specifies the clipping rectangle relative to the client rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="5f91b-128"><span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>\_DGV MCI \_ actualizar \_ Paint</span><span class="sxs-lookup"><span data-stu-id="5f91b-128"><span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>MCI\_DGV\_UPDATE\_PAINT</span></span>
</dt> <dd>

<span data-ttu-id="5f91b-129">Una aplicación usa esta marca cuando recibe un mensaje [**de \_ dibujo de WM**](/windows/desktop/gdi/wm-paint) diseñado para un controlador de dominio de pantalla.</span><span class="sxs-lookup"><span data-stu-id="5f91b-129">An application uses this flag when it receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message that is intended for a display DC.</span></span> <span data-ttu-id="5f91b-130">Normalmente, un dispositivo de búfer de fotogramas pinta el color de la clave.</span><span class="sxs-lookup"><span data-stu-id="5f91b-130">A frame-buffer device usually paints the key color.</span></span> <span data-ttu-id="5f91b-131">Si el dispositivo de pantalla no tiene un búfer de fotogramas, podría omitir el comando de actualización de MCI \_ cuando se use la marca de **\_ Paint de \_ actualización \_ de MCI DGV** , ya que la pantalla se volverá a dibujar durante la operación de reproducción.</span><span class="sxs-lookup"><span data-stu-id="5f91b-131">If the display device does not have a frame buffer, it might ignore the MCI\_UPDATE command when the **MCI\_DGV\_UPDATE\_PAINT** flag is used because the display will be repainted during the playback operation.</span></span>

</dd> </dl>

<span data-ttu-id="5f91b-132">En el caso de los dispositivos de vídeo digital, el parámetro *lpDest* apunta a una estructura [**MCI \_ DGV \_ Update \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) .</span><span class="sxs-lookup"><span data-stu-id="5f91b-132">For digital-video devices, the *lpDest* parameter points to an [**MCI\_DGV\_UPDATE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f91b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f91b-133">Requirements</span></span>



| <span data-ttu-id="5f91b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f91b-134">Requirement</span></span> | <span data-ttu-id="5f91b-135">Value</span><span class="sxs-lookup"><span data-stu-id="5f91b-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f91b-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f91b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5f91b-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5f91b-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5f91b-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f91b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5f91b-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5f91b-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5f91b-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f91b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f91b-141"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f91b-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f91b-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f91b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f91b-143">MCI</span><span class="sxs-lookup"><span data-stu-id="5f91b-143">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5f91b-144">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="5f91b-144">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

