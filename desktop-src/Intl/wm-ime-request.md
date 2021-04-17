---
description: Se envía a una aplicación para proporcionar comandos y solicitar información. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: c5e9f256-eed2-46cb-bb33-0e640a975f1f
title: Mensaje de WM_IME_REQUEST (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d0cea120d088fe1423b1d7dcb822307886675b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652433"
---
# <a name="wm_ime_request-message"></a><span data-ttu-id="e6d13-104">Mensaje WM_IME_REQUEST</span><span class="sxs-lookup"><span data-stu-id="e6d13-104">WM_IME_REQUEST message</span></span>

<span data-ttu-id="e6d13-105">Se envía a una aplicación para proporcionar comandos y solicitar información.</span><span class="sxs-lookup"><span data-stu-id="e6d13-105">Sent to an application to provide commands and request information.</span></span> <span data-ttu-id="e6d13-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e6d13-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_REQUEST,  
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="e6d13-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6d13-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6d13-108">*identificador*</span><span class="sxs-lookup"><span data-stu-id="e6d13-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e6d13-109">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="e6d13-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="e6d13-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6d13-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6d13-111">Comando.</span><span class="sxs-lookup"><span data-stu-id="e6d13-111">Command.</span></span> <span data-ttu-id="e6d13-112">Este parámetro puede tener uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="e6d13-112">This parameter can have one of the following values:</span></span>

<dl> 
<dd><span data-ttu-id="e6d13-113"><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="e6d13-113"><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="e6d13-114"><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="e6d13-114"><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="e6d13-115"><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="e6d13-115"><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="e6d13-116"><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></span><span class="sxs-lookup"><span data-stu-id="e6d13-116"><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></span></span></dd> 
<dd><span data-ttu-id="e6d13-117"><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></span><span class="sxs-lookup"><span data-stu-id="e6d13-117"><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></span></span></dd> 
<dd><span data-ttu-id="e6d13-118"><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></span><span class="sxs-lookup"><span data-stu-id="e6d13-118"><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></span></span></dd> 
<dd><span data-ttu-id="e6d13-119"><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></span><span class="sxs-lookup"><span data-stu-id="e6d13-119"><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></span></span></dd> 
</dl> 
</dd> 
<dt>

<span data-ttu-id="e6d13-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6d13-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6d13-121">Datos específicos del comando.</span><span class="sxs-lookup"><span data-stu-id="e6d13-121">Command-specific data.</span></span> <span data-ttu-id="e6d13-122">Para obtener más información, consulte la descripción de cada comando.</span><span class="sxs-lookup"><span data-stu-id="e6d13-122">For more information, see the description for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6d13-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6d13-123">Return value</span></span>

<span data-ttu-id="e6d13-124">Devuelve un valor específico del comando.</span><span class="sxs-lookup"><span data-stu-id="e6d13-124">Returns a command-specific value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6d13-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6d13-125">Requirements</span></span>



| <span data-ttu-id="e6d13-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6d13-126">Requirement</span></span> | <span data-ttu-id="e6d13-127">Value</span><span class="sxs-lookup"><span data-stu-id="e6d13-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d13-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6d13-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e6d13-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e6d13-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="e6d13-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6d13-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e6d13-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e6d13-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="e6d13-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6d13-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6d13-133"><dt>Winuser. h (include Windows. h); </dt> <dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6d13-133"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6d13-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6d13-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6d13-135">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="e6d13-135">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="e6d13-136">Mensajes del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="e6d13-136">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="e6d13-137">IMR_CANDIDATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="e6d13-137">IMR_CANDIDATEWINDOW</span></span>](imr-candidatewindow.md)
</dt> <dt>

[<span data-ttu-id="e6d13-138">IMR_COMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="e6d13-138">IMR_COMPOSITIONFONT</span></span>](imr-compositionfont.md)
</dt> <dt>

[<span data-ttu-id="e6d13-139">IMR_COMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="e6d13-139">IMR_COMPOSITIONWINDOW</span></span>](imr-compositionwindow.md)
</dt> <dt>

[<span data-ttu-id="e6d13-140">IMR_CONFIRMRECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="e6d13-140">IMR_CONFIRMRECONVERTSTRING</span></span>](imr-confirmreconvertstring.md)
</dt> <dt>

[<span data-ttu-id="e6d13-141">IMR_DOCUMENTFEED</span><span class="sxs-lookup"><span data-stu-id="e6d13-141">IMR_DOCUMENTFEED</span></span>](imr-documentfeed.md)
</dt> <dt>

[<span data-ttu-id="e6d13-142">IMR_QUERYCHARPOSITION</span><span class="sxs-lookup"><span data-stu-id="e6d13-142">IMR_QUERYCHARPOSITION</span></span>](imr-querycharposition.md)
</dt> <dt>

[<span data-ttu-id="e6d13-143">IMR_RECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="e6d13-143">IMR_RECONVERTSTRING</span></span>](imr-reconvertstring.md)
</dt> </dl>

 

 
