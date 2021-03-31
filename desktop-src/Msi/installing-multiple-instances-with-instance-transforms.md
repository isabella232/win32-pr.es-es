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
# <a name="installing-multiple-instances-with-instance-transforms"></a>Instalar varias instancias con transformaciones de instancia

En este tema se proporcionan instrucciones para instalar o volver a instalar una instalación de varias instancias de que usa transformaciones de instancia de.

-   Al instalar una nueva instancia de con una transformación de instancia, incluya la propiedad **MSINEWINSTANCE** y establezca **MSINEWINSTANCE**= 1.
-   Al instalar una nueva instancia de con una transformación de instancia, incluya la propiedad Transformations y establezca la primera transformación en la lista de transformaciones en la transformación de instancia que cambia el código de producto. Las transformaciones de personalización deben seguir la transformación de instancia al principio de esta lista.
-   La forma más sencilla de iniciar una instalación de mantenimiento y volver a instalar una instancia de es hacer referencia al código de producto de la instancia. Si inicia la instalación de mantenimiento mediante la ruta de acceso del paquete, también debe especificar el código de producto de la instancia. En la línea de comandos, use la opción/n {product code}. Desde código o script, use la propiedad **MSIINSTANCEGUID** .

En el ejemplo siguiente se muestra cómo instalar una nueva instancia desde una línea de comandos en la que la transformación de instancia tiene como prefijo un signo de dos puntos que especifica que la transformación está incrustada en el paquete.

**msiexec/I mypackage.msi Transformations =: Instance. MST MSINEWINSTANCE = 1/QB**

En el ejemplo siguiente se muestra cómo instalar una nueva instancia de mediante [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("TRANSFORMS=:instance.mst MSINEWINSTANCE=1"));
```

En el ejemplo siguiente se muestra la instalación de la nueva instancia desde el script.

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "TRANSFORMS=:instance.mst MSINEWINSTANCE=1"
```

En el ejemplo siguiente se vuelve a instalar una instancia sin volver a almacenar en caché el paquete. El código de producto hace referencia a la instancia {00000001-0002-0000-0000-624474736554} .

**msiexec/I {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = OMUs/QB**

En el ejemplo siguiente se vuelve a instalar una instancia de y se vuelve a almacenar en caché el paquete desde la línea de comandos. La ruta de acceso del paquete hace referencia a la instancia. Solo es necesario incluir la opción/n {Product Code} si el producto se instaló originalmente con una transformación de instancia.

**msiexec/I c: \\ newpath \\mypackage.msi/N {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = vomus/QB**

En el ejemplo siguiente se vuelve a instalar una instancia de y se almacena en caché el paquete con **MsiInstallProduct**. La ruta de acceso del paquete hace referencia a la instancia. Use la propiedad **MSIINSTANCEGUID** para proporcionar el código de producto de la instancia.

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"));
```

En el ejemplo siguiente se vuelve a instalar una instancia de y se almacena en caché el paquete mediante el script. Use la propiedad **MSIINSTANCEGUID** para proporcionar el código de producto de la instancia.

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"
```

En el ejemplo siguiente se muestra cómo anunciar una instancia de mediante la línea de comandos.

**msiexec/JM mypackage.msi/t: Instance. MST/c/QB**

En el ejemplo siguiente se muestra cómo instalar para anunciar una instancia mediante **MsiAdvertiseProductEx**.

``` syntax
UINT uiStat = MsiAdvertiseProductEx(_T("path to mypackage.msi"), NULL, _T(":instance.mst"), 0, 0, MSIADVERTISEOPTIONS_INSTANCE);
```

En el ejemplo siguiente se muestra cómo aplicar una revisión a una instancia desde una línea de comandos. Solo es necesario incluir la opción/n {Product Code} si el producto se instaló originalmente con una transformación de instancia.

**msiexec/p mi patch. MSP/n {00000001-0002-0000-0000-624474736554} /qb**

En el ejemplo siguiente se muestra cómo aplicar una revisión a una instalación de instancia mediante [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).

``` syntax
UINT uiStat = MsiApplyPatch(_T("path to mypatch.msp"), _T("{00000001-0002-0000-0000-624474736554}"), INSTALLTYPE_SINGLE_INSTANCE, _T("REINSTALL=ALL REINSTALLMODE=omus"));
```

Para obtener más información, consulte [instalación de varias instancias de productos y revisiones](installing-multiple-instances-of-products-and-patches.md) y [creación de varias instancias con transformaciones de instancias](authoring-multiple-instances-with-instance-transforms.md).

 

 



