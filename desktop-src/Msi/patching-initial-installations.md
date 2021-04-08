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
# <a name="patching-initial-installations"></a>Aplicar revisiones a las instalaciones iniciales

Se puede aplicar una revisión de Windows Installer (MSP) al instalar una aplicación por primera vez mediante la propiedad [**patch**](patch.md) .

Para aplicar una revisión la primera vez que se instala la aplicación, se debe establecer la propiedad [**patch**](patch.md) en la línea de comandos. Especifique la ruta de acceso completa a la revisión en la línea de comandos como el par de propiedad-valor "PATCH = {*path to patch*}".

Tenga en cuenta que si se especifica la propiedad [**patch**](patch.md) en la línea de comandos, se reemplazarán las comprobaciones de aplicabilidad de patch realizadas al usar [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o la [opción de línea de comandos](command-line-options.md)/p.

Si se aplica una revisión mediante [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o la [opción de línea de comandos](command-line-options.md)/p, el instalador compara las aplicaciones instaladas actualmente en el equipo con la lista de códigos de producto que se puede seleccionar para recibir la revisión en la propiedad Resumen de la [**plantilla**](template-summary.md) .

Cuando se establece la propiedad [**patch**](patch.md) en la línea de comandos que se va a instalar en la primera instalación, las aplicaciones válidas para recibir la revisión vienen determinadas por las condiciones de validación de las transformaciones incrustadas en el paquete de revisión. El método recomendado para generar un paquete de revisión es usar una herramienta de creación de revisiones como [Msimsp.exe](msimsp-exe.md) y [PATCHWIZ.DLL](patchwiz-dll.md). Las condiciones de validación de las transformaciones de la revisión se originan en la columna ProductValidateFlags de la tabla [TargetImages](targetimages-table-patchwiz-dll-.md) del archivo de propiedades de creación de revisiones (. PCP).

La revisión se puede aplicar la primera vez que la aplicación se instala mediante una línea de comandos, otra aplicación o un script.

A continuación se muestra la revisión por primera vez desde la línea de comandos.

**msiexec/i** *package.msi* **patch =**_"c: \\ Directory \\ patch. MSP"_

A continuación se muestra la revisión por primera vez de otra aplicación.

``` syntax
UINT uiStat = MsiInstallProduct(_T("package.msi"), _T("PATCH=c:\directory\patch.msp"));
```

A continuación se muestra la revisión por primera vez del script.


```VB
Dim Installer as Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "package.msi", "PATCH=c:\directory\patch.msp"
```



* * Windows Installer 3,0 y versiones posteriores: * *

A partir de Windows Installer versión 3,0, se pueden aplicar varias revisiones al instalar una aplicación por primera vez. Establezca la propiedad [**patch**](patch.md) en una lista delimitada por punto y coma de las rutas de acceso completas de las revisiones. A continuación se muestra la revisión por primera vez de varias revisiones desde la línea de comandos.

**msiexec/i** *package.msi* **patch =**_"c: \\ Directory \\ patch. MSP; c: \\ Directory \\ Patch2. MSP; c: \\ Directory \\ Patch3. MSP"_

 

 



