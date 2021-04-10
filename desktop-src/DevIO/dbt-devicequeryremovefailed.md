---
description: El sistema difunde el \_ evento de dispositivo DBT DEVICEQUERYREMOVEFAILED cuando se ha cancelado una solicitud para quitar un dispositivo o un elemento multimedia.
ms.assetid: a24916a9-b67a-4622-b9f3-4b4f26bf4d6b
title: Evento DBT_DEVICEQUERYREMOVEFAILED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848c7378cdbac95729eee70c70a1e323373b8e85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907221"
---
# <a name="dbt_devicequeryremovefailed-event"></a><span data-ttu-id="1b1a2-103">\_Evento DBT DEVICEQUERYREMOVEFAILED</span><span class="sxs-lookup"><span data-stu-id="1b1a2-103">DBT\_DEVICEQUERYREMOVEFAILED event</span></span>

<span data-ttu-id="1b1a2-104">El sistema difunde el \_ evento de dispositivo DBT DEVICEQUERYREMOVEFAILED cuando se ha cancelado una solicitud para quitar un dispositivo o un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-104">The system broadcasts the DBT\_DEVICEQUERYREMOVEFAILED device event when a request to remove a device or piece of media has been canceled.</span></span>

<span data-ttu-id="1b1a2-105">Para difundir este evento de dispositivo, el sistema usa el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) con *wParam* establecido en DBT \_ DEVICEQUERYREMOVEFAILED y *lParam* , tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEQUERYREMOVEFAILED and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="1b1a2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b1a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b1a2-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="1b1a2-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="1b1a2-108">Identificador a una ventana.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="1b1a2-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="1b1a2-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="1b1a2-110">Identificador del mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="1b1a2-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1b1a2-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b1a2-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b1a2-112">Establézcalo en DBT \_ DEVICEQUERYREMOVEFAILED.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-112">Set to DBT\_DEVICEQUERYREMOVEFAILED.</span></span>

</dd> <dt>

<span data-ttu-id="1b1a2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b1a2-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b1a2-114">Puntero a una estructura que identifica el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="1b1a2-115">La estructura consta de un encabezado independiente del evento, seguido de los miembros dependientes del evento que describen el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="1b1a2-116">Para usar esta estructura, trate la estructura como una [**estructura \_ \_ HDR de difusión de desarrollo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) y, a continuación, compruebe su miembro **dbch \_ DeviceType** para determinar el tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b1a2-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b1a2-117">Return value</span></span>

<span data-ttu-id="1b1a2-118">Devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="1b1a2-118">Return **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="1b1a2-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1b1a2-119">Examples</span></span>

<span data-ttu-id="1b1a2-120">Para ver un ejemplo, consulte [procesamiento de una solicitud para quitar un dispositivo](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="1b1a2-120">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b1a2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b1a2-121">Requirements</span></span>



| <span data-ttu-id="1b1a2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b1a2-122">Requirement</span></span> | <span data-ttu-id="1b1a2-123">Value</span><span class="sxs-lookup"><span data-stu-id="1b1a2-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1b1a2-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b1a2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1b1a2-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1b1a2-125">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="1b1a2-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b1a2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1b1a2-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1b1a2-127">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="1b1a2-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b1a2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b1a2-129"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b1a2-129"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b1a2-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b1a2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b1a2-131">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="1b1a2-131">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="1b1a2-132">Eventos de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="1b1a2-132">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="1b1a2-133">**DEV \_ Broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="1b1a2-133">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="1b1a2-134">**DEVICECHANGE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="1b1a2-134">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




