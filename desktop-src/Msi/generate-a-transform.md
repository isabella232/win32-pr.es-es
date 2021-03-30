---
description: El WiGenXfm.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este script de ejemplo puede generar una transformación de dos bases de datos Windows Installer. Para obtener más información, vea transformaciones de base de datos.
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: Generar una transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92617c2e007b9deb01685679d4940095285b8218
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815214"
---
# <a name="generate-a-transform"></a><span data-ttu-id="ff9ad-105">Generar una transformación</span><span class="sxs-lookup"><span data-stu-id="ff9ad-105">Generate a Transform</span></span>

<span data-ttu-id="ff9ad-106">El WiGenXfm.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="ff9ad-106">The VBScript file WiGenXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="ff9ad-107">Este script de ejemplo puede generar una transformación de dos bases de datos Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-107">This sample script can generate a transform from two Windows Installer databases.</span></span> <span data-ttu-id="ff9ad-108">Para obtener más información, vea [transformaciones de base de datos](database-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="ff9ad-108">For more information see [Database Transforms](database-transforms.md).</span></span>

<span data-ttu-id="ff9ad-109">En el ejemplo se muestra el uso de:</span><span class="sxs-lookup"><span data-stu-id="ff9ad-109">The sample demonstrates the use of:</span></span>

[<span data-ttu-id="ff9ad-110">**Método OpenDatabase (objeto Installer)**</span><span class="sxs-lookup"><span data-stu-id="ff9ad-110">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)

<span data-ttu-id="ff9ad-111">[**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="ff9ad-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>

<span data-ttu-id="ff9ad-112">[**Método GenerateTransform**](database-generatetransform.md) del [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="ff9ad-112">[**GenerateTransform method**](database-generatetransform.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="ff9ad-113">Para usar este ejemplo, necesitará la versión CScript.exe o WScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-113">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="ff9ad-114">Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la siguiente sintaxis.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-114">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="ff9ad-115">La ayuda se muestra si el primer argumento es/?</span><span class="sxs-lookup"><span data-stu-id="ff9ad-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="ff9ad-116">o si se especifican pocos argumentos.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-116">or if too few arguments are specified.</span></span> <span data-ttu-id="ff9ad-117">Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] .</span><span class="sxs-lookup"><span data-stu-id="ff9ad-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="ff9ad-118">El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="ff9ad-119">**cscript WiGenXfm.vbs \[ ruta de acceso de la base de datos original a la ruta de acceso de la \] \[ base de datos revisada \] \[\]**</span><span class="sxs-lookup"><span data-stu-id="ff9ad-119">**cscript WiGenXfm.vbs \[path to original database\]\[path to revised database\]\[path to transform file\]**</span></span>

<span data-ttu-id="ff9ad-120">Especifique la ruta de acceso a la base de datos de Windows Installer original.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-120">Specify the path to the original Windows Installer database.</span></span> <span data-ttu-id="ff9ad-121">Especifique la ruta de acceso a la base de datos revisada.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-121">Specify the path to the revised database.</span></span> <span data-ttu-id="ff9ad-122">Especifique la ruta de acceso al archivo de transformación que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-122">Specify the path to the transform file to be created.</span></span> <span data-ttu-id="ff9ad-123">Si se omite la ruta de acceso al archivo de transformación, las dos bases de datos solo se comparan.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-123">If the path to the transform file is omitted, the two databases are only compared.</span></span>

<span data-ttu-id="ff9ad-124">Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="ff9ad-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="ff9ad-125">Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ff9ad-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="ff9ad-126">Tenga en cuenta que [un ejemplo de localización](a-localization-example.md) muestra [la generación de una transformación de personalización](generating-a-customization-transform.md).</span><span class="sxs-lookup"><span data-stu-id="ff9ad-126">Note that [A Localization Example](a-localization-example.md) demonstrates [Generating a Customization Transform](generating-a-customization-transform.md).</span></span>

 

 



