---
description: El WiLangID.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores.
ms.assetid: 319e9ffd-ff9f-4b4c-913e-2c571f2ec9ee
title: Administrar idioma y página de códigos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfb96f04d75ed79f32c8a49fe58b8dcc86f184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678402"
---
# <a name="manage-language-and-codepage"></a><span data-ttu-id="2a30b-103">Administrar idioma y página de códigos</span><span class="sxs-lookup"><span data-stu-id="2a30b-103">Manage Language and Codepage</span></span>

<span data-ttu-id="2a30b-104">El WiLangID.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="2a30b-104">The VBScript file WiLangID.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="2a30b-105">Este ejemplo muestra cómo se usa el script para tener acceso a la información de idioma y la página de códigos de un paquete.</span><span class="sxs-lookup"><span data-stu-id="2a30b-105">This sample shows how script is used to access a package's language information and codepage.</span></span> <span data-ttu-id="2a30b-106">Para obtener más información, vea [localizar un paquete de Windows Installer](localizing-a-windows-installer-package.md) y [control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="2a30b-106">For more information, see [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md) and [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

<span data-ttu-id="2a30b-107">En el ejemplo se muestra el uso de:</span><span class="sxs-lookup"><span data-stu-id="2a30b-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="2a30b-108">**Método OpenDatabase (objeto Installer)**</span><span class="sxs-lookup"><span data-stu-id="2a30b-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="2a30b-109">**Método CreateRecord**</span><span class="sxs-lookup"><span data-stu-id="2a30b-109">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="2a30b-110">[**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="2a30b-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="2a30b-111">**Método OpenView**</span><span class="sxs-lookup"><span data-stu-id="2a30b-111">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="2a30b-112">[**Propiedad SummaryInformation (objeto Database)**](database-summaryinformation.md) del [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="2a30b-112">[**SummaryInformation property (Database Object)**](database-summaryinformation.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="2a30b-113">El uso de este ejemplo requiere la versión CScript.exe o WScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="2a30b-113">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="2a30b-114">Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la siguiente sintaxis.</span><span class="sxs-lookup"><span data-stu-id="2a30b-114">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="2a30b-115">La ayuda se muestra si el primer argumento es/?</span><span class="sxs-lookup"><span data-stu-id="2a30b-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="2a30b-116">o si se especifican pocos argumentos.</span><span class="sxs-lookup"><span data-stu-id="2a30b-116">or if too few arguments are specified.</span></span> <span data-ttu-id="2a30b-117">Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] .</span><span class="sxs-lookup"><span data-stu-id="2a30b-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="2a30b-118">El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.</span><span class="sxs-lookup"><span data-stu-id="2a30b-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="2a30b-119">**cscript WiLangID.vbs la \[ ruta de acceso al valor de la \] \[ palabra clave Database \] \[\]**</span><span class="sxs-lookup"><span data-stu-id="2a30b-119">**cscript WiLangID.vbs \[path to database\]\[keyword\]\[value\]**</span></span>

<span data-ttu-id="2a30b-120">Especifique la ruta de acceso a la base de datos Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2a30b-120">Specify the path to the Windows Installer database.</span></span> <span data-ttu-id="2a30b-121">Para cambiar un valor, especifique una de las siguientes palabras clave seguido del nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="2a30b-121">To change a value specify one of the following keywords followed by the new value.</span></span> <span data-ttu-id="2a30b-122">Si no se especifica ningún valor, el ejemplo devuelve el valor actual.</span><span class="sxs-lookup"><span data-stu-id="2a30b-122">If no value is specified the sample returns the current value.</span></span>



| <span data-ttu-id="2a30b-123">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="2a30b-123">Keyword</span></span>      | <span data-ttu-id="2a30b-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a30b-124">Description</span></span>                                                                                                                                                                                |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a30b-125">**Package**</span><span class="sxs-lookup"><span data-stu-id="2a30b-125">**Package**</span></span>  | <span data-ttu-id="2a30b-126">Las versiones de idioma admitidas por la base de datos.</span><span class="sxs-lookup"><span data-stu-id="2a30b-126">The language versions supported by the database.</span></span> <span data-ttu-id="2a30b-127">Para obtener más información, consulte [**Template Summary**](template-summary.md) Property.</span><span class="sxs-lookup"><span data-stu-id="2a30b-127">For information, see [**Template Summary**](template-summary.md) property.</span></span>                                                               |
| <span data-ttu-id="2a30b-128">**Producto**</span><span class="sxs-lookup"><span data-stu-id="2a30b-128">**Product**</span></span>  | <span data-ttu-id="2a30b-129">Idioma que debe utilizar el instalador para cualquier cadena de la interfaz de usuario que no se haya creado en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="2a30b-129">Language the installer should use for any strings in the user interface that are not authored into the database.</span></span> <span data-ttu-id="2a30b-130">Para obtener más información, consulte propiedad [**ProductLanguage**](productlanguage.md) .</span><span class="sxs-lookup"><span data-stu-id="2a30b-130">For information, see [**ProductLanguage**](productlanguage.md) property.</span></span> |
| <span data-ttu-id="2a30b-131">**Codepage**</span><span class="sxs-lookup"><span data-stu-id="2a30b-131">**Codepage**</span></span> | <span data-ttu-id="2a30b-132">Página de códigos ANSI única para el grupo de cadenas.</span><span class="sxs-lookup"><span data-stu-id="2a30b-132">Single ANSI code page for the string pool.</span></span> <span data-ttu-id="2a30b-133">Para obtener más información, vea [control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="2a30b-133">For information, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>                                       |



 

<span data-ttu-id="2a30b-134">Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="2a30b-134">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="2a30b-135">En el caso de utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2a30b-135">For sample utilities that do not require Windows Script Host see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="2a30b-136">Para obtener más información, vea [determinar la página de códigos de una base](determining-an-installation-database-s-code-page.md) de datos de instalación y [establecer la página de códigos de una base de datos](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="2a30b-136">For more information, see [Determining an Installation Database's Code Page](determining-an-installation-database-s-code-page.md) and [Setting the Code Page of a Database](setting-the-code-page-of-a-database.md).</span></span>

 

 



