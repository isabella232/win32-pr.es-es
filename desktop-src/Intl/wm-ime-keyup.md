---
description: El IME lo envía a una aplicación para notificar a la aplicación de una versión de clave y mantener el orden de los mensajes. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 652f951f-4e9f-407c-844c-b250b6a9e6f5
title: Mensaje de WM_IME_KEYUP (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0eb6c6701510a373573ff6d85d5b50a8541b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686820"
---
# <a name="wm_ime_keyup-message"></a><span data-ttu-id="b474b-104">\_Mensaje KEYUP del IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="b474b-104">WM\_IME\_KEYUP message</span></span>

<span data-ttu-id="b474b-105">El IME lo envía a una aplicación para notificar a la aplicación de una versión de clave y mantener el orden de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="b474b-105">Sent to an application by the IME to notify the application of a key release and to keep message order.</span></span> <span data-ttu-id="b474b-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b474b-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_KEYUP,    
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="b474b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b474b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b474b-108">*identificador*</span><span class="sxs-lookup"><span data-stu-id="b474b-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b474b-109">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="b474b-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="b474b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b474b-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b474b-111">Código de tecla virtual de la clave.</span><span class="sxs-lookup"><span data-stu-id="b474b-111">Virtual key code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="b474b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b474b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b474b-113">Recuento de repeticiones, código de recorrido, marca de clave extendida, código de contexto, marca de estado de clave anterior y marca de estado de transición, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="b474b-113">Repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, as shown below.</span></span>



| <span data-ttu-id="b474b-114">bit</span><span class="sxs-lookup"><span data-stu-id="b474b-114">Bit</span></span>   | <span data-ttu-id="b474b-115">Significado</span><span class="sxs-lookup"><span data-stu-id="b474b-115">Meaning</span></span>                                                                     |
|-------|-----------------------------------------------------------------------------|
| <span data-ttu-id="b474b-116">0-15</span><span class="sxs-lookup"><span data-stu-id="b474b-116">0-15</span></span>  | <span data-ttu-id="b474b-117">Recuento de repeticiones.</span><span class="sxs-lookup"><span data-stu-id="b474b-117">Repeat count.</span></span> <span data-ttu-id="b474b-118">Este valor siempre es 1.</span><span class="sxs-lookup"><span data-stu-id="b474b-118">This value is always 1.</span></span>                                       |
| <span data-ttu-id="b474b-119">16-23</span><span class="sxs-lookup"><span data-stu-id="b474b-119">16-23</span></span> | <span data-ttu-id="b474b-120">Examinar código.</span><span class="sxs-lookup"><span data-stu-id="b474b-120">Scan code.</span></span>                                                                  |
| <span data-ttu-id="b474b-121">24</span><span class="sxs-lookup"><span data-stu-id="b474b-121">24</span></span>    | <span data-ttu-id="b474b-122">Clave extendida.</span><span class="sxs-lookup"><span data-stu-id="b474b-122">Extended key.</span></span> <span data-ttu-id="b474b-123">Este valor es 1 si es una clave extendida.</span><span class="sxs-lookup"><span data-stu-id="b474b-123">This value is 1 if it is an extended key.</span></span> <span data-ttu-id="b474b-124">De lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="b474b-124">Otherwise, it is 0.</span></span> |
| <span data-ttu-id="b474b-125">25-28</span><span class="sxs-lookup"><span data-stu-id="b474b-125">25-28</span></span> | <span data-ttu-id="b474b-126">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b474b-126">Not used.</span></span>                                                                   |
| <span data-ttu-id="b474b-127">29</span><span class="sxs-lookup"><span data-stu-id="b474b-127">29</span></span>    | <span data-ttu-id="b474b-128">Código de contexto.</span><span class="sxs-lookup"><span data-stu-id="b474b-128">Context code.</span></span> <span data-ttu-id="b474b-129">Este valor siempre es 0.</span><span class="sxs-lookup"><span data-stu-id="b474b-129">This value is always 0.</span></span>                                       |
| <span data-ttu-id="b474b-130">30</span><span class="sxs-lookup"><span data-stu-id="b474b-130">30</span></span>    | <span data-ttu-id="b474b-131">Estado de clave anterior.</span><span class="sxs-lookup"><span data-stu-id="b474b-131">Previous key state.</span></span> <span data-ttu-id="b474b-132">Este valor siempre es 1.</span><span class="sxs-lookup"><span data-stu-id="b474b-132">This value is always 1.</span></span>                                 |
| <span data-ttu-id="b474b-133">31</span><span class="sxs-lookup"><span data-stu-id="b474b-133">31</span></span>    | <span data-ttu-id="b474b-134">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="b474b-134">Transition state.</span></span> <span data-ttu-id="b474b-135">Este valor siempre es 1.</span><span class="sxs-lookup"><span data-stu-id="b474b-135">This value is always 1.</span></span>                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b474b-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b474b-136">Return value</span></span>

<span data-ttu-id="b474b-137">Una aplicación debe devolver 0 si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="b474b-137">An application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="b474b-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b474b-138">Remarks</span></span>

<span data-ttu-id="b474b-139">Una aplicación puede procesar este mensaje o pasarlo a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  para generar un mensaje [**de \_ KEYUP de WM**](../inputdev/wm-keyup.md) coincidente.</span><span class="sxs-lookup"><span data-stu-id="b474b-139">An application can process this message or pass it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function to generate a matching [**WM\_KEYUP**](../inputdev/wm-keyup.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b474b-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b474b-140">Requirements</span></span>



| <span data-ttu-id="b474b-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="b474b-141">Requirement</span></span> | <span data-ttu-id="b474b-142">Value</span><span class="sxs-lookup"><span data-stu-id="b474b-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b474b-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b474b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b474b-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b474b-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b474b-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b474b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b474b-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b474b-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b474b-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b474b-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="b474b-148"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b474b-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b474b-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="b474b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b474b-150">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="b474b-150">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="b474b-151">Mensajes del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="b474b-151">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
