---
description: En la tabla InstallExecuteSequence se enumeran las acciones que se ejecutan cuando el instalador ejecuta la acción INSTALL de nivel superior. Vea Grupo de tablas de procedimientos de instalación, Uso de una tabla de secuencia y Ejemplo detallado de tabla de secuencia.
ms.assetid: cdd4f02a-cfe6-4a23-9fc2-f4cb810379aa
title: Importación de InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586557130c6aa9af197d5d28f6bd750f4de736feb6982f3b7f12ce73ccf41c83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430775"
---
# <a name="importing-the-installexecutesequence"></a>Importación de InstallExecuteSequence

En [la tabla InstallExecuteSequence](installexecutesequence-table.md) se enumeran las acciones que se ejecutan cuando el instalador ejecuta la acción [INSTALL de nivel superior.](install-action.md) Vea [Grupo de tablas de procedimientos de](installation-procedure-tables-group.md)instalación , Uso de una tabla de [secuencia](using-a-sequence-table.md)y Ejemplo detallado de tabla [de secuencias](sequence-table-detailed-example.md).

Si en [](importing-a-blank-database.md) la sección Importación de una base de datos en blanco usó uisample.msi desde el SDK del instalador de Windows, las tablas de secuencia de la copia de MNP2000.msi ya contienen las secuencias de acciones sugeridas descritas en Uso de una tabla de [secuencia.](using-a-sequence-table.md) No es necesario realizar ningún cambio en estas secuencias para crear el Bloc de notas de instalación.

Use el editor de bases de datos para MNP2000.msi y escriba los datos siguientes en la tabla InstallExecuteSequence.

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

 

 



