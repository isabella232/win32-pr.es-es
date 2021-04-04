---
description: La \_ clase WMI WMISetting singleton de Win32 contiene los parámetros operativos para el servicio WMI. Esta clase solo puede tener una instancia, que siempre existe para cada sistema de Windows y no se puede eliminar. No se pueden crear instancias adicionales.
ms.assetid: d33cd4f3-969b-46ce-baff-466f1a464906
ms.tgt_platform: multiple
title: Win32_WMISetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMISetting
- Win32_WMISetting.Caption
- Win32_WMISetting.Description
- Win32_WMISetting.SettingID
- Win32_WMISetting.ASPScriptDefaultNamespace
- Win32_WMISetting.ASPScriptEnabled
- Win32_WMISetting.AutorecoverMofs
- Win32_WMISetting.AutoStartWin9X
- Win32_WMISetting.BackupInterval
- Win32_WMISetting.BackupLastTime
- Win32_WMISetting.BuildVersion
- Win32_WMISetting.DatabaseDirectory
- Win32_WMISetting.DatabaseMaxSize
- Win32_WMISetting.EnableAnonWin9xConnections
- Win32_WMISetting.EnableEvents
- Win32_WMISetting.EnableStartupHeapPreallocation
- Win32_WMISetting.HighThresholdOnClientObjects
- Win32_WMISetting.HighThresholdOnEvents
- Win32_WMISetting.InstallationDirectory
- Win32_WMISetting.LastStartupHeapPreallocation
- Win32_WMISetting.LoggingDirectory
- Win32_WMISetting.LoggingLevel
- Win32_WMISetting.LowThresholdOnClientObjects
- Win32_WMISetting.LowThresholdOnEvents
- Win32_WMISetting.MaxLogFileSize
- Win32_WMISetting.MaxWaitOnClientObjects
- Win32_WMISetting.MaxWaitOnEvents
- Win32_WMISetting.MofSelfInstallDirectory
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 8f94524d18074e3a35c7bcad09e9b9fba80e8470
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907007"
---
# <a name="win32_wmisetting-class"></a><span data-ttu-id="0345f-105">\_Clase Win32 WMISetting</span><span class="sxs-lookup"><span data-stu-id="0345f-105">Win32\_WMISetting class</span></span>

<span data-ttu-id="0345f-106">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ WMISetting** singleton de Win32 contiene los parámetros operativos para el servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-106">The **Win32\_WMISetting** singleton [WMI class](../wmisdk/retrieving-a-class.md) contains the operational parameters for the WMI service.</span></span> <span data-ttu-id="0345f-107">Esta clase solo puede tener una instancia, que siempre existe para cada sistema de Windows y no se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="0345f-107">This class can only have one instance, which always exists for each Windows system and cannot be deleted.</span></span> <span data-ttu-id="0345f-108">No se pueden crear instancias adicionales.</span><span class="sxs-lookup"><span data-stu-id="0345f-108">Additional instances cannot be created.</span></span>

<span data-ttu-id="0345f-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0345f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0345f-110">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="0345f-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0345f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0345f-111">Syntax</span></span>

``` syntax
[Singleton, Dynamic, Provider("WBEMCORE"), UUID("{A83EF166-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMISetting : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  string   ASPScriptDefaultNamespace = "\\\\root\\cimv2";
  boolean  ASPScriptEnabled;
  string   AutorecoverMofs[];
  uint32   AutoStartWin9X;
  uint32   BackupInterval;
  datetime BackupLastTime;
  string   BuildVersion;
  string   DatabaseDirectory;
  uint32   DatabaseMaxSize;
  boolean  EnableAnonWin9xConnections;
  boolean  EnableEvents;
  boolean  EnableStartupHeapPreallocation;
  uint32   HighThresholdOnClientObjects;
  uint32   HighThresholdOnEvents;
  string   InstallationDirectory;
  uint32   LastStartupHeapPreallocation;
  string   LoggingDirectory;
  uint32   LoggingLevel;
  uint32   LowThresholdOnClientObjects;
  uint32   LowThresholdOnEvents;
  uint32   MaxLogFileSize;
  uint32   MaxWaitOnClientObjects;
  uint32   MaxWaitOnEvents;
  string   MofSelfInstallDirectory;
};
```

## <a name="members"></a><span data-ttu-id="0345f-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="0345f-112">Members</span></span>

<span data-ttu-id="0345f-113">La **clase \_ WMISetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0345f-113">The **Win32\_WMISetting** class has these types of members:</span></span>

-   [<span data-ttu-id="0345f-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0345f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0345f-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0345f-115">Properties</span></span>

<span data-ttu-id="0345f-116">La **clase \_ WMISetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0345f-116">The **Win32\_WMISetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0345f-117">**ASPScriptDefaultNamespace**</span><span class="sxs-lookup"><span data-stu-id="0345f-117">**ASPScriptDefaultNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0345f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-120">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ scripting \| default namespace")</span><span class="sxs-lookup"><span data-stu-id="0345f-120">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\scripting\|Default Namespace")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-121">Espacio de nombres de script predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0345f-121">Default script namespace.</span></span> <span data-ttu-id="0345f-122">Esta propiedad contiene el espacio de nombres utilizado por las llamadas de la API de scripting para WMI si no se especifica ninguno en el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="0345f-122">This property contains the namespace used by calls from the Scripting API for WMI if none is specified by the caller.</span></span>

<span data-ttu-id="0345f-123">Esta propiedad refleja el valor de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="0345f-123">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="0345f-124">**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **scripting \| default namespace**    </span><span class="sxs-lookup"><span data-stu-id="0345f-124">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **scripting\|Default Namespace**</span></span>

