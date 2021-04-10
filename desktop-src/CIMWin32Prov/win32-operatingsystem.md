---
description: Representa un sistema operativo basado en Windows instalado en un equipo.
ms.assetid: eb6a8cff-20a0-4211-b46a-3084e9c39246
ms.tgt_platform: multiple
title: Clase Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem
- Win32_OperatingSystem.BootDevice
- Win32_OperatingSystem.BuildNumber
- Win32_OperatingSystem.BuildType
- Win32_OperatingSystem.Caption
- Win32_OperatingSystem.CodeSet
- Win32_OperatingSystem.CountryCode
- Win32_OperatingSystem.CreationClassName
- Win32_OperatingSystem.CSCreationClassName
- Win32_OperatingSystem.CSDVersion
- Win32_OperatingSystem.CSName
- Win32_OperatingSystem.CurrentTimeZone
- Win32_OperatingSystem.DataExecutionPrevention_Available
- Win32_OperatingSystem.DataExecutionPrevention_32BitApplications
- Win32_OperatingSystem.DataExecutionPrevention_Drivers
- Win32_OperatingSystem.DataExecutionPrevention_SupportPolicy
- Win32_OperatingSystem.Debug
- Win32_OperatingSystem.Description
- Win32_OperatingSystem.Distributed
- Win32_OperatingSystem.EncryptionLevel
- Win32_OperatingSystem.ForegroundApplicationBoost
- Win32_OperatingSystem.FreePhysicalMemory
- Win32_OperatingSystem.FreeSpaceInPagingFiles
- Win32_OperatingSystem.FreeVirtualMemory
- Win32_OperatingSystem.InstallDate
- Win32_OperatingSystem.LargeSystemCache
- Win32_OperatingSystem.LastBootUpTime
- Win32_OperatingSystem.LocalDateTime
- Win32_OperatingSystem.Locale
- Win32_OperatingSystem.Manufacturer
- Win32_OperatingSystem.MaxNumberOfProcesses
- Win32_OperatingSystem.MaxProcessMemorySize
- Win32_OperatingSystem.MUILanguages
- Win32_OperatingSystem.Name
- Win32_OperatingSystem.NumberOfLicensedUsers
- Win32_OperatingSystem.NumberOfProcesses
- Win32_OperatingSystem.NumberOfUsers
- Win32_OperatingSystem.OperatingSystemSKU
- Win32_OperatingSystem.Organization
- Win32_OperatingSystem.OSArchitecture
- Win32_OperatingSystem.OSLanguage
- Win32_OperatingSystem.OSProductSuite
- Win32_OperatingSystem.OSType
- Win32_OperatingSystem.OtherTypeDescription
- Win32_OperatingSystem.PAEEnabled
- Win32_OperatingSystem.PlusProductID
- Win32_OperatingSystem.PlusVersionNumber
- Win32_OperatingSystem.PortableOperatingSystem
- Win32_OperatingSystem.Primary
- Win32_OperatingSystem.ProductType
- Win32_OperatingSystem.RegisteredUser
- Win32_OperatingSystem.SerialNumber
- Win32_OperatingSystem.ServicePackMajorVersion
- Win32_OperatingSystem.ServicePackMinorVersion
- Win32_OperatingSystem.SizeStoredInPagingFiles
- Win32_OperatingSystem.Status
- Win32_OperatingSystem.SuiteMask
- Win32_OperatingSystem.SystemDevice
- Win32_OperatingSystem.SystemDirectory
- Win32_OperatingSystem.SystemDrive
- Win32_OperatingSystem.TotalSwapSpaceSize
- Win32_OperatingSystem.TotalVirtualMemorySize
- Win32_OperatingSystem.TotalVisibleMemorySize
- Win32_OperatingSystem.Version
- Win32_OperatingSystem.WindowsDirectory
- Win32_OperatingSystem.QuantumLength
- Win32_OperatingSystem.QuantumType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15a6a1bf7bec8c830d1a15ec690b01ec9ea22e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275076"
---
# <a name="win32_operatingsystem-class"></a><span data-ttu-id="48ab3-103">Win32 \_ OperatingSystem (clase)</span><span class="sxs-lookup"><span data-stu-id="48ab3-103">Win32\_OperatingSystem class</span></span>

<span data-ttu-id="48ab3-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ OperatingSystem de Win32** representa un sistema operativo basado en Windows instalado en un equipo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-104">The **Win32\_OperatingSystem** [WMI class](../wmisdk/retrieving-a-class.md) represents a Windows-based operating system installed on a computer.</span></span>

<span data-ttu-id="48ab3-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="48ab3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="48ab3-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="48ab3-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="48ab3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48ab3-107">Syntax</span></span>

``` syntax
[Singleton, Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4DE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OperatingSystem : CIM_OperatingSystem
{
  string   BootDevice;
  string   BuildNumber;
  string   BuildType;
  string   Caption;
  string   CodeSet;
  string   CountryCode;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSDVersion;
  string   CSName;
  sint16   CurrentTimeZone;
  boolean  DataExecutionPrevention_Available;
  boolean  DataExecutionPrevention_32BitApplications;
  boolean  DataExecutionPrevention_Drivers;
  uint8    DataExecutionPrevention_SupportPolicy;
  boolean  Debug;
  string   Description;
  boolean  Distributed;
  uint32   EncryptionLevel;
  uint8    ForegroundApplicationBoost = 2;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  uint32   LargeSystemCache;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  string   Locale;
  string   Manufacturer;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   MUILanguages[];
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint32   OperatingSystemSKU;
  string   Organization;
  string   OSArchitecture;
  uint32   OSLanguage;
  uint32   OSProductSuite;
  uint16   OSType;
  string   OtherTypeDescription;
  Boolean  PAEEnabled;
  string   PlusProductID;
  string   PlusVersionNumber;
  boolean  PortableOperatingSystem;
  boolean  Primary;
  uint32   ProductType;
  string   RegisteredUser;
  string   SerialNumber;
  uint16   ServicePackMajorVersion;
  uint16   ServicePackMinorVersion;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint32   SuiteMask;
  string   SystemDevice;
  string   SystemDirectory;
  string   SystemDrive;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
  string   WindowsDirectory;
  uint8    QuantumLength;
  uint8    QuantumType;
};
```

## <a name="members"></a><span data-ttu-id="48ab3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="48ab3-108">Members</span></span>

<span data-ttu-id="48ab3-109">La clase **Win32 \_ OperatingSystem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="48ab3-109">The **Win32\_OperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="48ab3-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="48ab3-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="48ab3-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48ab3-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="48ab3-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="48ab3-112">Methods</span></span>

<span data-ttu-id="48ab3-113">La clase **Win32 \_ OperatingSystem** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="48ab3-113">The **Win32\_OperatingSystem** class has these methods.</span></span>



| <span data-ttu-id="48ab3-114">Método</span><span class="sxs-lookup"><span data-stu-id="48ab3-114">Method</span></span>                                                                                     | <span data-ttu-id="48ab3-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="48ab3-115">Description</span></span>                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48ab3-116">**Reboot**</span><span class="sxs-lookup"><span data-stu-id="48ab3-116">**Reboot**</span></span>](reboot-method-in-class-win32-operatingsystem.md)                             | <span data-ttu-id="48ab3-117">Apaga el sistema y reinicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-117">Shuts down and then restarts the computer system.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="48ab3-118">**SetDateTime**</span><span class="sxs-lookup"><span data-stu-id="48ab3-118">**SetDateTime**</span></span>](setdatetime-method-in-class-win32-operatingsystem.md)                   | <span data-ttu-id="48ab3-119">Permite establecer la fecha y hora del equipo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-119">Allows the computer date and time to be set.</span></span><br/>                                                                                                                                                                                                                |
| [<span data-ttu-id="48ab3-120">**Apagado**</span><span class="sxs-lookup"><span data-stu-id="48ab3-120">**Shutdown**</span></span>](shutdown-method-in-class-win32-operatingsystem.md)                         | <span data-ttu-id="48ab3-121">Descarga programas y archivos dll hasta el punto en el que es seguro apagar el equipo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-121">Unloads programs and DLLs to the point where it is safe to turn off the computer.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="48ab3-122">**Win32Shutdown**</span><span class="sxs-lookup"><span data-stu-id="48ab3-122">**Win32Shutdown**</span></span>](win32shutdown-method-in-class-win32-operatingsystem.md)               | <span data-ttu-id="48ab3-123">Proporciona el conjunto completo de opciones de apagado compatibles con los sistemas operativos Windows.</span><span class="sxs-lookup"><span data-stu-id="48ab3-123">Provides the full set of shutdown options supported by Windows operating systems.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="48ab3-124">**Win32ShutdownTracker**</span><span class="sxs-lookup"><span data-stu-id="48ab3-124">**Win32ShutdownTracker**</span></span>](win32shutdowntracker-method-in-class-win32-operatingsystem.md) | <span data-ttu-id="48ab3-125">Proporciona el mismo conjunto de opciones de cierre admitido por el método [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) en el **\_ OperatingSystem de Win32**, pero también permite especificar comentarios, un motivo para el cierre o un tiempo de espera agotado.</span><span class="sxs-lookup"><span data-stu-id="48ab3-125">Provides the same set of shutdown options supported by the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method in **Win32\_OperatingSystem**, but also allows you to specify comments, a reason for shutdown, or a timeout.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="48ab3-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48ab3-126">Properties</span></span>

<span data-ttu-id="48ab3-127">La clase **Win32 \_ OperatingSystem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="48ab3-127">The **Win32\_OperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48ab3-128">**BootDevice**</span><span class="sxs-lookup"><span data-stu-id="48ab3-128">**BootDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-131">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| información de asignación de unidad inesperados win32api \_ \_ \| btInt13Unit")</span><span class="sxs-lookup"><span data-stu-id="48ab3-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|DRIVE\_MAP\_INFO\|btInt13Unit")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-132">Nombre de la unidad de disco desde la que se inicia el sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="48ab3-132">Name of the disk drive from which the Windows operating system starts.</span></span>

<span data-ttu-id="48ab3-133">Ejemplo: " \\ \\ dispositivo \\ Harddisk0"</span><span class="sxs-lookup"><span data-stu-id="48ab3-133">Example: "\\\\Device\\Harddisk0"</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-134">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="48ab3-134">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-137">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwBuildNumber")</span><span class="sxs-lookup"><span data-stu-id="48ab3-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|dwBuildNumber")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-138">Número de compilación de un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-138">Build number of an operating system.</span></span> <span data-ttu-id="48ab3-139">Se puede utilizar para obtener información de versión más precisa que los números de versión de lanzamiento del producto.</span><span class="sxs-lookup"><span data-stu-id="48ab3-139">It can be used for more precise version information than product release version numbers.</span></span>

<span data-ttu-id="48ab3-140">Ejemplo: "1381"</span><span class="sxs-lookup"><span data-stu-id="48ab3-140">Example: "1381"</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-141">**BuildType**</span><span class="sxs-lookup"><span data-stu-id="48ab3-141">**BuildType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-144">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| CurrentType")</span><span class="sxs-lookup"><span data-stu-id="48ab3-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows\\\\CurrentVersion\|CurrentType")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-145">Tipo de compilación usado para un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-145">Type of build used for an operating system.</span></span>

<span data-ttu-id="48ab3-146">Ejemplos: "" compilación comercial "", "compilación comprobada" "</span><span class="sxs-lookup"><span data-stu-id="48ab3-146">Examples: ""retail build"", ""checked build""</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-147">**Caption**</span><span class="sxs-lookup"><span data-stu-id="48ab3-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-150">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="48ab3-150">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-151">Breve descripción del objeto: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="48ab3-151">Short description of the object—a one-line string.</span></span> <span data-ttu-id="48ab3-152">La cadena incluye la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-152">The string includes the operating system version.</span></span> <span data-ttu-id="48ab3-153">Por ejemplo, "Microsoft Windows 7 Enterprise".</span><span class="sxs-lookup"><span data-stu-id="48ab3-153">For example, "Microsoft Windows 7 Enterprise ".</span></span> <span data-ttu-id="48ab3-154">Esta propiedad se puede localizar.</span><span class="sxs-lookup"><span data-stu-id="48ab3-154">This property can be localized.</span></span>

<span data-ttu-id="48ab3-155">**Windows Vista y Windows 7:** Esta propiedad puede contener caracteres finales.</span><span class="sxs-lookup"><span data-stu-id="48ab3-155">**Windows Vista and Windows 7:** This property may contain trailing characters.</span></span> <span data-ttu-id="48ab3-156">Por ejemplo, la cadena "Microsoft Windows 7 Enterprise" (espacio final incluido) puede ser necesaria para recuperar información mediante esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="48ab3-156">For example, the string "Microsoft Windows 7 Enterprise " (trailing space included) may be necessary to retrieve information using this property.</span></span>

<span data-ttu-id="48ab3-157">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-158">**Dese**</span><span class="sxs-lookup"><span data-stu-id="48ab3-158">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-161">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (6), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| National Language support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| configuración regional \_ IDEFAULTANSICODEPAGE")</span><span class="sxs-lookup"><span data-stu-id="48ab3-161">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (6), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_IDEFAULTANSICODEPAGE")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-162">Valor de la página de códigos que utiliza un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-162">Code page value an operating system uses.</span></span> <span data-ttu-id="48ab3-163">Una página de códigos contiene una tabla de caracteres que un sistema operativo usa para traducir cadenas para distintos idiomas.</span><span class="sxs-lookup"><span data-stu-id="48ab3-163">A code page contains a character table that an operating system uses to translate strings for different languages.</span></span> <span data-ttu-id="48ab3-164">En el American National Standards Institute (ANSI) se muestran los valores que representan las páginas de códigos definidas.</span><span class="sxs-lookup"><span data-stu-id="48ab3-164">The American National Standards Institute (ANSI) lists values that represent defined code pages.</span></span> <span data-ttu-id="48ab3-165">Si un sistema operativo no usa una página de códigos ANSI, este miembro se establece en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="48ab3-165">If an operating system does not use an ANSI code page, this member is set to 0 (zero).</span></span> <span data-ttu-id="48ab3-166">La cadena codebase puede utilizar un máximo de seis caracteres para definir el valor **de la página** de códigos.</span><span class="sxs-lookup"><span data-stu-id="48ab3-166">The **CodeSet** string can use a maximum of six characters to define the code page value.</span></span>

<span data-ttu-id="48ab3-167">Ejemplo: "1255"</span><span class="sxs-lookup"><span data-stu-id="48ab3-167">Example: "1255"</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-168">**País**</span><span class="sxs-lookup"><span data-stu-id="48ab3-168">**CountryCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-171">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| National Language support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| configuración regional \_ ICOUNTRY")</span><span class="sxs-lookup"><span data-stu-id="48ab3-171">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_ICOUNTRY")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-172">Código para el país o región que utiliza un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-172">Code for the country/region that an operating system uses.</span></span> <span data-ttu-id="48ab3-173">Los valores se basan en prefijos de marcado telefónico internacional, también conocidos como códigos de país o región de IBM.</span><span class="sxs-lookup"><span data-stu-id="48ab3-173">Values are based on international phone dialing prefixes—also referred to as IBM country/region codes.</span></span> <span data-ttu-id="48ab3-174">Esta propiedad puede usar un máximo de seis caracteres para definir el valor de código de país o región.</span><span class="sxs-lookup"><span data-stu-id="48ab3-174">This property can use a maximum of six characters to define the country/region code value.</span></span>

<span data-ttu-id="48ab3-175">Ejemplo: "1" (Estados Unidos)</span><span class="sxs-lookup"><span data-stu-id="48ab3-175">Example: "1" (United States)</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="48ab3-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-179">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="48ab3-179">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-180">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="48ab3-180">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="48ab3-181">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="48ab3-181">When used with other key properties of the class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="48ab3-182">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-182">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-183">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="48ab3-183">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-186">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="48ab3-186">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-187">Nombre de la clase de creación del sistema de ámbito del equipo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-187">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="48ab3-188">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-188">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-189">**CSDVersion**</span><span class="sxs-lookup"><span data-stu-id="48ab3-189">**CSDVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-192">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **szCSDVersion**")</span><span class="sxs-lookup"><span data-stu-id="48ab3-192">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**szCSDVersion**")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-193">Cadena terminada en **null** que indica el Service Pack más reciente instalado en un equipo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-193">**NULL**-terminated string that indicates the latest service pack installed on a computer.</span></span> <span data-ttu-id="48ab3-194">Si no hay ningún Service Pack instalado, la cadena es **null**.</span><span class="sxs-lookup"><span data-stu-id="48ab3-194">If no service pack is installed, the string is **NULL**.</span></span>

