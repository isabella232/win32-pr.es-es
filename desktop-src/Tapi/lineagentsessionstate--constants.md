---
description: Las \_ constantes LINEAGENTSESSIONSTATE describen varios Estados de sesión del agente.
ms.assetid: 8a0d06bb-51ba-4eaf-8719-120aed817f63
title: Constantes de LINEAGENTSESSIONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfd1be8cf846d0e23828f0a3540960a86a83ef1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679515"
---
# <a name="lineagentsessionstate_-constants"></a><span data-ttu-id="d64fd-103">Constantes de LINEAGENTSESSIONSTATE \_</span><span class="sxs-lookup"><span data-stu-id="d64fd-103">LINEAGENTSESSIONSTATE\_ Constants</span></span>

<span data-ttu-id="d64fd-104">Las **\_ constantes LINEAGENTSESSIONSTATE** describen varios Estados de sesión del agente.</span><span class="sxs-lookup"><span data-stu-id="d64fd-104">The **LINEAGENTSESSIONSTATE\_ constants** describe various agent session states.</span></span>

<dl> <dt>

<span data-ttu-id="d64fd-105"><span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**LINEAGENTSESSIONSTATE \_ BUSYONCALL**</span><span class="sxs-lookup"><span data-stu-id="d64fd-105"><span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**LINEAGENTSESSIONSTATE\_BUSYONCALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d64fd-106">El agente está ocupado administrando una llamada.</span><span class="sxs-lookup"><span data-stu-id="d64fd-106">The agent is busy handling a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d64fd-107"><span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**LINEAGENTSESSIONSTATE \_ BUSYWRAPUP**</span><span class="sxs-lookup"><span data-stu-id="d64fd-107"><span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**LINEAGENTSESSIONSTATE\_BUSYWRAPUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d64fd-108">El agente está ocupado administrando el ajuste de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d64fd-108">The agent is busy handling the wrap-up of the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d64fd-109"><span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE \_ finalizado**</span><span class="sxs-lookup"><span data-stu-id="d64fd-109"><span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE\_ENDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d64fd-110">La sesión del agente ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="d64fd-110">The agent session has ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d64fd-111"><span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE \_ NOhuellal**</span><span class="sxs-lookup"><span data-stu-id="d64fd-111"><span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d64fd-112">El agente ha iniciado sesión, pero está ocupado con una tarea que no es atender una llamada (por ejemplo, en un salto).</span><span class="sxs-lookup"><span data-stu-id="d64fd-112">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="d64fd-113">No se deben enrutar llamadas adicionales al agente.</span><span class="sxs-lookup"><span data-stu-id="d64fd-113">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d64fd-114"><span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE \_ listo**</span><span class="sxs-lookup"><span data-stu-id="d64fd-114"><span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d64fd-115">El agente está listo para aceptar llamadas.</span><span class="sxs-lookup"><span data-stu-id="d64fd-115">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d64fd-116"><span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE \_ liberado**</span><span class="sxs-lookup"><span data-stu-id="d64fd-116"><span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE\_RELEASED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d64fd-117">Se liberó la sesión del agente.</span><span class="sxs-lookup"><span data-stu-id="d64fd-117">The agent session has been released.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d64fd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d64fd-118">Requirements</span></span>



| <span data-ttu-id="d64fd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d64fd-119">Requirement</span></span> | <span data-ttu-id="d64fd-120">Value</span><span class="sxs-lookup"><span data-stu-id="d64fd-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d64fd-121">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="d64fd-121">TAPI version</span></span><br/> | <span data-ttu-id="d64fd-122">Requiere TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="d64fd-122">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="d64fd-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d64fd-123">Header</span></span><br/>       | <dl> <span data-ttu-id="d64fd-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d64fd-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




