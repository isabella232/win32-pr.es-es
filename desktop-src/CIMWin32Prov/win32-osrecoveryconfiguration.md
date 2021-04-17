---
description: Win32 \_ OSRecoveryConfiguration&\# 8194; La clase WMI representa los tipos de información que se recopilarán de la memoria cuando se produzca un error en el sistema operativo. Esto incluye los errores de arranque y los bloqueos del sistema.
ms.assetid: 0c8a2aeb-2fd9-44b7-8f91-d19afb8d2de6
ms.tgt_platform: multiple
title: Win32_OSRecoveryConfiguration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OSRecoveryConfiguration
- Win32_OSRecoveryConfiguration.Caption
- Win32_OSRecoveryConfiguration.Description
- Win32_OSRecoveryConfiguration.SettingID
- Win32_OSRecoveryConfiguration.AutoReboot
- Win32_OSRecoveryConfiguration.DebugFilePath
- Win32_OSRecoveryConfiguration.DebugInfoType
- Win32_OSRecoveryConfiguration.ExpandedDebugFilePath
- Win32_OSRecoveryConfiguration.ExpandedMiniDumpDirectory
- Win32_OSRecoveryConfiguration.KernelDumpOnly
- Win32_OSRecoveryConfiguration.MiniDumpDirectory
- Win32_OSRecoveryConfiguration.Name
- Win32_OSRecoveryConfiguration.OverwriteExistingDebugFile
- Win32_OSRecoveryConfiguration.SendAdminAlert
- Win32_OSRecoveryConfiguration.WriteDebugInfo
- Win32_OSRecoveryConfiguration.WriteToSystemLog
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2371ba7ee449497e2d695e60d75c59454282d54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659700"
---
# <a name="win32_osrecoveryconfiguration-class"></a><span data-ttu-id="f56ae-104">\_Clase Win32 OSRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f56ae-104">Win32\_OSRecoveryConfiguration class</span></span>

<span data-ttu-id="f56ae-105">La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ OSRecoveryConfiguration de Win32** representa los tipos de información que se recopilarán de la memoria cuando se produzca un error en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f56ae-105">The **Win32\_OSRecoveryConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the types of information that will be gathered from memory when the operating system fails.</span></span> <span data-ttu-id="f56ae-106">Esto incluye los errores de arranque y los bloqueos del sistema.</span><span class="sxs-lookup"><span data-stu-id="f56ae-106">This includes boot failures and system crashes.</span></span>

