---
description: El código de control obtiene una lista de direcciones de transporte locales de la familia de protocolos del socket a la que se puede enlazar la aplicación.
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: Código de control de SIO_ADDRESS_LIST_QUERY
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 7a728293afa51ceb58d61141e7184077478b787c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720651"
---
# <a name="sio_address_list_query-control-code"></a>Código de control de SIO_ADDRESS_LIST_QUERY

## <a name="description"></a>Descripción

El código de control de consulta de la lista de direcciones de SiO obtiene una lista de direcciones de transporte locales de la familia de protocolos del socket a la que se puede enlazar la aplicación. **\_ \_ \_**
La lista de direcciones varía en función de la familia de direcciones y algunas direcciones se excluyen de la lista.

Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

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

Un descriptor que identifica un socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Código de control de la operación.
Use **la \_ \_ \_ consulta** de la lista de direcciones de SiO para esta operación.

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
| **WSAEFAULT** | El parámetro *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | La función se invoca cuando una devolución de llamada está en curso. |
| **WSAEINTR** | Se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | El parámetro *dwIoControlCode* no es un comando válido o un parámetro de entrada especificado no es aceptable, o bien el comando no es aplicable al tipo de socket especificado. Se devuelve este error si el parámetro *cbInBuffer* no se establece en **null**. |
| **WSAENETDOWN** | Error en el subsistema de red. |
| **WSAENOBUFS** | No hay espacio de búfer disponible. |
| **WSAENOPROTOOPT** | No se admite la opción socket en el protocolo especificado. |
| **WSAENOTSOCK** | El descriptor *s* no es un socket. |
| **WSAEOPNOTSUPP** | No se admite el comando IOCTL especificado. Se devuelve este error si el proveedor de transporte no admite el ioctl de consulta de la **\_ lista de direcciones de \_ \_ SiO** . |

## <a name="remarks"></a>Observaciones

El ioctl de consulta de la lista de direcciones de SiO es compatible con Windows 2000 y versiones posteriores del sistema operativo. **\_ \_ \_**

El código de control de consulta de la lista de direcciones de SiO obtiene una lista de direcciones de transporte locales de la familia de protocolos del socket a la que se puede enlazar la aplicación. **\_ \_ \_**
La lista de direcciones varía en función de la familia de direcciones.

En el caso de la \_ familia de direcciones AF inet6, se devuelven todas las direcciones excepto las siguientes:

* Cualquier dirección IP en la que el estado de detección de direcciones duplicadas (DAD) no es IpDadStatePreferred.
* Cualquier dirección IP con un nivel de ámbito inferior a ScopeLevelSubnet en una interfaz en la que el tipo de interfaz es **si el \_ tipo es \_ \_ bucle invertido**.
Esto significa que las direcciones locales de vínculo (fe80: *) y de bucle invertido (:: 1) en las interfaces de si se excluye el tipo de **\_ \_ \_ bucle invertido de software** , pero no si estas direcciones se encuentran en una interfaz con un tipo diferente.

En el caso de la familia de direcciones de **AF \_ inet** , se devuelven todas las direcciones excepto las siguientes:

* Cualquier dirección IP en la que el estado de detección de direcciones duplicadas (DAD) no es IpDadStatePreferred.
* Cualquier dirección IP de una interfaz en la que el tipo de interfaz sea **si el \_ tipo de \_ \_ bucle invertido** y el vínculo es local.
Esto significa que las direcciones locales de vínculo (169,254 *) y bucle invertido (127.*) en las interfaces de si se excluye el tipo de **\_ \_ \_ bucle invertido de software** , pero no si estas direcciones se encuentran en una interfaz con un tipo diferente.

Para obtener más información sobre el estado del padre, consulte la documentación de la aplicación auxiliar de IP en la estructura de [**\_ \_ Estado**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) de los direcciones IP de los adaptadores de IP y la [**\_ \_ \_ dirección de unidifusión**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) y la documentación de MIB en la estructura de [**\_ \_ filas MIB UNICASTIPADDRESS**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) .
Para obtener más información sobre el tipo de interfaz, consulte la documentación de la aplicación auxiliar de IP en la estructura de [**direcciones del \_ adaptador \_ de IP**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) y la función [**GETADAPTERSADDRESSES**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) y la documentación de MIB en [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) estructura.
Para obtener más información sobre el nivel de ámbito, consulte la documentación de la aplicación auxiliar de IP en la estructura de [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) y la enumeración de [**\_ nivel de ámbito**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) .

La lista devuelta en el búfer de salida al que apunta el parámetro *lpvOutBuffer* tiene el formato de una estructura de [**lista de \_ direcciones \_ de socket**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) .

Si el búfer de salida especificado en el parámetro *lpvOutBuffer* no es lo suficientemente grande como para contener la lista de direcciones, el **\_ error de socket** se devuelve como resultado de este ioctl y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [WSAEFAULT](windows-sockets-error-codes-2.md).
En este caso, se devuelve el tamaño necesario, en bytes, para el búfer de salida en el parámetro *lpcbBytesReturned* .
Nota: el código de error [WSAEFAULT](windows-sockets-error-codes-2.md) también se devuelve si el parámetro *lpvInBuffer*, *lpvOutBuffer* o *lpcbBytesReturned* no está completamente incluido en una parte válida del espacio de direcciones del usuario.

Normalmente, la consulta de la lista de direcciones de SiO ioctl se llama sincrónicamente con el parámetro *lpvOverlapped* establecido en **null**, ya que la lista de direcciones se devuelve inmediatamente. **\_ \_ \_**

**Nota:**  En los entornos de plug-n-Play de Windows, las direcciones se pueden agregar y quitar de forma dinámica.
Por lo tanto, las aplicaciones no pueden basarse en la información devuelta por la consulta de lista de direcciones de SiO para ser persistentes. **\_ \_ \_**
Las aplicaciones pueden registrarse para recibir notificaciones de cambio de dirección a través del cambio de la lista de direcciones de SiO que proporciona la notificación a través de un evento de **cambio de \_ \_ lista \_ de direcciones** de e/s o FD superpuesto. **\_ \_ \_**
Se puede usar la siguiente secuencia de acciones para garantizar que la aplicación tenga siempre información de lista de direcciones actual:

* Emitir el **cambio de la lista de direcciones de SiO \_ \_ \_** ioctl
* Emitir la **consulta de la lista de direcciones de SiO \_ \_ \_** ioctl
* Siempre que el cambio de la **lista de direcciones de SiO \_ \_ \_ cambie** la llamada de ioctl notifica a la aplicación de un cambio en la lista de direcciones (ya sea a través de e/s superpuesta o por evento de cambio de **\_ \_ lista \_ de direcciones FD** ), se debe repetir la secuencia de acciones completa.

En el kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y el código de control de consulta de la lista de direcciones de SiO se define en el archivo de encabezado *Ws2def. h* . **\_ \_ \_**
Tenga en cuenta que el archivo de encabezado *Ws2def. h* se incluye automáticamente en *WinSock2. h* y nunca se debe usar directamente.

## <a name="see-also"></a>Vea también

[**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[**IP_ADAPTER_UNICAST_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[**IP_DAD_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[**MIB_UNICASTIPADDRESS_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[**SCOPE_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[**SOCKET_ADDRESS_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[**tomacorriente**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
