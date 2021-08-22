---
title: Cancelación de la operación del administrador de reinicio actual
description: Cuando una acción del usuario dirige al instalador a realizar una acción diferente, se puede usar el método siguiente para cancelar la operación de Restart Manager actual.
ms.assetid: 87c8cf27-cd77-46fb-8298-cccbf4b1071a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c745a76ab8c72acaff0b9f1ae85ded380e1113c3687822e916b422cad9ef51f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010253"
---
# <a name="canceling-the-current-restart-manager-operation"></a>Cancelación de la operación del administrador de reinicio actual

Cuando una acción del usuario dirige al instalador a realizar una acción diferente, se puede usar el método siguiente para cancelar la operación de Restart Manager actual.

**Para cancelar la operación actual del Administrador de reinicio**

-   El instalador puede llamar a la [**función RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) desde otro subproceso para cancelar la operación [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) o [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) actual. El Administrador de reinicio puede cancelar la operación en función de la medida en que se haya completado la operación cuando se llame a la **función RMCancelCurrentTask.**

 

 




