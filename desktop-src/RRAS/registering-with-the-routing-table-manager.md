---
title: Registro con el administrador de tablas de enrutamiento
description: Para que un cliente pueda acceder a la tabla de enrutamiento, primero debe registrarse con el administrador de tablas de enrutamiento mediante la función RtmRegisterEntity.
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- Administrador de tablas de enrutamiento versión 2 RRAS, registrar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ce5a1b350ec5420b3fc32a4e5a68a213a61151
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268701"
---
# <a name="registering-with-the-routing-table-manager"></a>Registro con el administrador de tablas de enrutamiento

Para que un cliente pueda acceder a la tabla de enrutamiento, primero debe registrarse con el administrador de tablas de enrutamiento mediante la función [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) .

Cuando un cliente se registra, pasa a la estructura de información de la [**\_ \_ entidad RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) del administrador de tablas de enrutamiento. Esta estructura contiene la información que identifica de forma única un cliente, la familia de direcciones y la instancia del administrador de tabla de enrutamiento con la que el cliente se registra. Un cliente también puede establecer la devolución de llamada de [**\_ devolución de \_ llamada de evento de RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) . El administrador de tablas de enrutamiento usará esta devolución de llamada para notificar al cliente los eventos, como las notificaciones de cambio y los registros de cliente.

El administrador de tablas de enrutamiento completa su procesamiento de registro y devuelve un identificador al cliente. El cliente debe utilizar este identificador para todas las llamadas subsiguientes a las funciones de RTMv2.

La función [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) que se usa en RTMv2 es análoga a la función [**RtmRegisterClient**](rtmregisterclient.md) que se usa en RTMv1. La función **RtmRegisterClient** está obsoleta, excepto los clientes que usan IPX.

Una vez que un cliente ha terminado de interactuar con el administrador de tablas de enrutamiento, debe llamar a [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity). El administrador de tablas de enrutamiento destruye el identificador asociado con el cliente. Para evitar pérdidas de memoria, el cliente debe asegurarse de que libera todos los identificadores y elimina todas las rutas y los próximos saltos que posee antes de llamar a **RtmDeregisterEntity**.

Para ver el código de ejemplo que muestra cómo usar estas funciones, consulte [registrar con el administrador de tablas de enrutamiento](register-with-the-routing-table-manager.md) y [usar la devolución de llamada de notificación de eventos](use-the-event-notification-callback.md).

 

 




