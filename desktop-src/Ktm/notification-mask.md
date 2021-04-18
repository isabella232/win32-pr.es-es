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
# <a name="notification_mask"></a>máscara de notificación \_

Enumera los distintos tipos de notificaciones que puede recibir una inscripción.

<dl> <dt>

<span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**\_máscara de notificación de transacción \_**
</dt> <dd> <dl> <dt>

0x3FFFFFFF
</dt> <dt>



Máscara que indica todos los bits válidos para una notificación de transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**prepreparación de \_ notificaciones de transacción \_**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Se llama a esta notificación después de que un cliente llame a [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) y ningún administrador de recursos (RM) admita la confirmación en una fase o un administrador de transacciones superior (TM) llame a [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment). El RMs recibe esta notificación que indica que deben completar cualquier trabajo que pueda hacer que otro RMs tenga que darse de alta en una transacción, como vaciar su memoria caché. Después de completar estas operaciones, RM debe llamar a [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete). Para recibir esta notificación, RM también debe admitir la **\_ \_ confirmación** de la notificación de transacciones **\_ \_ preparar** y la notificación de transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**\_preparar notificación de transacción \_**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Se llama a esta notificación después de que se complete el procesamiento de **\_ \_ prepreparación** de la transacción. Indica a RM que complete todo el trabajo asociado a esta inscripción para que pueda garantizar que una operación de confirmación puede realizarse correctamente y también se puede realizar una operación de anulación. Normalmente, la mayor parte del trabajo de una transacción se realiza durante la fase de preparación. En el caso de RMs duradero, deben registrar su estado antes de llamar a la función [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) . Esta es la última oportunidad para que el RM solicite que se revierta la transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**\_confirmación de notificación de transacción \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Esta notificación indica a RM que complete todo el trabajo asociado a esta inscripción. Normalmente, el RM libera los bloqueos, libera cualquier información necesaria para revertir la transacción. El RM debe responder llamando a la función [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) cuando haya finalizado estas operaciones.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**reversión de notificación de transacción \_ \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Esta notificación señala al RM para deshacer todo el trabajo que ha hecho que está asociado a la transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**\_finalización de notificación de transacción \_ \_ finalizada**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Esta notificación señala al TM superior que se completó correctamente una operación previa a la preparación.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**preparación de notificación de transacción \_ \_ \_ completada**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Esta notificación señala al TM superior que se completó correctamente una operación de preparación.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**confirmación de notificación de transacción \_ \_ \_ completada**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Esta notificación señala al TM superior que una operación de confirmación se completó correctamente.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**reversión de notificación de transacción \_ \_ \_ completada**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Esta notificación señala al TM superior que se completó correctamente una operación de reversión.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**TRANSACCIÓN de \_ notificación de \_ recuperación**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Esta notificación señala a RMs que debe recuperar su estado porque debe reenviarse un resultado de la transacción. Por ejemplo, cuando se recupera un RM y cuando hay transacciones pendientes. Esta notificación se entrega una vez que se resuelve el estado dudoso.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**\_confirmación de \_ una sola \_ fase \_ de notificación de transacción**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Esta notificación indica al RM que complete y confirme la transacción sin usar un protocolo de confirmación en dos fases. Si el RM quiere usar una operación en dos fases, debe responder llamando a la función [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) .


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**\_confirmación de \_ delegado de notificación de transacción \_**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



KTM está señalando al TM superior para realizar una operación de confirmación.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**\_consulta de notificación de \_ recuperación de transacción \_**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



KTM está señalando al TM superior para consultar el estado de una transacción dudosa.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**prepreparación de \_ notificaciones de notificación de transacción \_ \_**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Esta notificación señala al TM superior que las notificaciones de prepreparación deben entregarse en la inscripción especificada.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**\_ \_ última \_ recuperación de la notificación de transacción**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Esta notificación indica que la operación de recuperación se ha completado para este RM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**induda de la notificación de transacción \_ \_**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



La transacción especificada se encuentra en un estado dudoso. El RM recibe esta notificación durante las operaciones de recuperación cuando se ha preparado una transacción, pero no hay ningún administrador de transacciones superior (TM) disponible. Por ejemplo, cuando una transacción implica un TM remoto y ese nodo no está disponible, su nodo no está disponible o el servicio local [Coordinador de transacciones distribuidas](/previous-versions/windows/desktop/ms684146(v=vs.85)) no está disponible, el estado de la transacción es dudoso.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**TRANSACCIÓN \_ Notify \_ TM \_ en línea**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



TM está en línea y acepta solicitudes.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**\_resultado de \_ solicitud de notificación de transacción \_**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Señala a RMs que hay información de resultados disponible y que se debe realizar una solicitud de esa información.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**\_Finalizar notificación de \_ confirmación \_ de transacción**
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
| Encabezado<br/>                   | <dl> <dt>KtmTypes. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Coordinador de transacciones distribuidas](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> <dt>

[Constantes del administrador de transacciones de kernel](kernel-transaction-manager-constants.md)
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

[**notificación de transacción \_**](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 

