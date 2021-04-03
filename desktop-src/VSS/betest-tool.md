---
description: COMTEST es un solicitante de VSS que prueba las operaciones avanzadas de copia de seguridad y restauración.
ms.assetid: a6cc7308-a9fa-4a84-9e7c-4d0adda28db5
title: Herramienta de prueba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7559c304532b337214108435b740595897694f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913386"
---
# <a name="betest-tool"></a><span data-ttu-id="66ef0-103">Herramienta de prueba</span><span class="sxs-lookup"><span data-stu-id="66ef0-103">BETest Tool</span></span>

<span data-ttu-id="66ef0-104">COMTEST es un solicitante de VSS que prueba las operaciones avanzadas de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="66ef0-104">BETest is a VSS requester that tests advanced backup and restore operations.</span></span> <span data-ttu-id="66ef0-105">Esta herramienta se puede usar para probar el uso de una aplicación de características de VSS complejas, como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="66ef0-105">This tool can be used to test an application's use of complex VSS features such as the following:</span></span>

-   <span data-ttu-id="66ef0-106">Copia de seguridad incremental y diferencial</span><span class="sxs-lookup"><span data-stu-id="66ef0-106">Incremental and differential backup</span></span>
-   <span data-ttu-id="66ef0-107">Opciones de restauración complejas, como la restauración autoritativa</span><span class="sxs-lookup"><span data-stu-id="66ef0-107">Complex restore options, such as authoritative restore</span></span>
-   <span data-ttu-id="66ef0-108">Opciones de puesta al día</span><span class="sxs-lookup"><span data-stu-id="66ef0-108">Rollforward options</span></span>

