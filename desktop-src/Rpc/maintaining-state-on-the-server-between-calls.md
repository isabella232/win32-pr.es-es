---
title: Mantener el estado en el servidor entre llamadas
description: A menudo es necesario mantener el estado en el servidor entre llamadas RPC independientes \ 8212; el uso de identificadores de contexto es la mejor manera de hacerlo. Unas cuantas palabras sobre cómo funcionan internamente los identificadores de contexto ayuda a comprender cuándo funcionan mejor los controles de contexto.
ms.assetid: f76ec489-f48e-473d-b519-3ac143d41fa4
keywords:
- RPC llamada a procedimiento remoto, procedimientos recomendados, mantener el estado entre llamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00090fb317cba8c33e7b60ac81762d7d21dd4dc9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772721"
---
# <a name="maintaining-state-on-the-server-between-calls"></a>Mantener el estado en el servidor entre llamadas

A menudo es necesario mantener el estado en el servidor entre llamadas RPC independientes; el uso de identificadores de contexto es la mejor manera de hacerlo. Unas cuantas palabras sobre cómo funcionan internamente los identificadores de contexto ayuda a comprender cuándo funcionan mejor los controles de contexto.

El cliente nunca recibe el estado que se mantiene en el servidor. Normalmente, el estado del servidor es un puntero a un bloque de memoria y el cliente no tiene información sobre él. Todas las recepciones de cliente son un número único grande, con otra información asociada, que el servidor envía al cliente y que representa el identificador de contexto en todas las operaciones posteriores. Cada vez que el cliente hace referencia a un identificador abierto, envía el número grande recibido desde el servidor cuando se abre ese identificador de contexto.

El servidor realiza un seguimiento de todos los números grandes que envía a un cliente. Cuando el servidor recibe un número grande que representa un identificador de contexto, busca el número en la colección de identificadores de contexto vigentes y pendientes para ese cliente, y busca el contexto del servidor correspondiente a un número grande determinado. Esto se pasa a la rutina del servidor. Si no se encuentra el número grande, se genera una excepción de error de coincidencia de contexto de RPC \_ X \_ SS \_ \_ y se propaga al cliente.

La corollaries de este diseño es la siguiente:

-   Un identificador de contexto solo es válido en el contexto de la sesión de cliente/servidor existente. No se puede pasar a otro cliente.
-   Un identificador de contexto deja de ser válido si el servidor se reinicia o se pierde la conexión con el cliente.
-   El cliente no puede interpretar lo que representa el identificador de contexto en el servidor. Para un cliente, todos los identificadores de contexto son simplemente números grandes.

Si se produce un error en el cliente, el servidor recibirá una notificación y limpiará los identificadores de contexto mediante el mecanismo de ejecución.

 

 




