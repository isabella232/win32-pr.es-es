---
description: Tema de navegación de los ioctl de socket de Windows Sockets (Winsock).
ms.assetid: 6a63c2c9-4e09-4a62-b39f-3ccb26287da8
title: IOCTLs de Winsock (Winsock2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7094f802b815bfbd7511bd67eb4e6b1767cb94
ms.sourcegitcommit: 392c0a56f99f4d19686e734291abcac887fc5ba2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/22/2021
ms.locfileid: "105649315"
---
# <a name="winsock-ioctls"></a>Ioctl de Winsock

En esta sección se describen los controles de entrada y salida (ioctl) de socket de Winsock para diversas ediciones de sistemas operativos Windows. Utilice la función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) o [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) para emitir un ioctl de Winsock para controlar el modo de un socket, el protocolo de transporte o el subsistema de comunicaciones.

Algunos ioctl de Winsock requieren más explicación de lo que puede transmitir esta tabla; Estas opciones contienen vínculos a temas adicionales.

Es posible adoptar un esquema de codificación que conserve los códigos de operación de [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) definidos actualmente y proporcione una manera cómoda de particionar el espacio del identificador de código de operación en tanto como el parámetro *dwIoControlCode* es ahora una entidad de 32 bits. El parámetro *dwIoControlCode* se crea para permitir la independencia del protocolo y del proveedor al agregar nuevos códigos de control al tiempo que se conserva la compatibilidad con versiones anteriores de los códigos de control de Windows sockets 1,1 y Unix. El parámetro *dwIoControlCode* tiene el formato siguiente.

| I  | O  | V  | T  | Familia de proveedores/direcciones | Código                   |
|-|-|-|-|-|-|
| 3  | 3  | 2  | 2 2 | 2 2 2 2 2 2 2 1 1 1 1 | 1 1 1 1 1 1              |
| 1  | 0  | 9  | 8 7 | 6 5 4 3 2 1 0 9 8 7 6 | 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 |

> [!Note] 
> Los bits del parámetro *dwIoControlCode* que se muestran en la tabla deben leerse verticalmente de arriba a abajo por columna. Por tanto, el bit de la izquierda es el bit 31, el siguiente bit es el bit 30 y el bit más a la derecha es el bit 0.

Se establece si el búfer de entrada es válido para el código, como con **IOC_IN**.

O se establece si el búfer de salida es válido para el código, como con **IOC_OUT**. Los códigos de control que usan los búferes de entrada y salida establecen I y O.

V se establece si no hay ningún parámetro para el código, como con **IOC_VOID**.

T es una cantidad de 2 bits que define el tipo de IOCTL. Se definen los valores siguientes:

0 el IOCTL es un código IOCTL de UNIX estándar, como con **FIONREAD** y **FIONBIO**.

1 el IOCTL es un código genérico de IOCTL de Windows Sockets 2. Los nuevos códigos de IOCTL definidos para Windows Sockets 2 tendrán T = = 1.

2 el IOCTL se aplica solo a una familia de direcciones específica.

3 el IOCTL se aplica solo a un proveedor de un proveedor específico, como con **IOC_VENDOR**. Este tipo permite a las compañías asignar un número de proveedor que aparece en el parámetro **Vendor/Address Family** . A continuación, el proveedor puede definir nuevos ioctl específicos para ese proveedor sin tener que registrar el IOCTL con un centro de activación, lo que proporciona la flexibilidad y la privacidad del proveedor.

**Familia de proveedores/direcciones** Una cantidad de 11 bits que define al proveedor que posee el código (si T = = 3) o que contiene la familia de direcciones a la que se aplica el código (si T = = 2). Si se trata de un código de IOCTL de UNIX (T = = 0), este parámetro tiene el mismo valor que el código de Unix. Si se trata de un IOCTL genérico de Windows Sockets 2 (T = = 1), este parámetro se puede usar como extensión del parámetro de código para proporcionar valores de código adicionales.

**Código** de La cantidad de 16 bits que contiene el código IOCTL específico para la operación.

## <a name="unix-ioctl-codes"></a>Códigos IOCTL de UNIX

Se admiten los siguientes códigos IOCTL de UNIX (comandos).

### <a name="fionbio"></a>FIONBIO

Habilitar o deshabilitar el modo sin bloqueo en socket *s*. El parámetro *lpvInBuffer* apunta a un **valor Long** (QoS) sin signo, que es distinto de cero si se va a habilitar el modo sin bloqueo y cero si se va a deshabilitar. Cuando se crea un socket, funciona en modo de bloqueo (es decir, el modo sin bloqueo está deshabilitado). Esto es coherente con los sockets BSD.

