---
description: La abstracción del socket de flujo incluye la noción de datos fuera de banda (OOB).
ms.assetid: 1a517885-2688-421f-9389-2d329e5c3d56
title: Protocol-Independent datos fuera de banda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1918ba1525462f4352d76c989d7fb5d92beeb59766f92cdccbdda66a5b82744d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860835"
---
# <a name="protocol-independent-out-of-band-data"></a>Protocol-Independent datos fuera de banda

La abstracción del socket de flujo incluye la noción de datos fuera de banda (OOB). Muchos protocolos permiten que partes de los datos entrantes se marquen como especiales de alguna manera, y estos bloques de datos especiales se pueden entregar al usuario fuera de la secuencia normal. Algunos ejemplos son los datos rápidos en X.25 y otros protocolos OSI, y los datos urgentes en BSD UNIX uso de TCP. En la sección siguiente se describe el control de datos de OOB de forma independiente del protocolo. Una explicación de los datos de OOB implementados con datos urgentes de TCP sigue la explicación independiente del protocolo. En cada explicación, el uso de [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) también implica [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)y [**WSARecvFrom,**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)y las referencias a [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) también se aplican a [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect).

## <a name="protocol-independent-oob-data"></a>Datos de OOB independientes del protocolo

Los datos de OOB son un canal de transmisión independiente lógicamente asociado a cada par de sockets de flujo conectados. Los datos de OOB se pueden entregar al usuario independientemente de los datos normales. La abstracción define que las instalaciones de datos de OOB deben admitir la entrega confiable de al menos un bloque de datos OOB a la vez. Este bloque de datos puede contener al menos un byte de datos y al menos un bloque de datos OOB puede estar pendiente de entrega al usuario en cualquier momento. Para los protocolos de comunicaciones que admiten la señalización en banda (como TCP, donde los datos urgentes se entregan en secuencia con los datos normales), el sistema normalmente extrae los datos de OOB del flujo de datos normal y los almacena por separado (dejando un espacio en el flujo de datos normal). Esto permite a los usuarios elegir entre recibir los datos de OOB en orden y recibirlos fuera de la secuencia sin tener que almacenar en búfer todos los datos intermedios. Es posible echar un vistazo a los datos fuera de banda (OOB).

Un usuario puede determinar si algún dato de OOB está esperando ser leído mediante la función [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) o [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) con **SIOCATMARK** IOCTL. Para los protocolos en los que el concepto de la posición del bloque de datos OOB dentro del flujo de datos normal es significativo, como TCP, un proveedor de servicios Windows Sockets mantiene un marcador conceptual que indica la posición del último byte de los datos de OOB dentro del flujo de datos normal. Esto no es necesario para la implementación de las funciones **ioctlsocket** o **WSAIoctl** que **admiten SIOCATMARK**. Se requiere la presencia o ausencia de datos de OOB.

Para los protocolos en los que el concepto de la posición del bloque de datos OOB dentro del flujo de datos normal es significativo, una aplicación podría procesar datos fuera de banda en línea, como parte del flujo de datos normal. Esto se logra estableciendo la opción de socket SO \_ OOBINLINE con la [**función setsockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt) Para otros protocolos en los que los bloques de datos de OOB son realmente independientes del flujo de datos normal, el intento de establecer SO \_ OOBINLINE produce un error. Una aplicación puede usar la función [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) o [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) con **SIOCATMARK** IOCTL para determinar si hay algún dato OOB no leído antes de la marca. Por ejemplo, puede usar esta información para resincronizar con su par asegurándose de que todos los datos hasta la marca del flujo de datos se descartan cuando sea necesario.

Con SO \_ OOBINLINE deshabilitado (la configuración predeterminada):

-   Windows Sockets notifica a una aplicación un evento FD OOB, si la aplicación se registró para la notificación con \_ [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect), exactamente de la misma manera que se usa FD READ para notificar la presencia de datos \_ normales. Es decir, FD OOB se publica cuando llegan datos \_ de OOB sin datos de OOB previamente puestos en cola. La OOB de FD también se publica cuando se leen datos mediante la marca OOB MSG, mientras que algunos datos de OOB permanecen en cola después de que se haya devuelto \_ \_ la operación de lectura. Los mensajes DE LECTURA de FD \_ no se publican para los datos de OOB.
-   Windows Sockets devuelve de [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) con el socket *exceptfds* adecuado establecido si los datos de OOB se ponen en cola en el socket.
-   La aplicación puede llamar a [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) con MSG \_ OOB para leer el bloque de datos urgente en cualquier momento. El bloque de datos de OOB salta a la cola.
-   La aplicación puede llamar a [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) sin MSG \_ OOB para leer el flujo de datos normal. El bloque de datos OOB no aparece en el flujo de datos con datos normales. Si los datos de OOB permanecen después de cualquier llamada a **recv**, Windows Sockets notifica a la aplicación con FD OOB o \_ con *exceptfds* cuando se usa [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select).
-   Para los protocolos en los que los datos de OOB tienen una posición dentro del flujo de datos normal, una sola [**operación de recv**](/windows/desktop/api/winsock/nf-winsock-recv) no abarca esa posición. Una **recv** devuelve los datos normales antes de la marca y se requiere una segunda **recv** para empezar a leer los datos después de la marca.

