---
title: Atributos asincrónicos
description: Cuando un programa invoca un procedimiento en una interfaz, el procedimiento se puede ejecutar de forma sincrónica o asincrónica.
ms.assetid: 3e6c6c13-1524-41b2-96dc-3885eadb847c
keywords:
- MIDL IDL, atributos MIDL, asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aca2276bf1fa5178f1dca3ae4803544066d983
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651359"
---
# <a name="asynchronous-attributes"></a>Atributos asincrónicos

Cuando un programa invoca un procedimiento en una interfaz, el procedimiento se puede ejecutar de forma sincrónica o asincrónica. Un procedimiento sincrónico hace que el programa que realiza la llamada espere hasta que el procedimiento vuelva antes de que el programa pueda continuar. Un procedimiento asincrónico vuelve inmediatamente sin esperar los resultados. Posteriormente, el programa de llamada debe volver a sincronizarse con el procedimiento de interfaz para recibir datos. Para obtener más información, vea [RPC asincrónico](/windows/desktop/Rpc/asynchronous-rpc).

Puede usar los siguientes atributos para proporcionar compatibilidad con las llamadas a procedimientos remotos asincrónicas.



| Atributo                         | Uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)            | Cuando se aplica a un parámetro de función, define un identificador que permite al llamador realizar una llamada asincrónica y devolver inmediatamente sin esperar los resultados y, posteriormente, volver a sincronizar con la función llamada para recibir datos después de que se complete la llamada. El atributo [**Async**](async.md) también se usa en archivos ACF para definir un identificador asincrónico para un procedimiento o una interfaz completa. En el caso de las interfaces COM, esta interfaz está obsoleta y no se puede usar para nuevas interfaces. |
| [**\_UUID asincrónico**](async-uuid.md) | Indica al compilador de MIDL que defina las versiones sincrónicas y asincrónicas de una interfaz COM.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**incluso**](maybe.md)            | El cliente que realiza esta llamada a procedimiento remoto no espera ninguna respuesta que indique la entrega o la finalización de la llamada, y no se garantiza la entrega. Esto contrasta con las operaciones de **mensajes** en las que no se espera ninguna respuesta, pero se garantiza la entrega.                                                                                                                                                                                                                    |
| [**Mensaje**](message.md)        | La llamada a procedimiento remoto se tratará como un mensaje asíncrono desde el cliente al servidor. El cliente realiza la llamada y se devuelve inmediatamente, mientras que la llamada real se controla mediante el transporte de cola de mensajes ([**ncadg \_ MQ**](ncadg-mq.md)).                                                                                                                                                                                                                              |



 

 

 