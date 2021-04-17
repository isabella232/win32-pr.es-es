---
description: La acción InstallFiles copia los archivos especificados en la tabla de archivos del directorio de origen en el directorio de destino.
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: InstallFiles (acción)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2a0206ec5a64974f27375e175f25ce1888b430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666732"
---
# <a name="installfiles-action"></a><span data-ttu-id="8075d-103">InstallFiles (acción)</span><span class="sxs-lookup"><span data-stu-id="8075d-103">InstallFiles Action</span></span>

<span data-ttu-id="8075d-104">La acción InstallFiles copia los archivos especificados en la tabla de archivos del directorio de origen en el directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="8075d-104">The InstallFiles action copies files specified in the File table from the source directory to the destination directory.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8075d-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="8075d-105">Sequence Restrictions</span></span>

<span data-ttu-id="8075d-106">La acción InstallFiles debe aparecer después de la acción [InstallValidate](installvalidate-action.md) y antes de cualquier acción dependiente de archivos.</span><span class="sxs-lookup"><span data-stu-id="8075d-106">The InstallFiles action must come after the [InstallValidate](installvalidate-action.md) action and before any file-dependent actions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8075d-107">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="8075d-107">ActionData Messages</span></span>



| <span data-ttu-id="8075d-108">Campo</span><span class="sxs-lookup"><span data-stu-id="8075d-108">Field</span></span> | <span data-ttu-id="8075d-109">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="8075d-109">Description of action data</span></span>                      |
|-------|-------------------------------------------------|
| <span data-ttu-id="8075d-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8075d-110">\[1\]</span></span> | <span data-ttu-id="8075d-111">Identificador del archivo instalado.</span><span class="sxs-lookup"><span data-stu-id="8075d-111">Identifier of installed file.</span></span>                   |
| <span data-ttu-id="8075d-112">\[6\]</span><span class="sxs-lookup"><span data-stu-id="8075d-112">\[6\]</span></span> | <span data-ttu-id="8075d-113">Tamaño del archivo instalado en bytes.</span><span class="sxs-lookup"><span data-stu-id="8075d-113">Size of installed file in bytes.</span></span>                |
| <span data-ttu-id="8075d-114">\[9\]</span><span class="sxs-lookup"><span data-stu-id="8075d-114">\[9\]</span></span> | <span data-ttu-id="8075d-115">Identificador del directorio que contiene el archivo instalado.</span><span class="sxs-lookup"><span data-stu-id="8075d-115">Identifier of directory holding installed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8075d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8075d-116">Remarks</span></span>

