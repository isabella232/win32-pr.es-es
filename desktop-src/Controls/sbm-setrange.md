---
title: Mensaje de SBM_SETRANGE (Winuser. h)
description: El \_ mensaje SBM SetRange se envía para establecer los valores de posición mínimo y máximo del control de barra de desplazamiento.
ms.assetid: 9cf84354-3944-4c10-9b59-39427b840868
keywords:
- SBM_SETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SBM_SETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7a720531ae58fdb0712b8f23fd1aef88b3e4caa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905554"
---
# <a name="sbm_setrange-message"></a><span data-ttu-id="96190-104">\_Mensaje SBM SetRange</span><span class="sxs-lookup"><span data-stu-id="96190-104">SBM\_SETRANGE message</span></span>

<span data-ttu-id="96190-105">El mensaje **SBM \_ SetRange** se envía para establecer los valores de posición mínimo y máximo del control de barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="96190-105">The **SBM\_SETRANGE** message is sent to set the minimum and maximum position values for the scroll bar control.</span></span>

<span data-ttu-id="96190-106">Las aplicaciones no deben enviar este mensaje directamente.</span><span class="sxs-lookup"><span data-stu-id="96190-106">Applications should not send this message directly.</span></span> <span data-ttu-id="96190-107">En su lugar, deben utilizar la función [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) .</span><span class="sxs-lookup"><span data-stu-id="96190-107">Instead, they should use the [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) function.</span></span> <span data-ttu-id="96190-108">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="96190-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="96190-109">Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **SetScrollRange** funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="96190-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollRange** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="96190-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96190-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96190-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96190-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96190-112">Especifica la posición de desplazamiento mínima.</span><span class="sxs-lookup"><span data-stu-id="96190-112">Specifies the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="96190-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96190-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96190-114">Especifica la posición de desplazamiento máxima.</span><span class="sxs-lookup"><span data-stu-id="96190-114">Specifies the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96190-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96190-115">Return value</span></span>

<span data-ttu-id="96190-116">**ComCtl32.dll versión 5,0**: Si ha cambiado la posición del cuadro de desplazamiento, el valor devuelto es la posición anterior del cuadro de desplazamiento. de lo contrario, es cero.</span><span class="sxs-lookup"><span data-stu-id="96190-116">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="96190-117">**ComCtl32.dll versión 6,0**: la posición actual del cuadro de desplazamiento, independientemente de si ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="96190-117">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="96190-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96190-118">Remarks</span></span>

<span data-ttu-id="96190-119">Los valores de posición mínimo y máximo predeterminados son cero.</span><span class="sxs-lookup"><span data-stu-id="96190-119">The default minimum and maximum position values are zero.</span></span> <span data-ttu-id="96190-120">La diferencia entre los valores especificados por los parámetros *wParam* e *lParam* no debe ser mayor que MAXLONG.</span><span class="sxs-lookup"><span data-stu-id="96190-120">The difference between the values specified by the *wParam* and *lParam* parameters must not be greater than MAXLONG.</span></span>

<span data-ttu-id="96190-121">Si los valores de posición mínimo y máximo son iguales, el control de barra de desplazamiento se oculta y, en efecto, se deshabilita.</span><span class="sxs-lookup"><span data-stu-id="96190-121">If the minimum and maximum position values are equal, the scroll bar control is hidden and, in effect, disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="96190-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96190-122">Requirements</span></span>



| <span data-ttu-id="96190-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="96190-123">Requirement</span></span> | <span data-ttu-id="96190-124">Value</span><span class="sxs-lookup"><span data-stu-id="96190-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96190-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96190-125">Minimum supported client</span></span><br/> | <span data-ttu-id="96190-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="96190-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="96190-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96190-127">Minimum supported server</span></span><br/> | <span data-ttu-id="96190-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="96190-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="96190-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96190-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="96190-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96190-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96190-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="96190-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="96190-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="96190-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="96190-133">**SBM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="96190-133">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="96190-134">**SBM \_ GETRANGE**</span><span class="sxs-lookup"><span data-stu-id="96190-134">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="96190-135">**SBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="96190-135">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="96190-136">**SBM \_ SETRANGEREDRAW**</span><span class="sxs-lookup"><span data-stu-id="96190-136">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

