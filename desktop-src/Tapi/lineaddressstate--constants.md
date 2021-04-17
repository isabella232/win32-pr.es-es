---
description: Las \_ constantes de marcador de bits LINEADDRESSSTATE describen varios elementos de estado de dirección.
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: Constantes de LINEADDRESSSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483ac665c41989c65b43419442601dfb70667dc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690975"
---
# <a name="lineaddressstate_-constants"></a><span data-ttu-id="775e2-103">Constantes de LINEADDRESSSTATE \_</span><span class="sxs-lookup"><span data-stu-id="775e2-103">LINEADDRESSSTATE\_ Constants</span></span>

<span data-ttu-id="775e2-104">Las constantes de marcador de bits **LINEADDRESSSTATE \_** describen varios elementos de estado de dirección.</span><span class="sxs-lookup"><span data-stu-id="775e2-104">The **LINEADDRESSSTATE\_** bit-flag constants describe various address status items.</span></span>

<dl> <dt>

<span data-ttu-id="775e2-105"><span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE \_ CAPSCHANGE**</span><span class="sxs-lookup"><span data-stu-id="775e2-105"><span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="775e2-106">Indica que, debido a los cambios de configuración realizados por el usuario u otras circunstancias, uno o varios de los miembros de la estructura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) para la dirección han cambiado.</span><span class="sxs-lookup"><span data-stu-id="775e2-106">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure for the address have changed.</span></span> <span data-ttu-id="775e2-107">La aplicación debe usar [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) para leer la estructura actualizada.</span><span class="sxs-lookup"><span data-stu-id="775e2-107">The application should use [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) to read the updated structure.</span></span> <span data-ttu-id="775e2-108">Si un proveedor de servicios envía un mensaje [**line \_ ADDRESSSTATE**](line-addressstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1,4 o posterior de TAPI; las aplicaciones que negocian una versión anterior de API recibirán los mensajes de [**línea \_ LINEDEVSTATE**](line-linedevstate.md) que especifican LINEDEVSTATE \_ reinit, lo que les obliga a apagar y reinicializar su conexión a TAPI para obtener la información actualizada.</span><span class="sxs-lookup"><span data-stu-id="775e2-108">If a service provider sends a [**LINE\_ADDRESSSTATE**](line-addressstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will receive [**LINE\_LINEDEVSTATE**](line-linedevstate.md) messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="775e2-109"><span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="775e2-109"><span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="775e2-110">El elemento específico del dispositivo del estado de la dirección ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="775e2-110">The device-specific item of the address status has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="775e2-111"><span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**LINEADDRESSSTATE \_ adelante**</span><span class="sxs-lookup"><span data-stu-id="775e2-111"><span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**LINEADDRESSSTATE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="775e2-112">El estado de reenvío de la dirección ha cambiado, incluido posiblemente el número de anillos para determinar una condición de no respuesta.</span><span class="sxs-lookup"><span data-stu-id="775e2-112">The forwarding status of the address has changed, including possibly the number of rings for determining a no-answer condition.</span></span> <span data-ttu-id="775e2-113">La aplicación debe comprobar el estado de la dirección para determinar los detalles sobre el estado de reenvío actual de la dirección.</span><span class="sxs-lookup"><span data-stu-id="775e2-113">The application should check the address status to determine details about the address's current forwarding status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="775e2-114"><span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE \_ INUSEMANY**</span><span class="sxs-lookup"><span data-stu-id="775e2-114"><span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE\_INUSEMANY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="775e2-115">La dirección supervisada o con puentes ha cambiado para que una estación la esté usando más de una.</span><span class="sxs-lookup"><span data-stu-id="775e2-115">The monitored or bridged address has changed from being in use by one station to being in use by more than one station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="775e2-116"><span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE \_ INUSEONE**</span><span class="sxs-lookup"><span data-stu-id="775e2-116"><span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE\_INUSEONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="775e2-117">La dirección ha cambiado de inactiva o en uso por muchas estaciones puente para que solo una estación la esté usando.</span><span class="sxs-lookup"><span data-stu-id="775e2-117">The address has changed from idle or in use by many bridged stations to being in use by just one station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="775e2-118"><span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE \_ INUSEZERO**</span><span class="sxs-lookup"><span data-stu-id="775e2-118"><span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE\_INUSEZERO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="775e2-119">La dirección ha cambiado a inactiva (no está en uso por ninguna estación).</span><span class="sxs-lookup"><span data-stu-id="775e2-119">The address has changed to idle (it is not in use by any stations).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="775e2-120"><span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE \_ NUMCALLS**</span><span class="sxs-lookup"><span data-stu-id="775e2-120"><span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE\_NUMCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="775e2-121">El número de llamadas en la dirección ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="775e2-121">The number of calls on the address has changed.</span></span> <span data-ttu-id="775e2-122">Este es el resultado de eventos como una nueva llamada entrante, una llamada saliente en la dirección o una llamada que cambia su estado de suspensión.</span><span class="sxs-lookup"><span data-stu-id="775e2-122">This is the result of events such as a new incoming call, an outgoing call on the address, or a call changing its hold status.</span></span> <span data-ttu-id="775e2-123">Esta marca cubre los cambios en cualquiera de los miembros **dwNumActiveCalls**, **dwNumOnHoldCalls** y **dwNumOnHoldPendingCalls** en la estructura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) .</span><span class="sxs-lookup"><span data-stu-id="775e2-123">This flag covers changes in any of the members **dwNumActiveCalls**, **dwNumOnHoldCalls** and **dwNumOnHoldPendingCalls** in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure.</span></span> <span data-ttu-id="775e2-124">La aplicación debe comprobar los tres miembros cuando recibe un mensaje [**line \_ ADDRESSSTATE**](line-addressstate.md) (numCalls).</span><span class="sxs-lookup"><span data-stu-id="775e2-124">The application should check all three of these members when it receives a [**LINE\_ADDRESSSTATE**](line-addressstate.md) (numCalls) message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="775e2-125"><span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE \_ otro**</span><span class="sxs-lookup"><span data-stu-id="775e2-125"><span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="775e2-126">Los elementos de estado de dirección distintos de los que se enumeran a continuación han cambiado.</span><span class="sxs-lookup"><span data-stu-id="775e2-126">Address-status items other than those listed below have changed.</span></span> <span data-ttu-id="775e2-127">La aplicación debe comprobar el estado de la dirección actual para determinar qué elementos han cambiado.</span><span class="sxs-lookup"><span data-stu-id="775e2-127">The application should check the current address status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="775e2-128"><span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**\_terminales LINEADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="775e2-128"><span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**LINEADDRESSSTATE\_TERMINALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="775e2-129">La configuración de terminal para la dirección ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="775e2-129">The terminal settings for the address have changed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="775e2-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="775e2-130">Remarks</span></span>

<span data-ttu-id="775e2-131">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="775e2-131">No extensibility.</span></span> <span data-ttu-id="775e2-132">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="775e2-132">All 32 bits are reserved.</span></span>

<span data-ttu-id="775e2-133">A una aplicación se le notifican los cambios de estos elementos de estado en el mensaje [**line \_ ADDRESSSTATE**](line-addressstate.md) .</span><span class="sxs-lookup"><span data-stu-id="775e2-133">An application is notified about changes to these status items in the [**LINE\_ADDRESSSTATE**](line-addressstate.md) message.</span></span> <span data-ttu-id="775e2-134">Las funcionalidades de dispositivo de la dirección indican qué cambios de estado de dirección se pueden notificar para esta dirección.</span><span class="sxs-lookup"><span data-stu-id="775e2-134">The address's device capabilities indicate which address state changes can possibly be reported for this address.</span></span>

## <a name="requirements"></a><span data-ttu-id="775e2-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="775e2-135">Requirements</span></span>



| <span data-ttu-id="775e2-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="775e2-136">Requirement</span></span> | <span data-ttu-id="775e2-137">Value</span><span class="sxs-lookup"><span data-stu-id="775e2-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="775e2-138">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="775e2-138">TAPI version</span></span><br/> | <span data-ttu-id="775e2-139">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="775e2-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="775e2-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="775e2-140">Header</span></span><br/>       | <dl> <span data-ttu-id="775e2-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="775e2-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="775e2-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="775e2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="775e2-143">**LÍNEA \_ ADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="775e2-143">**LINE\_ADDRESSSTATE**</span></span>](line-addressstate.md)
</dt> <dt>

[<span data-ttu-id="775e2-144">**LÍNEA \_ LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="775e2-144">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="775e2-145">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="775e2-145">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="775e2-146">**LINEADDRESSSTATUS**</span><span class="sxs-lookup"><span data-stu-id="775e2-146">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="775e2-147">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="775e2-147">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




