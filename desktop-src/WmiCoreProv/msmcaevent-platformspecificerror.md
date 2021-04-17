---
description: Indica un error específico de la plataforma de la arquitectura de comprobación de la máquina (MCA). Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: 409641d5-3451-4d26-88d1-bfd0e55db257
title: MSMCAEvent_PlatformSpecificError (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PlatformSpecificError
- MSMCAEvent_PlatformSpecificError.Active
- MSMCAEvent_PlatformSpecificError.AdditionalErrors
- MSMCAEvent_PlatformSpecificError.Cpu
- MSMCAEvent_PlatformSpecificError.ErrorSeverity
- MSMCAEvent_PlatformSpecificError.InstanceName
- MSMCAEvent_PlatformSpecificError.OEM_COMPONENT_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_BUS_SPECIFIC_DATA
- MSMCAEvent_PlatformSpecificError.PLATFORM_ERROR_STATUS
- MSMCAEvent_PlatformSpecificError.PLATFORM_REQUESTOR_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_RESPONDER_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_TARGET_ID
- MSMCAEvent_PlatformSpecificError.RawRecord
- MSMCAEvent_PlatformSpecificError.RecordId
- MSMCAEvent_PlatformSpecificError.Size
- MSMCAEvent_PlatformSpecificError.Type
- MSMCAEvent_PlatformSpecificError.VALIDATION_BITS
- MSMCAEvent_PlatformSpecificError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 51993c8c41206dac8f4c944d24fa59ae7b689f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497435"
---
# <a name="msmcaevent_platformspecificerror-class"></a><span data-ttu-id="67ffe-104">MSMCAEvent \_ PlatformSpecificError (clase)</span><span class="sxs-lookup"><span data-stu-id="67ffe-104">MSMCAEvent\_PlatformSpecificError class</span></span>

<span data-ttu-id="67ffe-105">La clase **MSMCAEvent \_ PlatformSpecificError** indica un error específico de la plataforma de la arquitectura de comprobación de equipo (MCA).</span><span class="sxs-lookup"><span data-stu-id="67ffe-105">The **MSMCAEvent\_PlatformSpecificError** class indicates a Machine Check Architecture (MCA) platform-specific error.</span></span> <span data-ttu-id="67ffe-106">Esta clase solo está disponible en sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="67ffe-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="67ffe-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="67ffe-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="67ffe-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="67ffe-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ffe-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67ffe-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PlatformSpecificError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   OEM_COMPONENT_ID;
  uint64  PLATFORM_BUS_SPECIFIC_DATA;
  uint64  PLATFORM_ERROR_STATUS;
  uint64  PLATFORM_REQUESTOR_ID;
  uint64  PLATFORM_RESPONDER_ID;
  uint64  PLATFORM_TARGET_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="67ffe-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="67ffe-110">Members</span></span>

<span data-ttu-id="67ffe-111">La clase **MSMCAEvent \_ PlatformSpecificError** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="67ffe-111">The **MSMCAEvent\_PlatformSpecificError** class has these types of members:</span></span>

-   [<span data-ttu-id="67ffe-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67ffe-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67ffe-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67ffe-113">Properties</span></span>

<span data-ttu-id="67ffe-114">La clase **MSMCAEvent \_ PlatformSpecificError** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="67ffe-114">The **MSMCAEvent\_PlatformSpecificError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67ffe-115">**Activo**</span><span class="sxs-lookup"><span data-stu-id="67ffe-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-116">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="67ffe-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-118">**True** si esta instancia de la clase está activa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="67ffe-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="67ffe-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="67ffe-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67ffe-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-122">Número de errores adicionales en el registro.</span><span class="sxs-lookup"><span data-stu-id="67ffe-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="67ffe-123">**CPU**</span><span class="sxs-lookup"><span data-stu-id="67ffe-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67ffe-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-126">CPU que ha detectado el error.</span><span class="sxs-lookup"><span data-stu-id="67ffe-126">CPU that reported the error.</span></span> <span data-ttu-id="67ffe-127">Esta propiedad solo se aplica a un sistema de varios procesadores en el que el primer procesador tiene asignado el número 0, el segundo procesador tiene asignado el número 1 y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="67ffe-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="67ffe-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="67ffe-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-129">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="67ffe-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-131">Nivel de gravedad del error comunicado.</span><span class="sxs-lookup"><span data-stu-id="67ffe-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="67ffe-132">Value</span><span class="sxs-lookup"><span data-stu-id="67ffe-132">Value</span></span>                                                                                                | <span data-ttu-id="67ffe-133">Significado</span><span class="sxs-lookup"><span data-stu-id="67ffe-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="67ffe-134"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="67ffe-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="67ffe-135">Recuperable</span><span class="sxs-lookup"><span data-stu-id="67ffe-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="67ffe-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="67ffe-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="67ffe-137">Crítico</span><span class="sxs-lookup"><span data-stu-id="67ffe-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="67ffe-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="67ffe-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="67ffe-139">Corregible</span><span class="sxs-lookup"><span data-stu-id="67ffe-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="67ffe-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="67ffe-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67ffe-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-143">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="67ffe-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-144">Identificador único de esta instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="67ffe-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="67ffe-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="67ffe-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67ffe-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-148">Si es 0 (cero), este evento no se registra en el registro de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="67ffe-148">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="67ffe-149">**\_identificador del componente OEM \_**</span><span class="sxs-lookup"><span data-stu-id="67ffe-149">**OEM\_COMPONENT\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-150">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="67ffe-150">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-152">Identificador único del componente que informa del error.</span><span class="sxs-lookup"><span data-stu-id="67ffe-152">Unique identifier of the component that reports the error.</span></span>

</dd> <dt>

<span data-ttu-id="67ffe-153">**\_ \_ datos específicos de Platform bus \_**</span><span class="sxs-lookup"><span data-stu-id="67ffe-153">**PLATFORM\_BUS\_SPECIFIC\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-154">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="67ffe-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-156">Datos específicos del bus de OEM.</span><span class="sxs-lookup"><span data-stu-id="67ffe-156">OEM-specific, bus-dependent data.</span></span>

<span data-ttu-id="67ffe-157">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67ffe-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="67ffe-158">**\_Estado de error de plataforma \_**</span><span class="sxs-lookup"><span data-stu-id="67ffe-158">**PLATFORM\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-159">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="67ffe-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-161">Estado de error de plataforma genérica.</span><span class="sxs-lookup"><span data-stu-id="67ffe-161">Generic platform error status.</span></span>

<span data-ttu-id="67ffe-162">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67ffe-162">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="67ffe-163">**identificador del solicitante de plataforma \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67ffe-163">**PLATFORM\_REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-164">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="67ffe-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-166">Identificador del solicitante en el momento del evento.</span><span class="sxs-lookup"><span data-stu-id="67ffe-166">Requestor identifier at the time of the event.</span></span>

<span data-ttu-id="67ffe-167">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67ffe-167">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="67ffe-168">**\_identificador del respondedor de plataforma \_**</span><span class="sxs-lookup"><span data-stu-id="67ffe-168">**PLATFORM\_RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-169">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="67ffe-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-171">Identificador del respondedor en el momento del evento.</span><span class="sxs-lookup"><span data-stu-id="67ffe-171">Responder identifier at the time of the event.</span></span>

<span data-ttu-id="67ffe-172">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67ffe-172">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="67ffe-173">**\_identificador de destino de la plataforma \_**</span><span class="sxs-lookup"><span data-stu-id="67ffe-173">**PLATFORM\_TARGET\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-174">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="67ffe-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-176">Identificador de destino en el momento del evento.</span><span class="sxs-lookup"><span data-stu-id="67ffe-176">Target identifier at the time of the event.</span></span>

<span data-ttu-id="67ffe-177">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67ffe-177">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="67ffe-178">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="67ffe-178">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-179">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="67ffe-179">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-181">Matriz de bytes que contiene el registro de errores sin procesar tal y como se presenta en Windows por la capa de abstracción del sistema (SAL).</span><span class="sxs-lookup"><span data-stu-id="67ffe-181">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="67ffe-182">La propiedad **size** especifica el número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="67ffe-182">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="67ffe-183">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="67ffe-183">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-184">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="67ffe-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-186">Identificador de registro del registro de errores para este error.</span><span class="sxs-lookup"><span data-stu-id="67ffe-186">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="67ffe-187">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67ffe-187">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="67ffe-188">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="67ffe-188">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-189">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67ffe-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-191">Tamaño del registro de errores sin procesar.</span><span class="sxs-lookup"><span data-stu-id="67ffe-191">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="67ffe-192">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="67ffe-192">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-193">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67ffe-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-195">Tipo de mensaje de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="67ffe-195">Type of event log message.</span></span> <span data-ttu-id="67ffe-196">Estos mensajes se corresponden con los códigos de mensaje de registro de eventos utilizados para insertar mensajes de registro de eventos del proveedor de consumidores del registro de eventos de Windows cuando recibe uno de los eventos.</span><span class="sxs-lookup"><span data-stu-id="67ffe-196">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="67ffe-197">**BITS de validación \_**</span><span class="sxs-lookup"><span data-stu-id="67ffe-197">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffe-198">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="67ffe-198">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67ffe-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67ffe-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffe-200">Bits de validación que se usan para indicar la validez de los campos siguientes.</span><span class="sxs-lookup"><span data-stu-id="67ffe-200">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="67ffe-201">Value</span><span class="sxs-lookup"><span data-stu-id="67ffe-201">Value</span></span>                                                                                                                                         | <span data-ttu-id="67ffe-202">Significado</span><span class="sxs-lookup"><span data-stu-id="67ffe-202">Meaning</span></span>                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <span data-ttu-id="67ffe-203"><dt>**1 0x1**</dt></span><span class="sxs-lookup"><span data-stu-id="67ffe-203"><dt>**1 0x1**</dt></span></span> </dl>          | <span data-ttu-id="67ffe-204">**Plataforma \_ de El \_ Estado de error** es válido.</span><span class="sxs-lookup"><span data-stu-id="67ffe-204">**PLATFORM\_ERROR\_STATUS** is valid.</span></span><br/>            |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <span data-ttu-id="67ffe-205"><dt>**2 0X2**</dt></span><span class="sxs-lookup"><span data-stu-id="67ffe-205"><dt>**2 0x2**</dt></span></span> </dl>          | <span data-ttu-id="67ffe-206">**Plataforma \_ de El \_ \_ identificador del solicitante de errores** es válido.</span><span class="sxs-lookup"><span data-stu-id="67ffe-206">**PLATFORM\_ERROR\_REQUESTOR\_ID** is valid.</span></span><br/>     |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <span data-ttu-id="67ffe-207"><dt>**4 0x4**</dt></span><span class="sxs-lookup"><span data-stu-id="67ffe-207"><dt>**4 0x4**</dt></span></span> </dl>          | <span data-ttu-id="67ffe-208">**Plataforma \_ de El \_ \_ identificador del respondedor de errores** es válido.</span><span class="sxs-lookup"><span data-stu-id="67ffe-208">**PLATFORM\_ERROR\_RESPONDER\_ID** is valid.</span></span><br/>     |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <span data-ttu-id="67ffe-209"><dt>**8 0x8**</dt></span><span class="sxs-lookup"><span data-stu-id="67ffe-209"><dt>**8 0x8**</dt></span></span> </dl>          | <span data-ttu-id="67ffe-210">**Plataforma \_ de El \_ \_ ID** . de destino del error es válido.</span><span class="sxs-lookup"><span data-stu-id="67ffe-210">**PLATFORM\_ERROR\_TARGET\_ID** is valid.</span></span><br/>        |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <span data-ttu-id="67ffe-211"><dt>**16 0x10**</dt></span><span class="sxs-lookup"><span data-stu-id="67ffe-211"><dt>**16 0x10**</dt></span></span> </dl>    | <span data-ttu-id="67ffe-212">**Plataforma \_ de Los \_ \_ datos específicos del error** son válidos.</span><span class="sxs-lookup"><span data-stu-id="67ffe-212">**PLATFORM\_ERROR\_SPECIFIC\_DATA** is valid.</span></span><br/>    |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <span data-ttu-id="67ffe-213"><dt>**32 0x20**</dt></span><span class="sxs-lookup"><span data-stu-id="67ffe-213"><dt>**32 0x20**</dt></span></span> </dl>    | <span data-ttu-id="67ffe-214">**Plataforma \_ de El \_ \_ ID** . de OEM del error es válido.</span><span class="sxs-lookup"><span data-stu-id="67ffe-214">**PLATFORM\_ERROR\_OEM\_ID** is valid.</span></span><br/>           |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <span data-ttu-id="67ffe-215"><dt>**64 0x40**</dt></span><span class="sxs-lookup"><span data-stu-id="67ffe-215"><dt>**64 0x40**</dt></span></span> </dl>    | <span data-ttu-id="67ffe-216">**Plataforma \_ de ERROR \_ el \_ \_ struct de datos OEM** es válido.</span><span class="sxs-lookup"><span data-stu-id="67ffe-216">**PLATFORM\_ERROR\_OEM\_DATA\_STRUCT** is valid.</span></span><br/> |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <span data-ttu-id="67ffe-217"><dt>**128 0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="67ffe-217"><dt>**128 0x80**</dt></span></span> </dl> | <span data-ttu-id="67ffe-218">**Plataforma \_ de ERROR: la \_ \_ ruta de \_ acceso del dispositivo OEM** es válida.</span><span class="sxs-lookup"><span data-stu-id="67ffe-218">**PLATFORM\_ERROR\_OEM\_DEVICE\_PATH** is valid.</span></span><br/> |



 

<span data-ttu-id="67ffe-219">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67ffe-219">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67ffe-220">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67ffe-220">Remarks</span></span>

<span data-ttu-id="67ffe-221">La clase **MSMCAEvent \_ PlatformSpecificError** se deriva de [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="67ffe-221">The **MSMCAEvent\_PlatformSpecificError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67ffe-222">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67ffe-222">Requirements</span></span>



| <span data-ttu-id="67ffe-223">Requisito</span><span class="sxs-lookup"><span data-stu-id="67ffe-223">Requirement</span></span> | <span data-ttu-id="67ffe-224">Value</span><span class="sxs-lookup"><span data-stu-id="67ffe-224">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67ffe-225">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67ffe-225">Minimum supported client</span></span><br/> | <span data-ttu-id="67ffe-226">Windows XP</span><span class="sxs-lookup"><span data-stu-id="67ffe-226">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="67ffe-227">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67ffe-227">Minimum supported server</span></span><br/> | <span data-ttu-id="67ffe-228">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="67ffe-228">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="67ffe-229">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="67ffe-229">Namespace</span></span><br/>                | <span data-ttu-id="67ffe-230">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="67ffe-230">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="67ffe-231">MOF</span><span class="sxs-lookup"><span data-stu-id="67ffe-231">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67ffe-232"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67ffe-232"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="67ffe-233">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="67ffe-233">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67ffe-234"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67ffe-234"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67ffe-235">Vea también</span><span class="sxs-lookup"><span data-stu-id="67ffe-235">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ffe-236">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="67ffe-236">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="67ffe-237">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="67ffe-237">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

