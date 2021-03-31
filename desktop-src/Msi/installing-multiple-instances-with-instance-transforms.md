---
description: En este tema se proporcionan instrucciones para instalar o volver a instalar una instalación de varias instancias de que usa transformaciones de instancia de.
ms.assetid: cf9076b1-5674-4ba8-9890-e981221d7b03
title: Instalar varias instancias con transformaciones de instancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bae8d73ad60567e1557257c1207558290ba29db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082281"
---
# <a name="installing-multiple-instances-with-instance-transforms"></a><span data-ttu-id="81c21-103">Instalar varias instancias con transformaciones de instancia</span><span class="sxs-lookup"><span data-stu-id="81c21-103">Installing Multiple Instances with Instance Transforms</span></span>

<span data-ttu-id="81c21-104">En este tema se proporcionan instrucciones para instalar o volver a instalar una instalación de varias instancias de que usa transformaciones de instancia de.</span><span class="sxs-lookup"><span data-stu-id="81c21-104">This topic provides guidelines for installing or reinstalling a multiple instance installation that uses instance transforms.</span></span>

-   <span data-ttu-id="81c21-105">Al instalar una nueva instancia de con una transformación de instancia, incluya la propiedad **MSINEWINSTANCE** y establezca **MSINEWINSTANCE**= 1.</span><span class="sxs-lookup"><span data-stu-id="81c21-105">When installing a new instance with an instance transform, include the **MSINEWINSTANCE** property and set **MSINEWINSTANCE**=1.</span></span>
-   <span data-ttu-id="81c21-106">Al instalar una nueva instancia de con una transformación de instancia, incluya la propiedad Transformations y establezca la primera transformación en la lista de transformaciones en la transformación de instancia que cambia el código de producto.</span><span class="sxs-lookup"><span data-stu-id="81c21-106">When installing a new instance with an instance transform, include the TRANSFORMS property and set the first transform in the list of transforms to the instance transform that changes the product code.</span></span> <span data-ttu-id="81c21-107">Las transformaciones de personalización deben seguir la transformación de instancia al principio de esta lista.</span><span class="sxs-lookup"><span data-stu-id="81c21-107">Any customization transforms should follow the instance transform at the beginning of this list.</span></span>
-   <span data-ttu-id="81c21-108">La forma más sencilla de iniciar una instalación de mantenimiento y volver a instalar una instancia de es hacer referencia al código de producto de la instancia.</span><span class="sxs-lookup"><span data-stu-id="81c21-108">The easiest way to initiate a maintenance installation, and reinstall an instance, is to reference the product code of the instance.</span></span> <span data-ttu-id="81c21-109">Si inicia la instalación de mantenimiento mediante la ruta de acceso del paquete, también debe especificar el código de producto de la instancia.</span><span class="sxs-lookup"><span data-stu-id="81c21-109">If you initiate the maintenance installation by using the package path, you must also specify the product code of the instance.</span></span> <span data-ttu-id="81c21-110">En la línea de comandos, use la opción/n {product code}.</span><span class="sxs-lookup"><span data-stu-id="81c21-110">From the command line, use the /n {Product Code} option.</span></span> <span data-ttu-id="81c21-111">Desde código o script, use la propiedad **MSIINSTANCEGUID** .</span><span class="sxs-lookup"><span data-stu-id="81c21-111">From code or script, use the **MSIINSTANCEGUID** property.</span></span>

<span data-ttu-id="81c21-112">En el ejemplo siguiente se muestra cómo instalar una nueva instancia desde una línea de comandos en la que la transformación de instancia tiene como prefijo un signo de dos puntos que especifica que la transformación está incrustada en el paquete.</span><span class="sxs-lookup"><span data-stu-id="81c21-112">The following example shows installing a new instance from a command line where the instance transform is prefixed by a colon which specifies that the transform is embedded in the package.</span></span>

<span data-ttu-id="81c21-113">**msiexec/I mypackage.msi Transformations =: Instance. MST MSINEWINSTANCE = 1/QB**</span><span class="sxs-lookup"><span data-stu-id="81c21-113">**msiexec /I mypackage.msi TRANSFORMS=:instance.mst MSINEWINSTANCE=1 /qb**</span></span>

<span data-ttu-id="81c21-114">En el ejemplo siguiente se muestra cómo instalar una nueva instancia de mediante [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).</span><span class="sxs-lookup"><span data-stu-id="81c21-114">The following example shows installing a new instance using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("TRANSFORMS=:instance.mst MSINEWINSTANCE=1"));
```

<span data-ttu-id="81c21-115">En el ejemplo siguiente se muestra la instalación de la nueva instancia desde el script.</span><span class="sxs-lookup"><span data-stu-id="81c21-115">The following example shows installing the new instance from script.</span></span>

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "TRANSFORMS=:instance.mst MSINEWINSTANCE=1"
```

<span data-ttu-id="81c21-116">En el ejemplo siguiente se vuelve a instalar una instancia sin volver a almacenar en caché el paquete.</span><span class="sxs-lookup"><span data-stu-id="81c21-116">The following example reinstalls an instance without re-caching the package.</span></span> <span data-ttu-id="81c21-117">El código de producto hace referencia a la instancia {00000001-0002-0000-0000-624474736554} .</span><span class="sxs-lookup"><span data-stu-id="81c21-117">The instance is referred to by its product code {00000001-0002-0000-0000-624474736554}.</span></span>

