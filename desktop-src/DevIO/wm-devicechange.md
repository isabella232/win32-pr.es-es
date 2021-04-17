---
description: Notifica a una aplicación de un cambio en la configuración de hardware de un dispositivo o del equipo.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: Mensaje de WM_DEVICECHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f631d75f89f306adc0594a3df6c63d63753e163
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423296"
---
# <a name="wm_devicechange-message"></a><span data-ttu-id="f0598-103">Mensaje de DEVICECHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="f0598-103">WM\_DEVICECHANGE message</span></span>

<span data-ttu-id="f0598-104">Notifica a una aplicación de un cambio en la configuración de hardware de un dispositivo o del equipo.</span><span class="sxs-lookup"><span data-stu-id="f0598-104">Notifies an application of a change to the hardware configuration of a device or the computer.</span></span>

<span data-ttu-id="f0598-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f0598-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a><span data-ttu-id="f0598-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0598-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0598-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="f0598-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f0598-108">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f0598-108">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="f0598-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="f0598-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="f0598-110">Identificador **de \_ DEVICECHANGE de WM** .</span><span class="sxs-lookup"><span data-stu-id="f0598-110">The **WM\_DEVICECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f0598-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0598-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0598-112">Evento que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="f0598-112">The event that has occurred.</span></span> <span data-ttu-id="f0598-113">Este parámetro puede ser uno de los siguientes valores del archivo de encabezado DBT. h.</span><span class="sxs-lookup"><span data-stu-id="f0598-113">This parameter can be one of the following values from the Dbt.h header file.</span></span>



