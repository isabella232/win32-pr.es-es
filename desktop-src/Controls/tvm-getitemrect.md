---
title: Mensaje de TVM_GETITEMRECT (commctrl. h)
description: Recupera el rectángulo delimitador de un elemento de vista de árbol e indica si el elemento está visible. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemRect de TreeView.
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- TVM_GETITEMRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebdf4d73fb83ddbd8e9e682f11ee1f5ecfbd5153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150184"
---
# <a name="tvm_getitemrect-message"></a><span data-ttu-id="24c51-105">\_Mensaje de GETITEMRECT TVM</span><span class="sxs-lookup"><span data-stu-id="24c51-105">TVM\_GETITEMRECT message</span></span>

<span data-ttu-id="24c51-106">Recupera el rectángulo delimitador de un elemento de vista de árbol e indica si el elemento está visible.</span><span class="sxs-lookup"><span data-stu-id="24c51-106">Retrieves the bounding rectangle for a tree-view item and indicates whether the item is visible.</span></span> <span data-ttu-id="24c51-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemRect de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="24c51-107">You can send this message explicitly or by using the [**TreeView\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="24c51-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24c51-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24c51-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24c51-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24c51-110">Valor que especifica la parte del elemento para la que se va a recuperar el rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="24c51-110">Value specifying the portion of the item for which to retrieve the bounding rectangle.</span></span> <span data-ttu-id="24c51-111">Si este parámetro es **true**, el rectángulo delimitador solo incluye el texto del elemento.</span><span class="sxs-lookup"><span data-stu-id="24c51-111">If this parameter is **TRUE**, the bounding rectangle includes only the text of the item.</span></span> <span data-ttu-id="24c51-112">De lo contrario, incluye la línea completa que el elemento ocupa en el control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="24c51-112">Otherwise, it includes the entire line that the item occupies in the tree-view control.</span></span>

</dd> <dt>

<span data-ttu-id="24c51-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24c51-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24c51-114">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que, al enviar el mensaje, contiene el identificador del elemento para el que se va a recuperar el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="24c51-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that, when sending the message, contains the handle of the item to retrieve the rectangle for.</span></span> <span data-ttu-id="24c51-115">Vea el ejemplo siguiente para obtener más información sobre cómo colocar el identificador de elemento en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="24c51-115">See the example below for more information on how to place the item handle in this parameter.</span></span> <span data-ttu-id="24c51-116">Después de devolver el mensaje, este parámetro contiene el rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="24c51-116">After returning from the message, this parameter contains the bounding rectangle.</span></span> <span data-ttu-id="24c51-117">Las coordenadas son relativas a la esquina superior izquierda del control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="24c51-117">The coordinates are relative to the upper-left corner of the tree-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24c51-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24c51-118">Return value</span></span>

<span data-ttu-id="24c51-119">Si el elemento está visible y el rectángulo delimitador se recuperó correctamente, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="24c51-119">If the item is visible and the bounding rectangle was successfully retrieved, the return value is **TRUE**.</span></span> <span data-ttu-id="24c51-120">De lo contrario, el mensaje devuelve **false** y no recupera el rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="24c51-120">Otherwise, the message returns **FALSE** and does not retrieve the bounding rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="24c51-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24c51-121">Remarks</span></span>

<span data-ttu-id="24c51-122">Al enviar este mensaje, el parámetro *lParam* contiene el identificador del elemento para el que se recupera el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="24c51-122">When sending this message, the *lParam* parameter contains the handle of the item that the rectangle is being retrieved for.</span></span> <span data-ttu-id="24c51-123">El identificador se coloca en *lParam* tal y como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="24c51-123">The handle is placed in *lParam* as shown in the following example:</span></span>


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a><span data-ttu-id="24c51-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24c51-124">Requirements</span></span>



| <span data-ttu-id="24c51-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="24c51-125">Requirement</span></span> | <span data-ttu-id="24c51-126">Value</span><span class="sxs-lookup"><span data-stu-id="24c51-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24c51-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24c51-127">Minimum supported client</span></span><br/> | <span data-ttu-id="24c51-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="24c51-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24c51-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24c51-129">Minimum supported server</span></span><br/> | <span data-ttu-id="24c51-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="24c51-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="24c51-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24c51-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="24c51-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="24c51-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

