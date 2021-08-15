---
description: Se Windows aplicación de revisión del instalador (MSP) al instalar una aplicación por primera vez mediante la propiedad PATCH.
ms.assetid: 2c4b9d5a-34fb-4a0b-b530-30bf238468fd
title: Aplicación de revisiones a las instalaciones iniciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf89c3a83a6000a5716b5317a9fc2965562c217b110b020a2795573f8175235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377638"
---
# <a name="patching-initial-installations"></a>Aplicación de revisiones a las instalaciones iniciales

Al instalar una aplicación por primera vez, se puede aplicar una revisión del instalador de Windows (MSP) mediante la [**propiedad PATCH.**](patch.md)

Para aplicar una revisión la primera vez que se instala la aplicación, la [**propiedad PATCH**](patch.md) debe establecerse en la línea de comandos. Especifique la ruta de acceso completa a la revisión en la línea de comandos como el par de propiedad-valor "PATCH={*path to patch*}".

Tenga en cuenta que al especificar la propiedad [**PATCH**](patch.md) en la línea de comandos se invalidan las comprobaciones de aplicabilidad de revisiones realizadas al usar [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o la opción de línea de comandos [/p](command-line-options.md).

Si se aplica una revisión mediante [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o la opción de línea de comandos [/p](command-line-options.md), el instalador compara [](template-summary.md) las aplicaciones instaladas actualmente en el equipo con la lista de códigos de producto aptos para recibir la revisión en la propiedad Resumen de plantilla.

Al establecer la [**propiedad PATCH**](patch.md) en la línea de comandos para instalarla en la primera instalación, las aplicaciones aptas para recibir la revisión se determinan mediante condiciones de validación en las transformaciones insertadas en el paquete de revisión. El método recomendado para generar un paquete de revisión es usar una herramienta de creación de revisiones como [Msimsp.exe](msimsp-exe.md) y [PATCHWIZ.DLL](patchwiz-dll.md). Las condiciones de validación en las transformaciones de la revisión se originan en la columna ProductValidateFlags de la tabla [TargetImages](targetimages-table-patchwiz-dll-.md) del archivo de propiedades de creación de revisiones (.condens).

La revisión se puede aplicar la primera vez que la aplicación se instala mediante una línea de comandos, otra aplicación o script.

A continuación se muestra la aplicación de revisiones por primera vez desde la línea de comandos.

**msiexec /I** *package.msi* **PATCH=**_"c: directory \\ \\ patch.msp"_

A continuación se muestra la aplicación de revisiones por primera vez desde otra aplicación.

``` syntax
UINT uiStat = MsiInstallProduct(_T("package.msi"), _T("PATCH=c:\directory\patch.msp"));
```

A continuación se muestra la aplicación de revisiones por primera vez desde el script.


```VB
Dim Installer as Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "package.msi", "PATCH=c:\directory\patch.msp"
```



**Windows Installer 3.0 y versiones posteriores: **

A partir Windows Installer versión 3.0, se pueden aplicar varias revisiones al instalar una aplicación por primera vez. Establezca la [**propiedad PATCH**](patch.md) en una lista delimitada por punto y coma de las rutas de acceso completas de las revisiones. A continuación se muestra la aplicación de revisiones por primera vez de varias revisiones desde la línea de comandos.

**msiexec /I** *package.msi* **PATCH=**_"c: directory \\ \\ patch.msp;c: directory \\ \\ patch2.msp;c: directory \\ \\ patch3.msp"_

 

 



