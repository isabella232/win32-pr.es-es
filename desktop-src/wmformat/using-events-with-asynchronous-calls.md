---
title: Usar eventos con llamadas asincrónicas
description: Usar eventos con llamadas asincrónicas
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- SDK de Windows Media Format, eventos con llamadas asincrónicas
- SDK de Windows Media Format, eventos de llamada asincrónica
- eventos, llamadas asincrónicas
- eventos de llamada asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1729108cae5b73ec96be208709c1360e9401ac0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419028"
---
# <a name="using-events-with-asynchronous-calls"></a>Usar eventos con llamadas asincrónicas

Con frecuencia, al utilizar métodos a los que se llama de forma asincrónica, querrá detener el procesamiento de la aplicación hasta que el método complete el procesamiento. Puede implementar cualquier técnica que desee para controlar esta situación. En esta sección se describe el uso de un evento para esperar llamadas asincrónicas en el subproceso que realiza la llamada. Esta técnica se usa con frecuencia con el SDK de Windows Media Format y se muestra en algunas de las aplicaciones de ejemplo.

En la lista siguiente se resume el uso de eventos para esperar llamadas asincrónicas.

1.  Cree un evento para usarlo con la aplicación mediante una llamada a la función **CreateEvent** del SDK de la plataforma.
2.  Al implementar las devoluciones de llamada adecuadas para la aplicación, Capture los mensajes que debe esperar. En la lógica de control de mensajes para los mensajes deseados, señale el evento llamando a la función **SetEvent** del SDK de la plataforma.
3.  Después de que se realicen llamadas a eventos asincrónicos en la aplicación, espere a que el evento señale llamando a la función **WaitForSingleObject** del SDK de la plataforma. Si diseña una aplicación para Windows, debe crear un bucle para comprobar los mensajes de Windows e incluir una llamada a **WaitForSingleObject** en el bucle con un breve tiempo de espera.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar los métodos de devolución de llamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




