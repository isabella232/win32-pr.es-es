---
description: Se envía para cancelar determinados modos, como la captura del mouse.
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: Mensaje de WM_CANCELMODE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23b842dfdfde7dc550d8ec6d942bcc83ea25f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706674"
---
# <a name="wm_cancelmode-message"></a><span data-ttu-id="7c63e-103">Mensaje de CANCELMODE de WM \_</span><span class="sxs-lookup"><span data-stu-id="7c63e-103">WM\_CANCELMODE message</span></span>

<span data-ttu-id="7c63e-104">Se envía para cancelar determinados modos, como la captura del mouse.</span><span class="sxs-lookup"><span data-stu-id="7c63e-104">Sent to cancel certain modes, such as mouse capture.</span></span> <span data-ttu-id="7c63e-105">Por ejemplo, el sistema envía este mensaje a la ventana activa cuando se muestra un cuadro de diálogo o un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="7c63e-105">For example, the system sends this message to the active window when a dialog box or message box is displayed.</span></span> <span data-ttu-id="7c63e-106">Ciertas funciones también envían este mensaje explícitamente a la ventana especificada independientemente de si se trata de la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="7c63e-106">Certain functions also send this message explicitly to the specified window regardless of whether it is the active window.</span></span> <span data-ttu-id="7c63e-107">Por ejemplo, la función [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) envía este mensaje al deshabilitar la ventana especificada.</span><span class="sxs-lookup"><span data-stu-id="7c63e-107">For example, the [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) function sends this message when disabling the specified window.</span></span>

<span data-ttu-id="7c63e-108">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7c63e-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CANCELMODE                   0x001F
```



## <a name="parameters"></a><span data-ttu-id="7c63e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c63e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c63e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c63e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c63e-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="7c63e-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c63e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c63e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c63e-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="7c63e-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c63e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c63e-114">Return value</span></span>

<span data-ttu-id="7c63e-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="7c63e-115">Type: **LRESULT**</span></span>

<span data-ttu-id="7c63e-116">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="7c63e-116">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c63e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c63e-117">Remarks</span></span>

<span data-ttu-id="7c63e-118">Cuando se envía el mensaje de **\_ CANCELMODE de WM** , la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) cancela el procesamiento interno de la entrada de la barra de desplazamiento estándar, cancela el procesamiento interno del menú y libera la captura del mouse.</span><span class="sxs-lookup"><span data-stu-id="7c63e-118">When the **WM\_CANCELMODE** message is sent, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function cancels internal processing of standard scroll bar input, cancels internal menu processing, and releases the mouse capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c63e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c63e-119">Requirements</span></span>



| <span data-ttu-id="7c63e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c63e-120">Requirement</span></span> | <span data-ttu-id="7c63e-121">Value</span><span class="sxs-lookup"><span data-stu-id="7c63e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c63e-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c63e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7c63e-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7c63e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7c63e-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c63e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7c63e-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7c63e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7c63e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c63e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c63e-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c63e-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c63e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c63e-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c63e-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="7c63e-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7c63e-130">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="7c63e-130">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="7c63e-131">**EnableWindow**</span><span class="sxs-lookup"><span data-stu-id="7c63e-131">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[<span data-ttu-id="7c63e-132">**ReleaseCapture**</span><span class="sxs-lookup"><span data-stu-id="7c63e-132">**ReleaseCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

<span data-ttu-id="7c63e-133">**Vista**</span><span class="sxs-lookup"><span data-stu-id="7c63e-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7c63e-134">Windows</span><span class="sxs-lookup"><span data-stu-id="7c63e-134">Windows</span></span>](windows.md)
</dt> </dl>

 

 
