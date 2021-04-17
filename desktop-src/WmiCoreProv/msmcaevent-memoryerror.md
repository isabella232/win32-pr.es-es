---
description: Representa un evento de error de memoria de arquitectura de comprobación de equipo (MCA). Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: 0db1d526-e2c3-4e48-90c8-cbcd9121040e
title: MSMCAEvent_MemoryError (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryError
- MSMCAEvent_MemoryError.Active
- MSMCAEvent_MemoryError.AdditionalErrors
- MSMCAEvent_MemoryError.BUS_SPECIFIC_DATA
- MSMCAEvent_MemoryError.Cpu
- MSMCAEvent_MemoryError.ErrorSeverity
- MSMCAEvent_MemoryError.InstanceName
- MSMCAEvent_MemoryError.MEM_BANK
- MSMCAEvent_MemoryError.MEM_BIT_POSITION
- MSMCAEvent_MemoryError.MEM_CARD
- MSMCAEvent_MemoryError.MEM_COLUMN
- MSMCAEvent_MemoryError.MEM_ERROR_STATUS
- MSMCAEvent_MemoryError.MEM_MODULE
- MSMCAEvent_MemoryError.MEM_NODE
- MSMCAEvent_MemoryError.MEM_PHYSICAL_ADDR
- MSMCAEvent_MemoryError.MEM_PHYSICAL_MASK
- MSMCAEvent_MemoryError.MEM_ROW
- MSMCAEvent_MemoryError.RawRecord
- MSMCAEvent_MemoryError.RecordId
- MSMCAEvent_MemoryError.REQUESTOR_ID
- MSMCAEvent_MemoryError.RESPONDER_ID
- MSMCAEvent_MemoryError.Size
- MSMCAEvent_MemoryError.TARGET_ID
- MSMCAEvent_MemoryError.Type
- MSMCAEvent_MemoryError.VALIDATION_BITS
- MSMCAEvent_MemoryError.MEM_DEVICE
- MSMCAEvent_MemoryError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 8dce82b8fa7a87676c34a9c6f26f43e4db10e227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697545"
---
# <a name="msmcaevent_memoryerror-class"></a><span data-ttu-id="f0751-104">MSMCAEvent \_ MemoryError (clase)</span><span class="sxs-lookup"><span data-stu-id="f0751-104">MSMCAEvent\_MemoryError class</span></span>

<span data-ttu-id="f0751-105">La clase **MSMCAEvent \_ MemoryError** representa un evento de error de memoria de arquitectura de comprobación de equipo (MCA).</span><span class="sxs-lookup"><span data-stu-id="f0751-105">The **MSMCAEvent\_MemoryError** class represents a Machine Check Architecture (MCA) memory error event.</span></span> <span data-ttu-id="f0751-106">Esta clase solo está disponible en sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f0751-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="f0751-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f0751-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f0751-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f0751-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0751-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0751-109">Syntax</span></span>

``` syntax
class MSMCAEvent_MemoryError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint64  BUS_SPECIFIC_DATA;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint16  MEM_BANK;
  uint16  MEM_BIT_POSITION;
  uint16  MEM_CARD;
  uint16  MEM_COLUMN;
  uint64  MEM_ERROR_STATUS;
  uint16  MEM_MODULE;
  uint16  MEM_NODE;
  uint64  MEM_PHYSICAL_ADDR;
  uint64  MEM_PHYSICAL_MASK;
  uint16  MEM_ROW;
  uint8   RawRecord[];
  uint64  RecordId;
  uint64  REQUESTOR_ID;
  uint64  RESPONDER_ID;
  uint32  Size;
  uint64  TARGET_ID;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint16  MEM_DEVICE;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="f0751-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f0751-110">Members</span></span>

<span data-ttu-id="f0751-111">La clase **MSMCAEvent \_ MemoryError** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f0751-111">The **MSMCAEvent\_MemoryError** class has these types of members:</span></span>

-   [<span data-ttu-id="f0751-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0751-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f0751-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0751-113">Properties</span></span>

<span data-ttu-id="f0751-114">La clase **MSMCAEvent \_ MemoryError** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f0751-114">The **MSMCAEvent\_MemoryError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f0751-115">**Activo**</span><span class="sxs-lookup"><span data-stu-id="f0751-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-116">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f0751-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-118">**True** si esta instancia de la clase está activa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="f0751-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="f0751-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="f0751-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0751-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-122">Número de errores adicionales en el registro de MCA.</span><span class="sxs-lookup"><span data-stu-id="f0751-122">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="f0751-123">**\_datos específicos de bus \_**</span><span class="sxs-lookup"><span data-stu-id="f0751-123">**BUS\_SPECIFIC\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-124">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f0751-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-126">Datos específicos del bus de OEM.</span><span class="sxs-lookup"><span data-stu-id="f0751-126">OEM-specific, bus-dependent data.</span></span>

<span data-ttu-id="f0751-127">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0751-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f0751-128">**CPU**</span><span class="sxs-lookup"><span data-stu-id="f0751-128">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0751-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-131">CPU que ha detectado el error.</span><span class="sxs-lookup"><span data-stu-id="f0751-131">CPU that reported the error.</span></span> <span data-ttu-id="f0751-132">Esta propiedad solo se aplica a un sistema de varios procesadores en el que el primer procesador tiene asignado el número 0, el segundo procesador tiene asignado el número 1 y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="f0751-132">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="f0751-133">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="f0751-133">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-134">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f0751-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-136">Nivel de gravedad del error comunicado.</span><span class="sxs-lookup"><span data-stu-id="f0751-136">Severity level of the error reported.</span></span>



| <span data-ttu-id="f0751-137">Value</span><span class="sxs-lookup"><span data-stu-id="f0751-137">Value</span></span>                                                                                                | <span data-ttu-id="f0751-138">Significado</span><span class="sxs-lookup"><span data-stu-id="f0751-138">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="f0751-139"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-139"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="f0751-140">Recuperable</span><span class="sxs-lookup"><span data-stu-id="f0751-140">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="f0751-141"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-141"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f0751-142">Crítico</span><span class="sxs-lookup"><span data-stu-id="f0751-142">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="f0751-143"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-143"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f0751-144">Corregible</span><span class="sxs-lookup"><span data-stu-id="f0751-144">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f0751-145">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="f0751-145">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0751-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0751-148">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f0751-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f0751-149">Identificador único de esta instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="f0751-149">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="f0751-150">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="f0751-150">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-151">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0751-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-153">Si es cero, este evento no se registra en el registro de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="f0751-153">If zero then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="f0751-154">**Banco de memoria \_**</span><span class="sxs-lookup"><span data-stu-id="f0751-154">**MEM\_BANK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-155">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0751-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-157">El módulo o el número de rango de la ubicación de errores de memoria.</span><span class="sxs-lookup"><span data-stu-id="f0751-157">The Module or RANK number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="f0751-158">**\_posición de bit de memoria \_**</span><span class="sxs-lookup"><span data-stu-id="f0751-158">**MEM\_BIT\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-159">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0751-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-161">Posición de bit en la palabra de memoria que contiene el error.</span><span class="sxs-lookup"><span data-stu-id="f0751-161">Bit position in the memory word that contains the error.</span></span>

</dd> <dt>

<span data-ttu-id="f0751-162">**tarjeta de memoria \_**</span><span class="sxs-lookup"><span data-stu-id="f0751-162">**MEM\_CARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-163">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0751-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-165">Número de tarjeta de la ubicación de errores de memoria.</span><span class="sxs-lookup"><span data-stu-id="f0751-165">Card number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="f0751-166">**\_columna MEM**</span><span class="sxs-lookup"><span data-stu-id="f0751-166">**MEM\_COLUMN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-167">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0751-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-169">Número de columna de la ubicación del error de memoria.</span><span class="sxs-lookup"><span data-stu-id="f0751-169">Column number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="f0751-170">**\_dispositivo MEM**</span><span class="sxs-lookup"><span data-stu-id="f0751-170">**MEM\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-171">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0751-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-173">Número de dispositivo de la ubicación de errores de memoria.</span><span class="sxs-lookup"><span data-stu-id="f0751-173">Device number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="f0751-174">**\_Estado de error de MEM \_**</span><span class="sxs-lookup"><span data-stu-id="f0751-174">**MEM\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-175">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f0751-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-177">Estado de error de memoria.</span><span class="sxs-lookup"><span data-stu-id="f0751-177">Memory error status.</span></span>

<span data-ttu-id="f0751-178">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0751-178">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f0751-179">**\_módulo MEM**</span><span class="sxs-lookup"><span data-stu-id="f0751-179">**MEM\_MODULE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-180">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0751-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-182">Módulo o número de rango de la ubicación de errores de memoria.</span><span class="sxs-lookup"><span data-stu-id="f0751-182">Module or rank number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="f0751-183">**nodo de memoria \_**</span><span class="sxs-lookup"><span data-stu-id="f0751-183">**MEM\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-184">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0751-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-186">Nodo que contiene el error de memoria.</span><span class="sxs-lookup"><span data-stu-id="f0751-186">Node that contains the memory error.</span></span> <span data-ttu-id="f0751-187">Esta propiedad solo se aplica en un sistema de varios nodos.</span><span class="sxs-lookup"><span data-stu-id="f0751-187">This property applies only in a multi-node system.</span></span> <span data-ttu-id="f0751-188">Esta propiedad es específica del proveedor.</span><span class="sxs-lookup"><span data-stu-id="f0751-188">This property is vendor-specific.</span></span>

</dd> <dt>

<span data-ttu-id="f0751-189">**\_dirección física de MEM \_**</span><span class="sxs-lookup"><span data-stu-id="f0751-189">**MEM\_PHYSICAL\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-190">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f0751-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-192">Dirección física del error de memoria.</span><span class="sxs-lookup"><span data-stu-id="f0751-192">Physical address of the memory error.</span></span>

<span data-ttu-id="f0751-193">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0751-193">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f0751-194">**\_máscara física de MEM \_**</span><span class="sxs-lookup"><span data-stu-id="f0751-194">**MEM\_PHYSICAL\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-195">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f0751-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-197">Bits de dirección válidos en la dirección física de 64 bits del error de memoria.</span><span class="sxs-lookup"><span data-stu-id="f0751-197">Valid address bits in the 64-bit physical address of the memory error.</span></span>

> [!Note]  
> <span data-ttu-id="f0751-198">La máscara física especifica la granularidad de la dirección física.</span><span class="sxs-lookup"><span data-stu-id="f0751-198">The physical mask specifies the granularity of the physical address.</span></span> <span data-ttu-id="f0751-199">La dirección física del error de memoria depende de factores de implementación de hardware.</span><span class="sxs-lookup"><span data-stu-id="f0751-199">The physical address of the memory error is dependent on hardware implementation factors.</span></span>

 

<span data-ttu-id="f0751-200">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0751-200">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f0751-201">**fila de memoria \_**</span><span class="sxs-lookup"><span data-stu-id="f0751-201">**MEM\_ROW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-202">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0751-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-204">Número de fila de la ubicación de errores de memoria.</span><span class="sxs-lookup"><span data-stu-id="f0751-204">Row number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="f0751-205">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="f0751-205">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-206">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="f0751-206">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f0751-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-208">Matriz de bytes que contiene el registro de errores sin procesar tal y como se presenta en Windows por la capa de abstracción del sistema (SAL).</span><span class="sxs-lookup"><span data-stu-id="f0751-208">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="f0751-209">La propiedad **size** especifica el número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="f0751-209">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="f0751-210">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="f0751-210">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-211">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f0751-211">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-213">Identificador de registro del registro de errores para este error.</span><span class="sxs-lookup"><span data-stu-id="f0751-213">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="f0751-214">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0751-214">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f0751-215">**identificador del solicitante \_**</span><span class="sxs-lookup"><span data-stu-id="f0751-215">**REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-216">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f0751-216">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-218">Dirección de hardware del dispositivo o componente que inicia la transacción.</span><span class="sxs-lookup"><span data-stu-id="f0751-218">Hardware address of the device or component that initiates the transaction.</span></span>

<span data-ttu-id="f0751-219">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0751-219">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f0751-220">**identificador del RESPONDEdor \_**</span><span class="sxs-lookup"><span data-stu-id="f0751-220">**RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-221">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f0751-221">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-223">Dirección de hardware del respondedor a la transacción.</span><span class="sxs-lookup"><span data-stu-id="f0751-223">Hardware address of the responder to the transaction.</span></span>

<span data-ttu-id="f0751-224">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0751-224">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f0751-225">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="f0751-225">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-226">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0751-226">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-227">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-228">Tamaño del registro de errores sin procesar en bytes.</span><span class="sxs-lookup"><span data-stu-id="f0751-228">Size of the raw error record in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f0751-229">**\_ID. de destino**</span><span class="sxs-lookup"><span data-stu-id="f0751-229">**TARGET\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-230">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f0751-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-232">Dirección de hardware del destino previsto de la transacción.</span><span class="sxs-lookup"><span data-stu-id="f0751-232">Hardware address of the intended target of the transaction.</span></span>

<span data-ttu-id="f0751-233">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0751-233">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f0751-234">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f0751-234">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-235">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0751-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-237">Tipo de mensaje de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="f0751-237">Type of event log message.</span></span> <span data-ttu-id="f0751-238">Estos mensajes se corresponden con los códigos de mensaje de registro de eventos utilizados para insertar mensajes de registro de eventos del proveedor de consumidores del registro de eventos de Windows cuando recibe uno de los eventos.</span><span class="sxs-lookup"><span data-stu-id="f0751-238">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="f0751-239">**BITS de validación \_**</span><span class="sxs-lookup"><span data-stu-id="f0751-239">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0751-240">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f0751-240">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f0751-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0751-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0751-242">Bits de validación que se usan para indicar la validez de los campos siguientes.</span><span class="sxs-lookup"><span data-stu-id="f0751-242">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="f0751-243">Valores</span><span class="sxs-lookup"><span data-stu-id="f0751-243">Values</span></span>                                                                                     | <span data-ttu-id="f0751-244">Significado</span><span class="sxs-lookup"><span data-stu-id="f0751-244">Meaning</span></span>                                                 |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="f0751-245"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-245"><dt>1 (0x1)</dt></span></span> </dl>         | <span data-ttu-id="f0751-246">El \_ Estado de error de MEM \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="f0751-246">MEM\_ERROR\_STATUS is valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="f0751-247"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-247"><dt>2 (0x2)</dt></span></span> </dl>         | <span data-ttu-id="f0751-248">La \_ dirección física de MEM \_ es válida.</span><span class="sxs-lookup"><span data-stu-id="f0751-248">MEM\_PHYSICAL\_ADDR is valid.</span></span><br/>                |
| <dl> <span data-ttu-id="f0751-249"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-249"><dt>4 (0x4)</dt></span></span> </dl>         | <span data-ttu-id="f0751-250">La \_ máscara de dirección de MEM \_ es válida.</span><span class="sxs-lookup"><span data-stu-id="f0751-250">MEM\_ADDR\_MASK is valid.</span></span><br/>                    |
| <dl> <span data-ttu-id="f0751-251"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-251"><dt>8 (0x8)</dt></span></span> </dl>         | <span data-ttu-id="f0751-252">El \_ nodo de memoria es válido.</span><span class="sxs-lookup"><span data-stu-id="f0751-252">MEM\_NODE is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="f0751-253"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-253"><dt>16 (0x10)</dt></span></span> </dl>       | <span data-ttu-id="f0751-254">La \_ tarjeta mem es válida.</span><span class="sxs-lookup"><span data-stu-id="f0751-254">MEM\_CARD is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="f0751-255"><dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-255"><dt>32 (0x20)</dt></span></span> </dl>       | <span data-ttu-id="f0751-256">El \_ módulo MEM es válido.</span><span class="sxs-lookup"><span data-stu-id="f0751-256">MEM\_MODULE is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="f0751-257"><dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-257"><dt>64 (0x40)</dt></span></span> </dl>       | <span data-ttu-id="f0751-258">El \_ Banco de memoria es válido.</span><span class="sxs-lookup"><span data-stu-id="f0751-258">MEM\_BANK is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="f0751-259"><dt>128 (0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-259"><dt>128 (0x80)</dt></span></span> </dl>      | <span data-ttu-id="f0751-260">El \_ dispositivo MEM es válido.</span><span class="sxs-lookup"><span data-stu-id="f0751-260">MEM\_DEVICE is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="f0751-261"><dt>256 (0x100)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-261"><dt>256 (0x100)</dt></span></span> </dl>     | <span data-ttu-id="f0751-262">La \_ fila de MEM es válida.</span><span class="sxs-lookup"><span data-stu-id="f0751-262">MEM\_ROW is valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="f0751-263"><dt>512 (0x200)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-263"><dt>512 (0x200)</dt></span></span> </dl>     | <span data-ttu-id="f0751-264">La \_ columna MEM es válida.</span><span class="sxs-lookup"><span data-stu-id="f0751-264">MEM\_COLUMN is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="f0751-265"><dt>1024 (0x400)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-265"><dt>1024 (0x400)</dt></span></span> </dl>    | <span data-ttu-id="f0751-266">La \_ posición de bit de memoria \_ es válida.</span><span class="sxs-lookup"><span data-stu-id="f0751-266">MEM\_BIT\_POSITION is valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="f0751-267"><dt>2048 (0x800)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-267"><dt>2048 (0x800)</dt></span></span> </dl>    | <span data-ttu-id="f0751-268">El identificador del solicitante de la plataforma de MEM \_ \_ \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="f0751-268">MEM\_PLATFORM\_REQUESTOR\_ID is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="f0751-269"><dt>4096 (0x1000)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-269"><dt>4096 (0x1000)</dt></span></span> </dl>   | <span data-ttu-id="f0751-270">El \_ identificador del respondedor de plataforma de MEM \_ \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="f0751-270">MEM\_PLATFORM\_RESPONDER\_ID is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="f0751-271"><dt>8192 (0x2000)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-271"><dt>8192 (0x2000)</dt></span></span> </dl>   | <span data-ttu-id="f0751-272">El destino de la plataforma de MEM \_ \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="f0751-272">MEM\_PLATFORM\_TARGET is valid.</span></span><br/>              |
| <dl> <span data-ttu-id="f0751-273"><dt>16384 (0x4000)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-273"><dt>16384 (0x4000)</dt></span></span> </dl>  | <span data-ttu-id="f0751-274">Los \_ datos específicos de bus de plataforma de MEM \_ \_ \_ son válidos.</span><span class="sxs-lookup"><span data-stu-id="f0751-274">MEM\_PLATFORM\_BUS\_SPECIFIC\_DATA is valid.</span></span><br/> |
| <dl> <span data-ttu-id="f0751-275"><dt>32768 (0x8000)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-275"><dt>32768 (0x8000)</dt></span></span> </dl>  | <span data-ttu-id="f0751-276">El \_ ID. de OEM de la plataforma de MEM \_ \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="f0751-276">MEM\_PLATFORM\_OEM\_ID is valid.</span></span><br/>             |
| <dl> <span data-ttu-id="f0751-277"><dt>65536 (0x10000)</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-277"><dt>65536 (0x10000)</dt></span></span> </dl> | <span data-ttu-id="f0751-278">La \_ estructura de datos OEM de la plataforma MEM \_ \_ \_ es válida.</span><span class="sxs-lookup"><span data-stu-id="f0751-278">MEM\_PLATFORM\_OEM\_DATA\_STRUCT is valid.</span></span><br/>   |



 

<span data-ttu-id="f0751-279">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0751-279">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0751-280">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0751-280">Remarks</span></span>

<span data-ttu-id="f0751-281">La clase **MSMCAEvent \_ MemoryError** se deriva de [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="f0751-281">The **MSMCAEvent\_MemoryError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0751-282">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0751-282">Requirements</span></span>



| <span data-ttu-id="f0751-283">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0751-283">Requirement</span></span> | <span data-ttu-id="f0751-284">Value</span><span class="sxs-lookup"><span data-stu-id="f0751-284">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0751-285">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0751-285">Minimum supported client</span></span><br/> | <span data-ttu-id="f0751-286">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f0751-286">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="f0751-287">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0751-287">Minimum supported server</span></span><br/> | <span data-ttu-id="f0751-288">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f0751-288">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="f0751-289">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f0751-289">Namespace</span></span><br/>                | <span data-ttu-id="f0751-290">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="f0751-290">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="f0751-291">MOF</span><span class="sxs-lookup"><span data-stu-id="f0751-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0751-292"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-292"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0751-293">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f0751-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0751-294"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0751-294"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0751-295">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0751-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0751-296">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="f0751-296">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="f0751-297">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="f0751-297">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

