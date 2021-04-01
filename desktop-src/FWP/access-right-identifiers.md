---
title: Acceder a los identificadores de derechos (Fwpmu. h)
description: La plataforma de filtrado de Windows (WFP) usa los derechos de acceso estándar de Win32 junto con un conjunto de derechos de acceso específicos de WFP integrados en la plataforma de filtrado.
ms.assetid: 77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c
topic_type:
- apiref
api_name:
- FWPM_ACTRL_ADD
- FWPM_ACTRL_ADD_LINK
- FWPM_ACTRL_BEGIN_READ_TXN
- FWPM_ACTRL_BEGIN_WRITE_TXN
- FWPM_ACTRL_CLASSIFY
- FWPM_ACTRL_ENUM
- FWPM_ACTRL_OPEN
- FWPM_ACTRL_READ
- FWPM_ACTRL_READ_STATS
- FWPM_ACTRL_SUBSCRIBE
- FWPM_ACTRL_WRITE
- FWPM_GENERIC_READ
- FWPM_GENERIC_EXECUTE
- FWPM_GENERIC_WRITE
- FWPM_GENERIC_ALL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af182a087ade590e278bd3dd1d2bb1a64b5c598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997063"
---
# <a name="access-right-identifiers"></a><span data-ttu-id="6774d-103">Acceder a los identificadores de derechos</span><span class="sxs-lookup"><span data-stu-id="6774d-103">Access Right Identifiers</span></span>

<span data-ttu-id="6774d-104">La plataforma de filtrado de Windows (WFP) usa los [derechos de acceso estándar de Win32](/windows/desktop/SecAuthZ/standard-access-rights) junto con un conjunto de derechos de acceso específicos de WFP integrados en la plataforma de filtrado.</span><span class="sxs-lookup"><span data-stu-id="6774d-104">Windows Filtering Platform (WFP) uses the [standard Win32 access rights](/windows/desktop/SecAuthZ/standard-access-rights) plus a set of WFP-specific access rights built into the filtering platform.</span></span> <span data-ttu-id="6774d-105">Estos derechos de acceso se usan para proteger objetos solo en modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="6774d-105">These access rights are used to secure objects in user mode only.</span></span> <span data-ttu-id="6774d-106">Los llamadores de modo kernel omiten todas las comprobaciones de acceso.</span><span class="sxs-lookup"><span data-stu-id="6774d-106">Kernel-mode callers bypass all access checks.</span></span>

<span data-ttu-id="6774d-107">Los identificadores de derechos de acceso específicos de WFP son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="6774d-107">WFP specific access right identifiers are as follows.</span></span>

<dl> <dt>

