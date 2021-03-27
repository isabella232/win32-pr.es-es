---
description: En este tema se describe el modo en que las aplicaciones pueden exponer información sobre ellos mismos necesarios para habilitar determinados escenarios.
ms.assetid: F88AA3E6-6F7B-442d-935A-7D2CB4958E6B
title: Registro de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857e96893d2fe717f1a4939d06c77af043ead318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000991"
---
# <a name="application-registration"></a><span data-ttu-id="8245f-103">Registro de la aplicación</span><span class="sxs-lookup"><span data-stu-id="8245f-103">Application Registration</span></span>

<span data-ttu-id="8245f-104">En este tema se describe el modo en que las aplicaciones pueden exponer información sobre ellos mismos necesarios para habilitar determinados escenarios.</span><span class="sxs-lookup"><span data-stu-id="8245f-104">This topic discusses how applications can expose information about themselves necessary to enable certain scenarios.</span></span> <span data-ttu-id="8245f-105">Esto incluye la información necesaria para localizar la aplicación, los verbos que admite la aplicación y los tipos de archivos que puede controlar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8245f-105">This includes information needed to locate the application, the verbs that the application supports and the types of files that an application can handle.</span></span>

<span data-ttu-id="8245f-106">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8245f-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="8245f-107">Buscar un archivo ejecutable de aplicación</span><span class="sxs-lookup"><span data-stu-id="8245f-107">Finding an Application Executable</span></span>](#finding-an-application-executable)
-   [<span data-ttu-id="8245f-108">Registro de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8245f-108">Registering Applications</span></span>](#registering-applications)
    -   [<span data-ttu-id="8245f-109">Usar la subclave de rutas de acceso de la aplicación</span><span class="sxs-lookup"><span data-stu-id="8245f-109">Using the App Paths Subkey</span></span>](#using-the-app-paths-subkey)
    -   [<span data-ttu-id="8245f-110">Usar la subclave Applications</span><span class="sxs-lookup"><span data-stu-id="8245f-110">Using the Applications Subkey</span></span>](#using-the-applications-subkey)
-   [<span data-ttu-id="8245f-111">Registrar verbos y otra información de Asociación de archivos</span><span class="sxs-lookup"><span data-stu-id="8245f-111">Registering Verbs and Other File Association Information</span></span>](#registering-verbs-and-other-file-association-information)
-   [<span data-ttu-id="8245f-112">Registrar un tipo percibido</span><span class="sxs-lookup"><span data-stu-id="8245f-112">Registering a Perceived Type</span></span>](#registering-a-perceived-type)
-   [<span data-ttu-id="8245f-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8245f-113">Related topics</span></span>](#related-topics)

> [!Note]  
> <span data-ttu-id="8245f-114">Las aplicaciones también pueden registrarse en las aplicaciones configurar el acceso y los valores predeterminados del equipo (SPAD) y establecer programas predeterminados (SYDP) del panel de control.</span><span class="sxs-lookup"><span data-stu-id="8245f-114">Applications can also be registered in the Set Program Access and Computer Defaults (SPAD) and Set Your Default Programs (SYDP) control panel applications.</span></span> <span data-ttu-id="8245f-115">Para obtener información acerca del registro de aplicaciones de SPAD y SYDP, consulte [directrices para asociaciones de archivos y programas predeterminados](appguide-fa-defpro.md), y [establecer el acceso a programas y los valores predeterminados del equipo (SPAD)](cpl-setprogramaccess.md).</span><span class="sxs-lookup"><span data-stu-id="8245f-115">For information about SPAD and SYDP application registration, see [Guidelines for File Associations and Default Programs](appguide-fa-defpro.md), and [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md).</span></span>

 

## <a name="finding-an-application-executable"></a><span data-ttu-id="8245f-116">Buscar un archivo ejecutable de aplicación</span><span class="sxs-lookup"><span data-stu-id="8245f-116">Finding an Application Executable</span></span>

<span data-ttu-id="8245f-117">Cuando se llama a la función [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) con el nombre de un archivo ejecutable en su parámetro *lpFile* , hay varios lugares en los que la función busca el archivo.</span><span class="sxs-lookup"><span data-stu-id="8245f-117">When the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called with the name of an executable file in its *lpFile* parameter, there are several places where the function looks for the file.</span></span> <span data-ttu-id="8245f-118">Se recomienda registrar la aplicación en la subclave del registro de rutas de acceso de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="8245f-118">We recommend registering your application in the **App Paths** registry subkey.</span></span> <span data-ttu-id="8245f-119">Al hacerlo, se evita la necesidad de que las aplicaciones modifiquen la variable de entorno de la ruta de acceso del sistema.</span><span class="sxs-lookup"><span data-stu-id="8245f-119">Doing so avoids the need for applications to modify the system PATH environment variable.</span></span>

<span data-ttu-id="8245f-120">El archivo se busca en las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="8245f-120">The file is sought in the following locations:</span></span>

-   <span data-ttu-id="8245f-121">El directorio de trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="8245f-121">The current working directory.</span></span>
-   <span data-ttu-id="8245f-122">Solo el directorio de **Windows** (no se busca ningún subdirectorio).</span><span class="sxs-lookup"><span data-stu-id="8245f-122">The **Windows** directory only (no subdirectories are searched).</span></span>
-   <span data-ttu-id="8245f-123">Directorio **\\ system32 de Windows** .</span><span class="sxs-lookup"><span data-stu-id="8245f-123">The **Windows\\System32** directory.</span></span>
-   <span data-ttu-id="8245f-124">Directorios enumerados en la variable de entorno PATH.</span><span class="sxs-lookup"><span data-stu-id="8245f-124">Directories listed in the PATH environment variable.</span></span>
-   <span data-ttu-id="8245f-125">Recomendado: **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App paths**</span><span class="sxs-lookup"><span data-stu-id="8245f-125">Recommended: **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**</span></span>

## <a name="registering-applications"></a><span data-ttu-id="8245f-126">Registro de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8245f-126">Registering Applications</span></span>

<span data-ttu-id="8245f-127">Las subclaves del registro de **aplicaciones** y rutas de acceso de la **aplicación** se usan para registrar y controlar el comportamiento del sistema en nombre de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8245f-127">Both the **App Paths** and **Applications** registry subkeys are used to register and control the behavior of the system on behalf of applications.</span></span> <span data-ttu-id="8245f-128">La subclave de rutas de acceso de la **aplicación** es la ubicación preferida.</span><span class="sxs-lookup"><span data-stu-id="8245f-128">The **App Paths** subkey is the preferred location.</span></span>

### <a name="using-the-app-paths-subkey"></a><span data-ttu-id="8245f-129">Usar la subclave de rutas de acceso de la aplicación</span><span class="sxs-lookup"><span data-stu-id="8245f-129">Using the App Paths Subkey</span></span>

<span data-ttu-id="8245f-130">En Windows 7 y versiones posteriores, se recomienda encarecidamente instalar aplicaciones por usuario en lugar de por equipo.</span><span class="sxs-lookup"><span data-stu-id="8245f-130">In Windows 7 and later, we strongly recommend you install applications per user rather than per machine.</span></span> <span data-ttu-id="8245f-131">Una aplicación que se instala para por usuario puede registrarse en **HKEY \_ Current \_ User** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App paths**.</span><span class="sxs-lookup"><span data-stu-id="8245f-131">An application that is installed for per user can be registered under **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**.</span></span> <span data-ttu-id="8245f-132">Una aplicación que se instala para todos los usuarios del equipo se puede registrar en **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App paths**.</span><span class="sxs-lookup"><span data-stu-id="8245f-132">An application that is installed for all users of the computer can be registered under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**.</span></span>

<span data-ttu-id="8245f-133">Las entradas que se encuentran en rutas de acceso de la **aplicación** se usan principalmente para los siguientes fines:</span><span class="sxs-lookup"><span data-stu-id="8245f-133">The entries found under **App Paths** are used primarily for the following purposes:</span></span>

-   <span data-ttu-id="8245f-134">Para asignar el nombre del archivo ejecutable de una aplicación a la ruta de acceso completa del archivo.</span><span class="sxs-lookup"><span data-stu-id="8245f-134">To map an application's executable file name to that file's fully qualified path.</span></span>
-   <span data-ttu-id="8245f-135">Para dejar pendiente la información en la variable de entorno PATH por aplicación y por proceso.</span><span class="sxs-lookup"><span data-stu-id="8245f-135">To pre-pend information to the PATH environment variable on a per-application, per-process basis.</span></span>

<span data-ttu-id="8245f-136">Si el nombre de una subclave de rutas de acceso de la **aplicación** coincide con el nombre de archivo, el shell realiza dos acciones:</span><span class="sxs-lookup"><span data-stu-id="8245f-136">If the name of a subkey of **App Paths** matches the file name, the Shell performs two actions:</span></span>

-   <span data-ttu-id="8245f-137">La entrada (predeterminada) se usa como ruta de acceso completa del archivo.</span><span class="sxs-lookup"><span data-stu-id="8245f-137">The (Default) entry is used as the file's fully qualified path.</span></span>
-   <span data-ttu-id="8245f-138">La entrada de la ruta de acceso de la subclave se antepone a la variable de entorno PATH de ese proceso.</span><span class="sxs-lookup"><span data-stu-id="8245f-138">The Path entry for that subkey is pre-pended to the PATH environment variable of that process.</span></span> <span data-ttu-id="8245f-139">Si no es necesario, se puede omitir el valor de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="8245f-139">If this is not required, the Path value can be omitted.</span></span>

<span data-ttu-id="8245f-140">Los posibles problemas que se deben tener en cuenta son:</span><span class="sxs-lookup"><span data-stu-id="8245f-140">Potential issues to be aware of include:</span></span>

-   <span data-ttu-id="8245f-141">El shell limita la longitud de una línea de comandos a la ruta de acceso máxima de \_ \* 2 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8245f-141">The Shell limits the length of a command line to MAX\_PATH \* 2 characters.</span></span> <span data-ttu-id="8245f-142">Si hay muchos archivos enumerados como entradas del registro o sus rutas de acceso son largas, los nombres de archivo que se encuentran más adelante en la lista podrían perderse mientras se trunca la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="8245f-142">If there are many files listed as registry entries or their paths are long, file names later in the list could be lost as the command line is truncated.</span></span>
-   <span data-ttu-id="8245f-143">Algunas aplicaciones no aceptan varios nombres de archivo en una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="8245f-143">Some applications do not accept multiple file names in a command line.</span></span>
-   <span data-ttu-id="8245f-144">Algunas aplicaciones que aceptan varios nombres de archivo no reconocen el formato en el que el Shell las proporciona.</span><span class="sxs-lookup"><span data-stu-id="8245f-144">Some applications that accept multiple file names do not recognize the format in which the Shell provides them.</span></span> <span data-ttu-id="8245f-145">El Shell proporciona la lista de parámetros como una cadena entrecomillada, pero algunas aplicaciones pueden requerir cadenas sin comillas.</span><span class="sxs-lookup"><span data-stu-id="8245f-145">The Shell provides the parameter list as a quoted string, but some applications might require strings without quotes.</span></span>
-   <span data-ttu-id="8245f-146">No todos los elementos que se pueden arrastrar son parte del sistema de archivos; por ejemplo, impresoras.</span><span class="sxs-lookup"><span data-stu-id="8245f-146">Not all items that can be dragged are part of the file system; for example, printers.</span></span> <span data-ttu-id="8245f-147">Estos elementos no tienen una ruta de acceso de Win32 estándar, por lo que no hay ninguna manera de proporcionar un valor de *lpParameters* significativo a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="8245f-147">These items do not have a standard Win32 path, so there is no way to provide a meaningful *lpParameters* value to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="8245f-148">El uso de la entrada DropTarget evita estos posibles problemas al proporcionar acceso a todos los formatos del portapapeles, incluido [CFSTR \_ SHELLIDLIST](clipboard.md) (para las listas de archivos largos) y [CFSTR \_ FILECONTENTS](clipboard.md) (para los objetos que no son del sistema de archivos).</span><span class="sxs-lookup"><span data-stu-id="8245f-148">Using the DropTarget entry avoids these potential issues by providing access to all of the clipboard formats, including [CFSTR\_SHELLIDLIST](clipboard.md) (for long file lists) and [CFSTR\_FILECONTENTS](clipboard.md) (for non-file-system objects).</span></span>

<span data-ttu-id="8245f-149">**Para registrar y controlar el comportamiento de las aplicaciones con la subclave de rutas de acceso de la aplicación**:</span><span class="sxs-lookup"><span data-stu-id="8245f-149">**To register and control the behavior of your applications with the App Paths subkey**:</span></span>

1.  <span data-ttu-id="8245f-150">Agregue una subclave con el mismo nombre que el archivo ejecutable a la subclave de rutas de acceso de la **aplicación** , tal como se muestra en la siguiente entrada del registro.</span><span class="sxs-lookup"><span data-stu-id="8245f-150">Add a subkey with the same name as your executable file to the **App Paths** subkey, as shown in the following registry entry.</span></span>

    ```
    HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   App Paths
                      file.exe
                         (Default)
                         DontUseDesktopChangeRouter
                         DropTarget
                         Path
                         UseUrl
    ```

2.  <span data-ttu-id="8245f-151">Vea la tabla siguiente para obtener detalles de las entradas de la subclave **paths de aplicación** .</span><span class="sxs-lookup"><span data-stu-id="8245f-151">See the following table for details of the **App Paths** subkey entries.</span></span> 

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="8245f-152">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="8245f-152">Registry entry</span></span></th>
    <th><span data-ttu-id="8245f-153">Detalles</span><span class="sxs-lookup"><span data-stu-id="8245f-153">Details</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="8245f-154">(Es el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="8245f-154">(Default)</span></span></td>
    <td><span data-ttu-id="8245f-155">Es la ruta de acceso completa a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8245f-155">Is the fully qualified path to the application.</span></span> <span data-ttu-id="8245f-156">El nombre de la aplicación proporcionado en la entrada (valor predeterminado) se puede indicar con o sin la extensión. exe.</span><span class="sxs-lookup"><span data-stu-id="8245f-156">The application name provided in the (Default) entry can be stated with or without its .exe extension.</span></span> <span data-ttu-id="8245f-157">Si es necesario, la función <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> agrega la extensión al buscar la subclave de rutas de acceso de la <strong>aplicación</strong> .</span><span class="sxs-lookup"><span data-stu-id="8245f-157">If necessary, the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> function adds the extension when searching <strong>App Paths</strong> subkey.</span></span> <span data-ttu-id="8245f-158">La entrada es del tipo de <strong>REG_SZ</strong> .</span><span class="sxs-lookup"><span data-stu-id="8245f-158">The entry is of the <strong>REG_SZ</strong> type.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="8245f-159">DontUseDesktopChangeRouter</span><span class="sxs-lookup"><span data-stu-id="8245f-159">DontUseDesktopChangeRouter</span></span></td>
    <td><span data-ttu-id="8245f-160">Es obligatorio para que las aplicaciones del depurador eviten los interbloqueos del cuadro de diálogo de archivo al depurar el proceso del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="8245f-160">Is mandatory for debugger applications to avoid file dialog deadlocks when debugging the Windows Explorer process.</span></span> <span data-ttu-id="8245f-161">Sin embargo, el establecimiento de la entrada DontUseDesktopChangeRouter produce un control ligeramente menos eficaz de las notificaciones de cambios.</span><span class="sxs-lookup"><span data-stu-id="8245f-161">Setting the DontUseDesktopChangeRouter entry produces a slightly less efficient handling of the change notifications, however.</span></span> <span data-ttu-id="8245f-162">La entrada es del tipo <strong>REG_DWORD</strong> y el valor es 0x1.</span><span class="sxs-lookup"><span data-stu-id="8245f-162">The entry is of the <strong>REG_DWORD</strong> type and the value is 0x1.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="8245f-163">DropTarget</span><span class="sxs-lookup"><span data-stu-id="8245f-163">DropTarget</span></span></td>
    <td><span data-ttu-id="8245f-164">Es un identificador de clase (CLSID).</span><span class="sxs-lookup"><span data-stu-id="8245f-164">Is a class identifier (CLSID).</span></span> <span data-ttu-id="8245f-165">La entrada DropTarget contiene el CLSID de un objeto (normalmente un servidor local en lugar de un servidor en proceso) que implementa <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8245f-165">The DropTarget entry contains the CLSID of an object (usually a local server rather than an in-process server) that implements <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>.</span></span> <span data-ttu-id="8245f-166">De forma predeterminada, cuando el destino de colocación es un archivo ejecutable y no se proporciona ningún valor de DropTarget, el shell convierte la lista de archivos colocados en un parámetro de línea de comandos y lo pasa a <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> a través de <em>lpParameters</em>.</span><span class="sxs-lookup"><span data-stu-id="8245f-166">By default, when the drop target is an executable file, and no DropTarget value is provided, the Shell converts the list of dropped files into a command-line parameter and passes it to <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> through <em>lpParameters</em>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="8245f-167">Ruta</span><span class="sxs-lookup"><span data-stu-id="8245f-167">Path</span></span></td>
    <td><span data-ttu-id="8245f-168">Proporciona una cadena (en forma de lista de directorios separados por punto y coma) para anexar a la variable de entorno PATH cuando se inicia una aplicación mediante una llamada a <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8245f-168">Supplies a string (in the form of a semicolon-separated list of directories) to append to the PATH environment variable when an application is launched by calling <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.</span></span> <span data-ttu-id="8245f-169">Es la ruta de acceso completa al archivo. exe.</span><span class="sxs-lookup"><span data-stu-id="8245f-169">It is the fully qualified path to the .exe.</span></span> <span data-ttu-id="8245f-170">Es de <strong>REG_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="8245f-170">It is of <strong>REG_SZ</strong>.</span></span> <span data-ttu-id="8245f-171">En <strong>Windows 7 y versiones posteriores</strong>, el tipo se puede <strong>REG_EXPAND_SZ</strong>y suele ser <strong>REG_EXPAND_SZ</strong> % ProgramFiles%.</span><span class="sxs-lookup"><span data-stu-id="8245f-171">In <strong>Windows 7 and later</strong>, the type can be <strong>REG_EXPAND_SZ</strong>, and is commonly <strong>REG_EXPAND_SZ</strong> %ProgramFiles%.</span></span>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="8245f-172">Además de las entradas (default), path y DropTarget reconocidas por el Shell, una aplicación también puede agregar valores personalizados a la subclave de las <strong>rutas</strong> de acceso de la aplicación de su archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="8245f-172">In addition to the (Default), Path, and DropTarget entries recognized by the Shell, an application can also add custom values to its executable file's <strong>App Paths</strong> subkey.</span></span> <span data-ttu-id="8245f-173">Se recomienda a los desarrolladores de aplicaciones que usen la subclave <strong>App paths</strong> para proporcionar una ruta de acceso específica de la aplicación en lugar de realizar adiciones a la ruta de acceso global del sistema.</span><span class="sxs-lookup"><span data-stu-id="8245f-173">We encourage application developers to use the <strong>App Paths</strong> subkey to provide an application-specific path instead of making additions to the global system path.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="8245f-174">SupportedProtocols</span><span class="sxs-lookup"><span data-stu-id="8245f-174">SupportedProtocols</span></span></td>
    <td><span data-ttu-id="8245f-175">Crea una cadena que contiene los esquemas de protocolo de dirección URL para una clave determinada.</span><span class="sxs-lookup"><span data-stu-id="8245f-175">Creates a string that contains the URL protocol schemes for a given key.</span></span> <span data-ttu-id="8245f-176">Puede contener varios valores del registro para indicar qué esquemas se admiten.</span><span class="sxs-lookup"><span data-stu-id="8245f-176">This can contain multiple registry values to indicate which schemes are supported.</span></span> <span data-ttu-id="8245f-177">Esta cadena sigue el formato de <strong>scheme1: scheme2</strong>.</span><span class="sxs-lookup"><span data-stu-id="8245f-177">This string follows the format of <strong>scheme1:scheme2</strong>.</span></span> <span data-ttu-id="8245f-178">Si esta lista no está vacía, se agregará <strong>File:</strong> a la cadena.</span><span class="sxs-lookup"><span data-stu-id="8245f-178">If this list is not empty, <strong>file:</strong> will be added to the string.</span></span> <span data-ttu-id="8245f-179">Este protocolo se admite implícitamente cuando se define <em>SupportedProtocols</em> .</span><span class="sxs-lookup"><span data-stu-id="8245f-179">This protocol is implicitly supported when <em>SupportedProtocols</em> is defined.</span></span> <br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="8245f-180">UseUrl</span><span class="sxs-lookup"><span data-stu-id="8245f-180">UseUrl</span></span></td>
    <td><span data-ttu-id="8245f-181">Indica que la aplicación puede aceptar una dirección URL (en lugar de un nombre de archivo) en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="8245f-181">Indicates that your application can accept a URL (instead of a file name) on the command line.</span></span> <span data-ttu-id="8245f-182">Las aplicaciones que pueden abrir documentos directamente desde Internet, como los exploradores Web y los reproductores multimedia, deben establecer esta entrada.</span><span class="sxs-lookup"><span data-stu-id="8245f-182">Applications that can open documents directly from the internet, like web browsers and media players, should set this entry.</span></span> <br/> <span data-ttu-id="8245f-183">Cuando la función <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> inicia una aplicación y no se establece el valor UseUrl = 1, <strong>ShellExecuteEx</strong> descarga el documento en un archivo local e invoca el controlador en la copia local.</span><span class="sxs-lookup"><span data-stu-id="8245f-183">When the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> function starts an application and the UseUrl=1 value is not set, <strong>ShellExecuteEx</strong> downloads the document to a local file and invokes the handler on the local copy.</span></span><br/> <span data-ttu-id="8245f-184">Por ejemplo, si la aplicación tiene este conjunto de entrada y un usuario hace clic con el botón secundario en un archivo almacenado en un servidor Web, el verbo abierto estará disponible.</span><span class="sxs-lookup"><span data-stu-id="8245f-184">For example, if the application has this entry set and a user right-clicks on a file stored on a web server, the Open verb will be made available.</span></span> <span data-ttu-id="8245f-185">Si no es así, el usuario tendrá que descargar el archivo y abrir la copia local.</span><span class="sxs-lookup"><span data-stu-id="8245f-185">If not, the user will have to download the file and open the local copy.</span></span> <br/> <span data-ttu-id="8245f-186">La entrada UseUrl es de <strong>REG_DWORD</strong> tipo y el valor es 0x1.</span><span class="sxs-lookup"><span data-stu-id="8245f-186">The UseUrl entry is of <strong>REG_DWORD</strong> type, and the value is 0x1.</span></span><br/> <span data-ttu-id="8245f-187">En Windows Vista y versiones anteriores, esta entrada indicaba que la dirección URL se debe pasar a la aplicación junto con un nombre de archivo local, cuando se llama a través de ShellExecuteEx.</span><span class="sxs-lookup"><span data-stu-id="8245f-187">In Windows Vista and earlier, this entry indicated that the URL should be passed to the application along with a local file name, when called via ShellExecuteEx.</span></span> <span data-ttu-id="8245f-188">En Windows 7, indica que la aplicación puede comprender cualquier dirección URL http o https que se le pase, sin tener que proporcionar también el nombre del archivo de caché.</span><span class="sxs-lookup"><span data-stu-id="8245f-188">In Windows 7, it indicates that the application can understand any http or https url that is passed to it, without having to supply the cache file name as well.</span></span> <span data-ttu-id="8245f-189">Esta clave del registro está asociada a la clave <em>SupportedProtocols</em> .</span><span class="sxs-lookup"><span data-stu-id="8245f-189">This registry key is associated with the <em>SupportedProtocols</em> key.</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

### <a name="using-the-applications-subkey"></a><span data-ttu-id="8245f-190">Usar la subclave Applications</span><span class="sxs-lookup"><span data-stu-id="8245f-190">Using the Applications Subkey</span></span>

<span data-ttu-id="8245f-191">A través de la inclusión de entradas del registro en la subclave **HKEY \_ classes \_ root** \\ **Applications** \\ *ApplicationName.exe* , las aplicaciones pueden proporcionar la información específica de la aplicación que se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8245f-191">Through the inclusion of registry entries under the **HKEY\_CLASSES\_ROOT**\\**Applications**\\*ApplicationName.exe* subkey, applications can provide the application-specific information shown in the following table.</span></span>



| <span data-ttu-id="8245f-192">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="8245f-192">Registry entry</span></span>                   | <span data-ttu-id="8245f-193">Descripción</span><span class="sxs-lookup"><span data-stu-id="8245f-193">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8245f-194">verbo de Shell \\</span><span class="sxs-lookup"><span data-stu-id="8245f-194">shell\\verb</span></span>                      | <span data-ttu-id="8245f-195">Proporciona el método de verbo para llamar a la aplicación desde OpenWith.</span><span class="sxs-lookup"><span data-stu-id="8245f-195">Provides the verb method for calling the application from OpenWith.</span></span> <span data-ttu-id="8245f-196">Sin una definición de verbo especificada aquí, el sistema supone que la aplicación admite [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)y pasa el nombre de archivo en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="8245f-196">Without a verb definition specified here, the system assumes that the application supports [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa), and passes the file name on the command line.</span></span> <span data-ttu-id="8245f-197">Esta funcionalidad se aplica a todos los métodos de verbo, incluidos DropTarget, ExecuteCommand y Intercambio dinámico de datos (DDE).</span><span class="sxs-lookup"><span data-stu-id="8245f-197">This functionality applies to all the verb methods, including DropTarget, ExecuteCommand, and Dynamic Data Exchange (DDE).</span></span>                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="8245f-198">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="8245f-198">DefaultIcon</span></span>                      | <span data-ttu-id="8245f-199">Permite a una aplicación proporcionar un icono específico para representar la aplicación en lugar del primer icono almacenado en el archivo. exe.</span><span class="sxs-lookup"><span data-stu-id="8245f-199">Enables an application to provide a specific icon to represent the application instead of the first icon stored in the .exe file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="8245f-200">FriendlyAppName</span><span class="sxs-lookup"><span data-stu-id="8245f-200">FriendlyAppName</span></span>                  | <span data-ttu-id="8245f-201">Proporciona una manera de obtener un nombre traducible para mostrarlo en una aplicación, en lugar de solo la información de versión que aparece, que puede no ser localizable.</span><span class="sxs-lookup"><span data-stu-id="8245f-201">Provides a way to get a localizable name to display for an application instead of just the version information appearing, which may not be localizable.</span></span> <span data-ttu-id="8245f-202">La consulta de asociación [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) Lee este valor de entrada del registro y revierte a usar el nombre de FileDescription en la información de versión.</span><span class="sxs-lookup"><span data-stu-id="8245f-202">The association query [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) reads this registry entry value and falls back to use the FileDescription name in the version information.</span></span> <span data-ttu-id="8245f-203">Si falta ese nombre, la consulta de asociación tiene como valor predeterminado el nombre para mostrar del archivo.</span><span class="sxs-lookup"><span data-stu-id="8245f-203">If that name is missing, the association query defaults to the display name of the file.</span></span> <span data-ttu-id="8245f-204">Las aplicaciones deben usar **ASSOCSTR \_ FRIENDLYAPPNAME** para recuperar esta información con el fin de obtener el comportamiento correcto.</span><span class="sxs-lookup"><span data-stu-id="8245f-204">Applications should use **ASSOCSTR\_FRIENDLYAPPNAME** to retrieve this information to obtain the proper behavior.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="8245f-205">SupportedTypes</span><span class="sxs-lookup"><span data-stu-id="8245f-205">SupportedTypes</span></span>                   | <span data-ttu-id="8245f-206">Enumera los tipos de archivo que admite la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8245f-206">Lists the file types that the application supports.</span></span> <span data-ttu-id="8245f-207">Esto permite que la aplicación se muestre en el menú en cascada del cuadro de diálogo **abrir con** .</span><span class="sxs-lookup"><span data-stu-id="8245f-207">Doing so enables the application to be listed in the cascade menu of the **Open with** dialog box.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8245f-208">NoOpenWith</span><span class="sxs-lookup"><span data-stu-id="8245f-208">NoOpenWith</span></span>                       | <span data-ttu-id="8245f-209">Indica que no se ha especificado ninguna aplicación para abrir este tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="8245f-209">Indicates that no application is specified for opening this file type.</span></span> <span data-ttu-id="8245f-210">Tenga en cuenta que si se ha establecido una subclave OpenWithProgIDs para una aplicación por tipo de archivo, y la propia subclave ProgID no tiene también una entrada NoOpenWith, esa aplicación aparecerá en la lista de aplicaciones recomendadas o disponibles incluso si se ha especificado la entrada NoOpenWith.</span><span class="sxs-lookup"><span data-stu-id="8245f-210">Be aware that if an OpenWithProgIDs subkey has been set for an application by file type, and the ProgID subkey itself does not also have a NoOpenWith entry, that application will appear in the list of recommended or available applications even if it has specified the NoOpenWith entry.</span></span> <span data-ttu-id="8245f-211">Para obtener más información, vea cómo [incluir una aplicación en el cuadro de diálogo Abrir con](how-to-include-an-application-on-the-open-with-dialog-box.md) y [Cómo excluir una aplicación del cuadro de diálogo Abrir con](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="8245f-211">For more information, see [How to How to Include an Application in the Open With Dialog Box](how-to-include-an-application-on-the-open-with-dialog-box.md) and [How to exclude an Application from the Open with Dialog Box](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).</span></span><br/> |
| <span data-ttu-id="8245f-212">IsHostApp</span><span class="sxs-lookup"><span data-stu-id="8245f-212">IsHostApp</span></span>                        | <span data-ttu-id="8245f-213">Indica que el proceso es un proceso de host, como Rundll32.exe o Dllhost.exe, y no debe tenerse en cuenta para el anclaje o la inclusión del menú **Inicio** en la lista de usados con mayor frecuencia (MFU).</span><span class="sxs-lookup"><span data-stu-id="8245f-213">Indicates that the process is a host process, such as Rundll32.exe or Dllhost.exe, and should not be considered for **Start** menu pinning or inclusion in the Most Frequently Used (MFU) list.</span></span> <span data-ttu-id="8245f-214">Cuando se inicia con un acceso directo que contiene una lista de argumentos que no son NULL o un [identificador de modelo de usuario de aplicación explícito (AppUserModelIDs)](appids.md), el proceso se puede anclar (como ese método abreviado).</span><span class="sxs-lookup"><span data-stu-id="8245f-214">When launched with a shortcut that contains a non-null argument list or an explicit [Application User Model IDs (AppUserModelIDs)](appids.md), the process can be pinned (as that shortcut).</span></span> <span data-ttu-id="8245f-215">Estos métodos abreviados son candidatos para su inclusión en la lista de MFU.</span><span class="sxs-lookup"><span data-stu-id="8245f-215">Such shortcuts are candidates for inclusion in the MFU list.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="8245f-216">NoStartPage</span><span class="sxs-lookup"><span data-stu-id="8245f-216">NoStartPage</span></span>                      | <span data-ttu-id="8245f-217">Indica que el archivo ejecutable de la aplicación y los accesos directos deben excluirse del menú **Inicio** y de anclarse o incluirse en la lista de MFU.</span><span class="sxs-lookup"><span data-stu-id="8245f-217">Indicates that the application executable and shortcuts should be excluded from the **Start** menu and from pinning or inclusion in the MFU list.</span></span> <span data-ttu-id="8245f-218">Esta entrada se usa normalmente para excluir las herramientas del sistema, los instaladores y los desinstaladores, y los archivos Léame.</span><span class="sxs-lookup"><span data-stu-id="8245f-218">This entry is typically used to exclude system tools, installers and uninstallers, and readme files.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8245f-219">UseExecutableForTaskbarGroupIcon</span><span class="sxs-lookup"><span data-stu-id="8245f-219">UseExecutableForTaskbarGroupIcon</span></span> | <span data-ttu-id="8245f-220">Hace que la barra de tareas Use el icono predeterminado de este archivo ejecutable si no hay ningún acceso directo anclado para esta aplicación y en lugar del icono de la ventana que se encontró por primera vez.</span><span class="sxs-lookup"><span data-stu-id="8245f-220">Causes the taskbar to use the default icon of this executable if there is no pinnable shortcut for this application, and instead of the icon of the window that was first encountered.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8245f-221">TaskbarGroupIcon</span><span class="sxs-lookup"><span data-stu-id="8245f-221">TaskbarGroupIcon</span></span>                 | <span data-ttu-id="8245f-222">Especifica el icono que se usa para invalidar el icono de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="8245f-222">Specifies the icon used to override the taskbar icon.</span></span> <span data-ttu-id="8245f-223">El icono de ventana se usa normalmente para la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="8245f-223">The window icon is normally used for the taskbar.</span></span> <span data-ttu-id="8245f-224">La configuración de la entrada TaskbarGroupIcon hace que el sistema use en su lugar el icono del archivo. exe para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8245f-224">Setting the TaskbarGroupIcon entry causes the system to use the icon from the .exe for the application instead.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

### <a name="examples"></a><span data-ttu-id="8245f-225">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8245f-225">Examples</span></span>

<span data-ttu-id="8245f-226">A continuación se muestran algunos ejemplos de registros de aplicación a través de la subclave de aplicaciones **\_ \_ raíz de las clases HKEY** \\  \\ *ApplicationName.exe* .</span><span class="sxs-lookup"><span data-stu-id="8245f-226">Some examples of application registrations through the **HKEY\_CLASSES\_ROOT**\\**Applications**\\*ApplicationName.exe* subkey are as follows.</span></span> <span data-ttu-id="8245f-227">Todos los valores de entrada del registro son del tipo **reg \_ SZ** , con la excepción de **DefaultIcon** , que es de tipo **reg \_ Expand \_** .</span><span class="sxs-lookup"><span data-stu-id="8245f-227">All registry entry values are of **REG\_SZ** type, with the exception of **DefaultIcon** which is of **REG\_EXPAND\_SZ** type.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      wordpad.exe
         FriendlyAppName = @%SystemRoot%\System32\shell32.dll,-22069
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         SupportedTypes
            .3gp2
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         DefaultIcon
            (Default) = %SystemRoot%\system32\wmploc.dll,-730
```

```
HKEY_CLASSES_ROOT
   Applications
      WScript.exe
         NoOpenWith
```

```
HKEY_CLASSES_ROOT
   Applications
      photoviewer.dll
         shell
            open
               DropTarget
                  Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
```

```
HKEY_CLASSES_ROOT
   Applications
      mspaint.exe
         SupportedTypes
            .bmp
            .dib
            .rle
            .jpg
            .jpeg
            .jpe
            .jfif
            .gif
            .emf
            .wmf
            .tif
            .tiff
            .png
            .ico
```

## <a name="registering-verbs-and-other-file-association-information"></a><span data-ttu-id="8245f-228">Registrar verbos y otra información de Asociación de archivos</span><span class="sxs-lookup"><span data-stu-id="8245f-228">Registering Verbs and Other File Association Information</span></span>

<span data-ttu-id="8245f-229">Las subclaves registradas en **\_ las clases HKEY \_ raíz** \\ **SystemFileAssociations** permiten al shell definir el comportamiento predeterminado de los atributos de los tipos de archivo y habilitar las asociaciones de archivos compartidos.</span><span class="sxs-lookup"><span data-stu-id="8245f-229">Subkeys registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** enable the Shell to define the default behavior of attributes for file types and enable shared file associations.</span></span> <span data-ttu-id="8245f-230">Cuando los usuarios cambian la aplicación predeterminada para un tipo de archivo, el ProgID de la nueva aplicación predeterminada tiene prioridad en proporcionar verbos y otra información de asociación.</span><span class="sxs-lookup"><span data-stu-id="8245f-230">When users change the default application for a file type, the ProgID of the new default application has priority in providing verbs and other association information.</span></span> <span data-ttu-id="8245f-231">Esta prioridad se debe a que es la primera entrada de la matriz de asociaciones.</span><span class="sxs-lookup"><span data-stu-id="8245f-231">This priority is due to it being the first entry in the association array.</span></span> <span data-ttu-id="8245f-232">Si se cambia el programa predeterminado, la información del ProgID anterior ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8245f-232">If the default program is changed, the information under the previous ProgID is no longer available.</span></span>

<span data-ttu-id="8245f-233">Para tratar de forma proactiva las consecuencias de un cambio en los programas predeterminados, puede usar **\_ las clases HKEY \_ raíz** \\ **SystemFileAssociations** para registrar verbos y otra información de asociación.</span><span class="sxs-lookup"><span data-stu-id="8245f-233">To deal proactively with the consequences of a change to default programs, you can use **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** to register verbs and other association information.</span></span> <span data-ttu-id="8245f-234">Debido a su ubicación después del identificador de programa (ProgID) de la matriz de asociaciones, estos registros tienen una prioridad más baja.</span><span class="sxs-lookup"><span data-stu-id="8245f-234">Due to their location after the ProgID in the association array, these registrations are lower priority.</span></span> <span data-ttu-id="8245f-235">Estos SystemFileAssociationsregistrations son estables incluso cuando los usuarios cambian los programas predeterminados y proporcionan una ubicación para registrar verbos secundarios que siempre estarán disponibles para un tipo de archivo determinado.</span><span class="sxs-lookup"><span data-stu-id="8245f-235">These SystemFileAssociationsregistrations are stable even when users change the default programs, and provide a location to register secondary verbs that will always be available for a particular file type.</span></span> <span data-ttu-id="8245f-236">Para obtener un ejemplo del registro, vea [registrar un tipo percibido](#registering-a-perceived-type) más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="8245f-236">For a registry example, see [Registering a Perceived Type](#registering-a-perceived-type) later in this topic.</span></span>

<span data-ttu-id="8245f-237">En el ejemplo del Registro siguiente se muestra lo que ocurre cuando el usuario ejecuta el elemento **programas predeterminados** en el panel de control para cambiar el valor predeterminado de los archivos. mp3 a App2ProgID.</span><span class="sxs-lookup"><span data-stu-id="8245f-237">The following registry example shows what happens when the user runs the **Default Programs** item in Control Panel to change the default for .mp3 files to App2ProgID.</span></span> <span data-ttu-id="8245f-238">Después de cambiar el valor predeterminado, Verb1 ya no está disponible y Verb2 se convierte en el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8245f-238">After changing the default, Verb1 is no longer available, and Verb2 becomes the default.</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = App1ProgID
```

```
HKEY_CLASSES_ROOT
   App1ProgID
      shell
         Verb1
```

```
HKEY_CLASSES_ROOT
   App2ProgID
      shell
         Verb2
```

## <a name="registering-a-perceived-type"></a><span data-ttu-id="8245f-239">Registrar un tipo percibido</span><span class="sxs-lookup"><span data-stu-id="8245f-239">Registering a Perceived Type</span></span>

<span data-ttu-id="8245f-240">Los valores del registro para los tipos percibidos se definen como subclaves de la subclave del registro SystemFileAssociations de **\_ las clases HKEY \_ raíz** \\  .</span><span class="sxs-lookup"><span data-stu-id="8245f-240">Registry values for perceived types are defined as subkeys of the **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** registry subkey.</span></span> <span data-ttu-id="8245f-241">Por ejemplo, el **texto** de tipo percibido se registra de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8245f-241">For example, the perceived type **text** is registered as follows:</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      text
         shell
            edit
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
            open
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
```

<span data-ttu-id="8245f-242">El tipo percibido de un tipo de archivo se indica incluyendo un valor PerceivedType en la subclave del tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="8245f-242">A file type's perceived type is indicated by including a PerceivedType value in the file type's subkey.</span></span> <span data-ttu-id="8245f-243">El valor PerceivedType se establece en el nombre del tipo percibido registrado en la subclave del registro SystemFileAssociations de **\_ las clases \_ HKEY** \\  , tal como se muestra en el ejemplo del registro anterior.</span><span class="sxs-lookup"><span data-stu-id="8245f-243">The PerceivedType value is set to the name of the perceived type registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** registry subkey, as shown in the previous registry example.</span></span> <span data-ttu-id="8245f-244">Para declarar los archivos. cpp como de tipo "texto" percibido, por ejemplo, agregue la siguiente entrada del registro:</span><span class="sxs-lookup"><span data-stu-id="8245f-244">To declare .cpp files as being of perceived type "text", for example, add the following registry entry:</span></span>

```
HKEY_CLASSES_ROOT
   .cpp
      PerceivedType = text
```

## <a name="related-topics"></a><span data-ttu-id="8245f-245">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8245f-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8245f-246">Tipos de archivo</span><span class="sxs-lookup"><span data-stu-id="8245f-246">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="8245f-247">Cómo funcionan las asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="8245f-247">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="8245f-248">Vista de contenido por tipo de archivo o tipo</span><span class="sxs-lookup"><span data-stu-id="8245f-248">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="8245f-249">Comprobador de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="8245f-249">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="8245f-250">Controladores de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="8245f-250">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="8245f-251">Identificadores de programación</span><span class="sxs-lookup"><span data-stu-id="8245f-251">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="8245f-252">Tipos percibidos</span><span class="sxs-lookup"><span data-stu-id="8245f-252">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="8245f-253">Matrices de asociación</span><span class="sxs-lookup"><span data-stu-id="8245f-253">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

