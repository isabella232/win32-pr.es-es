---
description: El código de control consulta la configuración de transporte en un socket.
ms.assetid: 3845BE07-A414-4118-96E8-8BEF1DEDB1D3
title: SIO_QUERY_TRANSPORT_SETTING código de control
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 60dca8346d9a4cd11de4d53dd87611e79e01c45dba555f45907721fe529b352a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097505"
---
# <a name="sio_query_transport_setting-control-code"></a>SIO_QUERY_TRANSPORT_SETTING código de control

## <a name="description"></a>Descripción

El código de control **\_ SIO QUERY \_ TRANSPORT \_ SETTING** consulta la configuración de transporte en un socket.

Para realizar esta operación, llame a la [**función WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
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

Descriptor que identifica un socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Código de control de la operación.
Use **SIO \_ QUERY TRANSPORT \_ SETTING \_ para** esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada.
Este parámetro contiene un puntero a una estructura donde [](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) el primer miembro de la estructura es una estructura TRANSPORT_SETTING_ID que determina qué configuración de transporte se consulta.

### <a name="cbinbuffer"></a>cbInBuffer

Tamaño, en bytes, del búfer de entrada.
Este parámetro depende de la configuración de transporte que se consulta.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntero al búfer de salida.
Este parámetro depende de la configuración de transporte que se consulta si los parámetros *lpOverlapped* y *lpCompletionRoutine* son **NULL.**

### <a name="cboutbuffer"></a>cbOutBuffer

Tamaño, en bytes, del búfer de salida.

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
| **ERROR \_ BÚFER \_ INSUFICIENTE** | El área de datos pasada a una llamada del sistema es demasiado pequeña. Este error se devuelve si el búfer al que apunta el parámetro *lpvOutBuffer* con un tamaño de búfer pasado en el *parámetro cbOutBuffer* es demasiado pequeño. El tamaño de búfer necesario se devolverá en el *parámetro lpcbBytesReturned.* |
| **WSA \_ IO \_ PENDING** | Se inició correctamente una operación superpuesta y la finalización se indicará más adelante. |
| **WSA \_ OPERATION \_ ABORTED** | Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **IOCTL DE SIO \_ FLUSH.** |
| **WSAEFAULT** | El *parámetro lpvOutBuffer*, *lpcbBytesReturned,* *lpOverlapped* o *lpCompletionRoutine* no está totalmente contenido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | La función se invoca cuando hay una devolución de llamada en curso. |
| **WSAEINTR** | Se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | El *parámetro dwIoControlCode* no es un comando válido, o un parámetro de entrada especificado no es aceptable o el comando no es aplicable al tipo de socket especificado. |
| **WSAENETDOWN** | Error en el subsistema de red. |
| **WSAENOPROTOOPT** | La opción socket no se admite en el protocolo especificado. |
| **WSAENOTCONN** | Los sockets no están conectados. |
| **WSAENOTSOCK** | El descriptor s no es un socket. |
| **WSAEOPNOTSUPP** | No se admite el comando IOCTL especificado. Este error se devuelve si el proveedor de transporte no admite **SIO \_ QUERY TRANSPORT \_ \_ SETTING** IOCTL. |

## <a name="remarks"></a>Comentarios

**SIO \_ QUERY TRANSPORT \_ \_ SETTING** IOCTL se admite en Windows 8, Windows Server 2012 y versiones posteriores del sistema operativo.

**SIO \_ QUERY \_ TRANSPORT \_ SETTING** IOCTL es una IOCTL genérica que se usa para consultar la configuración de transporte en un socket.
La configuración de transporte que se consulta se basa en el [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) pasado en el *parámetro lpvInBuffer.*

La única configuración de transporte que define actualmente es para la funcionalidad **\_ FUNCIONALIDAD DE NOTIFICACIÓN \_ \_ EN** TIEMPO REAL en un socket TCP.

Si el [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) pasado en el parámetro *lpvInBuffer* tiene el miembro Guid establecido en FUNCIONALIDAD DE NOTIFICACIÓN EN TIEMPO REAL , se trata de una solicitud para consultar la configuración de notificación en tiempo real del socket TCP usado con [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) para recibir notificaciones de red en segundo plano en una aplicación de Windows Store. **\_ \_ \_**
El *parámetro lpvInBuffer* debe apuntar a una [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) estructura.
El *parámetro lpvOutBuffer* debe apuntar a una estructura **DE SALIDA DE CONFIGURACIÓN DE NOTIFICACIÓN \_ \_ \_ \_ EN TIEMPO REAL.**
Esta configuración de transporte solo se aplica a los sockets TCP.
Esta configuración de transporte proporciona una manera de que WinInet o servicios de red similares consulten un socket TCP determinado para determinar el [**estado de ControlChannelTrigger.**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)
Una Windows store no llamará directamente a esta IOCTL.
Si la [**llamada a WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** es correcta, esta IOCTL devuelve una estructura DE SALIDA **DE \_ \_ CONFIGURACIÓN \_ \_** DE NOTIFICACIÓN EN TIEMPO REAL con el estado actual.

**SIO \_ QUERY \_ TRANSPORT \_ SETTING** IOCTL proporciona una manera de que WinInet o servicios de red similares consulten el estado de configuración de transporte de un socket TCP determinado para determinar si [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) está habilitado en el socket.
Una Windows store no llamará directamente a esta IOCTL.

Esta IOCTL solo se aplica a los sockets TCP.

## <a name="see-also"></a>Vea también

[**CONTROL_CHANNEL_TRIGGER_STATUS**](/windows/desktop/api/mstcpip/ne-mstcpip-control_channel_trigger_status)

[**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-real_time_notification_setting_output)

[**SIO_APPLY_TRANSPORT_SETTING**](sio-apply-transport-setting.md)

[Zócalo](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
