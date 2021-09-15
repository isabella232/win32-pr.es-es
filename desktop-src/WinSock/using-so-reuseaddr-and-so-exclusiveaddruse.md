---
description: El desarrollo de una infraestructura de red segura de alto nivel es una prioridad para la mayoría de los desarrolladores de aplicaciones de red. Sin embargo, la seguridad de sockets a menudo se pasa por alto a pesar de ser muy crítica al considerar una solución totalmente segura.
ms.assetid: b37a3e33-65ee-43b1-bc8b-3280db7ebee4
title: Uso SO_REUSEADDR y SO_EXCLUSIVEADDRUSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa4024f031102cbd634c235bb39f4c7860e6c1d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359222"
---
# <a name="using-so_reuseaddr-and-so_exclusiveaddruse"></a>Uso de SO \_ REUSEADDR y SO \_ EXCLUSIVEADDRUSE

El desarrollo de una infraestructura de red segura de alto nivel es una prioridad para la mayoría de los desarrolladores de aplicaciones de red. Sin embargo, la seguridad de sockets a menudo se pasa por alto a pesar de ser muy crítica al considerar una solución totalmente segura. La seguridad de sockets, en concreto, se ocupa de los procesos que se enlazan al mismo puerto enlazado previamente por otro proceso de aplicación. En el pasado, era posible que una aplicación de red "secuestrase" el puerto de otra aplicación, lo que podía provocar fácilmente un ataque de "denegación de servicio" o un robo de datos.

En general, la seguridad de sockets se aplica a los procesos del lado servidor. Más concretamente, la seguridad de sockets se aplica a cualquier aplicación de red que acepte conexiones y reciba tráfico de datagramas IP. Estas aplicaciones normalmente se enlazan a un puerto conocido y son destinos comunes de código de red malintencionado.

Es menos probable que las aplicaciones cliente sean los destinos de estos ataques, no porque sean menos susceptibles, sino porque la mayoría de los clientes se enlazan a puertos locales "efímeros" en lugar de puertos estáticos de "servicio". Las aplicaciones de red cliente siempre deben enlazarse a puertos efímeros (especificando el puerto [](/windows/win32/api/winsock/nf-winsock-bind) 0 en la estructura [**SOCKADDR**](sockaddr-2.md) a la que apunta el parámetro *name* al llamar a la función bind), a menos que haya una razón arquitectónica atractiva para no hacerlo. Los puertos locales efímeros constan de puertos mayores que el puerto 49151. La mayoría de las aplicaciones de servidor para servicios dedicados se enlazan a un puerto reservado conocido que es menor o igual que el puerto 49151. Por lo tanto, para la mayoría de las aplicaciones, no suele haber un conflicto para las solicitudes de enlace entre aplicaciones cliente y servidor.

En esta sección se describe el nivel predeterminado de seguridad en varias plataformas de Microsoft Windows y cómo las opciones de socket específicas **SO \_ REUSEADDR** y [SO \_ EXCLUSIVEADDRUSE](so-exclusiveaddruse.md) afectan y afectan a la seguridad de las aplicaciones de red. Hay disponible una característica adicional denominada seguridad de socket mejorada en Windows Server 2003 y versiones posteriores. La disponibilidad de estas opciones de socket y la seguridad de socket mejorada varía según las versiones de los sistemas operativos de Microsoft, como se muestra en la tabla siguiente.

| Plataforma            | ASÍ QUE \_ REUSEADDR | SO \_ EXCLUSIVEADDRUSE                  | Seguridad de socket mejorada |
|---------------------|---------------|---------------------------------------|--------------------------|
| Windows 95          | Disponible     | No disponible                         | No disponible            |
| Windows 98          | Disponible     | No disponible                         | No disponible            |
| Windows Me          | Disponible     | No disponible                         | No disponible            |
| Windows NT 4.0      | Disponible     | Disponible en Service Pack 4 y versiones posteriores | No disponible            |
| Windows 2000        | Disponible     | Disponible                             | No disponible            |
| Windows XP          | Disponible     | Disponible                             | No disponible            |
| Windows Server 2003 | Disponible     | Disponible                             | Disponible                |
| Windows Vista       | Disponible     | Disponible                             | Disponible                |
| Windows Server 2008 | Disponible     | Disponible                             | Disponible                |
| Windows 7 y versiones más recientes  | Disponible     | Disponible                             | Disponible                |

## <a name="using-so_reuseaddr"></a>Uso de SO \_ REUSEADDR

