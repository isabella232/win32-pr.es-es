---
description: Notifica a una aplicación un cambio en la configuración de hardware de un dispositivo o del equipo.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: WM_DEVICECHANGE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cc45d7a7978d5501e51cc1355c43afcf12b956
ms.sourcegitcommit: 8c1942ac6731488abbeae46a7dbe3da166fee2d6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/16/2021
ms.locfileid: "107581507"
---
# <a name="wm_devicechange-message"></a><span data-ttu-id="676b6-103">Mensaje \_ DEVICECHANGE de WM</span><span class="sxs-lookup"><span data-stu-id="676b6-103">WM\_DEVICECHANGE message</span></span>

<span data-ttu-id="676b6-104">Notifica a una aplicación un cambio en la configuración de hardware de un dispositivo o del equipo.</span><span class="sxs-lookup"><span data-stu-id="676b6-104">Notifies an application of a change to the hardware configuration of a device or the computer.</span></span>

<span data-ttu-id="676b6-105">Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="676b6-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```

## <a name="parameters"></a><span data-ttu-id="676b6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="676b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="676b6-107">*Hwnd*</span><span class="sxs-lookup"><span data-stu-id="676b6-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="676b6-108">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="676b6-108">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="676b6-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="676b6-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="676b6-110">Identificador **DE \_ WM DEVICECHANGE.**</span><span class="sxs-lookup"><span data-stu-id="676b6-110">The **WM\_DEVICECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="676b6-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="676b6-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="676b6-112">Evento que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="676b6-112">The event that has occurred.</span></span> <span data-ttu-id="676b6-113">Este parámetro puede ser uno de los siguientes valores del archivo de encabezado Dbt.h.</span><span class="sxs-lookup"><span data-stu-id="676b6-113">This parameter can be one of the following values from the Dbt.h header file.</span></span>

