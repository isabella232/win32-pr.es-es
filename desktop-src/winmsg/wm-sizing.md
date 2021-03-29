---
description: Se envía a una ventana que el usuario está cambiando de tamaño. Al procesar este mensaje, una aplicación puede supervisar el tamaño y la posición del rectángulo de arrastre y, si es necesario, cambiar su tamaño o posición.
ms.assetid: 8cf56194-8a10-48e1-b0eb-aa3d66896599
title: Mensaje de WM_SIZING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ab865994352eba28cdebaff3faab72a484ce0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813867"
---
# <a name="wm_sizing-message"></a><span data-ttu-id="14c04-104">Mensaje de ajuste de tamaño de WM \_</span><span class="sxs-lookup"><span data-stu-id="14c04-104">WM\_SIZING message</span></span>

<span data-ttu-id="14c04-105">Se envía a una ventana que el usuario está cambiando de tamaño.</span><span class="sxs-lookup"><span data-stu-id="14c04-105">Sent to a window that the user is resizing.</span></span> <span data-ttu-id="14c04-106">Al procesar este mensaje, una aplicación puede supervisar el tamaño y la posición del rectángulo de arrastre y, si es necesario, cambiar su tamaño o posición.</span><span class="sxs-lookup"><span data-stu-id="14c04-106">By processing this message, an application can monitor the size and position of the drag rectangle and, if needed, change its size or position.</span></span>

