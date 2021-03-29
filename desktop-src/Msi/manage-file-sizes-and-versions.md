---
description: El WiFilVer.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. En el ejemplo se muestra cómo puede usar un script para notificar o actualizar la información de versión, tamaño e idioma del archivo.
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: Administrar versiones y tamaños de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426acf71956d87fe1458447119d79bc142f1ee75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810730"
---
# <a name="manage-file-sizes-and-versions"></a><span data-ttu-id="007e0-104">Administrar versiones y tamaños de archivo</span><span class="sxs-lookup"><span data-stu-id="007e0-104">Manage File Sizes and Versions</span></span>

<span data-ttu-id="007e0-105">El WiFilVer.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="007e0-105">The VBScript file WiFilVer.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="007e0-106">En el ejemplo se muestra cómo puede usar un script para notificar o actualizar la información de versión, tamaño e idioma del archivo.</span><span class="sxs-lookup"><span data-stu-id="007e0-106">The sample shows you how you can use a script to report or update the file version, size, and language information.</span></span>

<span data-ttu-id="007e0-107">El ejemplo también muestra Windows Installer acciones, cómo obtener acceso a una base de datos Windows Installer y el uso de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="007e0-107">The sample also shows you Windows Installer actions, how to access a Windows Installer database, and the use of the following:</span></span>