La rutina [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) o [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) establece automáticamente un socket en modo de no bloqueo. Si **WSAAsyncSelect** o **WSAEventSelect** se ha emitido en un socket, cualquier intento de usar [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para volver a establecer el socket en modo de bloqueo producirá un error con WSAEINVAL. Para volver a establecer el socket en modo de bloqueo, una aplicación debe deshabilitar primero **WSAAsyncSelect** llamando a **WSAAsyncSelect** con el parámetro *lEvent* igual a cero o deshabilitar **WSAEventSelect** llamando a **WSAEventSelect** con el parámetro *lNetworkEvents* igual a cero.

### <a name="fionread"></a>FIONREAD

Determine la cantidad de datos que se pueden leer de forma atómica desde socket *s*. El parámetro *lpvOutBuffer* apunta a una **longitud sin signo** en la que [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) almacena el resultado.

Si el socket que se pasa en el parámetro *s* está orientado a un flujo (por ejemplo, escriba sock \_ Stream), **FIONREAD** devuelve la cantidad total de datos que se pueden leer en una sola operación de recepción; esto suele ser el mismo que la cantidad total de datos en cola en el socket (puesto que un flujo de datos está orientado a bytes, no se garantiza).

Si el socket que se pasa en el parámetro *s* está orientado a mensajes (por ejemplo, escriba sock \_ DGRAM), **FIONREAD** devuelve el número total de bytes disponibles para la lectura, no el tamaño del primer datagrama (mensaje) en cola en el socket.

### <a name="siocatmark"></a>SIOCATMARK

Determine si se han leído todos los datos OOB. Esto se aplica solo a un socket de estilo de secuencia (por ejemplo, tipo SOCK \_ Stream) que se ha configurado para la recepción en línea de cualquier dato OOB (por lo que \_ OOBINLINE). Si no hay datos OOB en espera de ser leídos, la operación devuelve TRUE. De lo contrario, devuelve **false** y la siguiente operación de recepción realizada en el socket recuperará algunos o todos los datos que preceden a la marca; la aplicación debe usar la operación **SIOCATMARK** para determinar si queda alguna. Si hay datos normales que preceden a los datos urgentes (fuera de banda), se recibirán en orden. (Tenga en cuenta que las operaciones [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) nunca mezclarán datos OOB y normal en la misma llamada). *lpvOutBuffer* apunta a un booleano en el que [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) almacena el resultado.

## <a name="windows-sockets-2-commands"></a>Comandos de Windows Sockets 2

Se admiten los siguientes comandos de Windows Sockets 2.

### <a name="sio_acquire_port_reservation-opcode-setting-i-t3"></a>SIO_ACQUIRE_PORT_RESERVATION (configuración de OpCode: I, T = = 3)

Solicitar una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP. En el caso de las reservas de puerto en tiempo de ejecución, el grupo de puertos requiere que se consuman reservas del proceso en cuyo socket se concedió la reserva. Las reservas de puerto en tiempo de ejecución solo duran el tiempo que dure el socket en el que se llamó al método de [**adquisición de puerto de adquisición de SiO \_ \_ \_**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) . Por el contrario, cualquier proceso puede consumir reservas de Puerto persistentes creadas con la función [**CreatePersistentTcpPortReservation**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) con la capacidad de obtener reservas persistentes.

Para obtener información más detallada, consulte la referencia de la [**reserva de puerto de adquisición de SiO \_ \_ \_**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) .

[**SiO \_ La adquisición del \_ Puerto de \_ adquisición**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) es compatible con Windows Vista y versiones posteriores del sistema operativo.

### <a name="sio_address_list_change-opcode-setting-v-t1"></a>Cambio en la lista de direcciones de SIO \_ \_ \_ (configuración de OpCode: V, T = = 1)

Para recibir una notificación de los cambios en la lista de direcciones de transporte locales de la familia de protocolos del socket a la que se puede enlazar la aplicación. No se proporcionará información de salida tras la finalización de este IOCTL; la finalización indica simplemente que la lista de direcciones locales disponibles ha cambiado y se debe consultar de nuevo a través de la consulta de la **\_ lista de direcciones de \_ \_ SiO**.

Se supone (aunque no es necesario) que la aplicación utiliza e/s superpuestas para recibir notificaciones de cambio mediante la finalización de la solicitud de cambio de la **\_ lista de direcciones de \_ \_ SiO** . Como alternativa, si la **lista de direcciones de SiO \_ \_ \_ cambia** ioctl se emite en un socket que no es de bloqueo y sin parámetros superpuestos (*lpOverlapped* /  *lpCompletionRoutine* se establecen en **null**), se completará inmediatamente con el error [WSAEWOULDBLOCK](windows-sockets-error-codes-2.md). A continuación, la aplicación puede esperar los eventos de cambio de la lista de direcciones a través de una llamada a [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) o [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) con \_ \_ \_ el bit de cambio de lista de direcciones de FD en la máscara de bits de eventos de red.

### <a name="sio_address_list_query-opcode-setting-o-t1"></a>\_Consulta de la lista de direcciones de SiO \_ \_ (configuración de OpCode: O, T = = 1)

Obtiene una lista de direcciones de transporte locales de la familia de protocolos del socket a la que se puede enlazar la aplicación. La lista de direcciones varía en función de la familia de direcciones y algunas direcciones se excluyen de la lista.

> [!Note] 
> En los entornos de plug-n-Play de Windows, las direcciones se pueden agregar y quitar de forma dinámica. Por lo tanto, las aplicaciones no pueden basarse en la información devuelta por la consulta de lista de direcciones de SiO para ser persistentes. **\_ \_ \_** Las aplicaciones pueden registrarse para recibir notificaciones de cambio de dirección a través del cambio de la lista de direcciones de SiO que proporciona la notificación a través de un evento de cambio de lista de direcciones de e/s o FD superpuesto **\_ \_ \_** \_ \_ \_ . Se puede usar la siguiente secuencia de acciones para garantizar que la aplicación tenga siempre información de lista de direcciones actual:

-  Problema **de \_ \_ \_ cambio** en la lista de direcciones de SiO ioctl
-  Emitir **\_ consulta de \_ lista \_ de direcciones de SiO** ioctl
-  Cada vez que el cambio de la lista de direcciones de SiO envía una notificación a la aplicación del cambio en la lista de direcciones (ya sea a través de e/s superpuesta o por evento de cambio de lista de **\_ \_ \_** \_ direcciones FD \_ \_ ), se debe repetir la secuencia de acciones completa.

Para obtener información más detallada, consulte la referencia de consulta de la [**\_ lista de direcciones de \_ \_ SiO**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) . **SiO \_ La \_ \_ consulta** de la lista de direcciones es compatible con Windows 2000 y versiones posteriores.

### <a name="sio_apply_transport_setting-opcode-setting-i-t3"></a>SIO \_ aplicar \_ configuración de transporte \_ (configuración de OpCode: I, T = = 3)

Aplica una configuración de transporte a un socket. La configuración de transporte que se está aplicando se basa en el [**\_ \_ identificador de configuración de transporte**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) que se ha pasado en el parámetro *lpvInBuffer* .

La única configuración de transporte que define actualmente es para la funcionalidad de **\_ notificación en tiempo \_ \_ real** en un socket TCP.

Si el [**\_ \_ ID. de configuración de transporte**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) que se ha pasado tiene el miembro **GUID** establecido en funcionalidad de **\_ \_ notificación \_ en tiempo real**, se trata de una solicitud para aplicar la configuración de notificación en tiempo real para el socket TCP que se usa con la [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) para recibir notificaciones de red en segundo plano en una aplicación de la tienda Windows.

Para obtener información más detallada, consulte la referencia de configuración de transporte de la [**\_ aplicación \_ \_ SiO**](/previous-versions/windows/desktop/legacy/jj553481(v=vs.85)) . **SiO \_ La \_ \_ configuración de aplicar transporte** es compatible con Windows 8, Windows Server 2012 y versiones posteriores.

### <a name="sio_associate_handle-opcode-setting-i-t1"></a>SIO \_ identificador de asociación \_ (configuración de OpCode: I, T = = 1)

Asocie este socket al identificador (handle) especificado de la interfaz correspondiente. El búfer de entrada contiene el valor entero que corresponde a la constante de manifiesto para la interfaz complementaria (por ejemplo, \_ NETDEV y TH \_ TAPI.), seguido de un valor que es un identificador de la interfaz complementaria especificada, junto con cualquier otra información necesaria. Consulte la sección correspondiente en los [anexos de Winsock](winsock-annexes.md) para obtener detalles específicos de una determinada interfaz del complemento. El tamaño total se refleja en la longitud del búfer de entrada. No se requiere ningún búfer de salida. El código de error [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) se indica para los proveedores de servicios que no admiten este ioctl. El identificador asociado a este IOCTL se puede recuperar mediante **el \_ \_ identificador SiO translate**.

Se puede usar una interfaz complementaria, por ejemplo, si un proveedor determinado proporciona (1) una gran cantidad de controles adicionales sobre el comportamiento de un socket y (2) los controles son lo suficientemente específicos del proveedor que no se asignan a las funciones de Windows socket existentes o que probablemente se definirán en el futuro. Se recomienda usar el modelo de objetos componentes (COM) en lugar de este IOCTL para detectar y realizar el seguimiento de otras interfaces que podrían ser compatibles con un socket. Este IOCTL está presente para la compatibilidad (inversa) con sistemas en los que COM no está disponible o no se puede usar por algún otro motivo.

### <a name="sio_associate_port_reservation-opcode-setting-i-t3"></a>SIO \_ asociar \_ reserva de puerto \_ (configuración de OpCode: I, T = = 3)

Asociar un socket con una reserva persistente o en tiempo de ejecución para un bloque de puertos TCP o UDP identificados por el token de reserva de puerto. Se debe emitir el ioctl de reserva de puertos de Asociación de la [**\_ Asociación \_ \_**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) para que el socket esté enlazado. Si y cuando se enlaza el socket, el puerto asignado a él se seleccionará en la reserva de Puerto identificada por el token especificado. Si no hay puertos disponibles en la reserva especificada, se producirá un error en la llamada a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) .

Para obtener información más detallada, consulte la referencia de la [**reserva de puerto de Asociación de SiO \_ \_ \_**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) .

[**SiO \_ En \_ \_**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) Windows Vista y versiones posteriores del sistema operativo se admite la reserva de puertos asociada.

### <a name="sio_base_handle-opcode-setting-o-t1"></a>\_Identificador base \_ de sio (configuración de OpCode: O, T = = 1)

Recupera el identificador del proveedor de servicios base para un socket determinado. El valor devuelto es un **socket**.

Un proveedor de servicios por niveles nunca interceptaría este IOCTL, ya que el valor devuelto debe ser el identificador de socket del proveedor de servicios base.

Si el búfer de salida no es suficientemente grande para un identificador de socket ( *cbOutBuffer* es menor que el tamaño de un **socket**) o el parámetro *lpvOutBuffer* es un puntero **nulo** , se devuelve un **\_ error de socket** como resultado de este ioctl y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [WSAEFAULT](windows-sockets-error-codes-2.md).

**SiO \_ El \_ identificador base** se define en el archivo de encabezado *mswsock. h* y se admite en Windows Vista y versiones posteriores.

### <a name="sio_bsp_handle-opcode-setting-o-t1"></a>\_Identificador del BSP \_ de sio (configuración de OpCode: O, T = = 1)

Recupera el identificador del proveedor de servicios base para un socket utilizado por la función [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) . El valor devuelto es un **socket**.

