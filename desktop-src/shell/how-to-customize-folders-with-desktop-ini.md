---
description: Personalización de la apariencia y el comportamiento de una carpeta individual con Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Personalización de carpetas con Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a671b169c4b025683cdd220ee3a920b4d592488
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581753"
---
# <a name="how-to-customize-folders-with-desktopini"></a><span data-ttu-id="d1b2c-103">Personalización de carpetas con Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="d1b2c-103">How to Customize Folders with Desktop.ini</span></span>

<span data-ttu-id="d1b2c-104">Las carpetas del sistema de archivos se muestran normalmente con un icono estándar y un conjunto de propiedades, que especifican, por ejemplo, si la carpeta se comparte.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-104">File system folders are commonly displayed with a standard icon and set of properties, which specify, for instance, whether the folder is shared.</span></span> <span data-ttu-id="d1b2c-105">Puede personalizar la apariencia y el comportamiento de una carpeta individual mediante la creación de un Desktop.ini para esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-105">You can customize the appearance and behavior of an individual folder by creating a Desktop.ini file for that folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="d1b2c-106">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="d1b2c-106">Instructions</span></span>

### <a name="using-desktopini-files"></a><span data-ttu-id="d1b2c-107">Uso de Desktop.ini files</span><span class="sxs-lookup"><span data-stu-id="d1b2c-107">Using Desktop.ini Files</span></span>

<span data-ttu-id="d1b2c-108">Normalmente, las carpetas se muestran con el icono de carpeta estándar.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-108">Folders are normally displayed with the standard folder icon.</span></span> <span data-ttu-id="d1b2c-109">Un uso común del archivo Desktop.ini es asignar un icono personalizado o una imagen en miniatura a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-109">A common use of the Desktop.ini file is to assign a custom icon or thumbnail image to a folder.</span></span> <span data-ttu-id="d1b2c-110">También puede usar Desktop.ini para crear  una información que muestre información sobre la carpeta y controle algunos aspectos del comportamiento de la carpeta, como especificar nombres localizados para la carpeta o los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-110">You can also use Desktop.ini to create an *infotip* that displays information about the folder and controls some aspects of the folder's behavior, such as specifying localized names for the folder or items in the folder.</span></span>

<span data-ttu-id="d1b2c-111">**Use el procedimiento siguiente para personalizar el estilo de una carpeta con Desktop.ini:**</span><span class="sxs-lookup"><span data-stu-id="d1b2c-111">**Use the following procedure to customize a folder's style with Desktop.ini:**</span></span>

1.  <span data-ttu-id="d1b2c-112">Use [**PathMakeSystemFolder para**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) convertir la carpeta en una carpeta del sistema.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-112">Use [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) to make the folder a system folder.</span></span> <span data-ttu-id="d1b2c-113">Esto establece el bit de solo lectura en la carpeta para indicar que el comportamiento especial reservado para Desktop.ini debe estar habilitado.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-113">This sets the read-only bit on the folder to indicate that the special behavior reserved for Desktop.ini should be enabled.</span></span> <span data-ttu-id="d1b2c-114">También puede convertir una carpeta en una carpeta del sistema desde la línea de comandos mediante **attrib +s** *FolderName*.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-114">You can also make a folder a system folder from the command line by using **attrib +s** *FolderName*.</span></span>
2.  <span data-ttu-id="d1b2c-115">Cree un Desktop.ini para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-115">Create a Desktop.ini file for the folder.</span></span> <span data-ttu-id="d1b2c-116">Debe marcarlo como oculto *y* *sistema para* asegurarse de que está oculto para los usuarios normales.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-116">You should mark it as *hidden* and *system* to ensure that it is hidden from normal users.</span></span>
3.  <span data-ttu-id="d1b2c-117">Asegúrese de que Desktop.ini archivo que cree esté en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-117">Make sure the Desktop.ini file that you create is in the Unicode format.</span></span> <span data-ttu-id="d1b2c-118">Esto es necesario para almacenar las cadenas localizadas que se pueden mostrar a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-118">This is necessary to store the localized strings that can be displayed to users.</span></span>

### <a name="creating-a-desktopini-file"></a><span data-ttu-id="d1b2c-119">Creación de un Desktop.ini archivo</span><span class="sxs-lookup"><span data-stu-id="d1b2c-119">Creating a Desktop.ini File</span></span>

<span data-ttu-id="d1b2c-120">El Desktop.ini es un archivo de texto que permite especificar cómo se ve una carpeta del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-120">The Desktop.ini file is a text file that allows you to specify how a file system folder is viewed.</span></span> <span data-ttu-id="d1b2c-121">. \[ La sección ShellClassInfo permite personalizar la vista de la carpeta mediante la asignación de \] valores a varias entradas:</span><span class="sxs-lookup"><span data-stu-id="d1b2c-121">The \[.ShellClassInfo\] section, allows you to customize the folder's view by assigning values to several entries:</span></span>

