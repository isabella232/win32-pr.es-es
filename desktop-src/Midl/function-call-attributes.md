---
title: Atributos de llamada de función
description: Los programas pueden usar estos atributos en funciones individuales dentro de la interfaz y solo afectan a esa función.
ms.assetid: c54dbcd9-46c9-4755-b4a8-0f78068920b7
keywords:
- IDL MIDL, atributos, llamada a función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3800b62bb6b94aac330ecf0b06761d62227a4ed6100f2fabdde5b61cd952d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895315"
---
# <a name="function-call-attributes"></a>Atributos de llamada de función

Los programas pueden usar estos atributos en funciones individuales dentro de la interfaz y solo afectan a esa función.



| Atributo                        | Uso                                                                                                                                                                                                                                                      |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Mensaje**](message.md)       | La llamada a procedimiento remoto se va a tratar como un mensaje asincrónico desde el cliente al servidor. El cliente realiza la llamada y devuelve inmediatamente, mientras que el transporte message-queuing [**(ncadg \_ mq)**](ncadg-mq.md)controla la llamada real. |
| [**quizás**](maybe.md)           | El cliente que realiza esta llamada a procedimiento remoto no espera ninguna respuesta que indique la entrega o finalización de la llamada. Esto contrasta con las [**operaciones de**](message.md) mensaje en las que no se espera ninguna respuesta, pero se garantiza la entrega.        |
| [**Difusión**](broadcast.md)   | La llamada a procedimiento remoto se enviará a todos los servidores de la red. El cliente acepta la primera devolución y se descartan las respuestas posteriores de otros servidores.                                                                                    |
| [**idempotent**](idempotent.md) | La llamada no cambia el estado y devuelve la misma información cada vez que se llama con los mismos parámetros de entrada.                                                                                                                                     |
| [**devolución de llamada**](callback.md)     | Designa una función que reside en la aplicación cliente, a la que el servidor puede llamar para obtener información del cliente.                                                                                                                             |
| [**llamar \_ a como**](call-as.md)      | Mapas una función no remotable a una llamada a procedimiento remoto.                                                                                                                                                                                                   |
| [**Local**](local.md)           | Designa un procedimiento local para el que MIDL no genera código auxiliar.                                                                                                                                                                                   |



 

En las interfaces [**que**](object.md) no son de objeto, también puede aplicar el atributo [**de \_**](context-handle.md) identificador de contexto a una función para especificar las características del valor devuelto.

 

 




