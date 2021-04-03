---
title: Devoluciones de llamada locales Leave
description: Una vez que IGMP notifica al administrador del grupo de multidifusión que no hay más receptores presentes para un grupo en una interfaz, el administrador del grupo de multidifusión invoca la devolución de llamada de la \_ devolución de llamada de salida local de PMGM \_ \_ al Protocolo de enrutamiento de esa interfaz, si existe. Esta devolución de llamada notifica al Protocolo de enrutamiento el cambio.
ms.assetid: 47696533-603c-459f-9aa7-3ce42fff3332
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a98d32e041b048e15497bc7fe35d17628b9331d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075936"
---
# <a name="local-leave-callbacks"></a><span data-ttu-id="db62b-104">Devoluciones de llamada locales Leave</span><span class="sxs-lookup"><span data-stu-id="db62b-104">Local Leave Callbacks</span></span>

<span data-ttu-id="db62b-105">Una vez que IGMP notifica al administrador del grupo de multidifusión que no hay más receptores presentes para un grupo en una interfaz, el administrador del grupo de multidifusión invoca la devolución de llamada de la [**\_ devolución de \_ \_ llamada de salida local de PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) al Protocolo de enrutamiento de esa interfaz, si existe.</span><span class="sxs-lookup"><span data-stu-id="db62b-105">After the multicast group manager is notified by IGMP that there are no more receivers present for a group on an interface, the multicast group manager invokes the [**PMGM\_LOCAL\_LEAVE\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) callback to the routing protocol on that interface if one exists.</span></span> <span data-ttu-id="db62b-106">Esta devolución de llamada notifica al Protocolo de enrutamiento el cambio.</span><span class="sxs-lookup"><span data-stu-id="db62b-106">This callback notifies the routing protocol of the change.</span></span>

<span data-ttu-id="db62b-107">Esta devolución de llamada y la devolución de llamada de [**\_ \_ \_ devoluciones de llamada de combinación local PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) se usan para sincronizar el reenvío entre IGMP y los protocolos de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="db62b-107">This callback and the [**PMGM\_LOCAL\_JOIN\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) callback are used to synchronize forwarding between IGMP and routing protocols.</span></span>

 

 