<span data-ttu-id="8075d-117">La acción InstallFiles opera en los archivos especificados en la [tabla File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="8075d-117">The InstallFiles action operates on files specified in the [File table](file-table.md).</span></span> <span data-ttu-id="8075d-118">Cada archivo se instala en función del estado de instalación del componente asociado del archivo en la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8075d-118">Each file is installed based on the installation state of the file's associated component in the [Component table](component-table.md).</span></span> <span data-ttu-id="8075d-119">Solo se pueden copiar los archivos cuyos componentes se resuelven en el estado **msiInstallStatelocal** .</span><span class="sxs-lookup"><span data-stu-id="8075d-119">Only those files whose components are resolved to the **msiInstallStatelocal** state are eligible for copying.</span></span>

<span data-ttu-id="8075d-120">La acción InstallFiles implementa las siguientes columnas de la tabla File.</span><span class="sxs-lookup"><span data-stu-id="8075d-120">The InstallFiles action implements the following columns of the File table.</span></span>

-   <span data-ttu-id="8075d-121">La columna FileName especifica el nombre del archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="8075d-121">The FileName column specifies the target file name.</span></span>
-   <span data-ttu-id="8075d-122">La columna version especifica la versión del archivo.</span><span class="sxs-lookup"><span data-stu-id="8075d-122">The Version column specifies the file version.</span></span>
-   <span data-ttu-id="8075d-123">La columna atributos especifica los bits del indicador de atributo de instalación y archivo.</span><span class="sxs-lookup"><span data-stu-id="8075d-123">The Attributes column specifies the file and installation attribute flag bits.</span></span>
-   <span data-ttu-id="8075d-124">La columna archivo especifica el token de archivo único.</span><span class="sxs-lookup"><span data-stu-id="8075d-124">The File column specifies the unique file token.</span></span>
-   <span data-ttu-id="8075d-125">La columna archivo especifica el tamaño de archivo sin comprimir en bytes.</span><span class="sxs-lookup"><span data-stu-id="8075d-125">The FileSize column specifies the uncompressed file size in bytes.</span></span>
-   <span data-ttu-id="8075d-126">La columna Language especifica el identificador de idioma del archivo.</span><span class="sxs-lookup"><span data-stu-id="8075d-126">The Language column specifies the file language identifier.</span></span>
-   <span data-ttu-id="8075d-127">La columna Sequence especifica el número de secuencia en el medio.</span><span class="sxs-lookup"><span data-stu-id="8075d-127">The Sequence column specifies the sequence number on media.</span></span>

<span data-ttu-id="8075d-128">La acción InstallFiles implementa las siguientes columnas de la tabla de componentes.</span><span class="sxs-lookup"><span data-stu-id="8075d-128">The InstallFiles action implements the following columns of the Component table.</span></span>

-   <span data-ttu-id="8075d-129">La \_ columna Directory especifica una referencia a un elemento de [tabla de directorio](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="8075d-129">The Directory\_ column specifies a reference to a [Directory table](directory-table.md) item.</span></span>
-   <span data-ttu-id="8075d-130">La columna componente especifica un nombre único para el elemento de componente.</span><span class="sxs-lookup"><span data-stu-id="8075d-130">The Component column specifies a unique name for the component item.</span></span>

<span data-ttu-id="8075d-131">El archivo especificado solo se copia si se cumple una de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="8075d-131">The specified file is copied only if one of the following is true:</span></span>

-   <span data-ttu-id="8075d-132">El archivo no está instalado actualmente en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="8075d-132">The file is not currently installed on the local computer.</span></span>
-   <span data-ttu-id="8075d-133">El archivo está en el equipo local, pero tiene un número de versión inferior al del archivo en la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="8075d-133">The file is on the local computer but has a lower version number than the file in the [File table](file-table.md).</span></span>
-   <span data-ttu-id="8075d-134">El archivo está en el equipo local, pero no hay ningún número de versión asociado.</span><span class="sxs-lookup"><span data-stu-id="8075d-134">The file is on the local computer, but there is no associated version number.</span></span>

<span data-ttu-id="8075d-135">El directorio de origen de cada archivo que se va a copiar viene determinado por el sourceMode, que a su vez depende del valor de la columna Cabinet de la tabla de medios.</span><span class="sxs-lookup"><span data-stu-id="8075d-135">The source directory for each file to be copied is determined by the sourceMode, which in turn depends on the value in the Cabinet column of the Media table.</span></span> <span data-ttu-id="8075d-136">Para obtener una descripción completa del modo de origen, vea la [tabla de medios](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="8075d-136">For a full discussion of the source mode, see the [Media table](media-table.md).</span></span>

<span data-ttu-id="8075d-137">Si el directorio de origen de un archivo que se va a copiar reside en un medio extraíble, como un disquete o un CD-ROM, la acción InstallFiles comprueba que se inserte el medio de origen adecuado antes de intentar copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="8075d-137">If the source directory for a file to be copied resides on removable media such as a floppy disk or CD-ROM, the InstallFiles action verifies that the proper source media is inserted before attempting to copy the file.</span></span> <span data-ttu-id="8075d-138">InstallFiles busca medios del mismo tipo extraíble con una etiqueta de [*volumen*](v-gly.md) que coincida con el valor especificado en la columna VolumeLabel de la tabla de medios.</span><span class="sxs-lookup"><span data-stu-id="8075d-138">The InstallFiles searches for media of the same removable type with a [*volume*](v-gly.md) label that matches the value given in the VolumeLabel column of the Media table.</span></span> <span data-ttu-id="8075d-139">Si se encuentra un volumen montado coincidente, el proceso de copia de archivos continúa.</span><span class="sxs-lookup"><span data-stu-id="8075d-139">If a matching mounted volume is found, the file copying process proceeds.</span></span> <span data-ttu-id="8075d-140">Si no se encuentra ninguna coincidencia, un cuadro de diálogo solicita al usuario que inserte el medio adecuado.</span><span class="sxs-lookup"><span data-stu-id="8075d-140">If no match is found, a dialog box requests that the user to insert the proper media.</span></span> <span data-ttu-id="8075d-141">En este caso, el cuadro de diálogo utiliza el nombre de medio que se encuentra en la columna DiskPrompt de la tabla de medios como parte del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8075d-141">In this case, the dialog box uses the media name found in the DiskPrompt column of the Media table as part of the prompt.</span></span>

<span data-ttu-id="8075d-142">Se debe tener cuidado porque la acción InstallFiles puede eliminar un archivo original y no reemplazarlo.</span><span class="sxs-lookup"><span data-stu-id="8075d-142">Caution must be exercised because the InstallFiles action can delete an original file and not replace it.</span></span> <span data-ttu-id="8075d-143">Esto sucede cuando la acción InstallFiles experimenta un error al reemplazar un archivo más antiguo y el usuario elige omitir el error.</span><span class="sxs-lookup"><span data-stu-id="8075d-143">This occurs when the InstallFiles action experiences an error while replacing an older file and the user chooses to ignore the error.</span></span> <span data-ttu-id="8075d-144">El comportamiento predeterminado del instalador es eliminar un archivo antiguo antes de asegurarse de que el nuevo archivo se copia correctamente.</span><span class="sxs-lookup"><span data-stu-id="8075d-144">The default behavior of installer is to delete an old file before ensuring the new file is copied correctly.</span></span>

<span data-ttu-id="8075d-145">Para consultar las reglas de control de versiones de archivo que usa el instalador, consulte [reglas de control de versiones de archivos](file-versioning-rules.md).</span><span class="sxs-lookup"><span data-stu-id="8075d-145">For the file versioning rules used by the installer, see [File Versioning Rules](file-versioning-rules.md).</span></span>

 

 



