---
description: Solicita el modo en que la pila de red debe controlar ciertos comportamientos para los que la manera predeterminada de controlar el comportamiento puede diferir en las versiones de Windows.
ms.assetid: 9574e21f-5ac4-4210-8031-2f3b07416813
title: Código de control de SIO_SET_COMPATIBILITY_MODE
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 58972595adb71a30728cb4817a80814cd987a6de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720362"
---
# <a name="sio_set_compatibility_mode-control-code"></a>Código de control de SIO_SET_COMPATIBILITY_MODE

## <a name="description"></a>Descripción

El código de control de **\_ modo de \_ compatibilidad \_ SiO Set** solicita el modo en que la pila de red debe controlar ciertos comportamientos para los que la manera predeterminada de controlar el comportamiento puede diferir en las versiones de Windows.

Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_SET_COMPATIBILITY_MODE, // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to WSA_COMPATIBILITY_MODE struct
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
  (socket) s,             // descriptor identifying a socket
  SIO_SET_COMPATIBILITY_MODE, // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to WSA_COMPATIBILITY_MODE struct
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
Use **SiO \_ set \_ Compatibility \_ mode** para esta operación.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntero al búfer de entrada.
Este parámetro debe apuntar a una estructura de **\_ \_ modo de compatibilidad WSA** .

### <a name="cbinbuffer"></a>cbInBuffer

Tamaño, en bytes, del búfer de entrada.
Este parámetro debe ser igual o mayor que el tamaño de la estructura del **\_ \_ modo de compatibilidad WSA** señalada por el parámetro *lpvInBuffer* .

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
| **WSAEINVAL** | El parámetro *dwIoControlCode* no es un comando válido o un parámetro de entrada especificado no es aceptable, o bien el comando no es aplicable al tipo de socket especificado. Se devuelve este error si el parámetro *cbInBuffer* es menor que el tamaño de la estructura del **\_ \_ modo de compatibilidad WSA** .
| **WSAENETDOWN** | Error en el subsistema de red. |
| **WSAENOPROTOOPT** | No se admite la opción socket en el protocolo especificado. |
| **WSAENOTCONN** | El socket s no está conectado. |
| **WSAENOTSOCK** | El descriptor *s* no es un socket. |
| **WSAEOPNOTSUPP** | No se admite el comando IOCTL especificado. Este error se devuelve si el proveedor de transporte no admite el **\_ modo de \_ compatibilidad \_ de SiO Set** . También se devuelve este error cuando se intenta usar el **modo de \_ \_ compatibilidad \_ de SiO Set** ioctl en un socket de datagrama. |

## <a name="remarks"></a>Observaciones

el método **SiO \_ set \_ Compatibility \_ mode** solicita cómo la pila de red debe controlar ciertos comportamientos para los que la manera predeterminada de controlar el comportamiento puede diferir en las versiones de Windows.
La estructura de argumentos de entrada para el **\_ modo de \_ compatibilidad \_ de SiO Set** se especifica en la estructura del **\_ \_ modo de compatibilidad WSA** definida en el archivo de encabezado *Mswsockdef. h* .
Un puntero a la estructura del **\_ \_ modo de compatibilidad WSA** se pasa en el parámetro *cbInBuffer* .
Esta estructura se define de la siguiente manera:

