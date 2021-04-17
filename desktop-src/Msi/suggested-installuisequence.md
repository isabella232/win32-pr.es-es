---
description: Las secuencias de acción sugeridas para una tabla InstalUISequence básica en una base de datos Windows Installer.
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: InstallUISequence sugerido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1accfc889d51cb75b3928df60931c848b30bcad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652734"
---
# <a name="suggested-installuisequence"></a>InstallUISequence sugerido



| Acción                                          | Condición                                                                                                  | Secuencia |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|
| FatalErrorDlg                                   |                                                                                                            | -3       |
| UserExitDlg                                     |                                                                                                            | -2       |
| ExitDlg                                         |                                                                                                            | -1       |
| [LaunchConditions](launchconditions-action.md) |                                                                                                            | 100      |
| PrepareDlg                                      |                                                                                                            | 140      |
| [AppSearch](appsearch-action.md)               |                                                                                                            | 400      |
| [CCPSearch](ccpsearch-action.md)               | NO [ **instalado**](installed.md)                                                                         | 500      |
| [RMCCPSearch](rmccpsearch-action.md)           | NO [ **instalado**](installed.md)                                                                         | 600      |
| [CostInitialize](costinitialize-action.md)     |                                                                                                            | 800      |
| [FileCost](filecost-action.md)                 |                                                                                                            | 900      |
| [CostFinalize](costfinalize-action.md)         |                                                                                                            | 1000     |
| WelcomeDlg                                      | NO [ **instalado**](installed.md)                                                                         | 1230     |
| ResumeDlg                                       | [**Instalado**](installed.md) Y ( [**reanudar**](resume.md) o [**preseleccionar**](preselected.md))       | 1240     |
| MaintenanceWelcomeDlg                           | [**Instalado**](installed.md) Y no se [**reanudan**](resume.md) y no se [**preseleccionan**](preselected.md) | 1250     |
| ProgressDlg                                     |                                                                                                            | 1280     |
| [ExecuteAction](executeaction-action.md)       |                                                                                                            | 1300     |



 

 

 



