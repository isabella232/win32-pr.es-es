---
description: El código de control obtiene una lista de direcciones de transporte local de la familia de protocolos del socket a la que la aplicación puede enlazar.
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: SIO_ADDRESS_LIST_QUERY código de control
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 57d529ed4ea525b01e294efcacc1aa8dd2b118106177bd46cb64ffdf42a31a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097535"
---
# <a name="sio_address_list_query-control-code"></a>SIO_ADDRESS_LIST_QUERY código de control

## <a name="description"></a>Descripción

El código de control **SIO \_ ADDRESS LIST \_ \_ QUERY** obtiene una lista de direcciones de transporte local de la familia de protocolos del socket a la que se puede enlazar la aplicación.
La lista de direcciones varía en función de la familia de direcciones y algunas direcciones se excluyen de la lista.

Para realizar esta operación, llame a la [**función WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
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
Use **SIO \_ ADDRESS LIST \_ QUERY \_ para** esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada.
Este parámetro no se usa para esta operación.

### <a name="cbinbuffer"></a>cbInBuffer

Tamaño, en bytes, del búfer de entrada.
Este parámetro no se usa para esta operación.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntero al búfer de salida.

### <a name="cboutbuffer"></a>cbOutBuffer

Tamaño, en bytes, del búfer de salida.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.

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

Puntero a una [**estructura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que usará el proveedor en una llamada posterior a [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).
El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)

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
| **WSA \_ OPERATION \_ ABORTED** | Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **IOCTL DE SIO \_ FLUSH.** |
| **WSAEFAULT** | El *parámetro lpOverlapped* o *lpCompletionRoutine* no está totalmente contenido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | La función se invoca cuando hay una devolución de llamada en curso. |
| **WSAEINTR** | Se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | El *parámetro dwIoControlCode* no es un comando válido, o un parámetro de entrada especificado no es aceptable o el comando no es aplicable al tipo de socket especificado. Este error se devuelve si el *parámetro cbInBuffer* no está establecido en **NULL.** |
| **WSAENETDOWN** | Error en el subsistema de red. |
| **WSAENOBUFS** | No hay espacio de búfer disponible. |
| **WSAENOPROTOOPT** | La opción socket no se admite en el protocolo especificado. |
| **WSAENOTSOCK** | El descriptor *s* no es un socket. |
| **WSAEOPNOTSUPP** | No se admite el comando IOCTL especificado. Este error se devuelve si el proveedor de transporte no admite **SIO \_ ADDRESS LIST \_ \_ QUERY** IOCTL. |

## <a name="remarks"></a>Comentarios

**SIO \_ ADDRESS LIST \_ \_ QUERY** IOCTL se admite en Windows 2000 y versiones posteriores del sistema operativo.

El código de control **SIO \_ ADDRESS LIST \_ \_ QUERY** obtiene una lista de direcciones de transporte local de la familia de protocolos del socket a la que se puede enlazar la aplicación.
La lista de direcciones varía en función de la familia de direcciones.

Para la familia \_ de direcciones DE AF INET6, se devuelven todas las direcciones excepto las siguientes:

* Cualquier dirección IP en la que el estado de detección de direcciones duplicadas (DETECTOR) no sea IpDadStateP.
* Cualquier dirección IP con un nivel de ámbito inferior a ScopeLevelSubnet en una interfaz donde el tipo de interfaz **es IF TYPE SOFTWARE \_ \_ \_ LOOPBACK**.
Esto significa que se excluyen las direcciones locales de vínculo (fe80:*) y bucles de retroceso (::1) en interfaces de tipo **IF \_ TYPE SOFTWARE \_ \_ LOOPBACK,** pero no si estas direcciones están en una interfaz con un tipo diferente.

Para la **familia de direcciones DE AF \_ INET,** se devuelven todas las direcciones excepto las siguientes:

* Cualquier dirección IP en la que el estado de detección de direcciones duplicadas (DETECTOR) no sea IpDadStateP.
* Cualquier dirección IP en una interfaz donde el tipo de interfaz **es IF TYPE SOFTWARE \_ \_ \_ LOOPBACK** y el vínculo es local.
Esto significa que se excluyen las direcciones de vínculo local (169.254. ) y de bucleback *(127.*) en interfaces de tipo **IF TYPE SOFTWARE \_ \_ \_ LOOPBACK,** pero no si estas direcciones están en una interfaz con un tipo diferente.

Para obtener más información sobre el estado DE LA PROPIEDAD, consulte la documentación del asistente de IP sobre la enumeración [**IP DEL ESTADO DE IP \_ y \_**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) la estructura DE DIRECCIONES [**\_ \_ UNICAST \_**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) del ADAPTADOR DE IP y la documentación de MIB sobre la estructura [**\_ UNICASTIPADDRESS \_ ROW de MIB.**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)
Para obtener más información sobre el tipo de interfaz, vea la documentación del asistente de IP sobre la estructura [**IP \_ ADAPTER \_ ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) y la función [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) y la documentación de MIB [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) estructura.
Para obtener más información sobre el nivel de ámbito, consulte la documentación del asistente de IP sobre la [**estructura IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) y la [**enumeración SCOPE \_ LEVEL.**](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

La lista devuelta en el búfer de salida al que apunta el parámetro *lpvOutBuffer* tiene el formato de una [**estructura SOCKET ADDRESS \_ \_ LIST.**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

Si el búfer de salida especificado en el parámetro *lpvOutBuffer* no es lo suficientemente grande como para contener la lista de direcciones, se devuelve **SOCKET \_ ERROR** como resultado de esta IOCTL y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [WSAEFAULT](windows-sockets-error-codes-2.md).
El tamaño necesario, en bytes, para el búfer de salida se devuelve en el *parámetro lpcbBytesReturned* en este caso.
Tenga en cuenta que también se devuelve el código de error de [WSAEFAULT](windows-sockets-error-codes-2.md) si el parámetro *lpvInBuffer*, *lpvOutBuffer* o *lpcbBytesReturned* no está completamente contenido en una parte válida del espacio de direcciones del usuario.

La **IOCTL SIO \_ ADDRESS LIST \_ \_ QUERY** normalmente se llama sincrónicamente con el parámetro *lpvOverlapped* establecido en **NULL,** ya que la lista de direcciones se devuelve inmediatamente.

**Nota**  En Windows entornos plug-n-play, las direcciones se pueden agregar y quitar dinámicamente.
Por lo tanto, las aplicaciones no pueden confiar en que la información devuelta por **SIO \_ ADDRESS LIST \_ \_ QUERY** sea persistente.
Las aplicaciones pueden registrarse para recibir notificaciones de cambio de dirección a través de **SIO \_ ADDRESS LIST \_ \_ CHANGE** IOCTL, que proporciona la notificación a través de E/S superpuesta o evento **FD ADDRESS LIST \_ \_ \_ CHANGE.**
La siguiente secuencia de acciones se puede usar para garantizar que la aplicación siempre tiene información de lista de direcciones actual:

* Emisión de **LA LISTA DE DIRECCIONES DE SIO \_ \_ \_ CHANGE** IOCTL
* Emitir la **IOCTL DE CONSULTA DE LISTA \_ \_ DE \_ DIRECCIONES** DE SIO
* Cada vez que la llamada IOCTL CHANGE LIST **\_ \_ \_ DE SIO** ADDRESS LIST notifica a la aplicación un cambio en la lista de direcciones (ya sea a través de E/S superpuestas o mediante la señalización del evento **FD ADDRESS LIST \_ \_ \_ CHANGE),** se debe repetir toda la secuencia de acciones.

En el Kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y el código de control **SIO \_ ADDRESS LIST \_ \_ QUERY** se define en el archivo de encabezado *Ws2def.h.*
Tenga en cuenta que el archivo de encabezado *Ws2def.h* se incluye automáticamente en *Winsock2.h* y nunca se debe usar directamente.

## <a name="see-also"></a>Vea también

[**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[**IP_ADAPTER_UNICAST_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[**IP_DAD_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[**MIB_UNICASTIPADDRESS_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[**SCOPE_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[**SOCKET_ADDRESS_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[**Zócalo**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