Este ioctl lo usa un proveedor de servicios por niveles para asegurarse de que el proveedor intercepta la función [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .

Si el búfer de salida no es suficientemente grande para un identificador de socket ( *cbOutBuffer* es menor que el tamaño de un **socket**) o el parámetro *lpvOutBuffer* es un puntero **nulo** , se devuelve un **\_ error de socket** como resultado de este ioctl y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [WSAEFAULT](windows-sockets-error-codes-2.md).

**SiO \_ El \_ identificador de BSP** se define en el archivo de encabezado *mswsock. h* y se admite en Windows Vista y versiones posteriores.

### <a name="sio_bsp_handle_select-opcode-setting-o-t1"></a>\_ \_ \_ Operación de selección de controlador de BSP de sio (configuración de OpCode: O, T = = 1)

Recupera el identificador del proveedor de servicios base para un socket utilizado por la función [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) . El valor devuelto es un **socket**.

Un proveedor de servicios por niveles utiliza este ioctl para asegurarse de que el proveedor intercepte la función [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) .

Si el búfer de salida no es suficientemente grande para un identificador de socket ( *cbOutBuffer* es menor que el tamaño de un **socket**) o el parámetro *lpvOutBuffer* es un puntero **nulo** , se devuelve un **\_ error de socket** como resultado de este ioctl y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [WSAEFAULT](windows-sockets-error-codes-2.md).

**SiO \_ La \_ \_ selección de identificador BSP** se define en el archivo de encabezado *mswsock. h* y se admite en Windows Vista y versiones posteriores.

### <a name="sio_bsp_handle_poll-opcode-setting-o-t1"></a>El \_ \_ \_ sondeo de control de el BSP de sio (configuración de OpCode: O, T = = 1)

Recupera el identificador del proveedor de servicios base para un socket utilizado por la función [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) . El parámetro *lpOverlapped* debe ser un puntero **nulo** . El valor devuelto es un **socket**.

Este ioctl lo usa un proveedor de servicios por niveles para asegurarse de que el proveedor intercepta la función [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .

Si el búfer de salida no es suficientemente grande para un identificador de socket ( *cbOutBuffer* es menor que el tamaño de un **socket**), el parámetro *lpvOutBuffer* es un puntero **nulo** , o el parámetro *lpOverlapped* no es un puntero **nulo** , se devuelve un **\_ error de socket** como resultado de este ioctl y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [WSAEFAULT](windows-sockets-error-codes-2.md).

**SiO \_ El \_ \_ sondeo de identificador de BSP** se define en el archivo de encabezado *mswsock. h* y se admite en Windows Vista y versiones posteriores.

### <a name="sio_chk_qos-opcode-setting-i-o-t3"></a>SIO \_ CHK \_ QoS (configuración de OpCode: I, O, T = = 3)

Recupera información sobre las características de tráfico de QoS. Durante la fase de transición del sistema de envío entre la configuración de Flow y la recepción de un mensaje RESV (vea [cómo el servicio RSVP invoca TC](/previous-versions/windows/desktop/qos/how-the-rsvp-service-invokes-tc) para obtener más información sobre la fase de transición), el tráfico asociado a un flujo RSVP se basa en el tipo de servicio ([mejor esfuerzo](/previous-versions/windows/desktop/qos/best-effort), [carga controlada](/previous-versions/windows/desktop/qos/controlled-load)o [garantizado](/previous-versions/windows/desktop/qos/guaranteed)). Para obtener más información, vea [usar \_ el \_ QoS de SiO CHK](/previous-versions/windows/desktop/qos/using-sio-chk-qos) en la sección [calidad de servicio](/previous-versions/windows/desktop/qos/qos-start-page) del SDK de la plataforma.

### <a name="sio_cpu_affinity-opcode-setting-i-t3"></a>SIO_CPU_AFFINITY (configuración de OpCode: I, T = = 3)

Habilita la paralelización de indicación de recepción y uso compartido de puertos. Cuando la aplicación usa esta opción de socket para asociar Sockets a diferentes procesadores y, a continuación, enlaza los sockets a la misma dirección, las indicaciones de recepción se distribuirán entre los sockets según el hash de ajuste de escala en lado de recepción (RSS). La configuración de RSS no cambia, por lo que cualquier flujo determinado (punto de conexión local, par de punto de conexión remoto) siempre se indicará en el mismo procesador. Como resultado, todos los paquetes que pertenecen a un flujo determinado se indicarán en el mismo Socket. Se debe llamar a este IOCTL antes de enlazar; de lo contrario, se devolverá WSAEINVAL. El búfer de entrada es un índice de procesador (basado en 0) de tipo USHORT. IOCTL no es compatible con SO_REUSEADDR y SO_REUSE_MULTICASTPORT. Solo se admite para sockets UDP.

> [!NOTE]
> Si tiene como destino la versión 10.0.19041.0 (Windows 10, versión 2004) de la Windows SDK, use el valor `0x98000015` en lugar del nombre **SIO_CPU_AFFINITY**.

### <a name="sio_enable_circular_queueing-opcode-setting-v-t1"></a>SIO \_ habilitar \_ la \_ puesta en cola circular (configuración de OpCode: V, T = = 1)

Indica al proveedor de servicios subyacente orientado a mensajes que un mensaje recién recibido nunca se debe quitar debido a un desbordamiento de la cola de búfer. En su lugar, se debe eliminar el mensaje más antiguo de la cola para dar cabida al mensaje recién llegado. No se requieren búferes de entrada y salida. Tenga en cuenta que este IOCTL solo es válido para Sockets asociados a protocolos no confiables orientados a mensajes. El código de error [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) se indica para los proveedores de servicios que no admiten este ioctl.

### <a name="sio_find_route-opcode-setting-o-t1"></a>SIO \_ Buscar \_ ruta (configuración de OpCode: O, T = = 1)

Cuando se emite, este IOCTL solicita que se detecte la ruta a la dirección remota especificada como [**sockaddr**](sockaddr-2.md) en el búfer de entrada. Si la dirección ya existe en la memoria caché local, su entrada se invalida. En el caso de IPX de Novell, esta llamada inicia un GetLocalTarget de IPX (GLT), que consulta la dirección remota especificada en la red.

### <a name="sio_flush-opcode-setting-v-t1"></a>SIO \_ Flush (configuración de OpCode: V, T = = 1)

Descarta el contenido actual de la cola de envío asociada a este socket. No se requieren búferes de entrada y salida. El código de error [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) se indica para los proveedores de servicios que no admiten este ioctl.

### <a name="sio_get_broadcast_address-opcode-setting-o-t1"></a>SIO \_ obtener \_ dirección de difusión \_ (configuración de OpCode: O, T = = 1)

Este ioctl rellena el búfer de salida con una estructura [sockaddr](sockaddr-2.md) que contiene una dirección de difusión adecuada para su uso con [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) /  [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto). Este IOCTL no es compatible con los sockets IPv6 y devuelve el código de error [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) .

### <a name="sio_get_extension_function_pointer-opcode-setting-o-i-t1"></a>SIO \_ obtener \_ \_ puntero de función \_ de extensión (configuración de OpCode: O, I, T = = 1)

Recupera un puntero a la función de extensión especificada admitida por el proveedor de servicios asociado. El búfer de entrada contiene un identificador único global (**GUID**) cuyo valor identifica la función de extensión en cuestión. El puntero a la función deseada se devuelve en el búfer de salida. Los identificadores de función de extensión los establecen los proveedores de proveedores de servicios y deben incluirse en la documentación del proveedor que describe las capacidades y la semántica de la función de extensión.

Los valores GUID de las funciones de extensión admitidos por el proveedor de servicios TCP/IP de Windows se definen en el archivo de encabezado *mswsock. h* . El valor posible para estos GUID es el siguiente:

| Término                                                                                                                | Descripción                                                                               |
|-|-|
| <span id="WSAID_ACCEPTEX"></span><span id="wsaid_acceptex"></span>WSAID \_ ACCEPTEX<br/>                                     | La función de extensión [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) .<br/>                         |
| <span id="WSAID_CONNECTEX"></span><span id="wsaid_connectex"></span>WSAID \_ CONNECTEX<br/>                                  | La función de extensión [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) . <br/>                      |
| <span id="WSAID_DISCONNECTEX"></span><span id="wsaid_disconnectex"></span>WSAID \_ DISCONNECTEX<br/>                         | La función de extensión [**DisconnectEx**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) . <br/>                |
| <span id="WSAID_GETACCEPTEXSOCKADDRS"></span><span id="wsaid_getacceptexsockaddrs"></span>WSAID \_ GETACCEPTEXSOCKADDRS<br/> | La función de extensión [**GetAcceptExSockaddrs**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs) .<br/> |
| <span id="WSAID_TRANSMITFILE"></span><span id="wsaid_transmitfile"></span>WSAID \_ TRANSMITFILE<br/>                         | La función de extensión [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile) .<br/>                 |
| <span id="WSAID_TRANSMITPACKETS"></span><span id="wsaid_transmitpackets"></span>WSAID \_ TRANSMITPACKETS<br/>                | La función de extensión [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) . <br/>          |
| <span id="WSAID_WSARECVMSG"></span><span id="wsaid_wsarecvmsg"></span>WSAID \_ WSARECVMSG<br/>                               | La función de extensión [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .<br/>                     |
| <span id="WSAID_WSASENDMSG"></span><span id="wsaid_wsasendmsg"></span>WSAID \_ WSASENDMSG<br/>                               | La función de extensión [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) . <br/>                      |

### <a name="sio_get_group_qos-opcode-setting-o-i-t1"></a>SIO \_ obtener \_ QoS de grupo \_ (configuración de OpCode: O, I, T = = 1)

Reservado para uso futuro con Sockets.

Recupera la estructura de [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) asociada al grupo de sockets al que pertenece este socket. El búfer de entrada es opcional. Algunos protocolos (por ejemplo, RSVP) permiten usar el búfer de entrada para calificar una solicitud de calidad de servicio. La estructura de **QoS** se copiará en el búfer de salida. Si este socket no pertenece a un grupo de sockets adecuado, los miembros **SendingFlowspec** y **ReceivingFlowspec** de la estructura de **QoS** devuelta se establecen en **null**. El código de error [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) se indica para los proveedores de servicios que no admiten la calidad de servicio.

### <a name="sio_get_interface_list-opcode-setting-o-t0"></a>SIO \_ Get \_ interface \_ List (configuración de OpCode: O, T = = 0)

Devuelve una lista de interfaces IP configuradas y sus parámetros como una matriz de estructuras de [**\_ información de interfaz**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) .

> [!Note]  
> La compatibilidad de este comando es obligatoria para los proveedores de servicios TCP/IP compatibles con Windows Sockets 2.

El parámetro *lpvOutBuffer* apunta al búfer en el que se va a almacenar la información sobre las interfaces como una matriz de estructuras de [**\_ información de interfaz**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) para las direcciones IP de unidifusión en las interfaces. El parámetro *cbOutBuffer* especifica la longitud del búfer de salida. El número de interfaces devueltas (el número de estructuras devueltas en el búfer señalado por el parámetro *lpvOutBuffer* ) se puede determinar en función de la longitud real del búfer de salida devuelto en el parámetro *lpcbBytesReturned* .

Si se llama a la función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) con la lista de interfaces de la obtención de SiO y el miembro de nivel del parámetro socket *s* no está definido como **IPPROTO \_ IP**, se devuelve **WSAEINVAL** . **\_ \_ \_** Una llamada a la función **WSAIoctl** con **SiO \_ Get \_ interface \_ List** devuelve **WSAEFAULT** si el parámetro *cbOutBuffer* que especifica la longitud del búfer de salida es demasiado pequeño y recibe la lista de interfaces configuradas.

**SiO \_ GET \_ interface \_ List** es compatible con Windows Me/98 y Windows NT 4,0 con SP4 y versiones posteriores.

### <a name="sio_get_interface_list_ex-opcode-setting-o-t0"></a>SIO \_ Get \_ interface \_ List \_ ex (configuración de OpCode: O, T = = 0)

Reservado para uso futuro con Sockets.

Devuelve una lista de interfaces IP configuradas y sus parámetros como una matriz de estructuras de [**información de interfaz \_ \_ ex**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex) .

El parámetro *lpvOutBuffer* apunta al búfer en el que se va a almacenar la información sobre las interfaces como una matriz de estructuras de [**información de interfaz \_ \_ ex**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex) para las direcciones IP de unidifusión en la interfaz. El parámetro *cbOutBuffer* especifica la longitud del búfer de salida. El número de interfaces devueltas (el número de estructuras devueltas en *lpvOutBuffer*) se puede determinar en función de la longitud real del búfer de salida devuelto en el parámetro *lpcbBytesReturned* .

**SiO \_ GET \_ interface \_ List \_ ex** no se admite actualmente en Windows.

### <a name="sio_get_qos-opcode-setting-o-t1"></a>SIO \_ obtener \_ QoS (configuración de OpCode: O, T = = 1)

Reservado para uso futuro con Sockets. Recupera la estructura de [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) asociada al socket. El búfer de entrada es opcional. Algunos protocolos (por ejemplo, RSVP) permiten usar el búfer de entrada para calificar una solicitud de calidad de servicio. La estructura de **QoS** se copiará en el búfer de salida. El tamaño del búfer de salida debe ser lo suficientemente grande como para poder contener la estructura completa de **QoS** . El código de error [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) se indica para los proveedores de servicios que no admiten la calidad de servicio.

Es posible que un remitente no llame a la operación **SiO \_ Get \_ QoS** hasta que el socket esté conectado.

Un receptor puede llamar a **SiO \_ obtener \_ QoS** en cuanto está enlazado.

### <a name="sio_ideal_send_backlog_change-opcode-setting-v-t0"></a>SIO \_ el \_ cambio de trabajo pendiente de envío ideal \_ \_ (configuración de OpCode: V, T = = 0)

Notifica a una aplicación cuando cambia el valor de trabajo pendiente de envío (ISB) ideal para la conexión subyacente.

Al enviar datos a través de una conexión TCP mediante Windows Sockets, es importante mantener una cantidad suficiente de datos pendientes (enviados pero no confirmados todavía) en TCP para lograr el máximo rendimiento. El valor ideal para la cantidad de datos pendientes para lograr el mejor rendimiento para la conexión TCP se denomina el tamaño de trabajo pendiente de envío (ISB) ideal. El valor de ISB es una función del producto de retraso de ancho de banda de la conexión TCP y la ventana de recepción anunciada del receptor (y, en parte, de la cantidad de congestión de la red).

El valor de ISB por conexión está disponible en la implementación del protocolo TCP en Windows Server 2008, Windows Vista con SP1 y versiones posteriores del sistema operativo. La aplicación puede usar el ioctl de **\_ \_ \_ \_ cambio de trabajo pendiente de envío ideal de SiO** para recibir una notificación cuando el valor de ISB Cambie dinámicamente para una conexión.

Para obtener información más detallada, consulte la referencia de [**\_ \_ \_ \_ cambio del trabajo pendiente de envío de SiO**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85)) .

[**SiO \_ Se admite el \_ \_ \_ cambio de trabajo pendiente de envío ideal**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85)) en Windows Server 2008, Windows Vista con SP1 y versiones posteriores del sistema operativo.