| <span data-ttu-id="d1b2c-122">Value</span><span class="sxs-lookup"><span data-stu-id="d1b2c-122">Value</span></span>             | <span data-ttu-id="d1b2c-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1b2c-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b2c-124">**ConfirmFileOp**</span><span class="sxs-lookup"><span data-stu-id="d1b2c-124">**ConfirmFileOp**</span></span> | <span data-ttu-id="d1b2c-125">Establezca esta entrada en 0 para evitar una advertencia "Está eliminando una carpeta del sistema" al eliminar o mover la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-125">Set this entry to 0 to avoid a "You Are Deleting a System Folder" warning when deleting or moving the folder.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d1b2c-126">**No compartir**</span><span class="sxs-lookup"><span data-stu-id="d1b2c-126">**NoSharing**</span></span>     | <span data-ttu-id="d1b2c-127">No se admite en Windows Vista o versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-127">Not supported under Windows Vista or later.</span></span> <span data-ttu-id="d1b2c-128">Establezca esta entrada en 1 para evitar que la carpeta se comparta.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-128">Set this entry to 1 to prevent the folder from being shared.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d1b2c-129">**IconFile**</span><span class="sxs-lookup"><span data-stu-id="d1b2c-129">**IconFile**</span></span>      | <span data-ttu-id="d1b2c-130">Si desea especificar un icono personalizado para la carpeta, establezca esta entrada en el nombre de archivo del icono.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-130">If you want to specify a custom icon for the folder, set this entry to the icon's file name.</span></span> <span data-ttu-id="d1b2c-131">Se prefiere la extensión de nombre de archivo .ico, pero también es posible especificar .bmp archivos o .exe y .dll archivos que contienen iconos.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-131">The .ico file name extension is preferred, but it is also possible to specify .bmp files, or .exe and .dll files that contain icons.</span></span> <span data-ttu-id="d1b2c-132">Si usa una ruta de acceso relativa, el icono está disponible para las personas que ven la carpeta a través de la red.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-132">If you use a relative path, the icon is available to people who view the folder over the network.</span></span> <span data-ttu-id="d1b2c-133">También debe establecer la entrada **IconIndex.**</span><span class="sxs-lookup"><span data-stu-id="d1b2c-133">You must also set the **IconIndex** entry.</span></span> |
| <span data-ttu-id="d1b2c-134">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="d1b2c-134">**IconIndex**</span></span>     | <span data-ttu-id="d1b2c-135">Establezca esta entrada para especificar el índice de un icono personalizado.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-135">Set this entry to specify the index for a custom icon.</span></span> <span data-ttu-id="d1b2c-136">Si el archivo asignado a **IconFile** solo contiene un solo icono, establezca **IconIndex** en 0.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-136">If the file assigned to **IconFile** only contains a single icon, set **IconIndex** to 0.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="d1b2c-137">**InfoTip**</span><span class="sxs-lookup"><span data-stu-id="d1b2c-137">**InfoTip**</span></span>       | <span data-ttu-id="d1b2c-138">Establezca esta entrada en una cadena de texto informativo.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-138">Set this entry to an informational text string.</span></span> <span data-ttu-id="d1b2c-139">Se muestra como información cuando el cursor mantiene el puntero sobre la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-139">It is displayed as an infotip when the cursor hovers over the folder.</span></span> <span data-ttu-id="d1b2c-140">Si el usuario hace clic en la carpeta, el texto de la información se muestra en el bloque de información de la carpeta, debajo de la información estándar.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-140">If the user clicks the folder, the information text is displayed in the folder's information block, below the standard information.</span></span>                                                                                                                      |



 

<span data-ttu-id="d1b2c-141">Las siguientes ilustraciones son de la carpeta Música con un archivo Desktop.ini personalizado.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-141">The following illustrations are of the Music folder with a custom Desktop.ini file.</span></span> <span data-ttu-id="d1b2c-142">La carpeta ahora:</span><span class="sxs-lookup"><span data-stu-id="d1b2c-142">The folder now:</span></span>

-   <span data-ttu-id="d1b2c-143">Tiene un icono personalizado.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-143">Has a custom icon.</span></span>
-   <span data-ttu-id="d1b2c-144">No muestra una advertencia "Está eliminando una carpeta del sistema" si la carpeta se mueve o elimina.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-144">Does not display a "You Are Deleting a System Folder" warning if the folder is moved or deleted.</span></span>
-   <span data-ttu-id="d1b2c-145">No se puede compartir.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-145">Cannot be shared.</span></span>
-   <span data-ttu-id="d1b2c-146">Muestra texto informativo cuando el cursor mantiene el puntero sobre la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-146">Displays informational text when the cursor hovers over the folder.</span></span>

<span data-ttu-id="d1b2c-147">Las opciones de carpeta de las ilustraciones siguientes se establecen para mostrar los archivos ocultos para que Desktop.ini esté visible.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-147">The folder options in the following illustrations are set to show hidden files so that Desktop.ini is visible.</span></span> <span data-ttu-id="d1b2c-148">La carpeta tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="d1b2c-148">The folder looks like this:</span></span>

![captura de pantalla de la carpeta con icono personalizado](images/webview4.jpg)

<span data-ttu-id="d1b2c-150">Cuando el cursor mantiene el puntero sobre la carpeta, se muestra la información.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-150">When the cursor hovers over the folder, the infotip is displayed.</span></span>

![captura de pantalla de la carpeta con información](images/webview6.jpg)

<span data-ttu-id="d1b2c-152">El icono personalizado reemplaza el icono de carpeta donde aparezca el nombre de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-152">The custom icon replaces the folder icon everywhere the folder name appears.</span></span>

![captura de pantalla del icono personalizado reemplazando el icono de carpeta](images/webview5.jpg)

<span data-ttu-id="d1b2c-154">El siguiente desktop.ini se usó para personalizar la carpeta Música, como se muestra en las ilustraciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="d1b2c-154">The following desktop.ini file was used to customize the Music folder, as seen in the preceding illustrations.</span></span>


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



