---
title: Código de notificación de NM_RELEASEDCAPTURE (monthcal) (commctrl. h)
description: Notifica a la ventana primaria de un control monthcal que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: c05d3331-26f3-41f4-8032-36ed38d47917
keywords:
- Controles de Windows de código de notificación de NM_RELEASEDCAPTURE (monthcal)
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
ms.openlocfilehash: 0b9c743a076c8046aa57ba4306145248ed00f0fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801088"
---
# <a name="nm_releasedcapture-monthcal-notification-code"></a><span data-ttu-id="afd2b-105">Código de notificación de NM \_ RELEASEDCAPTURE (monthcal)</span><span class="sxs-lookup"><span data-stu-id="afd2b-105">NM\_RELEASEDCAPTURE (monthcal) notification code</span></span>

<span data-ttu-id="afd2b-106">Notifica a la ventana primaria de un control monthcal que el control está liberando la captura del mouse.</span><span class="sxs-lookup"><span data-stu-id="afd2b-106">Notifies a monthcal control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="afd2b-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="afd2b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="afd2b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afd2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afd2b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="afd2b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afd2b-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="afd2b-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afd2b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afd2b-111">Return value</span></span>

<span data-ttu-id="afd2b-112">El control omite el valor devuelto de este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="afd2b-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="afd2b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afd2b-113">Requirements</span></span>



| <span data-ttu-id="afd2b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="afd2b-114">Requirement</span></span> | <span data-ttu-id="afd2b-115">Value</span><span class="sxs-lookup"><span data-stu-id="afd2b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="afd2b-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afd2b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="afd2b-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="afd2b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="afd2b-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afd2b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="afd2b-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="afd2b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="afd2b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afd2b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="afd2b-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="afd2b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





