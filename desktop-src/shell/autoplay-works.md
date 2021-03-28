---
description: La creación de una aplicación habilitada para AutoRun es un procedimiento sencillo. En este tema se usa un CD-ROM como ejemplo (era el primer medio para implementar esta tecnología), pero hoy en día hay muchos tipos de medios diferentes que pueden utilizarlo.
title: Creación de una aplicación AutoRun-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0d01f4a2-64c4-4b31-9fc9-361da6825ab8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 24a944b011c926d1638e5d0bcb0d35fc348e5783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153921"
---
# <a name="creating-an-autorun-enabled-application"></a><span data-ttu-id="89e71-104">Creación de una aplicación AutoRun-Enabled</span><span class="sxs-lookup"><span data-stu-id="89e71-104">Creating an AutoRun-Enabled Application</span></span>

<span data-ttu-id="89e71-105">La creación de una aplicación habilitada para AutoRun es un procedimiento sencillo.</span><span class="sxs-lookup"><span data-stu-id="89e71-105">Creating an AutoRun-enabled application is a straightforward procedure.</span></span> <span data-ttu-id="89e71-106">En este tema se usa un CD-ROM como ejemplo (era el primer medio para implementar esta tecnología), pero hoy en día hay muchos tipos de medios diferentes que pueden utilizarlo.</span><span class="sxs-lookup"><span data-stu-id="89e71-106">This topic uses CD-ROM as an example (it was the first medium to implement this technology) but today there are many different media types that can use it.</span></span>

<span data-ttu-id="89e71-107">Para habilitar la ejecución automática en la aplicación, solo tiene que incluir dos archivos esenciales:</span><span class="sxs-lookup"><span data-stu-id="89e71-107">To enable AutoRun in your application, you simply include two essential files:</span></span>

-   <span data-ttu-id="89e71-108">Un archivo Autorun. inf</span><span class="sxs-lookup"><span data-stu-id="89e71-108">An Autorun.inf file</span></span>
-   <span data-ttu-id="89e71-109">Una aplicación de inicio</span><span class="sxs-lookup"><span data-stu-id="89e71-109">A startup application</span></span>