| <span data-ttu-id="f0598-114">Value</span><span class="sxs-lookup"><span data-stu-id="f0598-114">Value</span></span>                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="f0598-115">Significado</span><span class="sxs-lookup"><span data-stu-id="f0598-115">Meaning</span></span>                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span><dl> <span data-ttu-id="f0598-116"><dt>**[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt></span><span class="sxs-lookup"><span data-stu-id="f0598-116"><dt>**[DBT\_CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt></span></span> </dl>             | <span data-ttu-id="f0598-117">Se ha cancelado una solicitud para cambiar la configuración actual (acoplar o desacoplar).</span><span class="sxs-lookup"><span data-stu-id="f0598-117">A request to change the current configuration (dock or undock) has been canceled.</span></span><br/>                                           |
| <span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span><dl> <span data-ttu-id="f0598-118"><dt>**[DBT \_ CONFIGCHANGED](dbt-configchanged.md)**</dt> <dt>0x0018</dt></span><span class="sxs-lookup"><span data-stu-id="f0598-118"><dt>**[DBT\_CONFIGCHANGED](dbt-configchanged.md)**</dt> <dt>0x0018</dt></span></span> </dl>                                         | <span data-ttu-id="f0598-119">La configuración actual ha cambiado debido a un acoplamiento o desacoplamiento.</span><span class="sxs-lookup"><span data-stu-id="f0598-119">The current configuration has changed, due to a dock or undock.</span></span><br/>                                                             |
| <span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span><dl> <span data-ttu-id="f0598-120"><dt>**[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt></span><span class="sxs-lookup"><span data-stu-id="f0598-120"><dt>**[DBT\_CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt></span></span> </dl>                                                 | <span data-ttu-id="f0598-121">Se ha producido un evento personalizado.</span><span class="sxs-lookup"><span data-stu-id="f0598-121">A custom event has occurred.</span></span><br/>                                                                                                |
| <span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span><dl> <span data-ttu-id="f0598-122"><dt>**[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="f0598-122"><dt>**[DBT\_DEVICEARRIVAL](dbt-devicearrival.md)**</dt> <dt>0x8000</dt></span></span> </dl>                                         | <span data-ttu-id="f0598-123">Se ha insertado un dispositivo o parte de un medio y ahora está disponible.</span><span class="sxs-lookup"><span data-stu-id="f0598-123">A device or piece of media has been inserted and is now available.</span></span><br/>                                                          |
| <span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span><dl> <span data-ttu-id="f0598-124"><dt>**[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt></span><span class="sxs-lookup"><span data-stu-id="f0598-124"><dt>**[DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt></span></span> </dl>                         | <span data-ttu-id="f0598-125">Se solicita permiso para quitar un dispositivo o parte de un medio.</span><span class="sxs-lookup"><span data-stu-id="f0598-125">Permission is requested to remove a device or piece of media.</span></span> <span data-ttu-id="f0598-126">Cualquier aplicación puede denegar esta solicitud y cancelar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="f0598-126">Any application can deny this request and cancel the removal.</span></span><br/> |
| <span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span><dl> <span data-ttu-id="f0598-127"><dt>**[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt></span><span class="sxs-lookup"><span data-stu-id="f0598-127"><dt>**[DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt></span></span> </dl> | <span data-ttu-id="f0598-128">Se ha cancelado una solicitud para quitar un dispositivo o un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="f0598-128">A request to remove a device or piece of media has been canceled.</span></span><br/>                                                           |
| <span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span><dl> <span data-ttu-id="f0598-129"><dt>**[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt></span><span class="sxs-lookup"><span data-stu-id="f0598-129"><dt>**[DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt></span></span> </dl>             | <span data-ttu-id="f0598-130">Se ha quitado un dispositivo o un medio.</span><span class="sxs-lookup"><span data-stu-id="f0598-130">A device or piece of media has been removed.</span></span><br/>                                                                                |
| <span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span><dl> <span data-ttu-id="f0598-131"><dt>**[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt></span><span class="sxs-lookup"><span data-stu-id="f0598-131"><dt>**[DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt></span></span> </dl>                 | <span data-ttu-id="f0598-132">Se va a quitar un dispositivo o parte de un medio.</span><span class="sxs-lookup"><span data-stu-id="f0598-132">A device or piece of media is about to be removed.</span></span> <span data-ttu-id="f0598-133">No se puede denegar.</span><span class="sxs-lookup"><span data-stu-id="f0598-133">Cannot be denied.</span></span><br/>                                                        |
| <span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span><dl> <span data-ttu-id="f0598-134"><dt>**[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt></span><span class="sxs-lookup"><span data-stu-id="f0598-134"><dt>**[DBT\_DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt></span></span> </dl>                     | <span data-ttu-id="f0598-135">Se ha producido un evento específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f0598-135">A device-specific event has occurred.</span></span><br/>                                                                                       |
| <span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span><dl> <span data-ttu-id="f0598-136"><dt>**[DBT \_ DEVNODES \_ cambió](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="f0598-136"><dt>**[DBT\_DEVNODES\_CHANGED](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt></span></span> </dl>                            | <span data-ttu-id="f0598-137">Se ha agregado o quitado un dispositivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="f0598-137">A device has been added to or removed from the system.</span></span><br/>                                                                      |
| <span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span><dl> <span data-ttu-id="f0598-138"><dt>**[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt></span><span class="sxs-lookup"><span data-stu-id="f0598-138"><dt>**[DBT\_QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt></span></span> </dl>                         | <span data-ttu-id="f0598-139">Se solicita permiso para cambiar la configuración actual (acoplar o desacoplar).</span><span class="sxs-lookup"><span data-stu-id="f0598-139">Permission is requested to change the current configuration (dock or undock).</span></span><br/>                                               |
| <span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span><dl> <span data-ttu-id="f0598-140"><dt>**[DBT \_ USERDEFINED](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="f0598-140"><dt>**[DBT\_USERDEFINED](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt></span></span> </dl>                                                 | <span data-ttu-id="f0598-141">El significado de este mensaje está definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f0598-141">The meaning of this message is user-defined.</span></span><br/>                                                                                |



 

</dd> <dt>

<span data-ttu-id="f0598-142">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0598-142">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0598-143">Puntero a una estructura que contiene datos específicos del evento.</span><span class="sxs-lookup"><span data-stu-id="f0598-143">A pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="f0598-144">Su formato depende del valor del parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="f0598-144">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="f0598-145">Para obtener más información, consulte la documentación de cada evento.</span><span class="sxs-lookup"><span data-stu-id="f0598-145">For more information, refer to the documentation for each event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0598-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0598-146">Return value</span></span>

<span data-ttu-id="f0598-147">Devuelva **true** para conceder la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f0598-147">Return **TRUE** to grant the request.</span></span>

<span data-ttu-id="f0598-148">Devuelve **la \_ consulta \_ de difusión deny** para denegar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f0598-148">Return **BROADCAST\_QUERY\_DENY** to deny the request.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0598-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0598-149">Remarks</span></span>

<span data-ttu-id="f0598-150">En el caso de los dispositivos que ofrecen características controlables por software, como la expulsión y el bloqueo, el sistema normalmente envía un mensaje [ \_ DEVICEREMOVEPENDING de DBT](dbt-deviceremovepending.md) para permitir que las aplicaciones y los controladores de dispositivos terminen su uso del dispositivo correctamente.</span><span class="sxs-lookup"><span data-stu-id="f0598-150">For devices that offer software-controllable features, such as ejection and locking, the system typically sends a [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) message to let applications and device drivers end their use of the device gracefully.</span></span> <span data-ttu-id="f0598-151">Si el sistema quita de forma forzada un dispositivo, es posible que no envíe un mensaje de [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) antes de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="f0598-151">If the system forcibly removes a device, it may not send a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message before doing so.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0598-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0598-152">Requirements</span></span>



| <span data-ttu-id="f0598-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0598-153">Requirement</span></span> | <span data-ttu-id="f0598-154">Value</span><span class="sxs-lookup"><span data-stu-id="f0598-154">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0598-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0598-155">Minimum supported client</span></span><br/> | <span data-ttu-id="f0598-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f0598-156">Windows XP</span></span><br/>                                                                                             |
| <span data-ttu-id="f0598-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0598-157">Minimum supported server</span></span><br/> | <span data-ttu-id="f0598-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f0598-158">Windows Server 2003</span></span><br/>                                                                                    |
| <span data-ttu-id="f0598-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0598-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0598-160"><dt>Winuser. h (incluye Windows. h o DBT. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0598-160"><dt>Winuser.h (include Windows.h or Dbt.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0598-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0598-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0598-162">DBT \_ CONFIGCHANGECANCELED</span><span class="sxs-lookup"><span data-stu-id="f0598-162">DBT\_CONFIGCHANGECANCELED</span></span>](dbt-configchangecanceled.md)
</dt> <dt>

[<span data-ttu-id="f0598-163">DBT \_ CONFIGCHANGED</span><span class="sxs-lookup"><span data-stu-id="f0598-163">DBT\_CONFIGCHANGED</span></span>](dbt-configchanged.md)
</dt> <dt>

[<span data-ttu-id="f0598-164">DBT \_ CUSTOMEVENT</span><span class="sxs-lookup"><span data-stu-id="f0598-164">DBT\_CUSTOMEVENT</span></span>](dbt-customevent.md)
</dt> <dt>

[<span data-ttu-id="f0598-165">DBT \_ DEVICEARRIVAL</span><span class="sxs-lookup"><span data-stu-id="f0598-165">DBT\_DEVICEARRIVAL</span></span>](dbt-devicearrival.md)
</dt> <dt>

[<span data-ttu-id="f0598-166">DBT \_ DEVICEQUERYREMOVE</span><span class="sxs-lookup"><span data-stu-id="f0598-166">DBT\_DEVICEQUERYREMOVE</span></span>](dbt-devicequeryremove.md)
</dt> <dt>

[<span data-ttu-id="f0598-167">DBT \_ DEVICEQUERYREMOVEFAILED</span><span class="sxs-lookup"><span data-stu-id="f0598-167">DBT\_DEVICEQUERYREMOVEFAILED</span></span>](dbt-devicequeryremovefailed.md)
</dt> <dt>

[<span data-ttu-id="f0598-168">DBT \_ DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="f0598-168">DBT\_DEVICEREMOVECOMPLETE</span></span>](dbt-deviceremovecomplete.md)
</dt> <dt>

[<span data-ttu-id="f0598-169">DBT \_ DEVICEREMOVEPENDING</span><span class="sxs-lookup"><span data-stu-id="f0598-169">DBT\_DEVICEREMOVEPENDING</span></span>](dbt-deviceremovepending.md)
</dt> <dt>

[<span data-ttu-id="f0598-170">DBT \_ DEVICETYPESPECIFIC</span><span class="sxs-lookup"><span data-stu-id="f0598-170">DBT\_DEVICETYPESPECIFIC</span></span>](dbt-devicetypespecific.md)
</dt> <dt>

[<span data-ttu-id="f0598-171">DBT \_ DEVNODES \_ Changed</span><span class="sxs-lookup"><span data-stu-id="f0598-171">DBT\_DEVNODES\_CHANGED</span></span>](dbt-devnodes-changed.md)
</dt> <dt>

[<span data-ttu-id="f0598-172">DBT \_ QUERYCHANGECONFIG</span><span class="sxs-lookup"><span data-stu-id="f0598-172">DBT\_QUERYCHANGECONFIG</span></span>](dbt-querychangeconfig.md)
</dt> <dt>

[<span data-ttu-id="f0598-173">DBT \_ USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="f0598-173">DBT\_USERDEFINED</span></span>](dbt-userdefined.md)
</dt> </dl>

 

