---
title: Mensaje de HDM_GETITEMDROPDOWNRECT (commctrl. h)
description: Obtiene el rectángulo delimitador del botón de expansión de un elemento de encabezado con el estilo HDF \_ SPLITBUTTON. Envíe este mensaje explícitamente o mediante la \_ macro header GetItemDropDownRect.
ms.assetid: d7188dfb-4ffa-4641-b210-2c2ec480ca13
keywords:
- HDM_GETITEMDROPDOWNRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86f3df8de5224e79ca4e15ea18409e13972ca5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079404"
---
# <a name="hdm_getitemdropdownrect-message"></a><span data-ttu-id="e34cf-105">HDM \_ GETITEMDROPDOWNRECT</span><span class="sxs-lookup"><span data-stu-id="e34cf-105">HDM\_GETITEMDROPDOWNRECT message</span></span>

<span data-ttu-id="e34cf-106">Obtiene el rectángulo delimitador del botón de expansión de un elemento de encabezado con el estilo **HDF \_ SPLITBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="e34cf-106">Gets the bounding rectangle of the split button for a header item with style **HDF\_SPLITBUTTON**.</span></span> <span data-ttu-id="e34cf-107">Envíe este mensaje explícitamente o mediante la macro [**Header \_ GetItemDropDownRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) .</span><span class="sxs-lookup"><span data-stu-id="e34cf-107">Send this message explicitly or by using the [**Header\_GetItemDropDownRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e34cf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e34cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e34cf-109">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e34cf-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e34cf-110">Índice de base cero del elemento de control de encabezado para el que se va a recuperar el rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="e34cf-110">The zero-based index of the header control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="e34cf-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e34cf-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e34cf-112">Puntero a una estructura [**Rect**](/windows/win32/api/windef/ns-windef-rect) que recibe la información del rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="e34cf-112">A pointer to a [**RECT**](/windows/win32/api/windef/ns-windef-rect) structure that receives the bounding rectangle information.</span></span> <span data-ttu-id="e34cf-113">El remitente del mensaje es responsable de la asignación de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="e34cf-113">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="e34cf-114">Las coordenadas devueltas en la estructura RECT se expresan en relación con el elemento primario del control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="e34cf-114">The coordinates returned in the RECT structure are expressed relative to the header control parent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e34cf-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e34cf-115">Return value</span></span>

<span data-ttu-id="e34cf-116">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e34cf-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e34cf-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e34cf-117">Remarks</span></span>

<span data-ttu-id="e34cf-118">El elemento de encabezado debe tener el estilo **HDF \_ SPLITBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="e34cf-118">The header item must have style **HDF\_SPLITBUTTON**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e34cf-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e34cf-119">Requirements</span></span>



| <span data-ttu-id="e34cf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e34cf-120">Requirement</span></span> | <span data-ttu-id="e34cf-121">Value</span><span class="sxs-lookup"><span data-stu-id="e34cf-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e34cf-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e34cf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e34cf-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e34cf-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e34cf-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e34cf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e34cf-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e34cf-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e34cf-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e34cf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e34cf-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e34cf-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e34cf-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e34cf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e34cf-129">Acerca de los controles de encabezado</span><span class="sxs-lookup"><span data-stu-id="e34cf-129">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





