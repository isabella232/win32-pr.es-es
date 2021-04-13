---
description: Indica un error del BIOS del sistema de la arquitectura de comprobación de la máquina (MCA). Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: b451ca45-6208-4445-b9f1-b4e3174837a4
title: MSMCAEvent_SMBIOSError (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SMBIOSError
- MSMCAEvent_SMBIOSError.Active
- MSMCAEvent_SMBIOSError.AdditionalErrors
- MSMCAEvent_SMBIOSError.Cpu
- MSMCAEvent_SMBIOSError.ErrorSeverity
- MSMCAEvent_SMBIOSError.InstanceName
- MSMCAEvent_SMBIOSError.RawRecord
- MSMCAEvent_SMBIOSError.RecordId
- MSMCAEvent_SMBIOSError.Size
- MSMCAEvent_SMBIOSError.SMBIOS_EVENT_TYPE
- MSMCAEvent_SMBIOSError.Type
- MSMCAEvent_SMBIOSError.VALIDATION_BITS
- MSMCAEvent_SMBIOSError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 709d480e8865c5d5bde2a9f5e8de45f138e66548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278417"
---
# <a name="msmcaevent_smbioserror-class"></a><span data-ttu-id="339bf-104">MSMCAEvent \_ SMBIOSError (clase)</span><span class="sxs-lookup"><span data-stu-id="339bf-104">MSMCAEvent\_SMBIOSError class</span></span>

<span data-ttu-id="339bf-105">La clase **MSMCAEvent \_ SMBIOSError** indica un error del BIOS del sistema de la arquitectura de comprobación del equipo (MCA).</span><span class="sxs-lookup"><span data-stu-id="339bf-105">The **MSMCAEvent\_SMBIOSError** class indicates a Machine Check Architecture (MCA) system BIOS error.</span></span> <span data-ttu-id="339bf-106">Esta clase solo está disponible en sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="339bf-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="339bf-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="339bf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="339bf-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="339bf-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="339bf-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="339bf-109">Syntax</span></span>

``` syntax
class MSMCAEvent_SMBIOSError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint8   SMBIOS_EVENT_TYPE;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="339bf-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="339bf-110">Members</span></span>

<span data-ttu-id="339bf-111">La clase **MSMCAEvent \_ SMBIOSError** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="339bf-111">The **MSMCAEvent\_SMBIOSError** class has these types of members:</span></span>

-   [<span data-ttu-id="339bf-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="339bf-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="339bf-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="339bf-113">Properties</span></span>

<span data-ttu-id="339bf-114">La clase **MSMCAEvent \_ SMBIOSError** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="339bf-114">The **MSMCAEvent\_SMBIOSError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="339bf-115">**Activo**</span><span class="sxs-lookup"><span data-stu-id="339bf-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339bf-116">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="339bf-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="339bf-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339bf-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="339bf-118">**True** si esta instancia de la clase está activa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="339bf-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="339bf-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="339bf-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339bf-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="339bf-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="339bf-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339bf-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="339bf-122">Número de errores adicionales en el registro.</span><span class="sxs-lookup"><span data-stu-id="339bf-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="339bf-123">**CPU**</span><span class="sxs-lookup"><span data-stu-id="339bf-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339bf-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="339bf-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="339bf-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339bf-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="339bf-126">CPU que ha detectado el error.</span><span class="sxs-lookup"><span data-stu-id="339bf-126">CPU that reported the error.</span></span> <span data-ttu-id="339bf-127">Esta propiedad solo se aplica a un sistema de varios procesadores en el que el primer procesador tiene asignado el número 0, el segundo procesador tiene asignado el número 1 y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="339bf-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="339bf-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="339bf-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339bf-129">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="339bf-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="339bf-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339bf-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="339bf-131">Nivel de gravedad del error comunicado.</span><span class="sxs-lookup"><span data-stu-id="339bf-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="339bf-132">Value</span><span class="sxs-lookup"><span data-stu-id="339bf-132">Value</span></span>                                                                                                | <span data-ttu-id="339bf-133">Significado</span><span class="sxs-lookup"><span data-stu-id="339bf-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="339bf-134"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="339bf-135">Recuperable</span><span class="sxs-lookup"><span data-stu-id="339bf-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="339bf-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="339bf-137">Crítico</span><span class="sxs-lookup"><span data-stu-id="339bf-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="339bf-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="339bf-139">Corregible</span><span class="sxs-lookup"><span data-stu-id="339bf-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="339bf-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="339bf-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339bf-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="339bf-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="339bf-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339bf-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="339bf-143">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="339bf-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="339bf-144">Identificador único de esta instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="339bf-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="339bf-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="339bf-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339bf-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="339bf-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="339bf-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339bf-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="339bf-148">Si es 0 (cero), este evento no se registra en el registro de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="339bf-148">If 0 (zero), then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="339bf-149">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="339bf-149">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339bf-150">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="339bf-150">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="339bf-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339bf-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="339bf-152">Matriz de bytes que contiene el registro de errores sin procesar.</span><span class="sxs-lookup"><span data-stu-id="339bf-152">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="339bf-153">El número de elementos de la matriz que especifica la propiedad **size** .</span><span class="sxs-lookup"><span data-stu-id="339bf-153">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="339bf-154">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="339bf-154">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339bf-155">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="339bf-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="339bf-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339bf-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="339bf-157">Identificador de registro del registro de errores para este error.</span><span class="sxs-lookup"><span data-stu-id="339bf-157">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="339bf-158">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="339bf-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="339bf-159">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="339bf-159">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339bf-160">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="339bf-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="339bf-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339bf-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="339bf-162">Tamaño del registro de errores sin procesar.</span><span class="sxs-lookup"><span data-stu-id="339bf-162">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="339bf-163">**\_tipo de evento SMBIOS \_**</span><span class="sxs-lookup"><span data-stu-id="339bf-163">**SMBIOS\_EVENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339bf-164">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="339bf-164">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="339bf-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339bf-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="339bf-166">Tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="339bf-166">Event type.</span></span>



| <span data-ttu-id="339bf-167">Value</span><span class="sxs-lookup"><span data-stu-id="339bf-167">Value</span></span>                                                                                                  | <span data-ttu-id="339bf-168">Significado</span><span class="sxs-lookup"><span data-stu-id="339bf-168">Meaning</span></span>                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="339bf-169"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-169"><dt>**0**</dt></span></span> </dl>   | <span data-ttu-id="339bf-170">Reservado.</span><span class="sxs-lookup"><span data-stu-id="339bf-170">Reserved.</span></span><br/>                                                                                                        |
| <span id="1"></span><dl> <span data-ttu-id="339bf-171"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-171"><dt>**1**</dt></span></span> </dl>   | <span data-ttu-id="339bf-172">Error de memoria ECC de bit único.</span><span class="sxs-lookup"><span data-stu-id="339bf-172">Single bit ECC memory error.</span></span><br/>                                                                                     |
| <span id="2"></span><dl> <span data-ttu-id="339bf-173"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-173"><dt>**2**</dt></span></span> </dl>   | <span data-ttu-id="339bf-174">Error de memoria ECC de bits múltiple.</span><span class="sxs-lookup"><span data-stu-id="339bf-174">Multiple bit ECC memory error.</span></span><br/>                                                                                   |
| <span id="3"></span><dl> <span data-ttu-id="339bf-175"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-175"><dt>**3**</dt></span></span> </dl>   | <span data-ttu-id="339bf-176">Error de memoria de paridad.</span><span class="sxs-lookup"><span data-stu-id="339bf-176">Parity Memory error.</span></span><br/>                                                                                             |
| <span id="4"></span><dl> <span data-ttu-id="339bf-177"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-177"><dt>**4**</dt></span></span> </dl>   | <span data-ttu-id="339bf-178">Tiempo de espera de bus.</span><span class="sxs-lookup"><span data-stu-id="339bf-178">Bus time out.</span></span><br/>                                                                                                    |
| <span id="5"></span><dl> <span data-ttu-id="339bf-179"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-179"><dt>**5**</dt></span></span> </dl>   | <span data-ttu-id="339bf-180">Comprobación del canal de e/s.</span><span class="sxs-lookup"><span data-stu-id="339bf-180">I/O Channel Check.</span></span><br/>                                                                                               |
| <span id="6"></span><dl> <span data-ttu-id="339bf-181"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-181"><dt>**6**</dt></span></span> </dl>   | <span data-ttu-id="339bf-182">Software NMI.</span><span class="sxs-lookup"><span data-stu-id="339bf-182">Software NMI.</span></span><br/>                                                                                                    |
| <span id="7"></span><dl> <span data-ttu-id="339bf-183"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-183"><dt>**7**</dt></span></span> </dl>   | <span data-ttu-id="339bf-184">Cambiar el tamaño de la memoria.</span><span class="sxs-lookup"><span data-stu-id="339bf-184">Post Memory Resize.</span></span><br/>                                                                                              |
| <span id="8"></span><dl> <span data-ttu-id="339bf-185"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-185"><dt>**8**</dt></span></span> </dl>   | <span data-ttu-id="339bf-186">Error de POST.</span><span class="sxs-lookup"><span data-stu-id="339bf-186">POST Error.</span></span><br/>                                                                                                      |
| <span id="9"></span><dl> <span data-ttu-id="339bf-187"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-187"><dt>**9**</dt></span></span> </dl>   | <span data-ttu-id="339bf-188">Error de paridad de PCI.</span><span class="sxs-lookup"><span data-stu-id="339bf-188">PCI Parity Error.</span></span><br/>                                                                                                |
| <span id="10"></span><dl> <span data-ttu-id="339bf-189"><dt>**10**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-189"><dt>**10**</dt></span></span> </dl> | <span data-ttu-id="339bf-190">Error del sistema PCI.</span><span class="sxs-lookup"><span data-stu-id="339bf-190">PCI System Error.</span></span><br/>                                                                                                |
| <span id="11"></span><dl> <span data-ttu-id="339bf-191"><dt>**11**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-191"><dt>**11**</dt></span></span> </dl> | <span data-ttu-id="339bf-192">Error de CPU.</span><span class="sxs-lookup"><span data-stu-id="339bf-192">CPU Failure.</span></span><br/>                                                                                                     |
| <span id="12"></span><dl> <span data-ttu-id="339bf-193"><dt>**12**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-193"><dt>**12**</dt></span></span> </dl> | <span data-ttu-id="339bf-194">Tiempo de espera del temporizador de failsafe de EISA.</span><span class="sxs-lookup"><span data-stu-id="339bf-194">EISA Failsafe Timer time out.</span></span><br/>                                                                                    |
| <span id="13"></span><dl> <span data-ttu-id="339bf-195"><dt>**13**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-195"><dt>**13**</dt></span></span> </dl> | <span data-ttu-id="339bf-196">Registro de memoria corregido deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="339bf-196">Correctable memory log disabled.</span></span><br/>                                                                                 |
| <span id="14"></span><dl> <span data-ttu-id="339bf-197"><dt>**14**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-197"><dt>**14**</dt></span></span> </dl> | <span data-ttu-id="339bf-198">Registro deshabilitado para un tipo de evento específico.</span><span class="sxs-lookup"><span data-stu-id="339bf-198">Logging disabled for a specific event type.</span></span> <span data-ttu-id="339bf-199">Se recibieron demasiados errores del mismo tipo en un breve período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="339bf-199">Too many errors of the same type received in a short amount of time.</span></span><br/> |
| <span id="15"></span><dl> <span data-ttu-id="339bf-200"><dt>**15**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-200"><dt>**15**</dt></span></span> </dl> | <span data-ttu-id="339bf-201">Reservado.</span><span class="sxs-lookup"><span data-stu-id="339bf-201">Reserved.</span></span><br/>                                                                                                        |
| <span id="16"></span><dl> <span data-ttu-id="339bf-202"><dt>**16**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-202"><dt>**16**</dt></span></span> </dl> | <span data-ttu-id="339bf-203">Se superó el límite del sistema (por ejemplo, se superó el umbral de voltaje o temperatura).</span><span class="sxs-lookup"><span data-stu-id="339bf-203">System limit exceeded (for example, voltage or temperature threshold exceeded).</span></span><br/>                                  |
| <span id="17"></span><dl> <span data-ttu-id="339bf-204"><dt>**18**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-204"><dt>**17**</dt></span></span> </dl> | <span data-ttu-id="339bf-205">El temporizador de hardware asincrónico ha expirado y ha emitido un restablecimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="339bf-205">Asynchronous hardware timer expired and issued a system reset.</span></span><br/>                                                   |
| <span id="18"></span><dl> <span data-ttu-id="339bf-206"><dt>**18**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-206"><dt>**18**</dt></span></span> </dl> | <span data-ttu-id="339bf-207">Información de configuración del sistema.</span><span class="sxs-lookup"><span data-stu-id="339bf-207">System configuration information.</span></span><br/>                                                                                |
| <span id="19"></span><dl> <span data-ttu-id="339bf-208"><dt>**19**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-208"><dt>**19**</dt></span></span> </dl> | <span data-ttu-id="339bf-209">Información del disco duro.</span><span class="sxs-lookup"><span data-stu-id="339bf-209">Hard disk information.</span></span><br/>                                                                                           |
| <span id="20"></span><dl> <span data-ttu-id="339bf-210"><dt>**20**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-210"><dt>**20**</dt></span></span> </dl> | <span data-ttu-id="339bf-211">El sistema se ha reconfigurado.</span><span class="sxs-lookup"><span data-stu-id="339bf-211">System reconfigured.</span></span><br/>                                                                                             |
| <span id="21"></span><dl> <span data-ttu-id="339bf-212"><dt>**21**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-212"><dt>**21**</dt></span></span> </dl> | <span data-ttu-id="339bf-213">Error no corregible de CPU-complejo.</span><span class="sxs-lookup"><span data-stu-id="339bf-213">Uncorrectable CPU-complex error.</span></span><br/>                                                                                 |
| <span id="22"></span><dl> <span data-ttu-id="339bf-214"><dt>**22**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-214"><dt>**22**</dt></span></span> </dl> | <span data-ttu-id="339bf-215">Restablecimiento o desactivación del área de registro.</span><span class="sxs-lookup"><span data-stu-id="339bf-215">Log Area Reset or Cleared.</span></span><br/>                                                                                       |
| <span id="23"></span><dl> <span data-ttu-id="339bf-216"><dt>**23**</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-216"><dt>**23**</dt></span></span> </dl> | <span data-ttu-id="339bf-217">Arranque del sistema.</span><span class="sxs-lookup"><span data-stu-id="339bf-217">System boot.</span></span> <span data-ttu-id="339bf-218">Si se implementa, se garantiza que esta entrada de registro es la primera que se escribe en cualquier arranque del sistema.</span><span class="sxs-lookup"><span data-stu-id="339bf-218">If implemented, this log entry is guaranteed to be the first one written on any system boot.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="339bf-219">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="339bf-219">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339bf-220">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="339bf-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="339bf-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339bf-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="339bf-222">Tipo de mensaje de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="339bf-222">Type of event log message.</span></span> <span data-ttu-id="339bf-223">Estos mensajes se corresponden con los códigos de mensaje de registro de eventos utilizados para insertar mensajes de registro de eventos del proveedor de consumidores del registro de eventos de Windows cuando recibe uno de los eventos.</span><span class="sxs-lookup"><span data-stu-id="339bf-223">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="339bf-224">**BITS de validación \_**</span><span class="sxs-lookup"><span data-stu-id="339bf-224">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="339bf-225">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="339bf-225">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="339bf-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="339bf-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="339bf-227">Bits de validación que se usan para indicar la validez de los campos siguientes.</span><span class="sxs-lookup"><span data-stu-id="339bf-227">Validation bits used to indicate the validity of the subsequent fields.</span></span> <span data-ttu-id="339bf-228">Un valor de 1 (0x1) significa que el **\_ evento de SMBIOS** es válido.</span><span class="sxs-lookup"><span data-stu-id="339bf-228">A value of 1 (0x1) means that the **SMBIOS\_EVENT** is valid.</span></span>

<span data-ttu-id="339bf-229">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="339bf-229">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="339bf-230">Observaciones</span><span class="sxs-lookup"><span data-stu-id="339bf-230">Remarks</span></span>

<span data-ttu-id="339bf-231">La clase **MSMCAEvent \_ SMBIOSError** se deriva de [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="339bf-231">The **MSMCAEvent\_SMBIOSError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="339bf-232">Requisitos</span><span class="sxs-lookup"><span data-stu-id="339bf-232">Requirements</span></span>



| <span data-ttu-id="339bf-233">Requisito</span><span class="sxs-lookup"><span data-stu-id="339bf-233">Requirement</span></span> | <span data-ttu-id="339bf-234">Value</span><span class="sxs-lookup"><span data-stu-id="339bf-234">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="339bf-235">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="339bf-235">Minimum supported client</span></span><br/> | <span data-ttu-id="339bf-236">Windows XP</span><span class="sxs-lookup"><span data-stu-id="339bf-236">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="339bf-237">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="339bf-237">Minimum supported server</span></span><br/> | <span data-ttu-id="339bf-238">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="339bf-238">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="339bf-239">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="339bf-239">Namespace</span></span><br/>                | <span data-ttu-id="339bf-240">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="339bf-240">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="339bf-241">MOF</span><span class="sxs-lookup"><span data-stu-id="339bf-241">MOF</span></span><br/>                      | <dl> <span data-ttu-id="339bf-242"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-242"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="339bf-243">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="339bf-243">DLL</span></span><br/>                      | <dl> <span data-ttu-id="339bf-244"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="339bf-244"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="339bf-245">Vea también</span><span class="sxs-lookup"><span data-stu-id="339bf-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="339bf-246">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="339bf-246">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="339bf-247">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="339bf-247">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

