---
description: Se envía a una aplicación para notificar los cambios en la ventana del IME. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 20e064b8-2baf-4b4c-8341-36c3e4643eff
title: Mensaje de WM_IME_NOTIFY (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca5ab1b2a1fd62d159ab4f216bf9b1bb6892ed69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686819"
---
# <a name="wm_ime_notify-message"></a><span data-ttu-id="d2217-104">Mensaje WM_IME_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="d2217-104">WM_IME_NOTIFY message</span></span>

<span data-ttu-id="d2217-105">Se envía a una aplicación para notificar los cambios en la ventana del IME.</span><span class="sxs-lookup"><span data-stu-id="d2217-105">Sent to an application to notify it of changes to the IME window.</span></span> <span data-ttu-id="d2217-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d2217-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_NOTIFY,   
  WPARAM wParam,   
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="d2217-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2217-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2217-108">*identificador*</span><span class="sxs-lookup"><span data-stu-id="d2217-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d2217-109">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="d2217-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="d2217-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2217-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2217-111">El comando.</span><span class="sxs-lookup"><span data-stu-id="d2217-111">The command.</span></span> <span data-ttu-id="d2217-112">Este parámetro puede tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d2217-112">This parameter can have one of the following values.</span></span>

<dl>
<dd><span data-ttu-id="d2217-113"><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="d2217-113"><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="d2217-114"><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="d2217-114"><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="d2217-115"><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="d2217-115"><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="d2217-116"><a href="imn-guideline.md">IMN_GUIDELINE</a></span><span class="sxs-lookup"><span data-stu-id="d2217-116"><a href="imn-guideline.md">IMN_GUIDELINE</a></span></span></dd> 
<dd><span data-ttu-id="d2217-117"><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="d2217-117"><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="d2217-118"><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="d2217-118"><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="d2217-119"><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="d2217-119"><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="d2217-120"><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="d2217-120"><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="d2217-121"><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="d2217-121"><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="d2217-122"><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></span><span class="sxs-lookup"><span data-stu-id="d2217-122"><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></span></span></dd> 
<dd><span data-ttu-id="d2217-123"><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></span><span class="sxs-lookup"><span data-stu-id="d2217-123"><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></span></span></dd> 
<dd><span data-ttu-id="d2217-124"><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></span><span class="sxs-lookup"><span data-stu-id="d2217-124"><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></span></span></dd> 
<dd><span data-ttu-id="d2217-125"><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="d2217-125"><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></span></span></dd> 
</dl> 
</dd> 
<dt>

<span data-ttu-id="d2217-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2217-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2217-127">Datos específicos del comando, con el formato que depende del valor del parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="d2217-127">Command-specific data, with format dependent on the value of the *wParam* parameter.</span></span> <span data-ttu-id="d2217-128">Para obtener más información, consulte la documentación de cada comando.</span><span class="sxs-lookup"><span data-stu-id="d2217-128">For more information, refer to the documentation for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2217-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2217-129">Return value</span></span>

<span data-ttu-id="d2217-130">El valor devuelto depende del comando enviado.</span><span class="sxs-lookup"><span data-stu-id="d2217-130">The return value depends on the command sent.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2217-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2217-131">Remarks</span></span>

<span data-ttu-id="d2217-132">Una aplicación procesa este mensaje si es responsable de administrar la ventana del IME.</span><span class="sxs-lookup"><span data-stu-id="d2217-132">An application processes this message if it is responsible for managing the IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2217-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2217-133">Requirements</span></span>



| <span data-ttu-id="d2217-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2217-134">Requirement</span></span> | <span data-ttu-id="d2217-135">Value</span><span class="sxs-lookup"><span data-stu-id="d2217-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2217-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2217-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d2217-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d2217-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="d2217-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2217-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d2217-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d2217-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="d2217-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2217-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2217-141"><dt>Winuser. h (include Windows. h); </dt> <dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2217-141"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2217-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2217-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2217-143">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="d2217-143">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d2217-144">Mensajes del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="d2217-144">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="d2217-145">IMN_CHANGECANDIDATE</span><span class="sxs-lookup"><span data-stu-id="d2217-145">IMN_CHANGECANDIDATE</span></span>](imn-changecandidate.md)
</dt> <dt>

[<span data-ttu-id="d2217-146">IMN_CLOSECANDIDATE</span><span class="sxs-lookup"><span data-stu-id="d2217-146">IMN_CLOSECANDIDATE</span></span>](imn-closecandidate.md)
</dt> <dt>

[<span data-ttu-id="d2217-147">IMN_CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="d2217-147">IMN_CLOSESTATUSWINDOW</span></span>](imn-closestatuswindow.md)
</dt> <dt>

[<span data-ttu-id="d2217-148">IMN_GUIDELINE</span><span class="sxs-lookup"><span data-stu-id="d2217-148">IMN_GUIDELINE</span></span>](imn-guideline.md)
</dt> <dt>

[<span data-ttu-id="d2217-149">IMN_OPENCANDIDATE</span><span class="sxs-lookup"><span data-stu-id="d2217-149">IMN_OPENCANDIDATE</span></span>](imn-opencandidate.md)
</dt> <dt>

[<span data-ttu-id="d2217-150">IMN_OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="d2217-150">IMN_OPENSTATUSWINDOW</span></span>](imn-openstatuswindow.md)
</dt> <dt>

[<span data-ttu-id="d2217-151">IMN_SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="d2217-151">IMN_SETCANDIDATEPOS</span></span>](imn-setcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="d2217-152">IMN_SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="d2217-152">IMN_SETCOMPOSITIONFONT</span></span>](imn-setcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="d2217-153">IMN_SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="d2217-153">IMN_SETCOMPOSITIONWINDOW</span></span>](imn-setcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="d2217-154">IMN_SETCONVERSIONMODE</span><span class="sxs-lookup"><span data-stu-id="d2217-154">IMN_SETCONVERSIONMODE</span></span>](imn-setconversionmode.md)
</dt> <dt>

[<span data-ttu-id="d2217-155">IMN_SETOPENSTATUS</span><span class="sxs-lookup"><span data-stu-id="d2217-155">IMN_SETOPENSTATUS</span></span>](imn-setopenstatus.md)
</dt> <dt>

[<span data-ttu-id="d2217-156">IMN_SETSENTENCEMODE</span><span class="sxs-lookup"><span data-stu-id="d2217-156">IMN_SETSENTENCEMODE</span></span>](imn-setsentencemode.md)
</dt> <dt>

[<span data-ttu-id="d2217-157">IMN_SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="d2217-157">IMN_SETSTATUSWINDOWPOS</span></span>](imn-setstatuswindowpos.md)
</dt> </dl>

 

 
