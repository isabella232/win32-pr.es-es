---
title: Mensaje de BCM_SETDROPDOWNSTATE (commctrl. h)
description: Establece el estado desplegable de un botón con la \_ lista desplegable de estilo TBSTYLE. Envíe este mensaje explícitamente o mediante la \_ macro Button SetDropDownState.
ms.assetid: 725deff4-0bcb-497d-a6cf-e9c98b05f16e
keywords:
- BCM_SETDROPDOWNSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BCM_SETDROPDOWNSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc44ec58d40e047708591121f81c84f327ca47c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150270"
---
# <a name="bcm_setdropdownstate-message"></a><span data-ttu-id="6726b-105">\_Mensaje SETDROPDOWNSTATE de BCM</span><span class="sxs-lookup"><span data-stu-id="6726b-105">BCM\_SETDROPDOWNSTATE message</span></span>

<span data-ttu-id="6726b-106">Establece el estado desplegable de un botón con la [**\_ lista desplegable**](toolbar-control-and-button-styles.md)de estilo TBSTYLE.</span><span class="sxs-lookup"><span data-stu-id="6726b-106">Sets the drop down state for a button with style [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md).</span></span> <span data-ttu-id="6726b-107">Envíe este mensaje explícitamente o mediante la macro [**Button \_ SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) .</span><span class="sxs-lookup"><span data-stu-id="6726b-107">Send this message explicitly or by using the [**Button\_SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6726b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6726b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6726b-109">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6726b-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6726b-110">Valor **booleano** que es **true** para el estado de BST \_ DROPDOWNPUSHED o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6726b-110">A **BOOL** that is **TRUE** for state of BST\_DROPDOWNPUSHED, or **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="6726b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6726b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6726b-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6726b-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6726b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6726b-113">Return value</span></span>

<span data-ttu-id="6726b-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6726b-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6726b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6726b-115">Requirements</span></span>



| <span data-ttu-id="6726b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6726b-116">Requirement</span></span> | <span data-ttu-id="6726b-117">Value</span><span class="sxs-lookup"><span data-stu-id="6726b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6726b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6726b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6726b-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6726b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6726b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6726b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6726b-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6726b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6726b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6726b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6726b-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6726b-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6726b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6726b-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="6726b-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="6726b-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6726b-126">Estilos de botón</span><span class="sxs-lookup"><span data-stu-id="6726b-126">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="6726b-127">**Vista**</span><span class="sxs-lookup"><span data-stu-id="6726b-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6726b-128">Tipos de botón</span><span class="sxs-lookup"><span data-stu-id="6726b-128">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





