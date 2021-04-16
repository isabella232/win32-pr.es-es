---
description: Códigos de error de Windows Sockets (Winsock) devueltos por la función WSAGetLastError.
ms.assetid: 50b924f3-2c88-443b-8a90-4293fe5c3048
title: Códigos de error de Windows Sockets (WinSock2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c251d63872c05623a6d1c9e3820edd2d8f670e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718937"
---
# <a name="windows-sockets-error-codes"></a>Códigos de error de Windows Sockets

La mayoría de las funciones de Windows Sockets 2 no devuelven la causa específica de un error cuando la función devuelve. Para obtener más información, consulte el tema [control de errores de Winsock](handling-winsock-errors.md) .

La función [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve el último error que se produjo para el subproceso que realiza la llamada. Cuando una función de Windows Sockets determinada indica que se ha producido un error, se debe llamar a esta función inmediatamente para recuperar el código de error extendido de la llamada a la función con errores. Estos códigos de error y una breve descripción de texto asociada a un código de error se definen en el archivo de encabezado *Winerror. h* . La función [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) se puede usar para obtener la cadena de mensaje para el error devuelto.

Para obtener información sobre cómo controlar los códigos de error al trasladar aplicaciones de socket a Winsock, consulte [códigos de error: errno, h \_ errno y WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md).

En la lista siguiente se describen los posibles códigos de error devueltos por la función [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) . Los errores se muestran en orden numérico con el nombre de la macro de error. Algunos códigos de error definidos en el archivo de encabezado *WinSock2. h* no se devuelven desde ninguna función.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Código o valor devuelto</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="WSA_INVALID_HANDLE"></span><span id="wsa_invalid_handle"></span><dl> <dt><strong>WSA_INVALID_HANDLE</strong></dt> <dt>6</dt> </dl></td>
<td><dl> <dt><span id="Specified_event_object_handle_is_invalid."></span><span id="specified_event_object_handle_is_invalid."></span><span id="SPECIFIED_EVENT_OBJECT_HANDLE_IS_INVALID."></span>El identificador del objeto de evento especificado no es válido.</dt> <dd> Una aplicación intenta usar un objeto de evento, pero el identificador especificado no es válido.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span><dl> <dt><strong>WSA_NOT_ENOUGH_MEMORY</strong></dt> <dt>8</dt> </dl></td>
<td><dl> <dt><span id="Insufficient_memory_available."></span><span id="insufficient_memory_available."></span><span id="INSUFFICIENT_MEMORY_AVAILABLE."></span>Memoria insuficiente.</dt> <dd> Una aplicación utiliza una función de Windows Sockets que se asigna directamente a una función de Windows. La función de Windows indica una falta de recursos de memoria necesarios.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_INVALID_PARAMETER"></span><span id="wsa_invalid_parameter"></span><dl> <dt><strong>WSA_INVALID_PARAMETER</strong></dt> <dt>87</dt> </dl></td>
<td><dl> <dt><span id="One_or_more_parameters_are_invalid."></span><span id="one_or_more_parameters_are_invalid."></span><span id="ONE_OR_MORE_PARAMETERS_ARE_INVALID."></span>Uno o más parámetros no son válidos.</dt> <dd> Una aplicación usó una función de Windows Sockets que se asigna directamente a una función de Windows. La función de Windows indica un problema con uno o más parámetros.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span><dl> <dt><strong>WSA_OPERATION_ABORTED</strong></dt> <dt>995</dt> </dl></td>
<td><dl> <dt><span id="Overlapped_operation_aborted."></span><span id="overlapped_operation_aborted."></span><span id="OVERLAPPED_OPERATION_ABORTED."></span>Operación superpuesta anulada.</dt> <dd> Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando SIO_FLUSH en <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_IO_INCOMPLETE"></span><span id="wsa_io_incomplete"></span><dl> <dt><strong>WSA_IO_INCOMPLETE</strong></dt> <dt>996</dt> </dl></td>
<td><dl> <dt><span id="Overlapped_I_O_event_object_not_in_signaled_state."></span><span id="overlapped_i_o_event_object_not_in_signaled_state."></span><span id="OVERLAPPED_I_O_EVENT_OBJECT_NOT_IN_SIGNALED_STATE."></span>El objeto de evento de e/s superpuesto no está en el estado señalado.</dt> <dd> La aplicación ha intentado determinar el estado de una operación superpuesta que todavía no se ha completado. Las aplicaciones que usan <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult"><strong>WSAGetOverlappedResult</strong></a> (con la marca <em>FWait</em> establecida en <strong>false</strong>) en un modo de sondeo para determinar cuándo se ha completado una operación superpuesta, obtienen este código de error hasta que se complete la operación.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_IO_PENDING"></span><span id="wsa_io_pending"></span><dl> <dt><strong>WSA_IO_PENDING</strong></dt> <dt>997</dt> </dl></td>
<td>Las operaciones superpuestas se completarán más adelante. <br/> <dl> <dt><span></span></dt> <dd> La aplicación ha iniciado una operación superpuesta que no se puede finalizar inmediatamente. Después de completar la operación, se proporcionará una indicación de finalización.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINTR"></span><span id="wsaeintr"></span><dl> <dt><strong>WSAEINTR</strong></dt> <dt>10004</dt> </dl></td>
<td><dl> <dt><span id="Interrupted_function_call."></span><span id="interrupted_function_call."></span><span id="INTERRUPTED_FUNCTION_CALL."></span>Llamada de función interrumpida.</dt> <dd> Una operación de bloqueo fue interrumpida por una llamada a <a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEBADF"></span><span id="wsaebadf"></span><dl> <dt><strong>WSAEBADF</strong></dt> <dt>10009</dt> </dl></td>
<td><dl> <dt><span id="File_handle_is_not_valid."></span><span id="file_handle_is_not_valid."></span><span id="FILE_HANDLE_IS_NOT_VALID."></span>El identificador de archivo no es válido.</dt> <dd> El identificador de archivo proporcionado no es válido. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEACCES"></span><span id="wsaeacces"></span><dl> <dt><strong>WSAEACCES</strong></dt> <dt>10013</dt> </dl></td>
<td><dl> <dt><span id="Permission_denied."></span><span id="permission_denied."></span><span id="PERMISSION_DENIED."></span>Permiso denegado.</dt> <dd> Se intentó tener acceso a un socket de una manera prohibida por sus permisos de acceso. Un ejemplo es el uso de una dirección de difusión para <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a> sin permiso de difusión que se establece mediante el uso de <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>r (SO_BROADCAST</strong></a>). <br/> Otro posible motivo del error WSAEACCES es que, cuando se llama a la función de <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>enlace</strong></a> (en Windows NT 4,0 con SP4 y versiones posteriores), otra aplicación, servicio o controlador de modo kernel se enlaza a la misma dirección con acceso exclusivo. Este acceso exclusivo es una característica nueva de Windows NT 4,0 con SP4 y versiones posteriores, y se implementa mediante la opción <a href="/windows/desktop/winsock/so-exclusiveaddruse">SO_EXCLUSIVEADDRUSE</a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEFAULT"></span><span id="wsaefault"></span><dl> <dt><strong>WSAEFAULT</strong></dt> <dt>10014</dt> </dl></td>
<td><dl> <dt><span id="Bad_address."></span><span id="bad_address."></span><span id="BAD_ADDRESS."></span>Dirección incorrecta.</dt> <dd> El sistema detectó una dirección de puntero no válida al intentar utilizar un argumento de puntero de una llamada. Este error se produce si una aplicación pasa un valor de puntero no válido o si la longitud del búfer es demasiado pequeña. Por ejemplo, si la longitud de un argumento, que es una estructura <a href="/windows/desktop/winsock/sockaddr-2"><strong>sockaddr</strong></a> , es menor que el sizeof (sockaddr).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINVAL"></span><span id="wsaeinval"></span><dl> <dt><strong>WSAEINVAL</strong></dt> <dt>10022</dt> </dl></td>
<td><dl> <dt><span id="Invalid_argument."></span><span id="invalid_argument."></span><span id="INVALID_ARGUMENT."></span>Argumento no válido.</dt> <dd> Se ha proporcionado algún argumento no válido (por ejemplo, especificando un nivel no válido para la función de la función de la <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>función de la</strong></a> función de la En algunos casos, también hace referencia al estado actual del socket, por ejemplo, al llamar a <a href="/windows/desktop/api/Winsock2/nf-winsock2-accept"><strong>Accept</strong></a> en un socket que no está escuchando.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEMFILE"></span><span id="wsaemfile"></span><dl> <dt><strong>WSAEMFILE</strong></dt> <dt>10024</dt> </dl></td>
<td><dl> <dt><span id="Too_many_open_files."></span><span id="too_many_open_files."></span><span id="TOO_MANY_OPEN_FILES."></span>Demasiados archivos abiertos.</dt> <dd> Demasiados Sockets abiertos. Cada implementación puede tener un número máximo de identificadores de socket disponibles, ya sea globalmente, por proceso o por subproceso.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span><dl> <dt><strong>WSAEWOULDBLOCK</strong></dt> <dt>10035</dt> </dl></td>
<td><dl> <dt><span id="Resource_temporarily_unavailable."></span><span id="resource_temporarily_unavailable."></span><span id="RESOURCE_TEMPORARILY_UNAVAILABLE."></span>El recurso no está disponible temporalmente.</dt> <dd> Este error se devuelve de operaciones en sockets que no son de bloqueo y que no se pueden completar inmediatamente, <a href="/windows/desktop/api/winsock/nf-winsock-recv"><strong>por ejemplo,</strong></a> cuando no hay datos en la cola que se van a leer del socket. Es un error no irrecuperable y la operación se debe volver a intentar más tarde. Es normal que WSAEWOULDBLOCK se notifique como el resultado de llamar a <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>Connect</strong></a> en un socket de SOCK_STREAM no bloqueado, ya que debe transcurrir algún tiempo para que se establezca la conexión.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span><dl> <dt><strong>WSAEINPROGRESS</strong></dt> <dt>10036</dt> </dl></td>
<td><dl> <dt><span id="Operation_now_in_progress."></span><span id="operation_now_in_progress."></span><span id="OPERATION_NOW_IN_PROGRESS."></span>Operación en curso.</dt> <dd> Se está ejecutando una operación de bloqueo actualmente. Windows Sockets solo permite que una única operación de bloqueo (por tarea o subproceso) esté pendiente y, si se realiza cualquier otra llamada de función (tanto si hace referencia a esa como a cualquier otro socket), se produce un error en la función con el error WSAEINPROGRESS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEALREADY"></span><span id="wsaealready"></span><dl> <dt><strong>WSAEALREADY</strong></dt> <dt>10037</dt> </dl></td>
<td><dl> <dt><span id="Operation_already_in_progress."></span><span id="operation_already_in_progress."></span><span id="OPERATION_ALREADY_IN_PROGRESS."></span>La operación ya está en curso.</dt> <dd> Se intentó realizar una operación en un socket de no bloqueo con una operación que ya está en curso; es decir, se <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>está llamando a</strong></a> una segunda vez en un socket sin bloqueo que ya se está conectando, o bien se está cancelando una solicitud asincrónica (<strong>WSAAsyncGetXbyY</strong>) que ya se ha cancelado o completado.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span><dl> <dt><strong>WSAENOTSOCK</strong></dt> <dt>10038</dt> </dl></td>
<td><dl> <dt><span id="Socket_operation_on_nonsocket."></span><span id="socket_operation_on_nonsocket."></span><span id="SOCKET_OPERATION_ON_NONSOCKET."></span>Operación de socket en nonsocket.</dt> <dd> Se intentó realizar una operación en algo que no es un socket. El parámetro de identificador de Socket no hizo referencia a un socket válido, o bien para <a href="/windows/desktop/api/Winsock2/nf-winsock2-select"><strong>Select</strong></a>, un miembro de un <strong>fd_set</strong> no era válido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span><dl> <dt><strong>WSAEDESTADDRREQ</strong></dt> <dt>10039</dt> </dl></td>
<td><dl> <dt><span id="Destination_address_required."></span><span id="destination_address_required."></span><span id="DESTINATION_ADDRESS_REQUIRED."></span>Se requiere la dirección de destino.</dt> <dd> Se ha omitido una dirección necesaria de una operación en un socket. Por ejemplo, este error se devuelve si se llama a <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a> con la dirección remota de ADDR_ANY.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span><dl> <dt><strong>WSAEMSGSIZE</strong></dt> <dt>10040</dt> </dl></td>
<td><dl> <dt><span id="Message_too_long."></span><span id="message_too_long."></span><span id="MESSAGE_TOO_LONG."></span>Mensaje demasiado largo.</dt> <dd> Un mensaje enviado en un socket de datagrama era más grande que el búfer de mensajes interno u otro límite de red, o bien el búfer usado para recibir un datagrama era más pequeño que el propio datagrama.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span><dl> <dt><strong>WSAEPROTOTYPE</strong></dt> <dt>10041</dt> </dl></td>
<td><dl> <dt><span id="Protocol_wrong_type_for_socket."></span><span id="protocol_wrong_type_for_socket."></span><span id="PROTOCOL_WRONG_TYPE_FOR_SOCKET."></span>Tipo de protocolo incorrecto para el socket.</dt> <dd> Se especificó un protocolo en la llamada de función de <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>socket</strong></a> que no admite la semántica del tipo de socket solicitado. Por ejemplo, el protocolo UDP de Internet de ARPA no se puede especificar con un tipo de socket de SOCK_STREAM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span><dl> <dt><strong>WSAENOPROTOOPT</strong></dt> <dt>10042</dt> </dl></td>
<td><dl> <dt><span id="Bad_protocol_option."></span><span id="bad_protocol_option."></span><span id="BAD_PROTOCOL_OPTION."></span>Opción de protocolo incorrecto.</dt> <dd> Se especificó una opción o un nivel desconocido, no válido o no admitido en <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>una llamada a</strong></a> <a href="/windows/desktop/api/winsock/nf-winsock-getsockopt"><strong>getsockopt</strong></a> o a un método.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span><dl> <dt><strong>WSAEPROTONOSUPPORT</strong></dt> <dt>10043</dt> </dl></td>
<td><dl> <dt><span id="Protocol_not_supported."></span><span id="protocol_not_supported."></span><span id="PROTOCOL_NOT_SUPPORTED."></span>Protocolo no compatible.</dt> <dd> El protocolo solicitado no se ha configurado en el sistema o no existe ninguna implementación para él. Por ejemplo, una llamada de <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>socket</strong></a> solicita un socket SOCK_DGRAM, pero especifica un protocolo de secuencia.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span><dl> <dt><strong>WSAESOCKTNOSUPPORT</strong></dt> <dt>10044</dt> </dl></td>
<td><dl> <dt><span id="Socket_type_not_supported."></span><span id="socket_type_not_supported."></span><span id="SOCKET_TYPE_NOT_SUPPORTED."></span>Tipo de Socket no compatible.</dt> <dd> Esta familia de direcciones no es compatible con el tipo de socket especificado. Por ejemplo, el tipo opcional SOCK_RAW puede estar seleccionado en una llamada de <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>socket</strong></a> y la implementación no admite sockets de SOCK_RAW.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span><dl> <dt><strong>WSAEOPNOTSUPP</strong></dt> <dt>10045</dt> </dl></td>
<td><dl> <dt><span id="Operation_not_supported."></span><span id="operation_not_supported."></span><span id="OPERATION_NOT_SUPPORTED."></span>Operación no admitida.</dt> <dd> La operación intentada no se admite para el tipo de objeto al que se hace referencia. Normalmente esto sucede cuando un descriptor de socket a un socket que no admite esta operación está intentando aceptar una conexión en un socket de datagrama.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span><dl> <dt><strong>WSAEPFNOSUPPORT</strong></dt> <dt>10046</dt> </dl></td>
<td><dl> <dt><span id="Protocol_family_not_supported."></span><span id="protocol_family_not_supported."></span><span id="PROTOCOL_FAMILY_NOT_SUPPORTED."></span>Familia de protocolos no admitida.</dt> <dd> La familia de protocolos no se ha configurado en el sistema o no existe ninguna implementación para ella. Este mensaje tiene un significado ligeramente diferente de WSAEAFNOSUPPORT. Sin embargo, es intercambiable en la mayoría de los casos, y todas las funciones de Windows Sockets que devuelven uno de estos mensajes también especifican WSAEAFNOSUPPORT.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span><dl> <dt><strong>WSAEAFNOSUPPORT</strong></dt> <dt>10047</dt> </dl></td>
<td><dl> <dt><span id="Address_family_not_supported_by_protocol_family."></span><span id="address_family_not_supported_by_protocol_family."></span><span id="ADDRESS_FAMILY_NOT_SUPPORTED_BY_PROTOCOL_FAMILY."></span>Familia de direcciones no compatible con la familia de protocolos.</dt> <dd> Se usó una dirección no compatible con el protocolo solicitado. Todos los sockets se crean con una familia de direcciones asociada (es decir, AF_INET para protocolos de Internet) y un tipo de protocolo genérico (es decir, SOCK_STREAM). Este error se devuelve si se solicita explícitamente un protocolo incorrecto en la llamada de <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>socket</strong></a> , o si se usa una dirección de la familia equivocada para un socket, por ejemplo, en <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span><dl> <dt><strong>WSAEADDRINUSE</strong></dt> <dt>10048</dt> </dl></td>
<td><dl> <dt><span id="Address_already_in_use."></span><span id="address_already_in_use."></span><span id="ADDRESS_ALREADY_IN_USE."></span>La dirección ya está en uso.</dt> <dd> Normalmente, solo se permite un uso de cada dirección de socket (protocolo/dirección IP/puerto). Este error se produce si una aplicación intenta <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>enlazar</strong></a> un socket a una dirección o puerto IP que ya se ha utilizado para un socket existente, o un socket que no se ha cerrado correctamente o que todavía está en proceso de cierre. En el caso de las aplicaciones de servidor que necesitan <strong>enlazar</strong> varios Sockets al mismo número de puerto, considere la posibilidad <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>de usar el</strong></a> valor de la SO_REUSEADDR. Normalmente, las aplicaciones cliente no necesitan llamar a <strong>BIND</strong> en absoluto;<a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>conectar</strong></a> elige un puerto no utilizado automáticamente. Cuando se llama a <strong>BIND</strong> con una dirección comodín (que implica ADDR_ANY), se puede retrasar un error WSAEADDRINUSE hasta que se confirme la dirección específica. Esto podría ocurrir con una llamada a otra función más adelante, como <strong>Connect</strong>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-listen"><strong>Listen</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect"><strong>WSAConnect</strong></a>o <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf"><strong>WSAJoinLeaf</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span><dl> <dt><strong>WSAEADDRNOTAVAIL</strong></dt> <dt>10049</dt> </dl></td>
<td><dl> <dt><span id="Cannot_assign_requested_address."></span><span id="cannot_assign_requested_address."></span><span id="CANNOT_ASSIGN_REQUESTED_ADDRESS."></span>No se puede asignar la dirección solicitada.</dt> <dd> La dirección solicitada no es válida en su contexto. Esto suele ser el resultado de un intento de <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>enlazar</strong></a> a una dirección que no es válida para el equipo local. Esto también puede ser el resultado de <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>Connect</strong></a>, <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect"><strong>WSAConnect</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf"><strong>WSAJoinLeaf</strong></a>o <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsasendto"><strong>WSASendTo</strong></a> cuando la dirección remota o el puerto no son válidos para un equipo remoto (por ejemplo, la dirección o el puerto 0).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span><dl> <dt><strong>WSAENETDOWN</strong></dt> <dt>10050</dt> </dl></td>
<td><dl> <dt><span id="Network_is_down."></span><span id="network_is_down."></span><span id="NETWORK_IS_DOWN."></span>La red está inactiva.</dt> <dd> Una operación de socket encontró una red inactiva. Esto podría indicar un fallo serio del sistema de red (es decir, la pila de protocolo que desborda el DLL de Windows Sockets), la interfaz de red o la red local en sí.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span><dl> <dt><strong>WSAENETUNREACH</strong></dt> <dt>10051</dt> </dl></td>
<td><dl> <dt><span id="Network_is_unreachable."></span><span id="network_is_unreachable."></span><span id="NETWORK_IS_UNREACHABLE."></span>No se puede tener acceso a la red.</dt> <dd> Se intentó realizar una operación de socket en una red inaccesible. Normalmente, esto significa que el software local sabe que no hay ninguna ruta para llegar al host remoto.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENETRESET"></span><span id="wsaenetreset"></span><dl> <dt><strong>WSAENETRESET</strong></dt> <dt>10052</dt> </dl></td>
<td><dl> <dt><span id="Network_dropped_connection_on_reset."></span><span id="network_dropped_connection_on_reset."></span><span id="NETWORK_DROPPED_CONNECTION_ON_RESET."></span>Conexión de red quitada al restablecer.</dt> <dd> La conexión se ha interrumpido debido a que la actividad Keep-Alive detecta un error mientras la operación estaba en curso. También puede ser devuelto por <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>la</strong></a> función r si se realiza un intento de establecer <a href="/windows/desktop/winsock/so-keepalive"><strong>SO_KEEPALIVE</strong></a> en una conexión que ya ha generado un error.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span><dl> <dt><strong>WSAECONNABORTED</strong></dt> <dt>10053</dt> </dl></td>
<td><dl> <dt><span id="Software_caused_connection_abort."></span><span id="software_caused_connection_abort."></span><span id="SOFTWARE_CAUSED_CONNECTION_ABORT."></span>El software causó la anulación de la conexión.</dt> <dd> El software del equipo host anuló una conexión establecida, posiblemente debido a un error de tiempo de espera de transmisión de datos o de protocolo.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span><dl> <dt><strong>WSAECONNRESET</strong></dt> <dt>10054</dt> </dl></td>
<td><dl> <dt><span id="Connection_reset_by_peer."></span><span id="connection_reset_by_peer."></span><span id="CONNECTION_RESET_BY_PEER."></span>Conexión restablecida por el equipo del mismo nivel.</dt> <dd> El host remoto forzó el cierre de la conexión existente. Normalmente, esto se produce si la aplicación del mismo nivel en el host remoto se detiene repentinamente, se reinicia el host, se deshabilita el host o la interfaz de red remota, o el host remoto usa un cierre de disco (consulte la opción de la <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>conexión a-</strong></a> r para obtener más información sobre la opción SO_LINGER en el socket remoto). Este error también puede producirse si se interrumpió una conexión debido a que la actividad Keep-Alive está detectando un error mientras una o varias operaciones están en curso. Las operaciones que estaban en curso dan error con WSAENETRESET. Las operaciones subsiguientes producen un error con WSAECONNRESET.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span><dl> <dt><strong>WSAENOBUFS</strong></dt> <dt>10055</dt> </dl></td>
<td><dl> <dt><span id="No_buffer_space_available."></span><span id="no_buffer_space_available."></span><span id="NO_BUFFER_SPACE_AVAILABLE."></span>No hay espacio de búfer disponible.</dt> <dd> No se pudo realizar una operación en un socket porque el sistema no tenía suficiente espacio de búfer o porque la cola estaba llena.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEISCONN"></span><span id="wsaeisconn"></span><dl> <dt><strong>WSAEISCONN</strong></dt> <dt>10056</dt> </dl></td>
<td><dl> <dt><span id="Socket_is_already_connected."></span><span id="socket_is_already_connected."></span><span id="SOCKET_IS_ALREADY_CONNECTED."></span>El socket ya está conectado.</dt> <dd> Se realizó una solicitud de conexión en un socket ya conectado. Algunas implementaciones también devuelven este error si se llama a <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a> en un socket de SOCK_DGRAM conectado (para SOCK_STREAM sockets, se omite el parámetro <em>to</em> en <strong>SendTo</strong> ) aunque otras implementaciones tratan esto como una ocurrencia legal.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span><dl> <dt><strong>WSAENOTCONN</strong></dt> <dt>10057</dt> </dl></td>
<td><dl> <dt><span id="Socket_is_not_connected."></span><span id="socket_is_not_connected."></span><span id="SOCKET_IS_NOT_CONNECTED."></span>El socket no está conectado.</dt> <dd> No se ha permitido la solicitud para enviar o recibir datos porque el socket no está conectado y, al enviar un socket de datagramas mediante <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a>, no se proporcionó ninguna dirección. Cualquier otro tipo de operación también puede devolver este error; por ejemplo, si se establece el <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>valor de la</strong></a> opción de inicio de sesión <a href="/windows/desktop/winsock/so-keepalive"><strong>SO_KEEPALIVE</strong></a> si se ha restablecido la conexión.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span><dl> <dt><strong>WSAESHUTDOWN</strong></dt> <dt>10058</dt> </dl></td>
<td><dl> <dt><span id="Cannot_send_after_socket_shutdown."></span><span id="cannot_send_after_socket_shutdown."></span><span id="CANNOT_SEND_AFTER_SOCKET_SHUTDOWN."></span>No se puede enviar después del apagado de socket.</dt> <dd> No se ha permitido la solicitud para enviar o recibir datos porque el socket ya se había apagado en esa dirección con una llamada de <a href="/windows/desktop/api/winsock/nf-winsock-shutdown"><strong>cierre</strong></a> anterior. Al llamar al <strong>cierre</strong> , se solicita un cierre parcial de un socket, que es una señal que envía o recibe, o ambos se han suspendido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span><dl> <dt><strong>WSAETOOMANYREFS</strong></dt> <dt>10059</dt> </dl></td>
<td><dl> <dt><span id="Too_many_references."></span><span id="too_many_references."></span><span id="TOO_MANY_REFERENCES."></span>Demasiadas referencias.</dt> <dd> Demasiadas referencias a algún objeto de kernel.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span><dl> <dt><strong>WSAETIMEDOUT</strong></dt> <dt>10060</dt> </dl></td>
<td><dl> <dt><span id="Connection_timed_out."></span><span id="connection_timed_out."></span><span id="CONNECTION_TIMED_OUT."></span>Se agotó el tiempo de espera de la conexión.</dt> <dd> No se pudo realizar un intento de conexión porque la parte conectada no respondió correctamente después de un período de tiempo, o bien se produjo un error en la conexión establecida porque el host conectado no respondió.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span><dl> <dt><strong>WSAECONNREFUSED</strong></dt> <dt>10061</dt> </dl></td>
<td><dl> <dt><span id="Connection_refused."></span><span id="connection_refused."></span><span id="CONNECTION_REFUSED."></span>Conexión rechazada.</dt> <dd> No se pudo establecer ninguna conexión porque el equipo de destino la rechazó activamente. Esto suele ser el resultado de intentar conectarse a un servicio que está inactivo en el host externo, es decir, uno sin aplicación de servidor en ejecución.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAELOOP"></span><span id="wsaeloop"></span><dl> <dt><strong>WSAELOOP</strong></dt> <dt>10062</dt> </dl></td>
<td><dl> <dt><span id="Cannot_translate_name."></span><span id="cannot_translate_name."></span><span id="CANNOT_TRANSLATE_NAME."></span>No se puede convertir el nombre.</dt> <dd> No se puede traducir un nombre.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span><dl> <dt><strong>WSAENAMETOOLONG</strong></dt> <dt>10063</dt> </dl></td>
<td><dl> <dt><span id="Name_too_long."></span><span id="name_too_long."></span><span id="NAME_TOO_LONG."></span>Nombre demasiado largo.</dt> <dd> Un nombre o componente de nombre era demasiado largo.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span><dl> <dt><strong>WSAEHOSTDOWN</strong></dt> <dt>10064</dt> </dl></td>
<td><dl> <dt><span id="Host_is_down."></span><span id="host_is_down."></span><span id="HOST_IS_DOWN."></span>El host está inactivo.</dt> <dd> No se pudo realizar una operación de socket porque el host de destino está inactivo. Una operación de socket encontró un host inactivo. No se ha iniciado la actividad de red en el host local. Es más probable que estas condiciones se indiquen mediante el error WSAETIMEDOUT.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span><dl> <dt><strong>WSAEHOSTUNREACH</strong></dt> <dt>10065</dt> </dl></td>
<td><dl> <dt><span id="No_route_to_host."></span><span id="no_route_to_host."></span><span id="NO_ROUTE_TO_HOST."></span>No hay ninguna ruta al host.</dt> <dd> Se intentó realizar una operación de socket a un host inalcanzable. Vea WSAENETUNREACH.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span><dl> <dt><strong>WSAENOTEMPTY</strong></dt> <dt>10066</dt> </dl></td>
<td><dl> <dt><span id="Directory_not_empty."></span><span id="directory_not_empty."></span><span id="DIRECTORY_NOT_EMPTY."></span>El directorio no está vacío.</dt> <dd> No se puede quitar un directorio que no esté vacío.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span><dl> <dt><strong>WSAEPROCLIM</strong></dt> <dt>10067</dt> </dl></td>
<td><dl> <dt><span id="Too_many_processes."></span><span id="too_many_processes."></span><span id="TOO_MANY_PROCESSES."></span>Demasiados procesos.</dt> <dd> Una implementación de Windows Sockets puede tener un límite en cuanto al número de aplicaciones que puede usarla simultáneamente. <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup</strong></a> puede producir este error si se ha alcanzado el límite.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEUSERS"></span><span id="wsaeusers"></span><dl> <dt><strong>WSAEUSERS</strong></dt> <dt>10068</dt> </dl></td>
<td><dl> <dt><span id="User_quota_exceeded."></span><span id="user_quota_exceeded."></span><span id="USER_QUOTA_EXCEEDED."></span>Cuota de usuario superada.</dt> <dd> Se agotó la cuota de usuario. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDQUOT"></span><span id="wsaedquot"></span><dl> <dt><strong>WSAEDQUOT</strong></dt> <dt>10069</dt> </dl></td>
<td><dl> <dt><span id="Disk_quota_exceeded."></span><span id="disk_quota_exceeded."></span><span id="DISK_QUOTA_EXCEEDED."></span>Cuota de disco superada.</dt> <dd> Se agotó la cuota de disco. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESTALE"></span><span id="wsaestale"></span><dl> <dt><strong>WSAESTALE</strong></dt> <dt>10070</dt> </dl></td>
<td><dl> <dt><span id="Stale_file_handle_reference."></span><span id="stale_file_handle_reference."></span><span id="STALE_FILE_HANDLE_REFERENCE."></span>Referencia de identificador de archivo obsoleto.</dt> <dd> La referencia de identificador de archivo ya no está disponible. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEREMOTE"></span><span id="wsaeremote"></span><dl> <dt><strong>WSAEREMOTE</strong></dt> <dt>10071</dt> </dl></td>
<td><dl> <dt><span id="Item_is_remote."></span><span id="item_is_remote."></span><span id="ITEM_IS_REMOTE."></span>El elemento es remoto.</dt> <dd> El elemento no está disponible de forma local. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span><dl> <dt><strong>WSASYSNOTREADY</strong></dt> <dt>10091</dt> </dl></td>
<td><dl> <dt><span id="Network_subsystem_is_unavailable."></span><span id="network_subsystem_is_unavailable."></span><span id="NETWORK_SUBSYSTEM_IS_UNAVAILABLE."></span>El subsistema de red no está disponible.</dt> <dd> <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup</strong></a> devuelve este error si la implementación de Windows Sockets no funciona en este momento porque el sistema subyacente que usa para proporcionar servicios de red no está disponible actualmente. Los usuarios deben comprobar:<br/> </dd> </dl>
<ul>
<li>Que el archivo DLL de Windows Sockets adecuado se encuentra en la ruta de acceso actual.</li>
<li>Que no intenten usar más de una implementación de Windows Sockets simultáneamente. Si hay más de un archivo DLL de Winsock en el sistema, asegúrese de que el primero de la ruta de acceso es adecuado para el subsistema de red cargado actualmente.</li>
<li>La documentación de implementación de Windows Sockets para asegurarse de que todos los componentes necesarios estén instalados y configurados correctamente.</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span><dl> <dt><strong>WSAVERNOTSUPPORTED</strong></dt> <dt>10092</dt> </dl></td>
<td><dl> <dt><span id="Winsock.dll_version_out_of_range."></span><span id="winsock.dll_version_out_of_range."></span><span id="WINSOCK.DLL_VERSION_OUT_OF_RANGE."></span> Versión deWinsock.dll fuera del intervalo.</dt> <dd> La implementación actual de Windows Sockets no admite la versión de especificación de Windows Sockets solicitada por la aplicación. Compruebe que no se está teniendo acceso a ningún archivo DLL antiguo de Windows Sockets.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span><dl> <dt><strong>WSANOTINITIALISED</strong></dt> <dt>10093</dt> </dl></td>
<td><dl> <dt><span id="Successful_WSAStartup_not_yet_performed."></span><span id="successful_wsastartup_not_yet_performed."></span><span id="SUCCESSFUL_WSASTARTUP_NOT_YET_PERFORMED."></span>No se ha realizado correctamente WSAStartup.</dt> <dd> Se produjo un error en la aplicación que no llamó a <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup</strong></a> o a <strong>WSAStartup</strong> . Es posible que la aplicación tenga acceso a un socket que la tarea activa actual no posee (es decir, que intenta compartir un socket entre tareas) o a que se ha llamado a <a href="/windows/desktop/api/winsock/nf-winsock-wsacleanup"><strong>WSACleanup</strong></a> demasiadas veces.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDISCON"></span><span id="wsaediscon"></span><dl> <dt><strong>WSAEDISCON</strong></dt> <dt>10101</dt> </dl></td>
<td><dl> <dt><span id="Graceful_shutdown_in_progress."></span><span id="graceful_shutdown_in_progress."></span><span id="GRACEFUL_SHUTDOWN_IN_PROGRESS."></span>Cierre correcto en curso.</dt> <dd> Devuelto por <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsarecv"><strong>WSARecv</strong></a> y <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom"><strong>WSARecvFrom</strong></a> para indicar que la parte remota ha iniciado una secuencia de cierre estable.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOMORE"></span><span id="wsaenomore"></span><dl> <dt><strong>WSAENOMORE</strong></dt> <dt>10102</dt> </dl></td>
<td><dl> <dt><span id="No_more_results."></span><span id="no_more_results."></span><span id="NO_MORE_RESULTS."></span>No hay más resultados.</dt> <dd> La función <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a> no puede devolver más resultados.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span><dl> <dt><strong>WSAECANCELLED</strong></dt> <dt>10103</dt> </dl></td>
<td><dl> <dt><span id="Call_has_been_canceled."></span><span id="call_has_been_canceled."></span><span id="CALL_HAS_BEEN_CANCELED."></span>Se canceló la llamada.</dt> <dd> Se realizó una llamada a la función <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend"><strong>WSALookupServiceEnd</strong></a> mientras se sigue procesando esta llamada. Se canceló la llamada.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span><dl> <dt><strong>WSAEINVALIDPROCTABLE</strong></dt> <dt>10104</dt> </dl></td>
<td><dl> <dt><span id="Procedure_call_table_is_invalid."></span><span id="procedure_call_table_is_invalid."></span><span id="PROCEDURE_CALL_TABLE_IS_INVALID."></span>La tabla de llamadas a procedimientos no es válida.</dt> <dd> La tabla de llamadas de procedimiento del proveedor de servicios no es válida. Un proveedor de servicios devolvió una tabla de procedimientos fantasma para Ws2_32.dll. Esto suele deberse a que uno o varios de los punteros de función son <strong>null</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span><dl> <dt><strong>WSAEINVALIDPROVIDER</strong></dt> <dt>10105</dt> </dl></td>
<td><dl> <dt><span id="Service_provider_is_invalid."></span><span id="service_provider_is_invalid."></span><span id="SERVICE_PROVIDER_IS_INVALID."></span>El proveedor de servicios no es válido.</dt> <dd> El proveedor de servicios solicitado no es válido. Este error lo devuelven las funciones <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo"><strong>WSCGetProviderInfo</strong></a> y <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32"><strong>WSCGetProviderInfo32</strong></a> si no se encuentra la entrada de protocolo especificada. Este error también se devuelve si el proveedor de servicios devolvió un número de versión distinto de 2,0.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span><dl> <dt><strong>WSAEPROVIDERFAILEDINIT</strong></dt> <dt>10106</dt> </dl></td>
<td><dl> <dt><span id="Service_provider_failed_to_initialize."></span><span id="service_provider_failed_to_initialize."></span><span id="SERVICE_PROVIDER_FAILED_TO_INITIALIZE."></span>No se pudo inicializar el proveedor de servicios.</dt> <dd> No se pudo cargar o inicializar el proveedor de servicios solicitado. Se devuelve este error si no se pudo cargar una DLL del proveedor de servicios (error de<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> ) o se produjo un error en la función <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup"><strong>WSPStartup</strong></a> o <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup"><strong>NSPStartup</strong></a> del proveedor.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span><dl> <dt><strong>WSASYSCALLFAILURE</strong></dt> <dt>10107</dt> </dl></td>
<td><dl> <dt><span id="System_call_failure."></span><span id="system_call_failure."></span><span id="SYSTEM_CALL_FAILURE."></span>Error de llamada del sistema.</dt> <dd> Error en una llamada del sistema que nunca debe producir un error. Se trata de un código de error genérico, que se devuelve en varias condiciones. <br/> Se devuelve cuando se produce un error en una llamada del sistema que nunca debe producir un error. Por ejemplo, si se produce un error en una llamada a <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents"><strong>WaitForMultipleEvents</strong></a> o una de las funciones del registro no intenta manipular los catálogos del protocolo o espacio de nombres.<br/> Se devuelve cuando un proveedor no devuelve un valor correcto y no proporciona un código de error extendido. Puede indicar un error de implementación del proveedor de servicios.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span><dl> <dt><strong>WSASERVICE_NOT_FOUND</strong></dt> <dt>10108</dt> </dl></td>
<td><dl> <dt><span id="Service_not_found."></span><span id="service_not_found."></span><span id="SERVICE_NOT_FOUND."></span>No se encontró el servicio.</dt> <dd> No se conoce este servicio. No se encuentra el servicio en el espacio de nombres especificado.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span><dl> <dt><strong>WSATYPE_NOT_FOUND</strong></dt> <dt>10109</dt> </dl></td>
<td><dl> <dt><span id="Class_type_not_found."></span><span id="class_type_not_found."></span><span id="CLASS_TYPE_NOT_FOUND."></span>No se encontró el tipo de clase.</dt> <dd> No se encontró la clase especificada.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span><dl> <dt><strong>WSA_E_NO_MORE</strong></dt> <dt>10110</dt> </dl></td>
<td><dl> <dt><span id="No_more_results."></span><span id="no_more_results."></span><span id="NO_MORE_RESULTS."></span>No hay más resultados.</dt> <dd> La función <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a> no puede devolver más resultados.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span><dl> <dt><strong>WSA_E_CANCELLED</strong></dt> <dt>10111</dt> </dl></td>
<td><dl> <dt><span id="Call_was_canceled."></span><span id="call_was_canceled."></span><span id="CALL_WAS_CANCELED."></span>Se canceló la llamada.</dt> <dd> Se realizó una llamada a la función <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend"><strong>WSALookupServiceEnd</strong></a> mientras se sigue procesando esta llamada. Se canceló la llamada.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEREFUSED"></span><span id="wsaerefused"></span><dl> <dt><strong>WSAEREFUSED</strong></dt> <dt>10112</dt> </dl></td>
<td><dl> <dt><span id="Database_query_was_refused."></span><span id="database_query_was_refused."></span><span id="DATABASE_QUERY_WAS_REFUSED."></span>Se rechazó la consulta de base de datos.</dt> <dd> Error en una consulta de base de datos porque se rechazó activamente.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span><dl> <dt><strong>WSAHOST_NOT_FOUND</strong></dt> <dt>11001</dt> </dl></td>
<td><dl> <dt><span id="Host_not_found."></span><span id="host_not_found."></span><span id="HOST_NOT_FOUND."></span>No se encuentra el host.</dt> <dd> Se desconoce el host. El nombre no es un nombre de host o alias oficial, o no se encuentra en las bases de datos que se consultan. Este error también puede devolverse para las consultas de protocolo y servicio, y significa que el nombre especificado no se pudo encontrar en la base de datos correspondiente.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span><dl> <dt><strong>WSATRY_AGAIN</strong></dt> <dt>11002</dt> </dl></td>
<td><dl> <dt><span id="Nonauthoritative_host_not_found."></span><span id="nonauthoritative_host_not_found."></span><span id="NONAUTHORITATIVE_HOST_NOT_FOUND."></span>No se encontró ningún host no autoritativo.</dt> <dd> Suele ser un error temporal durante la resolución de nombres de host y significa que el servidor local no recibió una respuesta de un servidor autoritativo. Es posible que se consiga si se vuelve a intentar un poco más tarde.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span><dl> <dt><strong>WSANO_RECOVERY</strong></dt> <dt>11003</dt> </dl></td>
<td><dl> <dt><span id="This_is_a_nonrecoverable_error."></span><span id="this_is_a_nonrecoverable_error."></span><span id="THIS_IS_A_NONRECOVERABLE_ERROR."></span>Se trata de un error irrecuperable.</dt> <dd> Esto indica que se ha producido algún tipo de error irrecuperable durante una búsqueda en la base de datos. Esto puede deberse a que no se encontraron los archivos de base de datos (por ejemplo, los archivos de host, servicios o protocolos compatibles con BSD) o que el servidor ha devuelto una solicitud de DNS con un error grave.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSANO_DATA"></span><span id="wsano_data"></span><dl> <dt><strong>WSANO_DATA</strong></dt> <dt>11004</dt> </dl></td>
<td><dl> <dt><span id="Valid_name__no_data_record_of_requested_type."></span><span id="valid_name__no_data_record_of_requested_type."></span><span id="VALID_NAME__NO_DATA_RECORD_OF_REQUESTED_TYPE."></span>Nombre válido, no hay registro de datos del tipo solicitado.</dt> <dd> El nombre solicitado es válido y se encontró en la base de datos, pero no tiene los datos asociados correctos que se van a resolver. El ejemplo habitual es un intento de traducción de nombre de host a dirección (mediante <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname"><strong>gethostbyname</strong></a> o <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-wsaasyncgethostbyname"><strong>WSAAsyncGetHostByName</strong></a>) que usa el DNS (servidor de nombres de dominio). Se devuelve un registro MX pero no un registro, lo que indica que el propio host existe, pero no se puede acceder A él directamente.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span><dl> <dt><strong>WSA_QOS_RECEIVERS</strong></dt> <dt>11005</dt> </dl></td>
<td><dl> <dt><span id="QoS_receivers."></span><span id="qos_receivers."></span><span id="QOS_RECEIVERS."></span>Receptores de QoS.</dt> <dd> Ha llegado al menos una reserva de QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span><dl> <dt><strong>WSA_QOS_SENDERS</strong></dt> <dt>11006</dt> </dl></td>
<td><dl> <dt><span id="QoS_senders."></span><span id="qos_senders."></span><span id="QOS_SENDERS."></span>Remitentes de QoS.</dt> <dd> Ha llegado al menos una ruta de acceso de envío de QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span><dl> <dt><strong>WSA_QOS_NO_SENDERS</strong></dt> <dt>11007</dt> </dl></td>
<td><dl> <dt><span id="No_QoS_senders."></span><span id="no_qos_senders."></span><span id="NO_QOS_SENDERS."></span>Sin remitentes QoS.</dt> <dd> No hay remitentes de QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span><dl> <dt><strong>WSA_QOS_NO_RECEIVERS</strong></dt> <dt>11008</dt> </dl></td>
<td><dl> <dt><span id="QoS_no_receivers."></span><span id="qos_no_receivers."></span><span id="QOS_NO_RECEIVERS."></span>QoS sin destinatarios.</dt> <dd> No hay ningún receptor de QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span><dl> <dt><strong>WSA_QOS_REQUEST_CONFIRMED</strong></dt> <dt>11009</dt> </dl></td>
<td><dl> <dt><span id="QoS_request_confirmed."></span><span id="qos_request_confirmed."></span><span id="QOS_REQUEST_CONFIRMED."></span>Solicitud de QoS confirmada.</dt> <dd> Se ha confirmado la solicitud de reserva de QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span><dl> <dt><strong>WSA_QOS_ADMISSION_FAILURE</strong></dt> <dt>11010</dt> </dl></td>
<td><dl> <dt><span id="QoS_admission_error."></span><span id="qos_admission_error."></span><span id="QOS_ADMISSION_ERROR."></span>Error de admisión de QoS.</dt> <dd> Se produjo un error de QoS debido a la falta de recursos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span><dl> <dt><strong>WSA_QOS_POLICY_FAILURE</strong></dt> <dt>11011</dt> </dl></td>
<td><dl> <dt><span id="QoS_policy_failure."></span><span id="qos_policy_failure."></span><span id="QOS_POLICY_FAILURE."></span>Error de la directiva QoS.</dt> <dd> Se rechazó la solicitud QoS porque el sistema de directivas no pudo asignar el recurso solicitado dentro de la directiva existente. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span><dl> <dt><strong>WSA_QOS_BAD_STYLE</strong></dt> <dt>11012</dt> </dl></td>
<td><dl> <dt><span id="QoS_bad_style."></span><span id="qos_bad_style."></span><span id="QOS_BAD_STYLE."></span>Estilo de QoS incorrecto.</dt> <dd> Se encontró un estilo QoS desconocido o conflictivo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span><dl> <dt><strong>WSA_QOS_BAD_OBJECT</strong></dt> <dt>11013</dt> </dl></td>
<td><dl> <dt><span id="QoS_bad_object."></span><span id="qos_bad_object."></span><span id="QOS_BAD_OBJECT."></span>Objeto de QoS incorrecto.</dt> <dd> Se encontró un problema con alguna parte del FILTERSPEC o del búfer específico del proveedor en general.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span><dl> <dt><strong>WSA_QOS_TRAFFIC_CTRL_ERROR</strong></dt> <dt>11014</dt> </dl></td>
<td><dl> <dt><span id="QoS_traffic_control_error."></span><span id="qos_traffic_control_error."></span><span id="QOS_TRAFFIC_CONTROL_ERROR."></span>Error de control de tráfico de QoS.</dt> <dd> Se ha convertido un error con la API de control de tráfico subyacente (TC) como solicitud QoS genérica para el cumplimiento local por parte de la API de TC. Esto puede deberse a un error de memoria insuficiente o a un error interno del proveedor de QoS. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span><dl> <dt><strong>WSA_QOS_GENERIC_ERROR</strong></dt> <dt>11015</dt> </dl></td>
<td><dl> <dt><span id="QoS_generic_error."></span><span id="qos_generic_error."></span><span id="QOS_GENERIC_ERROR."></span>Error genérico de QoS.</dt> <dd> Error general de QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span><dl> <dt><strong>WSA_QOS_ESERVICETYPE</strong></dt> <dt>11016</dt> </dl></td>
<td><dl> <dt><span id="QoS_service_type_error."></span><span id="qos_service_type_error."></span><span id="QOS_SERVICE_TYPE_ERROR."></span>Error de tipo de servicio QoS.</dt> <dd> Se encontró un tipo de servicio no válido o no reconocido en el FLOWSPEC de QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span><dl> <dt><strong>WSA_QOS_EFLOWSPEC</strong></dt> <dt>11017</dt> </dl></td>
<td><dl> <dt><span id="QoS_flowspec_error."></span><span id="qos_flowspec_error."></span><span id="QOS_FLOWSPEC_ERROR."></span>Error FLOWSPEC de QoS.</dt> <dd> Se encontró un FLOWSPEC no válido o incoherente en la estructura de <a href="/windows/win32/api/winsock2/ns-winsock2-qos"><strong>QoS</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span><dl> <dt><strong>WSA_QOS_EPROVSPECBUF</strong></dt> <dt>11018</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider_buffer."></span><span id="invalid_qos_provider_buffer."></span><span id="INVALID_QOS_PROVIDER_BUFFER."></span>Búfer de proveedor QoS no válido.</dt> <dd> Búfer específico del proveedor QoS no válido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span><dl> <dt><strong>WSA_QOS_EFILTERSTYLE</strong></dt> <dt>11019</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_filter_style."></span><span id="invalid_qos_filter_style."></span><span id="INVALID_QOS_FILTER_STYLE."></span>Estilo de filtro QoS no válido.</dt> <dd> Se usó un estilo de filtro QoS no válido.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span><dl> <dt><strong>WSA_QOS_EFILTERTYPE</strong></dt> <dt>11020</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_filter_type."></span><span id="invalid_qos_filter_type."></span><span id="INVALID_QOS_FILTER_TYPE."></span>Tipo de filtro QoS no válido.</dt> <dd> Se usó un tipo de filtro QoS no válido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span><dl> <dt><strong>WSA_QOS_EFILTERCOUNT</strong></dt> <dt>11021</dt> </dl></td>
<td><dl> <dt><span id="Incorrect_QoS_filter_count."></span><span id="incorrect_qos_filter_count."></span><span id="INCORRECT_QOS_FILTER_COUNT."></span>Recuento de filtros QoS incorrectos.</dt> <dd> Se especificó un número incorrecto de FILTERSPECs de QoS en FLOWDESCRIPTOR.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span><dl> <dt><strong>WSA_QOS_EOBJLENGTH</strong></dt> <dt>11022</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_object_length."></span><span id="invalid_qos_object_length."></span><span id="INVALID_QOS_OBJECT_LENGTH."></span>Longitud de objeto QoS no válida.</dt> <dd> Se especificó un objeto con un campo ObjectLength no válido en el búfer específico del proveedor QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span><dl> <dt><strong>WSA_QOS_EFLOWCOUNT</strong></dt> <dt>11023</dt> </dl></td>
<td><dl> <dt><span id="Incorrect_QoS_flow_count."></span><span id="incorrect_qos_flow_count."></span><span id="INCORRECT_QOS_FLOW_COUNT."></span>Recuento de flujo de QoS incorrecto.</dt> <dd> Se especificó un número incorrecto de descriptores de flujo en la estructura de QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span><dl> <dt><strong>WSA_QOS_EUNKOWNPSOBJ</strong></dt> <dt>11024</dt> </dl></td>
<td><dl> <dt><span id="Unrecognized_QoS_object."></span><span id="unrecognized_qos_object."></span><span id="UNRECOGNIZED_QOS_OBJECT."></span>Objeto QoS no reconocido.</dt> <dd> Se encontró un objeto desconocido en el búfer específico del proveedor QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span><dl> <dt><strong>WSA_QOS_EPOLICYOBJ</strong></dt> <dt>11025</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_policy_object."></span><span id="invalid_qos_policy_object."></span><span id="INVALID_QOS_POLICY_OBJECT."></span>Objeto de directiva QoS no válido.</dt> <dd> Se encontró un objeto de Directiva no válido en el búfer específico del proveedor QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span><dl> <dt><strong>WSA_QOS_EFLOWDESC</strong></dt> <dt>11026</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_flow_descriptor."></span><span id="invalid_qos_flow_descriptor."></span><span id="INVALID_QOS_FLOW_DESCRIPTOR."></span>Descriptor de flujo de QoS no válido.</dt> <dd> Se encontró un descriptor de flujo de QoS no válido en la lista de descriptores de flujo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span><dl> <dt><strong>WSA_QOS_EPSFLOWSPEC</strong></dt> <dt>11027</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider-specific_flowspec."></span><span id="invalid_qos_provider-specific_flowspec."></span><span id="INVALID_QOS_PROVIDER-SPECIFIC_FLOWSPEC."></span>FLOWSPEC específico del proveedor QoS no válido.</dt> <dd> Se encontró un FLOWSPEC no válido o incoherente en el búfer específico del proveedor QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span><dl> <dt><strong>WSA_QOS_EPSFILTERSPEC</strong></dt> <dt>11028</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider-specific_filterspec."></span><span id="invalid_qos_provider-specific_filterspec."></span><span id="INVALID_QOS_PROVIDER-SPECIFIC_FILTERSPEC."></span>FILTERSPEC específicos del proveedor QoS no válidos.</dt> <dd> Se encontró un FILTERSPEC no válido en el búfer específico del proveedor QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span><dl> <dt><strong>WSA_QOS_ESDMODEOBJ</strong></dt> <dt>11029</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_shape_discard_mode_object."></span><span id="invalid_qos_shape_discard_mode_object."></span><span id="INVALID_QOS_SHAPE_DISCARD_MODE_OBJECT."></span>Objeto de modo de descarte de forma de QoS no válido.</dt> <dd> Se encontró un objeto de modo discard de forma no válido en el búfer específico del proveedor QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span><dl> <dt><strong>WSA_QOS_ESHAPERATEOBJ</strong></dt> <dt>11030</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_shaping_rate_object."></span><span id="invalid_qos_shaping_rate_object."></span><span id="INVALID_QOS_SHAPING_RATE_OBJECT."></span>Objeto de tasa de forma de QoS no válido.</dt> <dd> Se encontró un objeto de frecuencia de forma no válido en el búfer específico del proveedor QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span><dl> <dt><strong>WSA_QOS_RESERVED_PETYPE</strong></dt> <dt>11031</dt> </dl></td>
<td><dl> <dt><span id="Reserved_policy_QoS_element_type."></span><span id="reserved_policy_qos_element_type."></span><span id="RESERVED_POLICY_QOS_ELEMENT_TYPE."></span>Tipo de elemento de QoS de directiva reservada.</dt> <dd> Se encontró un elemento de directiva reservado en el búfer específico del proveedor QoS.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WinSock2. h; </dt> <dt>Winerror. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de error: errno, h \_ errno y WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[Control de errores de Winsock](handling-winsock-errors.md)
</dt> <dt>

[**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)
</dt> <dt>

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