<span data-ttu-id="0345f-125">Ejemplo: raíz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0345f-125">Example: root\\cimv2</span></span>

<span data-ttu-id="0345f-126">Para ver un script de ejemplo que usa esta propiedad, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="0345f-126">For an example script that uses this property, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="0345f-127">**ASPScriptEnabled**</span><span class="sxs-lookup"><span data-stu-id="0345f-127">**ASPScriptEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0345f-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-130">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ scripting \| enable for ASP")</span><span class="sxs-lookup"><span data-stu-id="0345f-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\scripting\|Enable for ASP")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-131">Si **es true**, el scripting de WMI puede usarse en páginas de Active Server (ASP).</span><span class="sxs-lookup"><span data-stu-id="0345f-131">If **True**, WMI scripting can be used on Active Server Pages (ASP).</span></span> <span data-ttu-id="0345f-132">Esta propiedad es válida en sistemas que solo ejecutan versiones no compatibles de Windows.</span><span class="sxs-lookup"><span data-stu-id="0345f-132">This property is valid on systems running unsupported versions of Windows only.</span></span> <span data-ttu-id="0345f-133">En el caso de los sistemas Windows compatibles, el scripting de WMI siempre se permite en ASP.</span><span class="sxs-lookup"><span data-stu-id="0345f-133">For supported Windows systems, WMI scripting is always allowed on ASP.</span></span>

</dd> <dt>

<span data-ttu-id="0345f-134">**AutorecoverMofs**</span><span class="sxs-lookup"><span data-stu-id="0345f-134">**AutorecoverMofs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-135">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="0345f-135">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0345f-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0345f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0345f-137">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software Win32Registry \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| autocover MOF")</span><span class="sxs-lookup"><span data-stu-id="0345f-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Autorecover MOFs")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-138">Lista de nombres de archivo MOF completos que se usan para inicializar o recuperar el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-138">List of fully qualified MOF file names used to initialize or recover the WMI repository.</span></span> <span data-ttu-id="0345f-139">La lista determina el orden en que se compilan los archivos MOF.</span><span class="sxs-lookup"><span data-stu-id="0345f-139">The list determines the order in which MOF files are compiled.</span></span>

<span data-ttu-id="0345f-140">Esta propiedad refleja el valor de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="0345f-140">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="0345f-141">**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| autocover MOF**    </span><span class="sxs-lookup"><span data-stu-id="0345f-141">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|Autorecover MOFs**</span></span>

</dd> <dt>

<span data-ttu-id="0345f-142">**AutoStartWin9X**</span><span class="sxs-lookup"><span data-stu-id="0345f-142">**AutoStartWin9X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-143">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0345f-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-145">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X")</span><span class="sxs-lookup"><span data-stu-id="0345f-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|AutostartWin9X")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-146">No se admite.</span><span class="sxs-lookup"><span data-stu-id="0345f-146">Not supported.</span></span>

<dt>

<span id="Don_t_start"></span><span id="don_t_start"></span><span id="DON_T_START"></span>

<span data-ttu-id="0345f-147">**No iniciar** (0)</span><span class="sxs-lookup"><span data-stu-id="0345f-147">**Don't start** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Autostart"></span><span id="autostart"></span><span id="AUTOSTART"></span>

<span data-ttu-id="0345f-148">**Inicio automático** (1)</span><span class="sxs-lookup"><span data-stu-id="0345f-148">**Autostart** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_on_reboot"></span><span id="start_on_reboot"></span><span id="START_ON_REBOOT"></span>

<span data-ttu-id="0345f-149">**Iniciar al reiniciar** (2)</span><span class="sxs-lookup"><span data-stu-id="0345f-149">**Start on reboot** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0345f-150">**BackupInterval**</span><span class="sxs-lookup"><span data-stu-id="0345f-150">**BackupInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-151">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0345f-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-152">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-153">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Backup Interval Threshold"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span><span class="sxs-lookup"><span data-stu-id="0345f-153">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Backup Interval Threshold"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-154">No se admite.</span><span class="sxs-lookup"><span data-stu-id="0345f-154">Not supported.</span></span> <span data-ttu-id="0345f-155">En su lugar, realice una copia de seguridad manual del repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-155">Instead, backup the WMI repository manually.</span></span>

</dd> <dt>

<span data-ttu-id="0345f-156">**BackupLastTime**</span><span class="sxs-lookup"><span data-stu-id="0345f-156">**BackupLastTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-157">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0345f-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-158">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-159">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Time Functions \| GetTimeZoneInformation")</span><span class="sxs-lookup"><span data-stu-id="0345f-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Functions\|GetTimeZoneInformation")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-160">Fecha y hora en que se realizó la última copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0345f-160">Date and time the last backup was performed.</span></span>

</dd> <dt>

<span data-ttu-id="0345f-161">**BuildVersion**</span><span class="sxs-lookup"><span data-stu-id="0345f-161">**BuildVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0345f-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0345f-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0345f-164">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \| Build")</span><span class="sxs-lookup"><span data-stu-id="0345f-164">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|Build")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-165">Información de versión para el servicio WMI instalado actualmente.</span><span class="sxs-lookup"><span data-stu-id="0345f-165">Version information for the currently installed WMI service.</span></span>

<span data-ttu-id="0345f-166">Período de tiempo que transcurre entre las copias de seguridad de la base de datos WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-166">Length of time that elapses between backups of the WMI database.</span></span>

<span data-ttu-id="0345f-167">Esta propiedad refleja el valor de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="0345f-167">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="0345f-168">**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM \| Build**</span><span class="sxs-lookup"><span data-stu-id="0345f-168">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|Build**</span></span>

</dd> <dt>

