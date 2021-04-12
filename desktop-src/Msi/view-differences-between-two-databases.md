---
description: El WiDiffDb.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este script de ejemplo genera un archivo de transformación temporal entre dos bases de datos de Windows Installer y muestra la transformación.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Ver las diferencias entre dos bases de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b0c97afc0bd7145170209ed87497b6af90e64d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541190"
---
# <a name="view-differences-between-two-databases"></a><span data-ttu-id="027df-104">Ver las diferencias entre dos bases de datos</span><span class="sxs-lookup"><span data-stu-id="027df-104">View Differences Between Two Databases</span></span>

<span data-ttu-id="027df-105">El WiDiffDb.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="027df-105">The VBScript file WiDiffDb.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="027df-106">Este script de ejemplo genera un archivo de transformación temporal entre dos bases de datos de Windows Installer y muestra la transformación.</span><span class="sxs-lookup"><span data-stu-id="027df-106">This sample script generates a temporary transform file between two Windows Installer databases and displays the transform.</span></span>

<span data-ttu-id="027df-107">En el ejemplo se muestra el uso de:</span><span class="sxs-lookup"><span data-stu-id="027df-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="027df-108">**Método OpenDatabase (objeto Installer)**</span><span class="sxs-lookup"><span data-stu-id="027df-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="027df-109">[**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="027df-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="027df-110">**Método OpenView**</span><span class="sxs-lookup"><span data-stu-id="027df-110">**OpenView method**</span></span>](database-openview.md)
-   [<span data-ttu-id="027df-111">**Propiedad SummaryInformation (objeto Database)**</span><span class="sxs-lookup"><span data-stu-id="027df-111">**SummaryInformation property (Database Object)**</span></span>](database-summaryinformation.md)
-   [<span data-ttu-id="027df-112">**Método GenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="027df-112">**GenerateTransform method**</span></span>](database-generatetransform.md)
-   [<span data-ttu-id="027df-113">**Método ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="027df-113">**ApplyTransform method**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="027df-114">**Objeto de base de datos**</span><span class="sxs-lookup"><span data-stu-id="027df-114">**Database object**</span></span>](database-object.md)
-   <span data-ttu-id="027df-115">[**Método fetch**](view-fetch.md) del [ **objeto View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="027df-115">[**Fetch method**](view-fetch.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="027df-116">**Propiedad IsNull**</span><span class="sxs-lookup"><span data-stu-id="027df-116">**IsNull property**</span></span>](record-isnull.md)
-   <span data-ttu-id="027df-117">[**Propiedad StringData**](record-stringdata.md) del [ **objeto record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="027df-117">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>
-   [<span data-ttu-id="027df-118">\_Tabla TransformView</span><span class="sxs-lookup"><span data-stu-id="027df-118">\_TransformView table</span></span>](-transformview-table.md)

<span data-ttu-id="027df-119">El uso de este ejemplo requiere la versión CScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="027df-119">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="027df-120">Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la siguiente sintaxis.</span><span class="sxs-lookup"><span data-stu-id="027df-120">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="027df-121">La ayuda se muestra si el primer argumento es/?</span><span class="sxs-lookup"><span data-stu-id="027df-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="027df-122">o si se especifican pocos argumentos.</span><span class="sxs-lookup"><span data-stu-id="027df-122">or if too few arguments are specified.</span></span> <span data-ttu-id="027df-123">Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] .</span><span class="sxs-lookup"><span data-stu-id="027df-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="027df-124">El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.</span><span class="sxs-lookup"><span data-stu-id="027df-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="027df-125">**cscript WiDiffDb.vbs** ruta de acceso de la base de datos *\[ original \] \[ a la base de datos \] revisada*</span><span class="sxs-lookup"><span data-stu-id="027df-125">**cscript WiDiffDb.vbs** *\[path to original database\]\[path to revised database\]*</span></span>

<span data-ttu-id="027df-126">Especifique la ruta de acceso a la base de datos de Windows Installer original.</span><span class="sxs-lookup"><span data-stu-id="027df-126">Specify the path to the original Windows Installer database.</span></span> <span data-ttu-id="027df-127">Especifique la ruta de acceso a la base de datos revisada.</span><span class="sxs-lookup"><span data-stu-id="027df-127">Specify the path to the revised database.</span></span> <span data-ttu-id="027df-128">El script de ejemplo mostrará la transformación.</span><span class="sxs-lookup"><span data-stu-id="027df-128">The sample script will display the transform.</span></span>

<span data-ttu-id="027df-129">Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="027df-129">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="027df-130">Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="027df-130">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



