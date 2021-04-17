---
Description: El proceso de Win32 \_&\# 32; La clase WMI representa un proceso en un sistema operativo.
ms.assetid: 51206aca-4784-4d18-95ca-bc0a45691f78
ms.tgt_platform: multiple
title: Clase Win32_Process
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process
- Win32_Process.CreationClassName
- Win32_Process.Caption
- Win32_Process.CommandLine
- Win32_Process.CreationDate
- Win32_Process.CSCreationClassName
- Win32_Process.CSName
- Win32_Process.Description
- Win32_Process.ExecutablePath
- Win32_Process.ExecutionState
- Win32_Process.Handle
- Win32_Process.HandleCount
- Win32_Process.InstallDate
- Win32_Process.KernelModeTime
- Win32_Process.MaximumWorkingSetSize
- Win32_Process.MinimumWorkingSetSize
- Win32_Process.Name
- Win32_Process.OSCreationClassName
- Win32_Process.OSName
- Win32_Process.OtherOperationCount
- Win32_Process.OtherTransferCount
- Win32_Process.PageFaults
- Win32_Process.PageFileUsage
- Win32_Process.ParentProcessId
- Win32_Process.PeakPageFileUsage
- Win32_Process.PeakVirtualSize
- Win32_Process.PeakWorkingSetSize
- Win32_Process.Priority
- Win32_Process.PrivatePageCount
- Win32_Process.ProcessId
- Win32_Process.QuotaNonPagedPoolUsage
- Win32_Process.QuotaPagedPoolUsage
- Win32_Process.QuotaPeakNonPagedPoolUsage
- Win32_Process.QuotaPeakPagedPoolUsage
- Win32_Process.ReadOperationCount
- Win32_Process.ReadTransferCount
- Win32_Process.SessionId
- Win32_Process.Status
- Win32_Process.TerminationDate
- Win32_Process.ThreadCount
- Win32_Process.UserModeTime
- Win32_Process.VirtualSize
- Win32_Process.WindowsVersion
- Win32_Process.WorkingSetSize
- Win32_Process.WriteOperationCount
- Win32_Process.WriteTransferCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb8d1d37bd5d4db59942aaab7170119283c5cc7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660479"
---
# <a name="win32_process-class"></a><span data-ttu-id="60c81-103">\_Clase de proceso Win32</span><span class="sxs-lookup"><span data-stu-id="60c81-103">Win32\_Process class</span></span>

<span data-ttu-id="60c81-104">La [clase WMI](../wmisdk/retrieving-a-class.md) de **\_ proceso de Win32** representa un proceso en un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="60c81-104">The **Win32\_Process** [WMI class](../wmisdk/retrieving-a-class.md) represents a process on an operating system.</span></span>

<span data-ttu-id="60c81-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="60c81-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

