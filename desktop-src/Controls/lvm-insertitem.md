---
title: Mensaje de LVM_INSERTITEM (commctrl. h)
description: Inserta un nuevo elemento en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro InsertItem de ListView.
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- LVM_INSERTITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_INSERTITEM
- LVM_INSERTITEMA
- LVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467c6b595e307dc16f87e40da858ff8b120fb3f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658331"
---
# <a name="lvm_insertitem-message"></a><span data-ttu-id="7ac8f-105">\_Mensaje INSERTITEM de LVM</span><span class="sxs-lookup"><span data-stu-id="7ac8f-105">LVM\_INSERTITEM message</span></span>

<span data-ttu-id="7ac8f-106">Inserta un nuevo elemento en un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="7ac8f-106">Inserts a new item in a list-view control.</span></span> <span data-ttu-id="7ac8f-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ InsertItem de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="7ac8f-107">You can send this message explicitly or by using the [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ac8f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ac8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ac8f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ac8f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7ac8f-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7ac8f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7ac8f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ac8f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ac8f-112">Puntero a una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que especifica los atributos del elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="7ac8f-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that specifies the attributes of the list-view item.</span></span> <span data-ttu-id="7ac8f-113">Use el miembro **iItem** para especificar el índice basado en cero en el que se debe insertar el nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="7ac8f-113">Use the **iItem** member to specify the zero-based index at which the new item should be inserted.</span></span> <span data-ttu-id="7ac8f-114">Si este valor es mayor que el número de elementos que contiene ListView actualmente, el nuevo elemento se anexará al final de la lista y se le asignará el índice correcto.</span><span class="sxs-lookup"><span data-stu-id="7ac8f-114">If this value is greater than the number of items currently contained by the listview, the new item will be appended to the end of the list and assigned the correct index.</span></span> <span data-ttu-id="7ac8f-115">Examine el valor devuelto del mensaje para determinar el índice real asignado al elemento.</span><span class="sxs-lookup"><span data-stu-id="7ac8f-115">Examine the message's return value to determine the actual index assigned to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ac8f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ac8f-116">Return value</span></span>

<span data-ttu-id="7ac8f-117">Devuelve el índice del nuevo elemento si se realiza correctamente, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7ac8f-117">Returns the index of the new item if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ac8f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ac8f-118">Remarks</span></span>

<span data-ttu-id="7ac8f-119">No se puede usar [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) o **LVM \_ InsertItem** para insertar subelementos.</span><span class="sxs-lookup"><span data-stu-id="7ac8f-119">You cannot use [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) or **LVM\_INSERTITEM** to insert subitems.</span></span> <span data-ttu-id="7ac8f-120">El miembro **iSubItem** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7ac8f-120">The **iSubItem** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure must be zero.</span></span> <span data-ttu-id="7ac8f-121">Vea [**LVM \_ SETITEM**](lvm-setitem.md) para obtener información sobre la configuración de subelementos.</span><span class="sxs-lookup"><span data-stu-id="7ac8f-121">See [**LVM\_SETITEM**](lvm-setitem.md) for information on setting subitems.</span></span>

<span data-ttu-id="7ac8f-122">Si un control de vista de lista tiene establecido el estilo [**\_ \_ casillas de LVS ex**](extended-list-view-styles.md) , se omitirá cualquier valor colocado en los bits 12 a 15 del miembro **State** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="7ac8f-122">If a list-view control has the [**LVS\_EX\_CHECKBOXES**](extended-list-view-styles.md) style set, any value placed in bits 12 through 15 of the **state** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure will be ignored.</span></span> <span data-ttu-id="7ac8f-123">Cuando se agrega un elemento con este conjunto de estilos, siempre se establecerá en el estado desactivado.</span><span class="sxs-lookup"><span data-stu-id="7ac8f-123">When an item is added with this style set, it will always be set to the unchecked state.</span></span>

<span data-ttu-id="7ac8f-124">Si un control de vista de lista tiene el estilo de ventana [**LVS \_ SORTASCENDING**](list-view-window-styles.md) o [**LVS \_ SORTDESCENDING**](list-view-window-styles.md) , se producirá un error en un mensaje **\_ INSERTITEM de LVM** si intenta insertar un elemento que tenga LPSTR \_ TEXTCALLBACK como valor para su miembro **miembros pszText** .</span><span class="sxs-lookup"><span data-stu-id="7ac8f-124">If a list-view control has either the [**LVS\_SORTASCENDING**](list-view-window-styles.md) or [**LVS\_SORTDESCENDING**](list-view-window-styles.md) window style, an **LVM\_INSERTITEM** message will fail if you try to insert an item that has LPSTR\_TEXTCALLBACK as the value for its **pszText** member.</span></span>

<span data-ttu-id="7ac8f-125">El **mensaje \_ INSERTITEM de LVM** insertará el nuevo elemento en la posición adecuada en el criterio de ordenación si se cumplen las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="7ac8f-125">The **LVM\_INSERTITEM** message will insert the new item in the proper position in the sort order if the following conditions hold:</span></span>

-   <span data-ttu-id="7ac8f-126">Está usando uno de los estilos de LVS \_ SORTXXX.</span><span class="sxs-lookup"><span data-stu-id="7ac8f-126">You are using one of the LVS\_SORTXXX styles.</span></span>
-   <span data-ttu-id="7ac8f-127">No se usa el estilo [**\_ OWNERDRAW LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="7ac8f-127">You are not using the [**LVS\_OWNERDRAW**](list-view-window-styles.md) style.</span></span>
-   <span data-ttu-id="7ac8f-128">El miembro **miembros pszText** de la estructura a la que apunta **pitem** no se establece en LPSTR \_ TEXTCALLBACK.</span><span class="sxs-lookup"><span data-stu-id="7ac8f-128">The **pszText** member of the structure pointed to by **pitem** is not set to LPSTR\_TEXTCALLBACK.</span></span>

<span data-ttu-id="7ac8f-129">Si la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) no contiene LVIF \_ GROUPID en el miembro **Mask** , el valor del miembro **iGroupId** es GROUPIDCALLBACK de \_ forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7ac8f-129">If the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure does not contain LVIF\_GROUPID in the **mask** member, the value of the **iGroupId** member is I\_GROUPIDCALLBACK by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ac8f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ac8f-130">Requirements</span></span>



| <span data-ttu-id="7ac8f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ac8f-131">Requirement</span></span> | <span data-ttu-id="7ac8f-132">Value</span><span class="sxs-lookup"><span data-stu-id="7ac8f-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac8f-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ac8f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7ac8f-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7ac8f-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7ac8f-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ac8f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7ac8f-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ac8f-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ac8f-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ac8f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ac8f-138"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ac8f-138"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7ac8f-139">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="7ac8f-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7ac8f-140">**LVM \_ INSERTITEMW** (Unicode) y **\_ INSERTITEMA de LVM** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7ac8f-140">**LVM\_INSERTITEMW** (Unicode) and **LVM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





