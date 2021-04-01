---
title: Mensaje de TVM_GETSCROLLTIME (commctrl. h)
description: Recupera el tiempo de desplazamiento máximo para el control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro GetScrollTime de TreeView.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- TVM_GETSCROLLTIME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f0bacc6c12dd7f54f20d882faf738c11848d59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150058"
---
# <a name="tvm_getscrolltime-message"></a><span data-ttu-id="db5d4-105">\_Mensaje de GETSCROLLTIME TVM</span><span class="sxs-lookup"><span data-stu-id="db5d4-105">TVM\_GETSCROLLTIME message</span></span>

<span data-ttu-id="db5d4-106">Recupera el tiempo de desplazamiento máximo para el control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="db5d4-106">Retrieves the maximum scroll time for the tree-view control.</span></span> <span data-ttu-id="db5d4-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetScrollTime de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) .</span><span class="sxs-lookup"><span data-stu-id="db5d4-107">You can send this message explicitly or by using the [**TreeView\_GetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="db5d4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db5d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db5d4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="db5d4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="db5d4-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="db5d4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="db5d4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db5d4-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="db5d4-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="db5d4-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db5d4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db5d4-113">Return value</span></span>

<span data-ttu-id="db5d4-114">Devuelve el tiempo de desplazamiento máximo, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="db5d4-114">Returns the maximum scroll time, in milliseconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="db5d4-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db5d4-115">Remarks</span></span>

<span data-ttu-id="db5d4-116">El tiempo de desplazamiento máximo es la cantidad más larga de tiempo que puede tardar una operación de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="db5d4-116">The maximum scroll time is the longest amount of time that a scroll operation can take.</span></span> <span data-ttu-id="db5d4-117">El desplazamiento se ajustará para que el desplazamiento tenga lugar dentro del tiempo de desplazamiento máximo.</span><span class="sxs-lookup"><span data-stu-id="db5d4-117">The scrolling will be adjusted so that the scroll will take place within the maximum scroll time.</span></span> <span data-ttu-id="db5d4-118">Una operación de desplazamiento puede tardar menos tiempo que el máximo.</span><span class="sxs-lookup"><span data-stu-id="db5d4-118">A scroll operation may take less time than the maximum.</span></span>

## <a name="requirements"></a><span data-ttu-id="db5d4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db5d4-119">Requirements</span></span>



| <span data-ttu-id="db5d4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="db5d4-120">Requirement</span></span> | <span data-ttu-id="db5d4-121">Value</span><span class="sxs-lookup"><span data-stu-id="db5d4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db5d4-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db5d4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="db5d4-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="db5d4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db5d4-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db5d4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="db5d4-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="db5d4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db5d4-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db5d4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="db5d4-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="db5d4-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db5d4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="db5d4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db5d4-129">**TVM \_ SETSCROLLTIME**</span><span class="sxs-lookup"><span data-stu-id="db5d4-129">**TVM\_SETSCROLLTIME**</span></span>](tvm-setscrolltime.md)
</dt> </dl>

 

 





