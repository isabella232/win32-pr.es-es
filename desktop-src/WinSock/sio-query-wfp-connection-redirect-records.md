---
description: El código de control recupera el registro de redireccionamiento para la conexión TCP/IP aceptada para su uso por parte de un servicio de redireccionamiento de la plataforma de filtrado de Windows.
ms.assetid: E0D7CC1A-8F93-45A0-9543-3F2ACAF352F5
title: Código de control de SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 2389914d29bd403a33e23065c29f549a01adbb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720479"
---
# <a name="sio_query_wfp_connection_redirect_records-control-code"></a>Código de control de SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS

## <a name="description"></a>Descripción

El código de control de la conexión de WFP de la **consulta SiO recupera el registro \_ \_ \_ \_ \_** de redireccionamiento para la conexión TCP/IP aceptada para su uso por parte de un servicio de redireccionamiento de la plataforma de filtrado de Windows (WFP).

Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
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
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a>Parámetros

### <a name="s"></a>s

Un descriptor que identifica un socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Código de control de la operación.
Use **SiO \_ query \_ WFP \_ \_ redirigir \_ registros** para esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada.
Este parámetro no se usa para esta operación.

### <a name="cbinbuffer"></a>cbInBuffer

Tamaño, en bytes, del búfer de entrada.
Este parámetro no se usa para esta operación.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntero al búfer de salida.
Este parámetro debe apuntar a un tipo de datos **ULong** si los parámetros *lpOverlapped* y *lpCompletionRoutine* son **null**.

### <a name="cboutbuffer"></a>cbOutBuffer

Tamaño, en bytes, del búfer de salida.
Este parámetro debe ser al menos el tamaño de un tipo de datos **ULong** .

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.

Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *LpcbBytesReturned* apunta a un valor **DWORD** de cero.

Si *lpOverlapped* es **null**, el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* devuelto en una llamada correcta no puede ser cero.

Si el parámetro *lpOverlapped* no es **null** para los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.
El valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que no se puede determinar el tamaño de los datos almacenados hasta que se haya completado la operación superpuesta.
Se puede recuperar el estado final de finalización cuando se señala el método de finalización adecuado cuando se ha completado la operación.

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
| **ERROR \_ de \_ búfer insuficiente** | El área de datos que se pasa a una llamada del sistema es demasiado pequeña. Se devuelve este error si el búfer señalado por el parámetro *lpvOutBuffer* con un tamaño de búfer pasado en el parámetro *cbOutBuffer* es demasiado pequeño. El tamaño de búfer necesario se devolverá en el parámetro *lpcbBytesReturned* . |
| **WSA_IO_PENDING** | Se inició correctamente una operación superpuesta y la finalización se indicará en un momento posterior. |
| **WSA_OPERATION_ABORTED** | Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **SIO_FLUSH** ioctl. |
| **WSAEFAULT** | Los parámetros *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no están totalmente contenidos en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | La función se invoca cuando una devolución de llamada está en curso. |
| **WSAEINTR** | Se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | El parámetro *dwIoControlCode* no es un comando válido o un parámetro de entrada especificado no es aceptable, o bien el comando no es aplicable al tipo de socket especificado. Se devuelve este error si el parámetro *cbOutBuffer* es menor que el tamaño de un tipo de datos **ULong** . |
| **WSAENETDOWN** | Error en el subsistema de red. |
| **WSAENOPROTOOPT** | No se admite la opción socket en el protocolo especificado. |
| **WSAENOTCONN** | El socket *s* no está conectado. |
| **WSAENOTSOCK** | El descriptor *s* no es un socket. |
| **WSAEOPNOTSUPP** | No se admite el comando IOCTL especificado. Este error se devuelve si el proveedor de transporte no admite los registros de la conexión de WFP de la **\_ consulta \_ \_ \_ \_ SiO** . |

## <a name="remarks"></a>Observaciones

Los registros de la conexión de WFP de la **\_ consulta \_ \_ \_ \_ SiO** se admiten en Windows 8, Windows Server 2012 y versiones posteriores del sistema operativo.

WFP permite el acceso a la ruta de procesamiento de paquetes TCP/IP, en la que se pueden examinar o cambiar los paquetes salientes y entrantes antes de permitir que se procesen más.
Al puntear en la ruta de acceso de procesamiento de TCP/IP, los fabricantes de software independientes (ISV) pueden crear más fácilmente firewalls, software antivirus, software de diagnóstico y otros tipos de aplicaciones y servicios.
WFP proporciona componentes en modo de usuario y de modo kernel para que los ISV de terceros puedan participar en las decisiones de filtrado que tienen lugar en varias capas de la pila de protocolos TCP/IP y en todo el sistema operativo.
La característica de redirección de conexión de WFP permite a un controlador de kernel de llamada de WFP redirigir una conexión localmente a un proceso de modo de usuario, realizar la inspección de contenido en modo de usuario y reenviar el contenido inspeccionado mediante una conexión diferente al destino original.

