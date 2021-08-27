---
description: En las aplicaciones winsock, un descriptor de socket no es un descriptor de archivo y se debe usar con las funciones winsock.
ms.assetid: bc434b35-9231-4b03-bc8f-cf59aaeb821e
title: Tipo de datos de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a95f890a14f68a0422ec91d31cb09735e2c85ab15cad52f9bd40499cee1167c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121245"
---
# <a name="socket-data-type"></a>Tipo de datos de socket

En las aplicaciones winsock, un descriptor de socket no es un descriptor de archivo y se debe usar con las funciones winsock.

En UNIX, un descriptor de socket se representa mediante un descriptor de archivo estándar. Como resultado, un descriptor de socket en UNIX se puede pasar a cualquiera de las funciones de E/S de archivo estándar (lectura y escritura, por ejemplo).

Además, todos los identificadores de UNIX, incluidos los identificadores de socket, son pequeños enteros no negativos y algunas aplicaciones hacen suposiciones de que esto será así.

Windows Los identificadores de sockets no tienen ninguna restricción, aparte de que el valor INVALID \_ SOCKET no es un socket válido. Los identificadores de socket pueden tomar cualquier valor entre 0 y \_ SOCKET–1 no válido.

Dado que el tipo **SOCKET** no está firmado, la compilación del código fuente existente de, por ejemplo, un entorno de UNIX puede provocar advertencias del compilador sobre errores de coincidencia de tipos de datos firmados o sin signo.

Esto significa, por ejemplo, que la [](/windows/desktop/api/Winsock2/nf-winsock2-accept) comprobación de errores cuando el [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y las funciones de aceptación devuelven no deben realizarse comparando el valor devuelto con –1 o viendo si el valor es negativo (enfoques comunes y legales en UNIX). En su lugar, una aplicación debe usar la constante de manifiesto INVALID SOCKET tal como se define en el archivo de \_ *encabezado Winsock2.h.* Por ejemplo:

Estilo de UNIX BSD típico


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

[Porte de aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Consideraciones de programación de Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



