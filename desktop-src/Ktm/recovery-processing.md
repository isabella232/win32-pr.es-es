---
description: Después de cualquier tipo de error que interrumpa el procesamiento normal de transacciones, KTM y cada administrador de recursos deben realizar operaciones de recuperación. La recuperación es el proceso por el que los participantes de la transacción llegan a una vista coherente del estado de cada transacción.
ms.assetid: 5bc9a155-6ba4-41f8-8e12-e87f48d83940
title: Procesamiento de recuperación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec99ad63d18c95da3ebb3ad5db6c204301d75336cc1842dd21e1edf79f5f9a38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146498"
---
# <a name="recovery-processing"></a>Procesamiento de recuperación

Después de cualquier tipo de error que interrumpa el procesamiento normal de transacciones, KTM y cada administrador de recursos deben realizar operaciones *de recuperación.* La recuperación es el proceso por el que los participantes de la transacción llegan a una vista coherente del estado de cada transacción.

Los administradores  de recursos pueden tener dudas sobre el resultado de una transacción, lo que significa que, en el momento del error, han recibido una notificación TRANSACTION NOTIFY PREPARE, se han preparado para un almacenamiento duradero, pero no han recibido (o recibido, pero no registrado) un resultado final para \_ la \_ transacción. De forma similar, KTM puede tener dudas sobre una transacción si se había preparado pero no había recibido (o no registrado) un resultado. En tiempo de recuperación, se deben volver a enviar todos los resultados que se han enviado pero no se han reconocido. Por ejemplo, si un administrador de recursos recibió una notificación TRANSACTION NOTIFY COMMIT y llamó a la función CommitComplete, es posible que rm reciba una notificación TRANSACTION NOTIFY COMMIT duplicada en el momento de la \_ \_ [](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) \_ \_ recuperación.

Para que una transacción se recupere correctamente después de un error del sistema o del administrador de recursos, cada administrador de recursos debe hacer lo siguiente cada vez que se inicia:

1.  Llame a [**la función OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) para volver a abrir su identificador de Resource Manager con su nombre único y persistente. Esto informa a KTM de que el administrador de recursos se está ejecutando de nuevo y está disponible para realizar la recuperación. Si no existe ninguna lista para recuperarse, se puede producir un error en la **llamada a OpenResourceManager.** Llame [**a CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) para volver a crear el objeto RM.
2.  Llame [**a RecoverResourceManager.**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager) El administrador de recursos recibirá un evento de notificación [**TRANSACTION \_ NOTIFY \_ RECOVER**](notification-mask.md) para cada registro para el que necesite realizar operaciones de recuperación, seguido de TRANSACTION \_ NOTIFY LAST \_ \_ RECOVER. El evento de notificación incluye un identificador único global para la transacción y la alta.
3.  Llame a [**la función OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) para volver a abrir cada identificador de registro para el que el administrador de recursos recibió una notificación \_ TRANSACTION NOTIFY \_ RECOVER.
4.  Para cada registro abierto por [**OpenEnlistment,**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)llame a [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment). Esto hace que se reenvíe la notificación TRANSACTION NOTIFY COMMIT o \_ \_ TRANSACTION NOTIFY \_ \_ INDOUBT.
5.  Si el RM recibió TRANSACTION \_ NOTIFY \_ COMMIT, el RM puede completar la transacción llamando a [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete).

    Si el RM recibió TRANSACTION \_ NOTIFY \_ INDOUBT, el rm debe esperar a que llegue la notificación de resultados.

6.  En el caso de las transacciones para las que el RM no recibe una notificación TRANSACTION NOTIFY RECOVER, pero que previamente recibió una notificación TRANSACTION NOTIFY PREPARE para , el rm debe procesar la transacción como si se \_ \_ \_ \_ revierte.

> [!Note]
>
> Los administradores de recursos pueden dar de alta o crear nuevas transacciones mientras se realiza la recuperación.

 

KTM usa un *modelo de transacción de anulación* supuesto. En el escenario siguiente se muestra este comportamiento. Suponga que KTM y un administrador de recursos existen en el mismo equipo. Supongamos que KTM emite una notificación de preparación para una transacción, pero el sistema se bloquea antes de que KTM registra la notificación de preparación. Supongamos además que el administrador de recursos recibe y registra la notificación de preparación justo antes de que se bloquea el sistema. Una vez restaurado el sistema, KTM no tiene conocimiento de la transacción, ya que nunca registró la fase de preparación. El administrador de recursos tiene conocimiento de la transacción, ya que recibió, procesó y registró la notificación de preparación. Cuando KTM emite sus notificaciones de recuperación, el administrador de recursos no incluye una notificación de recuperación para la transacción en cuestión. Con el modelo de anulación supuesto, el administrador de recursos en este caso tratará la transacción preparada como anulada cuando no reciba notificaciones para realizar la recuperación en esa transacción.

 

 



