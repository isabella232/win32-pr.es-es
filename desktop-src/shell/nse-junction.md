---
description: La raíz de una extensión de espacio de nombres se muestra normalmente en el explorador de Windows como una carpeta en las vistas de árbol y de carpeta.
title: Especificar la ubicación de una extensión de espacio de nombres
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2c1fdd5d-b359-4d5c-a20e-0622f3a1cb1d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7617c7361c5f2ae76331c5f1b59eb845f6806395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910778"
---
# <a name="specifying-a-namespace-extensions-location"></a><span data-ttu-id="9d3eb-103">Especificar la ubicación de una extensión de espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9d3eb-103">Specifying a Namespace Extension's Location</span></span>

<span data-ttu-id="9d3eb-104">La raíz de una extensión de espacio de nombres se muestra normalmente en el explorador de Windows como una carpeta en las vistas de árbol y de carpeta.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-104">The root of a namespace extension is normally displayed by Windows Explorer as a folder in both tree and folder views.</span></span> <span data-ttu-id="9d3eb-105">Para que el explorador de Windows muestre los archivos y subcarpetas de la extensión, debe especificar dónde se encuentra la carpeta raíz en la jerarquía del espacio de nombres del shell.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-105">For Windows Explorer to display your extension's files and subfolders, you must specify where the root folder is located in the Shell namespace hierarchy.</span></span> <span data-ttu-id="9d3eb-106">Esta ubicación se conoce como punto de *Unión*.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-106">This location is referred to as a *junction point*.</span></span>

