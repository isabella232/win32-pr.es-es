---
title: Mensaje de SBM_SETPOS (Winuser. h)
description: El \_ mensaje SBM SETPOS se envía para establecer la posición del cuadro de desplazamiento (Thumb) y, si se solicita, vuelve a dibujar la barra de desplazamiento para reflejar la nueva posición del cuadro de desplazamiento.
ms.assetid: 6b3c16ba-1cdf-41ff-8546-ba98477af334
keywords:
- SBM_SETPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SBM_SETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a7dc99da5f4b3dbb301f15ddd722f1d664932f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493048"
---
# <a name="sbm_setpos-message"></a><span data-ttu-id="b431a-104">\_Mensaje SETPOS SBM</span><span class="sxs-lookup"><span data-stu-id="b431a-104">SBM\_SETPOS message</span></span>

<span data-ttu-id="b431a-105">El mensaje **SBM \_ SETPOS** se envía para establecer la posición del cuadro de desplazamiento (Thumb) y, si se solicita, vuelve a dibujar la barra de desplazamiento para reflejar la nueva posición del cuadro de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="b431a-105">The **SBM\_SETPOS** message is sent to set the position of the scroll box (thumb) and, if requested, redraw the scroll bar to reflect the new position of the scroll box.</span></span>

<span data-ttu-id="b431a-106">Las aplicaciones no deben enviar este mensaje directamente.</span><span class="sxs-lookup"><span data-stu-id="b431a-106">Applications should not send this message directly.</span></span> <span data-ttu-id="b431a-107">En su lugar, deben utilizar la función [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="b431a-107">Instead, they should use the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span> <span data-ttu-id="b431a-108">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b431a-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="b431a-109">Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **SetScrollPos** funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="b431a-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollPos** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="b431a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b431a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b431a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b431a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b431a-112">Especifica la nueva posición del cuadro de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="b431a-112">Specifies the new position of the scroll box.</span></span> <span data-ttu-id="b431a-113">Debe encontrarse dentro del intervalo de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="b431a-113">It must be within the scrolling range.</span></span> <span data-ttu-id="b431a-114">Si este parámetro está fuera del intervalo de desplazamiento, el valor se redondea hacia arriba o hacia abajo al valor válido más próximo.</span><span class="sxs-lookup"><span data-stu-id="b431a-114">If this parameter is outside of the scrolling range, the value is rounded up or down to the nearest valid value.</span></span>

</dd> <dt>

<span data-ttu-id="b431a-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b431a-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b431a-116">Especifica si la barra de desplazamiento debe volver a dibujarse para reflejar la nueva posición del cuadro de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="b431a-116">Specifies whether the scroll bar should be redrawn to reflect the new scroll box position.</span></span> <span data-ttu-id="b431a-117">Si este parámetro es **true**, se vuelve a dibujar la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="b431a-117">If this parameter is **TRUE**, the scroll bar is redrawn.</span></span> <span data-ttu-id="b431a-118">Si es **false**, la barra de desplazamiento no se vuelve a dibujar.</span><span class="sxs-lookup"><span data-stu-id="b431a-118">If it is **FALSE**, the scroll bar is not redrawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b431a-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b431a-119">Return value</span></span>

<span data-ttu-id="b431a-120">**ComCtl32.dll versión 5,0**: Si ha cambiado la posición del cuadro de desplazamiento, el valor devuelto es la posición anterior del cuadro de desplazamiento. de lo contrario, es cero.</span><span class="sxs-lookup"><span data-stu-id="b431a-120">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="b431a-121">**ComCtl32.dll versión 6,0**: la posición actual del cuadro de desplazamiento, independientemente de si ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="b431a-121">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="b431a-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b431a-122">Remarks</span></span>

<span data-ttu-id="b431a-123">Si el control de barra de desplazamiento se vuelve a dibujar mediante una llamada subsiguiente a otra función, resulta útil establecer el parámetro *lParam* en **false** .</span><span class="sxs-lookup"><span data-stu-id="b431a-123">If the scroll bar control is redrawn by a subsequent call to another function, setting the *lParam* parameter to **FALSE** is useful.</span></span>

## <a name="requirements"></a><span data-ttu-id="b431a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b431a-124">Requirements</span></span>



| <span data-ttu-id="b431a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b431a-125">Requirement</span></span> | <span data-ttu-id="b431a-126">Value</span><span class="sxs-lookup"><span data-stu-id="b431a-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b431a-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b431a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b431a-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b431a-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b431a-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b431a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b431a-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b431a-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b431a-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b431a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b431a-132"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b431a-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b431a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="b431a-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="b431a-134">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b431a-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b431a-135">**SBM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="b431a-135">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="b431a-136">**SBM \_ GETRANGE**</span><span class="sxs-lookup"><span data-stu-id="b431a-136">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="b431a-137">**SBM \_ SetRange**</span><span class="sxs-lookup"><span data-stu-id="b431a-137">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="b431a-138">**SBM \_ SETRANGEREDRAW**</span><span class="sxs-lookup"><span data-stu-id="b431a-138">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

