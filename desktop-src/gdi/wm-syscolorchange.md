---
description: El mensaje de SYSCOLORCHANGE de WM \_ se envía a todas las ventanas de nivel superior cuando se realiza un cambio en la configuración de color del sistema.
ms.assetid: ffe61768-86d6-4ea8-ae2d-1095a9afa925
title: Mensaje de WM_SYSCOLORCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3883f0534d91a6d852b0e70fbb4edabdcab56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986055"
---
# <a name="wm_syscolorchange-message"></a><span data-ttu-id="415c7-103">Mensaje de SYSCOLORCHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="415c7-103">WM\_SYSCOLORCHANGE message</span></span>

<span data-ttu-id="415c7-104">El mensaje de **\_ SYSCOLORCHANGE de WM** se envía a todas las ventanas de nivel superior cuando se realiza un cambio en la configuración de color del sistema.</span><span class="sxs-lookup"><span data-stu-id="415c7-104">The **WM\_SYSCOLORCHANGE** message is sent to all top-level windows when a change is made to a system color setting.</span></span>

<span data-ttu-id="415c7-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="415c7-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="415c7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="415c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="415c7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="415c7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="415c7-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="415c7-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="415c7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="415c7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="415c7-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="415c7-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="415c7-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="415c7-111">Remarks</span></span>

<span data-ttu-id="415c7-112">El sistema envía un mensaje de [**\_ dibujo de WM**](wm-paint.md) a cualquier ventana afectada por un cambio de color del sistema.</span><span class="sxs-lookup"><span data-stu-id="415c7-112">The system sends a [**WM\_PAINT**](wm-paint.md) message to any window that is affected by a system color change.</span></span>

<span data-ttu-id="415c7-113">Las aplicaciones que tienen pinceles que usan los colores del sistema existentes deben eliminar esos pinceles y volver a crearlos con los nuevos colores del sistema.</span><span class="sxs-lookup"><span data-stu-id="415c7-113">Applications that have brushes using the existing system colors should delete those brushes and re-create them using the new system colors.</span></span>

<span data-ttu-id="415c7-114">Las ventanas de nivel superior que usan controles comunes deben reenviar el mensaje de **\_ SYSCOLORCHANGE de WM** a los controles; de lo contrario, los controles no recibirán una notificación del cambio de color.</span><span class="sxs-lookup"><span data-stu-id="415c7-114">Top level windows that use common controls must forward the **WM\_SYSCOLORCHANGE** message to the controls; otherwise, the controls will not be notified of the color change.</span></span> <span data-ttu-id="415c7-115">Esto garantiza que los colores utilizados por los controles comunes son coherentes con los utilizados por otros objetos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="415c7-115">This ensures that the colors used by your common controls are consistent with those used by other user interface objects.</span></span> <span data-ttu-id="415c7-116">Por ejemplo, un control de barra de herramientas usa el color "objetos 3D" para dibujar sus botones.</span><span class="sxs-lookup"><span data-stu-id="415c7-116">For example, a toolbar control uses the "3D Objects" color to draw its buttons.</span></span> <span data-ttu-id="415c7-117">Si el usuario cambia el color de los objetos 3D, pero el mensaje de **\_ SYSCOLORCHANGE de WM** no se reenvía a la barra de herramientas, los botones de la barra de herramientas permanecen en su color original mientras que el color de otros botones del sistema cambia.</span><span class="sxs-lookup"><span data-stu-id="415c7-117">If the user changes the 3D Objects color but the **WM\_SYSCOLORCHANGE** message is not forwarded to the toolbar, the toolbar buttons will remain in their original color while the color of other buttons in the system changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="415c7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="415c7-118">Requirements</span></span>



| <span data-ttu-id="415c7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="415c7-119">Requirement</span></span> | <span data-ttu-id="415c7-120">Value</span><span class="sxs-lookup"><span data-stu-id="415c7-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="415c7-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="415c7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="415c7-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="415c7-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="415c7-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="415c7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="415c7-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="415c7-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="415c7-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="415c7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="415c7-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="415c7-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="415c7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="415c7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="415c7-128">Información general sobre colores</span><span class="sxs-lookup"><span data-stu-id="415c7-128">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="415c7-129">Mensajes de color</span><span class="sxs-lookup"><span data-stu-id="415c7-129">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="415c7-130">**pintura de WM \_**</span><span class="sxs-lookup"><span data-stu-id="415c7-130">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
