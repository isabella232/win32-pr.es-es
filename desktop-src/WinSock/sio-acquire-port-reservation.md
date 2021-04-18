---
description: El código de control adquiere una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP.
ms.assetid: 1A2E3920-88D2-4109-B7EF-E66BD4AB6153
title: Código de control de SIO_ACQUIRE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8eab53aeb945837b55c70560294b2fc295160a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720498"
---
# <a name="sio_acquire_port_reservation-control-code"></a>Código de control de SIO_ACQUIRE_PORT_RESERVATION

## <a name="description"></a>Descripción

El código de control de reserva de puerto de adquisición de SiO adquiere una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP. **\_ \_ \_**

Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to an INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to a INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a>Parámetros

### <a name="s"></a>s

Un descriptor que identifica un socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Código de control de la operación.
Utilice **la \_ \_ \_ reserva de puerto de adquisición de SiO**  para esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada.
Este parámetro contiene un puntero a una estructura de [**\_ \_ intervalo de puertos inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) que especifica el número de punto inicial y el número de puertos que se van a reservar.

### <a name="cbinbuffer"></a>cbInBuffer

Tamaño, en bytes, del búfer de entrada.
Este parámetro debe ser el tamaño de la estructura de [**\_ \_ intervalo de puertos inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) .

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntero al búfer de salida.
Si el resultado es correcto, este parámetro contiene un puntero a una estructura de [**\_ instancia de \_ reserva \_ de Puerto inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) .

### <a name="cboutbuffer"></a>cbOutBuffer

Tamaño, en bytes, del búfer de salida.
Este parámetro debe ser al menos el tamaño de la estructura de la [**\_ instancia de \_ reserva \_ de Puerto inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) .

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.

Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *LpcbBytesReturned* apunta a un valor **DWORD** de cero.

Si *lpOverlapped* es **null**, el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* devuelto en una llamada correcta no puede ser cero.

Si el parámetro *lpOverlapped* no es **null** para los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.
El valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que no se puede determinar el tamaño de los datos almacenados hasta que se haya completado la operación superpuesta.
Se puede recuperar el estado final de finalización cuando se señala el método de finalización adecuado cuando se ha completado la operación.

### <a name="lpvoverlapped"></a>lpvOverlapped

Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .

Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .

Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).
En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.

En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.
De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).

### <a name="lpthreadid"></a>lpThreadId

Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a **WPUQueueApc**.
El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función **WPUQueueApc** .

**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .

### <a name="lperrno"></a>lpErrno

Puntero al código de error.

**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.

Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.
Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Código de error | Significado |
|------------|---------|
|**\_e/s de WSA \_ pendientes** | La operación de e/s superpuesta está en curso. Se devuelve este valor si una operación superpuesta se ha iniciado correctamente y la finalización se indicará en un momento posterior. |
| **\_operación WSA \_ anulada** | La operación de e/s se ha anulado debido a una salida de subproceso o una solicitud de aplicación. Se devuelve este error si se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando de ioctl de **\_ volcado de SiO** . |
| **WSAEFAULT** | El sistema detectó una dirección de puntero no válida al intentar usar un argumento de puntero en una llamada. Este error se devuelve cuando el parámetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | Se está ejecutando una operación de bloqueo actualmente. Se devuelve este error si la función se invoca cuando hay una devolución de llamada en curso. |
| **WSAEINTR** | Una operación de bloqueo fue interrumpida por una llamada a [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall). Se devuelve este error si se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | Se proporcionó un argumento no válido. Se devuelve este error si el parámetro *dwIoControlCode* no es un comando válido o si un parámetro de entrada especificado no es aceptable, o si el comando no es aplicable al tipo de socket especificado. |
| **WSAENETDOWN** | Una operación de socket encontró una red inactiva. Se devuelve este error si se ha producido un error en el subsistema de red. |
| **WSAENOTSOCK** | Se intentó realizar una operación en algo que no es un socket. Se devuelve este error si el *descriptor* no es un socket. |
| **WSAEOPNOTSUPP** | La operación intentada no se admite para el tipo de objeto al que se hace referencia. Se devuelve este error si no se admite el comando IOCTL especificado. Este error también se devuelve si el proveedor de transporte no admite el ioctl de **reserva de puertos de adquisición de SiO \_ \_ \_** . Este error también se devuelve cuando un intento de usar el ioctl de reserva de puerto de adquisición de SiO se realiza en un socket distinto de UDP o TCP. **\_ \_ \_** |

## <a name="remarks"></a>Observaciones

El ioctl de reserva de puertos de adquisición de SiO es compatible con Windows Vista y versiones posteriores del sistema operativo. **\_ \_ \_**

