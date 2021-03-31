---
description: El sistema envía el \_ evento de dispositivo DBT CUSTOMEVENT cuando se ha producido un evento personalizado definido por el controlador.
ms.assetid: 6e66fa93-0cd7-4202-83eb-cddc668525ae
title: Evento DBT_CUSTOMEVENT (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777049a0a94b16450ed9ee8567f3fc6506e47174
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807423"
---
# <a name="dbt_customevent-event"></a><span data-ttu-id="4cae7-103">\_Evento DBT CUSTOMEVENT</span><span class="sxs-lookup"><span data-stu-id="4cae7-103">DBT\_CUSTOMEVENT event</span></span>

<span data-ttu-id="4cae7-104">El sistema envía el \_ evento de dispositivo DBT CUSTOMEVENT cuando se ha producido un evento personalizado definido por el controlador.</span><span class="sxs-lookup"><span data-stu-id="4cae7-104">The system sends the DBT\_CUSTOMEVENT device event when a driver-defined custom event has occurred.</span></span>

<span data-ttu-id="4cae7-105">Para difundir este evento de dispositivo, el sistema usa el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) con *wParam* establecido en DBT \_ CUSTOMEVENT y *lParam* , tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="4cae7-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CUSTOMEVENT and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="4cae7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4cae7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cae7-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="4cae7-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="4cae7-108">Identificador a una ventana.</span><span class="sxs-lookup"><span data-stu-id="4cae7-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="4cae7-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="4cae7-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="4cae7-110">Identificador del mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="4cae7-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="4cae7-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4cae7-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cae7-112">Establézcalo en DBT \_ CUSTOMEVENT.</span><span class="sxs-lookup"><span data-stu-id="4cae7-112">Set to DBT\_CUSTOMEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="4cae7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4cae7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cae7-114">Puntero a una estructura que identifica el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4cae7-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="4cae7-115">La estructura consta de un encabezado independiente del evento, seguido de los miembros dependientes del evento que describen el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4cae7-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="4cae7-116">Para usar esta estructura, trate la estructura como una [**estructura \_ \_ HDR de difusión de desarrollo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) y, a continuación, compruebe su miembro **dbch \_ DeviceType** para determinar el tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4cae7-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cae7-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4cae7-117">Return value</span></span>

<span data-ttu-id="4cae7-118">Devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="4cae7-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cae7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cae7-119">Requirements</span></span>



| <span data-ttu-id="4cae7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cae7-120">Requirement</span></span> | <span data-ttu-id="4cae7-121">Value</span><span class="sxs-lookup"><span data-stu-id="4cae7-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4cae7-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cae7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4cae7-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4cae7-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="4cae7-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cae7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4cae7-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4cae7-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="4cae7-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4cae7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cae7-127"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cae7-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cae7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cae7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cae7-129">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="4cae7-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="4cae7-130">Eventos de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="4cae7-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="4cae7-131">**DEV \_ Broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="4cae7-131">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="4cae7-132">**DEVICECHANGE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="4cae7-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




