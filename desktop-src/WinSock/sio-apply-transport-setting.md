---
description: El código de control aplica una o más configuraciones de transporte a un socket.
ms.assetid: FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715
title: Código de control de SIO_APPLY_TRANSPORT_SETTING
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: e167a87e70dc3c6c44a263308beb333176a3d525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720482"
---
# <a name="sio_apply_transport_setting-control-code"></a>Código de control de SIO_APPLY_TRANSPORT_SETTING

## <a name="description"></a>Descripción

El código de control de **\_ \_ \_ configuración de transporte SiO** aplica una o más configuraciones de transporte a un socket.

Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
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
Use **la \_ \_ \_ opción de transporte SiO Apply** para esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada.
Este parámetro contiene un puntero a una estructura en la que el primer miembro de la estructura es una estructura [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) que determina qué configuración de transporte se aplica.

### <a name="cbinbuffer"></a>cbInBuffer

Tamaño, en bytes, del búfer de entrada.
Este parámetro depende de la configuración de transporte que se aplica.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntero al búfer de salida.
Este parámetro depende de la configuración de transporte que se aplica.

### <a name="cboutbuffer"></a>cbOutBuffer

Tamaño, en bytes, del búfer de salida.

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
| **\_operación WSA \_ anulada** | La operación de e/s se ha anulado debido a una salida de subproceso o una solicitud de aplicación. Se devuelve este error si se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando de ioctl de **\_ volcado de SiO** . |
| **WSAEFAULT** | El sistema detectó una dirección de puntero no válida al intentar usar un argumento de puntero en una llamada. Este error se devuelve cuando el parámetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | Se está ejecutando una operación de bloqueo actualmente. Se devuelve este error si la función se invoca cuando hay una devolución de llamada en curso. |
| **WSAEINTR** | Una operación de bloqueo fue interrumpida por una llamada a [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall). Se devuelve este error si se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | Se proporcionó un argumento no válido. Se devuelve este error si el parámetro *dwIoControlCode* no es un comando válido o si un parámetro de entrada especificado no es aceptable, o si el comando no es aplicable al tipo de socket especificado. |
| **WSAENETDOWN** | Una operación de socket encontró una red inactiva. Se devuelve este error si se ha producido un error en el subsistema de red. |
| **WSAENOTSOCK** | Se intentó realizar una operación en algo que no es un socket. Se devuelve este error si el *descriptor* no es un socket. |
| **WSAEOPNOTSUPP** | La operación intentada no se admite para el tipo de objeto al que se hace referencia. Se devuelve este error si no se admite el comando IOCTL especificado. Este error también se devuelve si el proveedor de transporte no admite la configuración de transporte de la **\_ \_ \_ opción SiO Apply** . Este error también se devuelve cuando se realiza un intento de usar la configuración de transporte de la **\_ \_ \_ opción SiO** en un socket distinto de UDP o TCP. |

## <a name="remarks"></a>Observaciones

El ioctl de **\_ \_ \_ configuración de transporte SiO** es compatible con windows 8, Windows Server 2012 y versiones posteriores del sistema operativo.

La **\_ configuración de \_ transporte \_ de SiO aplicar** es un ioctl genérico que se usa para aplicar la configuración de transporte al socket.
La configuración de transporte que se está aplicando se basa en el [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) pasado en el parámetro *lpvInBuffer* .

A partir de Windows 8 y Windows Server 2012, el sistema define la capacidad de **REAL_TIME_NOTIFICATION_CAPABILITY** en un socket TCP.
A partir de Windows 10 y Windows Server 2016, también se define el **\_ \_ contexto Associate NAMERES** .
Para obtener más información, vea [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) y [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).

Si el [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) pasado en el parámetro lpvInBuffer tiene el miembro GUID establecido en **\_ funcionalidad de \_ notificación \_ en tiempo real**, se trata de una solicitud para aplicar la configuración de notificación en tiempo real para el socket TCP que se usa con la [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) para recibir notificaciones de red en segundo plano en una aplicación de la tienda Windows.
El parámetro *lpvInBuffer* debe apuntar a una estructura **REAL_TIME_NOTIFICATION_SETTING_INPUT** .
El parámetro *lpvOutBuffer* no se usa para esta operación.
Esta configuración de transporte solo se aplica a los Sockets TCP.
Esta configuración de transporte proporciona una manera para que WinInet o servicios de red similares marquen un socket TCP determinado como [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) habilitado.
Windows marcará el socket TCP correspondiente y configurará la configuración de hardware y software adecuada cuando se llame a esta opción.
Una aplicación de la tienda Windows no llamará a este IOCTL directamente.

## <a name="see-also"></a>Vea también

[**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[tomacorriente](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SIO_QUERY_TRANSPORT_SETTING**](sio-query-transport-setting.md)

[**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
