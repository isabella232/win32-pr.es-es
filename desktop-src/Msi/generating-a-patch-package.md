---
description: El método recomendado para generar un paquete de revisión es usar una herramienta de creación de revisiones como Msimsp.exe para llamar a UiCreatePatchPackage en Patchwiz.dll. En el SDK de Windows Installer se proporcionan Msimsp.exe y PatchWiz.dll.
ms.assetid: 7fa661aa-d52c-4b08-961f-90ec778f02ff
title: Generar un paquete de revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef64ac66cd0201ae99080ec86e32230bc88407b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002263"
---
# <a name="generating-a-patch-package"></a><span data-ttu-id="f61eb-104">Generar un paquete de revisión</span><span class="sxs-lookup"><span data-stu-id="f61eb-104">Generating a Patch Package</span></span>

<span data-ttu-id="f61eb-105">El método recomendado para generar un paquete de revisión es usar una herramienta de creación de revisiones como [Msimsp.exe](msimsp-exe.md) para llamar a [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) en [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="f61eb-105">The recommended method for generating a patch package is to use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) to call [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="f61eb-106">En el SDK de Windows Installer se proporcionan Msimsp.exe y PatchWiz.dll.</span><span class="sxs-lookup"><span data-stu-id="f61eb-106">Msimsp.exe and PatchWiz.dll are provided in the Windows Installer SDK.</span></span>

<span data-ttu-id="f61eb-107">En la línea de comandos de ejemplo siguiente se usa Msimsp.exe y el archivo. PCP creado en [crear un archivo de propiedades de creación de revisiones](creating-a-patch-creation-properties-file.md) para generar el paquete de revisión de ejemplo MNP2000. msp.</span><span class="sxs-lookup"><span data-stu-id="f61eb-107">The following example command line uses Msimsp.exe and the .pcp file created in [Creating a Patch Creation Properties File](creating-a-patch-creation-properties-file.md) to generate the sample patch package MNP2000.msp.</span></span>

<span data-ttu-id="f61eb-108">**Msimsp.exe-s C: \\ Note \_ revisión del instalador \\ \\ MNP2000. PCP-p c: \\ Nota del \_ instalador \\ patch \\ MNP2000. MSP**</span><span class="sxs-lookup"><span data-stu-id="f61eb-108">**Msimsp.exe -s C:\\Note\_Installer\\Patch\\MNP2000.pcp -p C:\\Note\_Installer\\Patch\\MNP2000.msp**</span></span>

<span data-ttu-id="f61eb-109">Una herramienta de creación de revisiones creada puede generar el paquete de revisión llamando a [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="f61eb-109">An authored patch creation tool may generate the patch package by calling [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) as follows.</span></span>

``` syntax
UiCreatePatchPackage ("C:\\Note_Installer\\Patch\\MNP2000.pcp", "C:\\Note_Installer\\Patch\\MNP2000.msp", NULL, NULL, "", TRUE)
```

[<span data-ttu-id="f61eb-110">Continuar</span><span class="sxs-lookup"><span data-stu-id="f61eb-110">Continue</span></span>](applying-a-patch-package-to-a-local-installation.md)

 

 



