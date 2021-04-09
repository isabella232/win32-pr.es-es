---
title: Operaciones sincrónicas
description: Cuando se invoca RasDial como una operación sincrónica, la función no vuelve hasta que se ha establecido la conexión o se produce un error.
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2463e3112c3faac4d7601023ea73f0182e2d5b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076206"
---
# <a name="synchronous-operations"></a>Operaciones sincrónicas

Cuando se invoca [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) como una operación sincrónica, la función no vuelve hasta que se ha establecido la conexión o se produce un error. El modo sincrónico proporciona una manera sencilla para que un cliente RAS establezca una conexión. El cliente puede llamar simplemente a **rasdial**, esperar a que se devuelva la función y, a continuación, llamar a la función [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para determinar si la operación de conexión se realizó correctamente. Una vez establecida la conexión, la aplicación cliente puede finalizar sin interrumpir la conexión. Si se produce un error, la aplicación cliente debe [cerrar la operación de conexión antes de](disconnecting.md) finalizar.

El inconveniente del modo sincrónico es que el cliente no recibe notificaciones de progreso a medida que la operación de conexión continúa. Como solución alternativa para esta falta de notificaciones de progreso, un cliente en modo sincrónico puede usar un subproceso independiente que llama a [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para sondear y mostrar el estado actual. Sin embargo, para los clientes RAS que desean recibir información de progreso, la técnica preferida es invocar [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) de forma asincrónica.

 

 




