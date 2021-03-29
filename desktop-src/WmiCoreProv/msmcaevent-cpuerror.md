---
description: Representa un evento de error de CPU. Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: 4ee4aa51-a965-4569-b53c-0ba21bf42752
title: MSMCAEvent_CPUError (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_CPUError
- MSMCAEvent_CPUError.Active
- MSMCAEvent_CPUError.AdditionalErrors
- MSMCAEvent_CPUError.Cpu
- MSMCAEvent_CPUError.ErrorSeverity
- MSMCAEvent_CPUError.InstanceName
- MSMCAEvent_CPUError.Level
- MSMCAEvent_CPUError.RawRecord
- MSMCAEvent_CPUError.RecordId
- MSMCAEvent_CPUError.Size
- MSMCAEvent_CPUError.Type
- MSMCAEvent_CPUError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: dff990b46d730a1e8b54ef99a24a686745e3dacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541502"
---
# <a name="msmcaevent_cpuerror-class"></a><span data-ttu-id="66e15-104">MSMCAEvent \_ CPUError (clase)</span><span class="sxs-lookup"><span data-stu-id="66e15-104">MSMCAEvent\_CPUError class</span></span>

<span data-ttu-id="66e15-105">La clase **MSMCAEvent \_ CPUError** representa un evento de error de CPU.</span><span class="sxs-lookup"><span data-stu-id="66e15-105">The **MSMCAEvent\_CPUError** class represents a CPU error event.</span></span> <span data-ttu-id="66e15-106">Esta clase solo está disponible en sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="66e15-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="66e15-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="66e15-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="66e15-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="66e15-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="66e15-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66e15-109">Syntax</span></span>

``` syntax
class MSMCAEvent_CPUError : WmiEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint32  Level;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="66e15-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="66e15-110">Members</span></span>

<span data-ttu-id="66e15-111">La clase **MSMCAEvent \_ CPUError** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="66e15-111">The **MSMCAEvent\_CPUError** class has these types of members:</span></span>

-   [<span data-ttu-id="66e15-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="66e15-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66e15-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="66e15-113">Properties</span></span>

<span data-ttu-id="66e15-114">La clase **MSMCAEvent \_ CPUError** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="66e15-114">The **MSMCAEvent\_CPUError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66e15-115">**Activo**</span><span class="sxs-lookup"><span data-stu-id="66e15-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66e15-116">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="66e15-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66e15-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66e15-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66e15-118">**True** si esta instancia de la clase está activa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="66e15-118">**TRUE**, if this instance of the class is active; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="66e15-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="66e15-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66e15-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66e15-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66e15-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66e15-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66e15-122">Número de errores adicionales en el registro de MCA.</span><span class="sxs-lookup"><span data-stu-id="66e15-122">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="66e15-123">**CPU**</span><span class="sxs-lookup"><span data-stu-id="66e15-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66e15-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66e15-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66e15-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66e15-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66e15-126">CPU que ha detectado el error.</span><span class="sxs-lookup"><span data-stu-id="66e15-126">CPU that reported the error.</span></span> <span data-ttu-id="66e15-127">Esta propiedad solo se aplica a un sistema de varios procesadores en el que el primer procesador tiene asignado el número 0, el segundo procesador tiene asignado el número 1 y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="66e15-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="66e15-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="66e15-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66e15-129">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="66e15-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="66e15-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66e15-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66e15-131">Nivel de gravedad del error comunicado.</span><span class="sxs-lookup"><span data-stu-id="66e15-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="66e15-132">Value</span><span class="sxs-lookup"><span data-stu-id="66e15-132">Value</span></span>                                                                                                | <span data-ttu-id="66e15-133">Significado</span><span class="sxs-lookup"><span data-stu-id="66e15-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="66e15-134"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="66e15-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="66e15-135">Recuperable</span><span class="sxs-lookup"><span data-stu-id="66e15-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="66e15-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="66e15-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="66e15-137">Crítico</span><span class="sxs-lookup"><span data-stu-id="66e15-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="66e15-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="66e15-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="66e15-139">Corregible</span><span class="sxs-lookup"><span data-stu-id="66e15-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="66e15-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="66e15-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66e15-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="66e15-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66e15-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66e15-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66e15-143">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="66e15-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="66e15-144">Identificador único para esta instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="66e15-144">Unique identifier for this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="66e15-145">**Level**</span><span class="sxs-lookup"><span data-stu-id="66e15-145">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66e15-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66e15-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66e15-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66e15-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66e15-148">Calificadores: **WmiMissingData** (-1)</span><span class="sxs-lookup"><span data-stu-id="66e15-148">Qualifiers: **WmiMissingData** (-1)</span></span>
</dt> </dl>

<span data-ttu-id="66e15-149">Nivel de caché, búfer de traslación (TLB) o estructura de microarquitectura en la que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="66e15-149">Level of cache, translation buffer (TLB), or micro-architectural structure where the error occurred.</span></span> <span data-ttu-id="66e15-150">Un valor de 0 (cero) indica el primer nivel.</span><span class="sxs-lookup"><span data-stu-id="66e15-150">A value of 0 (zero) indicates the first level.</span></span>

</dd> <dt>

<span data-ttu-id="66e15-151">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="66e15-151">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66e15-152">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66e15-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66e15-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66e15-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66e15-154">Si es cero, este evento no se registra en el registro de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="66e15-154">If zero then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="66e15-155">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="66e15-155">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66e15-156">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="66e15-156">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="66e15-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66e15-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66e15-158">Matriz de bytes que contiene el registro de errores sin procesar.</span><span class="sxs-lookup"><span data-stu-id="66e15-158">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="66e15-159">El número de elementos de la matriz que especifica la propiedad **size** .</span><span class="sxs-lookup"><span data-stu-id="66e15-159">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="66e15-160">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="66e15-160">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66e15-161">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66e15-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66e15-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66e15-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66e15-163">Identificador de registro del registro de errores para este error.</span><span class="sxs-lookup"><span data-stu-id="66e15-163">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="66e15-164">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="66e15-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="66e15-165">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="66e15-165">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66e15-166">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66e15-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66e15-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66e15-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66e15-168">Tamaño del registro de errores sin procesar en bytes.</span><span class="sxs-lookup"><span data-stu-id="66e15-168">Size of the raw error record in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="66e15-169">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="66e15-169">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66e15-170">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66e15-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66e15-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66e15-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66e15-172">Tipo de mensaje de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="66e15-172">Type of event log message.</span></span> <span data-ttu-id="66e15-173">Estos mensajes se corresponden con los códigos de mensaje de registro de eventos utilizados para insertar mensajes de registro de eventos del proveedor de consumidores del registro de eventos de Windows cuando recibe uno de los eventos.</span><span class="sxs-lookup"><span data-stu-id="66e15-173">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66e15-174">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66e15-174">Remarks</span></span>

<span data-ttu-id="66e15-175">La clase **MSMCAEvent \_ CPUError** se deriva de [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="66e15-175">The **MSMCAEvent\_CPUError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66e15-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66e15-176">Requirements</span></span>



| <span data-ttu-id="66e15-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="66e15-177">Requirement</span></span> | <span data-ttu-id="66e15-178">Value</span><span class="sxs-lookup"><span data-stu-id="66e15-178">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66e15-179">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66e15-179">Minimum supported client</span></span><br/> | <span data-ttu-id="66e15-180">Windows XP</span><span class="sxs-lookup"><span data-stu-id="66e15-180">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="66e15-181">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66e15-181">Minimum supported server</span></span><br/> | <span data-ttu-id="66e15-182">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="66e15-182">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="66e15-183">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="66e15-183">Namespace</span></span><br/>                | <span data-ttu-id="66e15-184">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="66e15-184">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="66e15-185">MOF</span><span class="sxs-lookup"><span data-stu-id="66e15-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66e15-186"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66e15-186"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="66e15-187">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="66e15-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66e15-188"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66e15-188"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66e15-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="66e15-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66e15-190">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="66e15-190">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="66e15-191">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="66e15-191">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

