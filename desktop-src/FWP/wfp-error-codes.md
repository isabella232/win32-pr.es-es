---
title: Códigos de error de WFP (Winerror.h)
description: Códigos de error específicos de (WFP).
ms.assetid: 11f3085a-f044-4a78-b47a-59b9086562bf
topic_type:
- apiref
api_name:
- FWP_E_CALLOUT_NOT_FOUND
- FWP_E_CONDITION_NOT_FOUND
- FWP_E_FILTER_NOT_FOUND
- FWP_E_LAYER_NOT_FOUND
- FWP_E_PROVIDER_NOT_FOUND
- FWP_E_PROVIDER_CONTEXT_NOT_FOUND
- FWP_E_SUBLAYER_NOT_FOUND
- FWP_E_NOT_FOUND
- FWP_E_ALREADY_EXISTS
- FWP_E_IN_USE
- FWP_E_DYNAMIC_SESSION_IN_PROGRESS
- FWP_E_WRONG_SESSION
- FWP_E_NO_TXN_IN_PROGRESS
- FWP_E_TXN_IN_PROGRESS
- FWP_E_TXN_ABORTED
- FWP_E_SESSION_ABORTED
- FWP_E_INCOMPATIBLE_TXN
- FWP_E_TIMEOUT
- FWP_E_NET_EVENTS_DISABLED
- FWP_E_INCOMPATIBLE_LAYER
- FWP_E_KM_CLIENTS_ONLY
- FWP_E_LIFETIME_MISMATCH
- FWP_E_BUILTIN_OBJECT
- FWP_E_TOO_MANY_CALLOUTS
- FWP_E_NOTIFICATION_DROPPED
- FWP_E_TRAFFIC_MISMATCH
- FWP_E_INCOMPATIBLE_SA_STATE
- FWP_E_NULL_POINTER
- FWP_E_INVALID_ENUMERATOR
- FWP_E_INVALID_FLAGS
- FWP_E_INVALID_NET_MASK
- FWP_E_INVALID_RANGE
- FWP_E_INVALID_INTERVAL
- FWP_E_ZERO_LENGTH_ARRAY
- FWP_E_NULL_DISPLAY_NAME
- FWP_E_INVALID_ACTION_TYPE
- FWP_E_INVALID_WEIGHT
- FWP_E_MATCH_TYPE_MISMATCH
- FWP_E_TYPE_MISMATCH
- FWP_E_OUT_OF_BOUNDS
- FWP_E_RESERVED
- FWP_E_DUPLICATE_CONDITION
- FWP_E_DUPLICATE_KEYMOD
- FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER
- FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT
- FWP_E_INCOMPATIBLE_AUTH_METHOD
- FWP_E_INCOMPATIBLE_DH_GROUP
- FWP_E_EM_NOT_SUPPORTED
- FWP_E_NEVER_MATCH
- FWP_E_PROVIDER_CONTEXT_MISMATCH
- FWP_E_INVALID_PARAMETER
- FWP_E_TOO_MANY_SUBLAYERS
- FWP_E_CALLOUT_NOTIFICATION_FAILED
- FWP_E_INVALID_AUTH_TRANSFORM
- FWP_E_INVALID_CIPHER_TRANSFORM
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a0e7ee1ab0364a31f136f0c0cdbf87f459225b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491728"
---
# <a name="wfp-error-codes"></a><span data-ttu-id="f0b97-103">Códigos de error de WFP</span><span class="sxs-lookup"><span data-stu-id="f0b97-103">WFP Error Codes</span></span>

<span data-ttu-id="f0b97-104">Los códigos de error específicos de la plataforma de filtrado de Windows (WFP) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="f0b97-104">Windows Filtering Platform (WFP) specific error codes are as follows.</span></span>

<dl> <dt>