### <a name="sio_ideal_send_backlog_query-opcode-setting-o-t0"></a>SIO \_ la \_ \_ consulta de trabajo pendiente de envío ideal \_ (configuración de OpCode: O, T = = 0)

Recupera el valor de registro de envío (ISB) ideal para la conexión subyacente.

Al enviar datos a través de una conexión TCP mediante Windows Sockets, es importante mantener una cantidad suficiente de datos pendientes (enviados pero no confirmados todavía) en TCP para lograr el máximo rendimiento. El valor ideal para la cantidad de datos pendientes para lograr el mejor rendimiento para la conexión TCP se denomina el tamaño de trabajo pendiente de envío (ISB) ideal. El valor de ISB es una función del producto de retraso de ancho de banda de la conexión TCP y la ventana de recepción anunciada del receptor (y, en parte, de la cantidad de congestión de la red).

El valor de ISB por conexión está disponible en la implementación del protocolo TCP en Windows Server 2008 y versiones posteriores. Una aplicación puede usar el ioctl de **\_ \_ \_ \_ consulta de trabajo pendiente de envío ideal de SiO** para consultar el valor de ISB para una conexión.

Para obtener información más detallada, consulte la referencia de [**\_ consulta de envío de \_ \_ trabajo pendiente \_ de la opción SiO ideal**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85)) .

[**SiO \_ La \_ \_ \_ consulta de trabajo pendiente de envío ideal**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85)) es compatible con Windows Server 2008, Windows Vista con SP1 y versiones posteriores del sistema operativo.

### <a name="sio_keepalive_vals-opcode-setting-i-t3"></a>SIO \_ KEEPALIVE \_ Vals (configuración de OpCode: I, T = = 3)

Habilita o deshabilita el valor por conexión de la opción **Keep-Alive** de TCP, que especifica el tiempo de espera y el intervalo de mantenimiento de conexiones TCP. Para obtener más información acerca de la opción Keep-Alive, consulte la sección 4.2.3.6 sobre los *requisitos de los hosts de Internet: las capas de comunicación* especificadas en RFC 1122 están disponibles en el [sitio web de IETF](https://www.ietf.org/rfc/rfc1122.txt). (Este recurso solo está disponible en inglés).

**SiO \_ KEEPALIVE \_ vals** se puede usar para habilitar o deshabilitar sondeos Keep-Alive y establecer el intervalo y el tiempo de espera de mantenimiento de conexión. El tiempo de espera de Keep-Alive especifica el tiempo de espera, en milisegundos, sin actividad hasta que se envía el primer paquete Keep-Alive. El intervalo Keep-Alive especifica el intervalo, en milisegundos, entre el momento en que se envían los paquetes Keep-Alive sucesivos Si no se recibe ninguna confirmación.

La opción [**para \_ KEEPALIVE**](so-keepalive.md) , que es una de las [Opciones de socket de \_ socket sol](sol-socket-socket-options.md), también puede usarse para habilitar o deshabilitar TCP Keep-Alive en una conexión, así como para consultar el estado actual de esta opción. Para consultar si TCP Keep-Alive está habilitado en un socket, se puede llamar a la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) con la opción **para \_ KEEPALIVE** . Para habilitar o deshabilitar TCP Keep-Alive, se puede llamar a [**la función de llamada con la opción**](/windows/desktop/api/winsock/nf-winsock-setsockopt) [**\_ KEEPALIVE**](so-keepalive.md) . Si TCP Keep-Alive está habilitado con la opción **\_ KeepAlive**, se usará la configuración predeterminada de TCP para el tiempo de espera de mantenimiento de conexión y el intervalo, a menos que estos valores se hayan cambiado mediante **SiO \_ KEEPALIVE \_ vals**.

