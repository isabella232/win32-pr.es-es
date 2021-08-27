---
description: Cuando llega una nueva sesión de comunicaciones, se enviará una notificación de eventos a las aplicaciones TAPI que registraron un interés en la dirección y el tipo de medio.
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: Responder a la sesión iniciada en otro lugar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c74554b48919f7532561bfdf0bab7a163a58fbeb3734dc15e4a8d7e0869dad2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072855"
---
# <a name="respond-to-session-initiated-elsewhere"></a>Responder a la sesión iniciada en otro lugar

Cuando llega una nueva sesión de comunicaciones, se [](address-ovr.md) enviará [](media-type-ovr.md) una notificación de eventos a las aplicaciones TAPI que registraron un interés en la dirección y el tipo de [medio.](event-notification.md) Solo se ofrecerán [privilegios](privilege-ovr.md) de propiedad a una aplicación durante la sesión. Esta aplicación no puede rechazar la sesión.

Se ofrece el estado de llamada inicial de una sesión entrante. Mientras la llamada está en estado de oferta, una aplicación puede obtener información como el modo de portador y la razón de la llamada, si los proveedores de servicios proporcionaron esta información y está disponible. Es posible que alguna información de llamada no esté disponible inmediatamente, como el identificador del autor de la llamada.

Hay seis respuestas básicas a una sesión ofrecida: [responder](answer-ovr.md) [,](accept-ovr.md)aceptar [,](handoffs-ovr.md) [entregar,](drop-ovr.md) [colocar,](forward-ovr.md)reenviar y [redirigir](redirect-ovr.md). Dependiendo del proveedor de servicios, es posible que el conjunto completo de estas operaciones no esté disponible.

 

 



