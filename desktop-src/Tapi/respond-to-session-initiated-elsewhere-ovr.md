---
description: Cuando llega una nueva sesión de comunicaciones, las aplicaciones TAPI que registraron interés en la dirección y el tipo de medio se enviarán a una notificación de eventos.
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: Responder a la sesión iniciada en otro lugar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e25651b58f8841ac4de9bf14f4d139161c1359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678561"
---
# <a name="respond-to-session-initiated-elsewhere"></a>Responder a la sesión iniciada en otro lugar

Cuando llega una nueva sesión de comunicaciones, las aplicaciones TAPI que registraron interés en la [Dirección](address-ovr.md) y el [tipo de medio](media-type-ovr.md) se enviarán a una [notificación de eventos](event-notification.md). Solo se ofrecerá a una aplicación [privilegios](privilege-ovr.md) de propiedad a través de la sesión. Esta aplicación no puede rechazar la sesión.

El estado de la llamada inicial de una sesión entrante es ofrecer. Mientras la llamada está en el estado de la oferta, una aplicación puede obtener información como el modo de portador y el motivo de la llamada, si los proveedores de servicios proporcionan esta información y está disponible. Es posible que parte de la información de llamada no esté disponible de inmediato, como el identificador del autor de la llamada.

Hay seis respuestas básicas a una sesión ofrecida: [responder](answer-ovr.md), [Aceptar](accept-ovr.md), [entregar](handoffs-ovr.md), [quitar](drop-ovr.md), [reenviar](forward-ovr.md)y [redirigir](redirect-ovr.md). Dependiendo del proveedor de servicios, es posible que el conjunto completo de estas operaciones no esté disponible.

 

 



