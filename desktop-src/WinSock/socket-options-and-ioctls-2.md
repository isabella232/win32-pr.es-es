---
description: En la tabla siguiente se resumen algunas de las opciones de socket para Windows Sockets 2.
ms.assetid: 6731d27c-fb7d-421a-badf-0cad6a4712ea
title: Opciones de socket y ioctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472d37bd8d2d97eead66d7c9d2319e57fc5dafde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716630"
---
# <a name="socket-options-and-ioctls"></a>Opciones de socket y ioctl

En la tabla siguiente se resumen algunas de las opciones de socket para Windows Sockets 2. En la sección 4, en [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) y/o [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)), se proporciona información más detallada. Hay otras nuevas opciones de socket específicas del protocolo que se pueden encontrar en el anexo Protocol-Specific. Puede encontrar una lista completa de [**las opciones de socket**](socket-options.md) para Windows Sockets en la referencia de Winsock.

Para obtener un resumen de algunos de los ioctl de Winsock, consulte [Summary of socket ioctl opcodesing](summary-of-socket-ioctl-opcodes-2.md). Puede encontrar una lista completa de los [**ioctl de Winsock**](winsock-ioctls.md) en la referencia de Winsock.

## <a name="summary-of-common-socket-options"></a>Resumen de opciones de socket comunes

Un proveedor de servicios Winsock debe reconocer todas estas opciones, y (para [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) devolverá los valores de plausible para cada uno. En la tabla siguiente se muestra el valor predeterminado de cada opción.

Value

Tipo

Significado

Valor predeterminado

Nota

<span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>\_ACCEPTCONN

BOOL

El socket está escuchando.

FALSE, a menos que se haya realizado un [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) .

<span id="SO_BROADCAST"></span><span id="so_broadcast"></span>\_difundir

BOOL

Socket está configurado para la transmisión y recepción de mensajes de difusión.

false

<span id="SO_DEBUG"></span><span id="so_debug"></span>\_depurar

BOOL

La depuración está habilitada.

false

Configur

<span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>\_DONTLINGER

BOOL

Si es true, la \_ opción de permanencia está deshabilitada.

TRUE

<span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>\_DONTROUTE

BOOL

El enrutamiento está deshabilitado. Se realiza correctamente, pero se omite en los \_ sockets de AF inet; produce un error en los \_ sockets de AF inet6 con [WSAENOPROTOOPT](windows-sockets-error-codes-2.md). No se admite en sockets ATM (se produce un error).

false

Configur

<span id="SO_ERROR"></span><span id="so_error"></span>\_error

int

Recupera el estado de error y borra.

0

<span id="SO_GROUP_ID"></span><span id="so_group_id"></span>\_identificador de grupo \_

GROUP

Reservado.

NULL

Obtener solo

<span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>\_prioridad de grupo \_

int

Reservado.

0

[**\_KEEPALIVE**](so-keepalive.md)

BOOL

Se están enviando Keepalives. No se admite en sockets ATM (se produce un error).

false

Configur

<span id="SO_LINGER"></span><span id="so_linger"></span>por tanto, \_ permanencia

Permanencia de estructura

Devuelve las opciones de permanencia actual.

l \_ OnOff es 0

<span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>\_tamaño de \_ mensaje \_ máximo

int

Tamaño máximo de salida de un mensaje para los tipos de sockets de mensajes. No hay ninguna disposición para determinar el tamaño máximo de los mensajes entrantes. No tiene ningún significado para los sockets orientados a flujos.

Dependiente de la implementación

Obtener solo

<span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>\_OOBINLINE

BOOL

Los datos OOB se reciben en el flujo de datos normal.

false

<span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>\_Protocolo \_ INFOW

[ **\_ información de WSAPROTOCOL** de estructura](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)

Descripción de la información de protocolo para el protocolo que está enlazado a este socket.

Dependiente del Protocolo

Obtener solo

<span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>\_RCVBUF

int

Espacio total de búfer por socket reservado para las recepciones. Esto no está relacionado con \_ \_ \_ el tamaño máximo del mensaje y no se corresponde necesariamente con el tamaño de la ventana de recepción de TCP.

Dependiente de la implementación

Configur

<span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>\_REUSEADDR

BOOL

Otros usuarios pueden usar la dirección a la que está enlazado este socket. No es aplicable en sockets ATM.

false

<span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>\_SNDBUF

int

Espacio total de búfer por socket reservado para los envíos. Esto no está relacionado con \_ \_ \_ el tamaño máximo del mensaje y no se corresponde necesariamente con el tamaño de una ventana de envío TCP.

Dependiente de la implementación

Configur

<span id="SO_TYPE"></span><span id="so_type"></span>\_Escriba

int

Tipo del socket (por ejemplo, SOCK \_ Stream).

Tal como se creó a través de socket.

<span id="PVD_CONFIG"></span><span id="pvd_config"></span>configuración de PVD \_

char FAR \*

Objeto de estructura de datos opaco que contiene información de configuración del proveedor de servicios.

Dependiente de la implementación

<span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>retardo de TCP \_

BOOL

Deshabilita el algoritmo de Nagle para la fusión de envíos.

Dependiente de la implementación

(i) un proveedor de servicios puede omitir esta opción de forma silenciosa en [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) y devolver un valor constante para [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), o puede aceptar un valor para **WSPSetSockOpt** y devolver el valor correspondiente en **WSPGetSockOpt** sin usar el valor de ninguna manera.



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Opciones de socket**](socket-options.md)
</dt> <dt>

[**\_Opciones de socket de socket sol**](sol-socket-socket-options.md)
</dt> <dt>

[**\_Opciones de socket TCP de IPPROTO**](ipproto-tcp-socket-options.md)
</dt> <dt>

[**\_Opciones de socket UDP de IPPROTO**](ipproto-udp-socket-options.md)
</dt> <dt>

[**Ioctl de Winsock**](winsock-ioctls.md)
</dt> </dl>

 

 
