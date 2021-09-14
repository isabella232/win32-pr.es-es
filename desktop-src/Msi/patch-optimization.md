---
description: Windows El instalador puede optimizar la aplicación de revisiones para reducir el tiempo necesario para aplicar revisiones a las aplicaciones instaladas.
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: Optimización de revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86215855bb02314d7eb54c774541b0a2086c7c99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250886"
---
# <a name="patch-optimization"></a>Optimización de revisiones

Windows El instalador puede optimizar la aplicación de revisiones para reducir el tiempo necesario para aplicar revisiones a las aplicaciones instaladas.

**Windows Installer 2.0:** No se admite. Para las versiones de Windows Installer publicadas antes de Windows Installer 3.0, la aplicación de revisiones ejecuta una instalación de reparación completa de la aplicación, lo que puede tardar mucho más tiempo.

**Windows Installer 3.0 y versiones posteriores:** El proceso de aplicación de revisiones solo cambia las partes de una aplicación que se modifican mediante una revisión.

**Windows Installer 3.1 y versiones posteriores:** A partir de Windows Installer 3.1, la optimización de revisiones requiere que todas las revisiones de la transacción tengan la propiedad OptimizedInstallMode establecida en 1 (uno) en la tabla [MsiPatchMetadata](msipatchmetadata-table.md).

Si una revisión solo modifica las tablas siguientes, Windows Installer 3.0 o posterior omite las acciones asociadas con todas las demás tablas, incluso si esas acciones aparecen en las tablas de secuencia del paquete de instalación de la aplicación original (.msi archivo).

-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [Condition](condition-table.md)
-   [CustomAction](customaction-table.md)
-   [Archivo](file-table.md)
-   [FileSFPCatalog](filesfpcatalog-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [Elementos multimedia](media-table.md)
-   [MoveFile](movefile-table.md)
-   [MsiAssembly](msiassembly-table.md)
-   [MsiDigitalCertificate](msidigitalcertificate-table.md)
-   [MsiDigitalSignature](msidigitalsignature-table.md)
-   [MsiFileHash](msifilehash-table.md)
-   [MsiPatchHeaders](msipatchheaders-table.md)
-   [Revisión](patch-table.md)
-   [PatchPackage](patchpackage-table.md)
-   [Propiedad](property-table.md)
-   [Registro](registry-table.md)
-   [SFPCatalog](sfpcatalog-table.md)
-   [Typelib](typelib-table.md)
-   [\_Columnas](-columns-table.md)
-   [\_Almacenajes](-storages-table.md)
-   [\_Secuencias](-streams-table.md)
-   [\_Tablas](-tables-table.md)
-   [\_Tabla TransformView](-transformview-table.md)
-   [\_Validación](-validation-table.md)

Para desactivar la opción de optimización de revisiones, use [la directiva DisableFlyWeightPatching.](disableflyweightpatching.md)

 

 