| <span data-ttu-id="676b6-114">Value</span><span class="sxs-lookup"><span data-stu-id="676b6-114">Value</span></span> | <span data-ttu-id="676b6-115">Significado</span><span class="sxs-lookup"><span data-stu-id="676b6-115">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="676b6-116">**[DBT \_ DEVNODES \_ CHANGED](dbt-devnodes-changed.md)**</span><span class="sxs-lookup"><span data-stu-id="676b6-116">**[DBT\_DEVNODES\_CHANGED](dbt-devnodes-changed.md)**</span></span></br><span data-ttu-id="676b6-117">0x0007</span><span class="sxs-lookup"><span data-stu-id="676b6-117">0x0007</span></span> | <span data-ttu-id="676b6-118">Se ha agregado o quitado un dispositivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="676b6-118">A device has been added to or removed from the system.</span></span> |
| <span data-ttu-id="676b6-119">**[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</span><span class="sxs-lookup"><span data-stu-id="676b6-119">**[DBT\_QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</span></span></br><span data-ttu-id="676b6-120">0x0017</span><span class="sxs-lookup"><span data-stu-id="676b6-120">0x0017</span></span> | <span data-ttu-id="676b6-121">Se solicita permiso para cambiar la configuración actual (acoplar o desacoplar).</span><span class="sxs-lookup"><span data-stu-id="676b6-121">Permission is requested to change the current configuration (dock or undock).</span></span> |
| <span data-ttu-id="676b6-122">**[DBT \_ CONFIGCHANGED](dbt-configchanged.md)**</span><span class="sxs-lookup"><span data-stu-id="676b6-122">**[DBT\_CONFIGCHANGED](dbt-configchanged.md)**</span></span></br><span data-ttu-id="676b6-123">0x0018</span><span class="sxs-lookup"><span data-stu-id="676b6-123">0x0018</span></span> | <span data-ttu-id="676b6-124">La configuración actual ha cambiado debido a un acoplamiento o desacoplado.</span><span class="sxs-lookup"><span data-stu-id="676b6-124">The current configuration has changed, due to a dock or undock.</span></span> |
| <span data-ttu-id="676b6-125">**[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</span><span class="sxs-lookup"><span data-stu-id="676b6-125">**[DBT\_CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</span></span></br><span data-ttu-id="676b6-126">0x0019</span><span class="sxs-lookup"><span data-stu-id="676b6-126">0x0019</span></span> | <span data-ttu-id="676b6-127">Se ha cancelado una solicitud para cambiar la configuración actual (acoplar o desacoplar).</span><span class="sxs-lookup"><span data-stu-id="676b6-127">A request to change the current configuration (dock or undock) has been canceled.</span></span> |
| <span data-ttu-id="676b6-128">**[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)**</span><span class="sxs-lookup"><span data-stu-id="676b6-128">**[DBT\_DEVICEARRIVAL](dbt-devicearrival.md)**</span></span></br><span data-ttu-id="676b6-129">0x8000</span><span class="sxs-lookup"><span data-stu-id="676b6-129">0x8000</span></span> | <span data-ttu-id="676b6-130">Se ha insertado un dispositivo o un elemento multimedia y ahora está disponible.</span><span class="sxs-lookup"><span data-stu-id="676b6-130">A device or piece of media has been inserted and is now available.</span></span> |
| <span data-ttu-id="676b6-131">**[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</span><span class="sxs-lookup"><span data-stu-id="676b6-131">**[DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</span></span></br><span data-ttu-id="676b6-132">0x8001</span><span class="sxs-lookup"><span data-stu-id="676b6-132">0x8001</span></span> | <span data-ttu-id="676b6-133">Se solicita permiso para quitar un dispositivo o un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="676b6-133">Permission is requested to remove a device or piece of media.</span></span> <span data-ttu-id="676b6-134">Cualquier aplicación puede denegar esta solicitud y cancelar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="676b6-134">Any application can deny this request and cancel the removal.</span></span> |
| <span data-ttu-id="676b6-135">**[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</span><span class="sxs-lookup"><span data-stu-id="676b6-135">**[DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</span></span></br><span data-ttu-id="676b6-136">0x8002</span><span class="sxs-lookup"><span data-stu-id="676b6-136">0x8002</span></span> | <span data-ttu-id="676b6-137">Se ha cancelado una solicitud para quitar un dispositivo o un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="676b6-137">A request to remove a device or piece of media has been canceled.</span></span> |
| <span data-ttu-id="676b6-138">**[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</span><span class="sxs-lookup"><span data-stu-id="676b6-138">**[DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</span></span></br><span data-ttu-id="676b6-139">0x8003</span><span class="sxs-lookup"><span data-stu-id="676b6-139">0x8003</span></span> | <span data-ttu-id="676b6-140">Un dispositivo o un elemento multimedia está a punto de quitarse.</span><span class="sxs-lookup"><span data-stu-id="676b6-140">A device or piece of media is about to be removed.</span></span> <span data-ttu-id="676b6-141">No se puede denegar.</span><span class="sxs-lookup"><span data-stu-id="676b6-141">Cannot be denied.</span></span> |
| <span data-ttu-id="676b6-142">**[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</span><span class="sxs-lookup"><span data-stu-id="676b6-142">**[DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</span></span></br><span data-ttu-id="676b6-143">0x8004</span><span class="sxs-lookup"><span data-stu-id="676b6-143">0x8004</span></span> | <span data-ttu-id="676b6-144">Se ha quitado un dispositivo o un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="676b6-144">A device or piece of media has been removed.</span></span> |
| <span data-ttu-id="676b6-145">**[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</span><span class="sxs-lookup"><span data-stu-id="676b6-145">**[DBT\_DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</span></span></br><span data-ttu-id="676b6-146">0x8005</span><span class="sxs-lookup"><span data-stu-id="676b6-146">0x8005</span></span> | <span data-ttu-id="676b6-147">Se ha producido un evento específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="676b6-147">A device-specific event has occurred.</span></span> |
| <span data-ttu-id="676b6-148">**[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</span><span class="sxs-lookup"><span data-stu-id="676b6-148">**[DBT\_CUSTOMEVENT](dbt-customevent.md)**</span></span></br><span data-ttu-id="676b6-149">0x8006</span><span class="sxs-lookup"><span data-stu-id="676b6-149">0x8006</span></span> | <span data-ttu-id="676b6-150">Se ha producido un evento personalizado.</span><span class="sxs-lookup"><span data-stu-id="676b6-150">A custom event has occurred.</span></span> |
| <span data-ttu-id="676b6-151">**[DBT \_ DEFINIDO POR EL USUARIO](dbt-userdefined.md)**</span><span class="sxs-lookup"><span data-stu-id="676b6-151">**[DBT\_USERDEFINED](dbt-userdefined.md)**</span></span></br><span data-ttu-id="676b6-152">0xFFFF</span><span class="sxs-lookup"><span data-stu-id="676b6-152">0xFFFF</span></span> | <span data-ttu-id="676b6-153">El significado de este mensaje es definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="676b6-153">The meaning of this message is user-defined.</span></span> |

</dd> <dt>

<span data-ttu-id="676b6-154">*lParam*</span><span class="sxs-lookup"><span data-stu-id="676b6-154">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="676b6-155">Puntero a una estructura que contiene datos específicos del evento.</span><span class="sxs-lookup"><span data-stu-id="676b6-155">A pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="676b6-156">Su formato depende del valor del *parámetro wParam.*</span><span class="sxs-lookup"><span data-stu-id="676b6-156">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="676b6-157">Para obtener más información, consulte la documentación de cada evento.</span><span class="sxs-lookup"><span data-stu-id="676b6-157">For more information, refer to the documentation for each event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="676b6-158">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="676b6-158">Return value</span></span>

<span data-ttu-id="676b6-159">Devuelve **TRUE** para conceder la solicitud.</span><span class="sxs-lookup"><span data-stu-id="676b6-159">Return **TRUE** to grant the request.</span></span>

<span data-ttu-id="676b6-160">Devuelve **BROADCAST QUERY DENY \_ \_ para** denegar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="676b6-160">Return **BROADCAST\_QUERY\_DENY** to deny the request.</span></span>

## <a name="remarks"></a><span data-ttu-id="676b6-161">Observaciones</span><span class="sxs-lookup"><span data-stu-id="676b6-161">Remarks</span></span>

<span data-ttu-id="676b6-162">En el caso de los dispositivos que ofrecen características controlables por software, como la expulsión y el bloqueo, el sistema normalmente envía un mensaje [ \_ DBT DEVICEREMOVEPENDING](dbt-deviceremovepending.md) para permitir que las aplicaciones y los controladores de dispositivos finalicen correctamente el uso del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="676b6-162">For devices that offer software-controllable features, such as ejection and locking, the system typically sends a [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) message to let applications and device drivers end their use of the device gracefully.</span></span> <span data-ttu-id="676b6-163">Si el sistema quita forzadamente un dispositivo, es posible que no envíe un mensaje [ \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) de DBT antes de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="676b6-163">If the system forcibly removes a device, it may not send a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message before doing so.</span></span>

## <a name="requirements"></a><span data-ttu-id="676b6-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="676b6-164">Requirements</span></span>

| <span data-ttu-id="676b6-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="676b6-165">Requirement</span></span> | <span data-ttu-id="676b6-166">Value</span><span class="sxs-lookup"><span data-stu-id="676b6-166">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="676b6-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="676b6-167">Minimum supported client</span></span> | <span data-ttu-id="676b6-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="676b6-168">Windows XP</span></span> |
| <span data-ttu-id="676b6-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="676b6-169">Minimum supported server</span></span> | <span data-ttu-id="676b6-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="676b6-170">Windows Server 2003</span></span>|
| <span data-ttu-id="676b6-171">Header</span><span class="sxs-lookup"><span data-stu-id="676b6-171">Header</span></span> | <dl> <span data-ttu-id="676b6-172"><dt>Winuser.h (incluya Windows.h o Dbt.h)</dt></span><span class="sxs-lookup"><span data-stu-id="676b6-172"><dt>Winuser.h (include Windows.h or Dbt.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="676b6-173">Consulte también</span><span class="sxs-lookup"><span data-stu-id="676b6-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="676b6-174">DBT \_ CONFIGCHANGECANCELED</span><span class="sxs-lookup"><span data-stu-id="676b6-174">DBT\_CONFIGCHANGECANCELED</span></span>](dbt-configchangecanceled.md)
</dt> <dt>

[<span data-ttu-id="676b6-175">DBT \_ CONFIGCHANGED</span><span class="sxs-lookup"><span data-stu-id="676b6-175">DBT\_CONFIGCHANGED</span></span>](dbt-configchanged.md)
</dt> <dt>

[<span data-ttu-id="676b6-176">DBT \_ CUSTOMEVENT</span><span class="sxs-lookup"><span data-stu-id="676b6-176">DBT\_CUSTOMEVENT</span></span>](dbt-customevent.md)
</dt> <dt>

[<span data-ttu-id="676b6-177">DBT \_ DEVICEARRIVAL</span><span class="sxs-lookup"><span data-stu-id="676b6-177">DBT\_DEVICEARRIVAL</span></span>](dbt-devicearrival.md)
</dt> <dt>

[<span data-ttu-id="676b6-178">DBT \_ DEVICEQUERYREMOVE</span><span class="sxs-lookup"><span data-stu-id="676b6-178">DBT\_DEVICEQUERYREMOVE</span></span>](dbt-devicequeryremove.md)
</dt> <dt>

[<span data-ttu-id="676b6-179">DBT \_ DEVICEQUERYREMOVEFAILED</span><span class="sxs-lookup"><span data-stu-id="676b6-179">DBT\_DEVICEQUERYREMOVEFAILED</span></span>](dbt-devicequeryremovefailed.md)
</dt> <dt>

[<span data-ttu-id="676b6-180">DBT \_ DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="676b6-180">DBT\_DEVICEREMOVECOMPLETE</span></span>](dbt-deviceremovecomplete.md)
</dt> <dt>

[<span data-ttu-id="676b6-181">DBT \_ DEVICEREMOVEPENDING</span><span class="sxs-lookup"><span data-stu-id="676b6-181">DBT\_DEVICEREMOVEPENDING</span></span>](dbt-deviceremovepending.md)
</dt> <dt>

[<span data-ttu-id="676b6-182">DBT \_ DEVICETYPESPECIFIC</span><span class="sxs-lookup"><span data-stu-id="676b6-182">DBT\_DEVICETYPESPECIFIC</span></span>](dbt-devicetypespecific.md)
</dt> <dt>

[<span data-ttu-id="676b6-183">DBT \_ DEVNODES \_ CHANGED</span><span class="sxs-lookup"><span data-stu-id="676b6-183">DBT\_DEVNODES\_CHANGED</span></span>](dbt-devnodes-changed.md)
</dt> <dt>

[<span data-ttu-id="676b6-184">DBT \_ QUERYCHANGECONFIG</span><span class="sxs-lookup"><span data-stu-id="676b6-184">DBT\_QUERYCHANGECONFIG</span></span>](dbt-querychangeconfig.md)
</dt> <dt>

[<span data-ttu-id="676b6-185">DBT \_ DEFINIDO POR EL USUARIO</span><span class="sxs-lookup"><span data-stu-id="676b6-185">DBT\_USERDEFINED</span></span>](dbt-userdefined.md)
</dt> </dl>
