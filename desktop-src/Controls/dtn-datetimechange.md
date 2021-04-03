---
title: Código de notificación de DTN_DATETIMECHANGE (commctrl. h)
description: Se envía mediante un control de selector de fecha y hora (DTP) cada vez que se produce un cambio. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 65cdd8fb-1f07-4447-b503-d40fdfa37202
keywords:
- DTN_DATETIMECHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- DTN_DATETIMECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40072a54732a0a3575e3153ddb901ca1df291b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905427"
---
# <a name="dtn_datetimechange-notification-code"></a><span data-ttu-id="f1605-105">Código de notificación de DATETIMECHANGE de DTN \_</span><span class="sxs-lookup"><span data-stu-id="f1605-105">DTN\_DATETIMECHANGE notification code</span></span>

<span data-ttu-id="f1605-106">Se envía mediante un control de selector de fecha y hora (DTP) cada vez que se produce un cambio.</span><span class="sxs-lookup"><span data-stu-id="f1605-106">Sent by a date and time picker (DTP) control whenever a change occurs.</span></span> <span data-ttu-id="f1605-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f1605-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_DATETIMECHANGE

    lpChange = (LPNMDATETIMECHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f1605-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1605-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1605-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1605-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1605-110">Puntero a una estructura [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) que contiene información sobre el cambio que tuvo lugar en el control.</span><span class="sxs-lookup"><span data-stu-id="f1605-110">A pointer to an [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) structure containing information about the change that took place in the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1605-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1605-111">Return value</span></span>

<span data-ttu-id="f1605-112">El propietario del control debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="f1605-112">The owner of the control must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1605-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1605-113">Requirements</span></span>



| <span data-ttu-id="f1605-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1605-114">Requirement</span></span> | <span data-ttu-id="f1605-115">Value</span><span class="sxs-lookup"><span data-stu-id="f1605-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1605-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1605-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f1605-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f1605-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1605-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1605-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f1605-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f1605-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1605-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1605-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1605-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1605-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