La opción de socket **SO \_ REUSEADDR** permite que un socket se enlace forzadamente a un puerto en uso por otro socket. El segundo socket llama a [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) con el parámetro *optname* establecido en **SO \_ REUSEADDR** y el parámetro *optval* establecido en un valor booleano **de TRUE antes** de llamar a [**bind**](/windows/win32/api/winsock/nf-winsock-bind) en el mismo puerto que el socket original. Una vez que el segundo socket se ha enlazado correctamente, el comportamiento de todos los sockets enlazados a ese puerto es indeterminado. Por ejemplo, si todos los sockets del mismo puerto proporcionan el servicio TCP, no se puede garantizar que el socket correcto controle las solicitudes de conexión TCP entrantes a través del puerto; el comportamiento no es determinista. Un programa malintencionado puede usar **SO \_ REUSEADDR** para enlazar a la fuerza sockets que ya se usan para los servicios de protocolo de red estándar con el fin de denegar el acceso a esos servicios. No se requieren privilegios especiales para usar esta opción.

Si una aplicación cliente se enlaza a un puerto antes de que una aplicación de servidor pueda enlazarse al mismo puerto, pueden producirse problemas. Si la aplicación de servidor enlaza forzadamente mediante la opción de socket **SO \_ REUSEADDR** al mismo puerto, el comportamiento de todos los sockets enlazados a ese puerto es indeterminado.

La excepción a este comportamiento no determinista son los sockets de multidifusión. Si dos sockets están enlazados a la misma interfaz y puerto y son miembros del mismo grupo de multidifusión, los datos se entregarán a ambos sockets, en lugar de uno elegido arbitrariamente.

## <a name="using-so_exclusiveaddruse"></a>Uso de SO \_ EXCLUSIVEADDRUSE

Antes de que se introdujese la opción de socket **SO \_ EXCLUSIVEADDRUSE,** había muy poco que un desarrollador de aplicaciones de red pudiera hacer para evitar que un programa malintencionado se enlace al puerto en el que la aplicación de red tenía sus propios sockets enlazados. Para solucionar este problema de seguridad, Windows Sockets introdujo la opción de socket **SO \_ EXCLUSIVEADDRUSE,** que estaba disponible en Windows NT 4.0 con Service Pack 4 (SP4) y versiones posteriores.

Los miembros del grupo de seguridad Administradores solo pueden usar la opción de socket **SO \_ EXCLUSIVEADDRUSE** Windows XP y versiones anteriores. Los motivos por los que se cambió este requisito en Windows Server 2003 y versiones posteriores se explican más adelante en el artículo.

La opción **SO \_ EXCLUSIVEADDRUSE** se establece mediante una llamada a la función [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) con el parámetro *optname* establecido en **SO \_ EXCLUSIVEADDRUSE** y el parámetro *optval* establecido en un valor booleano **de TRUE** antes de enlazar el socket. Una vez establecida la opción , el comportamiento de las llamadas de [**enlace**](/windows/win32/api/winsock/nf-winsock-bind) posteriores difiere en función de la dirección de red especificada en cada llamada **de** enlace.

En la tabla siguiente se describe el comportamiento que se produce en Windows XP y versiones anteriores cuando un segundo socket intenta enlazarse a una dirección enlazada previamente por un primer socket mediante opciones de socket específicas.

> [!NOTE]  
> En la tabla siguiente, "carácter comodín" denota la dirección de carácter comodín para el protocolo especificado (por ejemplo, "0.0.0.0" para IPv4 y "::" para IPv6). "Específico" denota una dirección IP específica asignada a una interfaz. Las celdas de la tabla indican si el enlace se ha realizado correctamente ("Correcto") o si se devuelve un error ("INUSE" para el error [WSAEADDRINUSE;](windows-sockets-error-codes-2.md) "ACCESS" para el error [WSAEACCES).](windows-sockets-error-codes-2.md)

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Primera <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>llamada de</strong></a> enlace</td>
        <td bgcolor="#C0C0C0" colspan="6">Segunda <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>llamada de</strong></a> enlace</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">Valor predeterminado</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td bgcolor="#C0C0C0">Específico</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td bgcolor="#C0C0C0">Específico</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td bgcolor="#C0C0C0">Específico</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">Valor predeterminado</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
</table>

