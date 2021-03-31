---
description: Información general de la notificación de eventos
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: Información general de la notificación de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60c3251a74606f07f25ab6870cfd1f333ecbbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806074"
---
# <a name="overview-of-event-notification"></a>Información general de la notificación de eventos

Un filtro notifica al administrador de gráficos de filtro sobre un evento mediante la publicación de una notificación de eventos. El evento podría ser algo esperado, como el final de una secuencia, o podría representar un error, como un error al representar un flujo. El administrador de gráficos de filtro controla algunos eventos de filtro por sí mismo y deja a otros para que la aplicación los controle. Si Filter Graph Manager no controla un evento Filter, coloca la notificación de eventos en una cola. El gráfico de filtros también puede poner en cola sus propias notificaciones de eventos para la aplicación.

Una aplicación recupera los eventos de la cola y los responde en función del tipo de evento. La notificación de eventos en DirectShow es, por lo tanto, similar al esquema de Message Queue Server de Microsoft Windows. Una aplicación también puede cancelar el comportamiento predeterminado del administrador de gráficos de filtro para un tipo de evento determinado. Después, el administrador de gráficos de filtro coloca esos eventos directamente en la cola para que la aplicación los controle.

Este mecanismo permite

-   El administrador de gráficos de filtro para comunicarse con la aplicación.
-   Filtros para comunicarse con la aplicación y el administrador de gráficos de filtro.
-   La aplicación para determinar su grado de implicación en el control de eventos.

 

 



