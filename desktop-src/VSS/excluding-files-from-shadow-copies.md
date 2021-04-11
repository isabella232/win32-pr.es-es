---
description: En Windows Vista y Windows Server 2008 y versiones posteriores, el desarrollador de una VSS Writer o aplicación puede optar por excluir determinados archivos de las instantáneas.
ms.assetid: 4fe1ae94-7b2f-421a-9009-3a7e88822458
title: Excluir archivos de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52546c8ddc6da62433dc610f2bf4fc2c46c5e53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279127"
---
# <a name="excluding-files-from-shadow-copies"></a><span data-ttu-id="79de8-103">Excluir archivos de instantáneas</span><span class="sxs-lookup"><span data-stu-id="79de8-103">Excluding Files from Shadow Copies</span></span>

<span data-ttu-id="79de8-104">En Windows Vista y Windows Server 2008 y versiones posteriores, el desarrollador de una VSS Writer o aplicación puede optar por excluir determinados archivos de las instantáneas.</span><span class="sxs-lookup"><span data-stu-id="79de8-104">In Windows Vista and Windows Server 2008 and later, the developer of a VSS writer or application may choose to exclude certain files from shadow copies.</span></span>

<span data-ttu-id="79de8-105">El área de almacenamiento de instantáneas y el impacto en el rendimiento (también denominado "área de diferenciación") de un archivo en una instantánea se relacionan directamente con la cantidad de cambios en el contenido del archivo una vez creada la instantánea.</span><span class="sxs-lookup"><span data-stu-id="79de8-105">The performance impact and shadow copy storage area (also called "diff area") usage of a file in a shadow copy are directly related to the amount of change in the file's contents after the shadow copy is created.</span></span> <span data-ttu-id="79de8-106">Además, la exclusión de archivos de instantáneas puede ralentizar la creación de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="79de8-106">In addition, excluding files from shadow copies may slow down shadow copy creation.</span></span>

<span data-ttu-id="79de8-107">Por estos motivos, se debe excluir un archivo de las instantáneas solo si es grande, se producirá un cambio significativo entre una instantánea y la siguiente, y no es necesario hacer una copia de seguridad de ella.</span><span class="sxs-lookup"><span data-stu-id="79de8-107">For these reasons, a file should be excluded from shadow copies only if it is large, undergoes significant change between one shadow copy and the next, and does not need to be backed up.</span></span>

<span data-ttu-id="79de8-108">Solo debe excluir los archivos que pertenezcan a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="79de8-108">You should only exclude files that belong to your application.</span></span>

