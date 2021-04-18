---
description: Enumera los distintos tipos de notificaciones que puede recibir una inscripción.
ms.assetid: 65db8ba5-193c-439b-8e8c-6cb4a9bd4efd
title: NOTIFICATION_MASK (KtmTypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3650c10f619cf45db34d9172476261838897a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687932"
---
# <a name="notification_mask"></a><span data-ttu-id="5b4f1-103">máscara de notificación \_</span><span class="sxs-lookup"><span data-stu-id="5b4f1-103">NOTIFICATION\_MASK</span></span>

<span data-ttu-id="5b4f1-104">Enumera los distintos tipos de notificaciones que puede recibir una inscripción.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-104">Lists the different types of notifications that can be received by an enlistment.</span></span>

<dl> <dt>

<span data-ttu-id="5b4f1-105"><span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**\_máscara de notificación de transacción \_**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-105"><span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**TRANSACTION\_NOTIFY\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-106">0x3FFFFFFF</span><span class="sxs-lookup"><span data-stu-id="5b4f1-106">0x3FFFFFFF</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-107">Máscara que indica todos los bits válidos para una notificación de transacción.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-107">A mask that indicates all valid bits for a transaction notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-108"><span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**prepreparación de \_ notificaciones de transacción \_**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-108"><span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**TRANSACTION\_NOTIFY\_PREPREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5b4f1-109">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-110">Se llama a esta notificación después de que un cliente llame a [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) y ningún administrador de recursos (RM) admita la confirmación en una fase o un administrador de transacciones superior (TM) llame a [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment).</span><span class="sxs-lookup"><span data-stu-id="5b4f1-110">This notification is called after a client calls [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) and either no resource manager (RM) supports single-phase commit or a superior transaction manager (TM) calls [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment).</span></span> <span data-ttu-id="5b4f1-111">El RMs recibe esta notificación que indica que deben completar cualquier trabajo que pueda hacer que otro RMs tenga que darse de alta en una transacción, como vaciar su memoria caché.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-111">This notification is received by the RMs indicating that they should complete any work that could cause other RMs to need to enlist in a transaction, such as flushing its cache.</span></span> <span data-ttu-id="5b4f1-112">Después de completar estas operaciones, RM debe llamar a [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete).</span><span class="sxs-lookup"><span data-stu-id="5b4f1-112">After completing these operations the RM must call [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete).</span></span> <span data-ttu-id="5b4f1-113">Para recibir esta notificación, RM también debe admitir la **\_ \_ confirmación** de la notificación de transacciones **\_ \_ preparar** y la notificación de transacción.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-113">To receive this notification the RM must also support **TRANSACTION\_NOTIFY\_PREPARE** and **TRANSACTION\_NOTIFY\_COMMIT**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-114"><span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**\_preparar notificación de transacción \_**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-114"><span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**TRANSACTION\_NOTIFY\_PREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-115">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5b4f1-115">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-116">Se llama a esta notificación después de que se complete el procesamiento de **\_ \_ prepreparación** de la transacción.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-116">This notification is called after the **TRANSACTION\_NOTIFY\_PREPREPARE** processing is complete.</span></span> <span data-ttu-id="5b4f1-117">Indica a RM que complete todo el trabajo asociado a esta inscripción para que pueda garantizar que una operación de confirmación puede realizarse correctamente y también se puede realizar una operación de anulación.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-117">It signals the RM to complete all the work that is associated with this enlistment so that it can guarantee that a commit operation could succeed and an abort operation could also succeed.</span></span> <span data-ttu-id="5b4f1-118">Normalmente, la mayor parte del trabajo de una transacción se realiza durante la fase de preparación.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-118">Typically, the bulk of the work for a transaction is done during the prepare phase.</span></span> <span data-ttu-id="5b4f1-119">En el caso de RMs duradero, deben registrar su estado antes de llamar a la función [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) .</span><span class="sxs-lookup"><span data-stu-id="5b4f1-119">For durable RMs, they must log their state prior to calling the [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) function.</span></span> <span data-ttu-id="5b4f1-120">Esta es la última oportunidad para que el RM solicite que se revierta la transacción.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-120">This is the last chance for the RM to request that the transaction be rolled back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-121"><span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**\_confirmación de notificación de transacción \_**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-121"><span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**TRANSACTION\_NOTIFY\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-122">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5b4f1-122">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-123">Esta notificación indica a RM que complete todo el trabajo asociado a esta inscripción.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-123">This notification signals the RM to complete all the work that is associated with this enlistment.</span></span> <span data-ttu-id="5b4f1-124">Normalmente, el RM libera los bloqueos, libera cualquier información necesaria para revertir la transacción.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-124">Typically, the RM releases any locks, releases any information necessary to roll back the transaction.</span></span> <span data-ttu-id="5b4f1-125">El RM debe responder llamando a la función [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) cuando haya finalizado estas operaciones.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-125">The RM must respond by calling the [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) function when it has finished these operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-126"><span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**reversión de notificación de transacción \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-126"><span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**TRANSACTION\_NOTIFY\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-127">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5b4f1-127">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-128">Esta notificación señala al RM para deshacer todo el trabajo que ha hecho que está asociado a la transacción.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-128">This notification signals the RM to undo all the work it has done that is associated with the transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-129"><span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**\_finalización de notificación de transacción \_ \_ finalizada**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-129"><span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**TRANSACTION\_NOTIFY\_PREPREPARE\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-130">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b4f1-130">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-131">Esta notificación señala al TM superior que se completó correctamente una operación previa a la preparación.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-131">This notification signals to the superior TM that a pre-prepare operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-132"><span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**preparación de notificación de transacción \_ \_ \_ completada**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-132"><span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**TRANSACTION\_NOTIFY\_PREPARE\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-133">0x00000020</span><span class="sxs-lookup"><span data-stu-id="5b4f1-133">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-134">Esta notificación señala al TM superior que se completó correctamente una operación de preparación.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-134">This notification signals to the superior TM that a prepare operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-135"><span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**confirmación de notificación de transacción \_ \_ \_ completada**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-135"><span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**TRANSACTION\_NOTIFY\_COMMIT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-136">0x00000040</span><span class="sxs-lookup"><span data-stu-id="5b4f1-136">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-137">Esta notificación señala al TM superior que una operación de confirmación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-137">This notification signals to the superior TM that a commit operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-138"><span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**reversión de notificación de transacción \_ \_ \_ completada**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-138"><span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**TRANSACTION\_NOTIFY\_ROLLBACK\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-139">0x00000080</span><span class="sxs-lookup"><span data-stu-id="5b4f1-139">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-140">Esta notificación señala al TM superior que se completó correctamente una operación de reversión.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-140">This notification signals to the superior TM that a rollback operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-141"><span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**TRANSACCIÓN de \_ notificación de \_ recuperación**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-141"><span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**TRANSACTION\_NOTIFY\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-142">0x00000100</span><span class="sxs-lookup"><span data-stu-id="5b4f1-142">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-143">Esta notificación señala a RMs que debe recuperar su estado porque debe reenviarse un resultado de la transacción.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-143">This notification signals to RMs that they should recover their state because a transaction outcome must be redelivered.</span></span> <span data-ttu-id="5b4f1-144">Por ejemplo, cuando se recupera un RM y cuando hay transacciones pendientes.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-144">For example, when an RM is recovered, and when there are transactions left in-doubt.</span></span> <span data-ttu-id="5b4f1-145">Esta notificación se entrega una vez que se resuelve el estado dudoso.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-145">This notification is delivered once the in-doubt state is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-146"><span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**\_confirmación de \_ una sola \_ fase \_ de notificación de transacción**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-146"><span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**TRANSACTION\_NOTIFY\_SINGLE\_PHASE\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-147">0x00000200</span><span class="sxs-lookup"><span data-stu-id="5b4f1-147">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-148">Esta notificación indica al RM que complete y confirme la transacción sin usar un protocolo de confirmación en dos fases.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-148">This notification signals the RM to complete and commit the transaction without using a two-phase commit protocol.</span></span> <span data-ttu-id="5b4f1-149">Si el RM quiere usar una operación en dos fases, debe responder llamando a la función [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) .</span><span class="sxs-lookup"><span data-stu-id="5b4f1-149">If the RM wants to use a two-phase operation, it must respond by calling the [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-150"><span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**\_confirmación de \_ delegado de notificación de transacción \_**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-150"><span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**TRANSACTION\_NOTIFY\_DELEGATE\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-151">0x00000400</span><span class="sxs-lookup"><span data-stu-id="5b4f1-151">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-152">KTM está señalando al TM superior para realizar una operación de confirmación.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-152">KTM is signaling to the superior TM to perform a commit operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-153"><span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**\_consulta de notificación de \_ recuperación de transacción \_**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-153"><span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**TRANSACTION\_NOTIFY\_RECOVER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-154">0x00000800</span><span class="sxs-lookup"><span data-stu-id="5b4f1-154">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-155">KTM está señalando al TM superior para consultar el estado de una transacción dudosa.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-155">KTM is signaling to the superior TM to query the status of an in-doubt transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-156"><span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**prepreparación de \_ notificaciones de notificación de transacción \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-156"><span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**TRANSACTION\_NOTIFY\_ENLIST\_PREPREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-157">0x00001000</span><span class="sxs-lookup"><span data-stu-id="5b4f1-157">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-158">Esta notificación señala al TM superior que las notificaciones de prepreparación deben entregarse en la inscripción especificada.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-158">This notification signals to the superior TM that pre-prepare notifications must be delivered on the specified enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-159"><span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**\_ \_ última \_ recuperación de la notificación de transacción**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-159"><span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**TRANSACTION\_NOTIFY\_LAST\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-160">0x00002000</span><span class="sxs-lookup"><span data-stu-id="5b4f1-160">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-161">Esta notificación indica que la operación de recuperación se ha completado para este RM.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-161">This notification indicates that the recovery operation is complete for this RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-162"><span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**induda de la notificación de transacción \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-162"><span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**TRANSACTION\_NOTIFY\_INDOUBT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-163">0x00004000</span><span class="sxs-lookup"><span data-stu-id="5b4f1-163">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-164">La transacción especificada se encuentra en un estado dudoso.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-164">The specified transaction is in an in-doubt state.</span></span> <span data-ttu-id="5b4f1-165">El RM recibe esta notificación durante las operaciones de recuperación cuando se ha preparado una transacción, pero no hay ningún administrador de transacciones superior (TM) disponible.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-165">The RM receives this notification during recovery operations when a transaction has been prepared, but there is no superior transaction manager (TM) available.</span></span> <span data-ttu-id="5b4f1-166">Por ejemplo, cuando una transacción implica un TM remoto y ese nodo no está disponible, su nodo no está disponible o el servicio local [Coordinador de transacciones distribuidas](/previous-versions/windows/desktop/ms684146(v=vs.85)) no está disponible, el estado de la transacción es dudoso.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-166">For example, when a transaction involves a remote TM and that node is unavailable, its node is unavailable, or the local [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) service is unavailable, the transaction state is in-doubt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-167"><span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**TRANSACCIÓN \_ Notify \_ TM \_ en línea**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-167"><span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**TRANSACTION\_NOTIFY\_TM\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-168">0x02000000</span><span class="sxs-lookup"><span data-stu-id="5b4f1-168">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-169">TM está en línea y acepta solicitudes.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-169">The TM is online and accepting requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-170"><span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**\_resultado de \_ solicitud de notificación de transacción \_**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-170"><span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**TRANSACTION\_NOTIFY\_REQUEST\_OUTCOME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-171">0x20000000</span><span class="sxs-lookup"><span data-stu-id="5b4f1-171">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-172">Señala a RMs que hay información de resultados disponible y que se debe realizar una solicitud de esa información.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-172">Signals to RMs that there is outcome information available, and that a request for that information should be made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4f1-173"><span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**\_Finalizar notificación de \_ confirmación \_ de transacción**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-173"><span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**TRANSACTION\_NOTIFY\_COMMIT\_FINALIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b4f1-174">0x40000000</span><span class="sxs-lookup"><span data-stu-id="5b4f1-174">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="5b4f1-175">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-175">Reserved.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b4f1-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b4f1-176">Requirements</span></span>



| <span data-ttu-id="5b4f1-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b4f1-177">Requirement</span></span> | <span data-ttu-id="5b4f1-178">Value</span><span class="sxs-lookup"><span data-stu-id="5b4f1-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b4f1-179">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b4f1-179">Minimum supported client</span></span><br/> | <span data-ttu-id="5b4f1-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b4f1-180">Windows Vista</span></span><br/>                                                                                  |
| <span data-ttu-id="5b4f1-181">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b4f1-181">Minimum supported server</span></span><br/> | <span data-ttu-id="5b4f1-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b4f1-182">Windows Server 2008</span></span><br/>                                                                            |
| <span data-ttu-id="5b4f1-183">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b4f1-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b4f1-184"><dt>KtmTypes. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b4f1-184"><dt>KtmTypes.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b4f1-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b4f1-185">See also</span></span>

<dl> <dt>

<span data-ttu-id="5b4f1-186">[Coordinador de transacciones distribuidas](/previous-versions/windows/desktop/ms684146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5b4f1-186">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5b4f1-187">Constantes del administrador de transacciones de kernel</span><span class="sxs-lookup"><span data-stu-id="5b4f1-187">Kernel Transaction Manager Constants</span></span>](kernel-transaction-manager-constants.md)
</dt> <dt>

[<span data-ttu-id="5b4f1-188">**CreateEnlistment**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-188">**CreateEnlistment**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)
</dt> <dt>

[<span data-ttu-id="5b4f1-189">**CommitComplete**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-189">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
</dt> <dt>

[<span data-ttu-id="5b4f1-190">**GetNotificationResourceManager**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-190">**GetNotificationResourceManager**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)
</dt> <dt>

[<span data-ttu-id="5b4f1-191">**GetNotificationResourceManagerAsync**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-191">**GetNotificationResourceManagerAsync**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync)
</dt> <dt>

[<span data-ttu-id="5b4f1-192">**PrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-192">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
</dt> <dt>

[<span data-ttu-id="5b4f1-193">**SinglePhaseReject**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-193">**SinglePhaseReject**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)
</dt> <dt>

[<span data-ttu-id="5b4f1-194">**notificación de transacción \_**</span><span class="sxs-lookup"><span data-stu-id="5b4f1-194">**TRANSACTION\_NOTIFICATION**</span></span>](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 

