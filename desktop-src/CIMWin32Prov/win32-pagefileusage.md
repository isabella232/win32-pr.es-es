---
description: Win32 \_ PageFileUsage&\# 8194; La clase WMI representa el archivo usado para controlar el intercambio de archivos de memoria virtual en un sistema Win32. La información contenida en los objetos de los que se ha creado una instancia de esta clase especifica el estado de tiempo de ejecución del archivo de paginación.
ms.assetid: 635d7bd0-3738-4092-8b76-5e9583e079a9
ms.tgt_platform: multiple
title: Win32_PageFileUsage (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileUsage
- Win32_PageFileUsage.Caption
- Win32_PageFileUsage.Description
- Win32_PageFileUsage.InstallDate
- Win32_PageFileUsage.Status
- Win32_PageFileUsage.AllocatedBaseSize
- Win32_PageFileUsage.CurrentUsage
- Win32_PageFileUsage.Name
- Win32_PageFileUsage.PeakUsage
- Win32_PageFileUsage.TempPageFile
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9885bea242a9f2b781ccb0dcac479248a9ccc538
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539225"
---
# <a name="win32_pagefileusage-class"></a><span data-ttu-id="2d329-104">\_Clase Win32 PageFileUsage</span><span class="sxs-lookup"><span data-stu-id="2d329-104">Win32\_PageFileUsage class</span></span>

<span data-ttu-id="2d329-105">La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PageFileUsage de Win32** representa el archivo usado para controlar el intercambio de archivos de memoria virtual en un sistema Win32.</span><span class="sxs-lookup"><span data-stu-id="2d329-105">The **Win32\_PageFileUsage** [WMI class](../wmisdk/retrieving-a-class.md) represents the file used for handling virtual memory file swapping on a Win32 system.</span></span> <span data-ttu-id="2d329-106">La información contenida en los objetos de los que se ha creado una instancia de esta clase especifica el estado de tiempo de ejecución del archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="2d329-106">Information contained within objects instantiated from this class specify the run-time state of the page file.</span></span>

<span data-ttu-id="2d329-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2d329-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2d329-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2d329-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d329-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d329-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{9B3AC16A-EEE5-11d2-B13B-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileUsage : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AllocatedBaseSize;
  uint32   CurrentUsage;
  string   Name;
  uint32   PeakUsage;
  boolean  TempPageFile;
};
```

## <a name="members"></a><span data-ttu-id="2d329-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="2d329-110">Members</span></span>

<span data-ttu-id="2d329-111">La **clase \_ PageFileUsage de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2d329-111">The **Win32\_PageFileUsage** class has these types of members:</span></span>

-   [<span data-ttu-id="2d329-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2d329-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d329-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2d329-113">Properties</span></span>

<span data-ttu-id="2d329-114">La **clase \_ PageFileUsage de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2d329-114">The **Win32\_PageFileUsage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d329-115">**AllocatedBaseSize**</span><span class="sxs-lookup"><span data-stu-id="2d329-115">**AllocatedBaseSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d329-116">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d329-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d329-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d329-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d329-118">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwTotalPageFile"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="2d329-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwTotalPageFile"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="2d329-119">Cantidad real de espacio en disco asignado para su uso con este archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="2d329-119">Actual amount of disk space allocated for use with this page file.</span></span> <span data-ttu-id="2d329-120">Este valor corresponde al intervalo establecido en [**\_ PageFileSetting de Win32**](win32-pagefilesetting.md) en las propiedades **InitialSize** y **MaximumSize** , establecido al iniciar el sistema.</span><span class="sxs-lookup"><span data-stu-id="2d329-120">This value corresponds to the range established in [**Win32\_PageFileSetting**](win32-pagefilesetting.md) under the **InitialSize** and **MaximumSize** properties, set at system startup.</span></span>

<span data-ttu-id="2d329-121">Ejemplo: 178</span><span class="sxs-lookup"><span data-stu-id="2d329-121">Example: 178</span></span>

</dd> <dt>

<span data-ttu-id="2d329-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2d329-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d329-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2d329-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d329-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d329-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d329-125">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2d329-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2d329-126">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2d329-126">A short textual description of the object.</span></span>

<span data-ttu-id="2d329-127">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d329-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d329-128">**CurrentUsage**</span><span class="sxs-lookup"><span data-stu-id="2d329-128">**CurrentUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d329-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d329-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d329-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d329-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d329-131">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="2d329-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="2d329-132">Cantidad de espacio en disco utilizado actualmente por el archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="2d329-132">Amount of disk space currently used by the page file.</span></span>

</dd> <dt>

<span data-ttu-id="2d329-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2d329-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d329-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2d329-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d329-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d329-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d329-136">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="2d329-136">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2d329-137">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2d329-137">A textual description of the object.</span></span>

<span data-ttu-id="2d329-138">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d329-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d329-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2d329-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d329-140">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2d329-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2d329-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d329-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d329-142">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="2d329-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2d329-143">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="2d329-143">Indicates when the object was installed.</span></span> <span data-ttu-id="2d329-144">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="2d329-144">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2d329-145">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d329-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d329-146">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="2d329-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d329-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2d329-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d329-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d329-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d329-149">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2d329-149">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2d329-150">Nombre del archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="2d329-150">Name of the page file.</span></span>

<span data-ttu-id="2d329-151">Ejemplo: "C: \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="2d329-151">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="2d329-152">**PeakUsage**</span><span class="sxs-lookup"><span data-stu-id="2d329-152">**PeakUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d329-153">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d329-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d329-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d329-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d329-155">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="2d329-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="2d329-156">Archivo de paginación de uso más alto.</span><span class="sxs-lookup"><span data-stu-id="2d329-156">Highest use page file.</span></span>

</dd> <dt>

<span data-ttu-id="2d329-157">**Estado**</span><span class="sxs-lookup"><span data-stu-id="2d329-157">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d329-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2d329-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d329-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d329-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d329-160">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="2d329-160">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2d329-161">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2d329-161">String that indicates the current status of the object.</span></span> <span data-ttu-id="2d329-162">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="2d329-162">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2d329-163">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="2d329-163">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2d329-164">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="2d329-164">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2d329-165">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="2d329-165">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2d329-166">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="2d329-166">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2d329-167">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="2d329-167">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2d329-168">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d329-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2d329-169">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2d329-169">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2d329-170">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="2d329-170">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2d329-171">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="2d329-171">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2d329-172">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="2d329-172">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2d329-173">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="2d329-173">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2d329-174">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="2d329-174">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2d329-175">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="2d329-175">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2d329-176">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="2d329-176">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2d329-177">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="2d329-177">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2d329-178">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="2d329-178">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2d329-179">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="2d329-179">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2d329-180">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="2d329-180">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2d329-181">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="2d329-181">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2d329-182">**TempPageFile**</span><span class="sxs-lookup"><span data-stu-id="2d329-182">**TempPageFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d329-183">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2d329-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d329-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d329-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d329-185">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Session Manager \\ \\ Memory Management \| TempPageFile")</span><span class="sxs-lookup"><span data-stu-id="2d329-185">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|TempPageFile")</span></span>
</dt> </dl>

<span data-ttu-id="2d329-186">Si **es true**, se ha creado un archivo de página temporal, normalmente porque no hay ningún archivo de paginación permanente en el sistema del equipo actual.</span><span class="sxs-lookup"><span data-stu-id="2d329-186">If **true**, a temporary page file has been created, usually because there is no permanent page file on the current computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d329-187">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d329-187">Remarks</span></span>

<span data-ttu-id="2d329-188">La **clase \_ PageFileUsage de Win32** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d329-188">The **Win32\_PageFileUsage** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d329-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d329-189">Requirements</span></span>



| <span data-ttu-id="2d329-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d329-190">Requirement</span></span> | <span data-ttu-id="2d329-191">Value</span><span class="sxs-lookup"><span data-stu-id="2d329-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d329-192">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d329-192">Minimum supported client</span></span><br/> | <span data-ttu-id="2d329-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d329-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2d329-194">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d329-194">Minimum supported server</span></span><br/> | <span data-ttu-id="2d329-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d329-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2d329-196">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2d329-196">Namespace</span></span><br/>                | <span data-ttu-id="2d329-197">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2d329-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2d329-198">MOF</span><span class="sxs-lookup"><span data-stu-id="2d329-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d329-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d329-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d329-200">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2d329-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d329-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d329-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d329-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d329-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d329-203">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="2d329-203">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="2d329-204">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2d329-204">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
