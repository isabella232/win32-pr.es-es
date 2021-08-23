---
description: El código de control recupera el contexto de redireccionamiento para un registro de redirección utilizado por un Windows de redirección de la plataforma de filtrado.
ms.assetid: 87DB11BB-E08D-49DF-A211-133D813373E0
title: SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT código de control
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 268e1bf44c1370e49116414a367119ea8eb008a2711cbfcebdf64f6c3c1b8d62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244945"
---
# <a name="sio_query_wfp_connection_redirect_context-control-code"></a>SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT código de control

## <a name="description"></a>Descripción

El código de control **SIO \_ QUERY \_ WFP \_ CONNECTION REDIRECT \_ \_ CONTEXT** recupera el contexto de redirección para un registro de redirección utilizado por un servicio de redirección de Windows Filtering Platform (WFP).

Para realizar esta operación, llame a la [**función WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

```cpp
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
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
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
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
Use **SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ \_ CONTEXT** para esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada.
Este parámetro no se usa para esta operación.

### <a name="cbinbuffer"></a>cbInBuffer

Tamaño, en bytes, del búfer de entrada.
Este parámetro no se usa para esta operación.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntero al búfer de salida.
Este parámetro debe apuntar a un tipo de datos **ULONG** si los parámetros *lpOverlapped* y *lpCompletionRoutine* son **NULL.**

### <a name="cboutbuffer"></a>cbOutBuffer

Tamaño, en bytes, del búfer de salida.
Este parámetro debe ser al menos el tamaño de un **tipo de datos ULONG.**

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

En el caso de las operaciones superpuestas, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelve inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.
De lo contrario, la función no devuelve hasta que se ha completado la operación o se produce un error.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Puntero a la rutina de finalización a la que se llama cuando se ha completado la operación (se omite para sockets no superpuestos).

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
| **WSA \_ IO \_ PENDING** | Se inició correctamente una operación superpuesta y la finalización se indicará más adelante. |
| **OPERACIÓN WSA \_ \_ ANULADA** | Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del SIO_FLUSH IOCTL. |
| **WSAEFAULT** | El *parámetro lpvOutBuffer*, *lpcbBytesReturned,* *lpOverlapped* o *lpCompletionRoutine* no está totalmente contenido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | La función se invoca cuando hay una devolución de llamada en curso. |
| **WSAEINTR** | Se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | El *parámetro dwIoControlCode* no es un comando válido, un parámetro de entrada especificado no es aceptable o el comando no es aplicable al tipo de socket especificado. Este error se devuelve si el *parámetro cbOutBuffer* es menor que el tamaño de un **tipo de datos ULONG.** |
| **WSAENETDOWN** | Error en el subsistema de red. |
| **WSAENOPROTOOPT** | La opción de socket no se admite en el protocolo especificado. |
| **WSAENOTCONN** | Los *sockets no* están conectados. |
| **WSAENOTSOCK** | El descriptor *s no* es un socket. |
| **WSAEOPNOTSUPP** | No se admite el comando IOCTL especificado. Este error se devuelve si el proveedor de transporte no admite **SIO \_ QUERY \_ WFP \_ CONNECTION REDIRECT \_ \_ CONTEXT** IOCTL. |

## <a name="remarks"></a>Observaciones

**SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ \_ CONTEXT** IOCTL se admite en Windows 8, Windows Server 2012 y versiones posteriores del sistema operativo.

WFP permite el acceso a la ruta de procesamiento de paquetes TCP/IP, donde los paquetes salientes y entrantes se pueden examinar o cambiar antes de permitir que se procesen aún más.
Al pulsar en la ruta de acceso de procesamiento TCP/IP, los proveedores de software independientes (ISV) pueden crear más fácilmente firewalls, software antivirus, software de diagnóstico y otros tipos de aplicaciones y servicios.
WFP proporciona componentes de modo de usuario y modo kernel para que los ISV de terceros puedan participar en las decisiones de filtrado que tienen lugar en varias capas de la pila del protocolo TCP/IP y en todo el sistema operativo.
La característica de redirección de conexiones WFP permite que un controlador de kernel de llamada WFP redirija una conexión localmente a un proceso en modo de usuario, realice la inspección de contenido en modo de usuario y reenvía el contenido inspeccionado mediante una conexión diferente al destino original.

**SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ \_ CONTEXT** IOCTL y otros IOCTLS relacionados son componentes en modo de usuario que se usan para permitir que varias aplicaciones de proxy de conexión basadas en WFP inspeccionen el mismo flujo de tráfico de forma cooperativa.
Cada agente de inspección puede volver a inspeccionar de forma segura el tráfico de red que ya ha sido inspeccionado por otro agente de inspección.
Con la presencia de varios servidores proxy (desarrollados por diferentes ISV, por ejemplo), la conexión que usa un proxy para comunicarse con el destino final podría redirigirse a su vez mediante un segundo proxy y el proxy original podría redirigir de nuevo esa nueva conexión.
Sin el seguimiento de la conexión, es posible que la conexión original nunca llegue a su destino final, ya que se queda bloqueada en un bucle de proxy infinito.

**SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ \_ CONTEXT** IOCTL se usa para permitir que varias aplicaciones de proxy de conexión basadas en WFP inspeccionen el mismo flujo de tráfico de forma cooperativa.
Cada agente de inspección puede volver a inspeccionar de forma segura el tráfico de red que ya ha sido inspeccionado por otro agente de inspección.
Con la presencia de varios servidores proxy (desarrollados por diferentes ISV, por ejemplo), la conexión que usa un proxy para comunicarse con el destino final podría redirigirse a su vez mediante un segundo proxy y el proxy original podría redirigir de nuevo esa nueva conexión.
Sin el seguimiento de la conexión, es posible que la conexión original nunca llegue a su destino final, ya que se queda bloqueada en un bucle de proxy infinito.
**SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ \_ CONTEXT** IOCTL se usa para proporcionar el seguimiento de conexiones con proxy en las conexiones de socket redirigidas.
Esta característica WFP facilita el seguimiento de los registros de redireccionamiento desde el redireccionamiento inicial de una conexión a la conexión final al destino.

**Sio \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ \_ RECORDS** IOCTL es utilizado por un servicio de redirección basado en WFP para recuperar el registro de redirección de la conexión de paquete TCP/IP aceptada (el socket conectado para un socket TCP o un socket UDP, por ejemplo) redirigido a él mediante su llamada de modo kernel complementario registrada en las capas redirect de **ALE \_ CONNECT \_** en un controlador en modo kernel.
**Sio \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ \_ CONTEXT** IOCTL es utilizado por un servicio de redirección basado en WFP para recuperar el contexto de redireccionamiento de un registro de redireccionamiento de la conexión de paquetes TCP/IP aceptada (el socket conectado para un socket TCP o un socket UDP, por ejemplo) redirigido a él mediante su llamada complementaria registrada en las **capas** ALE_CONNECT_REDIRECT.
El contexto de redireccionamiento es opcional y se usa si el estado de redireccionamiento actual de una conexión es que el servicio de redirección que realiza la llamada redirija la conexión o que el servicio de redirección que realiza la llamada lo redirija previamente, pero posteriormente lo redirige de nuevo por otro servicio de redireccionamiento.
El servicio de redirección transfiere el registro de redireccionamiento recuperado al socket TCP que usa para proxyar el contenido original mediante **SIO \_ SET \_ WFP \_ CONNECTION REDIRECT \_ \_ RECORDS** IOCTL.

Dado que el contexto de redireccionamiento de WFP es un blob de datos de longitud variable establecido por el servicio de redirección, el autor de la llamada puede proporcionar un búfer de salida grande (un búfer de 1K al que apunta el parámetro *lpvOutBuffer,* por ejemplo) o puede pasar como un tamaño de búfer de salida en el *parámetro cbOutBuffer* de 0 para consultar el tamaño de búfer necesario para contener el blob devuelto.
Si el tamaño del búfer de salida no es suficiente para contener los datos, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devolverán **ERROR INSUFFICIENT \_ \_ BUFFER** y el tamaño de búfer necesario se devolverá en el valor al que apunta el parámetro *lpcbBytesReturned.*

La aplicación que llama a **SIO \_ QUERY \_ WF\P_CONNECTION \_ REDIRECT \_ RECORDS** IOCTL no necesita comprender el blob que contiene los registros de redirección recuperados.
Se trata de un blob opaco de datos que la aplicación necesita recuperar y devolver al nuevo socket.

## <a name="see-also"></a>Vea también

[**IPPROTO_IP sockets**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md)

[**SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS**](sio-set-wfp-connection-redirect-records.md)

[**Zócalo**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
