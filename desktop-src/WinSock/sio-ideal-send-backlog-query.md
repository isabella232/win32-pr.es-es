---
description: El código de control recupera el valor de trabajo pendiente de envío ideal para la conexión subyacente.
ms.assetid: 03fe964b-26f7-4af7-83bf-62cc877d01a8
title: Código de control de SIO_IDEAL_SEND_BACKLOG_QUERY
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 440e42477a8939a62eeb84b800c0fd8feead5aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720648"
---
# <a name="sio_ideal_send_backlog_query-control-code"></a>Código de control de SIO_IDEAL_SEND_BACKLOG_QUERY

## <a name="description"></a>Descripción

El código de control de **\_ \_ \_ \_ consulta de trabajo pendiente de envío ideal de SiO** recupera el valor de trabajo pendiente de envío (ISB) ideal para la conexión subyacente.

Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
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
Use **la \_ \_ consulta de \_ trabajo \_ pendiente de envío de SiO ideal** para esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada.
Este parámetro no se usa para esta operación.

### <a name="cbinbuffer"></a>cbInBuffer

Tamaño, en bytes, del búfer de entrada.
Este parámetro no se usa para esta operación.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntero al búfer de salida.
Este parámetro debe apuntar a un tipo de datos **ULong** si los parámetros *lpOverlapped* y *lpCompletionRoutine* son **null**.

### <a name="cboutbuffer"></a>cbOutBuffer

Tamaño, en bytes, del búfer de salida.
Este parámetro debe ser al menos el tamaño de un tipo de datos **ULong** .

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
| **WSAEFAULT** | Los parámetros *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no están totalmente contenidos en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | La función se invoca cuando una devolución de llamada está en curso. |
| **WSAEINTR** | Se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | El parámetro *dwIoControlCode* no es un comando válido o un parámetro de entrada especificado no es aceptable, o bien el comando no es aplicable al tipo de socket especificado. Se devuelve este error si el parámetro *cbOutBuffer* es menor que el tamaño de un tipo de datos **ULong** .
| **WSAENETDOWN** | Error en el subsistema de red. |
| **WSAENOPROTOOPT** | No se admite la opción socket en el protocolo especificado. |
| **WSAENOTCONN** | El socket s no está conectado. |
| **WSAENOTSOCK** | El descriptor *s* no es un socket. |
| **WSAEOPNOTSUPP** | No se admite el comando IOCTL especificado. Este error se devuelve si el proveedor de transporte no admite el ioctl de **\_ \_ \_ \_ consulta de trabajo pendiente de envío ideal de SiO** . Este error también se devuelve cuando se realiza un intento de usar el ioctl de **\_ \_ \_ \_ consulta de trabajo pendiente de envío de SiO ideal** en un socket de datagramas. |

## <a name="remarks"></a>Observaciones

El ioctl de **\_ \_ \_ \_ consulta de trabajo pendiente de envío ideal de SiO** es compatible con Windows Server 2008, Windows Vista con Service Pack 1 (SP1) y versiones posteriores del sistema operativo.

Al enviar datos a través de una conexión TCP mediante Windows Sockets, es importante mantener una cantidad suficiente de datos pendientes (enviados pero no confirmados todavía) en TCP para lograr el máximo rendimiento.
El valor ideal para la cantidad de datos pendientes para lograr el mejor rendimiento para la conexión TCP se denomina el tamaño de trabajo pendiente de envío (ISB) ideal.
El valor de ISB es una función del producto de retraso de ancho de banda de la conexión TCP y la ventana de recepción anunciada del receptor (y, en parte, de la cantidad de congestión de la red).

El valor de ISB por conexión está disponible en la implementación del protocolo TCP en Windows Server 2008, Windows Vista con SP1 y versiones posteriores del sistema operativo.
Una aplicación puede usar el ioctl de **\_ \_ \_ \_ consulta de trabajo pendiente de envío ideal de SiO** para recibir una notificación cuando el valor de ISB Cambie dinámicamente para una conexión.

En Windows Server 2008, Windows Vista con SP1 y versiones posteriores del sistema operativo, se admiten los ioctl de [**\_ \_ \_ \_ cambio de trabajo acumulado de envío**](sio-ideal-send-backlog-change.md) y **SiO \_ idóneos \_ \_ \_** en los sockets orientados a flujos que se encuentran en estado conectado.

En teoría, el intervalo para el valor de ISB para una conexión TCP puede variar de 0 a un máximo de 16 megabytes.

El uso típico de la opción de búsqueda de trabajo pendiente de envío ideal y SiO de la **\_ \_ \_ \_ consulta de trabajo pendiente de envío ideal** se basa en el método de envío que usan las aplicaciones. [**\_ \_ \_ \_**](sio-ideal-send-backlog-change.md)
Se describen dos casos comunes.

Las aplicaciones que realizan una solicitud de envío o de bloqueo sin bloqueo a la vez suelen basarse en el almacenamiento en búfer interno de Winsock para lograr un rendimiento aceptable.
El límite del búfer de envío para una conexión determinada se controla mediante la opción de socket **so \_ SNDBUF** .
En el caso del método de envío y bloqueo sin bloqueo, el límite del búfer de envío determina la cantidad de datos que se mantienen pendientes en TCP.
Si el valor de ISB para la conexión es mayor que el límite del búfer de envío, el rendimiento conseguido en la conexión no será óptimo.
Con el fin de lograr un mejor rendimiento, las aplicaciones pueden establecer el límite del búfer de envío según el resultado de la consulta de ISB a medida que se producen notificaciones de cambios de ISB en la conexión.

