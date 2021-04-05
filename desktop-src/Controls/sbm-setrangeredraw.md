---
title: Mensaje de SBM_SETRANGEREDRAW (Winuser. h)
description: Una aplicación envía el \_ mensaje SBM SETRANGEREDRAW a un control de barra de desplazamiento para establecer los valores de posición mínimo y máximo y para volver a dibujar el control.
ms.assetid: badb58cc-9e3a-4766-a67f-631a7feb6285
keywords:
- SBM_SETRANGEREDRAW controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SBM_SETRANGEREDRAW
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37c77a8f062ba3c7a8b73adc4338a11cdcf59442
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078854"
---
# <a name="sbm_setrangeredraw-message"></a><span data-ttu-id="5f421-104">\_Mensaje SETRANGEREDRAW SBM</span><span class="sxs-lookup"><span data-stu-id="5f421-104">SBM\_SETRANGEREDRAW message</span></span>

<span data-ttu-id="5f421-105">Una aplicación envía el mensaje **SBM \_ SETRANGEREDRAW** a un control de barra de desplazamiento para establecer los valores de posición mínimo y máximo y para volver a dibujar el control.</span><span class="sxs-lookup"><span data-stu-id="5f421-105">An application sends the **SBM\_SETRANGEREDRAW** message to a scroll bar control to set the minimum and maximum position values and to redraw the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f421-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f421-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f421-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f421-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f421-108">Especifica la posición de desplazamiento mínima.</span><span class="sxs-lookup"><span data-stu-id="5f421-108">Specifies the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="5f421-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f421-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f421-110">Especifica la posición de desplazamiento máxima.</span><span class="sxs-lookup"><span data-stu-id="5f421-110">Specifies the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f421-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f421-111">Return value</span></span>

<span data-ttu-id="5f421-112">**ComCtl32.dll versión 5,0**: Si ha cambiado la posición del cuadro de desplazamiento, el valor devuelto es la posición anterior del cuadro de desplazamiento. de lo contrario, es cero.</span><span class="sxs-lookup"><span data-stu-id="5f421-112">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="5f421-113">**ComCtl32.dll versión 6,0**: la posición actual del cuadro de desplazamiento, independientemente de si ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="5f421-113">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f421-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f421-114">Remarks</span></span>

<span data-ttu-id="5f421-115">Los valores de posición mínimo y máximo predeterminados son cero.</span><span class="sxs-lookup"><span data-stu-id="5f421-115">The default minimum and maximum position values are zero.</span></span> <span data-ttu-id="5f421-116">La diferencia entre los valores especificados por los parámetros *wParam* e *lParam* no debe ser mayor que MAXLONG.</span><span class="sxs-lookup"><span data-stu-id="5f421-116">The difference between the values specified by the *wParam* and *lParam* parameters must not be greater than MAXLONG.</span></span>

<span data-ttu-id="5f421-117">Si los valores de posición mínimo y máximo son iguales, el control de barra de desplazamiento se oculta y, en efecto, se deshabilita.</span><span class="sxs-lookup"><span data-stu-id="5f421-117">If the minimum and maximum position values are equal, the scroll bar control is hidden and, in effect, disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f421-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f421-118">Requirements</span></span>



| <span data-ttu-id="5f421-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f421-119">Requirement</span></span> | <span data-ttu-id="5f421-120">Value</span><span class="sxs-lookup"><span data-stu-id="5f421-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f421-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f421-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5f421-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5f421-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5f421-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f421-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5f421-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f421-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5f421-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f421-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f421-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f421-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f421-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f421-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f421-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="5f421-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5f421-129">**SBM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="5f421-129">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="5f421-130">**SBM \_ GETRANGE**</span><span class="sxs-lookup"><span data-stu-id="5f421-130">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="5f421-131">**SBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="5f421-131">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="5f421-132">**SBM \_ SetRange**</span><span class="sxs-lookup"><span data-stu-id="5f421-132">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> </dl>

 

 





