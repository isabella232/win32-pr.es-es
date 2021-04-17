---
description: Errores de Client-Side
ms.assetid: 95fb2ef1-eec2-4c74-891a-617450098160
title: Errores de Client-Side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef309858d1527fdcabe0f487de87df19d20635c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705279"
---
# <a name="client-side-errors"></a>Errores de Client-Side

Los errores del lado cliente se controlan de forma similar a los errores del servidor. [Message Queue Server](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) puede trasladar un mensaje a su cola de destino si, por ejemplo, el mensaje no se puede trasladar del cliente al servidor. En este caso, el mensaje se mueve a la cola de mensajes no enviados del lado cliente.

El servicio de componentes en cola de COM+ supervisa la cola de mensajes con problemas de entrega. Si se han migrado los mensajes, el servicio de componentes en cola crea una instancia de la clase de excepción y llama a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para solicitar [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol). Si esto se realiza correctamente, el monitor de cola de mensajes con problemas de entrega invoca [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).

El objeto puede realizar alguna acción para invertir el efecto de una transacción anterior. Si se confirma la reproducción, el mensaje se quita de la cola de mensajes con problemas de entrega Xact. Si se produce un error en la reproducción o el CLSID y la interfaz necesarios no están disponibles, el mensaje permanece en la cola de mensajes con problemas de entrega Xact.

Si necesita intervenir en el proceso descrito anteriormente, o si necesita mover un mensaje dudoso fuera de la cola de salida final, use la utilidad del Movedor de mensajes. Para obtener más información sobre la utilidad del Movedor de mensajes, vea [control de errores](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Errores de Client-Side persistentes](persistent-client-side-failures.md)
</dt> <dt>

[Errores del lado servidor](server-side-errors.md)
</dt> </dl>

 

 
