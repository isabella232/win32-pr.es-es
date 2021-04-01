---
title: Enumerar entidades registradas
description: Una vez registrado un cliente, el cliente puede obtener una lista de todos los demás clientes registrados con el administrador de tablas de enrutamiento. Algunos clientes deben realizar ciertas operaciones si se detecta la presencia de un tipo de cliente determinado.
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac92ccf89336d3fbca378209b9e79877d9b426a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075773"
---
# <a name="enumerating-registered-entities"></a>Enumerar entidades registradas

Una vez registrado un cliente, el cliente puede obtener una lista de todos los demás clientes registrados con el administrador de tablas de enrutamiento. Algunos clientes deben realizar ciertas operaciones si se detecta la presencia de un tipo de cliente determinado.

El cliente puede llamar a la función [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) . Se devuelve un búfer de estructuras de [**\_ \_ información de entidad RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) . Después de que el cliente haya procesado esta información, el cliente debe llamar a [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) para liberar los identificadores de las estructuras de información de la **\_ entidad \_ RTM** .

Si el cliente del administrador de tablas de enrutamiento proporcionó una función de devolución de llamada en la llamada a [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), el cliente recibe una notificación cuando otros clientes registran o anulan el registro.

Para ver el código de ejemplo que muestra cómo usar estas funciones, consulte [enumerar las entidades registradas](enumerate-the-registered-entities.md) y [usar la devolución de llamada de notificación de eventos](use-the-event-notification-callback.md).

 

 




