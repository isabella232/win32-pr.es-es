---
description: La función CreateTimerQueue crea una cola para temporizadores.
ms.assetid: ee85a6c3-3a1d-4f94-9112-cb8247b2a189
title: Colas de temporizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16e0ae30e02ad9fbc8889c0d7b1094895ebec27c3db8b67acf509ee02e9da85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885883"
---
# <a name="timer-queues"></a>Colas de temporizador

La [**función CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) crea una cola para temporizadores. Los temporizadores de esta cola, conocidos como temporizadores de la cola de temporizadores, son objetos *ligeros* que permiten especificar una función de devolución de llamada a la que se llamará cuando llegue el tiempo de vencimiento especificado. Un subproceso del grupo de subprocesos realiza la operación [de espera.](../procthread/thread-pooling.md)

Para agregar un temporizador a la cola, llame a [**la función CreateTimerQueueTimer.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) Para actualizar un temporizador de la cola de temporizador, llame a [**la función ChangeTimerQueueTimer.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) Puede especificar una función de devolución de llamada que ejecutará un subproceso de trabajo desde el grupo de subprocesos cuando expire el temporizador.

Para cancelar un temporizador pendiente, llame a [**la función DeleteTimerQueueTimer.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) Cuando haya terminado con la cola de temporizadores, llame a la [**función DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) para eliminar la cola de temporizador. Los temporizadores pendientes de la cola se cancelan y eliminan.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de colas de temporizador](using-timer-queues.md)
</dt> </dl>

 

 
