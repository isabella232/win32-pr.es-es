---
title: Código de notificación de LVN_ENDLABELEDIT (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista el final de la edición de la etiqueta de un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 03129fef-abf1-4374-b4b8-503c46ef7115
keywords:
- LVN_ENDLABELEDIT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_ENDLABELEDIT
- LVN_ENDLABELEDITA
- LVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a33ab69a04202aeb3817d3eeadf01fb6f1fcaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658422"
---
# <a name="lvn_endlabeledit-notification-code"></a><span data-ttu-id="ac74a-105">Código de notificación de ENDLABELEDIT de LVN \_</span><span class="sxs-lookup"><span data-stu-id="ac74a-105">LVN\_ENDLABELEDIT notification code</span></span>

<span data-ttu-id="ac74a-106">Notifica a la ventana primaria de un control de vista de lista el final de la edición de la etiqueta de un elemento.</span><span class="sxs-lookup"><span data-stu-id="ac74a-106">Notifies a list-view control's parent window about the end of label editing for an item.</span></span> <span data-ttu-id="ac74a-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ac74a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ENDLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ac74a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac74a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac74a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac74a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac74a-110">Puntero a una estructura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="ac74a-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="ac74a-111">El miembro del **elemento** de esta estructura es una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) cuyo miembro **iItem** identifica el elemento que se está editando.</span><span class="sxs-lookup"><span data-stu-id="ac74a-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure whose **iItem** member identifies the item being edited.</span></span> <span data-ttu-id="ac74a-112">El miembro **miembros pszText** del **elemento** contiene un valor válido cuando \_ se envía el código de notificación LVN ENDLABELEDIT, independientemente de si la \_ marca de texto LVIF está establecida en el miembro **Mask** de la estructura **LVITEM** .</span><span class="sxs-lookup"><span data-stu-id="ac74a-112">The **pszText** member of **item** contains a valid value when the LVN\_ENDLABELEDIT notification code is sent, regardless of whether the LVIF\_TEXT flag is set in the **mask** member of the **LVITEM** structure.</span></span> <span data-ttu-id="ac74a-113">Si el usuario cancela la edición, el miembro **miembros pszText** de la estructura **LVITEM** es **null**. de lo contrario, **miembros pszText** es la dirección del texto editado.</span><span class="sxs-lookup"><span data-stu-id="ac74a-113">If the user cancels editing, the **pszText** member of the **LVITEM** structure is **NULL**; otherwise, **pszText** is the address of the edited text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac74a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac74a-114">Return value</span></span>

<span data-ttu-id="ac74a-115">Si el miembro **miembros pszText** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) no es **null**, devuelva **true** para establecer la etiqueta del elemento en el texto editado.</span><span class="sxs-lookup"><span data-stu-id="ac74a-115">If the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure is non-**NULL**, return **TRUE** to set the item's label to the edited text.</span></span> <span data-ttu-id="ac74a-116">Devuelve **false** para rechazar el texto editado y volver a la etiqueta original.</span><span class="sxs-lookup"><span data-stu-id="ac74a-116">Return **FALSE** to reject the edited text and revert to the original label.</span></span>

<span data-ttu-id="ac74a-117">Si el miembro **miembros pszText** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) es **null**, se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="ac74a-117">If the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure is **NULL**, the return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac74a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac74a-118">Remarks</span></span>

<span data-ttu-id="ac74a-119">El valor devuelto del procedimiento de cuadro de diálogo es si se controló el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ac74a-119">The return value of the dialog procedure is whether the message was handled.</span></span> <span data-ttu-id="ac74a-120">El segundo valor devuelto se debe establecer llamando a [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) con **DWLP_MSGRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ac74a-120">The second return value must be set by calling [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) with **DWLP_MSGRESULT**.</span></span>

<span data-ttu-id="ac74a-121">Cuando el usuario comienza a editar una etiqueta de elemento, la ventana primaria del control de vista de lista recibe un código de notificación [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="ac74a-121">When the user begins editing an item label, the parent window of the list-view control receives an [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) notification code.</span></span> <span data-ttu-id="ac74a-122">Cuando el usuario cancela o completa la edición, la ventana primaria recibe un \_ código de notificación LVN ENDLABELEDIT.</span><span class="sxs-lookup"><span data-stu-id="ac74a-122">When the user cancels or completes the editing, the parent window receives an LVN\_ENDLABELEDIT notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac74a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac74a-123">Requirements</span></span>



| <span data-ttu-id="ac74a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac74a-124">Requirement</span></span> | <span data-ttu-id="ac74a-125">Value</span><span class="sxs-lookup"><span data-stu-id="ac74a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac74a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac74a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ac74a-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ac74a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ac74a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac74a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ac74a-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac74a-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac74a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac74a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac74a-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac74a-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ac74a-132">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ac74a-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ac74a-133">**LVN \_ ENDLABELEDITW** (Unicode) y **LVN \_ ENDLABELEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ac74a-133">**LVN\_ENDLABELEDITW** (Unicode) and **LVN\_ENDLABELEDITA** (ANSI)</span></span><br/>         |



 

 





