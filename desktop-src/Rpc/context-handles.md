---
title: Identificadores de contexto
description: En ocasiones, las aplicaciones distribuidas requieren que el programa de servidor mantenga la información de estado entre las llamadas de cliente.
ms.assetid: 91732a75-0a3a-44bd-9db9-c11be6fd2d70
keywords:
- Llamada a procedimiento remoto RPC, descrita, identificadores de contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ff36ff8f1a36843293060e091b7eecee0d8666
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069161"
---
# <a name="context-handles"></a>Identificadores de contexto

En ocasiones, las aplicaciones distribuidas requieren que el programa de servidor mantenga la información de estado entre las llamadas de cliente. Los programas de servidor que ofrecen servicio a más de un cliente a la vez deben mantener la información de estado de cada cliente. Dado que el cliente y el servidor usan espacios de direcciones diferentes en equipos diferentes y no confían necesariamente entre sí, los enfoques comunes para el uso compartido de datos a menudo no funcionan. Por ejemplo, el cliente y el servidor no pueden mantener la información de estado de su sesión remota en variables globales porque no comparten el mismo espacio de direcciones global. Es difícil mantener la información en un archivo compartido porque se ejecutan en equipos diferentes. Un enfoque simplista puede ser enviar todo el estado al cliente y hacer que el cliente lo devuelva en la siguiente llamada, pero este enfoque tiene errores: el servidor no confía necesariamente en el cliente para devolver el estado correcto y el estado puede estar vinculado implícitamente a algún otro estado en el servidor, como identificadores de archivo o sockets abiertos.

Rpc de Microsoft proporciona un mecanismo eficaz y seguro denominado identificadores de contexto para mantener el estado asociado a un cliente determinado en un servidor. La información de estado se denomina contexto del servidor. Los clientes pueden obtener un identificador de contexto para identificar el contexto del servidor para sus sesiones RPC individuales.

Por ejemplo, cada cliente de una aplicación distribuida puede hacer que el programa de servidor cree y actualice un archivo de datos para su sesión RPC. El servidor puede usar su identificador de archivo para el archivo de datos de cada cliente como identificador de contexto. Cada vez que un cliente solicita operaciones en el archivo de datos que el servidor crea para él, el cliente pasa el identificador de contexto al servidor. El cliente no obtiene realmente el propio identificador de archivo; obtiene un token opaco que el tiempo de ejecución rpc del servidor puede asociar de forma única al identificador de archivo. Puesto que el identificador de contexto es realmente un identificador de archivo, el identificador de contexto solo tiene sentido en el espacio de direcciones del servidor. Sin embargo, el programa cliente puede usar el identificador de contexto para decir al servidor en qué archivo se deben realizar las actualizaciones.

Otros datos también pueden ser identificadores de contexto. Por ejemplo, un cliente y un servidor pueden usar un número de registro de un registro de base de datos como identificador de archivo. Si el cliente necesita realizar varias actualizaciones en un registro determinado, podría obtener el número de registro como identificador de contexto. Pasaría el número de registro al servidor cada vez que invocó un procedimiento remoto para actualizar el registro de base de datos.

A menudo, un identificador de contexto apunta a un bloque de memoria en el servidor donde el servidor mantiene varias información de administración.

En esta sección se presenta información sobre cómo definir y usar identificadores de contexto. La discusión se presenta en los temas siguientes:

-   [Desarrollo de interfaces mediante identificadores de contexto](interface-development-using-context-handles.md)
-   [Desarrollo de servidores mediante identificadores de contexto](server-development-using-context-handles.md)
-   [Desarrollo de cliente mediante identificadores de contexto](client-development-using-context-handles.md)
-   [Rutina de ejecución de contexto de servidor](server-context-run-down-routine.md)
-   [Restablecimiento del contexto de cliente](client-context-reset.md)
-   [Clientes multiproceso y identificadores de contexto](multithreaded-clients-and-context-handles.md)

 

 




