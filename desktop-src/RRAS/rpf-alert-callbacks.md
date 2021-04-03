---
title: Devoluciones de llamada de alerta de RPF
description: Una vez que el administrador del grupo de multidifusión recibe la notificación de un paquete de un nuevo origen o de un paquete destinado a un grupo nuevo, el administrador del grupo de multidifusión busca la ruta al origen en la vista multidifusión de la tabla de enrutamiento.
ms.assetid: dacccca2-e6a5-417a-a217-06ff846d55f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7832a25f8b44821f4b46a69943b4bba3519207c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780202"
---
# <a name="rpf-alert-callbacks"></a><span data-ttu-id="b950e-103">Devoluciones de llamada de alerta de RPF</span><span class="sxs-lookup"><span data-stu-id="b950e-103">RPF Alert Callbacks</span></span>

<span data-ttu-id="b950e-104">Una vez que el administrador del grupo de multidifusión recibe la notificación de un paquete de un nuevo origen o de un paquete destinado a un grupo nuevo, el administrador del grupo de multidifusión busca la ruta al origen en la vista multidifusión de la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="b950e-104">After the multicast group manager receives notification of a packet from a new source or of a packet that is destined for a new group, the multicast group manager looks up the route to the source in the multicast view of the routing table.</span></span> <span data-ttu-id="b950e-105">Después, el administrador del grupo de multidifusión invoca la devolución de llamada de [**\_ devolución de \_ llamada de PMGM RPF**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) al protocolo que posee la interfaz en la que llegaron los datos.</span><span class="sxs-lookup"><span data-stu-id="b950e-105">The multicast group manager then invokes the [**PMGM\_RPF\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) callback to the protocol that owns the interface the data arrived on.</span></span>

<span data-ttu-id="b950e-106">Después de invocar esta devolución de llamada, el protocolo de enrutamiento puede cambiar la interfaz entrante si el protocolo de enrutamiento debe recibir los datos para el grupo en una interfaz diferente.</span><span class="sxs-lookup"><span data-stu-id="b950e-106">After this callback is invoked, the routing protocol can change the incoming interface if the routing protocol must receive the data for the group on a different interface.</span></span>

 

 




