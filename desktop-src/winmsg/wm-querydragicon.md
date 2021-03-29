---
description: Se envía a una ventana minimizada (icónica).
ms.assetid: e4f0e638-f606-4745-888b-14a846c7fd37
title: Mensaje de WM_QUERYDRAGICON (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c6040df06923e778eb717db4148bed233db4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360715"
---
# <a name="wm_querydragicon-message"></a><span data-ttu-id="9429c-103">Mensaje de QUERYDRAGICON de WM \_</span><span class="sxs-lookup"><span data-stu-id="9429c-103">WM\_QUERYDRAGICON message</span></span>

<span data-ttu-id="9429c-104">Se envía a una ventana minimizada (icónica).</span><span class="sxs-lookup"><span data-stu-id="9429c-104">Sent to a minimized (iconic) window.</span></span> <span data-ttu-id="9429c-105">La ventana está a punto de ser arrastrada por el usuario, pero no tiene un icono definido para su clase.</span><span class="sxs-lookup"><span data-stu-id="9429c-105">The window is about to be dragged by the user but does not have an icon defined for its class.</span></span> <span data-ttu-id="9429c-106">Una aplicación puede devolver un identificador a un icono o un cursor.</span><span class="sxs-lookup"><span data-stu-id="9429c-106">An application can return a handle to an icon or cursor.</span></span> <span data-ttu-id="9429c-107">El sistema muestra este cursor o icono mientras el usuario arrastra el icono.</span><span class="sxs-lookup"><span data-stu-id="9429c-107">The system displays this cursor or icon while the user drags the icon.</span></span>

<span data-ttu-id="9429c-108">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9429c-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_QUERYDRAGICON                0x0037
```



## <a name="parameters"></a><span data-ttu-id="9429c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9429c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9429c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9429c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9429c-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9429c-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9429c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9429c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9429c-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9429c-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9429c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9429c-114">Return value</span></span>

<span data-ttu-id="9429c-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="9429c-115">Type: **LRESULT**</span></span>

<span data-ttu-id="9429c-116">Una aplicación debe devolver un identificador a un cursor o icono que el sistema va a mostrar mientras el usuario arrastra el icono.</span><span class="sxs-lookup"><span data-stu-id="9429c-116">An application should return a handle to a cursor or icon that the system is to display while the user drags the icon.</span></span> <span data-ttu-id="9429c-117">El cursor o el icono deben ser compatibles con la resolución del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="9429c-117">The cursor or icon must be compatible with the display driver's resolution.</span></span> <span data-ttu-id="9429c-118">Si la aplicación devuelve **null**, el sistema muestra el cursor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9429c-118">If the application returns **NULL**, the system displays the default cursor.</span></span>

## <a name="remarks"></a><span data-ttu-id="9429c-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9429c-119">Remarks</span></span>

<span data-ttu-id="9429c-120">Cuando el usuario arrastra el icono de una ventana sin un icono de clase, el sistema reemplaza el icono por un cursor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9429c-120">When the user drags the icon of a window without a class icon, the system replaces the icon with a default cursor.</span></span> <span data-ttu-id="9429c-121">Si la aplicación requiere que se muestre un cursor diferente durante el arrastre, debe devolver un identificador para el cursor o el icono compatible con la resolución del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="9429c-121">If the application requires a different cursor to be displayed during dragging, it must return a handle to the cursor or icon compatible with the display driver's resolution.</span></span> <span data-ttu-id="9429c-122">Si una aplicación devuelve un identificador a un cursor de color o un icono, el sistema convierte el cursor o el icono en blanco y negro.</span><span class="sxs-lookup"><span data-stu-id="9429c-122">If an application returns a handle to a color cursor or icon, the system converts the cursor or icon to black and white.</span></span> <span data-ttu-id="9429c-123">La aplicación puede llamar a la función [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) o [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) para cargar un cursor o un icono de los recursos en su archivo ejecutable (. exe) y para recuperar este identificador.</span><span class="sxs-lookup"><span data-stu-id="9429c-123">The application can call the [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) or [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function to load a cursor or icon from the resources in its executable (.exe) file and to retrieve this handle.</span></span>

<span data-ttu-id="9429c-124">Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en un **booleano** y devolver el valor directamente.</span><span class="sxs-lookup"><span data-stu-id="9429c-124">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="9429c-125">Se omite el valor de **DWL \_ MSGRESULT** establecido por la función [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="9429c-125">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="9429c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9429c-126">Requirements</span></span>



| <span data-ttu-id="9429c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9429c-127">Requirement</span></span> | <span data-ttu-id="9429c-128">Value</span><span class="sxs-lookup"><span data-stu-id="9429c-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9429c-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9429c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9429c-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9429c-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9429c-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9429c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9429c-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9429c-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9429c-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9429c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9429c-134"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9429c-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9429c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="9429c-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="9429c-136">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="9429c-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9429c-137">**LoadCursor**</span><span class="sxs-lookup"><span data-stu-id="9429c-137">**LoadCursor**</span></span>](/windows/win32/api/winuser/nf-winuser-loadcursora)
</dt> <dt>

[<span data-ttu-id="9429c-138">**LoadIcon**</span><span class="sxs-lookup"><span data-stu-id="9429c-138">**LoadIcon**</span></span>](/windows/win32/api/winuser/nf-winuser-loadicona)
</dt> <dt>

<span data-ttu-id="9429c-139">**Vista**</span><span class="sxs-lookup"><span data-stu-id="9429c-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9429c-140">Windows</span><span class="sxs-lookup"><span data-stu-id="9429c-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
