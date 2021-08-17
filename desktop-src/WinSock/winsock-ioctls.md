---
description: Tema de navegación para Windows IOCTLs de sockets de sockets de Windows (Winsock).
ms.assetid: 6a63c2c9-4e09-4a62-b39f-3ccb26287da8
title: IOCTLs de Winsock (Winsock2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8d9c47e68433747e341bbc0a082b5d40af76403b473caabe3423f5a186f499f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739955"
---
# <a name="winsock-ioctls"></a>ICTLs de Winsock

En esta sección se describen los controles de entrada y salida (IOCTL) de Winsock Socket para varias ediciones de Windows sistemas operativos. Use la [**función WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) o [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) para emitir una IOCTL de Winsock para controlar el modo de un socket, el protocolo de transporte o el subsistema de comunicaciones.

Algunas ICTL de Winsock requieren más explicaciones de las que puede transmitir esta tabla. estas opciones contienen vínculos a temas adicionales.

Es posible adoptar un esquema de codificación que conserve los códigos de operación [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) definidos actualmente y, al mismo tiempo, proporcionar una manera cómoda de particionar el espacio del identificador de código de operación en tanto como el parámetro *dwIoControlCode* sea ahora una entidad de 32 bits. El *parámetro dwIoControlCode* se ha creado para permitir la independencia del protocolo y del proveedor al agregar nuevos códigos de control y mantener la compatibilidad con versiones anteriores con los códigos de control de Windows Sockets 1.1 y Unix. El *parámetro dwIoControlCode* tiene el formato siguiente.

| I  | O  | V  | T  | Familia de proveedores y direcciones | Código                   |
|-|-|-|-|-|-|
| 3  | 3  | 2  | 2 2 | 2 2 2 2 2 2 2 1 1 1 1 | 1 1 1 1 1 1              |
| 1  | 0  | 9  | 8 7 | 6 5 4 3 2 1 0 9 8 7 6 | 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 |

> [!Note] 
> Los bits del *parámetro dwIoControlCode* mostrado en la tabla deben leerse verticalmente de arriba abajo por columna. Por lo tanto, el bit más a la izquierda es el bit 31, el bit siguiente es el bit 30 y el bit más a la derecha es el bit 0.

Se establece si el búfer de entrada es válido para el código, como con **IOC_IN**.

O se establece si el búfer de salida es válido para el código, como con **IOC_OUT**. Los códigos de control que usan búferes de entrada y salida establecen E/S.

V se establece si no hay parámetros para el código, como con **IOC_VOID**.

T es una cantidad de 2 bits que define el tipo de la IOCTL. Se definen los valores siguientes:

0 La IOCTL es un código IOCTL de Unix estándar, como **con FIONREAD** y **FIONBIO.**

1 La IOCTL es un código Windows Sockets 2 IOCTL genérico. Los nuevos códigos IOCTL definidos para Windows Sockets 2 tendrán T == 1.

2 La IOCTL solo se aplica a una familia de direcciones específica.

3 La IOCTL solo se aplica al proveedor de un proveedor específico, como sucede **con IOC_VENDOR**. Este tipo permite asignar a las empresas un número de proveedor que aparece en el **parámetro de la familia Vendor/Address.** A continuación, el proveedor puede definir nuevas ICTL específicas de ese proveedor sin tener que registrar la IOCTL con un centro de compensación, lo que proporciona flexibilidad y privacidad al proveedor.

**Familia de proveedores y direcciones** Cantidad de 11 bits que define al proveedor propietario del código (si T == 3) o que contiene la familia de direcciones a la que se aplica el código (si T == 2). Si se trata de un código IOCTL de Unix (T == 0), este parámetro tiene el mismo valor que el código en Unix. Si se trata de un Windows Sockets 2 IOCTL (T == 1), este parámetro se puede usar como una extensión del parámetro de código para proporcionar valores de código adicionales.

**Código** Cantidad de 16 bits que contiene el código IOCTL específico para la operación.

## <a name="unix-ioctl-codes"></a>Códigos IOCTL de Unix

Se admiten los siguientes códigos (comandos) de IOCTL de Unix.

### <a name="fionbio"></a>FIONBIO

Habilite o deshabilite el modo de no bloqueo en el *socket.* El *parámetro lpvInBuffer* apunta **a** un long sin signo (QoS), que es distinto de cero si se va a habilitar el modo sin bloqueo y cero si se va a deshabilitar. Cuando se crea un socket, funciona en modo de bloqueo (es decir, el modo sin bloqueo está deshabilitado). Esto es coherente con los sockets de BSD.

La [**rutina WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) o [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) establece automáticamente un socket en modo sin bloqueo. Si **WSAAsyncSelect** o **WSAEventSelect** se han emitido en un socket, cualquier intento de usar [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para volver a establecer el socket en modo de bloqueo producirá un error con WSAEINVAL. Para volver a establecer el socket en modo de bloqueo, una aplicación debe deshabilitar primero **WSAAsyncSelect** llamando a **WSAAsyncSelect** con el parámetro *lEvent* igual a cero o deshabilitar **WSAEventSelect** llamando a **WSAEventSelect** con el parámetro *lNetworkEvents* igual a cero.

### <a name="fionread"></a>FIONREAD

Determine la cantidad de datos que se pueden leer de forma atómica desde el *socket.* El *parámetro lpvOutBuffer* apunta a **un long** sin signo en el que [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) almacena el resultado.

Si el socket pasado en el parámetro *s* está orientado a secuencias (por ejemplo, escriba SOCK \_ STREAM), **FIONREAD** devuelve la cantidad total de datos que se pueden leer en una sola operación de recepción; normalmente es la misma que la cantidad total de datos puestos en cola en el socket (dado que un flujo de datos está orientado a bytes, esto no se garantiza).

Si el socket pasado en el parámetro *s* está orientado a mensajes (por ejemplo, escriba SOCK \_ DGRAM), **FIONREAD** devuelve a los informes el número total de bytes disponibles para leer, no el tamaño del primer datagrama (mensaje) en cola en el socket.

### <a name="siocatmark"></a>SIOCATMARK

Determine si se han leído o no todos los datos de OOB. Esto solo se aplica a un socket de estilo de secuencia (por ejemplo, tipo SOCK STREAM) que se ha configurado para la recepción insertada de cualquier dato \_ de OOB (SO \_ OOBINLINE). Si no hay datos de OOB a la espera de ser leídos, la operación devuelve TRUE. De lo contrario, devuelve **FALSE** y la siguiente operación de recepción realizada en el socket recuperará algunos o todos los datos anteriores a la marca; La aplicación debe usar la **operación SIOCATMARK** para determinar si queda alguno. Si hay datos normales anteriores a los datos urgentes (fuera de banda), se recibirán en orden. (Tenga en cuenta que las operaciones de [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) nunca mezclarán datos normales y OOB en la misma llamada). *lpvOutBuffer* apunta a un BOOL en el que [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) almacena el resultado.

## <a name="windows-sockets-2-commands"></a>Windows Comandos de sockets 2

Se admiten los Windows sockets 2 siguientes.

### <a name="sio_acquire_port_reservation-opcode-setting-i-t3"></a>SIO_ACQUIRE_PORT_RESERVATION (configuración del código de operación: I, T==3)

Solicite una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP. Para las reservas de puertos en tiempo de ejecución, el grupo de puertos requiere que las reservas se consuman desde el proceso en cuyo socket se concedió la reserva. Las reservas de puertos en tiempo de ejecución solo duren mientras dure el socket en el que se llamó a [**SIO \_ ACQUIRE PORT \_ \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) IOCTL. Por el contrario, cualquier proceso puede consumir las reservas de puerto persistentes creadas mediante la función [**CreatePersistentTcpPortReservation**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) con la capacidad de obtener reservas persistentes.

Para obtener información más detallada, consulte la referencia [**DE SIO \_ ACQUIRE PORT \_ \_ RESERVATION.**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85))

[**SIO \_ ACQUIRE \_ PORT \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) se admite en Windows Vista y versiones posteriores del sistema operativo.

### <a name="sio_address_list_change-opcode-setting-v-t1"></a>SIO \_ ADDRESS LIST CHANGE \_ \_ (configuración del código de operación: V, T==1)

Para recibir la notificación de los cambios en la lista de direcciones de transporte local de la familia de protocolos del socket a la que se puede enlazar la aplicación. No se proporciona ninguna información de salida tras la finalización de esta IOCTL; la finalización simplemente indica que la lista de direcciones locales disponibles ha cambiado y se debe volver a consultar a través de **SIO \_ ADDRESS LIST \_ \_ QUERY**.

Se supone (aunque no es necesario) que la aplicación usa E/S superpuesta para recibir una notificación del cambio mediante la finalización de la **solicitud SIO \_ ADDRESS LIST \_ \_ CHANGE.** Como alternativa, si la INSTRUCCIÓN **SIO \_ ADDRESS LIST \_ \_ CHANGE** IOCTL se emite en un socket sin bloqueo y sin parámetros superpuestos *(lpOverlapped* lpCompletionRoutine se establece en NULL), se completará inmediatamente con /   el error [WSACTLCTLDBLOCK](windows-sockets-error-codes-2.md).  A continuación, la aplicación puede esperar eventos de cambio de lista de direcciones a través de una llamada a [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) o [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) con el conjunto de bits FD ADDRESS LIST CHANGE en la máscara de bits de eventos \_ de \_ \_ red.

### <a name="sio_address_list_query-opcode-setting-o-t1"></a>SIO \_ ADDRESS LIST QUERY \_ \_ (configuración del código de operación: O, T==1)

Obtiene una lista de direcciones de transporte local de la familia de protocolos del socket a la que se puede enlazar la aplicación. La lista de direcciones varía en función de la familia de direcciones y algunas direcciones se excluyen de la lista.

> [!Note] 
> En Windows entornos de Plug-n-Play, las direcciones se pueden agregar y quitar dinámicamente. Por lo tanto, las aplicaciones no pueden confiar en que la información devuelta por **SIO \_ ADDRESS LIST \_ \_ QUERY** sea persistente. Las aplicaciones pueden registrarse para recibir notificaciones de cambio de dirección a través de **SIO \_ ADDRESS LIST \_ \_ CHANGE** IOCTL, que proporciona la notificación mediante E/S superpuesta o evento FD \_ ADDRESS LIST \_ \_ CHANGE. La siguiente secuencia de acciones se puede usar para garantizar que la aplicación siempre tiene información de lista de direcciones actual:

-  Problema **de CAMBIO DE LA LISTA DE DIRECCIONES \_ DE SIO \_ \_** IOCTL
-  Problema **de SIO \_ ADDRESS LIST \_ \_ QUERY** IOCTL
-  Cada **vez que SIO ADDRESS LIST \_ \_ \_ CHANGE** IOCTL notifica a la aplicación el cambio de la lista de direcciones (ya sea a través de E/S superpuesta o señalando el evento FD ADDRESS LIST CHANGE), se debe repetir toda la secuencia de \_ \_ \_ acciones.

Para obtener información más detallada, consulte la [**referencia DE CONSULTA DE SIO ADDRESS \_ \_ LIST. \_**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) **SIO \_ ADDRESS \_ LIST \_ QUERY** se admite en Windows 2000 y versiones posteriores.

### <a name="sio_apply_transport_setting-opcode-setting-i-t3"></a>SIO \_ APPLY TRANSPORT SETTING \_ \_ (configuración del código de operación: I, T==3)

Aplica una configuración de transporte a un socket. La configuración de transporte que se está aplicando se basa en el [**identificador de CONFIGURACIÓN DE \_ \_ TRANSPORTE**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) pasado en *el parámetro lpvInBuffer.*

La única configuración de transporte que se define actualmente es para la funcionalidad FUNCIONALIDAD DE NOTIFICACIÓN **\_ \_ \_ EN** TIEMPO REAL en un socket TCP.

Si el identificador de CONFIGURACIÓN DE TRANSPORTE pasado tiene el miembro **GUID** establecido en FUNCIONALIDAD DE NOTIFICACIÓN EN TIEMPO REAL , se trata de una solicitud para aplicar la configuración de notificación en tiempo real para el socket TCP usado con [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) para recibir notificaciones de red en segundo plano en una aplicación de Windows Store. **\_ \_ \_** [**\_ \_**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id)

Para obtener información más detallada, consulte la [**referencia SIO \_ APPLY TRANSPORT \_ \_ SETTING.**](/previous-versions/windows/desktop/legacy/jj553481(v=vs.85)) **SIO \_ APPLY \_ TRANSPORT \_ SETTING se** admite en Windows 8, Windows Server 2012 y versiones posteriores.

### <a name="sio_associate_handle-opcode-setting-i-t1"></a>SIO \_ ASSOCIATE \_ HANDLE (configuración del código de operación: I, T==1)

Asocie este socket al identificador (handle) especificado de la interfaz correspondiente. El búfer de entrada contiene el valor entero correspondiente a la constante de manifiesto para la interfaz complementaria (por ejemplo, TH NETDEV y \_ TH TAPI)., seguido de un valor que es un identificador de la interfaz complementaria especificada, junto con cualquier otra información \_ necesaria. Consulte la sección adecuada de [Los anexos de Winsock](winsock-annexes.md) para obtener detalles específicos de una interfaz complementaria determinada. El tamaño total se refleja en la longitud del búfer de entrada. No se requiere ningún búfer de salida. El código de error [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) se indica para los proveedores de servicios que no admiten esta IOCTL. El identificador asociado por esta IOCTL se puede recuperar mediante **SIO \_ TRANSLATE \_ HANDLE**.

Se podría usar una interfaz complementaria, por ejemplo, si un proveedor determinado proporciona (1) una gran cantidad de controles adicionales sobre el comportamiento de un socket y (2) los controles son lo suficientemente específicos del proveedor como para que no se asignen a las funciones de socket de Windows existentes o a las que es probable que se definan en el futuro. Se recomienda usar el Modelo de objetos componentes (COM) en lugar de esta IOCTL para detectar y realizar un seguimiento de otras interfaces que podrían ser compatibles con un socket. Esta IOCTL está presente para la compatibilidad (inversa) con sistemas en los que COM no está disponible o no se puede usar por alguna otra razón.

### <a name="sio_associate_port_reservation-opcode-setting-i-t3"></a>SIO \_ ASSOCIATE PORT RESERVATION \_ \_ (configuración del código de operación: I, T==3)

Asocie un socket a una reserva persistente o en tiempo de ejecución para un bloque de puertos TCP o UDP identificados por el token de reserva de puertos. [**Sio \_ ASSOCIATE PORT \_ \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) IOCTL debe emitirse antes de enlazar el socket. Si y cuando se enlaza el socket, el puerto asignado a él se seleccionará de la reserva de puertos identificada por el token especificado. Si no hay puertos disponibles en la reserva especificada, se producirá un error en la llamada [**a**](/windows/desktop/api/winsock/nf-winsock-bind) la función de enlace.

Para obtener información más detallada, consulte la referencia [**de SIO \_ ASSOCIATE PORT \_ \_ RESERVATION.**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85))

