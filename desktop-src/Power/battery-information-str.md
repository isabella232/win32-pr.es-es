---
description: Contiene información de la batería.
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: BATTERY_INFORMATION estructura (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 1e892a14263822ddd009b162c6343975e1689683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667226"
---
# <a name="battery_information-structure"></a><span data-ttu-id="514cc-103">Estructura de información de la batería \_</span><span class="sxs-lookup"><span data-stu-id="514cc-103">BATTERY\_INFORMATION structure</span></span>

<span data-ttu-id="514cc-104">Contiene información de la batería.</span><span class="sxs-lookup"><span data-stu-id="514cc-104">Contains battery information.</span></span> <span data-ttu-id="514cc-105">Esta estructura la devuelve el código de control de la [**\_ información de \_ consulta \_**](ioctl-battery-query-information.md) de la batería de ioctl cuando se solicita el nivel de información de BatteryInformation.</span><span class="sxs-lookup"><span data-stu-id="514cc-105">This structure is returned by the [**IOCTL\_BATTERY\_QUERY\_INFORMATION**](ioctl-battery-query-information.md) control code when the BatteryInformation information level is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="514cc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="514cc-106">Syntax</span></span>


```C++
typedef struct _BATTERY_INFORMATION {
  ULONG Capabilities;
  UCHAR Technology;
  UCHAR Reserved[3];
  UCHAR Chemistry[4];
  ULONG DesignedCapacity;
  ULONG FullChargedCapacity;
  ULONG DefaultAlert1;
  ULONG DefaultAlert2;
  ULONG CriticalBias;
  ULONG CycleCount;
} BATTERY_INFORMATION, *PBATTERY_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="514cc-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="514cc-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="514cc-108">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="514cc-108">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="514cc-109">Las capacidades de la batería.</span><span class="sxs-lookup"><span data-stu-id="514cc-109">The battery capabilities.</span></span> <span data-ttu-id="514cc-110">Este miembro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="514cc-110">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="514cc-111">Value</span><span class="sxs-lookup"><span data-stu-id="514cc-111">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="514cc-112">Significado</span><span class="sxs-lookup"><span data-stu-id="514cc-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <span data-ttu-id="514cc-113"><dt>**Batería \_ de 0x40000000 \_ relativo**</dt> a la capacidad <dt></dt></span><span class="sxs-lookup"><span data-stu-id="514cc-113"><dt>**BATTERY\_CAPACITY\_RELATIVE**</dt> <dt>0x40000000</dt></span></span> </dl>                    | <span data-ttu-id="514cc-114">Indica que la capacidad de la batería y la información de velocidad son relativas, y no en unidades específicas.</span><span class="sxs-lookup"><span data-stu-id="514cc-114">Indicates that the battery capacity and rate information are relative, and not in any specific units.</span></span> <span data-ttu-id="514cc-115">Si no se establece este bit, las unidades de informe son milivatios-Hours (mWh) para Capacity y milivatios (mW) para Rate.</span><span class="sxs-lookup"><span data-stu-id="514cc-115">If this bit is not set, the reporting units are milliwatt-hours (mWh) for capacity and milliwatts (mW) for rate.</span></span> <span data-ttu-id="514cc-116">Si se establece este bit, se pueden omitir todas las referencias a las unidades de la documentación de la otra batería.</span><span class="sxs-lookup"><span data-stu-id="514cc-116">If this bit is set, all references to units in the other battery documentation can be ignored.</span></span> <span data-ttu-id="514cc-117">Toda la información de tarifas se registra en unidades por hora.</span><span class="sxs-lookup"><span data-stu-id="514cc-117">All rate information is reported in units per hour.</span></span> <span data-ttu-id="514cc-118">Por ejemplo, si la capacidad de carga completa se indica como 100, una tarifa de 200 indica que la batería usará toda su capacidad en media hora.</span><span class="sxs-lookup"><span data-stu-id="514cc-118">For example, if the fully charged capacity is reported as 100, a rate of 200 indicates that the battery will use all of its capacity in half an hour.</span></span><br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <span data-ttu-id="514cc-119"><dt>**Batería \_ de ES 0x20000000 a \_ corto \_ plazo**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="514cc-119"><dt>**BATTERY\_IS\_SHORT\_TERM**</dt> <dt>0x20000000</dt></span></span> </dl>                               | <span data-ttu-id="514cc-120">Indica que la operación normal es para una función a la que se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="514cc-120">Indicates that the normal operation is for a fail-safe function.</span></span> <span data-ttu-id="514cc-121">Si no se establece este bit, se espera que la batería se use durante el uso normal del sistema.</span><span class="sxs-lookup"><span data-stu-id="514cc-121">If this bit is not set the battery is expected to be used during normal system usage.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <span data-ttu-id="514cc-122"><dt>**Batería \_ de SET \_ Charge \_ support compatible**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="514cc-122"><dt>**BATTERY\_SET\_CHARGE\_SUPPORTED**</dt> <dt>0x00000001</dt></span></span> </dl>          | <span data-ttu-id="514cc-123">Indica que este dispositivo de batería admite las solicitudes Set Information del tipo BatteryCharge.</span><span class="sxs-lookup"><span data-stu-id="514cc-123">Indicates that set information requests of the type BatteryCharge are supported by this battery device.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <span data-ttu-id="514cc-124"><dt>**Batería \_ de ESTABLECER la \_ descarga \_ compatible**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="514cc-124"><dt>**BATTERY\_SET\_DISCHARGE\_SUPPORTED**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="514cc-125">Indica que este dispositivo de batería admite las solicitudes Set Information del tipo BatteryDischarge.</span><span class="sxs-lookup"><span data-stu-id="514cc-125">Indicates that set information requests of the type BatteryDischarge are supported by this battery device.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <span data-ttu-id="514cc-126"><dt>**Batería \_ de \_Batería del sistema**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="514cc-126"><dt>**BATTERY\_SYSTEM\_BATTERY**</dt> <dt>0x80000000</dt></span></span> </dl>                             | <span data-ttu-id="514cc-127">Indica que la batería puede proporcionar alimentación general para ejecutar el sistema.</span><span class="sxs-lookup"><span data-stu-id="514cc-127">Indicates that the battery can provide general power to run the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="514cc-128">**Technology**</span><span class="sxs-lookup"><span data-stu-id="514cc-128">**Technology**</span></span>
</dt> <dd>

<span data-ttu-id="514cc-129">La tecnología de la batería.</span><span class="sxs-lookup"><span data-stu-id="514cc-129">The battery technology.</span></span> <span data-ttu-id="514cc-130">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="514cc-130">This member can be one of the following values.</span></span>



| <span data-ttu-id="514cc-131">Value</span><span class="sxs-lookup"><span data-stu-id="514cc-131">Value</span></span>                                                                        | <span data-ttu-id="514cc-132">Significado</span><span class="sxs-lookup"><span data-stu-id="514cc-132">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="514cc-133"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="514cc-133"><dt>0</dt></span></span> </dl> | <span data-ttu-id="514cc-134">Batería no recargable, por ejemplo, alcalina.</span><span class="sxs-lookup"><span data-stu-id="514cc-134">Nonrechargeable battery, for example, alkaline.</span></span><br/> |
| <dl> <span data-ttu-id="514cc-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="514cc-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="514cc-136">Batería recargable, por ejemplo, acid plomo.</span><span class="sxs-lookup"><span data-stu-id="514cc-136">Rechargeable battery, for example, lead acid.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="514cc-137">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="514cc-137">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="514cc-138">Reservado.</span><span class="sxs-lookup"><span data-stu-id="514cc-138">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="514cc-139">**Químicos**</span><span class="sxs-lookup"><span data-stu-id="514cc-139">**Chemistry**</span></span>
</dt> <dd>

<span data-ttu-id="514cc-140">Cadena de caracteres abreviada que indica la química de la batería.</span><span class="sxs-lookup"><span data-stu-id="514cc-140">An abbreviated character string that indicates the battery's chemistry.</span></span> <span data-ttu-id="514cc-141">Esta cadena no es necesariamente terminada en cero.</span><span class="sxs-lookup"><span data-stu-id="514cc-141">This string is not necessarily zero-terminated.</span></span> <span data-ttu-id="514cc-142">La siguiente es una lista parcial de abreviaturas que se pueden devolver y los chemistries asociados.</span><span class="sxs-lookup"><span data-stu-id="514cc-142">The following is a partial list of abbreviations that can be returned and the associated chemistries.</span></span>



| <span data-ttu-id="514cc-143">Cadena de Unicode</span><span class="sxs-lookup"><span data-stu-id="514cc-143">Unicode string</span></span>                                                                                                                                           | <span data-ttu-id="514cc-144">Significado</span><span class="sxs-lookup"><span data-stu-id="514cc-144">Meaning</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <span data-ttu-id="514cc-145"><dt>**PbAc**</dt></span><span class="sxs-lookup"><span data-stu-id="514cc-145"><dt>**PbAc**</dt></span></span> </dl> | <span data-ttu-id="514cc-146">Acid inicial</span><span class="sxs-lookup"><span data-stu-id="514cc-146">Lead Acid</span></span><br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <span data-ttu-id="514cc-147"><dt>**LION**</dt></span><span class="sxs-lookup"><span data-stu-id="514cc-147"><dt>**LION**</dt></span></span> </dl>                        | <span data-ttu-id="514cc-148">Ion de litio</span><span class="sxs-lookup"><span data-stu-id="514cc-148">Lithium Ion</span></span><br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <span data-ttu-id="514cc-149"><dt>**Li-I**</dt></span><span class="sxs-lookup"><span data-stu-id="514cc-149"><dt>**Li-I**</dt></span></span> </dl> | <span data-ttu-id="514cc-150">Ion de litio</span><span class="sxs-lookup"><span data-stu-id="514cc-150">Lithium Ion</span></span><br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <span data-ttu-id="514cc-151"><dt>**NiCd**</dt></span><span class="sxs-lookup"><span data-stu-id="514cc-151"><dt>**NiCd**</dt></span></span> </dl> | <span data-ttu-id="514cc-152">Níquel cadmio</span><span class="sxs-lookup"><span data-stu-id="514cc-152">Nickel Cadmium</span></span><br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <span data-ttu-id="514cc-153"><dt>**NiMH**</dt></span><span class="sxs-lookup"><span data-stu-id="514cc-153"><dt>**NiMH**</dt></span></span> </dl> | <span data-ttu-id="514cc-154">Hidruro de níquel metal</span><span class="sxs-lookup"><span data-stu-id="514cc-154">Nickel Metal Hydride</span></span><br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <span data-ttu-id="514cc-155"><dt>**NiZn**</dt></span><span class="sxs-lookup"><span data-stu-id="514cc-155"><dt>**NiZn**</dt></span></span> </dl> | <span data-ttu-id="514cc-156">Cinc de níquel</span><span class="sxs-lookup"><span data-stu-id="514cc-156">Nickel Zinc</span></span><br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <span data-ttu-id="514cc-157"><dt>**RAM**</dt></span><span class="sxs-lookup"><span data-stu-id="514cc-157"><dt>**RAM**</dt></span></span> </dl>                           | <span data-ttu-id="514cc-158">Alkaline-Manganese recargable</span><span class="sxs-lookup"><span data-stu-id="514cc-158">Rechargeable Alkaline-Manganese</span></span><br/> |



 

<span data-ttu-id="514cc-159">Otros chemistries pueden aparecer en el futuro y el código debería ser capaz de controlarlos.</span><span class="sxs-lookup"><span data-stu-id="514cc-159">Other chemistries may appear in the future and your code should be able to handle them.</span></span>

</dd> <dt>

<span data-ttu-id="514cc-160">**DesignedCapacity**</span><span class="sxs-lookup"><span data-stu-id="514cc-160">**DesignedCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="514cc-161">La capacidad teórica de la batería cuando es nuevo, en mWh a menos que se establezca la capacidad de la batería \_ \_ relativa.</span><span class="sxs-lookup"><span data-stu-id="514cc-161">The theoretical capacity of the battery when new, in mWh unless BATTERY\_CAPACITY\_RELATIVE is set.</span></span> <span data-ttu-id="514cc-162">En ese caso, las unidades son indefinidas.</span><span class="sxs-lookup"><span data-stu-id="514cc-162">In that case, the units are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="514cc-163">**FullChargedCapacity**</span><span class="sxs-lookup"><span data-stu-id="514cc-163">**FullChargedCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="514cc-164">La capacidad total actual de la batería en mWh (o relativa).</span><span class="sxs-lookup"><span data-stu-id="514cc-164">The battery's current fully charged capacity in mWh (or relative).</span></span> <span data-ttu-id="514cc-165">Compare este valor con **DesignedCapacity** para estimar el desgaste de la batería.</span><span class="sxs-lookup"><span data-stu-id="514cc-165">Compare this value to **DesignedCapacity** to estimate the battery's wear.</span></span>

</dd> <dt>

<span data-ttu-id="514cc-166">**DefaultAlert1**</span><span class="sxs-lookup"><span data-stu-id="514cc-166">**DefaultAlert1**</span></span>
</dt> <dd>

<span data-ttu-id="514cc-167">La capacidad sugerida del fabricante, en mWh, en la que debe producirse una alerta de batería baja.</span><span class="sxs-lookup"><span data-stu-id="514cc-167">The manufacturer's suggested capacity, in mWh, at which a low battery alert should occur.</span></span> <span data-ttu-id="514cc-168">Las definiciones de Low varían según el fabricante.</span><span class="sxs-lookup"><span data-stu-id="514cc-168">Definitions of low vary from manufacturer to manufacturer.</span></span> <span data-ttu-id="514cc-169">En general, un estado de advertencia se produce antes de un estado bajo, pero no se debe suponer que siempre lo sea.</span><span class="sxs-lookup"><span data-stu-id="514cc-169">In general, a warning state will occur before a low state, but you should not assume that it always will.</span></span> <span data-ttu-id="514cc-170">Para reducir el riesgo de pérdida de datos, este valor se utiliza normalmente como configuración predeterminada para la alarma de batería crítica.</span><span class="sxs-lookup"><span data-stu-id="514cc-170">To reduce risk of data loss, this value is usually used as the default setting for the critical battery alarm.</span></span>

</dd> <dt>

<span data-ttu-id="514cc-171">**DefaultAlert2**</span><span class="sxs-lookup"><span data-stu-id="514cc-171">**DefaultAlert2**</span></span>
</dt> <dd>

<span data-ttu-id="514cc-172">La capacidad sugerida del fabricante, en mWh, en la que debe producirse una alerta de batería de advertencia.</span><span class="sxs-lookup"><span data-stu-id="514cc-172">The manufacturer's suggested capacity, in mWh, at which a warning battery alert should occur.</span></span> <span data-ttu-id="514cc-173">Las definiciones de advertencia varían de un fabricante a un fabricante.</span><span class="sxs-lookup"><span data-stu-id="514cc-173">Definitions of warning vary from manufacturer to manufacturer.</span></span> <span data-ttu-id="514cc-174">En general, un estado de advertencia se produce antes de un estado bajo, pero no se debe suponer que siempre lo sea.</span><span class="sxs-lookup"><span data-stu-id="514cc-174">In general, a warning state will occur before a low state, but you should not assume that it always will.</span></span> <span data-ttu-id="514cc-175">Para reducir el riesgo de pérdida de datos, este valor se utiliza normalmente como configuración predeterminada para la alarma de batería baja.</span><span class="sxs-lookup"><span data-stu-id="514cc-175">To reduce risk of data loss, this value is usually used as the default setting for the low battery alarm.</span></span>

</dd> <dt>

<span data-ttu-id="514cc-176">**CriticalBias**</span><span class="sxs-lookup"><span data-stu-id="514cc-176">**CriticalBias**</span></span>
</dt> <dd>

<span data-ttu-id="514cc-177">Una diferencia de cero, en mWh, que se aplica a los informes de batería.</span><span class="sxs-lookup"><span data-stu-id="514cc-177">A bias from zero, in mWh, which is applied to battery reporting.</span></span> <span data-ttu-id="514cc-178">Algunas baterías reservan una pequeña carga que se sesga de los valores de capacidad de la batería para mostrar "0" como nivel crítico de batería.</span><span class="sxs-lookup"><span data-stu-id="514cc-178">Some batteries reserve a small charge that is biased out of the battery's capacity values to show "0" as the critical battery level.</span></span> <span data-ttu-id="514cc-179">La diferencia crítica es análoga a la configuración de un medidor de combustible para mostrar "vacío" cuando hay varios litros de combustible a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="514cc-179">Critical bias is analogous to setting a fuel gauge to show "empty" when there are several liters of fuel left.</span></span>

</dd> <dt>

<span data-ttu-id="514cc-180">**CycleCount**</span><span class="sxs-lookup"><span data-stu-id="514cc-180">**CycleCount**</span></span>
</dt> <dd>

<span data-ttu-id="514cc-181">El número de ciclos de carga/descarga que ha experimentado la batería.</span><span class="sxs-lookup"><span data-stu-id="514cc-181">The number of charge/discharge cycles the battery has experienced.</span></span> <span data-ttu-id="514cc-182">Esto proporciona un medio para determinar el desgaste de la batería.</span><span class="sxs-lookup"><span data-stu-id="514cc-182">This provides a means to determine the battery's wear.</span></span> <span data-ttu-id="514cc-183">Si la batería no admite un contador de ciclo, este miembro es cero.</span><span class="sxs-lookup"><span data-stu-id="514cc-183">If the battery does not support a cycle counter, this member is zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="514cc-184">Observaciones</span><span class="sxs-lookup"><span data-stu-id="514cc-184">Remarks</span></span>

<span data-ttu-id="514cc-185">Por lo general, un estado de advertencia se produce antes de un estado bajo, pero no se debe suponer que lo sea.</span><span class="sxs-lookup"><span data-stu-id="514cc-185">Generally, a warning state occurs before a low state, but you should not assume it will.</span></span> <span data-ttu-id="514cc-186">Es posible sondear una batería y detectar que no se ha producido el nivel de alerta y, a continuación, volver a sondear la batería y encontrarla descargada en la medida en que se hayan conseguido ambos niveles.</span><span class="sxs-lookup"><span data-stu-id="514cc-186">It is possible to poll a battery and find that neither alert level has occurred, and poll the battery again and find it discharged to the extent that both levels have been achieved.</span></span> <span data-ttu-id="514cc-187">Esto puede indicar que no está sondeando a menudo lo suficiente.</span><span class="sxs-lookup"><span data-stu-id="514cc-187">This may indicate that you are not polling often enough.</span></span> <span data-ttu-id="514cc-188">También puede indicar que la batería no puede ocupar mucho tiempo y se está descargando más rápidamente de lo esperado.</span><span class="sxs-lookup"><span data-stu-id="514cc-188">It may also indicate that the battery is unable to hold a charge for very long and is discharging more rapidly than you expected.</span></span> <span data-ttu-id="514cc-189">Es posible que esta batería esté llegando al final de su vida útil o que esté dañada.</span><span class="sxs-lookup"><span data-stu-id="514cc-189">Such a battery may be nearing the end of its useful life, or it may be damaged.</span></span>

## <a name="requirements"></a><span data-ttu-id="514cc-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="514cc-190">Requirements</span></span>



| <span data-ttu-id="514cc-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="514cc-191">Requirement</span></span> | <span data-ttu-id="514cc-192">Value</span><span class="sxs-lookup"><span data-stu-id="514cc-192">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="514cc-193">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="514cc-193">Minimum supported client</span></span><br/> | <span data-ttu-id="514cc-194">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="514cc-194">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="514cc-195">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="514cc-195">Minimum supported server</span></span><br/> | <span data-ttu-id="514cc-196">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="514cc-196">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="514cc-197">Encabezado</span><span class="sxs-lookup"><span data-stu-id="514cc-197">Header</span></span><br/>                   | <dl> <span data-ttu-id="514cc-198"><dt>Poclass. h; </dt> <dt>Batclass. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="514cc-198"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="514cc-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="514cc-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="514cc-200">**\_información de \_ consulta de batería ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="514cc-200">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> </dl>

 

 