Las aplicaciones y los servicios que necesitan reservar puertos se dividen en dos categorías.
La primera categoría incluye componentes que necesitan un puerto determinado como parte de su funcionamiento.
Por lo general, estos componentes prefieren especificar su puerto necesario en el momento de la instalación (por ejemplo, en un manifiesto de aplicación).
La segunda categoría incluye componentes que necesitan cualquier puerto o bloque de puertos disponible en tiempo de ejecución.
Estas dos categorías corresponden a las solicitudes de reserva de puertos específicos y comodín.
Las solicitudes de reserva específicas pueden ser persistentes o en tiempo de ejecución, mientras que las solicitudes de reserva de Puerto comodín solo se admiten en tiempo de ejecución.

El ioctl de reserva de puertos de adquisición de SiO se usa para solicitar una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP. **\_ \_ \_**
En el caso de las reservas de puerto en tiempo de ejecución, el grupo de puertos requiere que se consuman reservas del proceso en cuyo socket se concedió la reserva.
Las reservas de puerto en tiempo de ejecución solo duran el tiempo que dure el socket en el que se llamó al método de **adquisición de puerto de adquisición de SiO \_ \_ \_**  .
Por el contrario, cualquier proceso puede consumir reservas de Puerto persistentes creadas con la función [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) con la capacidad de obtener reservas persistentes.

Una vez que se ha obtenido una reserva de puerto TCP o UDP en tiempo de ejecución, una aplicación puede solicitar asignaciones de puerto desde la reserva de puerto mediante la apertura de un socket TCP o UDP y, a continuación, una llamada a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) que especifica el ioctl de reserva de puertos de Asociación de SiO y el token de reserva antes de emitir una llamada a la función BIND en el socket [**\_ \_ \_**](sio-associate-port-reservation.md)

Si los parámetros *lpOverlapped* y *lpCompletionRoutine* son **null**, el socket de esta función se tratará como un socket no superpuesto.
En el caso de un socket no superpuesto, se omiten los parámetros *lpOverlapped* y *lpCompletionRoutine* , salvo que la función puede bloquearse si socket *s* está en modo de bloqueo.
Si socket *s* está en modo de no bloqueo, esta función seguirá bloqueando, ya que este ioctl determinado no admite el modo de no bloqueo.

En el caso de los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.

Cualquier IOCTL puede bloquearse indefinidamente, dependiendo de la implementación del proveedor de servicios.
Si la aplicación no puede tolerar el bloqueo en una llamada de función WSAIoctl o **WSPIoctl** , se aconsejará la e/s superpuesta para los IOCTL que es especialmente probable que se bloqueen.

Se puede producir un error en la operación de  adquisición de **Puerto de \_ adquisición \_ \_ SiO** ioctl con WSAEINTR o **WSA \_ \_ anulada** en los siguientes casos:

* El administrador de e/s cancela la solicitud.
* El socket está cerrado.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se adquiere una reserva de puerto en tiempo de ejecución, se crea un socket y se asigna un puerto a partir de la reserva de puerto en tiempo de ejecución para el socket y, a continuación, se cierra el socket y se libera la reserva de puertos en tiempo de ejecución.

