---
description: Las \_ constantes LINEAGENTSTATEEX describen el estado de un agente en una dirección.
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: Constantes de LINEAGENTSTATEEX_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 214b816a35e3fdb420a9d95772c466791c6d2f2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690973"
---
# <a name="lineagentstateex_-constants"></a><span data-ttu-id="240f7-103">Constantes de LINEAGENTSTATEEX \_</span><span class="sxs-lookup"><span data-stu-id="240f7-103">LINEAGENTSTATEEX\_ Constants</span></span>

<span data-ttu-id="240f7-104">Las **\_ constantes LINEAGENTSTATEEX** describen el estado de un agente en una dirección.</span><span class="sxs-lookup"><span data-stu-id="240f7-104">The **LINEAGENTSTATEEX\_ constants** describe the state of an agent on an address.</span></span>

<dl> <dt>

<span data-ttu-id="240f7-105"><span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX \_ BUSYACD**</span><span class="sxs-lookup"><span data-stu-id="240f7-105"><span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX\_BUSYACD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="240f7-106">El agente está ocupado administrando una llamada enrutada desde una cola de ACD.</span><span class="sxs-lookup"><span data-stu-id="240f7-106">The agent is busy handling a call routed from an ACD queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="240f7-107"><span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX \_ BUSYINCOMING**</span><span class="sxs-lookup"><span data-stu-id="240f7-107"><span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX\_BUSYINCOMING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="240f7-108">El agente está ocupado administrando una llamada entrante que no se transfirió al agente desde una cola de ACD en la que el agente ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="240f7-108">The agent is busy handling an incoming call that was not transferred to the agent from an ACD queue in which the agent is logged in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="240f7-109"><span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX \_ BUSYOUTGOING**</span><span class="sxs-lookup"><span data-stu-id="240f7-109"><span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX\_BUSYOUTGOING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="240f7-110">El agente está ocupado administrando una llamada saliente, como una enrutada desde una cola de marcado predictivo.</span><span class="sxs-lookup"><span data-stu-id="240f7-110">The agent is busy handling an outgoing call, such as one routed from a predictive dialing queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="240f7-111"><span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX \_ NOhuellal**</span><span class="sxs-lookup"><span data-stu-id="240f7-111"><span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="240f7-112">El agente ha iniciado sesión, pero está ocupado con una tarea que no es atender una llamada (por ejemplo, en un salto).</span><span class="sxs-lookup"><span data-stu-id="240f7-112">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="240f7-113">No se deben enrutar llamadas adicionales al agente.</span><span class="sxs-lookup"><span data-stu-id="240f7-113">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="240f7-114"><span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX \_ listo**</span><span class="sxs-lookup"><span data-stu-id="240f7-114"><span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="240f7-115">El agente está listo para aceptar llamadas.</span><span class="sxs-lookup"><span data-stu-id="240f7-115">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="240f7-116"><span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX \_ liberado**</span><span class="sxs-lookup"><span data-stu-id="240f7-116"><span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX\_RELEASED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="240f7-117">El agente se ha liberado, probablemente porque ha cerrado la sesión.</span><span class="sxs-lookup"><span data-stu-id="240f7-117">The agent has been released, probably because they logged off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="240f7-118"><span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="240f7-118"><span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="240f7-119">El estado del agente es desconocido actualmente, pero puede ser conocido más adelante.</span><span class="sxs-lookup"><span data-stu-id="240f7-119">The agent state is currently unknown, but may become known later.</span></span> <span data-ttu-id="240f7-120">Puede ser un estado de transición cuando se abre por primera vez una línea o dirección.</span><span class="sxs-lookup"><span data-stu-id="240f7-120">This can be a transitional state when a line or address is first opened.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="240f7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="240f7-121">Requirements</span></span>



| <span data-ttu-id="240f7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="240f7-122">Requirement</span></span> | <span data-ttu-id="240f7-123">Value</span><span class="sxs-lookup"><span data-stu-id="240f7-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="240f7-124">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="240f7-124">TAPI version</span></span><br/> | <span data-ttu-id="240f7-125">Requiere TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="240f7-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="240f7-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="240f7-126">Header</span></span><br/>       | <dl> <span data-ttu-id="240f7-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="240f7-127"><dt>Tapi.h</dt></span></span> </dl> |



 

 




