---
description: Contiene el estado actual de la batería.
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
title: BATTERY_STATUS estructura (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: d6e68f5cec0215687fe4fde66698ea1be0d62c6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667222"
---
# <a name="battery_status-structure"></a><span data-ttu-id="68840-103">Estructura de estado de la batería \_</span><span class="sxs-lookup"><span data-stu-id="68840-103">BATTERY\_STATUS structure</span></span>

<span data-ttu-id="68840-104">Contiene el estado actual de la batería.</span><span class="sxs-lookup"><span data-stu-id="68840-104">Contains the current state of the battery.</span></span> <span data-ttu-id="68840-105">Esta estructura la usa el código de control de [**\_ Estado de \_ consulta \_**](ioctl-battery-query-status.md) de la batería de ioctl.</span><span class="sxs-lookup"><span data-stu-id="68840-105">This structure is used by the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="68840-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68840-106">Syntax</span></span>


```C++
typedef struct _BATTERY_STATUS {
  ULONG PowerState;
  ULONG Capacity;
  ULONG Voltage;
  LONG  Rate;
} BATTERY_STATUS, *PBATTERY_STATUS;
```



## <a name="members"></a><span data-ttu-id="68840-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="68840-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="68840-108">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="68840-108">**PowerState**</span></span>
</dt> <dd>

<span data-ttu-id="68840-109">Estado de la batería.</span><span class="sxs-lookup"><span data-stu-id="68840-109">The battery state.</span></span> <span data-ttu-id="68840-110">Este miembro puede ser cero, uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="68840-110">This member can be zero, one, or more of the following values.</span></span>



| <span data-ttu-id="68840-111">Value</span><span class="sxs-lookup"><span data-stu-id="68840-111">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="68840-112">Significado</span><span class="sxs-lookup"><span data-stu-id="68840-112">Meaning</span></span>                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <span data-ttu-id="68840-113"><dt>**Batería \_ de Cargando**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="68840-113"><dt>**BATTERY\_CHARGING**</dt> <dt>0x00000004</dt></span></span> </dl>                  | <span data-ttu-id="68840-114">Indica que la batería se está cargando actualmente.</span><span class="sxs-lookup"><span data-stu-id="68840-114">Indicates that the battery is currently charging.</span></span><br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <span data-ttu-id="68840-115"><dt>**Batería \_ de**</dt> <dt>0x00000008</dt> crítico</span><span class="sxs-lookup"><span data-stu-id="68840-115"><dt>**BATTERY\_CRITICAL**</dt> <dt>0x00000008</dt></span></span> </dl>                  | <span data-ttu-id="68840-116">Indica que el error de la batería es inminente.</span><span class="sxs-lookup"><span data-stu-id="68840-116">Indicates that battery failure is imminent.</span></span> <span data-ttu-id="68840-117">Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="68840-117">See the Remarks section for more information.</span></span><br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <span data-ttu-id="68840-118"><dt>**Batería \_ de Descargar**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="68840-118"><dt>**BATTERY\_DISCHARGING**</dt> <dt>0x00000002</dt></span></span> </dl>         | <span data-ttu-id="68840-119">Indica que la batería se está descargando actualmente.</span><span class="sxs-lookup"><span data-stu-id="68840-119">Indicates that the battery is currently discharging.</span></span><br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <span data-ttu-id="68840-120"><dt>**Batería \_ de ENCENDIDO \_ en la \_ línea**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="68840-120"><dt>**BATTERY\_POWER\_ON\_LINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="68840-121">Indica que el sistema tiene acceso a la corriente alterna, por lo que no se está aplicando ninguna batería.</span><span class="sxs-lookup"><span data-stu-id="68840-121">Indicates that the system has access to AC power, so no batteries are being discharged.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="68840-122">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="68840-122">**Capacity**</span></span>
</dt> <dd>

<span data-ttu-id="68840-123">La capacidad actual de la batería, en mWh (o relativa).</span><span class="sxs-lookup"><span data-stu-id="68840-123">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="68840-124">Este valor se puede usar para generar una presentación de "medidor de gas" dividiéndolo por el miembro **FullChargedCapacity** de la estructura de [**\_ información**](battery-information-str.md) de la batería.</span><span class="sxs-lookup"><span data-stu-id="68840-124">This value can be used to generate a "gas gauge" display by dividing it by **FullChargedCapacity** member of the [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span> <span data-ttu-id="68840-125">Si la capacidad no está disponible, este miembro tiene una capacidad desconocida de la batería \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="68840-125">If the capacity is unavailable, this member is BATTERY\_UNKNOWN\_CAPACITY.</span></span>

</dd> <dt>

<span data-ttu-id="68840-126">**Voltaje**</span><span class="sxs-lookup"><span data-stu-id="68840-126">**Voltage**</span></span>
</dt> <dd>

<span data-ttu-id="68840-127">La tensión de la batería actual a través de los terminales de la batería, en milivoltios (MV).</span><span class="sxs-lookup"><span data-stu-id="68840-127">The current battery voltage across the battery terminals, in millivolts (mv).</span></span> <span data-ttu-id="68840-128">Si el voltaje no está disponible, este miembro es una tensión desconocida de la batería \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="68840-128">If the voltage is unavailable, this member is BATTERY\_UNKNOWN\_VOLTAGE.</span></span>

</dd> <dt>

<span data-ttu-id="68840-129">**Tarifa**</span><span class="sxs-lookup"><span data-stu-id="68840-129">**Rate**</span></span>
</dt> <dd>

<span data-ttu-id="68840-130">La tasa actual de carga o descarga de la batería.</span><span class="sxs-lookup"><span data-stu-id="68840-130">The current rate of battery charge or discharge.</span></span> <span data-ttu-id="68840-131">Este valor estará en milivatios a menos que la información sobre la frecuencia de la batería sea relativa, en cuyo caso estará en unidades arbitrarias por hora.</span><span class="sxs-lookup"><span data-stu-id="68840-131">This value will be in milliwatts unless the battery rate information is relative, in which case it will be in arbitrary units per hour.</span></span> <span data-ttu-id="68840-132">Para determinar si la información de la batería es relativa, examine la \_ marca relativa de la capacidad de la batería \_ en el miembro **Capabilities** de la estructura de [**\_ información**](battery-information-str.md) de la batería.</span><span class="sxs-lookup"><span data-stu-id="68840-132">To determine if battery information is relative, examine the BATTERY\_CAPACITY\_RELATIVE flag in the **Capabilities** member of the [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span> <span data-ttu-id="68840-133">Un valor distinto de cero, la tasa positiva indica la carga; una tasa negativa indica la descargación.</span><span class="sxs-lookup"><span data-stu-id="68840-133">A nonzero, positive rate indicates charging; a negative rate indicates discharging.</span></span> <span data-ttu-id="68840-134">Algunas baterías solo indican tarifas de descargado.</span><span class="sxs-lookup"><span data-stu-id="68840-134">Some batteries report only discharging rates.</span></span> <span data-ttu-id="68840-135">Si la tasa no está disponible, este miembro tiene una tasa de batería \_ desconocida \_ .</span><span class="sxs-lookup"><span data-stu-id="68840-135">If the rate is unavailable, this member is BATTERY\_UNKNOWN\_RATE.</span></span> <span data-ttu-id="68840-136">Si cambia el estado de la batería o de la fuente de alimentación, la velocidad puede estar disponible.</span><span class="sxs-lookup"><span data-stu-id="68840-136">If the state of the battery or power source changes, the rate may become available.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68840-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68840-137">Remarks</span></span>

<span data-ttu-id="68840-138">La marca crítica de la batería del \_ miembro **PowerState** de esta estructura indica una condición de "batería crítica" de hardware.</span><span class="sxs-lookup"><span data-stu-id="68840-138">The BATTERY\_CRITICAL flag in the **PowerState** member of this structure indicates a hardware "battery critical" condition.</span></span> <span data-ttu-id="68840-139">Este nivel crítico está establecido por el fabricante de la batería, no por el usuario en la "alarma de batería crítica".</span><span class="sxs-lookup"><span data-stu-id="68840-139">This critical level is set by the battery manufacturer, not by the user in the "critical battery alarm."</span></span> <span data-ttu-id="68840-140">Por lo general, significa que el sistema de batería ha calculado que la batería está completamente drenada y cualquier potencia que se está dibujando está más allá de lo esperado.</span><span class="sxs-lookup"><span data-stu-id="68840-140">It generally means that the battery system has calculated that the battery is totally drained, and any power being drawn is beyond what is expected.</span></span>

## <a name="requirements"></a><span data-ttu-id="68840-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68840-141">Requirements</span></span>



| <span data-ttu-id="68840-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="68840-142">Requirement</span></span> | <span data-ttu-id="68840-143">Value</span><span class="sxs-lookup"><span data-stu-id="68840-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68840-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68840-144">Minimum supported client</span></span><br/> | <span data-ttu-id="68840-145">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="68840-145">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="68840-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68840-146">Minimum supported server</span></span><br/> | <span data-ttu-id="68840-147">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="68840-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="68840-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68840-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="68840-149"><dt>Poclass. h; </dt> <dt>Batclass. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="68840-149"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68840-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="68840-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68840-151">**información de la batería \_**</span><span class="sxs-lookup"><span data-stu-id="68840-151">**BATTERY\_INFORMATION**</span></span>](battery-information-str.md)
</dt> <dt>

[<span data-ttu-id="68840-152">**Estado de la \_ consulta de batería ioctl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="68840-152">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> </dl>

 

 




