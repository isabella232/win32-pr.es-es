---
description: El sistema difunde el \_ evento de dispositivo DBT QUERYCHANGECONFIG para solicitar permiso para cambiar la configuración actual (acoplar o desacoplar). Cualquier aplicación puede denegar esta solicitud y cancelar el cambio.
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: Evento DBT_QUERYCHANGECONFIG (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48367da1788ae2985b21fad6e960153008e9ffd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538890"
---
# <a name="dbt_querychangeconfig-event"></a><span data-ttu-id="24b2e-104">\_Evento DBT QUERYCHANGECONFIG</span><span class="sxs-lookup"><span data-stu-id="24b2e-104">DBT\_QUERYCHANGECONFIG event</span></span>

<span data-ttu-id="24b2e-105">El sistema difunde el \_ evento de dispositivo DBT QUERYCHANGECONFIG para solicitar permiso para cambiar la configuración actual (acoplar o desacoplar).</span><span class="sxs-lookup"><span data-stu-id="24b2e-105">The system broadcasts the DBT\_QUERYCHANGECONFIG device event to request permission to change the current configuration (dock or undock).</span></span> <span data-ttu-id="24b2e-106">Cualquier aplicación puede denegar esta solicitud y cancelar el cambio.</span><span class="sxs-lookup"><span data-stu-id="24b2e-106">Any application can deny this request and cancel the change.</span></span>

<span data-ttu-id="24b2e-107">Para difundir este evento de dispositivo, el sistema usa el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) con *wParam* establecido en DBT \_ QUERYCHANGECONFIG y *lParam* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="24b2e-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_QUERYCHANGECONFIG and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="24b2e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24b2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24b2e-109">*identificador*</span><span class="sxs-lookup"><span data-stu-id="24b2e-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="24b2e-110">Identificador a una ventana.</span><span class="sxs-lookup"><span data-stu-id="24b2e-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="24b2e-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="24b2e-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="24b2e-112">Identificador del mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="24b2e-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="24b2e-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24b2e-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24b2e-114">Establézcalo en DBT \_ QUERYCHANGECONFIG.</span><span class="sxs-lookup"><span data-stu-id="24b2e-114">Set to DBT\_QUERYCHANGECONFIG.</span></span>

</dd> <dt>

<span data-ttu-id="24b2e-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24b2e-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24b2e-116">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="24b2e-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24b2e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24b2e-117">Return value</span></span>

<span data-ttu-id="24b2e-118">Devuelva **true** para conceder permiso para cambiar la configuración.</span><span class="sxs-lookup"><span data-stu-id="24b2e-118">Return **TRUE** to grant permission to change the configuration.</span></span>

<span data-ttu-id="24b2e-119">Devuelve \_ la consulta \_ de difusión deny para denegar el permiso para cambiar la configuración.</span><span class="sxs-lookup"><span data-stu-id="24b2e-119">Return BROADCAST\_QUERY\_DENY to deny permission to change the configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="24b2e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24b2e-120">Requirements</span></span>



| <span data-ttu-id="24b2e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="24b2e-121">Requirement</span></span> | <span data-ttu-id="24b2e-122">Value</span><span class="sxs-lookup"><span data-stu-id="24b2e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="24b2e-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24b2e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="24b2e-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="24b2e-124">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="24b2e-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24b2e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="24b2e-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="24b2e-126">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="24b2e-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24b2e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="24b2e-128"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="24b2e-128"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24b2e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="24b2e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24b2e-130">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="24b2e-130">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="24b2e-131">Eventos de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="24b2e-131">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="24b2e-132">**DEVICECHANGE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="24b2e-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




