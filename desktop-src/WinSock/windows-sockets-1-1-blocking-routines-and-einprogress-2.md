---
description: Un problema importante en la porción de aplicaciones de un entorno de Sockets de Berkeley a un Windows implica el bloqueo. es decir, invocar una función que no se devuelve hasta que se completa la operación asociada.
ms.assetid: 13aedad7-5f3b-4d73-b8e5-be3a095294bc
title: Windows Rutinas de bloqueo de sockets 1.1 y EINPROGRESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4028549862412b80d1343851fb2a147da804095821fdefab4b6aae0eb6ec5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641225"
---
# <a name="windows-sockets-11-blocking-routines-and-einprogress"></a>Windows Rutinas de bloqueo de sockets 1.1 y EINPROGRESS

Un problema importante en la porción de aplicaciones de un entorno de Sockets de Berkeley a un Windows implica el bloqueo. es decir, invocar una función que no se devuelve hasta que se completa la operación asociada. Surge un problema cuando la operación tarda un tiempo arbitrariamente largo en completarse: un ejemplo es una [**función de recv,**](/windows/desktop/api/winsock/nf-winsock-recv) que podría bloquearse hasta que se hayan recibido datos del sistema del mismo nivel. El comportamiento predeterminado dentro del modelo de Sockets de Berkeley es que un socket funcione en modo de bloqueo a menos que el programador solicite explícitamente que las operaciones se traten como no desbloqueadas. Windows Los entornos de sockets 1.1 no podían asumir la programación preferente. Por lo tanto, se recomienda encarecidamente que los programadores usen las operaciones de desbloqueo (asincrónicas) si es posible con Windows Sockets 1.1. Dado que esto no siempre era posible, se proporcionaron las funciones de pseudobloqueo descritas a continuación.

> [!Note]  
> Windows Sockets 2 solo se ejecuta en sistemas operativos de 32 bits preferentes donde los interbloqueos no son un problema. Los procedimientos de programación recomendados para Windows Sockets 1.1 no son necesarios en Windows Sockets 2.

 

Incluso en un socket de bloqueo, algunas funciones [**(enlazar**](/windows/desktop/api/winsock/nf-winsock-bind), [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)y [**getpeername,**](/windows/desktop/api/winsock/nf-winsock-getpeername) por ejemplo) se completan inmediatamente. No hay ninguna diferencia entre una operación de bloqueo y una operación de no bloqueo para esas funciones. Otras operaciones, como [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), pueden completarse inmediatamente o tardar un tiempo arbitrario en completarse, en función de las diversas condiciones de transporte. Cuando se aplica a un socket de bloqueo, estas operaciones se conocen como operaciones de bloqueo. Las siguientes funciones pueden bloquear:

-   [**recv**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**Enviar**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)

Con sockets de Windows de 16 bits 1.1, una operación de bloqueo que no se puede completar inmediatamente se controla mediante pseudobloqueo como se muestra a continuación.

El proveedor de servicios inicia la operación y, a continuación, entra en un bucle en el que envía los mensajes Windows (lo que produce el procesador a otro subproceso, si es necesario) y, a continuación, comprueba la finalización de la función Windows Sockets. Si se ha completado la función o si se ha invocado [**WSACancelBlockingCall,**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) la función de bloqueo se completa con un resultado adecuado.

Un proveedor de servicios debe permitir la instalación de una función de enlace de bloqueo que no procese mensajes para evitar la posibilidad de volver a recibir mensajes mientras hay pendiente una operación de bloqueo. La función de enlace de bloqueo más sencilla **devolvería FALSE.** Si un archivo DLL Windows Sockets depende de mensajes para la operación interna, puede ejecutar **PeekMessage**(**hMyWnd**...) antes de ejecutar el enlace de bloqueo de la aplicación para que pueda obtener sus mensajes sin afectar al resto del sistema.

En un entorno de Windows Sockets 1.1 de 16 bits, si se recibe un mensaje de Windows para un proceso para el que está en curso una operación de bloqueo, existe el riesgo de que la aplicación intente emitir otra llamada a Windows Sockets. Debido a la dificultad para administrar esta condición de forma segura, Windows Sockets 1.1 no admite este comportamiento de aplicación. No se permite que una aplicación realice más de una llamada de función Windows sockets anidados. Solo se permite una llamada de función pendiente para una tarea determinada. Las únicas excepciones son dos funciones que se proporcionan para ayudar al programador en esta situación: [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) y [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).

Se puede llamar a la función [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) en cualquier momento para determinar si hay o no una llamada Windows Sockets 1.1 de bloqueo en curso. De forma similar, se puede llamar a la función [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) en cualquier momento para cancelar una llamada de bloqueo en curso. Cualquier otro anidamiento de Windows sockets genera el error WSAEINPROGRESS.

Debe destacarse que esta restricción se aplica a las operaciones de bloqueo y de no bloqueo. Para Windows Sockets 2 que negocian la versión 2.0 o posterior en el momento de llamar a [**WSAStartup,**](/windows/desktop/api/winsock/nf-winsock-wsastartup)no se cierra ninguna restricción sobre el anidamiento de operaciones. Las operaciones se pueden anidar en circunstancias poco frecuentes, como durante una devolución de llamada de aceptación condicional de [**WSAAccept,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) o si un proveedor de servicios a su vez invoca una función Windows Sockets 2.

Aunque este mecanismo es suficiente para aplicaciones sencillas, no puede admitir los complejos requisitos de distribución de mensajes de aplicaciones más avanzadas (por ejemplo, aquellas que usan el modelo MDI). Para estas aplicaciones, Windows Sockets API incluye la función [**WSASetBlockingHook**](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook), que permite a la aplicación especificar una rutina especial a la que se puede llamar en lugar de la rutina de distribución de mensajes predeterminada descrita en la explicación anterior.

El proveedor Windows Sockets llama al enlace de bloqueo solo si se cumplen todas las condiciones siguientes:

-   La rutina es aquella que se define como capaz de bloquear.
-   El socket especificado es un socket de bloqueo.
-   La solicitud no se puede completar inmediatamente.

Un socket se establece en blocking de forma predeterminada, pero la función [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) con la función **FIONBIO** IOCTL o [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) puede establecer un socket en modo de no bloqueo.

Nunca se llama al enlace de bloqueo y la aplicación no necesita preocuparse de los problemas de reenganche que puede presentar el enlace de bloqueo, si una aplicación sigue estas directrices:

-   Solo usa sockets que no son de bloqueo.
-   Usa las [**rutinas WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) o **WSAAsyncGetXByY** en lugar de [**las**](/windows/desktop/api/Winsock2/nf-winsock2-select) rutinas select y **getXbyY.**

Si una aplicación Windows Sockets 1.1 invoca una operación asincrónica o de no bloqueo que toma un puntero a un objeto de memoria (un búfer o una variable global, por ejemplo) como argumento, es responsabilidad de la aplicación asegurarse de que el objeto está disponible para Windows Sockets a lo largo de la operación. La aplicación no debe invocar ninguna función Windows que pueda afectar a la asignación o viabilidad de la dirección de la memoria implicada.

 

 



