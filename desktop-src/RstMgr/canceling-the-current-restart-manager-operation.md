---
title: Cancelando la operación del administrador de reinicio actual
description: Cuando una acción del usuario indica al instalador que realice una acción diferente, se puede usar el método siguiente para cancelar la operación actual del administrador de reinicio.
ms.assetid: 87c8cf27-cd77-46fb-8298-cccbf4b1071a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633882cc723f19823c6b832ee6927c5a3aacaab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780196"
---
# <a name="canceling-the-current-restart-manager-operation"></a>Cancelando la operación del administrador de reinicio actual

Cuando una acción del usuario indica al instalador que realice una acción diferente, se puede usar el método siguiente para cancelar la operación actual del administrador de reinicio.

**Para cancelar la operación actual del administrador de reinicio**

-   El instalador puede llamar a la función [**RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) desde otro subproceso para cancelar la operación [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) o [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) actual. El administrador de reinicio puede cancelar la operación según la medida en la que se ha completado la operación cuando se llama a la función **RMCancelCurrentTask** .

 

 




