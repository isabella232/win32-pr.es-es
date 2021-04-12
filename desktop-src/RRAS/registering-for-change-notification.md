---
title: Registrando para la notificación de cambios
description: Un cliente puede registrarse para recibir notificaciones de cambios en la información de enrutamiento almacenada en el administrador de tablas de enrutamiento. Esta solicitud solo puede realizarse después de que un cliente se ha registrado con el administrador de tablas de enrutamiento.
ms.assetid: 90dc98eb-0d0b-4450-848b-c7cedab75a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3a98062fee73c481c1f47c32fa7eeb5465a112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357004"
---
# <a name="registering-for-change-notification"></a>Registrando para la notificación de cambios

Un cliente puede registrarse para recibir notificaciones de cambios en la información de enrutamiento almacenada en el administrador de tablas de enrutamiento. Esta solicitud solo puede realizarse después de que un cliente se ha registrado con el administrador de tablas de enrutamiento.

Para registrar la notificación de cambios, un cliente debe llamar a [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), especificando los tipos de cambios para los que el cliente debe recibir la notificación. Si se debe notificar al cliente el cambio a destinos específicos, el cliente llama a [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) una vez para cada destino.

El cliente puede dejar de recibir notificaciones de cambios mediante una llamada a [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification).

Para ver el código de ejemplo que muestra cómo usar estas funciones, consulte [registrar para la notificación de cambios](register-for-change-notification.md).

 

 




