---
description: La secuencia de la interfaz de usuario se importa en la base de datos de ejemplo.
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: Importación de InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f20de59a752da6d24a5f3e7fed94e00aa4f0048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277743"
---
# <a name="importing-the-installuisequence"></a>Importación de InstallUISequence

En la [tabla InstallUISequence](installuisequence-table.md) se enumeran las acciones que se ejecutan cuando se ejecuta la [acción de instalación](install-action.md) de nivel superior y el nivel interno de la interfaz de usuario se establece en interfaz de usuario completa o en interfaz de usuario reducida. El instalador omite las acciones de esta tabla si el nivel de la interfaz de usuario se establece en la interfaz de usuario básica o en ninguna interfaz de usuario. Vea [los niveles](user-interface-levels.md)de interfaz [de usuario y](user-interface.md) interfaz de usuario. Vea [grupo de tablas de procedimientos de instalación](installation-procedure-tables-group.md), [uso de una tabla de secuencia](using-a-sequence-table.md)y el [ejemplo detallado](sequence-table-detailed-example.md)de la tabla de secuencia.

Si en la sección [importar una base de datos en blanco](importing-a-blank-database.md) usada uisample.msi del SDK de Windows Installer, las tablas de secuencia de la copia de MNP2000.msi ya contienen las secuencias de acción sugeridas que se describen en [uso de una tabla de secuencia](using-a-sequence-table.md). No es necesario realizar ningún cambio en estas secuencias para crear el paquete de instalación del Bloc de notas.

Utilice el editor de base de datos para abrir MNP2000.msi y escriba los datos siguientes en la tabla InstallUISequence.

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
| MaintenanceWelcomeDlg | Instalado, no REANUDAdo y no preseleccionado | 1250     |
| PrepareDlg            |                                              | 140      |
| ProgressDlg           |                                              | 1280     |
| ResumeDlg             | Instalado y (REANUDAr o preseleccionado)        | 1240     |
| RMCCPSearch           | NO instalado                                | 600      |
| UserExitDlg           |                                              | -2       |
| WelcomeDlg            | NO instalado                                | 1230     |
| MigrateFeatureStates  |                                              | 1200     |
| FindRelatedProducts   |                                              | 200      |



 

[Continuar](importing-the-adminexecutesequence.md)

 

 