<span data-ttu-id="6774d-108"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ Add**</span><span class="sxs-lookup"><span data-stu-id="6774d-108"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM\_ACTRL\_ADD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6774d-109">Agregue un objeto al motor de filtrado de base (BFE).</span><span class="sxs-lookup"><span data-stu-id="6774d-109">Add an object to the Base Filtering Engine (BFE).</span></span> <span data-ttu-id="6774d-110">Este derecho de acceso es necesario para llamar a las funciones de [**Fwpm \* Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) .</span><span class="sxs-lookup"><span data-stu-id="6774d-110">This access right is needed in order to call [**Fwpm\*Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6774d-111"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ agregar \_ vínculo**</span><span class="sxs-lookup"><span data-stu-id="6774d-111"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM\_ACTRL\_ADD\_LINK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6774d-112">Agregue un objeto al que se hace referencia a través de un vínculo.</span><span class="sxs-lookup"><span data-stu-id="6774d-112">Add an object referenced through a link.</span></span> <span data-ttu-id="6774d-113">Por ejemplo, este derecho de acceso es necesario para las llamadas a las que se hace referencia a través de GUID.</span><span class="sxs-lookup"><span data-stu-id="6774d-113">For example, this access right is needed for callouts referenced through GUIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6774d-114"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Read \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="6774d-114"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM\_ACTRL\_BEGIN\_READ\_TXN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6774d-115">Comienza una transacción de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6774d-115">Begin a read-only transaction.</span></span> <span data-ttu-id="6774d-116">Este derecho de acceso es necesario para llamar a [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).</span><span class="sxs-lookup"><span data-stu-id="6774d-116">This access right is needed in order to call [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6774d-117"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Write \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="6774d-117"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6774d-118">Comienza una transacción de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="6774d-118">Begin a read/write transaction.</span></span> <span data-ttu-id="6774d-119">Este derecho de acceso es necesario para llamar a [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) para una transacción de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="6774d-119">This access right is needed in order to call [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) for a read/write transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6774d-120"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_clasificación de ACTRL de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="6774d-120"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM\_ACTRL\_CLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6774d-121">Clasifique llamada a procedimiento remoto (RPC).</span><span class="sxs-lookup"><span data-stu-id="6774d-121">Classify Remote Procedure Call (RPC).</span></span> <span data-ttu-id="6774d-122">Este derecho de acceso es necesario para el tiempo de ejecución de RPC con el fin de aplicar los filtros RPC.</span><span class="sxs-lookup"><span data-stu-id="6774d-122">This access right is needed by the RPC run-time in order to enforce RPC filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6774d-123"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL ( \_ enumeración)**</span><span class="sxs-lookup"><span data-stu-id="6774d-123"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM\_ACTRL\_ENUM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6774d-124">Enumerar.</span><span class="sxs-lookup"><span data-stu-id="6774d-124">Enumerate.</span></span> <span data-ttu-id="6774d-125">Este derecho de acceso es necesario para llamar a las funciones de [**Fwpm \* CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) .</span><span class="sxs-lookup"><span data-stu-id="6774d-125">This access right is needed in order to call [**Fwpm\*CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) functions.</span></span> <span data-ttu-id="6774d-126">Para enumerar un objeto, el llamador también necesita el \_ acceso de lectura de FWPM ACTRL \_ al objeto.</span><span class="sxs-lookup"><span data-stu-id="6774d-126">To enumerate an object, the caller also needs FWPM\_ACTRL\_READ access to the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6774d-127"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ Open**</span><span class="sxs-lookup"><span data-stu-id="6774d-127"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM\_ACTRL\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6774d-128">Abra una sesión en el motor de filtro.</span><span class="sxs-lookup"><span data-stu-id="6774d-128">Open a session to the filter engine.</span></span> <span data-ttu-id="6774d-129">Este derecho de acceso es necesario para llamar a [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span><span class="sxs-lookup"><span data-stu-id="6774d-129">This access right is needed in order to call [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6774d-130"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ lectura**</span><span class="sxs-lookup"><span data-stu-id="6774d-130"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM\_ACTRL\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6774d-131">Lectura.</span><span class="sxs-lookup"><span data-stu-id="6774d-131">Read.</span></span> <span data-ttu-id="6774d-132">Este derecho de acceso es necesario para llamar a las funciones [**Fwpm \* GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) y [**Fwpm \* GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) .</span><span class="sxs-lookup"><span data-stu-id="6774d-132">This access right is needed in order to call [**Fwpm\*GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) and [**Fwpm\*GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6774d-133"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM \_ ACTRL \_ leer \_ estadísticas**</span><span class="sxs-lookup"><span data-stu-id="6774d-133"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM\_ACTRL\_READ\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6774d-134">Leer estadísticas.</span><span class="sxs-lookup"><span data-stu-id="6774d-134">Read statistics.</span></span> <span data-ttu-id="6774d-135">Este derecho de acceso es necesario para llamar a [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) y [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).</span><span class="sxs-lookup"><span data-stu-id="6774d-135">This access right is needed in order to call [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) and [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6774d-136"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**suscripción a FWPM \_ ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="6774d-136"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM\_ACTRL\_SUBSCRIBE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6774d-137">Suscríbase.</span><span class="sxs-lookup"><span data-stu-id="6774d-137">Subscribe.</span></span> <span data-ttu-id="6774d-138">Este derecho de acceso es necesario para llamar a las funciones de [**Fwpm \* SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) .</span><span class="sxs-lookup"><span data-stu-id="6774d-138">This access right is needed in order to call [**Fwpm\*SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) functions.</span></span> <span data-ttu-id="6774d-139">Para recibir una notificación de un objeto, un suscriptor también necesita \_ el acceso de lectura de FWPM ACTRL \_ al objeto.</span><span class="sxs-lookup"><span data-stu-id="6774d-139">To receive a notification for an object, a subscriber also needs FWPM\_ACTRL\_READ access to the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6774d-140"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ Write**</span><span class="sxs-lookup"><span data-stu-id="6774d-140"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM\_ACTRL\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6774d-141">Opciones del motor de escritura.</span><span class="sxs-lookup"><span data-stu-id="6774d-141">Write engine options.</span></span> <span data-ttu-id="6774d-142">Este derecho de acceso es necesario para llamar a [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).</span><span class="sxs-lookup"><span data-stu-id="6774d-142">This access right is needed in order to call [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6774d-143"><span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**\_lectura genérica \_ FWPM**</span><span class="sxs-lookup"><span data-stu-id="6774d-143"><span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**FWPM\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6774d-144">STANDARD \_ Rights \_ Read \| FWPM \_ ACTRL \_ Begin \_ Read \_ TXN \| FWPM \_ ACTRL \_ clasifique \| FWPM \_ ACTRL \_ Open \| FWPM \_ ACTRL \_ Read \| FWPM \_ ACTRL \_ Read \_ stats</span><span class="sxs-lookup"><span data-stu-id="6774d-144">STANDARD\_RIGHTS\_READ \| FWPM\_ACTRL\_BEGIN\_READ\_TXN \| FWPM\_ACTRL\_CLASSIFY \| FWPM\_ACTRL\_OPEN \| FWPM\_ACTRL\_READ \| FWPM\_ACTRL\_READ\_STATS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6774d-145"><span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**\_ejecución genérica de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="6774d-145"><span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**FWPM\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6774d-146">\_derechos estándar \_ Execute \| FWPM \_ ACTRL \_ enum \| FWPM \_ ACTRL \_ subscribe</span><span class="sxs-lookup"><span data-stu-id="6774d-146">STANDARD\_RIGHTS\_EXECUTE \| FWPM\_ACTRL\_ENUM \| FWPM\_ACTRL\_SUBSCRIBE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6774d-147"><span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**\_escritura genérica de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="6774d-147"><span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**FWPM\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6774d-148">STANDARD \_ Rights \_ Write \| Delete \| FWPM \_ ACTRL \_ agregar \| FWPM \_ ACTRL \_ Add \_ Link \| FWPM \_ ACTRL \_ Begin \_ Write \_ TXN \| FWPM \_ ACTRL \_ Write</span><span class="sxs-lookup"><span data-stu-id="6774d-148">STANDARD\_RIGHTS\_WRITE \| DELETE \| FWPM\_ACTRL\_ADD \| FWPM\_ACTRL\_ADD\_LINK \| FWPM\_ACTRL\_BEGIN\_WRITE\_TXN \| FWPM\_ACTRL\_WRITE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6774d-149"><span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM \_ genérico \_ todo**</span><span class="sxs-lookup"><span data-stu-id="6774d-149"><span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM\_GENERIC\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6774d-150">\_derechos estándar \_ obligatorios \| FWPM \_ ACTRL \_ agregar \| FWPM \_ ACTRL \_ Add \_ Link \| FWPM \_ ACTRL \_ Begin \_ Read \_ TXN FWPM \| \_ ACTRL \_ Begin \_ Write \_ TXN \| FWPM \_ ACTRL \_ clasifique \| FWPM \_ ACTRL \_ enum \| FWPM \_ ACTRL \_ Open \| FWPM \_ ACTRL \_ Read \| FWPM \_ ACTRL \_ Read \_ stats \| FWPM ACTRL \_ \_ subscribe FWPM ACTRL \| \_ \_ Write</span><span class="sxs-lookup"><span data-stu-id="6774d-150">STANDARD\_RIGHTS\_REQUIRED \| FWPM\_ACTRL\_ADD \| FWPM\_ACTRL\_ADD\_LINK \| FWPM\_ACTRL\_BEGIN\_READ\_TXN \| FWPM\_ACTRL\_BEGIN\_WRITE\_TXN \| FWPM\_ACTRL\_CLASSIFY \| FWPM\_ACTRL\_ENUM \| FWPM\_ACTRL\_OPEN \| FWPM\_ACTRL\_READ \| FWPM\_ACTRL\_READ\_STATS \| FWPM\_ACTRL\_SUBSCRIBE \| FWPM\_ACTRL\_WRITE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6774d-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6774d-151">Requirements</span></span>



| <span data-ttu-id="6774d-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="6774d-152">Requirement</span></span> | <span data-ttu-id="6774d-153">Value</span><span class="sxs-lookup"><span data-stu-id="6774d-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6774d-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6774d-154">Minimum supported client</span></span><br/> | <span data-ttu-id="6774d-155">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6774d-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6774d-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6774d-156">Minimum supported server</span></span><br/> | <span data-ttu-id="6774d-157">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6774d-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6774d-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6774d-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="6774d-159"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="6774d-159"><dt>Fwpmu.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6774d-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="6774d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6774d-161">Modelo de Access Control de plataforma de filtrado de Windows</span><span class="sxs-lookup"><span data-stu-id="6774d-161">Windows Filtering Platform Access Control Model</span></span>](access-control.md)
</dt> <dt>

[<span data-ttu-id="6774d-162">Derechos de acceso estándar</span><span class="sxs-lookup"><span data-stu-id="6774d-162">Standard Access Rights</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

