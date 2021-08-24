---
title: Enumerar entidades registradas
description: Una vez registrado un cliente, el cliente puede obtener una lista de todos los demás clientes que se han registrado con el administrador de tablas de enrutamiento. Algunos clientes deben realizar determinadas operaciones si se detecta la presencia de un tipo determinado de cliente.
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1d67a810806c1bc29f8f18c4cdea9f3a36e5b5a95922e8f66a943a99923ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674165"
---
# <a name="enumerating-registered-entities"></a>Enumerar entidades registradas

Una vez registrado un cliente, el cliente puede obtener una lista de todos los demás clientes que se han registrado con el administrador de tablas de enrutamiento. Algunos clientes deben realizar determinadas operaciones si se detecta la presencia de un tipo determinado de cliente.

El cliente puede llamar a [**la función RtmGetRegisteredEntities.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) Se devuelve un búfer [**de estructuras ENTITY INFO \_ \_ de RTM.**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) Después de que el cliente haya procesado esta información, el cliente debe llamar a [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) para liberar los identificadores de las estructuras **DE INFORMACIÓN DE ENTIDAD \_ \_ DE RTM.**

Si el cliente del administrador de tablas de enrutamiento proporcionó una función de devolución de llamada en la llamada a [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), se notificará al cliente cuando otros clientes se registren o anulen el registro.

Para obtener código de ejemplo que muestra cómo usar estas funciones, vea [Enumerar](enumerate-the-registered-entities.md) las entidades registradas y [Usar la devolución](use-the-event-notification-callback.md)de llamada de notificación de eventos .

 

 




