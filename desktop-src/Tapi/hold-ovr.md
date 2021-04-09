---
description: La operación Hold permite que una sola dirección controle varias sesiones de comunicación.
ms.assetid: 65e22e4e-e346-41c2-929a-ba0d1f7f1732
title: Contener
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df54b246c5bde5914a14b53dd56b71688d92a5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908281"
---
# <a name="hold"></a>Contener

La operación Hold permite que una sola dirección controle varias sesiones de comunicación. La colocación de una sesión en un disco duro de retención libera la línea o la dirección del usuario para realizar otras llamadas. Normalmente, una llamada en retención no se puede transferir ni incluir en una llamada de conferencia, pero sí una llamada de consulta. Las llamadas de consulta se inician mediante operaciones de [Conferencia](conference-ovr.md) o [transferencia](transfer-ovr.md) .

Una vez que se ha colocado correctamente una llamada en espera, el estado de la llamada normalmente realiza la transición al estado de suspensión. Mientras una llamada está en espera, la aplicación puede recibir mensajes sobre los cambios de estado de la llamada retenida. Por ejemplo, si la parte que contiene se cuelga, el estado de la llamada puede pasar a desconectado.

En una situación de puente, es posible que la operación de retención no coloque realmente la llamada en espera. El estado de otras estaciones de la llamada puede regir (por ejemplo, si se intenta "mantener" una llamada cuando no se pueden participar otras estaciones). en su lugar, la llamada solo se puede cambiar al estado inactivo mientras permanezca conectado en otras estaciones.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2. x:** Vea [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).

**TAPI 3. x:** Vea [**ITBasicCallControl:: Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).

 

 
