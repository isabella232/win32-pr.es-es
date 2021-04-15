---
title: Cambios en la mejor ruta a una red
description: Un cambio en cualquiera de los siguientes valores para la mejor ruta a una red de destino determinada hace que el administrador de tablas de enrutamiento genere un mensaje de notificación enviado a cada cliente registrado y a los reenviadores
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8c43483dbd69f5407f9859d5943e515e8825d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676219"
---
# <a name="changes-to-the-best-route-to-a-network"></a>Cambios en la mejor ruta a una red

**Windows Server 2003:** Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las nuevas aplicaciones deben usar la API del administrador de tablas de enrutamiento versión 2.

Un cambio en cualquiera de los siguientes valores para la mejor ruta a una red de destino determinada hace que el administrador de tablas de enrutamiento genere un mensaje de notificación enviado a cada cliente registrado y a los reenviadores:

-   Identificador de protocolo
-   Índice de interfaz
-   Dirección del enrutador de próximo salto
-   Datos específicos de la familia de protocolos que incluyen métricas de ruta

Un cambio en el identificador de protocolo, el índice de interfaz o la dirección del enrutador de próximo salto se produce cuando se agrega una nueva entrada de ruta mejor, o cuando se elimina o se agota la entrada de la mejor ruta actual, y deja otra ruta como la nueva ruta mejor.

 

 