```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h.>
#include <winsock2.h>
#include <mstcpip.h>
#include <ws2ipdef.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Ws2_32.lib for Winsock functions
#pragma comment(lib, "ws2_32.lib")

int wmain(int argc, WCHAR ** argv)
{

    // Declare and initialize variables

    int startPort = 0;          // host byte order
    int numPorts = 0;
    USHORT startPortns = 0;     // Network byte order

    INET_PORT_RANGE portRange = { 0 };
    INET_PORT_RESERVATION_INSTANCE portRes = { 0 };

    unsigned long status = 0;

    WSADATA wsaData = { 0 };
    int iResult = 0;

    SOCKET sock = INVALID_SOCKET;
    int iFamily = AF_INET;
    int iType = 0;
    int iProtocol = 0;

    SOCKET sockRes = INVALID_SOCKET;

    DWORD bytesReturned = 0;

    // Note that the sockaddr_in struct works only with AF_INET not AF_INET6
    // An application needs to use the sockaddr_in6 for AF_INET6
    sockaddr_in service;
    sockaddr_in sockName;
    int nameLen = sizeof (sockName);

    // Validate the parameters
    if (argc != 6) {
        wprintf
            (L"usage: %s <addressfamily> <type> <protocol> <StartingPort> <NumberOfPorts>\n",
             argv[0]);
        wprintf(L"Opens a socket for the specified family, type, & protocol\n");
        wprintf
            (L"and then acquires a runtime port reservation for the protocol specified\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 2 2 17 5000 20\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_DGRAM=2 IPPROTO_UDP=17 StartPort=5000 NumPorts=20", argv[0]);

        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    startPort = _wtoi(argv[4]);
    if (startPort < 0 || startPort > 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }
    startPortns = htons((USHORT) startPort);

    numPorts = _wtoi(argv[5]);
    if (numPorts < 0) {
        wprintf(L"Number of ports must be a positive number\n");
        return 1;
    }

    portRange.StartPort = startPortns;
    portRange.NumberOfPorts = (USHORT) numPorts;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error = %d\n", iResult);
        return 1;
    }

    sock = socket(iFamily, iType, iProtocol);
    if (sock == INVALID_SOCKET) {
        wprintf(L"socket function failed with error = %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    } else {
        wprintf(L"socket function succeeded\n");

        iResult =
            WSAIoctl(sock, SIO_ACQUIRE_PORT_RESERVATION, (LPVOID) & portRange,
                     sizeof (INET_PORT_RANGE), (LPVOID) & portRes,
                     sizeof (INET_PORT_RESERVATION_INSTANCE), &bytesReturned, NULL, NULL);
        if (iResult != 0) {
            wprintf(L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) failed with error = %d\n",
                    WSAGetLastError());
            closesocket(sock);
            WSACleanup();
            return 1;
        } else {
            wprintf
                (L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                 bytesReturned);
            wprintf(L"  Starting port=%d,  Number of Ports=%d, Token=%I64d\n",
                    htons(portRes.Reservation.StartPort),
                    portRes.Reservation.NumberOfPorts, portRes.Token);

            sockRes = socket(iFamily, iType, iProtocol);
            if (sockRes == INVALID_SOCKET) {
                wprintf(L"socket function for second socket failed with error = %d\n",
                        WSAGetLastError());
                closesocket(sock);
                WSACleanup();
                return 1;
            } else {
                wprintf(L"socket function for second socket succeeded\n");

                iResult =
                    WSAIoctl(sock, SIO_ASSOCIATE_PORT_RESERVATION,
                             (LPVOID) & portRes.Token, sizeof (ULONG64), NULL, 0,
                             &bytesReturned, NULL, NULL);
                if (iResult != 0) {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) failed with error = %d\n",
                         WSAGetLastError());
                } else {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                         bytesReturned);

                    service.sin_family = (ADDRESS_FAMILY) iFamily;
                    service.sin_addr.s_addr = INADDR_ANY;
                    service.sin_port = 0;

                    iResult = bind(sock, (SOCKADDR *) & service, sizeof (service));
                    if (iResult == SOCKET_ERROR)
                        wprintf(L"bind failed with error = %d\n", WSAGetLastError());
                    else {
                        wprintf(L"bind succeeded\n");
                        iResult = getsockname(sock, (SOCKADDR *) & sockName, &nameLen);
                        if (iResult == SOCKET_ERROR)
                            wprintf(L"getsockname failed with error = %d\n",
                                    WSAGetLastError());
                        else {
                            wprintf(L"getsockname succeeded\n");
                            wprintf(L"Port number allocated = %u\n",
                                    ntohs(sockName.sin_port));
                        }
                    }
                }
            }

            // comment out this block of code if you don't want to delete the reservation just created
            iResult =
                WSAIoctl(sock, SIO_RELEASE_PORT_RESERVATION, (LPVOID) & portRes.Token,
                         sizeof (ULONG64), NULL, 0, &bytesReturned, NULL, NULL);
            if (iResult != 0) {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) failed with error = %d\n",
                     WSAGetLastError());
            } else {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                     bytesReturned);
            }
        }

        if (sockRes != INVALID_SOCKET) {
            iResult = closesocket(sockRes);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for second socket failed with error = %d\n",
                        WSAGetLastError());
            }
        }
        if (sock != INVALID_SOCKET) {
            iResult = closesocket(sock);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for first socket failed with error = %d\n",
                        WSAGetLastError());
            }
        }
    }

    WSACleanup();

    return 0;
}
```

## <a name="see-also"></a>Vea también

[**acept**](/windows/desktop/api/winsock2/nf-winsock2-accept)

[**volver**](/windows/desktop/api/winsock/nf-winsock-bind)

[**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[**DeletePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[**DeletePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[**\_intervalo de puertos inet \_**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range)

[**\_instancia de \_ reserva de Puerto inet \_**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance)

[**LookupPersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[**LookupPersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[**SIO \_ asociar \_ reserva de puerto \_**](sio-associate-port-reservation.md)

[**versión de la reserva del puerto de lanzamiento de SIO \_ \_ \_**](sio-release-port-reservation.md)

[**tomacorriente**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
