---
description: La \_ clase WMI BootConfiguration de Win32 representa la configuración de arranque de un equipo que ejecuta Windows.
ms.assetid: c2db28dd-3feb-44bb-a532-c91cab980ba3
ms.tgt_platform: multiple
title: Win32_BootConfiguration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BootConfiguration
- Win32_BootConfiguration.Caption
- Win32_BootConfiguration.Description
- Win32_BootConfiguration.SettingID
- Win32_BootConfiguration.BootDirectory
- Win32_BootConfiguration.ConfigurationPath
- Win32_BootConfiguration.LastDrive
- Win32_BootConfiguration.Name
- Win32_BootConfiguration.ScratchDirectory
- Win32_BootConfiguration.TempDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 556688d7c80038f04dd5b94b7c61c5d6dfef3199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659710"
---
# <a name="win32_bootconfiguration-class"></a><span data-ttu-id="209c1-103">\_Clase Win32 BootConfiguration</span><span class="sxs-lookup"><span data-stu-id="209c1-103">Win32\_BootConfiguration class</span></span>

<span data-ttu-id="209c1-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ BootConfiguration de Win32** representa la configuración de arranque de un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="209c1-104">The **Win32\_BootConfiguration** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the boot configuration of a computer system running Windows.</span></span>

<span data-ttu-id="209c1-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="209c1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="209c1-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="209c1-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="209c1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="209c1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_BootConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string BootDirectory;
  string ConfigurationPath;
  string LastDrive;
  string Name;
  string ScratchDirectory;
  string TempDirectory;
};
```

## <a name="members"></a><span data-ttu-id="209c1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="209c1-108">Members</span></span>

<span data-ttu-id="209c1-109">La **clase \_ BootConfiguration de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="209c1-109">The **Win32\_BootConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="209c1-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="209c1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="209c1-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="209c1-111">Properties</span></span>

<span data-ttu-id="209c1-112">La **clase \_ BootConfiguration de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="209c1-112">The **Win32\_BootConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="209c1-113">**BootDirectory**</span><span class="sxs-lookup"><span data-stu-id="209c1-113">**BootDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="209c1-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="209c1-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="209c1-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="209c1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="209c1-116">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Process and Thread Functions \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir")</span><span class="sxs-lookup"><span data-stu-id="209c1-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Process and Thread Functions\|[**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable)\|WinBootDir")</span></span>
</dt> </dl>

<span data-ttu-id="209c1-117">Ruta de acceso a los archivos del sistema necesarios para arrancar el sistema.</span><span class="sxs-lookup"><span data-stu-id="209c1-117">Path to the system files required for booting the system.</span></span>

<span data-ttu-id="209c1-118">Ejemplo: "C: \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="209c1-118">Example: "C:\\Windows"</span></span>

</dd> <dt>

<span data-ttu-id="209c1-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="209c1-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="209c1-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="209c1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="209c1-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="209c1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="209c1-122">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="209c1-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="209c1-123">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="209c1-123">Short textual description of the current object.</span></span>

<span data-ttu-id="209c1-124">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="209c1-124">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="209c1-125">**ConfigurationPath**</span><span class="sxs-lookup"><span data-stu-id="209c1-125">**ConfigurationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="209c1-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="209c1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="209c1-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="209c1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="209c1-128">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Process and Thread Functions \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir")</span><span class="sxs-lookup"><span data-stu-id="209c1-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Process and Thread Functions\|[**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable)\|WinBootDir")</span></span>
</dt> </dl>

<span data-ttu-id="209c1-129">Ruta de acceso a los archivos de configuración.</span><span class="sxs-lookup"><span data-stu-id="209c1-129">Path to the configuration files.</span></span> <span data-ttu-id="209c1-130">Este valor puede ser similar al valor de la propiedad **BootDirectory** .</span><span class="sxs-lookup"><span data-stu-id="209c1-130">This value may be similar to the value in the **BootDirectory** property.</span></span>

</dd> <dt>

<span data-ttu-id="209c1-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="209c1-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="209c1-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="209c1-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="209c1-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="209c1-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="209c1-134">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="209c1-134">Textual description of the current object.</span></span>

<span data-ttu-id="209c1-135">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="209c1-135">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="209c1-136">**LastDrive**</span><span class="sxs-lookup"><span data-stu-id="209c1-136">**LastDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="209c1-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="209c1-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="209c1-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="209c1-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="209c1-139">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File Functions \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="209c1-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="209c1-140">Última letra de unidad a la que se asigna una unidad física.</span><span class="sxs-lookup"><span data-stu-id="209c1-140">Last drive letter to which a physical drive is assigned.</span></span>

<span data-ttu-id="209c1-141">Ejemplo: "E:"</span><span class="sxs-lookup"><span data-stu-id="209c1-141">Example: "E:"</span></span>

</dd> <dt>

<span data-ttu-id="209c1-142">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="209c1-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="209c1-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="209c1-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="209c1-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="209c1-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="209c1-145">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="209c1-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="209c1-146">Nombre de la configuración de arranque.</span><span class="sxs-lookup"><span data-stu-id="209c1-146">Name of the boot configuration.</span></span> <span data-ttu-id="209c1-147">Es un identificador de la configuración de arranque.</span><span class="sxs-lookup"><span data-stu-id="209c1-147">It is an identifier for the boot configuration.</span></span>

</dd> <dt>

<span data-ttu-id="209c1-148">**ScratchDirectory**</span><span class="sxs-lookup"><span data-stu-id="209c1-148">**ScratchDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="209c1-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="209c1-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="209c1-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="209c1-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="209c1-151">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File Functions \| GetTempPath")</span><span class="sxs-lookup"><span data-stu-id="209c1-151">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetTempPath")</span></span>
</dt> </dl>

<span data-ttu-id="209c1-152">Directorio en el que pueden residir los archivos temporales durante el arranque.</span><span class="sxs-lookup"><span data-stu-id="209c1-152">Directory where temporary files can reside during boot time.</span></span>

</dd> <dt>

<span data-ttu-id="209c1-153">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="209c1-153">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="209c1-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="209c1-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="209c1-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="209c1-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="209c1-156">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="209c1-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="209c1-157">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="209c1-157">Identifier by which the current object is known.</span></span>

<span data-ttu-id="209c1-158">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="209c1-158">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="209c1-159">**TempDirectory**</span><span class="sxs-lookup"><span data-stu-id="209c1-159">**TempDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="209c1-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="209c1-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="209c1-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="209c1-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="209c1-162">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File Functions \| GetTempPath")</span><span class="sxs-lookup"><span data-stu-id="209c1-162">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetTempPath")</span></span>
</dt> </dl>

<span data-ttu-id="209c1-163">Directorio donde se almacenan los archivos temporales.</span><span class="sxs-lookup"><span data-stu-id="209c1-163">Directory where temporary files are stored.</span></span>

<span data-ttu-id="209c1-164">Ejemplo: "C: \\ Temp"</span><span class="sxs-lookup"><span data-stu-id="209c1-164">Example: "C:\\TEMP"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="209c1-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="209c1-165">Remarks</span></span>

<span data-ttu-id="209c1-166">La **clase \_ BootConfiguration de Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="209c1-166">The **Win32\_BootConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="examples"></a><span data-ttu-id="209c1-167">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="209c1-167">Examples</span></span>

<span data-ttu-id="209c1-168">La [lista de las propiedades de configuración de arranque de un ejemplo Perl de equipo](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) devuelve información de configuración de arranque para un equipo.</span><span class="sxs-lookup"><span data-stu-id="209c1-168">The [List the Boot Configuration Properties of a Computer](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) Perl sample returns boot configuration information for a computer.</span></span>

<span data-ttu-id="209c1-169">El siguiente ejemplo de VBScript devuelve información de configuración de arranque para un equipo.</span><span class="sxs-lookup"><span data-stu-id="209c1-169">The following VBScript sample returns boot configuration information for a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BootConfiguration") 
 
For Each objItem in colItems 
    Wscript.Echo "Boot Directory: " & objItem.BootDirectory 
    Wscript.Echo "Configuration Path: " & objItem.ConfigurationPath 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Last Drive: " & objItem.LastDrive 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Scratch Directory: " & objItem.ScratchDirectory 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Temp Directory: " & objItem.TempDirectory 
Next 
```



