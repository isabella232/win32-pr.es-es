---
title: Código de notificación de NM_TOOLTIPSCREATED (commctrl. h)
description: Notifica a la ventana primaria de un control que el control ha creado un control ToolTip. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 8108f084-212d-4a16-b604-1ec134b1bb43
keywords:
- NM_TOOLTIPSCREATED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e2e99850b17b0f2b06948a09b70a89e67e65a50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079199"
---
# <a name="nm_tooltipscreated-notification-code"></a><span data-ttu-id="61db3-105">Código de notificación de NM \_ TOOLTIPSCREATED</span><span class="sxs-lookup"><span data-stu-id="61db3-105">NM\_TOOLTIPSCREATED notification code</span></span>

<span data-ttu-id="61db3-106">Notifica a la ventana primaria de un control que el control ha creado un control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="61db3-106">Notifies a control's parent window that the control has created a tooltip control.</span></span> <span data-ttu-id="61db3-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="61db3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="61db3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61db3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61db3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61db3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61db3-110">Puntero a una estructura [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="61db3-110">A pointer to an [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61db3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61db3-111">Return value</span></span>

<span data-ttu-id="61db3-112">A menos que se especifique lo contrario, el control omite el valor devuelto de este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="61db3-112">Unless otherwise specified, the control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="61db3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61db3-113">Requirements</span></span>



| <span data-ttu-id="61db3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="61db3-114">Requirement</span></span> | <span data-ttu-id="61db3-115">Value</span><span class="sxs-lookup"><span data-stu-id="61db3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61db3-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61db3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61db3-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="61db3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61db3-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61db3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61db3-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="61db3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61db3-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61db3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="61db3-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="61db3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