```cpp
// Need to #include <mswsock.h>

/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

El valor especificado en el miembro **BehaviorId** indica el comportamiento solicitado.
El valor especificado en el miembro **TargetOsVersion** indica la versión de Windows que se solicita para el comportamiento.

El miembro **BehaviorId** puede ser uno de los valores del tipo de enumeración de identificador de **\_ \_ comportamiento \_ de compatibilidad WSA** definido en el archivo de encabezado *Mswsockdef. h* .
Los valores posibles para el miembro **BehaviorId** son los siguientes:

| Término | Descripción |
|------|-------------|
| WsaBehaviorAll | Esto es equivalente a solicitar todos los posibles comportamientos compatibles definidos para el **identificador de \_ \_ comportamiento de \_ compatibilidad WSA**. |
| WsaBehaviorReceiveBuffering | Cuando el miembro **TargetOsVersion** se establece en un valor de Windows Vista o posterior, se permite reducir el tamaño del búfer de recepción TCP en este socket mediante la opción de socket **so \_ RCVBUF** , incluso después de establecer una conexión TCP. Cuando el miembro **TargetOsVersion** se establece en un valor anterior a Windows Vista, no se permiten las reducciones del tamaño del búfer de recepción TCP en este socket mediante la opción de socket **so \_ RCVBUF** después del establecimiento de la conexión. |
| WsaBehaviorAutoTuning | Cuando el miembro **TargetOsVersion** se establece en un valor de Windows Vista o posterior, el ajuste automático de la ventana de recepción está habilitado y el factor de escala de la ventana TCP se reduce a 2 desde el valor predeterminado de 8. Cuando **TargetOsVersion** se establece en un valor anterior a Windows Vista, se deshabilita el ajuste automático de la ventana de recepción. La opción de escalado de la ventana TCP también está deshabilitada y el tamaño máximo de la ventana de recepción true está limitado a 65.535 bytes. No se puede negociar la opción de escalado de la ventana TCP en la conexión aunque se haya llamado a la opción de socket for **\_ RCVBUF** en este socket, especificando un valor superior a 65.535 bytes antes de que se establezca la conexión. |

El miembro **TargetOsVersion** puede ser una de las constantes de la versión NTDDI definidas en el archivo de encabezado *Sdkddkver. h* .
Algunos de los valores posibles para el miembro **TargetOsVersion** son los siguientes:

| Término | Descripción |
|------|-------------|
| NTDDI \_ Longhorn | El comportamiento de destino es el valor predeterminado para Windows Vista. |
| NTDDI \_ WS03 | El comportamiento de destino es el valor predeterminado para Windows Server 2003. |
| NTDDI \_ WinXP | El comportamiento de destino es el valor predeterminado para Windows XP. |
| NTDDI \_ WIN2K | El comportamiento de destino es el valor predeterminado para Windows 2000. |

El impacto principal del miembro **TargetOsVersion** es si este miembro está establecido en un valor igual o mayor que **NTDDI \_ Longhorn**.

El rendimiento de TCP no depende solo de la velocidad de transferencia en sí, sino en el producto de la velocidad de transferencia y el tiempo de retraso de ida y vuelta.
Este producto de retraso de ancho de banda mide la cantidad de datos que "rellenarán la canalización".
Este producto de retraso de ancho de banda es el espacio de búfer necesario en el remitente y el receptor para obtener el máximo rendimiento de la conexión TCP a través de la ruta de acceso.
Este espacio de búfer representa la cantidad de datos no confirmados que TCP debe administrar para mantener la canalización completa.
Los problemas de rendimiento de TCP surgen cuando el producto de retraso de ancho de banda es grande.
Una ruta de acceso de red que opere bajo estas condiciones se denomina a menudo "canalización de larga y FAT".
Entre los ejemplos se incluyen vínculos satélite de paquetes de alta capacidad, vínculos inalámbricos de alta velocidad y vínculos ópticos de fibra terrestre a larga distancia.

El encabezado TCP usa un campo de datos de 16 bits (el campo de ventana del encabezado del paquete TCP) para notificar el tamaño de la ventana de recepción al remitente.
Por lo tanto, la ventana más grande que se puede utilizar es 65.535 bytes.
Para eludir esta limitación, se ha agregado una opción de extensión TCP, escala de ventana de TCP, para TCP de alto rendimiento con el fin de admitir Windows de más de 65.535 bytes.
La opción de escala de ventana de TCP (WSopt) se define en RFC 1323, disponible en el [sitio web de IETF](https://www.ietf.org/rfc/rfc1122.txt).
La extensión WSopt expande la definición de la ventana TCP a 32 bits mediante un factor de escala logarítmica de un byte para extender el campo de la ventana de 16 bits en el encabezado TCP.
La extensión WSopt define un factor de escala implícito (2 a cierta potencia), que se usa para multiplicar el valor de tamaño de la ventana que se encuentra en un encabezado TCP para obtener el tamaño de ventana verdadero.
Por lo tanto, un factor de escala de una ventana de 8 daría como resultado un tamaño de ventana verdadero igual al valor en el campo de la ventana en el encabezado TCP multiplicado por 2 ^ 8 o 256.
Por tanto, si el campo de la ventana del encabezado TCP se estableció en el valor máximo de 65.535 bytes y el factor de escala WSopt se negoció con un valor de 8, el tamaño de ventana verdadero sería de 16.776.960 bytes.

El tamaño de la ventana de recepción real y, por tanto, el factor de escala viene determinado por el espacio máximo del búfer de recepción.
Este espacio de búfer máximo es la cantidad de datos que un receptor TCP permite enviar a un remitente de TCP antes de tener que esperar una confirmación.
Una vez establecida la conexión, el tamaño de la ventana de recepción se anuncia en cada segmento TCP (el campo de ventana del encabezado TCP).
La publicidad de la cantidad máxima de datos que el remitente puede enviar es un mecanismo de control de flujo del receptor que impide que el remitente envíe datos que el receptor no puede almacenar.
Un host de envío solo puede enviar la cantidad máxima de datos anunciada por el receptor antes de esperar una confirmación y una actualización del tamaño de la ventana de recepción.

En Windows Server 2003 y Windows XP, el espacio de búfer de recepción máximo que representa el tamaño de la ventana de recepción para la pila TCP/IP tiene un valor predeterminado basado en la velocidad de vínculo de la interfaz de envío.
El valor real se ajusta automáticamente a los incrementos pares del tamaño máximo de segmento (MSS) negociado durante el establecimiento de la conexión TCP.
Por lo tanto, para un vínculo de 10 Mbits/s, el tamaño de la ventana de recepción predeterminada se establecería normalmente en 16 k bytes, mientras que en un vínculo de 100 MBit/s el tamaño de la ventana de recepción predeterminada se establecería en 65.535 bytes.

En Windows Server 2003 y Windows XP, el tamaño máximo de la ventana de recepción máxima para la pila TCP/IP puede configurarse manualmente con los siguientes valores del registro en una interfaz específica o en todo el sistema:

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\TCPWindowSize`

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\Interface\TCPWindowSize`

El valor del registro para **TcpWindowSize** se puede establecer en un máximo de 65.535 bytes si no se usa la extensión WSopt o un máximo de 1.073.741.823 bytes cuando se usa la extensión WSopt (se admite un factor de escala máximo de 4).
Sin el escalado de ventanas, una aplicación solo puede lograr un rendimiento de aproximadamente 5 megabits por segundo (Mbps) en una ruta de acceso con un tiempo de ida y vuelta (RTT) de 100 milisegundos, independientemente del ancho de banda de la ruta de acceso.
Este rendimiento se puede escalar a más de un gigabit por segundo (Gbps) con el escalado de ventanas, lo que permite que TCP negocie el factor de escala para el tamaño de la ventana durante el establecimiento de la conexión.

En Windows Server 2003 y Windows XP, la extensión WSopt se puede habilitar estableciendo el siguiente valor del registro.

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\Tcp1323Opts`

