---
description: El sistema difunde el \_ evento de dispositivo DBT DEVICEREMOVECOMPLETE cuando se ha quitado físicamente un dispositivo o un elemento multimedia.
ms.assetid: e25d35b9-f8f1-4850-996c-e1cb393cca66
title: Evento DBT_DEVICEREMOVECOMPLETE (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c899d8cee4a0be34829ba0a8edbaf27be71f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659543"
---
# <a name="dbt_deviceremovecomplete-event"></a><span data-ttu-id="0411a-103">\_Evento DBT DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="0411a-103">DBT\_DEVICEREMOVECOMPLETE event</span></span>

<span data-ttu-id="0411a-104">El sistema difunde el \_ evento de dispositivo DBT DEVICEREMOVECOMPLETE cuando se ha quitado físicamente un dispositivo o un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="0411a-104">The system broadcasts the DBT\_DEVICEREMOVECOMPLETE device event when a device or piece of media has been physically removed.</span></span>

<span data-ttu-id="0411a-105">Para difundir este evento de dispositivo, el sistema usa el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) con *wParam* establecido en DBT \_ DEVICEREMOVECOMPLETE y *lParam* , tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="0411a-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEREMOVECOMPLETE and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="0411a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0411a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0411a-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="0411a-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="0411a-108">Identificador a una ventana.</span><span class="sxs-lookup"><span data-stu-id="0411a-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="0411a-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="0411a-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="0411a-110">Identificador del mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="0411a-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0411a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0411a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0411a-112">Establecer en DBT \_ DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="0411a-112">Set to DBT\_DEVICEREMOVECOMPLETE</span></span>

</dd> <dt>

<span data-ttu-id="0411a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0411a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0411a-114">Puntero a una estructura que identifica el dispositivo que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="0411a-114">A pointer to a structure identifying the device removed.</span></span> <span data-ttu-id="0411a-115">La estructura consta de un encabezado independiente del evento, seguido de los miembros dependientes del evento que describen el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0411a-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="0411a-116">Para usar esta estructura, trate la estructura como una [**estructura \_ \_ HDR de difusión de desarrollo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) y, a continuación, compruebe su miembro **dbch \_ DeviceType** para determinar el tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0411a-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0411a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0411a-117">Return value</span></span>

<span data-ttu-id="0411a-118">Devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="0411a-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0411a-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0411a-119">Remarks</span></span>

<span data-ttu-id="0411a-120">El sistema puede difundir un mensaje de DEVICEREMOVECOMPLETE de DBT \_ sin enviar mensajes [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) y [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) correspondientes.</span><span class="sxs-lookup"><span data-stu-id="0411a-120">The system may broadcast a DBT\_DEVICEREMOVECOMPLETE message without sending corresponding [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) and [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) messages.</span></span> <span data-ttu-id="0411a-121">En tales casos, las aplicaciones y los controladores deben recuperarse de la pérdida del dispositivo lo mejor posible.</span><span class="sxs-lookup"><span data-stu-id="0411a-121">In such cases, the applications and drivers must recover from the loss of the device as best they can.</span></span>

<span data-ttu-id="0411a-122">Si se quita un medio, el tipo de dispositivo que llega a él es un volumen (el miembro **dbch \_ DEVICETYPE** es DBT \_ DEVTYP \_ ) y el cambio afecta a los medios (el miembro **dbcv \_ Flags** es DBTF \_ media).</span><span class="sxs-lookup"><span data-stu-id="0411a-122">If media is being removed, the type of device arriving is a volume (the **dbch\_devicetype** member is DBT\_DEVTYP\_VOLUME) and the change effects the media (the **dbcv\_flags** member is DBTF\_MEDIA).</span></span>

## <a name="examples"></a><span data-ttu-id="0411a-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0411a-123">Examples</span></span>

<span data-ttu-id="0411a-124">Para ver un ejemplo, consulte detección de la [inserción o eliminación de medios](detecting-media-insertion-or-removal.md) o [procesamiento de una solicitud para quitar un dispositivo](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="0411a-124">For an example, see [Detecting Media Insertion or Removal](detecting-media-insertion-or-removal.md) or [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0411a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0411a-125">Requirements</span></span>



| <span data-ttu-id="0411a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0411a-126">Requirement</span></span> | <span data-ttu-id="0411a-127">Value</span><span class="sxs-lookup"><span data-stu-id="0411a-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0411a-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0411a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0411a-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0411a-129">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="0411a-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0411a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0411a-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0411a-131">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="0411a-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0411a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0411a-133"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="0411a-133"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0411a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="0411a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0411a-135">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="0411a-135">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="0411a-136">Eventos de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="0411a-136">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="0411a-137">**DEV \_ Broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="0411a-137">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="0411a-138">**DEVICECHANGE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="0411a-138">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