<span data-ttu-id="14c04-107">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="14c04-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SIZING                       0x0214
```



## <a name="parameters"></a><span data-ttu-id="14c04-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14c04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c04-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14c04-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14c04-110">Borde de la ventana a la que se va a ajustar el tamaño.</span><span class="sxs-lookup"><span data-stu-id="14c04-110">The edge of the window that is being sized.</span></span> <span data-ttu-id="14c04-111">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="14c04-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="14c04-112">Valor</span><span class="sxs-lookup"><span data-stu-id="14c04-112">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="14c04-113">Significado</span><span class="sxs-lookup"><span data-stu-id="14c04-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WMSZ_BOTTOM"></span><span id="wmsz_bottom"></span><dl> <span data-ttu-id="14c04-114"><dt>**WMSZ \_ INFERIOR**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="14c04-114"><dt>**WMSZ\_BOTTOM**</dt> <dt>6</dt></span></span> </dl>                | <span data-ttu-id="14c04-115">Borde inferior</span><span class="sxs-lookup"><span data-stu-id="14c04-115">Bottom edge</span></span><br/>         |
| <span id="WMSZ_BOTTOMLEFT"></span><span id="wmsz_bottomleft"></span><dl> <span data-ttu-id="14c04-116"><dt>**WMSZ \_ BOTTOMLEFT**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="14c04-116"><dt>**WMSZ\_BOTTOMLEFT**</dt> <dt>7</dt></span></span> </dl>    | <span data-ttu-id="14c04-117">Esquina inferior izquierda</span><span class="sxs-lookup"><span data-stu-id="14c04-117">Bottom-left corner</span></span><br/>  |
| <span id="WMSZ_BOTTOMRIGHT"></span><span id="wmsz_bottomright"></span><dl> <span data-ttu-id="14c04-118"><dt>**WMSZ \_ BOTTOMRIGHT**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="14c04-118"><dt>**WMSZ\_BOTTOMRIGHT**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="14c04-119">Esquina inferior derecha</span><span class="sxs-lookup"><span data-stu-id="14c04-119">Bottom-right corner</span></span><br/> |
| <span id="WMSZ_LEFT"></span><span id="wmsz_left"></span><dl> <span data-ttu-id="14c04-120"><dt>**WMSZ \_ IZQUIERDA**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="14c04-120"><dt>**WMSZ\_LEFT**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="14c04-121">Borde izquierdo</span><span class="sxs-lookup"><span data-stu-id="14c04-121">Left edge</span></span><br/>           |
| <span id="WMSZ_RIGHT"></span><span id="wmsz_right"></span><dl> <span data-ttu-id="14c04-122"><dt>**WMSZ \_ DERECHA**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="14c04-122"><dt>**WMSZ\_RIGHT**</dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="14c04-123">Borde derecho</span><span class="sxs-lookup"><span data-stu-id="14c04-123">Right edge</span></span><br/>          |
| <span id="WMSZ_TOP"></span><span id="wmsz_top"></span><dl> <span data-ttu-id="14c04-124"><dt>**WMSZ \_**</dt>Los <dt>3</dt> principales</span><span class="sxs-lookup"><span data-stu-id="14c04-124"><dt>**WMSZ\_TOP**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="14c04-125">Borde superior</span><span class="sxs-lookup"><span data-stu-id="14c04-125">Top edge</span></span><br/>            |
| <span id="WMSZ_TOPLEFT"></span><span id="wmsz_topleft"></span><dl> <span data-ttu-id="14c04-126"><dt>**WMSZ \_ Lado izquierdo**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="14c04-126"><dt>**WMSZ\_TOPLEFT**</dt> <dt>4</dt></span></span> </dl>             | <span data-ttu-id="14c04-127">Esquina superior izquierda</span><span class="sxs-lookup"><span data-stu-id="14c04-127">Top-left corner</span></span><br/>     |
| <span id="WMSZ_TOPRIGHT"></span><span id="wmsz_topright"></span><dl> <span data-ttu-id="14c04-128"><dt>**WMSZ \_**</dt> <dt>5</dt> de la derecha</span><span class="sxs-lookup"><span data-stu-id="14c04-128"><dt>**WMSZ\_TOPRIGHT**</dt> <dt>5</dt></span></span> </dl>          | <span data-ttu-id="14c04-129">Esquina superior derecha</span><span class="sxs-lookup"><span data-stu-id="14c04-129">Top-right corner</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="14c04-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14c04-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14c04-131">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) con las coordenadas de pantalla del rectángulo de arrastre.</span><span class="sxs-lookup"><span data-stu-id="14c04-131">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure with the screen coordinates of the drag rectangle.</span></span> <span data-ttu-id="14c04-132">Para cambiar el tamaño o la posición del rectángulo de arrastre, una aplicación debe cambiar los miembros de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="14c04-132">To change the size or position of the drag rectangle, an application must change the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14c04-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14c04-133">Return value</span></span>

<span data-ttu-id="14c04-134">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="14c04-134">Type: **LRESULT**</span></span>

<span data-ttu-id="14c04-135">Una aplicación debe devolver **true** si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="14c04-135">An application should return **TRUE** if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="14c04-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14c04-136">Requirements</span></span>



| <span data-ttu-id="14c04-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="14c04-137">Requirement</span></span> | <span data-ttu-id="14c04-138">Value</span><span class="sxs-lookup"><span data-stu-id="14c04-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14c04-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14c04-139">Minimum supported client</span></span><br/> | <span data-ttu-id="14c04-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="14c04-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="14c04-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14c04-141">Minimum supported server</span></span><br/> | <span data-ttu-id="14c04-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14c04-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="14c04-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14c04-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="14c04-144"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14c04-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14c04-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="14c04-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="14c04-146">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="14c04-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="14c04-147">**movimiento de WM \_**</span><span class="sxs-lookup"><span data-stu-id="14c04-147">**WM\_MOVING**</span></span>](wm-moving.md)
</dt> <dt>

[<span data-ttu-id="14c04-148">**tamaño de WM \_**</span><span class="sxs-lookup"><span data-stu-id="14c04-148">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

<span data-ttu-id="14c04-149">**Vista**</span><span class="sxs-lookup"><span data-stu-id="14c04-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="14c04-150">Windows</span><span class="sxs-lookup"><span data-stu-id="14c04-150">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="14c04-151">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="14c04-151">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="14c04-152">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="14c04-152">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

 
