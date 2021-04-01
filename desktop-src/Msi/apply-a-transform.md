---
description: El WiUseXfm.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este ejemplo muestra cómo se puede utilizar el script para aplicar una transformación a una base de datos de Windows Installer.
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: Aplicar una transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e86acc495fc2a0bb8dff562832e58d29483256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909105"
---
# <a name="apply-a-transform"></a><span data-ttu-id="0623e-104">Aplicar una transformación</span><span class="sxs-lookup"><span data-stu-id="0623e-104">Apply a Transform</span></span>

<span data-ttu-id="0623e-105">El WiUseXfm.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="0623e-105">The VBScript file WiUseXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="0623e-106">Este ejemplo muestra cómo se puede utilizar el script para aplicar una transformación a una base de datos de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0623e-106">This sample shows how script can be used to apply a transform to a Windows Installer database.</span></span>

<span data-ttu-id="0623e-107">En el ejemplo se muestra el uso de</span><span class="sxs-lookup"><span data-stu-id="0623e-107">The sample demonstrates the use of</span></span>

-   [<span data-ttu-id="0623e-108">**Método OpenDatabase (objeto Installer)**</span><span class="sxs-lookup"><span data-stu-id="0623e-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="0623e-109">[**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="0623e-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="0623e-110">**Método ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="0623e-110">**ApplyTransform method**</span></span>](database-applytransform.md)
-   <span data-ttu-id="0623e-111">[**Método commit**](database-commit.md) del [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="0623e-111">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="0623e-112">Para usar este ejemplo, necesitará la versión CScript.exe o WScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="0623e-112">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="0623e-113">Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la siguiente sintaxis.</span><span class="sxs-lookup"><span data-stu-id="0623e-113">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="0623e-114">La ayuda se muestra si el primer argumento es/?</span><span class="sxs-lookup"><span data-stu-id="0623e-114">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="0623e-115">o si se especifican pocos argumentos.</span><span class="sxs-lookup"><span data-stu-id="0623e-115">or if too few arguments are specified.</span></span> <span data-ttu-id="0623e-116">Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] .</span><span class="sxs-lookup"><span data-stu-id="0623e-116">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="0623e-117">El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.</span><span class="sxs-lookup"><span data-stu-id="0623e-117">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="0623e-118">**cscript WiUseXfm.vbs \[ ruta de acceso a la ruta de acceso de base de datos original \] \[ para transformar opciones de archivo \] \[\]**</span><span class="sxs-lookup"><span data-stu-id="0623e-118">**cscript WiUseXfm.vbs \[path to original database\]\[path to transform file\]\[options\]**</span></span>

<span data-ttu-id="0623e-119">Especifique la ruta de acceso a la base de datos Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0623e-119">Specify the path to the Windows Installer database.</span></span> <span data-ttu-id="0623e-120">Especifique la ruta de acceso al archivo de transformación.</span><span class="sxs-lookup"><span data-stu-id="0623e-120">Specify the path to the transform file.</span></span> <span data-ttu-id="0623e-121">Si se omite la ruta de acceso al archivo de transformación, las dos bases de datos solo se comparan.</span><span class="sxs-lookup"><span data-stu-id="0623e-121">If the path to the transform file is omitted, the two databases are only compared.</span></span> <span data-ttu-id="0623e-122">El tercer argumento es un valor numérico opcional que especifica un conjunto de condiciones de error que se van a suprimir.</span><span class="sxs-lookup"><span data-stu-id="0623e-122">The third argument is an optional numeric value that specifies a set of error conditions that are to be suppressed.</span></span> <span data-ttu-id="0623e-123">Agregue estos valores juntos para suprimir varias condiciones.</span><span class="sxs-lookup"><span data-stu-id="0623e-123">Add these values together to suppress multiple conditions.</span></span>



| <span data-ttu-id="0623e-124">Value</span><span class="sxs-lookup"><span data-stu-id="0623e-124">Value</span></span> | <span data-ttu-id="0623e-125">Condición de error que se va a suprimir</span><span class="sxs-lookup"><span data-stu-id="0623e-125">Error condition to suppress</span></span>                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="0623e-126">1</span><span class="sxs-lookup"><span data-stu-id="0623e-126">1</span></span>     | <span data-ttu-id="0623e-127">Agregando una fila que ya existe.</span><span class="sxs-lookup"><span data-stu-id="0623e-127">Adding a row that already exists.</span></span>             |
| <span data-ttu-id="0623e-128">2</span><span class="sxs-lookup"><span data-stu-id="0623e-128">2</span></span>     | <span data-ttu-id="0623e-129">Eliminar una fila que no existe.</span><span class="sxs-lookup"><span data-stu-id="0623e-129">Deleting a row that does not exist.</span></span>           |
| <span data-ttu-id="0623e-130">4</span><span class="sxs-lookup"><span data-stu-id="0623e-130">4</span></span>     | <span data-ttu-id="0623e-131">Agregando una tabla que ya existe.</span><span class="sxs-lookup"><span data-stu-id="0623e-131">Adding a table that already exists.</span></span>           |
| <span data-ttu-id="0623e-132">8</span><span class="sxs-lookup"><span data-stu-id="0623e-132">8</span></span>     | <span data-ttu-id="0623e-133">Eliminando una tabla que no existe.</span><span class="sxs-lookup"><span data-stu-id="0623e-133">Deleting a table that does not exist.</span></span>         |
| <span data-ttu-id="0623e-134">16</span><span class="sxs-lookup"><span data-stu-id="0623e-134">16</span></span>    | <span data-ttu-id="0623e-135">Actualizar una fila que no existe.</span><span class="sxs-lookup"><span data-stu-id="0623e-135">Updating a row that does not exist.</span></span>           |
| <span data-ttu-id="0623e-136">256</span><span class="sxs-lookup"><span data-stu-id="0623e-136">256</span></span>   | <span data-ttu-id="0623e-137">No coinciden las páginas de códigos de base de datos y de transformación.</span><span class="sxs-lookup"><span data-stu-id="0623e-137">Mismatch of database and transform codepages.</span></span> |



 

<span data-ttu-id="0623e-138">Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="0623e-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="0623e-139">Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0623e-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



