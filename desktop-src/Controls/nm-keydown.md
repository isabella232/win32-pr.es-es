---
title: NM_KEYDOWN de notificación (Commctrl.h)
description: 'NM_KEYDOWN de notificación: enviado por un control cuando el control tiene el foco del teclado y el usuario presiona una tecla. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.'
ms.assetid: e3b38096-797d-4948-9595-a252cf33dcdd
keywords:
- NM_KEYDOWN código de notificación controles de Windows
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce595378995e41fd8a0f481d7470c8cf791f6379
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112353"
---
# <a name="nm_keydown-notification-code"></a><span data-ttu-id="5da08-105">Código \_ de notificación NM KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="5da08-105">NM\_KEYDOWN notification code</span></span>

<span data-ttu-id="5da08-106">Lo envía un control cuando el control tiene el foco del teclado y el usuario presiona una tecla.</span><span class="sxs-lookup"><span data-stu-id="5da08-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="5da08-107">Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="5da08-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5da08-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5da08-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5da08-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5da08-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5da08-110">Puntero a una estructura [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) que contiene información adicional sobre la clave que produjo el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="5da08-110">A pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5da08-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5da08-111">Return value</span></span>

<span data-ttu-id="5da08-112">Devuelve un valor distinto de cero para evitar que el control procese la clave, o bien cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5da08-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5da08-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5da08-113">Requirements</span></span>



| <span data-ttu-id="5da08-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5da08-114">Requirement</span></span> | <span data-ttu-id="5da08-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5da08-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5da08-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5da08-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5da08-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5da08-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5da08-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5da08-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5da08-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5da08-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5da08-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5da08-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5da08-121"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="5da08-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