-   [<span data-ttu-id="9d3eb-107">Usar carpetas virtuales como puntos de Unión</span><span class="sxs-lookup"><span data-stu-id="9d3eb-107">Using Virtual Folders as Junction Points</span></span>](#using-virtual-folders-as-junction-points)
-   [<span data-ttu-id="9d3eb-108">Usar carpetas del sistema de archivos como puntos de Unión</span><span class="sxs-lookup"><span data-stu-id="9d3eb-108">Using File System Folders as Junction Points</span></span>](#using-file-system-folders-as-junction-points)
-   [<span data-ttu-id="9d3eb-109">Abrir una vista de una extensión de espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9d3eb-109">Opening a View of a Namespace Extension</span></span>](#opening-a-view-of-a-namespace-extension)

## <a name="using-virtual-folders-as-junction-points"></a><span data-ttu-id="9d3eb-110">Usar carpetas virtuales como puntos de Unión</span><span class="sxs-lookup"><span data-stu-id="9d3eb-110">Using Virtual Folders as Junction Points</span></span>

<span data-ttu-id="9d3eb-111">La manera más sencilla de definir el punto de unión de una extensión es convertir la carpeta raíz en una subcarpeta de una carpeta virtual del sistema.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-111">The simplest way to define an extension's junction point is to make the root folder a subfolder of a system virtual folder.</span></span> <span data-ttu-id="9d3eb-112">Este tipo de punto de Unión se conoce como *punto de Unión virtual*.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-112">This type of junction point is referred to as a *virtual junction point*.</span></span> <span data-ttu-id="9d3eb-113">Las carpetas **Desktop** y **mi PC** son las ubicaciones típicas de los puntos de Unión virtuales, pero también puede definir un punto de Unión virtual en un equipo remoto o en las carpetas **mis sitios de red**, **Internet Explorer** y **Panel de control** .</span><span class="sxs-lookup"><span data-stu-id="9d3eb-113">The **Desktop** and **My Computer** folders are the typical locations for virtual junction points, but you can also define a virtual junction point on a remote computer or under the **My Network Places**, **Internet Explorer**, and **Control Panel** folders.</span></span>

<span data-ttu-id="9d3eb-114">Para definir un punto de Unión virtual, cree una subclave de la clave que represente la carpeta virtual adecuada y asígnele el nombre de la forma de cadena del identificador de clase (CLSID) de la extensión.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-114">To define a virtual junction point, create a subkey of the key that represents the appropriate virtual folder and name it with the string form of your extension's class identifier (CLSID).</span></span> <span data-ttu-id="9d3eb-115">El CLSID registrado aparecería de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-115">The registered CLSID would appear as follows.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  Virtual Folder Name
                     NameSpace
                        {Extension CLSID}
                           (Default) = Junction Point Name
```

<span data-ttu-id="9d3eb-116">El nombre de la *carpeta virtual* es una de las subclaves de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-116">*Virtual Folder Name* is one of the subkeys in the following table.</span></span>



| <span data-ttu-id="9d3eb-117">Ubicación</span><span class="sxs-lookup"><span data-stu-id="9d3eb-117">Location</span></span>          | <span data-ttu-id="9d3eb-118">Nombre de carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9d3eb-118">Virtual Folder Name</span></span>                        |
|-------------------|--------------------------------------------|
| <span data-ttu-id="9d3eb-119">Panel de control</span><span class="sxs-lookup"><span data-stu-id="9d3eb-119">Control Panel</span></span>     | <span data-ttu-id="9d3eb-120">**ControlPanel**</span><span class="sxs-lookup"><span data-stu-id="9d3eb-120">**ControlPanel**</span></span>                           |
| <span data-ttu-id="9d3eb-121">Escritorio</span><span class="sxs-lookup"><span data-stu-id="9d3eb-121">Desktop</span></span>           | <span data-ttu-id="9d3eb-122">**Dispositivo de escritorio**</span><span class="sxs-lookup"><span data-stu-id="9d3eb-122">**Desktop**</span></span>                                |
| <span data-ttu-id="9d3eb-123">Red completa</span><span class="sxs-lookup"><span data-stu-id="9d3eb-123">Entire Network</span></span>    | <span data-ttu-id="9d3eb-124">**NetworkNeighborhood** \\ **EntireNetwork**</span><span class="sxs-lookup"><span data-stu-id="9d3eb-124">**NetworkNeighborhood**\\**EntireNetwork**</span></span> |
| <span data-ttu-id="9d3eb-125">Mi PC</span><span class="sxs-lookup"><span data-stu-id="9d3eb-125">My Computer</span></span>       | <span data-ttu-id="9d3eb-126">**MyComputer**</span><span class="sxs-lookup"><span data-stu-id="9d3eb-126">**MyComputer**</span></span>                             |
| <span data-ttu-id="9d3eb-127">Mis sitios de red</span><span class="sxs-lookup"><span data-stu-id="9d3eb-127">My Network Places</span></span> | <span data-ttu-id="9d3eb-128">**NetworkNeighborhood**</span><span class="sxs-lookup"><span data-stu-id="9d3eb-128">**NetworkNeighborhood**</span></span>                    |
| <span data-ttu-id="9d3eb-129">Equipo remoto</span><span class="sxs-lookup"><span data-stu-id="9d3eb-129">Remote Computer</span></span>   | <span data-ttu-id="9d3eb-130">**Equiporemoto**</span><span class="sxs-lookup"><span data-stu-id="9d3eb-130">**RemoteComputer**</span></span>                         |
| <span data-ttu-id="9d3eb-131">Archivos de usuarios</span><span class="sxs-lookup"><span data-stu-id="9d3eb-131">Users Files</span></span>       | <span data-ttu-id="9d3eb-132">**UsersFiles**</span><span class="sxs-lookup"><span data-stu-id="9d3eb-132">**UsersFiles**</span></span>                             |



 

<span data-ttu-id="9d3eb-133">Las extensiones remotas se deben inicializar con [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).</span><span class="sxs-lookup"><span data-stu-id="9d3eb-133">Remote extensions must be initialized with [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).</span></span>

## <a name="using-file-system-folders-as-junction-points"></a><span data-ttu-id="9d3eb-134">Usar carpetas del sistema de archivos como puntos de Unión</span><span class="sxs-lookup"><span data-stu-id="9d3eb-134">Using File System Folders as Junction Points</span></span>

<span data-ttu-id="9d3eb-135">Hay dos maneras de definir carpetas del sistema de archivos como puntos de Unión.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-135">There are two ways to define file system folders as junction points.</span></span> <span data-ttu-id="9d3eb-136">El enfoque más sencillo consiste en crear una carpeta en la ubicación adecuada y anexar un punto al nombre de la carpeta, seguido de la forma de cadena del CLSID de la extensión.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-136">The simplest approach is to create a folder in the appropriate location and append a period to the folder's name, followed by the string form of the CLSID of your extension.</span></span> <span data-ttu-id="9d3eb-137">Solo el nombre de la carpeta será visible en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-137">Only the folder name will be visible in Windows Explorer.</span></span> <span data-ttu-id="9d3eb-138">En el ejemplo siguiente se crea un punto de unión con un nombre para mostrar de mi carpeta.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-138">The following example creates a junction point with a display name of MyFolder.</span></span>


```
MyFolder.{Extension CLSID}
```



<span data-ttu-id="9d3eb-139">Como alternativa, puede definir una carpeta con el nombre convencional como punto de Unión:</span><span class="sxs-lookup"><span data-stu-id="9d3eb-139">Alternatively, you can define a conventionally named folder as a junction point by:</span></span>

-   <span data-ttu-id="9d3eb-140">Crear la carpeta de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-140">Making the folder read-only.</span></span>
-   <span data-ttu-id="9d3eb-141">Convertir la carpeta en una carpeta del sistema mediante una llamada a [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).</span><span class="sxs-lookup"><span data-stu-id="9d3eb-141">Making the folder a system folder by calling [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).</span></span>
-   <span data-ttu-id="9d3eb-142">Colocar un archivo de Desktop.ini oculto en la carpeta que incluye el CLSID de la extensión.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-142">Placing a hidden Desktop.ini file in the folder that includes the extension's CLSID.</span></span>

<span data-ttu-id="9d3eb-143">Desktop.ini es un archivo de texto estándar que se puede Agregar a cualquier carpeta para personalizar determinados aspectos del comportamiento de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-143">Desktop.ini is a standard text file that can be added to any folder to customize certain aspects of the folder's behavior.</span></span> <span data-ttu-id="9d3eb-144">Para obtener una explicación general sobre cómo usar este archivo, consulte [Cómo personalizar carpetas con Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="9d3eb-144">For a general discussion of how to use this file, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span> <span data-ttu-id="9d3eb-145">Para definir una carpeta como punto de Unión, el \[ . \] La sección ShellClassInfo de Desktop.ini debe contener el CLSID de la extensión como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="9d3eb-145">To define a folder as a junction point, the \[.ShellClassInfo\] section of Desktop.ini must contain the extension's CLSID as follows:</span></span>


```
[.ShellClassInfo]
CLSID={Extension CLSID}
```



## <a name="opening-a-view-of-a-namespace-extension"></a><span data-ttu-id="9d3eb-146">Abrir una vista de una extensión de espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9d3eb-146">Opening a View of a Namespace Extension</span></span>

<span data-ttu-id="9d3eb-147">Cuando un usuario examina un punto de Unión, el explorador de Windows crea automáticamente una vista de la carpeta raíz.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-147">When a user browses into a junction point, Windows Explorer automatically creates a view of the root folder.</span></span> <span data-ttu-id="9d3eb-148">También puede crear una vista mediante el inicio explícito de Explorer.exe con el CLSID de la extensión como argumento.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-148">You can also create a view by explicitly launching Explorer.exe with the extension's CLSID as an argument.</span></span> <span data-ttu-id="9d3eb-149">Por ejemplo, puede usar este enfoque para iniciar una vista de una extensión desde un menú contextual o un acceso directo.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-149">You can, for instance, use this approach to launch a view of an extension from a shortcut menu or shortcut.</span></span> <span data-ttu-id="9d3eb-150">Por ejemplo, para iniciar una vista de una extensión que incluye una vista de árbol, puede utilizar la siguiente cadena de comandos.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-150">For example, to launch a view of MyExtension that includes a tree view, you can use the following command string.</span></span>


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID}
```



<span data-ttu-id="9d3eb-151">Se puede usar una cadena de comandos alternativa para iniciar una vista de un objeto dentro de la extensión.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-151">An alternative command string can be used to launch a view of an object within the extension.</span></span> <span data-ttu-id="9d3eb-152">Esta característica sería útil, por ejemplo, para una extensión que utiliza una vista de carpeta para permitir que los usuarios vean el contenido de uno de varios archivos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-152">This feature would be useful, for instance, for an extension that uses a folder view to allow users to view the contents of one of a number of compressed files.</span></span>


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID},objectname
```



<span data-ttu-id="9d3eb-153">El parámetro *objectname* es el nombre del objeto que se va a ver.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-153">The *objectname* parameter is the name of the object that is to be viewed.</span></span> <span data-ttu-id="9d3eb-154">El explorador de Windows convierte el nombre en su PIDL correspondiente y pasa el PIDL al método [**IPersistFolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) del objeto de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-154">Windows Explorer converts the name to its corresponding PIDL and passes the PIDL to the new folder object's [**IPersistFolder::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) method.</span></span>

> [!Note]  
> <span data-ttu-id="9d3eb-155">La cadena CLSID debe ir precedida de un par de dos puntos (::) o se producirá un error en el comando.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-155">The CLSID string must be preceded by a pair of colons (::) or the command will fail.</span></span> <span data-ttu-id="9d3eb-156">La marca de barra diagonal-e (/e) utilizada en las dos líneas de comandos de ejemplo mostradas anteriormente indica al explorador de Windows que muestre una vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-156">The slash-e (/e) flag used in the two sample command lines shown previously instructs Windows Explorer to display a tree view.</span></span> <span data-ttu-id="9d3eb-157">La marca se debe separar entre los dos dos puntos mediante una coma.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-157">The flag must be separated from the two colons by a comma.</span></span> <span data-ttu-id="9d3eb-158">Si no desea una vista de árbol, omita la marca/e y la coma.</span><span class="sxs-lookup"><span data-stu-id="9d3eb-158">If you do not want a tree view, omit the /e flag and the comma.</span></span>

 

 

 



