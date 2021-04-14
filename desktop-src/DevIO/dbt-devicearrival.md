---
description: El sistema difunde el \_ evento de dispositivo DBT DEVICEARRIVAL cuando se ha insertado un dispositivo o un elemento multimedia y está disponible.
ms.assetid: 8e44cb02-cf79-4b19-807e-20cea07362af
title: Evento DBT_DEVICEARRIVAL (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69c2feec996b4306c271454767ca4e75d1ff855
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496211"
---
# <a name="dbt_devicearrival-event"></a><span data-ttu-id="37411-103">\_Evento DBT DEVICEARRIVAL</span><span class="sxs-lookup"><span data-stu-id="37411-103">DBT\_DEVICEARRIVAL event</span></span>

<span data-ttu-id="37411-104">El sistema difunde el \_ evento de dispositivo DBT DEVICEARRIVAL cuando se ha insertado un dispositivo o un elemento multimedia y está disponible.</span><span class="sxs-lookup"><span data-stu-id="37411-104">The system broadcasts the DBT\_DEVICEARRIVAL device event when a device or piece of media has been inserted and becomes available.</span></span>

<span data-ttu-id="37411-105">Para difundir este evento de dispositivo, el sistema usa el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) con *wParam* establecido en DBT \_ DEVICEARRIVAL y *lParam* , tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="37411-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEARRIVAL and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="37411-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37411-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37411-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="37411-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="37411-108">Identificador a una ventana.</span><span class="sxs-lookup"><span data-stu-id="37411-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="37411-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="37411-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="37411-110">Identificador del mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="37411-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="37411-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37411-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37411-112">Establézcalo en DBT \_ DEVICEARRIVAL.</span><span class="sxs-lookup"><span data-stu-id="37411-112">Set to DBT\_DEVICEARRIVAL.</span></span>

</dd> <dt>

<span data-ttu-id="37411-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37411-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37411-114">Puntero a una estructura que identifica el dispositivo insertado.</span><span class="sxs-lookup"><span data-stu-id="37411-114">A pointer to a structure identifying the device inserted.</span></span> <span data-ttu-id="37411-115">La estructura consta de un encabezado independiente del evento, seguido de los miembros dependientes del evento que describen el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37411-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="37411-116">Para usar esta estructura, trate la estructura como una [**estructura \_ \_ HDR de difusión de desarrollo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) y, a continuación, compruebe su miembro **dbch \_ DeviceType** para determinar el tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37411-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37411-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37411-117">Return value</span></span>

<span data-ttu-id="37411-118">Devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="37411-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="37411-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37411-119">Remarks</span></span>

<span data-ttu-id="37411-120">Si se inserta un medio, el tipo de dispositivo que llega es un volumen (el miembro **dbch \_ DEVICETYPE** es DBT \_ DEVTYP \_ ) y el cambio afecta a los medios (el miembro **dbcv \_ Flags** es DBTF \_ media).</span><span class="sxs-lookup"><span data-stu-id="37411-120">If media is being inserted, the type of device arriving is a volume (the **dbch\_devicetype** member is DBT\_DEVTYP\_VOLUME) and the change effects the media (the **dbcv\_flags** member is DBTF\_MEDIA).</span></span>

## <a name="examples"></a><span data-ttu-id="37411-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="37411-121">Examples</span></span>

<span data-ttu-id="37411-122">Para obtener un ejemplo, vea [detectar la inserción o eliminación de medios](detecting-media-insertion-or-removal.md).</span><span class="sxs-lookup"><span data-stu-id="37411-122">For an example, see [Detecting Media Insertion or Removal](detecting-media-insertion-or-removal.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37411-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37411-123">Requirements</span></span>



| <span data-ttu-id="37411-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="37411-124">Requirement</span></span> | <span data-ttu-id="37411-125">Value</span><span class="sxs-lookup"><span data-stu-id="37411-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="37411-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37411-126">Minimum supported client</span></span><br/> | <span data-ttu-id="37411-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="37411-127">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="37411-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37411-128">Minimum supported server</span></span><br/> | <span data-ttu-id="37411-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="37411-129">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="37411-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37411-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="37411-131"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="37411-131"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37411-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="37411-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37411-133">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="37411-133">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="37411-134">Eventos de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="37411-134">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="37411-135">**DEV \_ Broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="37411-135">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="37411-136">**DEVICECHANGE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="37411-136">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




