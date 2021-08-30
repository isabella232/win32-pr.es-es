---
title: Upload Procedimientos recomendados
description: Las cargas elevadas pueden provocar varias condiciones de tiempo de espera del servidor, lo que a su vez puede aumentar la carga cuando el cliente vuelve a inactividad.
ms.assetid: 8210f849-2aae-497b-b5dd-af25f6f4b8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2ad85fd7552ed42068ecd02830321fedcec4d147ba9beb8b766dda2e76ab49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004675"
---
# <a name="upload-best-practices"></a>Upload Procedimientos recomendados

Las cargas elevadas pueden provocar varias condiciones de tiempo de espera del servidor, lo que a su vez puede aumentar la carga cuando el cliente vuelve a inactividad. Además, un gran número de conexiones pendientes consumirá más recursos de servidor y hará que la situación empeore. Además, si la aplicación back-end no está escrita para controlar condiciones de carga alta, puede bloquearse o comportarse mal. La aplicación realizará los pasos siguientes para limitar la carga en el back-end.

Si la aplicación de servidor no está escrita para controlar grandes volúmenes, pueden producirse condiciones de tiempo de espera, lo que a su vez puede aumentar la carga cuando el cliente vuelve a inactividad. Además, un gran número de conexiones pendientes consumirá más recursos de servidor.

Al probar la aplicación de servidor, pruebe con la carga más alta posible. Debe usar varias máquinas cliente, cada una con varios trabajos de BITS simultáneos en primer plano, y medir el rendimiento máximo en el back-end. Si no puede medir el rendimiento, tendrá que calcularlo.

La aplicación de servidor debe residir en una dirección URL diferente de la dirección URL de carga (vea la propiedad IIS bits, **BITSServerNotificationURL).**

Es una buena práctica limitar la carga en el servidor de aplicaciones en función de los valores de rendimiento probados. Debe usar las propiedades de IIS, **MaxBandwidth** y **MaxConnections**, para limitar la carga en el servidor de aplicaciones.

 

 




