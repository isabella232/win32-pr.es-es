---
description: El sistema difunde el \_ evento de dispositivo DBT DEVICEREMOVEPENDING cuando se está quitando un dispositivo o un elemento multimedia y ya no está disponible para su uso.
ms.assetid: 28cb4481-8961-4896-9608-afccba9a2bfe
title: Evento DBT_DEVICEREMOVEPENDING (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421851dc46d905ae85941b92df6649ccb504ee50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153093"
---
# <a name="dbt_deviceremovepending-event"></a><span data-ttu-id="1b644-103">\_Evento DBT DEVICEREMOVEPENDING</span><span class="sxs-lookup"><span data-stu-id="1b644-103">DBT\_DEVICEREMOVEPENDING event</span></span>

<span data-ttu-id="1b644-104">El sistema difunde el \_ evento de dispositivo DBT DEVICEREMOVEPENDING cuando se está quitando un dispositivo o un elemento multimedia y ya no está disponible para su uso.</span><span class="sxs-lookup"><span data-stu-id="1b644-104">The system broadcasts the DBT\_DEVICEREMOVEPENDING device event when a device or piece of media is being removed and is no longer available for use.</span></span>

<span data-ttu-id="1b644-105">Para difundir este evento de dispositivo, el sistema usa el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) con *wParam* establecido en DBT \_ DEVICEREMOVEPENDING y *lParam* , tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="1b644-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEREMOVEPENDING and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="1b644-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b644-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b644-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="1b644-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="1b644-108">Identificador a una ventana.</span><span class="sxs-lookup"><span data-stu-id="1b644-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="1b644-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="1b644-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="1b644-110">Identificador del mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="1b644-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1b644-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b644-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b644-112">Establézcalo en DBT \_ DEVICEREMOVEPENDING.</span><span class="sxs-lookup"><span data-stu-id="1b644-112">Set to DBT\_DEVICEREMOVEPENDING.</span></span>

</dd> <dt>

<span data-ttu-id="1b644-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b644-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b644-114">Puntero a una estructura que identifica el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b644-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="1b644-115">La estructura consta de un encabezado independiente del evento, seguido de los miembros dependientes del evento que describen el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b644-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="1b644-116">Para usar esta estructura, trate la estructura como una [**estructura \_ \_ HDR de difusión de desarrollo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) y, a continuación, compruebe su miembro **dbch \_ DeviceType** para determinar el tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b644-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b644-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b644-117">Return value</span></span>

<span data-ttu-id="1b644-118">Devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="1b644-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b644-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b644-119">Remarks</span></span>

<span data-ttu-id="1b644-120">El sistema puede difundir un mensaje de DEVICEREMOVEPENDING de DBT \_ sin enviar un mensaje de [ \_ DEVICEQUERYREMOVE de DBT](dbt-devicequeryremove.md) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1b644-120">The system may broadcast a DBT\_DEVICEREMOVEPENDING message without sending a corresponding [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message.</span></span> <span data-ttu-id="1b644-121">En tales casos, las aplicaciones y los controladores deben recuperarse de la pérdida del dispositivo lo mejor posible.</span><span class="sxs-lookup"><span data-stu-id="1b644-121">In such cases, the applications and drivers must recover from the loss of the device as best they can.</span></span>

## <a name="examples"></a><span data-ttu-id="1b644-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1b644-122">Examples</span></span>

<span data-ttu-id="1b644-123">Para ver un ejemplo, consulte [procesamiento de una solicitud para quitar un dispositivo](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="1b644-123">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b644-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b644-124">Requirements</span></span>



| <span data-ttu-id="1b644-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b644-125">Requirement</span></span> | <span data-ttu-id="1b644-126">Value</span><span class="sxs-lookup"><span data-stu-id="1b644-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1b644-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b644-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1b644-128">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1b644-128">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="1b644-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b644-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1b644-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1b644-130">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="1b644-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b644-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b644-132"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b644-132"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b644-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b644-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b644-134">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="1b644-134">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="1b644-135">Eventos de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="1b644-135">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="1b644-136">**DEV \_ Broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="1b644-136">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="1b644-137">**DEVICECHANGE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="1b644-137">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




