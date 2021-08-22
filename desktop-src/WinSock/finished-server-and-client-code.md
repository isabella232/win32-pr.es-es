---
description: Ejecución del código de ejemplo de aplicación de servidor y cliente TCP/IP completo.
ms.assetid: 617dfdf6-f7a7-4e72-8c77-8cfa3ab232e7
title: Ejecución del ejemplo de código de cliente y servidor de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdb5a4b2385c9545410cfc29c913ea81660f6dc2810b92279fad22212781065c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132488"
---
# <a name="running-the-winsock-client-and-server-code-sample"></a>Ejecución del ejemplo de código de cliente y servidor de Winsock

Esta sección contiene el código fuente completo para las aplicaciones cliente y servidor TCP/IP:

-   [Completar el código de cliente de Winsock](complete-client-code.md)
-   [Completar el código del servidor Winsock](complete-server-code.md)

La aplicación de servidor debe iniciarse antes de iniciar la aplicación cliente.

Para ejecutar el servidor, compile el código fuente completo del servidor y ejecute el archivo ejecutable. La aplicación de servidor escucha en el puerto TCP 27015 para que un cliente se conecte. Una vez que un cliente se conecta, el servidor recibe datos del cliente y devuelve (envía) los datos recibidos al cliente. Cuando el cliente apaga la conexión, el servidor apaga el socket de cliente, cierra el socket y se cierra.

Para ejecutar el cliente, compile el código fuente de cliente completo y ejecute el archivo ejecutable. La aplicación cliente requiere que el nombre del equipo o la dirección IP del equipo donde se ejecuta la aplicación de servidor se pase como un parámetro de línea de comandos cuando se ejecute el cliente. Si el cliente y el servidor se ejecutan en el equipo de ejemplo, el cliente se puede iniciar de la siguiente manera:

**client localhost**

El cliente intenta conectarse al servidor en el puerto TCP 27015. Una vez que el cliente se conecta, el cliente envía datos al servidor y recibe los datos enviados desde el servidor. A continuación, el cliente cierra el socket y se cierra.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con Winsock](getting-started-with-winsock.md)
</dt> </dl>

 

 



