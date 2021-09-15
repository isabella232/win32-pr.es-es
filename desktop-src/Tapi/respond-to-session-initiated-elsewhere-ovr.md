---
description: Cuando llegue una nueva sesión de comunicaciones, se enviará una notificación de eventos a las aplicaciones TAPI que registraron un interés en la dirección y el tipo de medio.
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: Responder a la sesión iniciada en otro lugar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e25651b58f8841ac4de9bf14f4d139161c1359
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474688"
---
# <a name="respond-to-session-initiated-elsewhere"></a>Responder a la sesión iniciada en otro lugar

Cuando llegue una nueva sesión de comunicaciones, se [](address-ovr.md) enviará [](media-type-ovr.md) una notificación de eventos a las aplicaciones TAPI que registraron un interés en la dirección y el tipo de [medio.](event-notification.md) Solo se ofrecerán [privilegios](privilege-ovr.md) de propiedad a una aplicación durante la sesión. Esta aplicación no puede rechazar la sesión.

Se ofrece el estado de llamada inicial de una sesión entrante. Mientras la llamada se encuentra en el estado de oferta, una aplicación puede obtener información como el modo de portador y el motivo de la llamada, si los proveedores de servicios proporcionaron esta información y está disponible. Es posible que alguna información de llamada no esté disponible inmediatamente, como el identificador de autor de la llamada.

Hay seis respuestas básicas a una sesión [](handoffs-ovr.md)ofrecida: [respuesta,](answer-ovr.md)aceptación, entrega, [colocación,](drop-ovr.md) [](forward-ovr.md)reenvío y [redireccionamiento.](redirect-ovr.md) [](accept-ovr.md) Dependiendo del proveedor de servicios, es posible que el conjunto completo de estas operaciones no esté disponible.

 

 



