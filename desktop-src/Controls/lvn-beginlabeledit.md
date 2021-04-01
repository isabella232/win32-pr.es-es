---
title: Código de notificación de LVN_BEGINLABELEDIT (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista el inicio de la edición de la etiqueta de un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- LVN_BEGINLABELEDIT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_BEGINLABELEDIT
- LVN_BEGINLABELEDITA
- LVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f77550b474534cee096b610a0805bce547d9b429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995974"
---
# <a name="lvn_beginlabeledit-notification-code"></a><span data-ttu-id="94c67-105">Código de notificación de BEGINLABELEDIT de LVN \_</span><span class="sxs-lookup"><span data-stu-id="94c67-105">LVN\_BEGINLABELEDIT notification code</span></span>

<span data-ttu-id="94c67-106">Notifica a la ventana primaria de un control de vista de lista el inicio de la edición de la etiqueta de un elemento.</span><span class="sxs-lookup"><span data-stu-id="94c67-106">Notifies a list-view control's parent window about the start of label editing for an item.</span></span> <span data-ttu-id="94c67-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="94c67-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="94c67-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94c67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94c67-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94c67-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94c67-110">Puntero a una estructura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="94c67-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="94c67-111">El miembro del **elemento** de esta estructura es una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) cuyo miembro **iItem** identifica el elemento que se está editando.</span><span class="sxs-lookup"><span data-stu-id="94c67-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure whose **iItem** member identifies the item being edited.</span></span> <span data-ttu-id="94c67-112">Tenga en cuenta que no se pueden editar los subelementos; el miembro **iSubItem** siempre se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="94c67-112">Note that subitems cannot be edited; the **iSubItem** member is always set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94c67-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94c67-113">Return value</span></span>

<span data-ttu-id="94c67-114">Para permitir al usuario editar la etiqueta, devuelva **false**.</span><span class="sxs-lookup"><span data-stu-id="94c67-114">To allow the user to edit the label, return **FALSE**.</span></span>

<span data-ttu-id="94c67-115">Para evitar que el usuario edite la etiqueta, devuelva **true**.</span><span class="sxs-lookup"><span data-stu-id="94c67-115">To prevent the user from editing the label, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="94c67-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94c67-116">Remarks</span></span>

<span data-ttu-id="94c67-117">Cuando comienza la edición de etiquetas, se crea, coloca y Inicializa un control de edición.</span><span class="sxs-lookup"><span data-stu-id="94c67-117">When label editing begins, an edit control is created, positioned, and initialized.</span></span> <span data-ttu-id="94c67-118">Antes de que se muestre, el control de vista de lista envía a su ventana primaria un \_ código de notificación LVN BEGINLABELEDIT.</span><span class="sxs-lookup"><span data-stu-id="94c67-118">Before it is displayed, the list-view control sends its parent window an LVN\_BEGINLABELEDIT notification code.</span></span>

<span data-ttu-id="94c67-119">Para personalizar la edición de etiquetas, implemente un controlador para LVN \_ BEGINLABELEDIT y envíe un mensaje [**LVM \_ GETEDITCONTROL**](lvm-geteditcontrol.md) al control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="94c67-119">To customize label editing, implement a handler for LVN\_BEGINLABELEDIT and have it send an [**LVM\_GETEDITCONTROL**](lvm-geteditcontrol.md) message to the list-view control.</span></span> <span data-ttu-id="94c67-120">Si se está editando una etiqueta, el valor devuelto será un identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="94c67-120">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="94c67-121">Use este identificador para personalizar el control de edición mediante el envío de los mensajes de **em \_ XXX** habituales.</span><span class="sxs-lookup"><span data-stu-id="94c67-121">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

<span data-ttu-id="94c67-122">Cuando el usuario cancela o completa la edición, la ventana primaria recibe un código de notificación [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="94c67-122">When the user cancels or completes the editing, the parent window receives an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="94c67-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94c67-123">Requirements</span></span>



| <span data-ttu-id="94c67-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="94c67-124">Requirement</span></span> | <span data-ttu-id="94c67-125">Value</span><span class="sxs-lookup"><span data-stu-id="94c67-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94c67-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94c67-126">Minimum supported client</span></span><br/> | <span data-ttu-id="94c67-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="94c67-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="94c67-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94c67-128">Minimum supported server</span></span><br/> | <span data-ttu-id="94c67-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="94c67-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="94c67-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94c67-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="94c67-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="94c67-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="94c67-132">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="94c67-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="94c67-133">**LVN \_ BEGINLABELEDITW** (Unicode) y **LVN \_ BEGINLABELEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="94c67-133">**LVN\_BEGINLABELEDITW** (Unicode) and **LVN\_BEGINLABELEDITA** (ANSI)</span></span><br/>     |



 

 





