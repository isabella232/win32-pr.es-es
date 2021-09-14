---
description: El método recomendado para generar un paquete de revisión es usar una herramienta de creación de revisiones como Msimsp.exe para llamar a UiCreatePatchPackage en Patchwiz.dll. Msimsp.exe y PatchWiz.dll se proporcionan en el SDK Windows Installer.
ms.assetid: 7fa661aa-d52c-4b08-961f-90ec778f02ff
title: Generar un paquete de revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef64ac66cd0201ae99080ec86e32230bc88407b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074739"
---
# <a name="generating-a-patch-package"></a>Generar un paquete de revisión

El método recomendado para generar un paquete de revisión es usar una herramienta de creación de revisiones [ comoMsimsp.exe](msimsp-exe.md) para llamar a [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) [ enPatchwiz.dll](patchwiz-dll.md). Msimsp.exe y PatchWiz.dll se proporcionan en el SDK Windows Installer.

En la línea de comandos de ejemplo siguiente se usa Msimsp.exe y el archivo .msp creado en [Crear](creating-a-patch-creation-properties-file.md) un archivo de propiedades de creación de revisiones para generar el paquete de revisión de ejemplo MNP2000.msp.

**Msimsp.exe -s C: Nota Revisión del instalador \\ \_ \\ \\ MNP2000.debian -p C: Nota Revisión del instalador \\ \_ \\ \\ MNP2000.msp**

Una herramienta de creación de revisiones puede generar el paquete de revisión mediante una llamada a [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) como se muestra a continuación.

``` syntax
UiCreatePatchPackage ("C:\\Note_Installer\\Patch\\MNP2000.pcp", "C:\\Note_Installer\\Patch\\MNP2000.msp", NULL, NULL, "", TRUE)
```

[Continuar](applying-a-patch-package-to-a-local-installation.md)

 

 



