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
# <a name="generating-a-patch-package"></a>Generar un paquete de revisión

El método recomendado para generar un paquete de revisión es usar una herramienta de creación de revisiones como [Msimsp.exe](msimsp-exe.md) para llamar a [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) en [Patchwiz.dll](patchwiz-dll.md). En el SDK de Windows Installer se proporcionan Msimsp.exe y PatchWiz.dll.

En la línea de comandos de ejemplo siguiente se usa Msimsp.exe y el archivo. PCP creado en [crear un archivo de propiedades de creación de revisiones](creating-a-patch-creation-properties-file.md) para generar el paquete de revisión de ejemplo MNP2000. msp.

**Msimsp.exe-s C: \\ Note \_ revisión del instalador \\ \\ MNP2000. PCP-p c: \\ Nota del \_ instalador \\ patch \\ MNP2000. MSP**

Una herramienta de creación de revisiones creada puede generar el paquete de revisión llamando a [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) como se indica a continuación.

``` syntax
UiCreatePatchPackage ("C:\\Note_Installer\\Patch\\MNP2000.pcp", "C:\\Note_Installer\\Patch\\MNP2000.msp", NULL, NULL, "", TRUE)
```

[Continuar](applying-a-patch-package-to-a-local-installation.md)

 

 



