---
title: Registro con el Administrador de tablas de enrutamiento
description: Para que un cliente pueda acceder a la tabla de enrutamiento, primero debe registrarse con el administrador de tablas de enrutamiento mediante la función RtmRegisterEntity.
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- RRAS de Routing Table Manager versión 2, registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 088072fac8679d9b2f87729b67a826ac850e77109f18b28fef3c2dc33c433f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028295"
---
# <a name="registering-with-the-routing-table-manager"></a>Registro con el Administrador de tablas de enrutamiento

Para que un cliente pueda acceder a la tabla de enrutamiento, primero debe registrarse con el administrador de tablas de enrutamiento mediante la [**función RtmRegisterEntity.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)

Cuando un cliente se registra, pasa al administrador de tablas de enrutamiento una estructura [**RTM \_ ENTITY \_ INFO.**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) Esta estructura contiene la información que identifica de forma única un cliente, la familia de direcciones y la instancia del administrador de tablas de enrutamiento con el que se registra el cliente. Un cliente también puede establecer la devolución de llamada [**\_ RTM EVENT \_ CALLBACK.**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) El administrador de tablas de enrutamiento usará esta devolución de llamada para notificar al cliente eventos como notificaciones de cambios y registros de cliente.

El administrador de tablas de enrutamiento completa su procesamiento de registro y devuelve un identificador al cliente. El cliente debe usar este identificador para todas las llamadas posteriores a funciones RTMv2.

La [**función RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) que se usa en RTMv2 es análoga a la función [**RtmRegisterClient**](rtmregisterclient.md) que se usa en RTMv1. La **función RtmRegisterClient** está obsoleta, excepto para los clientes que usan IPX.

Una vez que un cliente ha terminado de interactuar con el administrador de tablas de enrutamiento, debe llamar a [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity). El administrador de tabla de enrutamiento destruye el identificador asociado al cliente. Para evitar pérdidas de memoria, el cliente debe asegurarse de que libera todos los identificadores y elimina todas las rutas y próximo saltos que posee antes de llamar a **RtmDeregisterEntity**.

Para obtener código de ejemplo que muestra cómo usar estas funciones, vea Registrar con el Administrador de tablas [de](register-with-the-routing-table-manager.md) enrutamiento y [Usar la devolución de](use-the-event-notification-callback.md)llamada de notificación de eventos .

 

 




