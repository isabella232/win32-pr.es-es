---
title: Atributos de llamada de función
description: Los programas pueden utilizar estos atributos en funciones individuales dentro de la interfaz y solo afectan a esa función.
ms.assetid: c54dbcd9-46c9-4755-b4a8-0f78068920b7
keywords:
- MIDL, atributos, llamada de función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d53407abf464d7b201c49d9cb2b1d3f3625b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779620"
---
# <a name="function-call-attributes"></a>Atributos de llamada de función

Los programas pueden utilizar estos atributos en funciones individuales dentro de la interfaz y solo afectan a esa función.



| Atributo                        | Uso                                                                                                                                                                                                                                                      |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Mensaje**](message.md)       | La llamada a procedimiento remoto se tratará como un mensaje asíncrono desde el cliente al servidor. El cliente realiza la llamada y se devuelve inmediatamente, mientras que la llamada real se controla mediante el transporte de cola de mensajes ([**ncadg \_ MQ**](ncadg-mq.md)). |
| [**incluso**](maybe.md)           | El cliente que realiza esta llamada a procedimiento remoto no espera ninguna respuesta que indique la entrega o la finalización de la llamada. Esto contrasta con las operaciones de [**mensajes**](message.md) en las que no se espera ninguna respuesta, pero se garantiza la entrega.        |
| [**amplia**](broadcast.md)   | La llamada a procedimiento remoto se va a enviar a todos los servidores de la red. El cliente acepta la primera devolución, las respuestas posteriores de otros servidores se descartan.                                                                                    |
| [**idempotent**](idempotent.md) | La llamada no cambia el estado y devuelve la misma información cada vez que se llama con los mismos parámetros de entrada.                                                                                                                                     |
| [**devolución de llamada**](callback.md)     | Designa una función que reside en la aplicación cliente, a la que el servidor puede llamar para obtener información del cliente.                                                                                                                             |
| [**llamar a \_ como**](call-as.md)      | Asigna una función no utilizables a una llamada a procedimiento remoto.                                                                                                                                                                                                   |
| [**localizar**](local.md)           | Designa un procedimiento local para el que MIDL no genera código auxiliar.                                                                                                                                                                                   |



 

En las interfaces que no son de [**objeto**](object.md) , también puede aplicar el atributo de [**\_ identificador de contexto**](context-handle.md) a una función para especificar las características del valor devuelto.

 

 




