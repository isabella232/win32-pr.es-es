---
title: Mensaje de LVM_GETITEMRECT (commctrl. h)
description: Recupera el rectángulo delimitador para todo o parte de un elemento de la vista actual. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemRect de ListView.
ms.assetid: 7ce74b65-3360-42b4-9889-d90aefe2d284
keywords:
- LVM_GETITEMRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0915c9afc16f13ac8f36a639524fb5af6e8082
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079654"
---
# <a name="lvm_getitemrect-message"></a><span data-ttu-id="6d65c-105">\_Mensaje GETITEMRECT LVM</span><span class="sxs-lookup"><span data-stu-id="6d65c-105">LVM\_GETITEMRECT message</span></span>

<span data-ttu-id="6d65c-106">Recupera el rectángulo delimitador para todo o parte de un elemento de la vista actual.</span><span class="sxs-lookup"><span data-stu-id="6d65c-106">Retrieves the bounding rectangle for all or part of an item in the current view.</span></span> <span data-ttu-id="6d65c-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemRect de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="6d65c-107">You can send this message explicitly or by using the [**ListView\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d65c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d65c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d65c-109">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6d65c-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d65c-110">Índice del elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="6d65c-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="6d65c-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6d65c-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d65c-112">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="6d65c-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span> <span data-ttu-id="6d65c-113">Cuando se envía el mensaje, el miembro **izquierdo** de esta estructura se usa para especificar la parte del elemento de vista de lista de la que se va a recuperar el rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="6d65c-113">When the message is sent, the **left** member of this structure is used to specify the portion of the list-view item from which to retrieve the bounding rectangle.</span></span> <span data-ttu-id="6d65c-114">Debe establecerse en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="6d65c-114">It must be set to one of the following values:</span></span>



| <span data-ttu-id="6d65c-115">Value</span><span class="sxs-lookup"><span data-stu-id="6d65c-115">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="6d65c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="6d65c-116">Meaning</span></span>                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <span data-ttu-id="6d65c-117"><dt>**límites de LVIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6d65c-117"><dt>**LVIR\_BOUNDS**</dt></span></span> </dl>                   | <span data-ttu-id="6d65c-118">Devuelve el rectángulo delimitador del elemento completo, incluidos el icono y la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="6d65c-118">Returns the bounding rectangle of the entire item, including the icon and label.</span></span><br/>                     |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <span data-ttu-id="6d65c-119"><dt>**icono de LVIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6d65c-119"><dt>**LVIR\_ICON**</dt></span></span> </dl>                         | <span data-ttu-id="6d65c-120">Devuelve el rectángulo delimitador del icono o del icono pequeño.</span><span class="sxs-lookup"><span data-stu-id="6d65c-120">Returns the bounding rectangle of the icon or small icon.</span></span><br/>                                            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <span data-ttu-id="6d65c-121"><dt>**\_etiqueta LVIR**</dt></span><span class="sxs-lookup"><span data-stu-id="6d65c-121"><dt>**LVIR\_LABEL**</dt></span></span> </dl>                      | <span data-ttu-id="6d65c-122">Devuelve el rectángulo delimitador del texto del elemento.</span><span class="sxs-lookup"><span data-stu-id="6d65c-122">Returns the bounding rectangle of the item text.</span></span><br/>                                                     |
| <span id="LVIR_SELECTBOUNDS"></span><span id="lvir_selectbounds"></span><dl> <span data-ttu-id="6d65c-123"><dt>**LVIR \_ SELECTBOUNDS**</dt></span><span class="sxs-lookup"><span data-stu-id="6d65c-123"><dt>**LVIR\_SELECTBOUNDS**</dt></span></span> </dl> | <span data-ttu-id="6d65c-124">Devuelve la Unión del icono de LVIR \_ y los \_ rectángulos de etiqueta de LVIR, pero excluye las columnas en la vista de informe.</span><span class="sxs-lookup"><span data-stu-id="6d65c-124">Returns the union of the LVIR\_ICON and LVIR\_LABEL rectangles, but excludes columns in report view.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d65c-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d65c-125">Return value</span></span>

<span data-ttu-id="6d65c-126">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6d65c-126">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d65c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d65c-127">Requirements</span></span>



| <span data-ttu-id="6d65c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d65c-128">Requirement</span></span> | <span data-ttu-id="6d65c-129">Value</span><span class="sxs-lookup"><span data-stu-id="6d65c-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d65c-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d65c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6d65c-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6d65c-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d65c-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d65c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6d65c-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6d65c-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d65c-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d65c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d65c-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d65c-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

