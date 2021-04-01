---
title: Mensaje de TVM_SETITEMHEIGHT (commctrl. h)
description: Establece el alto de los elementos de la vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro SetItemHeight de TreeView.
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- TVM_SETITEMHEIGHT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114769f689cbf8d9475460e40d205c4282a1a787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996554"
---
# <a name="tvm_setitemheight-message"></a><span data-ttu-id="fb29d-105">\_Mensaje de SETITEMHEIGHT TVM</span><span class="sxs-lookup"><span data-stu-id="fb29d-105">TVM\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="fb29d-106">Establece el alto de los elementos de la vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="fb29d-106">Sets the height of the tree-view items.</span></span> <span data-ttu-id="fb29d-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetItemHeight de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) .</span><span class="sxs-lookup"><span data-stu-id="fb29d-107">You can send this message explicitly or by using the [**TreeView\_SetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fb29d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb29d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb29d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fb29d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb29d-110">Nuevo alto de cada elemento en la vista de árbol, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="fb29d-110">New height of every item in the tree view, in pixels.</span></span> <span data-ttu-id="fb29d-111">El alto inferior a 1 se establecerá en 1.</span><span class="sxs-lookup"><span data-stu-id="fb29d-111">Heights less than 1 will be set to 1.</span></span> <span data-ttu-id="fb29d-112">Si este argumento no es par y el control de vista de árbol no tiene el [**estilo \_ NONEVENHEIGHT de TV**](tree-view-control-window-styles.md) , este valor se redondeará al valor par más cercano.</span><span class="sxs-lookup"><span data-stu-id="fb29d-112">If this argument is not even and the tree-view control does not have the [**TVS\_NONEVENHEIGHT**](tree-view-control-window-styles.md) style, this value will be rounded down to the nearest even value.</span></span> <span data-ttu-id="fb29d-113">Si este argumento es-1, el control volverá a usar su alto predeterminado del elemento.</span><span class="sxs-lookup"><span data-stu-id="fb29d-113">If this argument is -1, the control will revert to using its default item height.</span></span>

</dd> <dt>

<span data-ttu-id="fb29d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb29d-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fb29d-115">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fb29d-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb29d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb29d-116">Return value</span></span>

<span data-ttu-id="fb29d-117">Devuelve el alto anterior de los elementos, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="fb29d-117">Returns the previous height of the items, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb29d-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb29d-118">Remarks</span></span>

<span data-ttu-id="fb29d-119">El control de vista de árbol usa este valor para el alto de todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="fb29d-119">The tree-view control uses this value for the height of all items.</span></span> <span data-ttu-id="fb29d-120">Para modificar el alto de elementos individuales, vea la descripción del miembro **iIntegral** de la estructura [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .</span><span class="sxs-lookup"><span data-stu-id="fb29d-120">To modify the height of individual items, see the description of the **iIntegral** member of the [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb29d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb29d-121">Requirements</span></span>



| <span data-ttu-id="fb29d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb29d-122">Requirement</span></span> | <span data-ttu-id="fb29d-123">Value</span><span class="sxs-lookup"><span data-stu-id="fb29d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb29d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb29d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fb29d-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fb29d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fb29d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb29d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fb29d-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb29d-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fb29d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb29d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb29d-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb29d-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb29d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb29d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb29d-131">**TVM \_ GETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="fb29d-131">**TVM\_GETITEMHEIGHT**</span></span>](tvm-getitemheight.md)
</dt> </dl>

 

 





