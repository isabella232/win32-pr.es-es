---
title: Mensaje de SBM_SETSCROLLINFO (Winuser. h)
description: El \_ mensaje SBM SETSCROLLINFO se envía para establecer los parámetros de una barra de desplazamiento.
ms.assetid: e0e42a81-67be-4d40-88c8-77398b068617
keywords:
- SBM_SETSCROLLINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SBM_SETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98abbca2d53d4b104caea22954472a17dfd5c1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658289"
---
# <a name="sbm_setscrollinfo-message"></a><span data-ttu-id="d9b84-104">\_Mensaje SETSCROLLINFO SBM</span><span class="sxs-lookup"><span data-stu-id="d9b84-104">SBM\_SETSCROLLINFO message</span></span>

<span data-ttu-id="d9b84-105">El mensaje **SBM \_ SETSCROLLINFO** se envía para establecer los parámetros de una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="d9b84-105">The **SBM\_SETSCROLLINFO** message is sent to set the parameters of a scroll bar.</span></span>

<span data-ttu-id="d9b84-106">Las aplicaciones no deben enviar este mensaje directamente.</span><span class="sxs-lookup"><span data-stu-id="d9b84-106">Applications should not send this message directly.</span></span> <span data-ttu-id="d9b84-107">En su lugar, deben utilizar la función [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="d9b84-107">Instead, they should use the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function.</span></span> <span data-ttu-id="d9b84-108">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d9b84-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="d9b84-109">Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **SetScrollInfo** funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="d9b84-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollInfo** function to function properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9b84-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9b84-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9b84-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9b84-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9b84-112">Especifica si la barra de desplazamiento se vuelve a dibujar para reflejar la nueva posición del cuadro de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="d9b84-112">Specifies whether the scroll bar is redrawn to reflect the new scroll box position.</span></span> <span data-ttu-id="d9b84-113">Si este parámetro es **true**, se vuelve a dibujar la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="d9b84-113">If this parameter is **TRUE**, the scroll bar is redrawn.</span></span> <span data-ttu-id="d9b84-114">Si es **false**, la barra de desplazamiento no se vuelve a dibujar.</span><span class="sxs-lookup"><span data-stu-id="d9b84-114">If it is **FALSE**, the scroll bar is not redrawn.</span></span>

</dd> <dt>

<span data-ttu-id="d9b84-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9b84-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9b84-116">Puntero a una estructura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="d9b84-116">Pointer to a [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="d9b84-117">Antes de llamar a [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), establezca el miembro **cbSize** de la estructura en **sizeof**(**SCROLLINFO**), establezca el miembro **fMask** para indicar los parámetros que se van a establecer y especifique los nuevos valores de parámetro en los miembros adecuados.</span><span class="sxs-lookup"><span data-stu-id="d9b84-117">Before calling [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), set the **cbSize** member of the structure to **sizeof**(**SCROLLINFO**), set the **fMask** member to indicate the parameters to set, and specify the new parameter values in the appropriate members.</span></span>

<span data-ttu-id="d9b84-118">El miembro **fMask** puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d9b84-118">The **fMask** member can be one or more of the following values.</span></span>



| <span data-ttu-id="d9b84-119">Value</span><span class="sxs-lookup"><span data-stu-id="d9b84-119">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="d9b84-120">Significado</span><span class="sxs-lookup"><span data-stu-id="d9b84-120">Meaning</span></span>                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIF_DISABLENOSCROLL"></span><span id="sif_disablenoscroll"></span><dl> <span data-ttu-id="d9b84-121"><dt>**SIF \_ DISABLENOSCROLL**</dt></span><span class="sxs-lookup"><span data-stu-id="d9b84-121"><dt>**SIF\_DISABLENOSCROLL**</dt></span></span> </dl> | <span data-ttu-id="d9b84-122">Deshabilita la barra de desplazamiento en lugar de quitarla, si los nuevos parámetros de la barra de desplazamiento hacen que la barra de desplazamiento sea innecesaria.</span><span class="sxs-lookup"><span data-stu-id="d9b84-122">Disables the scroll bar instead of removing it, if the scroll bar's new parameters make the scroll bar unnecessary.</span></span><br/> |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <span data-ttu-id="d9b84-123"><dt>**\_Página SIF**</dt></span><span class="sxs-lookup"><span data-stu-id="d9b84-123"><dt>**SIF\_PAGE**</dt></span></span> </dl>                                  | <span data-ttu-id="d9b84-124">Establece la página de desplazamiento en el valor especificado en el miembro **nPage** .</span><span class="sxs-lookup"><span data-stu-id="d9b84-124">Sets the scroll page to the value specified in the **nPage** member.</span></span><br/>                                                |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <span data-ttu-id="d9b84-125"><dt>**SIF \_ pos**</dt></span><span class="sxs-lookup"><span data-stu-id="d9b84-125"><dt>**SIF\_POS**</dt></span></span> </dl>                                     | <span data-ttu-id="d9b84-126">Establece la posición de desplazamiento en el valor especificado en el miembro **NPOs** .</span><span class="sxs-lookup"><span data-stu-id="d9b84-126">Sets the scroll position to the value specified in the **nPos** member.</span></span> <br/>                                            |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <span data-ttu-id="d9b84-127"><dt>**intervalo de SIF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d9b84-127"><dt>**SIF\_RANGE**</dt></span></span> </dl>                               | <span data-ttu-id="d9b84-128">Establece el intervalo de desplazamiento en el valor especificado en los miembros **nmín.** y **nmáx.** .</span><span class="sxs-lookup"><span data-stu-id="d9b84-128">Sets the scroll range to the value specified in the **nMin** and **nMax** members.</span></span> <br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9b84-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9b84-129">Return value</span></span>

<span data-ttu-id="d9b84-130">El valor devuelto es la posición actual del cuadro de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="d9b84-130">The return value is the current position of the scroll box.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9b84-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9b84-131">Remarks</span></span>

<span data-ttu-id="d9b84-132">Los mensajes que indican la posición de la barra de desplazamiento, [**WM \_ HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md), proporcionan únicamente 16 bits de datos de posición.</span><span class="sxs-lookup"><span data-stu-id="d9b84-132">The messages that indicate scroll bar position, [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md), provide only 16 bits of position data.</span></span> <span data-ttu-id="d9b84-133">Sin embargo, la estructura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) usada [**por \_ SBM GETSCROLLINFO**](sbm-getscrollinfo.md), **SBM \_ SETSCROLLINFO**, [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)y [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) proporciona 32 bits de datos de posición de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="d9b84-133">However, the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure used by [**SBM\_GETSCROLLINFO**](sbm-getscrollinfo.md), **SBM\_SETSCROLLINFO**, [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), and [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) provides 32 bits of scroll bar position data.</span></span> <span data-ttu-id="d9b84-134">Puede usar estos mensajes y funciones al procesar los mensajes de **WM \_ HSCROLL** o **WM \_ VSCROLL** para obtener datos de posición de la barra de desplazamiento de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d9b84-134">You can use these messages and functions while processing either the **WM\_HSCROLL** or **WM\_VSCROLL** messages to obtain 32-bit scroll bar position data.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9b84-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9b84-135">Requirements</span></span>



| <span data-ttu-id="d9b84-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9b84-136">Requirement</span></span> | <span data-ttu-id="d9b84-137">Value</span><span class="sxs-lookup"><span data-stu-id="d9b84-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b84-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9b84-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d9b84-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d9b84-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d9b84-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9b84-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d9b84-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9b84-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d9b84-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9b84-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9b84-143"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9b84-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9b84-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9b84-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="d9b84-145">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d9b84-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d9b84-146">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="d9b84-146">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="d9b84-147">**SBM \_ GETSCROLLINFO**</span><span class="sxs-lookup"><span data-stu-id="d9b84-147">**SBM\_GETSCROLLINFO**</span></span>](sbm-getscrollinfo.md)
</dt> <dt>

[<span data-ttu-id="d9b84-148">**SCROLLINFO**</span><span class="sxs-lookup"><span data-stu-id="d9b84-148">**SCROLLINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[<span data-ttu-id="d9b84-149">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="d9b84-149">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

