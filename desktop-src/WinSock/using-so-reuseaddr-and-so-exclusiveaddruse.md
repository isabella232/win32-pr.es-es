---
description: El desarrollo de una infraestructura de red segura de alto nivel es una prioridad para la mayoría de los desarrolladores de aplicaciones de red. Sin embargo, a menudo se pasa por alto la seguridad de socket a pesar de ser muy importante a la hora de considerar una solución totalmente segura.
ms.assetid: b37a3e33-65ee-43b1-bc8b-3280db7ebee4
title: Usar SO_REUSEADDR y SO_EXCLUSIVEADDRUSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa4024f031102cbd634c235bb39f4c7860e6c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814355"
---
# <a name="using-so_reuseaddr-and-so_exclusiveaddruse"></a>Usar SO \_ REUSEADDR y so \_ EXCLUSIVEADDRUSE

El desarrollo de una infraestructura de red segura de alto nivel es una prioridad para la mayoría de los desarrolladores de aplicaciones de red. Sin embargo, a menudo se pasa por alto la seguridad de socket a pesar de ser muy importante a la hora de considerar una solución totalmente segura. La seguridad de sockets, específicamente, se ocupa de los procesos que se enlazan al mismo puerto previamente enlazado por otro proceso de aplicación. En el pasado, era posible que una aplicación de red "secuestrara" el puerto de otra aplicación, lo que podía conducir fácilmente a un ataque de denegación de servicio o a un robo de datos.

En general, la seguridad de sockets se aplica a los procesos del lado servidor. Más concretamente, la seguridad de sockets se aplica a cualquier aplicación de red que acepte conexiones y reciba tráfico de datagramas IP. Estas aplicaciones normalmente se enlazan a un puerto conocido y son destinos comunes del código de red malintencionado.

Es menos probable que las aplicaciones cliente sean los objetivos de estos ataques, no porque son menos susceptibles, pero como la mayoría de los clientes se enlazan a puertos locales "efímeros" en lugar de a puertos estáticos de "servicio". Las aplicaciones de red de cliente siempre se deben enlazar a los puertos efímeros (especificando el puerto 0 en la estructura [**SOCKADDR**](sockaddr-2.md) a la que apunta el parámetro *Name* al llamar a la función [**BIND**](/windows/win32/api/winsock/nf-winsock-bind) ) a menos que haya una buena razón de arquitectura que no sea. Los puertos locales efímeros se componen de puertos mayores que el puerto 49151. La mayoría de las aplicaciones de servidor para servicios dedicados se enlazan a un puerto reservado conocido que es menor o igual que el puerto 49151. Por lo tanto, para la mayoría de las aplicaciones, normalmente no hay un conflicto para las solicitudes de enlace entre las aplicaciones cliente y servidor.

En esta sección se describe el nivel de seguridad predeterminado en varias plataformas de Microsoft Windows y cómo las opciones específicas de sockets **, por lo que \_ REUSEADDR** y [ \_ EXCLUSIVEADDRUSE](so-exclusiveaddruse.md) afectan a la seguridad de la aplicación de red. En Windows Server 2003 y versiones posteriores, hay disponible una característica adicional denominada seguridad de sockets mejorada. La disponibilidad de estas opciones de socket y la seguridad mejorada de los sockets varía en función de las versiones de los sistemas operativos de Microsoft, tal y como se muestra en la tabla siguiente.

| Plataforma            | \_REUSEADDR | \_EXCLUSIVEADDRUSE                  | Seguridad de sockets mejorada |
|---------------------|---------------|---------------------------------------|--------------------------|
| Windows 95          | Disponible     | No disponible                         | No disponible            |
| Windows 98          | Disponible     | No disponible                         | No disponible            |
| Windows me          | Disponible     | No disponible                         | No disponible            |
| Windows NT 4.0      | Disponible     | Disponible en Service Pack 4 y versiones posteriores | No disponible            |
| Windows 2000        | Disponible     | Disponible                             | No disponible            |
| Windows XP          | Disponible     | Disponible                             | No disponible            |
| Windows Server 2003 | Disponible     | Disponible                             | Disponible                |
| Windows Vista       | Disponible     | Disponible                             | Disponible                |
| Windows Server 2008 | Disponible     | Disponible                             | Disponible                |
| Windows 7and más reciente  | Disponible     | Disponible                             | Disponible                |

## <a name="using-so_reuseaddr"></a>Usar SO \_ REUSEADDR

