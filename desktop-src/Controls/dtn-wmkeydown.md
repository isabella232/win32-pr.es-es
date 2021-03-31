---
title: Código de notificación de DTN_WMKEYDOWN (commctrl. h)
description: Se envía mediante un control de selector de fecha y hora (DTP) cuando el usuario escribe en un campo de devolución de llamada. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- DTN_WMKEYDOWN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- DTN_WMKEYDOWN
- DTN_WMKEYDOWNA
- DTN_WMKEYDOWNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce2e7d0761308805746278d2f542f5e9458b56d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149984"
---
# <a name="dtn_wmkeydown-notification-code"></a><span data-ttu-id="e7329-105">Código de notificación de WMKEYDOWN de DTN \_</span><span class="sxs-lookup"><span data-stu-id="e7329-105">DTN\_WMKEYDOWN notification code</span></span>

<span data-ttu-id="e7329-106">Se envía mediante un control de selector de fecha y hora (DTP) cuando el usuario escribe en un campo de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="e7329-106">Sent by a date and time picker (DTP) control when the user types in a callback field.</span></span> <span data-ttu-id="e7329-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e7329-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_WMKEYDOWN

    lpDTKeystroke = (LPNMDATETIMEWMKEYDOWN)lParam;
```



## <a name="parameters"></a><span data-ttu-id="e7329-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7329-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7329-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7329-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7329-110">Puntero a una estructura [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) que contiene información sobre esta instancia del código de notificación.</span><span class="sxs-lookup"><span data-stu-id="e7329-110">A pointer to an [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) structure containing information about this instance of the notification code.</span></span> <span data-ttu-id="e7329-111">La estructura incluye información sobre la clave que el usuario ha escrito, la subcadena que define el campo de devolución de llamada y la fecha y hora actuales del sistema.</span><span class="sxs-lookup"><span data-stu-id="e7329-111">The structure includes information about the key that the user typed, the substring that defines the callback field, and the current system date and time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7329-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7329-112">Return value</span></span>

<span data-ttu-id="e7329-113">El propietario del control debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="e7329-113">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7329-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7329-114">Remarks</span></span>

<span data-ttu-id="e7329-115">El control de este código de notificación permite que el propietario del control proporcione respuestas específicas a las pulsaciones de teclas dentro de los campos de devolución de llamada del control.</span><span class="sxs-lookup"><span data-stu-id="e7329-115">Handling this notification code allows the owner of the control to provide specific responses to keystrokes within the callback fields of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7329-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7329-116">Requirements</span></span>



| <span data-ttu-id="e7329-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7329-117">Requirement</span></span> | <span data-ttu-id="e7329-118">Value</span><span class="sxs-lookup"><span data-stu-id="e7329-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7329-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7329-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e7329-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e7329-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7329-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7329-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e7329-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7329-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7329-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7329-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7329-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7329-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e7329-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="e7329-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e7329-126">**DTN \_ WMKEYDOWNW** (Unicode) y **DTN \_ WMKEYDOWNA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e7329-126">**DTN\_WMKEYDOWNW** (Unicode) and **DTN\_WMKEYDOWNA** (ANSI)</span></span><br/>               |



 

 





