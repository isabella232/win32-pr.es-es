---
title: Devoluciones de llamada del administrador de grupo de multidifusión
description: El administrador del grupo de multidifusión usa las siguientes devoluciones de llamada para notificar a los clientes (normalmente, los protocolos de enrutamiento) de eventos y cambios de estado.
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ba18f874005e23aef6daca6071362362312e8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904713"
---
# <a name="multicast-group-manager-callbacks"></a><span data-ttu-id="f3ebd-103">Devoluciones de llamada del administrador de grupo de multidifusión</span><span class="sxs-lookup"><span data-stu-id="f3ebd-103">Multicast Group Manager Callbacks</span></span>

<span data-ttu-id="f3ebd-104">El administrador del grupo de multidifusión usa las siguientes devoluciones de llamada para notificar a los clientes (normalmente, los protocolos de enrutamiento) de eventos y cambios de estado:</span><span class="sxs-lookup"><span data-stu-id="f3ebd-104">The multicast group manager uses the following callbacks to notify clients (typically, routing protocols) of events and state changes:</span></span>

[<span data-ttu-id="f3ebd-105">**\_devolución de \_ llamada de alerta de creación de PMGM \_**</span><span class="sxs-lookup"><span data-stu-id="f3ebd-105">**PMGM\_CREATION\_ALERT\_CALLBACK**</span></span>](/windows/win32/api/mgm/nc-mgm-pmgm_creation_alert_callback)

[<span data-ttu-id="f3ebd-106">**\_devolución de \_ llamada de alerta de combinación de PMGM \_**</span><span class="sxs-lookup"><span data-stu-id="f3ebd-106">**PMGM\_JOIN\_ALERT\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)

[<span data-ttu-id="f3ebd-107">**\_devolución de \_ llamada de alerta de eliminación de PMGM \_**</span><span class="sxs-lookup"><span data-stu-id="f3ebd-107">**PMGM\_PRUNE\_ALERT\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

[<span data-ttu-id="f3ebd-108">**\_devolución de \_ llamada de combinación local de PMGM \_**</span><span class="sxs-lookup"><span data-stu-id="f3ebd-108">**PMGM\_LOCAL\_JOIN\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback)

[<span data-ttu-id="f3ebd-109">**\_devolución de \_ llamada de Leave local de PMGM \_**</span><span class="sxs-lookup"><span data-stu-id="f3ebd-109">**PMGM\_LOCAL\_LEAVE\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback)

[<span data-ttu-id="f3ebd-110">**devolución de llamada de \_ RPF PMGM \_**</span><span class="sxs-lookup"><span data-stu-id="f3ebd-110">**PMGM\_RPF\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback)

[<span data-ttu-id="f3ebd-111">**PMGM \_ incorrecto \_ si la \_ devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="f3ebd-111">**PMGM\_WRONG\_IF\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)

<span data-ttu-id="f3ebd-112">El administrador del grupo de multidifusión usa las siguientes devoluciones de llamada para notificar a IGMP de eventos y cambios de estado:</span><span class="sxs-lookup"><span data-stu-id="f3ebd-112">The multicast group manager uses the following callbacks to notify IGMP of events and state changes:</span></span>

[<span data-ttu-id="f3ebd-113">**PMGM \_ deshabilitar \_ \_ devolución de llamada IGMP**</span><span class="sxs-lookup"><span data-stu-id="f3ebd-113">**PMGM\_DISABLE\_IGMP\_CALLBACK**</span></span>](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback)

[<span data-ttu-id="f3ebd-114">**PMGM \_ habilitar \_ \_ devolución de llamada IGMP**</span><span class="sxs-lookup"><span data-stu-id="f3ebd-114">**PMGM\_ENABLE\_IGMP\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

 

 