<span data-ttu-id="f56ae-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f56ae-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f56ae-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f56ae-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f56ae-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f56ae-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4E8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OSRecoveryConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AutoReboot;
  string  DebugFilePath;
  uint32  DebugInfoType;
  string  ExpandedDebugFilePath;
  string  ExpandedMiniDumpDirectory;
  boolean KernelDumpOnly;
  string  MiniDumpDirectory;
  string  Name;
  boolean OverwriteExistingDebugFile;
  boolean SendAdminAlert;
  boolean WriteDebugInfo;
  boolean WriteToSystemLog;
};
```

## <a name="members"></a><span data-ttu-id="f56ae-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f56ae-110">Members</span></span>

<span data-ttu-id="f56ae-111">La **clase \_ OSRecoveryConfiguration de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f56ae-111">The **Win32\_OSRecoveryConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="f56ae-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f56ae-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f56ae-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f56ae-113">Properties</span></span>

<span data-ttu-id="f56ae-114">La **clase \_ OSRecoveryConfiguration de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f56ae-114">The **Win32\_OSRecoveryConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f56ae-115">**AutoReboot**</span><span class="sxs-lookup"><span data-stu-id="f56ae-115">**AutoReboot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56ae-116">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f56ae-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f56ae-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-118">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ CrashControl \| AutoReboot")</span><span class="sxs-lookup"><span data-stu-id="f56ae-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|AutoReboot")</span></span>
</dt> </dl>

<span data-ttu-id="f56ae-119">El sistema se reiniciará automáticamente durante una operación de recuperación.</span><span class="sxs-lookup"><span data-stu-id="f56ae-119">System will automatically reboot during a recovery operation.</span></span>

</dd> <dt>

<span data-ttu-id="f56ae-120">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f56ae-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56ae-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f56ae-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f56ae-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-123">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="f56ae-123">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f56ae-124">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="f56ae-124">Short textual description of the current object.</span></span>

<span data-ttu-id="f56ae-125">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="f56ae-125">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="f56ae-126">**DebugFilePath**</span><span class="sxs-lookup"><span data-stu-id="f56ae-126">**DebugFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56ae-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f56ae-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-128">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f56ae-128">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-129">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ CrashControl \| dumpfile")</span><span class="sxs-lookup"><span data-stu-id="f56ae-129">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|DumpFile")</span></span>
</dt> </dl>

<span data-ttu-id="f56ae-130">Ruta de acceso completa al archivo de depuración.</span><span class="sxs-lookup"><span data-stu-id="f56ae-130">Full path to the debug file.</span></span> <span data-ttu-id="f56ae-131">Un archivo de depuración se crea con el estado de memoria del equipo después de un error del equipo.</span><span class="sxs-lookup"><span data-stu-id="f56ae-131">A debug file is created with the memory state of the computer after a computer failure.</span></span>

<span data-ttu-id="f56ae-132">Ejemplo: "C: \\ Windows \\ Memory. DMP"</span><span class="sxs-lookup"><span data-stu-id="f56ae-132">Example: "C:\\Windows\\Memory.dmp"</span></span>

</dd> <dt>

<span data-ttu-id="f56ae-133">**DebugInfoType**</span><span class="sxs-lookup"><span data-stu-id="f56ae-133">**DebugInfoType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56ae-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f56ae-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f56ae-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f56ae-136">Tipo de información de depuración escrita en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="f56ae-136">Type of debugging information written to the log file.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="f56ae-137">**Ninguno** (0)</span><span class="sxs-lookup"><span data-stu-id="f56ae-137">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Complete_memory_dump"></span><span id="complete_memory_dump"></span><span id="COMPLETE_MEMORY_DUMP"></span>

<span data-ttu-id="f56ae-138">**Volcado de memoria completo** (1)</span><span class="sxs-lookup"><span data-stu-id="f56ae-138">**Complete memory dump** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Kernel_memory_dump"></span><span id="kernel_memory_dump"></span><span id="KERNEL_MEMORY_DUMP"></span>

<span data-ttu-id="f56ae-139">**Volcado de memoria del kernel** (2)</span><span class="sxs-lookup"><span data-stu-id="f56ae-139">**Kernel memory dump** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Small_memory_dump"></span><span id="small_memory_dump"></span><span id="SMALL_MEMORY_DUMP"></span>

<span data-ttu-id="f56ae-140">**Volcado de memoria pequeño** (3)</span><span class="sxs-lookup"><span data-stu-id="f56ae-140">**Small memory dump** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f56ae-141">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f56ae-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56ae-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f56ae-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f56ae-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f56ae-144">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="f56ae-144">Textual description of the current object.</span></span>

<span data-ttu-id="f56ae-145">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="f56ae-145">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="f56ae-146">**ExpandedDebugFilePath**</span><span class="sxs-lookup"><span data-stu-id="f56ae-146">**ExpandedDebugFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56ae-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f56ae-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f56ae-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f56ae-149">Versión expandida de la propiedad **DebugFilePath** .</span><span class="sxs-lookup"><span data-stu-id="f56ae-149">Expanded version of the **DebugFilePath** property.</span></span>

<span data-ttu-id="f56ae-150">Ejemplo: "C: \\ Windows \\ Memory. DMP"</span><span class="sxs-lookup"><span data-stu-id="f56ae-150">Example: "C:\\Windows\\Memory.dmp"</span></span>

</dd> <dt>

<span data-ttu-id="f56ae-151">**ExpandedMiniDumpDirectory**</span><span class="sxs-lookup"><span data-stu-id="f56ae-151">**ExpandedMiniDumpDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56ae-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f56ae-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-153">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f56ae-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f56ae-154">Versión expandida de la propiedad **MiniDumpDirectory** .</span><span class="sxs-lookup"><span data-stu-id="f56ae-154">Expanded version of the **MiniDumpDirectory** property.</span></span>

<span data-ttu-id="f56ae-155">Ejemplo: "C: \\ minivolcado de Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="f56ae-155">Example: "C:\\Windows\\MiniDump"</span></span>

</dd> <dt>

<span data-ttu-id="f56ae-156">**KernelDumpOnly**</span><span class="sxs-lookup"><span data-stu-id="f56ae-156">**KernelDumpOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56ae-157">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f56ae-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-158">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f56ae-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-159">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ CrashControl \| KernelDumpOnly")</span><span class="sxs-lookup"><span data-stu-id="f56ae-159">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|KernelDumpOnly")</span></span>
</dt> </dl>

<span data-ttu-id="f56ae-160">Solo la información de depuración del kernel se escribirá en el archivo de registro de depuración.</span><span class="sxs-lookup"><span data-stu-id="f56ae-160">Only kernel debug information will be written to the debug log file.</span></span> <span data-ttu-id="f56ae-161">Si es **true**, solo el estado del kernel se escribe en un archivo en caso de que se produzca un error del sistema.</span><span class="sxs-lookup"><span data-stu-id="f56ae-161">If **TRUE**, then only the state of the kernel is written to a file in the event of a system failure.</span></span> <span data-ttu-id="f56ae-162">Si **es false**, el sistema intentará registrar el estado de la memoria y los dispositivos que puedan proporcionar información sobre el sistema cuando se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="f56ae-162">If **FALSE**, the system will try to log the state of the memory, and any devices that can provide information about the system when it failed.</span></span>

</dd> <dt>

<span data-ttu-id="f56ae-163">**MiniDumpDirectory**</span><span class="sxs-lookup"><span data-stu-id="f56ae-163">**MiniDumpDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56ae-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f56ae-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f56ae-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-166">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ CrashControl \| MiniDumpDir")</span><span class="sxs-lookup"><span data-stu-id="f56ae-166">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|MiniDumpDir")</span></span>
</dt> </dl>

<span data-ttu-id="f56ae-167">Directorio en el que se registrarán y acumularán pequeños archivos de volcado de memoria.</span><span class="sxs-lookup"><span data-stu-id="f56ae-167">Directory where small memory dump files will be recorded and accumulated.</span></span>

<span data-ttu-id="f56ae-168">Ejemplo: "% systemRoot% \\ minivolcado"</span><span class="sxs-lookup"><span data-stu-id="f56ae-168">Example: "%systemRoot%\\MiniDump"</span></span>

</dd> <dt>

<span data-ttu-id="f56ae-169">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f56ae-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56ae-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f56ae-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f56ae-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-172">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="f56ae-172">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="f56ae-173">Nombre de identificación para esta instancia de la clase **\_ OSRecoveryConfiguration de Win32** .</span><span class="sxs-lookup"><span data-stu-id="f56ae-173">Identifying name for this instance of the **Win32\_OSRecoveryConfiguration** class.</span></span>

</dd> <dt>

<span data-ttu-id="f56ae-174">**OverwriteExistingDebugFile**</span><span class="sxs-lookup"><span data-stu-id="f56ae-174">**OverwriteExistingDebugFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56ae-175">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f56ae-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-176">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f56ae-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-177">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ CrashControl \| Overwrite")</span><span class="sxs-lookup"><span data-stu-id="f56ae-177">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|Overwrite")</span></span>
</dt> </dl>

<span data-ttu-id="f56ae-178">El nuevo archivo de depuración sobrescribirá una existente.</span><span class="sxs-lookup"><span data-stu-id="f56ae-178">New debug file will overwrite an existing one.</span></span>

</dd> <dt>

<span data-ttu-id="f56ae-179">**SendAdminAlert**</span><span class="sxs-lookup"><span data-stu-id="f56ae-179">**SendAdminAlert**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56ae-180">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f56ae-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f56ae-181">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-182">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ CrashControl \| SendAlert")</span><span class="sxs-lookup"><span data-stu-id="f56ae-182">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|SendAlert")</span></span>
</dt> </dl>

<span data-ttu-id="f56ae-183">El mensaje de alerta se enviará al administrador del sistema en caso de que se produzca un error del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f56ae-183">Alert message will be sent to the system administrator in the event of an operating system failure.</span></span>

</dd> <dt>

<span data-ttu-id="f56ae-184">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="f56ae-184">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56ae-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f56ae-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f56ae-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-187">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="f56ae-187">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f56ae-188">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="f56ae-188">Identifier by which the current object is known.</span></span>

<span data-ttu-id="f56ae-189">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="f56ae-189">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="f56ae-190">**WriteDebugInfo**</span><span class="sxs-lookup"><span data-stu-id="f56ae-190">**WriteDebugInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56ae-191">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f56ae-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-192">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f56ae-192">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-193">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ CrashControl \| CrashDumpEnabled")</span><span class="sxs-lookup"><span data-stu-id="f56ae-193">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|CrashDumpEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="f56ae-194">La información de depuración se escribirá en un archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="f56ae-194">Debugging information is to be written to a log file.</span></span>

</dd> <dt>

<span data-ttu-id="f56ae-195">**WriteToSystemLog**</span><span class="sxs-lookup"><span data-stu-id="f56ae-195">**WriteToSystemLog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56ae-196">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f56ae-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-197">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f56ae-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f56ae-198">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ CrashControl \| LogEvent")</span><span class="sxs-lookup"><span data-stu-id="f56ae-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|LogEvent")</span></span>
</dt> </dl>

<span data-ttu-id="f56ae-199">Los eventos se escribirán en un registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="f56ae-199">Events will be written to a system log.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f56ae-200">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f56ae-200">Remarks</span></span>

<span data-ttu-id="f56ae-201">La **clase \_ OSRecoveryConfiguration de Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="f56ae-201">The **Win32\_OSRecoveryConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f56ae-202">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f56ae-202">Requirements</span></span>



| <span data-ttu-id="f56ae-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="f56ae-203">Requirement</span></span> | <span data-ttu-id="f56ae-204">Value</span><span class="sxs-lookup"><span data-stu-id="f56ae-204">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f56ae-205">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f56ae-205">Minimum supported client</span></span><br/> | <span data-ttu-id="f56ae-206">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f56ae-206">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f56ae-207">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f56ae-207">Minimum supported server</span></span><br/> | <span data-ttu-id="f56ae-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f56ae-208">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f56ae-209">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f56ae-209">Namespace</span></span><br/>                | <span data-ttu-id="f56ae-210">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f56ae-210">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f56ae-211">MOF</span><span class="sxs-lookup"><span data-stu-id="f56ae-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f56ae-212"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f56ae-212"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f56ae-213">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f56ae-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f56ae-214"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f56ae-214"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f56ae-215">Vea también</span><span class="sxs-lookup"><span data-stu-id="f56ae-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f56ae-216">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f56ae-216">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="f56ae-217">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f56ae-217">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