> [!NOTE]
> <span data-ttu-id="60c81-106">Para obtener una explicación general sobre los procesos y subprocesos de Windows, vea el tema [procesos y subprocesos](/ProcThread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-106">For a general discussion on Processes and Threads within Windows, please see the topic [Processes and Threads](/ProcThread/processes-and-threads.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="60c81-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60c81-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), UUID("{8502C4DC-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes"), AMENDMENT]
class Win32_Process : CIM_Process
{
  string   CreationClassName;
  string   Caption;
  string   CommandLine;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   ExecutablePath;
  uint16   ExecutionState;
  string   Handle;
  uint32   HandleCount;
  datetime InstallDate;
  uint64   KernelModeTime;
  uint32   MaximumWorkingSetSize;
  uint32   MinimumWorkingSetSize;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint64   OtherOperationCount;
  uint64   OtherTransferCount;
  uint32   PageFaults;
  uint32   PageFileUsage;
  uint32   ParentProcessId;
  uint32   PeakPageFileUsage;
  uint64   PeakVirtualSize;
  uint32   PeakWorkingSetSize;
  uint32   Priority = NULL;
  uint64   PrivatePageCount;
  uint32   ProcessId;
  uint32   QuotaNonPagedPoolUsage;
  uint32   QuotaPagedPoolUsage;
  uint32   QuotaPeakNonPagedPoolUsage;
  uint32   QuotaPeakPagedPoolUsage;
  uint64   ReadOperationCount;
  uint64   ReadTransferCount;
  uint32   SessionId;
  string   Status;
  datetime TerminationDate;
  uint32   ThreadCount;
  uint64   UserModeTime;
  uint64   VirtualSize;
  string   WindowsVersion;
  uint64   WorkingSetSize;
  uint64   WriteOperationCount;
  uint64   WriteTransferCount;
};
```

## <a name="members"></a><span data-ttu-id="60c81-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="60c81-108">Members</span></span>

<span data-ttu-id="60c81-109">La clase de **\_ proceso de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="60c81-109">The **Win32\_Process** class has these types of members:</span></span>

-   [<span data-ttu-id="60c81-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="60c81-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="60c81-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60c81-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="60c81-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="60c81-112">Methods</span></span>

<span data-ttu-id="60c81-113">La clase de **\_ proceso de Win32** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="60c81-113">The **Win32\_Process** class has these methods.</span></span>



| <span data-ttu-id="60c81-114">Método</span><span class="sxs-lookup"><span data-stu-id="60c81-114">Method</span></span>                                                                   | <span data-ttu-id="60c81-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="60c81-115">Description</span></span>                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60c81-116">**AttachDebugger**</span><span class="sxs-lookup"><span data-stu-id="60c81-116">**AttachDebugger**</span></span>](attachdebugger-method-in-class-win32-process.md)   | <span data-ttu-id="60c81-117">Inicia el depurador registrado actualmente para un proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-117">Launches the currently registered debugger for a process.</span></span><br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="60c81-118">**A**</span><span class="sxs-lookup"><span data-stu-id="60c81-118">**Create**</span></span>](create-method-in-class-win32-process.md)                   | <span data-ttu-id="60c81-119">Crea un nuevo proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-119">Creates a new process.</span></span><br/>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="60c81-120">**GetAvailableVirtualSize**</span><span class="sxs-lookup"><span data-stu-id="60c81-120">**GetAvailableVirtualSize**</span></span>](getavailablevirtualsize-win32-process.md) | <span data-ttu-id="60c81-121">Recupera el tamaño actual, en bytes, del espacio de direcciones virtuales libre disponible para el proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-121">Retrieves the current size, in bytes, of the free virtual address space available to the process.</span></span><br/> <span data-ttu-id="60c81-122">**Windows server 2012, Windows 8, Windows 7, Windows server 2008 y Windows Vista:** Este método no se admite antes de Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="60c81-122">**Windows Server 2012, Windows 8, Windows 7, Windows Server 2008 and Windows Vista:** This method is not supported before Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="60c81-123">**GetOwner**</span><span class="sxs-lookup"><span data-stu-id="60c81-123">**GetOwner**</span></span>](getowner-method-in-class-win32-process.md)               | <span data-ttu-id="60c81-124">Recupera el nombre de usuario y el nombre de dominio en el que se está ejecutando el proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-124">Retrieves the user name and domain name under which the process is running.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="60c81-125">**GetOwnerSid**</span><span class="sxs-lookup"><span data-stu-id="60c81-125">**GetOwnerSid**</span></span>](getownersid-method-in-class-win32-process.md)         | <span data-ttu-id="60c81-126">Recupera el identificador de seguridad (SID) del propietario de un proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-126">Retrieves the security identifier (SID) for the owner of a process.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="60c81-127">**SetPriority**</span><span class="sxs-lookup"><span data-stu-id="60c81-127">**SetPriority**</span></span>](setpriority-method-in-class-win32-process.md)         | <span data-ttu-id="60c81-128">Cambia la prioridad de ejecución de un proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-128">Changes the execution priority of a process.</span></span><br/>                                                                                                                                                                                                                                   |
| [<span data-ttu-id="60c81-129">**Terminate**</span><span class="sxs-lookup"><span data-stu-id="60c81-129">**Terminate**</span></span>](terminate-method-in-class-win32-process.md)             | <span data-ttu-id="60c81-130">Finaliza un proceso y todos sus subprocesos.</span><span class="sxs-lookup"><span data-stu-id="60c81-130">Terminates a process and all of its threads.</span></span><br/>                                                                                                                                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="60c81-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60c81-131">Properties</span></span>

<span data-ttu-id="60c81-132">La clase de **\_ proceso de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="60c81-132">The **Win32\_Process** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60c81-133">**Caption**</span><span class="sxs-lookup"><span data-stu-id="60c81-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c81-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-136">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="60c81-136">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-137">Breve descripción de un objeto: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="60c81-137">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="60c81-138">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-139">**CommandLine**</span><span class="sxs-lookup"><span data-stu-id="60c81-139">**CommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c81-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-142">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("línea de comandos para iniciar proceso")</span><span class="sxs-lookup"><span data-stu-id="60c81-142">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Command Line To Start Process")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-143">Línea de comandos que se usa para iniciar un proceso específico, si procede.</span><span class="sxs-lookup"><span data-stu-id="60c81-143">Command line used to start a specific process, if applicable.</span></span>

</dd> <dt>

<span data-ttu-id="60c81-144">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="60c81-144">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c81-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-147">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="60c81-147">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-148">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="60c81-148">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="60c81-149">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="60c81-149">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="60c81-150">Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-150">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-151">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="60c81-151">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-152">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="60c81-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-154">Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")</span><span class="sxs-lookup"><span data-stu-id="60c81-154">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-155">Fecha en que comienza la ejecución del proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-155">Date the process begins executing.</span></span>

<span data-ttu-id="60c81-156">Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-156">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-157">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="60c81-157">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c81-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-160">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**displayName**](../wmisdk/standard-qualifiers.md) (" Computer System Class name ")</span><span class="sxs-lookup"><span data-stu-id="60c81-160">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-161">Nombre de la clase de creación del sistema de ámbito del equipo.</span><span class="sxs-lookup"><span data-stu-id="60c81-161">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="60c81-162">Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-162">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-163">**CSName**</span><span class="sxs-lookup"><span data-stu-id="60c81-163">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c81-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-166">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**displayName**](../wmisdk/standard-qualifiers.md) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="60c81-166">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-167">Nombre del sistema de ámbito del equipo.</span><span class="sxs-lookup"><span data-stu-id="60c81-167">Name of the scoping computer system.</span></span>

<span data-ttu-id="60c81-168">Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-168">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-169">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="60c81-169">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c81-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-172">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="60c81-172">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-173">Descripción de un objeto.</span><span class="sxs-lookup"><span data-stu-id="60c81-173">Description of an object.</span></span>

<span data-ttu-id="60c81-174">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-175">**ExecutablePath _s**</span><span class="sxs-lookup"><span data-stu-id="60c81-175">**ExecutablePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c81-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-178">Calificadores: [**privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Tool Help Structures \| [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) \| SzExePath"), [**displayName**](../wmisdk/standard-qualifiers.md) ("ruta de acceso del archivo ejecutable")</span><span class="sxs-lookup"><span data-stu-id="60c81-178">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32)\|szExePath"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Executable Path")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-179">Ruta de acceso al archivo ejecutable del proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-179">Path to the executable file of the process.</span></span>

<span data-ttu-id="60c81-180">Ejemplo: "C: \\ Windows \\ System \\Explorer.Exe"</span><span class="sxs-lookup"><span data-stu-id="60c81-180">Example: "C:\\Windows\\System\\Explorer.Exe"</span></span>

</dd> <dt>

<span data-ttu-id="60c81-181">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="60c81-181">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-182">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60c81-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-184">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("estado de ejecución")</span><span class="sxs-lookup"><span data-stu-id="60c81-184">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Execution State")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-185">Condición de funcionamiento actual del proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-185">Current operating condition of the process.</span></span>

<span data-ttu-id="60c81-186">Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-186">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="60c81-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="60c81-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="60c81-188">Unknown</span><span class="sxs-lookup"><span data-stu-id="60c81-188">Unknown</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="60c81-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="60c81-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="60c81-190">Otros</span><span class="sxs-lookup"><span data-stu-id="60c81-190">Other</span></span>

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="60c81-191"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Listo** (2)</span><span class="sxs-lookup"><span data-stu-id="60c81-191"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="60c81-192"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="60c81-192"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="60c81-193"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Bloqueado** (4)</span><span class="sxs-lookup"><span data-stu-id="60c81-193"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blocked** (4)</span></span>


</dt> <dd>

<span data-ttu-id="60c81-194">Bloqueado</span><span class="sxs-lookup"><span data-stu-id="60c81-194">Blocked</span></span>

</dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="60c81-195"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspendido bloqueado** (5)</span><span class="sxs-lookup"><span data-stu-id="60c81-195"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="60c81-196"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspendido preparado** (6)</span><span class="sxs-lookup"><span data-stu-id="60c81-196"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspended Ready** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="60c81-197"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminada** (7)</span><span class="sxs-lookup"><span data-stu-id="60c81-197"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="60c81-198"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (8)</span><span class="sxs-lookup"><span data-stu-id="60c81-198"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span data-ttu-id="60c81-199"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>En **aumento** (9)</span><span class="sxs-lookup"><span data-stu-id="60c81-199"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Growing** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60c81-200">**Handle**</span><span class="sxs-lookup"><span data-stu-id="60c81-200">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c81-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-203">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**displayName**](../wmisdk/standard-qualifiers.md) ("Handle")</span><span class="sxs-lookup"><span data-stu-id="60c81-203">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-204">Identificador del proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-204">Process identifier.</span></span>

<span data-ttu-id="60c81-205">Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-205">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-206">**HandleCount**</span><span class="sxs-lookup"><span data-stu-id="60c81-206">**HandleCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-207">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c81-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-209">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \| información de proceso del sistema de estado de proceso inesperados win32api \_ \_ \| HandleCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("número de identificadores")</span><span class="sxs-lookup"><span data-stu-id="60c81-209">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|HandleCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle Count")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-210">Número total de identificadores abiertos propiedad del proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-210">Total number of open handles owned by the process.</span></span> <span data-ttu-id="60c81-211">**HandleCount** es la suma de los identificadores abiertos actualmente por cada subproceso de este proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-211">**HandleCount** is the sum of the handles currently open by each thread in this process.</span></span> <span data-ttu-id="60c81-212">Un identificador se utiliza para examinar o modificar los recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="60c81-212">A handle is used to examine or modify the system resources.</span></span> <span data-ttu-id="60c81-213">Cada controlador tiene una entrada en una tabla que se mantiene internamente.</span><span class="sxs-lookup"><span data-stu-id="60c81-213">Each handle has an entry in a table that is maintained internally.</span></span> <span data-ttu-id="60c81-214">Las entradas contienen las direcciones de los recursos y los datos para identificar el tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="60c81-214">Entries contain the addresses of the resources and data to identify the resource type.</span></span>

</dd> <dt>

<span data-ttu-id="60c81-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="60c81-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-216">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="60c81-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-218">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="60c81-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-219">Fecha en que se instala un objeto.</span><span class="sxs-lookup"><span data-stu-id="60c81-219">Date an object is installed.</span></span> <span data-ttu-id="60c81-220">El objeto se puede instalar sin que se escriba un valor en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="60c81-220">The object may be installed without a value being written to this property.</span></span>

<span data-ttu-id="60c81-221">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-222">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="60c81-222">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-223">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60c81-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-225">Calificadores: [**invalidación**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**unidades**](../wmisdk/standard-qualifiers.md) ("100 nanosegundos")</span><span class="sxs-lookup"><span data-stu-id="60c81-225">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-226">Tiempo en modo kernel, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="60c81-226">Time in kernel mode, in milliseconds.</span></span> <span data-ttu-id="60c81-227">Si esta información no está disponible, utilice un valor de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="60c81-227">If this information is not available, use a value of 0 (zero).</span></span>

<span data-ttu-id="60c81-228">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-228">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-229">**MaximumWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="60c81-229">**MaximumWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-230">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c81-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-232">Calificadores: [**privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| Winnt. H \| \_ límites \| de cuota MaximumWorkingSetSize "), [**displayName**](../wmisdk/standard-qualifiers.md) (" tamaño máximo del espacio de trabajo "), [**unidades**](../wmisdk/standard-qualifiers.md) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="60c81-232">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\|WINNT.H\|QUOTA\_LIMITS\|MaximumWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Maximum Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-233">Tamaño máximo del espacio de trabajo del proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-233">Maximum working set size of the process.</span></span> <span data-ttu-id="60c81-234">El espacio de trabajo de un proceso es el conjunto de páginas de memoria visibles para el proceso en la RAM física.</span><span class="sxs-lookup"><span data-stu-id="60c81-234">The working set of a process is the set of memory pages visible to the process in physical RAM.</span></span> <span data-ttu-id="60c81-235">Estas páginas son residentes y están disponibles para que una aplicación las use sin desencadenar un error de página.</span><span class="sxs-lookup"><span data-stu-id="60c81-235">These pages are resident, and available for an application to use without triggering a page fault.</span></span>

<span data-ttu-id="60c81-236">Ejemplo: 1413120</span><span class="sxs-lookup"><span data-stu-id="60c81-236">Example: 1413120</span></span>

</dd> <dt>

<span data-ttu-id="60c81-237">**MinimumWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="60c81-237">**MinimumWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-238">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c81-238">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-240">Calificadores: [**privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| Winnt. H \| \_ límites \| de cuota MinimumWorkingSetSize "), [**displayName**](../wmisdk/standard-qualifiers.md) (" tamaño mínimo del espacio de trabajo "), [**unidades**](../wmisdk/standard-qualifiers.md) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="60c81-240">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\|WINNT.H\|QUOTA\_LIMITS\|MinimumWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Minimum Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-241">Tamaño mínimo del espacio de trabajo del proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-241">Minimum working set size of the process.</span></span> <span data-ttu-id="60c81-242">El espacio de trabajo de un proceso es el conjunto de páginas de memoria visibles para el proceso en la RAM física.</span><span class="sxs-lookup"><span data-stu-id="60c81-242">The working set of a process is the set of memory pages visible to the process in physical RAM.</span></span> <span data-ttu-id="60c81-243">Estas páginas son residentes y están disponibles para que una aplicación las use sin desencadenar un error de página.</span><span class="sxs-lookup"><span data-stu-id="60c81-243">These pages are resident and available for an application to use without triggering a page fault.</span></span>

<span data-ttu-id="60c81-244">Ejemplo: 20480</span><span class="sxs-lookup"><span data-stu-id="60c81-244">Example: 20480</span></span>

</dd> <dt>

<span data-ttu-id="60c81-245">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="60c81-245">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-246">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c81-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-248">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="60c81-248">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-249">Nombre del archivo ejecutable responsable del proceso, equivalente a la propiedad nombre de imagen del administrador de tareas.</span><span class="sxs-lookup"><span data-stu-id="60c81-249">Name of the executable file responsible for the process, equivalent to the Image Name property in Task Manager.</span></span>

<span data-ttu-id="60c81-250">Cuando se hereda mediante una subclase, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="60c81-250">When inherited by a subclass, the property can be overridden to be a key property.</span></span> <span data-ttu-id="60c81-251">El nombre se codifica de forma rígida en la propia aplicación y no se ve afectado por el cambio del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="60c81-251">The name is hard-coded into the application itself and is not affected by changing the file name.</span></span> <span data-ttu-id="60c81-252">Por ejemplo, incluso si cambia el nombre de Calc.exe, el nombre Calc.exe seguirá apareciendo en el administrador de tareas y en cualquier script de WMI que recupere el nombre del proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-252">For example, even if you rename Calc.exe, the name Calc.exe will still appear in Task Manager and in any WMI scripts that retrieve the process name.</span></span>

<span data-ttu-id="60c81-253">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-253">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-254">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="60c81-254">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-255">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c81-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-257">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre de clase del sistema operativo ")</span><span class="sxs-lookup"><span data-stu-id="60c81-257">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Operating System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-258">Nombre de la clase de creación del sistema operativo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="60c81-258">Creation class name of the scoping operating system.</span></span>

<span data-ttu-id="60c81-259">Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-259">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-260">**OSName**</span><span class="sxs-lookup"><span data-stu-id="60c81-260">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c81-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-263">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Nombre**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre del sistema operativo ")</span><span class="sxs-lookup"><span data-stu-id="60c81-263">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Operating System Name")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-264">Nombre del sistema operativo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="60c81-264">Name of the scoping operating system.</span></span>

<span data-ttu-id="60c81-265">Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-265">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-266">**OtherOperationCount**</span><span class="sxs-lookup"><span data-stu-id="60c81-266">**OtherOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-267">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60c81-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-269">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| información de proceso del sistema \_ \_ \| OtherOperationCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("otro recuento de operaciones")</span><span class="sxs-lookup"><span data-stu-id="60c81-269">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|OtherOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-270">Número de operaciones de e/s realizadas que no son operaciones de lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="60c81-270">Number of I/O operations performed that are not read or write operations.</span></span>

<span data-ttu-id="60c81-271">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-271">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-272">**OtherTransferCount**</span><span class="sxs-lookup"><span data-stu-id="60c81-272">**OtherTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-273">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60c81-273">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-275">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| información de proceso del sistema \_ \_ \| OtherTransferCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("otro recuento de transferencias"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="60c81-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|OtherTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-276">Cantidad de datos transferidos durante las operaciones que no son operaciones de lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="60c81-276">Amount of data transferred during operations that are not read or write operations.</span></span>

<span data-ttu-id="60c81-277">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-277">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-278">**PageFaults**</span><span class="sxs-lookup"><span data-stu-id="60c81-278">**PageFaults**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-279">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c81-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-281">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \| \_ información de proceso del sistema de estado de proceso inesperados win32api \_ \| PageFaultCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("número de errores de página")</span><span class="sxs-lookup"><span data-stu-id="60c81-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PageFaultCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Number Of Page Faults")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-282">Número de errores de página que genera un proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-282">Number of page faults that a process generates.</span></span>

<span data-ttu-id="60c81-283">Ejemplo: 10</span><span class="sxs-lookup"><span data-stu-id="60c81-283">Example: 10</span></span>

</dd> <dt>

<span data-ttu-id="60c81-284">**PageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="60c81-284">**PageFileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-285">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c81-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-287">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \| información de proceso del sistema de estado de proceso inesperados win32api \_ \_ \| PagefileUsage"), [**displayName**](../wmisdk/standard-qualifiers.md) ("uso del archivo de paginación"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="60c81-287">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-288">Cantidad de espacio del archivo de paginación que un proceso está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="60c81-288">Amount of page file space that a process is using currently.</span></span> <span data-ttu-id="60c81-289">Este valor es coherente con el valor de **VMSize** en TaskMgr.exe.</span><span class="sxs-lookup"><span data-stu-id="60c81-289">This value is consistent with the **VMSize** value in TaskMgr.exe.</span></span>

<span data-ttu-id="60c81-290">Ejemplo: 102435</span><span class="sxs-lookup"><span data-stu-id="60c81-290">Example: 102435</span></span>

</dd> <dt>

<span data-ttu-id="60c81-291">**ParentProcessId**</span><span class="sxs-lookup"><span data-stu-id="60c81-291">**ParentProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-292">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c81-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-294">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process status Process \| System \_ \_ Information \| InheritedFromUniqueProcessId"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Parent Process ID")</span><span class="sxs-lookup"><span data-stu-id="60c81-294">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|InheritedFromUniqueProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Parent Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-295">Identificador único del proceso que crea un proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-295">Unique identifier of the process that creates a process.</span></span> <span data-ttu-id="60c81-296">Los números de identificador de proceso se reutilizan, por lo que solo identifican un proceso para la duración de ese proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-296">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="60c81-297">Es posible que el proceso identificado por **ParentProcessId** termine, de modo que **ParentProcessId** no puede hacer referencia a un proceso en ejecución.</span><span class="sxs-lookup"><span data-stu-id="60c81-297">It is possible that the process identified by **ParentProcessId** is terminated, so **ParentProcessId** may not refer to a running process.</span></span> <span data-ttu-id="60c81-298">También es posible que **ParentProcessId** haga referencia incorrectamente a un proceso que reutiliza un identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-298">It is also possible that **ParentProcessId** incorrectly refers to a process that reuses a process identifier.</span></span> <span data-ttu-id="60c81-299">Puede usar la propiedad **CreationDate** para determinar si se ha creado el elemento primario especificado después de que se haya creado el proceso representado por esta instancia de **\_ proceso de Win32** .</span><span class="sxs-lookup"><span data-stu-id="60c81-299">You can use the **CreationDate** property to determine whether the specified parent was created after the process represented by this **Win32\_Process** instance was created.</span></span>

</dd> <dt>

<span data-ttu-id="60c81-300">**PeakPageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="60c81-300">**PeakPageFileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-301">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c81-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-303">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process status \| \_ Process System \_ Information Information \| PeakPagefileUsage"), [**displayName**](../wmisdk/standard-qualifiers.md) ("uso máximo de archivo de paginación"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="60c81-303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakPagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-304">Cantidad máxima de espacio de archivo de paginación utilizada durante la vida de un proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-304">Maximum amount of page file space used during the life of a process.</span></span>

<span data-ttu-id="60c81-305">Ejemplo: 102367</span><span class="sxs-lookup"><span data-stu-id="60c81-305">Example: 102367</span></span>

</dd> <dt>

<span data-ttu-id="60c81-306">**PeakVirtualSize**</span><span class="sxs-lookup"><span data-stu-id="60c81-306">**PeakVirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-307">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60c81-307">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-309">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process status \| \_ Process System \_ Information Information \| PeakVirtualSize"), [**displayName**](../wmisdk/standard-qualifiers.md) ("pico de uso de espacio de direcciones de virtual"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="60c81-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakVirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Virual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-310">Espacio de direcciones virtuales máximo que utiliza un proceso en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="60c81-310">Maximum virtual address space a process uses at any one time.</span></span> <span data-ttu-id="60c81-311">El uso del espacio de direcciones virtuales no implica necesariamente el uso correspondiente del disco o las páginas de memoria principal.</span><span class="sxs-lookup"><span data-stu-id="60c81-311">Using virtual address space does not necessarily imply corresponding use of either disk or main memory pages.</span></span> <span data-ttu-id="60c81-312">Sin embargo, el espacio virtual es finito y, si se usa demasiado, es posible que el proceso no pueda cargar bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="60c81-312">However, virtual space is finite, and by using too much the process might not be able to load libraries.</span></span>

<span data-ttu-id="60c81-313">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-313">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-314">**PeakWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="60c81-314">**PeakWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-315">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c81-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-317">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process status \| \_ Process System \_ Information Information \| PeakWorkingSetSize"), [**displayName**](../wmisdk/standard-qualifiers.md) ("tamaño máximo del espacio de trabajo"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="60c81-317">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-318">Tamaño máximo del espacio de trabajo de un proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-318">Peak working set size of a process.</span></span>

<span data-ttu-id="60c81-319">Ejemplo: 1413120</span><span class="sxs-lookup"><span data-stu-id="60c81-319">Example: 1413120</span></span>

</dd> <dt>

<span data-ttu-id="60c81-320">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="60c81-320">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-321">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c81-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-323">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process status \| Process System \_ \_ Information \| BasePriority"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Priority")</span><span class="sxs-lookup"><span data-stu-id="60c81-323">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|BasePriority"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Priority")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-324">La prioridad de programación de un proceso dentro de un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="60c81-324">Scheduling priority of a process within an operating system.</span></span> <span data-ttu-id="60c81-325">Cuanto mayor sea el valor, más prioridad recibirá un proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-325">The higher the value, the higher priority a process receives.</span></span> <span data-ttu-id="60c81-326">Los valores de prioridad pueden oscilar entre 0 (cero), que es la prioridad más baja a 31, que es la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="60c81-326">Priority values can range from 0 (zero), which is the lowest priority to 31, which is highest priority.</span></span>

<span data-ttu-id="60c81-327">Ejemplo: 7</span><span class="sxs-lookup"><span data-stu-id="60c81-327">Example: 7</span></span>

</dd> <dt>

<span data-ttu-id="60c81-328">**PrivatePageCount**</span><span class="sxs-lookup"><span data-stu-id="60c81-328">**PrivatePageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-329">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60c81-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-331">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| información de proceso del sistema de estado de proceso inesperados win32api \| \_ \_ \| PrivatePageCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("número de páginas privadas")</span><span class="sxs-lookup"><span data-stu-id="60c81-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PrivatePageCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Private Page Count")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-332">Número actual de páginas asignadas que solo son accesibles para el proceso representado por esta instancia de **\_ proceso de Win32** .</span><span class="sxs-lookup"><span data-stu-id="60c81-332">Current number of pages allocated that are only accessible to the process represented by this **Win32\_Process** instance.</span></span>

<span data-ttu-id="60c81-333">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-334">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="60c81-334">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-335">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c81-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-337">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**Process \_ Information**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) \| DwProcessId"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Process ID")</span><span class="sxs-lookup"><span data-stu-id="60c81-337">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**PROCESS\_INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)\|dwProcessId "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-338">Identificador numérico que se usa para distinguir un proceso de otro.</span><span class="sxs-lookup"><span data-stu-id="60c81-338">Numeric identifier used to distinguish one process from another.</span></span> <span data-ttu-id="60c81-339">Los ProcessIDs son válidos desde el momento de creación del proceso para la terminación del proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-339">ProcessIDs are valid from process creation time to process termination.</span></span> <span data-ttu-id="60c81-340">Tras la finalización, se puede aplicar el mismo identificador numérico a un nuevo proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-340">Upon termination, that same numeric identifier can be applied to a new process.</span></span>

<span data-ttu-id="60c81-341">Esto significa que no puede usar ProcessID solo para supervisar un proceso determinado.</span><span class="sxs-lookup"><span data-stu-id="60c81-341">This means that you cannot use ProcessID alone to monitor a particular process.</span></span> <span data-ttu-id="60c81-342">Por ejemplo, una aplicación podría tener un ProcessID de 7 y, a continuación, producir un error.</span><span class="sxs-lookup"><span data-stu-id="60c81-342">For example, an application could have a ProcessID of 7, and then fail.</span></span> <span data-ttu-id="60c81-343">Cuando se inicia un nuevo proceso, se puede asignar el ID. de proceso 7 al nuevo proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-343">When a new process is started, the new process could be assigned ProcessID 7.</span></span> <span data-ttu-id="60c81-344">Por lo tanto, un script que solo comprobó un ProcessID especificado podría "engañarse" para pensar que la aplicación original todavía se estaba ejecutando.</span><span class="sxs-lookup"><span data-stu-id="60c81-344">A script that checked only for a specified ProcessID could thus be "fooled" into thinking that the original application was still running.</span></span>

</dd> <dt>

<span data-ttu-id="60c81-345">**QuotaNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="60c81-345">**QuotaNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-346">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c81-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-348">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \| información de proceso del sistema de estado de proceso inesperados win32api \_ \_ \| QuotaNonPagedPoolUsage"), [**displayName**](../wmisdk/standard-qualifiers.md) ("cuota de uso de bloque no paginado")</span><span class="sxs-lookup"><span data-stu-id="60c81-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Non-Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-349">Cuota de uso de bloque no paginado para un proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-349">Quota amount of nonpaged pool usage for a process.</span></span>

<span data-ttu-id="60c81-350">Ejemplo: 15</span><span class="sxs-lookup"><span data-stu-id="60c81-350">Example: 15</span></span>

</dd> <dt>

<span data-ttu-id="60c81-351">**QuotaPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="60c81-351">**QuotaPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-352">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c81-352">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-354">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \| información de proceso del sistema de estado de proceso inesperados win32api \_ \_ \| QuotaPagedPoolUsage"), [**displayName**](../wmisdk/standard-qualifiers.md) ("cuota de uso del grupo paginado")</span><span class="sxs-lookup"><span data-stu-id="60c81-354">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-355">Cuota de uso del grupo paginado para un proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-355">Quota amount of paged pool usage for a process.</span></span>

<span data-ttu-id="60c81-356">Ejemplo: 22</span><span class="sxs-lookup"><span data-stu-id="60c81-356">Example: 22</span></span>

</dd> <dt>

<span data-ttu-id="60c81-357">**QuotaPeakNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="60c81-357">**QuotaPeakNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-358">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c81-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-360">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \| información de proceso del sistema de estado de proceso inesperados win32api \_ \_ \| QuotaPeakNonPagedPoolUsage"), [**displayName**](../wmisdk/standard-qualifiers.md) ("cuota máxima de uso de bloque no paginado")</span><span class="sxs-lookup"><span data-stu-id="60c81-360">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPeakNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Non-Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-361">Cantidad máxima de cuota de uso de bloque no paginado para un proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-361">Peak quota amount of nonpaged pool usage for a process.</span></span>

<span data-ttu-id="60c81-362">Ejemplo: 31</span><span class="sxs-lookup"><span data-stu-id="60c81-362">Example: 31</span></span>

</dd> <dt>

<span data-ttu-id="60c81-363">**QuotaPeakPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="60c81-363">**QuotaPeakPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-364">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c81-364">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-366">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \| información de proceso del sistema de estado de proceso inesperados win32api \_ \_ \| QuotaPeakPagedPoolUsage"), [**displayName**](../wmisdk/standard-qualifiers.md) ("cuota máxima de uso del grupo paginado")</span><span class="sxs-lookup"><span data-stu-id="60c81-366">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPeakPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-367">Cantidad máxima de cuota de uso del grupo paginado para un proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-367">Peak quota amount of paged pool usage for a process.</span></span>

<span data-ttu-id="60c81-368">Ejemplo: 31</span><span class="sxs-lookup"><span data-stu-id="60c81-368">Example: 31</span></span>

</dd> <dt>

<span data-ttu-id="60c81-369">**ReadOperationCount**</span><span class="sxs-lookup"><span data-stu-id="60c81-369">**ReadOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-370">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60c81-370">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-372">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| de proceso y estructuras de subprocesos \| información de proceso del sistema \_ \_ \| ReadOperationCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("número de operaciones de lectura")</span><span class="sxs-lookup"><span data-stu-id="60c81-372">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|ReadOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-373">Número de operaciones de lectura realizadas.</span><span class="sxs-lookup"><span data-stu-id="60c81-373">Number of read operations performed.</span></span>

<span data-ttu-id="60c81-374">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-374">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-375">**ReadTransferCount**</span><span class="sxs-lookup"><span data-stu-id="60c81-375">**ReadTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-376">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60c81-376">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-378">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| información de proceso del sistema \_ \_ \| ReadTransferCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("recuento de transferencias de lectura"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="60c81-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|ReadTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-379">Cantidad de datos leídos.</span><span class="sxs-lookup"><span data-stu-id="60c81-379">Amount of data read.</span></span>

<span data-ttu-id="60c81-380">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-380">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-381">**SessionId**</span><span class="sxs-lookup"><span data-stu-id="60c81-381">**SessionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-382">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c81-382">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-384">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process status \| System \_ Process \_ Information \| SessionID"), [**displayName**](../wmisdk/standard-qualifiers.md) ("ID. de sesión")</span><span class="sxs-lookup"><span data-stu-id="60c81-384">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|SessionId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Session Id")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-385">Identificador único que genera un sistema operativo cuando se crea una sesión.</span><span class="sxs-lookup"><span data-stu-id="60c81-385">Unique identifier that an operating system generates when a session is created.</span></span> <span data-ttu-id="60c81-386">Una sesión abarca un período de tiempo desde el inicio de sesión hasta el cierre de sesión desde un sistema específico.</span><span class="sxs-lookup"><span data-stu-id="60c81-386">A session spans a period of time from logon until logoff from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="60c81-387">**Estado**</span><span class="sxs-lookup"><span data-stu-id="60c81-387">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-388">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c81-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-389">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-389">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-390">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="60c81-390">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-391">Esta propiedad no está implementada y no se rellena para ninguna instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="60c81-391">This property is not implemented and does not get populated for any instance of this class.</span></span> <span data-ttu-id="60c81-392">Siempre es **null**.</span><span class="sxs-lookup"><span data-stu-id="60c81-392">It is always **NULL**.</span></span>

<span data-ttu-id="60c81-393">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-393">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="60c81-394">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="60c81-394">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="60c81-395">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="60c81-395">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="60c81-396">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="60c81-396">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="60c81-397">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="60c81-397">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="60c81-398">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="60c81-398">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="60c81-399">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="60c81-399">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="60c81-400">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="60c81-400">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="60c81-401">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="60c81-401">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="60c81-402">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="60c81-402">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="60c81-403">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="60c81-403">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="60c81-404">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="60c81-404">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="60c81-405">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="60c81-405">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="60c81-406">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="60c81-406">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60c81-407">**TerminationDate**</span><span class="sxs-lookup"><span data-stu-id="60c81-407">**TerminationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-408">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="60c81-408">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-409">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-410">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("fecha de finalización")</span><span class="sxs-lookup"><span data-stu-id="60c81-410">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Termination Date")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-411">El proceso se detuvo o finalizó.</span><span class="sxs-lookup"><span data-stu-id="60c81-411">Process was stopped or terminated.</span></span> <span data-ttu-id="60c81-412">Para obtener el tiempo de finalización, se debe mantener abierto un identificador del proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-412">To get the termination time, a handle to the process must be held open.</span></span> <span data-ttu-id="60c81-413">De lo contrario, esta propiedad devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="60c81-413">Otherwise, this property returns **NULL**.</span></span>

<span data-ttu-id="60c81-414">Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-414">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-415">**ThreadCount**</span><span class="sxs-lookup"><span data-stu-id="60c81-415">**ThreadCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-416">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c81-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-417">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-418">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process status \| \_ Process System \_ Information \| NumberOfThreads"), [**displayName**](../wmisdk/standard-qualifiers.md) ("recuento de subprocesos")</span><span class="sxs-lookup"><span data-stu-id="60c81-418">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|NumberOfThreads"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Thread Count")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-419">Número de subprocesos activos en un proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-419">Number of active threads in a process.</span></span> <span data-ttu-id="60c81-420">Una instrucción es la unidad básica de ejecución en un procesador y un subproceso es el objeto que ejecuta una instrucción.</span><span class="sxs-lookup"><span data-stu-id="60c81-420">An instruction is the basic unit of execution in a processor, and a thread is the object that executes an instruction.</span></span> <span data-ttu-id="60c81-421">Cada proceso en ejecución tiene al menos un subproceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-421">Each running process has at least one thread.</span></span>

</dd> <dt>

<span data-ttu-id="60c81-422">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="60c81-422">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-423">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60c81-423">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-424">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-425">Calificadores: [**invalidación**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**unidades**](../wmisdk/standard-qualifiers.md) ("100 nanosegundos")</span><span class="sxs-lookup"><span data-stu-id="60c81-425">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-426">Tiempo en modo de usuario, en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="60c81-426">Time in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="60c81-427">Si esta información no está disponible, utilice un valor de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="60c81-427">If this information is not available, use a value of 0 (zero).</span></span>

<span data-ttu-id="60c81-428">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-428">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-429">**VirtualSize**</span><span class="sxs-lookup"><span data-stu-id="60c81-429">**VirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-430">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60c81-430">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-431">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-432">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \| información de proceso del sistema de estado de proceso inesperados win32api \_ \_ \| VirtualSize"), [**displayName**](../wmisdk/standard-qualifiers.md) ("uso del espacio de direcciones virtuales"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="60c81-432">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|VirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Virtual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-433">Tamaño actual del espacio de direcciones virtuales que usa un proceso, no de la memoria física o virtual usada realmente por el proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-433">Current size of the virtual address space that a process is using, not the physical or virtual memory actually used by the process.</span></span> <span data-ttu-id="60c81-434">El uso del espacio de direcciones virtuales no implica necesariamente el uso correspondiente del disco o las páginas de memoria principal.</span><span class="sxs-lookup"><span data-stu-id="60c81-434">Using virtual address space does not necessarily imply corresponding use of either disk or main memory pages.</span></span> <span data-ttu-id="60c81-435">El espacio virtual es finito y, si se usa demasiado, es posible que el proceso no pueda cargar bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="60c81-435">Virtual space is finite, and by using too much, the process might not be able to load libraries.</span></span> <span data-ttu-id="60c81-436">Este valor es coherente con lo que se ve en Perfmon.exe.</span><span class="sxs-lookup"><span data-stu-id="60c81-436">This value is consistent with what you see in Perfmon.exe.</span></span>

<span data-ttu-id="60c81-437">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-437">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-438">**WindowsVersion**</span><span class="sxs-lookup"><span data-stu-id="60c81-438">**WindowsVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-439">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c81-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-441">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Functions \| GetProcessVersion"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Windows version")</span><span class="sxs-lookup"><span data-stu-id="60c81-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Functions\|GetProcessVersion"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Windows Version")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-442">Versión de Windows en la que se está ejecutando el proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-442">Version of Windows in which the process is running.</span></span>

<span data-ttu-id="60c81-443">Ejemplo: 4,0</span><span class="sxs-lookup"><span data-stu-id="60c81-443">Example: 4.0</span></span>

</dd> <dt>

<span data-ttu-id="60c81-444">**WorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="60c81-444">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-445">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60c81-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-446">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-447">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("tamaño del espacio de trabajo"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="60c81-447">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-448">Cantidad de memoria en bytes que un proceso necesita ejecutar de forma eficaz — para un sistema operativo que usa la administración de memoria basada en páginas.</span><span class="sxs-lookup"><span data-stu-id="60c81-448">Amount of memory in bytes that a process needs to execute efficiently—for an operating system that uses page-based memory management.</span></span> <span data-ttu-id="60c81-449">Si el sistema no tiene suficiente memoria (menos que el tamaño del espacio de trabajo), se produce la paginación excesiva.</span><span class="sxs-lookup"><span data-stu-id="60c81-449">If the system does not have enough memory (less than the working set size), thrashing occurs.</span></span> <span data-ttu-id="60c81-450">Si no se conoce el tamaño del espacio de trabajo, utilice **null** o 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="60c81-450">If the size of the working set is not known, use **NULL** or 0 (zero).</span></span> <span data-ttu-id="60c81-451">Si se proporcionan datos del espacio de trabajo, puede supervisar la información para comprender los requisitos de memoria variables de un proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-451">If working set data is provided, you can monitor the information to understand the changing memory requirements of a process.</span></span>

<span data-ttu-id="60c81-452">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-452">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="60c81-453">Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-453">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-454">**WriteOperationCount**</span><span class="sxs-lookup"><span data-stu-id="60c81-454">**WriteOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-455">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60c81-455">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-456">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-456">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-457">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| de proceso y estructuras de subprocesos \| información de proceso del sistema \_ \_ \| WriteOperationCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("número de operaciones de escritura")</span><span class="sxs-lookup"><span data-stu-id="60c81-457">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|WriteOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-458">Número de operaciones de escritura realizadas.</span><span class="sxs-lookup"><span data-stu-id="60c81-458">Number of write operations performed.</span></span>

<span data-ttu-id="60c81-459">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-459">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c81-460">**WriteTransferCount**</span><span class="sxs-lookup"><span data-stu-id="60c81-460">**WriteTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c81-461">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60c81-461">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60c81-462">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c81-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c81-463">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| información de proceso del sistema \_ \_ \| WriteTransferCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("recuento de transferencias de escritura"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="60c81-463">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|WriteTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="60c81-464">Cantidad de datos escritos.</span><span class="sxs-lookup"><span data-stu-id="60c81-464">Amount of data written.</span></span>

<span data-ttu-id="60c81-465">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-465">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60c81-466">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60c81-466">Remarks</span></span>

<span data-ttu-id="60c81-467">La clase de **\_ proceso de Win32** se deriva del [**\_ proceso CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-467">The **Win32\_Process** class is derived from [**CIM\_Process**](cim-process.md).</span></span> <span data-ttu-id="60c81-468">El proceso de llamada que usa esta clase debe tener el privilegio de **\_ \_ nombre de restauración se** en el equipo en el que reside el registro.</span><span class="sxs-lookup"><span data-stu-id="60c81-468">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="60c81-469">Para obtener más información, vea [ejecutar operaciones con privilegios](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-469">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

### <a name="overview"></a><span data-ttu-id="60c81-470">Información general</span><span class="sxs-lookup"><span data-stu-id="60c81-470">Overview</span></span>

<span data-ttu-id="60c81-471">Los procesos subyacen casi todo lo que ocurre en un equipo.</span><span class="sxs-lookup"><span data-stu-id="60c81-471">Processes underlie almost everything that happens on a computer.</span></span> <span data-ttu-id="60c81-472">De hecho, se puede realizar un seguimiento de la causa principal de la mayoría de los problemas del equipo con los procesos; por ejemplo, se podrían estar ejecutando demasiados procesos en un equipo (y se está consiguiendo un conjunto finito de recursos), o bien un único proceso podría estar usando más de su recurso compartido de recursos.</span><span class="sxs-lookup"><span data-stu-id="60c81-472">In fact, the root cause of most computer problems can be traced to processes; for example, too many processes might be running on a computer (and contending for a finite set of resources), or a single process might be using more than its share of resources.</span></span> <span data-ttu-id="60c81-473">Estos factores hacen que sea importante mantener una observación cercana en los procesos que se ejecutan en un equipo.</span><span class="sxs-lookup"><span data-stu-id="60c81-473">These factors make it important to keep a close watch on the processes running on a computer.</span></span> <span data-ttu-id="60c81-474">La supervisión de procesos, la actividad principal en la administración de procesos, permite determinar lo que realmente hace un equipo, qué aplicaciones ejecuta el equipo y cómo se ven afectadas por los cambios en el entorno informático.</span><span class="sxs-lookup"><span data-stu-id="60c81-474">Process monitoring, the main activity in process management, allows you to determine what a computer actually does, what applications the computer runs, and how those applications are affected by changes in the computing environment.</span></span>

### <a name="monitoring-a-process"></a><span data-ttu-id="60c81-475">Supervisión de un proceso</span><span class="sxs-lookup"><span data-stu-id="60c81-475">Monitoring a Process</span></span>

<span data-ttu-id="60c81-476">La supervisión de procesos de forma periódica le ayuda a garantizar que un equipo se ejecute con una eficacia máxima y que lleve a cabo sus tareas designadas según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="60c81-476">Monitoring processes on a regular basis helps you ensure that a computer runs at peak efficiency and that it carries out its appointed tasks as expected.</span></span> <span data-ttu-id="60c81-477">Por ejemplo, mediante la supervisión de procesos se puede recibir una notificación inmediata de cualquier aplicación que haya dejado de responder y, a continuación, realizar los pasos necesarios para finalizar el proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-477">For example, by monitoring processes you can be notified immediately of any application that has stopped responding, and then take steps to end that process.</span></span> <span data-ttu-id="60c81-478">Además, la supervisión de procesos permite identificar problemas antes de que se produzcan.</span><span class="sxs-lookup"><span data-stu-id="60c81-478">In addition, process monitoring enables you to identify problems before they occur.</span></span> <span data-ttu-id="60c81-479">Por ejemplo, al comprobar repetidamente la cantidad de memoria usada por un proceso, puede identificar una fuga de memoria.</span><span class="sxs-lookup"><span data-stu-id="60c81-479">For example, by repeatedly checking the amount of memory used by a process, you can identify a memory leak.</span></span> <span data-ttu-id="60c81-480">Después, puede detener el proceso antes de que la aplicación errante utilice toda la memoria disponible y el equipo se detenga.</span><span class="sxs-lookup"><span data-stu-id="60c81-480">You can then stop the process before the errant application uses all of the available memory and brings the computer to a halt.</span></span>

<span data-ttu-id="60c81-481">La supervisión de procesos también ayuda a minimizar las interrupciones causadas por las interrupciones planeadas para las actualizaciones y el mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="60c81-481">Process monitoring also helps minimize the disruptions caused by planned outages for upgrades and maintenance.</span></span> <span data-ttu-id="60c81-482">Por ejemplo, al comprobar el estado de una aplicación de base de datos que se ejecuta en los equipos cliente, puede determinar el impacto de dejar la base de datos sin conexión para actualizar el software.</span><span class="sxs-lookup"><span data-stu-id="60c81-482">For example, by checking the status of a database application running on client computers, you can determine the impact of taking the database offline in order to upgrade the software.</span></span>

<span data-ttu-id="60c81-483">Supervisión de la disponibilidad del proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-483">Monitoring process availability.</span></span> <span data-ttu-id="60c81-484">Mide el porcentaje de tiempo que un proceso está disponible.</span><span class="sxs-lookup"><span data-stu-id="60c81-484">Measures the percentage of time that a process is available.</span></span> <span data-ttu-id="60c81-485">La disponibilidad normalmente se supervisa mediante el uso de un sondeo simple, que indica si el proceso sigue en ejecución.</span><span class="sxs-lookup"><span data-stu-id="60c81-485">Availability is typically monitored by use of a simple probe, which reports whether the process is still running.</span></span> <span data-ttu-id="60c81-486">Al realizar un seguimiento de los resultados de cada sondeo, puede calcular la disponibilidad del proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-486">By keeping track of the results of each probe, you can calculate the availability of the process.</span></span> <span data-ttu-id="60c81-487">Por ejemplo, un proceso que se sondea 100 veces y responde en 95 de esas ocasiones tiene una disponibilidad del 95 por ciento.</span><span class="sxs-lookup"><span data-stu-id="60c81-487">For example, a process that is probed 100 times and responds on 95 of those occasions has an availability of 95 percent.</span></span> <span data-ttu-id="60c81-488">Este tipo de supervisión normalmente se reserva para las bases de datos, programas de correo y otras aplicaciones que se espera que se ejecuten en todo momento.</span><span class="sxs-lookup"><span data-stu-id="60c81-488">This type of monitoring is typically reserved for databases, mail programs, and other applications that are expected to run at all times.</span></span> <span data-ttu-id="60c81-489">No es adecuado para programas de procesamiento de texto, hojas de cálculo u otras aplicaciones que se inician de forma rutinaria y se detienen varias veces al día.</span><span class="sxs-lookup"><span data-stu-id="60c81-489">It is not appropriate for word processing programs, spreadsheets, or other applications that are routinely started and stopped several times a day.</span></span>

<span data-ttu-id="60c81-490">Puede crear una instancia de la clase [**Win32 \_ ProcessStartup**](win32-processstartup.md) para configurar el proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-490">You can create an instance of the [**Win32\_ProcessStartup**](win32-processstartup.md) class to configure the process.</span></span>

<span data-ttu-id="60c81-491">Puede supervisar el rendimiento de los procesos con la clase de [**proceso de Win32 \_ PerfFormattedData \_ PerfProc \_**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) y un objeto de actualizador de WMI, como [**SWbemRefresher**](../wmisdk/swbemrefresher.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-491">You can monitor process performance with the [**Win32\_PerfFormattedData\_PerfProc\_Process**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) class and a WMI refresher object, such as [**SWbemRefresher**](../wmisdk/swbemrefresher.md).</span></span> <span data-ttu-id="60c81-492">Para obtener más información, vea [supervisar datos de rendimiento](../wmisdk/monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="60c81-492">For more information, see [Monitoring Performance Data](../wmisdk/monitoring-performance-data.md).</span></span>

## <a name="examples"></a><span data-ttu-id="60c81-493">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="60c81-493">Examples</span></span>

<span data-ttu-id="60c81-494">En el ejemplo [de código de PowerShell de las propiedades de las clases WMI](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) de la galería de TechNet se describe la clase de **\_ proceso de Win32** y se muestran los resultados en formato de Excel.</span><span class="sxs-lookup"><span data-stu-id="60c81-494">The [List the Properties of WMI Classes](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) PowerShell code sample on TechNet Gallery describes the **Win32\_Process** class, and outputs the results in Excel format.</span></span>

<span data-ttu-id="60c81-495">El [proceso de finalización en ejecución en varios servidores](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) finaliza un proceso que se ejecuta en uno o varios equipos.</span><span class="sxs-lookup"><span data-stu-id="60c81-495">The [Terminate running process on multiple servers](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) terminates a process running on a single or multiple computers.</span></span>

<span data-ttu-id="60c81-496">En el tema [ejemplo: llamar a un método de proveedor](../wmisdk/example--calling-a-provider-method.md) , el código usa C++ para llamar al **\_ proceso de Win32** para crear un proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-496">In the [Example: Calling a Provider Method](../wmisdk/example--calling-a-provider-method.md) topic, the code uses C++ to call **Win32\_Process** to create a process.</span></span>

<span data-ttu-id="60c81-497">La disponibilidad es la forma más sencilla de supervisión de procesos: con este enfoque, solo tiene que asegurarse de que el proceso se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="60c81-497">Availability is the simplest form of process monitoring: with this approach, you simply ensure that the process is running.</span></span> <span data-ttu-id="60c81-498">Al supervisar la disponibilidad de los procesos, normalmente se recupera una lista de procesos que se ejecutan en un equipo y, a continuación, se comprueba que un proceso determinado todavía está activo.</span><span class="sxs-lookup"><span data-stu-id="60c81-498">When you monitor for process availability, you typically retrieve a list of processes running on a computer and then verify that a particular process is still active.</span></span> <span data-ttu-id="60c81-499">Si el proceso está activo, se considera que está disponible.</span><span class="sxs-lookup"><span data-stu-id="60c81-499">If the process is active, it is considered available.</span></span> <span data-ttu-id="60c81-500">Si el proceso no está activo, no está disponible.</span><span class="sxs-lookup"><span data-stu-id="60c81-500">If the process is not active, it is not available.</span></span> <span data-ttu-id="60c81-501">El siguiente ejemplo de VBScript supervisa la disponibilidad del proceso mediante la comprobación de la lista de procesos que se ejecutan en un equipo y la emisión de una notificación si no se encuentra el proceso de Database.exe.</span><span class="sxs-lookup"><span data-stu-id="60c81-501">The following VBScript sample monitors process availability by checking the list of processes running on a computer and issuing a notification if the Database.exe process is not found.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Database.exe'")
If colProcesses.Count = 0 Then
 Wscript.Echo "Database.exe is not running."
Else
 Wscript.Echo "Database.exe is running."
End If
```



