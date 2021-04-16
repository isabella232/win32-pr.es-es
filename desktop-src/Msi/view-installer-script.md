---
description: El WiLstScr.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este script de ejemplo muestra el visor de scripts de Windows Installer.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Ver script del instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56888f478bb7cdd43ebcee817c86f6f9f163840e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677521"
---
# <a name="view-installer-script"></a><span data-ttu-id="e769c-104">Ver script del instalador</span><span class="sxs-lookup"><span data-stu-id="e769c-104">View Installer Script</span></span>

<span data-ttu-id="e769c-105">El WiLstScr.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="e769c-105">The VBScript file WiLstScr.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="e769c-106">Este script de ejemplo muestra el visor de scripts de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e769c-106">This sample script demonstrates the Windows Installer script viewer.</span></span>

<span data-ttu-id="e769c-107">En el ejemplo se muestra el uso de:</span><span class="sxs-lookup"><span data-stu-id="e769c-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="e769c-108">**Método OpenDatabase (objeto Installer)**</span><span class="sxs-lookup"><span data-stu-id="e769c-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="e769c-109">Método [**LastErrorRecord**](installer-lasterrorrecord.md) del objeto [**Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="e769c-109">[**LastErrorRecord**](installer-lasterrorrecord.md) method of the [**Installer**](installer-object.md) object</span></span>
-   <span data-ttu-id="e769c-110">Método [**OpenView**](database-openview.md) del objeto [**Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="e769c-110">[**OpenView**](database-openview.md) method of the [**Database**](database-object.md) object</span></span>
-   <span data-ttu-id="e769c-111">Método [**Fetch**](view-fetch.md) del objeto [**View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="e769c-111">[**Fetch**](view-fetch.md) method of the [**View**](view-object.md) object</span></span>
-   <span data-ttu-id="e769c-112">Método [**FormatText**](record-formattext.md)</span><span class="sxs-lookup"><span data-stu-id="e769c-112">[**FormatText**](record-formattext.md) method</span></span>
-   <span data-ttu-id="e769c-113">Propiedad [**FieldCount**](record-fieldcount.md)</span><span class="sxs-lookup"><span data-stu-id="e769c-113">[**FieldCount**](record-fieldcount.md) property</span></span>
-   <span data-ttu-id="e769c-114">Propiedad [**StringData**](record-stringdata.md) del objeto [**Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="e769c-114">[**StringData**](record-stringdata.md) property of the [**Record**](record-object.md) object</span></span>
-   [<span data-ttu-id="e769c-115">\_Tabla TransformView</span><span class="sxs-lookup"><span data-stu-id="e769c-115">\_TransformView table</span></span>](-transformview-table.md)

<span data-ttu-id="e769c-116">El uso de este ejemplo requiere la versión CScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="e769c-116">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="e769c-117">Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la siguiente sintaxis.</span><span class="sxs-lookup"><span data-stu-id="e769c-117">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="e769c-118">La ayuda se muestra si el primer argumento es/?</span><span class="sxs-lookup"><span data-stu-id="e769c-118">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="e769c-119">o si se especifican pocos argumentos.</span><span class="sxs-lookup"><span data-stu-id="e769c-119">or if too few arguments are specified.</span></span> <span data-ttu-id="e769c-120">Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] .</span><span class="sxs-lookup"><span data-stu-id="e769c-120">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="e769c-121">El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.</span><span class="sxs-lookup"><span data-stu-id="e769c-121">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="e769c-122">**cscript WiLstScr.vbs** *\[ ruta de acceso a Windows Installer \] script de ejecución*</span><span class="sxs-lookup"><span data-stu-id="e769c-122">**cscript WiLstScr.vbs** *\[path to Windows Installer execution script\]*</span></span>

<span data-ttu-id="e769c-123">Especifique la ruta de acceso al script de ejecución del instalador.</span><span class="sxs-lookup"><span data-stu-id="e769c-123">Specify the path to the installer execution script.</span></span>

<span data-ttu-id="e769c-124">Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="e769c-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="e769c-125">Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e769c-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