[**SIO \_ ASSOCIATE \_ PORT \_ RESERVATION se**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) admite en Windows Vista y versiones posteriores del sistema operativo.

### <a name="sio_base_handle-opcode-setting-o-t1"></a>SIO \_ BASE \_ HANDLE (configuración de código de operación: O, T==1)

Recupera el identificador del proveedor de servicios base para un socket determinado. El valor devuelto es **socket**.

Un proveedor de servicios en capas nunca interceptaría esta IOCTL, ya que el valor devuelto debe ser el identificador de socket del proveedor de servicios base.

Si el búfer de salida no es lo suficientemente grande para un identificador de socket *(cbOutBuffer* es menor que el tamaño de un **SOCKET)** o el parámetro *lpvOutBuffer* es un puntero **NULL,** se devuelve **SOCKET \_ ERROR** como resultado de esta IOCTL y [**WSAGetLastError devuelve**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) [WSAEFAULT.](windows-sockets-error-codes-2.md)

**SIO \_ BASE \_ HANDLE** se define en el archivo de encabezado *Mswsock.h* y se admite en Windows Vista y versiones posteriores.

### <a name="sio_bsp_handle-opcode-setting-o-t1"></a>SIO \_ BSP \_ HANDLE (configuración de código de operación: O, T==1)

Recupera el identificador del proveedor de servicios base para un socket utilizado por la [**función WSASendMsg.**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) El valor devuelto es **socket**.

Un proveedor de servicios por capas usa esta ioctl para asegurarse de que el proveedor intercepta la [**función WSASendMsg.**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)

Si el búfer de salida no es lo suficientemente grande para un identificador de socket *(cbOutBuffer* es menor que el tamaño de un **SOCKET)** o el parámetro *lpvOutBuffer* es un puntero **NULL,** se devuelve **SOCKET \_ ERROR** como resultado de esta IOCTL y [**WSAGetLastError devuelve**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) [WSAEFAULT.](windows-sockets-error-codes-2.md)

**SIO \_ El identificador \_ de BSP** se define en el archivo de encabezado *Mswsock.h* y se admite en Windows Vista y versiones posteriores.

### <a name="sio_bsp_handle_select-opcode-setting-o-t1"></a>SIO \_ BSP \_ HANDLE SELECT \_ (configuración de código de operación: O, T==1)

Recupera el identificador del proveedor de servicios base para un socket usado por la [**función select.**](/windows/desktop/api/Winsock2/nf-winsock2-select) El valor devuelto es **socket**.

Un proveedor de servicios en capas usa esta ioctl para asegurarse de que el proveedor intercepta la [**función select.**](/windows/desktop/api/Winsock2/nf-winsock2-select)

Si el búfer de salida no es lo suficientemente grande para un identificador de socket *(cbOutBuffer* es menor que el tamaño de un **SOCKET)** o el parámetro *lpvOutBuffer* es un puntero **NULL,** se devuelve **SOCKET \_ ERROR** como resultado de esta IOCTL y [**WSAGetLastError devuelve**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) [WSAEFAULT.](windows-sockets-error-codes-2.md)

**SIO \_ BSP \_ HANDLE \_ SELECT** se define en el archivo de encabezado *Mswsock.h* y se admite en Windows Vista y versiones posteriores.

### <a name="sio_bsp_handle_poll-opcode-setting-o-t1"></a>SIO \_ BSP \_ HANDLE POLL \_ (configuración del código de operación: O, T==1)

Recupera el identificador del proveedor de servicios base para un socket utilizado por la [**función WSAPoll.**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) El *parámetro lpOverlapped* debe ser un **puntero NULL.** El valor devuelto es **socket**.