<span data-ttu-id="f0b97-105"><span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**\_ \_ \_ no \_ se encontró el FWP E llamada**</span><span class="sxs-lookup"><span data-stu-id="f0b97-105"><span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**FWP\_E\_CALLOUT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-106">0x80320001</span><span class="sxs-lookup"><span data-stu-id="f0b97-106">0x80320001</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-107">La llamada no existe.</span><span class="sxs-lookup"><span data-stu-id="f0b97-107">The callout does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-108"><span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**\_ \_ \_ no \_ se encontró la condición de FWP E**</span><span class="sxs-lookup"><span data-stu-id="f0b97-108"><span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**FWP\_E\_CONDITION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-109">0x80320002</span><span class="sxs-lookup"><span data-stu-id="f0b97-109">0x80320002</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-110">La condición de filtro no existe.</span><span class="sxs-lookup"><span data-stu-id="f0b97-110">The filter condition does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-111"><span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**\_ \_ \_ no \_ se encontró el filtro de FWP E**</span><span class="sxs-lookup"><span data-stu-id="f0b97-111"><span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**FWP\_E\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-112">0x80320003</span><span class="sxs-lookup"><span data-stu-id="f0b97-112">0x80320003</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-113">El filtro no existe.</span><span class="sxs-lookup"><span data-stu-id="f0b97-113">The filter does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-114"><span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**\_ \_ \_ no \_ se encontró el nivel de FWP E**</span><span class="sxs-lookup"><span data-stu-id="f0b97-114"><span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**FWP\_E\_LAYER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-115">0x80320004</span><span class="sxs-lookup"><span data-stu-id="f0b97-115">0x80320004</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-116">La capa no existe.</span><span class="sxs-lookup"><span data-stu-id="f0b97-116">The layer does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-117"><span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**\_ \_ \_ no \_ se encontró el proveedor de FWP E**</span><span class="sxs-lookup"><span data-stu-id="f0b97-117"><span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**FWP\_E\_PROVIDER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-118">0x80320005</span><span class="sxs-lookup"><span data-stu-id="f0b97-118">0x80320005</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-119">El proveedor no existe.</span><span class="sxs-lookup"><span data-stu-id="f0b97-119">The provider does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-120"><span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**\_ \_ \_ \_ no se encontró el contexto \_ del proveedor de FWP E**</span><span class="sxs-lookup"><span data-stu-id="f0b97-120"><span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**FWP\_E\_PROVIDER\_CONTEXT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-121">0x80320006</span><span class="sxs-lookup"><span data-stu-id="f0b97-121">0x80320006</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-122">El contexto del proveedor no existe.</span><span class="sxs-lookup"><span data-stu-id="f0b97-122">The provider context does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-123"><span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**\_ \_ \_ no \_ se encontró el subnivel de FWP E**</span><span class="sxs-lookup"><span data-stu-id="f0b97-123"><span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**FWP\_E\_SUBLAYER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-124">0x80320007</span><span class="sxs-lookup"><span data-stu-id="f0b97-124">0x80320007</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-125">La subcapa no existe.</span><span class="sxs-lookup"><span data-stu-id="f0b97-125">The sub-layer does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-126"><span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**\_ \_ no \_ se encontró el FWP E**</span><span class="sxs-lookup"><span data-stu-id="f0b97-126"><span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**FWP\_E\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-127">0x80320008</span><span class="sxs-lookup"><span data-stu-id="f0b97-127">0x80320008</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-128">El objeto no existe.</span><span class="sxs-lookup"><span data-stu-id="f0b97-128">The object does not exist.</span></span>

