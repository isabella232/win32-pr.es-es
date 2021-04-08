---
description: Cancela las suscripciones de las notificaciones de cambio de estado del servicio.
ms.assetid: 8c04ebf7-4d61-4617-b120-dbe26b2f9ad2
title: Función UnsubscribeServiceChangeNotifications (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnsubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: ebecfb133172c9c7a56ed6d28f7ad6b395d8afce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911245"
---
# <a name="unsubscribeservicechangenotifications-function"></a><span data-ttu-id="0678a-103">UnsubscribeServiceChangeNotifications función)</span><span class="sxs-lookup"><span data-stu-id="0678a-103">UnsubscribeServiceChangeNotifications function</span></span>

<span data-ttu-id="0678a-104">Cancela las suscripciones de las notificaciones de cambio de estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="0678a-104">Unsubscribes from service status change notifications.</span></span> <span data-ttu-id="0678a-105">Esta función usa las suscripciones devueltas por [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md).</span><span class="sxs-lookup"><span data-stu-id="0678a-105">This function uses subscriptions returned by [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0678a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0678a-106">Syntax</span></span>


```C++
 VOID WINAPI UnsubscribeServiceChangeNotifications(
  _In_ PSC_NOTIFICATION_REGISTRATION pSubscription
);
```



## <a name="parameters"></a><span data-ttu-id="0678a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0678a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0678a-108">*pSubscription* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0678a-108">*pSubscription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0678a-109">Un puntero a la suscripción a la que se va a cancelar la suscripción.</span><span class="sxs-lookup"><span data-stu-id="0678a-109">A pointer to the subscription to be unsubscribed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0678a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0678a-110">Return value</span></span>

<span data-ttu-id="0678a-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0678a-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0678a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0678a-112">Remarks</span></span>

<span data-ttu-id="0678a-113">**UnsubscribeServiceChangeNotifications** no devuelve hasta que se completen las devoluciones de llamada en curso pendientes.</span><span class="sxs-lookup"><span data-stu-id="0678a-113">**UnsubscribeServiceChangeNotifications** does not return until outstanding in-process callbacks are complete.</span></span> <span data-ttu-id="0678a-114">Por lo tanto, no se puede llamar a **UnsubscribeServiceChangeNotifications** dentro de la devolución de llamada sin que se produzca un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="0678a-114">So, you cannot call **UnsubscribeServiceChangeNotifications** within the callback without causing a deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="0678a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0678a-115">Requirements</span></span>



| <span data-ttu-id="0678a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0678a-116">Requirement</span></span> | <span data-ttu-id="0678a-117">Value</span><span class="sxs-lookup"><span data-stu-id="0678a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0678a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0678a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0678a-119">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0678a-119">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0678a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0678a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0678a-121">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0678a-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0678a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0678a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0678a-123"><dt>Winsvcp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0678a-123"><dt>Winsvcp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0678a-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0678a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0678a-125"><dt>SecHost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0678a-125"><dt>SecHost.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0678a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0678a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0678a-127">**CreateService**</span><span class="sxs-lookup"><span data-stu-id="0678a-127">**CreateService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[<span data-ttu-id="0678a-128">**OpenService**</span><span class="sxs-lookup"><span data-stu-id="0678a-128">**OpenService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[<span data-ttu-id="0678a-129">**OpenSCManager**</span><span class="sxs-lookup"><span data-stu-id="0678a-129">**OpenSCManager**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[<span data-ttu-id="0678a-130">**SubscribeServiceChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="0678a-130">**SubscribeServiceChangeNotifications**</span></span>](subscribeservicechangenotifications.md)
</dt> <dt>

[<span data-ttu-id="0678a-131">**QueryServiceDynamicInformation**</span><span class="sxs-lookup"><span data-stu-id="0678a-131">**QueryServiceDynamicInformation**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

 