La opción de socket **so \_ REUSEADDR** permite que un socket se enlace forzosamente a un puerto en uso por otro socket. El segundo [**socket llama a la llamada a My**](/windows/win32/api/winsock/nf-winsock-setsockopt) con el parámetro *optname* establecido en **\_ REUSEADDR** y el parámetro *optval* establecido en un valor booleano de **true** antes de llamar a [**BIND**](/windows/win32/api/winsock/nf-winsock-bind) en el mismo puerto que el socket original. Una vez que el segundo socket se ha enlazado correctamente, el comportamiento de todos los sockets enlazados a ese puerto es indeterminado. Por ejemplo, si todos los sockets en el mismo puerto proporcionan el servicio TCP, no se puede garantizar que las solicitudes de conexión TCP entrantes a través del puerto se controlen mediante el socket correcto; el comportamiento no es determinista. Un programa malintencionado puede usarse de **modo que \_ REUSEADDR** para enlazar de forma forzada los sockets que ya están en uso para los servicios de protocolo de red estándar con el fin de denegar el acceso a esos servicios. No se requiere ningún privilegio especial para usar esta opción.

Si una aplicación cliente se enlaza a un puerto antes de que una aplicación de servidor pueda enlazar con el mismo puerto, pueden producirse problemas. Si la aplicación de servidor se enlaza de forma forzada mediante la opción de socket **so de \_ REUSEADDR** al mismo puerto, el comportamiento de todos los sockets enlazados a ese puerto es indeterminado.

La excepción a este comportamiento no determinista son los sockets de multidifusión. Si dos sockets están enlazados a la misma interfaz y puerto y son miembros del mismo grupo de multidifusión, los datos se entregarán a ambos sockets, en lugar de a una elección arbitrariamente.

## <a name="using-so_exclusiveaddruse"></a>Usar SO \_ EXCLUSIVEADDRUSE

Antes de **que \_** se introdujera la opción de socket EXCLUSIVEADDRUSE, había muy poco un desarrollador de aplicaciones de red podía hacer para impedir que un programa malintencionado se enlazase al puerto en el que la aplicación de red tenía sus propios Sockets enlazados. Con el fin de solucionar este problema de seguridad, Windows Sockets presentó la opción de socket for **\_ EXCLUSIVEADDRUSE** , que estaba disponible en Windows NT 4,0 con Service Pack 4 (SP4) y versiones posteriores.

La opción de socket **so \_ EXCLUSIVEADDRUSE** solo la pueden usar los miembros del grupo de seguridad Administrators en Windows XP y versiones anteriores. Los motivos por los que se cambió este requisito en Windows Server 2003 y versiones posteriores se describen más adelante en el artículo.

La opción for **\_ EXCLUSIVEADDRUSE** se establece mediante una llamada [**a la función My con el parámetro**](/windows/win32/api/winsock/nf-winsock-setsockopt) *optname* establecido en for **\_ EXCLUSIVEADDRUSE** y el parámetro *optval* establecido en un valor booleano **true** antes de enlazar el socket. Una vez establecida la opción, el comportamiento de las llamadas de [**enlace**](/windows/win32/api/winsock/nf-winsock-bind) subsiguientes varía en función de la dirección de red especificada en cada llamada de **enlace** .

En la tabla siguiente se describe el comportamiento que se produce en Windows XP y versiones anteriores cuando un segundo socket intenta enlazar con una dirección enlazada previamente a por un primer socket usando opciones de socket específicas.

> [!NOTE]  
> En la tabla siguiente, "carácter comodín" denota la dirección comodín para el protocolo especificado (por ejemplo, "0.0.0.0" para IPv4 y "::" para IPv6). "Específico" denota una dirección IP específica asignada a una interfaz. Las celdas de la tabla indican si el enlace se realiza correctamente ("Success") o si se devuelve un error ("INUSE" para el error [WSAEADDRINUSE](windows-sockets-error-codes-2.md) ; "ACCESS" para el error [WSAEACCES](windows-sockets-error-codes-2.md) ).

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Primera llamada de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>enlace</strong></a></td>
        <td bgcolor="#C0C0C0" colspan="6">Segunda llamada de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>enlace</strong></a></td>
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
        <td>Property</td>
        <td>Property</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>Property</td>
        <td>Property</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>Property</td>
        <td>Property</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>Property</td>
        <td>Property</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td>Property</td>
        <td>Property</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>Property</td>
        <td>Property</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>Property</td>
        <td>Property</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>Property</td>
        <td>Property</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td>Property</td>
        <td>Property</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>Property</td>
        <td>Property</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>Property</td>
        <td>Property</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>Property</td>
        <td>Property</td>
    </tr>
</table>

