---
description: Indica un error de componente PCI de arquitectura de comprobación de equipo (MCA). Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: 2b241333-2ea5-42cb-bdd3-27a10df51f3e
title: MSMCAEvent_PCIComponentError (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIComponentError
- MSMCAEvent_PCIComponentError.Active
- MSMCAEvent_PCIComponentError.AdditionalErrors
- MSMCAEvent_PCIComponentError.Cpu
- MSMCAEvent_PCIComponentError.ErrorSeverity
- MSMCAEvent_PCIComponentError.InstanceName
- MSMCAEvent_PCIComponentError.PCI_COMP_ERROR_STATUS
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_BusNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeBaseClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeInterface
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeSubClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceId
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_FunctionNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_SegmentNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_VendorId
- MSMCAEvent_PCIComponentError.RawRecord
- MSMCAEvent_PCIComponentError.RecordId
- MSMCAEvent_PCIComponentError.Size
- MSMCAEvent_PCIComponentError.Type
- MSMCAEvent_PCIComponentError.VALIDATION_BITS
- MSMCAEvent_PCIComponentError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cbcf3ee13e822fd59cdcdd30538d5e369d798aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706943"
---
# <a name="msmcaevent_pcicomponenterror-class"></a><span data-ttu-id="d4e74-104">MSMCAEvent \_ PCIComponentError (clase)</span><span class="sxs-lookup"><span data-stu-id="d4e74-104">MSMCAEvent\_PCIComponentError class</span></span>

<span data-ttu-id="d4e74-105">La clase **MSMCAEvent \_ PCIComponentError** indica un error de componente PCI de arquitectura de comprobación de equipo (MCA).</span><span class="sxs-lookup"><span data-stu-id="d4e74-105">The **MSMCAEvent\_PCIComponentError** class indicates an Machine Check Architecture (MCA) PCI component error.</span></span> <span data-ttu-id="d4e74-106">Esta clase solo está disponible en sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d4e74-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="d4e74-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d4e74-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d4e74-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d4e74-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4e74-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4e74-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PCIComponentError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_COMP_ERROR_STATUS;
  uint8   PCI_COMP_INFO_BusNumber;
  uint8   PCI_COMP_INFO_ClassCodeBaseClass;
  uint8   PCI_COMP_INFO_ClassCodeInterface;
  uint8   PCI_COMP_INFO_ClassCodeSubClass;
  uint16  PCI_COMP_INFO_DeviceId;
  uint8   PCI_COMP_INFO_DeviceNumber;
  uint8   PCI_COMP_INFO_FunctionNumber;
  uint8   PCI_COMP_INFO_SegmentNumber;
  uint16  PCI_COMP_INFO_VendorId;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="d4e74-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="d4e74-110">Members</span></span>

<span data-ttu-id="d4e74-111">La clase **MSMCAEvent \_ PCIComponentError** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d4e74-111">The **MSMCAEvent\_PCIComponentError** class has these types of members:</span></span>

-   [<span data-ttu-id="d4e74-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d4e74-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d4e74-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d4e74-113">Properties</span></span>

<span data-ttu-id="d4e74-114">La clase **MSMCAEvent \_ PCIComponentError** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d4e74-114">The **MSMCAEvent\_PCIComponentError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d4e74-115">**Activo**</span><span class="sxs-lookup"><span data-stu-id="d4e74-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-116">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d4e74-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-118">**True** si esta instancia de la clase está activa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="d4e74-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="d4e74-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4e74-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-122">Número de errores adicionales en el registro.</span><span class="sxs-lookup"><span data-stu-id="d4e74-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-123">**CPU**</span><span class="sxs-lookup"><span data-stu-id="d4e74-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4e74-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-126">CPU que ha detectado el error.</span><span class="sxs-lookup"><span data-stu-id="d4e74-126">CPU that reported the error.</span></span> <span data-ttu-id="d4e74-127">Esta propiedad solo se aplica a un sistema de varios procesadores en el que el primer procesador tiene asignado el número 0, el segundo procesador tiene asignado el número 1 y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="d4e74-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="d4e74-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-129">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d4e74-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-131">Nivel de gravedad del error comunicado.</span><span class="sxs-lookup"><span data-stu-id="d4e74-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="d4e74-132">Value</span><span class="sxs-lookup"><span data-stu-id="d4e74-132">Value</span></span>                                                                                                | <span data-ttu-id="d4e74-133">Significado</span><span class="sxs-lookup"><span data-stu-id="d4e74-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="d4e74-134"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="d4e74-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="d4e74-135">Recuperable</span><span class="sxs-lookup"><span data-stu-id="d4e74-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="d4e74-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="d4e74-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="d4e74-137">Crítico</span><span class="sxs-lookup"><span data-stu-id="d4e74-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="d4e74-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="d4e74-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="d4e74-139">Corregible</span><span class="sxs-lookup"><span data-stu-id="d4e74-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d4e74-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="d4e74-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d4e74-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-143">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d4e74-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-144">Identificador único de esta instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="d4e74-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="d4e74-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4e74-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-148">Si es 0 (cero), este evento no se registra en el registro de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="d4e74-148">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-149">**\_Estado de \_ error de COMP de PCI \_**</span><span class="sxs-lookup"><span data-stu-id="d4e74-149">**PCI\_COMP\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-150">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d4e74-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-152">Código de error interno.</span><span class="sxs-lookup"><span data-stu-id="d4e74-152">Internal error code.</span></span>

<span data-ttu-id="d4e74-153">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d4e74-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-154">**Información de COMP de PCI \_ \_ \_ BusNumber**</span><span class="sxs-lookup"><span data-stu-id="d4e74-154">**PCI\_COMP\_INFO\_BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-155">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d4e74-155">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-157">Número de bus del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="d4e74-157">Bus number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-158">**Información de COMP de PCI \_ \_ \_ ClassCodeBaseClass**</span><span class="sxs-lookup"><span data-stu-id="d4e74-158">**PCI\_COMP\_INFO\_ClassCodeBaseClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-159">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d4e74-159">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-161">Código de clase de la clase base del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="d4e74-161">Class code of the base class of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-162">**Información de COMP de PCI \_ \_ \_ ClassCodeInterface**</span><span class="sxs-lookup"><span data-stu-id="d4e74-162">**PCI\_COMP\_INFO\_ClassCodeInterface**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-163">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d4e74-163">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-165">Interfaz de código de clase del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="d4e74-165">Class code interface of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-166">**Información de COMP de PCI \_ \_ \_ ClassCodeSubClass**</span><span class="sxs-lookup"><span data-stu-id="d4e74-166">**PCI\_COMP\_INFO\_ClassCodeSubClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-167">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d4e74-167">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-169">Subclase de código de clase del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="d4e74-169">Class code subclass of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-170">**\_DeviceId de \_ información de comp. de PCI \_**</span><span class="sxs-lookup"><span data-stu-id="d4e74-170">**PCI\_COMP\_INFO\_DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-171">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4e74-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-173">Identificador de dispositivo del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="d4e74-173">Device identifier of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-174">**Información de COMP de PCI \_ \_ \_ DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="d4e74-174">**PCI\_COMP\_INFO\_DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-175">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d4e74-175">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-177">Número de dispositivo del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="d4e74-177">Device number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-178">**Información de COMP de PCI \_ \_ \_ FunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="d4e74-178">**PCI\_COMP\_INFO\_FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-179">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d4e74-179">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-181">Número de función del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="d4e74-181">Function number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-182">**Información de COMP de PCI \_ \_ \_ SegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="d4e74-182">**PCI\_COMP\_INFO\_SegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-183">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d4e74-183">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-185">Número de segmento del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="d4e74-185">Segment number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-186">**ID. de información de COMP de PCI \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4e74-186">**PCI\_COMP\_INFO\_VendorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-187">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4e74-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-189">Identificador del proveedor del componente PCI.</span><span class="sxs-lookup"><span data-stu-id="d4e74-189">Vendor identifier of the PCI Component.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-190">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="d4e74-190">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-191">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="d4e74-191">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-193">Matriz de bytes que contiene el registro de errores sin procesar.</span><span class="sxs-lookup"><span data-stu-id="d4e74-193">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="d4e74-194">El número de elementos de la matriz que especifica la propiedad **size** .</span><span class="sxs-lookup"><span data-stu-id="d4e74-194">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-195">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="d4e74-195">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-196">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d4e74-196">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-198">Identificador de registro del registro de errores para este error.</span><span class="sxs-lookup"><span data-stu-id="d4e74-198">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="d4e74-199">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d4e74-199">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-200">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="d4e74-200">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-201">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4e74-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-203">Tamaño del registro de errores sin procesar.</span><span class="sxs-lookup"><span data-stu-id="d4e74-203">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-204">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d4e74-204">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-205">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4e74-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-207">Tipo de mensaje de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="d4e74-207">Type of event log message.</span></span> <span data-ttu-id="d4e74-208">Estos mensajes se corresponden con los códigos de mensaje de registro de eventos utilizados para insertar mensajes de registro de eventos del proveedor de consumidores del registro de eventos de Windows cuando recibe uno de los eventos.</span><span class="sxs-lookup"><span data-stu-id="d4e74-208">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="d4e74-209">**BITS de validación \_**</span><span class="sxs-lookup"><span data-stu-id="d4e74-209">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4e74-210">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d4e74-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d4e74-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4e74-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4e74-212">Bits de validación que se usan para indicar la validez de los campos siguientes.</span><span class="sxs-lookup"><span data-stu-id="d4e74-212">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="d4e74-213">Valores</span><span class="sxs-lookup"><span data-stu-id="d4e74-213">Values</span></span>                                                                               | <span data-ttu-id="d4e74-214">Significado</span><span class="sxs-lookup"><span data-stu-id="d4e74-214">Meaning</span></span>                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="d4e74-215"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="d4e74-215"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="d4e74-216">El estado de error de la COMP de PCI \_ \_ \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="d4e74-216">PCI\_COMP\_ERROR\_STATUS is valid.</span></span><br/>    |
| <dl> <span data-ttu-id="d4e74-217"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="d4e74-217"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="d4e74-218">La \_ información de COMP de PCI \_ es válida.</span><span class="sxs-lookup"><span data-stu-id="d4e74-218">PCI\_COMP\_INFO is valid.</span></span><br/>             |
| <dl> <span data-ttu-id="d4e74-219"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="d4e74-219"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="d4e74-220">El \_ número de MEM de COMP PCI \_ \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="d4e74-220">PCI\_COMP\_MEM\_NUM is valid.</span></span><br/>         |
| <dl> <span data-ttu-id="d4e74-221"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="d4e74-221"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="d4e74-222">El \_ número de e/s de COMP de PCI \_ \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="d4e74-222">PCI\_COMP\_IO\_NUM is valid.</span></span><br/>          |
| <dl> <span data-ttu-id="d4e74-223"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="d4e74-223"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="d4e74-224">El \_ par de datos REGS de COMP PCI \_ \_ \_ es válido.</span><span class="sxs-lookup"><span data-stu-id="d4e74-224">PCI\_COMP\_REGS\_DATA\_PAIR is valid.</span></span><br/> |



 

<span data-ttu-id="d4e74-225">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d4e74-225">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4e74-226">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4e74-226">Remarks</span></span>

<span data-ttu-id="d4e74-227">La clase **MSMCAEvent \_ PCIComponentError** se deriva de [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="d4e74-227">The **MSMCAEvent\_PCIComponentError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4e74-228">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4e74-228">Requirements</span></span>



| <span data-ttu-id="d4e74-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4e74-229">Requirement</span></span> | <span data-ttu-id="d4e74-230">Value</span><span class="sxs-lookup"><span data-stu-id="d4e74-230">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4e74-231">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4e74-231">Minimum supported client</span></span><br/> | <span data-ttu-id="d4e74-232">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d4e74-232">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="d4e74-233">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4e74-233">Minimum supported server</span></span><br/> | <span data-ttu-id="d4e74-234">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4e74-234">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="d4e74-235">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d4e74-235">Namespace</span></span><br/>                | <span data-ttu-id="d4e74-236">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="d4e74-236">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="d4e74-237">MOF</span><span class="sxs-lookup"><span data-stu-id="d4e74-237">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4e74-238"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4e74-238"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4e74-239">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d4e74-239">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4e74-240"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4e74-240"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4e74-241">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4e74-241">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4e74-242">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="d4e74-242">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="d4e74-243">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="d4e74-243">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

