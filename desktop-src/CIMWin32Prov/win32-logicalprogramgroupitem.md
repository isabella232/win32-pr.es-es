---
description: Win32 \_ LogicalProgramGroupItem&\# 8194; La clase WMI representa un elemento incluido en un \_ LogicalProgramGroup de Win32 que no es también otra instancia de Win32 \_ LogicalProgramGroup.
ms.assetid: 70b127bf-4e94-4c1a-98ff-909bdfe0f009
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroupItem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItem
- Win32_LogicalProgramGroupItem.Caption
- Win32_LogicalProgramGroupItem.Description
- Win32_LogicalProgramGroupItem.InstallDate
- Win32_LogicalProgramGroupItem.Status
- Win32_LogicalProgramGroupItem.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1afd78ba17e444520d8dec81eac05fffa103aede
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539358"
---
# <a name="win32_logicalprogramgroupitem-class"></a><span data-ttu-id="71b5a-103">\_Clase Win32 LogicalProgramGroupItem</span><span class="sxs-lookup"><span data-stu-id="71b5a-103">Win32\_LogicalProgramGroupItem class</span></span>

<span data-ttu-id="71b5a-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LogicalProgramGroupItem de Win32** representa un elemento incluido en [**un \_ LogicalProgramGroup Win32**](win32-logicalprogramgroup.md) que no es también otra instancia **\_ LogicalProgramGroup de Win32** .</span><span class="sxs-lookup"><span data-stu-id="71b5a-104">The **Win32\_LogicalProgramGroupItem** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an element contained by a [**Win32\_LogicalProgramGroup**](win32-logicalprogramgroup.md) that is not also another **Win32\_LogicalProgramGroup** instance.</span></span>

<span data-ttu-id="71b5a-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="71b5a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="71b5a-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="71b5a-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="71b5a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71b5a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{86E30E82-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItem : Win32_ProgramGroupOrItem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="71b5a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="71b5a-108">Members</span></span>

<span data-ttu-id="71b5a-109">La **clase \_ LogicalProgramGroupItem de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="71b5a-109">The **Win32\_LogicalProgramGroupItem** class has these types of members:</span></span>

