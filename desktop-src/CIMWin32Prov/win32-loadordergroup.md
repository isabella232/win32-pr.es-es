---
description: La \_ clase WMI LoadOrderGroup de Win32 representa un grupo de servicios del sistema que definen las dependencias de la ejecución.
ms.assetid: 0aa3151e-6622-46b4-9050-4e1c4c720902
ms.tgt_platform: multiple
title: Win32_LoadOrderGroup (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroup
- Win32_LoadOrderGroup.Caption
- Win32_LoadOrderGroup.Description
- Win32_LoadOrderGroup.InstallDate
- Win32_LoadOrderGroup.Status
- Win32_LoadOrderGroup.DriverEnabled
- Win32_LoadOrderGroup.GroupOrder
- Win32_LoadOrderGroup.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b81a6cb282018692fb72c8dbfe5ef0c5c74fe815
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153429"
---
# <a name="win32_loadordergroup-class"></a><span data-ttu-id="7033d-103">\_Clase Win32 LoadOrderGroup</span><span class="sxs-lookup"><span data-stu-id="7033d-103">Win32\_LoadOrderGroup class</span></span>

<span data-ttu-id="7033d-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LoadOrderGroup de Win32** representa un grupo de servicios del sistema que definen las dependencias de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="7033d-104">The **Win32\_LoadOrderGroup** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="7033d-105">Los servicios deben iniciarse en el orden especificado por el grupo de orden de carga, ya que los servicios dependen entre sí.</span><span class="sxs-lookup"><span data-stu-id="7033d-105">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="7033d-106">Estos servicios dependientes requieren la presencia de los servicios antecedentes para que funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="7033d-106">These dependent services require the presence of the antecedent services to function correctly.</span></span> <span data-ttu-id="7033d-107">Los datos de esta clase los deriva el proveedor de la clave del registro: **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **control** \\ **ServiceGroupOrder**.</span><span class="sxs-lookup"><span data-stu-id="7033d-107">The data in this class is derived by the provider from the registry key: **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**.</span></span>

<span data-ttu-id="7033d-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7033d-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7033d-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7033d-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7033d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7033d-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroup : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  DriverEnabled;
  uint32   GroupOrder;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="7033d-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="7033d-111">Members</span></span>

<span data-ttu-id="7033d-112">La **clase \_ LoadOrderGroup de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7033d-112">The **Win32\_LoadOrderGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="7033d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7033d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7033d-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7033d-114">Properties</span></span>

<span data-ttu-id="7033d-115">La **clase \_ LoadOrderGroup de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7033d-115">The **Win32\_LoadOrderGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7033d-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7033d-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7033d-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7033d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7033d-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7033d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7033d-119">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7033d-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7033d-120">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7033d-120">A short textual description of the object.</span></span>

<span data-ttu-id="7033d-121">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7033d-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7033d-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7033d-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7033d-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7033d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7033d-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7033d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7033d-125">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="7033d-125">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7033d-126">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7033d-126">A textual description of the object.</span></span>

<span data-ttu-id="7033d-127">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7033d-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7033d-128">**DriverEnabled**</span><span class="sxs-lookup"><span data-stu-id="7033d-128">**DriverEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7033d-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7033d-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7033d-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7033d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7033d-131">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ GroupOrderList")</span><span class="sxs-lookup"><span data-stu-id="7033d-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="7033d-132">Indica si este grupo de orden de carga puede incluir controladores junto con servicios del sistema.</span><span class="sxs-lookup"><span data-stu-id="7033d-132">Indicates whether this load order group can include drivers along with system services.</span></span>

</dd> <dt>

<span data-ttu-id="7033d-133">**GroupOrder**</span><span class="sxs-lookup"><span data-stu-id="7033d-133">**GroupOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7033d-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7033d-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7033d-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7033d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7033d-136">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ GroupOrderList")</span><span class="sxs-lookup"><span data-stu-id="7033d-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="7033d-137">Secuencia en la que se carga este grupo de servicios en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7033d-137">Sequence in which this group of services is loaded onto the operating system.</span></span>

<span data-ttu-id="7033d-138">Ejemplo: 2</span><span class="sxs-lookup"><span data-stu-id="7033d-138">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="7033d-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7033d-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7033d-140">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7033d-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7033d-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7033d-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7033d-142">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="7033d-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7033d-143">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="7033d-143">Indicates when the object was installed.</span></span> <span data-ttu-id="7033d-144">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="7033d-144">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7033d-145">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7033d-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7033d-146">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="7033d-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7033d-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7033d-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7033d-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7033d-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7033d-149">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ GroupOrderList")</span><span class="sxs-lookup"><span data-stu-id="7033d-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="7033d-150">Nombre del grupo de orden de carga.</span><span class="sxs-lookup"><span data-stu-id="7033d-150">Name of the load order group.</span></span>

<span data-ttu-id="7033d-151">Ejemplo: "disco principal"</span><span class="sxs-lookup"><span data-stu-id="7033d-151">Example: "Primary disk"</span></span>

</dd> <dt>

<span data-ttu-id="7033d-152">**Estado**</span><span class="sxs-lookup"><span data-stu-id="7033d-152">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7033d-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7033d-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7033d-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7033d-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7033d-155">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="7033d-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7033d-156">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7033d-156">String that indicates the current status of the object.</span></span> <span data-ttu-id="7033d-157">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="7033d-157">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7033d-158">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="7033d-158">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7033d-159">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="7033d-159">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7033d-160">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="7033d-160">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7033d-161">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="7033d-161">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7033d-162">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="7033d-162">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7033d-163">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7033d-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7033d-164">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7033d-164">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7033d-165">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="7033d-165">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7033d-166">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="7033d-166">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7033d-167">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="7033d-167">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7033d-168">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="7033d-168">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7033d-169">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="7033d-169">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7033d-170">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="7033d-170">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7033d-171">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="7033d-171">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7033d-172">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="7033d-172">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7033d-173">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="7033d-173">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7033d-174">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="7033d-174">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7033d-175">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="7033d-175">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7033d-176">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="7033d-176">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="7033d-177"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7033d-177"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="7033d-178">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7033d-178">Remarks</span></span>

<span data-ttu-id="7033d-179">La **clase \_ LoadOrderGroup de Win32** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7033d-179">The **Win32\_LoadOrderGroup** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7033d-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7033d-180">Requirements</span></span>



| <span data-ttu-id="7033d-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="7033d-181">Requirement</span></span> | <span data-ttu-id="7033d-182">Value</span><span class="sxs-lookup"><span data-stu-id="7033d-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7033d-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7033d-183">Minimum supported client</span></span><br/> | <span data-ttu-id="7033d-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7033d-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7033d-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7033d-185">Minimum supported server</span></span><br/> | <span data-ttu-id="7033d-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7033d-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7033d-187">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7033d-187">Namespace</span></span><br/>                | <span data-ttu-id="7033d-188">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7033d-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7033d-189">MOF</span><span class="sxs-lookup"><span data-stu-id="7033d-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7033d-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7033d-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7033d-191">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7033d-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7033d-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7033d-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7033d-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="7033d-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7033d-194">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="7033d-194">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="7033d-195">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7033d-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

