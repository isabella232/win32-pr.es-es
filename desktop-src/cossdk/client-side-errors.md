---
description: Client-Side errores
ms.assetid: 95fb2ef1-eec2-4c74-891a-617450098160
title: Client-Side errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef309858d1527fdcabe0f487de87df19d20635c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073008"
---
# <a name="client-side-errors"></a>Client-Side errores

Los errores del lado cliente se controlan de forma similar a los errores del lado servidor. [Message Queuing puede](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) mover un mensaje a su cola de destino si, por ejemplo, el mensaje no se puede mover de cliente a servidor. En este caso, el mensaje se mueve a la cola de mensajes no enviados del lado cliente.

El servicio de componentes en cola de COM+ supervisa la cola de mensajes no enviados. Si se han movido mensajes, el servicio de componentes en cola crea una instancia de la clase de excepción y llama a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para solicitar [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol). Si esto se realiza correctamente, el monitor de cola de mensajes fallidos invoca [**a IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).

El objeto puede realizar alguna acción para invertir el efecto de una transacción anterior. Si se confirma la reproducción, el mensaje se quita de la cola de mensajes no enviados de Xact. Si se produce un error en la reproducción o el CLSID y la interfaz necesarios no están disponibles, el mensaje permanece en la cola de mensajes no enviados de Xact.

Si necesita intervención en el proceso descrito anteriormente o si necesita mover un mensaje dudoso de su cola de reposo final, use la utilidad de mover mensajes. Para obtener más información sobre la utilidad de mover mensajes, vea [Controlar errores.](handling-errors-in-queued-components.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Errores Client-Side persistentes](persistent-client-side-failures.md)
</dt> <dt>

[Errores del lado servidor](server-side-errors.md)
</dt> </dl>

 

 
