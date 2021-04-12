---
description: Se envía a una aplicación cuando la ventana del IME no encuentra ningún espacio para extender el área de la ventana de composición. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: Mensaje de WM_IME_COMPOSITIONFULL (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33051ac3e4e893eb803d4b13d7bfbf53751258b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279489"
---
# <a name="wm_ime_compositionfull-message"></a><span data-ttu-id="93e1c-104">\_Mensaje COMPOSITIONFULL de IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="93e1c-104">WM\_IME\_COMPOSITIONFULL message</span></span>

<span data-ttu-id="93e1c-105">Se envía a una aplicación cuando la ventana del IME no encuentra ningún espacio para extender el área de la ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="93e1c-105">Sent to an application when the IME window finds no space to extend the area for the composition window.</span></span> <span data-ttu-id="93e1c-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="93e1c-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,
  WM_IME_COMPOSITIONFULL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="93e1c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93e1c-107">Parameters</span></span>

<span data-ttu-id="93e1c-108">Este mensaje no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="93e1c-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="93e1c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93e1c-109">Return value</span></span>

<span data-ttu-id="93e1c-110">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="93e1c-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="93e1c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93e1c-111">Remarks</span></span>

<span data-ttu-id="93e1c-112">La aplicación debe usar el comando [IMC \_ SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) para especificar cómo se debe mostrar la ventana.</span><span class="sxs-lookup"><span data-stu-id="93e1c-112">The application should use the [IMC\_SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) command to specify how the window should be displayed.</span></span>

<span data-ttu-id="93e1c-113">La ventana del IME, en lugar del IME, envía este mensaje de notificación mediante la función [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="93e1c-113">The IME window, instead of the IME, sends this notification message by the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="93e1c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93e1c-114">Requirements</span></span>



| <span data-ttu-id="93e1c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="93e1c-115">Requirement</span></span> | <span data-ttu-id="93e1c-116">Value</span><span class="sxs-lookup"><span data-stu-id="93e1c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93e1c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93e1c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="93e1c-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="93e1c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="93e1c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93e1c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="93e1c-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="93e1c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="93e1c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93e1c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="93e1c-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93e1c-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93e1c-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="93e1c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93e1c-124">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="93e1c-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="93e1c-125">Mensajes del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="93e1c-125">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="93e1c-126">SETCOMPOSITIONWINDOW de IMC \_</span><span class="sxs-lookup"><span data-stu-id="93e1c-126">IMC\_SETCOMPOSITIONWINDOW</span></span>](imc-setcompositionwindow.md)
</dt> </dl>

 

 