<span data-ttu-id="89e71-110">Cuando un usuario inserta un disco en una unidad de CD-ROM en un equipo compatible con AutoRun, el sistema comprueba inmediatamente si el disco tiene un sistema de archivos de equipo personal.</span><span class="sxs-lookup"><span data-stu-id="89e71-110">When a user inserts a disc into a CD-ROM drive on a AutoRun-compatible computer, the system immediately checks to see if the disc has a personal computer file system.</span></span> <span data-ttu-id="89e71-111">Si es así, el sistema busca un archivo denominado [Autorun. inf](#creating-an-autoruninf-file).</span><span class="sxs-lookup"><span data-stu-id="89e71-111">If it does, the system searches for a file named [Autorun.inf](#creating-an-autoruninf-file).</span></span> <span data-ttu-id="89e71-112">Este archivo especifica una aplicación de instalación que se ejecutará, junto con una variedad de opciones de configuración opcionales.</span><span class="sxs-lookup"><span data-stu-id="89e71-112">This file specifies a setup application that will be run, along with a variety of optional settings.</span></span> <span data-ttu-id="89e71-113">Normalmente, la aplicación de inicio instala, desinstala, configura y quizás ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="89e71-113">The startup application typically installs, uninstalls, configures, and perhaps runs the application.</span></span>

-   [<span data-ttu-id="89e71-114">Crear un archivo Autorun. inf</span><span class="sxs-lookup"><span data-stu-id="89e71-114">Creating an Autorun.inf File</span></span>](#creating-an-autoruninf-file)
-   <span data-ttu-id="89e71-115">[La \[ \] sección DeviceInstall](#the-deviceinstall-section)</span><span class="sxs-lookup"><span data-stu-id="89e71-115">[The \[DeviceInstall\] Section](#the-deviceinstall-section)</span></span>
-   [<span data-ttu-id="89e71-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89e71-116">Related topics</span></span>](#related-topics)

## <a name="creating-an-autoruninf-file"></a><span data-ttu-id="89e71-117">Crear un archivo Autorun. inf</span><span class="sxs-lookup"><span data-stu-id="89e71-117">Creating an Autorun.inf File</span></span>

<span data-ttu-id="89e71-118">Autorun. inf es un archivo de texto que se encuentra en el directorio raíz del CD-ROM que contiene la aplicación.</span><span class="sxs-lookup"><span data-stu-id="89e71-118">Autorun.inf is a text file located in the root directory of the CD-ROM that contains your application.</span></span> <span data-ttu-id="89e71-119">Su función principal es proporcionar al sistema el nombre y la ubicación del programa de inicio de la aplicación que se ejecutará cuando se inserte el disco.</span><span class="sxs-lookup"><span data-stu-id="89e71-119">Its primary function is to provide the system with the name and location of the application's startup program that will be run when the disc is inserted.</span></span>

> [!Note]  
> <span data-ttu-id="89e71-120">Los archivos Autorun. inf no se admiten en Windows XP para las unidades que devuelven la unidad \_ extraíble desde [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).</span><span class="sxs-lookup"><span data-stu-id="89e71-120">Autorun.inf files are not supported under Windows XP for drives that return DRIVE\_REMOVABLE from [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).</span></span>

 

<span data-ttu-id="89e71-121">El archivo Autorun. inf también puede contener información opcional, como:</span><span class="sxs-lookup"><span data-stu-id="89e71-121">The Autorun.inf file can also contain optional information including:</span></span>

-   <span data-ttu-id="89e71-122">El nombre de un archivo que contiene un icono que representará la unidad de CD-ROM de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="89e71-122">The name of a file that contains an icon that will represent your application's CD-ROM drive.</span></span> <span data-ttu-id="89e71-123">Este icono se mostrará en el explorador de Windows en lugar del icono de la unidad estándar.</span><span class="sxs-lookup"><span data-stu-id="89e71-123">This icon will be displayed by Windows Explorer in place of the standard drive icon.</span></span>
-   <span data-ttu-id="89e71-124">Comandos adicionales para el menú contextual que se muestra cuando el usuario hace clic con el botón secundario en el icono de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="89e71-124">Additional commands for the shortcut menu that is displayed when the user right-clicks the CD-ROM icon.</span></span> <span data-ttu-id="89e71-125">También puede especificar el comando predeterminado que se ejecuta cuando el usuario hace doble clic en el icono.</span><span class="sxs-lookup"><span data-stu-id="89e71-125">You can also specify the default command that is run when the user double-clicks the icon.</span></span>

<span data-ttu-id="89e71-126">Los archivos Autorun. inf son similares a los archivos. ini.</span><span class="sxs-lookup"><span data-stu-id="89e71-126">Autorun.inf files are similar to .ini files.</span></span> <span data-ttu-id="89e71-127">Están formados por una o varias secciones, cada una con un nombre entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="89e71-127">They consist of one or more sections, each headed by a name enclosed in square brackets.</span></span> <span data-ttu-id="89e71-128">Cada sección contiene una serie de comandos que se ejecutarán en el shell cuando se inserte el disco.</span><span class="sxs-lookup"><span data-stu-id="89e71-128">Each section contains a series of commands that will be run by the Shell when the disc is inserted.</span></span> <span data-ttu-id="89e71-129">Hay dos secciones que están definidas actualmente para los archivos Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="89e71-129">There are two sections that are currently defined for Autorun.inf files.</span></span>

-   <span data-ttu-id="89e71-130">La sección **\[ ejecución automática \]** contiene los comandos de ejecución automática predeterminados.</span><span class="sxs-lookup"><span data-stu-id="89e71-130">The **\[autorun\]** section contains the default AutoRun commands.</span></span> <span data-ttu-id="89e71-131">Todos los archivos Autorun. inf deben tener una sección de **\[ ejecución automática \]** .</span><span class="sxs-lookup"><span data-stu-id="89e71-131">All Autorun.inf files must have an **\[autorun\]** section.</span></span>
-   <span data-ttu-id="89e71-132">Se puede incluir una sección opcional **\[ Autorun. alpha \]** para los sistemas que se ejecutan en equipos basados en RISC.</span><span class="sxs-lookup"><span data-stu-id="89e71-132">An optional **\[autorun.alpha\]** section can be included for systems running on RISC-based computers.</span></span> <span data-ttu-id="89e71-133">Cuando se inserta un disco en una unidad de CD-ROM en un sistema basado en RISC, el shell ejecutará los comandos de esta sección en lugar de los de la sección **\[ ejecución automática \]** .</span><span class="sxs-lookup"><span data-stu-id="89e71-133">When a disc is inserted in a CD-ROM drive on a RISC-based system, the Shell will run the commands in this section instead of those in the **\[autorun\]** section.</span></span>

> [!Note]  
> <span data-ttu-id="89e71-134">El shell comprueba primero una sección específica de la arquitectura.</span><span class="sxs-lookup"><span data-stu-id="89e71-134">The Shell checks for an architecture-specific section first.</span></span> <span data-ttu-id="89e71-135">Si no encuentra uno, usa la información de la sección **\[ ejecución automática \]** .</span><span class="sxs-lookup"><span data-stu-id="89e71-135">If it does not find one, it uses the information in the **\[autorun\]** section.</span></span> <span data-ttu-id="89e71-136">Una vez que el shell encuentra una sección, omite todas las demás, por lo que cada sección debe ser independiente.</span><span class="sxs-lookup"><span data-stu-id="89e71-136">After the Shell finds a section, it ignores all others, so each section must be self-contained.</span></span>

 

<span data-ttu-id="89e71-137">Cada sección contiene una serie de comandos que determinan cómo tiene lugar la operación de ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="89e71-137">Each section contains a series of commands that determine how the Autorun operation takes place.</span></span> <span data-ttu-id="89e71-138">Hay cinco comandos disponibles.</span><span class="sxs-lookup"><span data-stu-id="89e71-138">There are five commands available.</span></span>



| <span data-ttu-id="89e71-139">Get-Help</span><span class="sxs-lookup"><span data-stu-id="89e71-139">Command</span></span>                         | <span data-ttu-id="89e71-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="89e71-140">Description</span></span>                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="89e71-141">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="89e71-141">defaulticon</span></span>](autorun-cmds.md) | <span data-ttu-id="89e71-142">Especifica el icono predeterminado para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="89e71-142">Specifies the default icon for the application.</span></span>                                        |
| [<span data-ttu-id="89e71-143">icono</span><span class="sxs-lookup"><span data-stu-id="89e71-143">icon</span></span>](autorun-cmds.md)        | <span data-ttu-id="89e71-144">Especifica la ruta de acceso y el nombre de un icono específico de la aplicación para la unidad de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="89e71-144">Specifies the path and file name of an application-specific icon for the CD-ROM drive.</span></span> |
| [<span data-ttu-id="89e71-145">open</span><span class="sxs-lookup"><span data-stu-id="89e71-145">open</span></span>](autorun-cmds.md)        | <span data-ttu-id="89e71-146">Especifica la ruta de acceso y el nombre de archivo de la aplicación de inicio.</span><span class="sxs-lookup"><span data-stu-id="89e71-146">Specifies the path and file name of the startup application.</span></span>                           |
| [<span data-ttu-id="89e71-147">useautorun</span><span class="sxs-lookup"><span data-stu-id="89e71-147">useautorun</span></span>](autorun-cmds.md)  | <span data-ttu-id="89e71-148">Especifica que se deben usar las características de reproducción de reproducción V2 si se admiten.</span><span class="sxs-lookup"><span data-stu-id="89e71-148">Specifies that Autoplay V2 features should be used if supported.</span></span>                       |
| [<span data-ttu-id="89e71-149">interfaz</span><span class="sxs-lookup"><span data-stu-id="89e71-149">shell</span></span>](autorun-cmds.md)       | <span data-ttu-id="89e71-150">Define el comando predeterminado en el menú contextual del CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="89e71-150">Defines the default command in the CD-ROM's shortcut menu.</span></span>                             |
| [<span data-ttu-id="89e71-151">verbo de Shell \_</span><span class="sxs-lookup"><span data-stu-id="89e71-151">shell\_verb</span></span>](autorun-cmds.md) | <span data-ttu-id="89e71-152">Agrega comandos al menú contextual del CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="89e71-152">Adds commands to the CD-ROM's shortcut menu.</span></span>                                           |



 

<span data-ttu-id="89e71-153">El siguiente es un ejemplo de un archivo Autorun. inf simple.</span><span class="sxs-lookup"><span data-stu-id="89e71-153">The following is an example of a simple Autorun.inf file.</span></span> <span data-ttu-id="89e71-154">Especifica Filename.exe como aplicación de inicio.</span><span class="sxs-lookup"><span data-stu-id="89e71-154">It specifies Filename.exe as the startup application.</span></span> <span data-ttu-id="89e71-155">El segundo icono de Filename.exe representará la unidad de CD-ROM en lugar del icono de la unidad estándar.</span><span class="sxs-lookup"><span data-stu-id="89e71-155">The second icon in Filename.exe will represent the CD-ROM drive instead of the standard drive icon.</span></span>


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



<span data-ttu-id="89e71-156">Este ejemplo Autorun. inf ejecuta diferentes aplicaciones de inicio en función del tipo de equipo.</span><span class="sxs-lookup"><span data-stu-id="89e71-156">This Autorun.inf sample runs different startup applications depending on the type of computer.</span></span>


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a><span data-ttu-id="89e71-157">La \[ \] sección DeviceInstall</span><span class="sxs-lookup"><span data-stu-id="89e71-157">The \[DeviceInstall\] Section</span></span>

<span data-ttu-id="89e71-158">Puede usar la sección **\[ DeviceInstall \]** en cualquier medio extraíble.</span><span class="sxs-lookup"><span data-stu-id="89e71-158">You can use the **\[DeviceInstall\]** section on any removable media.</span></span> <span data-ttu-id="89e71-159">Solo se admite en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="89e71-159">It is supported only under Windows XP.</span></span> <span data-ttu-id="89e71-160">Use **DriverPath** para especificar una ruta de acceso de directorio en la que Windows XP busca archivos de controlador, lo que evita una búsqueda larga en todo el contenido.</span><span class="sxs-lookup"><span data-stu-id="89e71-160">You use **DriverPath** to specify a directory path where Windows XP searches for driver files, which prevents a lengthy search through the entire contents.</span></span>

<span data-ttu-id="89e71-161">Use la sección **\[ DeviceInstall \]** con una instalación de controlador para especificar los directorios en los que Windows XP debe buscar los archivos de controlador.</span><span class="sxs-lookup"><span data-stu-id="89e71-161">You use the **\[DeviceInstall\]** section with a driver installation to specify directories where Windows XP should search the media for driver files.</span></span> <span data-ttu-id="89e71-162">En Windows XP, ya no se busca en todo el medio de forma predeterminada, por lo que se requiere **\[ DeviceInstall \]** para especificar ubicaciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="89e71-162">Under Windows XP, entire media are no longer searched by default, therefore requiring **\[DeviceInstall\]** to specify search locations.</span></span> <span data-ttu-id="89e71-163">A continuación se muestran los únicos medios extraíbles que Windows XP realiza búsquedas por completo sin una sección **\[ DeviceInstall \]** en un archivo Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="89e71-163">The following are the only removable media that Windows XP fully searches without a **\[DeviceInstall\]** section in an Autorun.inf file.</span></span>

-   <span data-ttu-id="89e71-164">Disquetes encontrados en las unidades A o B.</span><span class="sxs-lookup"><span data-stu-id="89e71-164">Floppy disks found in drives A or B.</span></span>
-   <span data-ttu-id="89e71-165">Los medios de CD/DVD tienen menos de 1 Gigabyte (GB) de tamaño.</span><span class="sxs-lookup"><span data-stu-id="89e71-165">CD/DVD media less that 1 gigabyte (GB) in size.</span></span>

<span data-ttu-id="89e71-166">Todos los demás medios deben incluir una sección **\[ DeviceInstall \]** para que Windows XP detecte los controladores almacenados en ese medio.</span><span class="sxs-lookup"><span data-stu-id="89e71-166">All other media must include a **\[DeviceInstall\]** section for Windows XP to detect any drivers stored on that media.</span></span>

> [!Note]  
> <span data-ttu-id="89e71-167">Al igual que con la sección de **\[ ejecución automática \]** , la sección **\[ DeviceInstall \]** puede ser específica de la arquitectura.</span><span class="sxs-lookup"><span data-stu-id="89e71-167">As with the **\[AutoRun\]** section, the **\[DeviceInstall\]** section can be architecture-specific.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="89e71-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89e71-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89e71-169">Cómo implementar aplicaciones de inicio de ejecución automática</span><span class="sxs-lookup"><span data-stu-id="89e71-169">How to Implement Autorun Startup Applications</span></span>](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[<span data-ttu-id="89e71-170">Escritura de una aplicación de instalación de dispositivos</span><span class="sxs-lookup"><span data-stu-id="89e71-170">Writing a Device Installation Application</span></span>](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
