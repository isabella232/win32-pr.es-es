---
title: Mensaje de SBM_GETSCROLLINFO (Winuser. h)
description: El \_ mensaje SBM GETSCROLLINFO se envía para recuperar los parámetros de una barra de desplazamiento.
ms.assetid: 3b43430f-b55f-43ec-8558-baf5c953064f
keywords:
- SBM_GETSCROLLINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SBM_GETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4cb05b05ba2686d755c5fa34adcff0016433346
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658387"
---
# <a name="sbm_getscrollinfo-message"></a><span data-ttu-id="9a2d1-104">\_Mensaje GETSCROLLINFO SBM</span><span class="sxs-lookup"><span data-stu-id="9a2d1-104">SBM\_GETSCROLLINFO message</span></span>

<span data-ttu-id="9a2d1-105">El mensaje **SBM \_ GETSCROLLINFO** se envía para recuperar los parámetros de una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-105">The **SBM\_GETSCROLLINFO** message is sent to retrieve the parameters of a scroll bar.</span></span>

<span data-ttu-id="9a2d1-106">Las aplicaciones no deben enviar este mensaje directamente.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-106">Applications should not send this message directly.</span></span> <span data-ttu-id="9a2d1-107">En su lugar, deben utilizar la función [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="9a2d1-107">Instead, they should use the [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) function.</span></span> <span data-ttu-id="9a2d1-108">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9a2d1-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="9a2d1-109">Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **GetScrollInfo** funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-109">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollInfo** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a2d1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a2d1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a2d1-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a2d1-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a2d1-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9a2d1-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a2d1-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a2d1-114">Puntero a una estructura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="9a2d1-114">Pointer to a [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="9a2d1-115">Antes de llamar a [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), establezca el miembro **cbSize** de la estructura en **sizeof**(**SCROLLINFO**) y establezca el miembro **fMask** para especificar los parámetros de la barra de desplazamiento que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-115">Before calling [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), set the **cbSize** member of the structure to **sizeof**(**SCROLLINFO**), and set the **fMask** member to specify the scroll bar parameters to retrieve.</span></span> <span data-ttu-id="9a2d1-116">Antes de devolver, el mensaje copia los parámetros especificados en los miembros adecuados de la estructura.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-116">Before returning, the message copies the specified parameters to the appropriate members of the structure.</span></span>

<span data-ttu-id="9a2d1-117">El miembro **fMask** puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-117">The **fMask** member can be one or more of the following values.</span></span>



| <span data-ttu-id="9a2d1-118">Value</span><span class="sxs-lookup"><span data-stu-id="9a2d1-118">Value</span></span>                                                                                                                                                      | <span data-ttu-id="9a2d1-119">Significado</span><span class="sxs-lookup"><span data-stu-id="9a2d1-119">Meaning</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="SIF_ALL"></span><span id="sif_all"></span><dl> <span data-ttu-id="9a2d1-120"><dt>**SIF \_ All**</dt></span><span class="sxs-lookup"><span data-stu-id="9a2d1-120"><dt>**SIF\_ALL**</dt></span></span> </dl>                | <span data-ttu-id="9a2d1-121">Combinación de la \_ Página SIF, SIF \_ pos, SIF \_ Range y SIF \_ TRACKPOS.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-121">Combination of SIF\_PAGE, SIF\_POS, SIF\_RANGE, and SIF\_TRACKPOS.</span></span><br/>       |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <span data-ttu-id="9a2d1-122"><dt>**\_Página SIF**</dt></span><span class="sxs-lookup"><span data-stu-id="9a2d1-122"><dt>**SIF\_PAGE**</dt></span></span> </dl>             | <span data-ttu-id="9a2d1-123">Copia la página de desplazamiento en el miembro nPage.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-123">Copies the scroll page to the nPage member.</span></span><br/>                              |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <span data-ttu-id="9a2d1-124"><dt>**SIF \_ pos**</dt></span><span class="sxs-lookup"><span data-stu-id="9a2d1-124"><dt>**SIF\_POS**</dt></span></span> </dl>                | <span data-ttu-id="9a2d1-125">Copia la posición de desplazamiento en el miembro nPos.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-125">Copies the scroll position to the nPos member.</span></span> <br/>                          |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <span data-ttu-id="9a2d1-126"><dt>**intervalo de SIF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9a2d1-126"><dt>**SIF\_RANGE**</dt></span></span> </dl>          | <span data-ttu-id="9a2d1-127">Copia el intervalo de desplazamiento en los miembros Nmín. y Nmáx..</span><span class="sxs-lookup"><span data-stu-id="9a2d1-127">Copies the scroll range to the nMin and nMax members.</span></span> <br/>                   |
| <span id="SIF_TRACKPOS"></span><span id="sif_trackpos"></span><dl> <span data-ttu-id="9a2d1-128"><dt>**SIF \_ TRACKPOS**</dt></span><span class="sxs-lookup"><span data-stu-id="9a2d1-128"><dt>**SIF\_TRACKPOS**</dt></span></span> </dl> | <span data-ttu-id="9a2d1-129">Copia la posición de seguimiento del cuadro de desplazamiento actual en el miembro nTrackPos.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-129">Copies the current scroll box tracking position to the nTrackPos member.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a2d1-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a2d1-130">Return value</span></span>