<span data-ttu-id="48ab3-195">Ejemplo: "Service Pack 3"</span><span class="sxs-lookup"><span data-stu-id="48ab3-195">Example: "Service Pack 3"</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-196">**CSName**</span><span class="sxs-lookup"><span data-stu-id="48ab3-196">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-199">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="48ab3-199">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-200">Nombre del sistema de ámbito del equipo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-200">Name of the scoping computer system.</span></span>

<span data-ttu-id="48ab3-201">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-201">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-202">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="48ab3-202">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-203">Tipo de datos: **sint16**</span><span class="sxs-lookup"><span data-stu-id="48ab3-203">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-205">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="48ab3-205">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-206">Número, en minutos, que un sistema operativo se desvía de la hora del meridiano de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="48ab3-206">Number, in minutes, an operating system is offset from Greenwich mean time (GMT).</span></span> <span data-ttu-id="48ab3-207">El número es positivo, negativo o cero.</span><span class="sxs-lookup"><span data-stu-id="48ab3-207">The number is positive, negative, or zero.</span></span>

<span data-ttu-id="48ab3-208">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-208">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-209">**DataExecutionPrevention \_ 32BitApplications**</span><span class="sxs-lookup"><span data-stu-id="48ab3-209">**DataExecutionPrevention\_32BitApplications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-210">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="48ab3-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-212">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="48ab3-212">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-213">Cuando la característica de hardware de prevención de ejecución de datos está disponible, esta propiedad indica que la característica está configurada para funcionar en aplicaciones de 32 bits si es **true**.</span><span class="sxs-lookup"><span data-stu-id="48ab3-213">When the data execution prevention hardware feature is available, this property indicates that the feature is set to work for 32-bit applications if **True**.</span></span> <span data-ttu-id="48ab3-214">En los equipos de 64 bits, la característica prevención de ejecución de datos se configura en el almacén de [datos de la configuración de arranque (BCD) (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) y las propiedades en el sistema **\_ operativo Win32** se establecen en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="48ab3-214">On 64-bit computers, the data execution prevention feature is configured in the [Boot Configuration Data (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-215">**DataExecutionPrevention \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="48ab3-215">**DataExecutionPrevention\_Available**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-216">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="48ab3-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-218">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="48ab3-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-219">La prevención de ejecución de datos es una característica de hardware para evitar ataques por saturación del búfer al detener la ejecución de código en páginas de memoria de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="48ab3-219">Data execution prevention is a hardware feature to prevent buffer overrun attacks by stopping the execution of code on data-type memory pages.</span></span> <span data-ttu-id="48ab3-220">Si es **true**, esta característica está disponible.</span><span class="sxs-lookup"><span data-stu-id="48ab3-220">If **True**, then this feature is available.</span></span> <span data-ttu-id="48ab3-221">En los equipos de 64 bits, la característica prevención de ejecución de datos se configura en el almacén BCD y las propiedades en el sistema **\_ operativo Win32** se establecen en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="48ab3-221">On 64-bit computers, the data execution prevention feature is configured in the BCD store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-222">**\_Controladores DataExecutionPrevention**</span><span class="sxs-lookup"><span data-stu-id="48ab3-222">**DataExecutionPrevention\_Drivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-223">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="48ab3-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-225">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="48ab3-225">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-226">Cuando la característica de hardware de prevención de ejecución de datos está disponible, esta propiedad indica que la característica está configurada para funcionar con los controladores si es **true**.</span><span class="sxs-lookup"><span data-stu-id="48ab3-226">When the data execution prevention hardware feature is available, this property indicates that the feature is set to work for drivers if **True**.</span></span> <span data-ttu-id="48ab3-227">En los equipos de 64 bits, la característica prevención de ejecución de datos se configura en el almacén BCD y las propiedades en el sistema **\_ operativo Win32** se establecen en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="48ab3-227">On 64-bit computers, the data execution prevention feature is configured in the BCD store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-228">**DataExecutionPrevention \_ SupportPolicy**</span><span class="sxs-lookup"><span data-stu-id="48ab3-228">**DataExecutionPrevention\_SupportPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-229">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="48ab3-229">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-231">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="48ab3-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-232">Indica la configuración de prevención de ejecución de datos (DEP) que se aplica.</span><span class="sxs-lookup"><span data-stu-id="48ab3-232">Indicates which Data Execution Prevention (DEP) setting is applied.</span></span> <span data-ttu-id="48ab3-233">La configuración de DEP especifica la medida en la que DEP se aplica a las aplicaciones de 32 bits en el sistema.</span><span class="sxs-lookup"><span data-stu-id="48ab3-233">The DEP setting specifies the extent to which DEP applies to 32-bit applications on the system.</span></span> <span data-ttu-id="48ab3-234">DEP siempre se aplica al kernel de Windows.</span><span class="sxs-lookup"><span data-stu-id="48ab3-234">DEP is always applied to the Windows kernel.</span></span>

<dt>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>

<span data-ttu-id="48ab3-235"><span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Siempre desactivado** (0)</span><span class="sxs-lookup"><span data-stu-id="48ab3-235"><span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Always Off** (0)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-236">DEP está desactivado para todas las aplicaciones de 32 bits del equipo sin excepciones.</span><span class="sxs-lookup"><span data-stu-id="48ab3-236">DEP is turned off for all 32-bit applications on the computer with no exceptions.</span></span> <span data-ttu-id="48ab3-237">Esta opción no está disponible para la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="48ab3-237">This setting is not available for the user interface.</span></span>

</dd> <dt>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>

<span data-ttu-id="48ab3-238"><span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always on** (1)</span><span class="sxs-lookup"><span data-stu-id="48ab3-238"><span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always On** (1)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-239">DEP está habilitado para todas las aplicaciones de 32 bits del equipo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-239">DEP is enabled for all 32-bit applications on the computer.</span></span> <span data-ttu-id="48ab3-240">Esta opción no está disponible para la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="48ab3-240">This setting is not available for the user interface.</span></span>

</dd> <dt>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>

<span data-ttu-id="48ab3-241"><span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Participación** (2)</span><span class="sxs-lookup"><span data-stu-id="48ab3-241"><span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Opt In** (2)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-242">DEP está habilitado para un número limitado de archivos binarios, el kernel y todos los servicios basados en Windows.</span><span class="sxs-lookup"><span data-stu-id="48ab3-242">DEP is enabled for a limited number of binaries, the kernel, and all Windows-based services.</span></span> <span data-ttu-id="48ab3-243">Sin embargo, está desactivada de forma predeterminada para todas las aplicaciones de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="48ab3-243">However, it is off by default for all 32-bit applications.</span></span> <span data-ttu-id="48ab3-244">Un usuario o administrador debe elegir explícitamente el valor de **Always on** o de la opción de **cancelación** antes de que se pueda aplicar DEP a las aplicaciones de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="48ab3-244">A user or administrator must explicitly choose either the **Always On** or the **Opt Out** setting before DEP can be applied to 32-bit applications.</span></span>

</dd> <dt>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>

<span data-ttu-id="48ab3-245"><span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Rechazar** (3)</span><span class="sxs-lookup"><span data-stu-id="48ab3-245"><span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Opt Out** (3)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-246">DEP está habilitado de forma predeterminada para todas las aplicaciones de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="48ab3-246">DEP is enabled by default for all 32-bit applications.</span></span> <span data-ttu-id="48ab3-247">Un usuario o administrador puede quitar explícitamente la compatibilidad con una aplicación de 32 bits agregando la aplicación a una lista de excepciones.</span><span class="sxs-lookup"><span data-stu-id="48ab3-247">A user or administrator can explicitly remove support for a 32-bit application by adding the application to an exceptions list.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="48ab3-248">**Depurar**</span><span class="sxs-lookup"><span data-stu-id="48ab3-248">**Debug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-249">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="48ab3-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-251">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ Debug")</span><span class="sxs-lookup"><span data-stu-id="48ab3-251">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)\|SM\_DEBUG")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-252">El sistema operativo es una compilación comprobada (depuración).</span><span class="sxs-lookup"><span data-stu-id="48ab3-252">Operating system is a checked (debug) build.</span></span> <span data-ttu-id="48ab3-253">Si es **true**, la versión de depuración está instalada.</span><span class="sxs-lookup"><span data-stu-id="48ab3-253">If **True**, the debugging version is installed.</span></span> <span data-ttu-id="48ab3-254">Las compilaciones comprobadas proporcionan comprobación de errores, comprobación de argumentos y código de depuración del sistema.</span><span class="sxs-lookup"><span data-stu-id="48ab3-254">Checked builds provide error checking, argument verification, and system debugging code.</span></span> <span data-ttu-id="48ab3-255">El código adicional en un binario comprobado genera un mensaje de error del depurador de kernel y se interrumpe en el depurador.</span><span class="sxs-lookup"><span data-stu-id="48ab3-255">Additional code in a checked binary generates a kernel debugger error message and breaks into the debugger.</span></span> <span data-ttu-id="48ab3-256">Esto ayuda a determinar de inmediato la causa y la ubicación del error.</span><span class="sxs-lookup"><span data-stu-id="48ab3-256">This helps immediately determine the cause and location of the error.</span></span> <span data-ttu-id="48ab3-257">El rendimiento puede verse afectado en una compilación comprobada debido al código adicional que se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="48ab3-257">Performance may be affected in a checked build due to the additional code that is executed.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-258">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="48ab3-258">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-259">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-260">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="48ab3-260">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-261">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="48ab3-261">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-262">Descripción del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="48ab3-262">Description of the Windows operating system.</span></span> <span data-ttu-id="48ab3-263">Algunas interfaces de usuario, por ejemplo, las que permiten editar esta descripción, limitan su longitud a 48 caracteres.</span><span class="sxs-lookup"><span data-stu-id="48ab3-263">Some user interfaces for example, those that allow editing of this description, limit its length to 48 characters.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-264">**Distribuya**</span><span class="sxs-lookup"><span data-stu-id="48ab3-264">**Distributed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-265">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="48ab3-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-266">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-267">Si es **true**, el sistema operativo se distribuye entre varios nodos de sistema de equipo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-267">If **True**, the operating system is distributed across several computer system nodes.</span></span> <span data-ttu-id="48ab3-268">Si es así, estos nodos deben agruparse como clúster.</span><span class="sxs-lookup"><span data-stu-id="48ab3-268">If so, these nodes should be grouped as a cluster.</span></span>

<span data-ttu-id="48ab3-269">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-269">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-270">**EncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="48ab3-270">**EncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-271">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48ab3-271">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-273">Nivel de cifrado para transacciones seguras: 40 bits, 128 bits o *n* bits.</span><span class="sxs-lookup"><span data-stu-id="48ab3-273">Encryption level for secure transactions: 40-bit, 128-bit, or *n*-bit.</span></span>

<dt>

<span id="40-bit"></span><span id="40-BIT"></span>

<span data-ttu-id="48ab3-274">**40** bits (0)</span><span class="sxs-lookup"><span data-stu-id="48ab3-274">**40-bit** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="128-bit"></span><span id="128-BIT"></span>

<span data-ttu-id="48ab3-275">**128** bits (1)</span><span class="sxs-lookup"><span data-stu-id="48ab3-275">**128-bit** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="n-bit"></span><span id="N-BIT"></span>

<span data-ttu-id="48ab3-276">**n bits** (2)</span><span class="sxs-lookup"><span data-stu-id="48ab3-276">**n-bit** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="48ab3-277">**ForegroundApplicationBoost**</span><span class="sxs-lookup"><span data-stu-id="48ab3-277">**ForegroundApplicationBoost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-278">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="48ab3-278">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-279">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="48ab3-279">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-280">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ PriorityControl \| Win32PrioritySeparation")</span><span class="sxs-lookup"><span data-stu-id="48ab3-280">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\PriorityControl\|Win32PrioritySeparation")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-281">El aumento de prioridad se da a la aplicación de primer plano.</span><span class="sxs-lookup"><span data-stu-id="48ab3-281">Increase in priority is given to the foreground application.</span></span> <span data-ttu-id="48ab3-282">La mejora de la aplicación se implementa al otorgar a una aplicación más intervalos de tiempo de ejecución (longitudes de cuanto).</span><span class="sxs-lookup"><span data-stu-id="48ab3-282">Application boost is implemented by giving an application more execution time slices (quantum lengths).</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="48ab3-283"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguno** (0)</span><span class="sxs-lookup"><span data-stu-id="48ab3-283"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-284">El sistema aumenta la longitud del cuanto 6.</span><span class="sxs-lookup"><span data-stu-id="48ab3-284">The system boosts the quantum length by 6.</span></span>

</dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="48ab3-285"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Mínimo** (1)</span><span class="sxs-lookup"><span data-stu-id="48ab3-285"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (1)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-286">El sistema aumenta la longitud del Quantum en 12.</span><span class="sxs-lookup"><span data-stu-id="48ab3-286">The system boosts the quantum length by 12.</span></span>

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="48ab3-287"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Máximo** (2)</span><span class="sxs-lookup"><span data-stu-id="48ab3-287"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-288">El sistema aumenta la longitud del Quantum en 18.</span><span class="sxs-lookup"><span data-stu-id="48ab3-288">The system boosts the quantum length by 18.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="48ab3-289">**FreePhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="48ab3-289">**FreePhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-290">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48ab3-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-292">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="48ab3-292">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-293">Número, en kilobytes, de la memoria física que actualmente no se usa y está disponible.</span><span class="sxs-lookup"><span data-stu-id="48ab3-293">Number, in kilobytes, of physical memory currently unused and available.</span></span>

<span data-ttu-id="48ab3-294">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="48ab3-294">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="48ab3-295">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-295">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-296">**FreeSpaceInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="48ab3-296">**FreeSpaceInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-297">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48ab3-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-299">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Configuración de la memoria del sistema DMTF \| 001,4 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="48ab3-299">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Memory Settings\|001.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-300">Número, en kilobytes, que se puede asignar a los archivos de paginación del sistema operativo sin provocar que se intercambien otras páginas.</span><span class="sxs-lookup"><span data-stu-id="48ab3-300">Number, in kilobytes, that can be mapped into the operating system paging files without causing any other pages to be swapped out.</span></span>

<span data-ttu-id="48ab3-301">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="48ab3-301">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="48ab3-302">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-302">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-303">**Freevirtualmemory (**</span><span class="sxs-lookup"><span data-stu-id="48ab3-303">**FreeVirtualMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-304">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48ab3-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-306">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="48ab3-306">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-307">Número, en kilobytes, de la memoria virtual que actualmente no se usa y está disponible.</span><span class="sxs-lookup"><span data-stu-id="48ab3-307">Number, in kilobytes, of virtual memory currently unused and available.</span></span>

<span data-ttu-id="48ab3-308">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="48ab3-308">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="48ab3-309">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-309">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-310">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="48ab3-310">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-311">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="48ab3-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-313">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="48ab3-313">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-314">Se instaló el objeto de fecha.</span><span class="sxs-lookup"><span data-stu-id="48ab3-314">Date object was installed.</span></span> <span data-ttu-id="48ab3-315">Esta propiedad no requiere un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="48ab3-315">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="48ab3-316">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-317">**LargeSystemCache**</span><span class="sxs-lookup"><span data-stu-id="48ab3-317">**LargeSystemCache**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-318">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48ab3-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-320">Calificadores: [ **desusados**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="48ab3-320">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-321">Esta propiedad está obsoleta y no se admite.</span><span class="sxs-lookup"><span data-stu-id="48ab3-321">This property is obsolete and not supported.</span></span>

<dt>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>

<span data-ttu-id="48ab3-322"><span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Optimizar para aplicaciones** (0)</span><span class="sxs-lookup"><span data-stu-id="48ab3-322"><span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Optimize for Applications** (0)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-323">Optimizar la memoria para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="48ab3-323">Optimize memory for applications.</span></span>

</dd> <dt>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>

<span data-ttu-id="48ab3-324"><span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Optimizar para el rendimiento del sistema** (1)</span><span class="sxs-lookup"><span data-stu-id="48ab3-324"><span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Optimize for System Performance** (1)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-325">Optimizar la memoria para el rendimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="48ab3-325">Optimize memory for system performance.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="48ab3-326">**LastBootUpTime**</span><span class="sxs-lookup"><span data-stu-id="48ab3-326">**LastBootUpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-327">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="48ab3-327">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-329">Fecha y hora en que el sistema operativo se reinició por última vez.</span><span class="sxs-lookup"><span data-stu-id="48ab3-329">Date and time the operating system was last restarted.</span></span>

<span data-ttu-id="48ab3-330">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-330">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-331">**LocalDateTime**</span><span class="sxs-lookup"><span data-stu-id="48ab3-331">**LocalDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-332">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="48ab3-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-334">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-REsources-MIB. hrSystemDate "," MIF. \|Información general de DMTF \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="48ab3-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemDate", "MIF.DMTF\|General Information\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-335">Versión del sistema operativo de la fecha y hora del día local.</span><span class="sxs-lookup"><span data-stu-id="48ab3-335">Operating system version of the local date and time-of-day.</span></span>

<span data-ttu-id="48ab3-336">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-336">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-337">**Configuración regional**</span><span class="sxs-lookup"><span data-stu-id="48ab3-337">**Locale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-338">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-340">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| National Language support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| configuración regional \_ ILANGUAGE")</span><span class="sxs-lookup"><span data-stu-id="48ab3-340">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_ILANGUAGE")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-341">Identificador de idioma usado por el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-341">Language identifier used by the operating system.</span></span> <span data-ttu-id="48ab3-342">Un identificador de idioma es una abreviatura numérica internacional estándar para un país o región.</span><span class="sxs-lookup"><span data-stu-id="48ab3-342">A language identifier is a standard international numeric abbreviation for a country/region.</span></span> <span data-ttu-id="48ab3-343">Cada idioma tiene un identificador de idioma único (LANGID), un valor de 16 bits que consta de un identificador de idioma principal y un identificador de idioma secundario.</span><span class="sxs-lookup"><span data-stu-id="48ab3-343">Each language has a unique language identifier (LANGID), a 16-bit value that consists of a primary language identifier and a secondary language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-344">**Le**</span><span class="sxs-lookup"><span data-stu-id="48ab3-344">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-345">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-347">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="48ab3-347">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-348">Nombre del fabricante del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-348">Name of the operating system manufacturer.</span></span> <span data-ttu-id="48ab3-349">En el caso de los sistemas basados en Windows, este valor es "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="48ab3-349">For Windows-based systems, this value is "Microsoft Corporation".</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-350">**MaxNumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="48ab3-350">**MaxNumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-351">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48ab3-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-352">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-353">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-REsources-MIB. hrSystemMaxProcesses ")</span><span class="sxs-lookup"><span data-stu-id="48ab3-353">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemMaxProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-354">Número máximo de contextos de proceso que el sistema operativo puede admitir.</span><span class="sxs-lookup"><span data-stu-id="48ab3-354">Maximum number of process contexts the operating system can support.</span></span> <span data-ttu-id="48ab3-355">El valor predeterminado establecido por el proveedor es 4294967295 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="48ab3-355">The default value set by the provider is 4294967295 (0xFFFFFFFF).</span></span> <span data-ttu-id="48ab3-356">Si no hay ningún máximo fijo, el valor debe ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="48ab3-356">If there is no fixed maximum, the value should be 0 (zero).</span></span> <span data-ttu-id="48ab3-357">En los sistemas que tienen un máximo fijo, este objeto puede ayudar a diagnosticar los errores que se producen cuando se alcanza el máximo, si se desconoce, escriba 4294967295 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="48ab3-357">On systems that have a fixed maximum, this object can help diagnose failures that occur when the maximum is reached—if unknown, enter 4294967295 (0xFFFFFFFF).</span></span>

<span data-ttu-id="48ab3-358">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-358">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-359">**MaxProcessMemorySize**</span><span class="sxs-lookup"><span data-stu-id="48ab3-359">**MaxProcessMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-360">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48ab3-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-362">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="48ab3-362">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-363">Número máximo, en kilobytes, de memoria que se puede asignar a un proceso.</span><span class="sxs-lookup"><span data-stu-id="48ab3-363">Maximum number, in kilobytes, of memory that can be allocated to a process.</span></span> <span data-ttu-id="48ab3-364">En el caso de los sistemas operativos sin memoria virtual, normalmente este valor es igual a la cantidad total de memoria física menos la memoria usada por el BIOS y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-364">For operating systems with no virtual memory, typically this value is equal to the total amount of physical memory minus the memory used by the BIOS and the operating system.</span></span> <span data-ttu-id="48ab3-365">En algunos sistemas operativos, este valor puede ser infinito, en cuyo caso se debe especificar 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="48ab3-365">For some operating systems, this value may be infinity, in which case 0 (zero) should be entered.</span></span> <span data-ttu-id="48ab3-366">En otros casos, este valor podría ser una constante, por ejemplo, 2G o 4G.</span><span class="sxs-lookup"><span data-stu-id="48ab3-366">In other cases, this value could be a constant, for example, 2G or 4G.</span></span>

<span data-ttu-id="48ab3-367">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="48ab3-367">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="48ab3-368">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-368">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-369">**MUILanguages**</span><span class="sxs-lookup"><span data-stu-id="48ab3-369">**MUILanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-370">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="48ab3-370">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-372">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="48ab3-372">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-373">Idiomas del paquete de interfaz de usuario multilingüe (MUI Pack) instalados en el equipo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-373">Multilingual User Interface Pack (MUI Pack ) languages installed on the computer.</span></span> <span data-ttu-id="48ab3-374">Por ejemplo, "en-US".</span><span class="sxs-lookup"><span data-stu-id="48ab3-374">For example, "en-us".</span></span> <span data-ttu-id="48ab3-375">Los idiomas del paquete MUI son archivos de recursos que se pueden instalar en la versión en inglés del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-375">MUI Pack languages are resource files that can be installed on the English version of the operating system.</span></span> <span data-ttu-id="48ab3-376">Cuando se instala un paquete MUI, puede cambiar el idioma de la interfaz de usuario a uno de los idiomas admitidos en 33.</span><span class="sxs-lookup"><span data-stu-id="48ab3-376">When an MUI Pack is installed, you can can change the user interface language to one of 33 supported languages.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-377">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="48ab3-377">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-378">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-378">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-379">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-380">Instancia del sistema operativo dentro de un equipo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-380">Operating system instance within a computer system.</span></span>

<span data-ttu-id="48ab3-381">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-381">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-382">**NumberOfLicensedUsers**</span><span class="sxs-lookup"><span data-stu-id="48ab3-382">**NumberOfLicensedUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-383">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48ab3-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-384">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-385">Número de licencias de usuario para el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-385">Number of user licenses for the operating system.</span></span> <span data-ttu-id="48ab3-386">Si es ilimitado, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="48ab3-386">If unlimited, enter 0 (zero).</span></span> <span data-ttu-id="48ab3-387">Si es desconocido, escriba-1.</span><span class="sxs-lookup"><span data-stu-id="48ab3-387">If unknown, enter -1.</span></span>

<span data-ttu-id="48ab3-388">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-388">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-389">**NumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="48ab3-389">**NumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-390">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48ab3-390">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-391">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-392">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-REsources-MIB. hrSystemProcesses ")</span><span class="sxs-lookup"><span data-stu-id="48ab3-392">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-393">Número de contextos de proceso cargados o en ejecución actualmente en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-393">Number of process contexts currently loaded or running on the operating system.</span></span>

<span data-ttu-id="48ab3-394">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-394">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-395">**NumberOfUsers**</span><span class="sxs-lookup"><span data-stu-id="48ab3-395">**NumberOfUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-396">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48ab3-396">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-398">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-REsources-MIB. hrSystemNumUsers ")</span><span class="sxs-lookup"><span data-stu-id="48ab3-398">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemNumUsers")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-399">Número de sesiones de usuario para las que el sistema operativo almacena información de Estado actualmente.</span><span class="sxs-lookup"><span data-stu-id="48ab3-399">Number of user sessions for which the operating system is storing state information currently.</span></span>

