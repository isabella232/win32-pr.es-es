---
description: En las aplicaciones Winsock, un descriptor de sockets no es un descriptor de archivo y debe usarse con las funciones de Winsock.
ms.assetid: bc434b35-9231-4b03-bc8f-cf59aaeb821e
title: Tipo de datos socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea031032e0d05abc02f7c3c948477c7fe9a1d1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361012"
---
# <a name="socket-data-type"></a>Tipo de datos socket

En las aplicaciones Winsock, un descriptor de sockets no es un descriptor de archivo y debe usarse con las funciones de Winsock.

En UNIX, un descriptor de socket se representa con un descriptor de archivo estándar. Como resultado, un descriptor de socket en UNIX se puede pasar a cualquiera de las funciones de e/s de archivo estándar (por ejemplo, lectura y escritura).

Además, todos los identificadores de UNIX, incluidos los identificadores de socket, son enteros pequeños y no negativos, y algunas aplicaciones realizan suposiciones de que esto será cierto.

Los identificadores de Windows Sockets no tienen restricciones, aparte de que el valor de Socket no válido \_ no sea un socket válido. Los identificadores de socket pueden tomar cualquier valor en el intervalo de 0 a Socket no válido \_ : 1.

Dado que el tipo de **socket** es sin signo, al compilar el código fuente existente desde, por ejemplo, un entorno de Unix puede provocar advertencias del compilador acerca de las discrepancias de tipos de datos firmados o sin firmar.

Esto significa, por ejemplo, que la comprobación de errores cuando el [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y las funciones de [**aceptación**](/windows/desktop/api/Winsock2/nf-winsock2-accept) devuelven no debería realizarse comparando el valor devuelto con – 1, o observando si el valor es negativo (enfoques comunes y legales en UNIX). En su lugar, una aplicación debe usar la constante de manifiesto Socket no válido \_ tal y como se define en el archivo de encabezado *WinSock2. h* . Por ejemplo:

Estilo típico de UNIX BSD


```C++
s = socket(...);
if (s == -1)    /* or s < 0 */
    {/*...*/}
```



Estilo preferido


```C++
s = socket(...);
if (s == INVALID_SOCKET)
    {/*...*/}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trasladar aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Consideraciones sobre la programación de Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



