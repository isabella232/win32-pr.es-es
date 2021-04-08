---
title: Notificaciones de cambios
description: Las notificaciones de cambio del motor de filtrado de base (BFE) siguen el patrón de publicación/suscripción.
ms.assetid: 443f1767-5694-4584-ba0f-229275900774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c7a3a2069525cc44823ed975fade3b5f100efd8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103994967"
---
# <a name="change-notifications"></a>Notificaciones de cambios

Las notificaciones de cambio del motor de filtrado de base (BFE) siguen el patrón de publicación/suscripción: para recibir una de las notificaciones de cambios publicadas, una aplicación tiene que suscribirse a ella.

Las notificaciones de cambios de BFE publicadas son agregar y quitar para [**llamadas**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**filtros**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**proveedores**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**contextos de proveedor**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)y [**subcapas**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).

Para suscribirse a una de las notificaciones anteriores, una aplicación llama a la función de administración de [**\* SubscribeChanges0 de Fwpm**](fwp-mgmt-functions.md) correspondiente (por ejemplo, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)). BFE llama a la función de devolución de llamada que se pasa como argumento a **Fwpm \* SubscribeChanges0** cuando se produce el cambio al que se ha suscrito.

Para cancelar la suscripción a una de las notificaciones anteriores, una aplicación llama a la función de administración de **\* UnsubscribeChanges0 de Fwpm** correspondiente (por ejemplo, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).

Para ver las suscripciones actuales de una de las notificaciones anteriores, una aplicación llama a la función de administración de [**\* SubscriptionsGet0 de Fwpm**](fwp-mgmt-functions.md) correspondiente (por ejemplo, [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).

Las notificaciones de cambio ofrecidas por BFE son:

-   Asincrónico: la llamada de función que desencadenó una notificación puede volver antes de que la notificación se envíe a todos los suscriptores.
-   No confiable: no se garantiza que las notificaciones se entreguen correctamente.

Los suscriptores no reciben notificaciones de los cambios realizados con el identificador de sesión que usaron para suscribirse. Por lo general, solo es necesario informar a los suscriptores de los cambios realizados por otros usuarios. ya saben qué cambios se realizaron por sí mismos.

 

 




