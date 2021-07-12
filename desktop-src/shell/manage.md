---
description: Shell proporciona varias maneras de administrar sistemas de archivos.
ms.assetid: d9ffda6f-adc0-44a3-b410-e23bf5f4f165
title: Administración del sistema de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0f3b47e17e691c540a9775f3b8588b311b9878
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581623"
---
# <a name="managing-the-file-system"></a><span data-ttu-id="8f746-103">Administración del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="8f746-103">Managing the File System</span></span>

<span data-ttu-id="8f746-104">Shell proporciona varias maneras de administrar sistemas de archivos.</span><span class="sxs-lookup"><span data-stu-id="8f746-104">The Shell provides a number of ways to manage file systems.</span></span> <span data-ttu-id="8f746-105">El Shell proporciona una función, [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa), que permite a una aplicación mover, copiar, cambiar el nombre y eliminar archivos mediante programación.</span><span class="sxs-lookup"><span data-stu-id="8f746-105">The Shell provides a function, [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa), that allows an application to programmatically move, copy, rename, and delete files.</span></span> <span data-ttu-id="8f746-106">Shell también admite algunas funcionalidades de administración de archivos adicionales.</span><span class="sxs-lookup"><span data-stu-id="8f746-106">The Shell also supports some additional file management capabilities.</span></span>

-   <span data-ttu-id="8f746-107">Los documentos HTML se pueden *conectar* a archivos relacionados, como archivos de gráficos o hojas de estilos.</span><span class="sxs-lookup"><span data-stu-id="8f746-107">HTML documents can be *connected* to related files, such as graphics files or style sheets.</span></span> <span data-ttu-id="8f746-108">Cuando se mueve o copia el documento, los archivos conectados también se mueven o copian automáticamente.</span><span class="sxs-lookup"><span data-stu-id="8f746-108">When the document is moved or copied, the connected files are automatically moved or copied as well.</span></span>
-   <span data-ttu-id="8f746-109">En el caso de los sistemas que están disponibles para más de un usuario, los archivos se pueden administrar por usuario.</span><span class="sxs-lookup"><span data-stu-id="8f746-109">For systems that are available to more than one user, files can be managed on a per-user basis.</span></span> <span data-ttu-id="8f746-110">Los usuarios tienen acceso fácil a sus archivos de datos, pero no a los archivos que pertenecen a otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="8f746-110">Users have easy access to their data files, but not to files belonging to other users.</span></span>
-   <span data-ttu-id="8f746-111">Si se agregan o modifican archivos de documento, se pueden agregar a la lista de documentos recientes del shell.</span><span class="sxs-lookup"><span data-stu-id="8f746-111">If document files are added or modified, they can be added to the Shell's list of recent documents.</span></span> <span data-ttu-id="8f746-112">Cuando el usuario hace clic en **el comando Documentos** del menú Inicio, aparece una lista de vínculos a los documentos.</span><span class="sxs-lookup"><span data-stu-id="8f746-112">When the user clicks the **Documents** command on the Start menu, a list of links to the documents appears.</span></span>

<span data-ttu-id="8f746-113">En este documento se describe cómo funcionan estas tecnologías de administración de archivos.</span><span class="sxs-lookup"><span data-stu-id="8f746-113">This document discusses how these file management technologies work.</span></span> <span data-ttu-id="8f746-114">A continuación, se describe cómo usar el Shell para mover, copiar, cambiar el nombre y eliminar archivos, y cómo administrar objetos en el papelera de reciclaje.</span><span class="sxs-lookup"><span data-stu-id="8f746-114">It then outlines how to use the Shell to move, copy, rename, and delete files, and how to manage objects in the Recycle Bin.</span></span>

