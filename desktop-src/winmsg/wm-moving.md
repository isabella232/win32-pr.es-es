---
description: Se envía a una ventana que el usuario está moviendo. Al procesar este mensaje, una aplicación puede supervisar la posición del rectángulo de arrastre y, si es necesario, cambiar su posición.
ms.assetid: f56a36c1-dbaa-438a-9e52-d12697a9dac9
title: Mensaje de WM_MOVING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5847189d64601ec999321920ead716fbdf22e2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677361"
---
# <a name="wm_moving-message"></a><span data-ttu-id="9ad5f-104">Mensaje de movimiento de WM \_</span><span class="sxs-lookup"><span data-stu-id="9ad5f-104">WM\_MOVING message</span></span>

<span data-ttu-id="9ad5f-105">Se envía a una ventana que el usuario está moviendo.</span><span class="sxs-lookup"><span data-stu-id="9ad5f-105">Sent to a window that the user is moving.</span></span> <span data-ttu-id="9ad5f-106">Al procesar este mensaje, una aplicación puede supervisar la posición del rectángulo de arrastre y, si es necesario, cambiar su posición.</span><span class="sxs-lookup"><span data-stu-id="9ad5f-106">By processing this message, an application can monitor the position of the drag rectangle and, if needed, change its position.</span></span>

<span data-ttu-id="9ad5f-107">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9ad5f-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOVING                       0x0216
```



## <a name="parameters"></a><span data-ttu-id="9ad5f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ad5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ad5f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ad5f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ad5f-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9ad5f-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9ad5f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ad5f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ad5f-112">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) con la posición actual de la ventana, en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="9ad5f-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure with the current position of the window, in screen coordinates.</span></span> <span data-ttu-id="9ad5f-113">Para cambiar la posición del rectángulo de arrastre, una aplicación debe cambiar los miembros de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="9ad5f-113">To change the position of the drag rectangle, an application must change the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ad5f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ad5f-114">Return value</span></span>

<span data-ttu-id="9ad5f-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="9ad5f-115">Type: **LRESULT**</span></span>

<span data-ttu-id="9ad5f-116">Una aplicación debe devolver **true** si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="9ad5f-116">An application should return **TRUE** if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ad5f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ad5f-117">Requirements</span></span>



| <span data-ttu-id="9ad5f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ad5f-118">Requirement</span></span> | <span data-ttu-id="9ad5f-119">Value</span><span class="sxs-lookup"><span data-stu-id="9ad5f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad5f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ad5f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9ad5f-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9ad5f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9ad5f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ad5f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9ad5f-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9ad5f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9ad5f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ad5f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ad5f-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ad5f-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ad5f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ad5f-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="9ad5f-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="9ad5f-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9ad5f-128">**movimiento de WM \_**</span><span class="sxs-lookup"><span data-stu-id="9ad5f-128">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="9ad5f-129">**tamaño de WM \_**</span><span class="sxs-lookup"><span data-stu-id="9ad5f-129">**WM\_SIZING**</span></span>](wm-sizing.md)
</dt> <dt>

<span data-ttu-id="9ad5f-130">**Vista**</span><span class="sxs-lookup"><span data-stu-id="9ad5f-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9ad5f-131">Windows</span><span class="sxs-lookup"><span data-stu-id="9ad5f-131">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="9ad5f-132">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="9ad5f-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="9ad5f-133">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ad5f-133">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

 