Para obtener información más detallada, consulte la referencia de [**SiO \_ KEEPALIVE \_ vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) . **SiO \_ KEEPALIVE \_ vals** es compatible con Windows 2000 y versiones posteriores.

### <a name="sio_loopback_fast_path-opcode-setting-i-t3"></a>\_Ruta de acceso rápido de bucle invertido de SiO \_ \_ (configuración de OpCode: I, T = = 3)

Configura un socket TCP para una menor latencia y operaciones más rápidas en la interfaz de bucle invertido. Este IOCTL solicita que la pila TCP/IP use una ruta de acceso rápida especial para las operaciones de bucle invertido en este socket. La [**\_ ruta de \_ \_ acceso rápido de bucle invertido de SiO**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) solo se puede usar con Sockets TCP. Este IOCTL debe usarse en ambos lados de la sesión de bucle invertido. La ruta de acceso rápido de bucle invertido TCP se admite mediante la interfaz de bucle invertido IPv4 o IPv6. De forma predeterminada, el valor de la **\_ ruta de \_ \_ acceso rápido de los bucles de SiO** es

Para obtener información más detallada, consulte la referencia de la [**\_ ruta de \_ \_ acceso rápida de los bucles de SiO**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) . **SiO \_ La \_ \_ ruta de acceso rápido de bucle invertido** es compatible con Windows 8, Windows Server 2012 y versiones posteriores.

### <a name="sio_multipoint_loopback-opcode-setting-v-t1"></a>SIO \_ Multipoint \_ loopback (configuración de OpCode: V, T = = 1)

Controla si los datos enviados por una aplicación en el equipo local (no necesariamente por el mismo socket) en una sesión de multidifusión se recibirán mediante un socket unido al grupo de destino de multidifusión en la interfaz de bucle invertido. Un valor de **true** hace que los datos de multidifusión enviados por una aplicación en el equipo local se entreguen a un socket de escucha en la interfaz de bucle invertido. Un valor de **false** evita que los datos de multidifusión enviados por una aplicación en el equipo local se entreguen a un socket de escucha en la interfaz de bucle invertido. De forma predeterminada, el **\_ \_ bucle invertido de Multipoint** está habilitado.

### <a name="sio_multicast_scope-opcode-setting-i-t1"></a>El \_ ámbito de multidifusión de SiO \_ (configuración de OpCode: I, T = = 1)

Especifica el ámbito en el que se realizarán las transmisiones de multidifusión. El ámbito se define como el número de segmentos de red enrutados que se van a cubrir. Un ámbito de cero indicaría que la transmisión por multidifusión no se colocaría en la conexión, pero podría diseminarse a través de sockets dentro del host local. Un valor de ámbito de uno (valor predeterminado) indica que la transmisión se colocará en la conexión, pero no cruzará ningún enrutador. Los valores de ámbito más altos determinan el número de enrutadores que se pueden cruzar. Tenga en cuenta que esto corresponde al parámetro Time-to-Live (TTL) de la multidifusión IP. De forma predeterminada, el ámbito es 1.

### <a name="sio_query_rss_processor_info-opcode-setting-o-t1"></a>\_Información del procesador de RSS de consulta SiO \_ \_ \_ (configuración de OpCode: O, T = = 1)

Consulta la asociación entre un socket y un nodo principal y NUMA del procesador de RSS.

La [**\_ información del \_ \_ procesador de \_ RSS de la consulta SiO**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) devuelve una estructura de [**\_ \_ afinidad del procesador de sockets**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) que contiene el [**\_ número de procesador**](/windows/win32/api/winnt/ns-winnt-processor_number) y el identificador de nodo Numa. La estructura **del \_ número de procesador** devuelto contiene un número de grupo y un número de procesador relativo dentro del grupo.

Para obtener información más detallada, consulte la referencia de la [**\_ \_ \_ \_ información del procesador RSS de la consulta SiO**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) . **SiO \_ La \_ \_ \_ información del procesador de RSS de consulta** es compatible con Windows 8, Windows Server 2012 y versiones posteriores.

### <a name="sio_query_rss_scalability_info-opcode-setting-o-t3"></a>\_Información de \_ escalabilidad RSS de consulta SiO \_ \_ (configuración de OpCode: O, T = = 3)

Consultas descarga interfaces para la funcionalidad de ajuste de escala en lado de recepción (RSS). La estructura de argumentos devuelta para la **\_ \_ \_ \_ información de escalabilidad RSS de consulta SiO** se especifica en la estructura de **\_ \_ información de escalabilidad RSS** definida en el archivo de encabezado *Mstcpip. h* . Esta estructura se define de la siguiente manera:

```cpp
// Scalability info for the transport
typedef struct _RSS_SCALABILITY_INFO {
   BOOLEAN RssEnabled;
} RSS_SCALABILITY_INFO, *PRSS_SCALABILITY_INFO;
```

El valor devuelto en el miembro **RssEnabled** indica si RSS está habilitado en al menos una interfaz.

Si el búfer de salida no es suficientemente grande para la estructura de **\_ \_ información de escalabilidad de RSS** (el valor de *cbOutBuffer* es menor que el tamaño de una **\_ \_ información de escalabilidad RSS**) o el parámetro *LpvOutBuffer* es un puntero **nulo** , se devuelve un **\_ error de socket** como resultado de este ioctl y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [WSAEINVAL](windows-sockets-error-codes-2.md).

En las redes de alta velocidad en las que varias CPU residen dentro de un solo sistema, la capacidad de la pila del Protocolo de red para escalar correctamente en un sistema de varias CPU se obstaculiza porque la arquitectura de NDIS 5,1 y versiones anteriores limita el procesamiento de protocolos a una única CPU. El ajuste de escala en lado de recepción (RSS) resuelve este problema al permitir que la carga de red de un adaptador de red se equilibre en varias CPU.

**SiO \_ La \_ \_ \_ información de escalabilidad de RSS de consulta** se admite en Windows Vista y versiones posteriores.

### <a name="sio_query_transport_setting-opcode-setting-i-t3"></a>\_Opción de transporte de consulta SiO \_ \_ (configuración de OpCode: I, T = = 3)

Consulta la configuración de transporte en un socket. La configuración de transporte que se consulta se basa en el [**\_ \_ identificador de configuración de transporte**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) que se ha pasado en el parámetro *lpvInBuffer* .

La única configuración de transporte que define actualmente es para la funcionalidad de **\_ notificación en tiempo \_ \_ real** en un socket TCP.

Si el [**\_ \_ identificador de configuración de transporte**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) tiene el miembro **GUID** establecido en **\_ \_ \_ funcionalidad de notificación en tiempo real**, se trata de una solicitud para consultar la configuración de notificación en tiempo real para el socket TCP que se usa con la [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) para recibir notificaciones de red en segundo plano en una aplicación de la tienda Windows. Si la llamada a [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) o [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) es correcta, este ioctl devuelve una estructura de [**salida de configuración de \_ notificación en tiempo \_ \_ \_ real**](/windows/desktop/api/Mstcpip/ns-mstcpip-real_time_notification_setting_input) con el estado actual.

Para obtener información más detallada, consulte la referencia de configuración de transporte de la [**\_ consulta \_ \_ SiO**](/previous-versions/windows/desktop/legacy/jj553483(v=vs.85)) . **SiO \_ La \_ \_ configuración de transporte de consultas** se admite en Windows 8, Windows Server 2012 y versiones posteriores.

### <a name="sio_query_wfp_ale_endpoint_handle-opcode-setting-o-t3"></a>SIO \_ query \_ \_ identificador de extremo Ale de WFP \_ \_ (configuración de OpCode: O, T = = 3)

Consulta el identificador del extremo de cumplimiento de la capa de aplicación (ALE).

La plataforma de filtrado de Windows (WFP) admite la inspección y modificación del tráfico de red. En Windows Vista, WFP se centra en escenarios en los que el equipo host es el punto de conexión de comunicación. En Windows Server 2008, sin embargo, hay implementaciones de firewall perimetral que desean aprovechar la plataforma WFP para inspeccionar el tráfico de paso a través y proxy. El servidor de Internet Security and Acceleration (ISA) es un ejemplo de este tipo de dispositivo perimetral.

Hay algunos escenarios de firewall que pueden requerir la capacidad de insertar un paquete de entrada en la ruta de acceso de envío asociada a un punto de conexión existente. Debe haber un mecanismo para detectar el identificador de extremo de la capa de transporte asociado al punto de conexión de destino. La aplicación que creó el extremo posee estos extremos de capa de transporte. Este IOCTL se usa para proporcionar el identificador de socket a la asignación de identificadores de punto de conexión de la capa de transporte.

Si el búfer de salida no es suficientemente grande para el identificador del punto de conexión ( *cbOutBuffer* es menor que el tamaño de un **UINT64**) o el parámetro *lpvOutBuffer* es un puntero **nulo** , se devuelve un **\_ error de socket** como resultado de este ioctl y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [WSAEINVAL](windows-sockets-error-codes-2.md).

