---
title: MSAD_ReplPendingOp (clase)
description: Representa la estructura de operaciones de REPL de DS \_ \_ , que describe una tarea de replicación que se está ejecutando actualmente o está pendiente de ejecución.
ms.assetid: d1c101fa-ae33-48da-9b00-93fde553a4f9
ms.tgt_platform: multiple
keywords:
- MSAD_ReplPendingOp clase Active Directory
- Active Directory de MSAD_ReplPendingOp de clase, se describe
topic_type:
- apiref
api_name:
- MSAD_ReplPendingOp
- MSAD_ReplPendingOp.SerialNumber
- MSAD_ReplPendingOp.PositionInQ
- MSAD_ReplPendingOp.OpStartTime
- MSAD_ReplPendingOp.TimeEnqueued
- MSAD_ReplPendingOp.Priority
- MSAD_ReplPendingOp.OpType
- MSAD_ReplPendingOp.Options
- MSAD_ReplPendingOp.NamingContextDN
- MSAD_ReplPendingOp.NamingContextObjGuid
- MSAD_ReplPendingOp.DsaDN
- MSAD_ReplPendingOp.DsaAddress
- MSAD_ReplPendingOp.DsaObjGuid
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f1c3faddac915f602104d7e5dc4e9b6bc7d6944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422324"
---
# <a name="msad_replpendingop-class"></a><span data-ttu-id="86846-105">MSAD \_ ReplPendingOp (clase)</span><span class="sxs-lookup"><span data-stu-id="86846-105">MSAD\_ReplPendingOp class</span></span>