<span data-ttu-id="0345f-169">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0345f-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0345f-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0345f-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0345f-172">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0345f-172">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0345f-173">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="0345f-173">Short textual description of the current object.</span></span>

<span data-ttu-id="0345f-174">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0345f-174">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="0345f-175">**DatabaseDirectory**</span><span class="sxs-lookup"><span data-stu-id="0345f-175">**DatabaseDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0345f-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0345f-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0345f-178">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| repository Directory")</span><span class="sxs-lookup"><span data-stu-id="0345f-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Repository Directory")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-179">Ruta de acceso al directorio que contiene el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-179">Directory path that contains the WMI repository.</span></span>

</dd> <dt>

<span data-ttu-id="0345f-180">**DatabaseMaxSize**</span><span class="sxs-lookup"><span data-stu-id="0345f-180">**DatabaseMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-181">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0345f-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0345f-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0345f-183">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("software de Win32Registry \| \\ \\ \\ \\ de Microsoft WBEM \\ \\ CIMOM \| Max dB size"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="0345f-183">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max DB Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-184">Tamaño máximo del repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-184">Maximum size of the WMI repository.</span></span>

</dd> <dt>

<span data-ttu-id="0345f-185">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0345f-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0345f-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0345f-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0345f-188">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="0345f-188">Textual description of the current object.</span></span>

<span data-ttu-id="0345f-189">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0345f-189">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="0345f-190">**EnableAnonWin9xConnections**</span><span class="sxs-lookup"><span data-stu-id="0345f-190">**EnableAnonWin9xConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-191">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0345f-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-192">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-192">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-193">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableAnonConnections")</span><span class="sxs-lookup"><span data-stu-id="0345f-193">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableAnonConnections")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-194">No se admite.</span><span class="sxs-lookup"><span data-stu-id="0345f-194">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0345f-195">**EnableEvents**</span><span class="sxs-lookup"><span data-stu-id="0345f-195">**EnableEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-196">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0345f-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-197">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-198">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software Win32Registry \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableEvents")</span><span class="sxs-lookup"><span data-stu-id="0345f-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableEvents")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-199">Si **es true**, el subsistema de eventos WMI debe estar habilitado.</span><span class="sxs-lookup"><span data-stu-id="0345f-199">If **True**, the WMI event subsystem should be enabled.</span></span>

<span data-ttu-id="0345f-200">Esta propiedad refleja el valor de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="0345f-200">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="0345f-201">**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**</span><span class="sxs-lookup"><span data-stu-id="0345f-201">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|EnableEvents**</span></span>

</dd> <dt>

<span data-ttu-id="0345f-202">**EnableStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="0345f-202">**EnableStartupHeapPreallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-203">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0345f-203">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-204">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-204">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-205">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableStartupHeapPreallocation")</span><span class="sxs-lookup"><span data-stu-id="0345f-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableStartupHeapPreallocation")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-206">Si **es true**, WMI crea un montón previamente asignado con el tamaño del valor de **LastStartupHeapPreallocation** cuando se inicializa WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-206">If **True**, WMI creates a pre-allocated heap with the size of the **LastStartupHeapPreallocation** value when WMI is initialized.</span></span>

</dd> <dt>

<span data-ttu-id="0345f-207">**HighThresholdOnClientObjects**</span><span class="sxs-lookup"><span data-stu-id="0345f-207">**HighThresholdOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-208">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0345f-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-209">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-210">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software Win32Registry \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| High threshold en objetos de cliente"), [**unidades**](../wmisdk/standard-qualifiers.md) ("objetos por segundo")</span><span class="sxs-lookup"><span data-stu-id="0345f-210">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|High Threshold On Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-211">Velocidad máxima a la que los objetos creados por el proveedor se pueden entregar a los clientes.</span><span class="sxs-lookup"><span data-stu-id="0345f-211">Maximum rate at which provider-created objects can be delivered to clients.</span></span> <span data-ttu-id="0345f-212">Para acomodar las diferencias de velocidad entre proveedores y clientes, WMI mantiene los objetos en las colas antes de entregarlos a los consumidores.</span><span class="sxs-lookup"><span data-stu-id="0345f-212">To accommodate speed differentials between providers and clients, WMI holds objects in queues before delivering them to consumers.</span></span> <span data-ttu-id="0345f-213">Para mayor eficacia, los consumidores deben recopilar los objetos a un ritmo que coincida con el proveedor.</span><span class="sxs-lookup"><span data-stu-id="0345f-213">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="0345f-214">Si la memoria mantenida por los objetos no recopilados alcanza el **LowThresholdOnObjects**, WMI ralentiza la adición de nuevos objetos a la cola.</span><span class="sxs-lookup"><span data-stu-id="0345f-214">If the memory held by uncollected objects reaches **LowThresholdOnObjects**, then WMI slows down the addition of new objects into the queue.</span></span> <span data-ttu-id="0345f-215">Si los eventos no recopilados continúan acumulados y se alcanza la espera máxima para la entrega de eventos en **MaxWaitOnClientObjects** mientras la memoria usada está en el valor de **HighThresholdOnClientObjects**, WMI no acepta más objetos de proveedores y **devuelve \_ WBEM \_ e \_ \_ memoria insuficiente** a los clientes.</span><span class="sxs-lookup"><span data-stu-id="0345f-215">If uncollected events continue to accumulate and the maximum wait to deliver events in **MaxWaitOnClientObjects** is reached while the memory used is at the value in **HighThresholdOnClientObjects**, then WMI accepts no more objects from providers and returns **WBEM\_E\_OUT\_OF\_MEMORY** to the clients.</span></span>

</dd> <dt>

