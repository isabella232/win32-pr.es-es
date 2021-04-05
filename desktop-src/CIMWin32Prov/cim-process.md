---
description: La \_ clase de proceso CIM representa una única instancia de un programa en ejecución. Un usuario suele ver un proceso como una aplicación o una tarea.
ms.assetid: 8b00ef6e-5c7f-410c-9e48-1205ea6e5a4c
ms.tgt_platform: multiple
title: CIM_Process (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Process
- CIM_Process.Caption
- CIM_Process.CreationClassName
- CIM_Process.CreationDate
- CIM_Process.CSCreationClassName
- CIM_Process.CSName
- CIM_Process.Description
- CIM_Process.ExecutionState
- CIM_Process.Handle
- CIM_Process.InstallDate
- CIM_Process.KernelModeTime
- CIM_Process.Name
- CIM_Process.OSCreationClassName
- CIM_Process.OSName
- CIM_Process.Priority
- CIM_Process.Status
- CIM_Process.TerminationDate
- CIM_Process.UserModeTime
- CIM_Process.WorkingSetSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 355e29929dc05a701a2beac0919a28aca573ca9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000797"
---
# <a name="cim_process-class"></a><span data-ttu-id="83120-104">\_Clase de proceso CIM</span><span class="sxs-lookup"><span data-stu-id="83120-104">CIM\_Process class</span></span>

<span data-ttu-id="83120-105">La clase de **\_ proceso CIM** representa una única instancia de un programa en ejecución.</span><span class="sxs-lookup"><span data-stu-id="83120-105">The **CIM\_Process** class represents a single instance of a running program.</span></span> <span data-ttu-id="83120-106">Un usuario suele ver un proceso como una aplicación o una tarea.</span><span class="sxs-lookup"><span data-stu-id="83120-106">A user typically sees a process as an application or task.</span></span> <span data-ttu-id="83120-107">Un proceso se define mediante un área de trabajo de recursos de memoria y configuraciones de entorno que se le asignan.</span><span class="sxs-lookup"><span data-stu-id="83120-107">A process is defined by a workspace of memory resources and environmental settings that are allocated to it.</span></span> <span data-ttu-id="83120-108">En un sistema multitarea, el área de trabajo evita la intrusión de recursos por parte de otros procesos.</span><span class="sxs-lookup"><span data-stu-id="83120-108">On a multitasking system, the workspace prevents intrusion of resources by other processes.</span></span> <span data-ttu-id="83120-109">Además, un proceso puede ejecutarse como varios subprocesos, todos los cuales se ejecutan dentro de la misma área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="83120-109">Additionally, a process can execute as multiple threads, all which run within the same workspace.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83120-110">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="83120-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="83120-111">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="83120-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="83120-112">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="83120-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="83120-113">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="83120-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="83120-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83120-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C566-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes (CIM)"), AMENDMENT]
class CIM_Process : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  datetime CreationDate;
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
  string   Status;
  datetime TerminationDate;
  uint64   UserModeTime;
  uint64   WorkingSetSize;
};
```

## <a name="members"></a><span data-ttu-id="83120-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="83120-115">Members</span></span>

<span data-ttu-id="83120-116">La clase de **\_ proceso CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="83120-116">The **CIM\_Process** class has these types of members:</span></span>

-   [<span data-ttu-id="83120-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83120-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83120-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83120-118">Properties</span></span>

<span data-ttu-id="83120-119">La clase de **\_ proceso CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="83120-119">The **CIM\_Process** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83120-120">**Caption**</span><span class="sxs-lookup"><span data-stu-id="83120-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83120-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83120-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-123">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="83120-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="83120-124">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="83120-124">Short textual description of the object.</span></span>

<span data-ttu-id="83120-125">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="83120-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="83120-126">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="83120-126">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83120-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83120-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-129">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="83120-129">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="83120-130">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="83120-130">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="83120-131">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="83120-131">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="83120-132">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="83120-132">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-133">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="83120-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="83120-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-135">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("CreationDate")</span><span class="sxs-lookup"><span data-stu-id="83120-135">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("CreationDate")</span></span>
</dt> </dl>

<span data-ttu-id="83120-136">Hora a la que se inició la ejecución del proceso.</span><span class="sxs-lookup"><span data-stu-id="83120-136">Time that the process began executing.</span></span>

</dd> <dt>

<span data-ttu-id="83120-137">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="83120-137">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83120-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83120-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-140">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Class name ")</span><span class="sxs-lookup"><span data-stu-id="83120-140">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="83120-141">Ámbito del nombre de la clase de creación del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="83120-141">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="83120-142">**CSName**</span><span class="sxs-lookup"><span data-stu-id="83120-142">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83120-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83120-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-145">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="83120-145">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="83120-146">Ámbito del nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="83120-146">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="83120-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="83120-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83120-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83120-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-150">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="83120-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="83120-151">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="83120-151">Textual description of the object.</span></span>

<span data-ttu-id="83120-152">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="83120-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="83120-153">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="83120-153">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-154">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83120-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83120-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-156">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("estado de ejecución")</span><span class="sxs-lookup"><span data-stu-id="83120-156">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Execution State")</span></span>
</dt> </dl>

<span data-ttu-id="83120-157">Condición de funcionamiento actual del proceso.</span><span class="sxs-lookup"><span data-stu-id="83120-157">Current operating condition of the process.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83120-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="83120-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="83120-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="83120-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="83120-160"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Listo** (2)</span><span class="sxs-lookup"><span data-stu-id="83120-160"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="83120-161"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="83120-161"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="83120-162"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Bloqueado** (4)</span><span class="sxs-lookup"><span data-stu-id="83120-162"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="83120-163"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspendido bloqueado** (5)</span><span class="sxs-lookup"><span data-stu-id="83120-163"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspended Blocked** (5)</span></span>


</dt> <dd>

<span data-ttu-id="83120-164">Suspendido bloqueado</span><span class="sxs-lookup"><span data-stu-id="83120-164">Suspended blocked</span></span>

</dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="83120-165"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspendido preparado** (6)</span><span class="sxs-lookup"><span data-stu-id="83120-165"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspended Ready** (6)</span></span>


</dt> <dd>

<span data-ttu-id="83120-166">Suspendido preparado</span><span class="sxs-lookup"><span data-stu-id="83120-166">Suspended ready</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="83120-167"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminada** (7)</span><span class="sxs-lookup"><span data-stu-id="83120-167"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="83120-168"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (8)</span><span class="sxs-lookup"><span data-stu-id="83120-168"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span data-ttu-id="83120-169"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>En **aumento** (9)</span><span class="sxs-lookup"><span data-stu-id="83120-169"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Growing** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="83120-170">**Handle**</span><span class="sxs-lookup"><span data-stu-id="83120-170">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83120-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83120-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-173">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Handle")</span><span class="sxs-lookup"><span data-stu-id="83120-173">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Handle")</span></span>
</dt> </dl>

<span data-ttu-id="83120-174">Identifica el proceso.</span><span class="sxs-lookup"><span data-stu-id="83120-174">Identifies the process.</span></span> <span data-ttu-id="83120-175">Un identificador de proceso es un tipo de identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="83120-175">A process identifier is a kind of process handle.</span></span>

</dd> <dt>

<span data-ttu-id="83120-176">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="83120-176">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-177">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="83120-177">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="83120-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-179">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="83120-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="83120-180">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="83120-180">Date and time the object was installed.</span></span> <span data-ttu-id="83120-181">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="83120-181">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="83120-182">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="83120-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="83120-183">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="83120-183">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-184">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="83120-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83120-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-186">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tiempo de modelo de kernel"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos")</span><span class="sxs-lookup"><span data-stu-id="83120-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kernel Model Time"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="83120-187">Tiempo en modo kernel, en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="83120-187">Time in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="83120-188">Si esta información no está disponible, se debe usar un valor de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="83120-188">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="83120-189">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="83120-189">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="83120-190">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="83120-190">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83120-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83120-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-193">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="83120-193">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="83120-194">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="83120-194">Label by which the object is known.</span></span> <span data-ttu-id="83120-195">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="83120-195">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="83120-196">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="83120-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="83120-197">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="83120-197">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-198">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83120-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83120-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-200">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre de clase del sistema operativo ")</span><span class="sxs-lookup"><span data-stu-id="83120-200">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Operating System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="83120-201">Ámbito del nombre de la clase de creación del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="83120-201">Scoping operating system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="83120-202">**OSName**</span><span class="sxs-lookup"><span data-stu-id="83120-202">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83120-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83120-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-205">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre del sistema operativo ")</span><span class="sxs-lookup"><span data-stu-id="83120-205">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Operating System Name")</span></span>
</dt> </dl>

<span data-ttu-id="83120-206">Ámbito del nombre del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="83120-206">Scoping operating system's name.</span></span>

</dd> <dt>

<span data-ttu-id="83120-207">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="83120-207">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-208">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83120-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83120-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-210">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Priority")</span><span class="sxs-lookup"><span data-stu-id="83120-210">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Priority")</span></span>
</dt> </dl>

<span data-ttu-id="83120-211">Urgencia o importancia para la ejecución de procesos.</span><span class="sxs-lookup"><span data-stu-id="83120-211">Urgency or importance for process execution.</span></span> <span data-ttu-id="83120-212">Si no se define una prioridad para un proceso, se debe utilizar un valor de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="83120-212">If a priority is not defined for a process, a value of 0 (zero) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="83120-213">**Estado**</span><span class="sxs-lookup"><span data-stu-id="83120-213">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-214">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="83120-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83120-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-216">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="83120-216">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="83120-217">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="83120-217">Current status of the object.</span></span>

<span data-ttu-id="83120-218">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="83120-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="83120-219">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="83120-219">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="83120-220">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="83120-220">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="83120-221">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="83120-221">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="83120-222">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="83120-222">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83120-223">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="83120-223">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="83120-224">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="83120-224">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="83120-225">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="83120-225">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="83120-226">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="83120-226">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="83120-227">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="83120-227">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="83120-228">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="83120-228">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="83120-229">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="83120-229">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="83120-230">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="83120-230">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="83120-231">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="83120-231">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="83120-232">**TerminationDate**</span><span class="sxs-lookup"><span data-stu-id="83120-232">**TerminationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-233">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="83120-233">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="83120-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-235">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("fecha de finalización")</span><span class="sxs-lookup"><span data-stu-id="83120-235">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Termination Date")</span></span>
</dt> </dl>

<span data-ttu-id="83120-236">Hora en que el proceso se detuvo o finalizó.</span><span class="sxs-lookup"><span data-stu-id="83120-236">Time that the process was stopped or terminated.</span></span>

</dd> <dt>

<span data-ttu-id="83120-237">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="83120-237">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-238">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="83120-238">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83120-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-240">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tiempo en modo de usuario"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos")</span><span class="sxs-lookup"><span data-stu-id="83120-240">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("User Mode Time"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="83120-241">Tiempo en modo de usuario, en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="83120-241">Time in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="83120-242">Si esta información no está disponible, se debe usar un valor de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="83120-242">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="83120-243">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="83120-243">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="83120-244">**WorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="83120-244">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83120-245">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="83120-245">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83120-246">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83120-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83120-247">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tamaño del espacio de trabajo"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="83120-247">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Working Set Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="83120-248">Cantidad de memoria, en bytes, que un proceso necesita para ejecutarse de forma eficaz para un sistema operativo que usa la administración de memoria basada en páginas.</span><span class="sxs-lookup"><span data-stu-id="83120-248">Amount of memory, in bytes, that a process needs to execute efficiently for an operating system that uses page-based memory management.</span></span> <span data-ttu-id="83120-249">Si el sistema no tiene suficiente memoria (menos que el tamaño del espacio de trabajo), se produce la paginación excesiva.</span><span class="sxs-lookup"><span data-stu-id="83120-249">If the system does not have enough memory (less than the working set size), thrashing occurs.</span></span> <span data-ttu-id="83120-250">Si no se conoce el tamaño del espacio de trabajo, utilice **null** o 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="83120-250">If the size of the working set is not known, use **NULL** or 0 (zero).</span></span> <span data-ttu-id="83120-251">Si se proporcionan datos del espacio de trabajo, puede supervisar la información para comprender los requisitos de memoria variables de un proceso.</span><span class="sxs-lookup"><span data-stu-id="83120-251">If working set data is provided, you can monitor the information to understand the changing memory requirements of a process.</span></span>

<span data-ttu-id="83120-252">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="83120-252">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83120-253">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83120-253">Remarks</span></span>

<span data-ttu-id="83120-254">La clase de **\_ proceso CIM** se deriva [**de \_ LogicalElement CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="83120-254">The **CIM\_Process** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="83120-255">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="83120-255">WMI does not implement this class.</span></span> <span data-ttu-id="83120-256">Para las clases WMI derivadas del **\_ proceso CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="83120-256">For WMI classes derived from **CIM\_Process**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="83120-257">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="83120-257">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="83120-258">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="83120-258">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="83120-259">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83120-259">Requirements</span></span>



| <span data-ttu-id="83120-260">Requisito</span><span class="sxs-lookup"><span data-stu-id="83120-260">Requirement</span></span> | <span data-ttu-id="83120-261">Value</span><span class="sxs-lookup"><span data-stu-id="83120-261">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83120-262">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83120-262">Minimum supported client</span></span><br/> | <span data-ttu-id="83120-263">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83120-263">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="83120-264">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83120-264">Minimum supported server</span></span><br/> | <span data-ttu-id="83120-265">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83120-265">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83120-266">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="83120-266">Namespace</span></span><br/>                | <span data-ttu-id="83120-267">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="83120-267">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="83120-268">MOF</span><span class="sxs-lookup"><span data-stu-id="83120-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83120-269"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83120-269"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="83120-270">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="83120-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83120-271"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83120-271"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83120-272">Vea también</span><span class="sxs-lookup"><span data-stu-id="83120-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83120-273">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="83120-273">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

