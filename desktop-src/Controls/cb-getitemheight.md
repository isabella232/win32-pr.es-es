---
title: Mensaje de CB_GETITEMHEIGHT (Winuser. h)
description: Determina el alto de los elementos de lista o el campo de selección en un cuadro combinado.
ms.assetid: 72fba6ca-0a51-4801-bd45-5f5a7d5ebee2
keywords:
- CB_GETITEMHEIGHT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4aac9d8f9a430c056f8b91a9306d77c182f4c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905244"
---
# <a name="cb_getitemheight-message"></a><span data-ttu-id="a5319-104">\_Mensaje GETITEMHEIGHT CB</span><span class="sxs-lookup"><span data-stu-id="a5319-104">CB\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="a5319-105">Determina el alto de los elementos de lista o el campo de selección en un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="a5319-105">Determines the height of list items or the selection field in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="a5319-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5319-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5319-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a5319-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5319-108">Componente de cuadro combinado cuyo alto se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="a5319-108">The combo box component whose height is to be retrieved.</span></span> <span data-ttu-id="a5319-109">Este parámetro debe ser-1 para recuperar el alto del campo de selección.</span><span class="sxs-lookup"><span data-stu-id="a5319-109">This parameter must be -1 to retrieve the height of the selection field.</span></span> <span data-ttu-id="a5319-110">Debe ser cero para recuperar el alto de los elementos de lista, a menos que el cuadro combinado tenga el estilo [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a5319-110">It must be zero to retrieve the height of list items, unless the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="a5319-111">En ese caso, el parámetro *wParam* es el índice de base cero de un elemento de lista específico.</span><span class="sxs-lookup"><span data-stu-id="a5319-111">In that case, the *wParam* parameter is the zero-based index of a specific list item.</span></span>

</dd> <dt>

<span data-ttu-id="a5319-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a5319-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5319-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a5319-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5319-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5319-114">Return value</span></span>

<span data-ttu-id="a5319-115">El valor devuelto es el alto, en píxeles, de los elementos de lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="a5319-115">The return value is the height, in pixels, of the list items in a combo box.</span></span> <span data-ttu-id="a5319-116">Si el cuadro combinado tiene el estilo [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) , es el alto del elemento especificado por el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="a5319-116">If the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style, it is the height of the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="a5319-117">Si *wParam* es-1, el valor devuelto es el alto de la parte del control de edición (o texto estático) del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="a5319-117">If *wParam* is -1, the return value is the height of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="a5319-118">Si se produce un error, el valor devuelto es CB \_ error.</span><span class="sxs-lookup"><span data-stu-id="a5319-118">If an error occurs, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5319-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5319-119">Requirements</span></span>



| <span data-ttu-id="a5319-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5319-120">Requirement</span></span> | <span data-ttu-id="a5319-121">Value</span><span class="sxs-lookup"><span data-stu-id="a5319-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5319-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5319-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a5319-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a5319-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a5319-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5319-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a5319-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5319-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a5319-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5319-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5319-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5319-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5319-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5319-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="a5319-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="a5319-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a5319-130">**CB \_ SETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="a5319-130">**CB\_SETITEMHEIGHT**</span></span>](cb-setitemheight.md)
</dt> <dt>

[<span data-ttu-id="a5319-131">**MEASUREITEM de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a5319-131">**WM\_MEASUREITEM**</span></span>](wm-measureitem.md)
</dt> </dl>

 

 