<span data-ttu-id="0345f-216">**HighThresholdOnEvents**</span><span class="sxs-lookup"><span data-stu-id="0345f-216">**HighThresholdOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-217">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0345f-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-218">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-218">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-219">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software Win32Registry \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| High Threshold on Events"), [**unidades**](../wmisdk/standard-qualifiers.md) ("eventos por segundo")</span><span class="sxs-lookup"><span data-stu-id="0345f-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|High Threshold On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("events per second")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-220">Velocidad máxima a la que se entregan los eventos a los clientes.</span><span class="sxs-lookup"><span data-stu-id="0345f-220">Maximum rate at which events are to be delivered to clients.</span></span> <span data-ttu-id="0345f-221">Para acomodar las diferencias de velocidad entre proveedores y clientes, WMI pone en cola los eventos antes de entregarlos a los consumidores.</span><span class="sxs-lookup"><span data-stu-id="0345f-221">To accommodate speed differentials between providers and clients, WMI queues events before delivering them to consumers.</span></span> <span data-ttu-id="0345f-222">Para mayor eficacia, los consumidores deben recopilar los eventos a un ritmo que coincida con el proveedor.</span><span class="sxs-lookup"><span data-stu-id="0345f-222">For more efficiency, consumers must collect the events at a pace that matches the provider.</span></span> <span data-ttu-id="0345f-223">Si la memoria mantenida por los eventos no recopilados alcanza **LowThresholdOnObjects**, WMI ralentiza la adición de nuevos eventos a la cola.</span><span class="sxs-lookup"><span data-stu-id="0345f-223">If the memory held by uncollected events reaches **LowThresholdOnObjects**, then WMI slows down the addition of new events into the queue.</span></span> <span data-ttu-id="0345f-224">Si los eventos no recopilados continúan acumulados y se alcanza la espera máxima de entrega de eventos en **MaxWaitOnEvents** mientras la memoria usada está en el valor de **HighThresholdOnEvents**, WMI no acepta más eventos de los proveedores y devuelve **WBEM \_ e \_ \_ \_ memoria insuficiente** a los clientes.</span><span class="sxs-lookup"><span data-stu-id="0345f-224">If uncollected events continue to accumulate and the maximum wait to deliver events in **MaxWaitOnEvents** is reached while the memory used is at the value in **HighThresholdOnEvents**, WMI accepts no more events from providers and returns **WBEM\_E\_OUT\_OF\_MEMORY** to the clients.</span></span>

> [!Note]  
> <span data-ttu-id="0345f-225">La limitación solo se realiza para los consumidores de eventos permanentes, por lo que los consumidores temporales no deberían esperar la limitación cuando se realiza una copia de seguridad de eventos en la cola de eventos internos de WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-225">Throttling is only done for Permanent Event consumers, so temporary consumers should not expect throttling when events get backed up in the WMI internal event queue.</span></span>

 

<span data-ttu-id="0345f-226">Esta propiedad refleja el valor de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="0345f-226">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="0345f-227">**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| alto umbral en objetos de cliente (B)**    </span><span class="sxs-lookup"><span data-stu-id="0345f-227">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects (B)**</span></span>

</dd> <dt>

<span data-ttu-id="0345f-228">**InstallationDirectory**</span><span class="sxs-lookup"><span data-stu-id="0345f-228">**InstallationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-229">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0345f-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0345f-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0345f-231">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \| Installation Directory")</span><span class="sxs-lookup"><span data-stu-id="0345f-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|Installation Directory")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-232">Ruta de acceso al directorio donde se ha instalado el software WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-232">Directory path where the WMI software has been installed.</span></span> <span data-ttu-id="0345f-233">La ubicación predeterminada es \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="0345f-233">The default location is \\System32\\Wbem.</span></span>

<span data-ttu-id="0345f-234">Esta propiedad refleja el valor de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="0345f-234">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="0345f-235">**HKEY \_ Software de \_ equipo local** \\  \\ Directorio de instalación de **Microsoft** \\ **WBEM \|**</span><span class="sxs-lookup"><span data-stu-id="0345f-235">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|Installation Directory**</span></span>

</dd> <dt>

<span data-ttu-id="0345f-236">**LastStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="0345f-236">**LastStartupHeapPreallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-237">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0345f-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0345f-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0345f-239">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| LastStartupHeapPreallocation"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="0345f-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|LastStartupHeapPreallocation"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-240">Tamaño del montón asignado previamente creado por WMI durante la inicialización.</span><span class="sxs-lookup"><span data-stu-id="0345f-240">Size of the pre-allocated heap created by WMI during initialization.</span></span>

<span data-ttu-id="0345f-241">Esta propiedad refleja el valor de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="0345f-241">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="0345f-242">**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| LastStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="0345f-242">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|LastStartupHeapPreallocation**</span></span>

</dd> <dt>

<span data-ttu-id="0345f-243">**LoggingDirectory**</span><span class="sxs-lookup"><span data-stu-id="0345f-243">**LoggingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-244">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0345f-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-245">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-245">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-246">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Logging Directory")</span><span class="sxs-lookup"><span data-stu-id="0345f-246">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Logging Directory")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-247">Ruta de acceso al directorio que contiene la ubicación de los archivos de registro del sistema WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-247">Directory path that contains the location of the WMI system log files.</span></span>

<span data-ttu-id="0345f-248">Esta propiedad refleja el valor de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="0345f-248">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="0345f-249">**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| Logging Directory**</span><span class="sxs-lookup"><span data-stu-id="0345f-249">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Logging Directory**</span></span>

</dd> <dt>