La opción **SiO Query de la \_ \_ \_ conexión WFP \_ \_ registra los registros** ioctl y otros ioctl relacionados son componentes de modo usuario que se usan para permitir que varias aplicaciones proxy de conexión basadas en WFP inspeccionen el mismo flujo de tráfico de forma cooperativa.
Cada agente de inspección puede volver a inspeccionar de forma segura el tráfico de red que ya ha inspeccionado otro agente de inspección.
Con la presencia de varios servidores proxy (desarrollados por fabricantes de software independientes, por ejemplo), la conexión utilizada por un proxy para comunicarse con el destino final podría redirigirse a su vez por un segundo proxy, y esa nueva conexión podría redirigirse de nuevo mediante el proxy original.
Sin el seguimiento de la conexión, la conexión original podría no llegar nunca a su destino final, ya que se bloquea en un bucle proxy infinito.

Los registros de la conexión de WFP de la **\_ consulta \_ \_ \_ \_ SiO** se usan para proporcionar el seguimiento de la conexión de proxy en las conexiones de socket redirigido.
Esta característica de WFP facilita el seguimiento de los registros de redireccionamiento de la redirección inicial de una conexión a la conexión final con el destino.

El servicio de redireccionamiento basado en WFP usa el servicio de redirección basada en WFP para recuperar el registro de redireccionamiento de la conexión de paquetes TCP/IP aceptada (el socket conectado para un socket TCP o un socket UDP, por ejemplo), se le redirigió mediante su llamada de modo kernel asociada a **ALE_CONNECT_REDIRECT** capas en un controlador de modo kernel. **\_ \_ \_ \_ \_**
El servicio de redirección basada en WFP usa el contexto de redireccionamiento de **\_ \_ \_ conexión \_ \_ WFP de la consulta SiO** para recuperar el contexto de redireccionamiento de un registro de redirección de la conexión de paquetes TCP/IP aceptada (el socket conectado para un socket TCP o un socket UDP, por ejemplo) redirigido a él mediante su llamada complementaria registrada en las capas de **\_ \_ redirección de Ale** .
El contexto de redireccionamiento es un contexto opcional asignado por el controlador que se usa si el estado de redirección actual de una conexión es que la conexión se redirigió mediante el servicio de redireccionamiento de llamada o la conexión se redirigió previamente mediante el servicio de redireccionamiento de llamada, pero posteriormente se redirigió de nuevo mediante otro servicio de redirección.
En el caso de una conexión de proxy TCP, el servicio de redirección transfiere el registro de redirección recuperado al socket TCP que usa para crear el proxy del contenido original mediante el protocolo **SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** .

Cuando el servicio de redirección está redirigiendo a un socket que no es TCP (por ejemplo, UDP), los registros de redireccionamiento devueltos por la conexión de la conexión de WFP de la **consulta SiO indican a este servicio el \_ \_ \_ \_ \_** servicio de redireccionamiento mediante la estructura [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) utilizada con la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .
El miembro de control de la estructura [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) tendría un cmsg_type en la estructura **WSACMSGHDR** establecida en **\_ \_ \_ registro de redirección de conexión IP**.
El servicio de redirección debe proporcionar el parámetro [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) al aceptar redirecciones que no son TCP.

Para el tráfico que no es TCP, el registro de redireccionamiento se reenvía mediante la estructura [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) con la función [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .

Tenga en cuenta que para el tráfico que no es TCP, solo el paquete de creación de flujo llevará el **\_ \_ \_ registro de redirección de la conexión IP**.
Como resultado, solo el primer paquete de proxy debe incluir esta información mediante la función [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .

Dado que el registro de redirección de WFP es un BLOB de datos de longitud variable, el autor de la llamada puede proporcionar un búfer de salida de gran tamaño (por ejemplo, un búfer de 1.024 bytes al que apunta el parámetro *lpvOutBuffer* ) o puede pasar un tamaño de búfer de salida en el parámetro *cbOutBuffer* de 0 para consultar el tamaño de búfer necesario para contener el BLOB devuelto.
Si el tamaño del búfer de salida no es suficiente para almacenar los datos, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devolverán un **error de \_ \_ búfer insuficiente** y se devolverá el tamaño de búfer necesario en el valor al que apunta el parámetro *lpcbBytesReturned* .

La aplicación que llama a la [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) no necesita comprender el BLOB que contiene el contexto de redireccionamiento recuperado.
Se trata de un BLOB opaco de datos que la aplicación necesita recuperar y devolver al nuevo socket.

## <a name="see-also"></a>Vea también

[**Opciones de IPPROTO_IP socket**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md)

[**tomacorriente**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)

[**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