Un proveedor de servicios en capas usa esta ioctl para asegurarse de que el proveedor intercepta la [**función WSAPoll.**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)

Si el búfer de salida no es lo suficientemente grande para un identificador de socket *(cbOutBuffer* es menor que el tamaño de un **SOCKET),** el parámetro *lpvOutBuffer* es un puntero **NULL** o el parámetro *lpOverlapped* no es un puntero **NULL,** se devuelve **SOCKET \_ ERROR** como resultado de esta IOCTL y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [WSAEFAULT.](windows-sockets-error-codes-2.md)

**SIO \_ BSP \_ HANDLE \_ POLL se** define en el archivo de encabezado *Mswsock.h* y se admite en Windows Vista y versiones posteriores.

### <a name="sio_chk_qos-opcode-setting-i-o-t3"></a>QOS \_ de SIO CHK \_ (configuración de código de operación: I, O, T==3)

Recupera información sobre las características del tráfico de QoS. Durante la fase de transición en el sistema de envío entre la configuración del flujo y la recepción de un mensaje [RESV](/previous-versions/windows/desktop/qos/how-the-rsvp-service-invokes-tc) (vea Cómo invoca TC el servicio RSVP para obtener más información sobre la fase de transición), el tráfico asociado a un flujo RSVP se configura en función del tipo de servicio[(BEST EFFORT,](/previous-versions/windows/desktop/qos/best-effort) [CONTROLLED LOAD](/previous-versions/windows/desktop/qos/controlled-load)o [GUARANTEED).](/previous-versions/windows/desktop/qos/guaranteed) Para más información, consulte [Using SIO CHK QOS (Uso de SIO \_ CHK \_ QOS)](/previous-versions/windows/desktop/qos/using-sio-chk-qos) en la [sección Quality of Service (Calidad](/previous-versions/windows/desktop/qos/qos-start-page) de servicio) del SDK de plataforma.

### <a name="sio_cpu_affinity-opcode-setting-i-t3"></a>SIO_CPU_AFFINITY (configuración del código de operación: I, T==3)

Habilita el uso compartido de puertos y la paralelización de indicaciones de recepción. Cuando la aplicación usa esta opción de socket para asociar sockets a distintos procesadores y, a continuación, enlaza los sockets a la misma dirección, las indicaciones de recepción se distribuirán entre los sockets en función del hash de escala del lado de recepción (RSS). La configuración de RSS no cambia, por lo que cualquier flujo determinado (punto de conexión local, par de punto de conexión remoto) siempre se indicará en el mismo procesador. Como resultado, todos los paquetes que pertenecen a un flujo determinado se indicarán en el mismo socket. Se debe llamar a esta IOCTL antes del enlace; de lo contrario, se devolverá WSAEINVAL. El búfer de entrada es un índice de procesador (basado en 0) de tipo USHORT. La IOCTL no es compatible con SO_REUSEADDR y SO_REUSE_MULTICASTPORT. Solo se admite para sockets UDP.

> [!NOTE]
> Si tiene como destino la versión 10.0.19041.0 (Windows 10, versión 2004) del SDK de Windows, use el valor en lugar del nombre `0x98000015` **SIO_CPU_AFFINITY**.

### <a name="sio_enable_circular_queueing-opcode-setting-v-t1"></a>SIO \_ ENABLE \_ CIRCULAR \_ QUEUEING (configuración de código de operación: V, T==1)

Indica al proveedor de servicios orientado a mensajes subyacente que nunca se debe descartar un mensaje recién llegado debido a un desbordamiento de cola de búfer. En su lugar, se debe eliminar el mensaje más antiguo de la cola para dar cabida al mensaje recién llegado. No se requieren búferes de entrada y salida. Tenga en cuenta que esta IOCTL solo es válida para los sockets asociados a protocolos no confiables orientados a mensajes. El código de error [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) se indica para los proveedores de servicios que no admiten esta IOCTL.

### <a name="sio_find_route-opcode-setting-o-t1"></a>SIO \_ FIND \_ ROUTE (configuración de código de operación: O, T==1)

Cuando se emite, esta IOCTL solicita que se descubra la ruta a la dirección remota especificada como [**sockaddr**](sockaddr-2.md) en el búfer de entrada. Si la dirección ya existe en la caché local, su entrada se invalida. En el caso del IPX de Dpi, esta llamada inicia una dirección IPX GetLocalTarget (GLT), que consulta la red para la dirección remota dada.

### <a name="sio_flush-opcode-setting-v-t1"></a>SIO \_ FLUSH (configuración del código de operación: V, T==1)

Descarta el contenido actual de la cola de envío asociada a este socket. No se requieren búferes de entrada y salida. El código de error [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) se indica para los proveedores de servicios que no admiten esta IOCTL.

### <a name="sio_get_broadcast_address-opcode-setting-o-t1"></a>SIO \_ GET BROADCAST ADDRESS \_ \_ (configuración del código de operación: O, T==1)

Esta IOCTL rellena el búfer de salida con una estructura [sockaddr](sockaddr-2.md) que contiene una dirección de difusión adecuada para su uso [**con sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) /  [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto). Esta IOCTL no se admite para sockets IPv6 y devuelve el código de error [WSAENOPROTOOPT.](windows-sockets-error-codes-2.md)

### <a name="sio_get_extension_function_pointer-opcode-setting-o-i-t1"></a>SIO \_ GET EXTENSION FUNCTION POINTER \_ \_ \_ (configuración de código de operación: O, I, T==1)

Recupere un puntero a la función de extensión especificada admitida por el proveedor de servicios asociado. El búfer de entrada contiene un identificador único global **(GUID)** cuyo valor identifica la función de extensión en cuestión. El puntero a la función deseada se devuelve en el búfer de salida. Los proveedores de proveedores de servicios establecen los identificadores de función de extensión y deben incluirse en la documentación del proveedor que describe las funcionalidades y semánticas de la función de extensión.

Los valores GUID de las funciones de extensión compatibles Windows proveedor de servicios TCP/IP se definen en el archivo de encabezado *Mswsock.h.* El valor posible de estos GUID es el siguiente:

| Término                                                                                                                | Descripción                                                                               |
|-|-|
| <span id="WSAID_ACCEPTEX"></span><span id="wsaid_acceptex"></span>WSAID \_ ACCEPTEX<br/>                                     | Función [**de extensión AcceptEx.**](/windows/win32/api/mswsock/nf-mswsock-acceptex)<br/>                         |
| <span id="WSAID_CONNECTEX"></span><span id="wsaid_connectex"></span>WSAID \_ CONNECTEX<br/>                                  | Función [**de extensión ConnectEx.**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) <br/>                      |
| <span id="WSAID_DISCONNECTEX"></span><span id="wsaid_disconnectex"></span>WSAID \_ DISCONNECTEX<br/>                         | La [**función de extensión DisconnectEx.**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) <br/>                |
| <span id="WSAID_GETACCEPTEXSOCKADDRS"></span><span id="wsaid_getacceptexsockaddrs"></span>WSAID \_ GETACCEPTEXSOCKADDRS<br/> | Función [**de extensión GetAcceptExSockaddrs.**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs)<br/> |
| <span id="WSAID_TRANSMITFILE"></span><span id="wsaid_transmitfile"></span>TRANSMITFILE de \_ WSAID<br/>                         | Función [**de extensión TransmitFile.**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)<br/>                 |
| <span id="WSAID_TRANSMITPACKETS"></span><span id="wsaid_transmitpackets"></span>TRANSMITPACKETS DE WSAID \_<br/>                | Función [**de extensión TransmitPackets.**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) <br/>          |
| <span id="WSAID_WSARECVMSG"></span><span id="wsaid_wsarecvmsg"></span>WSAID \_ WSARECVMSG<br/>                               | Función [**LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)<br/>                     |
| <span id="WSAID_WSASENDMSG"></span><span id="wsaid_wsasendmsg"></span>WSAID \_ WSASENDMSG<br/>                               | Función [**de extensión WSASendMsg.**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) <br/>                      |

### <a name="sio_get_group_qos-opcode-setting-o-i-t1"></a>SIO \_ GET \_ GROUP \_ QOS (configuración de código de operación: O, I, T==1)

Reservado para su uso futuro con sockets.

Recupere la [**estructura qos**](/windows/win32/api/winsock2/ns-winsock2-qos) asociada al grupo de sockets al que pertenece este socket. El búfer de entrada es opcional. Algunos protocolos (por ejemplo, RSVP) permiten usar el búfer de entrada para calificar una solicitud de calidad de servicio. La **estructura qos** se copiará en el búfer de salida. Si este socket no pertenece a un grupo de sockets adecuado, los miembros **SendingFlowspec** y **ReceivingFlowspec** de la estructura **QOS** devuelta se establecen en **NULL.** El código de error [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) se indica para los proveedores de servicios que no admiten la calidad de servicio.

### <a name="sio_get_interface_list-opcode-setting-o-t0"></a>SIO \_ GET INTERFACE LIST \_ \_ (configuración de código de operación: O, T==0)

Devuelve una lista de interfaces IP configuradas y sus parámetros como una matriz de estructuras [**INTERFACE \_ INFO.**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info)

> [!Note]  
> La compatibilidad con este comando es obligatoria para los Windows de servicio TCP/IP compatibles con Sockets 2.