El valor del registro **Tcp1323Opts** es una codificación **DWORD** que, cuando se establece el bit 0, está habilitada la extensión TCP WSopt.
Cuando se establece el bit 1, se habilita la opción de marca de tiempo de TCP (TSopt) definida en RFC 1323.
Por lo tanto, un valor de 1 o 3 habilitará la extensión WSopt.

En Windows Server 2003 y Windows XP, el valor predeterminado es que no se crean los valores del registro TCPWindowSize y Tcp1323Opts.
De modo que el valor predeterminado es que la extensión WSopt está deshabilitada y el tamaño de la ventana de recepción TCP se establece en el valor máximo de hasta 65.535 bytes según la velocidad del vínculo.
Cuando el escalado de ventanas está habilitado en Windows Server 2003 y Windows XP mediante el establecimiento del valor del registro Tcp1323Opts, el escalado de ventanas en una conexión TCP se sigue usando solo cuando el remitente y el receptor incluyen una opción de escala de ventana TCP en el segmento sincronizado (SYN) que se envía entre sí para negociar un factor de escala de ventana.
Cuando se usa el escalado de ventanas en una conexión, el campo de ventana del encabezado TCP se establece en 65.535 bytes y el factor de escala de la ventana se usa para ajustar el tamaño de la ventana de recepción real de forma ascendente por el factor de escala de la ventana negociado cuando se establece la conexión.

