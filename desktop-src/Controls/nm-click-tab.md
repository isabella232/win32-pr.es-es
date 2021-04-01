---
title: Código de notificación de NM_CLICK (pestaña) (commctrl. h)
description: Notifica a la ventana primaria de un control de pestaña que el usuario ha haga clic en el botón primario del mouse dentro del control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: b892aded-d6b8-4a04-bfdd-0153b65eaccc
keywords:
- Controles de Windows de código de notificación de NM_CLICK (pestaña)
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e451a7a87d1b02140f59797c7485b8eb250dad13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151272"
---
# <a name="nm_click-tab-notification-code"></a><span data-ttu-id="a8bd1-105">NM \_ código de notificación de clic (pestaña)</span><span class="sxs-lookup"><span data-stu-id="a8bd1-105">NM\_CLICK (tab) notification code</span></span>

<span data-ttu-id="a8bd1-106">Notifica a la ventana primaria de un control de pestaña que el usuario ha haga clic en el botón primario del mouse dentro del control.</span><span class="sxs-lookup"><span data-stu-id="a8bd1-106">Notifies the parent window of a tab control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="a8bd1-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a8bd1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a8bd1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8bd1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8bd1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8bd1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8bd1-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="a8bd1-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8bd1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8bd1-111">Return value</span></span>

<span data-ttu-id="a8bd1-112">El control de pestaña omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="a8bd1-112">The return value is ignored by the tab control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8bd1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8bd1-113">Requirements</span></span>



| <span data-ttu-id="a8bd1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8bd1-114">Requirement</span></span> | <span data-ttu-id="a8bd1-115">Value</span><span class="sxs-lookup"><span data-stu-id="a8bd1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bd1-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8bd1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a8bd1-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a8bd1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8bd1-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8bd1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a8bd1-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8bd1-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8bd1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8bd1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8bd1-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8bd1-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





