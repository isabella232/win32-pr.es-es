---
description: VShadow es una herramienta de línea de comandos que puede usar para crear y administrar instantáneas de volumen.
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: Herramienta y ejemplo de VShadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7a9a697ecdf39f91d43fa0c66faebd37cfbfed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497524"
---
# <a name="vshadow-tool-and-sample"></a><span data-ttu-id="473c2-103">Herramienta y ejemplo de VShadow</span><span class="sxs-lookup"><span data-stu-id="473c2-103">VShadow Tool and Sample</span></span>

<span data-ttu-id="473c2-104">VShadow es una herramienta de línea de comandos que puede usar para crear y administrar instantáneas de volumen.</span><span class="sxs-lookup"><span data-stu-id="473c2-104">VShadow is a command-line tool that you can use to create and manage volume shadow copies.</span></span>

> [!Note]  
> <span data-ttu-id="473c2-105">VShadow se incluye en el kit de desarrollo de software (SDK) de Microsoft Windows para Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="473c2-105">VShadow is included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="473c2-106">El SDK de VSS 7,2 incluye una versión de VShadow que solo se ejecuta en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="473c2-106">The VSS 7.2 SDK includes a version of VShadow that runs only on Windows Server 2003.</span></span> <span data-ttu-id="473c2-107">Para obtener información acerca de cómo descargar el Windows SDK y el SDK de VSS 7,2, consulte [servicio de instantáneas de volumen](volume-shadow-copy-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="473c2-107">For information about downloading the Windows SDK and the VSS 7.2 SDK, see [Volume Shadow Copy Service](volume-shadow-copy-service-portal.md).</span></span>

 

<span data-ttu-id="473c2-108">La herramienta VShadow utiliza opciones de la línea de comandos y marcas opcionales para identificar el trabajo que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="473c2-108">The VShadow tool uses command-line options and optional flags to identify the work to perform.</span></span> <span data-ttu-id="473c2-109">Cuando se usa sin ninguna opción de línea de comandos, el comando VShadow crea un nuevo conjunto de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="473c2-109">When used without any command-line options, the VShadow command creates a new shadow copy set.</span></span>

<span data-ttu-id="473c2-110">Los comandos de VShadow realizan las operaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="473c2-110">VShadow commands perform the following operations:</span></span>

-   [<span data-ttu-id="473c2-111">Crear un conjunto de instantáneas</span><span class="sxs-lookup"><span data-stu-id="473c2-111">Creating a Shadow Copy Set</span></span>](#creating-a-shadow-copy-set)
-   [<span data-ttu-id="473c2-112">Importar un conjunto de instantáneas</span><span class="sxs-lookup"><span data-stu-id="473c2-112">Importing a Shadow Copy Set</span></span>](#importing-a-shadow-copy-set)
-   [<span data-ttu-id="473c2-113">Consultar propiedades de instantáneas</span><span class="sxs-lookup"><span data-stu-id="473c2-113">Querying Shadow Copy Properties</span></span>](#querying-shadow-copy-properties)
-   [<span data-ttu-id="473c2-114">Eliminar instantáneas</span><span class="sxs-lookup"><span data-stu-id="473c2-114">Deleting Shadow Copies</span></span>](#deleting-shadow-copies)
-   [<span data-ttu-id="473c2-115">Dividir un conjunto de instantáneas</span><span class="sxs-lookup"><span data-stu-id="473c2-115">Breaking a Shadow Copy Set</span></span>](#breaking-a-shadow-copy-set)
-   [<span data-ttu-id="473c2-116">Dividir un conjunto de instantáneas mediante el método BreakSnapshotSetEx</span><span class="sxs-lookup"><span data-stu-id="473c2-116">Breaking a Shadow Copy Set Using the BreakSnapshotSetEx Method</span></span>](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [<span data-ttu-id="473c2-117">Exponer una instantánea localmente</span><span class="sxs-lookup"><span data-stu-id="473c2-117">Exposing a Shadow Copy Locally</span></span>](#exposing-a-shadow-copy-locally)
-   [<span data-ttu-id="473c2-118">Exponer una instantánea de forma remota</span><span class="sxs-lookup"><span data-stu-id="473c2-118">Exposing a Shadow Copy Remotely</span></span>](#exposing-a-shadow-copy-remotely)
-   [<span data-ttu-id="473c2-119">Enumerar el estado y los metadatos del escritor</span><span class="sxs-lookup"><span data-stu-id="473c2-119">Listing Writer Status and Metadata</span></span>](#listing-writer-status-and-metadata)
-   [<span data-ttu-id="473c2-120">Realización de operaciones de restauración</span><span class="sxs-lookup"><span data-stu-id="473c2-120">Performing Restore Operations</span></span>](#performing-restore-operations)
-   [<span data-ttu-id="473c2-121">Revertir a una instantánea anterior</span><span class="sxs-lookup"><span data-stu-id="473c2-121">Reverting to a Previous Shadow Copy</span></span>](#reverting-to-a-previous-shadow-copy)
-   [<span data-ttu-id="473c2-122">Volver a sincronizar LUN</span><span class="sxs-lookup"><span data-stu-id="473c2-122">Resynchronizing LUNs</span></span>](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a><span data-ttu-id="473c2-123">Crear un conjunto de instantáneas</span><span class="sxs-lookup"><span data-stu-id="473c2-123">Creating a Shadow Copy Set</span></span>

<span data-ttu-id="473c2-124">**vshadow** \[ OptionalFlags \] *VolumeList*</span><span class="sxs-lookup"><span data-stu-id="473c2-124">**vshadow** \[OptionalFlags\] *VolumeList*</span></span>

<span data-ttu-id="473c2-125">Este comando crea un nuevo conjunto de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="473c2-125">This command creates a new shadow copy set.</span></span>

<span data-ttu-id="473c2-126">*VolumeList* es una lista de nombres de volumen.</span><span class="sxs-lookup"><span data-stu-id="473c2-126">*VolumeList* is a list of volume names.</span></span> <span data-ttu-id="473c2-127">VShadow crea una instantánea para cada volumen de la lista.</span><span class="sxs-lookup"><span data-stu-id="473c2-127">VShadow creates one shadow copy for each volume in the list.</span></span> <span data-ttu-id="473c2-128">Opcionalmente, un nombre de volumen puede terminar con una barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="473c2-128">A volume name can optionally be terminated with a backslash (\\).</span></span> <span data-ttu-id="473c2-129">Por ejemplo, C: y C: \\ son nombres de volumen válidos.</span><span class="sxs-lookup"><span data-stu-id="473c2-129">For example, both C: and C:\\ are valid volume names.</span></span> <span data-ttu-id="473c2-130">También puede especificar las carpetas montadas (por ejemplo, C: \\ directoryname) o los nombres de GUID de volumen (por ejemplo, \\ \\ ? \\ Volumen {edbed95e-7e8d-11d8-9d01-505054503030}).</span><span class="sxs-lookup"><span data-stu-id="473c2-130">You can also specify mounted folders (for example, C:\\DirectoryName) or volume GUID names (for example, \\\\?\\Volume{edbed95e-7e8d-11d8-9d01-505054503030}).</span></span>

<span data-ttu-id="473c2-131">*OptionalFlags* es una máscara de máscara de valores de marca opcionales de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="473c2-131">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="473c2-132">Valor opcional de marca</span><span class="sxs-lookup"><span data-stu-id="473c2-132">Optional Flag Value</span></span></th>
<th><span data-ttu-id="473c2-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="473c2-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="473c2-134"><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-134"><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-135">Esta marca opcional especifica las instantáneas de hardware diferenciales.</span><span class="sxs-lookup"><span data-stu-id="473c2-135">This optional flag specifies differential hardware shadow copies.</span></span> <span data-ttu-id="473c2-136">Esta marca y la marca <strong>-AP</strong> son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="473c2-136">This flag and the <strong>-ap</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="473c2-137">Esta marca solo se admite en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-137">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="473c2-138"><span id="-ap"></span><span id="-AP"></span><strong>-AP</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-138"><span id="-ap"></span><span id="-AP"></span><strong>-ap</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-139">Esta marca opcional especifica las instantáneas de hardware de Plex.</span><span class="sxs-lookup"><span data-stu-id="473c2-139">This optional flag specifies plex hardware shadow copies.</span></span> <span data-ttu-id="473c2-140">Esta marca y la marca <strong>-ad</strong> son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="473c2-140">This flag and the <strong>-ad</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="473c2-141">Esta marca solo se admite en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-141">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="473c2-142"><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong> <strong>-BC =</strong><em>File</em><strong>. XML</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-142"><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span> <strong></strong> <strong>-bc=</strong><em>File</em><strong>.xml</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-143">Esta marca opcional especifica las instantáneas no transportables y almacena el documento de componentes de copia de seguridad en el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="473c2-143">This optional flag specifies non-transportable shadow copies and stores the Backup Components Document into the specified file.</span></span> <span data-ttu-id="473c2-144">Este archivo se puede usar en una operación de restauración posterior.</span><span class="sxs-lookup"><span data-stu-id="473c2-144">This file can be used in a subsequent restore operation.</span></span> <span data-ttu-id="473c2-145">Esta marca y la marca <strong>-t</strong> son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="473c2-145">This flag and the <strong>-t</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="473c2-146">Esta marca solo se admite en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-146">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="473c2-147"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec =</strong><em>comando</em></span><span class="sxs-lookup"><span data-stu-id="473c2-147"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec=</strong><em>Command</em></span></span><br/></td>
<td><span data-ttu-id="473c2-148">Esta marca opcional ejecuta un comando o script después de crear las instantáneas, pero antes de que se cierre la herramienta VShadow.</span><span class="sxs-lookup"><span data-stu-id="473c2-148">This optional flag executes a command or script after the shadow copies are created but before the VShadow tool exits.</span></span> <span data-ttu-id="473c2-149">El <em>comando</em> puede especificar un comando de Shell ejecutable o un archivo CMD.</span><span class="sxs-lookup"><span data-stu-id="473c2-149"><em>Command</em> can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="473c2-150">Si especifica un comando de Shell, no se puede especificar ningún parámetro de comando.</span><span class="sxs-lookup"><span data-stu-id="473c2-150">If it specifies a shell command, no command parameters can be specified.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="473c2-151">Por motivos de seguridad y para simplificar la implementación, la marca opcional <strong>-exec</strong> no aceptará los parámetros que se van a pasar al comando o script.</span><span class="sxs-lookup"><span data-stu-id="473c2-151">For security reasons and to keep the implementation simple, the <strong>-exec</strong> optional flag will not accept parameters to be passed to the command or script.</span></span> <span data-ttu-id="473c2-152">La cadena completa pasada a la marca opcional <strong>-exec</strong> se trata como un único archivo CMD o exe.</span><span class="sxs-lookup"><span data-stu-id="473c2-152">The entire string passed to the <strong>-exec</strong> optional flag is treated as a single CMD or EXE file.</span></span> <span data-ttu-id="473c2-153">Para obtener más información sobre esta limitación, vea el código fuente de VShadow.</span><span class="sxs-lookup"><span data-stu-id="473c2-153">For more information about this limitation, see the VShadow source code.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="473c2-154"><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-154"><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-155">Esta marca opcional Especifica que la operación de instantáneas se debe completar solo si se pueden revertir todas las firmas de disco.</span><span class="sxs-lookup"><span data-stu-id="473c2-155">This optional flag specifies that the shadow copy operation should be completed only if all disk signatures can be reverted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="473c2-156">Esta marca solo se admite en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-156">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="473c2-157"><strong>Windows Server 2003:</strong> No compatible.</span><span class="sxs-lookup"><span data-stu-id="473c2-157"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="473c2-158"><span id="-mask"></span><span id="-MASK"></span><strong>-máscara</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-158"><span id="-mask"></span><span id="-MASK"></span><strong>-mask</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-159">Esta marca opcional Especifica que los LUN de instantáneas deben enmascararse del equipo cuando se interrumpe el conjunto de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="473c2-159">This optional flag specifies that the shadow copy LUNs should be masked from the computer when the shadow copy set is broken.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="473c2-160">Esta marca solo se admite en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-160">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="473c2-161"><strong>Windows Server 2003:</strong> No compatible.</span><span class="sxs-lookup"><span data-stu-id="473c2-161"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="473c2-162"><span id="-nar"></span><span id="-NAR"></span><strong>-Nar</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-162"><span id="-nar"></span><span id="-NAR"></span><strong>-nar</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-163">Esta marca opcional especifica instantáneas sin recuperación automática.</span><span class="sxs-lookup"><span data-stu-id="473c2-163">This optional flag specifies shadow copies without auto-recovery.</span></span> <span data-ttu-id="473c2-164">Para obtener más información acerca de esta opción, consulte la documentación de la VSS_VOLSNAP_ATTR_NO_AUTORECOVERY marca de la enumeración <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="473c2-164">For more information about this option, see the documentation for the VSS_VOLSNAP_ATTR_NO_AUTORECOVERY flag of the <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> enumeration.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="473c2-165"><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-165"><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-166">Esta marca opcional Especifica que las firmas de disco no se deben revertir.</span><span class="sxs-lookup"><span data-stu-id="473c2-166">This optional flag specifies that disk signatures should not be reverted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="473c2-167">Esta marca solo se admite en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-167">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="473c2-168"><strong>Windows Server 2003:</strong> No compatible.</span><span class="sxs-lookup"><span data-stu-id="473c2-168"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="473c2-169"><span id="-nw"></span><span id="-NW"></span><strong>-NW</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-169"><span id="-nw"></span><span id="-NW"></span><strong>-nw</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-170">Esta marca opcional especifica instantáneas sin necesidad de escritores.</span><span class="sxs-lookup"><span data-stu-id="473c2-170">This optional flag specifies shadow copies without involving writers.</span></span> <span data-ttu-id="473c2-171">Para obtener más información sobre las instantáneas sin participación del escritor, consulte los <a href="shadow-copy-creation-details.md">detalles de creación de instantáneas</a>.</span><span class="sxs-lookup"><span data-stu-id="473c2-171">For more information about shadow copies without writer participation, see <a href="shadow-copy-creation-details.md">Shadow Copy Creation Details</a>.</span></span> <span data-ttu-id="473c2-172">Esta marca y las marcas <strong>-Wi</strong> y <strong>-WX</strong> son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="473c2-172">This flag and the <strong>-wi</strong> and <strong>-wx</strong> flags are mutually exclusive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="473c2-173"><span id="-p"></span><span id="-P"></span><strong>-p</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-173"><span id="-p"></span><span id="-P"></span><strong>-p</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-174">Esta marca opcional especifica <a href="vssgloss-p.md"><em>instantáneas persistentes</em></a>.</span><span class="sxs-lookup"><span data-stu-id="473c2-174">This optional flag specifies <a href="vssgloss-p.md"><em>persistent shadow copies</em></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="473c2-175">Esta marca solo se admite en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-175">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="473c2-176"><span id="-rw"></span><span id="-RW"></span><strong>-RW</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-176"><span id="-rw"></span><span id="-RW"></span><strong>-rw</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-177">Esta marca opcional Especifica que los LUN de instantánea deben ser de lectura y escritura cuando se interrumpa el conjunto de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="473c2-177">This optional flag specifies that the shadow copy LUNs should be made read/write when the shadow copy set is broken.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="473c2-178">Esta marca solo se admite en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-178">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="473c2-179"><strong>Windows Server 2003:</strong> No compatible.</span><span class="sxs-lookup"><span data-stu-id="473c2-179"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="473c2-180"><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-180"><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-181">Esta marca opcional especifica <a href="vssgloss-c.md"><em>instantáneas accesibles para el cliente</em></a>.</span><span class="sxs-lookup"><span data-stu-id="473c2-181">This optional flag specifies <a href="vssgloss-c.md"><em>client-accessible shadow copies</em></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="473c2-182">Esta marca solo se admite en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-182">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="473c2-183"><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script =</strong><em>archivo</em><strong>. cmd</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-183"><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script=</strong><em>File</em><strong>.cmd</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-184">Esta marca opcional genera un archivo CMD que contiene variables de entorno relacionadas con las instantáneas creadas, como identificadores de instantáneas e identificadores de conjuntos de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="473c2-184">This optional flag generates a CMD file containing environment variables related to the created shadow copies, such as shadow copy IDs and shadow copy set IDs.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="473c2-185"><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t =</strong><em>File</em><strong>. XML</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-185"><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t=</strong><em>File</em><strong>.xml</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-186">Esta marca opcional especifica las instantáneas transportables y almacena el documento de componentes de copia de seguridad en el archivo especificado por el parámetro <em>File.xml</em> .</span><span class="sxs-lookup"><span data-stu-id="473c2-186">This optional flag specifies transportable shadow copies and stores the Backup Components Document into the file specified by the <em>File.xml</em> parameter.</span></span> <span data-ttu-id="473c2-187">Este archivo se puede usar en una operación de importación o restauración posterior.</span><span class="sxs-lookup"><span data-stu-id="473c2-187">This file can be used in a subsequent import and/or restore operation.</span></span> <span data-ttu-id="473c2-188">Esta marca y la marca <strong>-BC</strong> se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="473c2-188">This flag and the <strong>-bc</strong> flag are mutually exclusive.</span></span><br/> <span data-ttu-id="473c2-189"><strong>Windows server 2003, Standard Edition y Windows server 2003, Web Edition:</strong> No se admiten las instantáneas transportables.</span><span class="sxs-lookup"><span data-stu-id="473c2-189"><strong>Windows Server 2003, Standard Edition and Windows Server 2003, Web Edition:</strong> Transportable shadow copies are not supported.</span></span> <span data-ttu-id="473c2-190">Todas las ediciones de Windows Server 2003 con Service Pack 1 (SP1) admiten instantáneas transportables.</span><span class="sxs-lookup"><span data-stu-id="473c2-190">All editions of Windows Server 2003 with Service Pack 1 (SP1) support transportable shadow copies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="473c2-191"><span id="-tr"></span><span id="-TR"></span><strong>-TR</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-191"><span id="-tr"></span><span id="-TR"></span><strong>-tr</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-192">Esta marca opcional Especifica que la recuperación de TxF debe aplicarse durante la creación de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="473c2-192">This optional flag specifies that TxF recovery should be enforced during shadow copy creation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="473c2-193">Esta marca solo se admite en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-193">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="473c2-194"><span id="-tracing"></span><span id="-TRACING"></span><strong>-seguimiento</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-194"><span id="-tracing"></span><span id="-TRACING"></span><strong>-tracing</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-195">Esta marca opcional genera una salida detallada que se puede usar para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="473c2-195">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="473c2-196"><span id="-wait"></span><span id="-WAIT"></span><strong>-Wait</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-196"><span id="-wait"></span><span id="-WAIT"></span><strong>-wait</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-197">Esta marca opcional hace que la herramienta VShadow espere la confirmación del usuario antes de salir.</span><span class="sxs-lookup"><span data-stu-id="473c2-197">This optional flag causes the VShadow tool to wait for user confirmation before exiting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="473c2-198"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-Wi =</strong><em>redactor</em></span><span class="sxs-lookup"><span data-stu-id="473c2-198"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-wi=</strong><em>Writer</em></span></span><br/></td>
<td><span data-ttu-id="473c2-199">Esta marca opcional comprueba que el escritor o componente especificado se incluye en la instantánea.</span><span class="sxs-lookup"><span data-stu-id="473c2-199">This optional flag verifies that the specified writer or component is included in the shadow copy.</span></span> <span data-ttu-id="473c2-200">El <em>escritor</em> puede especificar una ruta de acceso de componente, un nombre de escritor, un identificador de escritor o un identificador de instancia de escritor.</span><span class="sxs-lookup"><span data-stu-id="473c2-200"><em>Writer</em> can specify a component path, writer name, writer ID, or writer instance ID.</span></span> <span data-ttu-id="473c2-201">Esta marca y la marca <strong>-NW</strong> son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="473c2-201">This flag and the <strong>-nw</strong> flag are mutually exclusive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="473c2-202"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-WX =</strong><em>redactor</em></span><span class="sxs-lookup"><span data-stu-id="473c2-202"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-wx=</strong><em>Writer</em></span></span><br/></td>
<td><span data-ttu-id="473c2-203">Esta marca opcional comprueba que el escritor o componente especificado está excluido de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="473c2-203">This optional flag verifies that the specified writer or component is excluded from the shadow copy.</span></span> <span data-ttu-id="473c2-204">El <em>escritor</em> puede especificar una ruta de acceso de componente, un nombre de escritor, un identificador de escritor o un identificador de instancia de escritor.</span><span class="sxs-lookup"><span data-stu-id="473c2-204"><em>Writer</em> can specify a component path, writer name, writer ID, or writer instance ID.</span></span> <span data-ttu-id="473c2-205">Esta marca y la marca <strong>-NW</strong> son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="473c2-205">This flag and the <strong>-nw</strong> flag are mutually exclusive.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="importing-a-shadow-copy-set"></a><span data-ttu-id="473c2-206">Importar un conjunto de instantáneas</span><span class="sxs-lookup"><span data-stu-id="473c2-206">Importing a Shadow Copy Set</span></span>

<span data-ttu-id="473c2-207">**vshadow** \[ OptionalFlags \] **-i =**_archivo_*_. XML_*</span><span class="sxs-lookup"><span data-stu-id="473c2-207">**vshadow** \[OptionalFlags\] **-i=**_File_*_.xml_*</span></span>

<span data-ttu-id="473c2-208">La opción de línea de comandos **-i** importa un conjunto de instantáneas transportables.</span><span class="sxs-lookup"><span data-stu-id="473c2-208">The **-i** command-line option imports a transportable shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="473c2-209">Esta opción de línea de comandos solo se admite en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-209">This command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="473c2-210">El archivo de *File.xml* debe ser un archivo de documento de componentes de copia de seguridad para un conjunto de instantáneas transportables creado con la marca opcional **-t** o **-BC** .</span><span class="sxs-lookup"><span data-stu-id="473c2-210">The *File.xml* file must be a Backup Components Document file for a transportable shadow copy set that was created with the **-t** or **-bc** optional flag.</span></span>

<span data-ttu-id="473c2-211">Un conjunto de instantáneas es una [*instantánea persistente*](vssgloss-p.md) si se creó con la marca opcional **-p** .</span><span class="sxs-lookup"><span data-stu-id="473c2-211">A shadow copy set is a [*persistent shadow copy*](vssgloss-p.md) if it was created with the **-p** optional flag.</span></span> <span data-ttu-id="473c2-212">Si el conjunto de instantáneas transportables es no persistente, aparece durante un breve período de tiempo mientras se ejecuta el comando de creación de instantáneas y se elimina automáticamente cuando el comando vuelve.</span><span class="sxs-lookup"><span data-stu-id="473c2-212">If the transportable shadow copy set is nonpersistent, it appears for a short time while the shadow copy creation command is running, and is automatically deleted when the command returns.</span></span> <span data-ttu-id="473c2-213">Puede importar instantáneas no persistentes solo durante la creación de instantáneas mediante la creación del conjunto de instantáneas mediante la marca opcional **-exec** para ejecutar un archivo CMD que llama a VShadow **-i**.</span><span class="sxs-lookup"><span data-stu-id="473c2-213">You can import nonpersistent shadow copies only during shadow copy creation, by creating the shadow copy set using the **-exec** optional flag to execute a CMD file that calls VShadow **-i**.</span></span>

<span data-ttu-id="473c2-214">La opción de línea de comandos **-i** no se puede combinar con otras opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="473c2-214">The **-i** command-line option cannot be combined with other command-line options.</span></span>

<span data-ttu-id="473c2-215">*OptionalFlags* es una máscara de máscara de valores de marca opcionales de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="473c2-215">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



| <span data-ttu-id="473c2-216">Valor opcional de marca</span><span class="sxs-lookup"><span data-stu-id="473c2-216">Optional Flag Value</span></span>                                                                                                            | <span data-ttu-id="473c2-217">Descripción</span><span class="sxs-lookup"><span data-stu-id="473c2-217">Description</span></span>                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="473c2-218"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**_comando_</span><span class="sxs-lookup"><span data-stu-id="473c2-218"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Command_</span></span><br/> | <span data-ttu-id="473c2-219">Esta marca opcional ejecuta un comando o script después de la importación de las instantáneas, pero antes de que se cierre la herramienta VShadow.</span><span class="sxs-lookup"><span data-stu-id="473c2-219">This optional flag executes a command or script after the shadow copies are imported but before the VShadow tool exits.</span></span> <span data-ttu-id="473c2-220">El *comando* puede especificar un comando de Shell ejecutable o un archivo CMD.</span><span class="sxs-lookup"><span data-stu-id="473c2-220">*Command* can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="473c2-221">Si especifica un comando de Shell, no se puede especificar ningún parámetro de comando.</span><span class="sxs-lookup"><span data-stu-id="473c2-221">If it specifies a shell command, no command parameters can be specified.</span></span><br/> |
| <span data-ttu-id="473c2-222"><span id="-tracing"></span><span id="-TRACING"></span>**-seguimiento**</span><span class="sxs-lookup"><span data-stu-id="473c2-222"><span id="-tracing"></span><span id="-TRACING"></span>**-tracing**</span></span><br/>                                                  | <span data-ttu-id="473c2-223">Esta marca opcional genera una salida detallada que se puede usar para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="473c2-223">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/>                                                                                                                                                                                 |
| <span data-ttu-id="473c2-224"><span id="-wait"></span><span id="-WAIT"></span>**-Wait**</span><span class="sxs-lookup"><span data-stu-id="473c2-224"><span id="-wait"></span><span id="-WAIT"></span>**-wait**</span></span><br/>                                                           | <span data-ttu-id="473c2-225">Esta marca opcional hace que la herramienta VShadow espere la confirmación del usuario antes de salir.</span><span class="sxs-lookup"><span data-stu-id="473c2-225">This optional flag causes the VShadow tool to wait for user confirmation before exiting.</span></span><br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a><span data-ttu-id="473c2-226">Consultar propiedades de instantáneas</span><span class="sxs-lookup"><span data-stu-id="473c2-226">Querying Shadow Copy Properties</span></span>

<span data-ttu-id="473c2-227">**vshadow** **-q**</span><span class="sxs-lookup"><span data-stu-id="473c2-227">**vshadow** **-q**</span></span>

<span data-ttu-id="473c2-228">**vshadow** **-QX =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="473c2-228">**vshadow** **-qx=**_ShadowCopySetId_</span></span>

<span data-ttu-id="473c2-229">**vshadow** **-s =**_ShadowCopyId_</span><span class="sxs-lookup"><span data-stu-id="473c2-229">**vshadow** **-s=**_ShadowCopyId_</span></span>

<span data-ttu-id="473c2-230">La opción de línea de comandos **-q** muestra las propiedades de todas las instantáneas del equipo.</span><span class="sxs-lookup"><span data-stu-id="473c2-230">The **-q** command-line option lists the properties of all shadow copies on the computer.</span></span>

<span data-ttu-id="473c2-231">La opción de línea de comandos **-QX** muestra las propiedades de todas las instantáneas del conjunto de instantáneas cuyo identificador se especifica mediante *ShadowCopySetId*.</span><span class="sxs-lookup"><span data-stu-id="473c2-231">The **-qx** command-line option lists the properties of all shadow copies in the shadow copy set whose ID is specified by *ShadowCopySetId*.</span></span>

<span data-ttu-id="473c2-232">La opción de línea de comandos **-s** muestra las propiedades de la instantánea cuyo identificador se especifica mediante *ShadowCopyId*.</span><span class="sxs-lookup"><span data-stu-id="473c2-232">The **-s** command-line option lists the properties of the shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="473c2-233">Estas opciones de línea de comandos usan una combinación de [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) y [**IVssBackupComponents:: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) para obtener las propiedades del conjunto de instantáneas especificado.</span><span class="sxs-lookup"><span data-stu-id="473c2-233">These command-line options use a combination of [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) and [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) to get the properties of the given set of shadow copies.</span></span>

<span data-ttu-id="473c2-234">Las opciones de línea de comandos **-q**, **-QX** y **-s** se excluyen mutuamente y no se pueden combinar con otras opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="473c2-234">The **-q**, **-qx**, and **-s** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="deleting-shadow-copies"></a><span data-ttu-id="473c2-235">Eliminar instantáneas</span><span class="sxs-lookup"><span data-stu-id="473c2-235">Deleting Shadow Copies</span></span>

<span data-ttu-id="473c2-236">**vshadow** **-da**</span><span class="sxs-lookup"><span data-stu-id="473c2-236">**vshadow** **-da**</span></span>

<span data-ttu-id="473c2-237">**vshadow** **-do**</span><span class="sxs-lookup"><span data-stu-id="473c2-237">**vshadow** **-do**</span></span>

<span data-ttu-id="473c2-238">**vshadow** **-DX =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="473c2-238">**vshadow** **-dx=**_ShadowCopySetId_</span></span>

<span data-ttu-id="473c2-239">**vshadow** **-DS =**_ShadowCopyId_</span><span class="sxs-lookup"><span data-stu-id="473c2-239">**vshadow** **-ds=**_ShadowCopyId_</span></span>

<span data-ttu-id="473c2-240">El comando **-da** elimina todas las instantáneas del equipo.</span><span class="sxs-lookup"><span data-stu-id="473c2-240">The **-da** command deletes all shadow copies on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="473c2-241">La opción de línea de comandos **-da** requiere la confirmación del usuario.</span><span class="sxs-lookup"><span data-stu-id="473c2-241">The **-da** command-line option requires user confirmation.</span></span>

 

<span data-ttu-id="473c2-242">La opción **de línea de comandos-do** elimina la instantánea más antigua del equipo.</span><span class="sxs-lookup"><span data-stu-id="473c2-242">The **-do** command-line option deletes the oldest shadow copy on the computer.</span></span>

<span data-ttu-id="473c2-243">La opción de línea de comandos **-DX** elimina todas las instantáneas del conjunto de instantáneas cuyo identificador se especifica mediante *ShadowCopySetId*.</span><span class="sxs-lookup"><span data-stu-id="473c2-243">The **-dx** command-line option deletes all shadow copies in the shadow copy set whose ID is specified by *ShadowCopySetId*.</span></span>

<span data-ttu-id="473c2-244">La opción de línea de comandos **-DS** elimina la instantánea cuyo identificador se especifica mediante *ShadowCopyId*.</span><span class="sxs-lookup"><span data-stu-id="473c2-244">The **-ds** command-line option deletes the shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="473c2-245">Estas opciones de línea de comandos solo se usan con [*instantáneas persistentes*](vssgloss-p.md) .</span><span class="sxs-lookup"><span data-stu-id="473c2-245">These command-line options are for use with [*persistent shadow copies*](vssgloss-p.md) only.</span></span> <span data-ttu-id="473c2-246">No es necesario eliminar de forma explícita las instantáneas no persistentes, ya que se eliminan automáticamente cuando se cierra el comando de creación de VShadow.</span><span class="sxs-lookup"><span data-stu-id="473c2-246">Nonpersistent shadow copies do not need to be explicitly deleted, because they are automatically deleted when the VShadow creation command exits.</span></span>

<span data-ttu-id="473c2-247">Las opciones de línea de comandos **-da**, **-do**, **-DX** y **-DS** se excluyen mutuamente y no se pueden combinar con otras opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="473c2-247">The **-da**, **-do**, **-dx**, and **-ds** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="breaking-a-shadow-copy-set"></a><span data-ttu-id="473c2-248">Dividir un conjunto de instantáneas</span><span class="sxs-lookup"><span data-stu-id="473c2-248">Breaking a Shadow Copy Set</span></span>

<span data-ttu-id="473c2-249">**vshadow** **-b =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="473c2-249">**vshadow** **-b=**_ShadowCopySetId_</span></span>

<span data-ttu-id="473c2-250">**vshadow** **-BW =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="473c2-250">**vshadow** **-bw=**_ShadowCopySetId_</span></span>

<span data-ttu-id="473c2-251">La opción de línea de comandos **-b =**_ShadowCopySetId_ convierte cada instantánea del conjunto de instantáneas en un volumen independiente de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="473c2-251">The **-b=**_ShadowCopySetId_ command-line option converts each shadow copy in the shadow copy set into a stand-alone read-only volume.</span></span>

<span data-ttu-id="473c2-252">La opción de línea de comandos **-BW =**_ShadowCopySetId_ convierte cada instantánea del conjunto de instantáneas en un volumen grabable independiente.</span><span class="sxs-lookup"><span data-stu-id="473c2-252">The **-bw=**_ShadowCopySetId_ command-line option converts each shadow copy in the shadow copy set into a stand-alone writable volume.</span></span>

> [!Note]  
> <span data-ttu-id="473c2-253">Las opciones de línea de comandos **-b** y **-BW** solo se admiten en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-253">The **-b** and **-bw** command-line options are supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="473c2-254">Para obtener información acerca de cómo dividir un conjunto de instantáneas, consulte [romper instantáneas](breaking-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="473c2-254">For information about breaking a shadow copy set, see [Breaking Shadow Copies](breaking-shadow-copies.md).</span></span>

<span data-ttu-id="473c2-255">Una vez interrumpido el conjunto de instantáneas, el conjunto de instantáneas y las instantáneas individuales ya no existen y no se pueden administrar mediante comandos de VSS.</span><span class="sxs-lookup"><span data-stu-id="473c2-255">After the shadow copy set is broken, the shadow copy set and the individual shadow copies no longer exist and cannot be managed using VSS commands.</span></span>

<span data-ttu-id="473c2-256">Un conjunto de instantáneas es persistente si se creó con la marca opcional **-p** .</span><span class="sxs-lookup"><span data-stu-id="473c2-256">A shadow copy set is persistent if it was created with the **-p** optional flag.</span></span> <span data-ttu-id="473c2-257">Si el conjunto de instantáneas transportables es no persistente, aparece durante un breve período de tiempo mientras se ejecuta el comando de creación de instantáneas y se elimina automáticamente cuando el comando vuelve.</span><span class="sxs-lookup"><span data-stu-id="473c2-257">If the transportable shadow copy set is nonpersistent, it appears for a short time while the shadow copy creation command is running, and is automatically deleted when the command returns.</span></span> <span data-ttu-id="473c2-258">Puede romper los conjuntos de instantáneas no persistentes solo durante la creación de instantáneas mediante la creación del conjunto de instantáneas mediante la marca opcional **-exec** para ejecutar un archivo CMD que llama a **vshadow** **-b** o **vshadow** **-BW**.</span><span class="sxs-lookup"><span data-stu-id="473c2-258">You can break nonpersistent shadow copy sets only during shadow copy creation, by creating the shadow copy set using the **-exec** optional flag to execute a CMD file that calls **vshadow** **-b** or **vshadow** **-bw**.</span></span>

<span data-ttu-id="473c2-259">Las opciones de línea de comandos **-b** y **-BW** se excluyen mutuamente y no se pueden combinar con otras opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="473c2-259">The **-b** and **-bw** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a><span data-ttu-id="473c2-260">Dividir un conjunto de instantáneas mediante el método BreakSnapshotSetEx</span><span class="sxs-lookup"><span data-stu-id="473c2-260">Breaking a Shadow Copy Set Using the BreakSnapshotSetEx Method</span></span>

<span data-ttu-id="473c2-261">**vshadow** **-BEX**</span><span class="sxs-lookup"><span data-stu-id="473c2-261">**vshadow** **-bex**</span></span>

<span data-ttu-id="473c2-262">La opción de línea de comandos **-BEX** divide un conjunto de instantáneas según las opciones especificadas por las marcas opcionales **-Mask**, **-RW**, **-forcerevert** y **-norevert** .</span><span class="sxs-lookup"><span data-stu-id="473c2-262">The **-bex** command-line option breaks a shadow copy set according to the options specified by the optional **-mask**, **-rw**, **-forcerevert**, and **-norevert** flags.</span></span> <span data-ttu-id="473c2-263">Esta opción de línea de comandos es similar a las opciones de línea de comandos **-b** y **-BW** .</span><span class="sxs-lookup"><span data-stu-id="473c2-263">This command-line option is similar to the **-b** and **-bw** command-line options.</span></span> <span data-ttu-id="473c2-264">La opción de línea de comandos **-BEX** usa el método [**IVssBackupComponentsEx2:: BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) , mientras que las opciones de línea de comandos **-b** y **-BW** usan el método [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .</span><span class="sxs-lookup"><span data-stu-id="473c2-264">The **-bex** command-line option uses the [**IVssBackupComponentsEx2::BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) method, whereas the **-b** and **-bw** command-line options use the [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) method.</span></span>

<span data-ttu-id="473c2-265">Para obtener información acerca de cómo dividir un conjunto de instantáneas, consulte [romper instantáneas](breaking-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="473c2-265">For information about breaking a shadow copy set, see [Breaking Shadow Copies](breaking-shadow-copies.md).</span></span>

> [!Note]  
> <span data-ttu-id="473c2-266">La opción de línea de comandos **-BEX** solo se admite en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-266">The **-bex** command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="473c2-267">**vshadow** **-BEX** **-Mask**</span><span class="sxs-lookup"><span data-stu-id="473c2-267">**vshadow** **-bex** **-mask**</span></span>

<span data-ttu-id="473c2-268">La marca **-Mask** especifica que el LUN de instantáneas se enmascarará desde el host.</span><span class="sxs-lookup"><span data-stu-id="473c2-268">The **-mask** flag specifies that the shadow copy LUN will be masked from the host.</span></span> <span data-ttu-id="473c2-269">Si se especifica la marca **-Mask** , no se pueden especificar las marcas **-RW**, **-forcerevert** y **-norevert** .</span><span class="sxs-lookup"><span data-stu-id="473c2-269">If the **-mask** flag is specified, the **-rw**, **-forcerevert**, and **-norevert** flags cannot be specified.</span></span>

<span data-ttu-id="473c2-270">**vshadow** **-BEX** **-RW**</span><span class="sxs-lookup"><span data-stu-id="473c2-270">**vshadow** **-bex** **-rw**</span></span>

<span data-ttu-id="473c2-271">La marca **-RW** especifica que el LUN de instantáneas se expondrá al host como un volumen de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="473c2-271">The **-rw** flag specifies that the shadow copy LUN will be exposed to the host as a read/write volume.</span></span>

<span data-ttu-id="473c2-272">**vshadow** **-BEX** **-forcerevert**</span><span class="sxs-lookup"><span data-stu-id="473c2-272">**vshadow** **-bex** **-forcerevert**</span></span>

<span data-ttu-id="473c2-273">La marca **-forcerevert** especifica que los identificadores de disco de todos los LUN de instantánea se revertirán a los de los LUN originales.</span><span class="sxs-lookup"><span data-stu-id="473c2-273">The **-forcerevert** flag specifies that the disk identifiers of all of the shadow copy LUNs will be reverted to that of the original LUNs.</span></span> <span data-ttu-id="473c2-274">Sin embargo, si alguno de los LUN originales está presente en el sistema, se producirá un error en la operación y no se revertirá ninguno de los identificadores.</span><span class="sxs-lookup"><span data-stu-id="473c2-274">However, if any of the original LUNs are present on the system, the operation will fail and none of the identifiers will be reverted.</span></span> <span data-ttu-id="473c2-275">Esta marca y la marca **-norevert** son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="473c2-275">This flag and the **-norevert** flag are mutually exclusive.</span></span>

<span data-ttu-id="473c2-276">**vshadow** **-BEX** **-norevert**</span><span class="sxs-lookup"><span data-stu-id="473c2-276">**vshadow** **-bex** **-norevert**</span></span>

<span data-ttu-id="473c2-277">La marca **-norevert** especifica que no se revertirá ninguno de los identificadores de disco LUN de instantánea.</span><span class="sxs-lookup"><span data-stu-id="473c2-277">The **-norevert** flag specifies that none of the shadow copy LUN disk identifiers will be reverted.</span></span> <span data-ttu-id="473c2-278">Esta marca y la marca **-forcerevert** son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="473c2-278">This flag and the **-forcerevert** flag are mutually exclusive.</span></span>

## <a name="exposing-a-shadow-copy-locally"></a><span data-ttu-id="473c2-279">Exponer una instantánea localmente</span><span class="sxs-lookup"><span data-stu-id="473c2-279">Exposing a Shadow Copy Locally</span></span>

<span data-ttu-id="473c2-280">**vshadow** **-el =**_ShadowCopyId_*_,_*_LocalEmptyDirectory_</span><span class="sxs-lookup"><span data-stu-id="473c2-280">**vshadow** **-el=**_ShadowCopyId_*_,_*_LocalEmptyDirectory_</span></span>

 <span data-ttu-id="473c2-281">**vshadow** **-el =**_ShadowCopyId_*_,_*_UnusedDriveLetter_</span><span class="sxs-lookup"><span data-stu-id="473c2-281">**vshadow** **-el=**_ShadowCopyId_*_,_*_UnusedDriveLetter_</span></span>

<span data-ttu-id="473c2-282">La opción de línea de comandos **-** el asigna una carpeta montada o una letra de unidad a una instantánea persistente.</span><span class="sxs-lookup"><span data-stu-id="473c2-282">The **-el** command-line option assigns a mounted folder or a drive letter to a persistent shadow copy.</span></span> <span data-ttu-id="473c2-283">Tenga en cuenta que el contenido del volumen seguirá siendo de solo lectura, a menos que llame a **vshadow** **-BW** posteriormente para interrumpir el conjunto de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="473c2-283">Note that the volume contents will remain read-only unless you subsequently call **vshadow** **-bw** to break the shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="473c2-284">Las instantáneas no persistentes y las [*instantáneas accesibles para el cliente*](vssgloss-c.md) no se pueden exponer localmente.</span><span class="sxs-lookup"><span data-stu-id="473c2-284">Nonpersistent shadow copies and [*client-accessible shadow copies*](vssgloss-c.md) cannot be exposed locally.</span></span>

 

<span data-ttu-id="473c2-285">Por ejemplo, si {edbed95e-7e8d-11d8-9d01-505054503030} es el GUID de una instantánea persistente existente y X: es una letra de unidad no utilizada, el siguiente comando expone la instantánea en X:</span><span class="sxs-lookup"><span data-stu-id="473c2-285">For example, if {edbed95e-7e8d-11d8-9d01-505054503030} is the GUID of an existing persistent shadow copy, and X: is an unused drive letter, the following command exposes the shadow copy under X:</span></span>

<span data-ttu-id="473c2-286">**vshadow** **-el = {edbed95e-7e8d-11d8-9d01-505054503030}, x:**</span><span class="sxs-lookup"><span data-stu-id="473c2-286">**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},x:**</span></span>

<span data-ttu-id="473c2-287">En el ejemplo siguiente se muestra cómo exponer la misma instantánea en la carpeta montada C: \\ ShadowCopies \\ June23:</span><span class="sxs-lookup"><span data-stu-id="473c2-287">The following example shows how to expose the same shadow copy under the mounted folder C:\\ShadowCopies\\June23:</span></span>

<span data-ttu-id="473c2-288">**mkdir c: \\ ShadowCopies \\ June23**</span><span class="sxs-lookup"><span data-stu-id="473c2-288">**mkdir c:\\ShadowCopies\\June23**</span></span>

<span data-ttu-id="473c2-289">**vshadow** **-el = {edbed95e-7e8d-11d8-9d01-505054503030}, c: \\ ShadowCopies \\ June23**</span><span class="sxs-lookup"><span data-stu-id="473c2-289">**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},c:\\ShadowCopies\\June23**</span></span>

<span data-ttu-id="473c2-290">La opción de línea de comandos **-** el no puede combinarse con otras opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="473c2-290">The **-el** command-line option cannot be combined with other command-line options.</span></span>

## <a name="exposing-a-shadow-copy-remotely"></a><span data-ttu-id="473c2-291">Exponer una instantánea de forma remota</span><span class="sxs-lookup"><span data-stu-id="473c2-291">Exposing a Shadow Copy Remotely</span></span>

<span data-ttu-id="473c2-292">**vshadow** **-er =**_ShadowCopyId_*_,_*_UnusedShareName_</span><span class="sxs-lookup"><span data-stu-id="473c2-292">**vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_</span></span>

 <span data-ttu-id="473c2-293">**vshadow** **-er =**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_</span><span class="sxs-lookup"><span data-stu-id="473c2-293">**vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_</span></span>

<span data-ttu-id="473c2-294">La opción de línea de comandos **-er** asigna un nombre de recurso compartido de solo lectura al directorio raíz (o un subdirectorio) de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="473c2-294">The **-er** command-line option assigns a read-only share name to the root directory (or a subdirectory) from the shadow copy.</span></span> <span data-ttu-id="473c2-295">Tenga en cuenta que el contenido del recurso compartido seguirá siendo de solo lectura, a menos que llame posteriormente a **vshadow** **-BW** para interrumpir el conjunto de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="473c2-295">Note that the share contents will remain read-only unless you subsequently call **vshadow** **-bw** to break the shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="473c2-296">Las [*instantáneas accesibles para el cliente*](vssgloss-c.md) no se pueden exponer de forma remota.</span><span class="sxs-lookup"><span data-stu-id="473c2-296">[*Client-accessible shadow copies*](vssgloss-c.md) cannot be exposed remotely.</span></span>

 

<span data-ttu-id="473c2-297">Por ejemplo, si {edbed95e-7e8d-11d8-9d01-505054503030} es el GUID de una instantánea persistente existente y el recurso compartido \_ 123 es un nombre de recurso compartido sin usar, el siguiente comando expone la instantánea en share \_ 123:</span><span class="sxs-lookup"><span data-stu-id="473c2-297">For example, if {edbed95e-7e8d-11d8-9d01-505054503030} is the GUID of an existing persistent shadow copy, and share\_123 is an unused share name, the following command exposes the shadow copy under share\_123:</span></span>

<span data-ttu-id="473c2-298">**vshadow** **-er = {edbed95e-7e8d-11d8-9d01-505054503030}, recurso compartido \_ 123**</span><span class="sxs-lookup"><span data-stu-id="473c2-298">**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share\_123**</span></span>

<span data-ttu-id="473c2-299">En el ejemplo siguiente se muestra cómo exponer solo un subárbol (denominado "Folder1 \\ Carpeta2") de la misma instantánea en el mismo recurso compartido:</span><span class="sxs-lookup"><span data-stu-id="473c2-299">The following example shows how to expose only a subtree (named "Folder1\\Folder2") of the same shadow copy under the same share:</span></span>

<span data-ttu-id="473c2-300">**vshadow** **-er = {edbed95e-7e8d-11d8-9d01-505054503030}, recurso compartido \_ 123, carpeta1 \\ Carpeta2**</span><span class="sxs-lookup"><span data-stu-id="473c2-300">**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share\_123,Folder1\\Folder2**</span></span>

<span data-ttu-id="473c2-301">La opción de línea de comandos **-er** no se puede combinar con otras opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="473c2-301">The **-er** command-line option cannot be combined with other command-line options.</span></span>

## <a name="listing-writer-status-and-metadata"></a><span data-ttu-id="473c2-302">Enumerar el estado y los metadatos del escritor</span><span class="sxs-lookup"><span data-stu-id="473c2-302">Listing Writer Status and Metadata</span></span>

<span data-ttu-id="473c2-303">**vshadow** **-WS**</span><span class="sxs-lookup"><span data-stu-id="473c2-303">**vshadow** **-ws**</span></span>

<span data-ttu-id="473c2-304">**vshadow** **-WM**</span><span class="sxs-lookup"><span data-stu-id="473c2-304">**vshadow** **-wm**</span></span>

<span data-ttu-id="473c2-305">**vshadow** **-wm2**</span><span class="sxs-lookup"><span data-stu-id="473c2-305">**vshadow** **-wm2**</span></span>

<span data-ttu-id="473c2-306">**vshadow** **-wm3**</span><span class="sxs-lookup"><span data-stu-id="473c2-306">**vshadow** **-wm3**</span></span>

<span data-ttu-id="473c2-307">La opción de línea de comandos **-WS** enumera los escritores de VSS que se están ejecutando actualmente en el equipo y describe su estado.</span><span class="sxs-lookup"><span data-stu-id="473c2-307">The **-ws** command-line option enumerates the VSS writers that are currently running on the computer and describes their state.</span></span> <span data-ttu-id="473c2-308">Este comando es el equivalente del comando [vssadmin List Writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="473c2-308">This command is the equivalent of the [Vssadmin list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) command.</span></span> <span data-ttu-id="473c2-309">Hay seis valores de estado posibles: estable, con errores, desconocido, en espera de inmovilización, congelada y en espera de finalización.</span><span class="sxs-lookup"><span data-stu-id="473c2-309">There are six possible state values: Stable, Failed, Unknown, Waiting for freeze, Frozen, and Waiting for completion.</span></span>

<span data-ttu-id="473c2-310">La opción de línea de comandos **-WM** muestra un resumen de los metadatos del escritor, incluidos los volúmenes afectados.</span><span class="sxs-lookup"><span data-stu-id="473c2-310">The **-wm** command-line option lists a summary of the writer metadata, including the affected volumes.</span></span>

<span data-ttu-id="473c2-311">La opción de línea de comandos **-wm2** enumera todos los metadatos del escritor.</span><span class="sxs-lookup"><span data-stu-id="473c2-311">The **-wm2** command-line option lists all writer metadata.</span></span>

<span data-ttu-id="473c2-312">La opción de línea de comandos **-wm3** enumera todos los metadatos del escritor en formato XML sin formato.</span><span class="sxs-lookup"><span data-stu-id="473c2-312">The **-wm3** command-line option lists all writer metadata in raw XML format.</span></span>

<span data-ttu-id="473c2-313">**Windows Vista y Windows Server 2003:** No se admite la opción de línea de comandos **-wm3** .</span><span class="sxs-lookup"><span data-stu-id="473c2-313">**Windows Vista and Windows Server 2003:** The **-wm3** command-line option is not supported.</span></span>

<span data-ttu-id="473c2-314">Puede usar esta información para determinar qué volúmenes se van a incluir en el conjunto de instantáneas de volumen.</span><span class="sxs-lookup"><span data-stu-id="473c2-314">You can use this information to determine which volumes to include in the volume shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="473c2-315">Si el estado del escritor es estable o está esperando a la finalización, se puede considerar que el escritor está en un estado estable, listo para la siguiente copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="473c2-315">If the writer state is Stable or Waiting for completion, the writer can be considered to be in a stable state, ready for the next backup.</span></span>

 

<span data-ttu-id="473c2-316">Las opciones **de línea de comandos-WS**, **-WM**, **-wm2** y **-wm3** se excluyen mutuamente y no se pueden combinar con otras opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="473c2-316">The **-ws**, **-wm**, **-wm2**, and **-wm3** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="performing-restore-operations"></a><span data-ttu-id="473c2-317">Realización de operaciones de restauración</span><span class="sxs-lookup"><span data-stu-id="473c2-317">Performing Restore Operations</span></span>

<span data-ttu-id="473c2-318">**vshadow** \[ OptionalFlags \] **-r =**_archivo_*_. XML_*</span><span class="sxs-lookup"><span data-stu-id="473c2-318">**vshadow** \[OptionalFlags\] **-r=**_File_*_.xml_*</span></span>

<span data-ttu-id="473c2-319">**vshadow** \[ OptionalFlags \] **-RS =**_archivo_*_. XML_*</span><span class="sxs-lookup"><span data-stu-id="473c2-319">**vshadow** \[OptionalFlags\] **-rs=**_File_*_.xml_*</span></span>

<span data-ttu-id="473c2-320">La opción de línea de comandos **-r** realiza una operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="473c2-320">The **-r** command-line option performs a restore operation.</span></span>

<span data-ttu-id="473c2-321">La opción de línea de comandos **-RS** realiza una operación de restauración simulada.</span><span class="sxs-lookup"><span data-stu-id="473c2-321">The **-rs** command-line option performs a simulated restore operation.</span></span>

<span data-ttu-id="473c2-322">El archivo de *File.xml* debe ser un archivo de documento de componentes de copia de seguridad para un conjunto de instantáneas creado con la marca opcional **-t** o **-BC** .</span><span class="sxs-lookup"><span data-stu-id="473c2-322">The *File.xml* file must be a Backup Components Document file for a shadow copy set that was created with the **-t** or **-bc** optional flag.</span></span>

<span data-ttu-id="473c2-323">Las opciones de línea de comandos **-r** y **-RS** se excluyen mutuamente y no se pueden combinar con otras opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="473c2-323">The **-r** and **-rs** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

<span data-ttu-id="473c2-324">*OptionalFlags* es una máscara de máscara de valores de marca opcionales de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="473c2-324">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



| <span data-ttu-id="473c2-325">Valor opcional de marca</span><span class="sxs-lookup"><span data-stu-id="473c2-325">Optional Flag Value</span></span>                                                                                                            | <span data-ttu-id="473c2-326">Descripción</span><span class="sxs-lookup"><span data-stu-id="473c2-326">Description</span></span>                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="473c2-327"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-Wi =**_redactor_</span><span class="sxs-lookup"><span data-stu-id="473c2-327"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-wi=**_Writer_</span></span><br/>             | <span data-ttu-id="473c2-328">Esta marca opcional comprueba que el escritor o componente especificado está incluido en la restauración.</span><span class="sxs-lookup"><span data-stu-id="473c2-328">This optional flag verifies that the specified writer or component is included in the restore.</span></span> <span data-ttu-id="473c2-329">El *escritor* puede especificar una ruta de acceso de componente, un nombre de escritor, un identificador de escritor o un identificador de instancia de escritor.</span><span class="sxs-lookup"><span data-stu-id="473c2-329">*Writer* can specify a component path, writer name, writer ID, or writer instance ID.</span></span><br/>                                                                                    |
| <span data-ttu-id="473c2-330"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-WX =**_redactor_</span><span class="sxs-lookup"><span data-stu-id="473c2-330"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-wx=**_Writer_</span></span><br/>             | <span data-ttu-id="473c2-331">Esta marca opcional comprueba que el escritor o componente especificado se excluya de la restauración.</span><span class="sxs-lookup"><span data-stu-id="473c2-331">This optional flag verifies that the specified writer or component is excluded from the restore.</span></span> <span data-ttu-id="473c2-332">El *escritor* puede especificar una ruta de acceso de componente, un nombre de escritor, un identificador de escritor o un identificador de instancia de escritor.</span><span class="sxs-lookup"><span data-stu-id="473c2-332">*Writer* can specify a component path, writer name, writer ID, or writer instance ID.</span></span><br/>                                                                                  |
| <span data-ttu-id="473c2-333"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**_comando_</span><span class="sxs-lookup"><span data-stu-id="473c2-333"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Command_</span></span><br/> | <span data-ttu-id="473c2-334">Esta marca opcional ejecuta un comando o un script entre los eventos previos y posteriores a la restauración que se envían a los escritores.</span><span class="sxs-lookup"><span data-stu-id="473c2-334">This optional flag executes a command or script between the pre-restore and post-restore events that are sent to the writers.</span></span> <span data-ttu-id="473c2-335">El *comando* puede especificar un comando de Shell ejecutable o un archivo CMD.</span><span class="sxs-lookup"><span data-stu-id="473c2-335">*Command* can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="473c2-336">Si especifica un comando de Shell, no se puede especificar ningún parámetro de comando.</span><span class="sxs-lookup"><span data-stu-id="473c2-336">If it specifies a shell command, no command parameters can be specified.</span></span><br/> |
| <span data-ttu-id="473c2-337"><span id="-tracing"></span><span id="-TRACING"></span>**-seguimiento**</span><span class="sxs-lookup"><span data-stu-id="473c2-337"><span id="-tracing"></span><span id="-TRACING"></span>**-tracing**</span></span><br/>                                                  | <span data-ttu-id="473c2-338">Esta marca opcional genera una salida detallada que se puede usar para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="473c2-338">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/>                                                                                                                                                                                       |



 

## <a name="reverting-to-a-previous-shadow-copy"></a><span data-ttu-id="473c2-339">Revertir a una instantánea anterior</span><span class="sxs-lookup"><span data-stu-id="473c2-339">Reverting to a Previous Shadow Copy</span></span>

<span data-ttu-id="473c2-340">**vshadow** **-Revert =**_ShadowCopyId_</span><span class="sxs-lookup"><span data-stu-id="473c2-340">**vshadow** **-revert=**_ShadowCopyId_</span></span>

> [!Note]  
> <span data-ttu-id="473c2-341">Esta opción de línea de comandos solo se admite en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-341">This command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="473c2-342">**Windows server 2008 y Windows server 2003:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="473c2-342">**Windows Server 2008 and Windows Server 2003:** Not supported.</span></span>

<span data-ttu-id="473c2-343">La opción de línea de comandos **-Revert** revierte un volumen a la instantánea anterior cuyo identificador se especifica mediante *ShadowCopyId*.</span><span class="sxs-lookup"><span data-stu-id="473c2-343">The **-revert** command-line option reverts a volume to the previous shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="473c2-344">La opción de línea de comandos **-Revert** no se puede combinar con otras opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="473c2-344">The **-revert** command-line option cannot be combined with other command-line options.</span></span>

## <a name="resynchronizing-luns"></a><span data-ttu-id="473c2-345">Volver a sincronizar LUN</span><span class="sxs-lookup"><span data-stu-id="473c2-345">Resynchronizing LUNs</span></span>

<span data-ttu-id="473c2-346">**vshadow** **-addresync =**_ShadowCopyId_ **-Resync =**_BCDFileName_ \[ OptionalResyncFlags\]</span><span class="sxs-lookup"><span data-stu-id="473c2-346">**vshadow** **-addresync=**_ShadowCopyId_ **-resync=**_BCDFileName_ \[OptionalResyncFlags\]</span></span>

<span data-ttu-id="473c2-347">**vshadow** **-addresync =**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-Resync =**_BCDFileName_ \[ OptionalResyncFlags\]</span><span class="sxs-lookup"><span data-stu-id="473c2-347">**vshadow** **-addresync=**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-resync=**_BCDFileName_ \[OptionalResyncFlags\]</span></span>

<span data-ttu-id="473c2-348">La opción de línea de comandos **-addresync** especifica los volúmenes que se van a incluir en una operación de resincronización de LUN.</span><span class="sxs-lookup"><span data-stu-id="473c2-348">The **-addresync** command-line option specifies the volumes to be included in a LUN resynchronization operation.</span></span> <span data-ttu-id="473c2-349">El parámetro *ShadowCopyId* especifica el identificador de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="473c2-349">The *ShadowCopyId* parameter specifies the identifier of the shadow copy.</span></span> <span data-ttu-id="473c2-350">El parámetro opcional *TargetVolumeDriveLetter* especifica el volumen de destino en el que se copiará el contenido del volumen de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="473c2-350">The optional *TargetVolumeDriveLetter* parameter specifies the destination volume where the contents of the shadow copy volume are to be copied.</span></span>

<span data-ttu-id="473c2-351">La opción de línea de comandos **-Resync** inicia una operación de resincronización de LUN.</span><span class="sxs-lookup"><span data-stu-id="473c2-351">The **-resync** command-line option initiates a LUN resynchronization operation.</span></span> <span data-ttu-id="473c2-352">Una vez completada la operación, la firma de cada LUN de destino debe ser idéntica a la del LUN de volumen de destino.</span><span class="sxs-lookup"><span data-stu-id="473c2-352">After the operation is complete, the signature of each target LUN should be identical to that of the target volume LUN.</span></span> <span data-ttu-id="473c2-353">El parámetro *BCDFileName* especifica el nombre del archivo XML que contiene el documento del componente de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="473c2-353">The *BCDFileName* parameter specifies the name of the XML file that contains the Backup Component Document.</span></span>

> [!Note]  
> <span data-ttu-id="473c2-354">Las opciones de línea de comandos **-addresync** y **-Resync** solo se admiten en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-354">The **-addresync** and **-resync** command-line options are supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="473c2-355">**Windows server 2008 y Windows server 2003:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="473c2-355">**Windows Server 2008 and Windows Server 2003:** Not supported.</span></span>

<span data-ttu-id="473c2-356">*OptionalResyncFlags* es una máscara de máscara de valores de marca opcionales de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="473c2-356">*OptionalResyncFlags* is a bitmask of optional flag values from the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="473c2-357">Valor opcional de marca</span><span class="sxs-lookup"><span data-stu-id="473c2-357">Optional flag value</span></span></th>
<th><span data-ttu-id="473c2-358">Descripción</span><span class="sxs-lookup"><span data-stu-id="473c2-358">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="473c2-359"><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-359"><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-360">Esta marca opcional Especifica que, una vez completada la operación, la firma de cada LUN de destino debe ser idéntica a la del LUN original que se usó para crear la instantánea, no el LUN de volumen de destino.</span><span class="sxs-lookup"><span data-stu-id="473c2-360">This optional flag specifies that after the operation is complete, the signature of each target LUN should be identical to that of the original LUN that was used to create the shadow copy, not the target volume LUN.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="473c2-361">La marca <strong>-revertsig</strong> solo se admite en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-361">The <strong>-revertsig</strong> flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="473c2-362"><strong>Windows server 2008 y Windows server 2003:</strong> No compatible.</span><span class="sxs-lookup"><span data-stu-id="473c2-362"><strong>Windows Server 2008 and Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="473c2-363"><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong></span><span class="sxs-lookup"><span data-stu-id="473c2-363"><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong></span></span><br/></td>
<td><span data-ttu-id="473c2-364">Esta marca opcional Especifica que el servicio VSS no debe comprobar si hay volúmenes no seleccionados que se sobrescribirán con la operación de resincronización de LUN.</span><span class="sxs-lookup"><span data-stu-id="473c2-364">This optional flag specifies that the VSS service should not check for unselected volumes that would be overwritten by the LUN resynchronization operation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="473c2-365">La marca <strong>-novolcheck</strong> solo se admite en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="473c2-365">The <strong>-novolcheck</strong> flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="473c2-366"><strong>Windows server 2008 y Windows server 2003:</strong> No compatible.</span><span class="sxs-lookup"><span data-stu-id="473c2-366"><strong>Windows Server 2008 and Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 
