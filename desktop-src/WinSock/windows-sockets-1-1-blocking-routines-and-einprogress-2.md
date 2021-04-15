---
description: Un problema importante en la migración de aplicaciones de un entorno de sockets de Berkeley a un entorno de Windows implica el bloqueo; es decir, al invocar una función que no devuelve ningún resultado hasta que se completa la operación asociada.
ms.assetid: 13aedad7-5f3b-4d73-b8e5-be3a095294bc
title: Rutinas de bloqueo de Windows Sockets 1,1 y EINPROGRESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea6d45b4d25578505a3cb4ab4beb7c2c2fe90e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715474"
---
# <a name="windows-sockets-11-blocking-routines-and-einprogress"></a>Rutinas de bloqueo de Windows Sockets 1,1 y EINPROGRESS

Un problema importante en la migración de aplicaciones de un entorno de sockets de Berkeley a un entorno de Windows implica el bloqueo; es decir, al invocar una función que no devuelve ningún resultado hasta que se completa la operación asociada. Surge un problema cuando la operación tarda un tiempo arbitrariamente largo en completarse: un ejemplo es una función [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) , que podría bloquearse hasta que se hayan recibido datos del sistema del mismo nivel. El comportamiento predeterminado dentro del modelo Berkeley sockets es para que un socket funcione en modo de bloqueo, a menos que el programador solicite explícitamente que las operaciones se traten como sin bloqueos. Los entornos de Windows Sockets 1,1 no pueden suponer la programación preferente. Por lo tanto, se recomienda encarecidamente que los programadores usen las operaciones de no bloqueo (asincrónicas) si es posible con Windows Sockets 1,1. Dado que esto no siempre era posible, se proporcionaron las instalaciones de bloqueo que se describen en lo siguiente.

> [!Note]  
> Windows Sockets 2 solo se ejecuta en sistemas operativos preferentemente de 32 bits en los que los interbloqueos no son un problema. Las prácticas de programación recomendadas para Windows Sockets 1,1 no son necesarias en Windows Sockets 2.

 

Incluso en un socket de bloqueo, algunas funciones ( [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind), [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)y [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) , por ejemplo) se completan inmediatamente. No hay ninguna diferencia entre un bloqueo y una operación de no bloqueo para esas funciones. Otras operaciones, como [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv), pueden completarse inmediatamente o tardar un tiempo arbitrario en completarse, en función de las distintas condiciones de transporte. Cuando se aplica a un socket de bloqueo, estas operaciones se conocen como operaciones de bloqueo. Las siguientes funciones pueden bloquear:

-   [**recv**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**Enviar**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)

Con Windows Sockets de 16 bits 1,1, una operación de bloqueo que no se puede completar inmediatamente se controla mediante el bloqueo pseudo como se indica a continuación.

El proveedor de servicios inicia la operación y, a continuación, escribe un bucle en el que envía los mensajes de Windows (lo que produce el procesador a otro subproceso, si es necesario) y, a continuación, comprueba la finalización de la función de Windows Sockets. Si la función se ha completado, o si se ha invocado [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) , la función de bloqueo se completa con un resultado adecuado.

Un proveedor de servicios debe permitir la instalación de una función de enlace de bloqueo que no procese mensajes para evitar la posibilidad de que se vuelvan a entrar mensajes mientras una operación de bloqueo esté pendiente. La función de enlace de bloqueo más sencilla devolverá **false**. Si una DLL de Windows Sockets depende de mensajes para una operación interna, puede ejecutar **PeekMessage**(**hMyWnd**...) antes de ejecutar el enlace de bloqueo de la aplicación para que pueda obtener sus mensajes sin afectar al resto del sistema.

En un entorno de Windows Sockets 1,1 de 16 bits, si se recibe un mensaje de Windows para un proceso para el que está en curso una operación de bloqueo, existe el riesgo de que la aplicación intente emitir otra llamada de Windows Sockets. Debido a la dificultad en la administración segura de esta condición, Windows Sockets 1,1 no admite este comportamiento de la aplicación. No se permite que una aplicación realice más de una llamada de función anidada de Windows Sockets. Solo se permite una llamada de función pendiente para una tarea determinada. Las únicas excepciones son dos funciones que se proporcionan para ayudar al programador en esta situación: [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) y [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).

Se puede llamar a la función [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) en cualquier momento para determinar si una llamada de bloqueo de Windows sockets 1,1 está en curso. Del mismo modo, se puede llamar a la función [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) en cualquier momento para cancelar una llamada de bloqueo en curso. Cualquier otro anidamiento de las funciones de Windows Sockets produce el error WSAEINPROGRESS.

Se debe resaltar que esta restricción se aplica a las operaciones de bloqueo y de no bloqueo. En el caso de las aplicaciones de Windows Sockets 2 que negocian la versión 2,0 o posterior en el momento de llamar a [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup), no se realiza ninguna restricción sobre el anidamiento de las operaciones. Las operaciones se pueden anidar en raras circunstancias, como durante una devolución de llamada de aceptación condicional [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) , o si un proveedor de servicios a su vez invoca una función de Windows Sockets 2.

Aunque este mecanismo es suficiente para aplicaciones sencillas, no puede admitir los requisitos complejos de distribución de mensajes de aplicaciones más avanzadas (por ejemplo, las que usan el modelo MDI). Para estas aplicaciones, la API de Windows Sockets incluye la función [**WSASetBlockingHook**](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook), que permite a la aplicación especificar una rutina especial a la que se puede llamar en lugar de la rutina de envío de mensajes predeterminada que se describe en la explicación anterior.

El proveedor de Windows Sockets llama al enlace de bloqueo solo si se cumplen todas las condiciones siguientes:

-   La rutina es una que se define como capaz de bloquearse.
-   El socket especificado es un socket de bloqueo.
-   La solicitud no se puede completar inmediatamente.

Un socket se establece en bloque de forma predeterminada, pero la función [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) con el ioctl **FIONBIO** o la función [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) puede establecer un socket en modo de no bloqueo.

Nunca se llama al enlace de bloqueo y la aplicación no necesita preocuparse por los problemas de reentrar que el enlace de bloqueo puede introducir, si una aplicación sigue estas instrucciones:

-   Solo usa Sockets sin bloqueos.
-   Usa las rutinas [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) y/o **WSAAsyncGetXByY** en lugar de las rutinas [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) y **getXbyY** .

Si una aplicación de Windows Sockets 1,1 invoca una operación asincrónica o de no bloqueo que toma un puntero a un objeto de memoria (un búfer o una variable global, por ejemplo) como argumento, es responsabilidad de la aplicación asegurarse de que el objeto está disponible para Windows Sockets durante toda la operación. La aplicación no debe invocar ninguna función de Windows que pueda afectar a la viabilidad de asignación o de dirección de la memoria implicada.

 

 



