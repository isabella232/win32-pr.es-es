---
title: Atributos de llamada de función
description: Los programas pueden usar estos atributos en funciones individuales dentro de la interfaz y solo afectan a esa función.
ms.assetid: c54dbcd9-46c9-4755-b4a8-0f78068920b7
keywords:
- IDL MIDL, atributos, llamada a función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d53407abf464d7b201c49d9cb2b1d3f3625b9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159578"
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

 

 