En el caso de las aplicaciones que usan el método de envío superpuesto con varias solicitudes de envío pendientes, la cantidad de datos que se mantienen pendientes en TCP viene determinada por el límite de búfer de envío en Winsock y la cantidad total de datos contenidos en las solicitudes de envío superpuestas pendientes.
En este caso, las aplicaciones deben usar el valor de ISB para determinar cuántas solicitudes de envío pendientes deben conservar y cuál debe ser el tamaño de los datos para cada solicitud de envío.
Idealmente, la aplicación debe intentar mantener la siguiente ecuación satisfactoria:

`ISB value == send buffer limit + (number of simultaneous overlapped send requests * data length per send request)`

Tenga en cuenta que el uso de los ioctl de ISB a través de Sockets TCP en el modo anterior puede provocar un aumento del uso de memoria en Exchange para aumentar el rendimiento en las conexiones con un producto de retraso de ancho de banda alto.
La implementación de TCP en Windows limitará los valores de ISB según sea necesario en función del uso global de la memoria del sistema.

El ioctl de **\_ \_ \_ \_ consulta de trabajo pendiente de envío ideal de SiO** solo se permite en un socket de secuencia que se encuentra en estado conectado.
De lo contrario, se producirá un error en la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con **WSAENOTCONN**.

Cualquier IOCTL puede bloquearse indefinidamente, dependiendo de la implementación del proveedor de servicios.
Si la aplicación no puede tolerar el bloqueo en una llamada de función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** , se aconsejará la e/s superpuesta para los IOCTL que es especialmente probable que se bloqueen.

No es probable que el ioctl de **\_ \_ \_ \_ consulta de trabajo pendiente de envío perfecto** no se bloquee, por lo que normalmente se llama sincrónicamente con los parámetros *lpOverlapped* y *lpCompletionRoutine* establecidos en **null**.

Se puede producir un error en el ioctl de **\_ \_ \_ \_ consulta de trabajo pendiente de envío de SiO ideal** con la operación **WSAEINTR** o **WSA \_ \_ anulada** en los siguientes casos:

La conexión TCP está correctamente desconectada en la dirección de envío.
Esto puede ocurrir como resultado de una llamada a la función Shutdown con el parámetro how establecido en **SD \_ send**, una llamada a la función **DisconnectEx** o una llamada a la función **TransmitFile** o **TransmitPackets** con el parámetro *dwFlags* establecido en **TF \_ Disconnect** o **TF \_ reuse**.
La conexión TCP se ha restablecido o anulado.
El administrador de e/s cancela la solicitud.

Dos funciones de contenedor en línea para estos ioctl se definen en el archivo de encabezado *Ws2tcpip. h* .
Se recomienda usar estas funciones insertadas en lugar de usar el [**\_ \_ \_ \_ cambio de trabajo pendiente de envío**](sio-ideal-send-backlog-change.md) y **SiO ideales para la \_ \_ \_ \_ consulta de trabajo pendiente de envío ideal** directamente.

La función de contenedor en línea para [**el \_ \_ cambio de \_ trabajo \_ pendiente de envío de SiO ideal**](sio-ideal-send-backlog-change.md) es la función **idealsendbacklognotify** .

La función de contenedor en línea para **la \_ opción \_ de \_ \_ búsqueda de trabajo pendiente de envío ideal de SiO** es la función **idealsendbacklogquery** .

El almacenamiento en búfer de envío dinámico para TCP se agregó en Windows 7 y Windows Server 2008 R2.
De forma predeterminada, el almacenamiento en búfer de envío dinámico para TCP está habilitado a menos que una aplicación establezca la opción de socket for **\_ SNDBUF** en el socket de flujo.

El uso de Netsh es el método recomendado para consultar o establecer el almacenamiento en búfer de envío dinámico para TCP.

El valor actual del almacenamiento en búfer de envío dinámico para TCP se puede recuperar con el siguiente comando:

`netsh winsock show autotuning`

El almacenamiento en búfer de envío dinámico para TCP se puede deshabilitar con el siguiente comando:

`netsh winsock set autotuning off`

El almacenamiento en búfer de envío dinámico para TCP se puede habilitar con el siguiente comando:

`netsh winsock set autotuning on`

Aunque no se recomienda, el almacenamiento en búfer de envío dinámico se puede deshabilitar en una aplicación si se establece el valor del Registro siguiente en cero:

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\AFD\Parameters\DynamicSendBufferDisable`

Al cambiar el valor del almacenamiento en búfer de envío dinámico mediante NetSh.exe o cambiar el valor del registro, el equipo debe reiniciarse para que el cambio surta efecto.

Con el almacenamiento en búfer dinámico de envíos en Windows 7 y Windows Server 2008 R2, el uso de los ioctl de **\_ \_ \_ \_ solicitud** de envío de [**\_ \_ \_ trabajo \_**](sio-ideal-send-backlog-change.md) en el trabajo de envío y SiO ideal solo es necesario en circunstancias especiales.

## <a name="see-also"></a>Vea también

[**SIO_IDEAL_SEND_BACKLOG_CHANGE**](sio-ideal-send-backlog-change.md)

[**tomacorriente**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
