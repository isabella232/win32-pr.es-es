---
title: Mensaje de TVM_INSERTITEM (commctrl. h)
description: Inserta un nuevo elemento en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro InsertItem de TreeView.
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- TVM_INSERTITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_INSERTITEM
- TVM_INSERTITEMA
- TVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719de4c2391ff924c9f6deb8cb4206cfdb56c3ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905102"
---
# <a name="tvm_insertitem-message"></a><span data-ttu-id="ba3fb-105">Mensaje de error de INSERTITEM de TVM \_</span><span class="sxs-lookup"><span data-stu-id="ba3fb-105">TVM\_INSERTITEM message</span></span>

<span data-ttu-id="ba3fb-106">Inserta un nuevo elemento en un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-106">Inserts a new item in a tree-view control.</span></span> <span data-ttu-id="ba3fb-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ InsertItem de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="ba3fb-107">You can send this message explicitly or by using the [**TreeView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba3fb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba3fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba3fb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba3fb-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ba3fb-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ba3fb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba3fb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba3fb-112">Puntero a una estructura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) que especifica los atributos del elemento de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-112">Pointer to a [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure that specifies the attributes of the tree-view item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba3fb-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba3fb-113">Return value</span></span>

<span data-ttu-id="ba3fb-114">Devuelve el identificador **HTREEITEM** para el nuevo elemento si se realiza correctamente, o **null** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-114">Returns the **HTREEITEM** handle to the new item if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba3fb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba3fb-115">Requirements</span></span>



| <span data-ttu-id="ba3fb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba3fb-116">Requirement</span></span> | <span data-ttu-id="ba3fb-117">Value</span><span class="sxs-lookup"><span data-stu-id="ba3fb-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba3fb-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba3fb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ba3fb-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ba3fb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba3fb-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba3fb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ba3fb-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba3fb-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba3fb-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba3fb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba3fb-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba3fb-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ba3fb-124">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ba3fb-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ba3fb-125">**TVM \_ INSERTITEMW** (Unicode) y **TVM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ba3fb-125">**TVM\_INSERTITEMW** (Unicode) and **TVM\_INSERTITEMA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="ba3fb-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba3fb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba3fb-127">TVN \_ ENDLABELEDIT</span><span class="sxs-lookup"><span data-stu-id="ba3fb-127">TVN\_ENDLABELEDIT</span></span>](tvn-endlabeledit.md)
</dt> </dl>

 

 





