---
description: El WiExport.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores.
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: Exportar archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1512650ee144fc00c2de851051b9bbb4d98a21e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687190"
---
# <a name="export-files"></a><span data-ttu-id="43adf-103">Exportar archivos</span><span class="sxs-lookup"><span data-stu-id="43adf-103">Export Files</span></span>

<span data-ttu-id="43adf-104">El WiExport.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="43adf-104">The VBScript file WiExport.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="43adf-105">En este ejemplo se muestra cómo escribir un script para exportar tablas a una base de datos de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="43adf-105">This sample shows how to write script to export tables into a Windows Installer database.</span></span> <span data-ttu-id="43adf-106">El ejemplo de script se conecta a un objeto de [**instalador**](installer-object.md) , abre una base de datos y exporta las tablas a los archivos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="43adf-106">The script sample connects to an [**Installer**](installer-object.md) object, opens a database and exports tables to archive files.</span></span>

<span data-ttu-id="43adf-107">En el ejemplo se muestra el uso de:</span><span class="sxs-lookup"><span data-stu-id="43adf-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="43adf-108">**Método OpenDatabase (objeto Installer)**</span><span class="sxs-lookup"><span data-stu-id="43adf-108">**OpenDatabase Method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="43adf-109">[**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="43adf-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="43adf-110">**Método Export**</span><span class="sxs-lookup"><span data-stu-id="43adf-110">**Export method**</span></span>](database-export.md)
-   <span data-ttu-id="43adf-111">[**Método OpenView**](database-openview.md) del [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="43adf-111">[**OpenView method**](database-openview.md) of the [**Database object**](database-object.md)</span></span>
-   <span data-ttu-id="43adf-112">[**Método fetch**](view-fetch.md) del [ **objeto View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="43adf-112">[**Fetch method**](view-fetch.md) of the [**View object**](view-object.md)</span></span>
-   <span data-ttu-id="43adf-113">[**Propiedad StringData**](record-stringdata.md) del [ **objeto record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="43adf-113">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="43adf-114">Para usar este ejemplo, necesitará la versión CScript.exe o WScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="43adf-114">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="43adf-115">Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la siguiente sintaxis.</span><span class="sxs-lookup"><span data-stu-id="43adf-115">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="43adf-116">La ayuda se muestra si el primer argumento es/?</span><span class="sxs-lookup"><span data-stu-id="43adf-116">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="43adf-117">o si se especifican pocos argumentos.</span><span class="sxs-lookup"><span data-stu-id="43adf-117">or if too few arguments are specified.</span></span> <span data-ttu-id="43adf-118">Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] .</span><span class="sxs-lookup"><span data-stu-id="43adf-118">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="43adf-119">El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.</span><span class="sxs-lookup"><span data-stu-id="43adf-119">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="43adf-120">**cscript WiExport.vbs \[ ruta de acceso de la base de datos \] \[ a la \] \[ lista de nombres de \] \[ tabla de opciones de carpeta\]**</span><span class="sxs-lookup"><span data-stu-id="43adf-120">**cscript WiExport.vbs \[path to database\]\[path to folder\]\[options\]\[table name list\]**</span></span>

<span data-ttu-id="43adf-121">Especifique la ruta de acceso a la base de datos del instalador desde la que se exportan las tablas.</span><span class="sxs-lookup"><span data-stu-id="43adf-121">Specify the path to the installer database from which the tables are being exported.</span></span> <span data-ttu-id="43adf-122">Especifique la ruta de acceso a la carpeta en la que se copiarán los archivos de almacenamiento exportados.</span><span class="sxs-lookup"><span data-stu-id="43adf-122">Specify the path to the folder into which the exported archive files are to be copied.</span></span> <span data-ttu-id="43adf-123">Enumera los nombres que distinguen mayúsculas de minúsculas de las [tablas de base de datos](database-tables.md) que se van a exportar.</span><span class="sxs-lookup"><span data-stu-id="43adf-123">List the case-sensitive names of the [database tables](database-tables.md) being exported.</span></span> <span data-ttu-id="43adf-124">Especifique ' \* ' para exportar todas las tablas, incluido \_ SummaryInformation.</span><span class="sxs-lookup"><span data-stu-id="43adf-124">Specify '\*' to export all the tables including \_SummaryInformation.</span></span>

<span data-ttu-id="43adf-125">Las siguientes opciones se pueden especificar en cualquier parte de la línea de comandos antes de la lista de nombres de tabla.</span><span class="sxs-lookup"><span data-stu-id="43adf-125">The following options may be specified anywhere on the command line before the table name list.</span></span>



| <span data-ttu-id="43adf-126">Opción</span><span class="sxs-lookup"><span data-stu-id="43adf-126">Option</span></span>              | <span data-ttu-id="43adf-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="43adf-127">Description</span></span>                                            |
|---------------------|--------------------------------------------------------|
| <span data-ttu-id="43adf-128">no se ha especificado ninguna opción</span><span class="sxs-lookup"><span data-stu-id="43adf-128">no option specified</span></span> | <span data-ttu-id="43adf-129">Los archivos de almacenamiento exportados pueden tener un nombre de archivo largo.</span><span class="sxs-lookup"><span data-stu-id="43adf-129">Exported archive files may have a long file name.</span></span>      |
| <span data-ttu-id="43adf-130">/s</span><span class="sxs-lookup"><span data-stu-id="43adf-130">/s</span></span>                  | <span data-ttu-id="43adf-131">Fuerce que los archivos de almacenamiento exportados tengan nombres de archivo cortos.</span><span class="sxs-lookup"><span data-stu-id="43adf-131">Force exported archive files to have short file names.</span></span> |



 

<span data-ttu-id="43adf-132">Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="43adf-132">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="43adf-133">Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="43adf-133">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



