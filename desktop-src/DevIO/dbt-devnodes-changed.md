---
description: El sistema difunde el \_ \_ evento de dispositivo DBT DEVNODES Changed cuando se ha agregado o quitado un dispositivo del sistema. Las aplicaciones que mantienen listas de dispositivos en el sistema deben actualizar sus listas.
ms.assetid: 62acc633-7dad-4792-a5a2-1f95356479d1
title: Evento DBT_DEVNODES_CHANGED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1450e9a87d541e5df3d9a9286e48601697e6aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153092"
---
# <a name="dbt_devnodes_changed-event"></a><span data-ttu-id="49606-104">\_Evento DBT DEVNODES \_ Changed</span><span class="sxs-lookup"><span data-stu-id="49606-104">DBT\_DEVNODES\_CHANGED event</span></span>

<span data-ttu-id="49606-105">El sistema difunde el \_ \_ evento de dispositivo DBT DEVNODES Changed cuando se ha agregado o quitado un dispositivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="49606-105">The system broadcasts the DBT\_DEVNODES\_CHANGED device event when a device has been added to or removed from the system.</span></span> <span data-ttu-id="49606-106">Las aplicaciones que mantienen listas de dispositivos en el sistema deben actualizar sus listas.</span><span class="sxs-lookup"><span data-stu-id="49606-106">Applications that maintain lists of devices in the system should refresh their lists.</span></span>

<span data-ttu-id="49606-107">Para difundir este evento de dispositivo, el sistema usa el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) con *wParam* establecido en DBT \_ DEVNODES \_ Changed y *lParam* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="49606-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVNODES\_CHANGED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="49606-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49606-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49606-109">*identificador*</span><span class="sxs-lookup"><span data-stu-id="49606-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="49606-110">Identificador a una ventana.</span><span class="sxs-lookup"><span data-stu-id="49606-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="49606-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="49606-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="49606-112">Identificador del mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="49606-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="49606-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49606-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49606-114">Se establece en DBT \_ DEVNODES \_ Changed.</span><span class="sxs-lookup"><span data-stu-id="49606-114">Set to DBT\_DEVNODES\_CHANGED.</span></span>

</dd> <dt>

<span data-ttu-id="49606-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49606-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49606-116">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="49606-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49606-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49606-117">Return value</span></span>

<span data-ttu-id="49606-118">Devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="49606-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="49606-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49606-119">Remarks</span></span>

<span data-ttu-id="49606-120">No hay información adicional sobre qué dispositivo se ha agregado o quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="49606-120">There is no additional information about which device has been added to or removed from the system.</span></span> <span data-ttu-id="49606-121">Las aplicaciones que requieren más información deben registrarse para recibir notificaciones de dispositivo mediante la función [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) .</span><span class="sxs-lookup"><span data-stu-id="49606-121">Applications that require more information should register for device notification using the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="49606-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49606-122">Requirements</span></span>



| <span data-ttu-id="49606-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="49606-123">Requirement</span></span> | <span data-ttu-id="49606-124">Value</span><span class="sxs-lookup"><span data-stu-id="49606-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="49606-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49606-125">Minimum supported client</span></span><br/> | <span data-ttu-id="49606-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="49606-126">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="49606-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49606-127">Minimum supported server</span></span><br/> | <span data-ttu-id="49606-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="49606-128">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="49606-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49606-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="49606-130"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="49606-130"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49606-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="49606-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49606-132">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="49606-132">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="49606-133">Eventos de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="49606-133">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="49606-134">**DEV \_ Broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="49606-134">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="49606-135">**DEVICECHANGE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="49606-135">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




