---
description: El código de control notifica a una aplicación cuándo cambia el valor de trabajo pendiente de envío ideal para la conexión.
ms.assetid: 337883a5-7ceb-40d3-b318-b86dd488b94a
title: SIO_IDEAL_SEND_BACKLOG_CHANGE código de control
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: daa4141d3ef00b562082fbcff9804326e12bbef671ae8f5d593009fe9d06b7f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097525"
---
# <a name="sio_ideal_send_backlog_change-control-code"></a>SIO_IDEAL_SEND_BACKLOG_CHANGE código de control

## <a name="description"></a>Descripción

El código de control **\_ SIO IDEAL \_ SEND \_ BACKLOG \_ CHANGE** notifica a una aplicación cuándo cambia el valor ideal del trabajo pendiente de envío (ISB) para la conexión.

Para realizar esta operación, llame a la [**función WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
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
Use **SIO \_ IDEAL SEND \_ \_ BACKLOG \_ CHANGE** para esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada.
Este parámetro no se usa para esta operación.

### <a name="cbinbuffer"></a>cbInBuffer

Tamaño, en bytes, del búfer de entrada. Este parámetro no se usa para esta operación.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntero al búfer de salida.
Este parámetro no se usa para esta operación.

### <a name="cboutbuffer"></a>cbOutBuffer

Tamaño, en bytes, del búfer de salida.
Este parámetro debe establecerse en cero.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.
Este parámetro devuelto apunta a un **valor DWORD** de cero para esta operación, ya que no hay ninguna salida.

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

Puntero a una [**estructura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que usará el proveedor en una llamada posterior a [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).
El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)

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
| **WSA \_ IO \_ PENDING** | Se inició correctamente una operación superpuesta y la finalización se indicará más adelante. |
| **WSA \_ OPERATION \_ ABORTED** | Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **IOCTL DE SIO \_ FLUSH.** |
| **WSAEFAULT** | El *parámetro lpOverlapped* o *lpCompletionRoutine* no está totalmente contenido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | La función se invoca cuando hay una devolución de llamada en curso. |
| **WSAEINTR** | Se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | El *parámetro dwIoControlCode* no es un comando válido, o un parámetro de entrada especificado no es aceptable o el comando no es aplicable al tipo de socket especificado. Este error se devuelve si el *parámetro cbOutBuffer* no es cero. |
| **WSAENETDOWN** | Error en el subsistema de red. |
| **WSAENOPROTOOPT** | La opción socket no se admite en el protocolo especificado. |
| **WSAENOTCONN** | Los *sockets no* están conectados. |
| **WSAENOTSOCK** | El descriptor *s* no es un socket. |
| **WSAEOPNOTSUPP** | No se admite el comando IOCTL especificado. Este error se devuelve si el proveedor de transporte no admite **SIO \_ IDEAL SEND \_ \_ BACKLOG \_ CHANGE** IOCTL. Este error también se devuelve cuando se realiza un intento de usar **SIO \_ IDEAL SEND \_ \_ BACKLOG \_ CHANGE** IOCTL en un socket de datagrama. |

## <a name="remarks"></a>Comentarios

**SIO \_ IDEAL \_ SEND \_ BACKLOG \_ CHANGE** IOCTL se admite en Windows Server 2008, Windows Vista con Service Pack 1 (SP1) y versiones posteriores del sistema operativo.

Al enviar datos a través de una conexión TCP mediante sockets Windows, es importante mantener una cantidad suficiente de datos pendientes (enviados pero aún no reconocidos) en TCP para lograr el máximo rendimiento.
El valor ideal para la cantidad de datos pendientes para lograr el mejor rendimiento para la conexión TCP se denomina tamaño de trabajo pendiente de envío (ISB) ideal.
El valor de ISB es una función del producto de retraso de ancho de banda de la conexión TCP y la ventana de recepción anunciada del receptor (y en parte la cantidad de congestión en la red).

El valor de ISB por conexión está disponible en la implementación del protocolo TCP en Windows Server 2008, Windows Vista con SP1 y versiones posteriores del sistema operativo.
Una aplicación puede usar **SIO \_ IDEAL SEND \_ \_ BACKLOG \_ CHANGE** IOCTL para obtener una notificación cuando el valor de ISB cambia dinámicamente para una conexión.

En Windows Server 2008, Windows Vista con SP1 y versiones posteriores del sistema operativo, las IOCTL DE CONSULTA DE **\_ \_ \_ BACKLOG \_** DE ENVÍO IDEAL DE SIO IDEAL y [**SIO \_ IDEAL SEND \_ \_ BACKLOG \_ QUERY**](sio-ideal-send-backlog-query.md) se admiten en sockets orientados a flujos que se encuentran en un estado conectado.

El intervalo del valor de ISB para una conexión TCP puede variar teóricamente de 0 a un máximo de 16 megabytes.

Consulte la página de referencia de IOCTL DE [**SIO \_ IDEAL SEND \_ \_ BACKLOG \_ QUERY**](sio-ideal-send-backlog-query.md) para el uso típico del mecanismo de ISB para lograr un mejor rendimiento a través de conexiones de productos con un alto retraso de ancho de banda.

**SIO \_ IDEAL SEND \_ \_ BACKLOG \_ CHANGE** IOCTL solo se permite en un socket de secuencia que se encuentra en el estado conectado.
De lo contrario, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) **o WSPIoctl** producirá un error **con WSAENOTCONN**.

