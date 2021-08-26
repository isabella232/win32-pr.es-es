---
title: Operaciones sincrónicas
description: Cuando RasDial se invoca como una operación sincrónica, la función no vuelve hasta que se ha establecido la conexión o se produce un error.
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c923a22758e7d6b9563cde9e4c9b2ce6036afa47f85116c0c18ed523996e49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025615"
---
# <a name="synchronous-operations"></a>Operaciones sincrónicas

Cuando [**RasDial se**](/windows/desktop/api/Ras/nf-ras-rasdiala) invoca como una operación sincrónica, la función no vuelve hasta que se ha establecido la conexión o se produce un error. El modo sincrónico proporciona una manera sencilla para que un cliente RAS establezca una conexión. El cliente simplemente puede llamar a **RasDial,** esperar a que la función devuelva y, a continuación, llamar a la [**función RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para determinar si la operación de conexión se ha realizado correctamente. Una vez establecida la conexión, la aplicación cliente puede finalizar sin interrumpir la conexión. Si se produce un error, la aplicación cliente debe [apagar la operación de conexión](disconnecting.md) antes de finalizar.

La desventaja del modo sincrónico es que el cliente no recibe notificaciones de progreso a medida que continúa la operación de conexión. Como solución alternativa para esta falta de notificaciones de progreso, un cliente en modo sincrónico puede usar un subproceso independiente que llame a [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para sondear y mostrar el estado actual. Sin embargo, para los clientes RAS que desean recibir información de progreso, la técnica preferida es invocar [**RasDial de forma**](/windows/desktop/api/Ras/nf-ras-rasdiala) asincrónica.

 

 




