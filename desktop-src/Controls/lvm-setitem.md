---
title: Mensaje de LVM_SETITEM (commctrl. h)
description: Establece algunos o todos los atributos de un elemento de vista de lista. También puede enviar LVM \_ SETITEM para establecer el texto de un subelemento. Puede enviar este mensaje explícitamente o mediante la \_ macro SetItem de ListView.
ms.assetid: f1189b5d-bce7-4569-b4b9-bd750d7ef505
keywords:
- LVM_SETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETITEM
- LVM_SETITEMA
- LVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623339c3d1ecc7a74cf20b5e52fb621666391bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079135"
---
# <a name="lvm_setitem-message"></a><span data-ttu-id="d0124-106">\_Mensaje SETITEM LVM</span><span class="sxs-lookup"><span data-stu-id="d0124-106">LVM\_SETITEM message</span></span>

<span data-ttu-id="d0124-107">Establece algunos o todos los atributos de un elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="d0124-107">Sets some or all of a list-view item's attributes.</span></span> <span data-ttu-id="d0124-108">También puede enviar LVM \_ SETITEM para establecer el texto de un subelemento.</span><span class="sxs-lookup"><span data-stu-id="d0124-108">You can also send LVM\_SETITEM to set the text of a subitem.</span></span> <span data-ttu-id="d0124-109">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetItem de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) .</span><span class="sxs-lookup"><span data-stu-id="d0124-109">You can send this message explicitly or by using the [**ListView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0124-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0124-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0124-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0124-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d0124-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d0124-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d0124-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0124-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0124-114">Puntero a una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que contiene los nuevos atributos de elemento.</span><span class="sxs-lookup"><span data-stu-id="d0124-114">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="d0124-115">Los miembros **iItem** y **iSubItem** identifican el elemento o subelemento y el miembro **Mask** especifica los atributos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="d0124-115">The **iItem** and **iSubItem** members identify the item or subitem, and the **mask** member specifies which attributes to set.</span></span> <span data-ttu-id="d0124-116">Si el miembro **Mask** especifica el \_ valor de texto LVIF, el miembro **miembros pszText** es la dirección de una cadena terminada en NULL y se omite el miembro **cchTextMax** .</span><span class="sxs-lookup"><span data-stu-id="d0124-116">If the **mask** member specifies the LVIF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span> <span data-ttu-id="d0124-117">Si el miembro **Mask** especifica el \_ valor de estado LVIF, el miembro **stateMask** especifica qué Estados de elemento se van a cambiar y el miembro **State** contiene los valores de esos Estados.</span><span class="sxs-lookup"><span data-stu-id="d0124-117">If the **mask** member specifies the LVIF\_STATE value, the **stateMask** member specifies which item states to change and the **state** member contains the values for those states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0124-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0124-118">Return value</span></span>

<span data-ttu-id="d0124-119">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d0124-119">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0124-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0124-120">Remarks</span></span>

<span data-ttu-id="d0124-121">Para establecer los atributos de un elemento de vista de lista, establezca el miembro **iItem** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) en el índice del elemento y establezca el miembro **iSubItem** en cero.</span><span class="sxs-lookup"><span data-stu-id="d0124-121">To set the attributes of a list-view item, set the **iItem** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure to the index of the item, and set the **iSubItem** member to zero.</span></span> <span data-ttu-id="d0124-122">Para un elemento, puede establecer los miembros **State**, **miembros pszText**, **iImage** y **lParam** de la estructura **LVITEM** .</span><span class="sxs-lookup"><span data-stu-id="d0124-122">For an item, you can set the **state**, **pszText**, **iImage**, and **lParam** members of the **LVITEM** structure.</span></span>

<span data-ttu-id="d0124-123">Para establecer el texto de un subelemento, establezca los miembros **iItem** y **iSubItem** para indicar el subelemento específico y use el miembro **miembros pszText** para especificar el texto.</span><span class="sxs-lookup"><span data-stu-id="d0124-123">To set the text of a subitem, set the **iItem** and **iSubItem** members to indicate the specific subitem, and use the **pszText** member to specify the text.</span></span> <span data-ttu-id="d0124-124">Como alternativa, puede usar la macro [**\_ SetItemText de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) para establecer el texto de un subelemento.</span><span class="sxs-lookup"><span data-stu-id="d0124-124">Alternatively, you can use the [**ListView\_SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) macro to set the text of a subitem.</span></span> <span data-ttu-id="d0124-125">No se pueden establecer los miembros **State** o **lParam** para los subelementos porque los subelementos no tienen estos atributos.</span><span class="sxs-lookup"><span data-stu-id="d0124-125">You cannot set the **state** or **lParam** members for subitems because subitems do not have these attributes.</span></span> <span data-ttu-id="d0124-126">En la versión 4,70 y posteriores, puede establecer el miembro **iImage** para los subelementos.</span><span class="sxs-lookup"><span data-stu-id="d0124-126">In version 4.70 and later, you can set the **iImage** member for subitems.</span></span> <span data-ttu-id="d0124-127">La imagen del subelemento se mostrará si el control de vista de lista tiene el estilo extendido [**LVS \_ ex \_ SUBITEMIMAGES**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d0124-127">The subitem image will be displayed if the list-view control has the [**LVS\_EX\_SUBITEMIMAGES**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="d0124-128">Las versiones anteriores omitirán la imagen del subelemento.</span><span class="sxs-lookup"><span data-stu-id="d0124-128">Previous versions will ignore the subitem image.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0124-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0124-129">Requirements</span></span>



| <span data-ttu-id="d0124-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0124-130">Requirement</span></span> | <span data-ttu-id="d0124-131">Value</span><span class="sxs-lookup"><span data-stu-id="d0124-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0124-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0124-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d0124-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d0124-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0124-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0124-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d0124-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0124-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0124-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0124-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0124-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0124-137"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d0124-138">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="d0124-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d0124-139">**LVM \_ SETITEMW** (Unicode) y **\_ SETITEMA de LVM** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d0124-139">**LVM\_SETITEMW** (Unicode) and **LVM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





