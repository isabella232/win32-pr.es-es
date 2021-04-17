---
description: Contiene información sobre las condiciones en las que se va a recuperar el estado de la batería.
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
title: BATTERY_WAIT_STATUS estructura (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_WAIT_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 08d1e3b85d22122426f1e4648f47a808468bfb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667221"
---
# <a name="battery_wait_status-structure"></a><span data-ttu-id="ca1bd-103">Estructura de estado de \_ espera de batería \_</span><span class="sxs-lookup"><span data-stu-id="ca1bd-103">BATTERY\_WAIT\_STATUS structure</span></span>

<span data-ttu-id="ca1bd-104">Contiene información sobre las condiciones en las que se va a recuperar el estado de la batería.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-104">Contains information about the conditions under which the battery status is to be retrieved.</span></span> <span data-ttu-id="ca1bd-105">Esta estructura la usa el código de control de [**\_ Estado de \_ consulta \_**](ioctl-battery-query-status.md) de la batería de ioctl.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-105">This structure is used by the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca1bd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca1bd-106">Syntax</span></span>


```C++
typedef struct _BATTERY_WAIT_STATUS {
  ULONG BatteryTag;
  ULONG Timeout;
  ULONG PowerState;
  ULONG LowCapacity;
  ULONG HighCapacity;
} BATTERY_WAIT_STATUS, *PBATTERY_WAIT_STATUS;
```



## <a name="members"></a><span data-ttu-id="ca1bd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ca1bd-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca1bd-108">**BatteryTag**</span><span class="sxs-lookup"><span data-stu-id="ca1bd-108">**BatteryTag**</span></span>
</dt> <dd>

<span data-ttu-id="ca1bd-109">La etiqueta de la batería actual para la batería.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-109">The current battery tag for the battery.</span></span> <span data-ttu-id="ca1bd-110">Solo se puede devolver información de una batería que coincida con la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-110">Only information for a battery matching the tag can be returned.</span></span> <span data-ttu-id="ca1bd-111">Cuando este valor no coincide con la etiqueta actual de la batería, se producirá un error en la operación [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con un código de error \_ \_ no \_ encontrado, lo que indica al autor de la llamada que la batería para la que tiene una etiqueta ya no está instalada, el autor de la llamada puede optar por usar la operación de etiqueta de consulta de batería de ioctl para determinar la etiqueta de la batería recién [**\_ \_ \_**](ioctl-battery-query-tag.md)</span><span class="sxs-lookup"><span data-stu-id="ca1bd-111">Whenever this value does not match the battery's current tag, the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) operation will fail with an error code of ERROR\_FILE\_NOT\_FOUND, which indicates to the caller that the battery for which it has a tag is no longer installed The caller may opt to use the [**IOCTL\_BATTERY\_QUERY\_TAG**](ioctl-battery-query-tag.md) operation to determine the tag of the newly installed battery, if any.</span></span> <span data-ttu-id="ca1bd-112">Además, si la solicitud está en curso cuando se quita la batería o la etiqueta cambia, la operación se anula con el estado \_ \_ no se encontró el archivo de error \_ .</span><span class="sxs-lookup"><span data-stu-id="ca1bd-112">In addition, if the request is in progress when the battery is removed, or the tag changes, the operation is aborted with the status of ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="ca1bd-113">(Consulte [etiquetas de batería](battery-information.md) para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="ca1bd-113">(See [Battery Tags](battery-information.md) for more information.)</span></span>

</dd> <dt>

<span data-ttu-id="ca1bd-114">**Tiempo de espera**</span><span class="sxs-lookup"><span data-stu-id="ca1bd-114">**Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="ca1bd-115">Número de milisegundos que la solicitud esperará a la condición especificada por los miembros **PowerState**, **LowCapacity** y **HighCapacity** antes de completarse.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-115">The number of milliseconds the request will wait for the condition specified by the **PowerState**, **LowCapacity**, and **HighCapacity** members before completing.</span></span> <span data-ttu-id="ca1bd-116">Un valor de-1 indica que la solicitud esperará indefinidamente a que se cumplan las condiciones.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-116">A value of -1 indicates that the request will wait indefinitely for the conditions to be satisfied.</span></span> <span data-ttu-id="ca1bd-117">Un valor de cero indica que la información de batería solicitada se devolverá inmediatamente, independientemente de las demás condiciones.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-117">A value of zero indicates that the requested battery information is to be returned immediately, regardless of the other conditions.</span></span> <span data-ttu-id="ca1bd-118">Cualquier otro valor indica que la solicitud debe esperar el período de tiempo o hasta que se cumpla alguna de las demás condiciones.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-118">Any other value indicates that the request should wait that length of time, or until any one of the other conditions is satisfied.</span></span>

<span data-ttu-id="ca1bd-119">Si el equipo ha entrado en modo de suspensión, el reloj seguirá ejecutándose, pero el recuento no volverá a activar el equipo.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-119">If the computer has entered sleep mode, the clock will continue to run, but exhausting the count will not wake the computer up.</span></span> <span data-ttu-id="ca1bd-120">Si el recuento se agota cuando el equipo es awoken y se cumplen otras condiciones, la llamada se devolverá inmediatamente al activar.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-120">If the count is exhausted when the computer is awoken, and other conditions are satisfied, the call will return immediately on awakening.</span></span>

</dd> <dt>

<span data-ttu-id="ca1bd-121">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="ca1bd-121">**PowerState**</span></span>
</dt> <dd>

<span data-ttu-id="ca1bd-122">Cero, uno o varios de los siguientes bits de estado, que indican el estado de la batería.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-122">Zero, one, or more of the following status bits, which indicate the state of the battery.</span></span> <span data-ttu-id="ca1bd-123">Es idéntico al miembro **PowerState** de la estructura de [**\_ Estado**](battery-status-str.md) de la batería.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-123">It is identical to the **PowerState** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>



| <span data-ttu-id="ca1bd-124">Value</span><span class="sxs-lookup"><span data-stu-id="ca1bd-124">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="ca1bd-125">Significado</span><span class="sxs-lookup"><span data-stu-id="ca1bd-125">Meaning</span></span>                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <span data-ttu-id="ca1bd-126"><dt>**Batería \_ de Cargando**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="ca1bd-126"><dt>**BATTERY\_CHARGING**</dt> <dt>0x00000004</dt></span></span> </dl>                  | <span data-ttu-id="ca1bd-127">Indica que la batería se está cargando actualmente.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-127">Indicates that the battery is currently charging.</span></span><br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <span data-ttu-id="ca1bd-128"><dt>**Batería \_ de**</dt> <dt>0x00000008</dt> crítico</span><span class="sxs-lookup"><span data-stu-id="ca1bd-128"><dt>**BATTERY\_CRITICAL**</dt> <dt>0x00000008</dt></span></span> </dl>                  | <span data-ttu-id="ca1bd-129">Indica que el error de la batería es inminente.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-129">Indicates that battery failure is imminent.</span></span> <span data-ttu-id="ca1bd-130">Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-130">See the Remarks section for more information.</span></span><br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <span data-ttu-id="ca1bd-131"><dt>**Batería \_ de Descargar**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="ca1bd-131"><dt>**BATTERY\_DISCHARGING**</dt> <dt>0x00000002</dt></span></span> </dl>         | <span data-ttu-id="ca1bd-132">Indica que la batería se está descargando actualmente.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-132">Indicates that the battery is currently discharging.</span></span><br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <span data-ttu-id="ca1bd-133"><dt>**Batería \_ de ENCENDIDO \_ en la \_ línea**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ca1bd-133"><dt>**BATTERY\_POWER\_ON\_LINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="ca1bd-134">Indica que la batería tiene acceso a la corriente alterna.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-134">Indicates that the battery has access to AC power.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="ca1bd-135">**LowCapacity**</span><span class="sxs-lookup"><span data-stu-id="ca1bd-135">**LowCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="ca1bd-136">La capacidad actual de la batería, en mWh (o relativa).</span><span class="sxs-lookup"><span data-stu-id="ca1bd-136">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="ca1bd-137">Este valor es idéntico al miembro **Capacity** de la estructura de [**\_ Estado**](battery-status-str.md) de la batería.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-137">This value is identical to the **Capacity** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ca1bd-138">**HighCapacity**</span><span class="sxs-lookup"><span data-stu-id="ca1bd-138">**HighCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="ca1bd-139">La capacidad actual de la batería, en mWh (o relativa).</span><span class="sxs-lookup"><span data-stu-id="ca1bd-139">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="ca1bd-140">Este valor es idéntico al miembro **Capacity** de la estructura de [**\_ Estado**](battery-status-str.md) de la batería.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-140">This value is identical to the **Capacity** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca1bd-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca1bd-141">Remarks</span></span>

<span data-ttu-id="ca1bd-142">Las solicitudes de información de la batería se posponen hasta que se produce uno de los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="ca1bd-142">Requests for battery information are postponed until one of the following occurs:</span></span>

-   <span data-ttu-id="ca1bd-143">El tiempo de espera expira (suponiendo que el tiempo de **espera** no es-1).</span><span class="sxs-lookup"><span data-stu-id="ca1bd-143">The time-out expires (assuming **Timeout** is not -1).</span></span>
-   <span data-ttu-id="ca1bd-144">El estado actual de la batería no coincide con **PowerState**.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-144">The battery's current status does not match **PowerState**.</span></span>
-   <span data-ttu-id="ca1bd-145">La capacidad de la batería es inferior a **LowCapacity**.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-145">The battery's capacity is below **LowCapacity**.</span></span>
-   <span data-ttu-id="ca1bd-146">La capacidad de la batería está por encima de **HighCapacity**.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-146">The battery's capacity is above **HighCapacity**.</span></span>
-   <span data-ttu-id="ca1bd-147">La etiqueta de la batería cambia.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-147">The battery tag changes.</span></span>

<span data-ttu-id="ca1bd-148">Cuando se cumple alguna de estas condiciones, se recopilan los datos y se devuelve la operación.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-148">When any one of these conditions is satisfied, the data is collected and the operation returns.</span></span> <span data-ttu-id="ca1bd-149">Esto permite a las aplicaciones supervisar la información de batería dinámica normal sin sondear el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-149">This allows applications to monitor typical dynamic battery information without polling the device.</span></span>

<span data-ttu-id="ca1bd-150">Antes de usar cualquiera de las dos condiciones de capacidad, asegúrese de que la batería las admita mediante el código de control de [**\_ Estado de \_ consulta \_**](ioctl-battery-query-status.md) de la batería de ioctl con un tiempo de espera de cero.</span><span class="sxs-lookup"><span data-stu-id="ca1bd-150">Before using either of the two Capacity conditions, make sure the battery supports them by using the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code with a time-out of zero.</span></span> <span data-ttu-id="ca1bd-151">Examine los resultados para determinar si se admite el miembro **Capacity** (es decir, no es una capacidad desconocida de la batería \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="ca1bd-151">Examine the results to determine if the **Capacity** member is supported (that is, not BATTERY\_UNKNOWN\_CAPACITY).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca1bd-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca1bd-152">Requirements</span></span>



| <span data-ttu-id="ca1bd-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca1bd-153">Requirement</span></span> | <span data-ttu-id="ca1bd-154">Value</span><span class="sxs-lookup"><span data-stu-id="ca1bd-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca1bd-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca1bd-155">Minimum supported client</span></span><br/> | <span data-ttu-id="ca1bd-156">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ca1bd-156">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="ca1bd-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca1bd-157">Minimum supported server</span></span><br/> | <span data-ttu-id="ca1bd-158">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ca1bd-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="ca1bd-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca1bd-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca1bd-160"><dt>Poclass. h; </dt> <dt>Batclass. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="ca1bd-160"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca1bd-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca1bd-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca1bd-162">**Estado de la batería \_**</span><span class="sxs-lookup"><span data-stu-id="ca1bd-162">**BATTERY\_STATUS**</span></span>](battery-status-str.md)
</dt> <dt>

[<span data-ttu-id="ca1bd-163">**Estado de la \_ consulta de batería ioctl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ca1bd-163">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="ca1bd-164">**\_etiqueta de \_ consulta ioctl Battery \_**</span><span class="sxs-lookup"><span data-stu-id="ca1bd-164">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> </dl>

 