-   <span data-ttu-id="007e0-108">Método [**Installer. OpenDatabase**](installer-opendatabase.md) del [ **objeto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="007e0-108">[**Installer.OpenDatabase**](installer-opendatabase.md) method of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="007e0-109">[**Installer. FileAttributes**](installer-fileattributes.md) (propiedad)</span><span class="sxs-lookup"><span data-stu-id="007e0-109">[**Installer.FileAttributes**](installer-fileattributes.md) property</span></span>
-   <span data-ttu-id="007e0-110">[**Instalador. FileHash**](installer-filehash.md) (método)</span><span class="sxs-lookup"><span data-stu-id="007e0-110">[**Installer.FileHash**](installer-filehash.md) method</span></span>
-   <span data-ttu-id="007e0-111">[**Installer. fileversion**](installer-fileversion.md) (método)</span><span class="sxs-lookup"><span data-stu-id="007e0-111">[**Installer.FileVersion**](installer-fileversion.md) method</span></span>
-   <span data-ttu-id="007e0-112">Método [**Installer. LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="007e0-112">[**Installer.LastErrorRecord**](installer-lasterrorrecord.md) method of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="007e0-113">[**Database. OpenView**](database-openview.md) (método)</span><span class="sxs-lookup"><span data-stu-id="007e0-113">[**Database.OpenView**](database-openview.md) method</span></span>
-   <span data-ttu-id="007e0-114">Propiedad [**Database. SummaryInformation**](database-summaryinformation.md) del [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="007e0-114">[**Database.SummaryInformation**](database-summaryinformation.md) property of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="007e0-115">[**Session. OnAction**](session-doaction.md) (método)</span><span class="sxs-lookup"><span data-stu-id="007e0-115">[**Session.DoAction**](session-doaction.md) method</span></span>
-   [<span data-ttu-id="007e0-116">**Session. Property**</span><span class="sxs-lookup"><span data-stu-id="007e0-116">**Session.Property**</span></span>](session-session.md)
-   <span data-ttu-id="007e0-117">[**Session. SourcePath**](session-sourcepath.md) (propiedad)</span><span class="sxs-lookup"><span data-stu-id="007e0-117">[**Session.SourcePath**](session-sourcepath.md) property</span></span>
-   <span data-ttu-id="007e0-118">Propiedad [**Session. Mode**](session-mode.md) del [ **objeto Session**](session-object.md)</span><span class="sxs-lookup"><span data-stu-id="007e0-118">[**Session.Mode**](session-mode.md) property of the [**Session Object**](session-object.md)</span></span>
-   <span data-ttu-id="007e0-119">Propiedad [**Record. StringData**](record-stringdata.md)</span><span class="sxs-lookup"><span data-stu-id="007e0-119">[**Record.StringData**](record-stringdata.md) property</span></span>
-   <span data-ttu-id="007e0-120">Propiedad [**Record. IntegerData**](record-integerdata.md) del [ **objeto record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="007e0-120">[**Record.IntegerData**](record-integerdata.md) property of the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="007e0-121">El uso de este ejemplo requiere la versión CScript.exe o WScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="007e0-121">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="007e0-122">Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema mediante la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="007e0-122">To use CScript.exe to run this sample, type a command at the command prompt by using the following syntax:</span></span>

<span data-ttu-id="007e0-123">**cscript WiFilVer.vbs \[ ruta de acceso a \] \[ ubicaciones de origen opcionales de base de datos\]**</span><span class="sxs-lookup"><span data-stu-id="007e0-123">**cscript WiFilVer.vbs \[path to database\]\[optional source locations\]**</span></span>

<span data-ttu-id="007e0-124">Tenga en cuenta también lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="007e0-124">Also be aware of the following:</span></span>

-   <span data-ttu-id="007e0-125">La ayuda se muestra si el primer argumento es/?</span><span class="sxs-lookup"><span data-stu-id="007e0-125">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="007e0-126">o si se especifican pocos argumentos.</span><span class="sxs-lookup"><span data-stu-id="007e0-126">or if too few arguments are specified.</span></span>
-   <span data-ttu-id="007e0-127">Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] .</span><span class="sxs-lookup"><span data-stu-id="007e0-127">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span>
-   <span data-ttu-id="007e0-128">El ejemplo devuelve un valor de 0 (cero) para Success, 1 (uno) si se invoca la ayuda y 2 (dos) si se produce un error en el script.</span><span class="sxs-lookup"><span data-stu-id="007e0-128">The sample returns a value of 0 (zero) for success, 1 (one) if help is invoked, and 2 (two) if the script fails.</span></span>

<span data-ttu-id="007e0-129">Especifique el Windows Installer base de datos que desea actualizar, que debe estar ubicado en la raíz del archivo de origen.</span><span class="sxs-lookup"><span data-stu-id="007e0-129">Specify the Windows Installer database that you want to be updated, which must be located at the source file root.</span></span> <span data-ttu-id="007e0-130">Sin embargo, puede especificar orígenes para la base de datos en ubicaciones independientes.</span><span class="sxs-lookup"><span data-stu-id="007e0-130">However, you can specify sources for the database at separate locations.</span></span> <span data-ttu-id="007e0-131">Si el origen está comprimido, todos los archivos se abren en la raíz.</span><span class="sxs-lookup"><span data-stu-id="007e0-131">If the source is compressed, all the files are opened at the root.</span></span>

<span data-ttu-id="007e0-132">Las siguientes opciones se pueden especificar en cualquier ubicación de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="007e0-132">The following options can be specified at any location on the command line.</span></span>



| <span data-ttu-id="007e0-133">Opción</span><span class="sxs-lookup"><span data-stu-id="007e0-133">Option</span></span>                | <span data-ttu-id="007e0-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="007e0-134">Description</span></span>                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="007e0-135">*no se ha especificado ninguna opción*</span><span class="sxs-lookup"><span data-stu-id="007e0-135">*no option specified*</span></span> | <span data-ttu-id="007e0-136">Mostrar la información de archivo de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="007e0-136">Display the file information of the database.</span></span>                                            |
| <span data-ttu-id="007e0-137">/U</span><span class="sxs-lookup"><span data-stu-id="007e0-137">/u</span></span>                    | <span data-ttu-id="007e0-138">Actualice el tamaño del archivo, la versión y la información de idioma en la base de datos desde el origen.</span><span class="sxs-lookup"><span data-stu-id="007e0-138">Update the file size, version, and language information in the database from the source.</span></span> |



 

<span data-ttu-id="007e0-139">Para obtener más información, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md) y herramientas de desarrollo de [Windows Installer](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="007e0-139">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) and [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



