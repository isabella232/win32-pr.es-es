---
description: El WiSubStg.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores.
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: Administrar subalmacenamientos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01876efdb85bdc89df1b4d64332d44674e5e860e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361394"
---
# <a name="manage-substorages"></a><span data-ttu-id="87be9-103">Administrar subalmacenamientos</span><span class="sxs-lookup"><span data-stu-id="87be9-103">Manage Substorages</span></span>

<span data-ttu-id="87be9-104">El WiSubStg.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="87be9-104">The VBScript file WiSubStg.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="87be9-105">Este ejemplo muestra cómo se puede utilizar el script para administrar los subalmacenamientos en una base de datos de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="87be9-105">This sample shows how script can be used to manage substorages in a Windows Installer database.</span></span> <span data-ttu-id="87be9-106">Una transformación puede agregarse a una base de datos de Windows Installer existente como un subalmacenamiento.</span><span class="sxs-lookup"><span data-stu-id="87be9-106">A transform can be added to an existing Windows Installer database as a substorage.</span></span>

<span data-ttu-id="87be9-107">En el ejemplo se muestra el uso de:</span><span class="sxs-lookup"><span data-stu-id="87be9-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="87be9-108">\_Tabla Storages</span><span class="sxs-lookup"><span data-stu-id="87be9-108">\_Storages table</span></span>](-storages-table.md)
-   [<span data-ttu-id="87be9-109">**Método OpenDatabase (objeto Installer)**</span><span class="sxs-lookup"><span data-stu-id="87be9-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="87be9-110">**Método CreateRecord**</span><span class="sxs-lookup"><span data-stu-id="87be9-110">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="87be9-111">[**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="87be9-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="87be9-112">**Método OpenView**</span><span class="sxs-lookup"><span data-stu-id="87be9-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="87be9-113">[**Método commit**](database-commit.md) del [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="87be9-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="87be9-114">**Fetch (método)**</span><span class="sxs-lookup"><span data-stu-id="87be9-114">**Fetch method**</span></span>](view-fetch.md)
-   [<span data-ttu-id="87be9-115">**Modify (método)**</span><span class="sxs-lookup"><span data-stu-id="87be9-115">**Modify method**</span></span>](view-modify.md)
-   <span data-ttu-id="87be9-116">[**Método Execute**](view-execute.md) del [ **objeto View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="87be9-116">[**Execute method**](view-execute.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="87be9-117">**Propiedad StringData**</span><span class="sxs-lookup"><span data-stu-id="87be9-117">**StringData property**</span></span>](record-stringdata.md)
-   <span data-ttu-id="87be9-118">[**Método SetStream**](record-setstream.md) del [ **objeto record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="87be9-118">[**SetStream method**](record-setstream.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="87be9-119">Para usar este ejemplo, necesitará la versión CScript.exe o WScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="87be9-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="87be9-120">Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la siguiente sintaxis.</span><span class="sxs-lookup"><span data-stu-id="87be9-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="87be9-121">La ayuda se muestra si el primer argumento es/?</span><span class="sxs-lookup"><span data-stu-id="87be9-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="87be9-122">o si se especifican pocos argumentos.</span><span class="sxs-lookup"><span data-stu-id="87be9-122">or if too few arguments are specified.</span></span> <span data-ttu-id="87be9-123">Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] .</span><span class="sxs-lookup"><span data-stu-id="87be9-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="87be9-124">El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.</span><span class="sxs-lookup"><span data-stu-id="87be9-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="87be9-125">**cscript WiSubStg.vbs \[ ruta de acceso a la ruta de acceso de la base \] \[ de datos al \] \[ nombre del \] \[ subalmacenamiento de opciones\]**</span><span class="sxs-lookup"><span data-stu-id="87be9-125">**cscript WiSubStg.vbs \[path to database\]\[path to file\]\[options\]\[substorage name\]**</span></span>

<span data-ttu-id="87be9-126">Especifique la ruta de acceso a la base de datos Windows Installer para agregar o quitar el subalmacenamiento.</span><span class="sxs-lookup"><span data-stu-id="87be9-126">Specify the path to the Windows Installer database to add or remove substorage.</span></span> <span data-ttu-id="87be9-127">Especifique una ruta de acceso al archivo de base de datos o de transformación que se va a agregar como subalmacenamiento.</span><span class="sxs-lookup"><span data-stu-id="87be9-127">Specify a path to the transform or database file that is being added as substorage.</span></span> <span data-ttu-id="87be9-128">Para enumerar los subalmacenamientos en la base de datos Windows Installer, omita la ruta de acceso a este archivo.</span><span class="sxs-lookup"><span data-stu-id="87be9-128">To list the substorages in the Windows Installer database, omit the path to this file.</span></span> <span data-ttu-id="87be9-129">Puede especificar un nombre de subalmacenamiento opcional, si se omite, el nombre del subalmacenamiento tiene como valor predeterminado el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="87be9-129">You may specify an optional substorage name, if this is omitted the substorage name defaults to the file name.</span></span>

<span data-ttu-id="87be9-130">Se puede especificar la opción siguiente.</span><span class="sxs-lookup"><span data-stu-id="87be9-130">The following option may be specified.</span></span>



| <span data-ttu-id="87be9-131">Opción</span><span class="sxs-lookup"><span data-stu-id="87be9-131">Option</span></span>              | <span data-ttu-id="87be9-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="87be9-132">Description</span></span>                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87be9-133">no se ha especificado ninguna opción</span><span class="sxs-lookup"><span data-stu-id="87be9-133">no option specified</span></span> | <span data-ttu-id="87be9-134">Agregue un subalmacenamiento a la base de datos Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="87be9-134">Add a substorage to the Windows Installer database.</span></span>                                                 |
| <span data-ttu-id="87be9-135">/d</span><span class="sxs-lookup"><span data-stu-id="87be9-135">/d</span></span>                  | <span data-ttu-id="87be9-136">Quitar un subalmacenamiento.</span><span class="sxs-lookup"><span data-stu-id="87be9-136">Remove a substorage.</span></span> <span data-ttu-id="87be9-137">Esta marca de opción debe ir seguida del nombre del subalmacenamiento que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="87be9-137">This option flag must be followed by the name of the substorage to be removed.</span></span> |



 

<span data-ttu-id="87be9-138">Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="87be9-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="87be9-139">Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="87be9-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="87be9-140">Tenga en cuenta que [un ejemplo de localización muestra la](a-localization-example.md) [incrustación de transformaciones de personalización como subalmacenamiento](embedding-customization-transforms-as-substorage.md).</span><span class="sxs-lookup"><span data-stu-id="87be9-140">Note that [A Localization Example](a-localization-example.md) demonstrates [Embedding Customization Transforms as Substorage](embedding-customization-transforms-as-substorage.md).</span></span>

 

 



