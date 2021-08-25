---
title: Cambios en la mejor ruta a una red
description: Un cambio en cualquiera de los siguientes valores para la mejor ruta a una red de destino determinada hace que el administrador de tablas de enrutamiento genere un mensaje de notificación enviado a cada cliente registrado y a los reenviadores.
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fe96a0b339325c2290c346ba581d5b892db24d1cd972f7a83a0b2ec525eeb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030365"
---
# <a name="changes-to-the-best-route-to-a-network"></a>Cambios en la mejor ruta a una red

**Windows Server 2003:** Esta API ha sido reemplazada por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las nuevas aplicaciones deben usar la API de Routing Table Manager versión 2.

Un cambio en cualquiera de los siguientes valores para la mejor ruta a una red de destino determinada hace que el administrador de tablas de enrutamiento genere un mensaje de notificación enviado a cada cliente registrado y a los reenviadores:

-   Identificador de protocolo
-   Índice de interfaz
-   Dirección del enrutador de próximo salto
-   Datos específicos de la familia de protocolos que incluyen métricas de ruta

Se produce un cambio en el identificador de protocolo, el índice de interfaz o la dirección del enrutador de próximo salto cuando se agrega una nueva entrada de mejor ruta o cuando se elimina o se añe la entrada de mejor ruta actual, y deja otra ruta como la mejor nueva.

 

 




