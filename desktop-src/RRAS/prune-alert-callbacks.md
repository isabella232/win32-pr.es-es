---
title: Eliminar devoluciones de llamada de alerta
description: Cuando se notifica al administrador del grupo de multidifusión que los receptores están abandonando un grupo en una interfaz, el administrador del grupo de multidifusión invoca la devolución de llamada de devolución de llamada de la alerta de eliminación de PMGM \_ \_ \_ .
ms.assetid: 34eb6941-9488-481f-93ca-821789acc140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a81dab70eaded0fd1fe21bd1b5ec1b5ca495272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076256"
---
# <a name="prune-alert-callbacks"></a><span data-ttu-id="2f852-103">Eliminar devoluciones de llamada de alerta</span><span class="sxs-lookup"><span data-stu-id="2f852-103">Prune Alert Callbacks</span></span>

<span data-ttu-id="2f852-104">Cuando se notifica al administrador del grupo de multidifusión que los receptores están abandonando un grupo en una interfaz, el administrador del grupo de multidifusión invoca la devolución de llamada de devolución de llamada de la [**\_ alerta de eliminación de \_ \_ PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) .</span><span class="sxs-lookup"><span data-stu-id="2f852-104">When the multicast group manager is notified that receivers are leaving a group on an interface, the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback.</span></span> <span data-ttu-id="2f852-105">Esta devolución de llamada notifica a los protocolos de enrutamiento que los clientes ya no pertenecen al grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="2f852-105">This callback notifies the routing protocols that clients no longer belong to the specified group.</span></span> <span data-ttu-id="2f852-106">Por lo tanto, los protocolos de enrutamiento deben dejar de solicitar datos de multidifusión para los grupos especificados.</span><span class="sxs-lookup"><span data-stu-id="2f852-106">Therefore, the routing protocols must stop requesting multicast data for the specified groups.</span></span>

<span data-ttu-id="2f852-107">El administrador del grupo de multidifusión tiene un conjunto predefinido de reglas que se utilizan para determinar cuándo se invoca esta devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="2f852-107">The multicast group manager has a predefined set of rules that are used to determine when this callback is invoked.</span></span> <span data-ttu-id="2f852-108">Estas reglas se basan en el tipo de solicitud de eliminación enviada por el cliente y en el orden en que se recibieron las solicitudes de eliminación.</span><span class="sxs-lookup"><span data-stu-id="2f852-108">These rules are based on both the type of prune request sent by the client and the order the prune requests were received in.</span></span>

## <a name="wildcard-prune-requests"></a><span data-ttu-id="2f852-109">Solicitudes de eliminación de caracteres comodín</span><span class="sxs-lookup"><span data-stu-id="2f852-109">Wildcard Prune Requests</span></span>

<span data-ttu-id="2f852-110">Cuando se recibe una eliminación de caracteres comodín para un grupo ( \* , g) y se quita la interfaz final del segundo al último cliente (es decir, cuando se conservan interfaces para un solo cliente), el administrador del grupo de multidifusión invoca la devolución de llamada de devolución de llamada de la alerta de eliminación de PMGM al cliente [**\_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) restante.</span><span class="sxs-lookup"><span data-stu-id="2f852-110">When a wildcard prune for a group (\*, g) is received and the final interface is being removed for the second-to-last client (that is, when interfaces for only a single client remain), the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback to that remaining client.</span></span> <span data-ttu-id="2f852-111">Después de quitar la interfaz final del último cliente (es decir, cuando no quedan otras interfaces), se invoca esta devolución de llamada para todos los demás clientes registrados con el administrador del grupo de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="2f852-111">After the final interface is removed for the last client (that is, when no other interfaces remain), then this callback is invoked for all the other clients that are registered with the multicast group manager.</span></span>

## <a name="source-specific-prune-requests"></a><span data-ttu-id="2f852-112">Solicitudes de eliminación de Source-Specific</span><span class="sxs-lookup"><span data-stu-id="2f852-112">Source-Specific Prune Requests</span></span>

<span data-ttu-id="2f852-113">Cuando se recibe una eliminación específica del origen de un grupo (s, g), el administrador del grupo de multidifusión invoca la devolución de llamada de devolución de llamada de la alerta de eliminación de PMGM solo para el cliente que posee la interfaz de entrada hacia los orígenes. [**\_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)</span><span class="sxs-lookup"><span data-stu-id="2f852-113">When a source-specific prune for a group (s, g) is received, the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback only for the client that owns the incoming interface towards the source s.</span></span>

 

 