<span data-ttu-id="0345f-250">**LoggingLevel**</span><span class="sxs-lookup"><span data-stu-id="0345f-250">**LoggingLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-251">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0345f-251">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-252">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-252">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-253">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("software Win32Registry de \| \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| logging")</span><span class="sxs-lookup"><span data-stu-id="0345f-253">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Logging")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-254">Habilitación del registro de eventos y el nivel de detalle del registro utilizado.</span><span class="sxs-lookup"><span data-stu-id="0345f-254">Enabling of event logging and the verbosity level of logging used.</span></span>

<span data-ttu-id="0345f-255">Esta propiedad refleja el valor de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="0345f-255">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="0345f-256">**HKEY \_ Software de \_ equipo local** \\  \\  \\ **\| \| registro CIMOM** de Microsoft WBEM</span><span class="sxs-lookup"><span data-stu-id="0345f-256">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Logging**</span></span>

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="0345f-257">**Desactivado** (0)</span><span class="sxs-lookup"><span data-stu-id="0345f-257">**Off** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Error_logging"></span><span id="error_logging"></span><span id="ERROR_LOGGING"></span>

<span data-ttu-id="0345f-258">**Registro de errores** (1)</span><span class="sxs-lookup"><span data-stu-id="0345f-258">**Error logging** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Verbose_Error_logging"></span><span id="verbose_error_logging"></span><span id="VERBOSE_ERROR_LOGGING"></span>

<span data-ttu-id="0345f-259">**Registro de errores detallado** (2)</span><span class="sxs-lookup"><span data-stu-id="0345f-259">**Verbose Error logging** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0345f-260">**LowThresholdOnClientObjects**</span><span class="sxs-lookup"><span data-stu-id="0345f-260">**LowThresholdOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-261">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0345f-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-262">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-262">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-263">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software Win32Registry \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Low threshold en objetos de cliente"), [**unidades**](../wmisdk/standard-qualifiers.md) ("objetos por segundo")</span><span class="sxs-lookup"><span data-stu-id="0345f-263">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Low Threshold On Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-264">Velocidad a la que WMI comienza a ralentizar la creación de nuevos objetos creados para clientes.</span><span class="sxs-lookup"><span data-stu-id="0345f-264">Rate at which WMI starts to slow the creation of new objects created for clients.</span></span> <span data-ttu-id="0345f-265">Para acomodar las diferencias de velocidad entre proveedores y clientes, WMI mantiene los objetos en las colas antes de entregarlos a los consumidores.</span><span class="sxs-lookup"><span data-stu-id="0345f-265">To accommodate speed differentials between providers and clients, WMI holds objects in queues before delivering them to consumers.</span></span> <span data-ttu-id="0345f-266">Para mayor eficacia, los consumidores deben recopilar los objetos a un ritmo que coincida con el proveedor.</span><span class="sxs-lookup"><span data-stu-id="0345f-266">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="0345f-267">Si la tasa de solicitudes de objetos alcanza **LowThresholdOnClientObjects**, WMI reduce gradualmente la creación de objetos nuevos para que coincidan con la tasa de uso del cliente.</span><span class="sxs-lookup"><span data-stu-id="0345f-267">If the rate of requests for objects reaches **LowThresholdOnClientObjects**, then WMI gradually slows down the creation of new objects to match the client's rate of use.</span></span> <span data-ttu-id="0345f-268">Esta ralentización se inicia cuando la velocidad a la que se crean los objetos supera el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0345f-268">This slowdown starts when the rate at which objects are being created exceeds the value of this property.</span></span> <span data-ttu-id="0345f-269">Vea **HighThresholdOnClientObjects**.</span><span class="sxs-lookup"><span data-stu-id="0345f-269">See **HighThresholdOnClientObjects**.</span></span>

<span data-ttu-id="0345f-270">Esta propiedad refleja el valor del registro.</span><span class="sxs-lookup"><span data-stu-id="0345f-270">This property reflects the registry value.</span></span>

<span data-ttu-id="0345f-271">**Clave \_ de Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| alto umbral en objetos de cliente (B)**    </span><span class="sxs-lookup"><span data-stu-id="0345f-271">**KEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects (B)**</span></span>

</dd> <dt>

<span data-ttu-id="0345f-272">**LowThresholdOnEvents**</span><span class="sxs-lookup"><span data-stu-id="0345f-272">**LowThresholdOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-273">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0345f-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-274">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-274">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-275">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software \\ \\ de Win32Registry \\ \\ de Microsoft WBEM \\ \\ CIMOM \| Low Threshold on Events"), [**unidades**](../wmisdk/standard-qualifiers.md) ("eventos por segundo")</span><span class="sxs-lookup"><span data-stu-id="0345f-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Low Threshold On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("events per second")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-276">Velocidad a la que WMI comienza a ralentizar la entrega de eventos nuevos.</span><span class="sxs-lookup"><span data-stu-id="0345f-276">Rate at which WMI starts to slow the delivery of new events.</span></span> <span data-ttu-id="0345f-277">Para acomodar las diferencias de velocidad entre proveedores y clientes, WMI pone en cola los eventos antes de entregarlos a los consumidores.</span><span class="sxs-lookup"><span data-stu-id="0345f-277">To accommodate speed differentials between providers and clients, WMI queues events before delivering them to consumers.</span></span> <span data-ttu-id="0345f-278">Para mayor eficacia, los consumidores deben recopilar los objetos a un ritmo que coincida con el proveedor.</span><span class="sxs-lookup"><span data-stu-id="0345f-278">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="0345f-279">Si la cola crece fuera del control, se reduce el nivel de rendimiento de WMI, lo que reduce la velocidad de los eventos para alinearlos con la tasa de clientes.</span><span class="sxs-lookup"><span data-stu-id="0345f-279">If the queue grows out of control, WMI throttles—slows down—the delivery of events gradually to align with the client rate.</span></span> <span data-ttu-id="0345f-280">Esta ralentización se inicia cuando la velocidad a la que se generan los eventos supera el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0345f-280">This slowdown starts when the rate at which events are generated exceeds the value of this property.</span></span> <span data-ttu-id="0345f-281">Vea **HighThresholdOnEvents**.</span><span class="sxs-lookup"><span data-stu-id="0345f-281">See **HighThresholdOnEvents**.</span></span>