**SIO \_ IDEAL \_ SEND \_ BACKLOG \_ CHANGE** IOCTL no usa búferes de entrada o salida ni pends o bloques hasta que se produce un cambio de ISB en la conexión subyacente.
Una vez completada esta IOCTL, una aplicación Winsock puede usar la IOCTL DE CONSULTA DE [**SIO \_ IDEAL SEND \_ \_ BACKLOG \_**](sio-ideal-send-backlog-query.md) para recuperar el nuevo valor de ISB en la conexión.

**SIO \_ IDEAL \_ SEND \_ BACKLOG \_ CHANGE** IOCTL no admite el modo sin bloqueo.
Una aplicación puede emitir esta IOCTL en un socket sin bloqueo, pero la IOCTL simplemente se bloqueará o se bloqueará hasta que cambie el valor de ISB.

Si los parámetros *lpOverlapped* y *lpCompletionRoutine* son NULL, el socket de esta función se tratará como un socket no superpuesto.
En el caso de un socket no superpuesto, se omiten los parámetros *lpOverlapped* y *lpCompletionRoutine,* salvo que la función puede bloquearse si el socket *s* está en modo de bloqueo.
Si el socket *s* está en modo de no bloqueo, esta función se bloqueará, ya que esta IOCTL concreta no admite el modo de no bloqueo.

En el caso de los sockets superpuestos, se iniciarán las operaciones que no se pueden completar inmediatamente y la finalización se indicará más adelante.

Cualquier IOCTL puede bloquearse indefinidamente, en función de la implementación del proveedor de servicios.
Si la aplicación no puede tolerar el bloqueo en una llamada de función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl,** se recomienda la E/S superpuesta para las E/STO que son especialmente probables que se bloqueen.

**SIO \_ IDEAL \_ SEND \_ BACKLOG \_ CHANGE** IOCTL proporciona una notificación y se espera que se bloquee o se bloquee hasta que cambie el valor de ISB.
Por lo tanto, normalmente se llamaría de forma asincrónica con el parámetro *lpOverlapped* establecido en una estructura WSAOVERLAPPED válida.

**SIO \_ IDEAL SEND \_ \_ BACKLOG \_ CHANGE** IOCTL puede producir un error **con WSAEINTR** o **WSA \_ OPERATION \_ ABORTED** en los casos siguientes:

* La conexión TCP se desconecta correctamente en la dirección de envío. Esto puede ocurrir como resultado de una llamada a la función shutdown con el parámetro how establecido en **SD \_ SEND,** una llamada a la función **DisconnectEx** o una llamada a la función **TransmitFile** o **TransmitPackets** con el parámetro *dwFlags* establecido en **TF \_ DISCONNECT** o **TF \_ REUSE.**
* La conexión TCP se ha restablecido o anulado.
* La aplicación emite un **SIO \_ IDEAL SEND \_ \_ BACKLOG \_ CHANGE** IOCTL cuando ya hay una solicitud de notificación de inserción. Solo se permite una solicitud **SIO \_ IDEAL SEND \_ \_ BACKLOG \_ CHANGE** a la vez.
* El Administrador de E/S cancela la solicitud.
* El socket está cerrado.

En el archivo de encabezado *Ws2tcpip.h* se definen dos funciones contenedoras insertadas para estas IOCTL.
Se recomienda usar estas funciones insertadas en lugar de usar las IOT DE CONSULTA DE **\_ \_ \_ BACKLOG \_** IDEAL SEND DE SIO IDEAL y [**SIO IDEAL \_ SEND \_ \_ BACKLOG \_ QUERY**](sio-ideal-send-backlog-query.md) directamente.

La función contenedora insertda para **SIO \_ IDEAL SEND \_ \_ BACKLOG \_ CHANGE** IOCTL es la **función idealsendbacklognotify.**

La función contenedora insertda para [**SIO \_ IDEAL SEND \_ \_ BACKLOG \_ QUERY**](sio-ideal-send-backlog-query.md) IOCTL es la **función idealsendbacklogquery.**

## <a name="see-also"></a>Vea también

[**SIO_IDEAL_SEND_BACKLOG_QUERY**](sio-ideal-send-backlog-query.md)

[**Zócalo**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
