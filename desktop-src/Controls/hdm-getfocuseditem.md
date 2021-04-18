---
title: Mensaje de HDM_GETFOCUSEDITEM (commctrl. h)
description: Obtiene el elemento de un control de encabezado que tiene el foco. Envíe este mensaje explícitamente o mediante la \_ macro header GetFocusedItem.
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- HDM_GETFOCUSEDITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_GETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c21fcb29f5f431e32ca3f07265b7e96620d5a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491477"
---
# <a name="hdm_getfocuseditem-message"></a><span data-ttu-id="2f272-105">HDM \_ GETFOCUSEDITEM</span><span class="sxs-lookup"><span data-stu-id="2f272-105">HDM\_GETFOCUSEDITEM message</span></span>

<span data-ttu-id="2f272-106">Obtiene el elemento de un control de encabezado que tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="2f272-106">Gets the item in a header control that has the focus.</span></span> <span data-ttu-id="2f272-107">Envíe este mensaje explícitamente o mediante la macro [**Header \_ GetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) .</span><span class="sxs-lookup"><span data-stu-id="2f272-107">Send this message explicitly or by using the [**Header\_GetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f272-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f272-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f272-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f272-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2f272-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="2f272-110">Not used.</span></span> <span data-ttu-id="2f272-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2f272-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2f272-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f272-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2f272-113">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="2f272-113">Not used.</span></span> <span data-ttu-id="2f272-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2f272-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f272-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f272-115">Return value</span></span>

<span data-ttu-id="2f272-116">Devuelve el índice del elemento en el foco.</span><span class="sxs-lookup"><span data-stu-id="2f272-116">Returns the index of the item in focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f272-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f272-117">Requirements</span></span>



| <span data-ttu-id="2f272-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f272-118">Requirement</span></span> | <span data-ttu-id="2f272-119">Value</span><span class="sxs-lookup"><span data-stu-id="2f272-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f272-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f272-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2f272-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2f272-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f272-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f272-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2f272-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f272-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f272-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f272-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f272-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f272-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f272-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f272-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f272-127">Acerca de los controles de encabezado</span><span class="sxs-lookup"><span data-stu-id="2f272-127">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