<span data-ttu-id="f0b97-129">Las [funciones \* IPsecSaContext](fwp-ipsec-functions.md) devuelven este error si no se encuentra el identificador de contexto de SA.</span><span class="sxs-lookup"><span data-stu-id="f0b97-129">The [IPsecSaContext\*](fwp-ipsec-functions.md) functions return this error if the SA context ID is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-130"><span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**el FWP \_ E \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="f0b97-130"><span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**FWP\_E\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-131">0x80320009</span><span class="sxs-lookup"><span data-stu-id="f0b97-131">0x80320009</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-132">Ya existe un objeto con ese GUID o LUID.</span><span class="sxs-lookup"><span data-stu-id="f0b97-132">An object with that GUID or LUID already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-133"><span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**FWP \_ E \_ en \_ uso**</span><span class="sxs-lookup"><span data-stu-id="f0b97-133"><span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**FWP\_E\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-134">0x8032000A</span><span class="sxs-lookup"><span data-stu-id="f0b97-134">0x8032000A</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-135">Otros objetos hacen referencia al objeto, por lo que no se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="f0b97-135">The object is referenced by other objects, so it cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-136"><span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**\_ \_ sesión dinámica de FWP E \_ \_ en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="f0b97-136"><span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**FWP\_E\_DYNAMIC\_SESSION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-137">0x8032000B</span><span class="sxs-lookup"><span data-stu-id="f0b97-137">0x8032000B</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-138">No se permite la llamada desde dentro de una sesión dinámica.</span><span class="sxs-lookup"><span data-stu-id="f0b97-138">The call is not allowed from within a dynamic session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-139"><span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**sesión de FWP \_ E \_ incorrecta \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-139"><span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**FWP\_E\_WRONG\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-140">0x8032000C</span><span class="sxs-lookup"><span data-stu-id="f0b97-140">0x8032000C</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-141">La llamada se realizó desde una sesión incorrecta, por lo que no se puede completar.</span><span class="sxs-lookup"><span data-stu-id="f0b97-141">The call was made from the wrong session, so it cannot be completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-142"><span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**FWP \_ E \_ no \_ TXN \_ en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="f0b97-142"><span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**FWP\_E\_NO\_TXN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-143">0x8032000D</span><span class="sxs-lookup"><span data-stu-id="f0b97-143">0x8032000D</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-144">La llamada se debe realizar desde una transacción explícita.</span><span class="sxs-lookup"><span data-stu-id="f0b97-144">The call must be made from within an explicit transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-145"><span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**FWP \_ E \_ TXN \_ en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="f0b97-145"><span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**FWP\_E\_TXN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-146">0x8032000E</span><span class="sxs-lookup"><span data-stu-id="f0b97-146">0x8032000E</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-147">No se permite la llamada desde dentro de una transacción explícita.</span><span class="sxs-lookup"><span data-stu-id="f0b97-147">The call is not allowed from within an explicit transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-148"><span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**FWP \_ E \_ TXN \_ anulado**</span><span class="sxs-lookup"><span data-stu-id="f0b97-148"><span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**FWP\_E\_TXN\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-149">0x8032000F</span><span class="sxs-lookup"><span data-stu-id="f0b97-149">0x8032000F</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-150">Se ha cancelado la transacción explícita.</span><span class="sxs-lookup"><span data-stu-id="f0b97-150">The explicit transaction has been forcibly canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-151"><span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**se \_ \_ anuló la sesión \_ de FWP E**</span><span class="sxs-lookup"><span data-stu-id="f0b97-151"><span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**FWP\_E\_SESSION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-152">0x80320010</span><span class="sxs-lookup"><span data-stu-id="f0b97-152">0x80320010</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-153">Se ha cancelado la sesión.</span><span class="sxs-lookup"><span data-stu-id="f0b97-153">The session has been canceled.</span></span>