El *parámetro lpvOutBuffer* apunta al búfer en el que se va a almacenar la información sobre las interfaces como una matriz de estructuras [**INTERFACE \_ INFO**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) para direcciones IP de unidifusión en las interfaces. El *parámetro cbOutBuffer* especifica la longitud del búfer de salida. El número de interfaces devueltas (número de estructuras devueltas en el búfer al que apunta el parámetro *lpvOutBuffer)* se puede determinar en función de la longitud real del búfer de salida devuelto en el parámetro *lpcbBytesReturned.*

Si se llama a la función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) con **SIO \_ GET INTERFACE \_ \_ LIST** y el miembro de nivel del parámetro *s* del socket no se define como **\_ IP IP DE IPPROTO,** se devuelve **WSAEINVAL.** Una llamada a la función **WSAIoctl** con **SIO \_ GET INTERFACE \_ \_ LIST** devuelve **WSAEFAULT** si el *parámetro cbOutBuffer* que especifica la longitud del búfer de salida es demasiado pequeño y recibe la lista de interfaces configuradas.

**SIO \_ GET \_ INTERFACE \_ LIST** se admite en Windows Me/98 y Windows NT 4.0 con SP4 y versiones posteriores.

### <a name="sio_get_interface_list_ex-opcode-setting-o-t0"></a>SIO \_ GET INTERFACE LIST EX \_ \_ \_ (configuración de código de operación: O, T==0)

Reservado para su uso futuro con sockets.

Devuelve una lista de interfaces IP configuradas y sus parámetros como una matriz de estructuras [**INTERFACE \_ INFO \_ EX.**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex)

El *parámetro lpvOutBuffer* apunta al búfer en el que se va a almacenar la información sobre las interfaces como una matriz de estructuras [**INTERFACE INFO \_ \_ EX**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex) para direcciones IP de unidifusión en la interfaz. El *parámetro cbOutBuffer* especifica la longitud del búfer de salida. El número de interfaces devueltas (número de estructuras devueltas en *lpvOutBuffer)* se puede determinar en función de la longitud real del búfer de salida devuelto en el parámetro *lpcbBytesReturned.*

**SIO \_ GET \_ INTERFACE \_ LIST \_ EX** no se admite actualmente en Windows.

### <a name="sio_get_qos-opcode-setting-o-t1"></a>SIO \_ GET \_ QOS (configuración de código de operación: O, T==1)

Reservado para su uso futuro con sockets. Recupere la [**estructura qos**](/windows/win32/api/winsock2/ns-winsock2-qos) asociada al socket. El búfer de entrada es opcional. Algunos protocolos (por ejemplo, RSVP) permiten usar el búfer de entrada para calificar una solicitud de calidad de servicio. La **estructura qos** se copiará en el búfer de salida. El búfer de salida debe tener un tamaño lo suficientemente grande como para poder contener la estructura **qos** completa. El código de error [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) se indica para los proveedores de servicios que no admiten la calidad de servicio.

Es posible que un remitente no llame **a SIO \_ GET \_ QOS** hasta que el socket esté conectado.

Un receptor puede llamar a **SIO \_ GET \_ QOS en** cuanto se enlaza.

### <a name="sio_get_tx_timestamp"></a>SIO_GET_TX_TIMESTAMP

Una IOCTL de socket usada para obtener marcas de tiempo para paquetes transmitidos (TX). Solo es válido para sockets de datagramas.

El **SIO_GET_TX_TIMESTAMP** control quita una marca de tiempo de transmisión de la cola de marca de tiempo de transmisión de un socket. Habilite primero la recepción de marca de tiempo mediante [**SIO_TIMESTAMPING**](#sio_timestamping) IOCTL del socket. A continuación, recupere las marcas de tiempo tx por identificador llamando a la función [**WSAIoctl**](/windows/win32/api/winsock2/nf-winsock2-wsaioctl) (o [**WSPIoctl)**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))con los parámetros siguientes.

Por **SIO_GET_TX_TIMESTAMP**, la entrada es un identificador de marca de tiempo **UINT32** y la salida es un valor de marca **de tiempo UINT64.** Si se ejecuta correctamente, la marca de tiempo tx está disponible y se devuelve. Si no hay marcas de tiempo de transmisión disponibles, [**WSAGetLastError**](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) devuelve **WSAEWOULDBLOCK**.

> [!NOTE]
> Las marcas de tiempo TX no se admiten al realizar un envío de forma UDP_SEND_MSG_SIZE **.**

Consulte también [Marca de tiempo de Winsock.](/windows/win32/winsock/winsock-timestamping)

### <a name="sio_ideal_send_backlog_change-opcode-setting-v-t0"></a>SIO \_ IDEAL \_ SEND \_ BACKLOG CHANGE \_ (configuración del código de operación: V, T==0)

Notifica a una aplicación cuándo cambia el valor del trabajo pendiente de envío ideal (ISB) para la conexión subyacente.

Al enviar datos a través de una conexión TCP mediante sockets Windows, es importante mantener una cantidad suficiente de datos pendientes (enviados pero no reconocidos todavía) en TCP para lograr el máximo rendimiento. El valor ideal para la cantidad de datos pendientes para lograr el mejor rendimiento para la conexión TCP se denomina tamaño de trabajo pendiente de envío (ISB) ideal. El valor de ISB es una función del producto de retraso de ancho de banda de la conexión TCP y la ventana de recepción anunciada del receptor (y en parte la cantidad de congestión en la red).

El valor de ISB por conexión está disponible en la implementación del protocolo TCP en Windows Server 2008, Windows Vista con SP1 y versiones posteriores del sistema operativo. Una aplicación puede usar **SIO \_ IDEAL SEND \_ \_ BACKLOG \_ CHANGE** IOCTL para obtener una notificación cuando el valor de ISB cambia dinámicamente para una conexión.

Para obtener información más detallada, consulte la referencia [**SIO \_ IDEAL SEND \_ \_ BACKLOG \_ CHANGE.**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85))

[**SIO \_ IDEAL \_ SEND \_ BACKLOG \_ CHANGE**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85)) se admite en Windows Server 2008, Windows Vista con SP1 y versiones posteriores del sistema operativo.

### <a name="sio_ideal_send_backlog_query-opcode-setting-o-t0"></a>SIO \_ IDEAL \_ SEND \_ BACKLOG QUERY \_ (configuración de código de operación: O, T==0)

Recupera el valor de trabajo pendiente de envío (ISB) ideal para la conexión subyacente.

Al enviar datos a través de una conexión TCP mediante sockets Windows, es importante mantener una cantidad suficiente de datos pendientes (enviados pero no reconocidos todavía) en TCP para lograr el máximo rendimiento. El valor ideal para la cantidad de datos pendientes para lograr el mejor rendimiento para la conexión TCP se denomina tamaño de trabajo pendiente de envío (ISB) ideal. El valor de ISB es una función del producto de retraso de ancho de banda de la conexión TCP y la ventana de recepción anunciada del receptor (y en parte la cantidad de congestión en la red).

El valor de ISB por conexión está disponible en la implementación del protocolo TCP en Windows Server 2008 y versiones posteriores. **Sio \_ IDEAL SEND \_ \_ BACKLOG \_ QUERY** IOCTL puede ser utilizado por una aplicación para consultar el valor de ISB para una conexión.

Para obtener información más detallada, consulte la referencia [**de SIO \_ IDEAL SEND \_ \_ BACKLOG \_ QUERY.**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85))

[**SIO \_ IDEAL \_ SEND \_ BACKLOG \_ QUERY**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85)) se admite en Windows Server 2008, Windows Vista con SP1 y versiones posteriores del sistema operativo.

### <a name="sio_keepalive_vals-opcode-setting-i-t3"></a>SIO \_ KEEPALIVE \_ VALS (configuración del código de operación: I, T==3)

