---
description: El archivo de ejemplo de código de VBScript WiTextIn.vbs se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores.
ms.assetid: ba6c6367-ebb1-4981-ae3a-bcff68aacdbf
title: Copiar archivo ANSI en un campo de base de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc6c4d3a945177581a35bf6b19d89855abb5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667676"
---
# <a name="copy-ansi-file-into-a-database-field"></a><span data-ttu-id="4ed2f-103">Copiar archivo ANSI en un campo de base de datos</span><span class="sxs-lookup"><span data-stu-id="4ed2f-103">Copy ANSI File Into a Database Field</span></span>

<span data-ttu-id="4ed2f-104">El archivo de ejemplo de código de VBScript WiTextIn.vbs se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="4ed2f-104">The VBScript code sample file WiTextIn.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="4ed2f-105">En el ejemplo se muestra cómo se puede utilizar un script para copiar un archivo en un campo de texto de una base de datos de Windows Installer y se muestra el procesamiento de los datos de la clave principal.</span><span class="sxs-lookup"><span data-stu-id="4ed2f-105">The sample shows how a script can be used to copy a file into a text field of a Windows Installer database, and demonstrates the processing of primary key data.</span></span>

<span data-ttu-id="4ed2f-106">En el ejemplo de código también se muestran los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="4ed2f-106">The code sample also shows you the following:</span></span>

-   <span data-ttu-id="4ed2f-107">[**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md) y el [**método LastErrorRecord**](installer-lasterrorrecord.md) del [**objeto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="4ed2f-107">[**OpenDatabase method (Installer Object)**](installer-opendatabase.md) and the [**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="4ed2f-108">[**Método OpenView**](database-openview.md), [**método commit**](database-commit.md)y la [**propiedad PrimaryKeys**](database-primarykeys.md) del [**objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="4ed2f-108">[**OpenView method**](database-openview.md), the [**Commit method**](database-commit.md), and the [**PrimaryKeys property**](database-primarykeys.md) of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="4ed2f-109">[**Método fetch**](view-fetch.md) y el [**método Modify**](view-modify.md) del [**objeto View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="4ed2f-109">[**Fetch method**](view-fetch.md) and the [**Modify method**](view-modify.md) of the [**View Object**](view-object.md)</span></span>
-   <span data-ttu-id="4ed2f-110">[**Propiedad StringData**](record-stringdata.md) y [**método ReadStream**](record-readstream.md) del [**objeto record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="4ed2f-110">[**StringData property**](record-stringdata.md) and [**ReadStream method**](record-readstream.md) of the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="4ed2f-111">Para usar el ejemplo de código, necesita la versión CScript.exe o WScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="4ed2f-111">To use the code sample you need the CScript.exe or WScript.exe version of Windows Script Host.</span></span>

<span data-ttu-id="4ed2f-112">**Para usar CScript.exe para ejecutar este ejemplo**</span><span class="sxs-lookup"><span data-stu-id="4ed2f-112">**To use CScript.exe to run this sample**</span></span>

-   <span data-ttu-id="4ed2f-113">En el símbolo del sistema, escriba la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="4ed2f-113">At the command prompt, type the following syntax:</span></span>

    <span data-ttu-id="4ed2f-114">**cscript WiTextIn.vbs \[ ruta de acceso al nombre de tabla de la base de datos \] \[ \] \[ valores de clave principal \] \[ \] \[ ruta de acceso al archivo\]**</span><span class="sxs-lookup"><span data-stu-id="4ed2f-114">**cscript WiTextIn.vbs \[path to database\]\[table name\]\[primary key values\]\[column name\]\[path to file\]**</span></span>

> [!Note]  
> <span data-ttu-id="4ed2f-115">La ayuda se muestra si el primer argumento es/?</span><span class="sxs-lookup"><span data-stu-id="4ed2f-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="4ed2f-116">o si se especifican pocos argumentos.</span><span class="sxs-lookup"><span data-stu-id="4ed2f-116">or if too few arguments are specified.</span></span>

 

<span data-ttu-id="4ed2f-117">**Para redirigir la salida a un archivo**</span><span class="sxs-lookup"><span data-stu-id="4ed2f-117">**To redirect the output to a file**</span></span>

-   <span data-ttu-id="4ed2f-118">Finalice la línea de comandos con lo siguiente: **VBS > \[ ruta de acceso al archivo \] . T**</span><span class="sxs-lookup"><span data-stu-id="4ed2f-118">End the command line with the following: **VBS > \[path to file\]. T**</span></span>

> [!Note]  
> <span data-ttu-id="4ed2f-119">El ejemplo devuelve un valor de 0 (cero) para Success, 1 (uno) si se invoca la ayuda y 2 (dos) si se produce un error en el script.</span><span class="sxs-lookup"><span data-stu-id="4ed2f-119">The sample returns a value of 0 (zero) for success, 1 (one) if Help is invoked, and 2 (two) if the script fails.</span></span>

 

<span data-ttu-id="4ed2f-120">En la lista siguiente se identifican los elementos que debe especificar:</span><span class="sxs-lookup"><span data-stu-id="4ed2f-120">The following list identifies the items that you must specify:</span></span>

-   <span data-ttu-id="4ed2f-121">Especifique la ruta de acceso a la base de datos Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="4ed2f-121">Specify the path to the Windows Installer database.</span></span>
-   <span data-ttu-id="4ed2f-122">Especifique el nombre de la tabla de base de datos.</span><span class="sxs-lookup"><span data-stu-id="4ed2f-122">Specify the name of the database table.</span></span>
-   <span data-ttu-id="4ed2f-123">Especifique todos los valores de clave principal de la fila, en orden, y concatenados con dos puntos.</span><span class="sxs-lookup"><span data-stu-id="4ed2f-123">Specify all the primary key values for the row, in order, and concatenated with colons.</span></span>
-   <span data-ttu-id="4ed2f-124">Especifique un nombre de columna que no sea una columna de clave.</span><span class="sxs-lookup"><span data-stu-id="4ed2f-124">Specify a column name that is not a key column.</span></span> <span data-ttu-id="4ed2f-125">Esta es la columna que desea que reciba los datos.</span><span class="sxs-lookup"><span data-stu-id="4ed2f-125">This is the column that you want to receive the data.</span></span>
-   <span data-ttu-id="4ed2f-126">Especifique la ruta de acceso al archivo de texto que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="4ed2f-126">Specify the path to the text file that is being copied.</span></span>

> [!Note]  
> <span data-ttu-id="4ed2f-127">Si se omite el último argumento, se muestra el valor actual del campo.</span><span class="sxs-lookup"><span data-stu-id="4ed2f-127">If the last argument is omitted, the current value in the field is displayed.</span></span>

 

<span data-ttu-id="4ed2f-128">Para obtener más ejemplos de scripting, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="4ed2f-128">For more scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="4ed2f-129">Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="4ed2f-129">For sample utilities that do not require the Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



