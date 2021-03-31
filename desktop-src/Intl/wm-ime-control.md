---
description: Enviado por una aplicación para dirigir la ventana del IME para llevar a cabo el comando solicitado.
ms.assetid: 5d3b7f8a-57c9-41e3-8022-9a3f515fc32e
title: Mensaje de WM_IME_CONTROL (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd0adc534883bc0b31984c8d3e9b57a04b555987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907991"
---
# <a name="wm_ime_control-message"></a><span data-ttu-id="e1697-103">Mensaje WM_IME_CONTROL</span><span class="sxs-lookup"><span data-stu-id="e1697-103">WM_IME_CONTROL message</span></span>

<span data-ttu-id="e1697-104">Enviado por una aplicación para dirigir la ventana del IME para llevar a cabo el comando solicitado.</span><span class="sxs-lookup"><span data-stu-id="e1697-104">Sent by an application to direct the IME window to carry out the requested command.</span></span> <span data-ttu-id="e1697-105">La aplicación usa este mensaje para controlar la ventana del IME que ha creado.</span><span class="sxs-lookup"><span data-stu-id="e1697-105">The application uses this message to control the IME window that it has created.</span></span> <span data-ttu-id="e1697-106">Para enviar este mensaje, la aplicación llama a la función [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="e1697-106">To send this message, the application calls the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage(
  HWND   hwnd,
  WM_IME_CONTROL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="e1697-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1697-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1697-108">*identificador*</span><span class="sxs-lookup"><span data-stu-id="e1697-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e1697-109">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="e1697-109">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="e1697-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e1697-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1697-111">El comando.</span><span class="sxs-lookup"><span data-stu-id="e1697-111">The command.</span></span> <span data-ttu-id="e1697-112">Este parámetro puede tener uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="e1697-112">This parameter can have one of the following values:</span></span>

<dl>
<dd><span data-ttu-id="e1697-113"><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="e1697-113"><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="e1697-114"><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="e1697-114"><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="e1697-115"><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="e1697-115"><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="e1697-116"><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="e1697-116"><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="e1697-117"><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="e1697-117"><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></span></span></dd> 
<dd><span data-ttu-id="e1697-118"><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="e1697-118"><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="e1697-119"><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="e1697-119"><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="e1697-120"><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></span><span class="sxs-lookup"><span data-stu-id="e1697-120"><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></span></span></dd> 
<dd><span data-ttu-id="e1697-121"><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="e1697-121"><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="e1697-122"><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="e1697-122"><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></span></span></dd> 
</dl>
</dd>

<dt>

<span data-ttu-id="e1697-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1697-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1697-124">Datos específicos del comando, con el formato que depende del valor del parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="e1697-124">Command-specific data, with format dependent on the value of the *wParam* parameter.</span></span> <span data-ttu-id="e1697-125">Para obtener más información, consulte la documentación de cada comando.</span><span class="sxs-lookup"><span data-stu-id="e1697-125">For more information, refer to the documentation for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1697-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1697-126">Return value</span></span>

<span data-ttu-id="e1697-127">El mensaje devuelve un valor específico del comando.</span><span class="sxs-lookup"><span data-stu-id="e1697-127">The message returns a command-specific value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1697-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1697-128">Requirements</span></span>



| <span data-ttu-id="e1697-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1697-129">Requirement</span></span> | <span data-ttu-id="e1697-130">Value</span><span class="sxs-lookup"><span data-stu-id="e1697-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1697-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1697-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e1697-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e1697-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="e1697-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1697-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e1697-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e1697-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="e1697-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1697-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1697-136"><dt>Winuser. h (include Windows. h); </dt> <dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1697-136"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1697-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1697-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1697-138">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="e1697-138">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="e1697-139">Mensajes del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="e1697-139">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="e1697-140">IMC_CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="e1697-140">IMC_CLOSESTATUSWINDOW</span></span>](imc-closestatuswindow.md)
</dt> <dt>

[<span data-ttu-id="e1697-141">IMC_GETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="e1697-141">IMC_GETCANDIDATEPOS</span></span>](imc-getcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="e1697-142">IMC_GETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="e1697-142">IMC_GETCOMPOSITIONFONT</span></span>](imc-getcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="e1697-143">IMC_GETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="e1697-143">IMC_GETCOMPOSITIONWINDOW</span></span>](imc-getcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="e1697-144">IMC_GETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="e1697-144">IMC_GETSTATUSWINDOWPOS</span></span>](imc-getstatuswindowpos.md)
</dt> <dt>

[<span data-ttu-id="e1697-145">IMC_OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="e1697-145">IMC_OPENSTATUSWINDOW</span></span>](imc-openstatuswindow.md)
</dt> <dt>

[<span data-ttu-id="e1697-146">IMC_SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="e1697-146">IMC_SETCANDIDATEPOS</span></span>](imc-setcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="e1697-147">IMC_SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="e1697-147">IMC_SETCOMPOSITIONFONT</span></span>](imc-setcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="e1697-148">IMC_SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="e1697-148">IMC_SETCOMPOSITIONWINDOW</span></span>](imc-setcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="e1697-149">IMC_SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="e1697-149">IMC_SETSTATUSWINDOWPOS</span></span>](imc-setstatuswindowpos.md)
</dt> </dl>

 

 