> [!Note]  
> <span data-ttu-id="0345f-282">La limitación solo se realiza para los consumidores de eventos permanentes, por lo que los consumidores temporales no deberían esperar la limitación cuando se realiza una copia de seguridad de eventos en la cola de eventos internos de WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-282">Throttling is only done for permanent event consumers, so temporary consumers should not expect throttling when events get backed up in the WMI internal event queue.</span></span>

 

<span data-ttu-id="0345f-283">Esta propiedad refleja el valor del registro.</span><span class="sxs-lookup"><span data-stu-id="0345f-283">This property reflects the registry value.</span></span>

<span data-ttu-id="0345f-284">**HKEY \_ Software de \_ máquina local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| alto umbral en objetos de cliente {B}**    </span><span class="sxs-lookup"><span data-stu-id="0345f-284">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects {B}**</span></span>

</dd> <dt>

<span data-ttu-id="0345f-285">**MaxLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="0345f-285">**MaxLogFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-286">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0345f-286">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-287">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-287">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-288">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Log File size Max size"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="0345f-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Log File Max Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-289">Tamaño máximo de los archivos de registro generados por el servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-289">Maximum size of the log files produced by the WMI service.</span></span>

<span data-ttu-id="0345f-290">Esta propiedad refleja el valor de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="0345f-290">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="0345f-291">**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| tamaño máximo del archivo de registro**</span><span class="sxs-lookup"><span data-stu-id="0345f-291">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Log File Max Size**</span></span>

</dd> <dt>

<span data-ttu-id="0345f-292">**MaxWaitOnClientObjects**</span><span class="sxs-lookup"><span data-stu-id="0345f-292">**MaxWaitOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-293">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0345f-293">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-294">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-294">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-295">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software Win32Registry \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max wait on Events"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milisegundos")</span><span class="sxs-lookup"><span data-stu-id="0345f-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-296">Cantidad de tiempo que espera un objeto recién creado para que lo use el cliente antes de que se descarte y se devuelva un valor de error.</span><span class="sxs-lookup"><span data-stu-id="0345f-296">Amount of time a newly created object waits to be used by the client before it is discarded and an error value is returned.</span></span> <span data-ttu-id="0345f-297">Esta propiedad interactúa con las propiedades **LowThresholdOnClientObjects** y **HighThresholdOnClientObjects** para limitar, ralentizar, la entrega de objetos a los consumidores cuando el consumidor recibe los objetos demasiado lentamente.</span><span class="sxs-lookup"><span data-stu-id="0345f-297">This property interacts with the **LowThresholdOnClientObjects** and **HighThresholdOnClientObjects** properties to throttle—slow down—the delivery of objects to consumers when the consumer is receiving the objects too slowly.</span></span>

</dd> <dt>

<span data-ttu-id="0345f-298">**MaxWaitOnEvents**</span><span class="sxs-lookup"><span data-stu-id="0345f-298">**MaxWaitOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-299">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0345f-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-300">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0345f-300">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0345f-301">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software Win32Registry \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max wait on Events"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milisegundos")</span><span class="sxs-lookup"><span data-stu-id="0345f-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-302">Cantidad de tiempo durante el cual un evento enviado a un cliente se pone en cola antes de que se descarte.</span><span class="sxs-lookup"><span data-stu-id="0345f-302">Amount of time for which an event sent to a client is queued before being discarded.</span></span> <span data-ttu-id="0345f-303">Esta propiedad interacts0 con **LowThresholdOnEvents** y **HighThresholdOnEvents** para limitar (ralentizar) la entrega de objetos a los consumidores cuando el consumidor recibe los objetos demasiado lentamente.</span><span class="sxs-lookup"><span data-stu-id="0345f-303">This property interacts0 with **LowThresholdOnEvents** and **HighThresholdOnEvents** to throttle—slow down—the delivery of objects to consumers when the consumer is receiving the objects too slowly.</span></span>

<span data-ttu-id="0345f-304">Esta propiedad refleja el valor del registro.</span><span class="sxs-lookup"><span data-stu-id="0345f-304">This property reflects the registry value.</span></span>

<span data-ttu-id="0345f-305">**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| Max wait on Events (MS)**    </span><span class="sxs-lookup"><span data-stu-id="0345f-305">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|Max Wait On Events (ms)**</span></span>

</dd> <dt>

<span data-ttu-id="0345f-306">**MofSelfInstallDirectory**</span><span class="sxs-lookup"><span data-stu-id="0345f-306">**MofSelfInstallDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0345f-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0345f-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0345f-309">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \| MOF Self-Install Directory")</span><span class="sxs-lookup"><span data-stu-id="0345f-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|MOF Self-Install Directory")</span></span>
</dt> </dl>

