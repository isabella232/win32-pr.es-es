---
title: Código de notificación de NM_SETFOCUS (fecha y hora) (commctrl. h)
description: Notifica a la ventana primaria de un control de fecha y hora que el control ha recibido el foco de entrada. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 61c62fb2-bc79-404b-9958-7208d1c781fa
keywords:
- NM_SETFOCUS (fecha y hora) controles de Windows de código de notificación
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba80ea119056c131f1dd94cdf1f39a84371b7052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489959"
---
# <a name="nm_setfocus-date-time-notification-code"></a><span data-ttu-id="8cf1b-105">NM \_ código de notificación de SETFOCUS (fecha y hora)</span><span class="sxs-lookup"><span data-stu-id="8cf1b-105">NM\_SETFOCUS (date time) notification code</span></span>

<span data-ttu-id="8cf1b-106">Notifica a la ventana primaria de un control de fecha y hora que el control ha recibido el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="8cf1b-106">Notifies a date and time picker control's parent window that the control has received the input focus.</span></span> <span data-ttu-id="8cf1b-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8cf1b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8cf1b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8cf1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cf1b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8cf1b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8cf1b-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="8cf1b-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cf1b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8cf1b-111">Return value</span></span>

<span data-ttu-id="8cf1b-112">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="8cf1b-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cf1b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cf1b-113">Requirements</span></span>



| <span data-ttu-id="8cf1b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cf1b-114">Requirement</span></span> | <span data-ttu-id="8cf1b-115">Value</span><span class="sxs-lookup"><span data-stu-id="8cf1b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf1b-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8cf1b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8cf1b-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8cf1b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8cf1b-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8cf1b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8cf1b-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8cf1b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8cf1b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8cf1b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cf1b-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cf1b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





