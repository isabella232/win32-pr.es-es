---
description: Se envía a una aplicación cuando el IME finaliza la composición. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: d0f05524-4dfc-45b2-9476-6f1244190de5
title: Mensaje de WM_IME_ENDCOMPOSITION (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ca9d1560810b22ae0d36010d2371e75b83a81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360325"
---
# <a name="wm_ime_endcomposition-message"></a><span data-ttu-id="db5d1-104">\_Mensaje ENDCOMPOSITION de IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="db5d1-104">WM\_IME\_ENDCOMPOSITION message</span></span>

<span data-ttu-id="db5d1-105">Se envía a una aplicación cuando el IME finaliza la composición.</span><span class="sxs-lookup"><span data-stu-id="db5d1-105">Sent to an application when the IME ends composition.</span></span> <span data-ttu-id="db5d1-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="db5d1-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,      
  WM_IME_ENDCOMPOSITION,  
  WPARAM wParam,      
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="db5d1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db5d1-107">Parameters</span></span>

<span data-ttu-id="db5d1-108">Este mensaje no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="db5d1-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="db5d1-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db5d1-109">Return value</span></span>

<span data-ttu-id="db5d1-110">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="db5d1-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db5d1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db5d1-111">Remarks</span></span>

<span data-ttu-id="db5d1-112">Una aplicación debe procesar este mensaje si muestra los propios caracteres de composición.</span><span class="sxs-lookup"><span data-stu-id="db5d1-112">An application should process this message if it displays composition characters itself.</span></span>

<span data-ttu-id="db5d1-113">Si la aplicación ha creado una ventana de IME, debe pasar este mensaje a esa ventana.</span><span class="sxs-lookup"><span data-stu-id="db5d1-113">If the application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="db5d1-114">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  procesa este mensaje pasándolo a la ventana IME predeterminada.</span><span class="sxs-lookup"><span data-stu-id="db5d1-114">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing it to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="db5d1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db5d1-115">Requirements</span></span>



| <span data-ttu-id="db5d1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="db5d1-116">Requirement</span></span> | <span data-ttu-id="db5d1-117">Value</span><span class="sxs-lookup"><span data-stu-id="db5d1-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db5d1-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db5d1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="db5d1-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="db5d1-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="db5d1-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db5d1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="db5d1-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="db5d1-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="db5d1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db5d1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="db5d1-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db5d1-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db5d1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="db5d1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db5d1-125">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="db5d1-125">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="db5d1-126">Mensajes del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="db5d1-126">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