Cuando dos sockets están enlazados al mismo número de puerto pero en interfaces explícitas diferentes, no hay ningún conflicto. Por ejemplo, en el caso de que un equipo tenga dos interfaces IP, 10.0.0.1 y 10.99.99.99, si la primera llamada a [**BIND**](/windows/win32/api/winsock/nf-winsock-bind) está en 10.0.0.1 con el puerto establecido en 5150 y, **por tanto, \_ EXCLUSIVEADDRUSE** especificado, una segunda llamada a **BIND** en 10.99.99.99 con el puerto también se establece en 5150 y ninguna de las opciones especificadas se realizará correctamente. Sin embargo, si el primer socket se enlaza a la dirección comodín y al puerto 5150, se producirá un error en cualquier llamada de enlace subsiguiente al puerto 5150 con el conjunto de **\_ EXCLUSIVEADDRUSE** , con [WSAEADDRINUSE](windows-sockets-error-codes-2.md) o [WSAEACCES](windows-sockets-error-codes-2.md) devuelto por la operación de **enlace** .

En el caso de que la primera llamada a [**BIND**](/windows/win32/api/winsock/nf-winsock-bind) establezca, de **modo que \_ REUSEADDR** o ninguna opción de socket, la segunda llamada de **enlace** "secuestrará" el puerto y la aplicación no podrá determinar cuál de los dos sockets recibió paquetes específicos enviados al puerto "compartido".

Una aplicación típica que llama a la función [**BIND**](/windows/win32/api/winsock/nf-winsock-bind) no asigna el socket enlazado para uso exclusivo, a menos que se llame a la opción de socket for **\_ EXCLUSIVEADDRUSE** en el socket antes de la llamada a la función de **enlace** . Si una aplicación cliente se enlaza a un puerto efímero o a un puerto específico antes de que una aplicación de servidor se enlace al mismo puerto, pueden producirse problemas. La aplicación de servidor puede enlazar de forma forzada al mismo puerto mediante la opción de socket **so \_ REUSEADDR** en el socket antes de llamar a la función de **enlace** , pero el comportamiento de todos los sockets enlazados a ese puerto es entonces indeterminado. Si la aplicación de servidor intenta utilizar la opción de socket for **\_ EXCLUSIVEADDRUSE** para el uso exclusivo del puerto, se producirá un error en la solicitud.

Por el contrario, un socket con el conjunto de **so for \_ EXCLUSIVEADDRUSE** no se puede volver a usar inmediatamente después del cierre del socket. Por ejemplo, si un socket de escucha con el conjunto de **\_ EXCLUSIVEADDRUSE** acepta una conexión y, a continuación, se cierra, otro socket (también con **\_ EXCLUSIVEADDRUSE**) no se puede enlazar al mismo puerto que el primer socket hasta que la conexión original pasa a estar inactiva.

Este problema puede ser complicado porque es posible que el protocolo de transporte subyacente no finalice la conexión aunque el socket se haya cerrado. Incluso después de que la aplicación haya cerrado el socket, el sistema debe transmitir los datos almacenados en búfer, enviar un mensaje de desconexión sin problemas al elemento del mismo nivel y esperar un mensaje de desconexión estable correspondiente del elemento del mismo nivel. Es posible que el protocolo de transporte subyacente nunca libere la conexión; por ejemplo, el elemento del mismo nivel que participa en la conexión original puede anunciar una ventana de tamaño cero o algún otro tipo de configuración de "ataque". En tal caso, la conexión de cliente permanece en estado activo a pesar de la solicitud de cierre, ya que los datos no confirmados permanecen en el búfer.

Para evitar esta situación, las aplicaciones de red deben garantizar un cierre estable llamando a [**Shutdown**](/windows/win32/api/winsock/nf-winsock-shutdown) con la \_ marca de envío SD establecida y, a continuación, esperan en un bucle [**RECV**](/windows/win32/api/winsock/nf-winsock-recv) hasta que se devuelvan cero bytes a través de la conexión. Esto garantiza que todos los datos son recibidos por el elemento del mismo nivel y también confirma con el par que ha recibido todos los datos transmitidos, así como para evitar el problema de reutilización del puerto mencionado anteriormente.