<span data-ttu-id="48ab3-400">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-400">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-401">**OperatingSystemSKU**</span><span class="sxs-lookup"><span data-stu-id="48ab3-401">**OperatingSystemSKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-402">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48ab3-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-404">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="48ab3-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-405">Número de referencia de almacén (SKU) para el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-405">Stock Keeping Unit (SKU) number for the operating system.</span></span> <span data-ttu-id="48ab3-406">Estos valores son los mismos que las constantes \*\* \_ \* Product\* _ definidas en Winnt. h que se usan con la función [_ *GetProductInfo* \*](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .</span><span class="sxs-lookup"><span data-stu-id="48ab3-406">These values are the same as the \**PRODUCT\_\** _ constants defined in WinNT.h that are used with the [_ *GetProductInfo*\*](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) function.</span></span>

<span data-ttu-id="48ab3-407">En la lista siguiente se enumeran los posibles valores de SKU.</span><span class="sxs-lookup"><span data-stu-id="48ab3-407">The following list lists possible SKU values.</span></span>

<dt>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>

<span data-ttu-id="48ab3-408"><span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**Producto \_ de Undefined** (0)</span><span class="sxs-lookup"><span data-stu-id="48ab3-408"><span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**PRODUCT\_UNDEFINED** (0)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-409">No definido</span><span class="sxs-lookup"><span data-stu-id="48ab3-409">Undefined</span></span>

</dd> <dt>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>

<span data-ttu-id="48ab3-410"><span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**Producto \_ de ULTIMATE** (1)</span><span class="sxs-lookup"><span data-stu-id="48ab3-410"><span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**PRODUCT\_ULTIMATE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-411">Ultimate Edition, por ejemplo, Windows Vista Ultimate.</span><span class="sxs-lookup"><span data-stu-id="48ab3-411">Ultimate Edition, e.g. Windows Vista Ultimate.</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>

<span data-ttu-id="48ab3-412"><span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**Producto \_ de HOME \_ Basic** (2)</span><span class="sxs-lookup"><span data-stu-id="48ab3-412"><span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**PRODUCT\_HOME\_BASIC** (2)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-413">Home Basic Edition</span><span class="sxs-lookup"><span data-stu-id="48ab3-413">Home Basic Edition</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>

<span data-ttu-id="48ab3-414"><span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**Producto \_ de HOME \_ Premium** (3)</span><span class="sxs-lookup"><span data-stu-id="48ab3-414"><span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**PRODUCT\_HOME\_PREMIUM** (3)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-415">Home Premium Edition</span><span class="sxs-lookup"><span data-stu-id="48ab3-415">Home Premium Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>

<span data-ttu-id="48ab3-416"><span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**Producto \_ de ENTERPRISE** (4)</span><span class="sxs-lookup"><span data-stu-id="48ab3-416"><span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**PRODUCT\_ENTERPRISE** (4)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-417">Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="48ab3-417">Enterprise Edition</span></span>

</dd> <dt>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>

<span data-ttu-id="48ab3-418"><span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**Producto \_ de EMPRESA** (6)</span><span class="sxs-lookup"><span data-stu-id="48ab3-418"><span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**PRODUCT\_BUSINESS** (6)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-419">Business Edition</span><span class="sxs-lookup"><span data-stu-id="48ab3-419">Business Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>

<span data-ttu-id="48ab3-420"><span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**Producto \_ de STANDARD \_ Server** (7)</span><span class="sxs-lookup"><span data-stu-id="48ab3-420"><span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**PRODUCT\_STANDARD\_SERVER** (7)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-421">Windows Server Standard Edition (instalación de experiencia de escritorio)</span><span class="sxs-lookup"><span data-stu-id="48ab3-421">Windows Server Standard Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>

<span data-ttu-id="48ab3-422"><span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**Producto \_ de Datacenter \_ Server** (8)</span><span class="sxs-lookup"><span data-stu-id="48ab3-422"><span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**PRODUCT\_DATACENTER\_SERVER** (8)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-423">Windows Server Datacenter Edition (instalación de experiencia de escritorio)</span><span class="sxs-lookup"><span data-stu-id="48ab3-423">Windows Server Datacenter Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>

<span data-ttu-id="48ab3-424"><span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**Producto \_ de \_Servidor SMALLBUSINESS** (9)</span><span class="sxs-lookup"><span data-stu-id="48ab3-424"><span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**PRODUCT\_SMALLBUSINESS\_SERVER** (9)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-425">Edición de Small Business Server</span><span class="sxs-lookup"><span data-stu-id="48ab3-425">Small Business Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>

<span data-ttu-id="48ab3-426"><span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**Producto \_ de ENTERPRISE \_ Server** (10)</span><span class="sxs-lookup"><span data-stu-id="48ab3-426"><span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**PRODUCT\_ENTERPRISE\_SERVER** (10)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-427">Edición Enterprise Server</span><span class="sxs-lookup"><span data-stu-id="48ab3-427">Enterprise Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>

<span data-ttu-id="48ab3-428"><span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**Producto \_ de Inicio** (11)</span><span class="sxs-lookup"><span data-stu-id="48ab3-428"><span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**PRODUCT\_STARTER** (11)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-429"> Starter Edition</span><span class="sxs-lookup"><span data-stu-id="48ab3-429">Starter Edition</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>

<span data-ttu-id="48ab3-430"><span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**Producto \_ de Datacenter \_ Server \_ Core** (12)</span><span class="sxs-lookup"><span data-stu-id="48ab3-430"><span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**PRODUCT\_DATACENTER\_SERVER\_CORE** (12)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-431">Datacenter Server Core Edition</span><span class="sxs-lookup"><span data-stu-id="48ab3-431">Datacenter Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>

<span data-ttu-id="48ab3-432"><span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**Producto \_ de STANDARD \_ Server \_ Core** (13)</span><span class="sxs-lookup"><span data-stu-id="48ab3-432"><span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**PRODUCT\_STANDARD\_SERVER\_CORE** (13)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-433">Standard Server Core Edition</span><span class="sxs-lookup"><span data-stu-id="48ab3-433">Standard Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>

<span data-ttu-id="48ab3-434"><span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**Producto \_ de ENTERPRISE \_ Server \_ Core** (14)</span><span class="sxs-lookup"><span data-stu-id="48ab3-434"><span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**PRODUCT\_ENTERPRISE\_SERVER\_CORE** (14)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-435">Enterprise Server Core Edition</span><span class="sxs-lookup"><span data-stu-id="48ab3-435">Enterprise Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>

<span data-ttu-id="48ab3-436"><span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**Producto \_ de \_Servidor Web** (17)</span><span class="sxs-lookup"><span data-stu-id="48ab3-436"><span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**PRODUCT\_WEB\_SERVER** (17)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-437">Edición del servidor Web</span><span class="sxs-lookup"><span data-stu-id="48ab3-437">Web Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>

<span data-ttu-id="48ab3-438"><span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**Producto \_ de \_Servidor principal** (19)</span><span class="sxs-lookup"><span data-stu-id="48ab3-438"><span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**PRODUCT\_HOME\_SERVER** (19)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-439">Home Server Edition</span><span class="sxs-lookup"><span data-stu-id="48ab3-439">Home Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>

<span data-ttu-id="48ab3-440"><span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**Producto \_ de \_ \_ Servidor de almacenamiento rápido** (20)</span><span class="sxs-lookup"><span data-stu-id="48ab3-440"><span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**PRODUCT\_STORAGE\_EXPRESS\_SERVER** (20)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-441">Storage Express Server Edition</span><span class="sxs-lookup"><span data-stu-id="48ab3-441">Storage Express Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>

<span data-ttu-id="48ab3-442"><span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**Producto \_ de STORAGE \_ Standard \_ Server** (21)</span><span class="sxs-lookup"><span data-stu-id="48ab3-442"><span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**PRODUCT\_STORAGE\_STANDARD\_SERVER** (21)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-443">Windows Storage Server Standard Edition (instalación de experiencia de escritorio)</span><span class="sxs-lookup"><span data-stu-id="48ab3-443">Windows Storage Server Standard Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>

<span data-ttu-id="48ab3-444"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**Producto \_ de \_ \_ Servidor de grupo de trabajo de almacenamiento** (22)</span><span class="sxs-lookup"><span data-stu-id="48ab3-444"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**PRODUCT\_STORAGE\_WORKGROUP\_SERVER** (22)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-445">Windows Storage Server Workgroup Edition (instalación de experiencia de escritorio)</span><span class="sxs-lookup"><span data-stu-id="48ab3-445">Windows Storage Server Workgroup Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>

