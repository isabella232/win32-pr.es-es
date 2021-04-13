---
title: Código de notificación de LVN_COLUMNOVERFLOWCLICK (commctrl. h)
description: Se envía por un control de vista de lista cuando se hace clic en el botón de desbordamiento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 3d3bb7be-b598-450a-b829-a5aa5b1a0c5d
keywords:
- LVN_COLUMNOVERFLOWCLICK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_COLUMNOVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7938d28be337f7255a9b84422fa090da5a494cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493336"
---
# <a name="lvn_columnoverflowclick-notification-code"></a><span data-ttu-id="a6f8f-105">Código de notificación de COLUMNOVERFLOWCLICK de LVN \_</span><span class="sxs-lookup"><span data-stu-id="a6f8f-105">LVN\_COLUMNOVERFLOWCLICK notification code</span></span>

<span data-ttu-id="a6f8f-106">Se envía por un control de vista de lista cuando se hace clic en el botón de desbordamiento.</span><span class="sxs-lookup"><span data-stu-id="a6f8f-106">Sent by a list-view control when its overflow button is clicked.</span></span> <span data-ttu-id="a6f8f-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a6f8f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNOVERFLOWCLICK
     
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a6f8f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6f8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6f8f-109">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a6f8f-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f8f-110">Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que describe el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="a6f8f-110">Pointer to a [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that describes the notification code.</span></span> <span data-ttu-id="a6f8f-111">El autor de la llamada es responsable de asignar esta estructura, incluida la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenida.</span><span class="sxs-lookup"><span data-stu-id="a6f8f-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="a6f8f-112">Establezca los miembros de la estructura **NMHDR** .</span><span class="sxs-lookup"><span data-stu-id="a6f8f-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="a6f8f-113">El miembro de **código** debe establecerse en LVN \_ COLUMNOVERFLOWCLICK.</span><span class="sxs-lookup"><span data-stu-id="a6f8f-113">The **code** member must be set to LVN\_COLUMNOVERFLOWCLICK.</span></span>

<span data-ttu-id="a6f8f-114">Establezca el miembro **iItem** de la estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) en-1.</span><span class="sxs-lookup"><span data-stu-id="a6f8f-114">Set the **iItem** member of the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure to -1.</span></span> <span data-ttu-id="a6f8f-115">Establezca el miembro **iSubItem** en el índice del subelemento.</span><span class="sxs-lookup"><span data-stu-id="a6f8f-115">Set the **iSubItem** member to the index of the subitem.</span></span> <span data-ttu-id="a6f8f-116">Establezca los miembros **uNewState**, **uOldState** y **lParam** en cero.</span><span class="sxs-lookup"><span data-stu-id="a6f8f-116">Set the **uNewState**, **uOldState**, and **lParam** members to zero.</span></span> <span data-ttu-id="a6f8f-117">No se usan los miembros restantes de la estructura **NMLISTVIEW** .</span><span class="sxs-lookup"><span data-stu-id="a6f8f-117">The remaining members of the **NMLISTVIEW** structure are not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6f8f-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6f8f-118">Return value</span></span>

<span data-ttu-id="a6f8f-119">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a6f8f-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6f8f-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6f8f-120">Remarks</span></span>

<span data-ttu-id="a6f8f-121">El receptor de notificaciones convierte *lParam* para recuperar la estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="a6f8f-121">The notification receiver casts *lParam* to retrieve the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="a6f8f-122">El parámetro *wParam* contiene el identificador del control que envía el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="a6f8f-122">The *wParam* parameter contains the ID of the control that sends the notification code.</span></span>

<span data-ttu-id="a6f8f-123">Si un control de encabezado es un elemento secundario del control ListView, el control de encabezado debería enviar este código de notificación al control ListView cuando el control de encabezado reciba el código de notificación [ \_ OVERFLOWCLICK de HDN](hdn-overflowclick.md) .</span><span class="sxs-lookup"><span data-stu-id="a6f8f-123">If a header control is a child of the listview, the header control should send this notification code to the listview control when the header control receives the [HDN\_OVERFLOWCLICK](hdn-overflowclick.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6f8f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6f8f-124">Requirements</span></span>



| <span data-ttu-id="a6f8f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6f8f-125">Requirement</span></span> | <span data-ttu-id="a6f8f-126">Value</span><span class="sxs-lookup"><span data-stu-id="a6f8f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6f8f-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6f8f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a6f8f-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a6f8f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6f8f-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6f8f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a6f8f-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6f8f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6f8f-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6f8f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6f8f-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6f8f-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





