---
description: El código de control habilita o deshabilita el valor por conexión de la opción Keep-Alive de TCP, que especifica el tiempo de espera y el intervalo de mantenimiento de conexiones TCP.
ms.assetid: c02e8ad5-bfad-489f-83bf-39b53fd68bde
title: Código de control de SIO_KEEPALIVE_VALS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ea8aabf452436ca2bbd6307366e7fc24f913dbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155865"
---
# <a name="sio_keepalive_vals-control-code"></a>Código de control de SIO_KEEPALIVE_VALS

## <a name="description"></a>Descripción

El código de control **SiO \_ KEEPALIVE \_ vals** habilita o deshabilita el valor por conexión de la opción Keep-Alive de TCP, que especifica el tiempo de espera y el intervalo de mantenimiento de conexiones TCP.

Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

```cpp
int WSAIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
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
Use **SiO \_ KEEPALIVE \_ vals** para esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada.
Este parámetro debe apuntar a una estructura **TCP \_ KeepAlive** .

### <a name="cbinbuffer"></a>cbInBuffer

Tamaño, en bytes, del búfer de entrada.
Este parámetro debe ser igual o mayor que el tamaño de la estructura **TCP \_ KeepAlive** señalada por el parámetro *lpvInBuffer* .

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
|**\_e/s de WSA \_ pendientes** | Se inició correctamente una operación superpuesta y la finalización se indicará en un momento posterior. |
| **\_operación WSA \_ anulada** | Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **SIO_FLUSH ioctl** . |
| **WSAEFAULT** | El parámetro *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | La función se invoca cuando una devolución de llamada está en curso. |
| **WSAEINTR** | Se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | El parámetro *dwIoControlCode* no es un comando válido o un parámetro de entrada especificado no es aceptable, o bien el comando no es aplicable al tipo de socket especificado. |
| **WSAENETDOWN** | Error en el subsistema de red. |
| **WSAENOPROTOOPT** | No se admite la opción socket en el protocolo especificado. Este error se devuelve para un socket de datagrama. |
| **WSAENOTSOCK** | El descriptor s no es un socket. |
| **WSAEOPNOTSUPP** | No se admite el comando IOCTL especificado. Este error se devuelve si el proveedor de transporte no admite el ioctl **SiO \_ KEEPALIVE \_ vals** . |

## <a name="remarks"></a>Observaciones

El ioctl de **\_ \_ vals KEEPALIVE** es compatible con Windows 2000 y versiones posteriores del sistema operativo.

El código de control **SiO \_ KEEPALIVE \_ vals** habilita o deshabilita el valor por conexión de la opción Keep-Alive de TCP, que especifica el tiempo de espera de mantenimiento de conexión TCP y el intervalo utilizado para los paquetes Keep-Alive de TCP.
Para obtener más información acerca de la opción Keep-Alive, consulte la sección 4.2.3.6 sobre los requisitos de los hosts de Internet: las capas de comunicación especificadas en RFC 1122 están disponibles en el [sitio web de IETF](https://www.ietf.org/rfc/rfc1122.txt).
(Este recurso solo está disponible en inglés).

El parámetro *lpvInBuffer* debe apuntar a una estructura **TCP \_ KeepAlive** definida en el archivo de encabezado *Mstcpip. h* .
Esta estructura se define de la siguiente manera:

```cpp
/* Argument structure for SIO_KEEPALIVE_VALS */
struct tcp_keepalive {
    u_long  onoff;
    u_long  keepalivetime;
    u_long  keepaliveinterval;
};
```

El valor especificado en el miembro **OnOff** determina si TCP Keep-Alive está habilitado o deshabilitado.
Si el miembro **OnOff** se establece en un valor distinto de cero, se habilita TCP Keep-Alive y se usan los demás miembros de la estructura.
El miembro **KeepAliveTime** especifica el tiempo de espera, en milisegundos, sin actividad hasta que se envía el primer paquete Keep-Alive.
El miembro **KeepAliveInterval** especifica el intervalo, en milisegundos, entre el momento en que se envían los paquetes Keep-Alive sucesivos Si no se recibe ninguna confirmación.

La opción [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) , que es una de las [**Opciones de socket de SOL_SOCKET**](/windows/desktop/winsock/sol-socket-socket-options), también puede usarse para habilitar o deshabilitar TCP Keep-Alive en una conexión, así como para consultar el estado actual de esta opción.
Para consultar si TCP Keep-Alive está habilitado en un socket, se puede llamar a la función getsockopt con la opción [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .
Para habilitar o deshabilitar TCP Keep-Alive, se puede llamar a **la función del método de llamada** con la opción [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .
Si TCP Keep-Alive está habilitado con [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), se usará la configuración predeterminada de TCP para el tiempo de espera de mantenimiento de conexión y el intervalo, a menos que estos valores se hayan cambiado mediante **SiO \_ KEEPALIVE \_ vals**.

El valor predeterminado para todo el sistema del tiempo de espera de mantenimiento de conexión se controla mediante la configuración del registro [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) , que toma un valor en milisegundos. Si no se establece la clave, el tiempo de espera de mantenimiento de conexión predeterminado es de 2 horas.
El valor predeterminado para todo el sistema del intervalo Keep-Alive se controla a través de la configuración del registro [**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) , que toma un valor en milisegundos. Si no se establece la clave, el intervalo de mantenimiento de conexión predeterminado es de 1 segundo.

En Windows Vista y versiones posteriores, el número de sondeos Keep-Alive (retransmisiones de datos) se establece en 10 y no se puede cambiar.

En Windows Server 2003, Windows XP y Windows 2000, la configuración predeterminada para el número de sondeos Keep-Alive es 5.
El número de sondeos Keep-Alive se controla a través de la configuración del registro **TcpMaxDataRetransmissions** y [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) .
El número de sondeos Keep-Alive se establece en el mayor de los dos valores de clave del registro.
Si este número es 0, no se enviarán sondeos Keep-Alive.
Si este número es superior a 255, se ajusta a 255.

## <a name="see-also"></a>Vea también

[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))

[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))

[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))

[tomacorriente](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
