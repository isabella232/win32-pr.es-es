---
title: Mensaje de UDM_GETPOS (commctrl. h)
description: Recupera la posición actual de un control de flechas con una precisión de 16 bits.
ms.assetid: 5f395de0-11b3-44f8-9bf4-42e27ce88a0c
keywords:
- UDM_GETPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- UDM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e78ad19289d85b93ebcb39a244a896ddb4f33f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656483"
---
# <a name="udm_getpos-message"></a><span data-ttu-id="17578-104">\_Mensaje GETPOS UDM</span><span class="sxs-lookup"><span data-stu-id="17578-104">UDM\_GETPOS message</span></span>

<span data-ttu-id="17578-105">Recupera la posición actual de un control de flechas con una precisión de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="17578-105">Retrieves the current position of an up-down control with 16-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="17578-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17578-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17578-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="17578-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="17578-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="17578-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="17578-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17578-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="17578-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="17578-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17578-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17578-111">Return value</span></span>

<span data-ttu-id="17578-112">Si es correcto, [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) se establece en cero y [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) se establece en la posición actual del control.</span><span class="sxs-lookup"><span data-stu-id="17578-112">If successful, the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is set to zero and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is set to the control's current position.</span></span> <span data-ttu-id="17578-113">Si se produce un error, **HIWORD** se establece en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="17578-113">If an error occurs, the **HIWORD** is set to a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17578-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17578-114">Remarks</span></span>

<span data-ttu-id="17578-115">Al procesar este mensaje, el control de flechas actualiza su posición actual en función del título de la ventana relacionada.</span><span class="sxs-lookup"><span data-stu-id="17578-115">When processing this message, the up-down control updates its current position based on the caption of the buddy window.</span></span> <span data-ttu-id="17578-116">El control de flechas devuelve un error si no hay ninguna ventana relacionada o si el título especifica un valor que no es válido o está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="17578-116">The up-down control returns an error if there is no buddy window or if the caption specifies an invalid or out-of-range value.</span></span> <span data-ttu-id="17578-117">Además, se establece una marca de error en el HIWORD de devolución si el control se crea sin el estilo [**uds \_ SETBUDDYINT**](up-down-control-styles.md) , aunque devuelva un valor de posición válido en el LOWORD de la devolución.</span><span class="sxs-lookup"><span data-stu-id="17578-117">Also, an error flag is set in the HIWORD of the return if the control is created without the [**UDS\_SETBUDDYINT**](up-down-control-styles.md) style, even though it returns a valid position value in the LOWORD of the return.</span></span>

<span data-ttu-id="17578-118">Si se han habilitado valores de 32 bits para un control de flechas con [**UDM \_ SETRANGE32**](udm-setrange32.md), este mensaje devuelve solo los 16 bits inferiores de la posición.</span><span class="sxs-lookup"><span data-stu-id="17578-118">If 32-bit values have been enabled for an up-down control with [**UDM\_SETRANGE32**](udm-setrange32.md), this message returns only the lower 16 bits of the position.</span></span> <span data-ttu-id="17578-119">Para recuperar la posición completa de 32 bits, use [**UDM \_ GETPOS32**](udm-getpos32.md).</span><span class="sxs-lookup"><span data-stu-id="17578-119">To retrieve the full 32-bit position, use [**UDM\_GETPOS32**](udm-getpos32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17578-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17578-120">Requirements</span></span>



| <span data-ttu-id="17578-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="17578-121">Requirement</span></span> | <span data-ttu-id="17578-122">Value</span><span class="sxs-lookup"><span data-stu-id="17578-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17578-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17578-123">Minimum supported client</span></span><br/> | <span data-ttu-id="17578-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="17578-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17578-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17578-125">Minimum supported server</span></span><br/> | <span data-ttu-id="17578-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="17578-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="17578-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17578-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="17578-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="17578-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17578-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="17578-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="17578-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="17578-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="17578-131">**UDM \_ GETRANGE**</span><span class="sxs-lookup"><span data-stu-id="17578-131">**UDM\_GETRANGE**</span></span>](udm-getrange.md)
</dt> <dt>

[<span data-ttu-id="17578-132">**UDM \_ GETRANGE32**</span><span class="sxs-lookup"><span data-stu-id="17578-132">**UDM\_GETRANGE32**</span></span>](udm-getrange32.md)
</dt> <dt>

[<span data-ttu-id="17578-133">**UDM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="17578-133">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="17578-134">**UDM \_ SETRANGE32**</span><span class="sxs-lookup"><span data-stu-id="17578-134">**UDM\_SETRANGE32**</span></span>](udm-setrange32.md)
</dt> </dl>

 

