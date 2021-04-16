---
title: Mensaje de CB_SETITEMHEIGHT (Winuser. h)
description: Una aplicación envía un \_ mensaje CB SETITEMHEIGHT para establecer el alto de los elementos de lista o el campo de selección en un cuadro combinado.
ms.assetid: 25a01170-5ffc-4d86-b696-706f5375570b
keywords:
- CB_SETITEMHEIGHT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e46be007cdea17857e5d8ec42a12228821539d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658362"
---
# <a name="cb_setitemheight-message"></a><span data-ttu-id="c4fee-104">\_Mensaje SETITEMHEIGHT CB</span><span class="sxs-lookup"><span data-stu-id="c4fee-104">CB\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="c4fee-105">Una aplicación envía un mensaje **CB \_ SETITEMHEIGHT** para establecer el alto de los elementos de lista o el campo de selección en un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="c4fee-105">An application sends a **CB\_SETITEMHEIGHT** message to set the height of list items or the selection field in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4fee-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4fee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4fee-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4fee-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4fee-108">Especifica el componente del cuadro combinado para el que se va a establecer el alto.</span><span class="sxs-lookup"><span data-stu-id="c4fee-108">Specifies the component of the combo box for which to set the height.</span></span>

<span data-ttu-id="c4fee-109">Este parámetro debe ser 1 para establecer el alto del campo de selección.</span><span class="sxs-lookup"><span data-stu-id="c4fee-109">This parameter must be  1 to set the height of the selection field.</span></span> <span data-ttu-id="c4fee-110">Debe ser cero para establecer el alto de los elementos de lista, a menos que el cuadro combinado tenga el estilo [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="c4fee-110">It must be zero to set the height of list items, unless the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="c4fee-111">En ese caso, el parámetro *wParam* es el índice de base cero de un elemento de lista específico.</span><span class="sxs-lookup"><span data-stu-id="c4fee-111">In that case, the *wParam* parameter is the zero-based index of a specific list item.</span></span>

</dd> <dt>

<span data-ttu-id="c4fee-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4fee-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4fee-113">Especifica el alto, en píxeles, del componente de cuadro combinado identificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="c4fee-113">Specifies the height, in pixels, of the combo box component identified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4fee-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4fee-114">Return value</span></span>

<span data-ttu-id="c4fee-115">Si el índice o el alto no son válidos, el valor devuelto es CB \_ error.</span><span class="sxs-lookup"><span data-stu-id="c4fee-115">If the index or height is invalid, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4fee-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4fee-116">Remarks</span></span>

<span data-ttu-id="c4fee-117">El alto del campo de selección en un cuadro combinado se establece independientemente del alto de los elementos de la lista.</span><span class="sxs-lookup"><span data-stu-id="c4fee-117">The selection field height in a combo box is set independently of the height of the list items.</span></span> <span data-ttu-id="c4fee-118">Una aplicación debe asegurarse de que el alto del campo de selección no sea menor que el alto de un elemento de lista determinado.</span><span class="sxs-lookup"><span data-stu-id="c4fee-118">An application must ensure that the height of the selection field is not smaller than the height of a particular list item.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4fee-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4fee-119">Requirements</span></span>



| <span data-ttu-id="c4fee-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4fee-120">Requirement</span></span> | <span data-ttu-id="c4fee-121">Value</span><span class="sxs-lookup"><span data-stu-id="c4fee-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4fee-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4fee-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c4fee-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c4fee-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c4fee-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4fee-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c4fee-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c4fee-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c4fee-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4fee-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4fee-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4fee-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4fee-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4fee-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="c4fee-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="c4fee-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c4fee-130">**CB \_ GETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="c4fee-130">**CB\_GETITEMHEIGHT**</span></span>](cb-getitemheight.md)
</dt> <dt>

[<span data-ttu-id="c4fee-131">**MEASUREITEM de WM \_**</span><span class="sxs-lookup"><span data-stu-id="c4fee-131">**WM\_MEASUREITEM**</span></span>](wm-measureitem.md)
</dt> </dl>

 

 