Cuando dos sockets están enlazados al mismo número de puerto pero en interfaces explícitas diferentes, no hay ningún conflicto. Por ejemplo, en el caso de que un equipo tenga dos interfaces IP, 10.0.0.1 y 10.99.99.99, Si la primera llamada para enlazar está en 10.0.0.1 con el puerto establecido en 5150 y se especificó **SO \_ EXCLUSIVEADDRUSE,** se realizará una segunda llamada para enlazar en 10.99.99.99 con el puerto también establecido en 5150 y ninguna opción especificada se realizará correctamente. [](/windows/win32/api/winsock/nf-winsock-bind)  Sin embargo, si el primer socket está enlazado a la dirección comodín y al puerto 5150, cualquier llamada de enlace posterior al puerto 5150 con el conjunto **SO \_ EXCLUSIVEADDRUSE** producirá un error con [WSAEADDRINUSE](windows-sockets-error-codes-2.md) o [WSAEACCES devueltos](windows-sockets-error-codes-2.md) por la operación **de** enlace.

En el caso de [](/windows/win32/api/winsock/nf-winsock-bind) que la primera llamada a bind establece SO  **\_ REUSEADDR** o ninguna opción de socket, la segunda llamada de enlace "secuestrará" el puerto y la aplicación no podrá determinar cuál de los dos sockets recibió paquetes específicos enviados al puerto "compartido".

Una aplicación típica que llama a la función [**bind**](/windows/win32/api/winsock/nf-winsock-bind) no asigna el socket enlazado para uso exclusivo, a menos que se llame a la opción de socket **SO \_ EXCLUSIVEADDRUSE** en el socket antes de llamar a la función **bind.** Si una aplicación cliente se enlaza a un puerto efímero o a un puerto específico antes de que una aplicación de servidor se enlace al mismo puerto, pueden producirse problemas. La aplicación de servidor puede enlazarse forzadamente al mismo puerto mediante la  opción de socket **SO \_ REUSEADDR** en el socket antes de llamar a la función de enlace, pero el comportamiento de todos los sockets enlazados a ese puerto es indeterminado. Si la aplicación de servidor intenta usar la opción de socket **SO \_ EXCLUSIVEADDRUSE** para el uso exclusivo del puerto, se producirá un error en la solicitud.

Por el contrario, un socket con **el conjunto SO \_ EXCLUSIVEADDRUSE** no se puede reutilizar necesariamente inmediatamente después del cierre del socket. Por ejemplo, si un socket de escucha con el conjunto **SO \_ EXCLUSIVEADDRUSE** acepta una conexión y se cierra posteriormente, otro socket (también con **SO \_ EXCLUSIVEADDRUSE)** no puede enlazarse al mismo puerto que el primer socket hasta que la conexión original se vuelva inactiva.

Este problema puede complicarse porque es posible que el protocolo de transporte subyacente no finalice la conexión aunque se haya cerrado el socket. Incluso después de que la aplicación haya cerrado el socket, el sistema debe transmitir los datos almacenados en búfer, enviar un mensaje de desconexión correcta al elemento del mismo nivel y esperar un mensaje de desconexión correcta correspondiente del mismo nivel. Es posible que el protocolo de transporte subyacente nunca libere la conexión; Por ejemplo, el elemento del mismo nivel que participa en la conexión original podría anunciar una ventana de tamaño cero o cualquier otra forma de configuración de "ataque". En tal caso, la conexión de cliente permanece en un estado activo a pesar de la solicitud para cerrarla, ya que los datos no reconocidos permanecen en el búfer.

Para evitar esta situación, las aplicaciones de red deben garantizar un cierre correcto mediante una llamada a [**shutdown**](/windows/win32/api/winsock/nf-winsock-shutdown) con la marca SD SEND establecida y, a continuación, esperar en un \_ bucle de [**recv**](/windows/win32/api/winsock/nf-winsock-recv) hasta que se devuelvan cero bytes a través de la conexión. Esto garantiza que el mismo nivel recibe todos los datos y, del mismo modo, confirma con el mismo nivel que ha recibido todos los datos transmitidos, así como evita el problema de reutilización de puertos mencionado anteriormente.

