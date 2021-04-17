---
title: Código de notificación de TVN_BEGINLABELEDIT (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol sobre el inicio de la edición de la etiqueta de un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44
keywords:
- TVN_BEGINLABELEDIT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_BEGINLABELEDIT
- TVN_BEGINLABELEDITA
- TVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34eccdeda553d0792a2862e3ca81a0889539d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658209"
---
# <a name="tvn_beginlabeledit-notification-code"></a><span data-ttu-id="ad8ca-105">Código de notificación de BEGINLABELEDIT de TVN \_</span><span class="sxs-lookup"><span data-stu-id="ad8ca-105">TVN\_BEGINLABELEDIT notification code</span></span>

<span data-ttu-id="ad8ca-106">Notifica a la ventana primaria de un control de vista de árbol sobre el inicio de la edición de la etiqueta de un elemento.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-106">Notifies a tree-view control's parent window about the start of label editing for an item.</span></span> <span data-ttu-id="ad8ca-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ad8ca-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="ad8ca-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad8ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad8ca-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad8ca-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad8ca-110">Puntero a una estructura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="ad8ca-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="ad8ca-111">El miembro del **elemento** es una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene información válida sobre el elemento que se está editando en los miembros **hItem**, **State**, **lParam** y **miembros pszText** .</span><span class="sxs-lookup"><span data-stu-id="ad8ca-111">The **item** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the item being edited in the **hItem**, **state**, **lParam**, and **pszText** members.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad8ca-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad8ca-112">Return value</span></span>

<span data-ttu-id="ad8ca-113">Devuelve **true** para cancelar la edición de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-113">Returns **TRUE** to cancel label editing.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad8ca-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad8ca-114">Remarks</span></span>

<span data-ttu-id="ad8ca-115">Cuando comienza la edición de etiquetas, se crea un control de edición pero no se coloca ni se muestra.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-115">When label editing begins, an edit control is created but not positioned or displayed.</span></span> <span data-ttu-id="ad8ca-116">Antes de que se muestre, el control de vista de árbol envía a su ventana primaria un \_ código de notificación TVN BEGINLABELEDIT.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-116">Before it is displayed, the tree-view control sends its parent window a TVN\_BEGINLABELEDIT notification code.</span></span>

<span data-ttu-id="ad8ca-117">Para personalizar la edición de etiquetas, implemente un controlador para TVN \_ BEGINLABELEDIT y envíe un mensaje [**TVM \_ GETEDITCONTROL**](tvm-geteditcontrol.md) al control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-117">To customize label editing, implement a handler for TVN\_BEGINLABELEDIT and have it send a [**TVM\_GETEDITCONTROL**](tvm-geteditcontrol.md) message to the tree-view control.</span></span> <span data-ttu-id="ad8ca-118">Si se está editando una etiqueta, el valor devuelto será un identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-118">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="ad8ca-119">Use este identificador para personalizar el control de edición mediante el envío de los mensajes de EM \_ XXX habituales.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-119">Use this handle to customize the edit control by sending the usual EM\_XXX messages.</span></span>

<span data-ttu-id="ad8ca-120">Cuando el usuario cancela o completa la edición, la ventana primaria recibe un código de notificación [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="ad8ca-120">When the user cancels or completes the editing, the parent window receives a [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad8ca-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad8ca-121">Requirements</span></span>



| <span data-ttu-id="ad8ca-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad8ca-122">Requirement</span></span> | <span data-ttu-id="ad8ca-123">Value</span><span class="sxs-lookup"><span data-stu-id="ad8ca-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad8ca-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad8ca-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ad8ca-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ad8ca-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ad8ca-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad8ca-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ad8ca-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad8ca-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad8ca-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad8ca-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad8ca-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad8ca-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ad8ca-130">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ad8ca-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ad8ca-131">**TVN \_ BEGINLABELEDITW** (Unicode) y **TVN \_ BEGINLABELEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ad8ca-131">**TVN\_BEGINLABELEDITW** (Unicode) and **TVN\_BEGINLABELEDITA** (ANSI)</span></span><br/>     |



 

 





