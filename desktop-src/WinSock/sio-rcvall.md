---
description: El código de control permite a un socket recibir todos los paquetes IPv4 o IPv6 que pasan a través de una interfaz de red.
ms.assetid: 1c198a70-6669-4599-bd9a-ffc26c9fe1d0
title: Código de control de SIO_RCVALL
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ddff631f1fa4b6b9f9af74f71e2b1eb38a2bf48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720363"
---
# <a name="sio_rcvall-control-code"></a>Código de control de SIO_RCVALL

## <a name="description"></a>Descripción
El código de control **SiO \_ RCVALL** permite a un socket recibir todos los paquetes IPv4 o IPv6 que pasan a través de una interfaz de red.

Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

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

Un descriptor que identifica un socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Código de control de la operación.
Use **SiO \_ RCVALL** para esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada que debe contener el valor de la opción.
Los valores posibles para la opción de ioctl **SiO \_ RCVALL** se especifican en la enumeración **RCVALL_VALUE** definida en el archivo de encabezado *Mstcpip. h* .

Los valores posibles para **SiO \_ RCVALL** son los siguientes:

| Value | Significado |
|-------|---------|
| **RCVALL \_ desactivado** | Deshabilite esta opción para que un socket no reciba todos los paquetes IPv4 o IPv6 que pasan a través de una interfaz de red. |
| **RCVALL \_** | Habilite esta opción para que un socket reciba todos los paquetes IPv4 o IPv6 que pasan a través de una interfaz de red. Esta opción habilita el modo promiscuo en la tarjeta de interfaz de red (NIC), si la NIC es compatible con el modo promiscuo. En un segmento LAN con un concentrador de red, una NIC que admita el modo promiscuo capturará todo el tráfico de IPv4 o IPv6 en la LAN, incluido el tráfico entre otros equipos del mismo segmento de LAN. Todos los paquetes capturados (IPv4 o IPv6, según el socket) se entregarán al socket sin formato. Esta opción no capturará otros paquetes (por ejemplo, paquetes ARP, IPX y NetBEUI) en la interfaz. Netmon usa el mismo modo para la interfaz de red, pero no usa esta opción para capturar el tráfico. |
| **RCVALL \_ SOCKETLEVELONLY** | Esta característica no está implementada actualmente, por lo que establecer esta opción no tiene ningún efecto. |
| **RCVALL \_ IPLEVEL** | Habilite esta opción para que un socket IPv4 o IPv6 reciba todos los paquetes en el nivel de IP que pasan a través de una interfaz de red. Esta opción no habilita el modo promiscuo en la tarjeta de interfaz de red. Esta opción solo afecta al procesamiento de paquetes en el nivel de IP. La NIC sigue recibiendo solo los paquetes dirigidos a sus direcciones de unidifusión y multidifusión configuradas. Sin embargo, un socket con esta opción habilitada no solo recibirá paquetes dirigidos a direcciones IP específicas, sino que recibirá todos los paquetes IPv4 o IPv6 que reciba la NIC. Esta opción no capturará otros paquetes (por ejemplo, los paquetes ARP, IPX y NetBEUI) recibidos en la interfaz. |

### <a name="cbinbuffer"></a>cbInBuffer

