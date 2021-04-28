---
title: NM_KEYDOWN de notificación (barra de herramientas) (Commctrl.h)
description: 'NM_KEYDOWN (barra de herramientas): se envía mediante un control cuando el control tiene el foco del teclado y el usuario presiona una tecla. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.'
ms.assetid: bdfcf9da-118b-4fe6-9a0a-6329eb9196ef
keywords:
- NM_KEYDOWN de notificación (barra de herramientas) Controles de Windows
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
ms.openlocfilehash: 1d53818cf417e1efac686e94d3b4ef5919f819ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112363"
---
# <a name="nm_keydown-toolbar-notification-code"></a><span data-ttu-id="e2f25-105">Código de \_ notificación NM KEYDOWN (barra de herramientas)</span><span class="sxs-lookup"><span data-stu-id="e2f25-105">NM\_KEYDOWN (toolbar) notification code</span></span>

<span data-ttu-id="e2f25-106">Lo envía un control cuando el control tiene el foco del teclado y el usuario presiona una tecla.</span><span class="sxs-lookup"><span data-stu-id="e2f25-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="e2f25-107">Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="e2f25-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e2f25-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2f25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f25-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2f25-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2f25-110">Puntero a una [**estructura NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) que contiene información adicional sobre la clave que provocó el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="e2f25-110">Pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2f25-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2f25-111">Return value</span></span>

<span data-ttu-id="e2f25-112">Devuelve un valor distinto de cero para evitar que el control procese la clave o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e2f25-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2f25-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2f25-113">Remarks</span></span>

<span data-ttu-id="e2f25-114">Actualmente, solo el control de barra de herramientas envía este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="e2f25-114">Currently, only the toolbar control sends this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f25-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2f25-115">Requirements</span></span>



| <span data-ttu-id="e2f25-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2f25-116">Requirement</span></span> | <span data-ttu-id="e2f25-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e2f25-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f25-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2f25-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e2f25-119">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2f25-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2f25-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2f25-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e2f25-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2f25-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2f25-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2f25-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2f25-123"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="e2f25-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





