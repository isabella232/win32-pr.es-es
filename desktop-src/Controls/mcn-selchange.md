---
title: Código de notificación de MCN_SELCHANGE (commctrl. h)
description: Se envía por un control de calendario mensual cuando cambia la fecha o el intervalo de fechas seleccionado actualmente. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 8923524f-d257-409d-bd3e-021684b88856
keywords:
- MCN_SELCHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- MCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffa328ca0173afd3a577f6cf14e0204cd5c0f7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079004"
---
# <a name="mcn_selchange-notification-code"></a><span data-ttu-id="4be68-105">Código de notificación de SELCHANGE de MCN \_</span><span class="sxs-lookup"><span data-stu-id="4be68-105">MCN\_SELCHANGE notification code</span></span>

<span data-ttu-id="4be68-106">Se envía por un control de calendario mensual cuando cambia la fecha o el intervalo de fechas seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="4be68-106">Sent by a month calendar control when the currently selected date or range of dates changes.</span></span> <span data-ttu-id="4be68-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4be68-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_SELCHANGE

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="4be68-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4be68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4be68-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4be68-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4be68-110">Puntero a una estructura [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) que contiene información sobre el intervalo de fechas seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="4be68-110">Pointer to an [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) structure that contains information about the currently selected date range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4be68-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4be68-111">Return value</span></span>

<span data-ttu-id="4be68-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4be68-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4be68-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4be68-113">Remarks</span></span>

<span data-ttu-id="4be68-114">Por ejemplo, el control envía MCN \_ SELCHANGE cuando el usuario cambia explícitamente la selección en el mes actual o cuando la selección se cambia implícitamente en respuesta a la navegación de mes anterior o siguiente.</span><span class="sxs-lookup"><span data-stu-id="4be68-114">For example, the control sends MCN\_SELCHANGE when the user explicitly changes the selection within the current month or when the selection is implicitly changed in response to next/previous month navigation.</span></span> <span data-ttu-id="4be68-115">El sistema también envía este código de notificación a intervalos regulares para que el control pueda responder a los cambios de fecha.</span><span class="sxs-lookup"><span data-stu-id="4be68-115">This notification code is also sent by the system at regular intervals so that the control can respond to date changes.</span></span>

<span data-ttu-id="4be68-116">Este código de notificación es similar a [MCN \_ Select](mcn-select.md), pero se envía como respuesta a cualquier cambio de selección.</span><span class="sxs-lookup"><span data-stu-id="4be68-116">This notification code is similar to [MCN\_SELECT](mcn-select.md), but it is sent in response to any selection change.</span></span> <span data-ttu-id="4be68-117">MCN \_ Select solo se envía para una selección de fecha explícita.</span><span class="sxs-lookup"><span data-stu-id="4be68-117">MCN\_SELECT is sent only for an explicit date selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="4be68-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4be68-118">Requirements</span></span>



| <span data-ttu-id="4be68-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4be68-119">Requirement</span></span> | <span data-ttu-id="4be68-120">Value</span><span class="sxs-lookup"><span data-stu-id="4be68-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4be68-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4be68-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4be68-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4be68-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4be68-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4be68-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4be68-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4be68-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4be68-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4be68-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4be68-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4be68-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





