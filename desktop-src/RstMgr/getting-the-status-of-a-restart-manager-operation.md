---
title: Obtener el estado de una operación del Administrador de reinicio
description: Cuando muchas aplicaciones y servicios deben apagarse o reiniciarse, la operación restart Manager puede tardar un largo período de tiempo. El método siguiente se puede usar para obtener el estado de la operación actual.
ms.assetid: 0df9de1f-df37-46a5-8010-6c8b34429376
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f96b7e247bdeb661e29d39cbb64bd8b7aaaa5caf9478bd1f1acc483c1dfbd614
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010193"
---
# <a name="getting-the-status-of-a-restart-manager-operation"></a>Obtener el estado de una operación del Administrador de reinicio

Cuando muchas aplicaciones y servicios deben apagarse o reiniciarse, la operación restart Manager puede tardar un largo período de tiempo. El método siguiente se puede usar para obtener el estado de la operación actual.

**Para obtener el estado de la operación actual del Administrador de reinicio**

1.  El instalador debe implementar una función [**RM \_ WRITE STATUS \_ \_ CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) que determine el estado de las aplicaciones que se han apagado o reiniciado. La función puede proporcionar la información a la interfaz de usuario o al registro.
2.  El instalador pasa el puntero a la función [**RM \_ WRITE STATUS \_ \_ CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) al llamar a la [**función RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) [**o RmRestart.**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)

 

 