Una aplicación puede especificar el tamaño de la ventana de recepción de TCP para una conexión mediante la opción de socket **so de \_ RCVBUF** .
El tamaño de la ventana de recepción TCP para un socket puede aumentarse en cualquier momento mediante **\_ RCVBUF**, pero solo se puede reducir antes de establecer una conexión.
Para usar el escalado de ventanas, una aplicación debe especificar un tamaño de ventana superior a 65.535 bytes al usar la opción de socket for **\_ RCVBUF** antes de establecer la conexión.

El valor ideal para el tamaño de la ventana de recepción TCP suele ser difícil de determinar.
Con el fin de rellenar la capacidad de la red entre el remitente y el receptor, el tamaño de la ventana de recepción debe establecerse en el producto de retraso de ancho de banda para la conexión, que es el ancho de banda multiplicado por el tiempo de ida y vuelta.
Incluso si una aplicación puede determinar correctamente el producto de retraso de ancho de banda, todavía no se sabe la rapidez con la que la aplicación receptora recuperará datos del búfer de datos de entrada (velocidad de recuperación de la aplicación).
A pesar de la compatibilidad con el escalado de ventanas de TCP, el tamaño máximo de la ventana de recepción en Windows Server 2003 y Windows XP puede seguir limitando el rendimiento, ya que es un tamaño máximo fijo para todas las conexiones TCP (a menos que se especifique por aplicación mediante **\_ RCVBUF**), lo que puede mejorar el rendimiento de algunas conexiones y reducir el rendimiento de otras.
Además, el tamaño de la ventana de recepción máximo fijo para una conexión TCP no varía según las condiciones de red variables.

Para solucionar el problema de determinar correctamente el valor del tamaño máximo de la ventana de recepción de una conexión TCP en función de las condiciones actuales de la red, la pila TCP/IP de Windows Vista admite una característica de ajuste automático de la ventana de recepción.
Cuando esta característica está habilitada, el ajuste automático de la ventana de recepción determina continuamente el tamaño óptimo de la ventana de recepción real midiendo el producto de retraso de ancho de banda y la tasa de recuperación de la aplicación, y ajusta el tamaño de la ventana de recepción real máximo en función de las condiciones de red variables.
El ajuste automático de la ventana de recepción habilita la extensión WSopt de TCP de forma predeterminada, lo que permite un máximo de 16.776.960 bytes para el tamaño de ventana verdadero.
A medida que los datos fluyen a través de la conexión, la pila TCP/IP supervisa la conexión, mide el producto de retraso de ancho de banda actual para la conexión y la velocidad de recepción de la aplicación, y ajusta el tamaño de la ventana de recepción real para optimizar el rendimiento.
La pila TCP/IP cambia el valor del campo de ventana en el encabezado TCP en función de las condiciones de la red, ya que el factor de escala WSopt se fija cuando se establece la conexión por primera vez.

La pila TCP/IP en Windows Vista ya no usa los valores del registro **TcpWindowSize** .
Con un mejor rendimiento entre los pares TCP, el uso del ancho de banda de red aumenta durante la transferencia de datos.
Si todas las aplicaciones están optimizadas para recibir datos de TCP, el uso general de la red puede aumentar considerablemente, lo que permite que el uso de calidad de servicio (QoS) sea más importante en redes que funcionan a la vez o cerca de su capacidad.

