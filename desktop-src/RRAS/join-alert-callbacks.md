---
title: Combinar devoluciones de llamada de alerta
description: Cuando se notifica al administrador del grupo de multidifusión que hay nuevos receptores presentes para un grupo en una interfaz, el administrador del grupo de multidifusión invoca la devolución de llamada de devolución de llamada de alerta de combinación de PMGM \_ \_ \_ .
ms.assetid: b625f8ec-f59b-4151-aa38-48cf8f004966
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00dc70160b99c3cfc0e41078a3bd5882d930f31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075938"
---
# <a name="join-alert-callbacks"></a><span data-ttu-id="7ee42-103">Combinar devoluciones de llamada de alerta</span><span class="sxs-lookup"><span data-stu-id="7ee42-103">Join Alert Callbacks</span></span>

<span data-ttu-id="7ee42-104">Cuando se notifica al administrador del grupo de multidifusión que hay nuevos receptores presentes para un grupo en una interfaz, el administrador del grupo de multidifusión invoca la devolución de llamada de [**devolución de llamada de alerta de combinación de PMGM \_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) .</span><span class="sxs-lookup"><span data-stu-id="7ee42-104">When the multicast group manager is notified that there are new receivers present for a group on an interface, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback.</span></span> <span data-ttu-id="7ee42-105">Esta devolución de llamada notifica a los protocolos de enrutamiento que los nuevos hosts se han unido a los grupos especificados.</span><span class="sxs-lookup"><span data-stu-id="7ee42-105">This callback notifies the routing protocols that new hosts have joined the specified groups .</span></span> <span data-ttu-id="7ee42-106">Por lo tanto, los protocolos de enrutamiento deben solicitar datos de multidifusión para los grupos especificados por la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="7ee42-106">Therefore, the routing protocols must request multicast data for the groups specified by the callback.</span></span>

<span data-ttu-id="7ee42-107">El administrador del grupo de multidifusión usa un conjunto predefinido de reglas que se utilizan para determinar cuándo se invoca esta devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="7ee42-107">The multicast group manager uses a predefined set of rules that are used to determine when this callback is invoked.</span></span> <span data-ttu-id="7ee42-108">Este conjunto de reglas se basa en el tipo de solicitud de combinación enviada por el cliente y en el orden en que se recibieron las solicitudes de Unión.</span><span class="sxs-lookup"><span data-stu-id="7ee42-108">This set of rules is based on both the type of join request sent by the client and the order the join requests were received in.</span></span>

## <a name="wildcard-join-requests"></a><span data-ttu-id="7ee42-109">Solicitudes de combinación comodín</span><span class="sxs-lookup"><span data-stu-id="7ee42-109">Wildcard Join Requests</span></span>

<span data-ttu-id="7ee42-110">Cuando se recibe una combinación de caracteres comodín para un grupo ( \* , g) del primer cliente, el administrador del grupo de multidifusión invoca la devolución de llamada de devolución de llamada de alerta de combinación de PMGM a todos los demás clientes registrados. [**\_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)</span><span class="sxs-lookup"><span data-stu-id="7ee42-110">When a wildcard join for a group (\*, g) is received from the first client, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback to all other registered clients.</span></span> <span data-ttu-id="7ee42-111">Cuando se recibe una combinación de caracteres comodín para un grupo desde el segundo cliente, el administrador del grupo de multidifusión invoca esta devolución de llamada al primer cliente para unirse al grupo.</span><span class="sxs-lookup"><span data-stu-id="7ee42-111">When a wildcard join for a group is received from the second client, the multicast group manager invokes this callback to the first client to join the group.</span></span>

## <a name="source-specific-join-requests"></a><span data-ttu-id="7ee42-112">Solicitudes de Source-Specific join</span><span class="sxs-lookup"><span data-stu-id="7ee42-112">Source-Specific Join Requests</span></span>

<span data-ttu-id="7ee42-113">El administrador del grupo de multidifusión no invoca esta devolución de llamada para las combinaciones posteriores al grupo.</span><span class="sxs-lookup"><span data-stu-id="7ee42-113">The multicast group manager does not invoke this callback for any subsequent joins to the group.</span></span>

<span data-ttu-id="7ee42-114">Cuando se recibe una combinación específica del origen para un grupo (s, g), el administrador del grupo de multidifusión invoca la devolución de llamada de [**devolución de llamada de alerta de PMGM \_ join \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) solo para el cliente que posee la interfaz de entrada hacia los orígenes.</span><span class="sxs-lookup"><span data-stu-id="7ee42-114">When a source-specific join for a group (s, g) is received, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback only for the client that owns the incoming interface towards the source s.</span></span>

 

 




