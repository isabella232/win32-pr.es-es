---
title: Recibir notificación de cambios
description: Muchos clientes pueden actualizar la tabla de enrutamiento simultáneamente y los clientes deben recibir una notificación cuando se produzcan cambios en la información de enrutamiento.
ms.assetid: d42e16e2-32b2-4178-967b-e937730b3cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacd8d1d0329cf29be82a890be30b602b9330249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418588"
---
# <a name="receiving-notification-of-changes"></a>Recibir notificación de cambios

Muchos clientes pueden actualizar la tabla de enrutamiento simultáneamente y los clientes deben recibir una notificación cuando se produzcan cambios en la información de enrutamiento. Por ejemplo, un cliente que no reciba notificaciones de los cambios de otro cliente en la tabla de enrutamiento podría anunciar información de ruta obsoleta. Esto puede evitarse mediante la programación de los clientes para que se registren en el administrador de tablas de enrutamiento para recibir notificaciones de los cambios en la tabla de enrutamiento. El administrador de tablas de enrutamiento envía notificaciones de cambios a todos los clientes que se registran para recibirlos.

La notificación de cambios solo se aplica a los destinos. No hay ninguna manera de consultar los cambios en una ruta determinada en el administrador de tablas de enrutamiento.

Cuando se realiza un cambio en una de las rutas a un destino, el administrador de tablas de enrutamiento envía una notificación de que se ha producido un cambio. Esta notificación solo se dirige a los clientes que se han registrado con el administrador de tabla de enrutamiento para el tipo de cambio que se ha producido. Todos los cambios en la información de enrutamiento del administrador de tablas de enrutamiento se producen en una o más vistas, y los mensajes de notificación de cambios se pueden solicitar en cualquier subconjunto de vistas admitidas.

Actualmente hay tres tipos de notificaciones de cambio para los que un cliente puede registrarse:

-   Notificación de cualquier cambio en las rutas del destino. Esta solicitud se realiza mediante la marca de tipo de cambio de RTM \_ \_ \_ todos.
-   Notificación si el mejor enrutamiento al destino cambia o cualquiera de los siguientes datos de la mejor ruta actual:

    -   Referencia
    -   Próximos saltos
    -   Marcas de ruta

    Esta solicitud se realiza con el \_ mejor indicador de tipo de cambio de RTM \_ \_ .

-   Notificación de todos los cambios del tipo de cambio de RTM de tipo \_ \_ \_ más adecuado, excepto los cambios en las marcas de no reenvío en la mejor ruta. Por ejemplo, el administrador de enrutadores espera los cambios de este tipo en la vista de unidifusión y actualiza la información en el reenviador de unidifusión. Esta solicitud se realiza mediante la \_ marca de \_ reenvío de tipo de cambio RTM \_ .

Las solicitudes de notificaciones de cambios también se pueden restringir a un subconjunto de destinos mediante el registro de notificaciones de cambios únicamente en los destinos "marcados". El cliente puede marcar un destino para la notificación de cambios mediante una llamada a [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification).

Cuando se produce un cambio, el administrador de tablas de enrutamiento comprueba para ver si hay clientes a los que se debe notificar este cambio. Se debe notificar a un cliente de un cambio si se cumplen todas las condiciones siguientes:

-   El tipo de cambio que se ha producido es un tipo para el que el cliente se ha registrado para la notificación
-   Se han producido cambios en un destino marcado por el cliente o en cualquier destino si el cliente ha solicitado cambios para todos los destinos.
-   La notificación de cambio solicitada por el cliente para la vista en la que se produjo este cambio

Si el cambio cumple todos los criterios anteriores, el cambio se almacena en caché y se notifica al cliente.

La notificación no especifica cuáles son los cambios reales, solo que se han producido. El cliente debe recuperar los cambios mediante una llamada a [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) con el identificador de notificación que se obtuvo de una llamada anterior a [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification).

 

 