<span data-ttu-id="86846-106">Representa la estructura de [**\_ \_ operaciones de REPL de DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) , que describe una tarea de replicación que se está ejecutando actualmente o está pendiente de ejecución.</span><span class="sxs-lookup"><span data-stu-id="86846-106">Represents the [**DS\_REPL\_OP**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) structure, which describes a replication task that is currently executing or pending execution.</span></span> <span data-ttu-id="86846-107">La función [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) devuelve esta estructura.</span><span class="sxs-lookup"><span data-stu-id="86846-107">This structure is returned by the [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="86846-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86846-108">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplPendingOp
{
  uint32   SerialNumber;
  uint32   PositionInQ;
  datetime OpStartTime;
  datetime TimeEnqueued;
  uint32   Priority;
  uint32   OpType;
  uint32   Options;
  String   NamingContextDN;
  String   NamingContextObjGuid;
  String   DsaDN;
  String   DsaAddress;
  String   DsaObjGuid;
};
```

## <a name="members"></a><span data-ttu-id="86846-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="86846-109">Members</span></span>

<span data-ttu-id="86846-110">La clase **MSAD \_ ReplPendingOp** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="86846-110">The **MSAD\_ReplPendingOp** class has these types of members:</span></span>

-   [<span data-ttu-id="86846-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="86846-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="86846-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="86846-112">Properties</span></span>

<span data-ttu-id="86846-113">La clase **MSAD \_ ReplPendingOp** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="86846-113">The **MSAD\_ReplPendingOp** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="86846-114">**DsaAddress**</span><span class="sxs-lookup"><span data-stu-id="86846-114">**DsaAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86846-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86846-115">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="86846-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86846-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86846-117">Obtiene la dirección de red específica del transporte del servidor remoto que está asociado a esta operación.</span><span class="sxs-lookup"><span data-stu-id="86846-117">Gets the transport-specific network address of the remote server that is associated with this operation.</span></span> <span data-ttu-id="86846-118">Es **null** si no hay ningún servidor remoto asociado a esta operación.</span><span class="sxs-lookup"><span data-stu-id="86846-118">**NULL** if there is no remote server that is associated with this operation.</span></span>

</dd> <dt>

<span data-ttu-id="86846-119">**DsaDN**</span><span class="sxs-lookup"><span data-stu-id="86846-119">**DsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86846-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86846-120">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="86846-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86846-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86846-122">Obtiene la ruta de acceso X. 500 del DSA asociado al servidor remoto que corresponde a esta operación.</span><span class="sxs-lookup"><span data-stu-id="86846-122">Gets the X.500 path of the DSA that is associated with the remote server that corresponds to this operation.</span></span> <span data-ttu-id="86846-123">**Es null** si no hay ningún servidor remoto que se corresponda con esta operación.</span><span class="sxs-lookup"><span data-stu-id="86846-123">**NULL** if no remote server corresponds to this operation.</span></span>

</dd> <dt>

<span data-ttu-id="86846-124">**DsaObjGuid**</span><span class="sxs-lookup"><span data-stu-id="86846-124">**DsaObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86846-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86846-125">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="86846-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86846-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86846-127">Obtiene el valor del atributo [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) del DSA identificado por la propiedad **DsaDN** .</span><span class="sxs-lookup"><span data-stu-id="86846-127">Gets the value of the [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) attribute of the DSA that is identified by the **DsaDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="86846-128">**NamingContextDN**</span><span class="sxs-lookup"><span data-stu-id="86846-128">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86846-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86846-129">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="86846-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86846-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86846-131">Obtiene la ruta de acceso X. 500 del contexto de nomenclatura (NC) que está asociado a esta operación.</span><span class="sxs-lookup"><span data-stu-id="86846-131">Gets the X.500 path of the naming context (NC) that is associated with this operation.</span></span>

</dd> <dt>

<span data-ttu-id="86846-132">**NamingContextObjGuid**</span><span class="sxs-lookup"><span data-stu-id="86846-132">**NamingContextObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86846-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86846-133">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="86846-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86846-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86846-135">Obtiene el atributo [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) del NC identificado por la propiedad **NamingContextDN** .</span><span class="sxs-lookup"><span data-stu-id="86846-135">Gets the [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) attribute of the NC that is identified by the **NamingContextDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="86846-136">**OpStartTime**</span><span class="sxs-lookup"><span data-stu-id="86846-136">**OpStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86846-137">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="86846-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="86846-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86846-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86846-139">Obtiene la hora a la que se inició la operación.</span><span class="sxs-lookup"><span data-stu-id="86846-139">Gets the time when the operation was started.</span></span> <span data-ttu-id="86846-140">Es **null** si esta operación todavía está en la cola.</span><span class="sxs-lookup"><span data-stu-id="86846-140">**NULL** if this operation is still in the queue.</span></span>

</dd> <dt>

<span data-ttu-id="86846-141">**Opciones**</span><span class="sxs-lookup"><span data-stu-id="86846-141">**Options**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86846-142">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86846-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86846-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86846-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86846-144">Obtiene el conjunto de marcadores que proporciona datos adicionales sobre la operación.</span><span class="sxs-lookup"><span data-stu-id="86846-144">Gets the set of flags that provides additional data about the operation.</span></span> <span data-ttu-id="86846-145">El contenido de este miembro viene determinado por el valor de la propiedad **OpType** .</span><span class="sxs-lookup"><span data-stu-id="86846-145">The contents of this member are determined by the value of the **OpType** property.</span></span>

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span data-ttu-id="86846-146"><span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**\_sincronización de \_ tipo de operación de REPL de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="86846-146"><span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**DS\_REPL\_OP\_TYPE\_SYNC**</span></span>


</dt> <dd>

<span data-ttu-id="86846-147">Contiene cero o una combinación de uno o varios de los valores \*\* \_ DS \_ \* REPSYNC\* _ definidos para el parámetro _Options \* en [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).</span><span class="sxs-lookup"><span data-stu-id="86846-147">Contains zero or a combination of one or more of the **DS\_REPSYNC\_\** _ values as defined for the _Options* parameter in [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span data-ttu-id="86846-148"><span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**\_ \_ Agregar tipo de operación de replicación de \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="86846-148"><span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**DS\_REPL\_OP\_TYPE\_ADD**</span></span>


</dt> <dd>

<span data-ttu-id="86846-149">Contiene cero o una combinación de uno o varios de los valores \*\* \_ DS \_ \* REPADD\* _ definidos para el parámetro _Options \* en [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).</span><span class="sxs-lookup"><span data-stu-id="86846-149">Contains zero or a combination of one or more of the **DS\_REPADD\_\** _ values as defined for the _Options* parameter in [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span data-ttu-id="86846-150"><span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**tipo de operación de REPL de DS \_ \_ \_ \_ Delete**</span><span class="sxs-lookup"><span data-stu-id="86846-150"><span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**DS\_REPL\_OP\_TYPE\_DELETE**</span></span>


</dt> <dd>

<span data-ttu-id="86846-151">Contiene cero o una combinación de uno o varios de los valores \*\* \_ DS \_ \* REPDEL\* _ definidos para el parámetro _Options \* en [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).</span><span class="sxs-lookup"><span data-stu-id="86846-151">Contains zero or a combination of one or more of the **DS\_REPDEL\_\** _ values as defined for the _Options* parameter in [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span data-ttu-id="86846-152"><span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**tipo de operación de REPL de DS \_ \_ \_ \_ modificar**</span><span class="sxs-lookup"><span data-stu-id="86846-152"><span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**DS\_REPL\_OP\_TYPE\_MODIFY**</span></span>


</dt> <dd>

<span data-ttu-id="86846-153">Contiene cero o una combinación de uno o varios de los valores \*\* \_ DS \_ \* REPMOD\* _ definidos para el parámetro _Options \* en [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).</span><span class="sxs-lookup"><span data-stu-id="86846-153">Contains zero or a combination of one or more of the **DS\_REPMOD\_\** _ values as defined for the _Options* parameter in [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span data-ttu-id="86846-154"><span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**\_referencias de \_ actualización del tipo de operación de replicación de \_ \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="86846-154"><span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**DS\_REPL\_OP\_TYPE\_UPDATE\_REFS**</span></span>


</dt> <dd>

<span data-ttu-id="86846-155">Contiene cero o una combinación de uno o varios de los valores \*\* \_ DS \_ \* REPSUPD\* _ definidos para el parámetro _Options \* en [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).</span><span class="sxs-lookup"><span data-stu-id="86846-155">Contains zero or a combination of one or more of the **DS\_REPSUPD\_\** _ values as defined for the _Options* parameter in [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="86846-156">**OpType**</span><span class="sxs-lookup"><span data-stu-id="86846-156">**OpType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86846-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86846-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86846-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86846-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86846-159">Obtiene el valor de [**\_ \_ \_ tipo**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) de operación de replicación de DS que indica el tipo de operación que esta clase representa.</span><span class="sxs-lookup"><span data-stu-id="86846-159">Gets the [**DS\_REPL\_OP\_TYPE**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) value that indicates the type of operation that this class represents.</span></span>

</dd> <dt>

<span data-ttu-id="86846-160">**PositionInQ**</span><span class="sxs-lookup"><span data-stu-id="86846-160">**PositionInQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86846-161">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86846-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86846-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86846-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86846-163">Obtiene la posición de esta operación en la cola.</span><span class="sxs-lookup"><span data-stu-id="86846-163">Gets the position of this operation in the queue.</span></span>

</dd> <dt>

<span data-ttu-id="86846-164">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="86846-164">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86846-165">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86846-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86846-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86846-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86846-167">Obtiene la prioridad de esta operación.</span><span class="sxs-lookup"><span data-stu-id="86846-167">Gets the priority of this operation.</span></span> <span data-ttu-id="86846-168">Las tareas de prioridad más alta se ejecutan en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="86846-168">Higher-priority tasks are executed first.</span></span> <span data-ttu-id="86846-169">El servidor calcula la prioridad basándose en el tipo de operación que esta clase representa y en los parámetros de la operación.</span><span class="sxs-lookup"><span data-stu-id="86846-169">The priority is calculated by the server based on the type of operation that this class represents and the parameters of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="86846-170">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="86846-170">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86846-171">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86846-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86846-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86846-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86846-173">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="86846-173">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="86846-174">Obtiene el identificador de la operación, que es único por equipo y por arranque.</span><span class="sxs-lookup"><span data-stu-id="86846-174">Gets the ID of the operation, which is unique per-machine and per-boot.</span></span>

</dd> <dt>

<span data-ttu-id="86846-175">**TimeEnqueued**</span><span class="sxs-lookup"><span data-stu-id="86846-175">**TimeEnqueued**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86846-176">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="86846-176">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="86846-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86846-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86846-178">Obtiene la hora a la que se agregó esta operación a la cola.</span><span class="sxs-lookup"><span data-stu-id="86846-178">Gets the time at which this operation was added to the queue.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="86846-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86846-179">Requirements</span></span>



| <span data-ttu-id="86846-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="86846-180">Requirement</span></span> | <span data-ttu-id="86846-181">Value</span><span class="sxs-lookup"><span data-stu-id="86846-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86846-182">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86846-182">Minimum supported client</span></span><br/> | <span data-ttu-id="86846-183">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="86846-183">None supported</span></span><br/>                                                               |
| <span data-ttu-id="86846-184">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86846-184">Minimum supported server</span></span><br/> | <span data-ttu-id="86846-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86846-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86846-186">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="86846-186">Namespace</span></span><br/>                | <span data-ttu-id="86846-187">\\MicrosoftActiveDirectory raíz</span><span class="sxs-lookup"><span data-stu-id="86846-187">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="86846-188">MOF</span><span class="sxs-lookup"><span data-stu-id="86846-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86846-189"><dt>ReplProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86846-189"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="86846-190">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="86846-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86846-191"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86846-191"><dt>Replprov.dll</dt></span></span> </dl> |



 

