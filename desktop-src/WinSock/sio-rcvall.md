---
description: El código de control permite que un socket reciba todos los paquetes IPv4 o IPv6 que pasan a través de una interfaz de red.
ms.assetid: 1c198a70-6669-4599-bd9a-ffc26c9fe1d0
title: SIO_RCVALL código de control
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: d545bcdf8f3cc01159b3afbc86a686fb2bf8e83493784d2197353f19ff01e576
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993435"
---
# <a name="sio_rcvall-control-code"></a>SIO_RCVALL código de control

## <a name="description"></a>Descripción
El código de control **\_ RCVALL** de SIO permite que un socket reciba todos los paquetes IPv4 o IPv6 que pasan a través de una interfaz de red.

Para realizar esta operación, llame a la [**función WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a>Parámetros

### <a name="s"></a>s

Descriptor que identifica un socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Código de control de la operación.
Use **SIO \_ RCVALL para** esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada que debe contener el valor de opción.
Los valores posibles de la opción IOCTL DE **SIO \_ RCVALL** se especifican en la enumeración **RCVALL_VALUE** definida en el archivo de encabezado *Mstcpip.h.*

Los valores posibles **para SIO \_ RCVALL** son los siguientes:

| Valor | Significado |
|-------|---------|
| **RCVALL \_ OFF** | Deshabilite esta opción para que un socket no reciba todos los paquetes IPv4 o IPv6 que pasan a través de una interfaz de red. |
| **RCVALL \_ ON** | Habilite esta opción para que un socket reciba todos los paquetes IPv4 o IPv6 que pasan a través de una interfaz de red. Esta opción habilita el modo promiscuo en la tarjeta de interfaz de red (NIC), si la NIC admite el modo promiscuo. En un segmento LAN con un centro de red, una NIC que admita el modo promiscuo capturará todo el tráfico IPv4 o IPv6 en la LAN, incluido el tráfico entre otros equipos en el mismo segmento de LAN. Todos los paquetes capturados (IPv4 o IPv6, según el socket) se entregarán al socket sin formato. Esta opción no capturará otros paquetes (paquetes ARP, IPX y NetBEUI, por ejemplo) en la interfaz. Netmon usa el mismo modo para la interfaz de red, pero no usa esta opción para capturar tráfico. |
| **RCVALL \_ SOCKETLEVELONLY** | Esta característica no está implementada actualmente, por lo que establecer esta opción no tiene ningún efecto. |
| **RCVALL \_ IPLEVEL** | Habilite esta opción para que un socket IPv4 o IPv6 reciba todos los paquetes en el nivel de IP que pasan a través de una interfaz de red. Esta opción no habilita el modo promiscuo en la tarjeta de interfaz de red. Esta opción solo afecta al procesamiento de paquetes en el nivel de IP. La NIC todavía recibe solo paquetes dirigidos a sus direcciones de unidifusión y multidifusión configuradas. Sin embargo, un socket con esta opción habilitada no solo recibirá paquetes dirigidos a direcciones IP específicas, sino que recibirá todos los paquetes IPv4 o IPv6 que recibe la NIC. Esta opción no capturará otros paquetes (paquetes ARP, IPX y NetBEUI, por ejemplo) recibidos en la interfaz. |

### <a name="cbinbuffer"></a>cbInBuffer

Tamaño, en bytes, del búfer de entrada.
Este parámetro debe ser igual o mayor que el tamaño de la enumeración **RCVALL_VALUE** valor de enumeración al que apunta *el parámetro lpvInBuffer.*

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntero al búfer de salida.
Este parámetro no se usa para esta operación.

### <a name="cboutbuffer"></a>cbOutBuffer

Tamaño, en bytes, del búfer de salida.
Este parámetro no se usa para esta operación.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.
Este parámetro no se usa para esta operación.

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
| **WSA \_ IO \_ PENDING** | Se inició correctamente una operación superpuesta y la finalización se indicará más adelante. |
| **WSA \_ OPERATION \_ ABORTED** | Se canceló una operación superpuesta debido al cierre del  socket o a la ejecución del SIO_FLUSH IOCTL. |
| **WSAEFAULT** | El *parámetro lpOverlapped* o *lpCompletionRoutine* no está totalmente contenido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | La función se invoca cuando hay una devolución de llamada en curso. |
| **WSAEINTR** | Se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | El *parámetro dwIoControlCode* no es un comando válido, o un parámetro de entrada especificado no es aceptable o el comando no es aplicable al tipo de socket especificado. Este error también se devuelve si el *parámetro cbInBuffer* es menor que o el parámetro `sizeof(UCHAR)` *lpvInBuffer* apunta a un valor que no es RCVALL_VALUE de enumeración.  Este error también se puede devolver si no se encuentra la interfaz de red asociada al socket. Esto podría ocurrir si se elimina o quita la interfaz de red asociada al socket (por ejemplo, un dispositivo de red PCMCIA o USB). |
| **WSAENETDOWN** | Error en el subsistema de red. |
| **WSAENOBUFS** | No hay espacio de búfer disponible. |
| **WSAENOPROTOOPT** | La opción socket no se admite en el protocolo especificado. |
| **WSAENOTSOCK** | El descriptor *s* no es un socket. |
| **WSAEOPNOTSUPP** | No se admite el comando IOCTL especificado. Este error se devuelve si el proveedor de transporte no admite LA IOCTL DE **SIO \_ RCVALL.** |

## <a name="remarks"></a>Comentarios

**SIO \_ RCVALL** IOCTL se admite en Windows 2000 y versiones posteriores del sistema operativo.

**SIO \_ RCVALL** IOCTL permite que un socket reciba todos los paquetes IPv4 o IPv6 en una interfaz de red.
El identificador de socket pasado a [**la función WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) **o WSPIoctl** debe ser uno de los siguientes:

* Socket IPv4 que se creó con la familia de direcciones establecida en AF_INET, el tipo de socket establecido en SOCK_RAW y el protocolo establecido en IPPROTO_IP.
* Socket IPv6 que se creó con la familia de direcciones establecida en AF_INET6, el tipo de socket establecido en SOCK_RAW y el protocolo establecido en IPPROTO_IPV6.

Para obtener más información sobre los sockets sin procesar, [**vea Sockets sin formato TCP/IP.**](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

El socket también debe enlazarse a una interfaz IPv4 o IPv6 local explícita, lo que significa que no se puede enlazar a **INADDR \_ ANY** ni **a in6addr. \_**

Una vez enlazado el socket y la IOCTL se completa correctamente, las llamadas a las funciones [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) o [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) devuelven datagramas IPv4 que pasan a través de la interfaz IPv4 dada o devuelven datagramas IPv6 que pasan a través de la interfaz IPv6 dada.
Tenga en cuenta que debe proporcionar un búfer lo suficientemente grande.
Establecer esta IOCTL solo capturará paquetes IPv4 o IPv6 en una interfaz determinada.
Esta IOCTL no capturará otros paquetes (paquetes ARP, IPX y NetBEUI, por ejemplo) en la interfaz.

Un socket enlazado a una interfaz local específica con LA IOCTL DE **SIO \_ RCVALL** recibirá solo los paquetes que pasan a través de esa interfaz.
No recibirá paquetes recibidos en otra interfaz y se reenviarán en otra interfaz diferente del socket enlazado con **SIO \_ RCVALL** IOCTL.

En Windows Server 2008 y versiones anteriores, la configuración DE IOCTL DE **SIO \_ RCVALL** no capturaba los paquetes locales enviados fuera de una interfaz de red.
Esto incluía los paquetes recibidos en otra interfaz y reenviaba la interfaz de red especificada para LA IOCTL DE **SIO \_ RCVALL.**

En Windows 7 y Windows Server 2008 R2, esto se cambió para que también se capturaron los paquetes locales enviados fuera de una interfaz de red.
Esto incluye los paquetes recibidos en otra interfaz y, a continuación, reenviado la interfaz de red enlazada al socket **con SIO \_ RCVALL** IOCTL.

Establecer esta IOCTL requiere privilegios de administrador en el equipo local.

Esta característica se conoce a veces como modo promiscuo.
No se admite ningún cambio directo al aplicar esta opción en una interfaz y, a continuación, en otra interfaz con una sola llamada mediante esta IOCTL.
Una aplicación debe usar primero esta IOCTL para desactivar el comportamiento en la primera interfaz y, a continuación, usar esta IOCTL para habilitar el comportamiento en una nueva interfaz.

## <a name="see-also"></a>Vea también

[**Zócalo**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**Sockets sin formato TCP/IP**](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
