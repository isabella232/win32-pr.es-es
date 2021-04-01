---
title: Código de notificación de MCN_GETDAYSTATE (commctrl. h)
description: Enviado por un control de calendario mensual para solicitar información acerca de cómo deben mostrarse los días individuales. Este código de notificación solo se envía por los controles de calendario mensual que usan el \_ estilo MCS DAYSTATE y se envía en forma de un mensaje de notificación de WM \_ .
ms.assetid: dc2608e0-c598-4b26-9195-208f09cd84b7
keywords:
- MCN_GETDAYSTATE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- MCN_GETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff81b9f171884f39063c517cb17299a55b4053b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802419"
---
# <a name="mcn_getdaystate-notification-code"></a><span data-ttu-id="6f99d-105">Código de notificación de GETDAYSTATE de MCN \_</span><span class="sxs-lookup"><span data-stu-id="6f99d-105">MCN\_GETDAYSTATE notification code</span></span>

<span data-ttu-id="6f99d-106">Enviado por un control de calendario mensual para solicitar información acerca de cómo deben mostrarse los días individuales.</span><span class="sxs-lookup"><span data-stu-id="6f99d-106">Sent by a month calendar control to request information about how individual days should be displayed.</span></span> <span data-ttu-id="6f99d-107">Este código de notificación solo se envía por los controles de calendario mensual que usan el estilo [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) y se envía en forma de un mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6f99d-107">This notification code is sent only by month calendar controls that use the [**MCS\_DAYSTATE**](month-calendar-control-styles.md) style, and it is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_GETDAYSTATE

    lpNMDayState = (LPNMDAYSTATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6f99d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f99d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f99d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f99d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f99d-110">Puntero a una estructura [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) .</span><span class="sxs-lookup"><span data-stu-id="6f99d-110">Pointer to an [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) structure.</span></span> <span data-ttu-id="6f99d-111">La estructura contiene información sobre el período de tiempo para el que el control necesita información y recibe la dirección de una matriz que proporciona estos datos.</span><span class="sxs-lookup"><span data-stu-id="6f99d-111">The structure contains information about the time frame for which the control needs information, and it receives the address of an array that provides this data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f99d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f99d-112">Return value</span></span>

<span data-ttu-id="6f99d-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6f99d-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f99d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f99d-114">Remarks</span></span>

<span data-ttu-id="6f99d-115">El control de este código de notificación permite que la aplicación Personalice su presentación especificando que determinados días se muestran en negrita.</span><span class="sxs-lookup"><span data-stu-id="6f99d-115">Handling this notification code allows your application to customize its display by specifying that certain days be displayed in bold.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f99d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f99d-116">Requirements</span></span>



| <span data-ttu-id="6f99d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f99d-117">Requirement</span></span> | <span data-ttu-id="6f99d-118">Value</span><span class="sxs-lookup"><span data-stu-id="6f99d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f99d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f99d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6f99d-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6f99d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f99d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f99d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6f99d-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f99d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f99d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f99d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f99d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f99d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





