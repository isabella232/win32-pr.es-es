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
# <a name="socket-data-type"></a><span data-ttu-id="59ac2-103">Tipo de datos socket</span><span class="sxs-lookup"><span data-stu-id="59ac2-103">Socket Data Type</span></span>

<span data-ttu-id="59ac2-104">En las aplicaciones Winsock, un descriptor de sockets no es un descriptor de archivo y debe usarse con las funciones de Winsock.</span><span class="sxs-lookup"><span data-stu-id="59ac2-104">In Winsock applications, a socket descriptor is not a file descriptor and must be used with the Winsock functions.</span></span>

<span data-ttu-id="59ac2-105">En UNIX, un descriptor de socket se representa con un descriptor de archivo estándar.</span><span class="sxs-lookup"><span data-stu-id="59ac2-105">In UNIX, a socket descriptor is represented by a standard file descriptor.</span></span> <span data-ttu-id="59ac2-106">Como resultado, un descriptor de socket en UNIX se puede pasar a cualquiera de las funciones de e/s de archivo estándar (por ejemplo, lectura y escritura).</span><span class="sxs-lookup"><span data-stu-id="59ac2-106">As a result, a socket descriptor on UNIX may be passed to any of the standard file I/O functions (read and write, for example).</span></span>

<span data-ttu-id="59ac2-107">Además, todos los identificadores de UNIX, incluidos los identificadores de socket, son enteros pequeños y no negativos, y algunas aplicaciones realizan suposiciones de que esto será cierto.</span><span class="sxs-lookup"><span data-stu-id="59ac2-107">Furthermore, all handles in UNIX, including socket handles, are small, non-negative integers, and some applications make assumptions that this will be true.</span></span>

<span data-ttu-id="59ac2-108">Los identificadores de Windows Sockets no tienen restricciones, aparte de que el valor de Socket no válido \_ no sea un socket válido.</span><span class="sxs-lookup"><span data-stu-id="59ac2-108">Windows Sockets handles have no restrictions, other than that the value INVALID\_SOCKET is not a valid socket.</span></span> <span data-ttu-id="59ac2-109">Los identificadores de socket pueden tomar cualquier valor en el intervalo de 0 a Socket no válido \_ : 1.</span><span class="sxs-lookup"><span data-stu-id="59ac2-109">Socket handles may take any value in the range 0 to INVALID\_SOCKET–1.</span></span>

<span data-ttu-id="59ac2-110">Dado que el tipo de **socket** es sin signo, al compilar el código fuente existente desde, por ejemplo, un entorno de Unix puede provocar advertencias del compilador acerca de las discrepancias de tipos de datos firmados o sin firmar.</span><span class="sxs-lookup"><span data-stu-id="59ac2-110">Because the **SOCKET** type is unsigned, compiling existing source code from, for example, a UNIX environment may lead to compiler warnings about signed/unsigned data type mismatches.</span></span>

<span data-ttu-id="59ac2-111">Esto significa, por ejemplo, que la comprobación de errores cuando el [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y las funciones de [**aceptación**](/windows/desktop/api/Winsock2/nf-winsock2-accept) devuelven no debería realizarse comparando el valor devuelto con – 1, o observando si el valor es negativo (enfoques comunes y legales en UNIX).</span><span class="sxs-lookup"><span data-stu-id="59ac2-111">This means, for example, that checking for errors when the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) and [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) functions return should not be done by comparing the return value with –1, or seeing if the value is negative (both common and legal approaches in UNIX).</span></span> <span data-ttu-id="59ac2-112">En su lugar, una aplicación debe usar la constante de manifiesto Socket no válido \_ tal y como se define en el archivo de encabezado *WinSock2. h* .</span><span class="sxs-lookup"><span data-stu-id="59ac2-112">Instead, an application should use the manifest constant INVALID\_SOCKET as defined in the *Winsock2.h* header file.</span></span> <span data-ttu-id="59ac2-113">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="59ac2-113">For example:</span></span>

<span data-ttu-id="59ac2-114">Estilo típico de UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="59ac2-114">Typical BSD UNIX Style</span></span>


```C++
s = socket(...);
if (s == -1)    /* or s < 0 */
    {/*...*/}
```



<span data-ttu-id="59ac2-115">Estilo preferido</span><span class="sxs-lookup"><span data-stu-id="59ac2-115">Preferred Style</span></span>


```C++
s = socket(...);
if (s == INVALID_SOCKET)
    {/*...*/}
```



## <a name="related-topics"></a><span data-ttu-id="59ac2-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59ac2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59ac2-117">Trasladar aplicaciones de socket a Winsock</span><span class="sxs-lookup"><span data-stu-id="59ac2-117">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="59ac2-118">Consideraciones sobre la programación de Winsock</span><span class="sxs-lookup"><span data-stu-id="59ac2-118">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



