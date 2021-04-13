---
title: Mensaje WM_POINTERDEVICEINRANGE
description: Se envía a una ventana cuando se detecta un dispositivo de puntero dentro del intervalo de un digitalizador de entrada. Este mensaje contiene información relacionada con el dispositivo y su proximidad.
ms.assetid: 04244758-E662-4FB2-850E-20B4B3D1294A
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERDEVICEINRANGE
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEINRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 76ab6ac4f96d1df4e4e29afbcefe86d34b8b602d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535152"
---
# <a name="wm_pointerdeviceinrange-message"></a><span data-ttu-id="88766-105">Mensaje WM_POINTERDEVICEINRANGE</span><span class="sxs-lookup"><span data-stu-id="88766-105">WM_POINTERDEVICEINRANGE message</span></span>

<span data-ttu-id="88766-106">Se envía a una ventana cuando se detecta un dispositivo de puntero dentro del intervalo de un digitalizador de entrada.</span><span class="sxs-lookup"><span data-stu-id="88766-106">Sent to a window when a pointer device is detected within range of an input digitizer.</span></span> <span data-ttu-id="88766-107">Este mensaje contiene información relacionada con el dispositivo y su proximidad.</span><span class="sxs-lookup"><span data-stu-id="88766-107">This message contains information regarding the device and its proximity.</span></span>

> <span data-ttu-id="88766-108">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="88766-108">\[!Important\]</span></span>  
> <span data-ttu-id="88766-109">Las aplicaciones de escritorio deben tener en cuenta los ppp.</span><span class="sxs-lookup"><span data-stu-id="88766-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="88766-110">Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP.</span><span class="sxs-lookup"><span data-stu-id="88766-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="88766-111">La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla).</span><span class="sxs-lookup"><span data-stu-id="88766-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="88766-112">Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88766-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDEVICEINRANGE       0X239
```



## <a name="parameters"></a><span data-ttu-id="88766-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88766-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88766-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="88766-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88766-115">Información adicional específica del mensaje.</span><span class="sxs-lookup"><span data-stu-id="88766-115">Additional message-specific information.</span></span>

</dd> <dt>

<span data-ttu-id="88766-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88766-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88766-117">Información adicional específica del mensaje.</span><span class="sxs-lookup"><span data-stu-id="88766-117">Additional message-specific information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88766-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88766-118">Return value</span></span>

<span data-ttu-id="88766-119">Si la aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="88766-119">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="88766-120">Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="88766-120">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="requirements"></a><span data-ttu-id="88766-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88766-121">Requirements</span></span>



| <span data-ttu-id="88766-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="88766-122">Requirement</span></span> | <span data-ttu-id="88766-123">Value</span><span class="sxs-lookup"><span data-stu-id="88766-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88766-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88766-124">Minimum supported client</span></span><br/> | <span data-ttu-id="88766-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="88766-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="88766-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88766-126">Minimum supported server</span></span><br/> | <span data-ttu-id="88766-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="88766-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="88766-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88766-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="88766-129"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88766-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88766-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="88766-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88766-131">Mensajes</span><span class="sxs-lookup"><span data-stu-id="88766-131">Messages</span></span>](messages.md)
</dt> </dl>

 

