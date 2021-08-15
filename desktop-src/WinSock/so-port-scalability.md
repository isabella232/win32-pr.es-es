---
description: Habilita la escalabilidad del puerto local para un socket.
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: SO_PORT_SCALABILITY (Ws2def.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 925d6337bc5b9d4633117fc1d8e1b8db2657f31b91a9cce602702ceb67e7e92e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993375"
---
# <a name="so_port_scalability"></a>ESCALABILIDAD \_ DE \_ PUERTOS

La opción de socket **\_ SO PORT \_ SCALABILITY** permite la escalabilidad del puerto local para un socket.

<dl> <dt>

<span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**ESCALABILIDAD \_ DE \_ PUERTOS**
</dt> <dd> <dl> <dt>

0x3006
</dt> <dt>



La opción de socket **SO \_ PORT \_ SCALABILITY** permite la escalabilidad del puerto local, ya que permite maximizar la asignación de puertos mediante la asignación de puertos comodín varias veces para diferentes pares de puertos de dirección local en un equipo local.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Nota: En las plataformas en las que se admiten SO PORT SCALABILITY y SO REUSE UNICASTPORT, se prefiere \_ usar SO REUSE \_ \_ \_ \_ \_ UNICASTPORT.

Los entornos de servidor proxy tienen problemas de escalabilidad debido a la disponibilidad limitada del puerto local. Una manera de evitarlo es agregar más direcciones IP a la máquina. Sin embargo, de forma predeterminada, los puertos comodín usados con la función [**de**](/windows/desktop/api/winsock/nf-winsock-bind) enlace se limitan al tamaño del intervalo de puertos dinámicos en la máquina local (hasta 64 000 puertos, pero normalmente menos) independientemente del número de direcciones IP del equipo local. Para evitarlo, la aplicación debe mantener su propio grupo de puertos con reserva de puertos o mediante heurística.

Para evitar que todas las aplicaciones que requieren escalabilidad administren su propio grupo de puertos y para permitir una mayor escalabilidad al tiempo que se mantiene la compatibilidad de la aplicación, Windows Server 2008 introdujo la opción de socket **SO \_ PORT \_ SCALABILITY** para ayudar a maximizar la asignación de puertos comodín. La asignación de puertos se maximiza al permitir que una aplicación asigne puertos comodín para cada par de puertos y direcciones locales únicos. Por lo tanto, si una máquina local tiene cuatro direcciones IP, se pueden asignar hasta 256 K puertos [](/windows/desktop/api/winsock/nf-winsock-bind) comodín (64 K puertos × 4 direcciones IP) mediante solicitudes de función de enlace de caracteres comodín.

Cuando se establece la opción de socket SO PORT [](/windows/desktop/api/winsock/nf-winsock-bind) **\_ \_ SCALABILITY** en un socket y se realiza  una llamada a la función de enlace para una dirección y un puerto comodín especificados (el parámetro name se establece con una dirección específica y un puerto de 0), Winsock asignará un puerto para la dirección especificada. Esta asignación se basará en todas las direcciones IP y puertos posibles/por dirección en el equipo local. Si se adquiere un puerto comodín mediante la opción **SO \_ PORT \_ SCALABILITY,** ese puerto no se puede asignar por otro socket sin la opción **SO PORT \_ \_ SCALABILITY.** Esta restricción se ha puesto en marcha para evitar problemas de compatibilidad con versiones anteriores con aplicaciones que asumen que no se puede reutilizar un puerto local con caracteres comodín. Tenga en cuenta que esto significa que las aplicaciones que adquieren un gran número de puertos mediante **SO \_ PORT \_ SCALABILITY** pueden tener aplicaciones heredadas de puertos. Si se han adquirido todos los puertos efímeros disponibles para al menos una dirección con **SO \_ PORT \_ SCALABILITY** , no se pueden asignar más puertos comodín sin la opción socket.

Para tener cualquier efecto, se debe establecer la **opción SO PORT \_ \_ SCALABILITY** antes de llamar [**a**](/windows/desktop/api/winsock/nf-winsock-bind) la función de enlace. A continuación se describe un ejemplo de cómo se usaría en un equipo con dos direcciones:

-   Un [**proceso**](/windows/desktop/api/Winsock2/nf-winsock2-socket) llama a la función de socket para crear un socket.
-   Se [**llama a la función setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para habilitar la opción de socket SO PORT **\_ \_ SCALABILITY** en el socket recién creado.
-   Se [**llama a**](/windows/desktop/api/winsock/nf-winsock-bind) la función de enlace para realizar un enlace en una de las direcciones IP y el puerto 0 del equipo local.
-   A [**continuación,**](/windows/desktop/api/Winsock2/nf-winsock2-connect) se llama a la función connect para conectarse a una dirección IP remota. La aplicación usa el socket según sea necesario.
-   El [**mismo**](/windows/desktop/api/Winsock2/nf-winsock2-socket) proceso (posiblemente un subproceso diferente) llama a una función de socket para crear un segundo socket.
-   Se [**llama a la función setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para habilitar la opción de socket SO PORT **\_ \_ SCALABILITY** en el segundo socket recién creado.
-   Se [**llama a**](/windows/desktop/api/winsock/nf-winsock-bind) la función de enlace con la segunda dirección IP y el puerto 0 del equipo local. Incluso cuando se han asignado previamente todos los puertos, esta llamada se realiza correctamente porque hay varias direcciones IP disponibles en el equipo local y la opción de socket **SO \_ PORT \_ SCALABILITY** se estableció en ambos sockets en el mismo proceso.
-   A [**continuación,**](/windows/desktop/api/Winsock2/nf-winsock2-connect) se llama a la función connect para conectarse a una dirección IP remota. La aplicación usa el segundo socket según sea necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Ws2def.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**Opciones \_ de socket DE SOL**](sol-socket-socket-options.md)
</dt> <dt>

[**Opciones de socket**](socket-options.md)
</dt> </dl>

 

 




