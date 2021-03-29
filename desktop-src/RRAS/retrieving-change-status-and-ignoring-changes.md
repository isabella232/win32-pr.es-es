---
title: Recuperar el estado del cambio y omitir los cambios
description: El cliente puede consultar el administrador de tablas de enrutamiento para averiguar si una notificación de un cambio en un destino está pendiente mediante una llamada a RtmGetChangeStatus. Esta función devuelve TRUE hasta que el autor de la llamada recupera este cambio llamando a RtmGetChangedDests.
ms.assetid: 778279ac-00c5-4de0-9ac7-eca1ac7fec6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a339cbf9ba4e97dfef25b2ebc2020ff94f8e20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774640"
---
# <a name="retrieving-change-status-and-ignoring-changes"></a>Recuperar el estado del cambio y omitir los cambios

El cliente puede consultar el administrador de tablas de enrutamiento para averiguar si una notificación de un cambio en un destino está pendiente mediante una llamada a [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus). Esta función devuelve **true** hasta que el autor de la llamada recupera este cambio llamando a [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).

Un cliente puede utilizar esta consulta para evitar realizar una acción que se tendría que deshacer una vez recibida y procesada la notificación de cambios. El uso de esta característica permite al cliente trabajar de forma eficaz aplazando ciertas operaciones en un momento posterior.

El cliente también puede omitir una notificación de cambio pendiente para un destino mediante una llamada a [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests). Una llamada posterior a [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) no devuelve este destino a menos que se produzca otro cambio después de la llamada a [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).

 

 




