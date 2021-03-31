---
description: Representa un error de bus PCI de arquitectura de comprobación de equipo (MCA). Esta clase solo está disponible para los equipos que se ejecutan en un sistema operativo Windows de 64 bits.
ms.assetid: d8995909-a91b-4fcc-a37f-011d8df95ce8
title: MSMCAEvent_PCIBusError (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIBusError
- MSMCAEvent_PCIBusError.Active
- MSMCAEvent_PCIBusError.AdditionalErrors
- MSMCAEvent_PCIBusError.Cpu
- MSMCAEvent_PCIBusError.ErrorSeverity
- MSMCAEvent_PCIBusError.InstanceName
- MSMCAEvent_PCIBusError.PCI_BUS_ADDRESS
- MSMCAEvent_PCIBusError.PCI_BUS_CMD
- MSMCAEvent_PCIBusError.PCI_BUS_DATA
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_STATUS
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_TYPE
- MSMCAEvent_PCIBusError.PCI_BUS_ID_BusNumber
- MSMCAEvent_PCIBusError.PCI_BUS_ID_SegmentNumber
- MSMCAEvent_PCIBusError.PCI_BUS_REQUESTOR_ID
- MSMCAEvent_PCIBusError.PCI_BUS_RESPONDER_ID
- MSMCAEvent_PCIBusError.RawRecord
- MSMCAEvent_PCIBusError.RecordId
- MSMCAEvent_PCIBusError.Size
- MSMCAEvent_PCIBusError.Type
- MSMCAEvent_PCIBusError.VALIDATION_BITS
- MSMCAEvent_PCIBusError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 7f2b800a07c0b979468a5df5a8be67e6adee39de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809686"
---
# <a name="msmcaevent_pcibuserror-class"></a><span data-ttu-id="4e600-104">MSMCAEvent \_ PCIBusError (clase)</span><span class="sxs-lookup"><span data-stu-id="4e600-104">MSMCAEvent\_PCIBusError class</span></span>

<span data-ttu-id="4e600-105">La clase **MSMCAEvent \_ PCIBusError** representa un error de bus PCI de arquitectura de comprobación de equipo (MCA).</span><span class="sxs-lookup"><span data-stu-id="4e600-105">The **MSMCAEvent\_PCIBusError** class represents a Machine Check Architecture (MCA) PCI bus error.</span></span> <span data-ttu-id="4e600-106">Esta clase solo está disponible para los equipos que se ejecutan en un sistema operativo Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4e600-106">This class is available only for computers running on a 64-bit Windows operating system.</span></span>

<span data-ttu-id="4e600-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4e600-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4e600-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="4e600-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e600-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e600-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PCIBusError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_BUS_ADDRESS;
  uint64  PCI_BUS_CMD;
  uint64  PCI_BUS_DATA;
  uint64  PCI_BUS_ERROR_STATUS;
  uint16  PCI_BUS_ERROR_TYPE;
  uint8   PCI_BUS_ID_BusNumber;
  uint8   PCI_BUS_ID_SegmentNumber;
  uint64  PCI_BUS_REQUESTOR_ID;
  uint64  PCI_BUS_RESPONDER_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="4e600-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="4e600-110">Members</span></span>

<span data-ttu-id="4e600-111">La clase **MSMCAEvent \_ PCIBusError** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4e600-111">The **MSMCAEvent\_PCIBusError** class has these types of members:</span></span>

-   [<span data-ttu-id="4e600-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4e600-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4e600-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4e600-113">Properties</span></span>

<span data-ttu-id="4e600-114">La clase **MSMCAEvent \_ PCIBusError** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4e600-114">The **MSMCAEvent\_PCIBusError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e600-115">**Activo**</span><span class="sxs-lookup"><span data-stu-id="4e600-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-116">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4e600-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-118">**True** si esta instancia de la clase está activa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="4e600-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4e600-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="4e600-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e600-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-122">Número de errores adicionales en el registro.</span><span class="sxs-lookup"><span data-stu-id="4e600-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="4e600-123">**CPU**</span><span class="sxs-lookup"><span data-stu-id="4e600-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e600-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-126">CPU que ha detectado el error.</span><span class="sxs-lookup"><span data-stu-id="4e600-126">CPU that reported the error.</span></span> <span data-ttu-id="4e600-127">Esta propiedad solo se aplica a un sistema de varios procesadores en el que el primer procesador tiene asignado el número 0, el segundo procesador tiene asignado el número 1 y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="4e600-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="4e600-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="4e600-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-129">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="4e600-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-131">Nivel de gravedad del error comunicado.</span><span class="sxs-lookup"><span data-stu-id="4e600-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="4e600-132">Value</span><span class="sxs-lookup"><span data-stu-id="4e600-132">Value</span></span>                                                                                                | <span data-ttu-id="4e600-133">Significado</span><span class="sxs-lookup"><span data-stu-id="4e600-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="4e600-134"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="4e600-135">Recuperable</span><span class="sxs-lookup"><span data-stu-id="4e600-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="4e600-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4e600-137">Crítico</span><span class="sxs-lookup"><span data-stu-id="4e600-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="4e600-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4e600-139">Corregible</span><span class="sxs-lookup"><span data-stu-id="4e600-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4e600-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="4e600-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e600-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e600-143">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4e600-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4e600-144">Identificador único de esta instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="4e600-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="4e600-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="4e600-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e600-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-148">Si es 0 (cero), este evento no se registra en el registro de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="4e600-148">If 0 (zero), then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="4e600-149">**\_dirección del bus PCI \_**</span><span class="sxs-lookup"><span data-stu-id="4e600-149">**PCI\_BUS\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-150">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4e600-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-152">Memoria o dirección de e/s en el bus PCI en el momento del evento.</span><span class="sxs-lookup"><span data-stu-id="4e600-152">Memory or I/O address on the PCI bus at the time of the event.</span></span>

<span data-ttu-id="4e600-153">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4e600-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4e600-154">**\_cmd de bus PCI \_**</span><span class="sxs-lookup"><span data-stu-id="4e600-154">**PCI\_BUS\_CMD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-155">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4e600-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-157">Comando u operación de bus en el momento del evento.</span><span class="sxs-lookup"><span data-stu-id="4e600-157">Bus command or operation at the time of the event.</span></span>

<span data-ttu-id="4e600-158">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4e600-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4e600-159">**\_datos de bus PCI \_**</span><span class="sxs-lookup"><span data-stu-id="4e600-159">**PCI\_BUS\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-160">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4e600-160">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-162">Datos en el bus PCI en el momento del evento.</span><span class="sxs-lookup"><span data-stu-id="4e600-162">Data on the PCI bus at the time of the event.</span></span>

<span data-ttu-id="4e600-163">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4e600-163">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4e600-164">**\_Estado de \_ error de bus PCI \_**</span><span class="sxs-lookup"><span data-stu-id="4e600-164">**PCI\_BUS\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-165">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4e600-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-167">Estado del bus en el momento del error.</span><span class="sxs-lookup"><span data-stu-id="4e600-167">Bus status at the time of the error.</span></span>

<span data-ttu-id="4e600-168">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4e600-168">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4e600-169">**\_tipo de \_ error de bus PCI \_**</span><span class="sxs-lookup"><span data-stu-id="4e600-169">**PCI\_BUS\_ERROR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-170">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e600-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-172">Tipo de error de bus PCI.</span><span class="sxs-lookup"><span data-stu-id="4e600-172">Type of PCI bus error.</span></span>



| <span data-ttu-id="4e600-173">Value</span><span class="sxs-lookup"><span data-stu-id="4e600-173">Value</span></span>                                                                                                | <span data-ttu-id="4e600-174">Significado</span><span class="sxs-lookup"><span data-stu-id="4e600-174">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="4e600-175"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-175"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="4e600-176">Error específico del sistema OEM o desconocido.</span><span class="sxs-lookup"><span data-stu-id="4e600-176">Unknown or OEM System Specific Error.</span></span><br/>            |
| <span id="1"></span><dl> <span data-ttu-id="4e600-177"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-177"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4e600-178">Error de paridad de datos.</span><span class="sxs-lookup"><span data-stu-id="4e600-178">Data Parity Error.</span></span><br/>                               |
| <span id="2"></span><dl> <span data-ttu-id="4e600-179"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-179"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4e600-180">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="4e600-180">System Error.</span></span><br/>                                    |
| <span id="3"></span><dl> <span data-ttu-id="4e600-181"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-181"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="4e600-182">Anulación maestra.</span><span class="sxs-lookup"><span data-stu-id="4e600-182">Master Abort.</span></span><br/>                                    |
| <span id="4"></span><dl> <span data-ttu-id="4e600-183"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-183"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="4e600-184">Tiempo de espera de bus agotado o no hay ningún dispositivo presente (NO DEVSEL \# ).</span><span class="sxs-lookup"><span data-stu-id="4e600-184">Bus Time Out or No Device Present (NO DEVSEL\#).</span></span><br/> |
| <span id="5"></span><dl> <span data-ttu-id="4e600-185"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-185"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="4e600-186">Error de paridad de datos maestros.</span><span class="sxs-lookup"><span data-stu-id="4e600-186">Master Data Parity Error.</span></span><br/>                        |
| <span id="6"></span><dl> <span data-ttu-id="4e600-187"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-187"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="4e600-188">Error de paridad de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4e600-188">Address Parity Error.</span></span><br/>                            |
| <span id="7"></span><dl> <span data-ttu-id="4e600-189"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-189"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="4e600-190">Error de paridad de comandos.</span><span class="sxs-lookup"><span data-stu-id="4e600-190">Command Parity Error.</span></span><br/>                            |



 

</dd> <dt>

<span data-ttu-id="4e600-191">**\_Identificador de bus PCI \_ \_ BusNumber**</span><span class="sxs-lookup"><span data-stu-id="4e600-191">**PCI\_BUS\_ID\_BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-192">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="4e600-192">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-194">Identificador designado para el bus PCI que encontró el error.</span><span class="sxs-lookup"><span data-stu-id="4e600-194">Designated identifier for the PCI bus that encountered the error.</span></span>

</dd> <dt>

<span data-ttu-id="4e600-195">**\_Identificador de bus PCI \_ \_ SegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="4e600-195">**PCI\_BUS\_ID\_SegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-196">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="4e600-196">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-198">Identificador de segmento designado para el bus PCI que detectó el error.</span><span class="sxs-lookup"><span data-stu-id="4e600-198">Designated segment identifier for the PCI bus that encountered the error.</span></span>

</dd> <dt>

<span data-ttu-id="4e600-199">**\_identificador del \_ solicitante de bus PCI \_**</span><span class="sxs-lookup"><span data-stu-id="4e600-199">**PCI\_BUS\_REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-200">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4e600-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-202">Identificador del solicitante del bus PCI en el momento del evento.</span><span class="sxs-lookup"><span data-stu-id="4e600-202">PCI Bus requestor identifier at the time of the event.</span></span>

<span data-ttu-id="4e600-203">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4e600-203">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4e600-204">**\_identificador del \_ respondedor de bus PCI \_**</span><span class="sxs-lookup"><span data-stu-id="4e600-204">**PCI\_BUS\_RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-205">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4e600-205">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-207">Identificador del respondedor de bus PCI en el momento del evento.</span><span class="sxs-lookup"><span data-stu-id="4e600-207">PCI Bus Responder identifier at the time of the event.</span></span>

<span data-ttu-id="4e600-208">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4e600-208">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4e600-209">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="4e600-209">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-210">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="4e600-210">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4e600-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-212">Matriz de bytes que contiene el registro de errores sin procesar tal y como se presenta en Windows por la capa de abstracción del sistema (SAL).</span><span class="sxs-lookup"><span data-stu-id="4e600-212">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="4e600-213">La propiedad **size** especifica el número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="4e600-213">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="4e600-214">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="4e600-214">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-215">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4e600-215">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-217">Identificador de registro del registro de errores para este error.</span><span class="sxs-lookup"><span data-stu-id="4e600-217">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="4e600-218">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4e600-218">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4e600-219">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="4e600-219">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-220">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e600-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-222">Tamaño del registro de errores sin procesar.</span><span class="sxs-lookup"><span data-stu-id="4e600-222">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="4e600-223">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4e600-223">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-224">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e600-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-226">Tipo de mensaje de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="4e600-226">Type of event log message.</span></span> <span data-ttu-id="4e600-227">Estos mensajes se corresponden con los códigos de mensaje de registro de eventos utilizados para insertar mensajes de registro de eventos del proveedor de consumidores del registro de eventos de Windows cuando recibe uno de los eventos.</span><span class="sxs-lookup"><span data-stu-id="4e600-227">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="4e600-228">**BITS de validación \_**</span><span class="sxs-lookup"><span data-stu-id="4e600-228">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e600-229">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4e600-229">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4e600-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e600-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e600-231">Bits de validación que se usan para indicar la validez de los campos siguientes.</span><span class="sxs-lookup"><span data-stu-id="4e600-231">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="4e600-232">Valores</span><span class="sxs-lookup"><span data-stu-id="4e600-232">Values</span></span>                                                                                  | <span data-ttu-id="4e600-233">Significado</span><span class="sxs-lookup"><span data-stu-id="4e600-233">Meaning</span></span>                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="4e600-234"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-234"><dt>1 (0x1)</dt></span></span> </dl>      | <span data-ttu-id="4e600-235">El \_ Estado de error de bus PCI \_ \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="4e600-235">PCI\_BUS\_ERROR\_STATUS is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="4e600-236"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-236"><dt>2 (0x2)</dt></span></span> </dl>      | <span data-ttu-id="4e600-237">El \_ tipo de error de bus PCI \_ \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="4e600-237">PCI\_BUS\_ERROR\_TYPE is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="4e600-238"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-238"><dt>4 (0x4)</dt></span></span> </dl>      | <span data-ttu-id="4e600-239">El \_ ID. de bus PCI \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="4e600-239">PCI\_BUS\_ID is valid.</span></span><br/>                |
| <dl> <span data-ttu-id="4e600-240"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-240"><dt>8 (0x8)</dt></span></span> </dl>      | <span data-ttu-id="4e600-241">La \_ dirección del bus PCI \_ es válida.</span><span class="sxs-lookup"><span data-stu-id="4e600-241">PCI\_BUS\_ADDRESS is valid.</span></span><br/>           |
| <dl> <span data-ttu-id="4e600-242"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-242"><dt>16 (0x10)</dt></span></span> </dl>    | <span data-ttu-id="4e600-243">Los \_ datos del bus PCI \_ son válidos.</span><span class="sxs-lookup"><span data-stu-id="4e600-243">PCI\_BUS\_DATA is valid.</span></span><br/>              |
| <dl> <span data-ttu-id="4e600-244"><dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-244"><dt>32 (0x20)</dt></span></span> </dl>    | <span data-ttu-id="4e600-245">\_Cmd de bus PCI \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="4e600-245">PCI\_BUS\_CMD is valid.</span></span><br/>               |
| <dl> <span data-ttu-id="4e600-246"><dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-246"><dt>64 (0x40)</dt></span></span> </dl>    | <span data-ttu-id="4e600-247">El \_ identificador del solicitante del bus PCI \_ \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="4e600-247">PCI\_BUS\_REQUESTOR\_ID is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="4e600-248"><dt>128 (0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-248"><dt>128 (0x80)</dt></span></span> </dl>   | <span data-ttu-id="4e600-249">El \_ identificador del respondedor de bus PCI \_ \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="4e600-249">PCI\_BUS\_RESPONDER\_ID is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="4e600-250"><dt>256 (0x100)</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-250"><dt>256 (0x100)</dt></span></span> </dl>  | <span data-ttu-id="4e600-251">El \_ ID. de destino del bus PCI \_ \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="4e600-251">PCI\_BUS\_TARGET\_ID is valid.</span></span><br/>        |
| <dl> <span data-ttu-id="4e600-252"><dt>512 (0x200)</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-252"><dt>512 (0x200)</dt></span></span> </dl>  | <span data-ttu-id="4e600-253">El \_ ID. de OEM del bus PCI \_ \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="4e600-253">PCI\_BUS\_OEM\_ID is valid.</span></span><br/>           |
| <dl> <span data-ttu-id="4e600-254"><dt>1024 (0x400)</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-254"><dt>1024 (0x400)</dt></span></span> </dl> | <span data-ttu-id="4e600-255">La \_ estructura de datos OEM del bus PCI \_ \_ \_ es válida.</span><span class="sxs-lookup"><span data-stu-id="4e600-255">PCI\_BUS\_OEM\_DATA\_STRUCT is valid.</span></span><br/> |



 

<span data-ttu-id="4e600-256">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4e600-256">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e600-257">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e600-257">Remarks</span></span>

<span data-ttu-id="4e600-258">La clase **MSMCAEvent \_ PCIBusError** se deriva de [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="4e600-258">The **MSMCAEvent\_PCIBusError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e600-259">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e600-259">Requirements</span></span>



| <span data-ttu-id="4e600-260">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e600-260">Requirement</span></span> | <span data-ttu-id="4e600-261">Value</span><span class="sxs-lookup"><span data-stu-id="4e600-261">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e600-262">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e600-262">Minimum supported client</span></span><br/> | <span data-ttu-id="4e600-263">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4e600-263">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="4e600-264">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e600-264">Minimum supported server</span></span><br/> | <span data-ttu-id="4e600-265">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4e600-265">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="4e600-266">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4e600-266">Namespace</span></span><br/>                | <span data-ttu-id="4e600-267">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="4e600-267">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="4e600-268">MOF</span><span class="sxs-lookup"><span data-stu-id="4e600-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e600-269"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-269"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e600-270">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e600-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e600-271"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e600-271"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e600-272">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e600-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e600-273">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="4e600-273">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="4e600-274">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="4e600-274">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