<span data-ttu-id="60c81-502">El siguiente ejemplo de VBScript supervisa la creación de procesos mediante un consumidor de eventos temporal.</span><span class="sxs-lookup"><span data-stu-id="60c81-502">The following VBScript sample monitors process creation using a temporary event consumer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
                                                     & "WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 Wscript.Echo objLatestProcess.TargetInstance.Name, Now
Loop
```



<span data-ttu-id="60c81-503">El siguiente VBScript supervisa la información de rendimiento del proceso.</span><span class="sxs-lookup"><span data-stu-id="60c81-503">The following VBScript monitors process performance information.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcessList
 Wscript.Echo "Process: " & objProcess.Name
 Wscript.Echo "Process ID: " & objProcess.ProcessID
 Wscript.Echo "Thread Count: " & objProcess.ThreadCount
 Wscript.Echo "Page File Size: " & objProcess.PageFileUsage
 Wscript.Echo "Page Faults: " & objProcess.PageFaults
 Wscript.Echo "Working Set Size: " & objProcess.WorkingSetSize
Next
```



<span data-ttu-id="60c81-504">En el ejemplo de código de VBScript siguiente se muestra cómo obtener el propietario de cada proceso en un equipo local.</span><span class="sxs-lookup"><span data-stu-id="60c81-504">The following VBScript code example shows how to obtain the owner of each process on a local computer.</span></span> <span data-ttu-id="60c81-505">Puede usar este script para obtener datos de un equipo remoto, por ejemplo, para determinar qué usuarios tienen procesos que ejecutan Terminal Server, sustituya el nombre del equipo remoto por "." en la primera línea.</span><span class="sxs-lookup"><span data-stu-id="60c81-505">You can use this script to obtain data from a remote computer, for example, to determine which users have processes running terminal server, substitute the name of the remote computer for "." in the first line.</span></span> <span data-ttu-id="60c81-506">También debe ser administrador en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="60c81-506">You must also be an administrator on the remote machine.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colProcesses = objWMIService.ExecQuery("select * from win32_process" )
For Each objProcess in colProcesses

  If objProcess.GetOwner ( User, Domain ) = 0 Then
    Wscript.Echo "Process " & objProcess.Caption & " belongs to " & Domain & "\" & User
  Else
    Wscript.Echo "Problem " & Rtn & " getting the owner for process " & objProcess.Caption
  End If
