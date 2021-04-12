---
description: Se envía a una aplicación cuando se activa una ventana. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: Mensaje de WM_IME_SETCONTEXT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b36cb1e80127d1a451dabcc457dc364a27878ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275441"
---
# <a name="wm_ime_setcontext-message"></a><span data-ttu-id="5d96d-104">\_Mensaje SETCONTEXT de IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="5d96d-104">WM\_IME\_SETCONTEXT message</span></span>

<span data-ttu-id="5d96d-105">Se envía a una aplicación cuando se activa una ventana.</span><span class="sxs-lookup"><span data-stu-id="5d96d-105">Sent to an application when a window is activated.</span></span> <span data-ttu-id="5d96d-106">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5d96d-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,  
  WM_IME_SETCONTEXT,  
  WPARAM wParam,      
  LPARAM lParam      
);
```



## <a name="parameters"></a><span data-ttu-id="5d96d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d96d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d96d-108">*identificador*</span><span class="sxs-lookup"><span data-stu-id="5d96d-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="5d96d-109">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="5d96d-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="5d96d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d96d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d96d-111">**True** si la ventana está activa y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5d96d-111">**TRUE** if the window is active, and **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="5d96d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d96d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d96d-113">Opciones de visualización.</span><span class="sxs-lookup"><span data-stu-id="5d96d-113">Display options.</span></span> <span data-ttu-id="5d96d-114">Este parámetro puede tener uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5d96d-114">This parameter can have one or more of the following values.</span></span>



| <span data-ttu-id="5d96d-115">Value</span><span class="sxs-lookup"><span data-stu-id="5d96d-115">Value</span></span>                                                                                                                                                                                                   | <span data-ttu-id="5d96d-116">Significado</span><span class="sxs-lookup"><span data-stu-id="5d96d-116">Meaning</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <span data-ttu-id="5d96d-117"><dt>**SHOWUICOMPOSITIONWINDOW de ISC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d96d-117"><dt>**ISC\_SHOWUICOMPOSITIONWINDOW**</dt></span></span> </dl> | <span data-ttu-id="5d96d-118">Mostrar la ventana de composición por la ventana de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d96d-118">Show the composition window by user interface window.</span></span><br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <span data-ttu-id="5d96d-119"><dt>**SHOWUIGUIDWINDOW de ISC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d96d-119"><dt>**ISC\_SHOWUIGUIDWINDOW**</dt></span></span> </dl>                      | <span data-ttu-id="5d96d-120">Mostrar la ventana guía por la ventana de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d96d-120">Show the guide window by user interface window.</span></span><br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <span data-ttu-id="5d96d-121"><dt>**SHOWUISOFTKBD de ISC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d96d-121"><dt>**ISC\_SHOWUISOFTKBD**</dt></span></span> </dl>                               | <span data-ttu-id="5d96d-122">Mostrar la ventana de la interfaz de usuario de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="5d96d-122">Show the soft keyboard by user interface window.</span></span><br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <span data-ttu-id="5d96d-123"><dt>**SHOWUICANDIDATEWINDOW de ISC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d96d-123"><dt>**ISC\_SHOWUICANDIDATEWINDOW**</dt></span></span> </dl>       | <span data-ttu-id="5d96d-124">Mostrar la ventana de candidatos de índice 0 por ventana de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d96d-124">Show the candidate window of index 0 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="5d96d-125"><dt>SHOWUICANDIDATEWINDOW de ISC \_ << 1</dt></span><span class="sxs-lookup"><span data-stu-id="5d96d-125"><dt>ISC\_SHOWUICANDIDATEWINDOW << 1</dt></span></span> </dl>                                                                                        | <span data-ttu-id="5d96d-126">Mostrar la ventana de candidatos de índice 1 por ventana de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d96d-126">Show the candidate window of index 1 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="5d96d-127"><dt>SHOWUICANDIDATEWINDOW de ISC \_ << 2</dt></span><span class="sxs-lookup"><span data-stu-id="5d96d-127"><dt>ISC\_SHOWUICANDIDATEWINDOW << 2</dt></span></span> </dl>                                                                                        | <span data-ttu-id="5d96d-128">Mostrar la ventana candidatos de índice 2 por ventana de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d96d-128">Show the candidate window of index 2 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="5d96d-129"><dt>SHOWUICANDIDATEWINDOW de ISC \_ << 3</dt></span><span class="sxs-lookup"><span data-stu-id="5d96d-129"><dt>ISC\_SHOWUICANDIDATEWINDOW << 3</dt></span></span> </dl>                                                                                        | <span data-ttu-id="5d96d-130">Mostrar la ventana candidato de la ventana índice 3 por interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d96d-130">Show the candidate window of index 3 by user interface window.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d96d-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d96d-131">Return value</span></span>

<span data-ttu-id="5d96d-132">Devuelve el valor devuelto por [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span><span class="sxs-lookup"><span data-stu-id="5d96d-132">Returns the value returned by [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span>

## <a name="remarks"></a><span data-ttu-id="5d96d-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d96d-133">Remarks</span></span>

<span data-ttu-id="5d96d-134">Si la aplicación ha creado una ventana de IME, debe llamar a [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span><span class="sxs-lookup"><span data-stu-id="5d96d-134">If the application has created an IME window, it should call [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span> <span data-ttu-id="5d96d-135">De lo contrario, debe pasar este mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="5d96d-135">Otherwise, it should pass this message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="5d96d-136">Si la aplicación dibuja la ventana de composición, la ventana del IME predeterminada no tiene que mostrar su ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="5d96d-136">If the application draws the composition window, the default IME window does not have to show its composition window.</span></span> <span data-ttu-id="5d96d-137">En este caso, la aplicación debe borrar el valor de **\_ SHOWUICOMPOSITIONWINDOW de ISC** del parámetro *lParam* antes de pasar el mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span><span class="sxs-lookup"><span data-stu-id="5d96d-137">In this case, the application must clear the **ISC\_SHOWUICOMPOSITIONWINDOW** value from the *lParam* parameter before passing the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span> <span data-ttu-id="5d96d-138">Para mostrar una determinada ventana de la interfaz de usuario, una aplicación debe quitar el valor correspondiente para que el IME no la muestre.</span><span class="sxs-lookup"><span data-stu-id="5d96d-138">To display a certain user interface window, an application should remove the corresponding value so that the IME will not display it.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d96d-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d96d-139">Requirements</span></span>



| <span data-ttu-id="5d96d-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d96d-140">Requirement</span></span> | <span data-ttu-id="5d96d-141">Value</span><span class="sxs-lookup"><span data-stu-id="5d96d-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d96d-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d96d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5d96d-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5d96d-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="5d96d-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d96d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5d96d-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5d96d-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="5d96d-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d96d-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d96d-147"><dt>Winuser. h (include Windows. h); </dt> <dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d96d-147"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d96d-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d96d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d96d-149">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="5d96d-149">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="5d96d-150">Mensajes del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="5d96d-150">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="5d96d-151">**ImmIsUIMessage**</span><span class="sxs-lookup"><span data-stu-id="5d96d-151">**ImmIsUIMessage**</span></span>](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