<span data-ttu-id="9a2d1-131">Si el mensaje recupera algún valor, el valor devuelto es **true**; de lo contrario, es **false**.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-131">If the message retrieved any values, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a2d1-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a2d1-132">Remarks</span></span>

<span data-ttu-id="9a2d1-133">Los mensajes que indican la posición de la barra de desplazamiento, [**WM \_ HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md), proporcionan únicamente 16 bits de datos de posición.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-133">The messages that indicate scroll bar position, [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md), provide only 16 bits of position data.</span></span> <span data-ttu-id="9a2d1-134">Sin embargo, la estructura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) usada **por \_ SBM GETSCROLLINFO**, [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md), [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)y [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) proporciona 32 bits de datos de posición de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-134">However, the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure used by **SBM\_GETSCROLLINFO**, [**SBM\_SETSCROLLINFO**](sbm-setscrollinfo.md), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), and [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) provides 32 bits of scroll bar position data.</span></span> <span data-ttu-id="9a2d1-135">Puede usar estos mensajes y funciones al procesar los mensajes de **WM \_ HSCROLL** o **WM \_ VSCROLL** para obtener datos de posición de la barra de desplazamiento de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-135">You can use these messages and functions while processing either the **WM\_HSCROLL** or **WM\_VSCROLL** messages to obtain 32-bit scroll bar position data.</span></span>

<span data-ttu-id="9a2d1-136">Para obtener la posición de 32 bits del cuadro de desplazamiento (Thumb) durante un \_ código de solicitud THUMBTRACK de SB en un mensaje de [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) , envíe **SBM \_ GETSCROLLINFO** con el \_ valor SIF TRACKPOS en el miembro **fMask** de la estructura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="9a2d1-136">To get the 32-bit position of the scroll box (thumb) during a SB\_THUMBTRACK request code in a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message, send **SBM\_GETSCROLLINFO** with the SIF\_TRACKPOS value in the **fMask** member of the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="9a2d1-137">El mensaje devuelve la posición de seguimiento del cuadro de desplazamiento en el miembro **nTrackPos** de la estructura **SCROLLINFO** .</span><span class="sxs-lookup"><span data-stu-id="9a2d1-137">The message returns the tracking position of the scroll box in the **nTrackPos** member of the **SCROLLINFO** structure.</span></span> <span data-ttu-id="9a2d1-138">Esto le permite obtener la posición del cuadro de desplazamiento cuando el usuario lo mueve.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-138">This allows you to get the position of the scroll box as the user moves it.</span></span> <span data-ttu-id="9a2d1-139">Como alternativa, puede usar la función [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) para obtener la misma información.</span><span class="sxs-lookup"><span data-stu-id="9a2d1-139">Alternatively, you can use the [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) function to get the same information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a2d1-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a2d1-140">Requirements</span></span>



| <span data-ttu-id="9a2d1-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a2d1-141">Requirement</span></span> | <span data-ttu-id="9a2d1-142">Value</span><span class="sxs-lookup"><span data-stu-id="9a2d1-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a2d1-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a2d1-143">Minimum supported client</span></span><br/> | <span data-ttu-id="9a2d1-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9a2d1-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9a2d1-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a2d1-145">Minimum supported server</span></span><br/> | <span data-ttu-id="9a2d1-146">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a2d1-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9a2d1-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a2d1-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a2d1-148"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a2d1-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a2d1-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a2d1-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="9a2d1-150">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="9a2d1-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9a2d1-151">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="9a2d1-151">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="9a2d1-152">**SBM \_ SETSCROLLINFO**</span><span class="sxs-lookup"><span data-stu-id="9a2d1-152">**SBM\_SETSCROLLINFO**</span></span>](sbm-setscrollinfo.md)
</dt> <dt>

[<span data-ttu-id="9a2d1-153">**SCROLLINFO**</span><span class="sxs-lookup"><span data-stu-id="9a2d1-153">**SCROLLINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[<span data-ttu-id="9a2d1-154">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="9a2d1-154">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

