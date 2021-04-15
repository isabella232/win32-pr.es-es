---
title: Identificadores de contexto
description: En ocasiones, es el caso de que las aplicaciones distribuidas requieran que el programa de servidor mantenga información de estado entre las llamadas del cliente.
ms.assetid: 91732a75-0a3a-44bd-9db9-c11be6fd2d70
keywords:
- RPC (llamada a procedimiento remoto), descripción, identificadores de contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ff36ff8f1a36843293060e091b7eecee0d8666
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676157"
---
# <a name="context-handles"></a>Identificadores de contexto

En ocasiones, es el caso de que las aplicaciones distribuidas requieran que el programa de servidor mantenga información de estado entre las llamadas del cliente. Los programas de servidor que prestan servicio a más de un cliente a la vez deben conservar la información de estado de cada cliente. Dado que el cliente y el servidor usan espacios de direcciones diferentes en distintos equipos y no necesariamente confían entre sí, los enfoques comunes para el uso compartido de datos a menudo no funcionan. Por ejemplo, el cliente y el servidor no pueden mantener la información de estado en su sesión remota en variables globales porque no comparten el mismo espacio de direcciones global. Es difícil mantener la información en un archivo compartido porque se ejecutan en equipos diferentes. Un enfoque simplista puede ser enviar todo el estado al cliente y hacer que el cliente lo devuelva en la siguiente llamada, pero este enfoque tiene defectos: el servidor no confía necesariamente en el cliente para que devuelva el estado correcto, y el estado puede estar vinculado implícitamente a otro estado del servidor, como identificadores de archivo o sockets abiertos.

Microsoft RPC proporciona un mecanismo eficaz y seguro denominado identificadores de contexto para mantener el estado asociado a un cliente determinado en un servidor. La información de estado se denomina contexto del servidor. Los clientes pueden obtener un identificador de contexto para identificar el contexto del servidor para sus sesiones RPC individuales.

Por ejemplo, cada cliente de una aplicación distribuida puede hacer que el programa de servidor cree y actualice un archivo de datos para su sesión RPC. El servidor puede utilizar su identificador de archivo para cada archivo de datos de cliente como el identificador de contexto. Cada vez que un cliente solicita operaciones en el archivo de datos que el servidor crea para él, el cliente pasa el identificador de contexto al servidor. El cliente no obtiene realmente el propio identificador de archivo; Obtiene un token opaco que el tiempo de ejecución de RPC del servidor puede asociar de forma única al identificador de archivo. Dado que el identificador de contexto es realmente un identificador de archivo, el identificador de contexto solo tiene sentido en el espacio de direcciones del servidor. Sin embargo, el programa cliente puede utilizar el identificador de contexto para indicar al servidor en qué archivo se van a realizar las actualizaciones.

Otros datos también pueden ser identificadores de contexto. Por ejemplo, un cliente y un servidor pueden utilizar un número de registro de un registro de base de datos como un identificador de archivo. Si el cliente necesita realizar una serie de actualizaciones en un registro determinado, podría obtener el número de registro como un identificador de contexto. Pasaría el número de registro al servidor cada vez que invocó un procedimiento remoto para actualizar el registro de base de datos.

La mayoría de las veces, un identificador de contexto apunta a un bloque de memoria en el servidor en el que el servidor mantiene diversa información de administración.

En esta sección se ofrece información sobre la definición y el uso de identificadores de contexto. La discusión se presenta en los temas siguientes:

-   [Desarrollo de interfaces con identificadores de contexto](interface-development-using-context-handles.md)
-   [Desarrollo de servidores con identificadores de contexto](server-development-using-context-handles.md)
-   [Desarrollo de cliente con identificadores de contexto](client-development-using-context-handles.md)
-   [Rutina de ejecución de contexto de servidor](server-context-run-down-routine.md)
-   [Restablecimiento de contexto de cliente](client-context-reset.md)
-   [Clientes multiproceso y controladores de contexto](multithreaded-clients-and-context-handles.md)

 

 




