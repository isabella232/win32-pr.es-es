---
description: Las \_ constantes de marcador de bits LINEADDRESSSHARING describen varias maneras en que se puede compartir una dirección entre las líneas.
ms.assetid: f37ba549-c8dc-4a7c-bfe6-8e5f733d9750
title: Constantes de LINEADDRESSSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785c7e924ffc958d3fe14b739bb2eb28dec322a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680250"
---
# <a name="lineaddresssharing_-constants"></a><span data-ttu-id="59e24-103">Constantes de LINEADDRESSSHARING \_</span><span class="sxs-lookup"><span data-stu-id="59e24-103">LINEADDRESSSHARING\_ Constants</span></span>

<span data-ttu-id="59e24-104">Las constantes de marcador de bits **LINEADDRESSSHARING \_** describen varias maneras en que se puede compartir una dirección entre las líneas.</span><span class="sxs-lookup"><span data-stu-id="59e24-104">The **LINEADDRESSSHARING\_** bit-flag constants describe various ways an address can be shared between lines.</span></span>

<dl> <dt>

<span data-ttu-id="59e24-105"><span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING \_ privado**</span><span class="sxs-lookup"><span data-stu-id="59e24-105"><span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING\_PRIVATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59e24-106">La dirección es privada para la línea del usuario; no se asigna a ninguna otra estación.</span><span class="sxs-lookup"><span data-stu-id="59e24-106">The address is private to the user's line; it is not assigned to any other station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59e24-107"><span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING \_ BRIDGEDEXCL**</span><span class="sxs-lookup"><span data-stu-id="59e24-107"><span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING\_BRIDGEDEXCL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59e24-108">La dirección se enlaza a una o varias estaciones.</span><span class="sxs-lookup"><span data-stu-id="59e24-108">The address is bridged to one or more other stations.</span></span> <span data-ttu-id="59e24-109">La primera línea para activar una llamada en la línea tendrá acceso exclusivo a la dirección y llamadas que pueden existir en ella.</span><span class="sxs-lookup"><span data-stu-id="59e24-109">The first line to activate a call on the line will have exclusive access to the address and calls that may exist on it.</span></span> <span data-ttu-id="59e24-110">Otras líneas no podrán usar la dirección de puente mientras esté en uso.</span><span class="sxs-lookup"><span data-stu-id="59e24-110">Other lines will not be able to use the bridged address while it is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59e24-111"><span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING \_ BRIDGEDNEW**</span><span class="sxs-lookup"><span data-stu-id="59e24-111"><span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING\_BRIDGEDNEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59e24-112">La dirección se enlaza con una o varias estaciones.</span><span class="sxs-lookup"><span data-stu-id="59e24-112">The address is bridged with one or more other stations.</span></span> <span data-ttu-id="59e24-113">La primera línea para activar una llamada en la línea tendrá acceso exclusivo únicamente a la llamada correspondiente.</span><span class="sxs-lookup"><span data-stu-id="59e24-113">The first line to activate a call on the line will have exclusive access to only the corresponding call.</span></span> <span data-ttu-id="59e24-114">Otras aplicaciones que utilizan la dirección darán lugar a una apariencia de llamada nueva y separada.</span><span class="sxs-lookup"><span data-stu-id="59e24-114">Other applications that use the address will result in new and separate call appearances.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59e24-115"><span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING \_ BRIDGEDSHARED**</span><span class="sxs-lookup"><span data-stu-id="59e24-115"><span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING\_BRIDGEDSHARED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59e24-116">La dirección se enlaza con una o varias líneas.</span><span class="sxs-lookup"><span data-stu-id="59e24-116">The address is bridged with one or more other lines.</span></span> <span data-ttu-id="59e24-117">Todas las entidades puente pueden compartirse en llamadas en la dirección, que, a continuación, funciona como una conferencia.</span><span class="sxs-lookup"><span data-stu-id="59e24-117">All bridged parties can share in calls on the address, which then functions as a conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59e24-118"><span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING \_ supervisado**</span><span class="sxs-lookup"><span data-stu-id="59e24-118"><span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING\_MONITORED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59e24-119">Se trata de una dirección cuyo estado de inactividad se pone a disposición de esta línea.</span><span class="sxs-lookup"><span data-stu-id="59e24-119">This is an address whose idle/busy status is made available to this line.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59e24-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59e24-120">Remarks</span></span>

<span data-ttu-id="59e24-121">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="59e24-121">No extensibility.</span></span> <span data-ttu-id="59e24-122">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="59e24-122">All 32 bits are reserved.</span></span>

<span data-ttu-id="59e24-123">La forma en que una dirección se comparte entre las líneas puede afectar al comportamiento de esa dirección.</span><span class="sxs-lookup"><span data-stu-id="59e24-123">The way in which an address is shared across lines can affect the behavior of that address.</span></span> <span data-ttu-id="59e24-124">[**Línea \_ de**](line-callstate.md) Los mensajes CALLSTATE y [**\_ ADDRESSSTATE de línea**](line-addressstate.md) se envían a la aplicación en respuesta a las actividades de las estaciones de puente.</span><span class="sxs-lookup"><span data-stu-id="59e24-124">[**LINE\_CALLSTATE**](line-callstate.md) and [**LINE\_ADDRESSSTATE**](line-addressstate.md) messages are sent to the application in response to activities by the bridging stations.</span></span> <span data-ttu-id="59e24-125">A través de estos mensajes, una aplicación puede realizar un seguimiento del estado de la dirección.</span><span class="sxs-lookup"><span data-stu-id="59e24-125">It is through these messages that an application can track the status of the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="59e24-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59e24-126">Requirements</span></span>



| <span data-ttu-id="59e24-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="59e24-127">Requirement</span></span> | <span data-ttu-id="59e24-128">Value</span><span class="sxs-lookup"><span data-stu-id="59e24-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="59e24-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="59e24-129">TAPI version</span></span><br/> | <span data-ttu-id="59e24-130">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="59e24-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="59e24-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59e24-131">Header</span></span><br/>       | <dl> <span data-ttu-id="59e24-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="59e24-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59e24-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="59e24-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59e24-134">**LÍNEA \_ ADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="59e24-134">**LINE\_ADDRESSSTATE**</span></span>](line-addressstate.md)
</dt> <dt>

[<span data-ttu-id="59e24-135">**LÍNEA \_ CALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="59e24-135">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> </dl>

 

 




