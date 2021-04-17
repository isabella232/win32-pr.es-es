---
description: Después de cualquier tipo de error que interrumpa el procesamiento de transacciones normal, KTM y cada administrador de recursos deben realizar operaciones de recuperación. La recuperación es el proceso por el que llegan los participantes de la transacción en una vista coherente de cada estado de las transacciones.
ms.assetid: 5bc9a155-6ba4-41f8-8e12-e87f48d83940
title: Procesamiento de recuperación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8e74d4f8bff3e56af03b017522212e7a02e232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687395"
---
# <a name="recovery-processing"></a>Procesamiento de recuperación

Después de cualquier tipo de error que interrumpa el procesamiento de transacciones normal, KTM y cada administrador de recursos deben realizar operaciones de *recuperación* . La recuperación es el proceso por el que llegan los participantes de la transacción en una vista coherente del estado de cada transacción.

Es posible que los administradores de recursos estén *en duda* sobre el resultado de una transacción, lo que significa que, en el momento en que se produjo el error, han recibido una notificación de preparación de una transacción \_ \_ , había preparado el almacenamiento duradero, pero no se ha recibido (o recibido pero no registrado) el resultado final de la transacción. Del mismo modo, KTM puede ser dudoso sobre una transacción si se había preparado pero no se ha recibido (o recibido pero no registrado) un resultado. En el momento de la recuperación, se deben volver a enviar todos los resultados enviados pero no confirmados. Por ejemplo, si un administrador de recursos ha recibido una notificación de confirmación de notificación de transacción y se ha \_ \_ llamado a la función [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) , es posible que el RM siga recibiendo una notificación de confirmación de notificación de transacción duplicada \_ \_ en el momento de la recuperación.

Para que una transacción se recupere correctamente después de un error del sistema o del administrador de recursos, cada administrador de recursos debe hacer lo siguiente cada vez que se inicia:

1.  Llame a la función [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) para volver a abrir su identificador de Resource Manager usando su nombre único y persistente. Esto informa a KTM de que el administrador de recursos se está ejecutando de nuevo y está disponible para realizar la recuperación. Si no existe ninguna inscripción para recuperarla, se puede producir un error en la llamada a **OpenResourceManager** . Llame a [**CreateResourceManager (**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) para volver a crear el objeto RM.
2.  Llame a [**RecoverResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager). El administrador de recursos recibirá un evento de notificación de notificaciones de [**\_ \_ recuperación de transacciones**](notification-mask.md) para cada inscripción para la que necesite realizar operaciones de recuperación, seguida de una notificación de la \_ \_ última recuperación de la transacción \_ . El evento de notificación incluye un identificador único global para la transacción y la inscripción.
3.  Llame a la función [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) para volver a abrir cada identificador de inscripción para el que el administrador de recursos haya recibido una notificación de solicitud de recuperación de la transacción \_ \_ .
4.  Para cada inscripción abierta por [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment), llame a [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment). Esto hace que se vuelvan a entregar la notificación de confirmación de notificación de transacción o de notificaciones \_ \_ \_ \_ de transacción.
5.  Si la transacción recibida de RM \_ notifica la \_ confirmación, el RM puede completar la transacción llamando a [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete).

    Si la transacción recibida de RM \_ notifica inadvertidamente \_ , el RM debe esperar a que llegue la notificación de resultados.

6.  En el caso de las transacciones que el RM no recibe, se notifica una \_ \_ notificación de recuperación de una transacción, pero anteriormente recibió una \_ notificación de notificaciones \_ de preparación para, el RM debe procesar la transacción como si se revirtió.

> [!Note]
>
> Los administradores de recursos pueden dar de alta o crear nuevas transacciones mientras están en proceso de realizar la recuperación.

 

KTM usa un modelo de transacción *presunta anulación* . En el escenario siguiente se muestra este comportamiento. Supongamos que KTM y un administrador de recursos existen en el mismo equipo. Suponga que KTM emite una notificación de preparación para una transacción, pero el sistema se bloquea antes de que KTM registre la notificación de preparación. Supongamos que el administrador de recursos recibe y registra la notificación de preparación justo antes de que se bloquee el sistema. Una vez restaurado el sistema, KTM no tiene ningún conocimiento de la transacción, porque nunca registró la fase de preparación. El administrador de recursos tiene conocimiento de la transacción, porque recibió, procesó y registró la notificación de preparación. Cuando KTM emite las notificaciones de recuperación, el administrador de recursos no incluye una notificación de recuperación para la transacción en cuestión. Con el modelo de anulación supuesto, el administrador de recursos en este caso tratará la transacción preparada como anulada cuando no reciba notificaciones para realizar la recuperación en esa transacción.

 

 



