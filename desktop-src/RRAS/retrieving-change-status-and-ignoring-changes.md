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
# <a name="retrieving-change-status-and-ignoring-changes"></a><span data-ttu-id="60453-104">Recuperar el estado del cambio y omitir los cambios</span><span class="sxs-lookup"><span data-stu-id="60453-104">Retrieving Change Status and Ignoring Changes</span></span>

<span data-ttu-id="60453-105">El cliente puede consultar el administrador de tablas de enrutamiento para averiguar si una notificación de un cambio en un destino está pendiente mediante una llamada a [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus).</span><span class="sxs-lookup"><span data-stu-id="60453-105">The client can query the routing table manager to find out if a notification of a change to a destination is pending by calling [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus).</span></span> <span data-ttu-id="60453-106">Esta función devuelve **true** hasta que el autor de la llamada recupera este cambio llamando a [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).</span><span class="sxs-lookup"><span data-stu-id="60453-106">This function returns **TRUE** until the caller retrieves this change by calling [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).</span></span>

<span data-ttu-id="60453-107">Un cliente puede utilizar esta consulta para evitar realizar una acción que se tendría que deshacer una vez recibida y procesada la notificación de cambios.</span><span class="sxs-lookup"><span data-stu-id="60453-107">A client can use this query to avoid performing an action that would have to be undone after the change notification is received and processed.</span></span> <span data-ttu-id="60453-108">El uso de esta característica permite al cliente trabajar de forma eficaz aplazando ciertas operaciones en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="60453-108">Using this feature allows the client to work efficiently by deferring certain operations to a later time.</span></span>

<span data-ttu-id="60453-109">El cliente también puede omitir una notificación de cambio pendiente para un destino mediante una llamada a [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span><span class="sxs-lookup"><span data-stu-id="60453-109">The client can also ignore a pending change notification for a destination by calling [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span></span> <span data-ttu-id="60453-110">Una llamada posterior a [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) no devuelve este destino a menos que se produzca otro cambio después de la llamada a [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span><span class="sxs-lookup"><span data-stu-id="60453-110">A later call to [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) does not return this destination unless another change occurs after the call to [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span></span>

 

 




