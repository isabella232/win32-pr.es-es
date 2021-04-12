---
description: El código de control asocia un socket con una reserva persistente o en tiempo de ejecución para un bloque de TCP o UDP identificado por el token de reserva de puerto.
ms.assetid: 4CBFB5F8-1FA1-44BA-9932-6F0329A465CB
title: Código de control de SIO_ASSOCIATE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 69af4f396fabd32f948d7e43cbf348aa34fb1a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278093"
---
# <a name="sio_associate_port_reservation-control-code"></a>Código de control de SIO_ASSOCIATE_PORT_RESERVATION

## <a name="description"></a>Descripción

El código de control de **\_ \_ \_ reserva de puerto asociado de SiO** asocia un socket con una reserva persistente o en tiempo de ejecución para un bloque de TCP o UDP identificado por el token de reserva de puerto.
Este IOCTL debe emitirse antes de enlazar el socket.
Si y cuando se enlaza el socket, el puerto asignado a él se seleccionará en la reserva de Puerto identificada por el token especificado.
Si no hay puertos disponibles en la reserva especificada, se producirá un error en la llamada a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) .

Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

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

Un descriptor que identifica un socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Código de control de la operación.
Use **SiO \_ asociar el \_ Puerto de \_ reserva** para esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada.
Este parámetro contiene un puntero a una estructura de [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) con el token para la reserva de puerto TCP o UDP que se va a asociar al socket.

### <a name="cbinbuffer"></a>cbInBuffer

Tamaño, en bytes, del búfer de entrada.
Este parámetro debe ser al menos el tamaño de la estructura [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) .

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntero al búfer de salida.
Este parámetro no se usa para esta operación.

### <a name="cboutbuffer"></a>cbOutBuffer

Tamaño, en bytes, del búfer de salida.
Este parámetro debe establecerse en cero.

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

Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).
El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .

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
| **\_operación WSA \_ anulada** | La operación de e/s se ha anulado debido a una salida de subproceso o una solicitud de aplicación. Se devuelve este error si se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando de **\_ ioctl de volcado de SiO** . |
| **WSAEACCES** | Se intentó tener acceso a un socket de una manera prohibida por sus permisos de acceso. Este error se devuelve en varias condiciones para las reservas de Puerto persistentes que incluyen lo siguiente: el usuario no dispone de los privilegios administrativos necesarios en el equipo local o la aplicación no se está ejecutando en un shell mejorado como administrador integrado ( `RunAs administrator` ). |
| **WSAEFAULT** | El sistema detectó una dirección de puntero no válida al intentar usar un argumento de puntero en una llamada. Este error se devuelve cuando el parámetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | Se está ejecutando una operación de bloqueo actualmente. Se devuelve este error si la función se invoca cuando hay una devolución de llamada en curso. |
| **WSAEINTR** | Una operación de bloqueo fue interrumpida por una llamada a [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall). Se devuelve este error si se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | Se proporcionó un argumento no válido. Se devuelve este error si el parámetro *dwIoControlCode* no es un comando válido o si un parámetro de entrada especificado no es aceptable, o si el comando no es aplicable al tipo de socket especificado. |
| **WSAENETDOWN** | Una operación de socket encontró una red inactiva. Se devuelve este error si se ha producido un error en el subsistema de red. |
| **WSAENOTSOCK** | Se intentó realizar una operación en algo que no es un socket. Se devuelve este error si el *descriptor* no es un socket. |
| **WSAEOPNOTSUPP** | La operación intentada no se admite para el tipo de objeto al que se hace referencia. Se devuelve este error si no se admite el comando IOCTL especificado. Este error también se devuelve si el proveedor de transporte no admite el ioctl de **reserva de puertos de Asociación de SiO \_ \_ \_** . Este error también se devuelve cuando se realiza un intento de usar el ioctl de reserva de puerto del asociado de SiO en un socket distinto de UDP o TCP. **\_ \_ \_** |

## <a name="remarks"></a>Observaciones

Se admite el ioctl de reserva de puertos de Asociación de SiO en Windows Vista y versiones posteriores del sistema operativo. **\_ \_ \_**

Las aplicaciones y los servicios que necesitan reservar puertos se dividen en dos categorías.
La primera categoría incluye componentes que necesitan un puerto determinado como parte de su funcionamiento.
Por lo general, estos componentes prefieren especificar su puerto necesario en el momento de la instalación (por ejemplo, en un manifiesto de aplicación).
La segunda categoría incluye componentes que necesitan cualquier puerto o bloque de puertos disponible en tiempo de ejecución.
Estas dos categorías corresponden a las solicitudes de reserva de puertos específicos y comodín.
Las solicitudes de reserva específicas pueden ser persistentes o en tiempo de ejecución, mientras que las solicitudes de reserva de Puerto comodín solo se admiten en tiempo de ejecución.

