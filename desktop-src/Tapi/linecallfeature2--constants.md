---
description: En las \_ constantes LINECALLFEATURE2 se enumeran las características complementarias disponibles para las conferencias, la transferencia y las llamadas de estacionamiento.
ms.assetid: 67a3b587-dd5b-4ccf-ab69-2137604706b8
title: Constantes de LINECALLFEATURE2_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977e71f722fba34da6b2ecbd6a3e914c34a0aae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690370"
---
# <a name="linecallfeature2_-constants"></a><span data-ttu-id="8fb8d-103">Constantes de LINECALLFEATURE2 \_</span><span class="sxs-lookup"><span data-stu-id="8fb8d-103">LINECALLFEATURE2\_ Constants</span></span>

<span data-ttu-id="8fb8d-104">En las constantes **LINECALLFEATURE2 \_** se enumeran las características complementarias disponibles para las conferencias, la transferencia y las llamadas de estacionamiento.</span><span class="sxs-lookup"><span data-stu-id="8fb8d-104">The **LINECALLFEATURE2\_** constants list the supplemental features available for conferencing, transferring, and parking calls.</span></span>

<dl> <dt>

<span data-ttu-id="8fb8d-105"><span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2 \_ COMPLCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="8fb8d-105"><span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2\_COMPLCALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8fb8d-106">Si este bit está activado, se puede invocar la característica de "devolución de llamada" mediante la \_ opción de devolución de llamada LINECOMPLMODE con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span><span class="sxs-lookup"><span data-stu-id="8fb8d-106">If this bit is on, the "callback" feature can be invoked by using the LINECOMPLMODE\_CALLBACK option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="8fb8d-107">El \_ bit LINECALLFEATURE COMPLETECALL también estará activado en el miembro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="8fb8d-107">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8fb8d-108"><span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2 \_ COMPLCAMPON**</span><span class="sxs-lookup"><span data-stu-id="8fb8d-108"><span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2\_COMPLCAMPON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8fb8d-109">Si este bit está activado, se puede invocar la característica "Camp on" mediante la opción LINECOMPLMODE \_ campoN con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span><span class="sxs-lookup"><span data-stu-id="8fb8d-109">If this bit is on, the "camp on" feature can be invoked by using the LINECOMPLMODE\_CAMPON option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="8fb8d-110">El \_ bit LINECALLFEATURE COMPLETECALL también estará activado en el miembro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="8fb8d-110">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8fb8d-111"><span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2 \_ COMPLINTRUDE**</span><span class="sxs-lookup"><span data-stu-id="8fb8d-111"><span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2\_COMPLINTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8fb8d-112">Si este bit está activado, se puede invocar la característica "intrusión" mediante la opción de \_ intrusión LINECOMPLMODE con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span><span class="sxs-lookup"><span data-stu-id="8fb8d-112">If this bit is on, the "intrude" feature can be invoked by using the LINECOMPLMODE\_INTRUDE option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="8fb8d-113">El \_ bit LINECALLFEATURE COMPLETECALL también estará activado en el miembro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="8fb8d-113">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8fb8d-114"><span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2 \_ COMPLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="8fb8d-114"><span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2\_COMPLMESSAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8fb8d-115">Si este bit está activado, se puede invocar la característica "dejar mensaje" mediante la opción de \_ mensaje LINECOMPLMODE con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span><span class="sxs-lookup"><span data-stu-id="8fb8d-115">If this bit is on, the "leave message" feature can be invoked by using the LINECOMPLMODE\_MESSAGE option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="8fb8d-116">El \_ bit LINECALLFEATURE COMPLETECALL también estará activado en el miembro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="8fb8d-116">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8fb8d-117"><span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2 \_ NOHOLDCONFERENCE**</span><span class="sxs-lookup"><span data-stu-id="8fb8d-117"><span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2\_NOHOLDCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8fb8d-118">Si este bit está activado, se puede crear una "Conferencia sin celebrar" mediante la \_ opción NOHOLDCONFERENCE de LINECALLPARAMFLAGS con [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference).</span><span class="sxs-lookup"><span data-stu-id="8fb8d-118">If this bit is on, a "no hold conference" can be created by using the LINECALLPARAMFLAGS\_NOHOLDCONFERENCE option with [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference).</span></span> <span data-ttu-id="8fb8d-119">El \_ bit LINECALLFEATURE SETUPCONF también estará activado en el miembro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="8fb8d-119">The LINECALLFEATURE\_SETUPCONF bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8fb8d-120"><span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2 \_ ONESTEPTRANSFER**</span><span class="sxs-lookup"><span data-stu-id="8fb8d-120"><span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2\_ONESTEPTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8fb8d-121">Si este bit está activado, se puede crear una transferencia de un solo paso mediante la \_ opción ONESTEPTRANSFER de LINECALLPARAMFLAGS con [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span><span class="sxs-lookup"><span data-stu-id="8fb8d-121">If this bit is on, "one step transfer" can be created by using the LINECALLPARAMFLAGS\_ONESTEPTRANSFER option with [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span></span> <span data-ttu-id="8fb8d-122">El \_ bit LINECALLFEATURE SETUPTRANSFER también estará activado en el miembro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="8fb8d-122">The LINECALLFEATURE\_SETUPTRANSFER bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="8fb8d-123">Si no se especifica ninguno de los bits "COMPl" en el miembro **dwCallFeatures2** de [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , pero se \_ especifica LINECALLFEATURE COMPLETECALL, es posible que cualquiera de ellos funcione, pero el proveedor de servicios no ha especificado cuál.</span><span class="sxs-lookup"><span data-stu-id="8fb8d-123">If none of the "COMPL" bits is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_COMPLETECALL is specified, then it is possible that any of them will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="8fb8d-124"><span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2 \_ TRANSFERCONF**</span><span class="sxs-lookup"><span data-stu-id="8fb8d-124"><span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2\_TRANSFERCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8fb8d-125">Si este bit está activado, se puede usar la función [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) para resolver la transferencia como una conferencia de tres vías.</span><span class="sxs-lookup"><span data-stu-id="8fb8d-125">If this bit is on, the [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) function can be used to resolve the transfer as a three-way conference.</span></span> <span data-ttu-id="8fb8d-126">El \_ bit LINECALLFEATURE COMPLETETRANSF también estará activado en el miembro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="8fb8d-126">The LINECALLFEATURE\_COMPLETETRANSF bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8fb8d-127"><span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2 \_ TRANSFERNORM**</span><span class="sxs-lookup"><span data-stu-id="8fb8d-127"><span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2\_TRANSFERNORM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8fb8d-128">Si este bit está activado, se puede usar la función [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) para resolver la transferencia como una transferencia normal.</span><span class="sxs-lookup"><span data-stu-id="8fb8d-128">If this bit is on, the [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) function can be used to resolve the transfer as a normal transfer.</span></span> <span data-ttu-id="8fb8d-129">El \_ bit LINECALLFEATURE COMPLETETRANSF también estará activado en el miembro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="8fb8d-129">The LINECALLFEATURE\_COMPLETETRANSF bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="8fb8d-130">Si no se especifica TRANSFERNORM ni TRANSFERCONF en el miembro **dwCallFeatures2** de [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) pero \_ se especifica LINECALLFEATURE COMPLETETRANSF, es posible que funcione, pero el proveedor de servicios no ha especificado cuál.</span><span class="sxs-lookup"><span data-stu-id="8fb8d-130">If neither TRANSFERNORM nor TRANSFERCONF is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_COMPLETETRANSF is specified, then it is possible that either will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="8fb8d-131"><span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2 \_ PARKDIRECT**</span><span class="sxs-lookup"><span data-stu-id="8fb8d-131"><span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2\_PARKDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8fb8d-132">Si este bit está activado, se puede invocar la característica "estacionamiento dirigido" mediante la \_ opción dirigida LINEPARKMODE con [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span><span class="sxs-lookup"><span data-stu-id="8fb8d-132">If this bit is on, the "directed park" feature can be invoked by using the LINEPARKMODE\_DIRECTED option with [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span></span> <span data-ttu-id="8fb8d-133">El bit de estacionamiento de LINECALLFEATURE \_ también estará activado en el miembro de **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="8fb8d-133">The LINECALLFEATURE\_PARK bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8fb8d-134"><span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2 \_ PARKNONDIRECT**</span><span class="sxs-lookup"><span data-stu-id="8fb8d-134"><span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2\_PARKNONDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8fb8d-135">Si este bit está activado, se puede invocar la característica "estacionamiento no dirigido" mediante la opción LINEPARKMODE no \_ Directed con [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span><span class="sxs-lookup"><span data-stu-id="8fb8d-135">If this bit is on, the "non-directed park" feature can be invoked by using the LINEPARKMODE\_NONDIRECTED option with [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span></span> <span data-ttu-id="8fb8d-136">El bit de estacionamiento de LINECALLFEATURE \_ también estará activado en el miembro de **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="8fb8d-136">The LINECALLFEATURE\_PARK bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="8fb8d-137">Si no se especifica PARKDIRECT ni PARKNONDIRECT en el miembro **dwCallFeatures2** de [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) pero \_ se especifica LINECALLFEATURE Park, es posible que funcione, pero el proveedor de servicios no ha especificado cuál.</span><span class="sxs-lookup"><span data-stu-id="8fb8d-137">If neither PARKDIRECT nor PARKNONDIRECT is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_PARK is specified, then it is possible that either will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8fb8d-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fb8d-138">Requirements</span></span>



| <span data-ttu-id="8fb8d-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fb8d-139">Requirement</span></span> | <span data-ttu-id="8fb8d-140">Value</span><span class="sxs-lookup"><span data-stu-id="8fb8d-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8fb8d-141">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="8fb8d-141">TAPI version</span></span><br/> | <span data-ttu-id="8fb8d-142">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8fb8d-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8fb8d-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8fb8d-143">Header</span></span><br/>       | <dl> <span data-ttu-id="8fb8d-144"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fb8d-144"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fb8d-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fb8d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb8d-146">**LINECALLSTATUS**</span><span class="sxs-lookup"><span data-stu-id="8fb8d-146">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="8fb8d-147">**lineCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="8fb8d-147">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[<span data-ttu-id="8fb8d-148">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="8fb8d-148">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="8fb8d-149">**linePark**</span><span class="sxs-lookup"><span data-stu-id="8fb8d-149">**linePark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepark)
</dt> <dt>

[<span data-ttu-id="8fb8d-150">**lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="8fb8d-150">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[<span data-ttu-id="8fb8d-151">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="8fb8d-151">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




