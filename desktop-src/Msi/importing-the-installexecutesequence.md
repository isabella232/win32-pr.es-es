---
description: En la tabla InstallExecuteSequence se enumeran las acciones que se ejecutan cuando el instalador ejecuta la acción de instalación de nivel superior. Vea Grupo de tablas de procedimientos de instalación, uso de una tabla de secuencia y el ejemplo detallado de la tabla de secuencia.
ms.assetid: cdd4f02a-cfe6-4a23-9fc2-f4cb810379aa
title: Importación de InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e4728b0a59c92dcc0d007fc816fd298455e049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002369"
---
# <a name="importing-the-installexecutesequence"></a>Importación de InstallExecuteSequence

En la [tabla InstallExecuteSequence](installexecutesequence-table.md) se enumeran las acciones que se ejecutan cuando el instalador ejecuta la [acción de instalación](install-action.md)de nivel superior. Vea [grupo de tablas de procedimientos de instalación](installation-procedure-tables-group.md), [uso de una tabla de secuencia](using-a-sequence-table.md)y el [ejemplo detallado](sequence-table-detailed-example.md)de la tabla de secuencia.

Si en la sección [importar una base de datos en blanco](importing-a-blank-database.md) usada uisample.msi del SDK de Windows Installer, las tablas de secuencia de la copia de MNP2000.msi ya contienen las secuencias de acción sugeridas que se describen en [uso de una tabla de secuencia](using-a-sequence-table.md). No es necesario realizar ningún cambio en estas secuencias para crear el paquete de instalación del Bloc de notas.

Utilice el editor de base de datos para abrir MNP2000.msi y escriba los datos siguientes en la tabla InstallExecuteSequence.

[Tabla InstallExecuteSequence](installexecutesequence-table.md)



| Acción                   | Condición     | Secuencia |
|--------------------------|---------------|----------|
| AllocateRegistrySpace    | NO instalado | 1550     |
| AppSearch                |               | 400      |
| BindImage                |               | 4300     |
| CCPSearch                | NO instalado | 500      |
| CostFinalize             |               | 1000     |
| CostInitialize           |               | 800      |
| CreateFolders            |               | 3700     |
| CreateShortcuts          |               | 4500     |
| DeleteServices           | VersionNT     | 2000     |
| DuplicateFiles           |               | 4210     |
| FileCost                 |               | 900      |
| FindRelatedProducts      |               | 200      |
| InstallFiles             |               | 4000     |
| InstallFinalize          |               | 6600     |
| InstallInitialize        |               | 1.500     |
| InstallODBC              |               | 5400     |
| InstallServices          | VersionNT     | 5800     |
| InstallValidate          |               | 1400     |
| LaunchConditions         |               | 100      |
| MigrateFeatureStates     |               | 1200     |
| MoveFiles                |               | 3800     |
| PatchFiles               |               | 4090     |
| ProcessComponents        |               | 1600     |
| PublishComponents        |               | 6200     |
| PublishFeatures          |               | 6300     |
| PublishProduct           |               | 6400     |
| RegisterClassInfo        |               | 4600     |
| RegisterComPlus          |               | 5700     |
| RegisterExtensionInfo    |               | 4700     |
| RegisterFonts            |               | 5300     |
| RegisterMIMEInfo         |               | 4900     |
| RegisterProduct          |               | 6100     |
| RegisterProgIdInfo       |               | 4800     |
| RegisterTypeLibraries    |               | 5500     |
| RegisterUser             |               | 6000     |
| RemoveDuplicateFiles     |               | 3400     |
| RemoveEnvironmentStrings |               | 3300     |
| RemoveExistingProducts   |               | 6700     |
| RemoveFiles              |               | 3500     |
| RemoveFolders            |               | 3600     |
| RemoveIniValues          |               | 3100     |
| RemoveODBC               |               | 2400     |
| RemoveRegistryValues     |               | 2600     |
| RemoveShortcuts          |               | 3200     |
| RMCCPSearch              | NO instalado | 600      |
| SelfRegModules           |               | 5600     |
| SelfUnregModules         |               | 2200     |
| SetODBCFolders           |               | 1100     |
| StartServices            | VersionNT     | 5900     |
| StopServices             | VersionNT     | 1900     |
| UnpublishComponents      |               | 1700     |
| UnpublishFeatures        |               | 1800     |
| UnregisterClassInfo      |               | 2700     |
| UnregisterComPlus        |               | 2100     |
| UnregisterExtensionInfo  |               | 2800     |
| UnregisterFonts          |               | 2.500     |
| UnregisterMIMEInfo       |               | 3000     |
| UnregisterProgIdInfo     |               | 2900     |
| UnregisterTypeLibraries  |               | 2300     |
| ValidateProductID        |               | 700      |
| WriteEnvironmentStrings  |               | 5200     |
| WriteIniValues           |               | 5100     |
| WriteRegistryValues      |               | 5000     |



 

[Continuar](importing-the-installuisequence.md)

 

 