Habilita o deshabilita la configuración por conexión de la **opción** de mantenimiento de TCP, que especifica el tiempo de espera y el intervalo de mantenimiento de TCP. Para obtener más información sobre la opción keep-alive, vea la sección 4.2.3.6 sobre los requisitos para hosts de *Internet:* capas de comunicación especificados en RFC 1122 disponible en el sitio web de [IETF](https://www.ietf.org/rfc/rfc1122.txt). (Este recurso solo puede estar disponible en inglés).

**SIO \_ KEEPALIVE \_ VALS** se puede usar para habilitar o deshabilitar los sondeos keep-alive y establecer el tiempo de espera y el intervalo de mantenimiento activo. El tiempo de espera de conexión continua especifica el tiempo de espera, en milisegundos, sin actividad hasta que se envía el primer paquete keep-alive. El intervalo de mantenimiento activo especifica el intervalo, en milisegundos, entre el momento en que se envían paquetes sucesivos de mantenimiento activo si no se recibe ninguna confirmación.

La [**opción \_ SO KEEPALIVE,**](so-keepalive.md) que es una de las opciones de socket de SOCKET DE [SOL, \_](sol-socket-socket-options.md)también se puede usar para habilitar o deshabilitar la conexión continua TCP en una conexión, así como para consultar el estado actual de esta opción. Para consultar si tcp keep-alive está habilitado en un socket, se puede llamar a la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) con la **opción SO \_ KEEPALIVE.** Para habilitar o deshabilitar tcp keep-alive, se puede llamar a la función [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con la [**opción SO \_ KEEPALIVE.**](so-keepalive.md) Si tcp keep-alive está habilitado con **SO \_ KEEPALIVE**, la configuración de TCP predeterminada se usa para el tiempo de espera y el intervalo de mantenimiento activo a menos que estos valores se hayan cambiado **mediante SIO \_ KEEPALIVE \_ VALS**.

Para obtener información más detallada, consulte la referencia [**de SIO \_ KEEPALIVE \_ VALS.**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) **SIO \_ KEEPALIVE \_ VALS se** admite en Windows 2000 y versiones posteriores.

### <a name="sio_loopback_fast_path-opcode-setting-i-t3"></a>SIO \_ LOOPBACK \_ FAST PATH \_ (configuración del código de operación: I, T==3)

Configura un socket TCP para una latencia más baja y operaciones más rápidas en la interfaz de bucle atrás. Esta IOCTL solicita que la pila TCP/IP use una ruta de acceso rápida especial para las operaciones de bucleback en este socket. [**SIO \_ LOOPBACK \_ FAST \_ PATH**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) IOCTL solo se puede usar con sockets TCP. Esta IOCTL debe usarse en ambos lados de la sesión de bucle atrás. La ruta de acceso rápida de bucle recuperación TCP se admite mediante la interfaz de bucle atrás IPv4 o IPv6. De forma predeterminada, **SIO \_ LOOPBACK \_ FAST \_ PATH** está deshabilitado.

Para obtener información más detallada, vea la referencia [**DE BUCLE DE BUCLE FAST PATH \_ \_ \_ de SIO.**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) **SIO \_ LOOPBACK \_ FAST \_ PATH** se admite en Windows 8, Windows Server 2012 y versiones posteriores.

### <a name="sio_multipoint_loopback-opcode-setting-v-t1"></a>SIO \_ MULTIPOINT \_ LOOPBACK (configuración de código de operación: V, T==1)

Controla si los datos enviados por una aplicación en el equipo local (no necesariamente por el mismo socket) de una sesión de multidifusión serán recibidos por un socket unido al grupo de destino de multidifusión en la interfaz de bucle atrás. Un valor **TRUE hace que** los datos de multidifusión enviados por una aplicación en el equipo local se entreguen a un socket de escucha en la interfaz de bucles bucles. Un valor **FALSE impide que** los datos de multidifusión enviados por una aplicación en el equipo local se entreguen a un socket de escucha en la interfaz de bucles bucles. De forma predeterminada, **SIO \_ MULTIPOINT \_ LOOPBACK** está habilitado.

### <a name="sio_multicast_scope-opcode-setting-i-t1"></a>ÁMBITO DE MULTIDIFUSIÓN DE SIO \_ \_ (configuración de código de operación: I, T==1)

Especifica el ámbito sobre el que se producirán las transmisiones de multidifusión. El ámbito se define como el número de segmentos de red enrutados que se va a cubrir. Un ámbito de cero indicaría que la transmisión de multidifusión no se colocaría en la conexión, pero se podría distribuir entre sockets dentro del host local. Un valor de ámbito de uno (el valor predeterminado) indica que la transmisión se colocará en la conexión, pero no atravesará ningún enrutador. Los valores de ámbito más altos determinan el número de enrutadores que se pueden atravesar. Tenga en cuenta que esto corresponde al parámetro de período de vida (TTL) en la multidifusión IP. De forma predeterminada, el ámbito es 1.

### <a name="sio_query_rss_processor_info-opcode-setting-o-t1"></a>SIO \_ QUERY RSS PROCESSOR INFO \_ \_ \_ (configuración del código de operación: O, T==1)

Consulta la asociación entre un socket y un núcleo de procesador RSS y un nodo NUMA.

[**SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) IOCTL devuelve una estructura DE AFINIDAD [**\_ DE \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) PROCESADOR DE SOCKET que contiene el NÚMERO DE PROCESADOR y el identificador de nodo NUMA. [**\_**](/windows/win32/api/winnt/ns-winnt-processor_number) La estructura **PROCESSOR \_ NUMBER devuelta** contiene un número de grupo y un número de procesador relativo dentro del grupo.

Para obtener información más detallada, consulte la referencia [**DE INFORMACIÓN DEL PROCESADOR RSS DE CONSULTA \_ \_ \_ \_ DE SIO.**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) **SIO \_ QUERY \_ RSS \_ PROCESSOR \_ INFO** se admite en Windows 8, Windows Server 2012 y versiones posteriores.

### <a name="sio_query_rss_scalability_info-opcode-setting-o-t3"></a>SIO \_ QUERY \_ RSS \_ SCALABILITY \_ INFO (opcode setting: O, T==3)

Las consultas descargan interfaces para la funcionalidad de escalado del lado de recepción (RSS). La estructura de argumentos devuelta para **SIO \_ QUERY RSS \_ \_ SCALABILITY \_ INFO** se especifica en la estructura **RSS \_ SCALABILITY \_ INFO** definida en el archivo de encabezado *Mstcpip.h.* Esta estructura se define de la siguiente manera:

```cpp
// Scalability info for the transport
typedef struct _RSS_SCALABILITY_INFO {
   BOOLEAN RssEnabled;
} RSS_SCALABILITY_INFO, *PRSS_SCALABILITY_INFO;
```

El valor devuelto en el **miembro RssEnabled** indica si RSS está habilitado en al menos una interfaz.

Si el búfer de salida no es lo suficientemente grande para la estructura **RSS \_ SCALABILITY \_ INFO** *(cbOutBuffer* es menor que el tamaño de una INFORMACIÓN DE ESCALABILIDAD **RSS) \_ \_** o el parámetro *lpvOutBuffer* es un puntero **NULL,** se devuelve **SOCKET \_ ERROR** como resultado de esta IOCTL y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [WSAEINVAL.](windows-sockets-error-codes-2.md)

En redes de alta velocidad en las que varias CPU residen dentro de un único sistema, la capacidad de la pila de protocolos de red para escalar bien en un sistema de varias CPU está inutilizable porque la arquitectura de NDIS 5.1 y versiones anteriores limita el procesamiento del protocolo de recepción a una sola CPU. El escalado en el lado de recepción (RSS) resuelve este problema al permitir que la carga de red de un adaptador de red se equilibre entre varias CPU.

**SIO \_ QUERY \_ RSS \_ SCALABILITY \_ INFO** se admite en Windows Vista y versiones posteriores.

### <a name="sio_query_transport_setting-opcode-setting-i-t3"></a>SIO \_ QUERY TRANSPORT SETTING \_ \_ (configuración del código de operación: I, T==3)

Consulta la configuración de transporte en un socket. La configuración de transporte que se consulta se basa en el identificador [**\_ de CONFIGURACIÓN DE \_ TRANSPORTE**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) pasado en *el parámetro lpvInBuffer.*

La única configuración de transporte que define actualmente es para la funcionalidad **\_ FUNCIONALIDAD DE NOTIFICACIÓN \_ \_ EN** TIEMPO REAL en un socket TCP.

Si el identificador DE CONFIGURACIÓN DE TRANSPORTE tiene el miembro **GUID** establecido en FUNCIONALIDAD DE NOTIFICACIÓN EN TIEMPO REAL, se trata de una solicitud para consultar la configuración de notificación en tiempo real del socket TCP usado con [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) para recibir notificaciones de red en segundo plano en una aplicación de Windows Store. **\_ \_ \_** [**\_ \_**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) Si la [**llamada a WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) o [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) es correcta, esta IOCTL devuelve una estructura DE SALIDA [**DE \_ \_ CONFIGURACIÓN \_ \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-real_time_notification_setting_input) DE NOTIFICACIÓN EN TIEMPO REAL con el estado actual.

Para obtener información más detallada, vea la referencia [**DE SIO \_ QUERY TRANSPORT \_ \_ SETTING.**](/previous-versions/windows/desktop/legacy/jj553483(v=vs.85)) **SIO \_ QUERY \_ TRANSPORT \_ SETTING** se admite en Windows 8, Windows Server 2012 y versiones posteriores.

### <a name="sio_query_wfp_ale_endpoint_handle-opcode-setting-o-t3"></a>SIO \_ QUERY \_ WFP \_ ALE ENDPOINT HANDLE \_ \_ (configuración de código de operación: O, T==3)

Consulta el identificador del punto de conexión de aplicación de cumplimiento de la capa de aplicación (ALE).

La plataforma Windows filtrado de datos (WFP) admite la inspección y modificación del tráfico de red. En Windows Vista, WFP se centra en escenarios en los que la máquina host es el punto de conexión de comunicación. En Windows Server 2008, sin embargo, hay implementaciones de firewall perimetral que le gustaría aprovechar la plataforma WFP para inspeccionar y proxy el tráfico de paso a través. El servidor de seguridad y aceleración de Internet (ISA) es un ejemplo de este tipo de dispositivo perimetral.

Hay algunos escenarios de firewall que pueden requerir la capacidad de insertar un paquete entrante en la ruta de acceso de envío asociada a un punto de conexión existente. Debe haber un mecanismo para detectar el identificador del punto de conexión de la capa de transporte asociado al punto de conexión de destino. La aplicación que creó el punto de conexión posee estos puntos de conexión de la capa de transporte. Esta IOCTL se usa para proporcionar el identificador de socket para la asignación del identificador del punto de conexión de la capa de transporte.

Si el búfer de salida no es lo suficientemente grande para el identificador del punto de conexión *(cbOutBuffer* es menor que el tamaño de **un UINT64)** o el parámetro *lpvOutBuffer* es un puntero **NULL,** se devuelve **SOCKET \_ ERROR** como resultado de esta IOCTL y [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [WSAEINVAL.](windows-sockets-error-codes-2.md)

**SIO \_ QUERY \_ WFP \_ ALE \_ ENDPOINT \_ HANDLE** se admite en Windows Vista y versiones posteriores.

### <a name="sio_query_wfp_connection_redirect_context-opcode-setting-i-t3"></a>SIO \_ QUERY \_ WFP \_ CONNECTION \_ REDIRECT \_ CONTEXT (opcode setting: I, T==3)

Consulta el contexto de redireccionamiento para un registro de redireccionamiento utilizado por un Windows de redirección de la plataforma de filtrado de filtros (WFP).

[**SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ \_ CONTEXT**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) IOCTL se usa para proporcionar seguimiento de conexiones con proxy en conexiones de socket redirigidas. Esta característica wfp facilita el seguimiento de los registros de redirección desde el redireccionamiento inicial de una conexión a la conexión final al destino.

Para obtener información más detallada, vea la referencia DE CONTEXTO DE REDIRECCIÓN [**\_ DE \_ CONEXIONES WFP \_ \_ \_ DE SIO QUERY.**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) **SIO \_ QUERY \_ WFP \_ CONNECTION REDIRECT \_ \_ CONTEXT** se admite en Windows 8, Windows Server 2012 y versiones posteriores.

### <a name="sio_query_wfp_connection_redirect_records-opcode-setting-i-t3"></a>SIO \_ QUERY \_ WFP \_ CONNECTION \_ REDIRECT \_ RECORDS (opcode setting: I, T==3)

Consulta el registro de redireccionamiento para la conexión TCP/IP aceptada para que la use un servicio de redirección Windows Filtering Platform (WFP).

[**SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ \_ RECORDS**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) IOCTL se usa para proporcionar seguimiento de conexiones con proxy en conexiones de socket redirigidas. Esta característica wfp facilita el seguimiento de los registros de redirección desde el redireccionamiento inicial de una conexión a la conexión final al destino.

Para obtener información más detallada, vea la referencia [**DE \_ SIO QUERY \_ WFP \_ CONNECTION REDIRECT \_ \_ RECORDS.**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) **SIO \_ QUERY \_ WFP \_ CONNECTION REDIRECT \_ \_ RECORDS** se admite en Windows 8, Windows Server 2012 y versiones posteriores.

### <a name="sio_rcvall-opcode-setting-i-t3"></a>SIO \_ RCVALL (configuración de código de operación: I, T==3)

Permite que un socket reciba todos los paquetes IPv4 o IPv6 que pasan una interfaz de red. El identificador de socket pasado a [**la función WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) debe ser uno de los siguientes:

-   Un socket IPv4 que se creó con la familia de direcciones establecida en AF INET, el tipo de socket establecido en SOCK RAW y el protocolo establecido en \_ \_ \_ IPPROTO IP.
-   Un socket IPv6 que se creó con la familia de direcciones establecida en AF INET6, el tipo de socket establecido en SOCK RAW y el protocolo establecido en \_ \_ IPPROTO \_ IPV6.

El socket también debe enlazarse a una interfaz IPv4 o IPv6 local explícita, lo que significa que no se puede enlazar a **INADDR \_ ANY** ni **a in6addr. \_**

En Windows Server 2008 y versiones anteriores, la configuración de IOCTL DE [**SIO \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) no capturaba paquetes locales enviados fuera de una interfaz de red. Esto incluía paquetes recibidos en otra interfaz y reenviaba la interfaz de red especificada para **LA IOCTL DE SIO \_ RCVALL.**

En Windows 7 y Windows Server 2008 R2 , esto se cambió para que también se capturan los paquetes locales enviados fuera de una interfaz de red. Esto incluye los paquetes recibidos en otra interfaz y, a continuación, se reenvía la interfaz de red enlazada al socket [**con SIO \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) IOCTL.

Establecer esta IOCTL requiere privilegios de administrador en el equipo local.

Esta característica se conoce a veces como modo promiscuo.

Los valores posibles de la opción **SIO \_ RCVALL** IOCTL se especifican en la enumeración **RCVALL \_ VALUE** definida en el archivo de encabezado *Mstcpip.h.* Los valores posibles para SIO \_ RCVALL son los siguientes:

| Término                                                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-|-|
| <span id="RCVALL_OFF"></span><span id="rcvall_off"></span>RCVALL \_ OFF<br/>                                     | Deshabilite esta opción para que un socket no reciba todos los paquetes IPv4 o IPv6 en la red. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RCVALL_ON"></span><span id="rcvall_on"></span>RCVALL \_ ON<br/>                                        | Habilite esta opción para que un socket reciba todos los paquetes IPv4 o IPv6 de la red. Esta opción habilita el modo promiscuo en la tarjeta de interfaz de red (NIC), si la NIC admite el modo promiscuo. En un segmento LAN con un centro de red, una NIC que admita el modo promiscuo capturará todo el tráfico IPv4 o IPv6 en la LAN, incluido el tráfico entre otros equipos en el mismo segmento de LAN. Todos los paquetes capturados (IPv4 o IPv6, según el socket) se entregarán al socket sin formato. <br/> Esta opción no capturará otros paquetes (paquetes ARP, IPX y NetBEUI, por ejemplo) en la interfaz.<br/> Netmon usa el mismo modo para la interfaz de red, pero no usa esta opción para capturar tráfico.<br/> |
| <span id="RCVALL_SOCKETLEVELONLY"></span><span id="rcvall_socketlevelonly"></span>RCVALL \_ SOCKETLEVELONLY<br/> | Esta característica no está implementada actualmente, por lo que establecer esta opción no tiene ningún efecto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="RCVALL_IPLEVEL"></span><span id="rcvall_iplevel"></span>RCVALL \_ IPLEVEL<br/>                         | Habilite esta opción para que un socket IPv4 o IPv6 reciba todos los paquetes en el nivel de IP de la red. Esta opción no habilita el modo promiscuo en la tarjeta de interfaz de red. Esta opción solo afecta al procesamiento de paquetes en el nivel de IP. La NIC todavía recibe solo paquetes dirigidos a sus direcciones de unidifusión y multidifusión configuradas. Sin embargo, un socket con esta opción habilitada no solo recibirá paquetes dirigidos a direcciones IP específicas, sino que recibirá todos los paquetes IPv4 o IPv6 que recibe la NIC.<br/> Esta opción no capturará otros paquetes (paquetes ARP, IPX y NetBEUI, por ejemplo) recibidos en la interfaz.<br/>                                                                                             |



 

Para obtener información más detallada, consulte la referencia [**de SIO \_ RCVALL.**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85))

**SIO \_ RCVALL se** admite en Windows 2000 y versiones posteriores.

### <a name="sio_rcvall_igmpmcast-opcode-setting-i-t3"></a>SIO \_ RCVALL \_ IGMPMCAST (configuración del código de operación: I, T==3)

Permite que un socket reciba todo el tráfico IP de multidifusión IGMP en la red, sin recibir otro tráfico IP de multidifusión. El identificador de socket pasado a la función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) debe ser de la familia de direcciones AF INET, el tipo de socket SOCK RAW y el \_ \_ protocolo \_ IPPROTO IGMP. El socket también debe enlazarse a una interfaz local explícita, lo que significa que no se puede enlazar a INADDR \_ ANY.