<span data-ttu-id="81c21-118">**msiexec/I {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = OMUs/QB**</span><span class="sxs-lookup"><span data-stu-id="81c21-118">**msiexec /I {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=omus /qb**</span></span>

<span data-ttu-id="81c21-119">En el ejemplo siguiente se vuelve a instalar una instancia de y se vuelve a almacenar en caché el paquete desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="81c21-119">The following example reinstalls an instance and re-caches the package from the command line.</span></span> <span data-ttu-id="81c21-120">La ruta de acceso del paquete hace referencia a la instancia.</span><span class="sxs-lookup"><span data-stu-id="81c21-120">The instance is referred to by the package path.</span></span> <span data-ttu-id="81c21-121">Solo es necesario incluir la opción/n {Product Code} si el producto se instaló originalmente con una transformación de instancia.</span><span class="sxs-lookup"><span data-stu-id="81c21-121">You are only required to include the /n {Product Code} option if the product is originally installed with an instance transform.</span></span>

<span data-ttu-id="81c21-122">**msiexec/I c: \\ newpath \\mypackage.msi/N {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = vomus/QB**</span><span class="sxs-lookup"><span data-stu-id="81c21-122">**msiexec /I c:\\newpath\\mypackage.msi /n {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=vomus /qb**</span></span>

<span data-ttu-id="81c21-123">En el ejemplo siguiente se vuelve a instalar una instancia de y se almacena en caché el paquete con **MsiInstallProduct**.</span><span class="sxs-lookup"><span data-stu-id="81c21-123">The following example reinstalls an instance and caches the package using **MsiInstallProduct**.</span></span> <span data-ttu-id="81c21-124">La ruta de acceso del paquete hace referencia a la instancia.</span><span class="sxs-lookup"><span data-stu-id="81c21-124">The instance is referred to by the package path.</span></span> <span data-ttu-id="81c21-125">Use la propiedad **MSIINSTANCEGUID** para proporcionar el código de producto de la instancia.</span><span class="sxs-lookup"><span data-stu-id="81c21-125">Use the **MSIINSTANCEGUID** property to provide the product code of the instance.</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"));
```

<span data-ttu-id="81c21-126">En el ejemplo siguiente se vuelve a instalar una instancia de y se almacena en caché el paquete mediante el script.</span><span class="sxs-lookup"><span data-stu-id="81c21-126">The following example reinstalls an instance and caches the package using script.</span></span> <span data-ttu-id="81c21-127">Use la propiedad **MSIINSTANCEGUID** para proporcionar el código de producto de la instancia.</span><span class="sxs-lookup"><span data-stu-id="81c21-127">Use the **MSIINSTANCEGUID** property to provide the product code of the instance.</span></span>

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"
```

<span data-ttu-id="81c21-128">En el ejemplo siguiente se muestra cómo anunciar una instancia de mediante la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="81c21-128">The following example shows how to advertise an instance using the command line.</span></span>

<span data-ttu-id="81c21-129">**msiexec/JM mypackage.msi/t: Instance. MST/c/QB**</span><span class="sxs-lookup"><span data-stu-id="81c21-129">**msiexec /jm mypackage.msi /t :instance.mst /c /qb**</span></span>

<span data-ttu-id="81c21-130">En el ejemplo siguiente se muestra cómo instalar para anunciar una instancia mediante **MsiAdvertiseProductEx**.</span><span class="sxs-lookup"><span data-stu-id="81c21-130">The following example shows how to install to advertise an instance using **MsiAdvertiseProductEx**.</span></span>

``` syntax
UINT uiStat = MsiAdvertiseProductEx(_T("path to mypackage.msi"), NULL, _T(":instance.mst"), 0, 0, MSIADVERTISEOPTIONS_INSTANCE);
```

<span data-ttu-id="81c21-131">En el ejemplo siguiente se muestra cómo aplicar una revisión a una instancia desde una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="81c21-131">The following example shows how to apply a patch to an instance from a command line.</span></span> <span data-ttu-id="81c21-132">Solo es necesario incluir la opción/n {Product Code} si el producto se instaló originalmente con una transformación de instancia.</span><span class="sxs-lookup"><span data-stu-id="81c21-132">You are only required to include the /n {Product Code} option if the product was originally installed with an instance transform.</span></span>

<span data-ttu-id="81c21-133">**msiexec/p mi patch. MSP/n {00000001-0002-0000-0000-624474736554} /qb**</span><span class="sxs-lookup"><span data-stu-id="81c21-133">**msiexec /p mypatch.msp /n {00000001-0002-0000-0000-624474736554} /qb**</span></span>

<span data-ttu-id="81c21-134">En el ejemplo siguiente se muestra cómo aplicar una revisión a una instalación de instancia mediante [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).</span><span class="sxs-lookup"><span data-stu-id="81c21-134">The following example shows how to apply a patch to an instance installation using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).</span></span>

``` syntax
UINT uiStat = MsiApplyPatch(_T("path to mypatch.msp"), _T("{00000001-0002-0000-0000-624474736554}"), INSTALLTYPE_SINGLE_INSTANCE, _T("REINSTALL=ALL REINSTALLMODE=omus"));
```

<span data-ttu-id="81c21-135">Para obtener más información, consulte [instalación de varias instancias de productos y revisiones](installing-multiple-instances-of-products-and-patches.md) y [creación de varias instancias con transformaciones de instancias](authoring-multiple-instances-with-instance-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="81c21-135">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md) and [Authoring Multiple Instances with Instance Transforms](authoring-multiple-instances-with-instance-transforms.md).</span></span>

 

 



