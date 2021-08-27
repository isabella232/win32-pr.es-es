---
description: Código de control que configura los parámetros de tiempo de espera de retransmisión inicial (RTO) en un socket.
ms.assetid: F5ABAE57-E0F0-4AEB-825C-B53AEE8210E7
title: SIO_TCP_INITIAL_RTO código de control
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 63ebbfd0d8d56c03d62c7bba417d69e3ac1a576abfc8c72ac489117a7d8b74c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097485"
---
# <a name="sio_tcp_initial_rto-control-code"></a>SIO_TCP_INITIAL_RTO código de control

## <a name="description"></a>Descripción

El **SIO_TCP_INITIAL_RTO** de control configura los parámetros de tiempo de espera de retransmisión inicial (RTO) en un socket.

Para realizar esta operación, llame a la [**función WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
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
Use **SIO_TCP_INITIAL_RTO** para esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada.
Este parámetro contiene un puntero al [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) asociado al socket.

### <a name="cbinbuffer"></a>cbInBuffer

Tamaño, en bytes, del búfer de entrada.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntero al búfer de salida.
Este parámetro no se usa para esta operación.

### <a name="cboutbuffer"></a>cbOutBuffer

Tamaño, en bytes, del búfer de salida.
Este parámetro debe establecerse en cero.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.

Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *lpcbBytesReturned* apunta a un **valor DWORD** de cero.

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

Puntero a una [**estructura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada posterior a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).
El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc.**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)

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
| **WSA \_ IO \_ PENDING** | La operación de E/S superpuesta está en curso. Este valor se devuelve si una operación superpuesta se inició correctamente y la finalización se indicará más adelante. |
| **OPERACIÓN WSA \_ \_ ANULADA** | La operación de E/S se ha anulado debido a una salida de subproceso o a una solicitud de aplicación. Este error se devuelve si se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **SIO \_ FLUSH** IOCTL. |
| **WSAEACCES** | Se intentó acceder a un socket de una manera prohibida por sus permisos de acceso. Este error se devuelve en varias condiciones que incluyen lo siguiente: el usuario carece de los privilegios administrativos necesarios en el equipo local o la aplicación no se ejecuta en un shell mejorado como administrador integrado ( `RunAs administrator` ). |
| **WSAEFAULT** | El sistema detectó una dirección de puntero no válida al intentar usar un argumento de puntero en una llamada. Este error se devuelve del parámetro *lpvInBuffer*, *lpvoutBuffer,* *lpcbBytesReturned,* *lpOverlapped* o *lpCompletionRoutine* no está totalmente contenido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | Se está ejecutando una operación de bloqueo actualmente. Este error se devuelve si se invoca la función cuando hay una devolución de llamada en curso. |
| **WSAEINTR** | Una operación de bloqueo se interrumpió mediante una llamada a *WSACancelBlockingCall*. Este error se devuelve si se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | Se proporcionó un argumento no válido. Este error se devuelve si el parámetro *dwIoControlCode* no es un comando válido, un parámetro de entrada especificado no es aceptable o el comando no es aplicable al tipo de socket especificado. |
| **WSAENETDOWN** | Una operación de socket encontró una red inactiva. Este error se devuelve si se ha producido un error en el subsistema de red. |
| **WSAENOTSOCK** | Se intentó realizar una operación en algo que no es un socket. Este error se devuelve si el descriptor s no es un socket. |
| **WSAEOPNOTSUPP** | La operación intentada no se admite para el tipo de objeto al que se hace referencia. Este error se devuelve si no se admite el comando IOCTL especificado. Este error también se devuelve si **el proveedor SIO_TCP_INITIAL_RTO** ioctl no es compatible con la E/S por parte del proveedor de transporte. |

## <a name="remarks"></a>Comentarios

Una aplicación puede usar **el** SIO_TCP_INITIAL_RTO IOCTL para controlar las características de retransmisión inicial (SYN/SYN+ACK) de un socket TCP si es necesario.
Una aplicación, si usa esta opción, debe proporcionar los valores adecuados antes de iniciar un intento de conexión TCP en el socket.

La [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) IOCTL permite a una aplicación configurar el tiempo de espera de retransmisión inicial (SYN) (RTO) utilizado por el socket.

Un puntero a una [**estructura TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) pasada en el parámetro *lpvInBuffer* permite a una aplicación configurar el tiempo de ida y vuelta inicial (RTT) utilizado para calcular el tiempo de espera de retransmisión.
La aplicación también puede configurar el número de retransmisiones que se intentarán antes de que se produce un error en el intento de conexión.

## <a name="see-also"></a>Vea también

[Zócalo](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
