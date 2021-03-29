---
title: Código de notificación de LVN_GETEMPTYMARKUP (commctrl. h)
description: Lo envía el control de vista de lista a su ventana primaria cuando el control no tiene elementos. El \_ código de notificación de GETEMPTYMARKUP de LVN es una solicitud para que la ventana primaria proporcione texto de marcado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- LVN_GETEMPTYMARKUP controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_GETEMPTYMARKUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea693475ca42f962be07936f980cd3f5d52479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905696"
---
# <a name="lvn_getemptymarkup-notification-code"></a><span data-ttu-id="f9107-106">Código de notificación de GETEMPTYMARKUP de LVN \_</span><span class="sxs-lookup"><span data-stu-id="f9107-106">LVN\_GETEMPTYMARKUP notification code</span></span>

<span data-ttu-id="f9107-107">Lo envía el control de vista de lista a su ventana primaria cuando el control no tiene elementos.</span><span class="sxs-lookup"><span data-stu-id="f9107-107">Sent by list-view control to its parent window when the control has no items.</span></span> <span data-ttu-id="f9107-108">El \_ código de notificación de GETEMPTYMARKUP de LVN es una solicitud para que la ventana primaria proporcione texto de marcado.</span><span class="sxs-lookup"><span data-stu-id="f9107-108">The LVN\_GETEMPTYMARKUP notification code is a request for the parent window to provide markup text.</span></span> <span data-ttu-id="f9107-109">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f9107-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETEMPTYMARKUP
        
    pnmMarkup = (NMLVEMPTYMARKUP*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f9107-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9107-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9107-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9107-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9107-112">Puntero a una estructura [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) .</span><span class="sxs-lookup"><span data-stu-id="f9107-112">Pointer to a [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) structure.</span></span> <span data-ttu-id="f9107-113">Establezca los miembros de esta estructura para proporcionar texto de marcado para el control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="f9107-113">Set the members of this structure to provide markup text for the list-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9107-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9107-114">Return value</span></span>

<span data-ttu-id="f9107-115">Devuelva **true** para establecer el texto de marcado en el control de vista de lista o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f9107-115">Return **TRUE** to set the markup text in the list-view control, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9107-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9107-116">Remarks</span></span>

<span data-ttu-id="f9107-117">El receptor de notificaciones convierte *lParam* para recuperar la estructura [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) .</span><span class="sxs-lookup"><span data-stu-id="f9107-117">The notification receiver casts *lParam* to retrieve the [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) structure.</span></span> <span data-ttu-id="f9107-118">El parámetro *wParam* contiene el identificador del control que envía este mensaje.</span><span class="sxs-lookup"><span data-stu-id="f9107-118">The *wParam* parameter contains the ID of the control that sends this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9107-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9107-119">Requirements</span></span>



| <span data-ttu-id="f9107-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9107-120">Requirement</span></span> | <span data-ttu-id="f9107-121">Value</span><span class="sxs-lookup"><span data-stu-id="f9107-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9107-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9107-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f9107-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f9107-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9107-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9107-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f9107-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f9107-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9107-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9107-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9107-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9107-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





