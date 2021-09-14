---
title: Atributos asincrónicos
description: Cuando un programa invoca un procedimiento en una interfaz, el procedimiento puede ejecutarse de forma sincrónica o asincrónica.
ms.assetid: 3e6c6c13-1524-41b2-96dc-3885eadb847c
keywords:
- IDL MIDL, atributos MIDL, asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aca2276bf1fa5178f1dca3ae4803544066d983
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159674"
---
# <a name="asynchronous-attributes"></a>Atributos asincrónicos

Cuando un programa invoca un procedimiento en una interfaz, el procedimiento puede ejecutarse de forma sincrónica o asincrónica. Un procedimiento sincrónico hace que el programa que realiza la llamada espere hasta que el procedimiento se devuelva antes de que el programa pueda continuar. Un procedimiento asincrónico devuelve inmediatamente sin esperar los resultados. Posteriormente, el programa que realiza la llamada debe resincronizarse con el procedimiento de interfaz para recibir datos. Para obtener más información, vea [RPC asincrónica.](/windows/desktop/Rpc/asynchronous-rpc)

Puede usar los atributos siguientes para proporcionar compatibilidad con llamadas a procedimientos remotos asincrónicos.



| Atributo                         | Uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Async**](async.md)            | Cuando se aplica a un parámetro de función, define un identificador que permite al autor de la llamada realizar una llamada asincrónica y volver inmediatamente sin esperar a los resultados y, posteriormente, volver a sincronizar con la función llamada para recibir datos una vez completada la llamada. El [**atributo asincrónico**](async.md) también se usa en archivos ACF para definir un identificador asincrónico para un procedimiento o una interfaz completa. En el caso de las interfaces COM, esta interfaz está obsoleta y no se puede usar para las interfaces nuevas. |
| [**uuid \_ asincrónico**](async-uuid.md) | Dirige al compilador MIDL para definir las versiones sincrónicas y asincrónicas de una interfaz COM.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**quizás**](maybe.md)            | El cliente que realiza esta llamada a procedimiento remoto no espera ninguna respuesta que indique la entrega o finalización de la llamada, y no se garantiza la entrega. Esto contrasta con las **operaciones de** mensaje en las que no se espera ninguna respuesta, pero se garantiza la entrega.                                                                                                                                                                                                                    |
| [**Mensaje**](message.md)        | La llamada a procedimiento remoto se tratará como un mensaje asincrónico desde el cliente al servidor. El cliente realiza la llamada y devuelve inmediatamente, mientras que la llamada real se controla mediante el transporte message-queuing ([**ncadg \_ mq**](ncadg-mq.md)).                                                                                                                                                                                                                              |



 

 

 