<span data-ttu-id="0345f-310">Ruta de acceso del directorio para las aplicaciones que instalan archivos MOF en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-310">Directory path for applications that install MOF files to the WMI repository.</span></span> <span data-ttu-id="0345f-311">WMI compila automáticamente cualquier archivo MOF colocado en este directorio y, dependiendo de si se ha realizado correctamente, mueve el MOF a un subdirectorio con la etiqueta Good o Bad.</span><span class="sxs-lookup"><span data-stu-id="0345f-311">WMI automatically compiles any MOF files placed in this directory and, depending on its success, moves the MOF to a subdirectory labeled good or bad.</span></span> <span data-ttu-id="0345f-312">Si \# se incluye el comando [pragma autorecover](../wmisdk/pragma-autorecover.md) , se agrega el nombre de archivo completo a la lista **AutorecoverMofs** que se usa cuando WMI se inicializa o recupera el repositorio.</span><span class="sxs-lookup"><span data-stu-id="0345f-312">If the \# [pragma autorecover](../wmisdk/pragma-autorecover.md) command is included, the fully qualified file name is added to the **AutorecoverMofs** list used when WMI is initializing or recovering the repository.</span></span> <span data-ttu-id="0345f-313">La lista determina el orden en el que se compilan los MOF.</span><span class="sxs-lookup"><span data-stu-id="0345f-313">The list determines the order in which MOFs are compiled.</span></span>

<span data-ttu-id="0345f-314">Esta propiedad refleja el valor de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="0345f-314">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="0345f-315">**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| MOF Self = directorio de instalación**</span><span class="sxs-lookup"><span data-stu-id="0345f-315">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|MOF Self=Install Directory**</span></span>

</dd> <dt>

<span data-ttu-id="0345f-316">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="0345f-316">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0345f-317">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0345f-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0345f-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0345f-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0345f-319">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0345f-319">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0345f-320">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="0345f-320">Identifier by which the current object is known.</span></span>

<span data-ttu-id="0345f-321">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0345f-321">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0345f-322">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0345f-322">Remarks</span></span>

<span data-ttu-id="0345f-323">La **clase \_ WMISetting de Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0345f-323">The **Win32\_WMISetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span> <span data-ttu-id="0345f-324">Solo puede existir una instancia de esta clase en un equipo.</span><span class="sxs-lookup"><span data-stu-id="0345f-324">Only one instance of this class can exist on a computer.</span></span>

<span data-ttu-id="0345f-325">Saber cómo se configura WMI en un equipo puede ser muy útil al depurar scripts o solucionar problemas con el propio servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-325">Knowing how WMI is configured on a computer can be very useful when you are debugging scripts or troubleshooting problems with the WMI service itself.</span></span> <span data-ttu-id="0345f-326">Por ejemplo, muchos scripts de WMI se escriben bajo la suposición de que \\ la raíz cimv2 es el espacio de nombres predeterminado en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="0345f-326">For example, many WMI scripts are written under the assumption that root\\cimv2 is the default namespace on the target computer.</span></span> <span data-ttu-id="0345f-327">Como resultado, \\ a menudo no se puede incluir el espacio de nombres en el moniker GetObject, como se muestra en el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="0345f-327">As a result, script writers who need to access a class in "Root\\CIMv2" often fail to include the namespace in the GetObject moniker, as shown in the following code sample:</span></span>

`Set colServices = GetObject("winmgmts:").ExecQuery ("SELECT * FROM Win32_Service")`

<span data-ttu-id="0345f-328">Si \\ la raíz cimv2 no es el espacio de nombres predeterminado en el equipo de destino, se producirá un error en este script.</span><span class="sxs-lookup"><span data-stu-id="0345f-328">If root\\cimv2 is not the default namespace on the target computer, this script will fail.</span></span> <span data-ttu-id="0345f-329">Para evitar que esto suceda, el espacio de nombres root \\ cimv2 debe estar incluido en el moniker, tal y como se muestra en el siguiente ejemplo de código:</span><span class="sxs-lookup"><span data-stu-id="0345f-329">To prevent this from happening, the namespace root\\cimv2 must be included in the moniker, as shown in the following code sample:</span></span>

`Set colServices = GetObject("winmgmts:root\cimv2").ExecQuery("SELECT * FROM Win32_Service")`

<span data-ttu-id="0345f-330">Si el espacio de nombres predeterminado en el equipo de destino es diferente del espacio de nombres asumido por un script, se producirá un error en el script.</span><span class="sxs-lookup"><span data-stu-id="0345f-330">If the default namespace on the target computer is different from the namespace assumed by a script, the script will fail.</span></span> <span data-ttu-id="0345f-331">Además de eso, se presentará al usuario el mensaje de error algo engañoso "clase no válida".</span><span class="sxs-lookup"><span data-stu-id="0345f-331">On top of that, the user will be presented with the somewhat misleading error message "Invalid class."</span></span> <span data-ttu-id="0345f-332">En realidad, el error no se debe a que la clase no es válida, pero no se encuentra la clase en el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0345f-332">In truth, the failure is not because the class is invalid but because the class cannot be found in the default namespace.</span></span> <span data-ttu-id="0345f-333">Se trata de un problema difícil de solucionar, porque es probable que investigue los posibles problemas con la clase en lugar de problemas con el espacio de nombres que se especificó (o, en este caso, no).</span><span class="sxs-lookup"><span data-stu-id="0345f-333">This is a difficult problem to troubleshoot, because you are likely to investigate possible problems with the class rather than problems with the namespace that was (or, in this case, was not) specified.</span></span>

<span data-ttu-id="0345f-334">Puede usar la clase **Win32 \_ WMISetting** para determinar cómo se ha configurado WMI en un equipo.</span><span class="sxs-lookup"><span data-stu-id="0345f-334">You can use the **Win32\_WMISetting** class to determine how WMI has been configured on a computer.</span></span> <span data-ttu-id="0345f-335">Los detalles de configuración como el espacio de nombres predeterminado o el número de compilación de WMI pueden ser útiles para solucionar problemas de scripts.</span><span class="sxs-lookup"><span data-stu-id="0345f-335">Configuration details such as the default namespace or the WMI build number can be useful in troubleshooting script problems.</span></span> <span data-ttu-id="0345f-336">Estas opciones también proporcionan información administrativa importante, como el modo en que se registran los errores de WMI en un equipo y los proveedores de WMI que se volverán a cargar automáticamente si es necesario volver a generar el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-336">These settings also provide important administrative information such as how, or even whether, WMI errors are logged on a computer and which WMI providers will automatically be reloaded if you need to rebuild the WMI repository.</span></span>

