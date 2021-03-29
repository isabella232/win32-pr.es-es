---
title: Código de notificación de TVN_ENDLABELEDIT (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol sobre el final de la edición de etiquetas para un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- TVN_ENDLABELEDIT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_ENDLABELEDIT
- TVN_ENDLABELEDITA
- TVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30d494ad90b3d55f85b1ad154aed0f814a1eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150359"
---
# <a name="tvn_endlabeledit-notification-code"></a><span data-ttu-id="e9aec-105">Código de notificación de ENDLABELEDIT de TVN \_</span><span class="sxs-lookup"><span data-stu-id="e9aec-105">TVN\_ENDLABELEDIT notification code</span></span>

<span data-ttu-id="e9aec-106">Notifica a la ventana primaria de un control de vista de árbol sobre el final de la edición de etiquetas para un elemento.</span><span class="sxs-lookup"><span data-stu-id="e9aec-106">Notifies a tree-view control's parent window about the end of label editing for an item.</span></span> <span data-ttu-id="e9aec-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e9aec-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="e9aec-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9aec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9aec-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9aec-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9aec-110">Puntero a una estructura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="e9aec-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="e9aec-111">El **miembro** de esta estructura es una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cuyos miembros **hItem**, **lParam** y **miembros pszText** contienen información válida sobre el elemento que se editó.</span><span class="sxs-lookup"><span data-stu-id="e9aec-111">The **item** member of this structure is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **hItem**, **lParam**, and **pszText** members contain valid information about the item that was edited.</span></span> <span data-ttu-id="e9aec-112">Si se canceló la edición de la etiqueta, el miembro **miembros pszText** de la estructura **TVITEM** es **null**. de lo contrario, **miembros pszText** es la dirección del texto editado.</span><span class="sxs-lookup"><span data-stu-id="e9aec-112">If label editing was canceled, the **pszText** member of the **TVITEM** structure is **NULL**; otherwise, **pszText** is the address of the edited text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9aec-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9aec-113">Return value</span></span>

<span data-ttu-id="e9aec-114">Si el miembro **miembros pszText** no es **null**, devuelva **true** para establecer la etiqueta del elemento en el texto editado.</span><span class="sxs-lookup"><span data-stu-id="e9aec-114">If the **pszText** member is non-**NULL**, return **TRUE** to set the item's label to the edited text.</span></span> <span data-ttu-id="e9aec-115">Devuelve **false** para rechazar el texto editado y volver a la etiqueta original.</span><span class="sxs-lookup"><span data-stu-id="e9aec-115">Return **FALSE** to reject the edited text and revert to the original label.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9aec-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9aec-116">Remarks</span></span>

<span data-ttu-id="e9aec-117">Si el miembro **miembros pszText** es **null**, se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="e9aec-117">If the **pszText** member is **NULL**, the return value is ignored.</span></span>

<span data-ttu-id="e9aec-118">Si especificó el \_ valor de LPSTR TEXTCALLBACK para este elemento y el miembro **miembros pszText** no es **null**, el \_ controlador TVN ENDLABELEDIT debe copiar el texto de **miembros pszText** en el almacenamiento local.</span><span class="sxs-lookup"><span data-stu-id="e9aec-118">If you specified the LPSTR\_TEXTCALLBACK value for this item and the **pszText** member is non-**NULL**, your TVN\_ENDLABELEDIT handler should copy the text from **pszText** to your local storage.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9aec-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9aec-119">Requirements</span></span>



| <span data-ttu-id="e9aec-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9aec-120">Requirement</span></span> | <span data-ttu-id="e9aec-121">Value</span><span class="sxs-lookup"><span data-stu-id="e9aec-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9aec-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9aec-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e9aec-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e9aec-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9aec-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9aec-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e9aec-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e9aec-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9aec-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9aec-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9aec-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9aec-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e9aec-128">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="e9aec-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e9aec-129">**TVN \_ ENDLABELEDITW** (Unicode) y **TVN \_ ENDLABELEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e9aec-129">**TVN\_ENDLABELEDITW** (Unicode) and **TVN\_ENDLABELEDITA** (ANSI)</span></span><br/>         |



 

 





