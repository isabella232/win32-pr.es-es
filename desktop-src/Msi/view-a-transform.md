---
description: El WiLstXfm.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este ejemplo de script se puede usar para ver un archivo de transformación.
ms.assetid: c2e3dd56-b0e5-481a-b7b8-5000fa686850
title: Ver una transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f4a858f8deb115de967da3b4d485b596f85cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652409"
---
# <a name="view-a-transform"></a><span data-ttu-id="0032e-104">Ver una transformación</span><span class="sxs-lookup"><span data-stu-id="0032e-104">View a Transform</span></span>

<span data-ttu-id="0032e-105">El WiLstXfm.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="0032e-105">The VBScript file WiLstXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="0032e-106">Este ejemplo de script se puede usar para ver un archivo de transformación.</span><span class="sxs-lookup"><span data-stu-id="0032e-106">This script sample can be used to view a transform file.</span></span>

<span data-ttu-id="0032e-107">En el ejemplo se muestra el uso de:</span><span class="sxs-lookup"><span data-stu-id="0032e-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="0032e-108">\_Tabla TransformView</span><span class="sxs-lookup"><span data-stu-id="0032e-108">\_TransformView table</span></span>](-transformview-table.md)
-   [<span data-ttu-id="0032e-109">**Método OpenDatabase (objeto Installer)**</span><span class="sxs-lookup"><span data-stu-id="0032e-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="0032e-110">[**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="0032e-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="0032e-111">**Método ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="0032e-111">**ApplyTransform method**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="0032e-112">**Método OpenView**</span><span class="sxs-lookup"><span data-stu-id="0032e-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="0032e-113">[**Método commit**](database-commit.md) del [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="0032e-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="0032e-114">**Propiedad IsNull**</span><span class="sxs-lookup"><span data-stu-id="0032e-114">**IsNull property**</span></span>](record-isnull.md)
-   <span data-ttu-id="0032e-115">[**Propiedad StringData**](record-stringdata.md) del [ **objeto record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="0032e-115">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="0032e-116">El uso de este ejemplo requiere la versión CScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="0032e-116">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="0032e-117">Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la siguiente sintaxis.</span><span class="sxs-lookup"><span data-stu-id="0032e-117">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="0032e-118">La ayuda se muestra si el primer argumento es/?</span><span class="sxs-lookup"><span data-stu-id="0032e-118">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="0032e-119">o si se especifican pocos argumentos.</span><span class="sxs-lookup"><span data-stu-id="0032e-119">or if too few arguments are specified.</span></span> <span data-ttu-id="0032e-120">Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] .</span><span class="sxs-lookup"><span data-stu-id="0032e-120">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="0032e-121">El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.</span><span class="sxs-lookup"><span data-stu-id="0032e-121">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="0032e-122">**cscript WiLstXfm.vbs** *\[ ruta de acceso de referencia de la opción de base \] \[ de datos a la \] \[ transformación que se va a ver \]*</span><span class="sxs-lookup"><span data-stu-id="0032e-122">**cscript WiLstXfm.vbs** *\[path to reference database\]\[option\]\[path to transform to be viewed\]*</span></span>

<span data-ttu-id="0032e-123">Especifique la ruta de acceso a la base de datos de Windows Installer de referencia.</span><span class="sxs-lookup"><span data-stu-id="0032e-123">Specify the path to the reference Windows Installer database.</span></span> <span data-ttu-id="0032e-124">Especifique una lista de rutas de acceso para transformar los archivos que se están viendo.</span><span class="sxs-lookup"><span data-stu-id="0032e-124">Specify a list of paths to transform files that are being viewed.</span></span> <span data-ttu-id="0032e-125">Cada ruta de acceso de la lista puede ir precedida de un valor numérico opcional.</span><span class="sxs-lookup"><span data-stu-id="0032e-125">Each path in the list may by preceded by an optional numeric value.</span></span> <span data-ttu-id="0032e-126">Este valor especifica un conjunto de condiciones de error que se van a suprimir.</span><span class="sxs-lookup"><span data-stu-id="0032e-126">This value specifies a set of error conditions that are to be suppressed.</span></span> <span data-ttu-id="0032e-127">Puede agregar estos valores juntos para suprimir varias condiciones.</span><span class="sxs-lookup"><span data-stu-id="0032e-127">You may add these values together to suppress multiple conditions.</span></span> <span data-ttu-id="0032e-128">Si no se especifica ninguna opción numérica, se suprimen todas las condiciones de error.</span><span class="sxs-lookup"><span data-stu-id="0032e-128">If no numeric option is specified, all the error conditions are suppressed.</span></span> <span data-ttu-id="0032e-129">Los argumentos de esta lista se ejecutan en el orden de izquierda a derecha en el que aparecen en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="0032e-129">The arguments in this list are executed in the left-to-right order in which they appear on the command line.</span></span>



| <span data-ttu-id="0032e-130">Value</span><span class="sxs-lookup"><span data-stu-id="0032e-130">Value</span></span> | <span data-ttu-id="0032e-131">Condición de error que se va a suprimir</span><span class="sxs-lookup"><span data-stu-id="0032e-131">Error condition to suppress</span></span>                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="0032e-132">1</span><span class="sxs-lookup"><span data-stu-id="0032e-132">1</span></span>     | <span data-ttu-id="0032e-133">Agregando una fila que ya existe.</span><span class="sxs-lookup"><span data-stu-id="0032e-133">Adding a row that already exists.</span></span>             |
| <span data-ttu-id="0032e-134">2</span><span class="sxs-lookup"><span data-stu-id="0032e-134">2</span></span>     | <span data-ttu-id="0032e-135">Eliminar una fila que no existe.</span><span class="sxs-lookup"><span data-stu-id="0032e-135">Deleting a row that does not exist.</span></span>           |
| <span data-ttu-id="0032e-136">4</span><span class="sxs-lookup"><span data-stu-id="0032e-136">4</span></span>     | <span data-ttu-id="0032e-137">Agregando una tabla que ya existe.</span><span class="sxs-lookup"><span data-stu-id="0032e-137">Adding a table that already exists.</span></span>           |
| <span data-ttu-id="0032e-138">8</span><span class="sxs-lookup"><span data-stu-id="0032e-138">8</span></span>     | <span data-ttu-id="0032e-139">Eliminando una tabla que no existe.</span><span class="sxs-lookup"><span data-stu-id="0032e-139">Deleting a table that does not exist.</span></span>         |
| <span data-ttu-id="0032e-140">16</span><span class="sxs-lookup"><span data-stu-id="0032e-140">16</span></span>    | <span data-ttu-id="0032e-141">Actualizar una fila que no existe.</span><span class="sxs-lookup"><span data-stu-id="0032e-141">Updating a row that does not exist.</span></span>           |
| <span data-ttu-id="0032e-142">256</span><span class="sxs-lookup"><span data-stu-id="0032e-142">256</span></span>   | <span data-ttu-id="0032e-143">No coinciden las páginas de códigos de base de datos y de transformación.</span><span class="sxs-lookup"><span data-stu-id="0032e-143">Mismatch of database and transform codepages.</span></span> |



 

<span data-ttu-id="0032e-144">Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="0032e-144">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="0032e-145">Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0032e-145">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



