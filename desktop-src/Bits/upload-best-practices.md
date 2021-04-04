---
title: Procedimientos recomendados de carga
description: Highloads puede provocar varias condiciones de tiempo de espera del servidor, lo que a su vez puede aumentar la carga cuando el cliente vuelve a intentarlo.
ms.assetid: 8210f849-2aae-497b-b5dd-af25f6f4b8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95a229ff1e229c41fde8fd377e347f91cf43010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075169"
---
# <a name="upload-best-practices"></a>Procedimientos recomendados de carga

Highloads puede provocar varias condiciones de tiempo de espera del servidor, lo que a su vez puede aumentar la carga cuando el cliente vuelve a intentarlo. Además, un gran número de conexiones pendientes consumirá más recursos del servidor y empeorará la situación. Además, si la aplicación de back-end no se escribe para controlar las condiciones de carga elevada, puede bloquearse o provocar un comportamiento incorrecto. La aplicación debe realizar los pasos siguientes para limitar la carga en el back-end.

Si no se escribe la aplicación de servidor para administrar grandes volúmenes, pueden producirse condiciones de tiempo de espera, lo que a su vez puede aumentar la carga cuando el cliente vuelve a intentarlo. Además, un gran número de conexiones pendientes consumirá más recursos del servidor.

Al probar la aplicación de servidor, pruebe con la carga más alta posible. Debe usar varios equipos cliente, cada uno con varios trabajos de BITS simultáneos y de primer plano, y medir el rendimiento máximo en el back-end. Si no puede medir el rendimiento, tendrá que calcular el rendimiento.

La aplicación de servidor debe residir en una dirección URL diferente de la dirección URL de carga (vea la propiedad de IIS de BITS, **BITSServerNotificationURL**).

Se recomienda limitar la carga en el servidor de aplicaciones en función de los valores de rendimiento probados. Debe utilizar las propiedades de IIS, **MaxBandwidth** y **MaxConnections**, para limitar la carga en el servidor de aplicaciones.

 

 