La \_ opción de socket persistente se puede establecer en un socket para evitar que el puerto pase a un estado de espera "activo"; sin embargo, esto no se recomienda, ya que puede dar lugar a efectos deseados, como restablecer conexiones. Por ejemplo, si los datos son recibidos por el elemento del mismo nivel, pero permanecen sin confirmar, y el equipo local cierra el socket con la \_ configuración de permanencia establecida en él, se restablece la conexión entre los dos equipos y los datos no confirmados se descartan por el mismo nivel. La elección de un tiempo adecuado para la permanencia es difícil porque un valor de tiempo de espera más pequeño suele dar lugar a las conexiones anuladas repentinamente, mientras que los valores de tiempo de espera mayores dejan que el sistema sea vulnerable a los ataques por denegación de servicio (mediante la creación de muchas conexiones y la posible detención o bloqueo de subprocesos de aplicación) Cerrar un socket que tenga un valor de tiempo de espera de permanencia distinto de cero también puede hacer que la llamada [**closesocket**](/windows/win32/api/winsock/nf-winsock-closesocket) se bloquee.

## <a name="enhanced-socket-security"></a>Seguridad de sockets mejorada

Se ha agregado seguridad de socket mejorada con la versión de Windows Server 2003. En las versiones anteriores del sistema operativo de servidor de Microsoft, la seguridad de sockets predeterminada permitía los procesos para secuestrar puertos de aplicaciones no sospechosas. En Windows Server 2003, los sockets no se encuentran en un estado que se pueda compartir de forma predeterminada. Por lo tanto, si una aplicación desea permitir que otros procesos reutilicen un puerto en el que ya está enlazado un socket, debe habilitarlo específicamente. En ese caso, el primer socket para llamar a [**BIND**](/windows/win32/api/winsock/nf-winsock-bind) en el puerto debe tener **\_ REUSEADDR** establecido en el socket. La única excepción a este caso se produce cuando la segunda llamada de **enlace** la realiza la misma cuenta de usuario que realizó la llamada original a **BIND**. Esta excepción existe únicamente para proporcionar compatibilidad con versiones anteriores.

En la tabla siguiente se describe el comportamiento que se produce en Windows Server 2003 y los sistemas operativos posteriores cuando un segundo socket intenta enlazar con una dirección enlazada previamente a por un primer socket usando opciones de socket específicas.

> [!NOTE]
> En la tabla siguiente, "carácter comodín" denota la dirección comodín para el protocolo especificado (por ejemplo, "0.0.0.0" para IPv4 y "::" para IPv6). "Específico" denota una dirección IP específica asignada a una interfaz. Las celdas de la tabla indican si el enlace se realiza correctamente ("Success") o el error devuelto ("INUSE" para el error [WSAEADDRINUSE](windows-sockets-error-codes-2.md) ; "ACCESS" para el error [WSAEACCES](windows-sockets-error-codes-2.md) ).
>
> Tenga en cuenta también que en esta tabla específica, ambas llamadas de [**enlace**](/windows/win32/api/winsock/nf-winsock-bind) se realizan en la misma cuenta de usuario.

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Primera llamada de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>enlace</strong></a></td>
        <td bgcolor="#C0C0C0" colspan="6">Segunda llamada de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>enlace</strong></a></td>
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
        <td>Property</td>
        <td>Correcto</td>
        <td>ACCESS</td>
        <td>Correcto</td>
        <td>Property</td>
        <td>Correcto</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>Correcto</td>
        <td>Property</td>
        <td>Correcto</td>
        <td>ACCESS</td>
        <td>Property</td>
        <td>Property</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td>Property</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>Property</td>
        <td>Correcto</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>Correcto</td>
        <td>Property</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>Property</td>
        <td>Property</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td>Property</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>Property</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>Correcto</td>
        <td>Property</td>
        <td>Correcto</td>
        <td>ACCESS</td>
        <td>Property</td>
        <td>Property</td>
    </tr>
</table>

Algunas de las entradas de la tabla anterior explican la explicación.

Por ejemplo, si el primer llamador establece **\_ EXCLUSIVEADDRUSE** en una dirección específica y el segundo intenta llamar a [**BIND**](/windows/win32/api/winsock/nf-winsock-bind) con una dirección comodín en el mismo puerto, la segunda llamada de **enlace** se realizará correctamente. En este caso concreto, el segundo llamador se enlaza a todas las interfaces excepto la dirección específica a la que está enlazado el primer llamador. Tenga en cuenta que la inverso de este caso no es true: Si el primer llamador establece de **modo que \_ EXCLUSIVEADDRUSE** y llama a **BIND** con la marca de comodín, el segundo llamador no puede llamar a **BIND** con el mismo puerto.

