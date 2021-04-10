---
title: Mensaje de LVM_GETITEMTEXT (commctrl. h)
description: Recupera el texto de un elemento o subelemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemText de ListView.
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- LVM_GETITEMTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMTEXT
- LVM_GETITEMTEXTA
- LVM_GETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c71eec6b9dab4c649b11da5b24568eea816774ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150893"
---
# <a name="lvm_getitemtext-message"></a><span data-ttu-id="5beb2-105">\_Mensaje GETITEMTEXT LVM</span><span class="sxs-lookup"><span data-stu-id="5beb2-105">LVM\_GETITEMTEXT message</span></span>

<span data-ttu-id="5beb2-106">Recupera el texto de un elemento o subelemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="5beb2-106">Retrieves the text of a list-view item or subitem.</span></span> <span data-ttu-id="5beb2-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemText de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) .</span><span class="sxs-lookup"><span data-stu-id="5beb2-107">You can send this message explicitly or by using the [**ListView\_GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5beb2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5beb2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5beb2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5beb2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5beb2-110">Índice del elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="5beb2-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="5beb2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5beb2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5beb2-112">Puntero a una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="5beb2-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="5beb2-113">Para recuperar el texto del elemento, establezca **iSubItem** en cero.</span><span class="sxs-lookup"><span data-stu-id="5beb2-113">To retrieve the item text, set **iSubItem** to zero.</span></span> <span data-ttu-id="5beb2-114">Para recuperar el texto de un subelemento, establezca **iSubItem** en el índice del subelemento.</span><span class="sxs-lookup"><span data-stu-id="5beb2-114">To retrieve the text of a subitem, set **iSubItem** to the subitem's index.</span></span> <span data-ttu-id="5beb2-115">El miembro **miembros pszText** apunta a un búfer que recibe el texto.</span><span class="sxs-lookup"><span data-stu-id="5beb2-115">The **pszText** member points to a buffer that receives the text.</span></span> <span data-ttu-id="5beb2-116">El miembro **cchTextMax** especifica el número de caracteres del búfer.</span><span class="sxs-lookup"><span data-stu-id="5beb2-116">The **cchTextMax** member specifies the number of characters in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5beb2-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5beb2-117">Return value</span></span>

<span data-ttu-id="5beb2-118">Si envía este mensaje explícitamente, devuelve el número de caracteres en el miembro **miembros pszText** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="5beb2-118">If you send this message explicitly, it returns the number of characters in the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="5beb2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5beb2-119">Remarks</span></span>

<span data-ttu-id="5beb2-120">También puede enviar este mensaje mediante una llamada a la macro [**\_ GetItemText de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) .</span><span class="sxs-lookup"><span data-stu-id="5beb2-120">You can also send this message by calling the [**ListView\_GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) macro.</span></span> <span data-ttu-id="5beb2-121">Sin embargo, esta macro no devuelve la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="5beb2-121">However, this macro does not return the string length.</span></span>

<span data-ttu-id="5beb2-122">**LVM \_ GETITEMTEXT** no se admite en el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5beb2-122">**LVM\_GETITEMTEXT** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="5beb2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5beb2-123">Requirements</span></span>



| <span data-ttu-id="5beb2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5beb2-124">Requirement</span></span> | <span data-ttu-id="5beb2-125">Value</span><span class="sxs-lookup"><span data-stu-id="5beb2-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5beb2-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5beb2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5beb2-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5beb2-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5beb2-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5beb2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5beb2-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5beb2-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5beb2-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5beb2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5beb2-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5beb2-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5beb2-132">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="5beb2-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5beb2-133">**LVM \_ GETITEMTEXTW** (Unicode) y **\_ GETITEMTEXTA de LVM** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5beb2-133">**LVM\_GETITEMTEXTW** (Unicode) and **LVM\_GETITEMTEXTA** (ANSI)</span></span><br/>           |



 

 





