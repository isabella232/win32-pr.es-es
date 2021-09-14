---
description: Enumera los distintos tipos de notificaciones que puede recibir una alta.
ms.assetid: 65db8ba5-193c-439b-8e8c-6cb4a9bd4efd
title: NOTIFICATION_MASK (KtmTypes.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3650c10f619cf45db34d9172476261838897a5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160028"
---
# <a name="notification_mask"></a>MÁSCARA DE \_ NOTIFICACIÓN

Enumera los distintos tipos de notificaciones que puede recibir una alta.

<dl> <dt>

<span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**TRANSACTION \_ NOTIFY \_ MASK**
</dt> <dd> <dl> <dt>

0x3FFFFFFF
</dt> <dt>



Máscara que indica todos los bits válidos para una notificación de transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**NOTIFICACIÓN \_ DE \_ TRANSACCIÓN PREPREPARE**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Se llama a esta notificación después de que un cliente llame a [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) y ningún administrador de recursos (RM) admita la confirmación de una sola fase o un administrador de transacciones superior (TM) llame a [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment). Los ADMINISTRADORes reciben esta notificación que indica que deben completar cualquier trabajo que pueda provocar que otros HSM necesiten dar de alta en una transacción, como vaciar la memoria caché. Después de completar estas operaciones, el rm debe llamar [**a PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete). Para recibir esta notificación, el RM también debe admitir **TRANSACTION \_ NOTIFY \_ PREPARE** y **TRANSACTION NOTIFY \_ \_ COMMIT**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**PREPARACIÓN DE \_ NOTIFICACIÓN DE \_ TRANSACCIÓN**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Se llama a esta notificación una vez completado el procesamiento **\_ de TRANSACTION NOTIFY \_ PREPREPARE.** Indica al RM que complete todo el trabajo asociado a esta alta para que pueda garantizar que una operación de confirmación se pueda realizar correctamente y que una operación de anulación también se realice correctamente. Normalmente, la mayor parte del trabajo de una transacción se realiza durante la fase de preparación. En el caso de los RMs duraderos, deben registrar su estado antes de llamar a la [**función PrepareComplete.**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) Esta es la última oportunidad para que el rm solicite que se revierte la transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**CONFIRMACIÓN \_ DE NOTIFICACIÓN DE \_ TRANSACCIÓN**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Esta notificación indica al RM que complete todo el trabajo asociado a esta alta. Normalmente, el RM libera los bloqueos y libera la información necesaria para revertir la transacción. El rm debe responder llamando a [**la función CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) cuando haya finalizado estas operaciones.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**REVERSIÓN \_ DE NOTIFICACIÓN \_ DE TRANSACCIÓN**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Esta notificación indica al rm que deshará todo el trabajo que ha realizado que está asociado a la transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**TRANSACTION \_ NOTIFY \_ PREPREPARE \_ COMPLETE**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Esta notificación indica a la tm superior que una operación de preparación previa se completó correctamente.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**TRANSACTION \_ NOTIFY \_ PREPARE \_ COMPLETE**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Esta notificación indica a la tm superior que una operación de preparación se completó correctamente.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**TRANSACTION \_ NOTIFY \_ COMMIT \_ COMPLETE**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Esta notificación indica a la TM superior que una operación de confirmación se completó correctamente.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**TRANSACTION \_ NOTIFY \_ ROLLBACK \_ COMPLETE**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Esta notificación indica a la tm superior que una operación de reversión se completó correctamente.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**TRANSACTION \_ NOTIFY \_ RECOVER**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Esta notificación indica a los HSM que deben recuperar su estado porque se debe volver a entregar un resultado de la transacción. Por ejemplo, cuando se recupera un RM y cuando hay transacciones que quedan en duda. Esta notificación se entrega una vez resuelto el estado dudoso.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**CONFIRMACIÓN DE \_ FASE ÚNICA DE NOTIFICACIÓN DE \_ \_ \_ TRANSACCIÓN**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Esta notificación indica al rm que complete y confirme la transacción sin usar un protocolo de confirmación en dos fases. Si el rm quiere usar una operación en dos fases, debe responder llamando a la [**función SinglePhaseReject.**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**CONFIRMACIÓN \_ DE DELEGADO DE NOTIFICACIÓN DE \_ \_ TRANSACCIÓN**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



KTM señala a la TM superior para realizar una operación de confirmación.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**CONSULTA DE \_ RECUPERACIÓN DE NOTIFICACIÓN \_ DE \_ TRANSACCIÓN**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



KTM señala a la TM superior para consultar el estado de una transacción dudosa.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**TRANSACTION \_ NOTIFY \_ ENLIST \_ PREPREPARE**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Esta notificación indica a la TM superior que las notificaciones previas a la preparación deben entregarse en la lista especificada.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**NOTIFICACIÓN \_ DE TRANSACCIÓN \_ ÚLTIMA \_ RECUPERACIÓN**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Esta notificación indica que la operación de recuperación se ha completado para este rm.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**NOTIFICACIÓN \_ DE \_ TRANSACCIÓN A INDOUBT**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



La transacción especificada está en un estado dudoso. El administrador de recursos recibe esta notificación durante las operaciones de recuperación cuando se ha preparado una transacción, pero no hay ningún administrador de transacciones (TM) superior disponible. Por ejemplo, cuando una transacción implica una TM remota y ese nodo no está disponible, su nodo no está disponible o el servicio [Coordinador de transacciones distribuidas](/previous-versions/windows/desktop/ms684146(v=vs.85)) local no está disponible, el estado de la transacción es dudoso.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**TRANSACTION \_ NOTIFY \_ TM \_ ONLINE**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



La TM está en línea y acepta solicitudes.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**RESULTADO DE \_ LA SOLICITUD DE NOTIFICACIÓN DE \_ \_ TRANSACCIÓN**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Indica a los HSM que hay información de resultados disponible y que se debe realizar una solicitud de esa información.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**TRANSACTION \_ NOTIFY \_ COMMIT \_ FINALIZE**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Reservado.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                            |
| Encabezado<br/>                   | <dl> <dt>KtmTypes.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Coordinador de transacciones distribuidas](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> <dt>

[Constantes del Administrador de transacciones de kernel](kernel-transaction-manager-constants.md)
</dt> <dt>

[**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)
</dt> <dt>

[**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
</dt> <dt>

[**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)
</dt> <dt>

[**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync)
</dt> <dt>

[**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
</dt> <dt>

[**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)
</dt> <dt>

[**NOTIFICACIÓN DE \_ TRANSACCIÓN**](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 