Con SO \_ OOBINLINE habilitado:

-   Los mensajes OOB de FD \_ no se publican para los datos de OOB. Los datos de OOB se tratan como normales para las funciones [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) y [**WSAAsyncSelect,**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) y se indican estableciendo el socket en *readfds* o enviando un mensaje FD READ respectivamente. \_
-   La aplicación no puede llamar [**a recv**](/windows/desktop/api/winsock/nf-winsock-recv) con la marca OOB MSG \_ establecida para leer el bloque de datos OOB. Se devuelve el código de error WSAEINVAL.
-   La aplicación puede llamar a [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) sin la marca \_ OOB MSG establecida. Los datos de OOB se entregan en el orden correcto dentro del flujo de datos normal. Los datos de OOB nunca se mezclan con datos normales. Debe haber tres solicitudes de lectura para pasar los datos de OOB. El primero devuelve los datos normales antes del bloque de datos OOB, el segundo devuelve los datos de OOB y el tercero devuelve los datos normales después de los datos de OOB. En otras palabras, se conservan los límites del bloque de datos OOB.

La [**rutina WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) es especialmente adecuada para controlar la notificación de la presencia de datos fuera de banda cuando SO \_ OOBINLINE está desactivado.

## <a name="oob-data-in-tcp"></a>Datos de OOB en TCP

> [!IMPORTANT]
> La siguiente explicación de los datos fuera de banda (OOB), implementada con datos urgentes tcp, sigue el modelo usado en la distribución de software de Berkeley. Los usuarios y los implementadores deben tener en cuenta lo siguiente:

 

-   Hay, en la actualidad, dos interpretaciones en conflicto de [RFC 793](https://www.ietf.org/rfc/rfc793.txt) (donde se introduce el concepto).
-   La implementación de datos de OOB en la distribución de software de Berkeley (BSD) no se ajusta a los requisitos de host especificados en [RFC 1122](https://www.ietf.org/rfc/rfc1122.txt).

    En concreto, el puntero urgente TCP en BSD apunta al byte después del byte de datos urgente y un puntero TCP urgente compatible con RFC apunta al byte de datos urgente. Como resultado, si una aplicación envía datos urgentes desde una implementación compatible con BSD a una implementación compatible con RFC 1122, el receptor lee el byte de datos urgente incorrecto (lee el byte situado después del byte correcto en el flujo de datos como byte de datos urgente).

    Para minimizar los problemas de interoperabilidad, se recomienda a los escritores de aplicaciones que no usen datos de OOB a menos que sea necesario para interoperar con un servicio existente. Windows Los proveedores de sockets se animan a documentar la semántica de OOB (BSD o RFC 1122) que implementa su producto.

La llegada de un segmento TCP con el conjunto de marcas UG (para urgentes) indica la existencia de un solo byte de datos OOB dentro del flujo de datos TCP. El bloque de datos OOB tiene un tamaño de un byte. El puntero urgente es un desplazamiento positivo del número de secuencia actual en el encabezado TCP que indica la ubicación del bloque de datos OOB (ambiguamente, como se indicó en el anterior). Por lo tanto, podría apuntar a datos que aún no se han recibido.

Si SO OOBINLINE está deshabilitado (valor predeterminado) cuando llega el segmento TCP que contiene el byte al que apunta el puntero urgente, el bloque de datos OOB (un byte) se quita del flujo de datos y se almacena en \_ búfer. Si llega un segmento TCP posterior con la marca urgente establecida (y un nuevo puntero urgente), el byte OOB actualmente en cola se puede perder, ya que se reemplaza por el nuevo bloque de datos OOB (como sucede en la distribución de software de Berkeley). Sin embargo, nunca se reemplaza en el flujo de datos.

Con SO \_ OOBINLINE habilitado, los datos urgentes permanecen en el flujo de datos. Como resultado, el bloque de datos OOB nunca se pierde cuando llega un nuevo segmento TCP que contiene datos urgentes. La marca de datos OOB existente se actualiza a la nueva posición.

> [!Note]  
> Cuando se establece la opción de socket SO \_ OOBINLINE, SIOCATMARK IOCTL siempre devuelve **TRUE** y los datos de OOB se devuelven al usuario como datos normales.

 

 

 



