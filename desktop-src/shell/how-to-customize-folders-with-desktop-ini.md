---
description: Personalizar la apariencia y el comportamiento de una carpeta individual con Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Cómo personalizar carpetas con Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaac3e6a96257e63b5e4210da0aa6e6e1db77eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560229"
---
# <a name="how-to-customize-folders-with-desktopini"></a><span data-ttu-id="a2835-103">Cómo personalizar carpetas con Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="a2835-103">How to Customize Folders with Desktop.ini</span></span>

<span data-ttu-id="a2835-104">Las carpetas del sistema de archivos se muestran normalmente con un icono y un conjunto de propiedades estándar que especifican, por ejemplo, si la carpeta está compartida.</span><span class="sxs-lookup"><span data-stu-id="a2835-104">File system folders are commonly displayed with a standard icon and set of properties, which specify, for instance, whether the folder is shared.</span></span> <span data-ttu-id="a2835-105">Puede personalizar la apariencia y el comportamiento de una carpeta individual creando un archivo de Desktop.ini para esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="a2835-105">You can customize the appearance and behavior of an individual folder by creating a Desktop.ini file for that folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="a2835-106">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="a2835-106">Instructions</span></span>

### <a name="using-desktopini-files"></a><span data-ttu-id="a2835-107">Usar archivos de Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="a2835-107">Using Desktop.ini Files</span></span>

<span data-ttu-id="a2835-108">Las carpetas se muestran normalmente con el icono de la carpeta estándar.</span><span class="sxs-lookup"><span data-stu-id="a2835-108">Folders are normally displayed with the standard folder icon.</span></span> <span data-ttu-id="a2835-109">Un uso común del archivo Desktop.ini es asignar un icono personalizado o una imagen en miniatura a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a2835-109">A common use of the Desktop.ini file is to assign a custom icon or thumbnail image to a folder.</span></span> <span data-ttu-id="a2835-110">También puede usar Desktop.ini para crear un recuadro informativo *que muestra* información sobre la carpeta y controla algunos aspectos del comportamiento de la carpeta, como la especificación de nombres localizados para la carpeta o los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a2835-110">You can also use Desktop.ini to create an *infotip* that displays information about the folder and controls some aspects of the folder's behavior, such as specifying localized names for the folder or items in the folder.</span></span>

<span data-ttu-id="a2835-111">**Utilice el siguiente procedimiento para personalizar el estilo de una carpeta con Desktop.ini:**</span><span class="sxs-lookup"><span data-stu-id="a2835-111">**Use the following procedure to customize a folder's style with Desktop.ini:**</span></span>

1.  <span data-ttu-id="a2835-112">Use [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) para convertir la carpeta en una carpeta del sistema.</span><span class="sxs-lookup"><span data-stu-id="a2835-112">Use [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) to make the folder a system folder.</span></span> <span data-ttu-id="a2835-113">Esto establece el bit de solo lectura en la carpeta para indicar que debe habilitarse el comportamiento especial reservado para Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="a2835-113">This sets the read-only bit on the folder to indicate that the special behavior reserved for Desktop.ini should be enabled.</span></span> <span data-ttu-id="a2835-114">También puede convertir una carpeta en una carpeta del sistema desde la línea de comandos mediante **attrib + s** *nombreDeCarpeta*.</span><span class="sxs-lookup"><span data-stu-id="a2835-114">You can also make a folder a system folder from the command line by using **attrib +s** *FolderName*.</span></span>
2.  <span data-ttu-id="a2835-115">Cree un archivo de Desktop.ini para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a2835-115">Create a Desktop.ini file for the folder.</span></span> <span data-ttu-id="a2835-116">Debe marcarlo como *oculto* y *sistema* para asegurarse de que está oculto para los usuarios normales.</span><span class="sxs-lookup"><span data-stu-id="a2835-116">You should mark it as *hidden* and *system* to ensure that it is hidden from normal users.</span></span>
3.  <span data-ttu-id="a2835-117">Asegúrese de que el archivo de Desktop.ini que crea está en el formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a2835-117">Make sure the Desktop.ini file that you create is in the Unicode format.</span></span> <span data-ttu-id="a2835-118">Esto es necesario para almacenar las cadenas traducidas que se pueden mostrar a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="a2835-118">This is necessary to store the localized strings that can be displayed to users.</span></span>

