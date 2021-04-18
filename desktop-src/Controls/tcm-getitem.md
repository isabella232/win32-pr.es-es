---
title: Mensaje de TCM_GETITEM (commctrl. h)
description: Recupera información sobre una pestaña de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetItem.
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- TCM_GETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_GETITEM
- TCM_GETITEMA
- TCM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f94f26a0893416847df052ff47731391a86f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658355"
---
# <a name="tcm_getitem-message"></a><span data-ttu-id="ded0d-105">\_Mensaje GETITEM de TCM</span><span class="sxs-lookup"><span data-stu-id="ded0d-105">TCM\_GETITEM message</span></span>

<span data-ttu-id="ded0d-106">Recupera información sobre una pestaña de un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="ded0d-106">Retrieves information about a tab in a tab control.</span></span> <span data-ttu-id="ded0d-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) .</span><span class="sxs-lookup"><span data-stu-id="ded0d-107">You can send this message explicitly or by using the [**TabCtrl\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ded0d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ded0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ded0d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ded0d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ded0d-110">Índice de la pestaña.</span><span class="sxs-lookup"><span data-stu-id="ded0d-110">Index of the tab.</span></span>

</dd> <dt>

<span data-ttu-id="ded0d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ded0d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ded0d-112">Puntero a una estructura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que especifica la información que se va a recuperar y recibe información sobre la ficha. Cuando se envía el mensaje, el miembro de la **máscara** especifica los atributos que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="ded0d-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that specifies the information to retrieve and receives information about the tab. When the message is sent, the **mask** member specifies which attributes to return.</span></span> <span data-ttu-id="ded0d-113">Si el miembro **Mask** especifica el \_ valor de texto TCIF, el miembro **miembros pszText** debe contener la dirección del búfer que recibe el texto del elemento y el miembro **cchTextMax** debe especificar el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="ded0d-113">If the **mask** member specifies the TCIF\_TEXT value, the **pszText** member must contain the address of the buffer that receives the item text, and the **cchTextMax** member must specify the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ded0d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ded0d-114">Return value</span></span>

<span data-ttu-id="ded0d-115">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ded0d-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ded0d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ded0d-116">Remarks</span></span>

<span data-ttu-id="ded0d-117">Si la \_ marca de texto TCIF se establece en el miembro **Mask** de la estructura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) , el control puede cambiar el miembro **miembros pszText** de la estructura para que apunte al nuevo texto en lugar de llenar el búfer con el texto solicitado.</span><span class="sxs-lookup"><span data-stu-id="ded0d-117">If the TCIF\_TEXT flag is set in the **mask** member of the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="ded0d-118">El control puede establecer el miembro **miembros pszText** en **null** para indicar que no hay texto asociado al elemento.</span><span class="sxs-lookup"><span data-stu-id="ded0d-118">The control may set the **pszText** member to **NULL** to indicate that no text is associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="ded0d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ded0d-119">Requirements</span></span>



| <span data-ttu-id="ded0d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ded0d-120">Requirement</span></span> | <span data-ttu-id="ded0d-121">Value</span><span class="sxs-lookup"><span data-stu-id="ded0d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ded0d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ded0d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ded0d-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ded0d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ded0d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ded0d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ded0d-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ded0d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ded0d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ded0d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ded0d-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ded0d-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ded0d-128">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ded0d-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ded0d-129">**TCM \_ GETITEMW** (Unicode) y **TCM \_ GETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ded0d-129">**TCM\_GETITEMW** (Unicode) and **TCM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





