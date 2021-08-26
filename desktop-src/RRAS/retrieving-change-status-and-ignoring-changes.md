---
title: Recuperar el estado del cambio e ignorar los cambios
description: El cliente puede consultar el administrador de tablas de enrutamiento para averiguar si hay una notificación de un cambio en un destino pendiente llamando a RtmGetChangeStatus. Esta función devuelve TRUE hasta que el autor de la llamada recupera este cambio mediante una llamada a RtmGetChangedDests.
ms.assetid: 778279ac-00c5-4de0-9ac7-eca1ac7fec6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a117130ac939788a74aaa32092000e8f6f29aa6b34e697ca6066c9e13259b8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028065"
---
# <a name="retrieving-change-status-and-ignoring-changes"></a>Recuperar el estado del cambio e ignorar los cambios

El cliente puede consultar el administrador de tablas de enrutamiento para averiguar si hay una notificación de un cambio en un destino pendiente llamando a [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus). Esta función devuelve **TRUE hasta** que el autor de la llamada recupera este cambio mediante una llamada [**a RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).

Un cliente puede usar esta consulta para evitar realizar una acción que tendría que deshacerse después de recibir y procesar la notificación de cambio. El uso de esta característica permite al cliente trabajar de forma eficaz aplazando ciertas operaciones a un momento posterior.

El cliente también puede omitir una notificación de cambio pendiente para un destino llamando a [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests). Una llamada posterior a [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) no devuelve este destino a menos que se produzca otro cambio después de la llamada a [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).

 

 




