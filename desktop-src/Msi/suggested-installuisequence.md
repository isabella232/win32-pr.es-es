---
description: Secuencias de acciones sugeridas para una tabla InstalUISequence básica en una base de Windows Installer.
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: Instalación sugeridaUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab5c65ed594cf86f86555de235d0ceb0530b9f3e233bfdf5c38d094ca9719a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624337"
---
# <a name="suggested-installuisequence"></a>Instalación sugeridaUISequence



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
| ResumeDlg                                       | [**Instalado**](installed.md) AND ( [**RESUME**](resume.md) OR [**Preselected**](preselected.md))       | 1240     |
| MaintenanceWelcomeDlg                           | [**Instalado**](installed.md) AND NOT [**RESUME**](resume.md) AND NOT [**Preselected**](preselected.md) | 1250     |
| ProgressDlg                                     |                                                                                                            | 1280     |
| [ExecuteAction](executeaction-action.md)       |                                                                                                            | 1300     |



 

 

 



