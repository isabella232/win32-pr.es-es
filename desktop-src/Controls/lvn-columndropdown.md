---
title: Código de notificación de LVN_COLUMNDROPDOWN (commctrl. h)
description: Se envía por un control de vista de lista cuando se presiona el botón desplegable de la vista de lista. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 752d745e-4482-425c-af3c-f9707cbb03d7
keywords:
- LVN_COLUMNDROPDOWN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_COLUMNDROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 792d29268548d95a7f3e70b05d9d2de368a03cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534174"
---
# <a name="lvn_columndropdown-notification-code"></a><span data-ttu-id="1ea69-105">Código de notificación de COLUMNDROPDOWN de LVN \_</span><span class="sxs-lookup"><span data-stu-id="1ea69-105">LVN\_COLUMNDROPDOWN notification code</span></span>

<span data-ttu-id="1ea69-106">Se envía por un control de vista de lista cuando se presiona el botón desplegable de la vista de lista.</span><span class="sxs-lookup"><span data-stu-id="1ea69-106">Sent by a list-view control when the list-view's drop-down button is pressed.</span></span> <span data-ttu-id="1ea69-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea69-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNDROPDOWN
        
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1ea69-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ea69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ea69-109">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1ea69-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ea69-110">Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que describe el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="1ea69-110">Pointer to a [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that describes the notification code.</span></span> <span data-ttu-id="1ea69-111">El autor de la llamada es responsable de asignar esta estructura, incluida la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenida.</span><span class="sxs-lookup"><span data-stu-id="1ea69-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="1ea69-112">Establezca los miembros de la estructura **NMHDR** .</span><span class="sxs-lookup"><span data-stu-id="1ea69-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="1ea69-113">El miembro de **código** debe establecerse en LVN \_ COLUMNDROPDOWN.</span><span class="sxs-lookup"><span data-stu-id="1ea69-113">The **code** member must be set to LVN\_COLUMNDROPDOWN.</span></span>

<span data-ttu-id="1ea69-114">Establezca el miembro **iItem** de la estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) en-1.</span><span class="sxs-lookup"><span data-stu-id="1ea69-114">Set the **iItem** member of the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure to -1.</span></span> <span data-ttu-id="1ea69-115">Establezca el miembro **iSubItem** en el índice del subelemento.</span><span class="sxs-lookup"><span data-stu-id="1ea69-115">Set the **iSubItem** member to the index of the subitem.</span></span> <span data-ttu-id="1ea69-116">Establezca los miembros **uNewState**, **uOldState** y **lParam** en cero.</span><span class="sxs-lookup"><span data-stu-id="1ea69-116">Set the **uNewState**, **uOldState**, and **lParam** members to zero.</span></span> <span data-ttu-id="1ea69-117">No se usan los miembros restantes de la estructura **NMLISTVIEW** .</span><span class="sxs-lookup"><span data-stu-id="1ea69-117">The remaining members of the **NMLISTVIEW** structure are not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ea69-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ea69-118">Return value</span></span>

<span data-ttu-id="1ea69-119">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1ea69-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ea69-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ea69-120">Remarks</span></span>

<span data-ttu-id="1ea69-121">El receptor de notificaciones convierte *lParam* para recuperar la estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="1ea69-121">The notification receiver casts *lParam* to retrieve the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="1ea69-122">El parámetro *wParam* contiene el identificador del control que envía el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="1ea69-122">The *wParam* parameter contains the ID of the control that sends the notification code.</span></span>

<span data-ttu-id="1ea69-123">Si un control de encabezado es un elemento secundario de la vista de lista, el control de encabezado debe enviar este código notificaciones al control de vista de lista cuando el control de encabezado recibe el código de notificación de la lista [ \_ desplegable HDN](hdn-dropdown.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea69-123">If a header control is a child of the list-view, the header control should send this notidication code to the list-view control when the header control receives the [HDN\_DROPDOWN](hdn-dropdown.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ea69-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ea69-124">Requirements</span></span>



| <span data-ttu-id="1ea69-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ea69-125">Requirement</span></span> | <span data-ttu-id="1ea69-126">Value</span><span class="sxs-lookup"><span data-stu-id="1ea69-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ea69-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ea69-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1ea69-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1ea69-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ea69-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ea69-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1ea69-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ea69-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ea69-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ea69-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ea69-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ea69-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