### <a name="creating-a-desktopini-file"></a><span data-ttu-id="a2835-119">Crear un archivo de Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="a2835-119">Creating a Desktop.ini File</span></span>

<span data-ttu-id="a2835-120">El archivo Desktop.ini es un archivo de texto que le permite especificar cómo se ve una carpeta del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="a2835-120">The Desktop.ini file is a text file that allows you to specify how a file system folder is viewed.</span></span> <span data-ttu-id="a2835-121">El \[ . \] La sección ShellClassInfo permite personalizar la vista de la carpeta asignando valores a varias entradas:</span><span class="sxs-lookup"><span data-stu-id="a2835-121">The \[.ShellClassInfo\] section, allows you to customize the folder's view by assigning values to several entries:</span></span>

|                   |                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2835-122">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="a2835-122">**Entry**</span></span>         | <span data-ttu-id="a2835-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a2835-123">**Value**</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="a2835-124">**ConfirmFileOp**</span><span class="sxs-lookup"><span data-stu-id="a2835-124">**ConfirmFileOp**</span></span> | <span data-ttu-id="a2835-125">Establezca esta entrada en 0 para evitar que se produzca una advertencia al eliminar una carpeta del sistema al eliminar o mover la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a2835-125">Set this entry to 0 to avoid a "You Are Deleting a System Folder" warning when deleting or moving the folder.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="a2835-126">**Uso compartido**</span><span class="sxs-lookup"><span data-stu-id="a2835-126">**NoSharing**</span></span>     | <span data-ttu-id="a2835-127">No se admite en Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="a2835-127">Not supported under Windows Vista or later.</span></span> <span data-ttu-id="a2835-128">Establezca esta entrada en 1 para evitar que se comparta la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a2835-128">Set this entry to 1 to prevent the folder from being shared.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="a2835-129">**IconFile**</span><span class="sxs-lookup"><span data-stu-id="a2835-129">**IconFile**</span></span>      | <span data-ttu-id="a2835-130">Si desea especificar un icono personalizado para la carpeta, establezca esta entrada en el nombre de archivo del icono.</span><span class="sxs-lookup"><span data-stu-id="a2835-130">If you want to specify a custom icon for the folder, set this entry to the icon's file name.</span></span> <span data-ttu-id="a2835-131">Se prefiere la extensión de nombre de archivo. ico, pero también es posible especificar archivos. bmp, o archivos. exe y. dll que contengan iconos.</span><span class="sxs-lookup"><span data-stu-id="a2835-131">The .ico file name extension is preferred, but it is also possible to specify .bmp files, or .exe and .dll files that contain icons.</span></span> <span data-ttu-id="a2835-132">Si usa una ruta de acceso relativa, el icono está disponible para los usuarios que ven la carpeta a través de la red.</span><span class="sxs-lookup"><span data-stu-id="a2835-132">If you use a relative path, the icon is available to people who view the folder over the network.</span></span> <span data-ttu-id="a2835-133">También debe establecer la entrada de **IconIndex** .</span><span class="sxs-lookup"><span data-stu-id="a2835-133">You must also set the **IconIndex** entry.</span></span> |
| <span data-ttu-id="a2835-134">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="a2835-134">**IconIndex**</span></span>     | <span data-ttu-id="a2835-135">Establezca esta entrada para especificar el índice de un icono personalizado.</span><span class="sxs-lookup"><span data-stu-id="a2835-135">Set this entry to specify the index for a custom icon.</span></span> <span data-ttu-id="a2835-136">Si el archivo asignado a **IconFile** solo contiene un único icono, establezca **IconIndex** en 0.</span><span class="sxs-lookup"><span data-stu-id="a2835-136">If the file assigned to **IconFile** only contains a single icon, set **IconIndex** to 0.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="a2835-137">**InfoTip**</span><span class="sxs-lookup"><span data-stu-id="a2835-137">**InfoTip**</span></span>       | <span data-ttu-id="a2835-138">Establezca esta entrada en una cadena de texto informativo.</span><span class="sxs-lookup"><span data-stu-id="a2835-138">Set this entry to an informational text string.</span></span> <span data-ttu-id="a2835-139">Se muestra como un recuadro informativo cuando el cursor se mantiene sobre la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a2835-139">It is displayed as an infotip when the cursor hovers over the folder.</span></span> <span data-ttu-id="a2835-140">Si el usuario hace clic en la carpeta, se muestra el texto de información en el bloque de información de la carpeta, debajo de la información estándar.</span><span class="sxs-lookup"><span data-stu-id="a2835-140">If the user clicks the folder, the information text is displayed in the folder's information block, below the standard information.</span></span>                                                                                                                      |



 