<span data-ttu-id="48ab3-446"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**Producto \_ de STORAGE \_ Enterprise \_ Server** (23)</span><span class="sxs-lookup"><span data-stu-id="48ab3-446"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**PRODUCT\_STORAGE\_ENTERPRISE\_SERVER** (23)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-447">Storage Enterprise Server Edition</span><span class="sxs-lookup"><span data-stu-id="48ab3-447">Storage Enterprise Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>

<span data-ttu-id="48ab3-448"><span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**Producto \_ de SERVIDOR \_ para \_ SMALLBUSINESS** (24)</span><span class="sxs-lookup"><span data-stu-id="48ab3-448"><span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**PRODUCT\_SERVER\_FOR\_SMALLBUSINESS** (24)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-449">Servidor para Small Business Edition</span><span class="sxs-lookup"><span data-stu-id="48ab3-449">Server For Small Business Edition</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>

<span data-ttu-id="48ab3-450"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**Producto \_ de SMALLBUSINESS \_ Server \_ Premium** (25)</span><span class="sxs-lookup"><span data-stu-id="48ab3-450"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**PRODUCT\_SMALLBUSINESS\_SERVER\_PREMIUM** (25)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-451">Edición Premium de Small Business Server</span><span class="sxs-lookup"><span data-stu-id="48ab3-451">Small Business Server Premium Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>

<span data-ttu-id="48ab3-452"><span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**Producto \_ de ENTERPRISE \_ N** (27)</span><span class="sxs-lookup"><span data-stu-id="48ab3-452"><span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**PRODUCT\_ENTERPRISE\_N** (27)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-453">Edición Enterprise de Windows</span><span class="sxs-lookup"><span data-stu-id="48ab3-453">Windows Enterprise Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>

<span data-ttu-id="48ab3-454"><span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**Producto \_ de ULTIMATE \_ N** (28)</span><span class="sxs-lookup"><span data-stu-id="48ab3-454"><span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**PRODUCT\_ULTIMATE\_N** (28)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-455">Windows Ultimate Edition</span><span class="sxs-lookup"><span data-stu-id="48ab3-455">Windows Ultimate Edition</span></span>

</dd> <dt>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>

<span data-ttu-id="48ab3-456"><span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**Producto \_ de \_Servidor Web \_ Core** (29)</span><span class="sxs-lookup"><span data-stu-id="48ab3-456"><span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**PRODUCT\_WEB\_SERVER\_CORE** (29)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-457">Windows Server Web Server Edition (instalación Server Core)</span><span class="sxs-lookup"><span data-stu-id="48ab3-457">Windows Server Web Server Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>

<span data-ttu-id="48ab3-458"><span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**Producto \_ de STANDARD \_ Server \_ V** (36)</span><span class="sxs-lookup"><span data-stu-id="48ab3-458"><span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**PRODUCT\_STANDARD\_SERVER\_V** (36)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-459">Windows Server Standard Edition sin Hyper-V</span><span class="sxs-lookup"><span data-stu-id="48ab3-459">Windows Server Standard Edition without Hyper-V</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>

<span data-ttu-id="48ab3-460"><span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**Producto \_ de Datacenter \_ Server \_ V** (37)</span><span class="sxs-lookup"><span data-stu-id="48ab3-460"><span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**PRODUCT\_DATACENTER\_SERVER\_V** (37)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-461">Windows Server Datacenter Edition sin Hyper-V (instalación completa)</span><span class="sxs-lookup"><span data-stu-id="48ab3-461">Windows Server Datacenter Edition without Hyper-V (full installation)</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>

<span data-ttu-id="48ab3-462"><span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**Producto \_ de ENTERPRISE \_ Server \_ V** (38)</span><span class="sxs-lookup"><span data-stu-id="48ab3-462"><span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**PRODUCT\_ENTERPRISE\_SERVER\_V** (38)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-463">Windows Server Enterprise Edition sin Hyper-V (instalación completa)</span><span class="sxs-lookup"><span data-stu-id="48ab3-463">Windows Server Enterprise Edition without Hyper-V (full installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>

<span data-ttu-id="48ab3-464"><span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**Producto \_ de Datacenter \_ Server \_ Core \_ V** (39)</span><span class="sxs-lookup"><span data-stu-id="48ab3-464"><span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**PRODUCT\_DATACENTER\_SERVER\_CORE\_V** (39)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-465">Windows Server Datacenter Edition sin Hyper-V (instalación Server Core)</span><span class="sxs-lookup"><span data-stu-id="48ab3-465">Windows Server Datacenter Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>

<span data-ttu-id="48ab3-466"><span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**Producto \_ de STANDARD \_ Server \_ Core \_ V** (40)</span><span class="sxs-lookup"><span data-stu-id="48ab3-466"><span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**PRODUCT\_STANDARD\_SERVER\_CORE\_V** (40)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-467">Windows Server Standard Edition sin Hyper-V (instalación Server Core)</span><span class="sxs-lookup"><span data-stu-id="48ab3-467">Windows Server Standard Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>

<span data-ttu-id="48ab3-468"><span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**Producto \_ de ENTERPRISE \_ Server \_ Core \_ V** (41)</span><span class="sxs-lookup"><span data-stu-id="48ab3-468"><span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**PRODUCT\_ENTERPRISE\_SERVER\_CORE\_V** (41)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-469">Windows Server Enterprise Edition sin Hyper-V (instalación Server Core)</span><span class="sxs-lookup"><span data-stu-id="48ab3-469">Windows Server Enterprise Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>

<span data-ttu-id="48ab3-470"><span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**Producto \_ de HYPERV** (42)</span><span class="sxs-lookup"><span data-stu-id="48ab3-470"><span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**PRODUCT\_HYPERV** (42)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-471">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="48ab3-471">Microsoft Hyper-V Server</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>

<span data-ttu-id="48ab3-472"><span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**Producto \_ de STORAGE \_ Express \_ Server \_ Core** (43)</span><span class="sxs-lookup"><span data-stu-id="48ab3-472"><span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**PRODUCT\_STORAGE\_EXPRESS\_SERVER\_CORE** (43)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-473">Storage Server Express Edition (instalación Server Core)</span><span class="sxs-lookup"><span data-stu-id="48ab3-473">Storage Server Express Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>

<span data-ttu-id="48ab3-474"><span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**Producto \_ de STORAGE \_ Standard \_ Server \_ Core** (44)</span><span class="sxs-lookup"><span data-stu-id="48ab3-474"><span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**PRODUCT\_STORAGE\_STANDARD\_SERVER\_CORE** (44)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-475">Storage Server Standard Edition (instalación Server Core)</span><span class="sxs-lookup"><span data-stu-id="48ab3-475">Storage Server Standard Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>

<span data-ttu-id="48ab3-476"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**Producto \_ de STORAGE \_ Workgroup \_ Server \_ Core** (45)</span><span class="sxs-lookup"><span data-stu-id="48ab3-476"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**PRODUCT\_STORAGE\_WORKGROUP\_SERVER\_CORE** (45)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-477">Storage Server Workgroup Edition (instalación Server Core)</span><span class="sxs-lookup"><span data-stu-id="48ab3-477">Storage Server Workgroup Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>

<span data-ttu-id="48ab3-478"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**Producto \_ de STORAGE \_ Enterprise \_ Server \_ Core** (46)</span><span class="sxs-lookup"><span data-stu-id="48ab3-478"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**PRODUCT\_STORAGE\_ENTERPRISE\_SERVER\_CORE** (46)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-479">Storage Server Workgroup Edition (instalación Server Core)</span><span class="sxs-lookup"><span data-stu-id="48ab3-479">Storage Server Workgroup Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>

<span data-ttu-id="48ab3-480"><span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**Producto \_ de PROFESSIONAL** (48)</span><span class="sxs-lookup"><span data-stu-id="48ab3-480"><span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**PRODUCT\_PROFESSIONAL** (48)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-481">Windows Professional</span><span class="sxs-lookup"><span data-stu-id="48ab3-481">Windows Professional</span></span>

</dd> <dt>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>

<span data-ttu-id="48ab3-482"><span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**Producto \_ de \_ \_ Servidor de soluciones SB** (50)</span><span class="sxs-lookup"><span data-stu-id="48ab3-482"><span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**PRODUCT\_SB\_SOLUTION\_SERVER** (50)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-483">Windows Server Essentials (instalación de experiencia de escritorio)</span><span class="sxs-lookup"><span data-stu-id="48ab3-483">Windows Server Essentials (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>

<span data-ttu-id="48ab3-484"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**Producto \_ de Servidor de SMALLBUSINESS \_ \_ Premium \_ Core** (63)</span><span class="sxs-lookup"><span data-stu-id="48ab3-484"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**PRODUCT\_SMALLBUSINESS\_SERVER\_PREMIUM\_CORE** (63)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-485">Small Business Server Premium (instalación Server Core)</span><span class="sxs-lookup"><span data-stu-id="48ab3-485">Small Business Server Premium (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>

<span data-ttu-id="48ab3-486"><span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**Producto \_ de CLUSTER \_ Server \_ V** (64)</span><span class="sxs-lookup"><span data-stu-id="48ab3-486"><span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**PRODUCT\_CLUSTER\_SERVER\_V** (64)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-487">Windows Compute Cluster Server sin Hyper-V</span><span class="sxs-lookup"><span data-stu-id="48ab3-487">Windows Compute Cluster Server without Hyper-V</span></span>

</dd> <dt>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>

<span data-ttu-id="48ab3-488"><span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**Producto \_ de CORE \_ ARM** (97)</span><span class="sxs-lookup"><span data-stu-id="48ab3-488"><span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**PRODUCT\_CORE\_ARM** (97)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-489">Windows RT</span><span class="sxs-lookup"><span data-stu-id="48ab3-489">Windows RT</span></span>

</dd> <dt>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>

<span data-ttu-id="48ab3-490"><span id="PRODUCT_CORE"></span><span id="product_core"></span>**Producto \_ de NÚCLEO** (101)</span><span class="sxs-lookup"><span data-stu-id="48ab3-490"><span id="PRODUCT_CORE"></span><span id="product_core"></span>**PRODUCT\_CORE** (101)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-491">Inicio de Windows</span><span class="sxs-lookup"><span data-stu-id="48ab3-491">Windows Home</span></span>

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>

<span data-ttu-id="48ab3-492"><span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**Producto \_ de PROFESSIONAL \_ WMC** (103)</span><span class="sxs-lookup"><span data-stu-id="48ab3-492"><span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**PRODUCT\_PROFESSIONAL\_WMC** (103)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-493">Windows Professional con Media Center</span><span class="sxs-lookup"><span data-stu-id="48ab3-493">Windows Professional with Media Center</span></span>

</dd> <dt>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>

<span data-ttu-id="48ab3-494"><span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**Producto \_ de MOBILE \_ Core** (104)</span><span class="sxs-lookup"><span data-stu-id="48ab3-494"><span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**PRODUCT\_MOBILE\_CORE** (104)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-495">Windows Mobile</span><span class="sxs-lookup"><span data-stu-id="48ab3-495">Windows Mobile</span></span>

</dd> <dt>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>

<span data-ttu-id="48ab3-496"><span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**Producto \_ de IOTUAP** (123)</span><span class="sxs-lookup"><span data-stu-id="48ab3-496"><span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**PRODUCT\_IOTUAP** (123)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-497">Windows IoT (Internet de las cosas) Core</span><span class="sxs-lookup"><span data-stu-id="48ab3-497">Windows IoT (Internet of Things) Core</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>

<span data-ttu-id="48ab3-498"><span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**Producto \_ de Datacenter \_ nano \_ SERVER** (143)</span><span class="sxs-lookup"><span data-stu-id="48ab3-498"><span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**PRODUCT\_DATACENTER\_NANO\_SERVER** (143)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-499">Windows Server Datacenter Edition (instalación de nano Server)</span><span class="sxs-lookup"><span data-stu-id="48ab3-499">Windows Server Datacenter Edition (Nano Server installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>

<span data-ttu-id="48ab3-500"><span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**Producto \_ de \_Nano \_ Server estándar** (144)</span><span class="sxs-lookup"><span data-stu-id="48ab3-500"><span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**PRODUCT\_STANDARD\_NANO\_SERVER** (144)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-501">Windows Server Standard Edition (instalación de nano Server)</span><span class="sxs-lookup"><span data-stu-id="48ab3-501">Windows Server Standard Edition (Nano Server installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>

<span data-ttu-id="48ab3-502"><span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**Producto \_ de Datacenter \_ WS \_ Server \_ Core** (147)</span><span class="sxs-lookup"><span data-stu-id="48ab3-502"><span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**PRODUCT\_DATACENTER\_WS\_SERVER\_CORE** (147)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-503">Windows Server Datacenter Edition (instalación Server Core)</span><span class="sxs-lookup"><span data-stu-id="48ab3-503">Windows Server Datacenter Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>

<span data-ttu-id="48ab3-504"><span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**Producto \_ de STANDARD \_ WS \_ Server \_ Core** (148)</span><span class="sxs-lookup"><span data-stu-id="48ab3-504"><span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**PRODUCT\_STANDARD\_WS\_SERVER\_CORE** (148)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-505">Windows Server Standard Edition (instalación Server Core)</span><span class="sxs-lookup"><span data-stu-id="48ab3-505">Windows Server Standard Edition (Server Core installation)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="48ab3-506">**Organización**</span><span class="sxs-lookup"><span data-stu-id="48ab3-506">**Organization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-507">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-507">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-508">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-508">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-509">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| RegisteredOrganization")</span><span class="sxs-lookup"><span data-stu-id="48ab3-509">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows\\\\CurrentVersion\|RegisteredOrganization")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-510">Nombre de la compañía para el usuario registrado del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-510">Company name for the registered user of the operating system.</span></span>

<span data-ttu-id="48ab3-511">Ejemplo: "Microsoft Corporation"</span><span class="sxs-lookup"><span data-stu-id="48ab3-511">Example: "Microsoft Corporation"</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-512">**OSArchitecture**</span><span class="sxs-lookup"><span data-stu-id="48ab3-512">**OSArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-513">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-513">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-514">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-515">Arquitectura del sistema operativo, en lugar del procesador.</span><span class="sxs-lookup"><span data-stu-id="48ab3-515">Architecture of the operating system, as opposed to the processor.</span></span> <span data-ttu-id="48ab3-516">Esta propiedad se puede localizar.</span><span class="sxs-lookup"><span data-stu-id="48ab3-516">This property can be localized.</span></span>

<span data-ttu-id="48ab3-517">Ejemplo: 32 bits</span><span class="sxs-lookup"><span data-stu-id="48ab3-517">Example: 32-bit</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-518">**OSLanguage**</span><span class="sxs-lookup"><span data-stu-id="48ab3-518">**OSLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-519">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48ab3-519">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-520">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-520">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-521">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ \\ \\ configuración regional internacional del panel de control \| ")</span><span class="sxs-lookup"><span data-stu-id="48ab3-521">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|DEFAULT\\\\Control Panel\\\\International\|Locale")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-522">Versión de idioma del sistema operativo instalado.</span><span class="sxs-lookup"><span data-stu-id="48ab3-522">Language version of the operating system installed.</span></span> <span data-ttu-id="48ab3-523">En la lista siguiente se enumeran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="48ab3-523">The following list lists the possible values.</span></span> <span data-ttu-id="48ab3-524">Ejemplo: 0x0807 (alemán, Suiza).</span><span class="sxs-lookup"><span data-stu-id="48ab3-524">Example: 0x0807 (German, Switzerland).</span></span>

<dt>

