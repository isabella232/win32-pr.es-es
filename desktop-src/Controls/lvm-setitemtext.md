---
title: Mensaje de LVM_SETITEMTEXT (commctrl. h)
description: Cambia el texto de un elemento o subelemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro SetItemText de ListView.
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- LVM_SETITEMTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMTEXT
- LVM_SETITEMTEXTA
- LVM_SETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326e48047325fc9aff2c6607da6d7d377965adf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905290"
---
# <a name="lvm_setitemtext-message"></a><span data-ttu-id="5cc45-105">\_Mensaje SETITEMTEXT LVM</span><span class="sxs-lookup"><span data-stu-id="5cc45-105">LVM\_SETITEMTEXT message</span></span>

<span data-ttu-id="5cc45-106">Cambia el texto de un elemento o subelemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="5cc45-106">Changes the text of a list-view item or subitem.</span></span> <span data-ttu-id="5cc45-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetItemText de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) .</span><span class="sxs-lookup"><span data-stu-id="5cc45-107">You can send this message explicitly or by using the [**ListView\_SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5cc45-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5cc45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cc45-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5cc45-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5cc45-110">Índice de base cero del elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="5cc45-110">Zero-based index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="5cc45-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5cc45-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5cc45-112">Puntero a una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="5cc45-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="5cc45-113">El miembro **iSubItem** es el índice del subelemento, o puede ser cero para establecer la etiqueta del elemento.</span><span class="sxs-lookup"><span data-stu-id="5cc45-113">The **iSubItem** member is the index of the subitem, or it can be zero to set the item label.</span></span> <span data-ttu-id="5cc45-114">El miembro **miembros pszText** es la dirección de una cadena terminada en null que contiene el nuevo texto. también puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="5cc45-114">The **pszText** member is the address of a null-terminated string containing the new text; it can also be **NULL**.</span></span> <span data-ttu-id="5cc45-115">El miembro **miembros pszText** también puede ser LPSTR \_ TEXTCALLBACK para indicar un elemento de devolución de llamada para el que la ventana primaria almacena el texto.</span><span class="sxs-lookup"><span data-stu-id="5cc45-115">The **pszText** member can also be LPSTR\_TEXTCALLBACK to indicate a callback item for which the parent window stores the text.</span></span> <span data-ttu-id="5cc45-116">En este caso, el control de vista de lista envía el elemento primario a un código de notificación [**LVN \_ GETDISPINFO**](lvn-getdispinfo.md) cuando necesita el texto.</span><span class="sxs-lookup"><span data-stu-id="5cc45-116">In this case, the list-view control sends the parent an [**LVN\_GETDISPINFO**](lvn-getdispinfo.md) notification code when it needs the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cc45-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5cc45-117">Return value</span></span>

<span data-ttu-id="5cc45-118">Si envía este mensaje explícitamente, devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5cc45-118">If you send this message explicitly, it returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cc45-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cc45-119">Requirements</span></span>



| <span data-ttu-id="5cc45-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cc45-120">Requirement</span></span> | <span data-ttu-id="5cc45-121">Value</span><span class="sxs-lookup"><span data-stu-id="5cc45-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5cc45-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5cc45-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5cc45-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5cc45-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5cc45-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5cc45-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5cc45-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5cc45-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5cc45-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5cc45-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cc45-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cc45-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5cc45-128">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="5cc45-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5cc45-129">**LVM \_ SETITEMTEXTW** (Unicode) y **\_ SETITEMTEXTA de LVM** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5cc45-129">**LVM\_SETITEMTEXTW** (Unicode) and **LVM\_SETITEMTEXTA** (ANSI)</span></span><br/>           |



 

 





