---
title: Código de notificación de NM_RELEASEDCAPTURE (arriba) (commctrl. h)
description: Notifica a la ventana primaria de un control de flechas que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 88a4a9a2-ba7f-4ccc-b5bf-749f49dc666b
keywords:
- NM_RELEASEDCAPTURE de código de notificación (arriba) controles de Windows
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b94f2a61727861cbf47720a41c7255763992b54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658295"
---
# <a name="nm_releasedcapture-up-down-notification-code"></a><span data-ttu-id="fde5c-105">NM \_ RELEASEDCAPTURE (arriba-abajo) código de notificación</span><span class="sxs-lookup"><span data-stu-id="fde5c-105">NM\_RELEASEDCAPTURE (up-down) notification code</span></span>

<span data-ttu-id="fde5c-106">Notifica a la ventana primaria de un control de flechas que el control está liberando la captura del mouse.</span><span class="sxs-lookup"><span data-stu-id="fde5c-106">Notifies an up-down control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="fde5c-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fde5c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fde5c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fde5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fde5c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fde5c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fde5c-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="fde5c-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fde5c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fde5c-111">Return value</span></span>

<span data-ttu-id="fde5c-112">El control omite el valor devuelto de este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="fde5c-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fde5c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fde5c-113">Requirements</span></span>



| <span data-ttu-id="fde5c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fde5c-114">Requirement</span></span> | <span data-ttu-id="fde5c-115">Value</span><span class="sxs-lookup"><span data-stu-id="fde5c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fde5c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fde5c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fde5c-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fde5c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fde5c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fde5c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fde5c-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fde5c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fde5c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fde5c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fde5c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fde5c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