Next
```



<span data-ttu-id="60c81-507">En el ejemplo de código de VBScript siguiente se muestra cómo obtener la sesión de inicio de sesión asociada a un proceso en ejecución.</span><span class="sxs-lookup"><span data-stu-id="60c81-507">The following VBScript code example shows how to obtain the logon session associated with a running process.</span></span> <span data-ttu-id="60c81-508">Un proceso debe estar en ejecución Notepad.exe antes de que se inicie el script.</span><span class="sxs-lookup"><span data-stu-id="60c81-508">A process must be running Notepad.exe before the script starts.</span></span> <span data-ttu-id="60c81-509">En el ejemplo se buscan las instancias de [**Win32 \_ LogonSession**](win32-logonsession.md) asociadas al **\_ proceso de Win32** que representa Notepad.exe.</span><span class="sxs-lookup"><span data-stu-id="60c81-509">The example locates the instances of [**Win32\_LogonSession**](win32-logonsession.md) associated with the **Win32\_Process** that represents Notepad.exe.</span></span> <span data-ttu-id="60c81-510">[**Win32 \_ SessionProcess**](win32-sessionprocess.md) se especifica como la clase Association.</span><span class="sxs-lookup"><span data-stu-id="60c81-510">[**Win32\_SessionProcess**](win32-sessionprocess.md) is specified as the association class.</span></span> <span data-ttu-id="60c81-511">Para obtener más información, vea [ASSOCIATORS OF Statement.](../wmisdk/associators-of-statement.md)</span><span class="sxs-lookup"><span data-stu-id="60c81-511">For more information, see [ASSOCIATORS OF Statement.](../wmisdk/associators-of-statement.md).</span></span>


```VB
On error resume next
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\.\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("Select * from Win32_Process Where Name = 'Notepad.exe'")
For Each objProcess in colProcesses
  ProcessId = objProcess.ProcessId
  Set colLogonSessions = objWMIService.ExecQuery("Associators of {Win32_Process='" & ProcessId & "'} " _
                                               & "Where Resultclass = Win32_LogonSession Assocclass = Win32_SessionProcess", "WQL", 48)
  If Err <> 0 Then
    WScript.Echo "Error on associators query= " & Err.number & " " & Err.Description
    WScript.Quit
  End If
  For Each LogonSession in colLogonSessions
    Wscript.Echo " Logon id is " & LogonSession.LogonId
  Next
