---
title: Método SyncNamingContext de la clase MSAD_ReplNeighbor
description: Llama a la función DsReplicaSync que sincroniza un contexto de nomenclatura de destino con uno de sus orígenes.
ms.assetid: 005053c4-8d9c-42f6-bae6-3ecdedd5ac2b
ms.tgt_platform: multiple
keywords:
- Método SyncNamingContext Active Directory
- Método SyncNamingContext Active Directory, clase MSAD_ReplNeighbor
- MSAD_ReplNeighbor de clase Active Directory, método SyncNamingContext
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor.SyncNamingContext
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 691bd3e943f491ba93d867097ac0167c97be6108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492178"
---
# <a name="syncnamingcontext-method-of-the-msad_replneighbor-class"></a><span data-ttu-id="329d0-106">Método SyncNamingContext de la \_ clase ReplNeighbor de MSAD</span><span class="sxs-lookup"><span data-stu-id="329d0-106">SyncNamingContext method of the MSAD\_ReplNeighbor class</span></span>

<span data-ttu-id="329d0-107">Llama a la función [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) que sincroniza un contexto de nomenclatura de destino con uno de sus orígenes.</span><span class="sxs-lookup"><span data-stu-id="329d0-107">Calls the [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) function that synchronizes a destination naming context with one of its sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="329d0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="329d0-108">Syntax</span></span>


```mof
void SyncNamingContext(
  [in] uint32 Options
);
```



## <a name="parameters"></a><span data-ttu-id="329d0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="329d0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="329d0-110">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="329d0-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="329d0-111">Datos adicionales que determinan cómo el método procesa la solicitud.</span><span class="sxs-lookup"><span data-stu-id="329d0-111">Additional data that determines how the method processes the request.</span></span> <span data-ttu-id="329d0-112">Este parámetro puede ser una combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="329d0-112">This parameter can be a combination of the following values.</span></span>

<dt>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>

<span data-ttu-id="329d0-113"><span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**\_ \_ Agregar referencia de REPSYNC de DS \_**</span><span class="sxs-lookup"><span data-stu-id="329d0-113"><span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**DS\_REPSYNC\_ADD\_REFERENCE**</span></span>


</dt> <dd>

<span data-ttu-id="329d0-114">Hace que el agente de sistema de directorio de origen (DSA) Compruebe que el DSA local está presente en la lista replicaciones de origen a.</span><span class="sxs-lookup"><span data-stu-id="329d0-114">Causes the source directory system agent (DSA) to verify that the local DSA is present in the source replicates-to list.</span></span> <span data-ttu-id="329d0-115">Si el DSA local no está presente, se agrega.</span><span class="sxs-lookup"><span data-stu-id="329d0-115">If the local DSA is not present, it is added.</span></span> <span data-ttu-id="329d0-116">Esto garantiza que el origen envíe notificaciones de cambios.</span><span class="sxs-lookup"><span data-stu-id="329d0-116">This ensures that the source sends change notifications.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>

<span data-ttu-id="329d0-117"><span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**\_REPSYNC de \_ todos los \_ orígenes de DS**</span><span class="sxs-lookup"><span data-stu-id="329d0-117"><span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS\_REPSYNC\_ALL\_SOURCES**</span></span>


</dt> <dd>

<span data-ttu-id="329d0-118">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="329d0-118">This value is not supported.</span></span>

<span data-ttu-id="329d0-119">**Windows server 2008 R2, Windows server 2008 y Windows server 2003:** Sincroniza desde todos los orígenes.</span><span class="sxs-lookup"><span data-stu-id="329d0-119">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** Synchronizes from all sources.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>

<span data-ttu-id="329d0-120"><span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**\_ \_ operación asincrónica REPSYNC de \_ DS**</span><span class="sxs-lookup"><span data-stu-id="329d0-120"><span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**DS\_REPSYNC\_ASYNCHRONOUS\_OPERATION**</span></span>


</dt> <dd>

<span data-ttu-id="329d0-121">Realiza esta operación de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="329d0-121">Performs this operation asynchronously.</span></span>

<span data-ttu-id="329d0-122">**Windows server 2008 R2, Windows server 2008 y Windows server 2003:** Se requiere cuando se usa **DS \_ REPSYNC \_ todos los \_ orígenes**.</span><span class="sxs-lookup"><span data-stu-id="329d0-122">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** Required when using **DS\_REPSYNC\_ALL\_SOURCES**.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>

<span data-ttu-id="329d0-123"><span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**\_fuerza de REPSYNC de DS \_**</span><span class="sxs-lookup"><span data-stu-id="329d0-123"><span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**DS\_REPSYNC\_FORCE**</span></span>


</dt> <dd>

