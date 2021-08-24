---
title: El código auxiliar del servidor
description: El código auxiliar del servidor proporciona puntos de entrada suplentes en el servidor para cada una de las operaciones definidas en el archivo IDL de entrada.
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- MIDL del compilador MIDL, MIDL y RPC MIDL, interfaces, código auxiliar de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddfc940ebbd90e4e028ce96dc3b5c47eb15179d41cfbd064cd235e87192822f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559913"
---
# <a name="the-server-stub"></a>El código auxiliar del servidor

El código auxiliar del servidor proporciona puntos de entrada suplentes en el servidor para cada una de las operaciones definidas en el archivo IDL de entrada.

Cuando la biblioteca en tiempo de ejecución rpc invoca una rutina de código auxiliar de servidor, realiza las siguientes funciones:

-   Desempaqueta los argumentos de entrada (desempaqueta los argumentos de sus formatos transmitidos).
-   Llama a la implementación real del procedimiento en el servidor.
-   Serializa los argumentos de salida (empaqueta los argumentos en los formularios transmitidos).

Los modificadores del compilador [**MIDL /server**](-server.md), [**/sstub**](-sstub.md)y [**/out**](-out.md) afectan al archivo de código auxiliar del servidor.

 

 




