---
description: Se envía inmediatamente antes de que el IME genere la cadena de composición como resultado de una pulsación de tecla. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 2740d009-8685-4f70-9b01-67b71f4ddcbd
title: Mensaje de WM_IME_STARTCOMPOSITION (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bd9a93b4c6c2e8dba6658c84b5f431dd9a54e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907989"
---
# <a name="wm_ime_startcomposition-message"></a><span data-ttu-id="f2f2f-104">\_Mensaje STARTCOMPOSITION de IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="f2f2f-104">WM\_IME\_STARTCOMPOSITION message</span></span>

<span data-ttu-id="f2f2f-105">Se envía inmediatamente antes de que el IME genere la cadena de composición como resultado de una pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-105">Sent immediately before the IME generates the composition string as a result of a keystroke.</span></span> <span data-ttu-id="f2f2f-106">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f2f2f-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,                
  WM_IME_STARTCOMPOSITION,  
  WPARAM wParam,            
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="f2f2f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2f2f-107">Parameters</span></span>

<span data-ttu-id="f2f2f-108">Este mensaje no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="f2f2f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2f2f-109">Return value</span></span>

<span data-ttu-id="f2f2f-110">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2f2f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2f2f-111">Remarks</span></span>

<span data-ttu-id="f2f2f-112">Este mensaje es una notificación a una ventana de IME para abrir su ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-112">This message is a notification to an IME window to open its composition window.</span></span> <span data-ttu-id="f2f2f-113">Una aplicación debe procesar este mensaje si muestra los propios caracteres de composición.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-113">An application should process this message if it displays composition characters itself.</span></span>

<span data-ttu-id="f2f2f-114">Si una aplicación ha creado una ventana de IME, debe pasar este mensaje a esa ventana.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-114">If an application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="f2f2f-115">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) procesa el mensaje pasándolo a la ventana IME predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function processes the message by passing it to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2f2f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2f2f-116">Requirements</span></span>



| <span data-ttu-id="f2f2f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2f2f-117">Requirement</span></span> | <span data-ttu-id="f2f2f-118">Value</span><span class="sxs-lookup"><span data-stu-id="f2f2f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2f2f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2f2f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f2f2f-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f2f2f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f2f2f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2f2f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f2f2f-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f2f2f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f2f2f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2f2f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2f2f-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2f2f-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2f2f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2f2f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2f2f-126">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="f2f2f-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="f2f2f-127">Mensajes del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="f2f2f-127">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