> [!Note]  
> <span data-ttu-id="66ef0-109">COMTEST se incluye en el kit de desarrollo de software (SDK) de Microsoft Windows para Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="66ef0-109">BETest is included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="66ef0-110">El SDK de VSS 7,2 incluye una versión de COMTEST que solo se ejecuta en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="66ef0-110">The VSS 7.2 SDK includes a version of BETest that runs only on Windows Server 2003.</span></span> <span data-ttu-id="66ef0-111">En este tema se describe la versión Windows SDK de COMTEST, no la versión 2003 de Windows Server incluida en el SDK de VSS 7,2.</span><span class="sxs-lookup"><span data-stu-id="66ef0-111">This topic describes the Windows SDK version of BETest, not the Windows Server 2003 version included in the VSS 7.2 SDK.</span></span> <span data-ttu-id="66ef0-112">Para obtener información acerca de cómo descargar el Windows SDK y el SDK de VSS 7,2, consulte [servicio de instantáneas de volumen](volume-shadow-copy-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="66ef0-112">For information about downloading the Windows SDK and the VSS 7.2 SDK, see [Volume Shadow Copy Service](volume-shadow-copy-service-portal.md).</span></span>

 

<span data-ttu-id="66ef0-113">En la instalación de Windows SDK, la herramienta COMTEST se puede encontrar en `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (para Windows de 64 bits) y `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (para windows de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="66ef0-113">In the Windows SDK installation, the BETest tool can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

## <a name="running-the-betest-tool"></a><span data-ttu-id="66ef0-114">Ejecutar la herramienta COMTEST</span><span class="sxs-lookup"><span data-stu-id="66ef0-114">Running the BETest Tool</span></span>

<span data-ttu-id="66ef0-115">Para ejecutar la herramienta COMTEST desde la línea de comandos, use la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="66ef0-115">To run the BETest tool from the command line, use the following syntax:</span></span>

<span data-ttu-id="66ef0-116"> *Opciones de línea de comandos de* test</span><span class="sxs-lookup"><span data-stu-id="66ef0-116">**BETest** *command-line-options*</span></span>

<span data-ttu-id="66ef0-117">En el ejemplo de uso siguiente se muestra cómo usar la herramienta COMTEST junto con la [herramienta VSS Writer](vss-test-writer-tool.md), que es una VSS Writer.</span><span class="sxs-lookup"><span data-stu-id="66ef0-117">The following usage example shows how to use the BETest tool together with the [VSS Test Writer tool](vss-test-writer-tool.md), which is a VSS writer.</span></span>

<span data-ttu-id="66ef0-118">**Ejemplo de uso de la herramienta de prueba**</span><span class="sxs-lookup"><span data-stu-id="66ef0-118">**BETest Tool Usage Example**</span></span>

1.  <span data-ttu-id="66ef0-119">Cree un directorio de prueba denominado C: \\ COMTEST.</span><span class="sxs-lookup"><span data-stu-id="66ef0-119">Create a test directory named C:\\BETest.</span></span> <span data-ttu-id="66ef0-120">Copie los siguientes archivos en este directorio:</span><span class="sxs-lookup"><span data-stu-id="66ef0-120">Copy the following files into this directory:</span></span>
    -   <span data-ttu-id="66ef0-121">betest.exe</span><span class="sxs-lookup"><span data-stu-id="66ef0-121">betest.exe</span></span>
    -   <span data-ttu-id="66ef0-122">vswriter.exe</span><span class="sxs-lookup"><span data-stu-id="66ef0-122">vswriter.exe</span></span>
    -   [<span data-ttu-id="66ef0-123">BetestSample.xml</span><span class="sxs-lookup"><span data-stu-id="66ef0-123">BetestSample.xml</span></span>](#sample-xml-configuration-file-betestsamplexml)
    -   [<span data-ttu-id="66ef0-124">VswriterSample.xml</span><span class="sxs-lookup"><span data-stu-id="66ef0-124">VswriterSample.xml</span></span>](#sample-xml-configuration-file-vswritersamplexml)
2.  <span data-ttu-id="66ef0-125">Cree un directorio denominado C: \\ TestPath.</span><span class="sxs-lookup"><span data-stu-id="66ef0-125">Create a directory named C:\\TestPath.</span></span> <span data-ttu-id="66ef0-126">Coloque algunos archivos de datos de prueba en este directorio.</span><span class="sxs-lookup"><span data-stu-id="66ef0-126">Put some test data files in this directory.</span></span>
3.  <span data-ttu-id="66ef0-127">Cree un directorio denominado C: \\ BackupDestination.</span><span class="sxs-lookup"><span data-stu-id="66ef0-127">Create a directory named C:\\BackupDestination.</span></span> <span data-ttu-id="66ef0-128">Deje este directorio vacío.</span><span class="sxs-lookup"><span data-stu-id="66ef0-128">Leave this directory empty.</span></span>
4.  <span data-ttu-id="66ef0-129">Abra dos ventanas de comandos con privilegios elevados y establezca el directorio de trabajo de cada en C: \\ compruébelo.</span><span class="sxs-lookup"><span data-stu-id="66ef0-129">Open two elevated command windows and set the working directory in each to C:\\BETest.</span></span>
5.  <span data-ttu-id="66ef0-130">En la primera ventana de comandos, inicie la [herramienta VSS test Writer](vss-test-writer-tool.md) de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="66ef0-130">In the first command window, start the [VSS Test Writer tool](vss-test-writer-tool.md) as follows:</span></span>

    <span data-ttu-id="66ef0-131">**vswriter.exe VswriterSample.xml**</span><span class="sxs-lookup"><span data-stu-id="66ef0-131">**vswriter.exe VswriterSample.xml**</span></span>

    <span data-ttu-id="66ef0-132">En el archivo vswriterSample.xml se configura la herramienta VSS Writer (vswriter) para notificar el contenido del directorio c: \\ TestPath como preparación para una operación de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="66ef0-132">The vswriterSample.xml file configures the VSS Test Writer tool (vswriter) to report the contents of the c:\\TestPath directory in preparation for a backup operation.</span></span> <span data-ttu-id="66ef0-133">Tenga en cuenta que la herramienta de escritura de prueba de VSS no producirá ningún resultado hasta que detecte actividad de un solicitante como COMTEST.</span><span class="sxs-lookup"><span data-stu-id="66ef0-133">Note that the VSS Test Writer tool will not produce output until it detects activity from a requester such as BETest.</span></span> <span data-ttu-id="66ef0-134">Para detener la herramienta VSS Writer, presione CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="66ef0-134">To stop the VSS Test Writer tool, press CTRL+C.</span></span>

6.  <span data-ttu-id="66ef0-135">En la segunda ventana de comandos, use la herramienta COMTEST para realizar una operación de copia de seguridad como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="66ef0-135">In the second command window, use the BETest tool to perform a backup operation as follows:</span></span>

    <span data-ttu-id="66ef0-136">**betest.exe/B/S backup.xml/D C: \\ BackupDestination/x BetestSample.xml**</span><span class="sxs-lookup"><span data-stu-id="66ef0-136">**betest.exe /B /S backup.xml /D C:\\BackupDestination /X BetestSample.xml**</span></span>

    <span data-ttu-id="66ef0-137">COMTEST hará una copia de seguridad de los archivos del \\ directorio c: TestPath en el \\ directorio c: BackupDestination</span><span class="sxs-lookup"><span data-stu-id="66ef0-137">BETest will back up the files from the C:\\TestPath directory to the C:\\BackupDestination directory.</span></span> <span data-ttu-id="66ef0-138">Se guardará el documento del componente de copia de seguridad en C: \\ Compruébelo \\backup.xml.</span><span class="sxs-lookup"><span data-stu-id="66ef0-138">It will save the backup component document to C:\\BETest\\backup.xml.</span></span>

7.  <span data-ttu-id="66ef0-139">Si la operación de copia de seguridad se realiza correctamente, elimine el contenido del directorio C: \\ TestPath y use la herramienta COMTEST para realizar una operación de restauración de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="66ef0-139">If the backup operation is successful, delete the contents of the C:\\TestPath directory, and use the BETest tool to perform a restore operation as follows:</span></span>

    <span data-ttu-id="66ef0-140">**betest.exe/R/S backup.xml/D C: \\ BackupDestination/x BetestSample.xml**</span><span class="sxs-lookup"><span data-stu-id="66ef0-140">**betest.exe /R /S backup.xml /D C:\\BackupDestination /X BetestSample.xml**</span></span>

## <a name="betest-tool-command-line-options"></a><span data-ttu-id="66ef0-141">Opciones de Command-Line de herramientas de prueba</span><span class="sxs-lookup"><span data-stu-id="66ef0-141">BETest Tool Command-Line Options</span></span>

<span data-ttu-id="66ef0-142">La herramienta COMTEST usa las siguientes opciones de línea de comandos para identificar el trabajo que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="66ef0-142">The BETest tool uses the following command-line options to identify the work to perform.</span></span>

<dl> <dt>

<span data-ttu-id="66ef0-143"><span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**</span><span class="sxs-lookup"><span data-stu-id="66ef0-143"><span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**</span></span>
</dt> <dd>

<span data-ttu-id="66ef0-144">Realiza una operación de restauración autoritativa para Active Directory o Active Directory Application Mode.</span><span class="sxs-lookup"><span data-stu-id="66ef0-144">Performs an authoritative restore operation for Active Directory or Active Directory Application Mode.</span></span>

<span data-ttu-id="66ef0-145">**Windows Server 2003:** No se admite esta opción de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="66ef0-145">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="66ef0-146"><span id="_B"></span><span id="_b"></span>**B**</span><span class="sxs-lookup"><span data-stu-id="66ef0-146"><span id="_B"></span><span id="_b"></span>**/B**</span></span>
</dt> <dd>

<span data-ttu-id="66ef0-147">Realiza una operación de copia de seguridad, pero no realiza una restauración.</span><span class="sxs-lookup"><span data-stu-id="66ef0-147">Performs a backup operation but does not perform a restore.</span></span>

</dd> <dt>

<span data-ttu-id="66ef0-148"><span id="_BC"></span><span id="_bc"></span>**/BC**</span><span class="sxs-lookup"><span data-stu-id="66ef0-148"><span id="_BC"></span><span id="_bc"></span>**/BC**</span></span>
</dt> <dd>

<span data-ttu-id="66ef0-149">Solo realiza la operación de copia de seguridad completa.</span><span class="sxs-lookup"><span data-stu-id="66ef0-149">Performs only the backup complete operation.</span></span>

<span data-ttu-id="66ef0-150">**Windows Server 2003:** No se admite esta opción de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="66ef0-150">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="66ef0-151"><span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *nombreDeArchivo*</span><span class="sxs-lookup"><span data-stu-id="66ef0-151"><span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *Filename*</span></span>
</dt> <dd>

> [!Note]  
> <span data-ttu-id="66ef0-152">Esta opción de línea de comandos solo se proporciona para la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="66ef0-152">This command-line option is provided only for backward compatibility.</span></span> <span data-ttu-id="66ef0-153">En su lugar, se debe utilizar la opción de línea de comandos **/x** .</span><span class="sxs-lookup"><span data-stu-id="66ef0-153">The **/X** command-line option should be used instead.</span></span>

 

<span data-ttu-id="66ef0-154">Selecciona los componentes de los que se va a realizar una copia de seguridad o que se van a restaurar según el contenido del archivo de configuración especificado por *filename*.</span><span class="sxs-lookup"><span data-stu-id="66ef0-154">Selects the components to be backed up or restored based on the contents of the configuration file specified by *Filename*.</span></span> <span data-ttu-id="66ef0-155">Este archivo debe contener solo caracteres ANSI en el intervalo comprendido entre 0 y 127, y no debe tener más de 1 MB.</span><span class="sxs-lookup"><span data-stu-id="66ef0-155">This file must contain only ANSI characters in the range from 0 through 127, and it must be no larger than 1 MB.</span></span> <span data-ttu-id="66ef0-156">Cada línea del archivo debe tener el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="66ef0-156">Each line in the file must use the following format:</span></span>

<span data-ttu-id="66ef0-157">*WriterId* : *ComponentName*;</span><span class="sxs-lookup"><span data-stu-id="66ef0-157">*WriterId* : *ComponentName*;</span></span>

<span data-ttu-id="66ef0-158">Donde *WriterId* es el identificador del escritor y *ComponentName* es el nombre de uno de los componentes del escritor.</span><span class="sxs-lookup"><span data-stu-id="66ef0-158">Where *WriterId* is the writer ID, and *ComponentName* is the name of one of the writer's components.</span></span> <span data-ttu-id="66ef0-159">El identificador del escritor y los nombres de los componentes deben estar entre comillas y debe haber espacios delante y detrás del signo de dos puntos (:).</span><span class="sxs-lookup"><span data-stu-id="66ef0-159">The writer ID and component names must be in quotation marks, and there must be spaces before and after the colon (:).</span></span> <span data-ttu-id="66ef0-160">Si se especifican dos o más componentes, deben separarse con comas.</span><span class="sxs-lookup"><span data-stu-id="66ef0-160">If two or more components are specified, they must be separated by commas.</span></span> <span data-ttu-id="66ef0-161">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="66ef0-161">For example:</span></span>

<span data-ttu-id="66ef0-162">"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";</span><span class="sxs-lookup"><span data-stu-id="66ef0-162">"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";</span></span>

</dd> <dt>

<span data-ttu-id="66ef0-163"><span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** ( *ruta* )</span><span class="sxs-lookup"><span data-stu-id="66ef0-163"><span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *Path*</span></span>
</dt> <dd>

<span data-ttu-id="66ef0-164">Guarde los archivos de copia de seguridad en o los restaure desde el directorio de copia de seguridad especificado por *path*.</span><span class="sxs-lookup"><span data-stu-id="66ef0-164">Save the backed-up files to or restore them from the backup directory specified by *Path*.</span></span>

</dd> <dt>

<span data-ttu-id="66ef0-165"><span id="_NBC"></span><span id="_nbc"></span>**/NBC**</span><span class="sxs-lookup"><span data-stu-id="66ef0-165"><span id="_NBC"></span><span id="_nbc"></span>**/NBC**</span></span>
</dt> <dd>

<span data-ttu-id="66ef0-166">Omite la operación de copia de seguridad completa.</span><span class="sxs-lookup"><span data-stu-id="66ef0-166">Omits the backup complete operation.</span></span>

<span data-ttu-id="66ef0-167">**Windows Server 2003:** No se admite esta opción de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="66ef0-167">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="66ef0-168"><span id="_O"></span><span id="_o"></span>**/O**</span><span class="sxs-lookup"><span data-stu-id="66ef0-168"><span id="_O"></span><span id="_o"></span>**/O**</span></span>
</dt> <dd>

<span data-ttu-id="66ef0-169">Especifica que la copia de seguridad incluye un estado del sistema de arranque.</span><span class="sxs-lookup"><span data-stu-id="66ef0-169">Specifies that the backup includes a bootable system state.</span></span>

</dd> <dt>

<span data-ttu-id="66ef0-170"><span id="_P"></span><span id="_p"></span>**/P**</span><span class="sxs-lookup"><span data-stu-id="66ef0-170"><span id="_P"></span><span id="_p"></span>**/P**</span></span>
</dt> <dd>

<span data-ttu-id="66ef0-171">Crea una instantánea persistente.</span><span class="sxs-lookup"><span data-stu-id="66ef0-171">Creates a persistent shadow copy.</span></span>

<span data-ttu-id="66ef0-172">**Windows Server 2003:** No se admite esta opción de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="66ef0-172">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="66ef0-173"><span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span> *Nombre de archivo* /pre</span><span class="sxs-lookup"><span data-stu-id="66ef0-173"><span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span>**/Pre** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="66ef0-174">Si el tipo de copia de seguridad especificado en la opción de línea de comandos **/t** es incremental o diferencial, establezca el documento de copia de seguridad en el archivo especificado por *filename* para la copia de seguridad completa o incremental anterior.</span><span class="sxs-lookup"><span data-stu-id="66ef0-174">If the backup type specified in the **/T** command-line option is INCREMENTAL or DIFFERENTIAL, set the backup document to the file specified by *Filename* for previous full or incremental backup.</span></span>

<span data-ttu-id="66ef0-175">**Windows Server 2003 y Windows XP:** No se admite esta opción de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="66ef0-175">**Windows Server 2003 and Windows XP:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="66ef0-176"><span id="_R"></span><span id="_r"></span>**/R**</span><span class="sxs-lookup"><span data-stu-id="66ef0-176"><span id="_R"></span><span id="_r"></span>**/R**</span></span>
</dt> <dd>

<span data-ttu-id="66ef0-177">Realiza la restauración pero no realiza la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="66ef0-177">Performs restore but does not perform backup.</span></span> <span data-ttu-id="66ef0-178">Se debe usar junto con la opción de línea de comandos **/s** .</span><span class="sxs-lookup"><span data-stu-id="66ef0-178">Must be used together with the **/S** command-line option.</span></span>

</dd> <dt>

<span data-ttu-id="66ef0-179"><span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**</span><span class="sxs-lookup"><span data-stu-id="66ef0-179"><span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**</span></span>
</dt> <dd>

<span data-ttu-id="66ef0-180">Crea una instantánea que se puede utilizar para la reversión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="66ef0-180">Creates a shadow copy that can be used for application rollback.</span></span>

<span data-ttu-id="66ef0-181">**Windows Server 2003:** No se admite esta opción de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="66ef0-181">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="66ef0-182"><span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *nombreDeArchivo*</span><span class="sxs-lookup"><span data-stu-id="66ef0-182"><span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="66ef0-183">En el caso de la copia de seguridad, guarda el documento de copia de seguridad en el archivo especificado por *filename*.</span><span class="sxs-lookup"><span data-stu-id="66ef0-183">In case of backup, saves the backup document to the file specified by *Filename*.</span></span> <span data-ttu-id="66ef0-184">En el caso de la restauración, carga el documento de copia de seguridad desde este archivo.</span><span class="sxs-lookup"><span data-stu-id="66ef0-184">In case of restore only, loads the backup document from this file.</span></span>

</dd> <dt>

<span data-ttu-id="66ef0-185"><span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**</span><span class="sxs-lookup"><span data-stu-id="66ef0-185"><span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**</span></span>
</dt> <dd>

<span data-ttu-id="66ef0-186">Crea una instantánea de volumen pero no realiza copias de seguridad ni restauración.</span><span class="sxs-lookup"><span data-stu-id="66ef0-186">Creates a volume shadow copy but does not perform backup or restore.</span></span>

<span data-ttu-id="66ef0-187">**Windows Server 2003:** No se admite esta opción de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="66ef0-187">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="66ef0-188"><span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**</span><span class="sxs-lookup"><span data-stu-id="66ef0-188"><span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**</span></span>
</dt> <dd>

<span data-ttu-id="66ef0-189">Detiene la prueba cuando se encuentra el primer error de escritura.</span><span class="sxs-lookup"><span data-stu-id="66ef0-189">Stops BETest when the first writer error is encountered.</span></span>

<span data-ttu-id="66ef0-190">**Windows Server 2003:** No se admite esta opción de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="66ef0-190">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="66ef0-191"><span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *copia*</span><span class="sxs-lookup"><span data-stu-id="66ef0-191"><span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*</span></span>
</dt> <dd>

<span data-ttu-id="66ef0-192">Especifica el tipo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="66ef0-192">Specifies the backup type.</span></span> <span data-ttu-id="66ef0-193">*Copia* puede ser completo, registro, copia, incremental o diferencial.</span><span class="sxs-lookup"><span data-stu-id="66ef0-193">*BackupType* can be FULL, LOG, COPY, INCREMENTAL, or DIFFERENTIAL.</span></span> <span data-ttu-id="66ef0-194">Para obtener más información sobre los tipos de copia de seguridad, vea [**\_ \_ tipo de copia de seguridad de VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).</span><span class="sxs-lookup"><span data-stu-id="66ef0-194">For more information about backup types, see [**VSS\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).</span></span>

</dd> <dt>

<span data-ttu-id="66ef0-195"><span id="_V"></span><span id="_v"></span>**/V**</span><span class="sxs-lookup"><span data-stu-id="66ef0-195"><span id="_V"></span><span id="_v"></span>**/V**</span></span>
</dt> <dd>

<span data-ttu-id="66ef0-196">Genera una salida detallada que se puede usar para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="66ef0-196">Generates verbose output that can be used for troubleshooting.</span></span>

<span data-ttu-id="66ef0-197">**Windows Server 2003:** No se admite esta opción de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="66ef0-197">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="66ef0-198"><span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *nombreDeArchivo*</span><span class="sxs-lookup"><span data-stu-id="66ef0-198"><span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="66ef0-199">Selecciona los componentes de los que se va a realizar una copia de seguridad o que se van a restaurar según el contenido del archivo de configuración XML especificado por *filename*.</span><span class="sxs-lookup"><span data-stu-id="66ef0-199">Selects the components to be backed up or restored based on the contents of the XML configuration file specified by *Filename*.</span></span> <span data-ttu-id="66ef0-200">Este archivo solo debe contener caracteres ANSI en el intervalo comprendido entre 0 y 127.</span><span class="sxs-lookup"><span data-stu-id="66ef0-200">This file must contain only ANSI characters in the range from 0 through 127.</span></span> <span data-ttu-id="66ef0-201">El formato del archivo XML lo define el esquema en el archivo de BETest.xml.</span><span class="sxs-lookup"><span data-stu-id="66ef0-201">The format of the XML file is defined by the schema in the BETest.xml file.</span></span> <span data-ttu-id="66ef0-202">Para obtener un archivo de configuración de ejemplo, vea BetestSample.xml.</span><span class="sxs-lookup"><span data-stu-id="66ef0-202">For a sample configuration file, see BetestSample.xml.</span></span> <span data-ttu-id="66ef0-203">Ambos archivos se encuentran en el directorio vsstools</span><span class="sxs-lookup"><span data-stu-id="66ef0-203">Both of these files are in the vsstools directory.</span></span>

> [!Note]  
> <span data-ttu-id="66ef0-204">Puede ver el archivo de BETest.xml en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="66ef0-204">You can view the BETest.xml file in Internet Explorer.</span></span> <span data-ttu-id="66ef0-205">Antes de abrir este archivo, asegúrese de que el archivo XDR-Schema. xsl está en el mismo directorio que BETest.xml.</span><span class="sxs-lookup"><span data-stu-id="66ef0-205">Before you open this file, make sure that the xdr-schema.xsl file is in the same directory as BETest.xml.</span></span> <span data-ttu-id="66ef0-206">El archivo XDR-Schema. xsl contiene instrucciones de representación que hacen que el archivo BETest.xml sea más legible.</span><span class="sxs-lookup"><span data-stu-id="66ef0-206">The xdr-schema.xsl file contains rendering instructions that make the BETest.xml file more readable.</span></span>

 

<span data-ttu-id="66ef0-207">**Windows Server 2003:** No se admite esta opción de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="66ef0-207">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> </dl>

## <a name="sample-xml-configuration-file-betestsamplexml"></a><span data-ttu-id="66ef0-208">Archivo de configuración XML de ejemplo: BetestSample.xml</span><span class="sxs-lookup"><span data-stu-id="66ef0-208">Sample XML Configuration File: BetestSample.xml</span></span>

<span data-ttu-id="66ef0-209">El siguiente archivo de configuración de ejemplo, BetestSample.xml, se puede encontrar en el directorio Vsstools</span><span class="sxs-lookup"><span data-stu-id="66ef0-209">The following sample configuration file, BetestSample.xml, can be found in the Vsstools directory.</span></span>

``` syntax
<BETest>
    <Writer writerid="5affb034-969f-4919-8875-88f830d0ef89">
        <Component componentName="TestFiles">
        </Component>
    </Writer>
</BETest>
```

<span data-ttu-id="66ef0-210">En este ejemplo de un archivo de configuración simple se selecciona un componente del que se va a realizar la copia de seguridad o la restauración.</span><span class="sxs-lookup"><span data-stu-id="66ef0-210">This example of a simple configuration file selects one component to be backed up or restored.</span></span>

## <a name="sample-xml-configuration-file-vswritersamplexml"></a><span data-ttu-id="66ef0-211">Archivo de configuración XML de ejemplo: VswriterSample.xml</span><span class="sxs-lookup"><span data-stu-id="66ef0-211">Sample XML Configuration File: VswriterSample.xml</span></span>

<span data-ttu-id="66ef0-212">El siguiente archivo de configuración de ejemplo, VswriterSample.xml, se puede encontrar en el directorio Vsstools</span><span class="sxs-lookup"><span data-stu-id="66ef0-212">The following sample configuration file, VswriterSample.xml, can be found in the Vsstools directory.</span></span>

``` syntax
<TestWriter   usage="USER_DATA"
                    deleteFiles="no">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED" 
                   writerRestore="always"
                   rebootRequired="no" />
    
    <Component componentType="filegroup" 
               componentName="TestFiles">
               <ComponentFile path="c:\TestPath" filespec="*" recursive="no" />
    </Component>

</TestWriter>
```

<span data-ttu-id="66ef0-213">El elemento raíz de este archivo de configuración se denomina TestWriter.</span><span class="sxs-lookup"><span data-stu-id="66ef0-213">The root element in this configuration file is named TestWriter.</span></span> <span data-ttu-id="66ef0-214">Todos los demás elementos se organizan bajo el elemento TestWriter.</span><span class="sxs-lookup"><span data-stu-id="66ef0-214">All other elements are arranged under the TestWriter element.</span></span>

<span data-ttu-id="66ef0-215">El primer atributo asociado a TestWriter es el atributo Usage.</span><span class="sxs-lookup"><span data-stu-id="66ef0-215">The first attribute associated with TestWriter is the usage attribute.</span></span> <span data-ttu-id="66ef0-216">Este atributo especifica el tipo de uso indicado a través del método [**IVssExamineWriterMetadata:: GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) .</span><span class="sxs-lookup"><span data-stu-id="66ef0-216">This attribute specifies the usage type reported through the [**IVssExamineWriterMetadata::GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) method.</span></span> <span data-ttu-id="66ef0-217">Uno de los valores posibles para este atributo son los \_ datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="66ef0-217">One of the possible values for this attribute is USER\_DATA.</span></span>

<span data-ttu-id="66ef0-218">El segundo atributo es el atributo deleteFiles.</span><span class="sxs-lookup"><span data-stu-id="66ef0-218">The second attribute is the deleteFiles attribute.</span></span> <span data-ttu-id="66ef0-219">Este atributo se describe en [configuración de los atributos del escritor](vss-test-writer-tool.md).</span><span class="sxs-lookup"><span data-stu-id="66ef0-219">This attribute is described in [Configuring Writer Attributes](vss-test-writer-tool.md).</span></span>

<span data-ttu-id="66ef0-220">El primer elemento secundario del elemento raíz es un elemento RestoreMethod.</span><span class="sxs-lookup"><span data-stu-id="66ef0-220">The first child element of the root element is a RestoreMethod element.</span></span> <span data-ttu-id="66ef0-221">Este elemento especifica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="66ef0-221">This element specifies the following:</span></span>

-   <span data-ttu-id="66ef0-222">El método restore (en este caso, RESTOre \_ If \_ \_ se puede \_ reemplazar)</span><span class="sxs-lookup"><span data-stu-id="66ef0-222">The restore method (in this case, RESTORE\_IF\_CAN\_BE\_REPLACED)</span></span>
-   <span data-ttu-id="66ef0-223">Si el escritor requiere eventos de restauración (en este caso, siempre)</span><span class="sxs-lookup"><span data-stu-id="66ef0-223">Whether the writer requires restore events (in this case, always)</span></span>
-   <span data-ttu-id="66ef0-224">Si es necesario un reinicio después de restaurar el escritor (en este caso, no)</span><span class="sxs-lookup"><span data-stu-id="66ef0-224">Whether a reboot is required after the writer is restored (in this case, no)</span></span>

<span data-ttu-id="66ef0-225">Este elemento puede especificar opcionalmente una asignación de ubicación alternativa.</span><span class="sxs-lookup"><span data-stu-id="66ef0-225">This element can optionally specify an alternate-location mapping.</span></span> <span data-ttu-id="66ef0-226">(En este caso, no se especifica ninguna ubicación alternativa). Para obtener más información, vea [especificar asignaciones de ubicaciones alternativas](vss-test-writer-tool.md).</span><span class="sxs-lookup"><span data-stu-id="66ef0-226">(In this case, no alternate location is specified.) For more information, see [Specifying Alternate Location Mappings](vss-test-writer-tool.md).</span></span>

<span data-ttu-id="66ef0-227">El segundo elemento secundario es un elemento de componente.</span><span class="sxs-lookup"><span data-stu-id="66ef0-227">The second child element is a Component element.</span></span> <span data-ttu-id="66ef0-228">Este elemento hace que el escritor agregue un componente a sus metadatos.</span><span class="sxs-lookup"><span data-stu-id="66ef0-228">This element causes the writer to add a component to its metadata.</span></span> <span data-ttu-id="66ef0-229">Un elemento Component contiene atributos para describir el componente y los elementos secundarios para describir el contenido del componente, como el siguiente:</span><span class="sxs-lookup"><span data-stu-id="66ef0-229">A Component element contains attributes to describe the component and child elements to describe the content of the component, such as the following:</span></span>

-   <span data-ttu-id="66ef0-230">componentType para indicar si se trata de un grupo de archivos o de una base de datos (en este caso, un grupo de archivos)</span><span class="sxs-lookup"><span data-stu-id="66ef0-230">componentType to indicate whether this is a filegroup or a database (in this case, a filegroup)</span></span>
-   <span data-ttu-id="66ef0-231">logicalPath para la ruta de acceso lógica del componente (en este caso, no se especifica ninguno)</span><span class="sxs-lookup"><span data-stu-id="66ef0-231">logicalPath for the component logical path (in this case, none is specified)</span></span>
-   <span data-ttu-id="66ef0-232">componentName para el nombre del componente (en este caso, "prueba")</span><span class="sxs-lookup"><span data-stu-id="66ef0-232">componentName for the name of the component (in this case, "TestFiles")</span></span>
-   <span data-ttu-id="66ef0-233">Selectable para indicar el estado Selectable-for-Backup</span><span class="sxs-lookup"><span data-stu-id="66ef0-233">selectable to indicate selectable-for-backup status</span></span>

<span data-ttu-id="66ef0-234">El elemento componente también tiene un elemento secundario denominado ComponentFile para agregar una especificación de archivo a este componente.</span><span class="sxs-lookup"><span data-stu-id="66ef0-234">The Component element also has a child element named ComponentFile to add a file specification to this component.</span></span> <span data-ttu-id="66ef0-235">(Un elemento de componente puede tener un número arbitrario de elementos ComponentFile que se pueden especificar para cada componente). Este elemento ComponentFile tiene los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="66ef0-235">(A Component element can have an arbitrary number of ComponentFile elements that can be specified for each component.) This ComponentFile element has the following attributes:</span></span>

-   <span data-ttu-id="66ef0-236">Ruta de acceso = "c: \\ TestPath"</span><span class="sxs-lookup"><span data-stu-id="66ef0-236">path="c:\\TestPath"</span></span>
-   <span data-ttu-id="66ef0-237">filespec = " \* "</span><span class="sxs-lookup"><span data-stu-id="66ef0-237">filespec="\*"</span></span>
-   <span data-ttu-id="66ef0-238">Recursive = "no"</span><span class="sxs-lookup"><span data-stu-id="66ef0-238">recursive="no"</span></span>

 

 