**SiO \_ En Windows Vista y versiones posteriores se admite el \_ \_ identificador del punto de \_ conexión \_ Ale de WFP** .

### <a name="sio_query_wfp_connection_redirect_context-opcode-setting-i-t3"></a>SIO \_ query \_ \_ contexto de \_ redireccionamiento de conexión de WFP \_ (configuración de OpCode: I, T = = 3)

Consulta el contexto de redirección para un registro de redireccionamiento usado por un servicio de redirección de la plataforma de filtrado de Windows (WFP).

El [**\_ contexto de \_ \_ \_ redirección \_ de conexión WFP de la consulta SiO**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) se usa para proporcionar un seguimiento de la conexión de proxy en las conexiones de socket redirigido. Esta característica de WFP facilita el seguimiento de los registros de redireccionamiento de la redirección inicial de una conexión a la conexión final con el destino.

Para obtener información más detallada, consulte la referencia de [**\_ \_ \_ \_ \_ contexto de redirección de conexión de WFP de la consulta SiO**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) . **SiO \_ El \_ \_ contexto de \_ redirección \_ de conexión WFP de consulta** se admite en windows 8, Windows Server 2012 y versiones posteriores.

### <a name="sio_query_wfp_connection_redirect_records-opcode-setting-i-t3"></a>SIO \_ query \_ \_ archivos de redirección de conexión de WFP \_ \_ (configuración de OpCode: I, T = = 3)

Consulta el registro de redirección para la conexión TCP/IP aceptada para su uso por parte de un servicio de redirección de la plataforma de filtrado de Windows (WFP).

Los registros de la conexión de WFP de la [**\_ consulta \_ \_ \_ \_ SiO**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) se usan para proporcionar el seguimiento de la conexión de proxy en las conexiones de socket redirigido. Esta característica de WFP facilita el seguimiento de los registros de redireccionamiento de la redirección inicial de una conexión a la conexión final con el destino.

Para obtener información más detallada, consulte la referencia de la [**consulta SiO de \_ \_ \_ \_ redirección de \_ registros de redireccionamiento**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) . **SiO \_ En Windows 8, Windows Server 2012 y versiones posteriores, se admiten \_ \_ \_ \_ registros de redirección de conexión de WFP** .

### <a name="sio_rcvall-opcode-setting-i-t3"></a>SIO \_ RCVALL (configuración de OpCode: I, T = = 3)

Permite a un socket recibir todos los paquetes IPv4 o IPv6 que pasan throuigh una interfaz de red. El identificador de socket que se pasa a la función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) debe ser uno de los siguientes:

-   Un socket IPv4 que se creó con la familia de direcciones establecida en AF \_ inet, el tipo de socket establecido en sock \_ raw y el protocolo establecido en IPPROTO \_ IP.
-   Un socket IPv6 que se creó con la familia de direcciones establecida en AF \_ inet6, el tipo de socket establecido en sock \_ raw y el protocolo establecido en IPPROTO \_ IPv6.

El socket también debe estar enlazado a una interfaz IPv4 o IPv6 local explícita, lo que significa que no se puede enlazar a **inaddress \_ any** o **in6addr \_ any**.

En Windows Server 2008 y versiones anteriores, el valor de ioctl de [**SiO \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) no capturar los paquetes locales enviados fuera de una interfaz de red. Esto incluye los paquetes recibidos en otra interfaz y reenviados fuera de la interfaz de red especificada para el ioctl **SiO \_ RCVALL** .

En Windows 7 y Windows Server 2008 R2, se ha cambiado para que los paquetes locales enviados fuera de una interfaz de red también se capturen. Esto incluye los paquetes recibidos en otra interfaz y, a continuación, reenviar la interfaz de red enlazada al socket con el ioctl [**SiO \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) .

La configuración de este IOCTL requiere privilegios de administrador en el equipo local.

Esta característica se denomina a veces modo promiscuo.

Los valores posibles para la opción de ioctl **SiO \_ RCVALL** se especifican en la enumeración de **\_ valores RCVALL** definida en el archivo de encabezado *Mstcpip. h* . Los valores posibles para SIO \_ RCVALL son los siguientes:

| Término                                                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-|-|
| <span id="RCVALL_OFF"></span><span id="rcvall_off"></span>RCVALL \_ desactivado<br/>                                     | Deshabilite esta opción para que un socket no reciba todos los paquetes IPv4 o IPv6 de la red. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RCVALL_ON"></span><span id="rcvall_on"></span>RCVALL \_<br/>                                        | Habilite esta opción para que un socket reciba todos los paquetes IPv4 o IPv6 de la red. Esta opción habilita el modo promiscuo en la tarjeta de interfaz de red (NIC), si la NIC es compatible con el modo promiscuo. En un segmento LAN con un concentrador de red, una NIC que admita el modo promiscuo capturará todo el tráfico de IPv4 o IPv6 en la LAN, incluido el tráfico entre otros equipos del mismo segmento de LAN. Todos los paquetes capturados (IPv4 o IPv6, según el socket) se entregarán al socket sin formato. <br/> Esta opción no capturará otros paquetes (por ejemplo, paquetes ARP, IPX y NetBEUI) en la interfaz.<br/> Netmon usa el mismo modo para la interfaz de red, pero no usa esta opción para capturar el tráfico.<br/> |
| <span id="RCVALL_SOCKETLEVELONLY"></span><span id="rcvall_socketlevelonly"></span>RCVALL \_ SOCKETLEVELONLY<br/> | Esta característica no está implementada actualmente, por lo que establecer esta opción no tiene ningún efecto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="RCVALL_IPLEVEL"></span><span id="rcvall_iplevel"></span>RCVALL \_ IPLEVEL<br/>                         | Habilite esta opción para que un socket IPv4 o IPv6 reciba todos los paquetes en el nivel de IP de la red. Esta opción no habilita el modo promiscuo en la tarjeta de interfaz de red. Esta opción solo afecta al procesamiento de paquetes en el nivel de IP. La NIC sigue recibiendo solo los paquetes dirigidos a sus direcciones de unidifusión y multidifusión configuradas. Sin embargo, un socket con esta opción habilitada no solo recibirá paquetes dirigidos a direcciones IP específicas, sino que recibirá todos los paquetes IPv4 o IPv6 que reciba la NIC.<br/> Esta opción no capturará otros paquetes (por ejemplo, los paquetes ARP, IPX y NetBEUI) recibidos en la interfaz.<br/>                                                                                             |



 

Para obtener información más detallada, consulte la referencia de [**SiO \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) .

**SiO \_ RCVALL** es compatible con Windows 2000 y versiones posteriores.

### <a name="sio_rcvall_igmpmcast-opcode-setting-i-t3"></a>SIO \_ RCVALL \_ IGMPMCAST (configuración de OpCode: I, T = = 3)

Permite que un socket reciba todo el tráfico IP de multidifusión IGMP de la red, sin que se reciba otro tráfico IP de multidifusión. El identificador de socket que se pasa a la función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) debe ser de la familia de direcciones de AF \_ inet, el \_ tipo de socket sin formato Sock y el \_ Protocolo IGMP IPPROTO. El socket también debe estar enlazado a una interfaz local explícita, lo que significa que no se puede enlazar a la entrada \_ any.

Una vez enlazado el socket y el conjunto de IOCTL, las llamadas a las funciones [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) o [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) devuelven datagramas IP de multidifusión que pasan a través de la interfaz determinada. Tenga en cuenta que debe proporcionar un búfer suficientemente grande. La configuración de este IOCTL requiere privilegios de administrador en el equipo local.

**SiO \_ RCVALL \_ IGMPMCAST** es compatible con Windows 2000 y versiones posteriores.

### <a name="sio_rcvall_mcast-opcode-setting-i-t3"></a>SIO \_ RCVALL \_ MCAST (configuración de OpCode: I, T = = 3)

Permite que un socket reciba todo el tráfico IP de multidifusión en la red (es decir, todos los paquetes IP destinados a las direcciones IP en el intervalo de 224.0.0.0 a 239.255.255.255). El identificador de socket que se pasa a la función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) debe ser de AF \_ inet Address Family, sock \_ Raw Socket Type y IPPROTO \_ UDP Protocol. El socket también debe enlazarse a una interfaz local explícita, lo que significa que no se puede enlazar a la indirección \_ . El socket debe enlazarse al puerto cero.

Una vez enlazado el socket y el conjunto de IOCTL, las llamadas a las funciones [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) o [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) devuelven datagramas IP de multidifusión que pasan a través de la interfaz determinada. Tenga en cuenta que debe proporcionar un búfer suficientemente grande. La configuración de este IOCTL requiere privilegios de administrador en el equipo local.

**SiO \_ RCVALL \_ MCAST** es compatible con Windows 2000 y versiones posteriores.