<span data-ttu-id="48ab3-525">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="48ab3-525">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-526">Árabe</span><span class="sxs-lookup"><span data-stu-id="48ab3-526">Arabic</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-527">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="48ab3-527">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-528">Chino (simplificado) – China</span><span class="sxs-lookup"><span data-stu-id="48ab3-528">Chinese (Simplified)– China</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-529">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="48ab3-529">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-530">Inglés</span><span class="sxs-lookup"><span data-stu-id="48ab3-530">English</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-531">1025 (0x401)</span><span class="sxs-lookup"><span data-stu-id="48ab3-531">1025 (0x401)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-532">Árabe – Arabia Saudí</span><span class="sxs-lookup"><span data-stu-id="48ab3-532">Arabic – Saudi Arabia</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-533">1026 (0x402)</span><span class="sxs-lookup"><span data-stu-id="48ab3-533">1026 (0x402)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-534">Búlgaro</span><span class="sxs-lookup"><span data-stu-id="48ab3-534">Bulgarian</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-535">1027 (0x403)</span><span class="sxs-lookup"><span data-stu-id="48ab3-535">1027 (0x403)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-536">Catalán</span><span class="sxs-lookup"><span data-stu-id="48ab3-536">Catalan</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-537">1028 (0x404)</span><span class="sxs-lookup"><span data-stu-id="48ab3-537">1028 (0x404)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-538">Chino (tradicional) – Taiwán</span><span class="sxs-lookup"><span data-stu-id="48ab3-538">Chinese (Traditional) – Taiwan</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-539">1029 (0x405)</span><span class="sxs-lookup"><span data-stu-id="48ab3-539">1029 (0x405)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-540">Checo</span><span class="sxs-lookup"><span data-stu-id="48ab3-540">Czech</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-541">1030 (0x406)</span><span class="sxs-lookup"><span data-stu-id="48ab3-541">1030 (0x406)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-542">Danés</span><span class="sxs-lookup"><span data-stu-id="48ab3-542">Danish</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-543">1031 (0x407)</span><span class="sxs-lookup"><span data-stu-id="48ab3-543">1031 (0x407)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-544">Alemán – Alemania</span><span class="sxs-lookup"><span data-stu-id="48ab3-544">German – Germany</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-545">1032 (0x408)</span><span class="sxs-lookup"><span data-stu-id="48ab3-545">1032 (0x408)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-546">Griego</span><span class="sxs-lookup"><span data-stu-id="48ab3-546">Greek</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-547">1033 (0xC0A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-547">1033 (0x409)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-548">Inglés – Estados Unidos</span><span class="sxs-lookup"><span data-stu-id="48ab3-548">English – United States</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-549">1034 (0x40A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-549">1034 (0x40A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-550">Español – Alfabetización tradicional</span><span class="sxs-lookup"><span data-stu-id="48ab3-550">Spanish – Traditional Sort</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-551">1035 (0x40B)</span><span class="sxs-lookup"><span data-stu-id="48ab3-551">1035 (0x40B)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-552">Finés</span><span class="sxs-lookup"><span data-stu-id="48ab3-552">Finnish</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-553">1036 (0x40C)</span><span class="sxs-lookup"><span data-stu-id="48ab3-553">1036 (0x40C)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-554">Francés – Francia</span><span class="sxs-lookup"><span data-stu-id="48ab3-554">French – France</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-555">1037 (0x40D)</span><span class="sxs-lookup"><span data-stu-id="48ab3-555">1037 (0x40D)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-556">Hebreo</span><span class="sxs-lookup"><span data-stu-id="48ab3-556">Hebrew</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-557">1038 (0x40E)</span><span class="sxs-lookup"><span data-stu-id="48ab3-557">1038 (0x40E)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-558">Húngaro</span><span class="sxs-lookup"><span data-stu-id="48ab3-558">Hungarian</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-559">1039 (0x40F)</span><span class="sxs-lookup"><span data-stu-id="48ab3-559">1039 (0x40F)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-560">Islandés</span><span class="sxs-lookup"><span data-stu-id="48ab3-560">Icelandic</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-561">1040 (0x410)</span><span class="sxs-lookup"><span data-stu-id="48ab3-561">1040 (0x410)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-562">Italiano – Italia</span><span class="sxs-lookup"><span data-stu-id="48ab3-562">Italian – Italy</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-563">1041 (0x411)</span><span class="sxs-lookup"><span data-stu-id="48ab3-563">1041 (0x411)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-564">Japonés</span><span class="sxs-lookup"><span data-stu-id="48ab3-564">Japanese</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-565">1042 (0x412)</span><span class="sxs-lookup"><span data-stu-id="48ab3-565">1042 (0x412)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-566">Coreano</span><span class="sxs-lookup"><span data-stu-id="48ab3-566">Korean</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-567">1043 (0x413)</span><span class="sxs-lookup"><span data-stu-id="48ab3-567">1043 (0x413)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-568">Neerlandés – Países Bajos</span><span class="sxs-lookup"><span data-stu-id="48ab3-568">Dutch – Netherlands</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-569">1044 (0x414)</span><span class="sxs-lookup"><span data-stu-id="48ab3-569">1044 (0x414)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-570">Noruego – Bokmal</span><span class="sxs-lookup"><span data-stu-id="48ab3-570">Norwegian – Bokmal</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-571">1045 (0x415)</span><span class="sxs-lookup"><span data-stu-id="48ab3-571">1045 (0x415)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-572">Polaco</span><span class="sxs-lookup"><span data-stu-id="48ab3-572">Polish</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-573">1046 (0x416)</span><span class="sxs-lookup"><span data-stu-id="48ab3-573">1046 (0x416)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-574">Portugués – Brasil</span><span class="sxs-lookup"><span data-stu-id="48ab3-574">Portuguese – Brazil</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-575">1047 (0x417)</span><span class="sxs-lookup"><span data-stu-id="48ab3-575">1047 (0x417)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-576">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="48ab3-576">Rhaeto-Romanic</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-577">1048 (0x418)</span><span class="sxs-lookup"><span data-stu-id="48ab3-577">1048 (0x418)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-578">Rumano</span><span class="sxs-lookup"><span data-stu-id="48ab3-578">Romanian</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-579">1049 (0x419)</span><span class="sxs-lookup"><span data-stu-id="48ab3-579">1049 (0x419)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-580">Ruso</span><span class="sxs-lookup"><span data-stu-id="48ab3-580">Russian</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-581">1050 (0x41A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-581">1050 (0x41A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-582">Croata</span><span class="sxs-lookup"><span data-stu-id="48ab3-582">Croatian</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-583">1051 (0x41B)</span><span class="sxs-lookup"><span data-stu-id="48ab3-583">1051 (0x41B)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-584">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="48ab3-584">Slovak</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-585">1052 (0x41C)</span><span class="sxs-lookup"><span data-stu-id="48ab3-585">1052 (0x41C)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-586">Albanés</span><span class="sxs-lookup"><span data-stu-id="48ab3-586">Albanian</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-587">1053 (0x41D)</span><span class="sxs-lookup"><span data-stu-id="48ab3-587">1053 (0x41D)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-588">Sueco</span><span class="sxs-lookup"><span data-stu-id="48ab3-588">Swedish</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-589">1054 (0x41E)</span><span class="sxs-lookup"><span data-stu-id="48ab3-589">1054 (0x41E)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-590">Tailandés</span><span class="sxs-lookup"><span data-stu-id="48ab3-590">Thai</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-591">1055 (0x41F)</span><span class="sxs-lookup"><span data-stu-id="48ab3-591">1055 (0x41F)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-592">Turco</span><span class="sxs-lookup"><span data-stu-id="48ab3-592">Turkish</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-593">1056 (0x420)</span><span class="sxs-lookup"><span data-stu-id="48ab3-593">1056 (0x420)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-594">Urdu</span><span class="sxs-lookup"><span data-stu-id="48ab3-594">Urdu</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-595">1057 (0x421)</span><span class="sxs-lookup"><span data-stu-id="48ab3-595">1057 (0x421)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-596">Indonesio</span><span class="sxs-lookup"><span data-stu-id="48ab3-596">Indonesian</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-597">1058 (0x422)</span><span class="sxs-lookup"><span data-stu-id="48ab3-597">1058 (0x422)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-598">Ucraniano</span><span class="sxs-lookup"><span data-stu-id="48ab3-598">Ukrainian</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-599">1059 (0x423)</span><span class="sxs-lookup"><span data-stu-id="48ab3-599">1059 (0x423)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-600">Bielorruso</span><span class="sxs-lookup"><span data-stu-id="48ab3-600">Belarusian</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-601">1060 (0x424)</span><span class="sxs-lookup"><span data-stu-id="48ab3-601">1060 (0x424)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-602">Esloveno</span><span class="sxs-lookup"><span data-stu-id="48ab3-602">Slovenian</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-603">1061 (0x425)</span><span class="sxs-lookup"><span data-stu-id="48ab3-603">1061 (0x425)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-604">Estonio</span><span class="sxs-lookup"><span data-stu-id="48ab3-604">Estonian</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-605">1062 (0x426 al)</span><span class="sxs-lookup"><span data-stu-id="48ab3-605">1062 (0x426)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-606">Letón</span><span class="sxs-lookup"><span data-stu-id="48ab3-606">Latvian</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-607">1063 (0x427)</span><span class="sxs-lookup"><span data-stu-id="48ab3-607">1063 (0x427)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-608">Lituano</span><span class="sxs-lookup"><span data-stu-id="48ab3-608">Lithuanian</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-609">1065 (0x429)</span><span class="sxs-lookup"><span data-stu-id="48ab3-609">1065 (0x429)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-610">Persa</span><span class="sxs-lookup"><span data-stu-id="48ab3-610">Persian</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-611">1066 (0x42A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-611">1066 (0x42A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-612">Vietnamita</span><span class="sxs-lookup"><span data-stu-id="48ab3-612">Vietnamese</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-613">1069 (0x42D)</span><span class="sxs-lookup"><span data-stu-id="48ab3-613">1069 (0x42D)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-614">Vasco (España)</span><span class="sxs-lookup"><span data-stu-id="48ab3-614">Basque (Basque)</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-615">1070 (0x42E)</span><span class="sxs-lookup"><span data-stu-id="48ab3-615">1070 (0x42E)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-616">Serbio</span><span class="sxs-lookup"><span data-stu-id="48ab3-616">Serbian</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-617">1071 (0x42F)</span><span class="sxs-lookup"><span data-stu-id="48ab3-617">1071 (0x42F)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-618">Macedonio (norte de Macedonia)</span><span class="sxs-lookup"><span data-stu-id="48ab3-618">Macedonian (North Macedonia)</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-619">1072 (0x430)</span><span class="sxs-lookup"><span data-stu-id="48ab3-619">1072 (0x430)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-620">Sutu</span><span class="sxs-lookup"><span data-stu-id="48ab3-620">Sutu</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-621">1073 (0x431)</span><span class="sxs-lookup"><span data-stu-id="48ab3-621">1073 (0x431)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-622">Tsonga</span><span class="sxs-lookup"><span data-stu-id="48ab3-622">Tsonga</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-623">1074 (0x432)</span><span class="sxs-lookup"><span data-stu-id="48ab3-623">1074 (0x432)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-624">Setswana</span><span class="sxs-lookup"><span data-stu-id="48ab3-624">Tswana</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-625">1076 (0x434)</span><span class="sxs-lookup"><span data-stu-id="48ab3-625">1076 (0x434)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-626">Xhosa</span><span class="sxs-lookup"><span data-stu-id="48ab3-626">Xhosa</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-627">1077 (0x435)</span><span class="sxs-lookup"><span data-stu-id="48ab3-627">1077 (0x435)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-628">Zulú</span><span class="sxs-lookup"><span data-stu-id="48ab3-628">Zulu</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-629">1078 (0x436)</span><span class="sxs-lookup"><span data-stu-id="48ab3-629">1078 (0x436)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-630">Afrikáans</span><span class="sxs-lookup"><span data-stu-id="48ab3-630">Afrikaans</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-631">1080 (0x438)</span><span class="sxs-lookup"><span data-stu-id="48ab3-631">1080 (0x438)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-632">Faroés</span><span class="sxs-lookup"><span data-stu-id="48ab3-632">Faeroese</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-633">1081 (0x439)</span><span class="sxs-lookup"><span data-stu-id="48ab3-633">1081 (0x439)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-634">Hindi</span><span class="sxs-lookup"><span data-stu-id="48ab3-634">Hindi</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-635">1082 (0x43A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-635">1082 (0x43A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-636">Maltés</span><span class="sxs-lookup"><span data-stu-id="48ab3-636">Maltese</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-637">1084 (0x43C)</span><span class="sxs-lookup"><span data-stu-id="48ab3-637">1084 (0x43C)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-638">Gaélico escocés (Reino Unido)</span><span class="sxs-lookup"><span data-stu-id="48ab3-638">Scottish Gaelic (United Kingdom)</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-639">1085 (0x43D)</span><span class="sxs-lookup"><span data-stu-id="48ab3-639">1085 (0x43D)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-640">Yidis</span><span class="sxs-lookup"><span data-stu-id="48ab3-640">Yiddish</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-641">1086 (establézcalo 0x43e)</span><span class="sxs-lookup"><span data-stu-id="48ab3-641">1086 (0x43E)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-642">Malayo: Malasia</span><span class="sxs-lookup"><span data-stu-id="48ab3-642">Malay – Malaysia</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-643">2049 (0x801)</span><span class="sxs-lookup"><span data-stu-id="48ab3-643">2049 (0x801)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-644">Árabe – Iraq</span><span class="sxs-lookup"><span data-stu-id="48ab3-644">Arabic – Iraq</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-645">2052 (0x804)</span><span class="sxs-lookup"><span data-stu-id="48ab3-645">2052 (0x804)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-646">Chino (simplificado) – PRC</span><span class="sxs-lookup"><span data-stu-id="48ab3-646">Chinese (Simplified) – PRC</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-647">2055 (0x807)</span><span class="sxs-lookup"><span data-stu-id="48ab3-647">2055 (0x807)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-648">Alemán – Suiza</span><span class="sxs-lookup"><span data-stu-id="48ab3-648">German – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-649">2057 (0x809)</span><span class="sxs-lookup"><span data-stu-id="48ab3-649">2057 (0x809)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-650">Inglés (Reino Unido)</span><span class="sxs-lookup"><span data-stu-id="48ab3-650">English – United Kingdom</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-651">2058 (0x80A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-651">2058 (0x80A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-652">Español – México</span><span class="sxs-lookup"><span data-stu-id="48ab3-652">Spanish – Mexico</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-653">2060 (0x80C)</span><span class="sxs-lookup"><span data-stu-id="48ab3-653">2060 (0x80C)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-654">Francés (Bélgica)</span><span class="sxs-lookup"><span data-stu-id="48ab3-654">French – Belgium</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-655">2064 (0x810)</span><span class="sxs-lookup"><span data-stu-id="48ab3-655">2064 (0x810)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-656">Italiano – Suiza</span><span class="sxs-lookup"><span data-stu-id="48ab3-656">Italian – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-657">2067 (0x813)</span><span class="sxs-lookup"><span data-stu-id="48ab3-657">2067 (0x813)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-658">Holandés – Bélgica</span><span class="sxs-lookup"><span data-stu-id="48ab3-658">Dutch – Belgium</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-659">2068 (0x814)</span><span class="sxs-lookup"><span data-stu-id="48ab3-659">2068 (0x814)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-660">Noruego – nynorsk</span><span class="sxs-lookup"><span data-stu-id="48ab3-660">Norwegian – Nynorsk</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-661">2070 (0x816)</span><span class="sxs-lookup"><span data-stu-id="48ab3-661">2070 (0x816)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-662">Portugués – Portugal</span><span class="sxs-lookup"><span data-stu-id="48ab3-662">Portuguese – Portugal</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-663">2072 (0x818)</span><span class="sxs-lookup"><span data-stu-id="48ab3-663">2072 (0x818)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-664">Rumano – Moldavia</span><span class="sxs-lookup"><span data-stu-id="48ab3-664">Romanian – Moldova</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-665">2073 (0x819)</span><span class="sxs-lookup"><span data-stu-id="48ab3-665">2073 (0x819)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-666">Ruso (Moldova)</span><span class="sxs-lookup"><span data-stu-id="48ab3-666">Russian – Moldova</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-667">2074 (0x81A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-667">2074 (0x81A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-668">Serbio: Latín</span><span class="sxs-lookup"><span data-stu-id="48ab3-668">Serbian – Latin</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-669">2077 (0x81D)</span><span class="sxs-lookup"><span data-stu-id="48ab3-669">2077 (0x81D)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-670">Sueco – Finlandia</span><span class="sxs-lookup"><span data-stu-id="48ab3-670">Swedish – Finland</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-671">3073 (0xC01)</span><span class="sxs-lookup"><span data-stu-id="48ab3-671">3073 (0xC01)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-672">Árabe – Egipto</span><span class="sxs-lookup"><span data-stu-id="48ab3-672">Arabic – Egypt</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-673">3076 (0xC04)</span><span class="sxs-lookup"><span data-stu-id="48ab3-673">3076 (0xC04)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-674">Chino (tradicional): Hong Kong RAE</span><span class="sxs-lookup"><span data-stu-id="48ab3-674">Chinese (Traditional) – Hong Kong SAR</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-675">3079 (0xC07)</span><span class="sxs-lookup"><span data-stu-id="48ab3-675">3079 (0xC07)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-676">Alemán – Austria</span><span class="sxs-lookup"><span data-stu-id="48ab3-676">German – Austria</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-677">3081 (0xC09)</span><span class="sxs-lookup"><span data-stu-id="48ab3-677">3081 (0xC09)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-678">Inglés (Australia)</span><span class="sxs-lookup"><span data-stu-id="48ab3-678">English – Australia</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-679">3082 (0xC0A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-679">3082 (0xC0A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-680">Español – alfabetización internacional</span><span class="sxs-lookup"><span data-stu-id="48ab3-680">Spanish – International Sort</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-681">3084 (0xC0C)</span><span class="sxs-lookup"><span data-stu-id="48ab3-681">3084 (0xC0C)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-682">Francés (Canadá)</span><span class="sxs-lookup"><span data-stu-id="48ab3-682">French – Canada</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-683">3098 (0xC1A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-683">3098 (0xC1A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-684">Serbio: cirílico</span><span class="sxs-lookup"><span data-stu-id="48ab3-684">Serbian – Cyrillic</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-685">4097 (0x1001)</span><span class="sxs-lookup"><span data-stu-id="48ab3-685">4097 (0x1001)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-686">Árabe – Libia</span><span class="sxs-lookup"><span data-stu-id="48ab3-686">Arabic – Libya</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-687">4100 (0x1004)</span><span class="sxs-lookup"><span data-stu-id="48ab3-687">4100 (0x1004)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-688">Chino (simplificado): Singapur</span><span class="sxs-lookup"><span data-stu-id="48ab3-688">Chinese (Simplified) – Singapore</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-689">4103 (0x1007)</span><span class="sxs-lookup"><span data-stu-id="48ab3-689">4103 (0x1007)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-690">Alemán – Luxemburgo</span><span class="sxs-lookup"><span data-stu-id="48ab3-690">German – Luxembourg</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-691">4105 (0x1009)</span><span class="sxs-lookup"><span data-stu-id="48ab3-691">4105 (0x1009)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-692">Inglés – Canadá</span><span class="sxs-lookup"><span data-stu-id="48ab3-692">English – Canada</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-693">4106 (0x100A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-693">4106 (0x100A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-694">Español – Guatemala</span><span class="sxs-lookup"><span data-stu-id="48ab3-694">Spanish – Guatemala</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-695">4108 (0x100C)</span><span class="sxs-lookup"><span data-stu-id="48ab3-695">4108 (0x100C)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-696">Francés (Suiza)</span><span class="sxs-lookup"><span data-stu-id="48ab3-696">French – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-697">5121 (0x1401)</span><span class="sxs-lookup"><span data-stu-id="48ab3-697">5121 (0x1401)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-698">Árabe (Argelia)</span><span class="sxs-lookup"><span data-stu-id="48ab3-698">Arabic – Algeria</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-699">5127 (0x1407)</span><span class="sxs-lookup"><span data-stu-id="48ab3-699">5127 (0x1407)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-700">Alemán – Liechtenstein</span><span class="sxs-lookup"><span data-stu-id="48ab3-700">German – Liechtenstein</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-701">5129 (0x1409)</span><span class="sxs-lookup"><span data-stu-id="48ab3-701">5129 (0x1409)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-702">Inglés – Nueva Zelanda</span><span class="sxs-lookup"><span data-stu-id="48ab3-702">English – New Zealand</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-703">5130 (0x140A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-703">5130 (0x140A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-704">Español – Costa Rica</span><span class="sxs-lookup"><span data-stu-id="48ab3-704">Spanish – Costa Rica</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-705">5132 (0x140C)</span><span class="sxs-lookup"><span data-stu-id="48ab3-705">5132 (0x140C)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-706">Francés – Luxemburgo</span><span class="sxs-lookup"><span data-stu-id="48ab3-706">French – Luxembourg</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-707">6145 (0x1801)</span><span class="sxs-lookup"><span data-stu-id="48ab3-707">6145 (0x1801)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-708">Árabe – Marruecos</span><span class="sxs-lookup"><span data-stu-id="48ab3-708">Arabic – Morocco</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-709">6153 (0x1809)</span><span class="sxs-lookup"><span data-stu-id="48ab3-709">6153 (0x1809)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-710">Inglés – Irlanda</span><span class="sxs-lookup"><span data-stu-id="48ab3-710">English – Ireland</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-711">6154 (0x180A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-711">6154 (0x180A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-712">Español – Panamá</span><span class="sxs-lookup"><span data-stu-id="48ab3-712">Spanish – Panama</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-713">7169 (0x1C01)</span><span class="sxs-lookup"><span data-stu-id="48ab3-713">7169 (0x1C01)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-714">Árabe – Túnez</span><span class="sxs-lookup"><span data-stu-id="48ab3-714">Arabic – Tunisia</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-715">7177 (0x1C09)</span><span class="sxs-lookup"><span data-stu-id="48ab3-715">7177 (0x1C09)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-716">Inglés (Sudáfrica)</span><span class="sxs-lookup"><span data-stu-id="48ab3-716">English – South Africa</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-717">7178 (0x1C0A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-717">7178 (0x1C0A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-718">Español (República Dominicana)</span><span class="sxs-lookup"><span data-stu-id="48ab3-718">Spanish – Dominican Republic</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-719">8193 (0x2001)</span><span class="sxs-lookup"><span data-stu-id="48ab3-719">8193 (0x2001)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-720">Árabe – Omán</span><span class="sxs-lookup"><span data-stu-id="48ab3-720">Arabic – Oman</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-721">8201 (0x2009)</span><span class="sxs-lookup"><span data-stu-id="48ab3-721">8201 (0x2009)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-722">Inglés – Jamaica</span><span class="sxs-lookup"><span data-stu-id="48ab3-722">English – Jamaica</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-723">8202 (0x200A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-723">8202 (0x200A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-724">Español – Venezuela</span><span class="sxs-lookup"><span data-stu-id="48ab3-724">Spanish – Venezuela</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-725">9217 (0x2401)</span><span class="sxs-lookup"><span data-stu-id="48ab3-725">9217 (0x2401)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-726">Árabe – Yemen</span><span class="sxs-lookup"><span data-stu-id="48ab3-726">Arabic – Yemen</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-727">9226 (0x240A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-727">9226 (0x240A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-728">Español – Colombia</span><span class="sxs-lookup"><span data-stu-id="48ab3-728">Spanish – Colombia</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-729">10241 (0x2801)</span><span class="sxs-lookup"><span data-stu-id="48ab3-729">10241 (0x2801)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-730">Árabe – Siria</span><span class="sxs-lookup"><span data-stu-id="48ab3-730">Arabic – Syria</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-731">10249 (0x2809)</span><span class="sxs-lookup"><span data-stu-id="48ab3-731">10249 (0x2809)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-732">Inglés – Belice</span><span class="sxs-lookup"><span data-stu-id="48ab3-732">English – Belize</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-733">10250 (0x280A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-733">10250 (0x280A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-734">Español – Perú</span><span class="sxs-lookup"><span data-stu-id="48ab3-734">Spanish – Peru</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-735">11265 (0x2C01)</span><span class="sxs-lookup"><span data-stu-id="48ab3-735">11265 (0x2C01)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-736">Árabe – Jordania</span><span class="sxs-lookup"><span data-stu-id="48ab3-736">Arabic – Jordan</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-737">11273 (0x2C09)</span><span class="sxs-lookup"><span data-stu-id="48ab3-737">11273 (0x2C09)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-738">Inglés – Trinidad</span><span class="sxs-lookup"><span data-stu-id="48ab3-738">English – Trinidad</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-739">11274 (0x2C0A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-739">11274 (0x2C0A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-740">Español – Argentina</span><span class="sxs-lookup"><span data-stu-id="48ab3-740">Spanish – Argentina</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-741">12289 (0x3001)</span><span class="sxs-lookup"><span data-stu-id="48ab3-741">12289 (0x3001)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-742">Árabe – Líbano</span><span class="sxs-lookup"><span data-stu-id="48ab3-742">Arabic – Lebanon</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-743">12298 (0x300A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-743">12298 (0x300A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-744">Español – Ecuador</span><span class="sxs-lookup"><span data-stu-id="48ab3-744">Spanish – Ecuador</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-745">13313 (0x3401)</span><span class="sxs-lookup"><span data-stu-id="48ab3-745">13313 (0x3401)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-746">Árabe – Kuwait</span><span class="sxs-lookup"><span data-stu-id="48ab3-746">Arabic – Kuwait</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-747">13322 (0x340A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-747">13322 (0x340A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-748">Español – Chile</span><span class="sxs-lookup"><span data-stu-id="48ab3-748">Spanish – Chile</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-749">14337 (0x3801)</span><span class="sxs-lookup"><span data-stu-id="48ab3-749">14337 (0x3801)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-750">Árabe – Emiratos Árabes Unidos</span><span class="sxs-lookup"><span data-stu-id="48ab3-750">Arabic – U.A.E.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-751">14346 (0x380A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-751">14346 (0x380A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-752">Español – Uruguay</span><span class="sxs-lookup"><span data-stu-id="48ab3-752">Spanish – Uruguay</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-753">15361 (0x3C01)</span><span class="sxs-lookup"><span data-stu-id="48ab3-753">15361 (0x3C01)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-754">Árabe – Bahrein</span><span class="sxs-lookup"><span data-stu-id="48ab3-754">Arabic – Bahrain</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-755">15370 (0x3C0A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-755">15370 (0x3C0A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-756">Español – Paraguay</span><span class="sxs-lookup"><span data-stu-id="48ab3-756">Spanish – Paraguay</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-757">16385 (0x4001)</span><span class="sxs-lookup"><span data-stu-id="48ab3-757">16385 (0x4001)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-758">Árabe – Qatar</span><span class="sxs-lookup"><span data-stu-id="48ab3-758">Arabic – Qatar</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-759">16394 (0x400A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-759">16394 (0x400A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-760">Español (Bolivia)</span><span class="sxs-lookup"><span data-stu-id="48ab3-760">Spanish – Bolivia</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-761">17418 (0x440A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-761">17418 (0x440A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-762">Español – El Salvador</span><span class="sxs-lookup"><span data-stu-id="48ab3-762">Spanish – El Salvador</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-763">18442 (0x480A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-763">18442 (0x480A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-764">Español – Honduras</span><span class="sxs-lookup"><span data-stu-id="48ab3-764">Spanish – Honduras</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-765">19466 (0x4C0A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-765">19466 (0x4C0A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-766">Español (Nicaragua)</span><span class="sxs-lookup"><span data-stu-id="48ab3-766">Spanish – Nicaragua</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-767">20490 (0x500A)</span><span class="sxs-lookup"><span data-stu-id="48ab3-767">20490 (0x500A)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-768">Español (Puerto Rico)</span><span class="sxs-lookup"><span data-stu-id="48ab3-768">Spanish – Puerto Rico</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="48ab3-769">**OSProductSuite**</span><span class="sxs-lookup"><span data-stu-id="48ab3-769">**OSProductSuite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-770">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48ab3-770">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-771">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-771">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-772">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ PRODUCTOPTIONS \| ProductSuite"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Small Business", "Enterprise", "BackOffice", "Communication Server", "Terminal Server", "Small Business (Restricted)", "Embedded NT", "Data Center")</span><span class="sxs-lookup"><span data-stu-id="48ab3-772">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\ProductOptions\|ProductSuite"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Small Business", "Enterprise", "BackOffice", "Communication Server", "Terminal Server", "Small Business(Restricted)", "Embedded NT", "Data Center")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-773">Se han instalado y con licencia las adiciones de productos del sistema al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-773">Installed and licensed system product additions to the operating system.</span></span> <span data-ttu-id="48ab3-774">Por ejemplo, el valor 146 (0x92) para **OSProductSuite** indica Enterprise, Terminal Services y Data Center (bits uno, cuatro y siete establecidos).</span><span class="sxs-lookup"><span data-stu-id="48ab3-774">For example, the value of 146 (0x92) for **OSProductSuite** indicates Enterprise, Terminal Services, and Data Center (bits one, four, and seven set).</span></span> <span data-ttu-id="48ab3-775">En la lista siguiente se enumeran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="48ab3-775">The following list lists possible values.</span></span>

<dt>

<span data-ttu-id="48ab3-776">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="48ab3-776">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-777">Microsoft Small Business Server se instaló una vez, pero es posible que se haya actualizado a otra versión de Windows.</span><span class="sxs-lookup"><span data-stu-id="48ab3-777">Microsoft Small Business Server was once installed, but may have been upgraded to another version of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-778">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="48ab3-778">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-779">Windows Server 2008 Enterprise está instalado.</span><span class="sxs-lookup"><span data-stu-id="48ab3-779">Windows Server 2008 Enterprise is installed.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-780">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="48ab3-780">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-781">Los componentes de Windows BackOffice están instalados.</span><span class="sxs-lookup"><span data-stu-id="48ab3-781">Windows BackOffice components are installed.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-782">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="48ab3-782">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-783">El servidor de comunicación está instalado.</span><span class="sxs-lookup"><span data-stu-id="48ab3-783">Communication Server is installed.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-784">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="48ab3-784">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-785">Terminal Services está instalado.</span><span class="sxs-lookup"><span data-stu-id="48ab3-785">Terminal Services is installed.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-786">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="48ab3-786">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-787">Microsoft Small Business Server se instala con la licencia de cliente restrictiva.</span><span class="sxs-lookup"><span data-stu-id="48ab3-787">Microsoft Small Business Server is installed with the restrictive client license.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-788">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="48ab3-788">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-789">Windows Embedded está instalado.</span><span class="sxs-lookup"><span data-stu-id="48ab3-789">Windows Embedded is installed.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-790">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="48ab3-790">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-791">Se instala una edición de Datacenter.</span><span class="sxs-lookup"><span data-stu-id="48ab3-791">A Datacenter edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-792">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="48ab3-792">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-793">Terminal Services está instalado, pero solo se admite una sesión interactiva.</span><span class="sxs-lookup"><span data-stu-id="48ab3-793">Terminal Services is installed, but only one interactive session is supported.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-794">512 (0x200)</span><span class="sxs-lookup"><span data-stu-id="48ab3-794">512 (0x200)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-795">Windows Home Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="48ab3-795">Windows Home Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-796">1024 (0x400)</span><span class="sxs-lookup"><span data-stu-id="48ab3-796">1024 (0x400)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-797">Web Server Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="48ab3-797">Web Server Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-798">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="48ab3-798">8192 (0x2000)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-799">Storage Server Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="48ab3-799">Storage Server Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-800">16384 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="48ab3-800">16384 (0x4000)</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-801">Compute Cluster Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="48ab3-801">Compute Cluster Edition is installed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="48ab3-802">**OSType**</span><span class="sxs-lookup"><span data-stu-id="48ab3-802">**OSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-803">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48ab3-803">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-804">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-804">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-805">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="48ab3-805">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-806">Tipo de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-806">Type of operating system.</span></span> <span data-ttu-id="48ab3-807">La lista siguiente identifica los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="48ab3-807">The following list identifies the possible values.</span></span>

<span data-ttu-id="48ab3-808">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-808">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48ab3-809"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="48ab3-809"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="48ab3-810"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="48ab3-810"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="48ab3-811"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="48ab3-811"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-812">MACROS</span><span class="sxs-lookup"><span data-stu-id="48ab3-812">MACROS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="48ab3-813"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="48ab3-813"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="48ab3-814"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="48ab3-814"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="48ab3-815"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="48ab3-815"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="48ab3-816"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="48ab3-816"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="48ab3-817"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="48ab3-817"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="48ab3-818"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="48ab3-818"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="48ab3-819"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="48ab3-819"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="48ab3-820"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="48ab3-820"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="48ab3-821"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="48ab3-821"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="48ab3-822"><span id="OS_2"></span><span id="os_2"></span>**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="48ab3-822"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="48ab3-823"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="48ab3-823"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="48ab3-824"><span id="MSDOS"></span><span id="msdos"></span>**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="48ab3-824"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="48ab3-825"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="48ab3-825"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="48ab3-826"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="48ab3-826"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="48ab3-827"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="48ab3-827"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="48ab3-828"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="48ab3-828"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="48ab3-829"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="48ab3-829"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="48ab3-830"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="48ab3-830"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="48ab3-831"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="48ab3-831"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="48ab3-832"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="48ab3-832"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="48ab3-833"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="48ab3-833"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="48ab3-834"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="48ab3-834"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="48ab3-835"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="48ab3-835"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="48ab3-836"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="48ab3-836"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="48ab3-837"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="48ab3-837"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="48ab3-838"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="48ab3-838"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="48ab3-839"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="48ab3-839"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd>

<span data-ttu-id="48ab3-840">Solaris</span><span class="sxs-lookup"><span data-stu-id="48ab3-840">Solaris</span></span>

</dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="48ab3-841"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="48ab3-841"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="48ab3-842"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="48ab3-842"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="48ab3-843"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="48ab3-843"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="48ab3-844"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="48ab3-844"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="48ab3-845"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="48ab3-845"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="48ab3-846"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="48ab3-846"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="48ab3-847"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="48ab3-847"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="48ab3-848"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="48ab3-848"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="48ab3-849"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="48ab3-849"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="48ab3-850"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="48ab3-850"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="48ab3-851"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="48ab3-851"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="48ab3-852"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="48ab3-852"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="48ab3-853"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="48ab3-853"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="48ab3-854"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="48ab3-854"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="48ab3-855"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="48ab3-855"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="48ab3-856"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="48ab3-856"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="48ab3-857"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="48ab3-857"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="48ab3-858"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="48ab3-858"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="48ab3-859"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="48ab3-859"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="48ab3-860"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="48ab3-860"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="48ab3-861"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="48ab3-861"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="48ab3-862"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="48ab3-862"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="48ab3-863"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="48ab3-863"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="48ab3-864"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="48ab3-864"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="48ab3-865"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="48ab3-865"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="48ab3-866"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="48ab3-866"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="48ab3-867"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="48ab3-867"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="48ab3-868"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="48ab3-868"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="48ab3-869"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="48ab3-869"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="48ab3-870"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="48ab3-870"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="48ab3-871"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span><span class="sxs-lookup"><span data-stu-id="48ab3-871"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="48ab3-872"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span><span class="sxs-lookup"><span data-stu-id="48ab3-872"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="48ab3-873"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span><span class="sxs-lookup"><span data-stu-id="48ab3-873"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="48ab3-874">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="48ab3-874">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-875">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-875">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-876">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-876">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-877">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="48ab3-877">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-878">Descripción adicional para la versión del sistema operativo actual.</span><span class="sxs-lookup"><span data-stu-id="48ab3-878">Additional description for the current operating system version.</span></span>

<span data-ttu-id="48ab3-879">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-879">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-880">**PAEEnabled**</span><span class="sxs-lookup"><span data-stu-id="48ab3-880">**PAEEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-881">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="48ab3-881">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-882">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-882">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-883">Si **es true**, el sistema operativo que ejecuta los procesadores Intel habilita las extensiones de dirección física (PAE).</span><span class="sxs-lookup"><span data-stu-id="48ab3-883">If **True**, the physical address extensions (PAE) are enabled by the operating system running on Intel processors.</span></span> <span data-ttu-id="48ab3-884">PAE permite a las aplicaciones abordar más de 4 GB de memoria física.</span><span class="sxs-lookup"><span data-stu-id="48ab3-884">PAE allows applications to address more than 4 GB of physical memory.</span></span> <span data-ttu-id="48ab3-885">Cuando PAE está habilitado, el sistema operativo utiliza la traducción de direcciones lineales de tres niveles en lugar de dos.</span><span class="sxs-lookup"><span data-stu-id="48ab3-885">When PAE is enabled, the operating system uses three-level linear address translation rather than two-level.</span></span> <span data-ttu-id="48ab3-886">Proporcionar más memoria física a una aplicación reduce la necesidad de intercambiar memoria con el archivo de paginación y aumenta el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="48ab3-886">Providing more physical memory to an application reduces the need to swap memory to the page file and increases performance.</span></span> <span data-ttu-id="48ab3-887">Para habilitar, PAE, use el modificador "/PAE" en el archivo de Boot.ini.</span><span class="sxs-lookup"><span data-stu-id="48ab3-887">To enable, PAE, use the "/PAE" switch in the Boot.ini file.</span></span> <span data-ttu-id="48ab3-888">Para obtener más información acerca de la característica de extensión de dirección física, vea <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912> .</span><span class="sxs-lookup"><span data-stu-id="48ab3-888">For more information about the Physical Address Extension feature, see <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912>.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-889">**PlusProductID**</span><span class="sxs-lookup"><span data-stu-id="48ab3-889">**PlusProductID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-890">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-890">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-891">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-891">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-892">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software WIN32REGISTRY \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| Plus</span><span class="sxs-lookup"><span data-stu-id="48ab3-892">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|Plus!</span></span> <span data-ttu-id="48ab3-893">ProductId ")</span><span class="sxs-lookup"><span data-stu-id="48ab3-893">ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-894">No se admite.</span><span class="sxs-lookup"><span data-stu-id="48ab3-894">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-895">**PlusVersionNumber**</span><span class="sxs-lookup"><span data-stu-id="48ab3-895">**PlusVersionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-896">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-896">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-897">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-897">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-898">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software WIN32REGISTRY \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| Plus</span><span class="sxs-lookup"><span data-stu-id="48ab3-898">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|Plus!</span></span> <span data-ttu-id="48ab3-899">VersionNumber ")</span><span class="sxs-lookup"><span data-stu-id="48ab3-899">VersionNumber")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-900">No se admite.</span><span class="sxs-lookup"><span data-stu-id="48ab3-900">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-901">**PortableOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="48ab3-901">**PortableOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-902">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="48ab3-902">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-903">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-903">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-904">Especifica si el sistema operativo arrancó desde un dispositivo USB externo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-904">Specifies whether the operating system booted from an external USB device.</span></span> <span data-ttu-id="48ab3-905">Si es true, el sistema operativo ha detectado que se está iniciando en un dispositivo de almacenamiento conectado localmente compatible.</span><span class="sxs-lookup"><span data-stu-id="48ab3-905">If true, the operating system has detected it is booting on a supported locally connected storage device.</span></span>

<span data-ttu-id="48ab3-906">**Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="48ab3-906">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8 and Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-907">**Principal**</span><span class="sxs-lookup"><span data-stu-id="48ab3-907">**Primary**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-908">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="48ab3-908">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-909">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-909">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-910">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="48ab3-910">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-911">Especifica si este es el sistema operativo principal.</span><span class="sxs-lookup"><span data-stu-id="48ab3-911">Specifies whether this is the primary operating system.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-912">**ProductType**</span><span class="sxs-lookup"><span data-stu-id="48ab3-912">**ProductType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-913">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48ab3-913">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-914">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-914">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-915">Información adicional del sistema.</span><span class="sxs-lookup"><span data-stu-id="48ab3-915">Additional system information.</span></span>

<dt>

<span id="Work_Station"></span><span id="work_station"></span><span id="WORK_STATION"></span>

<span data-ttu-id="48ab3-916">**Estación de trabajo** (1)</span><span class="sxs-lookup"><span data-stu-id="48ab3-916">**Work Station** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Domain_Controller"></span><span id="domain_controller"></span><span id="DOMAIN_CONTROLLER"></span>

<span data-ttu-id="48ab3-917">**Controlador de dominio** (2)</span><span class="sxs-lookup"><span data-stu-id="48ab3-917">**Domain Controller** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="48ab3-918">**Servidor** (3)</span><span class="sxs-lookup"><span data-stu-id="48ab3-918">**Server** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="48ab3-919">**QuantumLength**</span><span class="sxs-lookup"><span data-stu-id="48ab3-919">**QuantumLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-920">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="48ab3-920">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-921">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="48ab3-921">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-922">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ PriorityControl \| Win32PrioritySeparation")</span><span class="sxs-lookup"><span data-stu-id="48ab3-922">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\PriorityControl\|Win32PrioritySeparation")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-923">No compatible</span><span class="sxs-lookup"><span data-stu-id="48ab3-923">Not supported</span></span>

<span data-ttu-id="48ab3-924">\* \* Windows Server 2008 y Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="48ab3-924">\*\*Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="48ab3-925">La propiedad **QuantumLength** define el número de TICs de reloj por cuanto.</span><span class="sxs-lookup"><span data-stu-id="48ab3-925">The **QuantumLength** property defines the number of clock ticks per quantum.</span></span> <span data-ttu-id="48ab3-926">Un Quantum es una unidad de tiempo de ejecución que el programador puede conceder a una aplicación antes de cambiar a otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="48ab3-926">A quantum is a unit of execution time that the scheduler is allowed to give to an application before switching to other applications.</span></span> <span data-ttu-id="48ab3-927">Cuando un subproceso ejecuta un Quantum, el kernel lo adelanta y lo mueve al final de una cola para las aplicaciones con las mismas prioridades.</span><span class="sxs-lookup"><span data-stu-id="48ab3-927">When a thread runs one quantum, the kernel preempts it and moves it to the end of a queue for applications with equal priorities.</span></span> <span data-ttu-id="48ab3-928">La longitud real del Quantum de un subproceso varía en distintas plataformas de Windows.</span><span class="sxs-lookup"><span data-stu-id="48ab3-928">The actual length of a thread's quantum varies across different Windows platforms.</span></span> <span data-ttu-id="48ab3-929">Solo para Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="48ab3-929">For Windows NT/Windows 2000 only.</span></span>

<span data-ttu-id="48ab3-930">Los valores posibles son.</span><span class="sxs-lookup"><span data-stu-id="48ab3-930">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48ab3-931">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="48ab3-931">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="One_tick"></span><span id="one_tick"></span><span id="ONE_TICK"></span>

<span data-ttu-id="48ab3-932">**Un TIC** (1)</span><span class="sxs-lookup"><span data-stu-id="48ab3-932">**One tick** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Two_ticks"></span><span id="two_ticks"></span><span id="TWO_TICKS"></span>

<span data-ttu-id="48ab3-933">**Dos TICs** (2)</span><span class="sxs-lookup"><span data-stu-id="48ab3-933">**Two ticks** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="48ab3-934">**QuantumType**</span><span class="sxs-lookup"><span data-stu-id="48ab3-934">**QuantumType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-935">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="48ab3-935">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-936">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="48ab3-936">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-937">No compatible</span><span class="sxs-lookup"><span data-stu-id="48ab3-937">Not supported</span></span>

<span data-ttu-id="48ab3-938">\* \* Windows Server 2008 y Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="48ab3-938">\*\*Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="48ab3-939">La propiedad **QuantumType** especifica quantums de longitud fija o variable.</span><span class="sxs-lookup"><span data-stu-id="48ab3-939">The **QuantumType** property specifies either fixed or variable length quantums.</span></span> <span data-ttu-id="48ab3-940">Windows toma como valor predeterminado los quantums de longitud variable en los que la aplicación de primer plano tiene un Quantum más largo que las aplicaciones en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="48ab3-940">Windows defaults to variable length quantums where the foreground application has a longer quantum than the background applications.</span></span> <span data-ttu-id="48ab3-941">Windows Server tiene como valor predeterminado quantums de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="48ab3-941">Windows Server defaults to fixed-length quantums.</span></span> <span data-ttu-id="48ab3-942">Un Quantum es una unidad de tiempo de ejecución que el programador puede conceder a una aplicación antes de cambiar a otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="48ab3-942">A quantum is a unit of execution time that the scheduler is allowed to give to an application before switching to another application.</span></span> <span data-ttu-id="48ab3-943">Cuando un subproceso ejecuta un Quantum, el kernel lo adelanta y lo mueve al final de una cola para las aplicaciones con las mismas prioridades.</span><span class="sxs-lookup"><span data-stu-id="48ab3-943">When a thread runs one quantum, the kernel preempts it and moves it to the end of a queue for applications with equal priorities.</span></span> <span data-ttu-id="48ab3-944">La longitud real del Quantum de un subproceso varía en distintas plataformas de Windows.</span><span class="sxs-lookup"><span data-stu-id="48ab3-944">The actual length of a thread's quantum varies across different Windows platforms.</span></span>

<span data-ttu-id="48ab3-945">Los valores posibles son.</span><span class="sxs-lookup"><span data-stu-id="48ab3-945">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48ab3-946">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="48ab3-946">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

<span data-ttu-id="48ab3-947">**Fijo** (1)</span><span class="sxs-lookup"><span data-stu-id="48ab3-947">**Fixed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Variable"></span><span id="variable"></span><span id="VARIABLE"></span>

<span data-ttu-id="48ab3-948">**Variable** (2)</span><span class="sxs-lookup"><span data-stu-id="48ab3-948">**Variable** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="48ab3-949">**RegisteredUser**</span><span class="sxs-lookup"><span data-stu-id="48ab3-949">**RegisteredUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-950">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-950">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-951">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-951">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-952">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| RegisteredOwner")</span><span class="sxs-lookup"><span data-stu-id="48ab3-952">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|RegisteredOwner")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-953">Nombre del usuario registrado del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-953">Name of the registered user of the operating system.</span></span>

<span data-ttu-id="48ab3-954">Ejemplo: "Ben Smith"</span><span class="sxs-lookup"><span data-stu-id="48ab3-954">Example: "Ben Smith"</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-955">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="48ab3-955">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-956">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-956">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-957">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-957">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-958">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| ProductID")</span><span class="sxs-lookup"><span data-stu-id="48ab3-958">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-959">Número de identificación de serie del producto del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-959">Operating system product serial identification number.</span></span>

<span data-ttu-id="48ab3-960">Ejemplo: "10497-OEM-0031416-71674"</span><span class="sxs-lookup"><span data-stu-id="48ab3-960">Example: "10497-OEM-0031416-71674"</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-961">**ServicePackMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="48ab3-961">**ServicePackMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-962">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48ab3-962">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-963">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-963">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-964">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMajor**")</span><span class="sxs-lookup"><span data-stu-id="48ab3-964">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**wServicePackMajor**")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-965">Número de versión principal del Service Pack instalado en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-965">Major version number of the service pack installed on the computer system.</span></span> <span data-ttu-id="48ab3-966">Si no se ha instalado ningún Service Pack, el valor es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="48ab3-966">If no service pack has been installed, the value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-967">**ServicePackMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="48ab3-967">**ServicePackMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-968">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48ab3-968">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-969">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-969">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-970">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMinor**")</span><span class="sxs-lookup"><span data-stu-id="48ab3-970">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**wServicePackMinor**")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-971">Número de versión secundaria del Service Pack instalado en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-971">Minor version number of the service pack installed on the computer system.</span></span> <span data-ttu-id="48ab3-972">Si no se ha instalado ningún Service Pack, el valor es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="48ab3-972">If no service pack has been installed, the value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-973">**SizeStoredInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="48ab3-973">**SizeStoredInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-974">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48ab3-974">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-975">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-975">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-976">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Configuración de la memoria del sistema DMTF \| 001,3 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="48ab3-976">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Memory Settings\|001.3"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-977">Número total de kilobytes que se pueden almacenar en los archivos de paginación del sistema operativo: 0 (cero) indica que no hay ningún archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="48ab3-977">Total number of kilobytes that can be stored in the operating system paging files—0 (zero) indicates that there are no paging files.</span></span> <span data-ttu-id="48ab3-978">Tenga en cuenta que este número no representa el tamaño físico real del archivo de paginación en el disco.</span><span class="sxs-lookup"><span data-stu-id="48ab3-978">Be aware that this number does not represent the actual physical size of the paging file on disk.</span></span>

<span data-ttu-id="48ab3-979">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="48ab3-979">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="48ab3-980">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-980">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-981">**Estado**</span><span class="sxs-lookup"><span data-stu-id="48ab3-981">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-982">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-982">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-983">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-983">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-984">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="48ab3-984">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-985">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="48ab3-985">Current status of the object.</span></span> <span data-ttu-id="48ab3-986">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="48ab3-986">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="48ab3-987">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART puede funcionar correctamente, pero predice un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="48ab3-987">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive may function properly, but predicts a failure in the near future).</span></span> <span data-ttu-id="48ab3-988">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="48ab3-988">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="48ab3-989">El estado del servicio se aplica a la tarea administrativa, como la reduplicación de reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-989">The Service status applies to administrative work, such as mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="48ab3-990">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="48ab3-990">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="48ab3-991">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-991">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="48ab3-992">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="48ab3-992">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="48ab3-993">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="48ab3-993">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="48ab3-994">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="48ab3-994">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48ab3-995">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="48ab3-995">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="48ab3-996">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="48ab3-996">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="48ab3-997">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="48ab3-997">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="48ab3-998">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="48ab3-998">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="48ab3-999">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="48ab3-999">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="48ab3-1000">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="48ab3-1000">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="48ab3-1001">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="48ab3-1001">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="48ab3-1002">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="48ab3-1002">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="48ab3-1003">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="48ab3-1003">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="48ab3-1004">**SuiteMask**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1004">**SuiteMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-1005">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1005">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1006">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-1006">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1007">Calificadores: [**mapa de bits**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition", "Windows Server, BackOffice Edition", "Windows Server, Communications Edition", "Microsoft Terminal Services", "Windows Server, Small Business Edition restricted", "Windows Embedded", "Windows Server, Datacenter Edition", "single user", "Windows Home Edition", "Windows Server, Web Edition")</span><span class="sxs-lookup"><span data-stu-id="48ab3-1007">Qualifiers: [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition", "Windows Server, Backoffice Edition", "Windows Server, Communications Edition", "Microsoft Terminal Services", "Windows Server, Small Business Edition Restricted", "Windows Embedded", "Windows Server, Datacenter Edition", "Single User", "Windows Home Edition", "Windows Server, Web Edition")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-1008">Marcas de bits que identifican los conjuntos de productos disponibles en el sistema.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1008">Bit flags that identify the product suites available on the system.</span></span>

<span data-ttu-id="48ab3-1009">Por ejemplo, para especificar personal y BackOffice, establezca **SuiteMask** en `4 | 512` o `516` .</span><span class="sxs-lookup"><span data-stu-id="48ab3-1009">For example, to specify both Personal and BackOffice, set **SuiteMask** to `4 | 512` or `516`.</span></span>

<dt>

<span data-ttu-id="48ab3-1010">1</span><span class="sxs-lookup"><span data-stu-id="48ab3-1010">1</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-1011">Pequeñas empresas</span><span class="sxs-lookup"><span data-stu-id="48ab3-1011">Small Business</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1012">2</span><span class="sxs-lookup"><span data-stu-id="48ab3-1012">2</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-1013">Enterprise</span><span class="sxs-lookup"><span data-stu-id="48ab3-1013">Enterprise</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1014">4</span><span class="sxs-lookup"><span data-stu-id="48ab3-1014">4</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-1015">BackOffice</span><span class="sxs-lookup"><span data-stu-id="48ab3-1015">BackOffice</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1016">8</span><span class="sxs-lookup"><span data-stu-id="48ab3-1016">8</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-1017">Comunicaciones</span><span class="sxs-lookup"><span data-stu-id="48ab3-1017">Communications</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1018">16</span><span class="sxs-lookup"><span data-stu-id="48ab3-1018">16</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-1019">Terminal Services</span><span class="sxs-lookup"><span data-stu-id="48ab3-1019">Terminal Services</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1020">32</span><span class="sxs-lookup"><span data-stu-id="48ab3-1020">32</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-1021">Pequeña empresa restringida</span><span class="sxs-lookup"><span data-stu-id="48ab3-1021">Small Business Restricted</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1022">64</span><span class="sxs-lookup"><span data-stu-id="48ab3-1022">64</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-1023">Edición incrustada</span><span class="sxs-lookup"><span data-stu-id="48ab3-1023">Embedded Edition</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1024">128</span><span class="sxs-lookup"><span data-stu-id="48ab3-1024">128</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-1025">Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="48ab3-1025">Datacenter Edition</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1026">256</span><span class="sxs-lookup"><span data-stu-id="48ab3-1026">256</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-1027">Usuario único</span><span class="sxs-lookup"><span data-stu-id="48ab3-1027">Single User</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1028">512</span><span class="sxs-lookup"><span data-stu-id="48ab3-1028">512</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-1029">Edición Home</span><span class="sxs-lookup"><span data-stu-id="48ab3-1029">Home Edition</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1030">1024</span><span class="sxs-lookup"><span data-stu-id="48ab3-1030">1024</span></span>
</dt> <dd>

<span data-ttu-id="48ab3-1031">Edición del servidor Web</span><span class="sxs-lookup"><span data-stu-id="48ab3-1031">Web Server Edition</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="48ab3-1032">**SystemDevice**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1032">**SystemDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-1033">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1033">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1034">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-1034">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1035">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Functions \| [**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring) \| paths \| dispositivo")</span><span class="sxs-lookup"><span data-stu-id="48ab3-1035">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Registry Functions\|[**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring)\|Paths\|TargetDevice")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-1036">Partición de disco físico en la que está instalado el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1036">Physical disk partition on which the operating system is installed.</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1037">**SystemDirectory**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1037">**SystemDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-1038">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1038">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1039">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-1039">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1040">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| System Information Functions [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))</span><span class="sxs-lookup"><span data-stu-id="48ab3-1040">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-1041">Directorio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1041">System directory of the operating system.</span></span>

<span data-ttu-id="48ab3-1042">Ejemplo: "C: \\ Windows \\ system32"</span><span class="sxs-lookup"><span data-stu-id="48ab3-1042">Example: "C:\\WINDOWS\\SYSTEM32"</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1043">**SystemDrive**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1043">**SystemDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-1044">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1044">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1045">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-1045">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-1046">Letra de la unidad de disco en la que reside el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1046">Letter of the disk drive on which the operating system resides.</span></span> <span data-ttu-id="48ab3-1047">Ejemplo: "C:"</span><span class="sxs-lookup"><span data-stu-id="48ab3-1047">Example: "C:"</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1048">**TotalSwapSpaceSize**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1048">**TotalSwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-1049">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1049">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1050">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-1050">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1051">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="48ab3-1051">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-1052">Espacio de intercambio total en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1052">Total swap space in kilobytes.</span></span> <span data-ttu-id="48ab3-1053">Este valor puede ser **null** (no especificado) si el espacio de intercambio no se distingue de los archivos de paginación.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1053">This value may be **NULL** (unspecified) if the swap space is not distinguished from page files.</span></span> <span data-ttu-id="48ab3-1054">Sin embargo, algunos sistemas operativos distinguen estos conceptos.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1054">However, some operating systems distinguish these concepts.</span></span> <span data-ttu-id="48ab3-1055">Por ejemplo, en UNIX, se pueden intercambiar procesos completos cuando la lista de páginas disponibles cae y permanece por debajo de una cantidad especificada.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1055">For example, in UNIX, whole processes can be swapped out when the free page list falls and remains below a specified amount.</span></span>

<span data-ttu-id="48ab3-1056">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="48ab3-1056">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="48ab3-1057">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-1057">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1058">**TotalVirtualMemorySize**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1058">**TotalVirtualMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-1059">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1059">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1060">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-1060">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1061">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="48ab3-1061">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-1062">Número, en kilobytes, de la memoria virtual.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1062">Number, in kilobytes, of virtual memory.</span></span> <span data-ttu-id="48ab3-1063">Por ejemplo, esto puede calcularse agregando la cantidad de RAM total a la cantidad de espacio de paginación, es decir, agregando la cantidad de memoria en el sistema del equipo o la agregará a la propiedad **SizeStoredInPagingFiles**.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1063">For example, this may be calculated by adding the amount of total RAM to the amount of paging space, that is, adding the amount of memory in or aggregated by the computer system to the property, **SizeStoredInPagingFiles**.</span></span>

<span data-ttu-id="48ab3-1064">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="48ab3-1064">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="48ab3-1065">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-1065">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1066">**TotalVisibleMemorySize**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1066">**TotalVisibleMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-1067">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1067">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1068">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-1068">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1069">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="48ab3-1069">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-1070">Cantidad total, en kilobytes, de la memoria física disponible para el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1070">Total amount, in kilobytes, of physical memory available to the operating system.</span></span> <span data-ttu-id="48ab3-1071">Este valor no indica necesariamente la cantidad real de memoria física, sino lo que se notifica al sistema operativo como disponible para ella.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1071">This value does not necessarily indicate the true amount of physical memory, but what is reported to the operating system as available to it.</span></span>

<span data-ttu-id="48ab3-1072">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="48ab3-1072">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="48ab3-1073">Esta propiedad se hereda del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-1073">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1074">**Versión**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1074">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-1075">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1075">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1076">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-1076">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1077">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("version"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwMajorVersion, dwMinorVersion")</span><span class="sxs-lookup"><span data-stu-id="48ab3-1077">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Version"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|dwMajorVersion, dwMinorVersion")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-1078">Número de versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1078">Version number of the operating system.</span></span>

<span data-ttu-id="48ab3-1079">Ejemplo: "4,0"</span><span class="sxs-lookup"><span data-stu-id="48ab3-1079">Example: "4.0"</span></span>

</dd> <dt>

<span data-ttu-id="48ab3-1080">**WindowsDirectory**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1080">**WindowsDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48ab3-1081">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1081">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1082">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48ab3-1082">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48ab3-1083">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| System Information Functions \| [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")</span><span class="sxs-lookup"><span data-stu-id="48ab3-1083">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|[**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")</span></span>
</dt> </dl>

<span data-ttu-id="48ab3-1084">Directorio de Windows del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1084">Windows directory of the operating system.</span></span>

<span data-ttu-id="48ab3-1085">Ejemplo: "C: \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="48ab3-1085">Example: "C:\\WINDOWS"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48ab3-1086">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48ab3-1086">Remarks</span></span>

<span data-ttu-id="48ab3-1087">La clase **Win32 \_ OperatingSystem** se deriva del [**\_ OperatingSystem de CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="48ab3-1087">The **Win32\_OperatingSystem** class is derived from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

<span data-ttu-id="48ab3-1088">Los sistemas operativos que se pueden instalar en un equipo que puede ejecutar un sistema operativo basado en Windows son descendientes o miembros de esta clase.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1088">Any operating system that can be installed on a computer that can run a Windows-based operating system is a descendant or member of this class.</span></span> <span data-ttu-id="48ab3-1089">**Win32 \_ OperatingSystem** es una clase singleton.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1089">**Win32\_OperatingSystem** is a singleton class.</span></span> <span data-ttu-id="48ab3-1090">Para obtener la instancia única, use "@" para la clave.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1090">To get the single instance, use "@" for the key.</span></span>

<span data-ttu-id="48ab3-1091">A diferencia de la mayoría de las otras clases WMI generadas por MgmtClassGen, el método **OperatingSystem. CreateInstance**() devolverá un objeto **OperatingSystem** en blanco.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1091">Unlike most of the other WMI classes generated by MgmtClassGen, the **OperatingSystem.CreateInstance**() method will return a blank **OperatingSystem** object.</span></span> <span data-ttu-id="48ab3-1092">Por lo tanto, si usa C \# con MgmtClassGen, puede usar el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="48ab3-1092">Therefore, if you are using C\# with MgmtClassGen, you can use the following code:</span></span>


```CSharp
WMI.OperatingSystem os = new ROOT.CIMV2.win32.OperatingSystem();
```



## <a name="examples"></a><span data-ttu-id="48ab3-1093">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="48ab3-1093">Examples</span></span>

<span data-ttu-id="48ab3-1094">Puede encontrar un ejemplo de VBScript que obtiene los datos del sistema operativo y del procesador de [**Win32 \_ ComputerSystem**](win32-computersystem.md), el [**\_ procesador Win32**](win32-processor.md)y el **\_ OperatingSystem de Win32** en los ejemplos de temas del [**\_ procesador Win32**](win32-processor.md) .</span><span class="sxs-lookup"><span data-stu-id="48ab3-1094">You can find a VBScript example that obtains operating system and processor data from [**Win32\_ComputerSystem**](win32-computersystem.md), [**Win32\_Processor**](win32-processor.md), and **Win32\_OperatingSystem** in the [**Win32\_Processor**](win32-processor.md) topic examples.</span></span>

<span data-ttu-id="48ab3-1095">El ejemplo de [generación de informes de entorno de Exchange con](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) PowerShell PowerShell en la galería de TechNet usa una clase **Win32 \_ OperatingSystem** como parte de una aplicación más grande para generar informes de entorno de Exchange.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1095">The [Generate Exchange Environment Reports using Powershell](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) PowerShell sample on TechNet Gallery uses a **Win32\_OperatingSystem** class as part of a larger application to generate exchange environment reports.</span></span>

<span data-ttu-id="48ab3-1096">El ejemplo de [obtención de tiempo de actividad del servidor mediante WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) en la galería de TechNet usa la propiedad **LastBootupTime** para determinar cuánto tiempo el servidor ha estado activo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1096">The [Get Server Uptime Using WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) sample in the TechNet Gallery uses the **LastBootupTime** property to determine how long the server has been active.</span></span> <span data-ttu-id="48ab3-1097">En el ejemplo también se usa la opción timeout para asegurarse de que la llamada WMI no se bloquea.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1097">The sample also uses the timeout option to ensure that the WMI call does not hang.</span></span>

<span data-ttu-id="48ab3-1098">El ejemplo de código VBScript del administrador de [información de WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) de la galería de TechNet utiliza la clase de **Win32 \_ OperatingSystem** para recuperar información del sistema operativo de varios equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1098">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_OperatingSystem** class to retrieve OS information from a number of remote computers.</span></span>

<span data-ttu-id="48ab3-1099">El siguiente script obtiene las instancias de **Win32 \_ OperatingSystem** en el espacio de nombres predeterminado "root \\ CIMv2" y, a continuación, muestra información sobre el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1099">The following script obtains the instances of **Win32\_OperatingSystem** in the default "Root\\CIMv2" namespace, and then displays information about the operating system.</span></span>


```VB
On Error Resume Next
' Connect to WMI and obtain instances of Win32_OperatingSystem
For Each objOS in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

WScript.Echo "Name = " & objOS.Caption & "Version = " & objOS.Version &VBCR _
           & "Registered User = " & objOS.RegisteredUser &VBCR _
           & "Manufacturer = " & objOS.Manufacturer      
Next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



<span data-ttu-id="48ab3-1100">En el siguiente ejemplo de código de PowerShell se muestra toda la información operativa sobre el sistema operativo actual.</span><span class="sxs-lookup"><span data-stu-id="48ab3-1100">The following PowerShell code sample displays all the operating information about the current OS.</span></span>


```PowerShell
# get instance
$os = Get-WmiObject Win32_OperatingSystem

# output information:
"The class has {0} properties" -f $os.properties.count
"Details on this class:"
$os | Format-List *
```



## <a name="requirements"></a><span data-ttu-id="48ab3-1101">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48ab3-1101">Requirements</span></span>



| <span data-ttu-id="48ab3-1102">Requisito</span><span class="sxs-lookup"><span data-stu-id="48ab3-1102">Requirement</span></span> | <span data-ttu-id="48ab3-1103">Value</span><span class="sxs-lookup"><span data-stu-id="48ab3-1103">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48ab3-1104">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48ab3-1104">Minimum supported client</span></span><br/> | <span data-ttu-id="48ab3-1105">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48ab3-1105">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48ab3-1106">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48ab3-1106">Minimum supported server</span></span><br/> | <span data-ttu-id="48ab3-1107">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48ab3-1107">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48ab3-1108">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="48ab3-1108">Namespace</span></span><br/>                | <span data-ttu-id="48ab3-1109">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="48ab3-1109">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="48ab3-1110">MOF</span><span class="sxs-lookup"><span data-stu-id="48ab3-1110">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48ab3-1111"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48ab3-1111"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="48ab3-1112">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="48ab3-1112">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48ab3-1113"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48ab3-1113"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48ab3-1114">Vea también</span><span class="sxs-lookup"><span data-stu-id="48ab3-1114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48ab3-1115">**OperatingSystem de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="48ab3-1115">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="48ab3-1116">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="48ab3-1116">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="48ab3-1117">Tareas WMI: sistemas operativos</span><span class="sxs-lookup"><span data-stu-id="48ab3-1117">WMI Tasks: Operating Systems</span></span>](../wmisdk/wmi-tasks--operating-systems.md)
</dt> <dt>

[<span data-ttu-id="48ab3-1118">Tareas WMI: hardware del equipo</span><span class="sxs-lookup"><span data-stu-id="48ab3-1118">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> <dt>

[<span data-ttu-id="48ab3-1119">Tareas WMI: administración de escritorio</span><span class="sxs-lookup"><span data-stu-id="48ab3-1119">WMI Tasks: Desktop Management</span></span>](../wmisdk/wmi-tasks--desktop-management.md)
</dt> </dl>

 

 
