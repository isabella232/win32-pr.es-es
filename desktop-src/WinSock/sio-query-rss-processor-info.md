---
description: El código de control consulta la asociación entre un socket y un núcleo de procesador RSS y un nodo NUMA.
ms.assetid: DAF18C92-B479-474F-B438-0746CBA20653
title: SIO_QUERY_RSS_PROCESSOR_INFO código de control
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 6c0f690555beb19f7d5d79a81e2cc900194f731c3acacb075ae12dc304debffd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740387"
---
# <a name="sio_query_rss_processor_info-control-code"></a>SIO_QUERY_RSS_PROCESSOR_INFO código de control

## <a name="description"></a>Descripción

El código de control **SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO** consulta la asociación entre un socket y un núcleo de procesador RSS y un nodo NUMA.

Para realizar esta operación, llame a la [**función WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
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
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
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

Descriptor que identifica un socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Código de control de la operación.
Use **SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO** para esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada.
Este parámetro no se usa para esta operación.

### <a name="cbinbuffer"></a>cbInBuffer

Tamaño, en bytes, del búfer de entrada.
Este parámetro no se usa para esta operación.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntero al búfer de salida.
Este parámetro debe apuntar a una estructura [**SOCKET \_ PROCESSOR \_ AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) si los parámetros *lpOverlapped* y *lpCompletionRoutine* son **NULL.**

### <a name="cboutbuffer"></a>cbOutBuffer

Tamaño, en bytes, del búfer de salida.
Este parámetro debe ser al menos el tamaño de una estructura [**AFFINITY \_ de SOCKET PROCESSOR. \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.

Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *lpcbBytesReturned* apunta a un *valor DWORD* de cero.

Si *lpOverlapped* es **NULL,** el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve en una llamada correcta no puede ser cero.

Si el *parámetro lpOverlapped* no es **NULL** para sockets superpuestos, se iniciarán las operaciones que no se pueden completar inmediatamente y la finalización se indicará más adelante.
El **valor DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que el tamaño de los datos almacenados no se puede determinar hasta que se complete la operación superpuesta.
El estado de finalización final se puede recuperar cuando se señala el método de finalización adecuado cuando se ha completado la operación.

### <a name="lpvoverlapped"></a>lpvOverlapped

Puntero a una [**estructura WSAOVERLAPPED.**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

Si se *crearon sockets* sin el atributo superpuesto, se omite el parámetro *lpOverlapped.*

Si *s* se abrió con el atributo superpuesto y el parámetro *lpOverlapped* no es **NULL,** la operación se realiza como una operación superpuesta (asincrónica).
En este caso, *el parámetro lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.

Para las operaciones superpuestas, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelve inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.
De lo contrario, la función no devuelve hasta que se ha completado la operación o se produce un error.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Puntero a la rutina de finalización llamada cuando se ha completado la operación (omitida para sockets no superpuestos).

### <a name="lpthreadid"></a>lpThreadId

Puntero a una [**estructura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada posterior a [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).
El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)

**Nota**  Este parámetro solo se aplica a la **función WSPIoctl.**

### <a name="lperrno"></a>lpErrno

Puntero al código de error.

**Nota**  Este parámetro solo se aplica a la **función WSPIoctl.**

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, la [**función WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.

Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve **SOCKET \_ ERROR**.
Para obtener información de error extendida, llame [**a WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Código de error | Significado |
|------------|---------|
| **BÚFER INSUFICIENTE \_ \_ DE ERROR** | El área de datos pasada a una llamada del sistema es demasiado pequeña. Este error se devuelve si el búfer al que apunta el parámetro *lpvOutBuffer* con un tamaño de búfer pasado en el *parámetro cbOutBuffer* es demasiado pequeño. El tamaño de búfer necesario se devolverá en el *parámetro lpcbBytesReturned.* Este error se devuelve si el *parámetro cbOutBuffer* es menor que el tamaño de una estructura [**AFFINITY de SOCKET \_ PROCESSOR. \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) |
| **WSA \_ IO \_ PENDING** | Se inició correctamente una operación superpuesta y la finalización se indicará más adelante. |
| **OPERACIÓN WSA \_ \_ ANULADA** | Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **IOCTL \_ FLUSH de SIO.** |
| **WSAEFAULT** | El *parámetro lpvInBuffer*, *lpvoutBuffer,* *lpcbBytesReturned,* *lpOverlapped* o *lpCompletionRoutine* no está totalmente contenido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | La función se invoca cuando hay una devolución de llamada en curso. |
| **WSAEINTR** | Se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | El *parámetro dwIoControlCode* no es un comando válido, un parámetro de entrada especificado no es aceptable o el comando no es aplicable al tipo de socket especificado. Este error se devuelve si el *parámetro cbOutBuffer* es menor que el tamaño de una estructura [**AFFINITY de SOCKET \_ PROCESSOR. \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)
| **WSAENETDOWN** | Error en el subsistema de red. |
| **WSAENOPROTOOPT** | La opción de socket no se admite en el protocolo especificado. |
| **WSAENOTCONN** | Los *sockets no* están conectados. |
| **WSAENOTSOCK** | El descriptor *s no* es un socket. |
| **WSAEOPNOTSUPP** | No se admite el comando IOCTL especificado. Este error se devuelve si el proveedor de transporte no admite **SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO** IOCTL. |

## <a name="remarks"></a>Comentarios

**SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO** IOCTL se admite en Windows 8, Windows Server 2012 y versiones posteriores del sistema operativo.

**SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO** IOCTL se usa para determinar la asociación entre un socket y un núcleo de procesador RSS y un nodo NUMA.
Esta IOCTL devuelve una estructura [**SOCKET \_ PROCESSOR \_ AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) que contiene el [**NÚMERO DE \_ PROCESADOR**](/windows/desktop/api/winnt/ns-winnt-processor_number) y el identificador de nodo NUMA.
La estructura [**PROCESSOR \_ NUMBER devuelta**](/windows/desktop/api/winnt/ns-winnt-processor_number) contiene un número de grupo y un número de procesador relativo dentro del grupo.

Si el socket es un socket UDP, el socket debe estar conectado para que LA IOCTL DE INFORMACIÓN DEL PROCESADOR RSS DE CONSULTA DE SIO funcione correctamente. **\_ \_ \_ \_**

## <a name="see-also"></a>Vea también

[**PROCESSOR_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number)

[**Zócalo**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SOCKET_PROCESSOR_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
