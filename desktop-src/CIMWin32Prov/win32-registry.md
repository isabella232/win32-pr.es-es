---
description: El registro de Win32 \_&\# 8194; La clase WMI representa el registro del sistema en un equipo que ejecuta Windows.
ms.assetid: 4a6cd7d7-2845-434d-b024-d6dbb77371ea
ms.tgt_platform: multiple
title: Win32_Registry (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Registry
- Win32_Registry.Caption
- Win32_Registry.Description
- Win32_Registry.InstallDate
- Win32_Registry.Status
- Win32_Registry.CurrentSize
- Win32_Registry.MaximumSize
- Win32_Registry.Name
- Win32_Registry.ProposedSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a1dc5fd89ee589aabda5da5f97632d86b39f6beb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998147"
---
# <a name="win32_registry-class"></a><span data-ttu-id="879e5-103">\_Clase del registro Win32</span><span class="sxs-lookup"><span data-stu-id="879e5-103">Win32\_Registry class</span></span>

<span data-ttu-id="879e5-104">La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ del registro de Win32** representa el registro del sistema en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="879e5-104">The **Win32\_Registry** [WMI class](../wmisdk/retrieving-a-class.md) represents the system registry on a computer system running Windows.</span></span>

<span data-ttu-id="879e5-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="879e5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="879e5-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="879e5-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="879e5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="879e5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Registry : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   CurrentSize;
  uint32   MaximumSize;
  string   Name;
  uint32   ProposedSize;
};
```

## <a name="members"></a><span data-ttu-id="879e5-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="879e5-108">Members</span></span>

<span data-ttu-id="879e5-109">La **clase \_ del registro Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="879e5-109">The **Win32\_Registry** class has these types of members:</span></span>

-   [<span data-ttu-id="879e5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="879e5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="879e5-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="879e5-111">Properties</span></span>

<span data-ttu-id="879e5-112">La **clase \_ del registro Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="879e5-112">The **Win32\_Registry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="879e5-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="879e5-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879e5-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="879e5-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="879e5-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="879e5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879e5-116">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="879e5-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="879e5-117">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="879e5-117">A short textual description of the object.</span></span>

<span data-ttu-id="879e5-118">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="879e5-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="879e5-119">**CurrentSize**</span><span class="sxs-lookup"><span data-stu-id="879e5-119">**CurrentSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879e5-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="879e5-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="879e5-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="879e5-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879e5-122">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \|NTDLL.DLL\| [**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| SystemRegistryQuotaInformation"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="879e5-122">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|NTDLL.DLL\|[**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation)\|SystemRegistryQuotaInformation"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="879e5-123">Tamaño físico actual del registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="879e5-123">Current physical size of the Windows registry.</span></span>

<span data-ttu-id="879e5-124">Ejemplo: 10</span><span class="sxs-lookup"><span data-stu-id="879e5-124">Example: 10</span></span>

</dd> <dt>

<span data-ttu-id="879e5-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="879e5-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879e5-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="879e5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="879e5-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="879e5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879e5-128">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="879e5-128">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="879e5-129">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="879e5-129">A textual description of the object.</span></span>

<span data-ttu-id="879e5-130">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="879e5-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="879e5-131">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="879e5-131">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879e5-132">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="879e5-132">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="879e5-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="879e5-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879e5-134">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="879e5-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="879e5-135">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="879e5-135">Indicates when the object was installed.</span></span> <span data-ttu-id="879e5-136">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="879e5-136">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="879e5-137">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="879e5-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="879e5-138">**Tamañomáximo**</span><span class="sxs-lookup"><span data-stu-id="879e5-138">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879e5-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="879e5-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="879e5-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="879e5-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879e5-141">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \| RegistrySizeLimit"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="879e5-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\|RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="879e5-142">Tamaño máximo del registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="879e5-142">Maximum size of the Windows registry.</span></span> <span data-ttu-id="879e5-143">Si el sistema se ejecuta correctamente con la propiedad **ProposedSize** , **MaximumSize** debe contener el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="879e5-143">If the system is successful in using the **ProposedSize** property, **MaximumSize** should contain the same value.</span></span>

</dd> <dt>

<span data-ttu-id="879e5-144">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="879e5-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879e5-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="879e5-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="879e5-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="879e5-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879e5-147">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="879e5-147">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="879e5-148">Nombre del registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="879e5-148">Name of the Windows registry.</span></span> <span data-ttu-id="879e5-149">La longitud máxima es de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="879e5-149">The maximum length is 256 characters.</span></span>

</dd> <dt>

<span data-ttu-id="879e5-150">**ProposedSize**</span><span class="sxs-lookup"><span data-stu-id="879e5-150">**ProposedSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879e5-151">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="879e5-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="879e5-152">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="879e5-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="879e5-153">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \| RegistrySizeLimit"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="879e5-153">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\|RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="879e5-154">Tamaño propuesto del registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="879e5-154">Proposed size of the Windows registry.</span></span> <span data-ttu-id="879e5-155">Es la única configuración del registro que se puede modificar y se intenta su propuesta la próxima vez que se arranque el sistema.</span><span class="sxs-lookup"><span data-stu-id="879e5-155">It is the only registry setting that can be modified, and its proposal is attempted the next time the system boots.</span></span>

</dd> <dt>

<span data-ttu-id="879e5-156">**Estado**</span><span class="sxs-lookup"><span data-stu-id="879e5-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879e5-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="879e5-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="879e5-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="879e5-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879e5-159">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="879e5-159">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="879e5-160">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="879e5-160">String that indicates the current status of the object.</span></span> <span data-ttu-id="879e5-161">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="879e5-161">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="879e5-162">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="879e5-162">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="879e5-163">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="879e5-163">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="879e5-164">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="879e5-164">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="879e5-165">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="879e5-165">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="879e5-166">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="879e5-166">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="879e5-167">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="879e5-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="879e5-168">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="879e5-168">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="879e5-169">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="879e5-169">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="879e5-170">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="879e5-170">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="879e5-171">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="879e5-171">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="879e5-172">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="879e5-172">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="879e5-173">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="879e5-173">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="879e5-174">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="879e5-174">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="879e5-175">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="879e5-175">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="879e5-176">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="879e5-176">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="879e5-177">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="879e5-177">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="879e5-178">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="879e5-178">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="879e5-179">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="879e5-179">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="879e5-180">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="879e5-180">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="879e5-181"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="879e5-181"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="879e5-182">Observaciones</span><span class="sxs-lookup"><span data-stu-id="879e5-182">Remarks</span></span>

<span data-ttu-id="879e5-183">La **clase \_ del registro Win32** se deriva [**de \_ LogicalElement CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="879e5-183">The **Win32\_Registry** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="879e5-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="879e5-184">Requirements</span></span>



| <span data-ttu-id="879e5-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="879e5-185">Requirement</span></span> | <span data-ttu-id="879e5-186">Value</span><span class="sxs-lookup"><span data-stu-id="879e5-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="879e5-187">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="879e5-187">Minimum supported client</span></span><br/> | <span data-ttu-id="879e5-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="879e5-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="879e5-189">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="879e5-189">Minimum supported server</span></span><br/> | <span data-ttu-id="879e5-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="879e5-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="879e5-191">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="879e5-191">Namespace</span></span><br/>                | <span data-ttu-id="879e5-192">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="879e5-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="879e5-193">MOF</span><span class="sxs-lookup"><span data-stu-id="879e5-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="879e5-194"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="879e5-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="879e5-195">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="879e5-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="879e5-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="879e5-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="879e5-197">Vea también</span><span class="sxs-lookup"><span data-stu-id="879e5-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="879e5-198">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="879e5-198">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="879e5-199">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="879e5-199">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