<span data-ttu-id="a2835-141">Las siguientes ilustraciones son de la carpeta música con un archivo de Desktop.ini personalizado.</span><span class="sxs-lookup"><span data-stu-id="a2835-141">The following illustrations are of the Music folder with a custom Desktop.ini file.</span></span> <span data-ttu-id="a2835-142">La carpeta ahora:</span><span class="sxs-lookup"><span data-stu-id="a2835-142">The folder now:</span></span>

-   <span data-ttu-id="a2835-143">Tiene un icono personalizado.</span><span class="sxs-lookup"><span data-stu-id="a2835-143">Has a custom icon.</span></span>
-   <span data-ttu-id="a2835-144">No muestra la advertencia "se está eliminando una carpeta de sistema" si la carpeta se mueve o se elimina.</span><span class="sxs-lookup"><span data-stu-id="a2835-144">Does not display a "You Are Deleting a System Folder" warning if the folder is moved or deleted.</span></span>
-   <span data-ttu-id="a2835-145">No se puede compartir.</span><span class="sxs-lookup"><span data-stu-id="a2835-145">Cannot be shared.</span></span>
-   <span data-ttu-id="a2835-146">Muestra texto informativo cuando el cursor se mantiene sobre la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a2835-146">Displays informational text when the cursor hovers over the folder.</span></span>

<span data-ttu-id="a2835-147">Las opciones de carpeta de las ilustraciones siguientes se establecen para mostrar los archivos ocultos de modo que Desktop.ini esté visible.</span><span class="sxs-lookup"><span data-stu-id="a2835-147">The folder options in the following illustrations are set to show hidden files so that Desktop.ini is visible.</span></span> <span data-ttu-id="a2835-148">La carpeta tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="a2835-148">The folder looks like this:</span></span>

![captura de pantalla de la carpeta con icono personalizado](images/webview4.jpg)

<span data-ttu-id="a2835-150">Cuando el cursor se mantiene sobre la carpeta, se muestra el recuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="a2835-150">When the cursor hovers over the folder, the infotip is displayed.</span></span>

![captura de pantalla de la carpeta con un recuadro informativo](images/webview6.jpg)

<span data-ttu-id="a2835-152">El icono personalizado reemplaza el icono de carpeta en todas partes donde aparece el nombre de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a2835-152">The custom icon replaces the folder icon everywhere the folder name appears.</span></span>

![captura de pantalla del icono personalizado que reemplaza el icono de carpeta](images/webview5.jpg)

<span data-ttu-id="a2835-154">El siguiente archivo de desktop.ini se usó para personalizar la carpeta música, tal como se ha descrito en las ilustraciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="a2835-154">The following desktop.ini file was used to customize the Music folder, as seen in the preceding illustrations.</span></span>


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



