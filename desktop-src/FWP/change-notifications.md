---
title: Notificaciones de cambio
description: Las notificaciones de cambio del motor de filtrado base (BFE) siguen el patrón de publicación y suscripción.
ms.assetid: 443f1767-5694-4584-ba0f-229275900774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0038dc851cb15414dbc0180f205104725bf069b599632a93ae6e257fe7a1f84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078505"
---
# <a name="change-notifications"></a>Notificaciones de cambio

Las notificaciones de cambio del motor de filtrado base (BFE) siguen el patrón de publicación y suscripción: para recibir una de las notificaciones de cambios publicadas, una aplicación tiene que suscribirse a ella.

Las notificaciones de cambio de BFE publicadas son Agregar y quitar para [**llamadas,**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0) [**filtros,**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0) [**proveedores,**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0) [**contextos**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)de proveedor y [**sub capas.**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0)

Para suscribirse a una de las notificaciones anteriores, una aplicación llama a la función de administración [**\* Fwpm SubscribeChanges0**](fwp-mgmt-functions.md) correspondiente (por ejemplo, [**FwpmCalloutSubscribeChanges0).**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0) BFE invoca la función de devolución de llamada pasada como argumento a **Fwpm \* SubscribeChanges0** cuando se produce el cambio al que se suscribió.

Para cancelar la suscripción a una de las notificaciones anteriores, una aplicación llama a la función de administración **\* Fwpm UnsubscribeChanges0** correspondiente (por ejemplo, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).

Para ver las suscripciones actuales de una de las notificaciones anteriores, una aplicación llama a la función de administración [**Fwpm \* SubscriptionsGet0**](fwp-mgmt-functions.md) correspondiente (por [**ejemplo, FwpmCalloutSubscriptionsGet0).**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)

Las notificaciones de cambio que ofrece el BFE son:

-   Asincrónico: la llamada de función que desencadenó una notificación puede devolverse antes de que la notificación se haya enviado a todos los suscriptores.
-   No confiable: no se garantiza que las notificaciones se entreguen correctamente.

Los suscriptores no reciben notificaciones de los cambios realizados con el identificador de sesión que usaron para suscribirse. Por lo general, los suscriptores solo necesitan ser informados de los cambios realizados por otros usuarios. ya saben qué cambios se realizaron por sí mismos.

 

 




