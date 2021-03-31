---
description: Al realizar una copia de seguridad o restauración de VSS, el estado del sistema de Windows se define como una colección de varios elementos clave del sistema operativo y sus archivos. Estos elementos siempre se deben tratar como una unidad mediante operaciones de copia de seguridad y restauración.
ms.assetid: 48721358-8450-462f-8f99-23e207311041
title: Copia de seguridad y restauración del estado del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed61c3ccad51ebd8cd632fab292160c795741c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812806"
---
# <a name="backing-up-and-restoring-system-state"></a><span data-ttu-id="3399e-104">Copia de seguridad y restauración del estado del sistema</span><span class="sxs-lookup"><span data-stu-id="3399e-104">Backing Up and Restoring System State</span></span>

> [!Note]  
> <span data-ttu-id="3399e-105">Este tema se aplica a Windows Vista, Windows Server 2008 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3399e-105">This topic applies to Windows Vista, Windows Server 2008, and later.</span></span> <span data-ttu-id="3399e-106">Para obtener información acerca de Windows Server 2003, consulte [copia de seguridad y restauración del estado del sistema en Windows server 2003 R2 y Windows server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md) .</span><span class="sxs-lookup"><span data-stu-id="3399e-106">For information about Windows Server 2003, see [Backing Up and Restoring System State in Windows Server 2003 R2 and Windows Server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)</span></span>

 

<span data-ttu-id="3399e-107">Al realizar una copia de seguridad o restauración de VSS, el estado del sistema de Windows se define como una colección de varios elementos clave del sistema operativo y sus archivos.</span><span class="sxs-lookup"><span data-stu-id="3399e-107">When performing a VSS backup or restore, the Windows system state is defined as being a collection of several key operating system elements and their files.</span></span> <span data-ttu-id="3399e-108">Estos elementos siempre se deben tratar como una unidad mediante operaciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="3399e-108">These elements should always be treated as a unit by backup and restore operations.</span></span>

> [!Note]  
> <span data-ttu-id="3399e-109">Microsoft no proporciona soporte técnico para desarrolladores o profesionales de TI para implementar restauraciones de estado del sistema en línea en Windows (todas las versiones).</span><span class="sxs-lookup"><span data-stu-id="3399e-109">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span>

 

<span data-ttu-id="3399e-110">Al realizar copias de seguridad y recuperar el estado del sistema, la estrategia recomendada es realizar copias de seguridad y recuperar los volúmenes del sistema y de arranque, además de los archivos enumerados por los escritores de estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="3399e-110">When backing up and recovering system state, the recommended strategy is to back up and recover the system and boot volumes in addition to the files enumerated by the system state writers.</span></span> <span data-ttu-id="3399e-111">Los escritores de estado del sistema son escritores que tienen el atributo [**\_ \_ tipo de uso de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) establecido en VSS \_ UT \_ BOOTABLESYSTEMSTATE o VSS \_ UT \_ SYSTEMSERVICE.</span><span class="sxs-lookup"><span data-stu-id="3399e-111">System state writers are writers that have the [**VSS\_USAGE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) attribute set to either VSS\_UT\_BOOTABLESYSTEMSTATE or VSS\_UT\_SYSTEMSERVICE.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3399e-112">Si un escritor de VSS se identifica mediante [**su \_ \_ tipo de uso de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) como escritor de estado del sistema, debe estar incluido en una copia de seguridad del estado del sistema, incluso si es seleccionable.</span><span class="sxs-lookup"><span data-stu-id="3399e-112">If a VSS Writer is identified by its [**VSS\_USAGE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) as a system state writer it must be included in a system state backup even if it is selectable.</span></span>

 

<span data-ttu-id="3399e-113">Además de los archivos binarios del sistema operativo enumerados y controladores enumerados por los escritores de estado del sistema, hay algunos otros archivos de los que se debe hacer una copia de seguridad como parte del estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="3399e-113">In addition to the enumerated operating system and driver binary files that are enumerated by the system state writers, there are certain other files that must be backed up as part of system state.</span></span>

<span data-ttu-id="3399e-114">Todos los componentes indicados por un escritor de estado del sistema de VSS forman parte del estado del sistema, excepto aquellos para los que \_ \_ se establece la marca de estado CF no sistema de VSS \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3399e-114">All the components reported by a VSS system state writer are part of system state except those for which the VSS\_CF\_NOT\_SYSTEM\_STATE flag is set.</span></span>

