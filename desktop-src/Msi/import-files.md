---
description: El WiImport.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. En este ejemplo se muestra cómo escribir un script para importar tablas en una base de datos de Windows Installer.
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: Importar archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8508ee4e385e3edc737515f1b524de074489fb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652508"
---
# <a name="import-files"></a><span data-ttu-id="7bc52-104">Importar archivos</span><span class="sxs-lookup"><span data-stu-id="7bc52-104">Import Files</span></span>

<span data-ttu-id="7bc52-105">El WiImport.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="7bc52-105">The VBScript file WiImport.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="7bc52-106">En este ejemplo se muestra cómo escribir un script para importar tablas en una base de datos de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7bc52-106">This sample shows how to write a script to import tables into a Windows Installer database.</span></span>

<span data-ttu-id="7bc52-107">El script se conecta a un objeto del [**instalador**](installer-object.md) , abre una base de datos, procesa una lista de archivos y confirma los cambios antes de cerrar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="7bc52-107">The script connects to an [**Installer**](installer-object.md) object, opens a database, processes a list of files, and commits the changes before closing the database.</span></span>

<span data-ttu-id="7bc52-108">En el ejemplo se muestra el uso de:</span><span class="sxs-lookup"><span data-stu-id="7bc52-108">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="7bc52-109">**Método OpenDatabase (objeto Installer)**</span><span class="sxs-lookup"><span data-stu-id="7bc52-109">**OpenDatabase Method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="7bc52-110">[**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="7bc52-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="7bc52-111">**Método Import**</span><span class="sxs-lookup"><span data-stu-id="7bc52-111">**Import method**</span></span>](database-import.md)
-   <span data-ttu-id="7bc52-112">[**Método commit**](database-commit.md) del [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="7bc52-112">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="7bc52-113">Para usar este ejemplo, necesitará la versión CScript.exe o WScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="7bc52-113">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="7bc52-114">Para usar CScript.exe para ejecutar este ejemplo, use la siguiente sintaxis en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="7bc52-114">To use CScript.exe to run this sample, use the following syntax at the command prompt.</span></span>

<span data-ttu-id="7bc52-115">**cscript WiImport.vbs \[ ruta de acceso de la base de datos \] \[ a opciones de carpeta \] \[ lista de archivos de \] \[ almacenamiento**\]</span><span class="sxs-lookup"><span data-stu-id="7bc52-115">**cscript WiImport.vbs \[path to database\]\[path to folder\]\[options\] \[archive file list**\]</span></span>

<span data-ttu-id="7bc52-116">La ayuda se muestra si el primer argumento es/?</span><span class="sxs-lookup"><span data-stu-id="7bc52-116">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="7bc52-117">o si se especifican pocos argumentos.</span><span class="sxs-lookup"><span data-stu-id="7bc52-117">or if too few arguments are specified.</span></span> <span data-ttu-id="7bc52-118">Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ ruta de acceso al archivo \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.</span><span class="sxs-lookup"><span data-stu-id="7bc52-118">To redirect the output to a file, end the command line with VBS > \[path to file\].The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="7bc52-119">Especifique la ruta de acceso a una base de datos de Windows Installer que se va a crear o que va a recibir las tablas importadas.</span><span class="sxs-lookup"><span data-stu-id="7bc52-119">Specify the path to a Windows installer database that is to be created or that is to receive the imported tables.</span></span> <span data-ttu-id="7bc52-120">Especifique la ruta de acceso a la carpeta que contiene los archivos de almacenamiento de las tablas que se van a importar.</span><span class="sxs-lookup"><span data-stu-id="7bc52-120">Specify the path to the folder containing the archive files of the tables that are being imported.</span></span> <span data-ttu-id="7bc52-121">Enumera los nombres de los archivos de almacenamiento que se van a importar.</span><span class="sxs-lookup"><span data-stu-id="7bc52-121">List the names of the archive files that are being imported.</span></span> <span data-ttu-id="7bc52-122">Los nombres de archivo comodín, como \* . IDT, se pueden usar para importar varios archivos.</span><span class="sxs-lookup"><span data-stu-id="7bc52-122">Wildcard file names, such as \*.idt, can be used to import multiple files.</span></span>

<span data-ttu-id="7bc52-123">Las siguientes opciones se pueden especificar en cualquier parte de la línea de comandos antes de la lista de archivos.</span><span class="sxs-lookup"><span data-stu-id="7bc52-123">The following options may be specified anywhere on the command line before the file list.</span></span>



| <span data-ttu-id="7bc52-124">Opción</span><span class="sxs-lookup"><span data-stu-id="7bc52-124">Option</span></span>              | <span data-ttu-id="7bc52-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bc52-125">Description</span></span>                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bc52-126">no se ha especificado ninguna opción</span><span class="sxs-lookup"><span data-stu-id="7bc52-126">no option specified</span></span> | <span data-ttu-id="7bc52-127">Importe la lista de archivos de almacenamiento de tabla de la carpeta especificada en la base de datos de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7bc52-127">Import the list of table archive files from the specified folder into the Windows Installer database.</span></span>                                |
| <span data-ttu-id="7bc52-128">/C</span><span class="sxs-lookup"><span data-stu-id="7bc52-128">/c</span></span>                  | <span data-ttu-id="7bc52-129">Cree una base de datos de Windows Installer y, a continuación, importe la lista de archivos de almacenamiento de tabla de la carpeta especificada en la nueva base de datos.</span><span class="sxs-lookup"><span data-stu-id="7bc52-129">Create a Windows Installer database and then import the list of table archive files from the specified folder into the new database.</span></span> |



 

<span data-ttu-id="7bc52-130">Para obtener más información, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md) para obtener ejemplos adicionales de scripting.</span><span class="sxs-lookup"><span data-stu-id="7bc52-130">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) for additional scripting examples.</span></span> <span data-ttu-id="7bc52-131">Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="7bc52-131">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="7bc52-132">Tenga en cuenta que [un ejemplo de localización](a-localization-example.md) también muestra la [importación de tablas de error y de ActionText localizadas](importing-localized-error-and-actiontext-tables.md).</span><span class="sxs-lookup"><span data-stu-id="7bc52-132">Note that [A Localization Example](a-localization-example.md) also demonstrates [Importing Localized Error and ActionText Tables](importing-localized-error-and-actiontext-tables.md).</span></span>

 

 



