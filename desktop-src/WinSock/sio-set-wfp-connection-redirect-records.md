---
description: Código de control establece el registro de redirección en el nuevo socket TCP que se usa para conectar el servicio de redirección.
ms.assetid: 0AC78ED4-A6EC-4D62-919C-1EF7CDE8EE80
title: Código de control SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 11ce07c94104ecd986dc117b00dba2a49a7b5dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720646"
---
# <a name="sio_set_wfp_connection_redirect_records-control-code"></a>Código de control SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS

## <a name="description"></a>Descripción

El código de control **SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** establece el registro de redireccionamiento en el nuevo socket TCP usado para conectarse al destino final para que lo use un servicio de redirección de la plataforma de filtrado de Windows (WFP).

Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

```cpp
int WSAIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine, // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,              // a WSATHREADID structure
  (LPINT) lpErrno                          // a pointer to the error code.
);
```

## <a name="parameters"></a>Parámetros

### <a name="s"></a>s

Un descriptor que identifica un socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Código de control de la operación.
Use **SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** para esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada.
Este parámetro contiene un puntero al registro de redirección de WFP asociado al socket.

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
| **\_e/s de WSA \_ pendientes** | La operación de e/s superpuesta está en curso. Se devuelve este valor si una operación superpuesta se ha iniciado correctamente y la finalización se indicará en un momento posterior. |
| **\_operación WSA \_ anulada** | La operación de e/s se ha anulado debido a una salida de subproceso o una solicitud de aplicación. Se devuelve este error si se ha cancelado una operación superpuesta debido al cierre del socket o a la ejecución del comando **SIO_FLUSH** ioctl. |
| **WSAEACCES** | Se intentó tener acceso a un socket de una manera prohibida por sus permisos de acceso. Este error se devuelve en varias condiciones, entre las que se incluyen las siguientes: el usuario no dispone de los privilegios administrativos necesarios en el equipo local o la aplicación no se está ejecutando en un shell mejorado como administrador integrado ( `RunAs administrator` ). |
| **WSAEFAULT** | El sistema detectó una dirección de puntero no válida al intentar usar un argumento de puntero en una llamada. Este error se devuelve cuando el parámetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no está totalmente incluido en una parte válida del espacio de direcciones del usuario. |
| **WSAEINPROGRESS** | Se está ejecutando una operación de bloqueo actualmente. Se devuelve este error si la función se invoca cuando hay una devolución de llamada en curso. |
| **WSAEINTR** | Una operación de bloqueo fue interrumpida por una llamada a **WSACancelBlockingCall**. Se devuelve este error si se interrumpió una operación de bloqueo. |
| **WSAEINVAL** | Se proporcionó un argumento no válido. Se devuelve este error si el parámetro *dwIoControlCode* no es un comando válido o si un parámetro de entrada especificado no es aceptable, o si el comando no es aplicable al tipo de socket especificado. |
| **WSAENETDOWN** | Una operación de socket encontró una red inactiva. Se devuelve este error si se ha producido un error en el subsistema de red. |
| **WSAENOTSOCK** | Se intentó realizar una operación en algo que no es un socket. Se devuelve este error si el *descriptor* no es un socket. |
| **WSAEOPNOTSUPP** | La operación intentada no se admite para el tipo de objeto al que se hace referencia. Se devuelve este error si no se admite el comando IOCTL especificado. Este error también se devuelve si el proveedor de transporte no admite el **valor de SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** . |

## <a name="remarks"></a>Observaciones

El **valor de SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** es compatible con Windows 8, Windows Server 2012 y versiones posteriores del sistema operativo.

WFP permite el acceso a la ruta de procesamiento de paquetes TCP/IP, en la que se pueden examinar o cambiar los paquetes salientes y entrantes antes de permitir que se procesen más.
Al puntear en la ruta de acceso de procesamiento de TCP/IP, los fabricantes de software independientes (ISV) pueden crear más fácilmente firewalls, software antivirus, software de diagnóstico y otros tipos de aplicaciones y servicios.
WFP proporciona componentes en modo de usuario y de modo kernel para que los ISV de terceros puedan participar en las decisiones de filtrado que tienen lugar en varias capas de la pila de protocolos TCP/IP y en todo el sistema operativo.
La característica de redirección de conexión de WFP permite a un controlador de kernel de llamada de WFP redirigir una conexión localmente a un proceso de modo de usuario, realizar la inspección de contenido en modo de usuario y reenviar el contenido inspeccionado mediante una conexión diferente al destino original.

El **valor de SiO \_ set \_ WFP \_ Connection \_ Redirect \_ registra** ioctl y otros ioctl relacionados son componentes de modo usuario que se usan para permitir que varias aplicaciones proxy de conexión basadas en WFP inspeccionen el mismo flujo de tráfico de forma cooperativa.
Cada agente de inspección puede volver a inspeccionar de forma segura el tráfico de red que ya ha inspeccionado otro agente de inspección.
Con la presencia de varios servidores proxy (desarrollados por fabricantes de software independientes, por ejemplo), la conexión utilizada por un proxy para comunicarse con el destino final podría redirigirse a su vez por un segundo proxy, y esa nueva conexión podría redirigirse de nuevo mediante el proxy original.
Sin el seguimiento de la conexión, la conexión original podría no llegar nunca a su destino final, ya que se bloquea en un bucle proxy infinito.

El **valor de SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** se usa para proporcionar un seguimiento de la conexión de proxy en las conexiones de socket redirigido.
Esta característica de WFP facilita el seguimiento de los registros de redireccionamiento de la redirección inicial de una conexión a la conexión final con el destino.

El [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) ioctl se usa en un servicio de redireccionamiento basado en WFP para recuperar el registro de redireccionamiento de la conexión de paquetes TCP/IP aceptada (el socket conectado para un socket TCP o un socket UDP, por ejemplo) redireccionado a él mediante su llamada de modo kernel de la guía registrada en las capas de  **\_ \_ redirección de conexión Ale** en un controlador de modo kernel
El [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) ioctl recupera el contexto de redireccionamiento de un registro de redirección, que se utiliza.
El contexto de redireccionamiento es opcional y se usa si el estado de redirección actual de una conexión es que la conexión se redirigió mediante el servicio de redireccionamiento de llamada o que el servicio de redirección de llamada redirigió la conexión anteriormente, pero posteriormente se redirigió de nuevo mediante otro servicio de redirección. El servicio de redireccionamiento transfiere el registro de redireccionamiento recuperado al socket TCP que usa para crear el proxy del contenido original mediante el protocolo **SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** .

La aplicación que llama a la interfaz **SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records** no necesita comprender el BLOB que contiene el registro de redireccionamiento que se establece.
Se trata de un BLOB opaco de datos que la aplicación necesita devolver al nuevo socket.

## <a name="see-also"></a>Vea también

[**Opciones de IPPROTO_IP socket**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md)

[**tomacorriente**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
