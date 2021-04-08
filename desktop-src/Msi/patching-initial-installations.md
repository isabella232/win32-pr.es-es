---
description: Se puede aplicar una revisión de Windows Installer (MSP) al instalar una aplicación por primera vez mediante la propiedad PATCH.
ms.assetid: 2c4b9d5a-34fb-4a0b-b530-30bf238468fd
title: Aplicar revisiones a las instalaciones iniciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa85e15da18f7342f38cf82228bc31b6e3085f09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003043"
---
# <a name="patching-initial-installations"></a><span data-ttu-id="a041e-103">Aplicar revisiones a las instalaciones iniciales</span><span class="sxs-lookup"><span data-stu-id="a041e-103">Patching Initial Installations</span></span>

<span data-ttu-id="a041e-104">Se puede aplicar una revisión de Windows Installer (MSP) al instalar una aplicación por primera vez mediante la propiedad [**patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="a041e-104">A Windows Installer Patch (MSP) can be applied when installing an application for the first time by using the [**PATCH**](patch.md) property.</span></span>

<span data-ttu-id="a041e-105">Para aplicar una revisión la primera vez que se instala la aplicación, se debe establecer la propiedad [**patch**](patch.md) en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a041e-105">To apply a patch the first time the application is installed, the [**PATCH**](patch.md) property must be set on the command line.</span></span> <span data-ttu-id="a041e-106">Especifique la ruta de acceso completa a la revisión en la línea de comandos como el par de propiedad-valor "PATCH = {*path to patch*}".</span><span class="sxs-lookup"><span data-stu-id="a041e-106">Specify the full path to the patch on the command line as the "PATCH={*path to patch*}" property-value pair.</span></span>

<span data-ttu-id="a041e-107">Tenga en cuenta que si se especifica la propiedad [**patch**](patch.md) en la línea de comandos, se reemplazarán las comprobaciones de aplicabilidad de patch realizadas al usar [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o la [opción de línea de comandos](command-line-options.md)/p.</span><span class="sxs-lookup"><span data-stu-id="a041e-107">Note that specifying the [**PATCH**](patch.md) property on the command line overrides the patch applicability checks performed when using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the /p [Command Line Option](command-line-options.md).</span></span>

<span data-ttu-id="a041e-108">Si se aplica una revisión mediante [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o la [opción de línea de comandos](command-line-options.md)/p, el instalador compara las aplicaciones instaladas actualmente en el equipo con la lista de códigos de producto que se puede seleccionar para recibir la revisión en la propiedad Resumen de la [**plantilla**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="a041e-108">If a patch is applied using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the /p [Command Line Option](command-line-options.md), the installer compares the applications currently installed on the computer to the list of product codes eligible to receive the patch in the [**Template Summary**](template-summary.md) property.</span></span>

<span data-ttu-id="a041e-109">Cuando se establece la propiedad [**patch**](patch.md) en la línea de comandos que se va a instalar en la primera instalación, las aplicaciones válidas para recibir la revisión vienen determinadas por las condiciones de validación de las transformaciones incrustadas en el paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="a041e-109">When you set the [**PATCH**](patch.md) property on the command line to install on first installation, the applications eligible to receive the patch is determined by validation conditions on the transforms embedded in the patch package.</span></span> <span data-ttu-id="a041e-110">El método recomendado para generar un paquete de revisión es usar una herramienta de creación de revisiones como [Msimsp.exe](msimsp-exe.md) y [PATCHWIZ.DLL](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="a041e-110">The recommended method for generating a patch package is to use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) and [PATCHWIZ.DLL](patchwiz-dll.md).</span></span> <span data-ttu-id="a041e-111">Las condiciones de validación de las transformaciones de la revisión se originan en la columna ProductValidateFlags de la tabla [TargetImages](targetimages-table-patchwiz-dll-.md) del archivo de propiedades de creación de revisiones (. PCP).</span><span class="sxs-lookup"><span data-stu-id="a041e-111">The validation conditions on transforms in the patch originate from the ProductValidateFlags column in the [TargetImages](targetimages-table-patchwiz-dll-.md) table of the Patch Creation Properties (.pcp) file.</span></span>

<span data-ttu-id="a041e-112">La revisión se puede aplicar la primera vez que la aplicación se instala mediante una línea de comandos, otra aplicación o un script.</span><span class="sxs-lookup"><span data-stu-id="a041e-112">The patch can be applied the first time the application is installed by a command line, another application, or script.</span></span>

<span data-ttu-id="a041e-113">A continuación se muestra la revisión por primera vez desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a041e-113">The following shows first-time patching from the command line.</span></span>

<span data-ttu-id="a041e-114">**msiexec/i** *package.msi* **patch =**_"c: \\ Directory \\ patch. MSP"_</span><span class="sxs-lookup"><span data-stu-id="a041e-114">**msiexec /I** *package.msi* **PATCH=**_"c:\\directory\\patch.msp"_</span></span>

<span data-ttu-id="a041e-115">A continuación se muestra la revisión por primera vez de otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="a041e-115">The following shows first-time patching from another application.</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("package.msi"), _T("PATCH=c:\directory\patch.msp"));
```

<span data-ttu-id="a041e-116">A continuación se muestra la revisión por primera vez del script.</span><span class="sxs-lookup"><span data-stu-id="a041e-116">The following shows first-time patching from script.</span></span>


```VB
Dim Installer as Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "package.msi", "PATCH=c:\directory\patch.msp"
```



<span data-ttu-id="a041e-117">\* \* Windows Installer 3,0 y versiones posteriores: \* \*</span><span class="sxs-lookup"><span data-stu-id="a041e-117">\*\*Windows Installer 3.0 and later:  \*\*</span></span>

<span data-ttu-id="a041e-118">A partir de Windows Installer versión 3,0, se pueden aplicar varias revisiones al instalar una aplicación por primera vez.</span><span class="sxs-lookup"><span data-stu-id="a041e-118">Beginning with Windows Installer version 3.0, multiple patches can be applied when installing an application for the first time.</span></span> <span data-ttu-id="a041e-119">Establezca la propiedad [**patch**](patch.md) en una lista delimitada por punto y coma de las rutas de acceso completas de las revisiones.</span><span class="sxs-lookup"><span data-stu-id="a041e-119">Set the [**PATCH**](patch.md) property to a semicolon delimited list of the patches' full paths.</span></span> <span data-ttu-id="a041e-120">A continuación se muestra la revisión por primera vez de varias revisiones desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a041e-120">The following shows first-time patching of multiple patches from the command line.</span></span>

<span data-ttu-id="a041e-121">**msiexec/i** *package.msi* **patch =**_"c: \\ Directory \\ patch. MSP; c: \\ Directory \\ Patch2. MSP; c: \\ Directory \\ Patch3. MSP"_</span><span class="sxs-lookup"><span data-stu-id="a041e-121">**msiexec /I** *package.msi* **PATCH=**_"c:\\directory\\patch.msp;c:\\directory\\patch2.msp;c:\\directory\\patch3.msp"_</span></span>

 

 