Next
```



## <a name="requirements"></a><span data-ttu-id="60c81-512">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60c81-512">Requirements</span></span>



| <span data-ttu-id="60c81-513">Requisito</span><span class="sxs-lookup"><span data-stu-id="60c81-513">Requirement</span></span> | <span data-ttu-id="60c81-514">Value</span><span class="sxs-lookup"><span data-stu-id="60c81-514">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60c81-515">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60c81-515">Minimum supported client</span></span><br/> | <span data-ttu-id="60c81-516">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60c81-516">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60c81-517">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60c81-517">Minimum supported server</span></span><br/> | <span data-ttu-id="60c81-518">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60c81-518">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60c81-519">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="60c81-519">Namespace</span></span><br/>                | <span data-ttu-id="60c81-520">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="60c81-520">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="60c81-521">MOF</span><span class="sxs-lookup"><span data-stu-id="60c81-521">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60c81-522"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60c81-522"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="60c81-523">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60c81-523">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60c81-524"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60c81-524"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60c81-525">Vea también</span><span class="sxs-lookup"><span data-stu-id="60c81-525">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60c81-526">**\_Proceso CIM**</span><span class="sxs-lookup"><span data-stu-id="60c81-526">**CIM\_Process**</span></span>](cim-process.md)
</dt> <dt>

[<span data-ttu-id="60c81-527">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="60c81-527">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="60c81-528">Tareas de WMI: procesos</span><span class="sxs-lookup"><span data-stu-id="60c81-528">WMI Tasks: Processes</span></span>](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