La opción de socket SO LINGER se puede establecer en un socket para evitar que el puerto haga la transición a un estado de espera "activo"; sin embargo, esto no se recomienda, ya que puede provocar efectos deseados, como restablecer las \_ conexiones. Por ejemplo, si el mismo nivel recibe los datos, pero no los reconoce, y el equipo local cierra el socket con SO LINGER establecido en él, se restablece la conexión entre los dos equipos y el mismo nivel descarta los datos no \_ reconocidos. Elegir un tiempo adecuado para quedarse es difícil, ya que un valor de tiempo de espera más pequeño suele dar lugar a conexiones anuladas repentinamente, mientras que los valores de tiempo de espera más grandes dejan al sistema vulnerable a ataques por denegación de servicio (al establecer muchas conexiones y detener o bloquear subprocesos de aplicación). El cierre de un socket que tiene un valor de tiempo de espera de linger distinto de cero también puede hacer que [**la llamada a closesocket**](/windows/win32/api/winsock/nf-winsock-closesocket) se bloquee.

## <a name="enhanced-socket-security"></a>Seguridad de socket mejorada

Se agregó una seguridad de socket mejorada con la versión de Windows Server 2003. En versiones anteriores del sistema operativo del servidor de Microsoft, la seguridad de sockets predeterminada permitía fácilmente a los procesos secuestrar puertos de aplicaciones poco específicas. En Windows Server 2003, los sockets no se pueden compartir de forma predeterminada. Por lo tanto, si una aplicación desea permitir que otros procesos vuelvan a usar un puerto en el que ya está enlazado un socket, debe habilitarlo específicamente. Si ese es el caso, el primer socket para llamar a [**bind**](/windows/win32/api/winsock/nf-winsock-bind) en el puerto debe tener **SO \_ REUSEADDR** establecido en el socket. La única excepción a este  caso se produce cuando la segunda llamada de enlace la realiza la misma cuenta de usuario que realizó la llamada original para **enlazar**. Esta excepción existe únicamente para proporcionar compatibilidad con versiones anteriores.

En la tabla siguiente se describe el comportamiento que se produce en Windows Server 2003 y sistemas operativos posteriores cuando un segundo socket intenta enlazarse a una dirección enlazada previamente por un primer socket mediante opciones de socket específicas.

> [!NOTE]
> En la tabla siguiente, "carácter comodín" denota la dirección de carácter comodín para el protocolo especificado (por ejemplo, "0.0.0.0" para IPv4 y "::" para IPv6). "Específico" denota una dirección IP específica asignada a una interfaz. Las celdas de la tabla indican si el enlace se ha realizado correctamente ("Correcto") o el error devuelto ("INUSE" para el error [WSAEADDRINUSE;](windows-sockets-error-codes-2.md) "ACCESS" para el error [WSAEACCES).](windows-sockets-error-codes-2.md)
>
> Tenga en cuenta también que en esta tabla específica, ambas llamadas [**de**](/windows/win32/api/winsock/nf-winsock-bind) enlace se realizan en la misma cuenta de usuario.

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Primera <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>llamada de</strong></a> enlace</td>
        <td bgcolor="#C0C0C0" colspan="6">Segunda <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>llamada de</strong></a> enlace</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">Valor predeterminado</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td bgcolor="#C0C0C0">Específico</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td bgcolor="#C0C0C0">Específico</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td bgcolor="#C0C0C0">Específico</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">Valor predeterminado</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td>INUSE</td>
        <td>Correcto</td>
        <td>ACCESS</td>
        <td>Correcto</td>
        <td>INUSE</td>
        <td>Correcto</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>Correcto</td>
        <td>INUSE</td>
        <td>Correcto</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td>INUSE</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>INUSE</td>
        <td>Correcto</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>Correcto</td>
        <td>INUSE</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>Correcto</td>
        <td>INUSE</td>
        <td>Correcto</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
</table>

Unas cuantas entradas en la tabla anterior explicaciones de los fundamentos.

Por ejemplo, si el primer llamador establece **SO \_ EXCLUSIVEADDRUSE** en una dirección específica y el segundo  llamador intenta llamar a [**bind**](/windows/win32/api/winsock/nf-winsock-bind) con una dirección comodín en el mismo puerto, la segunda llamada de enlace se realizará correctamente. En este caso concreto, el segundo llamador está enlazado a todas las interfaces, excepto a la dirección específica a la que está enlazado el primer autor de la llamada. Tenga en cuenta que lo contrario de este caso no es cierto: si el primer autor de la  llamada establece **SO \_ EXCLUSIVEADDRUSE** y las llamadas se enlazan con la marca comodín, el segundo llamador no puede llamar al enlace con el mismo puerto. 

