---
title: Mensaje WM_POINTERDEVICECHANGE
description: Se envía a una ventana cuando se produce un cambio en la configuración de un monitor que tiene un digitalizador adjunto. Este mensaje contiene información sobre el escalado del modo de presentación.
ms.assetid: 9ED01D4C-58B4-4A21-B510-784281F9A909
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERDEVICECHANGE
topic_type:
- apiref
api_name:
- WM_POINTERDEVICECHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 38f570059f374f64e393e960a8458e605983d6c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105720219"
---
# <a name="wm_pointerdevicechange-message"></a><span data-ttu-id="76ae9-105">Mensaje WM_POINTERDEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="76ae9-105">WM_POINTERDEVICECHANGE message</span></span>

<span data-ttu-id="76ae9-106">Se envía a una ventana cuando se produce un cambio en la configuración de un monitor que tiene un digitalizador adjunto.</span><span class="sxs-lookup"><span data-stu-id="76ae9-106">Sent to a window when there is a change in the settings of a monitor that has a digitizer attached to it.</span></span> <span data-ttu-id="76ae9-107">Este mensaje contiene información sobre el escalado del modo de presentación.</span><span class="sxs-lookup"><span data-stu-id="76ae9-107">This message contains information regarding the scaling of the display mode.</span></span>

> <span data-ttu-id="76ae9-108">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="76ae9-108">\[!Important\]</span></span>  
> <span data-ttu-id="76ae9-109">Las aplicaciones de escritorio deben tener en cuenta los ppp.</span><span class="sxs-lookup"><span data-stu-id="76ae9-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="76ae9-110">Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP.</span><span class="sxs-lookup"><span data-stu-id="76ae9-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="76ae9-111">La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla).</span><span class="sxs-lookup"><span data-stu-id="76ae9-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="76ae9-112">Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="76ae9-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDEVICECHANGE       0X238
```



## <a name="parameters"></a><span data-ttu-id="76ae9-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76ae9-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76ae9-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76ae9-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76ae9-115">Contiene un valor del [**puntero**](pointer-device-change-constants.md)de las constantes de cambio de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76ae9-115">Contains a value from [**Pointer Device Change Constants**](pointer-device-change-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="76ae9-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76ae9-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76ae9-117">Información adicional específica del mensaje.</span><span class="sxs-lookup"><span data-stu-id="76ae9-117">Additional message-specific information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76ae9-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76ae9-118">Return value</span></span>

<span data-ttu-id="76ae9-119">Si la aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="76ae9-119">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="76ae9-120">Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="76ae9-120">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="requirements"></a><span data-ttu-id="76ae9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76ae9-121">Requirements</span></span>



| <span data-ttu-id="76ae9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="76ae9-122">Requirement</span></span> | <span data-ttu-id="76ae9-123">Value</span><span class="sxs-lookup"><span data-stu-id="76ae9-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76ae9-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76ae9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="76ae9-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="76ae9-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="76ae9-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76ae9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="76ae9-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="76ae9-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="76ae9-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76ae9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="76ae9-129"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76ae9-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76ae9-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="76ae9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76ae9-131">Mensajes</span><span class="sxs-lookup"><span data-stu-id="76ae9-131">Messages</span></span>](messages.md)
</dt> </dl>

 