-   [<span data-ttu-id="71b5a-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="71b5a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71b5a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="71b5a-111">Properties</span></span>

<span data-ttu-id="71b5a-112">La **clase \_ LogicalProgramGroupItem de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="71b5a-112">The **Win32\_LogicalProgramGroupItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71b5a-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="71b5a-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71b5a-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71b5a-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71b5a-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71b5a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71b5a-116">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="71b5a-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="71b5a-117">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="71b5a-117">A short textual description of the object.</span></span>

<span data-ttu-id="71b5a-118">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71b5a-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71b5a-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="71b5a-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71b5a-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71b5a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71b5a-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71b5a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71b5a-122">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="71b5a-122">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="71b5a-123">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="71b5a-123">A textual description of the object.</span></span>

<span data-ttu-id="71b5a-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71b5a-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71b5a-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="71b5a-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71b5a-126">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="71b5a-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="71b5a-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71b5a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71b5a-128">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="71b5a-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="71b5a-129">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="71b5a-129">Indicates when the object was installed.</span></span> <span data-ttu-id="71b5a-130">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="71b5a-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="71b5a-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71b5a-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71b5a-132">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="71b5a-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71b5a-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71b5a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71b5a-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71b5a-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71b5a-135">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| CWbemProviderGlue Class Methods \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="71b5a-135">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="71b5a-136">Instancia de dentro de un equipo.</span><span class="sxs-lookup"><span data-stu-id="71b5a-136">Instance within a computer system.</span></span> <span data-ttu-id="71b5a-137">Los grupos de programas se implementan como carpetas de archivos en Win32.</span><span class="sxs-lookup"><span data-stu-id="71b5a-137">Program groups are implemented as file folders in Win32.</span></span> <span data-ttu-id="71b5a-138">Se deben proporcionar los nombres de ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="71b5a-138">Full path names should be provided.</span></span>

<span data-ttu-id="71b5a-139">Ejemplo: "C: \\ usuarios \\ *alguien* \\ AppData \\ móvil en \\ \\ \\ el menú Inicio de Microsoft Windows \\ \\ accesorios \\ Notepad. lnk"</span><span class="sxs-lookup"><span data-stu-id="71b5a-139">Example: "C:\\Users\\*someone*\\AppData\\Roaming\\Microsoft\\Windows\\Start Menu\\Programs\\Accessories\\NotePad.Lnk"</span></span>

</dd> <dt>

<span data-ttu-id="71b5a-140">**Estado**</span><span class="sxs-lookup"><span data-stu-id="71b5a-140">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71b5a-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71b5a-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71b5a-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71b5a-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71b5a-143">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="71b5a-143">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="71b5a-144">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="71b5a-144">String that indicates the current status of the object.</span></span> <span data-ttu-id="71b5a-145">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="71b5a-145">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="71b5a-146">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="71b5a-146">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="71b5a-147">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="71b5a-147">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="71b5a-148">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="71b5a-148">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="71b5a-149">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="71b5a-149">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="71b5a-150">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="71b5a-150">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="71b5a-151">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71b5a-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="71b5a-152">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="71b5a-152">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="71b5a-153">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="71b5a-153">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="71b5a-154">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="71b5a-154">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="71b5a-155">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="71b5a-155">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71b5a-156">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="71b5a-156">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="71b5a-157">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="71b5a-157">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="71b5a-158">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="71b5a-158">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="71b5a-159">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="71b5a-159">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="71b5a-160">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="71b5a-160">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="71b5a-161">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="71b5a-161">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="71b5a-162">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="71b5a-162">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="71b5a-163">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="71b5a-163">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="71b5a-164">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="71b5a-164">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="71b5a-165"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="71b5a-165"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="71b5a-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71b5a-166">Remarks</span></span>

<span data-ttu-id="71b5a-167">La **clase \_ LogicalProgramGroupItem de Win32** se deriva de [**\_ ProgramGroupOrItem de Win32**](win32-programgrouporitem.md).</span><span class="sxs-lookup"><span data-stu-id="71b5a-167">The **Win32\_LogicalProgramGroupItem** class is derived from [**Win32\_ProgramGroupOrItem**](win32-programgrouporitem.md).</span></span>

<span data-ttu-id="71b5a-168">El proceso de llamada que usa esta clase debe tener el privilegio de **\_ \_ nombre de restauración se** en el equipo en el que reside el registro.</span><span class="sxs-lookup"><span data-stu-id="71b5a-168">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="71b5a-169">Por ejemplo, si enumera esta clase en el equipo local, la cuenta con la que se ejecuta la aplicación debe tener este privilegio.</span><span class="sxs-lookup"><span data-stu-id="71b5a-169">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="71b5a-170">Para obtener más información, vea [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="71b5a-170">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="71b5a-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71b5a-171">Requirements</span></span>



| <span data-ttu-id="71b5a-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="71b5a-172">Requirement</span></span> | <span data-ttu-id="71b5a-173">Value</span><span class="sxs-lookup"><span data-stu-id="71b5a-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71b5a-174">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71b5a-174">Minimum supported client</span></span><br/> | <span data-ttu-id="71b5a-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71b5a-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="71b5a-176">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71b5a-176">Minimum supported server</span></span><br/> | <span data-ttu-id="71b5a-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71b5a-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="71b5a-178">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="71b5a-178">Namespace</span></span><br/>                | <span data-ttu-id="71b5a-179">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="71b5a-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="71b5a-180">MOF</span><span class="sxs-lookup"><span data-stu-id="71b5a-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71b5a-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71b5a-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="71b5a-182">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="71b5a-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71b5a-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71b5a-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71b5a-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="71b5a-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b5a-185">**Win32 \_ ProgramGroupOrItem**</span><span class="sxs-lookup"><span data-stu-id="71b5a-185">**Win32\_ProgramGroupOrItem**</span></span>](win32-programgrouporitem.md)
</dt> <dt>

<span data-ttu-id="71b5a-186">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="71b5a-186">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

