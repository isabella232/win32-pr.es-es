---
description: La secuencia de la interfaz de usuario se importa en la base de datos de ejemplo.
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: Importación de InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f20de59a752da6d24a5f3e7fed94e00aa4f0048
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074427"
---
# <a name="importing-the-installuisequence"></a>Importación de InstallUISequence

En la [tabla InstallUISequence](installuisequence-table.md) se enumeran las acciones que se ejecutan cuando se ejecuta la acción [INSTALL](install-action.md) de nivel superior y el nivel de interfaz de usuario interno se establece en interfaz de usuario completa o interfaz de usuario reducida. El instalador omite las acciones de esta tabla si el nivel de interfaz de usuario está establecido en interfaz de usuario básica o en ninguna interfaz de usuario. Vea [Interfaz de usuario](user-interface.md) y [Interfaz de usuario niveles](user-interface-levels.md). Vea [Grupo de tablas de procedimientos de](installation-procedure-tables-group.md)instalación , Uso de una tabla de [secuencia](using-a-sequence-table.md)y Ejemplo detallado de tabla [de secuencia.](sequence-table-detailed-example.md)

Si en [](importing-a-blank-database.md) la sección Importación de una base de datos en blanco usó uisample.msi desde el SDK del instalador de Windows, las tablas de secuencia de la copia de MNP2000.msi ya contienen las secuencias de acciones sugeridas descritas en Uso de una tabla de [secuencia](using-a-sequence-table.md). No es necesario realizar ningún cambio en estas secuencias para crear el Bloc de notas de instalación.

Use el editor de bases de datos para MNP2000.msi y escriba los datos siguientes en la tabla InstallUISequence.

[Tabla InstallUISequence](installuisequence-table.md)



| Acción                | Condición                                    | Secuencia |
|-----------------------|----------------------------------------------|----------|
| AppSearch             |                                              | 400      |
| CCPSearch             | NO instalado                                | 500      |
| CostFinalize          |                                              | 1000     |
| CostInitialize        |                                              | 800      |
| ExecuteAction         |                                              | 1300     |
| ExitDlg               |                                              | -1       |
| FatalErrorDlg         |                                              | -3       |
| FileCost              |                                              | 900      |
| LaunchConditions      |                                              | 100      |
| MaintenanceWelcomeDlg | Instalado Y NO REANUDADO Y NO preseleccionado | 1250     |
| PrepareDlg            |                                              | 140      |
| ProgressDlg           |                                              | 1280     |
| ResumeDlg             | AND instalado (RESUME O preseleccionado)        | 1240     |
| RMCCPSearch           | NO instalado                                | 600      |
| UserExitDlg           |                                              | -2       |
| WelcomeDlg            | NO instalado                                | 1230     |
| MigrateFeatureStates  |                                              | 1200     |
| FindRelatedProducts   |                                              | 200      |



 

[Continuar](importing-the-adminexecutesequence.md)

 

 