Una vez enlazado el socket y el conjunto de IOCTL, las llamadas a las funciones [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) o [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) devuelven datagramas IP de multidifusión que pasan a través de la interfaz dada. Tenga en cuenta que debe proporcionar un búfer lo suficientemente grande. Establecer esta IOCTL requiere privilegios de administrador en el equipo local.

**SIO \_ RCVALL \_ IGMPMCAST** se admite en Windows 2000 y versiones posteriores.

### <a name="sio_rcvall_mcast-opcode-setting-i-t3"></a>SIO \_ RCVALL \_ MCAST (configuración de código de operación: I, T==3)

Permite que un socket reciba todo el tráfico IP de multidifusión en la red (es decir, todos los paquetes IP destinados a direcciones IP en el intervalo de 224.0.0.0 a 239.255.255.255). El identificador de socket pasado a la función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) debe ser de la familia de direcciones AF INET, el tipo de socket SOCK RAW y el \_ protocolo UDP \_ IPPROTO. \_ El socket también debe enlazarse a una interfaz local explícita, lo que significa que no se puede enlazar a INADDR \_ ANY. El socket debe enlazarse al puerto cero.

Una vez enlazado el socket y el conjunto de IOCTL, las llamadas a las funciones [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) o [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) devuelven datagramas IP de multidifusión que pasan a través de la interfaz dada. Tenga en cuenta que debe proporcionar un búfer lo suficientemente grande. Establecer esta IOCTL requiere privilegios de administrador en el equipo local.

**SIO \_ RCVALL \_ MCAST se** admite en Windows 2000 y versiones posteriores.

### <a name="sio_release_port_reservation-opcode-setting-i-t3"></a>SIO \_ RELEASE PORT RESERVATION \_ \_ (configuración del código de operación: I, T==3)

