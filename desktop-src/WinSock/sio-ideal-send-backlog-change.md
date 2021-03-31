---
description: El código de control notifica una aplicación cuando cambia el valor de trabajo pendiente de envío ideal para la conexión.
ms.assetid: 337883a5-7ceb-40d3-b318-b86dd488b94a
title: Código de control de SIO_IDEAL_SEND_BACKLOG_CHANGE
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 4eb07efecd39774c60d47cbcf7245c5831760e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812452"
---
# <a name="sio_ideal_send_backlog_change-control-code"></a>Código de control de SIO_IDEAL_SEND_BACKLOG_CHANGE

## <a name="description"></a>Descripción

El código de control de **\_ \_ \_ \_ cambio de trabajo pendiente de envío adecuado de SiO** notifica una aplicación cuando cambia el valor de trabajo pendiente de envío (ISB) ideal para la conexión.

Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

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

Un descriptor que identifica un socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Código de control de la operación.
Use **el \_ \_ cambio de \_ trabajo \_ acumulado de envío ideal** para esta operación.

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
Este parámetro devuelve un valor **DWORD** de cero para esta operación, ya que no hay ninguna salida.

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

Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).
El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) .

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
| **\_e/s de WSA \_ pendientes** | Se inició correctamente una operación superpuesta y la finalización se indicará en un momento posterior. |
| **\_operación WSA \_ anulada** | Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **SiO \_ Flush** ioctl. |
| **WSAEFAULT** | El parámetro *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | La función se invoca cuando una devolución de llamada está en curso. |
| **WSAEINTR** | Se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | El parámetro *dwIoControlCode* no es un comando válido o un parámetro de entrada especificado no es aceptable, o bien el comando no es aplicable al tipo de socket especificado. Se devuelve este error si el parámetro *cbOutBuffer* no es cero. |
| **WSAENETDOWN** | Error en el subsistema de red. |
| **WSAENOPROTOOPT** | No se admite la opción socket en el protocolo especificado. |
| **WSAENOTCONN** | El socket *s* no está conectado. |
| **WSAENOTSOCK** | El descriptor *s* no es un socket. |
| **WSAEOPNOTSUPP** | No se admite el comando IOCTL especificado. Se devuelve este error si el proveedor de transporte no admite el **\_ cambio de \_ trabajo pendiente de envío de \_ \_ intercambio ideal** . Este error también se devuelve cuando un intento de usar el **\_ cambio de \_ \_ trabajo pendiente \_ de envío de la opción SiO ideal** se realiza en un socket de datagrama. |

## <a name="remarks"></a>Observaciones

El ioctl de **\_ \_ \_ \_ intercambio de trabajo pendiente de la opción SiO** es compatible con Windows Server 2008, Windows Vista con Service Pack 1 (SP1) y versiones posteriores del sistema operativo.

Al enviar datos a través de una conexión TCP mediante Windows Sockets, es importante mantener una cantidad suficiente de datos pendientes (enviados pero no confirmados todavía) en TCP para lograr el máximo rendimiento.
El valor ideal para la cantidad de datos pendientes para lograr el mejor rendimiento para la conexión TCP se denomina el tamaño de trabajo pendiente de envío (ISB) ideal.
El valor de ISB es una función del producto de retraso de ancho de banda de la conexión TCP y la ventana de recepción anunciada del receptor (y, en parte, de la cantidad de congestión de la red).

El valor de ISB por conexión está disponible en la implementación del protocolo TCP en Windows Server 2008, Windows Vista con SP1 y versiones posteriores del sistema operativo.
Una aplicación puede usar el ioctl de **\_ \_ \_ \_ cambio de trabajo pendiente de envío ideal de SiO** para recibir una notificación cuando el valor de ISB Cambie dinámicamente para una conexión.

En Windows Server 2008, Windows Vista con SP1 y versiones posteriores del sistema operativo, se admiten los ioctl de **\_ \_ \_ \_ cambio de trabajo acumulado de envío** y [**SiO \_ idóneos \_ \_ \_**](sio-ideal-send-backlog-query.md) en los sockets orientados a flujos que se encuentran en estado conectado.

En teoría, el intervalo para el valor de ISB para una conexión TCP puede variar de 0 a un máximo de 16 megabytes.

