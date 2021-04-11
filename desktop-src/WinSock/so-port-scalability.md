---
description: Habilita la escalabilidad del puerto local para un socket.
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: SO_PORT_SCALABILITY (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565caeb472ac5cb15061d32b47a048a9a210885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154247"
---
# <a name="so_port_scalability"></a>\_ \_ escalabilidad de puertos

La opción de socket de **\_ \_ escalabilidad de puertos** permite habilitar la escalabilidad del puerto local para un socket.

<dl> <dt>

<span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**\_ \_ escalabilidad de puertos**
</dt> <dd> <dl> <dt>

0x3006
</dt> <dt>



La opción de socket de **\_ \_ escalabilidad de puertos** permite maximizar la escalabilidad del puerto local al permitir que la asignación de puertos se maximice asignando puertos comodín varias veces para distintos pares de puertos de direcciones locales en un equipo local.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Nota: en plataformas en las que \_ \_ se admiten tanto la escalabilidad de puertos como la \_ reutilización de \_ UNICASTPORT, es preferible usar \_ \_ UNICASTPORT.

Los entornos de servidor proxy tienen problemas de escalabilidad debido a la disponibilidad limitada del puerto local. Una manera de solucionar esto es agregar más direcciones IP a la máquina. Sin embargo, de forma predeterminada, los puertos comodín usados con la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) se limitan al tamaño del intervalo de puertos dinámicos en el equipo local (hasta 64 000 puertos, pero normalmente menos) independientemente del número de direcciones IP en el equipo local. Para evitar esto, es necesario que la aplicación mantenga su propio grupo de puertos con la reserva de puertos o mediante la heurística.

Para evitar que todas las aplicaciones que requieran escalabilidad administren su propio grupo de puertos y para permitir una mayor escalabilidad, al mismo tiempo que se mantiene la compatibilidad de las aplicaciones, Windows Server 2008 presentó la opción de socket de **\_ \_ escalabilidad de puertos** para ayudar a maximizar la asignación de puertos comodín. La asignación de puertos se maximiza permitiendo que una aplicación asigne puertos comodín para cada par de puerto y dirección local únicos. Por tanto, si un equipo local tiene cuatro direcciones IP, se pueden asignar hasta 256 K puertos comodín (64 K puertos x 4 direcciones IP) mediante solicitudes de función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) comodín.

Cuando se establece la opción de socket de **\_ \_ escalabilidad de puertos** en un socket y se realiza una llamada a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) para una dirección y un puerto comodín especificados (el parámetro *Name* se establece con una dirección específica y un puerto 0), Winsock asignará un puerto para la dirección especificada. Esta asignación se basará en todas las direcciones IP y puertos posibles y por dirección en el equipo local. Si se adquiere un puerto comodín con la opción de **\_ \_ escalabilidad de puertos** , ese puerto no se puede asignar a otro socket sin la opción de **\_ \_ escalabilidad de puertos** . Esta restricción se aplica para evitar los problemas de compatibilidad con versiones anteriores de las aplicaciones que suponen que no se puede volver a usar un puerto local comodín. Tenga en cuenta que esto significa que las aplicaciones que adquieren un gran número de puertos mediante la **\_ \_ escalabilidad del puerto** pueden privar a las aplicaciones heredadas de los puertos. Si se han adquirido todos los puertos efímeros disponibles para al menos una dirección con la **\_ \_ escalabilidad de puertos** , no se pueden realizar más asignaciones de Puerto comodín sin la opción de socket.

Para que surta efecto, se debe establecer la opción de **\_ \_ escalabilidad de puertos para que** se llame a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) . A continuación se muestra un ejemplo de cómo se utilizaría en un equipo con dos direcciones:

-   Un proceso llama a la función de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) para crear un socket.
-   Se llama a la función de llamada para [**Habilitar la opción**](/windows/desktop/api/winsock/nf-winsock-setsockopt) de socket de **\_ \_ escalabilidad de puertos** para el socket recién creado.
-   Se llama a la función [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) para realizar un enlace en una de las direcciones IP del equipo local y en el puerto 0.
-   A continuación, se llama a la función [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) para conectarse a una dirección IP remota. La aplicación usa el socket según sea necesario.
-   Una función de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) se llama mediante el mismo proceso (posiblemente un subproceso diferente) para crear un segundo Socket.
-   Se llama a la función de llamada para [**Habilitar la opción**](/windows/desktop/api/winsock/nf-winsock-setsockopt) de socket de **\_ \_ escalabilidad de puertos** para el segundo socket recién creado.
-   Se llama a la función [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) con la segunda dirección IP y el puerto 0 del equipo local. Incluso cuando todos los puertos se han asignado previamente, esta llamada se realiza correctamente porque hay varias direcciones IP disponibles en el equipo local y la opción de socket de **\_ \_ escalabilidad de puertos para que** se haya establecido en ambos Sockets en el mismo proceso.
-   A continuación, se llama a la función [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) para conectarse a una dirección IP remota. La aplicación usa el segundo socket según sea necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Ws2def. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**\_Opciones de socket de socket sol**](sol-socket-socket-options.md)
</dt> <dt>

[**Opciones de socket**](socket-options.md)
</dt> </dl>

 

 




