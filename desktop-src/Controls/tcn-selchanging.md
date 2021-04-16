---
title: Código de notificación de TCN_SELCHANGING (commctrl. h)
description: Notifica a la ventana primaria de un control de pestaña que está a punto de cambiar la pestaña seleccionada actualmente. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ec7b1bd3-8932-4418-9eed-ecb7c748e4dd
keywords:
- TCN_SELCHANGING controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TCN_SELCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6ba7dcf25d243d9b42876425564fba0e01c803f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656453"
---
# <a name="tcn_selchanging-notification-code"></a><span data-ttu-id="fcbf8-105">Código de notificación de SELCHANGING de TCN \_</span><span class="sxs-lookup"><span data-stu-id="fcbf8-105">TCN\_SELCHANGING notification code</span></span>

<span data-ttu-id="fcbf8-106">Notifica a la ventana primaria de un control de pestaña que está a punto de cambiar la pestaña seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-106">Notifies a tab control's parent window that the currently selected tab is about to change.</span></span> <span data-ttu-id="fcbf8-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fcbf8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_SELCHANGING 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fcbf8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcbf8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcbf8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fcbf8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcbf8-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcbf8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcbf8-111">Return value</span></span>

<span data-ttu-id="fcbf8-112">Devuelve **true** para evitar que la selección cambie o **false** para permitir que la selección cambie.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-112">Returns **TRUE** to prevent the selection from changing, or **FALSE** to allow the selection to change.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcbf8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcbf8-113">Remarks</span></span>

<span data-ttu-id="fcbf8-114">Para determinar la pestaña actualmente seleccionada, use la macro [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="fcbf8-114">To determine the currently selected tab, use the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcbf8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcbf8-115">Requirements</span></span>



| <span data-ttu-id="fcbf8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcbf8-116">Requirement</span></span> | <span data-ttu-id="fcbf8-117">Value</span><span class="sxs-lookup"><span data-stu-id="fcbf8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcbf8-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcbf8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fcbf8-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fcbf8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fcbf8-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcbf8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fcbf8-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fcbf8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fcbf8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fcbf8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcbf8-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcbf8-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcbf8-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcbf8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcbf8-125">TCN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="fcbf8-125">TCN\_SELCHANGE</span></span>](tcn-selchange.md)
</dt> </dl>

 

 