El comportamiento del enlace de socket cambia cuando las llamadas de enlace de socket se realizan en cuentas de usuario diferentes. En la tabla siguiente se especifica el comportamiento que se produce en Windows Server 2003 y sistemas operativos posteriores cuando un segundo socket intenta enlazarse a una dirección enlazada previamente por un primer socket mediante opciones de socket específicas y una cuenta de usuario diferente.

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Primera <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>llamada de</strong></a> enlace</td>
        <td bgcolor="#C0C0C0" colspan="6">Segunda <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>llamada de</strong></a> enlace</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">Valor predeterminado</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td bgcolor="#C0C0C0">Específico</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td bgcolor="#C0C0C0">Específico</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td bgcolor="#C0C0C0">Específico</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">Valor predeterminado</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>Correcto</td>
        <td>INUSE</td>
        <td>Correcto</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>Correcto</td>
        <td>INUSE</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>Correcto</td>
        <td>INUSE</td>
        <td>Correcto</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
</table>

Tenga en cuenta que el comportamiento predeterminado es diferente cuando las llamadas [**de**](/windows/win32/api/winsock/nf-winsock-bind) enlace se realizan en cuentas de usuario diferentes. Si el primer autor de la llamada no establece ninguna opción en el socket y se enlaza a la dirección comodín, el segundo llamador no puede establecer la opción **SO \_ REUSEADDR** y enlazar correctamente al mismo puerto. El comportamiento predeterminado sin ningún conjunto de opciones también devuelve un error.

En Windows Vista y versiones posteriores, se puede crear un socket de pila dual que funcione sobre IPv6 e IPv4. Cuando se enlaza un socket de pila dual a la dirección comodín, el puerto especificado se reserva en las pilas de red IPv4 e IPv6 y se realizan las comprobaciones asociadas a **SO \_ REUSEADDR** y **SO \_ EXCLUSIVEADDRUSE** (si se establece). Estas comprobaciones deben realizarse correctamente en ambas pilas de red. Por ejemplo, si un socket TCP de doble pila establece **SO \_ EXCLUSIVEADDRUSE** y, a continuación, intenta enlazar al puerto 5000, no se puede enlazar previamente ningún otro socket TCP al puerto 5000 (comodín o específico). En este caso, si un socket TCP IPv4 se enlazaba previamente a [](/windows/win32/api/winsock/nf-winsock-bind) la dirección de bucle atrás en el puerto 5000, la llamada de enlace para el socket de pila dual produciría un error [con WSAEACCES.](windows-sockets-error-codes-2.md)

## <a name="application-strategies"></a>Estrategias de aplicación

Al desarrollar aplicaciones de red que funcionan en la capa de socket, es importante tener en cuenta el tipo de seguridad de socket necesario. Las aplicaciones cliente ( aplicaciones que conectan o envían datos a un servicio) rara vez requieren pasos adicionales, ya que se enlazan a un puerto local aleatorio (efímero). Si el cliente requiere un enlace de puerto local específico para funcionar correctamente, debe tener en cuenta la seguridad del socket.

La **opción SO \_ REUSEADDR** tiene muy pocos usos en aplicaciones normales, aparte de los sockets de multidifusión donde los datos se entregan a todos los sockets enlazados en el mismo puerto. De lo contrario, cualquier aplicación que establece esta opción de socket debe rediseñarse para quitar la dependencia, ya que es vulnerable a "secuestro de sockets". Siempre que se pueda usar la opción de socket **SO \_ REUSEADDR** para secuestrar potencialmente un puerto en una aplicación de servidor, se debe considerar que la aplicación no es segura.

Todas las aplicaciones de servidor deben **establecer SO \_ EXCLUSIVEADDRUSE para** un alto nivel de seguridad de sockets. No solo impide que el software malintencionado secuestre el puerto, sino que también indica si otra aplicación está enlazada o no al puerto solicitado. Por ejemplo, se [](/windows/win32/api/winsock/nf-winsock-bind) producirá un error en una llamada para enlazar en la dirección comodín mediante un proceso con la opción de socket **SO \_ EXCLUSIVEADDRUSE** establecida si otro proceso está enlazado actualmente al mismo puerto en una interfaz específica.

Por último, aunque se ha mejorado la seguridad de sockets en Windows Server 2003, una aplicación siempre debe establecer la opción de socket **SO \_ EXCLUSIVEADDRUSE** para asegurarse de que se enlaza a todas las interfaces específicas que el proceso ha solicitado. La seguridad de sockets en Windows Server 2003 agrega un mayor nivel de seguridad para las aplicaciones heredadas, pero los desarrolladores de aplicaciones deben seguir diseñando sus productos teniendo en cuenta todos los aspectos de la seguridad.