Libera una reserva en tiempo de ejecución para un bloque de puertos TCP o UDP. La reserva en tiempo de ejecución que se va a liberar debe haber obtenido del proceso de emisión mediante [**SIO \_ ACQUIRE PORT \_ \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) IOCTL.

Para obtener información más detallada, consulte la referencia [**de SIO \_ RELEASE PORT \_ \_ RESERVATION.**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85))

[**SIO \_ RELEASE \_ PORT \_ RESERVATION se**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85)) admite en Windows Vista y versiones posteriores del sistema operativo.

### <a name="sio_routing_interface_change-opcode-setting-i-t1"></a>CAMBIO DE LA INTERFAZ DE ENRUTAMIENTO DE SIO \_ \_ \_ (configuración del código de operación: I, T==1)

Para recibir la notificación de un cambio de interfaz de enrutamiento que se debe usar para llegar a la dirección remota en el búfer de entrada (especificado como [**una estructura sockaddr).**](sockaddr-2.md) No se proporciona información de salida sobre la nueva interfaz de enrutamiento tras la finalización de esta IOCTL; la finalización simplemente indica que la interfaz de enrutamiento para un destino determinado ha cambiado y se debe consultar mediante LA CONSULTA DE LA INTERFAZ DE ENRUTAMIENTO DE **SIO \_ \_ \_** IOCTL.

Se supone, aunque no es necesario, que la aplicación usa E/S superpuestas para recibir una notificación del cambio de la interfaz de enrutamiento mediante la finalización de la solicitud DE CAMBIO DE LA INTERFAZ DE ENRUTAMIENTO **\_ \_ \_ DE SIO.** Como alternativa, si LA INTERFAZ DE ENRUTAMIENTO DE SIO CHANGE IOCTL se emite en un socket sin bloqueo con los parámetros *lpOverlapped* y *lpCompletionRoutine* establecidos en **NULL),** se completará la devolución inmediata y [WSAEWOULDBLOCK](windows-sockets-error-codes-2.md) como un error, y la aplicación puede esperar a que se enruten los eventos de cambio mediante la llamada a [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) o [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) con el bit CHANGE de LA INTERFAZ DE ENRUTAMIENTO de FD establecido en la máscara de bits del evento de **\_ \_ \_** \_ \_ \_ red.

Se reconoce que la información de enrutamiento permanece estable en la mayoría de los casos, por lo que exigir a la aplicación que mantenga varias E/SCL pendientes para obtener notificaciones sobre todos los destinos que le interesen, así como hacer que el proveedor de servicios realice un seguimiento de estas solicitudes de notificación usará una cantidad significativa de recursos del sistema. Esta situación se puede evitar ampliando el significado de los parámetros de entrada y relajando los requisitos del proveedor de servicios como se muestra a continuación:

-   La aplicación puede especificar una dirección comodín específica [](/windows/desktop/api/winsock/nf-winsock-bind) de la familia de protocolos (igual que la que se usa en la llamada de enlace al solicitar el enlace a cualquier dirección disponible) para solicitar notificaciones de los cambios de enrutamiento. Esto permite a la aplicación mantener solo un cambio de interfaz de enrutamiento de SIO pendiente para todos los sockets y destinos que tiene y, a continuación, usar **SIO \_ ROUTING INTERFACE \_ \_ QUERY** para obtener la información de enrutamiento real. **\_ \_ \_**
-   Un proveedor de servicios tiene la opción de omitir la información especificada por la aplicación en el búfer de entrada de **SIO \_ ROUTING INTERFACE \_ \_ CHANGE** (como si la aplicación especificase una dirección comodín) y completar el evento DE CAMBIO DE LA INTERFAZ DE ENRUTAMIENTO DE **SIO \_ \_ \_** IOCTL o señal FD ROUTING INTERFACE CHANGE en caso de cualquier cambio de información de enrutamiento (no solo la ruta al destino especificado en el búfer de \_ \_ \_ entrada).

### <a name="sio_routing_interface_query-opcode-setting-i-o-t1"></a>SIO \_ ROUTING INTERFACE QUERY \_ \_ (configuración de código de operación: I, O, T==1)

Para obtener la dirección de la interfaz local (representada como estructura [**sockaddr)**](sockaddr-2.md) que se debe usar para enviar a la dirección remota especificada en el búfer de entrada (como **sockaddr**). Las direcciones de multidifusión remotas se pueden enviar en el búfer de entrada para obtener la dirección de la interfaz preferida para la transmisión de multidifusión. En cualquier caso, la aplicación puede usar la dirección de interfaz devuelta en una solicitud bind() subsiguiente.

Tenga en cuenta que las rutas están sujetas a cambios. Por lo tanto, las aplicaciones no pueden confiar en la información devuelta por **SIO \_ ROUTING INTERFACE \_ \_ QUERY** para que sea persistente. Las aplicaciones pueden registrarse para enrutar las notificaciones de cambio a través de LA IOCTL CHANGE DE LA INTERFAZ DE ENRUTAMIENTO DE **SIO, \_ \_ \_** que proporciona la notificación a través de E/S superpuesta o un evento CHANGE de interfaz de enrutamiento \_ \_ de \_ FD. La siguiente secuencia de acciones se puede usar para garantizar que la aplicación siempre tiene información de la interfaz de enrutamiento actual para un destino determinado:

-   Problema de **CAMBIO DE LA INTERFAZ DE ENRUTAMIENTO \_ DE SIO \_ \_** IOCTL
-   Problema de **IOCTL de CONSULTA \_ DE LA INTERFAZ \_ DE \_ ENRUTAMIENTO** DE SIO
-   Cada **vez que SIO ROUTING INTERFACE \_ \_ \_ CHANGE** IOCTL notifica a la aplicación el cambio de enrutamiento (ya sea a través de E/S superpuesta o mediante la señalización del evento CHANGE de LA INTERFAZ DE ENRUTAMIENTO DE FD), se debe repetir toda la secuencia de \_ \_ \_ acciones.

