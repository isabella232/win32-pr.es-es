---
description: Se envía a una aplicación mediante el IME para notificar a la aplicación de una pulsación de tecla y mantener el orden de los mensajes. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: db7075fb-b3d4-4d32-a0db-096d17d67c72
title: Mensaje de WM_IME_KEYDOWN (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3089af3c839f70e7f55895ae13158e7b2240605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275443"
---
# <a name="wm_ime_keydown-message"></a><span data-ttu-id="7631a-104">\_Mensaje de KEYDOWN IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="7631a-104">WM\_IME\_KEYDOWN message</span></span>

<span data-ttu-id="7631a-105">Se envía a una aplicación mediante el IME para notificar a la aplicación de una pulsación de tecla y mantener el orden de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="7631a-105">Sent to an application by the IME to notify the application of a key press and to keep message order.</span></span> <span data-ttu-id="7631a-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7631a-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,        
  WM_IME_KEYDOWN,  
  WPARAM wParam, 
  LPARAM lParam      
);
```



## <a name="parameters"></a><span data-ttu-id="7631a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7631a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7631a-108">*identificador*</span><span class="sxs-lookup"><span data-stu-id="7631a-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="7631a-109">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="7631a-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="7631a-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7631a-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7631a-111">Código de tecla virtual de la clave.</span><span class="sxs-lookup"><span data-stu-id="7631a-111">Virtual key code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="7631a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7631a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7631a-113">Recuento de repeticiones, código de recorrido, marca de clave extendida, código de contexto, marca de estado de clave anterior y marca de estado de transición, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7631a-113">Repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, as shown in the following table.</span></span>



| <span data-ttu-id="7631a-114">bit</span><span class="sxs-lookup"><span data-stu-id="7631a-114">Bit</span></span>   | <span data-ttu-id="7631a-115">Significado</span><span class="sxs-lookup"><span data-stu-id="7631a-115">Meaning</span></span>                                                                     |
|-------|-----------------------------------------------------------------------------|
| <span data-ttu-id="7631a-116">0-15</span><span class="sxs-lookup"><span data-stu-id="7631a-116">0-15</span></span>  | <span data-ttu-id="7631a-117">Recuento de repeticiones.</span><span class="sxs-lookup"><span data-stu-id="7631a-117">Repeat count.</span></span>                                                               |
| <span data-ttu-id="7631a-118">16-23</span><span class="sxs-lookup"><span data-stu-id="7631a-118">16-23</span></span> | <span data-ttu-id="7631a-119">Examinar código.</span><span class="sxs-lookup"><span data-stu-id="7631a-119">Scan code.</span></span>                                                                  |
| <span data-ttu-id="7631a-120">24</span><span class="sxs-lookup"><span data-stu-id="7631a-120">24</span></span>    | <span data-ttu-id="7631a-121">Clave extendida.</span><span class="sxs-lookup"><span data-stu-id="7631a-121">Extended key.</span></span> <span data-ttu-id="7631a-122">Este valor es 1 si es una clave extendida.</span><span class="sxs-lookup"><span data-stu-id="7631a-122">This value is 1 if it is an extended key.</span></span> <span data-ttu-id="7631a-123">De lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="7631a-123">Otherwise, it is 0.</span></span> |
| <span data-ttu-id="7631a-124">25-28</span><span class="sxs-lookup"><span data-stu-id="7631a-124">25-28</span></span> | <span data-ttu-id="7631a-125">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="7631a-125">Not used.</span></span>                                                                   |
| <span data-ttu-id="7631a-126">29</span><span class="sxs-lookup"><span data-stu-id="7631a-126">29</span></span>    | <span data-ttu-id="7631a-127">Código de contexto.</span><span class="sxs-lookup"><span data-stu-id="7631a-127">Context code.</span></span> <span data-ttu-id="7631a-128">Este valor siempre es 0.</span><span class="sxs-lookup"><span data-stu-id="7631a-128">This value is always 0.</span></span>                                       |
| <span data-ttu-id="7631a-129">30</span><span class="sxs-lookup"><span data-stu-id="7631a-129">30</span></span>    | <span data-ttu-id="7631a-130">Estado de clave anterior.</span><span class="sxs-lookup"><span data-stu-id="7631a-130">Previous key state.</span></span> <span data-ttu-id="7631a-131">Este valor es 1 si la tecla está presionada o 0 si está activa.</span><span class="sxs-lookup"><span data-stu-id="7631a-131">This value is 1 if the key is down or 0 if it is up.</span></span>    |
| <span data-ttu-id="7631a-132">31</span><span class="sxs-lookup"><span data-stu-id="7631a-132">31</span></span>    | <span data-ttu-id="7631a-133">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="7631a-133">Transition state.</span></span> <span data-ttu-id="7631a-134">Este valor siempre es 0.</span><span class="sxs-lookup"><span data-stu-id="7631a-134">This value is always 0.</span></span>                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7631a-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7631a-135">Return value</span></span>

<span data-ttu-id="7631a-136">Una aplicación debe devolver 0 si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="7631a-136">An application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="7631a-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7631a-137">Remarks</span></span>

<span data-ttu-id="7631a-138">Una aplicación puede procesar este mensaje o pasarlo a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  para generar un mensaje [**\_ KEYDOWN de WM**](../inputdev/wm-keydown.md) coincidente.</span><span class="sxs-lookup"><span data-stu-id="7631a-138">An application can process this message or pass it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function to generate a matching [**WM\_KEYDOWN**](../inputdev/wm-keydown.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7631a-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7631a-139">Requirements</span></span>



| <span data-ttu-id="7631a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="7631a-140">Requirement</span></span> | <span data-ttu-id="7631a-141">Value</span><span class="sxs-lookup"><span data-stu-id="7631a-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7631a-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7631a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7631a-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7631a-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7631a-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7631a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7631a-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7631a-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7631a-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7631a-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="7631a-147"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7631a-147"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7631a-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="7631a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7631a-149">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="7631a-149">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="7631a-150">Mensajes del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="7631a-150">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
