---
title: Mensaje de LVM_GETITEM (commctrl. h)
description: Recupera algunos o todos los atributos de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItem de ListView.
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- LVM_GETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETITEM
- LVM_GETITEMA
- LVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c19632567db5e37059b1b028a8ec1fc9385268cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803397"
---
# <a name="lvm_getitem-message"></a><span data-ttu-id="15f75-105">\_Mensaje GETITEM de LVM</span><span class="sxs-lookup"><span data-stu-id="15f75-105">LVM\_GETITEM message</span></span>

<span data-ttu-id="15f75-106">Recupera algunos o todos los atributos de un elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="15f75-106">Retrieves some or all of a list-view item's attributes.</span></span> <span data-ttu-id="15f75-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItem de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) .</span><span class="sxs-lookup"><span data-stu-id="15f75-107">You can send this message explicitly or by using the [**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="15f75-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15f75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15f75-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15f75-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="15f75-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="15f75-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="15f75-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15f75-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15f75-112">Puntero a una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que especifica la información que se va a recuperar y recibe información sobre el elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="15f75-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that specifies the information to retrieve and receives information about the list-view item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15f75-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15f75-113">Return value</span></span>

<span data-ttu-id="15f75-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="15f75-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="15f75-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15f75-115">Remarks</span></span>

<span data-ttu-id="15f75-116">Cuando se envía el mensaje **\_ GETITEM de LVM** , los miembros **iItem** y **iSubItem** identifican el elemento o subelemento del que se va a recuperar información y el miembro de **máscara** especifica los atributos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="15f75-116">When the **LVM\_GETITEM** message is sent, the **iItem** and **iSubItem** members identify the item or subitem to retrieve information about and the **mask** member specifies which attributes to retrieve.</span></span> <span data-ttu-id="15f75-117">Para obtener una lista de los valores posibles, vea la descripción de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="15f75-117">For a list of possible values, see the description of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

<span data-ttu-id="15f75-118">Si la \_ marca de texto LVIF se establece en el miembro **Mask** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , el miembro **miembros pszText** debe apuntar a un búfer válido y el miembro **cchTextMax** debe establecerse en el número de caracteres de ese búfer.</span><span class="sxs-lookup"><span data-stu-id="15f75-118">If the LVIF\_TEXT flag is set in the **mask** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure, the **pszText** member must point to a valid buffer and the **cchTextMax** member must be set to the number of characters in that buffer.</span></span> <span data-ttu-id="15f75-119">Las aplicaciones no deben suponer que el texto se colocará necesariamente en el búfer especificado.</span><span class="sxs-lookup"><span data-stu-id="15f75-119">Applications should not assume that the text will necessarily be placed in the specified buffer.</span></span> <span data-ttu-id="15f75-120">En su lugar, el control puede cambiar el miembro **miembros pszText** de la estructura para que apunte al nuevo texto, en lugar de colocarlo en el búfer.</span><span class="sxs-lookup"><span data-stu-id="15f75-120">The control may instead change the **pszText** member of the structure to point to the new text, rather than place it in the buffer.</span></span>

<span data-ttu-id="15f75-121">Si el miembro **Mask** especifica el \_ valor de estado LVIF, el miembro **stateMask** debe especificar los bits de estado del elemento que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="15f75-121">If the **mask** member specifies the LVIF\_STATE value, the **stateMask** member must specify the item state bits to retrieve.</span></span> <span data-ttu-id="15f75-122">En la salida, el miembro **State** contiene los valores de los bits de estado especificados.</span><span class="sxs-lookup"><span data-stu-id="15f75-122">On output, the **state** member contains the values of the specified state bits.</span></span>

## <a name="requirements"></a><span data-ttu-id="15f75-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15f75-123">Requirements</span></span>



| <span data-ttu-id="15f75-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="15f75-124">Requirement</span></span> | <span data-ttu-id="15f75-125">Value</span><span class="sxs-lookup"><span data-stu-id="15f75-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15f75-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15f75-126">Minimum supported client</span></span><br/> | <span data-ttu-id="15f75-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="15f75-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="15f75-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15f75-128">Minimum supported server</span></span><br/> | <span data-ttu-id="15f75-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="15f75-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="15f75-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15f75-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="15f75-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="15f75-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="15f75-132">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="15f75-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="15f75-133">**LVM \_ GETITEMW** (Unicode) y **\_ GETITEMA de LVM** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="15f75-133">**LVM\_GETITEMW** (Unicode) and **LVM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





