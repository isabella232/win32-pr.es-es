---
description: El sistema difunde el \_ evento de dispositivo DBT DEVICEQUERYREMOVE para solicitar permiso para quitar un dispositivo o un elemento multimedia.
ms.assetid: a0e9aa57-da0e-4e9c-99d0-5502040d2664
title: Evento DBT_DEVICEQUERYREMOVE (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c9dbdee13318f9a664582fdba8f9e3f9bfc5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659544"
---
# <a name="dbt_devicequeryremove-event"></a><span data-ttu-id="27c88-103">\_Evento DBT DEVICEQUERYREMOVE</span><span class="sxs-lookup"><span data-stu-id="27c88-103">DBT\_DEVICEQUERYREMOVE event</span></span>

<span data-ttu-id="27c88-104">El sistema difunde el \_ evento de dispositivo DBT DEVICEQUERYREMOVE para solicitar permiso para quitar un dispositivo o un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="27c88-104">The system broadcasts the DBT\_DEVICEQUERYREMOVE device event to request permission to remove a device or piece of media.</span></span> <span data-ttu-id="27c88-105">Este mensaje es la última oportunidad para que las aplicaciones y los controladores se preparen para esta eliminación.</span><span class="sxs-lookup"><span data-stu-id="27c88-105">This message is the last chance for applications and drivers to prepare for this removal.</span></span> <span data-ttu-id="27c88-106">Sin embargo, cualquier aplicación puede denegar esta solicitud y cancelar la operación.</span><span class="sxs-lookup"><span data-stu-id="27c88-106">However, any application can deny this request and cancel the operation.</span></span>

<span data-ttu-id="27c88-107">Para difundir este evento de dispositivo, el sistema usa el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) con *wParam* establecido en DBT \_ DEVICEQUERYREMOVE y *lParam* , tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="27c88-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEQUERYREMOVE and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="27c88-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27c88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27c88-109">*identificador*</span><span class="sxs-lookup"><span data-stu-id="27c88-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="27c88-110">Identificador a una ventana.</span><span class="sxs-lookup"><span data-stu-id="27c88-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="27c88-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="27c88-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="27c88-112">Identificador del mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="27c88-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="27c88-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27c88-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27c88-114">Establézcalo en DBT \_ DEVICEQUERYREMOVE.</span><span class="sxs-lookup"><span data-stu-id="27c88-114">Set to DBT\_DEVICEQUERYREMOVE.</span></span>

</dd> <dt>

<span data-ttu-id="27c88-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27c88-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27c88-116">Puntero a una estructura que identifica el dispositivo que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="27c88-116">A pointer to a structure identifying the device to remove.</span></span> <span data-ttu-id="27c88-117">La estructura consta de un encabezado independiente del evento, seguido de los miembros dependientes del evento que describen el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27c88-117">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="27c88-118">Para usar esta estructura, trate la estructura como una [**estructura \_ \_ HDR de difusión de desarrollo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) y, a continuación, compruebe su miembro **dbch \_ DeviceType** para determinar el tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27c88-118">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27c88-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27c88-119">Return value</span></span>

<span data-ttu-id="27c88-120">Devuelva **true** para conceder permiso para quitar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27c88-120">Return **TRUE** to grant permission to remove a device.</span></span>

<span data-ttu-id="27c88-121">Devolver consulta de difusión \_ \_ denegar para denegar el permiso para quitar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27c88-121">Return BROADCAST\_QUERY\_DENY to deny permission to remove a device.</span></span>

## <a name="remarks"></a><span data-ttu-id="27c88-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27c88-122">Remarks</span></span>

<span data-ttu-id="27c88-123">Debe cerrar todos los identificadores del dispositivo o se producirá un error en la eliminación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27c88-123">You must close all handles to the device or the device removal will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="27c88-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="27c88-124">Examples</span></span>

<span data-ttu-id="27c88-125">Para ver un ejemplo, consulte [procesamiento de una solicitud para quitar un dispositivo](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="27c88-125">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="27c88-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27c88-126">Requirements</span></span>



| <span data-ttu-id="27c88-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="27c88-127">Requirement</span></span> | <span data-ttu-id="27c88-128">Value</span><span class="sxs-lookup"><span data-stu-id="27c88-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="27c88-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27c88-129">Minimum supported client</span></span><br/> | <span data-ttu-id="27c88-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="27c88-130">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="27c88-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27c88-131">Minimum supported server</span></span><br/> | <span data-ttu-id="27c88-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27c88-132">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="27c88-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27c88-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="27c88-134"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="27c88-134"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27c88-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="27c88-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c88-136">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="27c88-136">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="27c88-137">Eventos de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="27c88-137">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="27c88-138">**DEV \_ Broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="27c88-138">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="27c88-139">**DEVICECHANGE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="27c88-139">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




