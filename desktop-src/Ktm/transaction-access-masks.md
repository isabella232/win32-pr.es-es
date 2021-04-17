---
description: KTM define las siguientes máscaras de acceso a las transacciones que se van a usar al abrir una transacción.
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: Máscaras de acceso a transacciones (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b815bcb04a97dbd059c85c6c615a7d607bf77ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677695"
---
# <a name="transaction-access-masks"></a><span data-ttu-id="31a04-103">Máscaras de acceso a transacciones</span><span class="sxs-lookup"><span data-stu-id="31a04-103">Transaction Access Masks</span></span>

<span data-ttu-id="31a04-104">KTM define las siguientes máscaras de acceso a las transacciones que se van a usar al abrir una transacción.</span><span class="sxs-lookup"><span data-stu-id="31a04-104">KTM defines the following transaction access masks to be used when opening a transaction.</span></span>

<dl> <dt>

<span data-ttu-id="31a04-105"><span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**\_información de consulta de transacción \_**</span><span class="sxs-lookup"><span data-stu-id="31a04-105"><span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**TRANSACTION\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31a04-106">0x000001</span><span class="sxs-lookup"><span data-stu-id="31a04-106">0x000001</span></span>
</dt> <dt>



<span data-ttu-id="31a04-107">El autor de la llamada puede consultar la información de la transacción.</span><span class="sxs-lookup"><span data-stu-id="31a04-107">The caller can query transaction information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31a04-108"><span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**\_información del conjunto de transacciones \_**</span><span class="sxs-lookup"><span data-stu-id="31a04-108"><span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**TRANSACTION\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31a04-109">0x000002</span><span class="sxs-lookup"><span data-stu-id="31a04-109">0x000002</span></span>
</dt> <dt>



<span data-ttu-id="31a04-110">El autor de la llamada puede establecer la información de la transacción.</span><span class="sxs-lookup"><span data-stu-id="31a04-110">The caller can set transaction information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31a04-111"><span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**inscripción de transacciones \_**</span><span class="sxs-lookup"><span data-stu-id="31a04-111"><span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**TRANSACTION\_ENLIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31a04-112">0x000004</span><span class="sxs-lookup"><span data-stu-id="31a04-112">0x000004</span></span>
</dt> <dt>



<span data-ttu-id="31a04-113">El autor de la llamada puede darse de alta en esta transacción.</span><span class="sxs-lookup"><span data-stu-id="31a04-113">The caller can enlist in this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31a04-114"><span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**confirmación de transacción \_**</span><span class="sxs-lookup"><span data-stu-id="31a04-114"><span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**TRANSACTION\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31a04-115">0x000008</span><span class="sxs-lookup"><span data-stu-id="31a04-115">0x000008</span></span>
</dt> <dt>



<span data-ttu-id="31a04-116">El autor de la llamada puede confirmar esta transacción.</span><span class="sxs-lookup"><span data-stu-id="31a04-116">The caller can commit this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31a04-117"><span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**reversión de transacciones \_**</span><span class="sxs-lookup"><span data-stu-id="31a04-117"><span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**TRANSACTION\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31a04-118">0x000010</span><span class="sxs-lookup"><span data-stu-id="31a04-118">0x000010</span></span>
</dt> <dt>



<span data-ttu-id="31a04-119">El autor de la llamada puede revertir esta transacción.</span><span class="sxs-lookup"><span data-stu-id="31a04-119">The caller can roll back this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31a04-120"><span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**propagación de transacciones \_**</span><span class="sxs-lookup"><span data-stu-id="31a04-120"><span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**TRANSACTION\_PROPAGATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31a04-121">0x000020</span><span class="sxs-lookup"><span data-stu-id="31a04-121">0x000020</span></span>
</dt> <dt>



<span data-ttu-id="31a04-122">El autor de la llamada puede propagar esta transacción a un administrador de recursos superior, como el Coordinador de transacciones distribuidas (DTC).</span><span class="sxs-lookup"><span data-stu-id="31a04-122">The caller can propagate this transaction to a superior resource manager, such as the Distributed Transaction Coordinator (DTC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31a04-123"><span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**\_lectura genérica de transacción \_**</span><span class="sxs-lookup"><span data-stu-id="31a04-123"><span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**TRANSACTION\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31a04-124">0x120001</span><span class="sxs-lookup"><span data-stu-id="31a04-124">0x120001</span></span>
</dt> <dt>



<span data-ttu-id="31a04-125">El autor de la llamada tiene los siguientes privilegios: **\_ \_ lectura de derechos estándar**, **información de \_ consulta \_ de transacción** y **sincronización**.</span><span class="sxs-lookup"><span data-stu-id="31a04-125">The caller has the following privileges: **STANDARD\_RIGHTS\_READ**, **TRANSACTION\_QUERY\_INFORMATION**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31a04-126"><span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**\_escritura genérica de transacción \_**</span><span class="sxs-lookup"><span data-stu-id="31a04-126"><span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**TRANSACTION\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31a04-127">0x12003E</span><span class="sxs-lookup"><span data-stu-id="31a04-127">0x12003E</span></span>
</dt> <dt>



<span data-ttu-id="31a04-128">El autor de la llamada tiene los privilegios siguientes: **\_ \_ escritura de derechos estándar**, **información de \_ conjunto \_ de transacciones**, **\_ confirmación de transacciones**, **\_ inscripción de transacciones**, **\_ reversión de transacciones**, **\_ propagación de transacciones** y **sincronización**.</span><span class="sxs-lookup"><span data-stu-id="31a04-128">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **TRANSACTION\_SET\_INFORMATION**, **TRANSACTION\_COMMIT**, **TRANSACTION\_ENLIST**, **TRANSACTION\_ROLLBACK**, **TRANSACTION\_PROPAGATE**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31a04-129"><span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**\_ejecución genérica de transacción \_**</span><span class="sxs-lookup"><span data-stu-id="31a04-129"><span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**TRANSACTION\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31a04-130">0x120018</span><span class="sxs-lookup"><span data-stu-id="31a04-130">0x120018</span></span>
</dt> <dt>



<span data-ttu-id="31a04-131">El autor de la llamada tiene los siguientes privilegios: **\_ permisos estándar \_ Execute**, **\_ COMMIT TRANSACTION**, **\_ ROLLBACK TRANSACTION** y **SYNCHRONIZE**.</span><span class="sxs-lookup"><span data-stu-id="31a04-131">The caller has the following privileges: **STANDARD\_RIGHTS\_EXECUTE**, **TRANSACTION\_COMMIT**, **TRANSACTION\_ROLLBACK**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31a04-132"><span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**\_acceso a todas las transacciones \_**</span><span class="sxs-lookup"><span data-stu-id="31a04-132"><span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**TRANSACTION\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31a04-133">0x12003F</span><span class="sxs-lookup"><span data-stu-id="31a04-133">0x12003F</span></span>
</dt> <dt>



<span data-ttu-id="31a04-134">El autor de la llamada tiene el siguiente privilegio: **\_ derechos estándar \_ necesarios**, **\_ \_ lectura genérica de transacción**, **\_ \_ escritura genérica de transacción** y **\_ \_ ejecución genérica de transacción**.</span><span class="sxs-lookup"><span data-stu-id="31a04-134">The caller has the following privilege: **STANDARD\_RIGHTS\_REQUIRED**, **TRANSACTION\_GENERIC\_READ**, **TRANSACTION\_GENERIC\_WRITE**, and **TRANSACTION\_GENERIC\_EXECUTE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31a04-135"><span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**\_derechos del \_ Administrador de recursos de transacciones \_**</span><span class="sxs-lookup"><span data-stu-id="31a04-135"><span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**TRANSACTION\_RESOURCE\_MANAGER\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31a04-136">0x120037</span><span class="sxs-lookup"><span data-stu-id="31a04-136">0x120037</span></span>
</dt> <dt>



<span data-ttu-id="31a04-137">El autor de la llamada tiene los siguientes privilegios: **operación de \_ \_ lectura genérica de transacción**, **\_ \_ escritura de derechos estándar**, **\_ \_ información de conjunto de transacciones**, **\_ reversión de transacciones**, **\_ inscripción de transacciones**, **\_ propagación de transacciones** y **sincronización**.</span><span class="sxs-lookup"><span data-stu-id="31a04-137">The caller has the following privileges: **TRANSACTION\_GENERIC\_READ**, **STANDARD\_RIGHTS\_WRITE**, **TRANSACTION\_SET\_INFORMATION**, **TRANSACTION\_ROLLBACK**, **TRANSACTION\_ENLIST**, **TRANSACTION\_PROPAGATE**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31a04-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31a04-138">Remarks</span></span>

<span data-ttu-id="31a04-139">Se recomienda que los administradores de recursos, cuando se da de alta en una transacción, especifiquen derechos de administrador de recursos de transacciones al abrir una transacción. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="31a04-139">It is recommended that resource managers, when enlisting in a transaction, specify **TRANSACTION\_RESOURCE\_MANAGER\_RIGHTS** when opening a transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="31a04-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31a04-140">Requirements</span></span>



| <span data-ttu-id="31a04-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="31a04-141">Requirement</span></span> | <span data-ttu-id="31a04-142">Value</span><span class="sxs-lookup"><span data-stu-id="31a04-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="31a04-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31a04-143">Minimum supported client</span></span><br/> | <span data-ttu-id="31a04-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31a04-144">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="31a04-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31a04-145">Minimum supported server</span></span><br/> | <span data-ttu-id="31a04-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31a04-146">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="31a04-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31a04-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="31a04-148"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="31a04-148"><dt>WinNT.h</dt></span></span> </dl> |



 

 