<span data-ttu-id="329d0-124">Sincroniza aunque el vínculo esté deshabilitado actualmente.</span><span class="sxs-lookup"><span data-stu-id="329d0-124">Synchronizes even if the link is currently disabled.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>

<span data-ttu-id="329d0-125"><span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**\_REPSYNC DS \_ completo**</span><span class="sxs-lookup"><span data-stu-id="329d0-125"><span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS\_REPSYNC\_FULL**</span></span>


</dt> <dd>

<span data-ttu-id="329d0-126">Sincroniza a partir del primer número de secuencia de actualización (USN).</span><span class="sxs-lookup"><span data-stu-id="329d0-126">Synchronizes starting from the first Update Sequence Number (USN).</span></span>

</dd> <dt>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>

<span data-ttu-id="329d0-127"><span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**\_ \_ mensajería entre sitios de DS REPSYNC \_**</span><span class="sxs-lookup"><span data-stu-id="329d0-127"><span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**DS\_REPSYNC\_INTERSITE\_MESSAGING**</span></span>


</dt> <dd>

<span data-ttu-id="329d0-128">Sincroniza con ISM.</span><span class="sxs-lookup"><span data-stu-id="329d0-128">Synchronizes using an ISM.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>

<span data-ttu-id="329d0-129"><span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**REPSYNC de DS \_ \_ no \_ descartar**</span><span class="sxs-lookup"><span data-stu-id="329d0-129"><span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS\_REPSYNC\_NO\_DISCARD**</span></span>


</dt> <dd>

<span data-ttu-id="329d0-130">No descarta esta solicitud de sincronización, aunque esté pendiente una sincronización similar.</span><span class="sxs-lookup"><span data-stu-id="329d0-130">Does not discard this synchronization request, even if a similar synchronization is pending.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>

<span data-ttu-id="329d0-131"><span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**\_REPSYNC DS \_ periódico**</span><span class="sxs-lookup"><span data-stu-id="329d0-131"><span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS\_REPSYNC\_PERIODIC**</span></span>


</dt> <dd>

<span data-ttu-id="329d0-132">Indica que esta operación es una solicitud de sincronización periódica programada por el administrador.</span><span class="sxs-lookup"><span data-stu-id="329d0-132">Indicates that this operation is a periodic synchronization request that is scheduled by the administrator.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>

<span data-ttu-id="329d0-133"><span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**REPSYNC de DS \_ \_ urgente**</span><span class="sxs-lookup"><span data-stu-id="329d0-133"><span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS\_REPSYNC\_URGENT**</span></span>


</dt> <dd>

<span data-ttu-id="329d0-134">Indica que esta operación es una notificación de una actualización marcada como urgente.</span><span class="sxs-lookup"><span data-stu-id="329d0-134">Indicates that this operation is a notification of an update that is marked as urgent.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>

<span data-ttu-id="329d0-135"><span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**\_REPSYNC DS \_ grabable**</span><span class="sxs-lookup"><span data-stu-id="329d0-135"><span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS\_REPSYNC\_WRITEABLE**</span></span>


</dt> <dd>

<span data-ttu-id="329d0-136">Indica que se puede escribir en esta réplica.</span><span class="sxs-lookup"><span data-stu-id="329d0-136">Indicates that this replica is writable.</span></span> <span data-ttu-id="329d0-137">Si no se establece esta marca, la réplica es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="329d0-137">If this flag is not set, the replica is read-only.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="329d0-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="329d0-138">Return value</span></span>

<span data-ttu-id="329d0-139">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="329d0-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="329d0-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="329d0-140">Requirements</span></span>



| <span data-ttu-id="329d0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="329d0-141">Requirement</span></span> | <span data-ttu-id="329d0-142">Value</span><span class="sxs-lookup"><span data-stu-id="329d0-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="329d0-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="329d0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="329d0-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="329d0-144">None supported</span></span><br/>                                                               |
| <span data-ttu-id="329d0-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="329d0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="329d0-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="329d0-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="329d0-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="329d0-147">Namespace</span></span><br/>                | <span data-ttu-id="329d0-148">\\MicrosoftActiveDirectory raíz</span><span class="sxs-lookup"><span data-stu-id="329d0-148">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="329d0-149">MOF</span><span class="sxs-lookup"><span data-stu-id="329d0-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="329d0-150"><dt>ReplProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="329d0-150"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="329d0-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="329d0-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="329d0-152"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="329d0-152"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="329d0-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="329d0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="329d0-154">**MSAD \_ ReplNeighbor**</span><span class="sxs-lookup"><span data-stu-id="329d0-154">**MSAD\_ReplNeighbor**</span></span>](msad-replneighbor.md)
</dt> </dl>

 

 





