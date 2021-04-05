---
description: Win32 \_ LogicalProgramGroup&\# 8194; La clase WMI representa un grupo de programas en un equipo que ejecuta Windows. Por ejemplo, accesorios o inicio.
ms.assetid: e05b512d-92ab-4864-b8df-f4a8b66761c9
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroup (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroup
- Win32_LogicalProgramGroup.Caption
- Win32_LogicalProgramGroup.Description
- Win32_LogicalProgramGroup.InstallDate
- Win32_LogicalProgramGroup.Status
- Win32_LogicalProgramGroup.GroupName
- Win32_LogicalProgramGroup.Name
- Win32_LogicalProgramGroup.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db7c7484489ecbc87e908dc6eb1c3de156cda665
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907416"
---
# <a name="win32_logicalprogramgroup-class"></a><span data-ttu-id="c5726-104">\_Clase Win32 LogicalProgramGroup</span><span class="sxs-lookup"><span data-stu-id="c5726-104">Win32\_LogicalProgramGroup class</span></span>

<span data-ttu-id="c5726-105">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LogicalProgramGroup de Win32** representa un grupo de programas en un equipo con Windows.</span><span class="sxs-lookup"><span data-stu-id="c5726-105">The **Win32\_LogicalProgramGroup** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a program group in a computer system running Windows.</span></span> <span data-ttu-id="c5726-106">Por ejemplo, accesorios o inicio.</span><span class="sxs-lookup"><span data-stu-id="c5726-106">For example, Accessories or Startup.</span></span>

<span data-ttu-id="c5726-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c5726-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c5726-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c5726-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5726-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5726-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{D52706F2-8045-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroup : Win32_ProgramGroupOrItem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   GroupName;
  string   Name;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="c5726-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="c5726-110">Members</span></span>

<span data-ttu-id="c5726-111">La **clase \_ LogicalProgramGroup de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c5726-111">The **Win32\_LogicalProgramGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="c5726-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c5726-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5726-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c5726-113">Properties</span></span>

<span data-ttu-id="c5726-114">La **clase \_ LogicalProgramGroup de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c5726-114">The **Win32\_LogicalProgramGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5726-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c5726-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5726-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c5726-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5726-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5726-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5726-118">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c5726-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c5726-119">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c5726-119">A short textual description of the object.</span></span>

<span data-ttu-id="c5726-120">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c5726-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5726-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5726-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5726-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c5726-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5726-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5726-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5726-124">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="c5726-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c5726-125">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c5726-125">A textual description of the object.</span></span>

<span data-ttu-id="c5726-126">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c5726-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5726-127">**GroupName**</span><span class="sxs-lookup"><span data-stu-id="c5726-127">**GroupName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5726-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c5726-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5726-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5726-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5726-130">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| CWbemProviderGlue métodos de clase \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="c5726-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="c5726-131">Nombre del grupo de programas de Windows.</span><span class="sxs-lookup"><span data-stu-id="c5726-131">Name of the Windows program group.</span></span> <span data-ttu-id="c5726-132">Los grupos de programas se implementan como carpetas de archivos en Win32.</span><span class="sxs-lookup"><span data-stu-id="c5726-132">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="c5726-133">Ejemplo: " \\ herramientas del sistema de accesorios"</span><span class="sxs-lookup"><span data-stu-id="c5726-133">Example: "Accessories\\System Tools"</span></span>

</dd> <dt>

<span data-ttu-id="c5726-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c5726-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5726-135">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c5726-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c5726-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5726-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5726-137">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="c5726-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c5726-138">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="c5726-138">Indicates when the object was installed.</span></span> <span data-ttu-id="c5726-139">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="c5726-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c5726-140">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c5726-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5726-141">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c5726-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5726-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c5726-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5726-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5726-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5726-144">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| CWbemProviderGlue Class Methods \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="c5726-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="c5726-145">Nombre asignado por el usuario seguido del nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="c5726-145">User-assigned name followed by the group name.</span></span> <span data-ttu-id="c5726-146">Los grupos de programas se implementan como carpetas de archivos en Win32.</span><span class="sxs-lookup"><span data-stu-id="c5726-146">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="c5726-147">Ejemplo: "todos los usuarios: accesorios \\ herramientas del sistema"</span><span class="sxs-lookup"><span data-stu-id="c5726-147">Example: "All Users:Accessories\\System Tools"</span></span>

</dd> <dt>

<span data-ttu-id="c5726-148">**Estado**</span><span class="sxs-lookup"><span data-stu-id="c5726-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5726-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c5726-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5726-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5726-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5726-151">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c5726-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c5726-152">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c5726-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="c5726-153">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="c5726-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c5726-154">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="c5726-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c5726-155">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="c5726-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c5726-156">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="c5726-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c5726-157">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="c5726-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c5726-158">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="c5726-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c5726-159">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c5726-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c5726-160">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c5726-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c5726-161">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="c5726-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c5726-162">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="c5726-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c5726-163">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c5726-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c5726-164">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="c5726-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c5726-165">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="c5726-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c5726-166">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="c5726-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c5726-167">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="c5726-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c5726-168">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="c5726-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c5726-169">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="c5726-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c5726-170">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c5726-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c5726-171">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="c5726-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c5726-172">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="c5726-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c5726-173">**UserName**</span><span class="sxs-lookup"><span data-stu-id="c5726-173">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5726-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c5726-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5726-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5726-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5726-176">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| CWbemProviderGlue métodos de clase \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="c5726-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="c5726-177">Usuarios que pueden tener acceso al grupo de programas de Windows.</span><span class="sxs-lookup"><span data-stu-id="c5726-177">Users who can access the Windows program group.</span></span> <span data-ttu-id="c5726-178">Los grupos de programas se implementan como carpetas de archivos en Win32.</span><span class="sxs-lookup"><span data-stu-id="c5726-178">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="c5726-179">Ejemplo: "todos los usuarios"</span><span class="sxs-lookup"><span data-stu-id="c5726-179">Example: "All Users"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5726-180">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5726-180">Remarks</span></span>

<span data-ttu-id="c5726-181">La **clase \_ LogicalProgramGroup de Win32** se deriva de [**\_ ProgramGroupOrItem de Win32**](win32-programgrouporitem.md).</span><span class="sxs-lookup"><span data-stu-id="c5726-181">The **Win32\_LogicalProgramGroup** class is derived from [**Win32\_ProgramGroupOrItem**](win32-programgrouporitem.md).</span></span>

<span data-ttu-id="c5726-182">El proceso de llamada que usa esta clase debe tener el privilegio de **\_ \_ nombre de restauración se** en el equipo en el que reside el registro.</span><span class="sxs-lookup"><span data-stu-id="c5726-182">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="c5726-183">Por ejemplo, si enumera esta clase en el equipo local, la cuenta con la que se ejecuta la aplicación debe tener este privilegio.</span><span class="sxs-lookup"><span data-stu-id="c5726-183">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="c5726-184">Para obtener más información, vea [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="c5726-184">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5726-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5726-185">Requirements</span></span>



| <span data-ttu-id="c5726-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5726-186">Requirement</span></span> | <span data-ttu-id="c5726-187">Value</span><span class="sxs-lookup"><span data-stu-id="c5726-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5726-188">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5726-188">Minimum supported client</span></span><br/> | <span data-ttu-id="c5726-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5726-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c5726-190">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5726-190">Minimum supported server</span></span><br/> | <span data-ttu-id="c5726-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5726-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c5726-192">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c5726-192">Namespace</span></span><br/>                | <span data-ttu-id="c5726-193">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c5726-193">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c5726-194">MOF</span><span class="sxs-lookup"><span data-stu-id="c5726-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5726-195"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5726-195"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5726-196">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5726-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5726-197"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5726-197"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5726-198">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5726-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5726-199">**Win32 \_ ProgramGroupOrItem**</span><span class="sxs-lookup"><span data-stu-id="c5726-199">**Win32\_ProgramGroupOrItem**</span></span>](win32-programgrouporitem.md)
</dt> <dt>

<span data-ttu-id="c5726-200">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c5726-200">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