<span data-ttu-id="f0b97-154">El identificador de sesión debe cerrarse llamando a [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0), aunque ya no sea válido. de lo contrario, se filtrará el estado del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="f0b97-154">The session handle needs to be closed by calling [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0), even though it is no longer valid; otherwise, the client-side state will be leaked.</span></span> <span data-ttu-id="f0b97-155">Se debe crear una nueva sesión mediante una llamada a [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span><span class="sxs-lookup"><span data-stu-id="f0b97-155">A new session should be created by calling [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-156"><span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**\_ \_ TXN incompatible de FWP E incompatible \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-156"><span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**FWP\_E\_INCOMPATIBLE\_TXN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-157">0x80320011</span><span class="sxs-lookup"><span data-stu-id="f0b97-157">0x80320011</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-158">No se permite la llamada desde una transacción de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f0b97-158">The call is not allowed from within a read-only transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-159"><span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**tiempo de espera de FWP \_ E \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-159"><span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**FWP\_E\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-160">0x80320012</span><span class="sxs-lookup"><span data-stu-id="f0b97-160">0x80320012</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-161">Se agotó el tiempo de espera de la llamada mientras se esperaba a adquirir el bloqueo de la transacción.</span><span class="sxs-lookup"><span data-stu-id="f0b97-161">The call timed out while waiting to acquire the transaction lock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-162"><span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**\_eventos net de FWP E \_ \_ \_ deshabilitados**</span><span class="sxs-lookup"><span data-stu-id="f0b97-162"><span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**FWP\_E\_NET\_EVENTS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-163">0x80320013</span><span class="sxs-lookup"><span data-stu-id="f0b97-163">0x80320013</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-164">La colección de eventos de diagnóstico de red está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="f0b97-164">The collection of network diagnostic events is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-165"><span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**nivel de FWP \_ E \_ incompatible \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-165"><span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**FWP\_E\_INCOMPATIBLE\_LAYER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-166">0x80320014</span><span class="sxs-lookup"><span data-stu-id="f0b97-166">0x80320014</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-167">La capa especificada no admite la operación.</span><span class="sxs-lookup"><span data-stu-id="f0b97-167">The operation is not supported by the specified layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-168"><span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**solo clientes de FWP \_ E \_ km \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-168"><span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**FWP\_E\_KM\_CLIENTS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-169">0x80320015</span><span class="sxs-lookup"><span data-stu-id="f0b97-169">0x80320015</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-170">Solo se permite la llamada a los autores de llamadas en modo kernel.</span><span class="sxs-lookup"><span data-stu-id="f0b97-170">The call is allowed for kernel-mode callers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-171"><span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**\_ \_ duración \_ no coincidente de FWP E**</span><span class="sxs-lookup"><span data-stu-id="f0b97-171"><span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**FWP\_E\_LIFETIME\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-172">0x80320016</span><span class="sxs-lookup"><span data-stu-id="f0b97-172">0x80320016</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-173">La llamada intentó asociar dos objetos con duraciones incompatibles.</span><span class="sxs-lookup"><span data-stu-id="f0b97-173">The call tried to associate two objects with incompatible lifetimes.</span></span>

<span data-ttu-id="f0b97-174">Vea [Administración de objetos](object-management.md) para obtener más información sobre la duración de los objetos y la Asociación de objetos.</span><span class="sxs-lookup"><span data-stu-id="f0b97-174">See [Object Management](object-management.md) for more information on object lifetime and object association.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-175"><span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**FWP \_ E \_ Builtin ( \_ objeto)**</span><span class="sxs-lookup"><span data-stu-id="f0b97-175"><span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**FWP\_E\_BUILTIN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-176">0x80320017</span><span class="sxs-lookup"><span data-stu-id="f0b97-176">0x80320017</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-177">El objeto está integrado, por lo que no se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="f0b97-177">The object is built-in, so it cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-178"><span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**FWP \_ E \_ demasiadas \_ \_ llamadas**</span><span class="sxs-lookup"><span data-stu-id="f0b97-178"><span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**FWP\_E\_TOO\_MANY\_CALLOUTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-179">0x80320018</span><span class="sxs-lookup"><span data-stu-id="f0b97-179">0x80320018</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-180">Se ha alcanzado el número máximo de llamadas.</span><span class="sxs-lookup"><span data-stu-id="f0b97-180">The maximum number of callouts has been reached.</span></span>

<span data-ttu-id="f0b97-181">Como máximo, se pueden registrar 100.000 llamadas al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f0b97-181">At most, 100,000 callouts can be registered at the same time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-182"><span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**se \_ \_ quitó la notificación de FWP E \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-182"><span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**FWP\_E\_NOTIFICATION\_DROPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-183">0x80320019</span><span class="sxs-lookup"><span data-stu-id="f0b97-183">0x80320019</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-184">No se pudo entregar una notificación porque una cola de mensajes está a su capacidad máxima.</span><span class="sxs-lookup"><span data-stu-id="f0b97-184">A notification could not be delivered because a message queue is at its maximum capacity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-185"><span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**el \_ tráfico de FWP E \_ \_ no coincide**</span><span class="sxs-lookup"><span data-stu-id="f0b97-185"><span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**FWP\_E\_TRAFFIC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-186">0x8032001A</span><span class="sxs-lookup"><span data-stu-id="f0b97-186">0x8032001A</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-187">Los parámetros de tráfico de red no coinciden con los del contexto de la Asociación de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f0b97-187">The network traffic parameters do not match those for the security association context.</span></span>

<span data-ttu-id="f0b97-188">Se puede llamar a [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) varias veces, pero el autor de la llamada debe especificar el mismo [**\_ TRAFFIC0 de IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) cada vez.</span><span class="sxs-lookup"><span data-stu-id="f0b97-188">[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) can be called multiple times, but the caller must specify the same [**IPSEC\_TRAFFIC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) each time.</span></span> <span data-ttu-id="f0b97-189">Se devuelve este error si una llamada subsiguiente proporciona un **\_ TRAFFIC0 de IPSec** diferente.</span><span class="sxs-lookup"><span data-stu-id="f0b97-189">This error is returned if a subsequent call supplies a different **IPSEC\_TRAFFIC0**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-190"><span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**\_Estado de \_ SA incompatible de FWP E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-190"><span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**FWP\_E\_INCOMPATIBLE\_SA\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-191">0x8032001B</span><span class="sxs-lookup"><span data-stu-id="f0b97-191">0x8032001B</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-192">La llamada no está permitida para el estado de la Asociación de seguridad (SA) actual.</span><span class="sxs-lookup"><span data-stu-id="f0b97-192">The call is not allowed for the current security association (SA) state.</span></span>

<span data-ttu-id="f0b97-193">Las funciones de contexto SA deben llamarse en un orden específico:</span><span class="sxs-lookup"><span data-stu-id="f0b97-193">The SA context functions must be called in a specific order:</span></span>

-   [<span data-ttu-id="f0b97-194">**IPsecSaContextCreate0**</span><span class="sxs-lookup"><span data-stu-id="f0b97-194">**IPsecSaContextCreate0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)
-   [<span data-ttu-id="f0b97-195">**IPsecSaContextGetSpi0**</span><span class="sxs-lookup"><span data-stu-id="f0b97-195">**IPsecSaContextGetSpi0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)
-   [<span data-ttu-id="f0b97-196">**IPsecSaContextAddInbound0**</span><span class="sxs-lookup"><span data-stu-id="f0b97-196">**IPsecSaContextAddInbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)
-   [<span data-ttu-id="f0b97-197">**IPsecSaContextAddOutbound0**</span><span class="sxs-lookup"><span data-stu-id="f0b97-197">**IPsecSaContextAddOutbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)

<span data-ttu-id="f0b97-198">Se devuelve este error si se llama fuera de orden.</span><span class="sxs-lookup"><span data-stu-id="f0b97-198">This error is returned if they are called out of order.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-199"><span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**\_ \_ puntero nulo de FWP E \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-199"><span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**FWP\_E\_NULL\_POINTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-200">0x8032001C</span><span class="sxs-lookup"><span data-stu-id="f0b97-200">0x8032001C</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-201">Un puntero requerido es NULL.</span><span class="sxs-lookup"><span data-stu-id="f0b97-201">A required pointer is null.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-202"><span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**\_enumerador de FWP E \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-202"><span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**FWP\_E\_INVALID\_ENUMERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-203">0x8032001D</span><span class="sxs-lookup"><span data-stu-id="f0b97-203">0x8032001D</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-204">Un valor de enumerador de una estructura está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="f0b97-204">An enumerator value in a structure is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-205"><span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**\_ \_ marcas no válidas de FWP E \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-205"><span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**FWP\_E\_INVALID\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-206">0x8032001E</span><span class="sxs-lookup"><span data-stu-id="f0b97-206">0x8032001E</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-207">El campo Flags contiene un valor no válido.</span><span class="sxs-lookup"><span data-stu-id="f0b97-207">The flags field contains an invalid value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-208"><span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**\_máscara de \_ red no válida de FWP E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-208"><span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**FWP\_E\_INVALID\_NET\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-209">0x8032001F</span><span class="sxs-lookup"><span data-stu-id="f0b97-209">0x8032001F</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-210">Una máscara de red no es válida.</span><span class="sxs-lookup"><span data-stu-id="f0b97-210">A network mask is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-211"><span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**\_ \_ rango no válido de FWP E \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-211"><span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**FWP\_E\_INVALID\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-212">0x80320020</span><span class="sxs-lookup"><span data-stu-id="f0b97-212">0x80320020</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-213">Una estructura de [**FWP \_ RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0) no es válida.</span><span class="sxs-lookup"><span data-stu-id="f0b97-213">An [**FWP\_RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0) structure is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-214"><span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**\_ \_ intervalo no válido de FWP E \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-214"><span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**FWP\_E\_INVALID\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-215">0x80320021</span><span class="sxs-lookup"><span data-stu-id="f0b97-215">0x80320021</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-216">El intervalo de tiempo no es válido.</span><span class="sxs-lookup"><span data-stu-id="f0b97-216">The time interval is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-217"><span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**\_matriz de \_ longitud de cero \_ \_ de FWP**</span><span class="sxs-lookup"><span data-stu-id="f0b97-217"><span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**FWP\_E\_ZERO\_LENGTH\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-218">0x80320022</span><span class="sxs-lookup"><span data-stu-id="f0b97-218">0x80320022</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-219">Una matriz que debe contener al menos un elemento tiene una longitud cero.</span><span class="sxs-lookup"><span data-stu-id="f0b97-219">An array that must contain at least one element has zero length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-220"><span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**nombre para mostrar de FWP \_ E \_ null \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-220"><span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**FWP\_E\_NULL\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-221">0x80320023</span><span class="sxs-lookup"><span data-stu-id="f0b97-221">0x80320023</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-222">El campo **displayData.Name** no puede ser null.</span><span class="sxs-lookup"><span data-stu-id="f0b97-222">The **displayData.name** field cannot be null.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-223"><span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**\_tipo de \_ acción no válido de FWP E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-223"><span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**FWP\_E\_INVALID\_ACTION\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-224">0x80320024</span><span class="sxs-lookup"><span data-stu-id="f0b97-224">0x80320024</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-225">El tipo de acción no es ninguno de los tipos de acción permitidos para un filtro.</span><span class="sxs-lookup"><span data-stu-id="f0b97-225">The action type is not one of the allowed action types for a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-226"><span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**\_ \_ peso no válido de FWP E \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-226"><span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**FWP\_E\_INVALID\_WEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-227">0x80320025</span><span class="sxs-lookup"><span data-stu-id="f0b97-227">0x80320025</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-228">El peso del filtro no es válido.</span><span class="sxs-lookup"><span data-stu-id="f0b97-228">The filter weight is not valid.</span></span>

<span data-ttu-id="f0b97-229">Para obtener más información, vea [asignación de pesos de filtro](filter-weight-assignment.md) .</span><span class="sxs-lookup"><span data-stu-id="f0b97-229">See [Filter Weight Assignment](filter-weight-assignment.md) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-230"><span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**\_ \_ \_ no coinciden los tipos de coincidencia de FWP E \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-230"><span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**FWP\_E\_MATCH\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-231">0x80320026</span><span class="sxs-lookup"><span data-stu-id="f0b97-231">0x80320026</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-232">Una condición de filtro contiene un tipo de coincidencia que no es compatible con los operandos.</span><span class="sxs-lookup"><span data-stu-id="f0b97-232">A filter condition contains a match type that is not compatible with the operands.</span></span>

<span data-ttu-id="f0b97-233">Consulte [**\_ \_ tipo de coincidencia de FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f0b97-233">See [**FWP\_MATCH\_TYPE**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-234"><span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**error \_ de \_ coincidencia de tipo de FWP E \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-234"><span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**FWP\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-235">0x80320027</span><span class="sxs-lookup"><span data-stu-id="f0b97-235">0x80320027</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-236">Una estructura de [**FWP \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0) o una estructura VALUE0 de la [**\_ \_ condición FWPM**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0) es de tipo incorrecto.</span><span class="sxs-lookup"><span data-stu-id="f0b97-236">An [**FWP\_VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0) structure or an [**FWPM\_CONDITION\_VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0) structure is of the wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-237"><span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**FWP \_ E \_ fuera \_ de los \_ límites**</span><span class="sxs-lookup"><span data-stu-id="f0b97-237"><span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**FWP\_E\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-238">0x80320028</span><span class="sxs-lookup"><span data-stu-id="f0b97-238">0x80320028</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-239">Un valor entero está fuera del intervalo permitido.</span><span class="sxs-lookup"><span data-stu-id="f0b97-239">An integer value is outside the allowed range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-240"><span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**FWP \_ E \_ reservado**</span><span class="sxs-lookup"><span data-stu-id="f0b97-240"><span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**FWP\_E\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-241">0x80320029</span><span class="sxs-lookup"><span data-stu-id="f0b97-241">0x80320029</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-242">Un campo reservado es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="f0b97-242">A reserved field is nonzero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-243"><span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**\_ \_ condición duplicada de FWP E \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-243"><span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**FWP\_E\_DUPLICATE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-244">0x8032002A</span><span class="sxs-lookup"><span data-stu-id="f0b97-244">0x8032002A</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-245">Un filtro no puede contener varias condiciones que operan en un único campo.</span><span class="sxs-lookup"><span data-stu-id="f0b97-245">A filter cannot contain multiple conditions operating on a single field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-246"><span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**\_ \_ KEYMOD duplicado de FWP E \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-246"><span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**FWP\_E\_DUPLICATE\_KEYMOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-247">0x8032002B</span><span class="sxs-lookup"><span data-stu-id="f0b97-247">0x8032002B</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-248">Una directiva no puede contener el mismo módulo de creación de claves más de una vez.</span><span class="sxs-lookup"><span data-stu-id="f0b97-248">A policy cannot contain the same keying module more than once.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-249"><span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**\_ \_ acción de FWP E \_ incompatible \_ con el \_ nivel**</span><span class="sxs-lookup"><span data-stu-id="f0b97-249"><span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**FWP\_E\_ACTION\_INCOMPATIBLE\_WITH\_LAYER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-250">0x8032002C</span><span class="sxs-lookup"><span data-stu-id="f0b97-250">0x8032002C</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-251">El tipo de acción no es compatible con la capa.</span><span class="sxs-lookup"><span data-stu-id="f0b97-251">The action type is not compatible with the layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-252"><span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**\_ \_ acción de FWP E \_ incompatible \_ con \_ subcapa**</span><span class="sxs-lookup"><span data-stu-id="f0b97-252"><span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**FWP\_E\_ACTION\_INCOMPATIBLE\_WITH\_SUBLAYER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-253">0x8032002D</span><span class="sxs-lookup"><span data-stu-id="f0b97-253">0x8032002D</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-254">El tipo de acción no es compatible con la subcapa.</span><span class="sxs-lookup"><span data-stu-id="f0b97-254">The action type is not compatible with the sub-layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-255"><span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**\_ \_ contexto de FWP E \_ incompatible \_ con el \_ nivel**</span><span class="sxs-lookup"><span data-stu-id="f0b97-255"><span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**FWP\_E\_CONTEXT\_INCOMPATIBLE\_WITH\_LAYER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-256">0x8032002E</span><span class="sxs-lookup"><span data-stu-id="f0b97-256">0x8032002E</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-257">El contexto sin formato o el contexto del proveedor no es compatible con la capa.</span><span class="sxs-lookup"><span data-stu-id="f0b97-257">The raw context or the provider context is not compatible with the layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-258"><span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**\_ \_ contexto de FWP E \_ incompatible \_ con la \_ llamada**</span><span class="sxs-lookup"><span data-stu-id="f0b97-258"><span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**FWP\_E\_CONTEXT\_INCOMPATIBLE\_WITH\_CALLOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-259">0x8032002F</span><span class="sxs-lookup"><span data-stu-id="f0b97-259">0x8032002F</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-260">El contexto sin formato o el contexto del proveedor no es compatible con la llamada.</span><span class="sxs-lookup"><span data-stu-id="f0b97-260">The raw context or the provider context is not compatible with the callout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-261"><span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**método de autenticación de FWP \_ E \_ incompatible \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-261"><span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**FWP\_E\_INCOMPATIBLE\_AUTH\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-262">0x80320030</span><span class="sxs-lookup"><span data-stu-id="f0b97-262">0x80320030</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-263">El método de autenticación no es compatible con el tipo de directiva.</span><span class="sxs-lookup"><span data-stu-id="f0b97-263">The authentication method is not compatible with the policy type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-264"><span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**\_Grupo DH de FWP E \_ incompatible \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-264"><span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**FWP\_E\_INCOMPATIBLE\_DH\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-265">0x80320031L</span><span class="sxs-lookup"><span data-stu-id="f0b97-265">0x80320031L</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-266">El grupo de Diffie-Hellman no es compatible con el tipo de directiva.</span><span class="sxs-lookup"><span data-stu-id="f0b97-266">The Diffie-Hellman group is not compatible with the policy type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-267"><span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**no se admite el FWP \_ E \_ em \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-267"><span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**FWP\_E\_EM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-268">0x80320032</span><span class="sxs-lookup"><span data-stu-id="f0b97-268">0x80320032</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-269">Una directiva IKE no puede contener una directiva de modo extendido.</span><span class="sxs-lookup"><span data-stu-id="f0b97-269">An IKE policy cannot contain an Extended Mode policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-270"><span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**FWP \_ E \_ nunca \_ coinciden**</span><span class="sxs-lookup"><span data-stu-id="f0b97-270"><span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**FWP\_E\_NEVER\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-271">0x80320033</span><span class="sxs-lookup"><span data-stu-id="f0b97-271">0x80320033</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-272">La plantilla o la suscripción de enumeración nunca coincidirán con ningún objeto.</span><span class="sxs-lookup"><span data-stu-id="f0b97-272">The enumeration template or subscription will never match any objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-273"><span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**\_ \_ \_ no coincide el contexto del proveedor \_ de FWP E**</span><span class="sxs-lookup"><span data-stu-id="f0b97-273"><span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**FWP\_E\_PROVIDER\_CONTEXT\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-274">0x80320034</span><span class="sxs-lookup"><span data-stu-id="f0b97-274">0x80320034</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-275">El contexto del proveedor es de un tipo incorrecto.</span><span class="sxs-lookup"><span data-stu-id="f0b97-275">The provider context is of the wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-276"><span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**\_ \_ parámetro no válido de FWP E \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-276"><span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**FWP\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-277">0x80320035</span><span class="sxs-lookup"><span data-stu-id="f0b97-277">0x80320035</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-278">El parámetro no es correcto.</span><span class="sxs-lookup"><span data-stu-id="f0b97-278">The parameter is incorrect.</span></span>

<span data-ttu-id="f0b97-279">Causas posibles de este error:</span><span class="sxs-lookup"><span data-stu-id="f0b97-279">Possible reasons for this error:</span></span>

-   <span data-ttu-id="f0b97-280">Se llamó a [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) sin establecer la marca de túnel de marca **FWPM \_ \_ \_ \_ en \_ punto** y con condiciones distintas de la dirección local o remota.</span><span class="sxs-lookup"><span data-stu-id="f0b97-280">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) was called without setting the flag **FWPM\_TUNNEL\_FLAG\_POINT\_TO\_POINT** and with conditions other than local/remote address.</span></span>
-   <span data-ttu-id="f0b97-281">Una cadena Unicode no válida o una cadena Unicode que contiene caracteres no imprimibles.</span><span class="sxs-lookup"><span data-stu-id="f0b97-281">An invalid Unicode string, or a Unicode string that contains unprintable characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-282"><span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**FWP \_ E \_ demasiadas \_ \_ subcapas**</span><span class="sxs-lookup"><span data-stu-id="f0b97-282"><span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**FWP\_E\_TOO\_MANY\_SUBLAYERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-283">0x80320036</span><span class="sxs-lookup"><span data-stu-id="f0b97-283">0x80320036</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-284">Se ha alcanzado el número máximo de subcapas.</span><span class="sxs-lookup"><span data-stu-id="f0b97-284">The maximum number of sublayers has been reached.</span></span>

<span data-ttu-id="f0b97-285">WFP admite como máximo 2 6 subcapas.</span><span class="sxs-lookup"><span data-stu-id="f0b97-285">WFP supports at most 2 6 sublayers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-286"><span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**error en la notificación de llamada de FWP \_ E \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-286"><span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**FWP\_E\_CALLOUT\_NOTIFICATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-287">0x80320037</span><span class="sxs-lookup"><span data-stu-id="f0b97-287">0x80320037</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-288">La función de notificación de una llamada devolvió un error.</span><span class="sxs-lookup"><span data-stu-id="f0b97-288">The notification function for a callout returned an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-289"><span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**transformación de autenticación de FWP \_ E \_ no válida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-289"><span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**FWP\_E\_INVALID\_AUTH\_TRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-290">0x80320038</span><span class="sxs-lookup"><span data-stu-id="f0b97-290">0x80320038</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-291">La transformación de autenticación de IPsec no es válida.</span><span class="sxs-lookup"><span data-stu-id="f0b97-291">The IPsec authentication transform is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0b97-292"><span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**\_transformación de \_ \_ cifrado de FWP E no válida \_**</span><span class="sxs-lookup"><span data-stu-id="f0b97-292"><span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**FWP\_E\_INVALID\_CIPHER\_TRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0b97-293">0x80320039</span><span class="sxs-lookup"><span data-stu-id="f0b97-293">0x80320039</span></span>
</dt> <dt>



<span data-ttu-id="f0b97-294">La transformación de cifrado de IPsec no es válida.</span><span class="sxs-lookup"><span data-stu-id="f0b97-294">The IPsec cipher transform is not valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0b97-295">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0b97-295">Requirements</span></span>



| <span data-ttu-id="f0b97-296">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0b97-296">Requirement</span></span> | <span data-ttu-id="f0b97-297">Value</span><span class="sxs-lookup"><span data-stu-id="f0b97-297">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b97-298">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0b97-298">Minimum supported client</span></span><br/> | <span data-ttu-id="f0b97-299">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f0b97-299">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0b97-300">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0b97-300">Minimum supported server</span></span><br/> | <span data-ttu-id="f0b97-301">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0b97-301">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0b97-302">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0b97-302">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0b97-303"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0b97-303"><dt>Winerror.h</dt></span></span> </dl> |



 

 





