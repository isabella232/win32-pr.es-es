---
description: El código de control asocia un socket a una reserva persistente o en tiempo de ejecución para un bloque de TCP o UDP identificado por el token de reserva de puerto.
ms.assetid: 4CBFB5F8-1FA1-44BA-9932-6F0329A465CB
title: SIO_ASSOCIATE_PORT_RESERVATION código de control
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: a427cec68124cf0132b13a8d8420311106e8c8f3ba647ddcc912ef7f1415fb0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244955"
---
# <a name="sio_associate_port_reservation-control-code"></a>SIO_ASSOCIATE_PORT_RESERVATION código de control

## <a name="description"></a>Descripción

El código de control **SIO \_ ASSOCIATE PORT \_ \_ RESERVATION** asocia un socket a una reserva persistente o en tiempo de ejecución para un bloque de TCP o UDP identificado por el token de reserva de puertos.
Esta IOCTL debe emitirse antes de enlazar el socket.
Si y cuando se enlaza el socket, el puerto asignado a él se seleccionará de la reserva de puertos identificada por el token especificado.
Si no hay puertos disponibles en la reserva especificada, se producirá un error en la llamada [**a**](/windows/desktop/api/winsock/nf-winsock-bind) la función de enlace.

Para realizar esta operación, llame a la [**función WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a>Parámetros

### <a name="s"></a>s

Descriptor que identifica un socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Código de control de la operación.
Use **SIO \_ ASSOCIATE PORT \_ RESERVATION \_ para** esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada.
Este parámetro contiene un puntero a una [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) con el token para que la reserva de puertos TCP o UDP se asocie al socket.

### <a name="cbinbuffer"></a>cbInBuffer

Tamaño, en bytes, del búfer de entrada.
Este parámetro debe ser al menos el tamaño de la [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) estructura.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntero al búfer de salida.
Este parámetro no se usa para esta operación.

### <a name="cboutbuffer"></a>cbOutBuffer

Tamaño, en bytes, del búfer de salida.
Este parámetro debe establecerse en cero.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.

Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *lpcbBytesReturned* apunta a un valor **DWORD** de cero.

Si *lpOverlapped* es **NULL**, el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve en una llamada correcta no puede ser cero.

Si el *parámetro lpOverlapped* no es **NULL** para los sockets superpuestos, se iniciarán las operaciones que no se pueden completar inmediatamente y la finalización se indicará más adelante.
El **valor DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que el tamaño de los datos almacenados no se puede determinar hasta que se haya completado la operación superpuesta.
El estado de finalización final se puede recuperar cuando se señala el método de finalización adecuado cuando se ha completado la operación.

### <a name="lpvoverlapped"></a>lpvOverlapped

Puntero a una [**estructura WSAOVERLAPPED.**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

Si se *crearon sockets* sin el atributo superpuesto, se omite el parámetro *lpOverlapped.*

Si *s* se abrió con el atributo superpuesto y el parámetro *lpOverlapped* no es **NULL,** la operación se realiza como una operación superpuesta (asincrónica).
En este caso, *el parámetro lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.

En el caso de las operaciones superpuestas, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelve inmediatamente y se señala el método de finalización adecuado cuando se ha completado la operación.
De lo contrario, la función no se devuelve hasta que se ha completado la operación o se produce un error.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Puntero a la rutina de finalización a la que se llama cuando se ha completado la operación (se omite para los sockets no superpuestos).

### <a name="lpthreadid"></a>lpThreadId

Puntero a una [**estructura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que usará el proveedor en una llamada posterior a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).
El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc.**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)

**Nota**  Este parámetro solo se aplica a la **función WSPIoctl.**

### <a name="lperrno"></a>lpErrno

Puntero al código de error.

**Nota**  Este parámetro solo se aplica a la **función WSPIoctl.**

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, la [**función WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.

Si se produce un error en la operación o está pendiente, la [**función WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve **SOCKET \_ ERROR**.
Para obtener información de error extendida, llame [**a WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Código de error | Significado |
|------------|---------|
|**WSA \_ IO \_ PENDING** | La operación de E/S superpuesta está en curso. Este valor se devuelve si una operación superpuesta se inició correctamente y la finalización se indicará más adelante. |
| **WSA \_ OPERATION \_ ABORTED** | La operación de E/S se ha anulado debido a una salida del subproceso o a una solicitud de aplicación. Este error se devuelve si se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **\_ IOCTL DE SIO FLUSH.** |
| **WSAEACCES** | Se intentó acceder a un socket de una manera prohibida por sus permisos de acceso. Este error se devuelve en varias condiciones para las reservas de puertos persistentes que incluyen lo siguiente: el usuario carece de los privilegios administrativos necesarios en el equipo local o la aplicación no se ejecuta en un shell mejorado como administrador integrado ( `RunAs administrator` ). |
| **WSAEFAULT** | El sistema detectó una dirección de puntero no válida al intentar usar un argumento de puntero en una llamada. Este error se devuelve del parámetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no está totalmente contenido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | Se está ejecutando una operación de bloqueo actualmente. Este error se devuelve si se invoca la función cuando hay una devolución de llamada en curso. |
| **WSAEINTR** | Una llamada a [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)interrumpió una operación de bloqueo. Este error se devuelve si se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | Se proporcionó un argumento no válido. Este error se devuelve si el parámetro *dwIoControlCode* no es un comando válido, un parámetro de entrada especificado no es aceptable o el comando no es aplicable al tipo de socket especificado. |
| **WSAENETDOWN** | Una operación de socket encontró una red inactiva. Este error se devuelve si se ha producido un error en el subsistema de red. |
| **WSAENOTSOCK** | Se intentó realizar una operación en algo que no es un socket. Este error se devuelve si el descriptor *s* no es un socket. |
| **WSAEOPNOTSUPP** | La operación intentada no se admite para el tipo de objeto al que se hace referencia. Este error se devuelve si no se admite el comando IOCTL especificado. Este error también se devuelve si el proveedor de transporte no admite **SIO \_ ASSOCIATE PORT \_ \_ RESERVATION** IOCTL. Este error también se devuelve cuando se intenta usar **SIO \_ ASSOCIATE PORT \_ \_ RESERVATION** IOCTL en un socket distinto de UDP o TCP. |

## <a name="remarks"></a>Observaciones

**SIO \_ ASSOCIATE \_ PORT \_ RESERVATION** IOCTL se admite en Windows Vista y versiones posteriores del sistema operativo.

Las aplicaciones y los servicios que necesitan reservar puertos se divide en dos categorías.
La primera categoría incluye componentes que necesitan un puerto determinado como parte de su operación.
Por lo general, estos componentes prefieren especificar su puerto necesario en el momento de la instalación (por ejemplo, en un manifiesto de aplicación).
La segunda categoría incluye componentes que necesitan cualquier puerto o bloque de puertos disponible en tiempo de ejecución.
Estas dos categorías corresponden a solicitudes de reserva de puertos específicos y comodín.
Las solicitudes de reserva específicas pueden ser persistentes o en tiempo de ejecución, mientras que las solicitudes de reserva de puerto comodín solo se admiten en tiempo de ejecución.

**SIO \_ ASSOCIATE PORT \_ \_ RESERVATION** IOCTL se usa para asociar una reserva de puerto TCP o UDP con una reserva persistente o en tiempo de ejecución.

La [**función CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) proporciona la capacidad de una aplicación o servicio de reservar un bloque persistente de puertos TCP o UDP.
Las reservas de puertos persistentes se registran en un almacén persistente para el módulo TCP o UDP en Windows.
Tenga en cuenta que el token de una reserva de puerto persistente determinada puede cambiar cada vez que se reinicia el sistema.

Una vez que se ha obtenido una reserva de puerto TCP o UDP persistente, una aplicación puede solicitar asignaciones de puertos de la reserva de puertos abriendo un socket TCP [](/windows/desktop/api/winsock/nf-winsock-bind) o UDP y, a continuación, llamando a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) especificando **SIO \_ ASSOCIATE \_ PORT \_ RESERVATION** IOCTL y pasando el token de reserva antes de emitir una llamada a la función de enlace en el socket.

La [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL se puede usar para solicitar una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP.
Para las reservas de puertos en tiempo de ejecución, el grupo de puertos requiere que las reservas se consuman desde el proceso en cuyo socket se concedió la reserva.
Las reservas de puertos en tiempo de ejecución solo duren mientras dure el socket en el que [**se llamó SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL.
Por el contrario, cualquier proceso puede consumir las reservas de puertos persistentes creadas mediante la función [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) con la capacidad de obtener reservas persistentes.

Una vez que se ha obtenido una reserva de puerto TCP o UDP en tiempo de ejecución, una aplicación puede solicitar asignaciones de puerto de la reserva de puertos abriendo [](/windows/desktop/api/winsock/nf-winsock-bind) un socket TCP o UDP y, a continuación, llamando a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) especificando **SIO \_ ASSOCIATE \_ PORT \_ RESERVATION** IOCTL y pasando el token de reserva antes de emitir una llamada a la función de enlace en el socket.

Si los parámetros *lpOverlapped* y *lpCompletionRoutine* son NULL, el socket de esta función se tratará como un socket no superpuesto.
En el caso de un socket no superpuesto, se omiten los parámetros *lpOverlapped* y *lpCompletionRoutine,* salvo que la función puede bloquearse si el socket *s* está en modo de bloqueo.
Si el socket *s* está en modo de no bloqueo, esta función se bloqueará, ya que esta IOCTL concreta no admite el modo de no bloqueo.

En el caso de los sockets superpuestos, se iniciarán las operaciones que no se pueden completar inmediatamente y la finalización se indicará más adelante.

Cualquier IOCTL puede bloquearse indefinidamente, en función de la implementación del proveedor de servicios.
Si la aplicación no puede tolerar el bloqueo en una llamada de función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl,** se recomienda la E/S superpuesta para las E/STO que son especialmente probables que se bloqueen.

**SIO \_ ASSOCIATE PORT \_ \_ RESERVATION** IOCTL puede producir un error **con WSAEINTR** o **WSA_OPERATION_ABORTED** en los casos siguientes:

* El Administrador de E/S cancela la solicitud.
* El socket está cerrado.

La **IOCTL SIO \_ ASSOCIATE PORT \_ \_ RESERVATION** pasada a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** para una reserva de puerto persistente solo se puede usar en una aplicación cuando el usuario ha iniciado sesión como miembro del grupo Administradores.
Si **SIO \_ ASSOCIATE PORT \_ \_ RESERVATION** IOCTL se usa en una aplicación cuando el usuario no es miembro del grupo Administradores, se producirá un error en la llamada de función y se devolverá **WSAEACCES.**
El uso de **SIO \_ ASSOCIATE PORT \_ \_ RESERVATION** IOCTL también puede producir un error debido al control de cuentas de usuario (UAC) en Windows Vista y versiones posteriores.
Si una aplicación que usa esta IOCTL con una reserva de puerto persistente la ejecuta un usuario que inició sesión como miembro del grupo Administradores que no sea el administrador integrado, esta llamada producirá un error a menos que la aplicación se haya marcado en el archivo de manifiesto con un **requestedExecutionLevel** establecido en *requireAdministrator*.
Si la aplicación no tiene este archivo de manifiesto, un usuario que haya iniciado sesión como miembro del grupo Administradores distinto del administrador integrado debe ejecutar la aplicación en un shell mejorado como administrador integrado ( ) para que esta función se ejecute `RunAs administrator` correctamente.

## <a name="see-also"></a>Vea también

[**Atar**](/windows/desktop/api/winsock/nf-winsock-bind)

[**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[**DeletePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[**DeletePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[**LookupPersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[**LookupPersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md)

[**SIO_RELEASE_PORT_RESERVATION**](sio-release-port-reservation.md)

[Zócalo](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