<span data-ttu-id="209c1-170">En el siguiente ejemplo de código se muestra el uso de la clase WMI **\_ BootConfiguration de Win32** .</span><span class="sxs-lookup"><span data-stu-id="209c1-170">The following code sample demonstrates the use of the **Win32\_BootConfiguration** WMI class.</span></span>


```PowerShell
# Get Boot configuration from WMI

$boot = Get-WMIObject Win32_BootConfiguration

# Display information

"Boot Directory     : {0}" -f $boot.bootdirectory
"Caption            : {0}" -f $boot.caption
"Description        : {0}" -f $boot.description
"Last Drive         : {0}" -f $boot.lastdrive
"Scratch Directory  : {0}" -f $boot.scratchdirectory
"Temp Directory     : {0}" -f $boot.tempdirectory

```



<span data-ttu-id="209c1-171">En el ejemplo de código anterior se crea el siguiente resultado:</span><span class="sxs-lookup"><span data-stu-id="209c1-171">The previous code sample creates the following output:</span></span>

``` syntax
Boot Directory     : \WINDOWS
Caption            : \Device\Harddisk0\Partition1
Description        : \Device\Harddisk0\Partition1
Last Drive         : K:
Scratch Directory  : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
Temp Directory     : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
```

## <a name="requirements"></a><span data-ttu-id="209c1-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="209c1-172">Requirements</span></span>



| <span data-ttu-id="209c1-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="209c1-173">Requirement</span></span> | <span data-ttu-id="209c1-174">Value</span><span class="sxs-lookup"><span data-stu-id="209c1-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="209c1-175">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="209c1-175">Minimum supported client</span></span><br/> | <span data-ttu-id="209c1-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="209c1-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="209c1-177">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="209c1-177">Minimum supported server</span></span><br/> | <span data-ttu-id="209c1-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="209c1-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="209c1-179">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="209c1-179">Namespace</span></span><br/>                | <span data-ttu-id="209c1-180">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="209c1-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="209c1-181">MOF</span><span class="sxs-lookup"><span data-stu-id="209c1-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="209c1-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="209c1-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="209c1-183">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="209c1-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="209c1-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="209c1-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="209c1-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="209c1-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="209c1-186">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="209c1-186">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="209c1-187">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="209c1-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

