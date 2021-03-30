---
title: Código de notificación de TCN_SELCHANGE (commctrl. h)
description: Notifica a la ventana primaria de un control de pestaña que la pestaña seleccionada actualmente ha cambiado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: f40e30f6-169b-4381-a300-12c3befb5fc5
keywords:
- TCN_SELCHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8578ac9fee7754b1ae27c05c6ec1b15636090040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801046"
---
# <a name="tcn_selchange-notification-code"></a><span data-ttu-id="040b8-105">Código de notificación de SELCHANGE de TCN \_</span><span class="sxs-lookup"><span data-stu-id="040b8-105">TCN\_SELCHANGE notification code</span></span>

<span data-ttu-id="040b8-106">Notifica a la ventana primaria de un control de pestaña que la pestaña seleccionada actualmente ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="040b8-106">Notifies a tab control's parent window that the currently selected tab has changed.</span></span> <span data-ttu-id="040b8-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="040b8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_SELCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="040b8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="040b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="040b8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="040b8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="040b8-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="040b8-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="040b8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="040b8-111">Return value</span></span>

<span data-ttu-id="040b8-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="040b8-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="040b8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="040b8-113">Remarks</span></span>

<span data-ttu-id="040b8-114">Para determinar la pestaña actualmente seleccionada, use la macro [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="040b8-114">To determine the currently selected tab, use the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="040b8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="040b8-115">Requirements</span></span>



| <span data-ttu-id="040b8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="040b8-116">Requirement</span></span> | <span data-ttu-id="040b8-117">Value</span><span class="sxs-lookup"><span data-stu-id="040b8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="040b8-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="040b8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="040b8-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="040b8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="040b8-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="040b8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="040b8-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="040b8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="040b8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="040b8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="040b8-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="040b8-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="040b8-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="040b8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="040b8-125">TCN \_ SELCHANGING</span><span class="sxs-lookup"><span data-stu-id="040b8-125">TCN\_SELCHANGING</span></span>](tcn-selchanging.md)
</dt> </dl>

 

 





