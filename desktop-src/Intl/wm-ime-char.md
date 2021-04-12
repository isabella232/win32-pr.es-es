---
description: Se envía a una aplicación cuando el IME obtiene un carácter del resultado de la conversión. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: Mensaje de WM_IME_CHAR (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0e2df06d9d837b0c1fbc0f9c9d9eb852252c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424044"
---
# <a name="wm_ime_char-message"></a><span data-ttu-id="cd086-104">\_Mensaje de carácter IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="cd086-104">WM\_IME\_CHAR message</span></span>

<span data-ttu-id="cd086-105">Se envía a una aplicación cuando el IME obtiene un carácter del resultado de la conversión.</span><span class="sxs-lookup"><span data-stu-id="cd086-105">Sent to an application when the IME gets a character of the conversion result.</span></span> <span data-ttu-id="cd086-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cd086-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,
 WM_IME_CHAR,
 WPARAM wParam,
 LPARAM lParam   
);
```



## <a name="parameters"></a><span data-ttu-id="cd086-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd086-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd086-108">*identificador*</span><span class="sxs-lookup"><span data-stu-id="cd086-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="cd086-109">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="cd086-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="cd086-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd086-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd086-111">**DBCS:** Un valor de carácter de un solo byte o de doble byte.</span><span class="sxs-lookup"><span data-stu-id="cd086-111">**DBCS:** A single-byte or double-byte character value.</span></span> <span data-ttu-id="cd086-112">Para un carácter de doble byte, (BYTE) (wParam >> 8) contiene el byte inicial.</span><span class="sxs-lookup"><span data-stu-id="cd086-112">For a double-byte character, (BYTE)(wParam >> 8) contains the lead byte.</span></span> <span data-ttu-id="cd086-113">Tenga en cuenta que los paréntesis son necesarios porque el operador de conversión tiene mayor precedencia que el operador de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="cd086-113">Note that the parentheses are necessary because the cast operator has higher precedence than the shift operator.</span></span>

<span data-ttu-id="cd086-114">**Unicode:** Valor de carácter Unicode.</span><span class="sxs-lookup"><span data-stu-id="cd086-114">**Unicode:** A Unicode character value.</span></span>

</dd> <dt>

<span data-ttu-id="cd086-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd086-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd086-116">El número de repeticiones, el código de recorrido, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, con valores como se define a continuación.</span><span class="sxs-lookup"><span data-stu-id="cd086-116">The repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, with values as defined below.</span></span>



| <span data-ttu-id="cd086-117">bit</span><span class="sxs-lookup"><span data-stu-id="cd086-117">Bit</span></span>   | <span data-ttu-id="cd086-118">Significado</span><span class="sxs-lookup"><span data-stu-id="cd086-118">Meaning</span></span>                                                                              |
|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cd086-119">0-15</span><span class="sxs-lookup"><span data-stu-id="cd086-119">0-15</span></span>  | <span data-ttu-id="cd086-120">Recuento de repeticiones.</span><span class="sxs-lookup"><span data-stu-id="cd086-120">Repeat count.</span></span> <span data-ttu-id="cd086-121">Dado que el primer byte y el segundo byte son continuos, siempre es 1.</span><span class="sxs-lookup"><span data-stu-id="cd086-121">Since the first byte and second byte are continuous, this is always 1.</span></span> |
| <span data-ttu-id="cd086-122">16-23</span><span class="sxs-lookup"><span data-stu-id="cd086-122">16-23</span></span> | <span data-ttu-id="cd086-123">Digitalice el código para un carácter asiático completo.</span><span class="sxs-lookup"><span data-stu-id="cd086-123">Scan code for a complete Asian character.</span></span>                                            |
| <span data-ttu-id="cd086-124">24</span><span class="sxs-lookup"><span data-stu-id="cd086-124">24</span></span>    | <span data-ttu-id="cd086-125">Clave extendida.</span><span class="sxs-lookup"><span data-stu-id="cd086-125">Extended key.</span></span>                                                                        |
| <span data-ttu-id="cd086-126">25-28</span><span class="sxs-lookup"><span data-stu-id="cd086-126">25-28</span></span> | <span data-ttu-id="cd086-127">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="cd086-127">Not used.</span></span>                                                                            |
| <span data-ttu-id="cd086-128">29</span><span class="sxs-lookup"><span data-stu-id="cd086-128">29</span></span>    | <span data-ttu-id="cd086-129">Código de contexto.</span><span class="sxs-lookup"><span data-stu-id="cd086-129">Context code.</span></span>                                                                        |
| <span data-ttu-id="cd086-130">30</span><span class="sxs-lookup"><span data-stu-id="cd086-130">30</span></span>    | <span data-ttu-id="cd086-131">Estado de clave anterior.</span><span class="sxs-lookup"><span data-stu-id="cd086-131">Previous key state.</span></span>                                                                  |
| <span data-ttu-id="cd086-132">31</span><span class="sxs-lookup"><span data-stu-id="cd086-132">31</span></span>    | <span data-ttu-id="cd086-133">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="cd086-133">Transition state.</span></span>                                                                    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd086-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd086-134">Remarks</span></span>

<span data-ttu-id="cd086-135">A diferencia del mensaje de tipo [**\_ Char de WM**](../inputdev/wm-char.md) para una ventana no Unicode, este mensaje puede incluir valores de caracteres de doble byte y de un solo byte.</span><span class="sxs-lookup"><span data-stu-id="cd086-135">Unlike the [**WM\_CHAR**](../inputdev/wm-char.md) message for a non-Unicode window, this message can include double-byte and single-byte character values.</span></span> <span data-ttu-id="cd086-136">En el caso de una ventana Unicode, este mensaje es el mismo que el de WM \_ Char.</span><span class="sxs-lookup"><span data-stu-id="cd086-136">For a Unicode window, this message is the same as WM\_CHAR.</span></span>

<span data-ttu-id="cd086-137">En el caso de una ventana no Unicode, si \_ el \_ mensaje de carácter IME IME incluye un carácter de doble byte y la aplicación pasa este mensaje a [**DEFWINDOWPROC**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), el IME convierte este mensaje en dos \_ mensajes de WM Char, cada uno con un byte del carácter de doble byte.</span><span class="sxs-lookup"><span data-stu-id="cd086-137">For a non-Unicode window, if the WM\_IME\_CHAR message includes a double-byte character and the application passes this message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the IME converts this message into two WM\_CHAR messages, each containing one byte of the double-byte character.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd086-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd086-138">Requirements</span></span>



| <span data-ttu-id="cd086-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd086-139">Requirement</span></span> | <span data-ttu-id="cd086-140">Value</span><span class="sxs-lookup"><span data-stu-id="cd086-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd086-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd086-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cd086-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cd086-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cd086-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd086-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cd086-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cd086-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cd086-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd086-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd086-146"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd086-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd086-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd086-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd086-148">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="cd086-148">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="cd086-149">Mensajes del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="cd086-149">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
