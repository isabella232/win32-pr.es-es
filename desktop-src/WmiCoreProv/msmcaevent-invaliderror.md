---
description: Indica un error no válido de arquitectura de comprobación de equipo (MCA). Un error de MCA no válido identifica un formato de error que no se ajusta a las especificaciones de Windows. Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: 476ea558-2e0e-480f-b4ba-8d73fdef3308
title: MSMCAEvent_InvalidError (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_InvalidError
- MSMCAEvent_InvalidError.Active
- MSMCAEvent_InvalidError.AdditionalErrors
- MSMCAEvent_InvalidError.Cpu
- MSMCAEvent_InvalidError.ErrorSeverity
- MSMCAEvent_InvalidError.InstanceName
- MSMCAEvent_InvalidError.RawRecord
- MSMCAEvent_InvalidError.RecordId
- MSMCAEvent_InvalidError.Size
- MSMCAEvent_InvalidError.Type
- MSMCAEvent_InvalidError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: abd12cfa7280a1b2f6a718b47b17d4ddf121cc25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696366"
---
# <a name="msmcaevent_invaliderror-class"></a><span data-ttu-id="40339-105">MSMCAEvent \_ InvalidError (clase)</span><span class="sxs-lookup"><span data-stu-id="40339-105">MSMCAEvent\_InvalidError class</span></span>

<span data-ttu-id="40339-106">La clase **MSMCAEvent \_ InvalidError** indica un error no válido de arquitectura de comprobación de equipo (MCA).</span><span class="sxs-lookup"><span data-stu-id="40339-106">The **MSMCAEvent\_InvalidError** class indicates a Machine Check Architecture (MCA) invalid error.</span></span> <span data-ttu-id="40339-107">Un error de MCA no válido identifica un formato de error que no se ajusta a las especificaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="40339-107">An invalid MCA error identifies an error format that does not conform to Windows specifications.</span></span> <span data-ttu-id="40339-108">Esta clase solo está disponible en sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="40339-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="40339-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="40339-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="40339-110">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="40339-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="40339-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40339-111">Syntax</span></span>

``` syntax
class MSMCAEvent_InvalidError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="40339-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="40339-112">Members</span></span>

<span data-ttu-id="40339-113">La clase **MSMCAEvent \_ InvalidError** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="40339-113">The **MSMCAEvent\_InvalidError** class has these types of members:</span></span>

-   [<span data-ttu-id="40339-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="40339-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40339-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="40339-115">Properties</span></span>

<span data-ttu-id="40339-116">La clase **MSMCAEvent \_ InvalidError** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="40339-116">The **MSMCAEvent\_InvalidError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40339-117">**Activo**</span><span class="sxs-lookup"><span data-stu-id="40339-117">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40339-118">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="40339-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40339-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40339-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40339-120">**True** si esta instancia de la clase está activa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="40339-120">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="40339-121">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="40339-121">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40339-122">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40339-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40339-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40339-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40339-124">Número de errores adicionales en el registro de MCA.</span><span class="sxs-lookup"><span data-stu-id="40339-124">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="40339-125">**CPU**</span><span class="sxs-lookup"><span data-stu-id="40339-125">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40339-126">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40339-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40339-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40339-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40339-128">CPU que ha detectado el error.</span><span class="sxs-lookup"><span data-stu-id="40339-128">CPU that reported the error.</span></span> <span data-ttu-id="40339-129">Esta propiedad solo se aplica a un sistema de varios procesadores en el que el primer procesador tiene asignado el número 0, el segundo procesador tiene asignado el número 1 y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="40339-129">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="40339-130">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="40339-130">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40339-131">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="40339-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="40339-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40339-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40339-133">Nivel de gravedad del error comunicado.</span><span class="sxs-lookup"><span data-stu-id="40339-133">Severity level of the error reported.</span></span>



| <span data-ttu-id="40339-134">Value</span><span class="sxs-lookup"><span data-stu-id="40339-134">Value</span></span>                                                                                                | <span data-ttu-id="40339-135">Significado</span><span class="sxs-lookup"><span data-stu-id="40339-135">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="40339-136"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="40339-136"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="40339-137">Recuperable</span><span class="sxs-lookup"><span data-stu-id="40339-137">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="40339-138"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="40339-138"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="40339-139">Crítico</span><span class="sxs-lookup"><span data-stu-id="40339-139">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="40339-140"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="40339-140"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="40339-141">Corregible</span><span class="sxs-lookup"><span data-stu-id="40339-141">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="40339-142">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="40339-142">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40339-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="40339-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40339-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40339-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40339-145">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="40339-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="40339-146">Identificador único de esta instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="40339-146">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="40339-147">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="40339-147">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40339-148">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40339-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40339-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40339-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40339-150">Si es 0 (cero), este evento no se registra en el registro de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="40339-150">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="40339-151">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="40339-151">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40339-152">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="40339-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="40339-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40339-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40339-154">Matriz de bytes que contiene el registro de errores sin procesar tal y como se presenta en Windows por la capa de abstracción del sistema (SAL).</span><span class="sxs-lookup"><span data-stu-id="40339-154">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="40339-155">La propiedad **size** especifica el número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="40339-155">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="40339-156">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="40339-156">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40339-157">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="40339-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="40339-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40339-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40339-159">Identificador de registro del registro de errores para este error.</span><span class="sxs-lookup"><span data-stu-id="40339-159">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="40339-160">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="40339-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="40339-161">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="40339-161">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40339-162">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40339-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40339-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40339-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40339-164">Tamaño del registro de errores sin procesar.</span><span class="sxs-lookup"><span data-stu-id="40339-164">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="40339-165">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="40339-165">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40339-166">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40339-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40339-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40339-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40339-168">Tipo de mensaje de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="40339-168">Type of event log message.</span></span> <span data-ttu-id="40339-169">Estos mensajes se corresponden con los códigos de mensaje de registro de eventos utilizados para insertar mensajes de registro de eventos del proveedor de consumidores del registro de eventos de Windows cuando recibe uno de los eventos.</span><span class="sxs-lookup"><span data-stu-id="40339-169">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40339-170">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40339-170">Remarks</span></span>

<span data-ttu-id="40339-171">La clase **MSMCAEvent \_ InvalidError** se deriva de [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="40339-171">The **MSMCAEvent\_InvalidError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40339-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40339-172">Requirements</span></span>



| <span data-ttu-id="40339-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="40339-173">Requirement</span></span> | <span data-ttu-id="40339-174">Value</span><span class="sxs-lookup"><span data-stu-id="40339-174">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40339-175">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40339-175">Minimum supported client</span></span><br/> | <span data-ttu-id="40339-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="40339-176">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="40339-177">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40339-177">Minimum supported server</span></span><br/> | <span data-ttu-id="40339-178">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="40339-178">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="40339-179">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="40339-179">Namespace</span></span><br/>                | <span data-ttu-id="40339-180">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="40339-180">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="40339-181">MOF</span><span class="sxs-lookup"><span data-stu-id="40339-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40339-182"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40339-182"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="40339-183">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="40339-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40339-184"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40339-184"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40339-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="40339-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40339-186">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="40339-186">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="40339-187">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="40339-187">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

