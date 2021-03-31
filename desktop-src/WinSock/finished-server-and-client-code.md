---
description: Ejecutar el código de ejemplo completo de la aplicación de servidor y cliente TCP/IP.
ms.assetid: 617dfdf6-f7a7-4e72-8c77-8cfa3ab232e7
title: Ejecución del ejemplo de código de servidor y cliente Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b3588af6bac668f0b7c785bafe2f69de4ef2b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001143"
---
# <a name="running-the-winsock-client-and-server-code-sample"></a>Ejecución del ejemplo de código de servidor y cliente Winsock

Esta sección contiene el código fuente completo de las aplicaciones de cliente y servidor de TCP/IP:

-   [Completar el código de cliente Winsock](complete-client-code.md)
-   [Completar el código del servidor Winsock](complete-server-code.md)

La aplicación de servidor debe iniciarse antes de que se inicie la aplicación cliente.

Para ejecutar el servidor, compile el código fuente completo del servidor y ejecute el archivo ejecutable. La aplicación de servidor escucha en el puerto TCP 27015 para que un cliente se conecte. Una vez que un cliente se conecta, el servidor recibe datos del cliente y repite (envía) los datos recibidos en el cliente. Cuando el cliente cierra la conexión, el servidor apaga el socket de cliente, cierra el socket y se cierra.

Para ejecutar el cliente, compile el código fuente completo del cliente y ejecute el archivo ejecutable. La aplicación cliente requiere que el nombre del equipo o la dirección IP del equipo en el que se ejecuta la aplicación de servidor se pase como un parámetro de línea de comandos cuando se ejecute el cliente. Si el cliente y el servidor se ejecutan en el equipo de ejemplo, el cliente se puede iniciar de la siguiente manera:

**localhost de cliente**

El cliente intenta conectarse al servidor en el puerto TCP 27015. Una vez que el cliente se conecta, el cliente envía datos al servidor y recibe los datos devueltos desde el servidor. Después, el cliente cierra el socket y se cierra.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con Winsock](getting-started-with-winsock.md)
</dt> </dl>

 

 



