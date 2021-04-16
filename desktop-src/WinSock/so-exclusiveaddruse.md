---
description: La \_ opción de socket so EXCLUSIVEADDRUSE impide que otros Sockets se enlacen a la misma dirección y puerto.
ms.assetid: ce0d8188-54be-46e8-8753-d0680f690b84
title: Opción de socket de SO_EXCLUSIVEADDRUSE (WinSock2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d4747150f918a7e9c4ce37ec209e7261d1a00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705595"
---
# <a name="so_exclusiveaddruse-socket-option"></a><span data-ttu-id="f2f3d-103">\_EXCLUSIVEADDRUSE socket, opción</span><span class="sxs-lookup"><span data-stu-id="f2f3d-103">SO\_EXCLUSIVEADDRUSE socket option</span></span>

<span data-ttu-id="f2f3d-104">La \_ opción de socket so EXCLUSIVEADDRUSE impide que otros Sockets se enlacen a la misma dirección y puerto.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-104">The SO\_EXCLUSIVEADDRUSE socket option prevents other sockets from being forcibly bound to the same address and port.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2f3d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2f3d-105">Syntax</span></span>

<span data-ttu-id="f2f3d-106">La \_ opción for EXCLUSIVEADDRUSE impide que otros Sockets se enlacen a la misma dirección y puerto, una práctica habilitada por la \_ opción de socket for REUSEADDR.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-106">The SO\_EXCLUSIVEADDRUSE option prevents other sockets from being forcibly bound to the same address and port, a practice enabled by the SO\_REUSEADDR socket option.</span></span> <span data-ttu-id="f2f3d-107">Las aplicaciones malintencionadas pueden ejecutar esta reutilización para interrumpir la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-107">Such reuse can be executed by malicious applications to disrupt the application.</span></span> <span data-ttu-id="f2f3d-108">La \_ opción for EXCLUSIVEADDRUSE es muy útil para los servicios del sistema que requieren alta disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-108">The SO\_EXCLUSIVEADDRUSE option is very useful to system services requiring high availability.</span></span>

<span data-ttu-id="f2f3d-109">En el ejemplo de código siguiente se muestra la configuración de esta opción.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-109">The following code example illustrates setting this option.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>
#include <stdlib.h>             // Needed for _wtoi

#pragma comment(lib, "Ws2_32.lib")

int __cdecl wmain(int argc, wchar_t ** argv)
{
    WSADATA wsaData;
    int iResult = 0;
    int iError = 0;

    SOCKET s = INVALID_SOCKET;
    SOCKADDR_IN saLocal;
    int iOptval = 0;

    int iFamily = AF_UNSPEC;
    int iType = 0;
    int iProtocol = 0;

    int iPort = 0;

    // Validate the parameters
    if (argc != 5) {
        wprintf(L"usage: %ws <addressfamily> <type> <protocol> <port>\n", argv[0]);
        wprintf(L"    opens a socket for the specified family, type, & protocol\n");
        wprintf(L"    sets the SO_EXCLUSIVEADDRUSE socket option on the socket\n");
        wprintf(L"    then tries to bind the port specified on the command-line\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 0 2 17 5150\n", argv[0]);
        wprintf(L"   where AF_UNSPEC=0 SOCK_DGRAM=2 IPPROTO_UDP=17  PORT=5150\n",
                argv[0]);
        wprintf(L"   %ws 2 1 17 5150\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_STREAM=1 IPPROTO_TCP=6  PORT=5150\n", argv[0]);
        wprintf(L"   See the documentation for the socket function for other values\n");
        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    iPort = _wtoi(argv[4]);

    if (iFamily != AF_INET && iFamily != AF_INET6) {
        wprintf(L"Address family must be either AF_INET (2) or AF_INET6 (23)\n");
        return 1;
    }

    if (iPort <= 0 || iPort >= 65535) {
        wprintf(L"Port specified must be greater than 0 and less than 65535\n");
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error: %d\n", iResult);
        return 1;
    }
    // Create the socket
    s = socket(iFamily, iType, iProtocol);
    if (s == INVALID_SOCKET) {
        wprintf(L"socket failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    // Set the exclusive address option
    iOptval = 1;
    iResult = setsockopt(s, SOL_SOCKET, SO_EXCLUSIVEADDRUSE,
                         (char *) &iOptval, sizeof (iOptval));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"setsockopt for SO_EXCLUSIVEADDRUSE failed with error: %ld\n",
                WSAGetLastError());
    }

    saLocal.sin_family = (ADDRESS_FAMILY) iFamily;
    saLocal.sin_port = htons( (u_short) iPort);
    saLocal.sin_addr.s_addr = htonl(INADDR_ANY);

    // Bind the socket
    iResult = bind(s, (SOCKADDR *) & saLocal, sizeof (saLocal));
    if (iResult == SOCKET_ERROR) {

        // Most errors related to setting SO_EXCLUSIVEADDRUSE
        //    will occur at bind.
        iError = WSAGetLastError();
        if (iError == WSAEACCES)
            wprintf(L"bind failed with WSAEACCES (access denied)\n");
        else
            wprintf(L"bind failed with error: %ld\n", iError);

    } else {
        wprintf(L"bind on socket with SO_EXCLUSIVEADDRUSE succeeded to port: %ld\n",
                iPort);
    }

    // cleanup
    closesocket(s);
    WSACleanup();

    return 0;
}

```



<span data-ttu-id="f2f3d-110">Para que surta efecto, se \_ debe establecer la opción for EXCLUSIVADDRUSE antes de llamar a la función [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) (esto también se aplica a la \_ opción for REUSEADDR).</span><span class="sxs-lookup"><span data-stu-id="f2f3d-110">To have any effect, the SO\_EXCLUSIVADDRUSE option must be set before the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called (this also applies to the SO\_REUSEADDR option).</span></span> <span data-ttu-id="f2f3d-111">En la tabla 1 se muestran los efectos de establecer la \_ opción for EXCLUSIVEADDRUSE.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-111">Table 1 lists the effects of setting the SO\_EXCLUSIVEADDRUSE option.</span></span> <span data-ttu-id="f2f3d-112">El carácter comodín indica el enlace a la dirección comodín, como 0.0.0.0 para IPv4 y:: para IPv6.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-112">Wildcard indicates binding to the wildcard address, such as 0.0.0.0 for IPv4 and :: for IPv6.</span></span> <span data-ttu-id="f2f3d-113">Específico indica el enlace a una interfaz específica, como enlazar una dirección IP asignada a un adaptador.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-113">Specific indicates binding to a specific interface, such as binding an IP address assigned to an adapter.</span></span> <span data-ttu-id="f2f3d-114">Specific2 indica el enlace a una dirección específica diferente de la dirección enlazada a en el caso específico.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-114">Specific2 indicates binding to a specific address other than the address bound to in the Specific case.</span></span>

> [!Note]  
> <span data-ttu-id="f2f3d-115">El caso Specific2 solo es aplicable cuando el primer enlace se realiza con una dirección específica; en el caso en el que el primer socket está enlazado al carácter comodín, la entrada de cubre todos los casos de direcciones específicas.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-115">The Specific2 case is applicable only when the first bind is performed with a specific address; for the case in which the first socket is bound to the wildcard, the entry for Specific covers all specific address cases.</span></span>

 

<span data-ttu-id="f2f3d-116">Por ejemplo, Imagine un equipo con dos interfaces IP: 10.0.0.1 y 10.99.99.99.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-116">For example, consider a computer with two IP interfaces: 10.0.0.1 and 10.99.99.99.</span></span> <span data-ttu-id="f2f3d-117">Si el primer enlace es 10.0.0.1 y el puerto 5150 con la \_ opción for EXCLUSIVEADDRUSE establecida, el segundo enlace a 10.99.99.99 y el puerto 5150 con una o ninguna de las opciones establecidas se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-117">If the first bind is to 10.0.0.1 and port 5150 with the SO\_EXCLUSIVEADDRUSE option set, then the second bind to 10.99.99.99 and port 5150 with any or no options set succeeds.</span></span> <span data-ttu-id="f2f3d-118">Sin embargo, si el primer socket se enlaza a la dirección comodín (0.0.0.0) y al puerto 5150 por lo que se \_ establece EXCLUSIVEADDRUSE, se producirá un error en cualquier enlace subsiguiente al mismo puerto, independientemente de la dirección IP, con WSAEADDRINUSE (10048) o WSAEACCESS (10013), en función de las opciones que se hayan establecido en el segundo socket BIND.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-118">However, if the first socket is bound to the wildcard address (0.0.0.0) and port 5150 with SO\_EXCLUSIVEADDRUSE set, any subsequent bind to the same port—regardless of IP address—will fail with either WSAEADDRINUSE (10048) or WSAEACCESS (10013), depending on which options were set on the second bind socket.</span></span>

### <a name="bind-behavior-with-various-options-set"></a><span data-ttu-id="f2f3d-119">Comportamiento de enlace con varias opciones establecidas</span><span class="sxs-lookup"><span data-stu-id="f2f3d-119">Bind Behavior with Various Options Set</span></span>



<span data-ttu-id="f2f3d-120">Segundo enlace</span><span class="sxs-lookup"><span data-stu-id="f2f3d-120">Second bind</span></span>

<span data-ttu-id="f2f3d-121">Primer enlace</span><span class="sxs-lookup"><span data-stu-id="f2f3d-121">First bind</span></span>

<span data-ttu-id="f2f3d-122">*\_EXCLUSIVEADDRUSE*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-122">*SO\_EXCLUSIVEADDRUSE*</span></span>

<span data-ttu-id="f2f3d-123">*Ninguna opción* o *\_ REUSEADDR*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-123">*No options* or *SO\_REUSEADDR*</span></span>

<span data-ttu-id="f2f3d-124">*Wildcard (Carácter comodín)*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-124">*Wildcard*</span></span>

<span data-ttu-id="f2f3d-125">*Cuestión*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-125">*Specific*</span></span>

<span data-ttu-id="f2f3d-126">*Wildcard (Carácter comodín)*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-126">*Wildcard*</span></span>

<span data-ttu-id="f2f3d-127">*Cuestión*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-127">*Specific*</span></span>

<span data-ttu-id="f2f3d-128">$ {ROWSPAN3} $*so \_ EXCLUSIVEADDRUSE*$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f2f3d-128">${ROWSPAN3}$*SO\_EXCLUSIVEADDRUSE*${REMOVE}$</span></span>  

<span data-ttu-id="f2f3d-129">*Wildcard (Carácter comodín)*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-129">*Wildcard*</span></span>

<span data-ttu-id="f2f3d-130">Error (10048)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-130">Fail (10048)</span></span>

<span data-ttu-id="f2f3d-131">Error (10048)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-131">Fail (10048)</span></span>

<span data-ttu-id="f2f3d-132">Error (10048)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-132">Fail (10048)</span></span>

<span data-ttu-id="f2f3d-133">Error (10048)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-133">Fail (10048)</span></span>

<span data-ttu-id="f2f3d-134">*Cuestión*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-134">*Specific*</span></span>

<span data-ttu-id="f2f3d-135">Error (10048)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-135">Fail (10048)</span></span>

<span data-ttu-id="f2f3d-136">Error (10048)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-136">Fail (10048)</span></span>

<span data-ttu-id="f2f3d-137">Error (10048)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-137">Fail (10048)</span></span>

<span data-ttu-id="f2f3d-138">Error (10048)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-138">Fail (10048)</span></span>

<span data-ttu-id="f2f3d-139">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-139">*Specific2*</span></span>

<span data-ttu-id="f2f3d-140">N/D</span><span class="sxs-lookup"><span data-stu-id="f2f3d-140">n/a</span></span>

<span data-ttu-id="f2f3d-141">Correcto</span><span class="sxs-lookup"><span data-stu-id="f2f3d-141">Success</span></span>

<span data-ttu-id="f2f3d-142">N/D</span><span class="sxs-lookup"><span data-stu-id="f2f3d-142">n/a</span></span>

<span data-ttu-id="f2f3d-143">Correcto</span><span class="sxs-lookup"><span data-stu-id="f2f3d-143">Success</span></span>

<span data-ttu-id="f2f3d-144">$ {ROWSPAN3} $*no hay opciones*$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f2f3d-144">${ROWSPAN3}$*No options*${REMOVE}$</span></span>  

<span data-ttu-id="f2f3d-145">*Wildcard (Carácter comodín)*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-145">*Wildcard*</span></span>

<span data-ttu-id="f2f3d-146">Error (10048)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-146">Fail (10048)</span></span>

<span data-ttu-id="f2f3d-147">Error (10048)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-147">Fail (10048)</span></span>

<span data-ttu-id="f2f3d-148">Error (10048)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-148">Fail (10048)</span></span>

<span data-ttu-id="f2f3d-149">Error (10048)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-149">Fail (10048)</span></span>

<span data-ttu-id="f2f3d-150">*Cuestión*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-150">*Specific*</span></span>

<span data-ttu-id="f2f3d-151">Error (10048)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-151">Fail (10048)</span></span>

<span data-ttu-id="f2f3d-152">Error (10048)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-152">Fail (10048)</span></span>

<span data-ttu-id="f2f3d-153">Error (10048)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-153">Fail (10048)</span></span>

<span data-ttu-id="f2f3d-154">Error (10048)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-154">Fail (10048)</span></span>

<span data-ttu-id="f2f3d-155">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-155">*Specific2*</span></span>

<span data-ttu-id="f2f3d-156">N/D</span><span class="sxs-lookup"><span data-stu-id="f2f3d-156">n/a</span></span>

<span data-ttu-id="f2f3d-157">Correcto</span><span class="sxs-lookup"><span data-stu-id="f2f3d-157">Success</span></span>

<span data-ttu-id="f2f3d-158">N/D</span><span class="sxs-lookup"><span data-stu-id="f2f3d-158">n/a</span></span>

<span data-ttu-id="f2f3d-159">Correcto</span><span class="sxs-lookup"><span data-stu-id="f2f3d-159">Success</span></span>

<span data-ttu-id="f2f3d-160">$ {ROWSPAN3} $*so \_ REUSEADDR*$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f2f3d-160">${ROWSPAN3}$*SO\_REUSEADDR*${REMOVE}$</span></span>  

<span data-ttu-id="f2f3d-161">*Wildcard (Carácter comodín)*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-161">*Wildcard*</span></span>

<span data-ttu-id="f2f3d-162">Error (10013)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-162">Fail (10013)</span></span>

<span data-ttu-id="f2f3d-163">Error (10013)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-163">Fail (10013)</span></span>

<span data-ttu-id="f2f3d-164">Correcto\*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-164">Success\*</span></span>

<span data-ttu-id="f2f3d-165">Correcto</span><span class="sxs-lookup"><span data-stu-id="f2f3d-165">Success</span></span>

<span data-ttu-id="f2f3d-166">*Cuestión*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-166">*Specific*</span></span>

<span data-ttu-id="f2f3d-167">Error (10013)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-167">Fail (10013)</span></span>

<span data-ttu-id="f2f3d-168">Error (10013)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-168">Fail (10013)</span></span>

<span data-ttu-id="f2f3d-169">Correcto</span><span class="sxs-lookup"><span data-stu-id="f2f3d-169">Success</span></span>

<span data-ttu-id="f2f3d-170">Correcto\*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-170">Success\*</span></span>

<span data-ttu-id="f2f3d-171">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="f2f3d-171">*Specific2*</span></span>

<span data-ttu-id="f2f3d-172">N/D</span><span class="sxs-lookup"><span data-stu-id="f2f3d-172">n/a</span></span>

<span data-ttu-id="f2f3d-173">Correcto</span><span class="sxs-lookup"><span data-stu-id="f2f3d-173">Success</span></span>

<span data-ttu-id="f2f3d-174">N/D</span><span class="sxs-lookup"><span data-stu-id="f2f3d-174">n/a</span></span>

<span data-ttu-id="f2f3d-175">Correcto</span><span class="sxs-lookup"><span data-stu-id="f2f3d-175">Success</span></span>

<span data-ttu-id="f2f3d-176">\* El comportamiento no está definido en cuanto al socket que recibirá los paquetes.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-176">\* The behavior is undefined as to which socket will receive packets.</span></span>



 

<span data-ttu-id="f2f3d-177">En el caso en el que el primer enlace no establece ninguna opción, por lo que \_ REUSEADDR, y el segundo enlace realiza una, de modo que \_ REUSEADDR, el segundo socket ha sobrecargado el puerto y el comportamiento con respecto a qué socket recibirá los paquetes sin determinar.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-177">In the case where the first bind sets no options or SO\_REUSEADDR, and the second bind performs a SO\_REUSEADDR, the second socket has overtaken the port and behavior regarding which socket will receive packets is undetermined.</span></span> <span data-ttu-id="f2f3d-178">Por lo tanto, \_ se presentó EXCLUSIVEADDRUSE para abordar esta situación.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-178">SO\_EXCLUSIVEADDRUSE was introduced to address this situation.</span></span>

<span data-ttu-id="f2f3d-179">\_No siempre se puede volver a usar un socket con EXCLUSIVEADDRUSE Set inmediatamente después del cierre del socket.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-179">A socket with SO\_EXCLUSIVEADDRUSE set cannot always be reused immediately after socket closure.</span></span> <span data-ttu-id="f2f3d-180">Por ejemplo, si un socket de escucha con el conjunto de marcas exclusivo acepta una conexión después de la cual se cierra el socket de escucha, otro socket no puede enlazar con el mismo puerto que el primer socket de escucha con la marca exclusiva hasta que la conexión aceptada ya no esté activa.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-180">For example, if a listening socket with the exclusive flag set accepts a connection after which the listening socket is closed, another socket cannot bind to the same port as the first listening socket with the exclusive flag until the accepted connection is no longer active.</span></span>

<span data-ttu-id="f2f3d-181">Esta situación puede ser bastante complicada; Aunque el socket se ha cerrado, es posible que el transporte subyacente no termine su conexión.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-181">This situation can be quite complicated; even though the socket has been closed, the underlying transport may not terminate its connection.</span></span> <span data-ttu-id="f2f3d-182">Incluso después de cerrar el socket, el sistema debe enviar todos los datos almacenados en búfer, transmitir una desconexión correcta al elemento del mismo nivel y esperar a que se desconecten correctamente del elemento del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-182">Even after the socket is closed, the system must send all of the buffered data, transmit a graceful disconnect to the peer, and wait for a graceful disconnect from the peer.</span></span> <span data-ttu-id="f2f3d-183">Por lo tanto, es posible que el transporte subyacente nunca libere la conexión, por ejemplo, cuando el elemento del mismo nivel anuncia una ventana de tamaño cero u otros ataques de este tipo.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-183">It is therefore possible that the underlying transport may never release the connection, such as when the peer advertises a zero-size window, or other such attacks.</span></span> <span data-ttu-id="f2f3d-184">En el ejemplo anterior, el socket de escucha se cerró después de aceptar una conexión de cliente.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-184">In the previous example, the listening socket was closed after a client connection was accepted.</span></span> <span data-ttu-id="f2f3d-185">Ahora incluso si la conexión de cliente está cerrada, es posible que el puerto todavía no se reutilice si la conexión de cliente permanece en estado activo debido a datos no confirmados, etc.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-185">Now even if the client connection is closed, the port still may not be reused if the client connection remains in an active state because of unacknowledged data, and so forth.</span></span>

<span data-ttu-id="f2f3d-186">Para evitar esta situación, las aplicaciones deben garantizar un cierre estable: llamar a [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) con la \_ marca de envío SD y, después, esperar en un bucle [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) hasta que se devuelvan cero bytes.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-186">To avoid this situation, applications should ensure a graceful shutdown: call [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) with the SD\_SEND flag, then wait in a [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) loop until zero bytes are returned.</span></span> <span data-ttu-id="f2f3d-187">De este modo, se evita el problema asociado a la reutilización de puertos, se garantiza que todos los datos los recibió el elemento del mismo nivel y se garantiza que todos sus datos se recibieron correctamente.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-187">Doing so avoids the problem associated with port reuse, guarantees all data was received by the peer, and assures the peer that all its data was successfully received.</span></span>

<span data-ttu-id="f2f3d-188">La \_ opción so persistente se puede establecer en un socket para evitar que el puerto pase a uno de los Estados de espera activos; sin embargo, no se recomienda hacerlo porque puede provocar efectos no deseados, ya que puede provocar que se restablezca la conexión.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-188">The SO\_LINGER option may be set on a socket to prevent the port going into one of the active wait states; however, doing so is discouraged because it can lead to undesired effects, because it can cause the connection to be reset.</span></span> <span data-ttu-id="f2f3d-189">Por ejemplo, si los datos se han recibido pero aún no han sido confirmados por el elemento del mismo nivel y el equipo local cierra el socket con este \_ conjunto de permanencia, se restablece la conexión y el elemento del mismo nivel descarta los datos no confirmados.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-189">For example, if data has been received but not yet acknowledged by the peer, and the local computer closes the socket with SO\_LINGER set, the connection is reset and the peer discards the unacknowledged data.</span></span> <span data-ttu-id="f2f3d-190">Además, es difícil elegir un período de permanencia adecuado. un valor demasiado pequeño resulta en muchas conexiones anuladas, mientras que un tiempo de espera grande puede dejar que el sistema sea vulnerable a ataques de denegación de servicio mediante el establecimiento de muchas conexiones y, por tanto, la detención de numerosos subprocesos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-190">Also, picking a suitable time to linger is difficult; a value too small results in many aborted connections, while a large timeout can leave the system vulnerable to denial of service attacks by establishing many connections, and thereby stalling numerous application threads.</span></span>

> [!Note]  
> <span data-ttu-id="f2f3d-191">Un socket que use la opción for \_ EXCLUSIVEADDRUSE debe cerrarse correctamente antes de cerrarlo.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-191">A socket that is using the SO\_EXCLUSIVEADDRUSE option must be shut down properly prior to closing it.</span></span> <span data-ttu-id="f2f3d-192">Si no lo hace, puede producirse un ataque de denegación de servicio si el servicio asociado tiene que reiniciarse.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-192">Failure to do so can cause a denial of service attack if the associated service needs to restart.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f2f3d-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2f3d-193">Requirements</span></span>



| <span data-ttu-id="f2f3d-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2f3d-194">Requirement</span></span> | <span data-ttu-id="f2f3d-195">Value</span><span class="sxs-lookup"><span data-stu-id="f2f3d-195">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2f3d-196">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2f3d-196">Minimum supported client</span></span><br/> | <span data-ttu-id="f2f3d-197">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f2f3d-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f2f3d-198">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2f3d-198">Minimum supported server</span></span><br/> | <span data-ttu-id="f2f3d-199">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f2f3d-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2f3d-200">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2f3d-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2f3d-201"><dt>WinSock2. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2f3d-201"><dt>Winsock2.h</dt></span></span> </dl> |



 

 