Consulte la página de referencia de ioctl de la consulta de registro de carga de [**\_ \_ \_ trabajo \_ ideal**](sio-ideal-send-backlog-query.md) para el uso típico del mecanismo de ISB con el fin de lograr un mejor rendimiento de las conexiones de productos con retraso de ancho de banda alto.

El **\_ \_ \_ \_ intercambio de trabajo acumulado de envío ideal de SiO** solo se permite en un socket de secuencia que está en estado conectado.
De lo contrario, se producirá un error en la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con **WSAENOTCONN**.

El **\_ intercambio de \_ \_ trabajo pendiente \_ de envío ideal de SiO** no usa ningún búfer de entrada ni de salida, pends ni se bloquea hasta que se produce un cambio de ISB en la conexión subyacente.
Cuando se completa este IOCTL, una aplicación Winsock puede usar la [**\_ consulta de \_ \_ trabajo pendiente \_ de envío de la opción SiO ideal**](sio-ideal-send-backlog-query.md) para recuperar el nuevo valor de ISB en la conexión.

El **\_ intercambio de \_ \_ trabajo pendiente \_ de envío ideal de SiO** no admite el modo de no bloqueo.
Una aplicación puede emitir este IOCTL en un socket que no sea de bloqueo, pero el IOCTL simplemente se bloqueará o permanecerá hasta que cambie el valor de ISB.

Si los parámetros *lpOverlapped* y *lpCompletionRoutine* son NULL, el socket de esta función se tratará como un socket no superpuesto.
En el caso de un socket no superpuesto, se omiten los parámetros *lpOverlapped* y *lpCompletionRoutine* , salvo que la función puede bloquearse si socket *s* está en modo de bloqueo.
Si socket *s* está en modo de no bloqueo, esta función seguirá bloqueando, ya que este ioctl determinado no admite el modo de no bloqueo.

En el caso de los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.

Cualquier IOCTL puede bloquearse indefinidamente, dependiendo de la implementación del proveedor de servicios.
Si la aplicación no puede tolerar el bloqueo en una llamada de función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** , se aconsejará la e/s superpuesta para los IOCTL que es especialmente probable que se bloqueen.

El **\_ intercambio de \_ \_ trabajo pendiente \_ de envío ideal de SiO** proporciona una notificación y se espera que se bloquee o quede pendiente hasta que cambie el valor de ISB.
Por lo tanto, normalmente se llamaría de forma asincrónica con el parámetro *lpOverlapped* establecido en una estructura WSAOVERLAPPED válida.

Se puede producir un **error en la** **\_ operación \_** de **\_ \_ \_ \_ intercambio de trabajo pendiente de envío de la opción SiO** en los casos siguientes:

* La conexión TCP está correctamente desconectada en la dirección de envío. Esto puede ocurrir como resultado de una llamada a la función Shutdown con el parámetro how establecido en **SD \_ send**, una llamada a la función **DisconnectEx** o una llamada a la función **TransmitFile** o **TransmitPackets** con el parámetro *dwFlags* establecido en **TF \_ Disconnect** o **TF \_ reuse**.
* La conexión TCP se ha restablecido o anulado.
* La aplicación emite un **\_ intercambio de \_ \_ trabajo pendiente \_ de envío de SiO ideal** cuando ya hay una solicitud de notificación pendiente. Solo se permite la solicitud de **\_ \_ \_ \_ cambio de trabajo pendiente de envío** en una sola vez 1 1 a la vez.
* El administrador de e/s cancela la solicitud.
* El socket está cerrado.

Dos funciones de contenedor en línea para estos ioctl se definen en el archivo de encabezado *Ws2tcpip. h* .
Se recomienda usar estas funciones insertadas en lugar de usar el **\_ \_ \_ \_ cambio de trabajo pendiente de envío** y [**SiO ideales para la \_ \_ \_ \_ consulta de trabajo pendiente de envío ideal**](sio-ideal-send-backlog-query.md) directamente.

La función de contenedor en línea para **el \_ \_ cambio de \_ trabajo \_ pendiente de envío de SiO ideal** es la función **idealsendbacklognotify** .

La función de contenedor en línea para [**la \_ opción \_ de \_ \_ búsqueda de trabajo pendiente de envío ideal de SiO**](sio-ideal-send-backlog-query.md) es la función **idealsendbacklogquery** .

## <a name="see-also"></a>Vea también

[**SIO_IDEAL_SEND_BACKLOG_QUERY**](sio-ideal-send-backlog-query.md)

[**tomacorriente**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
