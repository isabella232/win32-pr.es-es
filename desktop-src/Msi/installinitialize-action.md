---
description: Las acciones InstallInitialize e InstallFinalize marcan el principio y el final de una secuencia de acciones que cambian el sistema.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: Acción InstallInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d500779ed018905edfc5347d85d21cc40e6175
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072038"
---
# <a name="installinitialize-action"></a>Acción InstallInitialize

Las acciones InstallInitialize e [InstallFinalize](installfinalize-action.md) marcan el principio y el final de una secuencia de acciones que cambian el sistema.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallInitialize debe secuenciarse antes de cualquier acción que cambie el sistema, como la acción [InstallFiles,](installfiles-action.md) [la acción WriteRegistryValues,](writeregistryvalues-action.md) la acción [SelfRegModules](selfregmodules-action.md) y la acción [ProcessComponents.](processcomponents-action.md) Por lo tanto, la acción InstallInitialize debe secuenciarse antes [de la acción InstallFinalize](installfinalize-action.md) y [la acción InstallExecute.](installexecute-action.md)

[](custom-actions.md) Las acciones personalizadas que modifican el paquete del instalador de Windows, por ejemplo [](registry-table.md) agregando filas a una tabla que controla los recursos instalables, como la tabla registry o [la tabla DuplicateFile,](duplicatefile-table.md) deben secuenciarse antes de la acción InstallInitialize.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

 

 



