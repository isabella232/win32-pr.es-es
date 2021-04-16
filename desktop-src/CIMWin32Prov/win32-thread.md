---
description: El \_ subproceso de Win32&\# 8194; La clase WMI representa un subproceso de ejecución.
ms.assetid: a284616c-1977-441a-9173-dff4f56b2d39
ms.tgt_platform: multiple
title: Win32_Thread (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Thread
- Win32_Thread.Caption
- Win32_Thread.CreationClassName
- Win32_Thread.CSCreationClassName
- Win32_Thread.CSName
- Win32_Thread.Description
- Win32_Thread.ElapsedTime
- Win32_Thread.ExecutionState
- Win32_Thread.Handle
- Win32_Thread.InstallDate
- Win32_Thread.KernelModeTime
- Win32_Thread.Name
- Win32_Thread.OSCreationClassName
- Win32_Thread.OSName
- Win32_Thread.Priority
- Win32_Thread.PriorityBase
- Win32_Thread.ProcessCreationClassName
- Win32_Thread.ProcessHandle
- Win32_Thread.StartAddress
- Win32_Thread.Status
- Win32_Thread.ThreadState
- Win32_Thread.ThreadWaitReason
- Win32_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6e9f6a8c821aa327e8b810b634c85bb06459910f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652347"
---
# <a name="win32_thread-class"></a><span data-ttu-id="c869f-103">\_Clase de subproceso Win32</span><span class="sxs-lookup"><span data-stu-id="c869f-103">Win32\_Thread class</span></span>

<span data-ttu-id="c869f-104">La  [clase WMI](../wmisdk/retrieving-a-class.md) de **\_ subproceso Win32** representa un subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="c869f-104">The **Win32\_Thread** [WMI class](../wmisdk/retrieving-a-class.md) represents a thread of execution.</span></span> <span data-ttu-id="c869f-105">Mientras que un proceso debe tener un subproceso de ejecución, el proceso puede crear otros subprocesos para ejecutar tareas en paralelo.</span><span class="sxs-lookup"><span data-stu-id="c869f-105">While a process must have one thread of execution, the process can create other threads to execute tasks in parallel.</span></span> <span data-ttu-id="c869f-106">Los subprocesos comparten el entorno de proceso, por lo que varios subprocesos del mismo proceso usan menos memoria que el mismo número de procesos.</span><span class="sxs-lookup"><span data-stu-id="c869f-106">Threads share the process environment, thus multiple threads under the same process use less memory than the same number of processes.</span></span>

<span data-ttu-id="c869f-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c869f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c869f-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c869f-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c869f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c869f-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4DD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Thread : CIM_Thread
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   ElapsedTime;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  uint32   PriorityBase;
  string   ProcessCreationClassName;
  string   ProcessHandle;
  uint32   StartAddress;
  string   Status;
  uint32   ThreadState;
  uint32   ThreadWaitReason;
  uint64   UserModeTime;
};
```

## <a name="members"></a><span data-ttu-id="c869f-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="c869f-110">Members</span></span>

<span data-ttu-id="c869f-111">La clase de **\_ subproceso de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c869f-111">The **Win32\_Thread** class has these types of members:</span></span>

-   [<span data-ttu-id="c869f-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c869f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c869f-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c869f-113">Properties</span></span>

<span data-ttu-id="c869f-114">La clase de **\_ subproceso de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c869f-114">The **Win32\_Thread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c869f-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c869f-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c869f-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-118">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c869f-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c869f-119">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c869f-119">Short description of the object.</span></span>

<span data-ttu-id="c869f-120">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c869f-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c869f-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c869f-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c869f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-124">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="c869f-124">Qualifiers: [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c869f-125">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="c869f-125">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="c869f-126">Cuando se usa con las otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="c869f-126">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c869f-127">Esta propiedad se hereda del [**\_ subproceso CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="c869f-127">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="c869f-128">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c869f-128">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c869f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-131">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ proceso de CIM**](cim-process.md).**CSCreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="c869f-131">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CSCreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c869f-132">Nombre de la clase de creación del sistema de ámbito del equipo.</span><span class="sxs-lookup"><span data-stu-id="c869f-132">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="c869f-133">Esta propiedad se hereda del [**\_ subproceso CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="c869f-133">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="c869f-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="c869f-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c869f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-137">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ proceso de CIM**](cim-process.md).**CSName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="c869f-137">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CSName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c869f-138">Nombre del sistema de ámbito del equipo.</span><span class="sxs-lookup"><span data-stu-id="c869f-138">Name of the scoping computer system.</span></span>

<span data-ttu-id="c869f-139">Esta propiedad se hereda del [**\_ subproceso CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="c869f-139">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="c869f-140">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c869f-140">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c869f-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-143">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="c869f-143">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c869f-144">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c869f-144">Description of the object.</span></span>

<span data-ttu-id="c869f-145">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c869f-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c869f-146">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="c869f-146">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-147">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c869f-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-149">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| performance Data Structures \| [**Perf \_ Object \_ Type**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PerfTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("Milliseconds")</span><span class="sxs-lookup"><span data-stu-id="c869f-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PerfTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="c869f-150">Tiempo de ejecución total, en milisegundos, dado a este subproceso desde su creación.</span><span class="sxs-lookup"><span data-stu-id="c869f-150">Total execution time, in milliseconds, given to this thread since its creation.</span></span>

<span data-ttu-id="c869f-151">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="c869f-151">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="c869f-152">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="c869f-152">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-153">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c869f-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c869f-155">Condición de funcionamiento actual del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c869f-155">Current operating condition of the thread.</span></span>

<span data-ttu-id="c869f-156">Esta propiedad se hereda del [**\_ subproceso CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="c869f-156">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c869f-157">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="c869f-157">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c869f-158">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="c869f-158">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="c869f-159">**Listo** (2)</span><span class="sxs-lookup"><span data-stu-id="c869f-159">**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="c869f-160">En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="c869f-160">**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="c869f-161">**Bloqueado** (4)</span><span class="sxs-lookup"><span data-stu-id="c869f-161">**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="c869f-162">**Suspendido bloqueado** (5)</span><span class="sxs-lookup"><span data-stu-id="c869f-162">**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="c869f-163">**Suspendido preparado** (6)</span><span class="sxs-lookup"><span data-stu-id="c869f-163">**Suspended Ready** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c869f-164">**Handle**</span><span class="sxs-lookup"><span data-stu-id="c869f-164">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c869f-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-167">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("Handle"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Tool Help Structures \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32ThreadID")</span><span class="sxs-lookup"><span data-stu-id="c869f-167">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Handle"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|th32ThreadID")</span></span>
</dt> </dl>

<span data-ttu-id="c869f-168">Identificador de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="c869f-168">Handle to a thread.</span></span> <span data-ttu-id="c869f-169">De forma predeterminada, el identificador tiene derechos de acceso completo.</span><span class="sxs-lookup"><span data-stu-id="c869f-169">The handle has full access rights by default.</span></span> <span data-ttu-id="c869f-170">Con el acceso de seguridad correcto, el identificador se puede utilizar en cualquier función que acepte un identificador de subproceso.</span><span class="sxs-lookup"><span data-stu-id="c869f-170">With the correct security access, the handle can be used in any function that accepts a thread handle.</span></span> <span data-ttu-id="c869f-171">Dependiendo de la marca de herencia especificada al crearse, este identificador puede ser heredado por procesos secundarios.</span><span class="sxs-lookup"><span data-stu-id="c869f-171">Depending on the inheritance flag specified when it is created, this handle can be inherited by child processes.</span></span>

</dd> <dt>

<span data-ttu-id="c869f-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c869f-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-173">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c869f-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-175">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="c869f-175">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c869f-176">Objeto instalado.</span><span class="sxs-lookup"><span data-stu-id="c869f-176">Object was installed.</span></span> <span data-ttu-id="c869f-177">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="c869f-177">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c869f-178">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c869f-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c869f-179">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="c869f-179">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-180">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c869f-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-182">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| performance Data Structures \| [**Perf \_ Object \_ TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PrivilegedTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanosegundos")</span><span class="sxs-lookup"><span data-stu-id="c869f-182">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PrivilegedTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="c869f-183">Tiempo en modo kernel, en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="c869f-183">Time in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="c869f-184">Si esta información no está disponible, se debe usar un valor de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="c869f-184">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="c869f-185">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="c869f-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="c869f-186">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c869f-186">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c869f-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-189">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c869f-189">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c869f-190">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="c869f-190">Label by which the object is known.</span></span> <span data-ttu-id="c869f-191">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="c869f-191">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="c869f-192">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c869f-192">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c869f-193">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c869f-193">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c869f-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-196">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ proceso de CIM**](cim-process.md).**OSCreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="c869f-196">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**OSCreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c869f-197">Nombre de la clase de creación del sistema operativo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="c869f-197">Creation class name of the scoping operating system.</span></span>

<span data-ttu-id="c869f-198">Esta propiedad se hereda del [**\_ subproceso CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="c869f-198">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="c869f-199">**OSName**</span><span class="sxs-lookup"><span data-stu-id="c869f-199">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-200">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c869f-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-202">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ proceso de CIM**](cim-process.md).**OSName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="c869f-202">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**OSName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c869f-203">Nombre del sistema operativo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="c869f-203">Name of the scoping operating system.</span></span>

<span data-ttu-id="c869f-204">Esta propiedad se hereda del [**\_ subproceso CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="c869f-204">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="c869f-205">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="c869f-205">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-206">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c869f-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-208">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Tool Help Structures \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| tpDeltaPri")</span><span class="sxs-lookup"><span data-stu-id="c869f-208">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|tpDeltaPri")</span></span>
</dt> </dl>

<span data-ttu-id="c869f-209">Prioridad dinámica del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c869f-209">Dynamic priority of the thread.</span></span> <span data-ttu-id="c869f-210">Cada subproceso tiene una prioridad dinámica que el programador usa para determinar qué subproceso se debe ejecutar.</span><span class="sxs-lookup"><span data-stu-id="c869f-210">Each thread has a dynamic priority that the scheduler uses to determine which thread to execute.</span></span> <span data-ttu-id="c869f-211">Inicialmente, la prioridad dinámica de un subproceso es igual que su prioridad base.</span><span class="sxs-lookup"><span data-stu-id="c869f-211">Initially, a thread's dynamic priority is the same as its base priority.</span></span> <span data-ttu-id="c869f-212">El sistema puede aumentar y disminuir la prioridad dinámica para garantizar que responde (lo que garantiza que ningún subproceso se queda sin tiempo de procesador).</span><span class="sxs-lookup"><span data-stu-id="c869f-212">The system can raise and lower the dynamic priority, to ensure that it is responsive (guaranteeing that no threads are starved for processor time).</span></span> <span data-ttu-id="c869f-213">El sistema no aumenta la prioridad de los subprocesos con un nivel de prioridad base entre 16 y 31.</span><span class="sxs-lookup"><span data-stu-id="c869f-213">The system does not boost the priority of threads with a base priority level between 16 and 31.</span></span> <span data-ttu-id="c869f-214">Solo los subprocesos con una prioridad base entre 0 y 15 reciben aumentos de prioridad dinámica.</span><span class="sxs-lookup"><span data-stu-id="c869f-214">Only threads with a base priority between 0 and 15 receive dynamic priority boosts.</span></span> <span data-ttu-id="c869f-215">Los números más altos indican prioridades más altas.</span><span class="sxs-lookup"><span data-stu-id="c869f-215">Higher numbers indicate higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="c869f-216">**PriorityBase**</span><span class="sxs-lookup"><span data-stu-id="c869f-216">**PriorityBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-217">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c869f-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-219">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| performance Data Structures \| [**Perf \_ Object \_ Type**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PerfPriorityBase")</span><span class="sxs-lookup"><span data-stu-id="c869f-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PerfPriorityBase")</span></span>
</dt> </dl>

<span data-ttu-id="c869f-220">Prioridad base actual de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="c869f-220">Current base priority of a thread.</span></span> <span data-ttu-id="c869f-221">El sistema operativo puede aumentar la prioridad dinámica del subproceso por encima de la prioridad base si el subproceso está controlando los datos proporcionados por el usuario o reducirlo hacia la prioridad base si el subproceso se convierte en un enlace de proceso.</span><span class="sxs-lookup"><span data-stu-id="c869f-221">The operating system may raise the thread's dynamic priority above the base priority if the thread is handling user input, or lower it toward the base priority if the thread becomes compute-bound.</span></span> <span data-ttu-id="c869f-222">La propiedad **PriorityBase** puede tener un valor entre 0 y 31.</span><span class="sxs-lookup"><span data-stu-id="c869f-222">The **PriorityBase** property can have a value between 0 and 31.</span></span>

</dd> <dt>

<span data-ttu-id="c869f-223">**ProcessCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c869f-223">**ProcessCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-224">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c869f-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-226">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ proceso de CIM**](cim-process.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="c869f-226">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c869f-227">Valor de la propiedad de proceso de ámbito de **CreationClassName** .</span><span class="sxs-lookup"><span data-stu-id="c869f-227">Value of the scoping process **CreationClassName** property.</span></span>

<span data-ttu-id="c869f-228">Esta propiedad se hereda del [**\_ subproceso CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="c869f-228">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="c869f-229">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="c869f-229">**ProcessHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-230">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c869f-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-232">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**invalidar**](../wmisdk/standard-qualifiers.md) ("ProcessHandle"), [**propagado**](../wmisdk/standard-qualifiers.md) ("[**\_ proceso de CIM**](cim-process.md).**Handle**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" inesperados win32api \| Tool Help Structures \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32OwnerProcessID ")</span><span class="sxs-lookup"><span data-stu-id="c869f-232">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("ProcessHandle"), [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**Handle**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|th32OwnerProcessID")</span></span>
</dt> </dl>

<span data-ttu-id="c869f-233">Proceso que creó el subproceso.</span><span class="sxs-lookup"><span data-stu-id="c869f-233">Process that created the thread.</span></span> <span data-ttu-id="c869f-234">Los elementos de la interfaz de programación de aplicaciones (API) de Windows pueden usar el contenido de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c869f-234">The contents of this property can be used by Windows application programming interface (API) elements.</span></span>

</dd> <dt>

<span data-ttu-id="c869f-235">**StartAddress**</span><span class="sxs-lookup"><span data-stu-id="c869f-235">**StartAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-236">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c869f-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-238">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| objeto inesperados win32api Thread \| LPTHREAD \_ Start \_ rutina \| lpStartAddress")</span><span class="sxs-lookup"><span data-stu-id="c869f-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIn32API\|Thread Object\|LPTHREAD\_START\_ROUTINE\|lpStartAddress")</span></span>
</dt> </dl>

<span data-ttu-id="c869f-239">Dirección inicial del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c869f-239">Starting address of the thread.</span></span> <span data-ttu-id="c869f-240">Dado que cualquier aplicación con el acceso adecuado al subproceso puede cambiar el contexto del subproceso, este valor solo puede ser una aproximación de la dirección de inicio del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c869f-240">Because any application with appropriate access to the thread can change the thread's context, this value may only be an approximation of the thread's starting address.</span></span>

</dd> <dt>

<span data-ttu-id="c869f-241">**Estado**</span><span class="sxs-lookup"><span data-stu-id="c869f-241">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-242">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c869f-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-244">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="c869f-244">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c869f-245">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c869f-245">Current status of the object.</span></span> <span data-ttu-id="c869f-246">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="c869f-246">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c869f-247">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="c869f-247">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c869f-248">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="c869f-248">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c869f-249">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="c869f-249">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c869f-250">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="c869f-250">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c869f-251">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c869f-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c869f-252">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c869f-252">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c869f-253">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="c869f-253">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c869f-254">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="c869f-254">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c869f-255">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c869f-255">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c869f-256">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="c869f-256">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c869f-257">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="c869f-257">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c869f-258">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="c869f-258">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c869f-259">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="c869f-259">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c869f-260">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="c869f-260">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c869f-261">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="c869f-261">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c869f-262">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c869f-262">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c869f-263">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="c869f-263">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c869f-264">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="c869f-264">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c869f-265">**ThreadState**</span><span class="sxs-lookup"><span data-stu-id="c869f-265">**ThreadState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-266">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c869f-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-267">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-268">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Thread State")</span><span class="sxs-lookup"><span data-stu-id="c869f-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Thread State")</span></span>
</dt> </dl>

<span data-ttu-id="c869f-269">Estado de ejecución actual del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c869f-269">Current execution state for the thread.</span></span>

<dt>

<span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>

<span data-ttu-id="c869f-270"><span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**Inicializado** (0)</span><span class="sxs-lookup"><span data-stu-id="c869f-270"><span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**Initialized** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c869f-271">Initialized: el microkernel lo reconoce.</span><span class="sxs-lookup"><span data-stu-id="c869f-271">Initialized — It is recognized by the microkernel.</span></span>

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="c869f-272"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Listo** (1)</span><span class="sxs-lookup"><span data-stu-id="c869f-272"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c869f-273">Listo: está preparado para ejecutarse en el siguiente procesador disponible.</span><span class="sxs-lookup"><span data-stu-id="c869f-273">Ready — It is prepared to run on the next available processor.</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="c869f-274"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (2)</span><span class="sxs-lookup"><span data-stu-id="c869f-274"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c869f-275">En ejecución: se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="c869f-275">Running — It is executing.</span></span>

</dd> <dt>

<span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>

<span data-ttu-id="c869f-276"><span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>En **espera** (3)</span><span class="sxs-lookup"><span data-stu-id="c869f-276"><span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>**Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c869f-277">Standby: está a punto de ejecutarse, solo un subproceso puede estar en este estado a la vez.</span><span class="sxs-lookup"><span data-stu-id="c869f-277">Standby — It is about to run, only one thread may be in this state at a time.</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="c869f-278"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminada** (4)</span><span class="sxs-lookup"><span data-stu-id="c869f-278"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c869f-279">Terminada: ha terminado de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="c869f-279">Terminated — It is finished executing.</span></span>

</dd> <dt>

<span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>

<span data-ttu-id="c869f-280"><span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>En **espera** (5)</span><span class="sxs-lookup"><span data-stu-id="c869f-280"><span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>**Waiting** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c869f-281">Esperando: no está listo para el procesador, cuando esté listo, se volverá a programar.</span><span class="sxs-lookup"><span data-stu-id="c869f-281">Waiting — It is not ready for the processor, when ready, it will be rescheduled.</span></span>

</dd> <dt>

<span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>

<span data-ttu-id="c869f-282"><span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**Transición** (6)</span><span class="sxs-lookup"><span data-stu-id="c869f-282"><span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**Transition** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c869f-283">Transición: el subproceso está esperando recursos distintos del procesador,</span><span class="sxs-lookup"><span data-stu-id="c869f-283">Transition — The thread is waiting for resources other than the processor,</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c869f-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (7)</span><span class="sxs-lookup"><span data-stu-id="c869f-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c869f-285">Desconocido: se desconoce el estado del subproceso.</span><span class="sxs-lookup"><span data-stu-id="c869f-285">Unknown — The thread state is unknown.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c869f-286">**ThreadWaitReason**</span><span class="sxs-lookup"><span data-stu-id="c869f-286">**ThreadWaitReason**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-287">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c869f-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-289">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| razón de espera del subproceso de inesperados win32api")</span><span class="sxs-lookup"><span data-stu-id="c869f-289">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Thread Wait Reason")</span></span>
</dt> </dl>

<span data-ttu-id="c869f-290">Motivo por el que el subproceso está esperando.</span><span class="sxs-lookup"><span data-stu-id="c869f-290">Reason why the thread is waiting.</span></span> <span data-ttu-id="c869f-291">Este valor solo es válido si el miembro **ThreadState** está establecido en Transition (6).</span><span class="sxs-lookup"><span data-stu-id="c869f-291">This value is only valid if the **ThreadState** member is set to Transition (6).</span></span> <span data-ttu-id="c869f-292">Los pares de eventos permiten la comunicación con subsistemas protegidos.</span><span class="sxs-lookup"><span data-stu-id="c869f-292">Event pairs allow communication with protected subsystems.</span></span>

<dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="c869f-293"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Ejecutivo** (0)</span><span class="sxs-lookup"><span data-stu-id="c869f-293"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="c869f-294"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (1)</span><span class="sxs-lookup"><span data-stu-id="c869f-294"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c869f-295">FreePage</span><span class="sxs-lookup"><span data-stu-id="c869f-295">FreePage</span></span>

</dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="c869f-296"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Buscapersonas** (2)</span><span class="sxs-lookup"><span data-stu-id="c869f-296"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span data-ttu-id="c869f-297"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (3)</span><span class="sxs-lookup"><span data-stu-id="c869f-297"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span data-ttu-id="c869f-298"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (4)</span><span class="sxs-lookup"><span data-stu-id="c869f-298"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="c869f-299"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (5)</span><span class="sxs-lookup"><span data-stu-id="c869f-299"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="c869f-300"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Buscapersonas** (6)</span><span class="sxs-lookup"><span data-stu-id="c869f-300"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="c869f-301"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Ejecutivo** (7)</span><span class="sxs-lookup"><span data-stu-id="c869f-301"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="c869f-302"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (8)</span><span class="sxs-lookup"><span data-stu-id="c869f-302"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="c869f-303"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Buscapersonas** (9)</span><span class="sxs-lookup"><span data-stu-id="c869f-303"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span data-ttu-id="c869f-304"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (10)</span><span class="sxs-lookup"><span data-stu-id="c869f-304"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span data-ttu-id="c869f-305"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (11)</span><span class="sxs-lookup"><span data-stu-id="c869f-305"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="c869f-306"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (12)</span><span class="sxs-lookup"><span data-stu-id="c869f-306"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="c869f-307"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Buscapersonas** (13)</span><span class="sxs-lookup"><span data-stu-id="c869f-307"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>

<span data-ttu-id="c869f-308"><span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**EventPairHigh** (14)</span><span class="sxs-lookup"><span data-stu-id="c869f-308"><span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**EventPairHigh** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>

<span data-ttu-id="c869f-309"><span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**EventPairLow** (15)</span><span class="sxs-lookup"><span data-stu-id="c869f-309"><span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**EventPairLow** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>

<span data-ttu-id="c869f-310"><span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**LPCReceive** (16)</span><span class="sxs-lookup"><span data-stu-id="c869f-310"><span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**LPCReceive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>

<span data-ttu-id="c869f-311"><span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**LPCReply** (17)</span><span class="sxs-lookup"><span data-stu-id="c869f-311"><span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**LPCReply** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>

<span data-ttu-id="c869f-312"><span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**VirtualMemory** (18)</span><span class="sxs-lookup"><span data-stu-id="c869f-312"><span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**VirtualMemory** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>

<span data-ttu-id="c869f-313"><span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**Pageout.** (19)</span><span class="sxs-lookup"><span data-stu-id="c869f-313"><span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**PageOut** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c869f-314"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (20)</span><span class="sxs-lookup"><span data-stu-id="c869f-314"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (20)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c869f-315">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="c869f-315">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c869f-316">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c869f-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c869f-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c869f-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c869f-318">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| performance Data Structures \| [**Perf \_ Object \_ TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| UserTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanosegundos")</span><span class="sxs-lookup"><span data-stu-id="c869f-318">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|UserTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="c869f-319">Tiempo en modo de usuario, en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="c869f-319">Time in user mode, in 100 nanoseconds units.</span></span> <span data-ttu-id="c869f-320">Si esta información no está disponible, se debe usar un valor de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="c869f-320">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="c869f-321">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="c869f-321">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c869f-322">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c869f-322">Remarks</span></span>

<span data-ttu-id="c869f-323">La clase de **\_ subproceso de Win32** se deriva del [**\_ subproceso CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="c869f-323">The **Win32\_Thread** class is derived from [**CIM\_Thread**](cim-thread.md).</span></span>

<span data-ttu-id="c869f-324">**Información general**</span><span class="sxs-lookup"><span data-stu-id="c869f-324">**Overview**</span></span>

<span data-ttu-id="c869f-325">En el caso de la supervisión diaria rutinaria, normalmente hay poca razón para tener una lista detallada de subprocesos y sus propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="c869f-325">For routine day-to-day monitoring, there is usually little reason to have a detailed list of threads and their associated properties.</span></span> <span data-ttu-id="c869f-326">Los equipos crean y eliminan miles de subprocesos durante el transcurso del día y algunas de estas creaciones o eliminaciones son significativas para cualquier persona, pero el desarrollador que escribió el software.</span><span class="sxs-lookup"><span data-stu-id="c869f-326">Computers create and delete thousands of threads during the course of a day, and few of these creations or deletions are meaningful to anyone but the developer who wrote the software.</span></span>

<span data-ttu-id="c869f-327">Sin embargo, cuando se están solucionando problemas con una aplicación, el seguimiento de los subprocesos individuales de un proceso permite identificar cuándo se crean los subprocesos y cuándo (o si) se destruyen.</span><span class="sxs-lookup"><span data-stu-id="c869f-327">However, when you are troubleshooting problems with an application, tracking the individual threads for a process allows you to identify when threads are created and when (or if) they are destroyed.</span></span> <span data-ttu-id="c869f-328">Dado que los subprocesos que se crean pero no se destruyen producen fugas de memoria, el seguimiento de subprocesos individuales puede ser información útil para los técnicos de soporte.</span><span class="sxs-lookup"><span data-stu-id="c869f-328">Because threads that are created but not destroyed cause memory leaks, tracking individual threads can be useful information for support technicians.</span></span> <span data-ttu-id="c869f-329">Del mismo modo, identificar las prioridades de subprocesos puede ayudar a identificar los subprocesos que, al ejecutarse con una prioridad anómalamente alta, son los ciclos de CPU que necesitan otros subprocesos y otros procesos.</span><span class="sxs-lookup"><span data-stu-id="c869f-329">Likewise, identifying thread priorities can help pinpoint threads that, by running at an abnormally high priority, are preempting CPU cycles needed by other threads and other processes.</span></span>

<span data-ttu-id="c869f-330">**Usar el \_ subproceso Win32**</span><span class="sxs-lookup"><span data-stu-id="c869f-330">**Using Win32\_Thread**</span></span>

<span data-ttu-id="c869f-331">Como se ha implícito en el bloque de sintaxis anterior, la clase de **\_ subproceso de Win32** no informa del nombre del proceso en el que se ejecuta cada subproceso.</span><span class="sxs-lookup"><span data-stu-id="c869f-331">As implied in the preceding syntax block, the **Win32\_Thread** class does not report the name of the process under which each thread runs.</span></span> <span data-ttu-id="c869f-332">En su lugar, notifica el identificador del proceso en el que se ejecuta el subproceso.</span><span class="sxs-lookup"><span data-stu-id="c869f-332">Instead, it reports the ID of the process under which the thread runs.</span></span> <span data-ttu-id="c869f-333">Para devolver el nombre de un proceso y una lista de todos los subprocesos, el script debe:</span><span class="sxs-lookup"><span data-stu-id="c869f-333">To return the name of a process and a list of all its threads, your script must:</span></span>

1.  <span data-ttu-id="c869f-334">Conéctese a la clase de [**\_ proceso de Win32**](win32-process.md) y devuelva la lista de procesos y sus identificadores de proceso.</span><span class="sxs-lookup"><span data-stu-id="c869f-334">Connect to the [**Win32\_Process**](win32-process.md) class and return the list of processes and their process IDs.</span></span>
2.  <span data-ttu-id="c869f-335">Almacene temporalmente esta información en un objeto de matriz o de diccionario.</span><span class="sxs-lookup"><span data-stu-id="c869f-335">Temporarily store this information in an array or Dictionary object.</span></span>
3.  <span data-ttu-id="c869f-336">Para cada ID. de proceso, devuelve la lista de subprocesos para ese proceso y, a continuación, muestra el nombre del proceso y la lista de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c869f-336">For each process ID, return the list of threads for that process, and then display the process name and the list of threads.</span></span>

## <a name="examples"></a><span data-ttu-id="c869f-337">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c869f-337">Examples</span></span>

<span data-ttu-id="c869f-338">En el siguiente ejemplo de VBScript se supervisan los subprocesos que se ejecutan en un equipo.</span><span class="sxs-lookup"><span data-stu-id="c869f-338">The following VBScript sample monitors the threads running on a computer.</span></span>


```VB
Set objDictionary = CreateObject("Scripting.Dictionary")
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcesses
 objDictionary.Add objProcess.ProcessID, objProcess.Name