### <a name="sio_release_port_reservation-opcode-setting-i-t3"></a>SIO \_ versión de \_ reserva de puerto \_ (configuración de OpCode: I, T = = 3)

Libera una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP. La reserva en tiempo de ejecución que se va a liberar debe haberse obtenido del proceso de emisión mediante el ioctl de [**reserva de puerto de adquisición de SiO \_ \_ \_**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) .

Para obtener información más detallada, consulte la referencia de la [**\_ reserva de \_ puertos \_ de versión SiO**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85)) .

[**SiO \_ La \_ \_ reserva de puertos de versión**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85)) se admite en Windows Vista y versiones posteriores del sistema operativo.

### <a name="sio_routing_interface_change-opcode-setting-i-t1"></a>SIO \_ cambio de la interfaz de enrutamiento \_ \_ (configuración de OpCode: I, T = = 1)

Para recibir una notificación de un cambio en la interfaz de enrutamiento que se debe usar para llegar a la dirección remota en el búfer de entrada (especificado como una estructura [**sockaddr**](sockaddr-2.md) ). No se proporcionará información de salida en la nueva interfaz de enrutamiento al finalizar este IOCTL; la finalización indica simplemente que la interfaz de enrutamiento de un destino determinado ha cambiado y debe consultarse mediante el ioctl de consulta de la **\_ interfaz de enrutamiento de \_ \_ SiO** .

Se presupone, aunque no es necesario, que la aplicación use e/s superpuestas para recibir una notificación del cambio de la interfaz de enrutamiento mediante la finalización de la solicitud de cambio de la **\_ interfaz de enrutamiento de \_ \_ SiO** . Como alternativa, si la **interfaz de enrutamiento de SiO \_ \_ \_ cambia** ioctl se emite en un socket que no es de bloqueo con los parámetros *lpOverlapped* y *lpCompletionRoutine* establecidos en **null**), se completará inmediatamente y [WSAEWOULDBLOCK](windows-sockets-error-codes-2.md) como un error, y la aplicación puede esperar a que se envíen los eventos de cambio de enrutamiento a través de la llamada a [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) o [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) con el \_ \_ \_ bit de cambio de interfaz de enrutamiento

Se reconoce que la información de enrutamiento sigue siendo estable en la mayoría de los casos, por lo que solicitar a la aplicación mantener varios ioctl pendientes para recibir notificaciones sobre todos los destinos en los que está interesado y que el proveedor de servicios realice un seguimiento de estas solicitudes de notificación usará una cantidad significativa de recursos del sistema. Esta situación se puede evitar extendiendo el significado de los parámetros de entrada y relajando los requisitos del proveedor de servicios de la manera siguiente:

-   La aplicación puede especificar una dirección comodín específica de la familia de protocolos (la misma que se usa en la llamada de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) cuando se solicita enlazar a cualquier dirección disponible) para solicitar notificaciones de cambios de enrutamiento. Esto permite a la aplicación mantener solo un **cambio de \_ \_ interfaz de \_ enrutamiento de SiO** pendiente para todos los sockets y destinos que tiene y, a continuación, usar la **\_ \_ \_ consulta de interfaz de enrutamiento de SiO** para obtener la información de enrutamiento real.
-   Un proveedor de servicios tiene la opción de omitir la información especificada por la aplicación en el búfer de entrada del cambio de la interfaz de enrutamiento de sio (como si la aplicación especificara una dirección de carácter comodín) y completar el evento de cambio de la interfaz de enrutamiento de SiO o de la interfaz de enrutamiento de Signal **\_ \_ \_** **\_ \_ \_** \_ \_ \_

### <a name="sio_routing_interface_query-opcode-setting-i-o-t1"></a>SIO \_ \_ \_ consulta de interfaz de enrutamiento (configuración de OpCode: I, O, T = = 1)

Para obtener la dirección de la interfaz local (representada como estructura [**sockaddr**](sockaddr-2.md) ), que se debe usar para enviar a la dirección remota especificada en el búfer de entrada (como **sockaddr**). Se pueden enviar direcciones de multidifusión remotas en el búfer de entrada para obtener la dirección de la interfaz preferida para la transmisión por multidifusión. En cualquier caso, la aplicación puede usar la dirección de la interfaz en una solicitud BIND () subsiguiente.

Tenga en cuenta que las rutas están sujetas a cambios. Por lo tanto, las aplicaciones no pueden confiar en la información devuelta por la consulta de interfaz de enrutamiento de SiO para ser persistente. **\_ \_ \_** Las aplicaciones pueden registrarse para el enrutamiento de notificaciones de cambio a través de la **interfaz de enrutamiento de SiO \_ \_ \_ Change** IOCTL que proporciona una notificación a través de un evento de cambio de interfaz de enrutamiento FD o de e/s superpuesta \_ \_ \_ . Se puede usar la siguiente secuencia de acciones para garantizar que la aplicación siempre tiene la información de la interfaz de enrutamiento actual para un destino determinado:

-   Problema de la **interfaz de enrutamiento de SiO \_ \_ \_ Change** ioctl
-   Problema **de \_ \_ \_ consulta de interfaz de enrutamiento de SiO** ioctl
-   Siempre que el cambio de la interfaz de enrutamiento de SiO notifica a la aplicación de cambios de enrutamiento (ya sea a través de e/s superpuestas o mediante **\_ \_ \_** \_ el evento de cambio de la interfaz de enrutamiento FD \_ \_ ), se debe repetir la secuencia de acciones completa.

Si el búfer de salida no es lo suficientemente grande como para contener la dirección de la interfaz, \_ se devuelve un error de socket como resultado de este ioctl y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [WSAEFAULT](windows-sockets-error-codes-2.md). En este caso, se devolverá el tamaño necesario del búfer de salida en *lpcbBytesReturned* . Nota: el código de error WSAEFAULT también se devuelve si el parámetro *lpvInBuffer*, *lpvOutBuffer* o *lpcbBytesReturned* no está totalmente incluido en una parte válida del espacio de direcciones del usuario.

Si no se puede tener acceso a la dirección de destino especificada en el búfer de entrada a través de cualquiera de las interfaces disponibles, \_ se devuelve un error de socket como resultado de este ioctl y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [WSAENETUNREACH](windows-sockets-error-codes-2.md) o incluso [WSAENETDOWN](windows-sockets-error-codes-2.md) si se pierde toda la conectividad de red.

### <a name="sio_set_compatibility_mode-opcode-setting-i-t3"></a>SIO \_ set \_ Compatibility \_ Mode (configuración de OpCode: I, T = = 3)

Solicita el modo en que la pila de red debe controlar ciertos comportamientos para los que la manera predeterminada de controlar el comportamiento puede diferir en las versiones de Windows. La estructura de argumentos **del \_ \_ \_ modo de compatibilidad de SiO Set** se especifica en la estructura del **\_ \_ modo de compatibilidad WSA** definida en el archivo de encabezado *Mswsockdef. h* . Esta estructura se define de la siguiente manera:

```cpp
/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

El valor especificado en el miembro **BehaviorId** indica el comportamiento solicitado. El valor especificado en el miembro **TargetOsVersion** indica la versión de Windows que se solicita para el comportamiento.

El miembro **BehaviorId** puede ser uno de los valores del tipo de enumeración de identificador de **\_ \_ comportamiento \_ de compatibilidad WSA** definido en el archivo de encabezado *Mswsockdef. h* . Los valores posibles para el miembro **BehaviorId** son los siguientes.

| Término                                                                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-|-|
| <span id="WsaBehaviorAll"></span><span id="wsabehaviorall"></span><span id="WSABEHAVIORALL"></span>WsaBehaviorAll<br/>                                                     | Esto es equivalente a solicitar todos los posibles comportamientos compatibles definidos para el **identificador de \_ \_ comportamiento de \_ compatibilidad WSA**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="WsaBehaviorReceiveBuffering"></span><span id="wsabehaviorreceivebuffering"></span><span id="WSABEHAVIORRECEIVEBUFFERING"></span>WsaBehaviorReceiveBuffering<br/> | Cuando el miembro **TargetOsVersion** se establece en un valor de Windows Vista o posterior, se permite reducir el tamaño del búfer de recepción TCP en este socket mediante la opción de socket **so \_ RCVBUF** , incluso después de establecer una conexión TCP. <br/> Cuando el miembro **TargetOsVersion** se establece en un valor anterior a Windows Vista, no se permiten las reducciones del tamaño del búfer de recepción TCP en este socket mediante la opción de socket **so \_ RCVBUF** después del establecimiento de la conexión. <br/>                                                                                                                                                                                  |
| <span id="WsaBehaviorAutoTuning"></span><span id="wsabehaviorautotuning"></span><span id="WSABEHAVIORAUTOTUNING"></span>WsaBehaviorAutoTuning<br/>                         | Cuando el miembro **TargetOsVersion** se establece en un valor de Windows Vista o posterior, el ajuste automático de la ventana de recepción está habilitado y el factor de escala de la ventana TCP se reduce a 2 desde el valor predeterminado de 8.<br/> Cuando **TargetOsVersion** se establece en un valor anterior a Windows Vista, se deshabilita el ajuste automático de la ventana de recepción. La opción de escalado de la ventana TCP también está deshabilitada y el tamaño máximo de la ventana de recepción true está limitado a 65.535 bytes. No se puede negociar la opción de escalado de la ventana TCP en la conexión aunque se haya llamado a la opción de socket for **\_ RCVBUF** en este socket, especificando un valor superior a 65.535 bytes antes de que se establezca la conexión.<br/> |



 

Para obtener información más detallada, consulte la referencia de [**\_ modo de \_ compatibilidad \_ de SiO Set**](/previous-versions/windows/desktop/legacy/cc136103(v=vs.85)) .

**SiO \_ El \_ \_ modo de compatibilidad Set** es compatible con Windows Vista y versiones posteriores.

### <a name="sio_set_group_qos-opcode-setting-i-t1"></a>SIO \_ establecer \_ QoS de grupo \_ (configuración de OpCode: I, T = = 1)

Reservado.

### <a name="sio_set_priority_hint-opcode-setting-i-t3"></a>SIO_SET_PRIORITY_HINT (configuración de OpCode: I, T = = 3)

Proporciona una sugerencia al Protocolo de transporte subyacente para tratar el tráfico de este socket con una prioridad específica. *LpvInBuffer* debe apuntar a una variable de tipo **PRIORITY_HINT** con *cbInBuffer* establecido en sizeof (PRIORITY_HINT). Los parámetros *lpvOutBuffer* y *CbOutBuffer* deben ser **null** y 0, respectivamente. La implementación de TCP de Microsoft Windows admite este IOCTL a partir de Windows 10, versión 1809 (10,0; Compilación 17763) y versiones posteriores, como se indica a continuación: cuando el valor de prioridad solicitado se establece en **IoPriorityHintVeryLow**, TCP usa una versión modificada del algoritmo LEDBAT (definida en RFC 6817) para controlar la velocidad de tráfico saliente en el socket. Este IOCTL no afecta al tráfico de entrada. LEDBAT es un algoritmo de eliminación de registros obsoletos, y su objetivo es mantener una latencia baja y evitar cualquier efecto adverso en el tráfico de prioridad normal al salir del camino cuando está presente tráfico de prioridad normal.

Consulte también [RFC 6817](https://tools.ietf.org/html/rfc6817).

**SIO_SET_PRIORITY_HINT** es compatible con Windows 10, versión 1809 (10,0; Compilación 17763) y versiones posteriores.

### <a name="sio_set_qos-opcode-setting-i-t1"></a>SIO \_ set \_ QoS (configuración de OpCode: I, T = = 1)

Asociar la estructura [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) especificada al socket. No se requiere ningún búfer de salida, la estructura de **QoS** se obtiene del búfer de entrada. El código de error [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) se indica para los proveedores de servicios que no admiten la calidad de servicio.

### <a name="sio_tcp_initial_rto-opcode-setting-i-t3"></a>SIO_TCP_INITIAL_RTO (configuración de OpCode: I, T = = 3)

Controla las características de retransmisión iniciales (SYN/SYN + ACK) de un socket TCP mediante la configuración de los parámetros de tiempo de espera de retransmisión inicial (RTO). Los parámetros de configuración se especifican en una estructura de [**\_ \_ \_ parámetros de RTO iniciales de TCP**](/windows/desktop/api/mswsock/ns-mswsock-transmit_file_buffers) .

Para obtener información más detallada, consulte la referencia de [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) . [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) es compatible con Windows 8, windows Server 2012 y versiones posteriores.

### <a name="sio_translate_handle-opcode-setting-i-o-t1"></a>SIO \_ translate \_ HANDLE (configuración de OpCode: I, O, T = = 1)

Para obtener un identificador correspondiente para socket *s* que es válido en el contexto de una interfaz complementaria (por ejemplo, \_ NETDEV y TH \_ TAPI). En el búfer de entrada se especifica una constante de manifiesto que identifica la interfaz complementaria junto con cualquier otro parámetro necesario. El identificador correspondiente estará disponible en el búfer de salida tras la finalización de esta función. Consulte la sección correspondiente en los [anexos de Winsock](winsock-annexes.md) para obtener detalles específicos de una determinada interfaz del complemento. El código de error [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) se indica para los proveedores de servicios que no admiten este ioctl para la interfaz complementaria especificada. Este IOCTL recupera el identificador asociado mediante el **\_ \_ identificador** de la traducción de SiO.

Se recomienda usar el modelo de objetos componentes (COM) en lugar de este IOCTL para detectar y realizar el seguimiento de otras interfaces que podrían ser compatibles con un socket. Este IOCTL está presente por compatibilidad con versiones anteriores de los sistemas en los que COM no está disponible o no se puede usar por algún otro motivo.

### <a name="sio_udp_connreset-opcode-setting-i-t3"></a>SIO \_ UDP \_ CONNRESET (configuración de OpCode: I, T = = 3)

**Windows XP:** Controla si \_ se registran los mensajes de puerto UDP INalcanzable. Establézcalo en **true** para habilitar la creación de informes. Establézcalo en **false** para deshabilitar los informes.

### <a name="sio_set_wfp_connection_redirect_records-opcode-setting-i-t3"></a>SIO \_ establecer \_ \_ registros de redirección de conexión de WFP \_ \_ (configuración de OpCode: I, T = = 3)

Establece el registro de redirección en el nuevo socket TCP usado para conectarse al destino final para que lo use un servicio de redirección de la plataforma de filtrado de Windows (WFP).

El [**valor de SiO \_ set \_ WFP \_ Connection \_ Redirect \_ Records**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) se usa como parte del seguimiento de la conexión de proxy en las conexiones de socket redirigido. Esta característica de WFP facilita el seguimiento de los registros de redireccionamiento de la redirección inicial de una conexión a la conexión final con el destino.

Para obtener información más detallada, consulte la referencia de los [**\_ \_ \_ \_ \_ registros de redireccionamiento de conexión de WFP Set**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) . **SiO \_ En Windows 8, Windows Server 2012 y versiones posteriores, se admite el establecimiento de \_ \_ \_ \_ registros de redirección de conexión de WFP** .

### <a name="sio_tcp_info-opcode-setting-i-o-t3"></a>SIO \_ TCP \_ info (configuración de OpCode: I, O, T = = 3)

Recupera las estadísticas TCP para un socket. Las estadísticas de TCP se proporcionan en una estructura [**\_ \_ V0 de TCP info**](/windows/desktop/api/Mstcpip/ns-mstcpip-tcp_info_v0) .

A diferencia de la recuperación de estadísticas TCP con la función [**GetPerTcpConnectionEStats**](/windows/win32/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) , la recuperación de estadísticas TCP con este código de control no requiere que el código de usuario cargue, almacene y filtre la tabla de conexiones TCP, y no requiere privilegios elevados para su uso.

Para obtener más información, consulte [**SiO \_ TCP \_ info**](/previous-versions/windows/desktop/legacy/mt823415(v=vs.85)). **SiO \_ La \_ información de TCP** es compatible con Windows 10, la versión 1703, Windows Server 2016 y versiones posteriores.

## <a name="remarks"></a>Observaciones

Los ioctl de Winsock se definen en varios archivos de encabezado diferentes. Entre ellos se incluyen el archivo de encabezado *WinSock2. h*, *mswsock. h* y *Mstcpip. h* .

En el kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y también se han definido varios ioctl de Winsock en los archivos de encabezado *Ws2def. h*, *Ws2ipdef. h* y *Mswsockdef. h* . El archivo de encabezado *Ws2def. h* se incluye automáticamente en el archivo de encabezado *WinSock2. h* . El archivo de encabezado *Ws2ipdef. h* se incluye automáticamente en el archivo de encabezado *Ws2tcpip. h* . El archivo de encabezado *Mswsockdef. h* se incluye automáticamente en el archivo de encabezado *Mswsockdef. h* .

## <a name="requirements"></a>Requisitos

|||
|-|-|
| Encabezado<br/> | <dl> <dt>WinSock2. h; </dt> <dt>Mstcpip. h; </dt> <dt>Mswsock. h; </dt> <dt>Mswsockdef. h en Windows Vista, Windows Server 2008 y Windows 7 (incluido mswsock. h); </dt> <dt>Ws2def. h en Windows Vista, Windows Server 2008 y Windows 7 (incluido WinSock2. h); </dt> <dt>Ws2ipdef. h en Windows Vista, Windows Server 2008 y Windows 7 (incluido Ws2tcpip. h)</dt> </dl> |