Se usa el ioctl de **reserva de puertos de Asociación de SiO \_ \_ \_** para asociar una reserva de puerto TCP o UDP con una reserva persistente o en tiempo de ejecución.

La función [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) proporciona la capacidad de una aplicación o servicio para reservar un bloque persistente de puertos TCP o UDP.
Las reservas de Puerto persistentes se registran en un almacén persistente para el módulo TCP o UDP en Windows.
Tenga en cuenta que el token de una reserva de Puerto persistente determinada puede cambiar cada vez que se reinicia el sistema.

Una vez obtenida una reserva de puerto TCP o UDP persistente, una aplicación puede solicitar asignaciones de puerto desde la reserva de Puerto abriendo un socket TCP o UDP y, a continuación, llamando a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) especificando el ioctl de reserva de puertos de Asociación de SiO y pasando el token de reserva antes de emitir una llamada a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) en el socket. **\_ \_ \_**

El [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) ioctl se puede usar para solicitar una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP.
En el caso de las reservas de puerto en tiempo de ejecución, el grupo de puertos requiere que se consuman reservas del proceso en cuyo socket se concedió la reserva.
Las reservas de puerto en tiempo de ejecución solo duran el tiempo que dure el socket en el que se llamó a la [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) ioctl.
Por el contrario, cualquier proceso puede consumir reservas de Puerto persistentes creadas con la función [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) con la capacidad de obtener reservas persistentes.

Una vez que se ha obtenido una reserva de puerto TCP o UDP en tiempo de ejecución, una aplicación puede solicitar asignaciones de puerto desde la reserva de puerto mediante la apertura de un socket TCP o UDP y, a continuación, una llamada a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) que especifica el ioctl de reserva de [](/windows/desktop/api/winsock/nf-winsock-bind) puertos de Asociación de SiO y el token de reserva antes de emitir una llamada a la función BIND en el socket **\_ \_ \_**

Si los parámetros *lpOverlapped* y *lpCompletionRoutine* son NULL, el socket de esta función se tratará como un socket no superpuesto.
En el caso de un socket no superpuesto, se omiten los parámetros *lpOverlapped* y *lpCompletionRoutine* , salvo que la función puede bloquearse si socket *s* está en modo de bloqueo.
Si socket *s* está en modo de no bloqueo, esta función seguirá bloqueando, ya que este ioctl determinado no admite el modo de no bloqueo.

En el caso de los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.

Cualquier IOCTL puede bloquearse indefinidamente, dependiendo de la implementación del proveedor de servicios.
Si la aplicación no puede tolerar el bloqueo en una llamada de función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** , se aconsejará la e/s superpuesta para los IOCTL que es especialmente probable que se bloqueen.

Se puede producir un error en el ioctl de  **reserva de \_ \_ puertos \_ de asociación** de **WSA_OPERATION_ABORTED** WSAEINTR en los siguientes casos:

* El administrador de e/s cancela la solicitud.
* El socket está cerrado.

El ioctl de reserva de puerto de Asociación de la **\_ Asociación \_ \_** IOCTL que se pasa a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** para una reserva de Puerto persistente solo se puede usar en una aplicación cuando el usuario ha iniciado sesión como miembro del grupo administradores.
Si se usa **SiO \_ Associate de \_ \_ reserva de Puerto** ioctl en una aplicación cuando el usuario no es miembro del grupo de administradores, se producirá un error en la llamada a la función y se devolverá **WSAEACCES** .
También se puede producir un error en el uso del ioctl de reserva de puertos de Asociación de SiO en Windows Vista y versiones posteriores. **\_ \_ \_**
Si una aplicación que usa este IOCTL con una reserva de Puerto persistente es ejecutada por un usuario que ha iniciado sesión como miembro del grupo de administradores distinto del administrador integrado, esta llamada producirá un error a menos que la aplicación se haya marcado en el archivo de manifiesto con una **requestedExecutionLevel** establecida en *requireAdministrator*.
Si la aplicación no tiene este archivo de manifiesto, un usuario que haya iniciado sesión como miembro del grupo administradores que no sea el administrador integrado deberá ejecutar la aplicación en un shell mejorado como administrador integrado ( `RunAs administrator` ) para que esta función se ejecute correctamente.

## <a name="see-also"></a>Vea también

[**volver**](/windows/desktop/api/winsock/nf-winsock-bind)

[**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[**DeletePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[**DeletePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[**LookupPersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[**LookupPersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md)

[**SIO_RELEASE_PORT_RESERVATION**](sio-release-port-reservation.md)

[tomacorriente](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