El comportamiento predeterminado en Windows Vista para el almacenamiento en búfer de recepción cuando no se especifica el **modo de compatibilidad de SiO \_ set \_ \_** con **WsaBehaviorReceiveBuffering** es que no se permite ninguna reducción del tamaño de la ventana de recepción con la opción de socket de **\_ RCVBUF** después de establecer una conexión.

El comportamiento predeterminado en Windows Vista para el ajuste automático cuando no se especifica el **modo de compatibilidad de SiO \_ \_ \_ set** con **WsaBehaviorAutoTuning** es que la pila realizará el ajuste automático de la ventana con un factor de escala de ventana de 8.
Tenga en cuenta que si una aplicación establece un tamaño de ventana de recepción válido con la opción de socket **so de \_ RCVBUF** , la pila usará el tamaño especificado y se deshabilitará el ajuste automático de la recepción de ventanas.
El ajuste automático de Windows también se puede deshabilitar por completo con el siguiente comando, `netsh interface tcp set global autotuninglevel=disabled` , en cuyo caso la especificación de **WsaBehaviorAutoTuning** no tendrá ningún efecto.
La optimización de la recepción de ventanas también puede deshabilitarse en función de la Directiva de grupo establecida en Windows Server 2008.

La opción **WsaBehaviorAutoTuning** es necesaria en Windows Vista para algunos dispositivos de puerta de enlace de Internet y firewalls que no admiten correctamente flujos de datos para las conexiones TCP que usan la extensión WSopt y un factor de escala de Windows.
En Windows Vista, un receptor negocia de forma predeterminada un factor de escala de ventana de 8 para un tamaño de ventana máximo real de 16.776.960 bytes.
Cuando los datos empiezan a fluir en un vínculo rápido, Windows comienza inicialmente con un tamaño de ventana de 64 kilobytes true estableciendo el campo de ventana del encabezado TCP en 256 y estableciendo el factor de escala de la ventana en 8 en las opciones de TCP (256 * 2 ^ 8 = 64 KB).
Algunos firewalls y dispositivos de puerta de enlace a Internet omiten el factor de escala de ventana y solo examinan el campo de la ventana anunciada en el encabezado TCP especificado como 256 y colocan los paquetes entrantes para la conexión que contienen más de 256 bytes de datos TCP.
Para admitir el escalado de la ventana de recepción TCP, un dispositivo de puerta de enlace o firewall debe supervisar el protocolo de enlace TCP y realizar el seguimiento del factor de escala de ventana negociada como parte de los datos de conexión TCP.
Además, algunas aplicaciones y implementaciones de pila de TCP en otras plataformas omiten la extensión TCP WSopt y el factor de escala de ventana.
Por lo tanto, el host remoto que envía los datos puede enviar datos a la tarifa anunciada en el campo de ventana del encabezado TCP (256 bytes).
Esto puede dar lugar a que el receptor reciba datos muy lentamente.

Al establecer el miembro **BehaviorId** en **WsaBehaviorAutoTuning** y **TargetOsVersion** en Windows Vista, se reduce el factor de escala de la ventana a 2, por lo que el campo de ventana del encabezado TCP se establece inicialmente en 16.384 bytes y el factor de escala de la ventana se establece en 2 para un tamaño de recepción de ventana verdadero inicial de 64 KB.
La característica de ajuste automático de ventana puede aumentar el tamaño de recepción de la ventana real hasta 262.140 bytes si se establece el campo de ventana del encabezado TCP en 65.535 bytes.
Una aplicación debe establecer el **\_ modo de \_ compatibilidad \_ de SiO Set** en cuanto se crea un socket, ya que esta opción no tiene sentido o se aplica después de que se envíe un SYN.
La configuración de esta opción tiene el mismo impacto que el comando siguiente: `netsh interface tcp set global autotuninglevel=highlyrestricted`

Tenga en cuenta que el archivo de encabezado *Mswsockdef. h* se incluye automáticamente en *mswsock. h* o *Netiodef. h*, y no debe usarse directamente.

## <a name="see-also"></a>Vea también

[**tomacorriente**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
