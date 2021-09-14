---
title: Mantener el estado en el servidor entre llamadas
description: A menudo es necesario mantener el estado en el servidor entre llamadas RPC independientes \ 8212; el uso de identificadores de contexto es la mejor manera de hacerlo. Unas pocas palabras sobre cómo funcionan internamente los identificadores de contexto ayuda a comprender cuándo funcionan mejor los identificadores de contexto.
ms.assetid: f76ec489-f48e-473d-b519-3ac143d41fa4
keywords:
- Llamada a procedimiento remoto RPC, procedimientos recomendados, mantenimiento del estado entre llamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00090fb317cba8c33e7b60ac81762d7d21dd4dc9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244514"
---
# <a name="maintaining-state-on-the-server-between-calls"></a>Mantener el estado en el servidor entre llamadas

A menudo es necesario mantener el estado en el servidor entre llamadas RPC independientes; el uso de identificadores de contexto es la mejor manera de hacerlo. Unas pocas palabras sobre cómo funcionan internamente los identificadores de contexto ayuda a comprender cuándo funcionan mejor los identificadores de contexto.

El cliente nunca recibe el estado que se mantiene en el servidor. A menudo, el estado del servidor es un puntero a un bloque de memoria y el cliente no tiene información sobre él. Todo lo que recibe el cliente es un número único grande, con otra información asociada, que el servidor envía al cliente y que representa el identificador de contexto en todas las operaciones posteriores. Siempre que el cliente hace referencia a un identificador abierto, envía el gran número que recibió del servidor cuando se abrió ese identificador de contexto.

El servidor realiza un seguimiento de todos los números grandes que envía a un cliente. Cuando el servidor recibe un número grande que representa un identificador de contexto, busca el número en la colección de identificadores de contexto válidos y pendientes para ese cliente y busca el contexto del lado servidor correspondiente a un número grande determinado. Esto se pasa a la rutina del servidor. Si no se encuentra el número grande, se genera una excepción MISMATCH DE CONTEXTO de SS RPC \_ X y se propaga al \_ \_ \_ cliente.

Las corolaries de este diseño son las siguientes:

-   Un identificador de contexto solo es válido en el contexto de la sesión de cliente/servidor existente. No se puede pasar a otro cliente.
-   Un identificador de contexto deja de ser válido si el servidor se reinicia o, de lo contrario, pierde su conexión con el cliente.
-   El cliente no puede interpretar lo que representa el identificador de contexto en el servidor. Para un cliente, todos los identificadores de contexto son simplemente números grandes.

Si se produce un error en el cliente, el servidor recibirá una notificación y limpiará sus identificadores de contexto mediante el mecanismo de ejecución.

 

 