<span data-ttu-id="79de8-109">Si la \_ marca VSS VOLSNAP \_ ATTR \_ no \_ se ha establecido el marcador de Autorrecuperación en el contexto de instantáneas, significa que la recuperación automática está deshabilitada y que no se puede excluir ningún archivo de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="79de8-109">If the VSS\_VOLSNAP\_ATTR\_NO\_AUTORECOVERY flag is set in the shadow copy context, this means that auto-recovery is disabled, and no files can be excluded from the shadow copy.</span></span> <span data-ttu-id="79de8-110">Para obtener más información, consulte la enumeración de [**\_ \_ \_ \_ atributos de instantáneas de volumen de VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) .</span><span class="sxs-lookup"><span data-stu-id="79de8-110">For more information, see the [**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration.</span></span>

## <a name="using-the-addexcludefilesfromsnapshot-method"></a><span data-ttu-id="79de8-111">Usar el método AddExcludeFilesFromSnapshot</span><span class="sxs-lookup"><span data-stu-id="79de8-111">Using the AddExcludeFilesFromSnapshot Method</span></span>

<span data-ttu-id="79de8-112">Un VSS Writer puede excluir archivos de una instantánea de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="79de8-112">A VSS writer can exclude files from a shadow copy as follows:</span></span>

1.  <span data-ttu-id="79de8-113">Llame al método [**IVssCreateWriterMetadataEx:: AddExcludeFilesFromSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) para notificar los archivos que se van a excluir.</span><span class="sxs-lookup"><span data-stu-id="79de8-113">Call the [**IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) method to report the files to be excluded.</span></span>
2.  <span data-ttu-id="79de8-114">En el método [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) del escritor, elimine los archivos de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="79de8-114">In the writer's [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) method, delete the files from the shadow copy.</span></span>

## <a name="using-the-filesnottosnapshot-registry-key"></a><span data-ttu-id="79de8-115">Uso de la clave del registro FilesNotToSnapshot</span><span class="sxs-lookup"><span data-stu-id="79de8-115">Using the FilesNotToSnapshot Registry Key</span></span>

> [!Note]  
> <span data-ttu-id="79de8-116">La clave del registro **FilesNotToSnapshot** está pensada para que solo las aplicaciones la usen.</span><span class="sxs-lookup"><span data-stu-id="79de8-116">The **FilesNotToSnapshot** registry key is intended to be used only by applications.</span></span> <span data-ttu-id="79de8-117">Los usuarios que intenten usarla tendrán limitaciones como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="79de8-117">Users who attempt to use it will encounter limitations such as the following:</span></span>
>
> -   <span data-ttu-id="79de8-118">No puede eliminar archivos de una instantánea creada en Windows Server mediante la característica Versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="79de8-118">It cannot delete files from a shadow copy that was created on a Windows Server by using the Previous Versions feature.</span></span>
> -   <span data-ttu-id="79de8-119">No puede eliminar archivos de las instantáneas para carpetas compartidas.</span><span class="sxs-lookup"><span data-stu-id="79de8-119">It cannot delete files from shadow copies for shared folders.</span></span>
> -   <span data-ttu-id="79de8-120">Puede eliminar archivos de una instantánea que se haya creado con la utilidad [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) , pero no puede eliminar archivos de una instantánea creada con la utilidad [vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="79de8-120">It can delete files from a shadow copy that was created by using the [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) utility, but it cannot delete files from a shadow copy that was created by using the [Vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) utility.</span></span>
> -   <span data-ttu-id="79de8-121">Los archivos se eliminan de una instantánea en función de la mejor opción.</span><span class="sxs-lookup"><span data-stu-id="79de8-121">Files are deleted from a shadow copy on a best-effort basis.</span></span> <span data-ttu-id="79de8-122">Como resultado, no se garantiza que se eliminen.</span><span class="sxs-lookup"><span data-stu-id="79de8-122">This means that they are not guaranteed to be deleted.</span></span>

 

<span data-ttu-id="79de8-123">Una aplicación VSS puede eliminar archivos de una instantánea durante la creación de instantáneas mediante la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="79de8-123">A VSS application can delete files from a shadow copy during shadow copy creation by using the following registry key:</span></span>

<span data-ttu-id="79de8-124">**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ BackupRestore \\ FilesNotToSnapshot**</span><span class="sxs-lookup"><span data-stu-id="79de8-124">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\BackupRestore\\FilesNotToSnapshot**</span></span>

<span data-ttu-id="79de8-125">Esta clave del registro tiene \_ \_ valores de reg multi SZ para cada aplicación cuyos archivos se pueden excluir.</span><span class="sxs-lookup"><span data-stu-id="79de8-125">This registry key has REG\_MULTI\_SZ values for each application whose files can be excluded.</span></span> <span data-ttu-id="79de8-126">Los archivos se especifican mediante rutas de acceso completas, que pueden contener el \* carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="79de8-126">The files are specified by fully qualified paths, which can contain the \* wildcard.</span></span>

<span data-ttu-id="79de8-127">En todos los casos, la entrada se omite si no hay archivos que coincidan con la cadena de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="79de8-127">In all cases, the entry is ignored if there are no files that match the path string.</span></span>

<span data-ttu-id="79de8-128">Después de agregar un archivo al valor de clave del registro adecuado, se elimina de la instantánea durante la creación del escritor de optimización de instantáneas de la mejor manera posible.</span><span class="sxs-lookup"><span data-stu-id="79de8-128">After a file is added to the appropriate registry key value, it is deleted from the shadow copy during creation by the shadow copy optimization writer on a best-effort basis.</span></span>

<span data-ttu-id="79de8-129">Si no se puede especificar una ruta de acceso completa, una ruta de acceso también puede estar implícita mediante la $UserProfile $ o la variable $AllVolumes $.</span><span class="sxs-lookup"><span data-stu-id="79de8-129">If a fully qualified path cannot be specified, then a path can also be implied by using the $UserProfile$ or $AllVolumes$ variable.</span></span> <span data-ttu-id="79de8-130">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="79de8-130">For example:</span></span>

-   <span data-ttu-id="79de8-131">$UserProfile \\ nombre de \\ archivo del subdirectorio $ Directory \\ .\*</span><span class="sxs-lookup"><span data-stu-id="79de8-131">$UserProfile$\\Directory\\Subdirectory\\FileName.\*</span></span>
-   <span data-ttu-id="79de8-132">$AllVolumes $ \\ TemporaryFiles \\ \* .\*</span><span class="sxs-lookup"><span data-stu-id="79de8-132">$AllVolumes$\\TemporaryFiles\\\*.\*</span></span>

<span data-ttu-id="79de8-133">Para que la ruta de acceso sea recursiva, anexe "/s" al final.</span><span class="sxs-lookup"><span data-stu-id="79de8-133">To make the path recursive, append " /s" to the end.</span></span> <span data-ttu-id="79de8-134">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="79de8-134">For example:</span></span>

-   <span data-ttu-id="79de8-135">$UserProfile $ \\ Directory \\ subdirectorio \\ nombreDeArchivo. \* /s</span><span class="sxs-lookup"><span data-stu-id="79de8-135">$UserProfile$\\Directory\\Subdirectory\\FileName.\* /s</span></span>
-   <span data-ttu-id="79de8-136">$AllVolumes $ \\ TemporaryFiles \\ \* . \* /s</span><span class="sxs-lookup"><span data-stu-id="79de8-136">$AllVolumes$\\TemporaryFiles\\\*.\* /s</span></span>

<span data-ttu-id="79de8-137">La variable $UserProfile $ hace que la cadena de ruta de acceso se aplique a todos los perfiles de usuario del equipo.</span><span class="sxs-lookup"><span data-stu-id="79de8-137">The $UserProfile$ variable causes the path string to be applied to all user profiles on the computer.</span></span> <span data-ttu-id="79de8-138">Los perfiles de usuario se enumeran examinando la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="79de8-138">The user profiles are enumerated by examining the following registry key:</span></span>

<span data-ttu-id="79de8-139">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ProfileList**</span><span class="sxs-lookup"><span data-stu-id="79de8-139">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\ProfileList**</span></span>

<span data-ttu-id="79de8-140">La variable $AllVolumes $ hace que la cadena de ruta de acceso se aplique a todas las instantáneas del equipo.</span><span class="sxs-lookup"><span data-stu-id="79de8-140">The $AllVolumes$ variable causes the path string to be applied to all shadow copies on the computer.</span></span> <span data-ttu-id="79de8-141">Por ejemplo, supongamos que la ruta de acceso es "$AllVolumes $ \\ TemporaryFiles \\ \* . \* /s ", y el equipo tiene tres volúmenes: C:, D: y E:.</span><span class="sxs-lookup"><span data-stu-id="79de8-141">For example, suppose the path is "$AllVolumes$\\TemporaryFiles\\\*.\* /s", and the computer has three volumes: C:, D:, and E:.</span></span> <span data-ttu-id="79de8-142">Si C: y E: contienen la ruta de acceso " \\ TemporaryFiles \\ " y el volumen d: contiene solo la ruta de acceso d: \\ Data \\ , el árbol de directorio c: \\ TemporaryFiles \\ se elimina de las instantáneas de C: y el árbol de directorios E: \\ TemporaryFiles \\ se elimina de las instantáneas de E:.</span><span class="sxs-lookup"><span data-stu-id="79de8-142">If C: and E: contain the path "\\TemporaryFiles\\", and volume D: contains only the path D:\\Data\\, the directory tree C:\\TemporaryFiles\\ is deleted from shadow copies of C:, and the directory tree E:\\TemporaryFiles\\ is deleted from shadow copies of E:.</span></span>

<span data-ttu-id="79de8-143">Los administradores pueden deshabilitar la expansión de la variable $UserProfile $ mediante la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="79de8-143">Administrators can disable expansion of the $UserProfile$ variable by using the following registry key:</span></span>

<span data-ttu-id="79de8-144">**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ configuración de VSS \\**</span><span class="sxs-lookup"><span data-stu-id="79de8-144">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Vss\\Settings**</span></span>

<span data-ttu-id="79de8-145">En esta clave del registro, especifique DisableUserProfileExpansion para el nombre del valor, REG \_ DWORD para el tipo de valor y un valor distinto de cero para los datos del valor.</span><span class="sxs-lookup"><span data-stu-id="79de8-145">Under this registry key, specify DisableUserProfileExpansion for the value name, REG\_DWORD for the value type, and a nonzero value for the value data.</span></span>

## <a name="about-the-filesnottobackup-registry-key"></a><span data-ttu-id="79de8-146">Acerca de la clave del registro FilesNotToBackup</span><span class="sxs-lookup"><span data-stu-id="79de8-146">About the FilesNotToBackup Registry Key</span></span>

<span data-ttu-id="79de8-147">La clave del registro **FilesNotToBackup** se puede usar para especificar los nombres de los archivos y directorios en los que las aplicaciones de copia de seguridad no deben realizar copias de seguridad ni restaurar.</span><span class="sxs-lookup"><span data-stu-id="79de8-147">The **FilesNotToBackup** registry key can be used to specify the names of the files and directories that backup applications should not backup or restore.</span></span> <span data-ttu-id="79de8-148">Sin embargo, no excluye esos archivos de las instantáneas.</span><span class="sxs-lookup"><span data-stu-id="79de8-148">However, it does not exclude those files from shadow copies.</span></span> <span data-ttu-id="79de8-149">Para obtener más información acerca de esta clave del registro, consulte [claves y valores del registro para copias de seguridad y restauración](../backup/registry-keys-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="79de8-149">For more information about this registry key, see [Registry Keys and Values for Backup and Restore](../backup/registry-keys-for-backup-and-restore.md).</span></span>

 

 
