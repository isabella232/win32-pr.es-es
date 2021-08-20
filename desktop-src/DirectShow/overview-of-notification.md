---
description: Información general de la notificación de eventos
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: Información general de la notificación de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ca5e6ffb4737054f773fc5be35d56939e711442a3b31761cd23c144ed00ac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148538"
---
# <a name="overview-of-event-notification"></a>Información general de la notificación de eventos

Un filtro notifica a Filter Graph Manager un evento mediante la publicación de una notificación de eventos. El evento podría ser algo esperado, como el final de una secuencia, o podría representar un error, como un error al representar una secuencia. Filter Graph Manager controla algunos eventos de filtro por sí mismo y deja otros para que la aplicación los controle. Si filter Graph Manager no controla un evento de filtro, coloca la notificación de eventos en una cola. El gráfico de filtros también puede poner en cola sus propias notificaciones de eventos para la aplicación.

Una aplicación recupera eventos de la cola y responde a ellos en función del tipo de evento. La notificación de eventos DirectShow por lo tanto es similar al esquema de cola Windows mensajes de Microsoft. Una aplicación también puede cancelar el comportamiento predeterminado de Filter Graph Manager para un tipo de evento determinado. A continuación, Graph administrador de filtros coloca esos eventos directamente en la cola para que la aplicación los controle.

Este mecanismo habilita

-   Filter Graph Manager para comunicarse con la aplicación.
-   Filtros para comunicarse con la aplicación y el Administrador de Graph Filtros.
-   Aplicación para determinar su grado de participación en el control de eventos.

 

 



