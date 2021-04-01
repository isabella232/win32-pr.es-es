---
title: Mensaje WM_POINTERDEVICEOUTOFRANGE
description: Se envía a una ventana cuando un dispositivo de puntero ha devuelto el intervalo de un digitalizador de entrada. Este mensaje contiene información relacionada con el dispositivo y su proximidad.
ms.assetid: 6BC667C1-6D9A-4E69-BAC6-761A1859F09E
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERDEVICEOUTOFRANGE
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEOUTOFRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: c222d9a35cae89838d7b6e1d99dcecd11f85b54d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150148"
---
# <a name="wm_pointerdeviceoutofrange-message"></a><span data-ttu-id="79988-105">Mensaje WM_POINTERDEVICEOUTOFRANGE</span><span class="sxs-lookup"><span data-stu-id="79988-105">WM_POINTERDEVICEOUTOFRANGE message</span></span>

<span data-ttu-id="79988-106">Se envía a una ventana cuando un dispositivo de puntero ha devuelto el intervalo de un digitalizador de entrada.</span><span class="sxs-lookup"><span data-stu-id="79988-106">Sent to a window when a pointer device has departed the range of an input digitizer.</span></span> <span data-ttu-id="79988-107">Este mensaje contiene información relacionada con el dispositivo y su proximidad.</span><span class="sxs-lookup"><span data-stu-id="79988-107">This message contains information regarding the device and its proximity.</span></span>

> <span data-ttu-id="79988-108">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="79988-108">\[!Important\]</span></span>  
> <span data-ttu-id="79988-109">Las aplicaciones de escritorio deben tener en cuenta los ppp.</span><span class="sxs-lookup"><span data-stu-id="79988-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="79988-110">Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP.</span><span class="sxs-lookup"><span data-stu-id="79988-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="79988-111">La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla).</span><span class="sxs-lookup"><span data-stu-id="79988-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="79988-112">Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79988-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDEVICEOUTOFRANGE       0X23A
```



## <a name="parameters"></a><span data-ttu-id="79988-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79988-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79988-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79988-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79988-115">Información adicional específica del mensaje.</span><span class="sxs-lookup"><span data-stu-id="79988-115">Additional message-specific information.</span></span>

</dd> <dt>

<span data-ttu-id="79988-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79988-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79988-117">Información adicional específica del mensaje.</span><span class="sxs-lookup"><span data-stu-id="79988-117">Additional message-specific information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79988-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79988-118">Return value</span></span>

<span data-ttu-id="79988-119">Si la aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="79988-119">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="79988-120">Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="79988-120">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="requirements"></a><span data-ttu-id="79988-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79988-121">Requirements</span></span>



| <span data-ttu-id="79988-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="79988-122">Requirement</span></span> | <span data-ttu-id="79988-123">Value</span><span class="sxs-lookup"><span data-stu-id="79988-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79988-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79988-124">Minimum supported client</span></span><br/> | <span data-ttu-id="79988-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="79988-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="79988-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79988-126">Minimum supported server</span></span><br/> | <span data-ttu-id="79988-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="79988-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="79988-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79988-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="79988-129"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79988-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79988-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="79988-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79988-131">Mensajes</span><span class="sxs-lookup"><span data-stu-id="79988-131">Messages</span></span>](messages.md)
</dt> </dl>

 

