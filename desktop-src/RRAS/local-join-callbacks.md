---
title: Devoluciones de llamada de combinación local
description: Una vez que IGMP notifica al administrador del grupo de multidifusión que hay nuevos receptores para un grupo en una interfaz, el administrador del grupo de multidifusión invoca la devolución de llamada de \_ devolución de llamada de combinación local de PMGM \_ \_ al Protocolo de enrutamiento que posee la interfaz si existe una.
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c97f0e16e08bc3781b946a51f69d2b0d65b3272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486938"
---
# <a name="local-join-callbacks"></a><span data-ttu-id="eda0a-103">Devoluciones de llamada de combinación local</span><span class="sxs-lookup"><span data-stu-id="eda0a-103">Local Join Callbacks</span></span>

<span data-ttu-id="eda0a-104">Una vez que IGMP notifica al administrador del grupo de multidifusión que hay nuevos receptores para un grupo en una interfaz, el administrador del grupo de multidifusión invoca la devolución de llamada de [**\_ devolución de \_ \_ llamada de combinación local de PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) al Protocolo de enrutamiento que posee la interfaz si existe una.</span><span class="sxs-lookup"><span data-stu-id="eda0a-104">After the multicast group manager is notified by IGMP that new receivers are present for a group on an interface, the multicast group manager invokes the [**PMGM\_LOCAL\_JOIN\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) callback to the routing protocol that owns the interface if one exists.</span></span> <span data-ttu-id="eda0a-105">Esta devolución de llamada notifica al Protocolo de enrutamiento el cambio.</span><span class="sxs-lookup"><span data-stu-id="eda0a-105">This callback notifies the routing protocol of the change.</span></span>

<span data-ttu-id="eda0a-106">Esta devolución de llamada y la devolución de llamada de [**\_ \_ salida \_ local de PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) se usan para sincronizar el reenvío entre IGMP y los protocolos de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="eda0a-106">This callback and the [**PMGM\_LOCAL\_LEAVE\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) callback are used to synchronize forwarding between IGMP and routing protocols.</span></span>

 

 




