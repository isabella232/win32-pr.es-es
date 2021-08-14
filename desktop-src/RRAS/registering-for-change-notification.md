---
title: Registro para la notificación de cambio
description: Un cliente puede registrarse para recibir una notificación de los cambios en la información de enrutamiento que se almacena en el administrador de tablas de enrutamiento. Esta solicitud solo se puede realizar después de que un cliente se haya registrado con el administrador de tablas de enrutamiento.
ms.assetid: 90dc98eb-0d0b-4450-848b-c7cedab75a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7049478a5be834b08b7bb17ad9ebfb0fdf70736837f27d53e7900bf7bfdc88dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788624"
---
# <a name="registering-for-change-notification"></a>Registro para la notificación de cambio

Un cliente puede registrarse para recibir una notificación de los cambios en la información de enrutamiento que se almacena en el administrador de tablas de enrutamiento. Esta solicitud solo se puede realizar después de que un cliente se haya registrado con el administrador de tablas de enrutamiento.

Para registrarse para la notificación de cambios, un cliente debe llamar a [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), especificando los tipos de cambios para los que el cliente debe recibir la notificación. Si se debe notificar al cliente el cambio en destinos específicos, el cliente llama a [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) una vez para cada destino.

El cliente puede dejar de recibir notificaciones de cambio llamando [**a RtmDeregisterFromChangeNotification.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification)

Para obtener código de ejemplo que muestra cómo usar estas funciones, vea [Register For Change Notification](register-for-change-notification.md).

 

 




