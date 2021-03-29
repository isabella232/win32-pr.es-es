---
description: Indica que se ha producido un evento del sistema de la interfaz de administración de plataforma inteligente (IPMI). El error se escribe en el registro de eventos del sistema de SMBIOS (SEL). Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: 1964f850-ac55-4639-9205-2eb0996dbaae
title: MSMCAEvent_SystemEventError (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SystemEventError
- MSMCAEvent_SystemEventError.Active
- MSMCAEvent_SystemEventError.AdditionalErrors
- MSMCAEvent_SystemEventError.Cpu
- MSMCAEvent_SystemEventError.ErrorSeverity
- MSMCAEvent_SystemEventError.InstanceName
- MSMCAEvent_SystemEventError.RawRecord
- MSMCAEvent_SystemEventError.RecordId
- MSMCAEvent_SystemEventError.SEL_DATA1
- MSMCAEvent_SystemEventError.SEL_DATA2
- MSMCAEvent_SystemEventError.SEL_DATA3
- MSMCAEvent_SystemEventError.SEL_EVENT_DIR_TYPE
- MSMCAEvent_SystemEventError.SEL_EVM_REV
- MSMCAEvent_SystemEventError.SEL_GENERATOR_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_TYPE
- MSMCAEvent_SystemEventError.SEL_SENSOR_NUM
- MSMCAEvent_SystemEventError.SEL_SENSOR_TYPE
- MSMCAEvent_SystemEventError.SEL_TIME_STAMP
- MSMCAEvent_SystemEventError.Size
- MSMCAEvent_SystemEventError.Type
- MSMCAEvent_SystemEventError.VALIDATION_BITS
- MSMCAEvent_SystemEventError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f20f95fb5e1b1bf07b0f70c25d54122642b13569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648597"
---
# <a name="msmcaevent_systemeventerror-class"></a><span data-ttu-id="201a6-105">MSMCAEvent \_ SystemEventError (clase)</span><span class="sxs-lookup"><span data-stu-id="201a6-105">MSMCAEvent\_SystemEventError class</span></span>

<span data-ttu-id="201a6-106">La clase **MSMCAEvent \_ SystemEventError** indica que se ha producido un evento del sistema de la interfaz de administración de plataforma inteligente (IPMI).</span><span class="sxs-lookup"><span data-stu-id="201a6-106">The **MSMCAEvent\_SystemEventError** class indicates that an Intelligent Platform Management Interface (IPMI) system event has occurred.</span></span> <span data-ttu-id="201a6-107">El error se escribe en el registro de eventos del sistema de SMBIOS (SEL).</span><span class="sxs-lookup"><span data-stu-id="201a6-107">The error is written to the SMBIOS System Event Log (SEL).</span></span> <span data-ttu-id="201a6-108">Esta clase solo está disponible en sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="201a6-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="201a6-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="201a6-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="201a6-110">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="201a6-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="201a6-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="201a6-111">Syntax</span></span>

``` syntax
class MSMCAEvent_SystemEventError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint8   SEL_DATA1;
  uint8   SEL_DATA2;
  uint8   SEL_DATA3;
  uint8   SEL_EVENT_DIR_TYPE;
  uint8   SEL_EVM_REV;
  uint16  SEL_GENERATOR_ID;
  uint16  SEL_RECORD_ID;
  uint8   SEL_RECORD_TYPE;
  uint8   SEL_SENSOR_NUM;
  uint8   SEL_SENSOR_TYPE;
  uint64  SEL_TIME_STAMP;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="201a6-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="201a6-112">Members</span></span>

<span data-ttu-id="201a6-113">La clase **MSMCAEvent \_ SystemEventError** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="201a6-113">The **MSMCAEvent\_SystemEventError** class has these types of members:</span></span>

-   [<span data-ttu-id="201a6-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="201a6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="201a6-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="201a6-115">Properties</span></span>

<span data-ttu-id="201a6-116">La clase **MSMCAEvent \_ SystemEventError** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="201a6-116">The **MSMCAEvent\_SystemEventError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="201a6-117">**Activo**</span><span class="sxs-lookup"><span data-stu-id="201a6-117">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-118">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="201a6-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-120">**True** si esta instancia de la clase está activa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="201a6-120">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-121">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="201a6-121">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-122">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="201a6-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-124">Número de errores adicionales en el registro.</span><span class="sxs-lookup"><span data-stu-id="201a6-124">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-125">**CPU**</span><span class="sxs-lookup"><span data-stu-id="201a6-125">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-126">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="201a6-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-128">CPU que ha detectado el error.</span><span class="sxs-lookup"><span data-stu-id="201a6-128">CPU that reported the error.</span></span> <span data-ttu-id="201a6-129">Esta propiedad solo se aplica a un sistema de varios procesadores en el que el primer procesador tiene asignado el número 0, el segundo procesador tiene asignado el número 1 y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="201a6-129">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-130">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="201a6-130">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-131">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="201a6-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-133">Nivel de gravedad del error comunicado.</span><span class="sxs-lookup"><span data-stu-id="201a6-133">Severity level of the error reported.</span></span>



| <span data-ttu-id="201a6-134">Value</span><span class="sxs-lookup"><span data-stu-id="201a6-134">Value</span></span>                                                                                                | <span data-ttu-id="201a6-135">Significado</span><span class="sxs-lookup"><span data-stu-id="201a6-135">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="201a6-136"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="201a6-136"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="201a6-137">Recuperable</span><span class="sxs-lookup"><span data-stu-id="201a6-137">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="201a6-138"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="201a6-138"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="201a6-139">Crítico</span><span class="sxs-lookup"><span data-stu-id="201a6-139">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="201a6-140"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="201a6-140"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="201a6-141">Corregible</span><span class="sxs-lookup"><span data-stu-id="201a6-141">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="201a6-142">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="201a6-142">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="201a6-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="201a6-145">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="201a6-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="201a6-146">Identificador único de esta instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="201a6-146">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-147">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="201a6-147">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-148">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="201a6-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-150">Si es 0 (cero), este evento no se registra en el registro de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="201a6-150">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-151">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="201a6-151">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-152">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="201a6-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="201a6-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-154">Matriz de bytes que contiene el registro de errores sin procesar.</span><span class="sxs-lookup"><span data-stu-id="201a6-154">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="201a6-155">El número de elementos de la matriz que especifica la propiedad **size** .</span><span class="sxs-lookup"><span data-stu-id="201a6-155">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-156">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="201a6-156">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-157">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="201a6-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-159">Identificador de registro del registro de errores para este error.</span><span class="sxs-lookup"><span data-stu-id="201a6-159">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="201a6-160">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="201a6-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="201a6-161">**SEL \_ Data1**</span><span class="sxs-lookup"><span data-stu-id="201a6-161">**SEL\_DATA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-162">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="201a6-162">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-164">Campo de datos de evento 1.</span><span class="sxs-lookup"><span data-stu-id="201a6-164">Event data field 1.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-165">**SEL \_ DATA2**</span><span class="sxs-lookup"><span data-stu-id="201a6-165">**SEL\_DATA2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-166">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="201a6-166">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-168">Campo de datos de evento 2.</span><span class="sxs-lookup"><span data-stu-id="201a6-168">Event data field 2.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-169">**SEL \_ DATA3**</span><span class="sxs-lookup"><span data-stu-id="201a6-169">**SEL\_DATA3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-170">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="201a6-170">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-172">Campo de datos de evento 3.</span><span class="sxs-lookup"><span data-stu-id="201a6-172">Event data field 3.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-173">**\_tipo de \_ Directorio de evento SEL \_**</span><span class="sxs-lookup"><span data-stu-id="201a6-173">**SEL\_EVENT\_DIR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-174">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="201a6-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-176">Tipo de directorio de eventos.</span><span class="sxs-lookup"><span data-stu-id="201a6-176">Event directory type.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-177">**SEL \_ EVM \_ Rev**</span><span class="sxs-lookup"><span data-stu-id="201a6-177">**SEL\_EVM\_REV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-178">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="201a6-178">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-180">Versión de formato del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="201a6-180">Format version of the error message.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-181">**\_ID. de generador de SEL \_**</span><span class="sxs-lookup"><span data-stu-id="201a6-181">**SEL\_GENERATOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-182">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="201a6-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-184">Identificador de software, si el evento fue generado por software.</span><span class="sxs-lookup"><span data-stu-id="201a6-184">Software identifier, if the event was software-generated.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-185">**\_ID. de registro SEL \_**</span><span class="sxs-lookup"><span data-stu-id="201a6-185">**SEL\_RECORD\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-186">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="201a6-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-188">Identificador de registro utilizado para el acceso al registro de eventos del sistema (SEL) de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="201a6-188">Record identifier used for SMBIOS system event log (SEL) access.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-189">**\_tipo de registro SEL \_**</span><span class="sxs-lookup"><span data-stu-id="201a6-189">**SEL\_RECORD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-190">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="201a6-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-192">Tipo de registro.</span><span class="sxs-lookup"><span data-stu-id="201a6-192">Record type.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-193">**\_número de sensor SEL \_**</span><span class="sxs-lookup"><span data-stu-id="201a6-193">**SEL\_SENSOR\_NUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-194">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="201a6-194">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-196">Número de sensor que generó el evento.</span><span class="sxs-lookup"><span data-stu-id="201a6-196">Sensor number that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-197">**\_tipo de sensor SEL \_**</span><span class="sxs-lookup"><span data-stu-id="201a6-197">**SEL\_SENSOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-198">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="201a6-198">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-200">Código de tipo de sensor del sensor que generó el evento.</span><span class="sxs-lookup"><span data-stu-id="201a6-200">Sensor type code of the sensor that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-201">**\_marca de tiempo de SEL \_**</span><span class="sxs-lookup"><span data-stu-id="201a6-201">**SEL\_TIME\_STAMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-202">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="201a6-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-204">Marca de tiempo del registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="201a6-204">Timestamp of the event log.</span></span>

<span data-ttu-id="201a6-205">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="201a6-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="201a6-206">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="201a6-206">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-207">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="201a6-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-209">Tamaño del registro de errores sin procesar.</span><span class="sxs-lookup"><span data-stu-id="201a6-209">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-210">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="201a6-210">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-211">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="201a6-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-213">Tipo de mensaje de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="201a6-213">Type of event log message.</span></span> <span data-ttu-id="201a6-214">Estos mensajes se corresponden con los códigos de mensaje de registro de eventos utilizados para insertar mensajes de registro de eventos del proveedor de consumidores del registro de eventos de Windows cuando recibe uno de los eventos.</span><span class="sxs-lookup"><span data-stu-id="201a6-214">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="201a6-215">**BITS de validación \_**</span><span class="sxs-lookup"><span data-stu-id="201a6-215">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="201a6-216">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="201a6-216">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="201a6-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="201a6-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="201a6-218">Bits de validación que se usan para indicar la validez de los campos siguientes.</span><span class="sxs-lookup"><span data-stu-id="201a6-218">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="201a6-219">Value</span><span class="sxs-lookup"><span data-stu-id="201a6-219">Value</span></span>                                                                                                                                            | <span data-ttu-id="201a6-220">Significado</span><span class="sxs-lookup"><span data-stu-id="201a6-220">Meaning</span></span>                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <span data-ttu-id="201a6-221"><dt>**1 0x1**</dt></span><span class="sxs-lookup"><span data-stu-id="201a6-221"><dt>**1 0x1**</dt></span></span> </dl>             | <span data-ttu-id="201a6-222">**SEL \_ El \_ ID** . de registro es válido.</span><span class="sxs-lookup"><span data-stu-id="201a6-222">**SEL\_RECORD\_ID** is valid.</span></span><br/>    |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <span data-ttu-id="201a6-223"><dt>**2 0X2**</dt></span><span class="sxs-lookup"><span data-stu-id="201a6-223"><dt>**2 0x2**</dt></span></span> </dl>             | <span data-ttu-id="201a6-224">**SEL \_ El \_ tipo de registro** es válido.</span><span class="sxs-lookup"><span data-stu-id="201a6-224">**SEL\_RECORD\_TYPE** is valid.</span></span><br/>  |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <span data-ttu-id="201a6-225"><dt>**4 0x4**</dt></span><span class="sxs-lookup"><span data-stu-id="201a6-225"><dt>**4 0x4**</dt></span></span> </dl>             | <span data-ttu-id="201a6-226">**SEL \_ El \_ ID** . de generador es válido.</span><span class="sxs-lookup"><span data-stu-id="201a6-226">**SEL\_GENERATOR\_ID** is valid.</span></span><br/> |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <span data-ttu-id="201a6-227"><dt>**8 0x8**</dt></span><span class="sxs-lookup"><span data-stu-id="201a6-227"><dt>**8 0x8**</dt></span></span> </dl>             | <span data-ttu-id="201a6-228">**SEL \_ EVM \_ Rev** es válido.</span><span class="sxs-lookup"><span data-stu-id="201a6-228">**SEL\_EVM\_REV** is valid.</span></span><br/>      |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <span data-ttu-id="201a6-229"><dt>**16 0x10**</dt></span><span class="sxs-lookup"><span data-stu-id="201a6-229"><dt>**16 0x10**</dt></span></span> </dl>       | <span data-ttu-id="201a6-230">**SEL \_ El \_ tipo de sensor** es válido.</span><span class="sxs-lookup"><span data-stu-id="201a6-230">**SEL\_SENSOR\_TYPE** is valid.</span></span><br/>  |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <span data-ttu-id="201a6-231"><dt>**32 0x20**</dt></span><span class="sxs-lookup"><span data-stu-id="201a6-231"><dt>**32 0x20**</dt></span></span> </dl>       | <span data-ttu-id="201a6-232">**SEL \_ El \_ número de sensores** es válido.</span><span class="sxs-lookup"><span data-stu-id="201a6-232">**SEL\_SENSOR\_NUM** is valid.</span></span><br/>   |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <span data-ttu-id="201a6-233"><dt>**64 0x40**</dt></span><span class="sxs-lookup"><span data-stu-id="201a6-233"><dt>**64 0x40**</dt></span></span> </dl>       | <span data-ttu-id="201a6-234">**SEL \_ El \_ Directorio de eventos** es válido.</span><span class="sxs-lookup"><span data-stu-id="201a6-234">**SEL\_EVENT\_DIR** is valid.</span></span><br/>    |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <span data-ttu-id="201a6-235"><dt>**128 0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="201a6-235"><dt>**128 0x80**</dt></span></span> </dl>    | <span data-ttu-id="201a6-236">**SEL \_ El evento \_ data1** es válido.</span><span class="sxs-lookup"><span data-stu-id="201a6-236">**SEL\_EVENT\_DATA1** is valid.</span></span><br/>  |
| <span id="256_0x100"></span><span id="256_0X100"></span><dl> <span data-ttu-id="201a6-237"><dt>**256 0x100**</dt></span><span class="sxs-lookup"><span data-stu-id="201a6-237"><dt>**256 0x100**</dt></span></span> </dl> | <span data-ttu-id="201a6-238">**SEL \_ El evento \_ DATA2** es válido.</span><span class="sxs-lookup"><span data-stu-id="201a6-238">**SEL\_EVENT\_DATA2** is valid.</span></span><br/>  |
| <span id="512_0x200"></span><span id="512_0X200"></span><dl> <span data-ttu-id="201a6-239"><dt>**512 0x200**</dt></span><span class="sxs-lookup"><span data-stu-id="201a6-239"><dt>**512 0x200**</dt></span></span> </dl> | <span data-ttu-id="201a6-240">**SEL \_ El evento \_ DATA3** es válido.</span><span class="sxs-lookup"><span data-stu-id="201a6-240">**SEL\_EVENT\_DATA3** is valid.</span></span><br/>  |



 

<span data-ttu-id="201a6-241">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="201a6-241">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="201a6-242">Observaciones</span><span class="sxs-lookup"><span data-stu-id="201a6-242">Remarks</span></span>

<span data-ttu-id="201a6-243">La clase **MSMCAEvent \_ SystemEventError** se deriva de [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="201a6-243">The **MSMCAEvent\_SystemEventError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="201a6-244">Requisitos</span><span class="sxs-lookup"><span data-stu-id="201a6-244">Requirements</span></span>



| <span data-ttu-id="201a6-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="201a6-245">Requirement</span></span> | <span data-ttu-id="201a6-246">Value</span><span class="sxs-lookup"><span data-stu-id="201a6-246">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="201a6-247">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="201a6-247">Minimum supported client</span></span><br/> | <span data-ttu-id="201a6-248">Windows XP</span><span class="sxs-lookup"><span data-stu-id="201a6-248">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="201a6-249">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="201a6-249">Minimum supported server</span></span><br/> | <span data-ttu-id="201a6-250">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="201a6-250">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="201a6-251">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="201a6-251">Namespace</span></span><br/>                | <span data-ttu-id="201a6-252">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="201a6-252">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="201a6-253">MOF</span><span class="sxs-lookup"><span data-stu-id="201a6-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="201a6-254"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="201a6-254"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="201a6-255">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="201a6-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="201a6-256"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="201a6-256"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="201a6-257">Vea también</span><span class="sxs-lookup"><span data-stu-id="201a6-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="201a6-258">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="201a6-258">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="201a6-259">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="201a6-259">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