-   [<span data-ttu-id="8f746-115">Administración de archivos por usuario</span><span class="sxs-lookup"><span data-stu-id="8f746-115">Per-User File Management</span></span>](#per-user-file-management)
-   [<span data-ttu-id="8f746-116">carpetas Mis documentos y Mis imágenes</span><span class="sxs-lookup"><span data-stu-id="8f746-116">My Documents and My Pictures Folders</span></span>](#my-documents-and-my-pictures-folders)
-   [<span data-ttu-id="8f746-117">Archivos conectados</span><span class="sxs-lookup"><span data-stu-id="8f746-117">Connected Files</span></span>](#connected-files)
-   [<span data-ttu-id="8f746-118">Mover, copiar, cambiar el nombre y eliminar archivos</span><span class="sxs-lookup"><span data-stu-id="8f746-118">Moving, Copying, Renaming, and Deleting Files</span></span>](#moving-copying-renaming-and-deleting-files)
    -   [<span data-ttu-id="8f746-119">Notificación al shell</span><span class="sxs-lookup"><span data-stu-id="8f746-119">Notifying the Shell</span></span>](#notifying-the-shell)
-   [<span data-ttu-id="8f746-120">Ejemplo sencillo de administración de archivos con SHFileOperation</span><span class="sxs-lookup"><span data-stu-id="8f746-120">Simple Example of Managing Files with SHFileOperation</span></span>](#simple-example-of-managing-files-with-shfileoperation)
-   [<span data-ttu-id="8f746-121">Agregar archivos a la lista de documentos recientes del shell</span><span class="sxs-lookup"><span data-stu-id="8f746-121">Adding Files to the Shell's List of Recent Documents</span></span>](#adding-files-to-the-shells-list-of-recent-documents)

## <a name="per-user-file-management"></a><span data-ttu-id="8f746-122">Per-User file management</span><span class="sxs-lookup"><span data-stu-id="8f746-122">Per-User File Management</span></span>

<span data-ttu-id="8f746-123">El Windows Shell 2000 permite asociar archivos a un usuario determinado para que los archivos permanezcan ocultos para otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="8f746-123">The Windows 2000 Shell allows files to be associated with a particular user so the files remain hidden from other users.</span></span> <span data-ttu-id="8f746-124">En cuanto al sistema de archivos, los archivos se almacenan en la carpeta de perfil del usuario, normalmente C: Documentos y Configuración Nombre de usuario \\ \\  \\ en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8f746-124">In terms of the file system, the files are stored under the user's profile folder, typically C:\\Documents and Settings\\*Username*\\ on Windows 2000 systems.</span></span> <span data-ttu-id="8f746-125">Esta característica permite a muchas personas usar el mismo equipo, al tiempo que se mantiene la privacidad de sus archivos de otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="8f746-125">This feature allows many individuals to use the same computer, while maintaining the privacy of their files from other users.</span></span> <span data-ttu-id="8f746-126">Los distintos usuarios pueden tener programas diferentes disponibles.</span><span class="sxs-lookup"><span data-stu-id="8f746-126">Different users can have different programs available.</span></span> <span data-ttu-id="8f746-127">También proporciona una manera sencilla para que los administradores y las aplicaciones almacenen cosas como la inicialización (.ini) o vincular archivos (.lnk).</span><span class="sxs-lookup"><span data-stu-id="8f746-127">It also provides a straightforward way for administrators and applications to store such things as initialization (.ini) or link (.lnk) files.</span></span> <span data-ttu-id="8f746-128">Por lo tanto, las aplicaciones pueden conservar un estado diferente para cada usuario y recuperar fácilmente ese estado concreto cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="8f746-128">Applications can thus preserve a different state for each user and easily recover that particular state when needed.</span></span> <span data-ttu-id="8f746-129">También hay una carpeta de perfil para almacenar información que es común a todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="8f746-129">There is also a profile folder for storing information that is common to all users.</span></span>

<span data-ttu-id="8f746-130">Dado que no es conveniente determinar qué usuario ha iniciado sesión y dónde se encuentran sus archivos, las carpetas estándar por usuario son carpetas especiales y se identifican mediante [**un CSIDL**](csidl.md).</span><span class="sxs-lookup"><span data-stu-id="8f746-130">Because it is inconvenient to determine which user is logged in and where their files are located, the standard per-user folders are special folders and are identified by a [**CSIDL**](csidl.md).</span></span> <span data-ttu-id="8f746-131">Por ejemplo, el CSIDL de la carpeta Archivos de programa por usuario es CSIDL \_ PROGRAMS.</span><span class="sxs-lookup"><span data-stu-id="8f746-131">For instance, the CSIDL for the per-user Program Files folder is CSIDL\_PROGRAMS.</span></span> <span data-ttu-id="8f746-132">Si la aplicación llama a [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) o [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con uno de los CSIDL por usuario, la función devuelve el puntero a una lista de identificadores de elemento (PIDL) o ruta de acceso adecuada para el usuario que ha iniciado sesión actualmente.</span><span class="sxs-lookup"><span data-stu-id="8f746-132">If your application calls [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) or [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) with one of the per-user CSIDLs, the function returns the pointer to an item identifier list (PIDL) or path appropriate to the currently logged-in user.</span></span> <span data-ttu-id="8f746-133">Si la aplicación necesita recuperar la ruta de acceso o PIDL de la carpeta de perfil, su CSIDL es **CSIDL \_ PROFILE**.</span><span class="sxs-lookup"><span data-stu-id="8f746-133">If your application needs to retrieve the path or PIDL of the profile folder, its CSIDL is **CSIDL\_PROFILE**.</span></span>

## <a name="my-documents-and-my-pictures-folders"></a><span data-ttu-id="8f746-134">carpetas Mis documentos y Mis imágenes</span><span class="sxs-lookup"><span data-stu-id="8f746-134">My Documents and My Pictures Folders</span></span>

<span data-ttu-id="8f746-135">Uno de los iconos estándar que se encuentran en el escritorio **es Mis documentos**.</span><span class="sxs-lookup"><span data-stu-id="8f746-135">One of the standard icons found on the desktop is **My Documents**.</span></span> <span data-ttu-id="8f746-136">Al abrir esta carpeta, contiene los archivos de documento del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="8f746-136">When you open this folder, it contains the current user's document files.</span></span> <span data-ttu-id="8f746-137">La instancia de escritorio de Mis documentos es una carpeta virtual (un alias de la ubicación del sistema de archivos que se usa para almacenar físicamente los documentos del usuario) que se encuentra inmediatamente debajo del escritorio en la jerarquía de espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="8f746-137">The desktop instance of My Documents is a virtual folder—an alias to the file system location used to physically store the user's documents—located immediately below the desktop in the namespace hierarchy.</span></span>

<span data-ttu-id="8f746-138">El propósito de las carpetas Mis documentos y Mis imágenes es proporcionar una manera sencilla y segura para que los usuarios accedan a sus archivos de documentos e imágenes en un sistema que podría tener varios usuarios.</span><span class="sxs-lookup"><span data-stu-id="8f746-138">The purpose of the My Documents and My Pictures folders is to provide a straightforward and secure way for users to access their document and picture files on a system that might have multiple users.</span></span> <span data-ttu-id="8f746-139">A cada usuario se le asignan carpetas del sistema de archivos independientes para sus archivos.</span><span class="sxs-lookup"><span data-stu-id="8f746-139">Each user is assigned separate file system folders for his or her files.</span></span> <span data-ttu-id="8f746-140">Por ejemplo, la ubicación de la carpeta documents de un usuario en el sistema de archivos suele ser algo parecido a C: Documents y Configuración nombre de \\ \\  \\ usuario Mis documentos.</span><span class="sxs-lookup"><span data-stu-id="8f746-140">For example, the location of a user's documents folder in the file system is typically something like C:\\Documents and Settings\\*username*\\My Documents.</span></span> <span data-ttu-id="8f746-141">No es necesario que los usuarios sepan nada sobre la ubicación física de sus carpetas del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="8f746-141">There is no need for users to know anything about the physical location of their file system folders.</span></span> <span data-ttu-id="8f746-142">Simplemente acceden a sus archivos a través del Mis documentos archivo.</span><span class="sxs-lookup"><span data-stu-id="8f746-142">They simply access their files through the My Documents icon.</span></span>

> [!Note]  
> <span data-ttu-id="8f746-143">Mis documentos permite que un usuario acceda a sus propios archivos, pero no a los de ningún otro usuario.</span><span class="sxs-lookup"><span data-stu-id="8f746-143">My Documents allows a user to access his or her own files but not those of any other user.</span></span> <span data-ttu-id="8f746-144">Si varias personas usan el mismo equipo, un administrador puede bloquear a los usuarios de la parte del sistema de archivos donde se almacenan los archivos reales.</span><span class="sxs-lookup"><span data-stu-id="8f746-144">If multiple individuals use the same computer, an administrator can lock users out of the part of the file system where the actual files are stored.</span></span> <span data-ttu-id="8f746-145">Por lo tanto, los usuarios podrán trabajar en sus propios documentos a través de la carpeta Mis documentos, pero no en documentos que pertenezcan a otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="8f746-145">Users will thus be able to work on their own documents through the My Documents folder but not on documents that belong to any other users.</span></span>

 

<span data-ttu-id="8f746-146">Por lo general, no es necesario que una aplicación sepa qué usuario ha iniciado sesión o dónde se encuentra en el sistema de archivos Mis documentos carpeta del usuario.</span><span class="sxs-lookup"><span data-stu-id="8f746-146">There is usually no need for an application to know which user is logged in or where in the file system that user's My Documents folder is located.</span></span> <span data-ttu-id="8f746-147">En su lugar, la aplicación puede recuperar el PIDL del icono de escritorio Mis documentos mediante una llamada al método [**IShellFolder::P arseDisplayName del**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) escritorio.</span><span class="sxs-lookup"><span data-stu-id="8f746-147">Instead, your application can retrieve the PIDL of the My Documents desktop icon by calling the desktop's [**IShellFolder::ParseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) method.</span></span> <span data-ttu-id="8f746-148">El nombre de análisis usado para identificar la carpeta Mis documentos no es una ruta de acceso de archivo, sino ::{450d8fba-ad25-11d0-98a8-0800361b1103}.</span><span class="sxs-lookup"><span data-stu-id="8f746-148">The parsing name used to identify the My Documents folder is not a file path but rather ::{450d8fba-ad25-11d0-98a8-0800361b1103}.</span></span> <span data-ttu-id="8f746-149">La expresión entre corchetes es la forma de texto Mis documentos GUID.</span><span class="sxs-lookup"><span data-stu-id="8f746-149">The bracketed expression is the text form of the My Documents GUID.</span></span> <span data-ttu-id="8f746-150">Por ejemplo, para recuperar el PIDL de Mis documentos, la aplicación debe usar esta llamada a **IShellFolder::P arseDisplayName**.</span><span class="sxs-lookup"><span data-stu-id="8f746-150">For example, to retrieve the PIDL of My Documents, your application should use this call to **IShellFolder::ParseDisplayName**.</span></span>


```C++
hr = psfDeskTop->ParseDisplayName(NULL, 
                                  NULL, 
                                  L"::{450d8fba-ad25-11d0-98a8-0800361b1103}", 
                                  &chEaten, 
                                  &pidlDocFiles, 
                                  NULL);
```



<span data-ttu-id="8f746-151">Una vez que la aplicación tiene el PIDL de Mis documentos, puede controlar la carpeta igual que lo haría con una carpeta normal del sistema de archivos: enumerar elementos, analizar, enlazar y realizar cualquier otra operación de carpeta válida.</span><span class="sxs-lookup"><span data-stu-id="8f746-151">Once your application has the My Documents PIDL, it can handle the folder just as it would a normal file system folder—enumerating items, parsing, binding, and performing any other valid folder operations.</span></span> <span data-ttu-id="8f746-152">El Shell asigna automáticamente los cambios de Mis documentos sus subcarpetas a las carpetas del sistema de archivos adecuadas.</span><span class="sxs-lookup"><span data-stu-id="8f746-152">The Shell automatically maps changes in My Documents or its subfolders to the appropriate file system folders.</span></span>

<span data-ttu-id="8f746-153">Si la aplicación necesita acceso a la carpeta del sistema de archivos real que contiene los documentos del usuario actual, pase CSIDL \_ PERSONAL a [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation).</span><span class="sxs-lookup"><span data-stu-id="8f746-153">If your application needs access to the actual file system folder that contains the current user's documents, pass CSIDL\_PERSONAL to [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation).</span></span> <span data-ttu-id="8f746-154">La función devuelve el PIDL de la carpeta del sistema de archivos que se muestra en la carpeta de Mis documentos usuario actual.</span><span class="sxs-lookup"><span data-stu-id="8f746-154">The function returns the PIDL of the file system folder that is displayed in the current user's My Documents folder.</span></span>

## <a name="connected-files"></a><span data-ttu-id="8f746-155">Archivos conectados</span><span class="sxs-lookup"><span data-stu-id="8f746-155">Connected Files</span></span>

<span data-ttu-id="8f746-156">Los documentos HTML suelen tener varios archivos de gráficos asociados, un archivo de hoja de estilos, varios archivos de Microsoft JScript (compatibles con la especificación del lenguaje ECMA 262), y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="8f746-156">HTML documents often have a number of associated graphics files, a style sheet file, several Microsoft JScript (compatible with ECMA 262 language specification ) files, and so on.</span></span> <span data-ttu-id="8f746-157">Al mover o copiar el documento HTML principal, normalmente también desea mover o copiar sus archivos asociados para evitar la separación de vínculos.</span><span class="sxs-lookup"><span data-stu-id="8f746-157">When you move or copy the primary HTML document, you also usually want to move or copy its associated files to avoid breaking links.</span></span> <span data-ttu-id="8f746-158">Desafortunadamente, hasta ahora no ha habido ninguna manera fácil de determinar qué archivos están relacionados con un documento HTML determinado que no sea mediante el análisis de su contenido.</span><span class="sxs-lookup"><span data-stu-id="8f746-158">Unfortunately, there has been no easy way until now to determine which files are related to any given HTML document other than by analyzing their contents.</span></span> <span data-ttu-id="8f746-159">Para mitigar este problema, Windows 2000 proporciona una manera sencilla de conectar un documento HTML principal *a* su grupo de archivos asociados.</span><span class="sxs-lookup"><span data-stu-id="8f746-159">To alleviate this problem, Windows 2000 provides a simple way to *connect* a primary HTML document to its group of associated files.</span></span> <span data-ttu-id="8f746-160">Si la conexión de archivos está habilitada, cuando se mueve o copia el documento, todos sus archivos conectados van con él.</span><span class="sxs-lookup"><span data-stu-id="8f746-160">If file connection is enabled, when the document is moved or copied all its connected files go with it.</span></span>

<span data-ttu-id="8f746-161">Para crear un grupo de archivos conectados, el documento principal debe tener una extensión .htm o .html de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="8f746-161">To create a group of connected files, the primary document must have an .htm or .html file name extension.</span></span> <span data-ttu-id="8f746-162">Cree una subcarpeta de la carpeta primaria del documento principal.</span><span class="sxs-lookup"><span data-stu-id="8f746-162">Create a subfolder of the primary document's parent folder.</span></span> <span data-ttu-id="8f746-163">El nombre de la subcarpeta debe ser el nombre del documento principal, menos la extensión .htm o .html, seguida de una de las extensiones enumeradas a continuación.</span><span class="sxs-lookup"><span data-stu-id="8f746-163">The subfolder's name must be the name of the primary document, minus the .htm or .html extension, followed by one of the extensions listed below.</span></span> <span data-ttu-id="8f746-164">Las extensiones más usadas son ".files" o \_ "files".</span><span class="sxs-lookup"><span data-stu-id="8f746-164">The most commonly used extensions are ".files" or "\_files".</span></span> <span data-ttu-id="8f746-165">Por ejemplo, si el documento principal se denomina MyDoc.htm, al asignar un nombre a la subcarpeta "MyDoc files" se define la subcarpeta como contenedor de los archivos conectados \_ del documento.</span><span class="sxs-lookup"><span data-stu-id="8f746-165">For instance, if the primary document is named MyDoc.htm, naming the subfolder "MyDoc\_files" defines the subfolder as the container for the document's connected files.</span></span> <span data-ttu-id="8f746-166">Si el documento principal se mueve o se copia, la subcarpeta y sus archivos también se mueven o copian.</span><span class="sxs-lookup"><span data-stu-id="8f746-166">If the primary document is moved or copied, the subfolder and its files are moved or copied as well.</span></span>

<span data-ttu-id="8f746-167">En algunos idiomas, es posible usar un equivalente localizado de \_ "archivos" para crear una subcarpeta para los archivos conectados.</span><span class="sxs-lookup"><span data-stu-id="8f746-167">For some languages, it is possible to use a localized equivalent of "\_files" to create a subfolder for connected files.</span></span> <span data-ttu-id="8f746-168">En la tabla siguiente se enumeran las cadenas válidas que se pueden anexar a un nombre de documento para crear una subcarpeta de archivos conectados.</span><span class="sxs-lookup"><span data-stu-id="8f746-168">The following table lists the valid strings that can be appended to a document name to create a connected files subfolder.</span></span> <span data-ttu-id="8f746-169">Tenga en cuenta que algunas de estas cadenas tienen "-" como primer carácter en lugar de \_ "" o ".".</span><span class="sxs-lookup"><span data-stu-id="8f746-169">Note that some of these strings have '-' as their first character rather than '\_' or '.'.</span></span>



:::row:::
   :::column span="":::
      <span data-ttu-id="8f746-170">\_"archivos"</span><span class="sxs-lookup"><span data-stu-id="8f746-170">"\_archivos"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8f746-171">\_"arquivos"</span><span class="sxs-lookup"><span data-stu-id="8f746-171">"\_arquivos"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8f746-172">\_"bestanden"</span><span class="sxs-lookup"><span data-stu-id="8f746-172">"\_bestanden"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8f746-173">\_"bylos"</span><span class="sxs-lookup"><span data-stu-id="8f746-173">"\_bylos"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="8f746-174">"-Dateien"</span><span class="sxs-lookup"><span data-stu-id="8f746-174">"-Dateien"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8f746-175">\_"datoteke"</span><span class="sxs-lookup"><span data-stu-id="8f746-175">"\_datoteke"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8f746-176">\_"dosyalar"</span><span class="sxs-lookup"><span data-stu-id="8f746-176">"\_dosyalar"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8f746-177">\_"elemei"</span><span class="sxs-lookup"><span data-stu-id="8f746-177">"\_elemei"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="8f746-178">" \_ failid"</span><span class="sxs-lookup"><span data-stu-id="8f746-178">"\_failid"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8f746-179">" \_ se produce un error"</span><span class="sxs-lookup"><span data-stu-id="8f746-179">"\_fails"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8f746-180">" \_ fa faq"</span><span class="sxs-lookup"><span data-stu-id="8f746-180">"\_fajlovi"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8f746-181">\_"fich..."</span><span class="sxs-lookup"><span data-stu-id="8f746-181">"\_ficheiros"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="8f746-182">\_"fichiers"</span><span class="sxs-lookup"><span data-stu-id="8f746-182">"\_fichiers"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8f746-183">"-filer"</span><span class="sxs-lookup"><span data-stu-id="8f746-183">"-filer"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8f746-184">".files"</span><span class="sxs-lookup"><span data-stu-id="8f746-184">".files"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8f746-185">" \_ files"</span><span class="sxs-lookup"><span data-stu-id="8f746-185">"\_files"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="8f746-186">" \_ file"</span><span class="sxs-lookup"><span data-stu-id="8f746-186">"\_file"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8f746-187">\_"fitxers"</span><span class="sxs-lookup"><span data-stu-id="8f746-187">"\_fitxers"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8f746-188">\_"fitxategiak"</span><span class="sxs-lookup"><span data-stu-id="8f746-188">"\_fitxategiak"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8f746-189">" \_ pliki"</span><span class="sxs-lookup"><span data-stu-id="8f746-189">"\_pliki"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="8f746-190">\_"soubory"</span><span class="sxs-lookup"><span data-stu-id="8f746-190">"\_soubory"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8f746-191">\_"tiedostot"</span><span class="sxs-lookup"><span data-stu-id="8f746-191">"\_tiedostot"</span></span>
   :::column-end:::
   :::column span="":::
   :::column-end:::
   :::column span="":::
   :::column-end:::
:::row-end:::



 

> [!Note]  
> <span data-ttu-id="8f746-192">Esta característica es sensible al caso de la extensión.</span><span class="sxs-lookup"><span data-stu-id="8f746-192">This feature is sensitive to the case of the extension.</span></span> <span data-ttu-id="8f746-193">Por ejemplo, en el ejemplo anterior, una subcarpeta denominada "MyDoc Files" no se conectará a \_ MyDoc.htm.</span><span class="sxs-lookup"><span data-stu-id="8f746-193">For instance, for the example given above, a subfolder named "MyDoc\_Files" will not be connected to MyDoc.htm.</span></span>

 

<span data-ttu-id="8f746-194">Si la conexión de archivos está habilitada o deshabilitada se controla mediante un **valor \_ REG DWORD,** NoFileFolderConnection, de la siguiente clave del Registro.</span><span class="sxs-lookup"><span data-stu-id="8f746-194">Whether file connection is enabled or disabled is controlled by a **REG\_DWORD** value, NoFileFolderConnection, of the following registry key.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
```

<span data-ttu-id="8f746-195">Normalmente, este valor no está definido y la conexión de archivos está habilitada.</span><span class="sxs-lookup"><span data-stu-id="8f746-195">This value normally is not defined, and file connection is enabled.</span></span> <span data-ttu-id="8f746-196">Si es necesario, puede deshabilitar la conexión de archivos si agrega este valor a la clave y lo establece en 1.</span><span class="sxs-lookup"><span data-stu-id="8f746-196">If necessary, you can disable file connection by adding this value to the key and setting it to 1.</span></span> <span data-ttu-id="8f746-197">Para volver a habilitar la conexión de archivos, establezca NoFileFolderConnection en cero.</span><span class="sxs-lookup"><span data-stu-id="8f746-197">To enable file connection again, set NoFileFolderConnection to zero.</span></span>

> [!Note]  
> <span data-ttu-id="8f746-198">Normalmente, la conexión de archivos debe habilitarse porque otras aplicaciones pueden depender de ella.</span><span class="sxs-lookup"><span data-stu-id="8f746-198">File connection should normally be enabled because other applications might depend on it.</span></span> <span data-ttu-id="8f746-199">Deshabilite la conexión de archivos solo si es absolutamente necesario.</span><span class="sxs-lookup"><span data-stu-id="8f746-199">Disable file connection only if absolutely necessary.</span></span>

 

## <a name="moving-copying-renaming-and-deleting-files"></a><span data-ttu-id="8f746-200">Mover, copiar, cambiar el nombre y eliminar archivos</span><span class="sxs-lookup"><span data-stu-id="8f746-200">Moving, Copying, Renaming, and Deleting Files</span></span>

<span data-ttu-id="8f746-201">El espacio de nombres no es estático y las aplicaciones normalmente necesitan administrar el sistema de archivos mediante una de las siguientes operaciones.</span><span class="sxs-lookup"><span data-stu-id="8f746-201">The namespace is not static, and applications commonly need to manage the file system by performing one of the following operations.</span></span>

-   <span data-ttu-id="8f746-202">Copiar un objeto en otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="8f746-202">Copying an object to another folder.</span></span>
-   <span data-ttu-id="8f746-203">Mover un objeto a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="8f746-203">Moving an object to another folder.</span></span>
-   <span data-ttu-id="8f746-204">Eliminar un objeto.</span><span class="sxs-lookup"><span data-stu-id="8f746-204">Deleting an object.</span></span>
-   <span data-ttu-id="8f746-205">Cambiar el nombre de un objeto.</span><span class="sxs-lookup"><span data-stu-id="8f746-205">Renaming an object.</span></span>

<span data-ttu-id="8f746-206">Todas estas operaciones se realizan con [**SHFileOperation.**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)</span><span class="sxs-lookup"><span data-stu-id="8f746-206">These operations are all performed with [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa).</span></span> <span data-ttu-id="8f746-207">Esta función toma uno o varios archivos de origen y genera los archivos de destino correspondientes.</span><span class="sxs-lookup"><span data-stu-id="8f746-207">This function takes one or more source files and produces corresponding destination files.</span></span> <span data-ttu-id="8f746-208">En el caso de la operación de eliminación, el sistema intenta colocar los archivos eliminados en el papelera de reciclaje.</span><span class="sxs-lookup"><span data-stu-id="8f746-208">In the case of the delete operation, the system attempts to put the deleted files into the Recycle Bin.</span></span>

<span data-ttu-id="8f746-209">También es posible mover archivos mediante la funcionalidad [de arrastrar y](dragdrop.md) colocar.</span><span class="sxs-lookup"><span data-stu-id="8f746-209">It is also possible to move files using the [drag-and-drop](dragdrop.md) functionality.</span></span>

<span data-ttu-id="8f746-210">Para usar la función , debe rellenar los miembros de una estructura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) y pasarla a [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa).</span><span class="sxs-lookup"><span data-stu-id="8f746-210">To use the function, you must fill in the members of an [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure and pass it to [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa).</span></span> <span data-ttu-id="8f746-211">Los miembros clave de la estructura son **pFrom** y **pTo**.</span><span class="sxs-lookup"><span data-stu-id="8f746-211">The key members of the structure are **pFrom** and **pTo**.</span></span>

<span data-ttu-id="8f746-212">El **miembro pFrom** es una cadena **terminada** en null doble que contiene uno o varios nombres de archivo de origen.</span><span class="sxs-lookup"><span data-stu-id="8f746-212">The **pFrom** member is a double **null**-terminated string that contains one or more source file names.</span></span> <span data-ttu-id="8f746-213">Estos nombres pueden ser rutas de acceso completas o caracteres comodín dos estándar, como \* \* .</span><span class="sxs-lookup"><span data-stu-id="8f746-213">These names can be either fully qualified paths or standard DOS wildcards such as \*.\*.</span></span> <span data-ttu-id="8f746-214">Aunque este miembro se declara como una cadena terminada en **NULL,** se usa como búfer para contener varios nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="8f746-214">Although this member is declared as a **null**-terminated string, it is used as a buffer to hold multiple file names.</span></span> <span data-ttu-id="8f746-215">El carácter NULL único habitual debe terminar cada nombre **de** archivo.</span><span class="sxs-lookup"><span data-stu-id="8f746-215">Each file name must be terminated by the usual single **NULL** character.</span></span> <span data-ttu-id="8f746-216">Se debe **anexar** un carácter NULL adicional al final del nombre final para indicar el final de **pFrom**.</span><span class="sxs-lookup"><span data-stu-id="8f746-216">An additional **NULL** character must be appended to the end of the final name to indicate the end of **pFrom**.</span></span>

<span data-ttu-id="8f746-217">El **miembro pTo** es una cadena **terminada** en null doble, muy parecido a **pFrom**.</span><span class="sxs-lookup"><span data-stu-id="8f746-217">The **pTo** member is a double **null**-terminated string, much like **pFrom**.</span></span> <span data-ttu-id="8f746-218">El **miembro pTo** contiene los nombres de uno o varios nombres de destino completos.</span><span class="sxs-lookup"><span data-stu-id="8f746-218">The **pTo** member contains the names of one or more fully qualified destination names.</span></span> <span data-ttu-id="8f746-219">Se empaquetan en **pTo de la** misma manera que para **pFrom**.</span><span class="sxs-lookup"><span data-stu-id="8f746-219">They are packed into **pTo** in the same way as they are for **pFrom**.</span></span> <span data-ttu-id="8f746-220">Si **pTo** contiene varios nombres, también debe establecer la marca **\_ FOF MULTIDESTFILES** en el **miembro fFlags.**</span><span class="sxs-lookup"><span data-stu-id="8f746-220">If **pTo** contains multiple names, you must also set the **FOF\_MULTIDESTFILES** flag in the **fFlags** member.</span></span> <span data-ttu-id="8f746-221">El uso de **pTo** depende de la operación como se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="8f746-221">The usage of **pTo** depends on the operation as described here.</span></span>

-   <span data-ttu-id="8f746-222">Para las operaciones de copia y movimiento, si todos los archivos van a un único directorio, **pTo** contiene el nombre completo del directorio.</span><span class="sxs-lookup"><span data-stu-id="8f746-222">For copy and move operations, if all the files are going to a single directory, **pTo** contains the fully qualified directory name.</span></span> <span data-ttu-id="8f746-223">Si los archivos van a destinos diferentes, **pTo** también puede contener un directorio completo o un nombre de archivo para cada archivo de origen.</span><span class="sxs-lookup"><span data-stu-id="8f746-223">If the files are going to different destinations, **pTo** can also contain one fully qualified directory or file name for each source file.</span></span> <span data-ttu-id="8f746-224">Si no existe un directorio, el sistema lo crea.</span><span class="sxs-lookup"><span data-stu-id="8f746-224">If a directory does not exist, the system creates it.</span></span>
-   <span data-ttu-id="8f746-225">Para las operaciones de cambio de nombre, **pTo** contiene una ruta de acceso completa para cada archivo de origen en **pFrom**.</span><span class="sxs-lookup"><span data-stu-id="8f746-225">For rename operations, **pTo** contains one fully qualified path for each source file in **pFrom**.</span></span>
-   <span data-ttu-id="8f746-226">Para las operaciones de eliminación, no se usa **pTo.**</span><span class="sxs-lookup"><span data-stu-id="8f746-226">For delete operations, **pTo** is not used.</span></span>

### <a name="notifying-the-shell"></a><span data-ttu-id="8f746-227">Notificación al shell</span><span class="sxs-lookup"><span data-stu-id="8f746-227">Notifying the Shell</span></span>

<span data-ttu-id="8f746-228">Notifique al Shell el cambio después de usar [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) para mover, copiar, cambiar el nombre o eliminar archivos, o después de realizar cualquier otra acción que afecte al espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="8f746-228">Notify the Shell of the change after using [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) to move, copy, rename, or delete files, or after taking any other action that affects the namespace.</span></span> <span data-ttu-id="8f746-229">Entre las acciones que deben ir acompañadas de la notificación se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="8f746-229">Actions that should be accompanied by notification include the following:</span></span>

-   <span data-ttu-id="8f746-230">Agregar o eliminar archivos o carpetas.</span><span class="sxs-lookup"><span data-stu-id="8f746-230">Adding or deleting files or folders.</span></span>
-   <span data-ttu-id="8f746-231">Mover, copiar o cambiar el nombre de archivos o carpetas.</span><span class="sxs-lookup"><span data-stu-id="8f746-231">Moving, copying, or renaming files or folders.</span></span>
-   <span data-ttu-id="8f746-232">Cambio de una asociación de archivos.</span><span class="sxs-lookup"><span data-stu-id="8f746-232">Changing a file association.</span></span>
-   <span data-ttu-id="8f746-233">Cambio de atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="8f746-233">Changing file attributes.</span></span>
-   <span data-ttu-id="8f746-234">Agregar o quitar unidades o medios de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="8f746-234">Adding or removing drives or storage media.</span></span>
-   <span data-ttu-id="8f746-235">Crear o deshabilitar una carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="8f746-235">Creating or disabling a shared folder.</span></span>
-   <span data-ttu-id="8f746-236">Cambiar la lista de imágenes del sistema.</span><span class="sxs-lookup"><span data-stu-id="8f746-236">Changing the system image list.</span></span>

<span data-ttu-id="8f746-237">Una aplicación notifica al Shell mediante una llamada a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) con los detalles de lo que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="8f746-237">An application notifies the Shell by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) with the details of what has changed.</span></span> <span data-ttu-id="8f746-238">A continuación, el Shell puede actualizar su imagen del espacio de nombres para reflejar con precisión su nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="8f746-238">The Shell can then update its image of the namespace to accurately reflect its new state.</span></span>

## <a name="simple-example-of-managing-files-with-shfileoperation"></a><span data-ttu-id="8f746-239">Ejemplo sencillo de administración de archivos con SHFileOperation</span><span class="sxs-lookup"><span data-stu-id="8f746-239">Simple Example of Managing Files with SHFileOperation</span></span>

<span data-ttu-id="8f746-240">En la siguiente aplicación de consola de ejemplo se muestra el uso de [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) para copiar archivos de un directorio a otro.</span><span class="sxs-lookup"><span data-stu-id="8f746-240">The following sample console application illustrates the use of [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) to copy files from one directory to another.</span></span> <span data-ttu-id="8f746-241">Los directorios de origen y destino, C: My Docs y \\ \_ C: \\ My Docs2, están codificados de forma fuerte en la aplicación para \_ simplificar.</span><span class="sxs-lookup"><span data-stu-id="8f746-241">The source and destination directories, C:\\My\_Docs and C:\\My\_Docs2, are hard-coded into the application for simplicity.</span></span>


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>

int main(void)
{
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfDocFiles = NULL;
    LPITEMIDLIST pidlDocFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IEnumIDList *ppenum = NULL;
    SHFILEOPSTRUCT sfo;
    STRRET strDispName;
    TCHAR szParseName[MAX_PATH];
    TCHAR szSourceFiles[256];
    int i;
    int iBufPos = 0;
    ULONG chEaten;
    ULONG celtFetched;
    size_t ParseNameSize = 0;
    HRESULT hr;
    

    szSourceFiles[0] = '\0';
    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->ParseDisplayName(NULL, NULL, L"c:\\My_Docs", 
         &chEaten, &pidlDocFiles, NULL);
    hr = psfDeskTop->BindToObject(pidlDocFiles, NULL, IID_IShellFolder, 
         (LPVOID *) &psfDocFiles);
    hr = psfDeskTop->Release();

    hr = psfDocFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, 
         &ppenum);

    while( (hr = ppenum->Next(1,&pidlItems, &celtFetched)) == S_OK 
       && (celtFetched) == 1)
    {
        psfDocFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, 
            &strDispName);
        StrRetToBuf(&strDispName, pidlItems, szParseName, MAX_PATH);
        
        hr = StringCchLength(szParseName, MAX_PATH, &ParseNameSize);
        
        if (SUCCEEDED(hr))
        {
            for(i=0; i<=ParseNameSize; i++)
            {
                szSourceFiles[iBufPos++] = szParseName[i];
            }
            CoTaskMemFree(pidlItems);
        }
    }
    ppenum->Release();
    
    szSourceFiles[iBufPos] = '\0';

    sfo.hwnd = NULL;
    sfo.wFunc = FO_COPY;
    sfo.pFrom = szSourceFiles;
    sfo.pTo = "c:\\My_Docs2\0";
    sfo.fFlags = FOF_SILENT | FOF_NOCONFIRMATION | FOF_NOCONFIRMMKDIR;

    hr = SHFileOperation(&sfo);
    
    SHChangeNotify(SHCNE_UPDATEDIR, SHCNF_PATH, (LPCVOID) "c:\\My_Docs2", 0);

    CoTaskMemFree(pidlDocFiles);
    psfDocFiles->Release();

    return 0;
}
```



<span data-ttu-id="8f746-242">En primer lugar, la aplicación recupera un puntero a la interfaz [**IShellFolder del**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) escritorio.</span><span class="sxs-lookup"><span data-stu-id="8f746-242">The application first retrieves a pointer to the desktop's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="8f746-243">A continuación, recupera el PIDL del directorio de origen pasando su ruta de acceso completa a [**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname).</span><span class="sxs-lookup"><span data-stu-id="8f746-243">It then retrieves the source directory's PIDL by passing its fully qualified path to [**IShellFolder::ParseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname).</span></span> <span data-ttu-id="8f746-244">Tenga en **cuenta que IShellFolder::P arseDisplayName** requiere que la ruta de acceso del directorio sea una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="8f746-244">Note that **IShellFolder::ParseDisplayName** requires the directory's path to be a Unicode string.</span></span> <span data-ttu-id="8f746-245">A continuación, la aplicación se enlaza al directorio de origen y usa su **interfaz IShellFolder** para recuperar la interfaz [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) de un objeto enumerador.</span><span class="sxs-lookup"><span data-stu-id="8f746-245">The application then binds to the source directory and uses its **IShellFolder** interface to retrieve an enumerator object's [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) interface.</span></span>

<span data-ttu-id="8f746-246">A medida que se enumera cada archivo del directorio de origen, se usa [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para recuperar su nombre.</span><span class="sxs-lookup"><span data-stu-id="8f746-246">As each file in the source directory is enumerated, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve its name.</span></span> <span data-ttu-id="8f746-247">Se establece la marca SHGDN FORPARSING, lo que hace que \_ **IShellFolder::GetDisplayNameOf** devuelva la ruta de acceso completa del archivo.</span><span class="sxs-lookup"><span data-stu-id="8f746-247">The SHGDN\_FORPARSING flag is set, which causes **IShellFolder::GetDisplayNameOf** to return the file's fully qualified path.</span></span> <span data-ttu-id="8f746-248">Las rutas de acceso de archivo, incluidos los caracteres **NULL** de terminación, se concatenan en una sola matriz, *szSourceFiles*.</span><span class="sxs-lookup"><span data-stu-id="8f746-248">The file paths, including the terminating **NULL** characters, are concatenated into a single array, *szSourceFiles*.</span></span> <span data-ttu-id="8f746-249">Se anexa **un segundo** carácter NULL a la ruta de acceso final para finalizar correctamente la matriz.</span><span class="sxs-lookup"><span data-stu-id="8f746-249">A second **NULL** character is appended to the final path to terminate the array properly.</span></span>

<span data-ttu-id="8f746-250">Una vez completada la enumeración, la aplicación asigna valores a una [**estructura SHFILEOPSTRUCT.**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa)</span><span class="sxs-lookup"><span data-stu-id="8f746-250">Once the enumeration is complete, the application assigns values to an [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="8f746-251">Tenga en cuenta que la matriz asignada **a pTo** para especificar el destino también debe terminar con un valor **NULL doble.**</span><span class="sxs-lookup"><span data-stu-id="8f746-251">Note that the array assigned to **pTo** to specify the destination must also be terminated by a double **NULL**.</span></span> <span data-ttu-id="8f746-252">En este caso, simplemente se incluye en la cadena que se asigna a **pTo**.</span><span class="sxs-lookup"><span data-stu-id="8f746-252">In this case, it is simply included in the string that is assigned to **pTo**.</span></span> <span data-ttu-id="8f746-253">Dado que se trata de una aplicación de consola, las marcas FOF \_ SILENT, FOF \_ NOCONFIRMATION y \_ FOF NOCONFIRMMKDIR se establecen para suprimir los cuadros de diálogo que puedan aparecer.</span><span class="sxs-lookup"><span data-stu-id="8f746-253">Because this is a console application, the FOF\_SILENT, FOF\_NOCONFIRMATION, and FOF\_NOCONFIRMMKDIR flags are set to suppress any dialog boxes that might appear.</span></span> <span data-ttu-id="8f746-254">Una [**vez que shfileoperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) devuelve, se llama a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) para notificar el cambio al shell.</span><span class="sxs-lookup"><span data-stu-id="8f746-254">After [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) returns, [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) is called to notify the Shell of the change.</span></span> <span data-ttu-id="8f746-255">A continuación, la aplicación realiza la limpieza habitual y devuelve .</span><span class="sxs-lookup"><span data-stu-id="8f746-255">Then the application performs the usual cleanup and returns.</span></span>

## <a name="adding-files-to-the-shells-list-of-recent-documents"></a><span data-ttu-id="8f746-256">Agregar archivos a la lista de documentos recientes del shell</span><span class="sxs-lookup"><span data-stu-id="8f746-256">Adding Files to the Shell's List of Recent Documents</span></span>

<span data-ttu-id="8f746-257">El Shell mantiene una lista de documentos agregados o modificados recientemente para cada usuario.</span><span class="sxs-lookup"><span data-stu-id="8f746-257">The Shell maintains a list of recently added or modified documents for each user.</span></span> <span data-ttu-id="8f746-258">El usuario puede mostrar una lista de vínculos a estos archivos haciendo clic en Documentos en la menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="8f746-258">The user can display a list of links to these files by clicking Documents on the Start menu.</span></span> <span data-ttu-id="8f746-259">Al igual Mis documentos, cada usuario tiene un directorio del sistema de archivos para contener los vínculos reales.</span><span class="sxs-lookup"><span data-stu-id="8f746-259">As with My Documents, each user has a file system directory to hold the actual links.</span></span> <span data-ttu-id="8f746-260">Para recuperar el PIDL del directorio Recent del usuario actual, la aplicación puede llamar a [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) con CSIDL RECENT o llamar a \_ [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) para recuperar su ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="8f746-260">To retrieve the PIDL of the current user's Recent directory, your application can call [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) with CSIDL\_RECENT, or call [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) to retrieve its path.</span></span>

<span data-ttu-id="8f746-261">La aplicación puede enumerar el contenido de la carpeta Recent mediante las técnicas que se han mencionado anteriormente en este documento.</span><span class="sxs-lookup"><span data-stu-id="8f746-261">Your application can enumerate the contents of the Recent folder using the techniques discussed earlier in this document.</span></span> <span data-ttu-id="8f746-262">Sin embargo, una aplicación no debe modificar el contenido de la carpeta como si fuera una carpeta normal del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="8f746-262">However, an application should not modify the contents of the folder as if it were a normal file system folder.</span></span> <span data-ttu-id="8f746-263">Si lo hace, la lista de documentos recientes del Shell no se actualizará correctamente y los cambios no se reflejarán en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="8f746-263">If it does so, the Shell's list of recent documents will not be updated properly, and the changes will not be reflected in the Start menu.</span></span> <span data-ttu-id="8f746-264">En su lugar, para agregar un vínculo de documento a la carpeta Recent de un usuario, la aplicación puede llamar a [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).</span><span class="sxs-lookup"><span data-stu-id="8f746-264">Instead, to add a document link to a user's Recent folder, your application can call [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).</span></span> <span data-ttu-id="8f746-265">El Shell agregará un vínculo a la carpeta del sistema de archivos adecuada, así como actualizar su lista de documentos recientes y el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="8f746-265">The Shell will add a link to the appropriate file system folder, as well as updating its list of recent documents and the Start menu.</span></span> <span data-ttu-id="8f746-266">También puede usar esta función para borrar la carpeta.</span><span class="sxs-lookup"><span data-stu-id="8f746-266">You can also use this function to clear the folder.</span></span>

 

 
