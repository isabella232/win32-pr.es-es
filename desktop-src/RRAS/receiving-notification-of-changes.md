---
title: Recibir notificación de cambios
description: Muchos clientes pueden actualizar simultáneamente la tabla de enrutamiento y los clientes deben recibir una notificación cuando se produzcan cambios en la información de enrutamiento.
ms.assetid: d42e16e2-32b2-4178-967b-e937730b3cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6eddc92404acb921b31bab22736561cbbc83e4c1c641da80a8ff95352e52f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788715"
---
# <a name="receiving-notification-of-changes"></a>Recibir notificación de cambios

Muchos clientes pueden actualizar simultáneamente la tabla de enrutamiento y los clientes deben recibir una notificación cuando se produzcan cambios en la información de enrutamiento. Por ejemplo, un cliente que no sea notificado de los cambios de otro cliente en la tabla de enrutamiento podría anunciar información de ruta obsoleta. Esto se puede evitar programando que los clientes se registren con el administrador de tablas de enrutamiento para recibir una notificación de los cambios en la tabla de enrutamiento. El administrador de tablas de enrutamiento envía notificaciones de cambios a todos los clientes que se registran para recibirlos.

La notificación de cambio solo se aplica a los destinos. No hay ninguna manera de consultar al administrador de tablas de enrutamiento para ver si hay cambios en una ruta determinada.

Cuando se realiza un cambio en una de las rutas a un destino, el administrador de tablas de enrutamiento envía una notificación de que se ha producido un cambio. Esta notificación solo se envía a los clientes que se han registrado con el administrador de tablas de enrutamiento para el tipo de cambio que se ha producido. Todos los cambios en la información de enrutamiento en el administrador de tablas de enrutamiento se producen en una o varias vistas, y los mensajes de notificación de cambios se pueden solicitar en cualquier subconjunto de vistas admitidas.

Actualmente hay tres tipos de notificaciones de cambio para las que un cliente puede registrarse:

-   Notificación de cualquier cambio en las rutas del destino. Esta solicitud se realiza mediante la marca \_ RTM CHANGE \_ TYPE \_ ALL.
-   Notificación si cambia la mejor ruta al destino o cualquiera de las siguientes información para la mejor ruta actual:

    -   Referencia
    -   Próximo salto
    -   Marcas de ruta

    Esta solicitud se realiza mediante la marca \_ RTM CHANGE \_ TYPE \_ BEST.

-   Notificación de todos los cambios del tipo RTM CHANGE TYPE BEST, excepto los cambios en las marcas de no reenvío \_ \_ en la mejor \_ ruta. Por ejemplo, el administrador de enrutadores espera cambios de este tipo en la vista de unidifusión y actualiza la información en el reenviador de unidifusión. Esta solicitud se realiza mediante la marca \_ RTM CHANGE \_ TYPE \_ FORWARDING.

Las solicitudes de notificaciones de cambios también se pueden restringir a un subconjunto de destinos mediante el registro de notificaciones de cambios solo en destinos "marcados". El cliente puede marcar un destino para la notificación de cambios llamando a [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification).

Cuando se produce un cambio, el administrador de tablas de enrutamiento comprueba si hay clientes a los que se debe notificar este cambio. Un cliente debe recibir una notificación de un cambio si se cumplen todas las condiciones siguientes:

-   El tipo de cambio que se ha producido es un tipo para el que el cliente se ha registrado para la notificación.
-   Se han producido cambios en un destino marcado por el cliente o en cualquier destino, si el cliente ha solicitado cambios para todos los destinos.
-   El cliente solicitó la notificación de cambio para la vista en la que se produjo este cambio.

Si el cambio cumple todos los criterios anteriores, el cambio se almacena en caché y se notifica al cliente.

La notificación no especifica cuáles son los cambios reales, solo que se han producido. El cliente debe recuperar los cambios llamando a [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) mediante el identificador de notificación obtenido de una llamada anterior a [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification).

 

 




