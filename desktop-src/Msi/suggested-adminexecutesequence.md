---
description: Las secuencias de acción sugeridas para una tabla AdminExecuteSequence básica en una base de datos Windows Installer.
ms.assetid: c54181d3-a16a-4007-a9ac-03ace98b637e
title: AdminExecuteSequence sugerido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ead890630b397062c6b8e645385b2810fa39d95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542726"
---
# <a name="suggested-adminexecutesequence"></a>AdminExecuteSequence sugerido



| Acción                                                | Condición | Secuencia |
|-------------------------------------------------------|-----------|----------|
| [CostInitialize](costinitialize-action.md)           |           | 800      |
| [FileCost](filecost-action.md)                       |           | 900      |
| [CostFinalize](costfinalize-action.md)               |           | 1000     |
| [InstallValidate](installvalidate-action.md)         |           | 1400     |
| [InstallInitialize](installinitialize-action.md)     |           | 1.500     |
| [InstallAdminPackage](installadminpackage-action.md) |           | 3900     |
| [InstallFiles](installfiles-action.md)               |           | 4000     |
| [InstallFinalize](installfinalize-action.md)         |           | 6600     |



 

 

 



