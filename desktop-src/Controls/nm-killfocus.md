---
title: Código de notificación de NM_KILLFOCUS (commctrl. h)
description: Notifica a la ventana primaria de un control que el control ha perdido el foco de entrada. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: d7538697-8b4c-4bbd-8b06-02cbc8069a22
keywords:
- NM_KILLFOCUS controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 873af3315dd58a12a61249ca59a317ca5af4b105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149891"
---
# <a name="nm_killfocus-notification-code"></a><span data-ttu-id="2064a-105">Código de notificación de NM \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="2064a-105">NM\_KILLFOCUS notification code</span></span>

<span data-ttu-id="2064a-106">Notifica a la ventana primaria de un control que el control ha perdido el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="2064a-106">Notifies a control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="2064a-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2064a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2064a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2064a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2064a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2064a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2064a-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="2064a-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2064a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2064a-111">Return value</span></span>

<span data-ttu-id="2064a-112">El control omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="2064a-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="2064a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2064a-113">Requirements</span></span>



| <span data-ttu-id="2064a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2064a-114">Requirement</span></span> | <span data-ttu-id="2064a-115">Value</span><span class="sxs-lookup"><span data-stu-id="2064a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2064a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2064a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2064a-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2064a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2064a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2064a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2064a-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2064a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2064a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2064a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2064a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2064a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





