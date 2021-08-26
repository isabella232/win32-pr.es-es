---
description: Las acciones InstallInitialize e InstallFinalize marcan el principio y el final de una secuencia de acciones que cambian el sistema.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: Acción InstallInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7031ab79bc099ea067fd8d83cb83d8cefd1f36a1e83f696a1ee3b4487b3cac88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996575"
---
# <a name="installinitialize-action"></a>Acción InstallInitialize

Las acciones InstallInitialize e [InstallFinalize](installfinalize-action.md) marcan el principio y el final de una secuencia de acciones que cambian el sistema.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallInitialize debe secuenciarse antes de cualquier acción que cambie el sistema, como la acción [InstallFiles,](installfiles-action.md) [la acción WriteRegistryValues,](writeregistryvalues-action.md) la acción [SelfRegModules](selfregmodules-action.md) y la acción [ProcessComponents.](processcomponents-action.md) Por lo tanto, la acción InstallInitialize debe secuenciarse antes [de la acción InstallFinalize](installfinalize-action.md) y [la acción InstallExecute.](installexecute-action.md)

[](custom-actions.md) Las acciones personalizadas que modifican el paquete del instalador de Windows, por ejemplo [](registry-table.md) agregando filas a una tabla que controla los recursos instalables, como la tabla del Registro o la tabla [DuplicateFile,](duplicatefile-table.md) deben secuenciarse antes de la acción InstallInitialize.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

 

 