Si el búfer de salida no es lo suficientemente grande como para contener la dirección de interfaz, se devuelve SOCKET ERROR como resultado de esta IOCTL y \_ [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [WSAEFAULT](windows-sockets-error-codes-2.md). El tamaño necesario del búfer de salida se devolverá *en lpcbBytesReturned* en este caso. Tenga en cuenta que también se devuelve el código de error de WSAEFAULT si el parámetro *lpvInBuffer*, *lpvOutBuffer* o *lpcbBytesReturned* no está totalmente contenido en una parte válida del espacio de direcciones del usuario.

Si no se puede acceder a la dirección de destino especificada en el búfer de entrada a través de cualquiera de las interfaces disponibles, SOCKET ERROR se devuelve como resultado de esta IOCTL y \_ [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [WSAENETUNREACH](windows-sockets-error-codes-2.md) o [incluso WSAENETDOWN](windows-sockets-error-codes-2.md) si se pierde toda la conectividad de red.

### <a name="sio_set_compatibility_mode-opcode-setting-i-t3"></a>SIO \_ SET COMPATIBILITY MODE \_ \_ (configuración de código de operación: I, T==3)

Solicita cómo la pila de redes debe controlar determinados comportamientos para los que la manera predeterminada de controlar el comportamiento puede diferir en Windows versiones. La estructura de argumentos **para SIO \_ SET COMPATIBILITY \_ \_ MODE** se especifica en la estructura **WSA \_ COMPATIBILITY \_ MODE** definida en el archivo de encabezado *Mswsockdef.h.* Esta estructura se define de la siguiente manera:

```cpp
/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

El valor especificado en el miembro **BehaviorId** indica el comportamiento solicitado. El valor especificado en el **miembro TargetOsVersion** indica la Windows que se solicita para el comportamiento.

El **miembro BehaviorId** puede ser uno de los valores del tipo de enumeración ID DE COMPORTAMIENTO DE COMPATIBILIDAD de **WSA \_ \_ \_** definido en el archivo de encabezado *Mswsockdef.h.* Los valores posibles para el **miembro BehaviorId** son los siguientes.

| Término                                                                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-|-|
| <span id="WsaBehaviorAll"></span><span id="wsabehaviorall"></span><span id="WSABEHAVIORALL"></span>WsaBehaviorAll<br/>                                                     | Esto equivale a solicitar todos los posibles comportamientos compatibles definidos para el identificador de COMPORTAMIENTO DE COMPATIBILIDAD **\_ \_ de \_ WSA.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="WsaBehaviorReceiveBuffering"></span><span id="wsabehaviorreceivebuffering"></span><span id="WSABEHAVIORRECEIVEBUFFERING"></span>WsaBehaviorReceiveBuffering<br/> | Cuando el miembro **TargetOsVersion** se establece en un valor para Windows Vista o posterior, se permiten reducciones en el tamaño del búfer de recepción TCP en este socket mediante la opción de socket **SO \_ RCVBUF** incluso después de que se haya establecido una conexión TCP. <br/> Cuando el miembro **TargetOsVersion** se establece en un valor anterior a Windows Vista, no se permiten reducciones en el tamaño del búfer de recepción TCP en este socket mediante la opción de socket **\_ SO RCVBUF** después del establecimiento de la conexión. <br/>                                                                                                                                                                                  |
| <span id="WsaBehaviorAutoTuning"></span><span id="wsabehaviorautotuning"></span><span id="WSABEHAVIORAUTOTUNING"></span>WsaBehaviorAutoTuning<br/>                         | Cuando el **miembro TargetOsVersion** se establece en un valor para Windows Vista o posterior, se habilita el ajuste automático de la ventana de recepción y el factor de escala de la ventana TCP se reduce a 2 desde el valor predeterminado de 8.<br/> Cuando **TargetOsVersion se** establece en un valor anterior a Windows Vista, se deshabilita el ajuste automático de la ventana de recepción. La opción de escalado de ventanas TCP también está deshabilitada y el tamaño máximo de la ventana de recepción verdadera está limitado a 65 535 bytes. La opción de escalado de ventana TCP no se puede negociar en la conexión aunque se llamó a la opción de socket **SO \_ RCVBUF** en este socket especificando un valor superior a 65 535 bytes antes de establecer la conexión.<br/> |



 

Para obtener información más detallada, consulte la referencia [**de SIO \_ SET COMPATIBILITY \_ \_ MODE.**](/previous-versions/windows/desktop/legacy/cc136103(v=vs.85))

**SIO \_ SET \_ COMPATIBILITY \_ MODE se** admite en Windows Vista y versiones posteriores.

### <a name="sio_set_group_qos-opcode-setting-i-t1"></a>SIO \_ SET \_ GROUP \_ QOS (configuración de código de operación: I, T==1)

Reservado.

### <a name="sio_set_priority_hint-opcode-setting-i-t3"></a>SIO_SET_PRIORITY_HINT (configuración del código de operación: I, T==3)

Proporciona una sugerencia al protocolo de transporte subyacente para tratar el tráfico en este socket con una prioridad específica. *lpvInBuffer debe* apuntar a una variable de tipo **PRIORITY_HINT** *con cbInBuffer* establecido en sizeof(PRIORITY_HINT). Los *parámetros lpvOutBuffer* y *cbOutBuffer* deben ser **NULL** y 0, respectivamente. La implementación Windows TCP de Microsoft admite esta IOCTL a partir Windows 10, versión 1809 (10.0; Compilación 17763) y versiones posteriores como sigue: cuando el valor de prioridad solicitado se establece en **IoPriorityHintVeryLow,** TCP usa una versión modificada del algoritmo LEDBAT (definido en RFC 6817) para controlar la velocidad de tráfico saliente en el socket. El tráfico entrante no se ve afectado por esta IOCTL. LEDBAT es un algoritmo de búsqueda y su objetivo es mantener la latencia baja y evitar cualquier efecto adverso en el tráfico de prioridad normal al salir del camino cuando el tráfico de prioridad normal está presente.

Consulte también [RFC 6817.](https://tools.ietf.org/html/rfc6817)

**SIO_SET_PRIORITY_HINT** se admite en Windows 10, versión 1809 (10.0; Compilación 17763) y versiones posteriores.

### <a name="sio_set_qos-opcode-setting-i-t1"></a>SIO \_ SET \_ QOS (configuración de código de operación: I, T==1)

Asocie la estructura [**de QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) especificada al socket. No se requiere ningún búfer de salida, la **estructura qos** se obtendrá del búfer de entrada. El código de error [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) se indica para los proveedores de servicios que no admiten la calidad de servicio.

### <a name="sio_tcp_initial_rto-opcode-setting-i-t3"></a>SIO_TCP_INITIAL_RTO (configuración del código de operación: I, T==3)

Controla las características iniciales de retransmisión (SYN/SYN+ACK) de un socket TCP mediante la configuración de parámetros de tiempo de espera de retransmisión inicial (RTO). Los parámetros de configuración se especifican en una [**estructura \_ TCP INITIAL \_ RTO \_ PARAMETERS.**](/windows/desktop/api/mswsock/ns-mswsock-transmit_file_buffers)

Para obtener información más detallada, consulte [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) referencia. [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) se admite en Windows 8, Windows Server 2012 y versiones posteriores.

### <a name="sio_timestamping"></a>SIO_TIMESTAMPING

Una IOCTL de socket usada para configurar la recepción de marcas de tiempo de transmisión/recepción de sockets. Solo es válido para sockets de datagramas. El tipo de entrada **para SIO_TIMESTAMPING** es la [**TIMESTAMPING_CONFIG**](/windows/win32/api/mstcpip/ns-mstcpip-timestamping_config) estructura.

Consulte también [Marca de tiempo de Winsock.](/windows/win32/winsock/winsock-timestamping)

### <a name="sio_translate_handle-opcode-setting-i-o-t1"></a>SIO \_ TRANSLATE \_ HANDLE (configuración de código de operación: I, O, T==1)

Para obtener un identificador correspondiente para *sockets* que sea válido en el contexto de una interfaz complementaria (por ejemplo, TH \_ NETDEV y TH \_ TAPI). En el búfer de entrada se especifica una constante de manifiesto que identifica la interfaz complementaria junto con cualquier otro parámetro necesario. El identificador correspondiente estará disponible en el búfer de salida tras la finalización de esta función. Consulte la sección adecuada de [Los anexos de Winsock](winsock-annexes.md) para obtener detalles específicos de una interfaz complementaria determinada. El código de error [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) se indica para los proveedores de servicios que no admiten esta IOCTL para la interfaz complementaria especificada. Esta IOCTL recupera el identificador asociado mediante **SIO \_ TRANSLATE \_ HANDLE**.

Se recomienda usar el Modelo de objetos componentes (COM) en lugar de esta IOCTL para detectar y realizar un seguimiento de otras interfaces que podrían ser compatibles con un socket. Esta IOCTL está presente por compatibilidad con versiones anteriores con sistemas en los que COM no está disponible o no se puede usar por alguna otra razón.

### <a name="sio_udp_connreset-opcode-setting-i-t3"></a>SIO \_ UDP \_ CONNRESET (configuración de código de operación: I, T==3)

**Windows XP:** Controla si se notifican mensajes UDP PORT \_ UNREACHABLE. Establezca en **TRUE para** habilitar los informes. Establezca en **FALSE para** deshabilitar los informes.

### <a name="sio_set_wfp_connection_redirect_records-opcode-setting-i-t3"></a>SIO \_ SET \_ WFP \_ CONNECTION \_ REDIRECT \_ RECORDS (opcode setting: I, T==3)

Establece el registro de redirección en el nuevo socket TCP usado para conectarse al destino final para que lo use un servicio de redirección de Windows Filtering Platform (WFP).

[**SIO \_ SET \_ WFP \_ CONNECTION REDIRECT \_ \_ RECORDS**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) IOCTL se usa como parte del seguimiento de conexiones con proxy en conexiones de socket redirigidas. Esta característica wfp facilita el seguimiento de los registros de redirección desde el redireccionamiento inicial de una conexión a la conexión final al destino.

Para obtener información más detallada, vea la referencia [**DE \_ SIO SET \_ WFP \_ CONNECTION REDIRECT \_ \_ RECORDS.**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) **SIO \_ SET \_ WFP \_ CONNECTION REDIRECT \_ \_ RECORDS** se admite en Windows 8, Windows Server 2012 y versiones posteriores.

### <a name="sio_tcp_info-opcode-setting-i-o-t3"></a>SIO \_ TCP \_ INFO (configuración del código de operación: I, O, T==3)

Recupera las estadísticas TCP de un socket. Las estadísticas tcp se proporcionan en una [**estructura \_ TCP INFO \_ v0.**](/windows/desktop/api/Mstcpip/ns-mstcpip-tcp_info_v0)

A diferencia de la recuperación de estadísticas TCP con la función [**GetPerTcpConnectionEStats,**](/windows/win32/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) la recuperación de estadísticas TCP con este código de control no requiere que el código de usuario cargue, almacene y filtre la tabla de conexión TCP, y no requiere privilegios elevados para su uso.

Para obtener más información, [**vea SIO \_ TCP \_ INFO**](/previous-versions/windows/desktop/legacy/mt823415(v=vs.85)). **SIO \_ TCP \_ INFO** se admite en Windows 10 versión 1703, Windows Server 2016 y versiones posteriores.

## <a name="remarks"></a>Comentarios

Las ioctls de Winsock se definen en una serie de archivos de encabezado diferentes. Estos incluyen el *archivo de encabezado Winsock2.h,* *Mswsock.h* y *Mstcpip.h.*

En el Kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y también se definen varias ioctls de Winsock en los archivos de encabezado *Ws2def.h,* *Ws2ipdef.h y* *Mswsockdef.h.* El archivo de encabezado *Winsock2.h* incluye automáticamente el archivo de encabezado *Ws2def.h.* El *archivo de encabezado Ws2tcpip.h* incluye automáticamente el archivo de encabezado *Ws2tcpip.h.* El *archivo de encabezado Mswsockdef.h* se incluye automáticamente en el archivo de encabezado *Mswsockdef.h.*

## <a name="requirements"></a>Requisitos

|Requisito|Value|
|-|-|
| Encabezado<br/> | <dl> <dt>Winsock2.h;</dt> <dt>Mstcpip.h;</dt> <dt>Mswsock.h;</dt> <dt>Mswsockdef.h en Windows Vista, Windows Server 2008 y Windows 7 (incluya Mswsock.h);</dt> <dt>Ws2def.h en Windows Vista, Windows Server 2008 y Windows 7 (incluye Winsock2.h);</dt> <dt>Ws2ipdef.h en Windows Vista, Windows Server 2008 y Windows 7 (incluido Ws2tcpip.h)</dt> </dl> |