El comportamiento de enlace del socket cambia cuando las llamadas de enlace de socket se realizan en diferentes cuentas de usuario. En la tabla siguiente se especifica el comportamiento que se produce en Windows Server 2003 y los sistemas operativos posteriores cuando un segundo socket intenta enlazar con una dirección enlazada previamente a por un primer socket usando opciones de socket específicas y una cuenta de usuario diferente.

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Primera llamada de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>enlace</strong></a></td>
        <td bgcolor="#C0C0C0" colspan="6">Segunda llamada de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>enlace</strong></a></td>
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
        <td>Property</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>Property</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>Correcto</td>
        <td>Property</td>
        <td>Correcto</td>
        <td>ACCESS</td>
        <td>Property</td>
        <td>Property</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td>Property</td>
        <td>ACCESS</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>Property</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>Correcto</td>
        <td>Property</td>
        <td>Correcto</td>
        <td>Correcto</td>
        <td>Property</td>
        <td>Property</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Wildcard (Carácter comodín)</td>
        <td>Property</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>Property</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específico</td>
        <td>Correcto</td>
        <td>Property</td>
        <td>Correcto</td>
        <td>ACCESS</td>
        <td>Property</td>
        <td>Property</td>
    </tr>
</table>

Tenga en cuenta que el comportamiento predeterminado es diferente cuando las llamadas de [**enlace**](/windows/win32/api/winsock/nf-winsock-bind) se realizan en distintas cuentas de usuario. Si el primer autor de la llamada no establece ninguna opción en el socket y se enlaza a la dirección comodín, el segundo llamador no puede establecer la opción **so de \_ REUSEADDR** y enlazarse correctamente con el mismo puerto. El comportamiento predeterminado sin ningún conjunto de opciones también devuelve un error.

En Windows Vista y versiones posteriores, se puede crear un socket de pila doble que opere a través de IPv6 e IPv4. Cuando un socket de pila doble se enlaza a la dirección comodín, el puerto especificado se reserva en las pilas de red IPv4 e IPv6, y las comprobaciones asociadas con **, por lo tanto, \_ REUSEADDR** y **, por tanto \_** , se realiza EXCLUSIVEADDRUSE (si se establece). Estas comprobaciones deben realizarse en ambas pilas de red. Por ejemplo, si un socket TCP de pila dual se establece de **modo que \_ EXCLUSIVEADDRUSE** y, a continuación, intenta enlazar con el puerto 5000, no se puede enlazar previamente ningún otro socket tcp al puerto 5000 (ya sea comodín o específico). En este caso, si un socket TCP IPv4 estaba previamente enlazado a la dirección de bucle invertido en el puerto 5000, la llamada de [**enlace**](/windows/win32/api/winsock/nf-winsock-bind) para el socket de pila dual produciría un error con [WSAEACCES](windows-sockets-error-codes-2.md).

## <a name="application-strategies"></a>Estrategias de aplicación

Al desarrollar una aplicación de red que opere en el nivel de socket, es importante tener en cuenta el tipo de seguridad de socket necesario. Las aplicaciones cliente de: las aplicaciones que se conectan o envían datos a un servicio de, raramente requieren pasos adicionales, ya que se enlazan a un puerto local aleatorio (efímero). Si el cliente requiere un enlace de puerto local específico para que funcione correctamente, debe tener en cuenta la seguridad del socket.

La opción for **\_ REUSEADDR** tiene muy pocos usos en aplicaciones normales, además de los sockets de multidifusión, donde los datos se entregan a todos los sockets enlazados en el mismo puerto. De lo contrario, cualquier aplicación que establezca esta opción de socket se debe volver a diseñar para quitar la dependencia, ya que es eminently vulnerable a "secuestro de socket". Siempre que se pueda usar la opción de socket **\_ REUSEADDR** para secuestrar un puerto en una aplicación de servidor, se debe considerar que la aplicación no es segura.

Todas las aplicaciones de servidor deben establecerse de **modo que \_ EXCLUSIVEADDRUSE** para un nivel de seguridad de socket fuerte. No solo impide que el software malintencionado piratee el puerto, sino que también indica si otra aplicación está enlazada al puerto solicitado. Por ejemplo, se producirá un error en una llamada para [**enlazar**](/windows/win32/api/winsock/nf-winsock-bind) en la dirección comodín de un proceso con el conjunto de opciones de socket for **\_ EXCLUSIVEADDRUSE** si hay otro proceso enlazado actualmente al mismo puerto en una interfaz específica.

Por último, aunque la seguridad de sockets se ha mejorado en Windows Server 2003, una aplicación debe establecer siempre la opción de socket for **\_ EXCLUSIVEADDRUSE** para asegurarse de que se enlaza a todas las interfaces específicas que el proceso ha solicitado. La seguridad de socket en Windows Server 2003 agrega un mayor nivel de seguridad para las aplicaciones heredadas, pero los desarrolladores de aplicaciones deben seguir diseñando sus productos con todos los aspectos de seguridad en mente.
