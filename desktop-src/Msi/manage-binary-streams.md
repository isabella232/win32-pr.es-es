---
description: El WiStream.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores.
ms.assetid: f96d1fdd-81c8-4fb2-a23e-fda49ace8bef
title: Administrar secuencias binarias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877631a40157a5d286ef0c2575732a6d561eefb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678252"
---
# <a name="manage-binary-streams"></a><span data-ttu-id="1cbd6-103">Administrar secuencias binarias</span><span class="sxs-lookup"><span data-stu-id="1cbd6-103">Manage Binary Streams</span></span>

<span data-ttu-id="1cbd6-104">El WiStream.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="1cbd6-104">The VBScript file WiStream.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="1cbd6-105">Este ejemplo muestra cómo se puede utilizar el script para administrar secuencias binarias en una base de datos de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1cbd6-105">This sample shows how script can be used to manage binary streams in a Windows Installer database.</span></span> <span data-ttu-id="1cbd6-106">El ejemplo se puede usar para especificar archivadores de archivos comprimidos en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="1cbd6-106">The sample may be used to enter compressed file cabinets into a database.</span></span> <span data-ttu-id="1cbd6-107">Este ejemplo muestra el funcionamiento de la [ \_ tabla streams](-streams-table.md) en la base de datos Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1cbd6-107">This sample demonstrates the operation of the [\_Streams table](-streams-table.md) in the Windows Installer database.</span></span>

<span data-ttu-id="1cbd6-108">En el ejemplo también se muestra el uso de:</span><span class="sxs-lookup"><span data-stu-id="1cbd6-108">The sample also demonstrates the use of:</span></span>

-   [<span data-ttu-id="1cbd6-109">**Método OpenDatabase (objeto Installer)**</span><span class="sxs-lookup"><span data-stu-id="1cbd6-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="1cbd6-110">**Método CreateRecord**</span><span class="sxs-lookup"><span data-stu-id="1cbd6-110">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="1cbd6-111">[**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="1cbd6-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="1cbd6-112">**Método OpenView**</span><span class="sxs-lookup"><span data-stu-id="1cbd6-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="1cbd6-113">[**Método commit**](database-commit.md) del [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="1cbd6-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="1cbd6-114">**Fetch (método)**</span><span class="sxs-lookup"><span data-stu-id="1cbd6-114">**Fetch method**</span></span>](view-fetch.md)
-   [<span data-ttu-id="1cbd6-115">**Modify (método)**</span><span class="sxs-lookup"><span data-stu-id="1cbd6-115">**Modify method**</span></span>](view-modify.md)
-   <span data-ttu-id="1cbd6-116">[**Método Execute**](view-execute.md) del [ **objeto View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="1cbd6-116">[**Execute method**](view-execute.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="1cbd6-117">**Propiedad StringData**</span><span class="sxs-lookup"><span data-stu-id="1cbd6-117">**StringData property**</span></span>](record-stringdata.md)
-   <span data-ttu-id="1cbd6-118">[**Método SetStream**](record-setstream.md) del [ **objeto record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="1cbd6-118">[**SetStream method**](record-setstream.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="1cbd6-119">Para usar este ejemplo, necesitará la versión CScript.exe o WScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="1cbd6-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="1cbd6-120">Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la siguiente sintaxis.</span><span class="sxs-lookup"><span data-stu-id="1cbd6-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="1cbd6-121">La ayuda se muestra si el primer argumento es/?</span><span class="sxs-lookup"><span data-stu-id="1cbd6-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="1cbd6-122">o si se especifican pocos argumentos.</span><span class="sxs-lookup"><span data-stu-id="1cbd6-122">or if too few arguments are specified.</span></span> <span data-ttu-id="1cbd6-123">Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] .</span><span class="sxs-lookup"><span data-stu-id="1cbd6-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="1cbd6-124">El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.</span><span class="sxs-lookup"><span data-stu-id="1cbd6-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="1cbd6-125">**cscript WiStream.vbs \[ ruta de acceso de la base de datos \] \[ al \] \[ \] \[ nombre del flujo de opciones de archivo\]**</span><span class="sxs-lookup"><span data-stu-id="1cbd6-125">**cscript WiStream.vbs \[path to database\]\[path to file\]\[options\]\[stream name\]**</span></span>

<span data-ttu-id="1cbd6-126">Especifique la ruta de acceso a la base de datos de Windows Installer que va a recibir la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1cbd6-126">Specify the path to the Windows Installer database that is to receive the stream.</span></span> <span data-ttu-id="1cbd6-127">Especifique una ruta de acceso al archivo binario que contiene los datos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1cbd6-127">Specify a path to the binary file containing the stream data.</span></span> <span data-ttu-id="1cbd6-128">Para enumerar las secuencias en la base de datos del instalador, omita esta ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="1cbd6-128">To list the streams in the installer database, omit this path.</span></span> <span data-ttu-id="1cbd6-129">Puede especificar un nombre de flujo opcional, si se omite, se toma como valor predeterminado el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="1cbd6-129">You may specify an optional stream name, if this is omitted it defaults to the file name.</span></span>

<span data-ttu-id="1cbd6-130">Se puede especificar la opción siguiente.</span><span class="sxs-lookup"><span data-stu-id="1cbd6-130">The following option may be specified.</span></span>



| <span data-ttu-id="1cbd6-131">Opción</span><span class="sxs-lookup"><span data-stu-id="1cbd6-131">Option</span></span>              | <span data-ttu-id="1cbd6-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cbd6-132">Description</span></span>                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cbd6-133">no se ha especificado ninguna opción</span><span class="sxs-lookup"><span data-stu-id="1cbd6-133">no option specified</span></span> | <span data-ttu-id="1cbd6-134">Agregue una secuencia a la base de datos Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1cbd6-134">Add a stream to the Windows Installer database.</span></span>                                                 |
| <span data-ttu-id="1cbd6-135">/d</span><span class="sxs-lookup"><span data-stu-id="1cbd6-135">/d</span></span>                  | <span data-ttu-id="1cbd6-136">Quitar un flujo.</span><span class="sxs-lookup"><span data-stu-id="1cbd6-136">Remove a stream.</span></span> <span data-ttu-id="1cbd6-137">Esta marca de opción debe ir seguida del nombre del subalmacenamiento que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="1cbd6-137">This option flag must be followed by the name of the substorage being removed.</span></span> |



 

<span data-ttu-id="1cbd6-138">Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="1cbd6-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="1cbd6-139">Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="1cbd6-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