## <a name="examples"></a><span data-ttu-id="0345f-337">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0345f-337">Examples</span></span>

<span data-ttu-id="0345f-338">En el ejemplo de código de VBScript [Modify WMI Settings](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) de la galería de TechNet se usa la clase **Win32 \_ WMISetting** para configurar el intervalo de copia de seguridad y el nivel de registro de WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-338">The [Modify WMI Settings](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript code example on the TechNet Gallery uses the **Win32\_WMISetting** class to configure the WMI backup interval and logging level.</span></span>

<span data-ttu-id="0345f-339">En el ejemplo de código VBScript [del espacio de nombres predeterminado](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) de la galería de TechNet se usa la clase **\_ WMISetting de Win32** para recuperar y mostrar el valor actual de "espacio de nombres predeterminado para scripting" de WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-339">The [List the Default Namespace](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) VBScript code example on the TechNet Gallery uses the **Win32\_WMISetting** class to retrieve and display the current WMI "Default namespace for scripting" setting.</span></span>

<span data-ttu-id="0345f-340">En el ejemplo de código de VBScript del [espacio de nombres WMI](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) de la galería de TechNet, se usa la propiedad **ASPScriptDefaultNamespace** para establecer el valor de "espacio de nombres predeterminado para scripting" en "root \\ cimv2".</span><span class="sxs-lookup"><span data-stu-id="0345f-340">The [Modify the Default WMI Namespace](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) VBScript code example on the TechNet Gallery uses the **ASPScriptDefaultNamespace** property to set the WMI "Default namespace for scripting" setting to "root\\cimv2".</span></span>

<span data-ttu-id="0345f-341">La [lista de todos los valores de WMI](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) ejemplo de código de VBScript utiliza un número de propiedades en **Win32 \_ WMISetting** para devolver una lista de las opciones de configuración de WMI configuradas en un equipo.</span><span class="sxs-lookup"><span data-stu-id="0345f-341">The [List All the WMI Settings](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) VBSCript code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="0345f-342">En el ejemplo de código JavaScript de la [información de configuración de WMI](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) se usa una serie de propiedades en **Win32 \_ WMISetting** para devolver una lista de las opciones de configuración de WMI configuradas en un equipo.</span><span class="sxs-lookup"><span data-stu-id="0345f-342">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) JavaScript code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="0345f-343">En el ejemplo de código de la [información de configuración de WMI](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) de la lista se usan varias propiedades de **Win32 \_ WMISetting** para devolver una lista de las opciones de configuración de WMI configuradas en un equipo.</span><span class="sxs-lookup"><span data-stu-id="0345f-343">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) Python code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="0345f-344">En el ejemplo de código del objeto de [información de configuración de WMI](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) de la lista se usan varias propiedades de **Win32 \_ WMISetting** para devolver una lista de las opciones de configuración de WMI configuradas en un equipo.</span><span class="sxs-lookup"><span data-stu-id="0345f-344">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) Object REXX code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="0345f-345">En el ejemplo de código de VBScript siguiente se muestra cómo obtener la versión de WMI que se ejecuta en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="0345f-345">The following VBScript code example shows how to obtain the version of WMI running on the local computer.</span></span> <span data-ttu-id="0345f-346">"Win32 \_ WMISetting = @" indica la instancia única de la clase.</span><span class="sxs-lookup"><span data-stu-id="0345f-346">The "Win32\_WMISetting=@" indicates the single instance of the class.</span></span> <span data-ttu-id="0345f-347">Para obtener más información, vea versiones de WMI.</span><span class="sxs-lookup"><span data-stu-id="0345f-347">For more information, see WMI versions.</span></span>


```VB
set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!/Root/CIMv2")

set objWMISetting = objWMIService.Get("Win32_WMISetting=@")

WScript.Echo  objWMISetting.BuildVersion
```



## <a name="requirements"></a><span data-ttu-id="0345f-348">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0345f-348">Requirements</span></span>



| <span data-ttu-id="0345f-349">Requisito</span><span class="sxs-lookup"><span data-stu-id="0345f-349">Requirement</span></span> | <span data-ttu-id="0345f-350">Value</span><span class="sxs-lookup"><span data-stu-id="0345f-350">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0345f-351">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0345f-351">Minimum supported client</span></span><br/> | <span data-ttu-id="0345f-352">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0345f-352">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0345f-353">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0345f-353">Minimum supported server</span></span><br/> | <span data-ttu-id="0345f-354">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0345f-354">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0345f-355">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0345f-355">Namespace</span></span><br/>                | <span data-ttu-id="0345f-356">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0345f-356">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0345f-357">MOF</span><span class="sxs-lookup"><span data-stu-id="0345f-357">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0345f-358"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0345f-358"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0345f-359">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0345f-359">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0345f-360"><dt>Wbemcore.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0345f-360"><dt>Wbemcore.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0345f-361">Vea también</span><span class="sxs-lookup"><span data-stu-id="0345f-361">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0345f-362">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="0345f-362">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="0345f-363">Clases de administración de servicios WMI</span><span class="sxs-lookup"><span data-stu-id="0345f-363">WMI Service Management Classes</span></span>](./wmi-service-management-classes.md)
</dt> </dl>

 

 
