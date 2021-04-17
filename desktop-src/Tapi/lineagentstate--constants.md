---
description: Las \_ constantes LINEAGENTSTATE describen el estado de un agente en una dirección.
ms.assetid: 1dbc33e7-05cc-4cb9-8904-f495b884b8db
title: Constantes de LINEAGENTSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b5afa8f93cfde5529f8f57fd8e48d37ecd415b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681097"
---
# <a name="lineagentstate_-constants"></a><span data-ttu-id="0a8c4-103">Constantes de LINEAGENTSTATE \_</span><span class="sxs-lookup"><span data-stu-id="0a8c4-103">LINEAGENTSTATE\_ Constants</span></span>

<span data-ttu-id="0a8c4-104">Las **\_ constantes LINEAGENTSTATE** describen el estado de un agente en una dirección.</span><span class="sxs-lookup"><span data-stu-id="0a8c4-104">The **LINEAGENTSTATE\_ constants** describe the state of an agent on an address.</span></span>

<dl> <dt>

<span data-ttu-id="0a8c4-105"><span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**LINEAGENTSTATE \_ BUSYACD**</span><span class="sxs-lookup"><span data-stu-id="0a8c4-105"><span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**LINEAGENTSTATE\_BUSYACD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0a8c4-106">El agente está ocupado administrando una llamada enrutada desde una cola de ACD.</span><span class="sxs-lookup"><span data-stu-id="0a8c4-106">The agent is busy handling a call routed from an ACD queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a8c4-107"><span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**LINEAGENTSTATE \_ BUSYINCOMING**</span><span class="sxs-lookup"><span data-stu-id="0a8c4-107"><span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**LINEAGENTSTATE\_BUSYINCOMING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0a8c4-108">El agente está ocupado administrando una llamada entrante que no se transfirió al agente desde una cola de ACD en la que el agente ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="0a8c4-108">The agent is busy handling an incoming call that was not transferred to the agent from an ACD queue in which the agent is logged in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a8c4-109"><span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**LINEAGENTSTATE \_ BUSYOTHER**</span><span class="sxs-lookup"><span data-stu-id="0a8c4-109"><span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**LINEAGENTSTATE\_BUSYOTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0a8c4-110">El agente está ocupado administrando otro tipo de llamada, como una llamada personal de salida que no se transfiere al agente mediante un marcador de predicción.</span><span class="sxs-lookup"><span data-stu-id="0a8c4-110">The agent is busy handling another type of call, such as an outgoing personal call not transferred to the agent by a predictive dialer.</span></span> <span data-ttu-id="0a8c4-111">Este valor también se puede usar cuando se sabe que el agente está ocupado en una llamada, pero se desconoce el tipo de llamada.</span><span class="sxs-lookup"><span data-stu-id="0a8c4-111">This value can also be used when the agent is known to be busy on a call but the type of call is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a8c4-112"><span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**LINEAGENTSTATE \_ BUSYOUTBOUND**</span><span class="sxs-lookup"><span data-stu-id="0a8c4-112"><span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**LINEAGENTSTATE\_BUSYOUTBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0a8c4-113">El agente está ocupado administrando una llamada saliente, como una enrutada desde una cola de marcado predictivo.</span><span class="sxs-lookup"><span data-stu-id="0a8c4-113">The agent is busy handling an outgoing call, such as one routed from a predictive dialing queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a8c4-114"><span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**LINEAGENTSTATE \_ LOGGEDOFF**</span><span class="sxs-lookup"><span data-stu-id="0a8c4-114"><span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**LINEAGENTSTATE\_LOGGEDOFF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0a8c4-115">Ningún agente ha iniciado sesión en la dirección.</span><span class="sxs-lookup"><span data-stu-id="0a8c4-115">No agent is logged in on the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a8c4-116"><span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE \_ NOhuellal**</span><span class="sxs-lookup"><span data-stu-id="0a8c4-116"><span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0a8c4-117">El agente ha iniciado sesión, pero está ocupado con una tarea que no es atender una llamada (por ejemplo, en un salto).</span><span class="sxs-lookup"><span data-stu-id="0a8c4-117">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="0a8c4-118">No se deben enrutar llamadas adicionales al agente.</span><span class="sxs-lookup"><span data-stu-id="0a8c4-118">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a8c4-119"><span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE \_ listo**</span><span class="sxs-lookup"><span data-stu-id="0a8c4-119"><span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0a8c4-120">El agente está listo para aceptar llamadas.</span><span class="sxs-lookup"><span data-stu-id="0a8c4-120">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a8c4-121"><span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="0a8c4-121"><span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0a8c4-122">El estado del agente es desconocido y nunca se conocerá.</span><span class="sxs-lookup"><span data-stu-id="0a8c4-122">The agent state is unknown and will never become known.</span></span> <span data-ttu-id="0a8c4-123">En [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus), esta condición también se puede representar mediante el miembro **dwAgentState** que se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="0a8c4-123">In [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus), this condition can also be represented by the **dwAgentState** member being set to 0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a8c4-124"><span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="0a8c4-124"><span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0a8c4-125">El estado del agente es desconocido actualmente, pero puede ser conocido más adelante.</span><span class="sxs-lookup"><span data-stu-id="0a8c4-125">The agent state is currently unknown, but may become known later.</span></span> <span data-ttu-id="0a8c4-126">Puede ser un estado de transición cuando se abre por primera vez una línea o dirección.</span><span class="sxs-lookup"><span data-stu-id="0a8c4-126">This can be a transitional state when a line or address is first opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a8c4-127"><span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**LINEAGENTSTATE \_ WORKINGAFTERCALL**</span><span class="sxs-lookup"><span data-stu-id="0a8c4-127"><span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**LINEAGENTSTATE\_WORKINGAFTERCALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0a8c4-128">El agente ha completado la llamada anterior, pero sigue ocupado con el trabajo relacionado con esa llamada.</span><span class="sxs-lookup"><span data-stu-id="0a8c4-128">The agent has completed the preceding call, but is still occupied with work related to that call.</span></span> <span data-ttu-id="0a8c4-129">El agente no debe recibir llamadas adicionales.</span><span class="sxs-lookup"><span data-stu-id="0a8c4-129">The agent should not receive additional calls.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a8c4-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a8c4-130">Remarks</span></span>

<span data-ttu-id="0a8c4-131">Los 16 bits superiores de este conjunto de constantes se reservan para las extensiones específicas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a8c4-131">The upper 16 bits of this set of constants are reserved for device-specific extensions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a8c4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a8c4-132">Requirements</span></span>



| <span data-ttu-id="0a8c4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a8c4-133">Requirement</span></span> | <span data-ttu-id="0a8c4-134">Value</span><span class="sxs-lookup"><span data-stu-id="0a8c4-134">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0a8c4-135">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="0a8c4-135">TAPI version</span></span><br/> | <span data-ttu-id="0a8c4-136">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="0a8c4-136">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="0a8c4-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a8c4-137">Header</span></span><br/>       | <dl> <span data-ttu-id="0a8c4-138"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a8c4-138"><dt>Tapi.h</dt></span></span> </dl> |



 

 




