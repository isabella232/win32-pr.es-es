---
title: Código de notificación de LVN_SETDISPINFO (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que debe actualizar la información que mantiene para un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- LVN_SETDISPINFO controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_SETDISPINFO
- LVN_SETDISPINFOA
- LVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659623d892f0f5a556f4890703d4e0dd725536b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996744"
---
# <a name="lvn_setdispinfo-notification-code"></a><span data-ttu-id="d7ef7-105">Código de notificación de SETDISPINFO de LVN \_</span><span class="sxs-lookup"><span data-stu-id="d7ef7-105">LVN\_SETDISPINFO notification code</span></span>

<span data-ttu-id="d7ef7-106">Notifica a la ventana primaria de un control de vista de lista que debe actualizar la información que mantiene para un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-106">Notifies a list-view control's parent window that it must update the information it maintains for an item.</span></span> <span data-ttu-id="d7ef7-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d7ef7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a><span data-ttu-id="d7ef7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7ef7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7ef7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7ef7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7ef7-110">Puntero a una estructura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) que especifica información del elemento modificado.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure that specifies information for the changed item.</span></span> <span data-ttu-id="d7ef7-111">El miembro del **elemento** de esta estructura es una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que contiene información sobre el elemento que se ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that contains information about the item that was changed.</span></span> <span data-ttu-id="d7ef7-112">El miembro **miembros pszText** del **elemento** contiene un valor válido, independientemente de si la \_ marca de texto LVIF se establece en el miembro de **máscara** de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-112">The **pszText** member of **item** contains a valid value, regardless of whether the LVIF\_TEXT flag is set in the **mask** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7ef7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7ef7-113">Return value</span></span>

<span data-ttu-id="d7ef7-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7ef7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7ef7-115">Remarks</span></span>

<span data-ttu-id="d7ef7-116">El receptor de notificaciones convierte *lParam* para recuperar la estructura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="d7ef7-116">The notification receiver casts *lParam* to retrieve the [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="d7ef7-117">El parámetro *wParam* contiene el código de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d7ef7-117">The *wParam* parameter contains the message code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7ef7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7ef7-118">Requirements</span></span>



| <span data-ttu-id="d7ef7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7ef7-119">Requirement</span></span> | <span data-ttu-id="d7ef7-120">Value</span><span class="sxs-lookup"><span data-stu-id="d7ef7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ef7-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7ef7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d7ef7-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d7ef7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7ef7-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7ef7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d7ef7-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7ef7-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7ef7-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7ef7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7ef7-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7ef7-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d7ef7-127">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="d7ef7-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d7ef7-128">**LVN \_ SETDISPINFOW** (Unicode) y **LVN \_ SETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d7ef7-128">**LVN\_SETDISPINFOW** (Unicode) and **LVN\_SETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="d7ef7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7ef7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7ef7-130">LVN \_ GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="d7ef7-130">LVN\_GETDISPINFO</span></span>](lvn-getdispinfo.md)
</dt> </dl>

 

 





