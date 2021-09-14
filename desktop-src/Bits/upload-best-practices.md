---
title: Upload Procedimientos recomendados
description: Las cargas elevadas pueden provocar varias condiciones de tiempo de espera del servidor, lo que a su vez puede aumentar la carga cuando el cliente vuelve a inactividad.
ms.assetid: 8210f849-2aae-497b-b5dd-af25f6f4b8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95a229ff1e229c41fde8fd377e347f91cf43010
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063408"
---
# <a name="upload-best-practices"></a>Upload Procedimientos recomendados

Las cargas elevadas pueden provocar varias condiciones de tiempo de espera del servidor, lo que a su vez puede aumentar la carga cuando el cliente vuelve a inactividad. Además, un gran número de conexiones pendientes consumirá más recursos de servidor y hará que la situación empeore. Además, si la aplicación de back-end no está escrita para controlar condiciones de carga alta, puede bloquearse o comportarse mal. La aplicación realizará los pasos siguientes para limitar la carga en el back-end.

Si la aplicación de servidor no se escribe para controlar grandes volúmenes, pueden producirse condiciones de tiempo de espera, que a su vez pueden aumentar la carga cuando el cliente vuelve a inactividad. Además, un gran número de conexiones pendientes consumirá más recursos de servidor.

Al probar la aplicación de servidor, pruebe con la carga más alta posible. Debe usar varias máquinas cliente, cada una con varios trabajos de BITS en primer plano simultáneos y medir el rendimiento máximo en el back-end. Si no puede medir el rendimiento, tendrá que calcular el rendimiento.

La aplicación de servidor debe residir en una dirección URL diferente de la dirección URL de carga (vea la propiedad **BITSServerNotificationURL de** BITS IIS).

Es un procedimiento recomendado limitar la carga en el servidor de aplicaciones en función de los valores de rendimiento probados. Debe usar las propiedades de IIS, **MaxBandwidth** y **MaxConnections**, para limitar la carga en el servidor de aplicaciones.

 

 