Next
Set colThreads = objWMIService.ExecQuery("SELECT * FROM Win32_Thread")
For Each objThread in colThreads
 intProcessID = CInt(objThread.ProcessHandle)
 strProcessName = objDictionary.Item(intProcessID)
 Wscript.Echo strProcessName & VbTab & objThread.ProcessHandle & _
              VbTab & objThread.Handle & VbTab & objThread.ThreadState
Next
```



## <a name="requirements"></a><span data-ttu-id="c869f-339">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c869f-339">Requirements</span></span>



| <span data-ttu-id="c869f-340">Requisito</span><span class="sxs-lookup"><span data-stu-id="c869f-340">Requirement</span></span> | <span data-ttu-id="c869f-341">Value</span><span class="sxs-lookup"><span data-stu-id="c869f-341">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c869f-342">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c869f-342">Minimum supported client</span></span><br/> | <span data-ttu-id="c869f-343">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c869f-343">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c869f-344">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c869f-344">Minimum supported server</span></span><br/> | <span data-ttu-id="c869f-345">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c869f-345">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c869f-346">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c869f-346">Namespace</span></span><br/>                | <span data-ttu-id="c869f-347">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c869f-347">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c869f-348">MOF</span><span class="sxs-lookup"><span data-stu-id="c869f-348">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c869f-349"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c869f-349"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c869f-350">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c869f-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c869f-351"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c869f-351"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c869f-352">Vea también</span><span class="sxs-lookup"><span data-stu-id="c869f-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c869f-353">**Subproceso CIM \_**</span><span class="sxs-lookup"><span data-stu-id="c869f-353">**CIM\_Thread**</span></span>](cim-thread.md)
</dt> <dt>

[<span data-ttu-id="c869f-354">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c869f-354">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
