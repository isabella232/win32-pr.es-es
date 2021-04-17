---
description: La \_ clase de subproceso CIM representa la capacidad de ejecutar unidades de un proceso o una tarea, en paralelo. Un proceso puede tener muchos subprocesos, cada uno de los cuales es débil para el proceso.
ms.assetid: 57222d57-61bd-4641-a77c-805263be04b7
ms.tgt_platform: multiple
title: CIM_Thread (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Thread
- CIM_Thread.Caption
- CIM_Thread.CreationClassName
- CIM_Thread.CSCreationClassName
- CIM_Thread.CSName
- CIM_Thread.Description
- CIM_Thread.ExecutionState
- CIM_Thread.Handle
- CIM_Thread.InstallDate
- CIM_Thread.KernelModeTime
- CIM_Thread.Name
- CIM_Thread.OSCreationClassName
- CIM_Thread.OSName
- CIM_Thread.Priority
- CIM_Thread.ProcessCreationClassName
- CIM_Thread.ProcessHandle
- CIM_Thread.Status
- CIM_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0a69554ef50a82695d2904b11f4189c3aab11b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659772"
---
# <a name="cim_thread-class"></a><span data-ttu-id="7ce07-104">\_Clase de subproceso CIM</span><span class="sxs-lookup"><span data-stu-id="7ce07-104">CIM\_Thread class</span></span>

<span data-ttu-id="7ce07-105">La clase de **\_ subproceso CIM** representa la capacidad de ejecutar unidades de un proceso o una tarea, en paralelo.</span><span class="sxs-lookup"><span data-stu-id="7ce07-105">The **CIM\_Thread** class represents the ability to execute units of a process or task, in parallel.</span></span> <span data-ttu-id="7ce07-106">Un proceso puede tener muchos subprocesos, cada uno de los cuales es débil para el proceso.</span><span class="sxs-lookup"><span data-stu-id="7ce07-106">A process can have many threads, each of which is weak to the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7ce07-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="7ce07-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7ce07-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7ce07-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7ce07-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7ce07-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7ce07-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7ce07-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ce07-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ce07-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C571-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Thread : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  string   ProcessCreationClassName;
  string   ProcessHandle;
  string   Status;
  uint64   UserModeTime;
};
```

## <a name="members"></a><span data-ttu-id="7ce07-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="7ce07-112">Members</span></span>

<span data-ttu-id="7ce07-113">La clase de **\_ subproceso CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7ce07-113">The **CIM\_Thread** class has these types of members:</span></span>

-   [<span data-ttu-id="7ce07-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ce07-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ce07-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ce07-115">Properties</span></span>

<span data-ttu-id="7ce07-116">La clase de **\_ subproceso CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7ce07-116">The **CIM\_Thread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ce07-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7ce07-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7ce07-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-120">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7ce07-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-121">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7ce07-121">Short textual description of the object.</span></span>

<span data-ttu-id="7ce07-122">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7ce07-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ce07-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7ce07-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7ce07-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-126">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7ce07-126">Qualifiers: [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-127">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="7ce07-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7ce07-128">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="7ce07-128">When used with other key properties of the class, this property allow all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="7ce07-129">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7ce07-129">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7ce07-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-132">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ proceso de CIM**](cim-process.md).**CSCreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7ce07-132">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CSCreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-133">Ámbito del nombre de la clase de creación del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="7ce07-133">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="7ce07-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="7ce07-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7ce07-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-137">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ proceso de CIM**](cim-process.md).**CSName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7ce07-137">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CSName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-138">Ámbito del nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="7ce07-138">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="7ce07-139">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7ce07-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7ce07-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-142">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="7ce07-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-143">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7ce07-143">Textual description of the object.</span></span>

<span data-ttu-id="7ce07-144">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7ce07-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ce07-145">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="7ce07-145">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-146">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7ce07-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-148">Indica la condición operativa actual del subproceso.</span><span class="sxs-lookup"><span data-stu-id="7ce07-148">Indicates the current operating condition of the thread.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7ce07-149">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="7ce07-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7ce07-150">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="7ce07-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="7ce07-151">**Listo** (2)</span><span class="sxs-lookup"><span data-stu-id="7ce07-151">**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="7ce07-152">En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="7ce07-152">**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="7ce07-153">**Bloqueado** (4)</span><span class="sxs-lookup"><span data-stu-id="7ce07-153">**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="7ce07-154">**Suspendido bloqueado** (5)</span><span class="sxs-lookup"><span data-stu-id="7ce07-154">**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="7ce07-155">**Suspendido preparado** (6)</span><span class="sxs-lookup"><span data-stu-id="7ce07-155">**Suspended Ready** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7ce07-156">**Handle**</span><span class="sxs-lookup"><span data-stu-id="7ce07-156">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7ce07-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-159">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7ce07-159">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-160">Identificador del subproceso.</span><span class="sxs-lookup"><span data-stu-id="7ce07-160">Identifier for the thread.</span></span>

</dd> <dt>

<span data-ttu-id="7ce07-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7ce07-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-162">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7ce07-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-164">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="7ce07-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-165">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="7ce07-165">Date and time the object was installed.</span></span> <span data-ttu-id="7ce07-166">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="7ce07-166">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="7ce07-167">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7ce07-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ce07-168">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="7ce07-168">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-169">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7ce07-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-171">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos")</span><span class="sxs-lookup"><span data-stu-id="7ce07-171">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-172">Tiempo, en modo kernel, en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="7ce07-172">Time, in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="7ce07-173">Si esta información no está disponible, se debe usar un valor de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="7ce07-173">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="7ce07-174">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="7ce07-174">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="7ce07-175">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="7ce07-175">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7ce07-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-178">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7ce07-178">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-179">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="7ce07-179">Label by which the object is known.</span></span> <span data-ttu-id="7ce07-180">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="7ce07-180">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7ce07-181">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7ce07-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ce07-182">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7ce07-182">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7ce07-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-185">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ proceso de CIM**](cim-process.md).**OSCreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7ce07-185">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**OSCreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-186">Ámbito del nombre de la clase de creación del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7ce07-186">Scoping operating system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="7ce07-187">**OSName**</span><span class="sxs-lookup"><span data-stu-id="7ce07-187">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-188">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7ce07-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-190">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ proceso de CIM**](cim-process.md).**OSName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7ce07-190">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**OSName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-191">Ámbito del nombre del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7ce07-191">Scoping operating system's name.</span></span>

</dd> <dt>

<span data-ttu-id="7ce07-192">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="7ce07-192">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-193">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7ce07-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-195">Urgencia para la ejecución de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="7ce07-195">Urgency for execution of a thread.</span></span> <span data-ttu-id="7ce07-196">Un subproceso puede tener una prioridad diferente a la del proceso propietario.</span><span class="sxs-lookup"><span data-stu-id="7ce07-196">A thread can have a different priority than its owning process.</span></span> <span data-ttu-id="7ce07-197">Si esta información no está disponible para un subproceso, se debe usar un valor de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="7ce07-197">If this information is not available for a thread, a value of 0 (zero) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="7ce07-198">**ProcessCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7ce07-198">**ProcessCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7ce07-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-201">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ proceso de CIM**](cim-process.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7ce07-201">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-202">Nombre de la clase de creación del proceso de ámbito.</span><span class="sxs-lookup"><span data-stu-id="7ce07-202">Scoping process's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="7ce07-203">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="7ce07-203">**ProcessHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-204">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7ce07-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-206">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ proceso de CIM**](cim-process.md).**Identificador**"), [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7ce07-206">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**Handle**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-207">Identificador del proceso de ámbito.</span><span class="sxs-lookup"><span data-stu-id="7ce07-207">Scoping process's handle.</span></span>

</dd> <dt>

<span data-ttu-id="7ce07-208">**Estado**</span><span class="sxs-lookup"><span data-stu-id="7ce07-208">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-209">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7ce07-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-211">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="7ce07-211">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-212">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7ce07-212">Current status of the object.</span></span> <span data-ttu-id="7ce07-213">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7ce07-213">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7ce07-214">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7ce07-214">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7ce07-215">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="7ce07-215">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7ce07-216">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="7ce07-216">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7ce07-217">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="7ce07-217">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7ce07-218">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="7ce07-218">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7ce07-219">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="7ce07-219">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7ce07-220">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="7ce07-220">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7ce07-221">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="7ce07-221">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7ce07-222">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="7ce07-222">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7ce07-223">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="7ce07-223">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7ce07-224">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="7ce07-224">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7ce07-225">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="7ce07-225">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7ce07-226">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="7ce07-226">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7ce07-227">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="7ce07-227">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce07-228">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7ce07-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ce07-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce07-230">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos")</span><span class="sxs-lookup"><span data-stu-id="7ce07-230">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="7ce07-231">Tiempo, en modo de usuario, en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="7ce07-231">Time, in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="7ce07-232">Si esta información no está disponible, se debe usar un valor de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="7ce07-232">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="7ce07-233">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="7ce07-233">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ce07-234">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ce07-234">Remarks</span></span>

<span data-ttu-id="7ce07-235">La clase de **\_ subproceso CIM** se deriva de [**\_ LogicalElement CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7ce07-235">The **CIM\_Thread** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="7ce07-236">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="7ce07-236">WMI does not implement this class.</span></span> <span data-ttu-id="7ce07-237">Para las clases WMI derivadas de un **\_ subproceso CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7ce07-237">For WMI classes derived from **CIM\_Thread**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="7ce07-238">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="7ce07-238">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7ce07-239">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="7ce07-239">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ce07-240">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ce07-240">Requirements</span></span>



| <span data-ttu-id="7ce07-241">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ce07-241">Requirement</span></span> | <span data-ttu-id="7ce07-242">Value</span><span class="sxs-lookup"><span data-stu-id="7ce07-242">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ce07-243">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ce07-243">Minimum supported client</span></span><br/> | <span data-ttu-id="7ce07-244">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ce07-244">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7ce07-245">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ce07-245">Minimum supported server</span></span><br/> | <span data-ttu-id="7ce07-246">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ce07-246">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7ce07-247">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7ce07-247">Namespace</span></span><br/>                | <span data-ttu-id="7ce07-248">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7ce07-248">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7ce07-249">MOF</span><span class="sxs-lookup"><span data-stu-id="7ce07-249">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ce07-250"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ce07-250"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ce07-251">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7ce07-251">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ce07-252"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ce07-252"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ce07-253">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ce07-253">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ce07-254">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="7ce07-254">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

