---
title: Uso de eventos con llamadas asincrónicas
description: Uso de eventos con llamadas asincrónicas
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- Windows SDK de formato multimedia, eventos con llamadas asincrónicas
- Windows SDK de formato multimedia, eventos de llamada asincrónica
- events,asynchronous calls
- eventos de llamada asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd315b56570419afd81aa3300cfa3ee1dd907e22310aba79432e4533f99a82db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929135"
---
# <a name="using-events-with-asynchronous-calls"></a>Uso de eventos con llamadas asincrónicas

Con frecuencia, al usar métodos a los que se llama de forma asincrónica, querrá detener el procesamiento adicional de la aplicación hasta que el método complete el procesamiento. Puede implementar cualquier técnica que quiera para controlar esta situación. En esta sección se describe el uso de un evento para esperar llamadas asincrónicas en el subproceso que realiza la llamada. Esta técnica se usa con frecuencia con Windows SDK de formato multimedia y se muestra en algunas de las aplicaciones de ejemplo.

En la lista siguiente se resume el uso de eventos para esperar llamadas asincrónicas.

1.  Cree un evento para usarlo con la aplicación mediante una llamada a la **función CreateEvent** del SDK de plataforma.
2.  Al implementar las devoluciones de llamada adecuadas para la aplicación, se capturan los mensajes para los que debe esperar. En la lógica de control de mensajes para los mensajes deseados, señale el evento mediante una llamada a la **función SetEvent** del SDK de plataforma.
3.  Después de realizar llamadas a eventos asincrónicos en la aplicación, espere a que el evento señale mediante una llamada a la **función WaitForSingleObject** del SDK de plataforma. Si está diseñando una aplicación Windows, debe crear un bucle para comprobar si hay mensajes de Windows e incluir una llamada a **WaitForSingleObject** en el bucle con un breve tiempo de espera.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar los métodos de devolución de llamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