<span data-ttu-id="3399e-115">Los programas de copia de seguridad también deben establecer la clave del registro **LastRestoreId** .</span><span class="sxs-lookup"><span data-stu-id="3399e-115">Backup programs should also set the **LastRestoreId** registry key.</span></span> <span data-ttu-id="3399e-116">Para obtener más información, vea [claves y valores del registro para copias de seguridad y restauración](../backup/registry-keys-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="3399e-116">For more information, see [Registry Keys and Values for Backup and Restore](../backup/registry-keys-for-backup-and-restore.md).</span></span>

> [!Note]  
> <span data-ttu-id="3399e-117">En Windows Vista, Windows Server 2008 y versiones posteriores, se han cambiado los nombres y las ubicaciones de algunos archivos del sistema como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="3399e-117">In Windows Vista, Windows Server 2008, and later, the names and locations of some system files have been changed as follows.</span></span>

 

## <a name="system-state"></a><span data-ttu-id="3399e-118">Estado del sistema</span><span class="sxs-lookup"><span data-stu-id="3399e-118">System State</span></span>

<span data-ttu-id="3399e-119">En Windows Server 2012 y versiones posteriores, además de los archivos que informan los diversos escritores de Estados del sistema VSS, solo es necesario incluir explícitamente los siguientes archivos de licencias, y es necesario excluir explícitamente los siguientes archivos DRM.</span><span class="sxs-lookup"><span data-stu-id="3399e-119">For Windows Server 2012 and later, in addition to the files reported by the various VSS system-state writers, only the following licensing files need to be included explicitly, and the following DRM files need to be excluded explicitly.</span></span>

## <a name="windows-media-digital-rights-management-files"></a><span data-ttu-id="3399e-120">Archivos Rights Management digitales de Windows Media</span><span class="sxs-lookup"><span data-stu-id="3399e-120">Windows Media Digital Rights Management Files</span></span>

<span data-ttu-id="3399e-121">En Windows Server 2008 y versiones posteriores, los siguientes archivos, incluidos todos los subdirectorios de la ruta de acceso siguiente, se excluyen del estado del sistema y no deben realizarse copias de seguridad:</span><span class="sxs-lookup"><span data-stu-id="3399e-121">In Windows Server 2008 and later, the following files, including all subdirectories under the following path, are excluded from system state and must not be backed up:</span></span>

-   <span data-ttu-id="3399e-122">% ProgramData% \\ DRM de Microsoft \\ Windows </span><span class="sxs-lookup"><span data-stu-id="3399e-122">%ProgramData%\\Microsoft\\Windows\\DRM</span></span>\\\\

<span data-ttu-id="3399e-123">Esto reemplaza la información de la sección Rights Management digital de Windows Media de [trabajar con el sistema de archivos y las características de seguridad](working-with-file-system-and-security-features.md).</span><span class="sxs-lookup"><span data-stu-id="3399e-123">This supersedes the information in the Windows Media Digital Rights Management section of [Working with File System and Security Features](working-with-file-system-and-security-features.md).</span></span>

## <a name="performance-counter-configuration-files"></a><span data-ttu-id="3399e-124">Archivos de configuración del contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="3399e-124">Performance Counter Configuration Files</span></span>

<span data-ttu-id="3399e-125">Los archivos de configuración del contador de rendimiento se encuentran en el directorio% SystemRoot% \\ system32 \\ y tienen los siguientes nombres:</span><span class="sxs-lookup"><span data-stu-id="3399e-125">The performance counter configuration files are located in the %SystemRoot%\\System32\\ directory and have the following names:</span></span>

<dl> <span data-ttu-id="3399e-126">¿Rendimiento? 00? incrementa</span><span class="sxs-lookup"><span data-stu-id="3399e-126">Perf?00?.dat</span></span>  
<span data-ttu-id="3399e-127">??. Perfc0 incrementa</span><span class="sxs-lookup"><span data-stu-id="3399e-127">Perfc0??.dat</span></span>  
<span data-ttu-id="3399e-128">??. Perfd0 incrementa</span><span class="sxs-lookup"><span data-stu-id="3399e-128">Perfd0??.dat</span></span>  
<span data-ttu-id="3399e-129">??. Perfh0 incrementa</span><span class="sxs-lookup"><span data-stu-id="3399e-129">Perfh0??.dat</span></span>  
<span data-ttu-id="3399e-130">??. Perfi0 incrementa</span><span class="sxs-lookup"><span data-stu-id="3399e-130">Perfi0??.dat</span></span>  
<span data-ttu-id="3399e-131">???. Prfc0 incrementa</span><span class="sxs-lookup"><span data-stu-id="3399e-131">Prfc0???.dat</span></span>  
<span data-ttu-id="3399e-132">???. Prfd0 incrementa</span><span class="sxs-lookup"><span data-stu-id="3399e-132">Prfd0???.dat</span></span>  
<span data-ttu-id="3399e-133">???. Prfh0 incrementa</span><span class="sxs-lookup"><span data-stu-id="3399e-133">Prfh0???.dat</span></span>  
<span data-ttu-id="3399e-134">???. Prfi0 incrementa</span><span class="sxs-lookup"><span data-stu-id="3399e-134">Prfi0???.dat</span></span>  
</dl>

<span data-ttu-id="3399e-135">Estos archivos solo se modifican durante la instalación de la aplicación y se deben realizar copias de seguridad y restaurar durante las copias de seguridad y restauraciones del estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="3399e-135">These files are only modified during application installation and should be backed up and restored during system state backups and restores.</span></span>

## <a name="iis-configuration-files"></a><span data-ttu-id="3399e-136">Archivos de configuración de IIS</span><span class="sxs-lookup"><span data-stu-id="3399e-136">IIS Configuration Files</span></span>

> [!Note]  
> <span data-ttu-id="3399e-137">En Windows Vista con Service Pack 1 (SP1) y versiones posteriores, no debe hacer una copia de seguridad de estos archivos.</span><span class="sxs-lookup"><span data-stu-id="3399e-137">In Windows Vista with Service Pack 1 (SP1) and later, you should not back up these files.</span></span> <span data-ttu-id="3399e-138">En su lugar, use el escritor de configuración de IIS en la caja.</span><span class="sxs-lookup"><span data-stu-id="3399e-138">Instead, use the in-box IIS configuration writer.</span></span> <span data-ttu-id="3399e-139">Para obtener más información sobre este escritor, consulte [escritores de VSS en la caja](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="3399e-139">For more information about this writer, see [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

<span data-ttu-id="3399e-140">A continuación se enumeran los archivos de configuración de IIS relevantes y sus ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="3399e-140">The relevant IIS configuration files and their locations are listed below:</span></span>

-   <span data-ttu-id="3399e-141">El archivo de machine.config de .NET FX se encuentra en el directorio de la versión de Framework.</span><span class="sxs-lookup"><span data-stu-id="3399e-141">The .NET FX machine.config file is located in the framework version directory.</span></span>
-   <span data-ttu-id="3399e-142">El archivo web.config raíz ASP.NET se encuentra en el directorio de la versión de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="3399e-142">The ASP.NET root web.config file is located in the framework version directory.</span></span>
    > [!Note]  
    > <span data-ttu-id="3399e-143">Los archivos de configuración de .NET FX y ASP.NET se encuentran en el directorio de versión de Framework.</span><span class="sxs-lookup"><span data-stu-id="3399e-143">The configuration files for both .NET FX and ASP.NET are in the framework version directory.</span></span> <span data-ttu-id="3399e-144">Si hay varias versiones de Framework instaladas en el equipo, este directorio contendrá un archivo de configuración para cada versión instalada.</span><span class="sxs-lookup"><span data-stu-id="3399e-144">If multiple versions of the framework are installed on the computer, this directory will contain one configuration file for each installed version.</span></span>

     

-   <span data-ttu-id="3399e-145">El archivo de configuración central de IIS applicationHost.config se encuentra en el directorio% WINDIR% \\ system32 \\ Inetsrv \\ config.</span><span class="sxs-lookup"><span data-stu-id="3399e-145">The IIS applicationHost.config central configuration file is located in the %windir%\\system32\\inetsrv\\config directory.</span></span> <span data-ttu-id="3399e-146">Para que el servidor comprenda este archivo de configuración, hay archivos de esquema que determinan su gramática y estructura.</span><span class="sxs-lookup"><span data-stu-id="3399e-146">For the server to understand this configuration file, there are schema files that determine its grammar and structure.</span></span> <span data-ttu-id="3399e-147">Estos archivos se encuentran en el directorio% WINDIR% \\ system32 \\ Inetsrv \\ config \\ Schema.</span><span class="sxs-lookup"><span data-stu-id="3399e-147">These files are located in the %windir%\\system32\\inetsrv\\config\\schema directory.</span></span>

<span data-ttu-id="3399e-148">La ruta de acceso del directorio de la versión de Framework se almacena en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="3399e-148">The framework version directory path is stored in the following registry key:</span></span>

<span data-ttu-id="3399e-149">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ . NETFramework \\ InstallRoot**</span><span class="sxs-lookup"><span data-stu-id="3399e-149">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\.NETFramework\\InstallRoot**</span></span>

<span data-ttu-id="3399e-150">Además, se debe realizar una copia de seguridad de las claves de cifrado siguientes:</span><span class="sxs-lookup"><span data-stu-id="3399e-150">In addition, the following cryptography keys must be backed up:</span></span><dl> <span data-ttu-id="3399e-151">% ProgramData% \\ Microsoft \\ Crypto \\ RSA \\ MachineKeys\\\*</span><span class="sxs-lookup"><span data-stu-id="3399e-151">%ProgramData%\\Microsoft\\Crypto\\RSA\\MachineKeys\\\*</span></span>  
<span data-ttu-id="3399e-152">% SystemRoot% \\ system32 \\ Microsoft \\ Protect\\\*</span><span class="sxs-lookup"><span data-stu-id="3399e-152">%SystemRoot%\\System32\\Microsoft\\Protect\\\*</span></span>  
</dl>

## <a name="framework-files"></a><span data-ttu-id="3399e-153">Archivos de marco</span><span class="sxs-lookup"><span data-stu-id="3399e-153">Framework Files</span></span>

<span data-ttu-id="3399e-154">Se debe realizar una copia de seguridad de todas las versiones de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="3399e-154">All versions of the .NET framework must be backed up.</span></span> <span data-ttu-id="3399e-155">Los archivos se encuentran en uno de los siguientes directorios o en ambos:</span><span class="sxs-lookup"><span data-stu-id="3399e-155">The files are located in one or both of the following directories:</span></span>

<dl> <span data-ttu-id="3399e-156">% WINDIR% \\ Microsoft.net \\ Framework</span><span class="sxs-lookup"><span data-stu-id="3399e-156">%windir%\\Microsoft.Net\\Framework</span></span>  
<span data-ttu-id="3399e-157">% WINDIR% \\ Microsoft.net \\ Framework64</span><span class="sxs-lookup"><span data-stu-id="3399e-157">%windir%\\Microsoft.Net\\Framework64</span></span>  
</dl>

<span data-ttu-id="3399e-158">Además, se debe realizar una copia de seguridad de los archivos de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="3399e-158">In addition, the assembly files must be backed up.</span></span> <span data-ttu-id="3399e-159">Estos archivos están ubicados en el directorio siguiente:</span><span class="sxs-lookup"><span data-stu-id="3399e-159">These files are located in the following directory:</span></span><dl> <span data-ttu-id="3399e-160">% WINDIR% \\ Assembly</span><span class="sxs-lookup"><span data-stu-id="3399e-160">%windir%\\assembly</span></span>  
</dl>

## <a name="task-scheduler-task-files"></a><span data-ttu-id="3399e-161">Archivos de tareas de Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="3399e-161">Task Scheduler Task Files</span></span>

<span data-ttu-id="3399e-162">Se debe realizar una copia de seguridad de los archivos de tarea del programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="3399e-162">The task scheduler's task files must be backed up.</span></span> <span data-ttu-id="3399e-163">Los archivos se encuentran en una o las dos ubicaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="3399e-163">The files are located in one or both of the following locations:</span></span>

<dl> <span data-ttu-id="3399e-164">% WINDIR% \\ system32 \\ Tasks y cualquier subdirectorio (recursivamente)</span><span class="sxs-lookup"><span data-stu-id="3399e-164">%windir%\\system32\\tasks and any subdirectories (recursively)</span></span>  
<span data-ttu-id="3399e-165">% WINDIR% \\ Tasks (sin subdirectorios)</span><span class="sxs-lookup"><span data-stu-id="3399e-165">%windir%\\tasks (no subdirectories)</span></span>  
</dl>

 

 
