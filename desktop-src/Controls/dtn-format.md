---
title: Código de notificación de DTN_FORMAT (commctrl. h)
description: Enviado por un control de selector de fecha y hora (DTP) para solicitar el texto que se va a mostrar en un campo de devolución de llamada. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ce0ee230-638e-425f-9f34-c379342cea93
keywords:
- DTN_FORMAT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- DTN_FORMAT
- DTN_FORMATA
- DTN_FORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fadd11b090777d2226eeed85f32d2062e8340e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491525"
---
# <a name="dtn_format-notification-code"></a><span data-ttu-id="7dc83-105">\_Código de notificación de formato DTN</span><span class="sxs-lookup"><span data-stu-id="7dc83-105">DTN\_FORMAT notification code</span></span>

<span data-ttu-id="7dc83-106">Enviado por un control de selector de fecha y hora (DTP) para solicitar el texto que se va a mostrar en un campo de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="7dc83-106">Sent by a date and time picker (DTP) control to request text to be displayed in a callback field.</span></span> <span data-ttu-id="7dc83-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7dc83-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_FORMAT

    lpNMFormat = (LPNMDATETIMEFORMAT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7dc83-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7dc83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dc83-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7dc83-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7dc83-110">Puntero a una estructura [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) que contiene información sobre esta instancia del código de notificación.</span><span class="sxs-lookup"><span data-stu-id="7dc83-110">A pointer to an [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) structure containing information regarding this instance of the notification code.</span></span> <span data-ttu-id="7dc83-111">La estructura contiene la subcadena que define el campo de devolución de llamada y recibe la cadena con formato que el control mostrará.</span><span class="sxs-lookup"><span data-stu-id="7dc83-111">The structure contains the substring that defines the callback field and receives the formatted string that the control will display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dc83-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7dc83-112">Return value</span></span>

<span data-ttu-id="7dc83-113">El propietario del control debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="7dc83-113">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dc83-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7dc83-114">Remarks</span></span>

<span data-ttu-id="7dc83-115">El control de este código de notificación permite que el propietario del control proporcione una cadena personalizada que mostrará el control.</span><span class="sxs-lookup"><span data-stu-id="7dc83-115">Handling this notification code allows the owner of the control to provide a custom string that the control will display.</span></span> <span data-ttu-id="7dc83-116">(Para obtener más información sobre los campos de devolución de llamada, vea [campos de devolución de llamada](date-and-time-picker-controls.md)).</span><span class="sxs-lookup"><span data-stu-id="7dc83-116">(For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="7dc83-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7dc83-117">Requirements</span></span>



| <span data-ttu-id="7dc83-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dc83-118">Requirement</span></span> | <span data-ttu-id="7dc83-119">Value</span><span class="sxs-lookup"><span data-stu-id="7dc83-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc83-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7dc83-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7dc83-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7dc83-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7dc83-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7dc83-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7dc83-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7dc83-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7dc83-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7dc83-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dc83-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dc83-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7dc83-126">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="7dc83-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7dc83-127">**DTN \_ FORMATW** (Unicode) y **DTN \_ formata** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7dc83-127">**DTN\_FORMATW** (Unicode) and **DTN\_FORMATA** (ANSI)</span></span><br/>                     |



 

 





