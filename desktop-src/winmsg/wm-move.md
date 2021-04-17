---
description: Se envía una vez que se ha despasado una ventana.
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: Mensaje de WM_MOVE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56004ec47266a50bf2ac82a828b9046c84a8ebfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677918"
---
# <a name="wm_move-message"></a><span data-ttu-id="5fc16-103">Mensaje de movimiento de WM \_</span><span class="sxs-lookup"><span data-stu-id="5fc16-103">WM\_MOVE message</span></span>

<span data-ttu-id="5fc16-104">Se envía una vez que se ha despasado una ventana.</span><span class="sxs-lookup"><span data-stu-id="5fc16-104">Sent after a window has been moved.</span></span>

<span data-ttu-id="5fc16-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="5fc16-105">A window receives this message through its [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```C++
#define WM_MOVE                         0x0003
```



## <a name="parameters"></a><span data-ttu-id="5fc16-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5fc16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fc16-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5fc16-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5fc16-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5fc16-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5fc16-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5fc16-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5fc16-110">Las coordenadas x e y de la esquina superior izquierda del área de cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="5fc16-110">The x and y coordinates of the upper-left corner of the client area of the window.</span></span> <span data-ttu-id="5fc16-111">La palabra de orden inferior contiene la coordenada x mientras que la palabra de orden superior contiene la coordenada y.</span><span class="sxs-lookup"><span data-stu-id="5fc16-111">The low-order word contains the x-coordinate while the high-order word contains the y coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fc16-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5fc16-112">Return value</span></span>

<span data-ttu-id="5fc16-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="5fc16-113">Type: **LRESULT**</span></span>

<span data-ttu-id="5fc16-114">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="5fc16-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fc16-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5fc16-115">Remarks</span></span>

<span data-ttu-id="5fc16-116">Los parámetros se proporcionan en coordenadas de pantalla para las ventanas superpuestas y ventanas emergentes, y en las coordenadas de cliente primario para las ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="5fc16-116">The parameters are given in screen coordinates for overlapped and pop-up windows and in parent-client coordinates for child windows.</span></span>

<span data-ttu-id="5fc16-117">En el ejemplo siguiente se muestra cómo obtener la posición del parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="5fc16-117">The following example demonstrates how to obtain the position from the *lParam* parameter.</span></span>


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



<span data-ttu-id="5fc16-118">También puede usar la macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) para convertir el parámetro *lParam* en una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5fc16-118">You can also use the [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro to convert the *lParam* parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure.</span></span>

<span data-ttu-id="5fc16-119">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía los mensajes de **\_ tamaño de WM** y **\_ movimiento de WM** cuando procesa el mensaje de [**\_ WINDOWPOSCHANGED de WM**](wm-windowposchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="5fc16-119">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the **WM\_SIZE** and **WM\_MOVE** messages when it processes the [**WM\_WINDOWPOSCHANGED**](wm-windowposchanged.md) message.</span></span>
<span data-ttu-id="5fc16-120">Los mensajes de **\_ tamaño de WM** y **\_ movimiento de WM** no se envían si una aplicación controla el mensaje de **\_ WINDOWPOSCHANGED de WM** sin llamar a **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="5fc16-120">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fc16-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fc16-121">Requirements</span></span>



| <span data-ttu-id="5fc16-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fc16-122">Requirement</span></span> | <span data-ttu-id="5fc16-123">Value</span><span class="sxs-lookup"><span data-stu-id="5fc16-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc16-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fc16-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5fc16-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5fc16-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5fc16-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fc16-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5fc16-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5fc16-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5fc16-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fc16-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fc16-129"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fc16-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fc16-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5fc16-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="5fc16-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="5fc16-131">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="5fc16-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5fc16-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="5fc16-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5fc16-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5fc16-134">**WINDOWPOSCHANGED de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5fc16-134">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="5fc16-135">**Vista**</span><span class="sxs-lookup"><span data-stu-id="5fc16-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5fc16-136">Windows</span><span class="sxs-lookup"><span data-stu-id="5fc16-136">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="5fc16-137">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="5fc16-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5fc16-138">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="5fc16-138">**MAKEPOINTS**</span></span>](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="5fc16-139">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5fc16-139">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

 
