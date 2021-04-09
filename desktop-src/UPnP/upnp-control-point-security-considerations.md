---
title: Consideraciones de seguridad de punto de control
description: Al crear un punto de control, debe tener en cuenta los siguientes problemas de seguridad.
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0165ad0c8a721b10d5cc34c49947a98f2c15d1de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994442"
---
# <a name="control-point-security-considerations"></a><span data-ttu-id="74a70-103">Consideraciones de seguridad de punto de control</span><span class="sxs-lookup"><span data-stu-id="74a70-103">Control Point Security Considerations</span></span>

<span data-ttu-id="74a70-104">Al crear un punto de control, debe tener en cuenta los siguientes problemas de seguridad.</span><span class="sxs-lookup"><span data-stu-id="74a70-104">When you are creating a control point, you need to take into consideration the following security issues.</span></span>

-   <span data-ttu-id="74a70-105">De forma predeterminada, todas las búsquedas de puntos de control se envían con un TTL de 1.</span><span class="sxs-lookup"><span data-stu-id="74a70-105">All control point searches are by default sent with a TTL of 1.</span></span> <span data-ttu-id="74a70-106">Esto significa que solo se detectan los dispositivos dentro de la misma subred.</span><span class="sxs-lookup"><span data-stu-id="74a70-106">This means that only devices within the same subnet are discovered.</span></span> <span data-ttu-id="74a70-107">Puede configurar un TTL superior en el registro.</span><span class="sxs-lookup"><span data-stu-id="74a70-107">You can configure a higher TTL in the registry.</span></span>
-   <span data-ttu-id="74a70-108">La descripción del dispositivo y del servicio de un dispositivo solo se descarga si está presente en el mismo dispositivo que envió el anuncio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74a70-108">A device's device and service description is only downloaded if it is present on the same device which sent the device announcement.</span></span>
-   <span data-ttu-id="74a70-109">Un dispositivo solo envía solicitudes de control y suscripción si las direcciones URL de control y suscripción se encuentran en el mismo dispositivo que envió los anuncios del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74a70-109">A device is only sent control and subscription requests if its control and subscription URLs are on the same device that sent the device announcements.</span></span>

 

 




