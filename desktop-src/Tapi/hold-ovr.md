---
description: La operación de retención permite que una sola dirección controle varias sesiones de comunicaciones.
ms.assetid: 65e22e4e-e346-41c2-929a-ba0d1f7f1732
title: Suspensión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afacd6d9664e9a095a1e8b0c725dc0171da709fdecffb88b428231a5b5359a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003643"
---
# <a name="hold"></a>Suspensión

La operación de retención permite que una sola dirección controle varias sesiones de comunicaciones. La colocación de una sesión en una retención permanente libera la línea o dirección del usuario para realizar otras llamadas. Normalmente, una llamada en espera dura no se puede transferir ni incluir en una llamada de conferencia, pero una llamada de consulta puede. Las llamadas de consulta se inician mediante [operaciones de conferencia](conference-ovr.md) o [transferencia.](transfer-ovr.md)

Una vez que una llamada se ha colocado correctamente en espera, el estado de la llamada normalmente pasa al estado de retención. Mientras una llamada está en espera, la aplicación puede recibir mensajes sobre los cambios de estado de la llamada retenido. Por ejemplo, si la entidad retenida se mantiene, el estado de la llamada puede pasar a desconectado.

En una situación de puente, es posible que la operación de retención no coloque realmente la llamada en espera. El estado de otras estaciones en la llamada puede regir (por ejemplo, no es posible intentar "mantener" una llamada cuando otras estaciones participan); en su lugar, la llamada simplemente se puede cambiar al estado inactivo mientras permanece conectada en otras estaciones.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2.x:** Vea [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).

**TAPI 3.x:** Vea [**ITBasicCallControl::Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).

 

 
