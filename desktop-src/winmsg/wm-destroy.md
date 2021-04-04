---
description: Se envía cuando se destruye una ventana. Se envía al procedimiento de ventana de la ventana que se va a destruir después de quitar la ventana de la pantalla.
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: Mensaje de WM_DESTROY (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db195c22c38759146fb76e98edf4ca7f605a1c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277766"
---
# <a name="wm_destroy-message"></a><span data-ttu-id="8c7c3-104">Mensaje de destrucción de WM \_</span><span class="sxs-lookup"><span data-stu-id="8c7c3-104">WM\_DESTROY message</span></span>

<span data-ttu-id="8c7c3-105">Se envía cuando se destruye una ventana.</span><span class="sxs-lookup"><span data-stu-id="8c7c3-105">Sent when a window is being destroyed.</span></span> <span data-ttu-id="8c7c3-106">Se envía al procedimiento de ventana de la ventana que se va a destruir después de quitar la ventana de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="8c7c3-106">It is sent to the window procedure of the window being destroyed after the window is removed from the screen.</span></span>

<span data-ttu-id="8c7c3-107">Este mensaje se envía primero a la ventana que se está destruyendo y, a continuación, a las ventanas secundarias (si existen) a medida que se destruyen.</span><span class="sxs-lookup"><span data-stu-id="8c7c3-107">This message is sent first to the window being destroyed and then to the child windows (if any) as they are destroyed.</span></span> <span data-ttu-id="8c7c3-108">Durante el procesamiento del mensaje, se puede suponer que todas las ventanas secundarias todavía existen.</span><span class="sxs-lookup"><span data-stu-id="8c7c3-108">During the processing of the message, it can be assumed that all child windows still exist.</span></span>

<span data-ttu-id="8c7c3-109">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8c7c3-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DESTROY                      0x0002
```



## <a name="parameters"></a><span data-ttu-id="8c7c3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c7c3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c7c3-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c7c3-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c7c3-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="8c7c3-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8c7c3-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c7c3-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c7c3-114">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="8c7c3-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c7c3-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c7c3-115">Return value</span></span>

<span data-ttu-id="8c7c3-116">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="8c7c3-116">Type: **LRESULT**</span></span>

<span data-ttu-id="8c7c3-117">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="8c7c3-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c7c3-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c7c3-118">Remarks</span></span>

<span data-ttu-id="8c7c3-119">Si la ventana que se va a destruir forma parte de la cadena del visor del portapapeles (establecida mediante una llamada a la función [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) ), la ventana debe quitarse de la cadena procesando la función [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) antes de volver del mensaje de **\_ destrucción de WM** .</span><span class="sxs-lookup"><span data-stu-id="8c7c3-119">If the window being destroyed is part of the clipboard viewer chain (set by calling the [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) function), the window must remove itself from the chain by processing the [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) function before returning from the **WM\_DESTROY** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c7c3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c7c3-120">Requirements</span></span>



| <span data-ttu-id="8c7c3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c7c3-121">Requirement</span></span> | <span data-ttu-id="8c7c3-122">Value</span><span class="sxs-lookup"><span data-stu-id="8c7c3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c7c3-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c7c3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8c7c3-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8c7c3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8c7c3-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c7c3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8c7c3-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8c7c3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8c7c3-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c7c3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c7c3-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c7c3-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c7c3-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c7c3-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="8c7c3-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="8c7c3-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8c7c3-131">**ChangeClipboardChain**</span><span class="sxs-lookup"><span data-stu-id="8c7c3-131">**ChangeClipboardChain**</span></span>](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[<span data-ttu-id="8c7c3-132">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="8c7c3-132">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="8c7c3-133">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="8c7c3-133">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[<span data-ttu-id="8c7c3-134">**SetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="8c7c3-134">**SetClipboardViewer**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[<span data-ttu-id="8c7c3-135">**cierre de WM \_**</span><span class="sxs-lookup"><span data-stu-id="8c7c3-135">**WM\_CLOSE**</span></span>](wm-close.md)
</dt> <dt>

<span data-ttu-id="8c7c3-136">**Vista**</span><span class="sxs-lookup"><span data-stu-id="8c7c3-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8c7c3-137">Windows</span><span class="sxs-lookup"><span data-stu-id="8c7c3-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
