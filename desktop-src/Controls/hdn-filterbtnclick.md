---
title: Código de notificación de HDN_FILTERBTNCLICK (commctrl. h)
description: Notifica a la ventana primaria del control de encabezado cuando se hace clic en el botón de filtro o en respuesta a un \_ mensaje SETITEM de HDM. Este código de notificación se envía en forma de mensaje de notificación de WM \_ .
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- HDN_FILTERBTNCLICK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_FILTERBTNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dbbdab8adf0bee400d591f3d8b4cec6fa1ea81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905033"
---
# <a name="hdn_filterbtnclick-notification-code"></a><span data-ttu-id="09854-105">Código de notificación de FILTERBTNCLICK de HDN \_</span><span class="sxs-lookup"><span data-stu-id="09854-105">HDN\_FILTERBTNCLICK notification code</span></span>

<span data-ttu-id="09854-106">Notifica a la ventana primaria del control de encabezado cuando se hace clic en el botón de filtro o en respuesta a un mensaje [**\_ SETITEM de HDM**](hdm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="09854-106">Notifies the header control's parent window when the filter button is clicked or in response to an [**HDM\_SETITEM**](hdm-setitem.md) message.</span></span> <span data-ttu-id="09854-107">Este código de notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="09854-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_FILTERBTNCLICK

    pNMHDFilterBtnClk = (LPNMHDFILTERBTNCLICK) lParam;
```



## <a name="parameters"></a><span data-ttu-id="09854-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09854-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09854-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09854-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09854-110">Puntero a una estructura [**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) que contiene información sobre el control de encabezado y el botón de filtro de encabezado.</span><span class="sxs-lookup"><span data-stu-id="09854-110">A pointer to an [**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) structure that contains information about the header control and the header filter button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09854-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09854-111">Return value</span></span>

<span data-ttu-id="09854-112">Si devuelve **true**, se enviará un código de notificación [HDN \_ FILTERCHANGE](hdn-filterchange.md) a la ventana primaria del control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="09854-112">If you return **TRUE**, an [HDN\_FILTERCHANGE](hdn-filterchange.md) notification code will be sent to the header control's parent window.</span></span> <span data-ttu-id="09854-113">Este código de notificación proporciona a la ventana primaria una oportunidad para sincronizar sus elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="09854-113">This notification code gives the parent window an opportunity to synchronize its user interface elements.</span></span> <span data-ttu-id="09854-114">Devuelve **false** si no desea que se envíe la notificación.</span><span class="sxs-lookup"><span data-stu-id="09854-114">Return **FALSE** if you do not want the notification sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="09854-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09854-115">Requirements</span></span>



| <span data-ttu-id="09854-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="09854-116">Requirement</span></span> | <span data-ttu-id="09854-117">Value</span><span class="sxs-lookup"><span data-stu-id="09854-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09854-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09854-118">Minimum supported client</span></span><br/> | <span data-ttu-id="09854-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="09854-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09854-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09854-120">Minimum supported server</span></span><br/> | <span data-ttu-id="09854-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="09854-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09854-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09854-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="09854-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="09854-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09854-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="09854-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09854-125">**NMHDFILTERBTNCLICK**</span><span class="sxs-lookup"><span data-stu-id="09854-125">**NMHDFILTERBTNCLICK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





