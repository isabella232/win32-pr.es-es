---
description: 'Más información sobre: ejemplos de herramientas de VShadow'
ms.assetid: 6a69b75b-ee4a-4613-ba05-d2deb42759b7
title: Ejemplos de la herramienta VShadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65fd2bfa1c390b1bd5310cd80f02e029dbf935f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809829"
---
# <a name="vshadow-tool-examples"></a><span data-ttu-id="a5c1c-103">Ejemplos de la herramienta VShadow</span><span class="sxs-lookup"><span data-stu-id="a5c1c-103">VShadow Tool Examples</span></span>

<span data-ttu-id="a5c1c-104">En los siguientes ejemplos se muestra cómo usar la herramienta VShadow para realizar las tareas más comunes:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-104">The following examples show how to use the VShadow tool to perform the most common tasks:</span></span>

-   [<span data-ttu-id="a5c1c-105">Obtener acceso a las propiedades de instantánea desde un script CMD</span><span class="sxs-lookup"><span data-stu-id="a5c1c-105">Accessing Shadow Copy Properties from a CMD Script</span></span>](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [<span data-ttu-id="a5c1c-106">Obtener acceso a instantáneas no persistentes</span><span class="sxs-lookup"><span data-stu-id="a5c1c-106">Accessing Nonpersistent Shadow Copies</span></span>](#accessing-nonpersistent-shadow-copies)
-   [<span data-ttu-id="a5c1c-107">Copiar un archivo de una instantánea</span><span class="sxs-lookup"><span data-stu-id="a5c1c-107">Copying a File from a Shadow Copy</span></span>](#copying-a-file-from-a-shadow-copy)
-   [<span data-ttu-id="a5c1c-108">Enumerar todos los archivos de un dispositivo de instantánea</span><span class="sxs-lookup"><span data-stu-id="a5c1c-108">Enumerating All Files on a Shadow Copy Device</span></span>](#enumerating-all-files-on-a-shadow-copy-device)
-   [<span data-ttu-id="a5c1c-109">Importar una instantánea transportable</span><span class="sxs-lookup"><span data-stu-id="a5c1c-109">Importing a Transportable Shadow Copy</span></span>](#importing-a-transportable-shadow-copy)
-   [<span data-ttu-id="a5c1c-110">Incluir escritores o componentes</span><span class="sxs-lookup"><span data-stu-id="a5c1c-110">Including Writers or Components</span></span>](#including-writers-or-components)
-   [<span data-ttu-id="a5c1c-111">Exclusión de escritores o componentes</span><span class="sxs-lookup"><span data-stu-id="a5c1c-111">Excluding Writers or Components</span></span>](#excluding-writers-or-components)
-   [<span data-ttu-id="a5c1c-112">Romper conjuntos de instantáneas mediante el método BreakSnapshotSetEx</span><span class="sxs-lookup"><span data-stu-id="a5c1c-112">Breaking Shadow Copy Sets Using the BreakSnapshotSetEx Method</span></span>](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

<span data-ttu-id="a5c1c-113">Para obtener una lista completa de las opciones de línea de comandos y su uso, vea [herramienta y ejemplo de VShadow](vshadow-tool-and-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a5c1c-113">For a complete list of command-line options and their use, see [VShadow Tool and Sample](vshadow-tool-and-sample.md).</span></span>

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a><span data-ttu-id="a5c1c-114">Obtener acceso a las propiedades de instantánea desde un script CMD</span><span class="sxs-lookup"><span data-stu-id="a5c1c-114">Accessing Shadow Copy Properties from a CMD Script</span></span>

<span data-ttu-id="a5c1c-115">Si usa la marca opcional **-script** al crear instantáneas, VShadow crea un archivo de script cmd que contiene variables de entorno relacionadas con las instantáneas recién creadas, como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-115">If you use the **-script** optional flag when you create shadow copies, VShadow creates a CMD script file containing environment variables related to the newly created shadow copies, such as the following:</span></span>

-   <span data-ttu-id="a5c1c-116">El identificador del conjunto de instantáneas, que se almacena en la \_ variable de entorno% VSHADOW set \_ ID%</span><span class="sxs-lookup"><span data-stu-id="a5c1c-116">The shadow copy set ID, which is stored in the %VSHADOW\_SET\_ID% environment variable</span></span>
-   <span data-ttu-id="a5c1c-117">Los identificadores de instantánea, que se almacenan en variables con el formato% VSHADOW \_ ID \_ *nnn*%, donde *nnn* representa el índice del volumen de origen en la línea de comandos de VSHADOW</span><span class="sxs-lookup"><span data-stu-id="a5c1c-117">The shadow copy IDs, which are stored in variables of the form %VSHADOW\_ID\_*NNN*%, where *NNN* represents the index of the source volume in the VShadow command line</span></span>
-   <span data-ttu-id="a5c1c-118">Los nombres de los dispositivos de instantáneas, que se almacenan en variables de la forma% VSHADOW \_ dispositivo \_ *nnn*%, donde *nnn* es el índice del volumen de origen en la línea de comandos de VSHADOW</span><span class="sxs-lookup"><span data-stu-id="a5c1c-118">The shadow copy device names, which are stored in variables of the form %VSHADOW\_DEVICE\_*NNN*%, where *NNN* is the index of the source volume in the VShadow command line</span></span>

<span data-ttu-id="a5c1c-119">Puede usar el archivo CMD generado para realizar operaciones de administración limitadas en las instantáneas.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-119">You can use the generated CMD file to perform limited management operations on the shadow copies.</span></span>

> [!Note]  
> <span data-ttu-id="a5c1c-120">El evento [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) Writer se envía después de ejecutar el script **-exec** .</span><span class="sxs-lookup"><span data-stu-id="a5c1c-120">The [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) writer event is sent after the **-exec** script is executed.</span></span> <span data-ttu-id="a5c1c-121">VSS llama al método **IVssBackupComponents:: BackupComplete** para indicar a los escritores que la copia de seguridad se ha completado y los escritores pueden truncar los registros en este momento.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-121">VSS calls the **IVssBackupComponents::BackupComplete** method to signal to the writers that the backup is completed, and the writers can potentially truncate logs at this point.</span></span> <span data-ttu-id="a5c1c-122">Por lo tanto, es importante comprobar que la instantánea o copia de seguridad se completó realmente.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-122">Therefore, it is important to verify that the shadow/backup actually completed.</span></span> <span data-ttu-id="a5c1c-123">Si se produjo un error en la copia de seguridad, puede cancelar el proceso de creación devolviendo un código de salida distinto de cero en el script o comando ejecutado.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-123">If the backup failed, you can cancel the creation process by returning a nonzero exit code in the executed script/command.</span></span> <span data-ttu-id="a5c1c-124">(Consulte la documentación del comando exit en la referencia de la [línea de comandos de Windows](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11))). Si el comando personalizado devuelve un código de salida distinto de cero, se cancela la creación de la instantánea y no se llamará a **IVssBackupComponents:: BackupComplete** .</span><span class="sxs-lookup"><span data-stu-id="a5c1c-124">(See the documentation for the exit command in the [Windows Command Line Reference](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)).) If the custom command returns with a nonzero exit code, then the shadow copy creation is canceled and **IVssBackupComponents::BackupComplete** will not be called.</span></span>

 

<span data-ttu-id="a5c1c-125">En el ejemplo siguiente se muestra cómo crear una instantánea persistente desde la línea de comandos y usar el script CMD para exponerla.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-125">The following example shows how to create a persistent shadow copy from the command line and use the CMD script to expose it.</span></span>

1.  <span data-ttu-id="a5c1c-126">**vshadow-p-NW-script = SETVAR1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-126">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
2.  <span data-ttu-id="a5c1c-127">**llamar a SETVAR1. cmd**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-127">**call SETVAR1.cmd**</span></span>
3.  <span data-ttu-id="a5c1c-128">**C: \\>vshadow-el =% vshadow \_ ID. \_ 1%, c: \\ directory1**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-128">**C:\\>vshadow -el=%VSHADOW\_ID\_1%,c:\\directory1**</span></span>

## <a name="accessing-nonpersistent-shadow-copies"></a><span data-ttu-id="a5c1c-129">Obtener acceso a instantáneas no persistentes</span><span class="sxs-lookup"><span data-stu-id="a5c1c-129">Accessing Nonpersistent Shadow Copies</span></span>

<span data-ttu-id="a5c1c-130">Las instantáneas no persistentes se eliminan automáticamente cuando se cierra el programa que las crea (en este caso, VShadow).</span><span class="sxs-lookup"><span data-stu-id="a5c1c-130">Nonpersistent shadow copies are automatically deleted when the program that creates them (in this case, VShadow) exits.</span></span> <span data-ttu-id="a5c1c-131">Para tener acceso al contenido de estas instantáneas, VShadow le permite ejecutar un script una vez creadas las instantáneas, pero antes de que se cierre el programa VShadow.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-131">To access the contents of these shadow copies, VShadow allows you to execute a script after the shadow copies are created but before the VShadow program exits.</span></span>

<span data-ttu-id="a5c1c-132">En el ejemplo siguiente se muestra cómo usar la opción de línea de comandos-Exec para ejecutar un script denominado "enum. cmd":</span><span class="sxs-lookup"><span data-stu-id="a5c1c-132">The following example shows how to use the -exec command-line option to run a script called "enum.cmd":</span></span>

<span data-ttu-id="a5c1c-133">**vshadow-NW-exec = enum. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-133">**vshadow -nw -exec=enum.cmd c:**</span></span>

<span data-ttu-id="a5c1c-134">En el script ejecutado, también puede ejecutar el script SETVAR generado en este comando personalizado.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-134">In the executed script, you can also run the generated SETVAR script in this custom command.</span></span> <span data-ttu-id="a5c1c-135">Esto permite que el script tenga acceso directamente al contenido de las instantáneas.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-135">This allows the script to access the contents of the shadow copies directly.</span></span> <span data-ttu-id="a5c1c-136">Recuerde que el dispositivo de instantáneas se puede recuperar de la variable de entorno VSHADOW del \_ dispositivo \_ nnn.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-136">Remember that the shadow device can be retrieved from the VSHADOW\_DEVICE\_NNN environment variable.</span></span>

<span data-ttu-id="a5c1c-137">Este es un ejemplo de script enum. cmd:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-137">Here is an example enum.cmd script:</span></span>

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

<span data-ttu-id="a5c1c-138">Esta es la línea de comandos para ejecutar el script enum. cmd:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-138">Here is the command line to execute the enum.cmd script:</span></span>

<span data-ttu-id="a5c1c-139">**vshadow-NW-exec = c: \\ enum. cmd-script = setvar1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-139">**vshadow -nw -exec=c:\\enum.cmd -script=setvar1.cmd c:**</span></span>

## <a name="copying-a-file-from-a-shadow-copy"></a><span data-ttu-id="a5c1c-140">Copiar un archivo de una instantánea</span><span class="sxs-lookup"><span data-stu-id="a5c1c-140">Copying a File from a Shadow Copy</span></span>

<span data-ttu-id="a5c1c-141">En el ejemplo siguiente se muestra cómo copiar un archivo de una instantánea.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-141">The following example shows how to copy a file from a shadow copy.</span></span>

1.  <span data-ttu-id="a5c1c-142">**DIR > c: \\somefile.txt**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-142">**dir > c:\\somefile.txt**</span></span>
2.  <span data-ttu-id="a5c1c-143">**vshadow-p-NW-script = SETVAR1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-143">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
3.  <span data-ttu-id="a5c1c-144">**llamar a SETVAR1. cmd**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-144">**call SETVAR1.cmd**</span></span>
4.  <span data-ttu-id="a5c1c-145">**copia% VSHADOW \_ dispositivo \_ 1% \\somefile.txt c: \\ somefile \_bak.txt**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-145">**copy %VSHADOW\_DEVICE\_1%\\somefile.txt c:\\somefile\_bak.txt**</span></span>

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a><span data-ttu-id="a5c1c-146">Enumerar todos los archivos de un dispositivo de instantánea</span><span class="sxs-lookup"><span data-stu-id="a5c1c-146">Enumerating All Files on a Shadow Copy Device</span></span>

<span data-ttu-id="a5c1c-147">En el ejemplo siguiente se muestra cómo enumerar todos los archivos de un dispositivo de instantáneas desde un archivo por lotes.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-147">The following example shows how to enumerate all files on a shadow copy device from a batch file.</span></span>

1.  <span data-ttu-id="a5c1c-148">**DIR > c: \\somefile.txt**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-148">**dir > c:\\somefile.txt**</span></span>
2.  <span data-ttu-id="a5c1c-149">**vshadow-p-NW-script = SETVAR1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-149">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
3.  <span data-ttu-id="a5c1c-150">**llamar a SETVAR1. cmd**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-150">**call SETVAR1.cmd**</span></span>
4.  <span data-ttu-id="a5c1c-151">**en el caso de/R% VSHADOW \_ dispositivo \_ 1% \\ %% i en ( \* ) haga @echo %% i**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-151">**for /R %VSHADOW\_DEVICE\_1%\\ %%i in (\*) do @echo %%i**</span></span>

## <a name="importing-a-transportable-shadow-copy"></a><span data-ttu-id="a5c1c-152">Importar una instantánea transportable</span><span class="sxs-lookup"><span data-stu-id="a5c1c-152">Importing a Transportable Shadow Copy</span></span>

<span data-ttu-id="a5c1c-153">Para crear una instantánea transportable en un equipo e importarlo en otro equipo, debe tener dos equipos conectados (a través de una configuración de SAN) a una matriz de almacenamiento que admita instantáneas de hardware de VSS.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-153">To create a transportable shadow copy on one machine and import it to another machine, you must have two computers that are connected (through a SAN configuration) to a storage array that supports VSS hardware shadow copies.</span></span> <span data-ttu-id="a5c1c-154">Debe haber un proveedor de hardware de VSS instalado en cada equipo.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-154">A VSS hardware provider must be installed on each computer.</span></span>

<span data-ttu-id="a5c1c-155">En el ejemplo siguiente se muestra cómo crear e importar la instantánea.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-155">The following example shows how to create and import the shadow copy.</span></span>

1.  <span data-ttu-id="a5c1c-156">Cree el conjunto de instantáneas en el equipo A (el servidor de producción) escribiendo el siguiente comando después del símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-156">Create the shadow copy set on computer A (the production server) by typing the following command after the command prompt:</span></span>

    <span data-ttu-id="a5c1c-157">**vshadow-p-t =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-157">**vshadow -p -t=bc1.xml**</span></span>

    <span data-ttu-id="a5c1c-158">Esto no expondrá ningún dispositivo de instantáneas en el equipo A.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-158">This will not expose any shadow copy devices on computer A.</span></span>

2.  <span data-ttu-id="a5c1c-159">Copie el documento componentes de copia de seguridad (bc1.xml) del equipo a al equipo B.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-159">Copy the backup components document (bc1.xml) from computer A to computer B.</span></span>
3.  <span data-ttu-id="a5c1c-160">Para importar el conjunto de instantáneas en el equipo B, escriba el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-160">Import the shadow set on machine B by typing the following command:</span></span>

    <span data-ttu-id="a5c1c-161">**vshadow-i =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-161">**vshadow -i=bc1.xml**</span></span>

<span data-ttu-id="a5c1c-162">Opcionalmente, puede exponer estas instantáneas como Letras de unidad o carpetas montadas.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-162">Optionally, you could expose these shadow copies as drive letters or mounted folders.</span></span> <span data-ttu-id="a5c1c-163">Además, podría romper el conjunto de instantáneas para convertir los nuevos volúmenes de instantáneas en lectura-escritura.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-163">Also, you could potentially break the shadow set to make the new shadow copy volumes read-write.</span></span>

<span data-ttu-id="a5c1c-164">Para automatizar el proceso de administración del conjunto de instantáneas, puede usar la opción de línea de comandos **-script** para generar el script cmd que contiene los identificadores de instantánea.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-164">To automate the shadow set management process you might use the **-script** command-line option to generate the CMD script containing the shadow copy IDs.</span></span> <span data-ttu-id="a5c1c-165">Después, puede copiar el script generado junto con los componentes de copia de seguridad en el otro equipo.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-165">Then you can copy the generated script along with the backup components to the other computer.</span></span>

<span data-ttu-id="a5c1c-166">En el ejemplo siguiente se muestra cómo crear, exponer e interrumpir las instantáneas transportables mediante scripts de CMD.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-166">The following example shows how to create, expose, and break transportable shadow copies using CMD scripts.</span></span>

1.  <span data-ttu-id="a5c1c-167">Cree el conjunto de instantáneas en el equipo A (el servidor de producción) desde la línea de comandos como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-167">Create the shadow copy set on computer A (the production server) from the command line as follows:</span></span>

    <span data-ttu-id="a5c1c-168">**vshadow-p-t =bc1.xml-script = SC1. cmd**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-168">**vshadow -p -t=bc1.xml -script=sc1.cmd**</span></span>

    <span data-ttu-id="a5c1c-169">Especifique la opción **-script** para generar el script que contiene las definiciones de variables de entorno adecuadas.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-169">Specify the **-script** option to generate the script containing the proper environment variable definitions.</span></span> <span data-ttu-id="a5c1c-170">Tenga en cuenta que esto no expondrá ningún dispositivo de instantáneas en el equipo A.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-170">Note that this will not expose any shadow copy devices on computer A.</span></span>

2.  <span data-ttu-id="a5c1c-171">Copie el documento componentes de copia de seguridad (bc1.xml) y el script generado (SC1. cmd) del equipo a al equipo B.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-171">Copy the backup components document (bc1.xml) and the generated script (sc1.cmd) from computer A to computer B.</span></span>
3.  <span data-ttu-id="a5c1c-172">Para importar el conjunto de instantáneas en el equipo B, escriba el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-172">Import the shadow set on machine B by typing the following command:</span></span>

    <span data-ttu-id="a5c1c-173">**vshadow-i =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-173">**vshadow -i=bc1.xml**</span></span>

    <span data-ttu-id="a5c1c-174">Esto hará que se muestren los dispositivos creados en el equipo B.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-174">This will surface the created devices on computer B.</span></span>

4.  <span data-ttu-id="a5c1c-175">Ejecute el script generado para establecer las variables de entorno para el conjunto de instantáneas. para ello, escriba el nombre de archivo en el símbolo del sistema como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-175">Run the generated script to set the environment variables for the shadow copy set by typing the file name at the command prompt as in the following example:</span></span>

    <span data-ttu-id="a5c1c-176">**SC1. cmd**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-176">**sc1.cmd**</span></span>

    <span data-ttu-id="a5c1c-177">Esto establecerá las variables de entorno pertinentes, tal como se describe en el apartado sobre propiedades de instantáneas de acceso de un script CMD.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-177">This will set the relevant environment variables as described in Access Shadow Copy Properties from a CMD Script.</span></span>

5.  <span data-ttu-id="a5c1c-178">Exponga las instantáneas en el equipo B escribiendo los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-178">Expose the shadow copies on computer B by typing the following commands:</span></span>
    1.  <span data-ttu-id="a5c1c-179">**rmdir/s c: \\ punto de montaje \_**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-179">**rmdir /s c:\\mount\_point**</span></span>
    2.  <span data-ttu-id="a5c1c-180">**mkdir c: \\ punto de montaje \_**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-180">**mkdir c:\\mount\_point**</span></span>
    3.  <span data-ttu-id="a5c1c-181">**vshadow – el =% VSHADOW \_ ID. \_ 1%, c \\ : \_ punto de montaje**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-181">**vshadow –el=%VSHADOW\_ID\_1%,c:\\mount\_point**</span></span>

    <span data-ttu-id="a5c1c-182">Esto mostrará los dispositivos de instantáneas creados en el equipo B.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-182">This will surface the created shadow copy devices on computer B.</span></span>
6.  <span data-ttu-id="a5c1c-183">Divida el conjunto de instantáneas para que los volúmenes puedan escribirse escribiendo el comando siguiente:**C: \\>vshadow – BW =% vshadow \_ set \_ ID%**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-183">Break the shadow copy set to make the volumes writable by typing the following command:**C:\\>vshadow –bw=%VSHADOW\_SET\_ID%**</span></span>

<span data-ttu-id="a5c1c-184">Tenga en cuenta que las instantáneas transportables no persistentes también se pueden importar, pero se eliminan automáticamente cuando finaliza el proceso **vshadow** **-i** .</span><span class="sxs-lookup"><span data-stu-id="a5c1c-184">Note that nonpersistent transportable shadow copies can also be imported, but they are automatically deleted when the **vshadow** **-i** process exits.</span></span> <span data-ttu-id="a5c1c-185">Para importar las instantáneas antes de que se eliminen, debe usar la opción de línea de comandos **-exec** tal y como se describe en acceso a instantáneas no persistentes.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-185">To import the shadow copies before they are deleted, you must use the **-exec** command-line option as described in Access Nonpersistent Shadow Copies.</span></span>

## <a name="including-writers-or-components"></a><span data-ttu-id="a5c1c-186">Incluir escritores o componentes</span><span class="sxs-lookup"><span data-stu-id="a5c1c-186">Including Writers or Components</span></span>

<span data-ttu-id="a5c1c-187">De forma predeterminada, todos los escritores participan en la creación de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-187">By default, all writers participate in shadow copy creation.</span></span> <span data-ttu-id="a5c1c-188">Para determinar qué escritores y componentes se incluirán en un conjunto de instantáneas, use la opción de línea de comandos **-WM** o **-wm2** tal como se describe en [enumeración del estado y los metadatos del escritor](vshadow-tool-and-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a5c1c-188">To determine which writers and components will be included in a shadow copy set, use the **-wm** or **-wm2** command-line option as described in [Listing Writer Status and Metadata](vshadow-tool-and-sample.md).</span></span>

<span data-ttu-id="a5c1c-189">Para comprobar que se incluyen todos los componentes de un escritor, use la marca opcional **-Wi** en cualquiera de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-189">To verify that all of a writer's components are included, use the **-wi** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="a5c1c-190">**vshadow** **-Wi** *WriterName*</span><span class="sxs-lookup"><span data-stu-id="a5c1c-190">**vshadow** **-wi** *WriterName*</span></span>
-   <span data-ttu-id="a5c1c-191">**vshadow** **-Wi** **"**_cadena de nombre de escritor_*_"_*</span><span class="sxs-lookup"><span data-stu-id="a5c1c-191">**vshadow** **-wi** **"**_Writer Name String_*_"_*</span></span>
-   <span data-ttu-id="a5c1c-192">**vshadow** **-Wi** **{**_WriterID_*_}_*</span><span class="sxs-lookup"><span data-stu-id="a5c1c-192">**vshadow** **-wi** **{**_WriterID_*_}_*</span></span>
-   <span data-ttu-id="a5c1c-193">**vshadow** **-Wi** **{**_InstanceID_*_}_*</span><span class="sxs-lookup"><span data-stu-id="a5c1c-193">**vshadow** **-wi** **{**_InstanceID_*_}_*</span></span>

<span data-ttu-id="a5c1c-194">Para comprobar que se incluyen determinados componentes, use la marca opcional **-Wi** en cualquiera de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-194">To verify that specific components are included, use the **-wi** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="a5c1c-195">**vshadow** **-Wi** \*WriterName \***: \\**_LogicalPath_\* _\\_ \* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="a5c1c-195">**vshadow** **-wi** *WriterName\***:\\**_LogicalPath_*_\\_\*_ComponentName_</span></span>
-   <span data-ttu-id="a5c1c-196">**vshadow** **-Wi** **"**_cadena de nombre de escritor_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="a5c1c-196">**vshadow** **-wi** **"**_Writer Name String_*_":\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="a5c1c-197">**vshadow** **-Wi** **{**_WriterID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="a5c1c-197">**vshadow** **-wi** **{**_WriterID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="a5c1c-198">**vshadow** **-Wi** **{**_InstanceID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="a5c1c-198">**vshadow** **-wi** **{**_InstanceID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>

<span data-ttu-id="a5c1c-199">En los siguientes ejemplos se muestra cómo usar la marca opcional **-Wi** .</span><span class="sxs-lookup"><span data-stu-id="a5c1c-199">The following examples show how to use the **-wi** optional flag.</span></span>

-   <span data-ttu-id="a5c1c-200">Especificación de *WriterName*: \\ *LogicalPath* \\ *ComponentName*:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-200">Specifying *WriterName*:\\*LogicalPath*\\*ComponentName*:</span></span>

    <span data-ttu-id="a5c1c-201">**vshadow-Wi = "escritor del registro: \\ registro"**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-201">**vshadow -wi="Registry Writer:\\Registry"**</span></span>

-   <span data-ttu-id="a5c1c-202">Especificación de {*WriterID*}:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-202">Specifying {*WriterID*}:</span></span>

    <span data-ttu-id="a5c1c-203">**vshadow-Wi = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-203">**vshadow -wi={BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span></span>

-   <span data-ttu-id="a5c1c-204">Especificando más de un escritor o componente:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-204">Specifying more than one writer or component:</span></span>

    <span data-ttu-id="a5c1c-205">**vshadow-Wi = "escritor del registro: \\ registro"-Wi = "com+ REGDB Writer"**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-205">**vshadow -wi="Registry Writer:\\Registry" -wi="COM+ REGDB Writer"**</span></span>

## <a name="excluding-writers-or-components"></a><span data-ttu-id="a5c1c-206">Exclusión de escritores o componentes</span><span class="sxs-lookup"><span data-stu-id="a5c1c-206">Excluding Writers or Components</span></span>

<span data-ttu-id="a5c1c-207">Para excluir todos los escritores, use la marca opcional **-NW** al crear la instantánea.</span><span class="sxs-lookup"><span data-stu-id="a5c1c-207">To exclude all writers, use the **-nw** optional flag when creating the shadow copy.</span></span>

<span data-ttu-id="a5c1c-208">Para excluir todos los componentes de un escritor, use la marca opcional **-WX** en cualquiera de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-208">To exclude all of a writer's components, use the **-wx** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="a5c1c-209">**vshadow** **-WX** *WriterName*</span><span class="sxs-lookup"><span data-stu-id="a5c1c-209">**vshadow** **-wx** *WriterName*</span></span>
-   <span data-ttu-id="a5c1c-210">**vshadow** **-WX** **"**_cadena de nombre de escritor_*_"_*</span><span class="sxs-lookup"><span data-stu-id="a5c1c-210">**vshadow** **-wx** **"**_Writer Name String_*_"_*</span></span>
-   <span data-ttu-id="a5c1c-211">**vshadow** **-WX** **{**_WriterID_*_}_*</span><span class="sxs-lookup"><span data-stu-id="a5c1c-211">**vshadow** **-wx** **{**_WriterID_*_}_*</span></span>
-   <span data-ttu-id="a5c1c-212">**vshadow** **-WX** **{**_InstanceID_*_}_*</span><span class="sxs-lookup"><span data-stu-id="a5c1c-212">**vshadow** **-wx** **{**_InstanceID_*_}_*</span></span>

<span data-ttu-id="a5c1c-213">Para excluir componentes específicos, use la marca opcional **-WX** en cualquiera de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-213">To exclude specific components, use the **-wx** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="a5c1c-214">**vshadow** **-WX** \*WriterName \***: \\**_LogicalPath_\* _\\_ \* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="a5c1c-214">**vshadow** **-wx** *WriterName\***:\\**_LogicalPath_*_\\_\*_ComponentName_</span></span>
-   <span data-ttu-id="a5c1c-215">**vshadow** **-WX** **"**_cadena de nombre de escritor_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="a5c1c-215">**vshadow** **-wx** **"**_Writer Name String_*_":\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="a5c1c-216">**vshadow** **-WX** **{**_WriterID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="a5c1c-216">**vshadow** **-wx** **{**_WriterID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="a5c1c-217">**vshadow** **-WX** **{**_InstanceID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="a5c1c-217">**vshadow** **-wx** **{**_InstanceID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>

<span data-ttu-id="a5c1c-218">En los siguientes ejemplos se muestra cómo usar la marca opcional **-WX** .</span><span class="sxs-lookup"><span data-stu-id="a5c1c-218">The following examples show how to use the **-wx** optional flag.</span></span>

-   <span data-ttu-id="a5c1c-219">Especificación de *WriterName*: \\ *LogicalPath* \\ *ComponentName*:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-219">Specifying *WriterName*:\\*LogicalPath*\\*ComponentName*:</span></span>

    <span data-ttu-id="a5c1c-220">**vshadow-WX = "escritor del registro: \\ registro"**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-220">**vshadow -wx="Registry Writer:\\Registry"**</span></span>

-   <span data-ttu-id="a5c1c-221">Especificación de {*WriterID*}:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-221">Specifying {*WriterID*}:</span></span>

    <span data-ttu-id="a5c1c-222">**vshadow-WX = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-222">**vshadow -wx={BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span></span>

-   <span data-ttu-id="a5c1c-223">Especificando más de un escritor o componente:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-223">Specifying more than one writer or component:</span></span>

    <span data-ttu-id="a5c1c-224">**vshadow-WX = "escritor del registro: \\ registro"-WX = "escritor de REGDB de com+"**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-224">**vshadow -wx="Registry Writer:\\Registry" -wx="COM+ REGDB Writer"**</span></span>

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a><span data-ttu-id="a5c1c-225">Romper conjuntos de instantáneas mediante el método BreakSnapshotSetEx</span><span class="sxs-lookup"><span data-stu-id="a5c1c-225">Breaking Shadow Copy Sets Using the BreakSnapshotSetEx Method</span></span>

<span data-ttu-id="a5c1c-226">En los siguientes ejemplos se muestra cómo usar la opción de línea de comandos **-BEX** .</span><span class="sxs-lookup"><span data-stu-id="a5c1c-226">The following examples show how to use the **-bex** command-line option.</span></span>

-   <span data-ttu-id="a5c1c-227">Especificar que el LUN de instantánea se enmascarará desde el host:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-227">Specifying that the shadow copy LUN will be masked from the host:</span></span>

    <span data-ttu-id="a5c1c-228">**vshadow** **-BEX** **-Mask**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-228">**vshadow** **-bex** **-mask**</span></span>

-   <span data-ttu-id="a5c1c-229">Especificar que el LUN de instantánea se exponga al host como un volumen de lectura/escritura:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-229">Specifying that the shadow copy LUN will be exposed to the host as a read/write volume:</span></span>

    <span data-ttu-id="a5c1c-230">**vshadow** **-BEX** **-RW**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-230">**vshadow** **-bex** **-rw**</span></span>

-   <span data-ttu-id="a5c1c-231">Especificar que el LUN de instantánea se exponga al host como un volumen de lectura y escritura, y que ninguna de las firmas de disco de los LUN de instantáneas se revertirá a la de los LUN originales:</span><span class="sxs-lookup"><span data-stu-id="a5c1c-231">Specifying that the shadow copy LUN will be exposed to the host as a read/write volume, and that none of the disk signatures on the shadow copy LUNs will be reverted to that of the original LUNs:</span></span>

    <span data-ttu-id="a5c1c-232">**vshadow** **-BEX** **-norevert**</span><span class="sxs-lookup"><span data-stu-id="a5c1c-232">**vshadow** **-bex** **-norevert**</span></span>

 

 
