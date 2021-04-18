---
description: KTM define las siguientes máscaras de acceso de inscripción que se usarán al abrir las inlistas.
ms.assetid: 93773eb7-141a-49f3-9306-ffbda2f4ab9f
title: Máscaras de acceso de inscripción (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63e4ebd67f93368215ebcdcd362595d0341adb52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688548"
---
# <a name="enlistment-access-masks"></a><span data-ttu-id="14395-103">Máscaras de acceso de inscripción</span><span class="sxs-lookup"><span data-stu-id="14395-103">Enlistment Access Masks</span></span>

<span data-ttu-id="14395-104">KTM define las siguientes máscaras de acceso de inscripción que se usarán al abrir las inlistas.</span><span class="sxs-lookup"><span data-stu-id="14395-104">KTM defines the following enlistment access masks to be used when opening enlistments.</span></span>

<dl> <dt>

<span data-ttu-id="14395-105"><span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**información de la \_ consulta de inscripción \_**</span><span class="sxs-lookup"><span data-stu-id="14395-105"><span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**ENLISTMENT\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14395-106">0x00001</span><span class="sxs-lookup"><span data-stu-id="14395-106">0x00001</span></span>
</dt> <dt>



<span data-ttu-id="14395-107">El autor de la llamada puede consultar el KTM para obtener información sobre la inscripción.</span><span class="sxs-lookup"><span data-stu-id="14395-107">The caller can query KTM for information about the enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="14395-108"><span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**información del conjunto de inscripción \_ \_**</span><span class="sxs-lookup"><span data-stu-id="14395-108"><span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**ENLISTMENT\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14395-109">0x00002</span><span class="sxs-lookup"><span data-stu-id="14395-109">0x00002</span></span>
</dt> <dt>



<span data-ttu-id="14395-110">El autor de la llamada puede establecer información sobre la inscripción.</span><span class="sxs-lookup"><span data-stu-id="14395-110">The caller can set information about the enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="14395-111"><span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**recuperación de inscripción \_**</span><span class="sxs-lookup"><span data-stu-id="14395-111"><span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**ENLISTMENT\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14395-112">0x00004</span><span class="sxs-lookup"><span data-stu-id="14395-112">0x00004</span></span>
</dt> <dt>



<span data-ttu-id="14395-113">El autor de la llamada puede recuperar una inscripción.</span><span class="sxs-lookup"><span data-stu-id="14395-113">The caller can recover an enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="14395-114"><span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**\_derechos subordinados de \_ inscripción**</span><span class="sxs-lookup"><span data-stu-id="14395-114"><span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**ENLISTMENT\_SUBORDINATE\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14395-115">0x00008</span><span class="sxs-lookup"><span data-stu-id="14395-115">0x00008</span></span>
</dt> <dt>



<span data-ttu-id="14395-116">El autor de la llamada puede completar las acciones que realiza un administrador de recursos en nombre de la transacción.</span><span class="sxs-lookup"><span data-stu-id="14395-116">The caller can complete actions that a resource manager does on behalf of the transaction.</span></span> <span data-ttu-id="14395-117">A continuación se muestra una lista de acciones:</span><span class="sxs-lookup"><span data-stu-id="14395-117">The following is a list of actions:</span></span>

-   [<span data-ttu-id="14395-118">**CommitComplete**</span><span class="sxs-lookup"><span data-stu-id="14395-118">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [<span data-ttu-id="14395-119">**PrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="14395-119">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [<span data-ttu-id="14395-120">**PrePrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="14395-120">**PrePrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)
-   [<span data-ttu-id="14395-121">**RollbackComplete**</span><span class="sxs-lookup"><span data-stu-id="14395-121">**RollbackComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)
-   [<span data-ttu-id="14395-122">**ReadOnlyEnlistment**</span><span class="sxs-lookup"><span data-stu-id="14395-122">**ReadOnlyEnlistment**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)
-   [<span data-ttu-id="14395-123">**RollbackEnlistment**</span><span class="sxs-lookup"><span data-stu-id="14395-123">**RollbackEnlistment**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)
-   [<span data-ttu-id="14395-124">**SinglePhaseReject**</span><span class="sxs-lookup"><span data-stu-id="14395-124">**SinglePhaseReject**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span data-ttu-id="14395-125"><span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**\_derechos superiores de inscripción \_**</span><span class="sxs-lookup"><span data-stu-id="14395-125"><span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**ENLISTMENT\_SUPERIOR\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14395-126">0x00010</span><span class="sxs-lookup"><span data-stu-id="14395-126">0x00010</span></span>
</dt> <dt>



<span data-ttu-id="14395-127">El autor de la llamada puede darse de alta en la transacción como un administrador de transacciones superior.</span><span class="sxs-lookup"><span data-stu-id="14395-127">The caller can enlist in the transaction as a superior transaction manager.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="14395-128"><span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**\_lectura genérica de inscripción \_**</span><span class="sxs-lookup"><span data-stu-id="14395-128"><span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**ENLISTMENT\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14395-129">0x20001</span><span class="sxs-lookup"><span data-stu-id="14395-129">0x20001</span></span>
</dt> <dt>



<span data-ttu-id="14395-130">El autor de la llamada tiene los privilegios siguientes: **\_ \_ información** de la consulta de inscripción y de **\_ \_ lectura de derechos estándar** .</span><span class="sxs-lookup"><span data-stu-id="14395-130">The caller has the following privileges: **STANDARD\_RIGHTS\_READ** and **ENLISTMENT\_QUERY\_INFORMATION**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="14395-131"><span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**\_escritura genérica de inscripción \_**</span><span class="sxs-lookup"><span data-stu-id="14395-131"><span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**ENLISTMENT\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14395-132">0x2001E</span><span class="sxs-lookup"><span data-stu-id="14395-132">0x2001E</span></span>
</dt> <dt>



<span data-ttu-id="14395-133">El autor de la llamada tiene los siguientes privilegios: **\_ \_ escritura de derechos estándar**, **información de \_ conjunto \_ de inscripción** y **\_ recuperación de inscripción**.</span><span class="sxs-lookup"><span data-stu-id="14395-133">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **ENLISTMENT\_SET\_INFORMATION**, and **ENLISTMENT\_RECOVER**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="14395-134"><span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**\_ejecución genérica de inscripción \_**</span><span class="sxs-lookup"><span data-stu-id="14395-134"><span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**ENLISTMENT\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14395-135">0x2001C</span><span class="sxs-lookup"><span data-stu-id="14395-135">0x2001C</span></span>
</dt> <dt>



<span data-ttu-id="14395-136">El autor de la llamada tiene los siguientes privilegios: **derechos estándar de \_ \_ ejecución**, **\_ recuperación de alta** y **inscripción \_ subordinada \_**.</span><span class="sxs-lookup"><span data-stu-id="14395-136">The caller has the following privileges: **STANDARD\_RIGHTS\_EXECUTE**, **ENLISTMENT\_RECOVER**, and **ENLISTMENT\_SUBORDINATE\_RIGHTS**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="14395-137"><span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**DAR de alta \_ todo el \_ acceso**</span><span class="sxs-lookup"><span data-stu-id="14395-137"><span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**ENLISTMENT\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14395-138">0xF001F</span><span class="sxs-lookup"><span data-stu-id="14395-138">0xF001F</span></span>
</dt> <dt>



<span data-ttu-id="14395-139">Este valor establece todos los bits válidos para un valor de acceso de inscripción.</span><span class="sxs-lookup"><span data-stu-id="14395-139">This value sets all valid bits for an enlistment access value.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14395-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14395-140">Requirements</span></span>



| <span data-ttu-id="14395-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="14395-141">Requirement</span></span> | <span data-ttu-id="14395-142">Value</span><span class="sxs-lookup"><span data-stu-id="14395-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="14395-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14395-143">Minimum supported client</span></span><br/> | <span data-ttu-id="14395-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14395-144">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="14395-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14395-145">Minimum supported server</span></span><br/> | <span data-ttu-id="14395-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14395-146">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="14395-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14395-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="14395-148"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="14395-148"><dt>WinNT.h</dt></span></span> </dl> |



 

 




