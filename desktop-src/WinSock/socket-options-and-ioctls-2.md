---
description: Algunas de las opciones de socket para Windows Sockets 2 se resumen en la tabla siguiente.
ms.assetid: 6731d27c-fb7d-421a-badf-0cad6a4712ea
title: Opciones de socket e ICTLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020495cca9f0c4ec412f0a4d3dd29ae7235e22e52f4beda4372cf9fb50409ece
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993415"
---
# <a name="socket-options-and-ioctls"></a>Opciones de socket e ICTLs

Algunas de las opciones de socket para Windows Sockets 2 se resumen en la tabla siguiente. Se proporciona información más detallada en la sección 4 de [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) o [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)). Hay otras nuevas opciones de socket específicas del protocolo que se pueden encontrar en el anexo Protocol-Specific protocolo. Hay una lista completa de [**las opciones**](socket-options.md) de socket Windows sockets están disponibles en la referencia de Winsock.

Para obtener un resumen de algunas de las ioctls de Winsock, consulte [Resumen de socket Ioctl Opcodes.](summary-of-socket-ioctl-opcodes-2.md) Hay una lista completa [**de ICTL de Winsock**](winsock-ioctls.md) disponibles en la referencia de Winsock.

## <a name="summary-of-common-socket-options"></a>Resumen de las opciones comunes de socket

Un proveedor de servicios Winsock debe reconocer todas estas opciones y (para [**WSPGetSockOpt)**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))devolver valores plausibles para cada una de ellas. El valor predeterminado de cada opción se muestra en la tabla siguiente.

Valor

Tipo

Significado

Valor predeterminado

Nota

<span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>ASÍ \_ QUE ACCEPTCONN

BOOL

El socket está escuchando.

FALSE a menos que se haya realizado un [**WSPListen.**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))

<span id="SO_BROADCAST"></span><span id="so_broadcast"></span>DIFUSIÓN \_ DE SO

BOOL

Socket está configurado para la transmisión y recepción de mensajes de difusión.

FALSE

<span id="SO_DEBUG"></span><span id="so_debug"></span>DEPURACIÓN \_ DE SO

BOOL

La depuración está habilitada.

FALSE

(i)

<span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>ASÍ \_ QUE DONTLINGER

BOOL

Si es true, la opción SO \_ LINGER está deshabilitada.

TRUE

<span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>ASÍ \_ QUE DONTROUTE

BOOL

El enrutamiento está deshabilitado. Se realiza correctamente, pero se omite en los sockets AF INET; se produce un error \_ en \_ los sockets AF INET6 con [WSAENOPROTOOPT](windows-sockets-error-codes-2.md). No se admite en sockets de ATM (se produce un error).

FALSE

(i)

<span id="SO_ERROR"></span><span id="so_error"></span>SO \_ ERROR

int

Recupera el estado de error y borra.

0

<span id="SO_GROUP_ID"></span><span id="so_group_id"></span>ID. \_ DE \_ GRUPO DE SO

GROUP

Reservado.

NULL

Obtener solo

<span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>PRIORIDAD \_ DE \_ GRUPO

int

Reservado.

0

[**ASÍ \_ QUE KEEPALIVE**](so-keepalive.md)

BOOL

Se envían keepalives. No se admite en sockets de ATM (se produce un error).

FALSE

(i)

<span id="SO_LINGER"></span><span id="so_linger"></span>SO \_ LINGER

Persistente de la estructura

Devuelve las opciones de persistente actuales.

l \_ onoff es 0

<span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>SO \_ MAX MSG SIZE (TAMAÑO MÁXIMO DE \_ \_ MENSAJES)

int

Tamaño de salida máximo de un mensaje para los tipos de socket de mensaje. No hay ninguna disposición para determinar el tamaño máximo del mensaje entrante. No tiene ningún significado para los sockets orientados a secuencias.

Dependiente de la implementación

Obtener solo

<span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>SO \_ OOBINLINE

BOOL

Los datos de OOB se reciben en el flujo de datos normal.

FALSE

<span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>SO \_ PROTOCOL \_ INFOW

estructura [ **WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)

Descripción de la información de protocolo para el protocolo enlazado a este socket.

Dependiente del protocolo

Obtener solo

<span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>SO \_ RCVBUF

int

Espacio total de búfer por socket reservado para las recibeciones. Esto no está relacionado con SO MAX MSG SIZE y no se corresponde necesariamente con el tamaño de la \_ \_ ventana de recepción \_ TCP.

Dependiente de la implementación

(i)

<span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>ASÍ QUE \_ REUSEADDR

BOOL

Otros usuarios pueden usar la dirección a la que está enlazado este socket. No es aplicable en sockets de ATM.

FALSE

<span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>SO \_ SNDBUF

int

Espacio total de búfer por socket reservado para envíos. Esto no está relacionado con SO MAX MSG SIZE y no se corresponde necesariamente con el tamaño de \_ una ventana de envío \_ \_ TCP.

Dependiente de la implementación

(i)

<span id="SO_TYPE"></span><span id="so_type"></span>SO \_ TYPE

int

Tipo del socket (por ejemplo, SOCK \_ STREAM).

Tal como se creó a través de socket.

<span id="PVD_CONFIG"></span><span id="pvd_config"></span>CONFIGURACIÓN DE \_ PVD

char FAR \*

Objeto de estructura de datos opaco que contiene información de configuración del proveedor de servicios.

Dependiente de la implementación

<span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP \_ NODELAY

BOOL

Deshabilita el algoritmo de Nagle para la fusión de envíos.

Dependiente de la implementación

(i) Un proveedor de servicios puede omitir silenciosamente esta opción en [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) y devolver un valor constante para [**WSPGetSockOpt,**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))o bien puede aceptar un valor para **WSPSetSockOpt** y devolver el valor correspondiente en **WSPGetSockOpt** sin usar el valor de ninguna manera.



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Opciones de socket**](socket-options.md)
</dt> <dt>

[**Opciones de socket DE SOL \_**](sol-socket-socket-options.md)
</dt> <dt>

[**Opciones de socket TCP de IPPROTO \_**](ipproto-tcp-socket-options.md)
</dt> <dt>

[**Opciones de socket UDP de IPPROTO \_**](ipproto-udp-socket-options.md)
</dt> <dt>

[**ICTLs de Winsock**](winsock-ioctls.md)
</dt> </dl>

 

 
