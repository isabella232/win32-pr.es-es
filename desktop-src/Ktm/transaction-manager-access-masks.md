---
description: KTM define las siguientes máscaras de acceso de inscripción que se usarán al abrir un administrador de transacciones (TM).
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: Máscaras de acceso del administrador de transacciones (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efae6c0bac1fc2bfa117e74e38aff8d439eb2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909185"
---
# <a name="transaction-manager-access-masks"></a><span data-ttu-id="091c7-103">Máscaras de acceso del administrador de transacciones</span><span class="sxs-lookup"><span data-stu-id="091c7-103">Transaction Manager Access Masks</span></span>

<span data-ttu-id="091c7-104">KTM define las siguientes máscaras de acceso de inscripción que se usarán al abrir un administrador de transacciones (TM).</span><span class="sxs-lookup"><span data-stu-id="091c7-104">KTM defines the following enlistment access masks to be used when opening a transaction manager (TM).</span></span>

<dl> <dt>

<span data-ttu-id="091c7-105"><span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**\_información de consulta de TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="091c7-105"><span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**TRANSACTIONMANAGER\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="091c7-106">0x00001</span><span class="sxs-lookup"><span data-stu-id="091c7-106">0x00001</span></span>
</dt> <dt>



<span data-ttu-id="091c7-107">El autor de la llamada puede consultar información sobre este TM.</span><span class="sxs-lookup"><span data-stu-id="091c7-107">The caller can query information about this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091c7-108"><span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**\_información del conjunto de TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="091c7-108"><span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**TRANSACTIONMANAGER\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="091c7-109">0x00002</span><span class="sxs-lookup"><span data-stu-id="091c7-109">0x00002</span></span>
</dt> <dt>



<span data-ttu-id="091c7-110">El autor de la llamada puede establecer información sobre este TM.</span><span class="sxs-lookup"><span data-stu-id="091c7-110">The caller can set information about this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091c7-111"><span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**recuperación de TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="091c7-111"><span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**TRANSACTIONMANAGER\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="091c7-112">0x00004</span><span class="sxs-lookup"><span data-stu-id="091c7-112">0x00004</span></span>
</dt> <dt>



<span data-ttu-id="091c7-113">El autor de la llamada puede recuperar este TM.</span><span class="sxs-lookup"><span data-stu-id="091c7-113">The caller can recover this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091c7-114"><span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**\_cambiar nombre de TRANSACTIONMANAGER**</span><span class="sxs-lookup"><span data-stu-id="091c7-114"><span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**TRANSACTIONMANAGER\_RENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="091c7-115">0x00008</span><span class="sxs-lookup"><span data-stu-id="091c7-115">0x00008</span></span>
</dt> <dt>



<span data-ttu-id="091c7-116">El autor de la llamada puede cambiar el nombre de una instancia de TM.</span><span class="sxs-lookup"><span data-stu-id="091c7-116">The caller can rename a TM instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091c7-117"><span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER \_ crear \_ RM**</span><span class="sxs-lookup"><span data-stu-id="091c7-117"><span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER\_CREATE\_RM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="091c7-118">0x00010</span><span class="sxs-lookup"><span data-stu-id="091c7-118">0x00010</span></span>
</dt> <dt>



<span data-ttu-id="091c7-119">El autor de la llamada puede crear un administrador de recursos asociado a este TM.</span><span class="sxs-lookup"><span data-stu-id="091c7-119">The caller can create a resource manager that is associated with this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091c7-120"><span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**\_transacción de enlace de TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="091c7-120"><span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**TRANSACTIONMANAGER\_BIND\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="091c7-121">0x00020</span><span class="sxs-lookup"><span data-stu-id="091c7-121">0x00020</span></span>
</dt> <dt>



<span data-ttu-id="091c7-122">Este valor está reservado.</span><span class="sxs-lookup"><span data-stu-id="091c7-122">This value is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091c7-123"><span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**\_lectura genérica de TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="091c7-123"><span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**TRANSACTIONMANAGER\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="091c7-124">0x20001</span><span class="sxs-lookup"><span data-stu-id="091c7-124">0x20001</span></span>
</dt> <dt>



<span data-ttu-id="091c7-125">El autor de la llamada tiene los siguientes privilegios: **derechos estándar de \_ \_ lectura** e **\_ \_ información de consulta de TRANSACTIONMANAGER**.</span><span class="sxs-lookup"><span data-stu-id="091c7-125">The caller has the following privileges: **STANDARD\_RIGHTS\_READ** and **TRANSACTIONMANAGER\_QUERY\_INFORMATION**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091c7-126"><span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**\_escritura genérica de TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="091c7-126"><span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**TRANSACTIONMANAGER\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="091c7-127">0x2001E</span><span class="sxs-lookup"><span data-stu-id="091c7-127">0x2001E</span></span>
</dt> <dt>



<span data-ttu-id="091c7-128">El autor de la llamada tiene los privilegios siguientes: **\_ \_ escritura de derechos estándar**, **información de \_ conjunto \_ de TransactionManager**, **\_ recuperación de TransactionManager**, **cambio de \_ nombre de TransactionManager** y **TransactionManager \_ Create \_ RM**.</span><span class="sxs-lookup"><span data-stu-id="091c7-128">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **TRANSACTIONMANAGER\_SET\_INFORMATION**, **TRANSACTIONMANAGER\_RECOVER**, **TRANSACTIONMANAGER\_RENAME**, and **TRANSACTIONMANAGER\_CREATE\_RM**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091c7-129"><span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**\_ejecución genérica de TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="091c7-129"><span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**TRANSACTIONMANAGER\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="091c7-130">0x20000</span><span class="sxs-lookup"><span data-stu-id="091c7-130">0x20000</span></span>
</dt> <dt>



<span data-ttu-id="091c7-131">El autor de la llamada tiene el siguiente privilegio: **permisos estándar de \_ \_ ejecución**.</span><span class="sxs-lookup"><span data-stu-id="091c7-131">The caller has the following privilege: **STANDARD\_RIGHTS\_EXECUTE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091c7-132"><span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**destransactionmanager \_ todo el \_ acceso**</span><span class="sxs-lookup"><span data-stu-id="091c7-132"><span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**TRANSACTIONMANAGER\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="091c7-133">0xF003F</span><span class="sxs-lookup"><span data-stu-id="091c7-133">0xF003F</span></span>
</dt> <dt>



<span data-ttu-id="091c7-134">Este valor establece todos los bits válidos para un valor de acceso de TM.</span><span class="sxs-lookup"><span data-stu-id="091c7-134">This value sets all valid bits for a TM access value.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="091c7-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="091c7-135">Requirements</span></span>



| <span data-ttu-id="091c7-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="091c7-136">Requirement</span></span> | <span data-ttu-id="091c7-137">Value</span><span class="sxs-lookup"><span data-stu-id="091c7-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="091c7-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="091c7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="091c7-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="091c7-139">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="091c7-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="091c7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="091c7-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="091c7-141">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="091c7-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="091c7-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="091c7-143"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="091c7-143"><dt>WinNT.h</dt></span></span> </dl> |



 

 




