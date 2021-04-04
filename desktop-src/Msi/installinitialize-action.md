---
description: La acción InstallInitialize y la acción InstallFinalize marcan el principio y el final de una secuencia de acciones que cambian el sistema.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: Acción InstallInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d500779ed018905edfc5347d85d21cc40e6175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810303"
---
# <a name="installinitialize-action"></a>Acción InstallInitialize

La acción InstallInitialize y la acción [InstallFinalize](installfinalize-action.md) marcan el principio y el final de una secuencia de acciones que cambian el sistema.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallInitialize se debe secuenciar antes que cualquier acción que cambie el sistema, como la acción [InstallFiles](installfiles-action.md) , la acción [WriteRegistryValues](writeregistryvalues-action.md) , la acción [SelfRegModules](selfregmodules-action.md) y la acción [ProcessComponents](processcomponents-action.md) . Por lo tanto, la acción InstallInitialize se debe secuenciar antes de la acción [InstallFinalize](installfinalize-action.md) y la acción [InstallExecute](installexecute-action.md) .

Las [acciones personalizadas](custom-actions.md) que modifican el paquete de Windows Installer, por ejemplo, agregando filas a una tabla que controla los recursos instalables, como la tabla [del registro](registry-table.md) o la tabla [DuplicateFile](duplicatefile-table.md) , se deben secuenciar antes de la acción InstallInitialize.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

 

 