Tamaño, en bytes, del búfer de entrada.
Este parámetro debe ser igual o mayor que el tamaño del valor de enumeración **RCVALL_VALUE** al que apunta el parámetro *lpvInBuffer* .

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
| **\_e/s de WSA \_ pendientes** | Se inició correctamente una operación superpuesta y la finalización se indicará en un momento posterior. |
| **\_operación WSA \_ anulada** | Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **SIO_FLUSH** ioctl. |
| **WSAEFAULT** | El parámetro *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | La función se invoca cuando una devolución de llamada está en curso. |
| **WSAEINTR** | Se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | El parámetro *dwIoControlCode* no es un comando válido o un parámetro de entrada especificado no es aceptable, o bien el comando no es aplicable al tipo de socket especificado. Este error también se devuelve si el parámetro *cbInBuffer* es menor que `sizeof(UCHAR)` o el parámetro *lpvInBuffer* apunta a un valor que no es un valor de enumeración de **RCVALL_VALUE** . Este error también se puede devolver si no se encuentra la interfaz de red asociada al socket. Esto puede ocurrir si se elimina o se quita la interfaz de red asociada con el socket (por ejemplo, se quita un dispositivo de red PCMCIA o USB). |
| **WSAENETDOWN** | Error en el subsistema de red. |
| **WSAENOBUFS** | No hay espacio de búfer disponible. |
| **WSAENOPROTOOPT** | No se admite la opción socket en el protocolo especificado. |
| **WSAENOTSOCK** | El descriptor *s* no es un socket. |
| **WSAEOPNOTSUPP** | No se admite el comando IOCTL especificado. Se devuelve este error si el proveedor de transporte no admite el ioctl **SiO \_ RCVALL** . |

## <a name="remarks"></a>Observaciones

El **ioctl \_ RCVALL de SiO** es compatible con Windows 2000 y versiones posteriores del sistema operativo.

El ioctl **SiO \_ RCVALL** permite a un socket recibir todos los paquetes IPv4 o IPv6 en una interfaz de red.
El identificador de socket que se pasa a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** debe ser uno de los siguientes:

* Un socket IPv4 creado con la familia de direcciones establecida en AF_INET, el tipo de socket establecido en SOCK_RAW y el protocolo establecido en IPPROTO_IP.
* Un socket IPv6 que se creó con la familia de direcciones establecida en AF_INET6, el tipo de socket establecido en SOCK_RAW y el protocolo establecido en IPPROTO_IPV6.

Para obtener más información sobre los sockets sin formato, consulte [**Sockets sin formato de TCP/IP**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).

El socket también debe estar enlazado a una interfaz IPv4 o IPv6 local explícita, lo que significa que no se puede enlazar a **inaddress \_ any** o **in6addr \_ any**.

Una vez que se enlaza el socket y el IOCTL se completa correctamente, las llamadas a las funciones [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) o [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) devuelven datagramas IPv4 que pasan a través de la interfaz IPv4 dada o devuelven datagramas IPv6 que pasan a través de la interfaz IPv6 dada.
Tenga en cuenta que debe proporcionar un búfer suficientemente grande.
Al establecer este IOCTL solo se capturarán los paquetes IPv4 o IPv6 en una interfaz determinada.
Este IOCTL no capturará otros paquetes (por ejemplo, paquetes ARP, IPX y NetBEUI) en la interfaz.

Un socket enlazado a una interfaz local específica con el ioctl **SiO \_ RCVALL** solo recibirá los paquetes que pasan a través de esa interfaz.
No recibirá los paquetes recibidos en otra interfaz y se reenviarán en otra interfaz diferente a la del socket enlazado con **SiO \_ RCVALL** ioctl.

En Windows Server 2008 y versiones anteriores, el valor de ioctl de **SiO \_ RCVALL** no capturar los paquetes locales enviados fuera de una interfaz de red.
Esto incluye los paquetes recibidos en otra interfaz y reenviados fuera de la interfaz de red especificada para el ioctl **SiO \_ RCVALL** .

En Windows 7 y Windows Server 2008 R2, se ha cambiado para que los paquetes locales enviados fuera de una interfaz de red también se capturen.
Esto incluye los paquetes recibidos en otra interfaz y, a continuación, reenviar la interfaz de red enlazada al socket con el ioctl **SiO \_ RCVALL** .

La configuración de este IOCTL requiere privilegios de administrador en el equipo local.

Esta característica se denomina a veces modo promiscuo.
No se admite cualquier cambio directo de aplicar esta opción en una interfaz y, a continuación, a otra interfaz con una única llamada mediante este IOCTL.
Una aplicación debe usar primero este IOCTL para desactivar el comportamiento en la primera interfaz y, a continuación, utilizar este IOCTL para habilitar el comportamiento en una nueva interfaz.

## <a name="see-also"></a>Vea también

[**tomacorriente**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**Sockets sin formato de TCP/IP**](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
