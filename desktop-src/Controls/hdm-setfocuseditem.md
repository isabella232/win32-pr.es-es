---
title: Mensaje de HDM_SETFOCUSEDITEM (commctrl. h)
description: Establece el foco en un elemento especificado de un control de encabezado. Envíe este mensaje explícitamente o mediante la \_ macro header SetFocusedItem.
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- HDM_SETFOCUSEDITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_SETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd416744478248760f4e2c9f94a362db5a8d327
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150823"
---
# <a name="hdm_setfocuseditem-message"></a><span data-ttu-id="092e3-105">HDM \_ SETFOCUSEDITEM</span><span class="sxs-lookup"><span data-stu-id="092e3-105">HDM\_SETFOCUSEDITEM message</span></span>

<span data-ttu-id="092e3-106">Establece el foco en un elemento especificado de un control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="092e3-106">Sets the focus to a specified item in a header control.</span></span> <span data-ttu-id="092e3-107">Envíe este mensaje explícitamente o mediante la macro [**Header \_ SetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) .</span><span class="sxs-lookup"><span data-stu-id="092e3-107">Send this message explicitly or by using the [**Header\_SetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="092e3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="092e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="092e3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="092e3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="092e3-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="092e3-110">Not used.</span></span> <span data-ttu-id="092e3-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="092e3-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="092e3-112">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="092e3-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="092e3-113">Índice del elemento.</span><span class="sxs-lookup"><span data-stu-id="092e3-113">The index of item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="092e3-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="092e3-114">Return value</span></span>

<span data-ttu-id="092e3-115">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="092e3-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="092e3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="092e3-116">Requirements</span></span>



| <span data-ttu-id="092e3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="092e3-117">Requirement</span></span> | <span data-ttu-id="092e3-118">Value</span><span class="sxs-lookup"><span data-stu-id="092e3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="092e3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="092e3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="092e3-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="092e3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="092e3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="092e3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="092e3-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="092e3-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="092e3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="092e3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="092e3-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="092e3-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="092e3-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="092e3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="092e3-126">Acerca de los controles de encabezado</span><span class="sxs-lookup"><span data-stu-id="092e3-126">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





