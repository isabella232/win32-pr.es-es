---
description: El código de control configura un socket TCP para una menor latencia y operaciones más rápidas en la interfaz de bucleback.
ms.assetid: 4F7A6454-E3ED-4529-A531-B0640B0767EF
title: SIO_LOOPBACK_FAST_PATH código de control
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8650cd267d321569aca584e7195fb1bdb79c83a33d931e59e8db37521b8933a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740414"
---
# <a name="sio_loopback_fast_path-control-code"></a>SIO_LOOPBACK_FAST_PATH código de control

## <a name="description"></a>Descripción

El código de control **\_ SIO LOOPBACK \_ FAST \_ PATH** configura un socket TCP para una menor latencia y operaciones más rápidas en la interfaz de bucles bucles.

**Importante**  **Sio \_ LOOPBACK \_ FAST \_ PATH** está en desuso y no se recomienda su uso en el código.

Para realizar esta operación, llame a la [**función WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
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
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
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
Use **SIO \_ LOOPBACK \_ FAST \_ PATH** para esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada.
Este parámetro contiene un puntero a un valor booleano que indica si el socket debe configurarse para las operaciones de buclesback rápidos.

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
|**WSA \_ IO \_ PENDING** | La operación de E/S superpuesta está en curso. Este valor se devuelve si una operación superpuesta se inició correctamente y la finalización se indicará más adelante. |
| **OPERACIÓN WSA \_ \_ ANULADA** | La operación de E/S se ha anulado debido a una salida de subproceso o a una solicitud de aplicación. Este error se devuelve si se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **\_ SIO FLUSH IOCTL.** |
| **WSAEACCES** | Se intentó acceder a un socket de una manera prohibida por sus permisos de acceso. Este error se devuelve en varias condiciones para las reservas de puertos persistentes que incluyen lo siguiente: el usuario carece de los privilegios administrativos necesarios en el equipo local o la aplicación no se ejecuta en un shell mejorado como administrador integrado ( `RunAs administrator` ). |
| **WSAEFAULT** | El sistema detectó una dirección de puntero no válida al intentar usar un argumento de puntero en una llamada. Este error se devuelve del parámetro *lpvInBuffer*, *lpvoutBuffer,* *lpcbBytesReturned,* *lpOverlapped* o *lpCompletionRoutine* no está totalmente contenido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | Se está ejecutando una operación de bloqueo actualmente. Este error se devuelve si se invoca la función cuando hay una devolución de llamada en curso. |
| **WSAEINTR** | Una operación de bloqueo se interrumpió mediante una llamada a [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall). Este error se devuelve si se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | Se proporcionó un argumento no válido. Este error se devuelve si el parámetro *dwIoControlCode* no es un comando válido, un parámetro de entrada especificado no es aceptable o el comando no es aplicable al tipo de socket especificado. |
| **WSAENETDOWN** | Una operación de socket encontró una red inactiva. Este error se devuelve si se ha producido un error en el subsistema de red. |
| **WSAENOTSOCK** | Se intentó realizar una operación en algo que no es un socket. Este error se devuelve si el descriptor *s* no es un socket. |
| **WSAEOPNOTSUPP** | La operación intentada no se admite para el tipo de objeto al que se hace referencia. Este error se devuelve si no se admite el comando IOCTL especificado. Este error también se devuelve si el proveedor de transporte no admite FAST **\_ \_ \_ SIO LOOPBACK FAST PATH** IOCTL. |

## <a name="remarks"></a>Comentarios

Una aplicación puede usar **SIO \_ LOOPBACK \_ FAST \_ PATH** IOCTL para reducir la latencia y mejorar el rendimiento de las operaciones de bucleback en un socket TCP.
Esta IOCTL solicita que la pila TCP/IP use una ruta de acceso rápida especial para las operaciones de bucleback en este socket.
EL **BUCLE \_ DE SIO FAST \_ \_ PATH** IOCTL solo se puede usar con sockets TCP.
Esta IOCTL debe usarse en ambos lados de la sesión de bucle recuperación.
La ruta de acceso rápida de bucles de retorno TCP se admite mediante la interfaz de bucleback IPv4 o IPv6.

El socket que planea iniciar la solicitud de conexión debe aplicar esta IOCTL antes de realizar la solicitud de conexión.
Por lo tanto, el socket usado por la función [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx,**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex) [**WSAConnect,**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect) [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist)o [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) para iniciar la conexión debe aplicar esta IOCTL para usar la ruta de acceso rápida para las operaciones de bucles de retorno.

El socket que escucha la solicitud de conexión debe aplicar esta IOCTL antes de aceptar la conexión.
Por lo tanto, el socket utilizado por la función de escucha debe aplicar esta IOCTL para que todos los sockets aceptados usen la ruta de acceso rápida para el bucle de retorno.
Los sockets devueltos por la función de escucha y pasados a la función [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex)o [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) se marcarán para usar la ruta de acceso rápida especial para las operaciones de bucleback.

Una vez que una aplicación establece la conexión en una interfaz de bucleback mediante la ruta de acceso rápida, todos los paquetes para la duración de la conexión deben usar la ruta de acceso rápida.

La aplicación **de SIO \_ LOOPBACK \_ FAST \_ PATH** a un socket que se conectará a una ruta de acceso sin bucles no tendrá ningún efecto.

Esta optimización del bucleback TCP da como resultado paquetes que fluyen a través de la capa de transporte (TL) en lugar del bucleback tradicional a través de la capa de red.
Esta optimización mejora la latencia de los paquetes de bucles de retorno.
Una vez que una aplicación opte por una configuración de nivel de conexión para usar la ruta de acceso rápida de bucle atrás, todos los paquetes seguirán la ruta de acceso del bucle de retorno.
Para las comunicaciones de bucle atrás, no se espera congestión ni pérdida de paquetes.
La noción de control de congestión y entrega confiable en TCP será innecesaria.
Sin embargo, esto no es cierto para el control de flujo.
Sin el control de flujo, el remitente puede sobrecargar el búfer de recepción, lo que conduce a un comportamiento erróneo del bucleback TCP.
El control de flujo en la ruta de acceso de bucle recuperación optimizada para TCP se mantiene colocando las solicitudes de envío en una cola.
Cuando el búfer de recepción está lleno, la pila TCP/IP garantiza que los envíos no se completan hasta que se mantiene el control de flujo de mantenimiento de la cola.

Las conexiones de bucle atrás de ruta de acceso rápida TCP en presencia de una llamada Windows Filtering Platform (WFP) para los datos de conexión deben tomar la ruta de acceso lenta no optimizada para bucles de recuperación.
Por lo tanto, los filtros WFP impedirán que se utilice esta nueva ruta de acceso rápida de bucles de retorno.
Cuando se habilita un filtro WFP, el sistema usará la ruta de acceso lenta incluso si se estableció el BUCLE DE BUCLE FAST **\_ \_ \_ RUTA** DE ACCESO DE SIO.
Esto garantiza que las aplicaciones en modo de usuario tengan la funcionalidad de seguridad de WFP completa.

De forma predeterminada, **SIO \_ LOOPBACK \_ FAST \_ PATH** está deshabilitado.

Solo se admite un subconjunto de las opciones de socket TCP/IP cuando se usa **SIO \_ LOOPBACK \_ FAST \_ PATH** IOCTL para habilitar la ruta de acceso rápida de bucle de retroceso en un socket.
La lista de opciones admitidas incluye lo siguiente:

* **TTL de IP \_**
* **IP \_ UNICAST \_ IF**
* **SALTOS \_ DE UNIDIFUSIÓN IPV6 \_**
* **IPV6 \_ UNICAST \_ IF**
* **IPV6 \_ V6ONLY**
* **ACEPTACIÓN \_ \_ CONDICIONAL DE SO**
* **SO \_ EXCLUSIVEADDRUSE**
* **ESCALABILIDAD \_ DE \_ PUERTOS**
* **SO \_ RCVBUF**
* **POR LO \_ TANTO, REUSEADDR**
* **TCP \_ BSDURGENT**

## <a name="see-also"></a>Vea también

[**IPPROTO_IP sockets**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**IPPROTO_IPV6 sockets**](/windows/desktop/winsock/ipproto-ipv6-socket-options)

[**IPPROTO_TCP sockets**](/windows/desktop/winsock/ipproto-tcp-socket-options)

[**Zócalo**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SOL_SOCKET sockets**](/windows/desktop/winsock/sol-socket-socket-options)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
