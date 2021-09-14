---
description: Habilita la escalabilidad del puerto local para un socket.
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: SO_PORT_SCALABILITY (Ws2def.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565caeb472ac5cb15061d32b47a048a9a210885e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170534"
---
# <a name="so_port_scalability"></a>ESCALABILIDAD \_ DE \_ PUERTOS SO

La opción de socket **\_ SO PORT \_ SCALABILITY** permite la escalabilidad del puerto local para un socket.

<dl> <dt>

<span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**ESCALABILIDAD \_ DE \_ PUERTOS SO**
</dt> <dd> <dl> <dt>

0x3006
</dt> <dt>



La opción de socket **SO \_ PORT \_ SCALABILITY** permite la escalabilidad del puerto local al permitir que la asignación de puertos se maximice mediante la asignación de puertos comodín varias veces para diferentes pares de puertos de dirección local en un equipo local.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Nota: En las plataformas en las que se admiten SO PORT SCALABILITY y SO REUSE UNICASTPORT, se prefiere usar \_ \_ SO REUSE \_ \_ \_ \_ UNICASTPORT.

Los entornos de servidor proxy tienen problemas de escalabilidad debido a la disponibilidad limitada del puerto local. Una manera de evitarlo es agregar más direcciones IP a la máquina. Sin embargo, de forma predeterminada, los puertos comodín usados con la función [**de**](/windows/desktop/api/winsock/nf-winsock-bind) enlace se limitan al tamaño del intervalo de puertos dinámicos en la máquina local (hasta 64 000 puertos, pero normalmente menos) independientemente del número de direcciones IP de la máquina local. Para evitarlo, la aplicación debe mantener su propio grupo de puertos con reserva de puertos o mediante heurística.

Para evitar que todas las aplicaciones que requieren escalabilidad administren su propio grupo de puertos y permitir una mayor escalabilidad al tiempo que se mantiene la compatibilidad de la aplicación, Windows Server 2008 introdujo la opción de socket **SO \_ PORT \_ SCALABILITY** para ayudar a maximizar la asignación de puertos comodín. La asignación de puertos se maximiza al permitir que una aplicación asigne puertos comodín para cada par de puertos y direcciones locales únicos. Por lo tanto, si una máquina local tiene cuatro direcciones IP, las solicitudes de función de enlace comodín pueden [](/windows/desktop/api/winsock/nf-winsock-bind) asignar hasta 256 K puertos comodín (64 K puertos × 4 direcciones IP).

Cuando se establece la opción de socket SO PORT [](/windows/desktop/api/winsock/nf-winsock-bind) **\_ \_ SCALABILITY** en un socket y se realiza  una llamada a la función de enlace para una dirección y un puerto comodín especificados (el parámetro name se establece con una dirección específica y un puerto de 0), Winsock asignará un puerto para la dirección especificada. Esta asignación se basará en todas las direcciones IP y puertos posibles/por dirección en el equipo local. Si se adquiere un puerto comodín mediante la opción **SO \_ PORT \_ SCALABILITY,** ese puerto no se puede asignar mediante otro socket sin la opción **SO PORT \_ \_ SCALABILITY.** Esta restricción se ha puesto en marcha para evitar problemas de compatibilidad con versiones anteriores con aplicaciones que asumen que no se puede reutilizar un puerto local con caracteres comodín. Tenga en cuenta que esto significa que las aplicaciones que adquieren un gran número de puertos mediante **SO \_ PORT \_ SCALABILITY** pueden tener aplicaciones heredadas de puertos. Si se han adquirido todos los puertos efímeros disponibles para al menos una dirección con **SO \_ PORT \_ SCALABILITY** , no se pueden realizar más asignaciones de puertos comodín sin la opción de socket.

Para tener cualquier efecto, se debe **establecer la opción SO PORT \_ \_ SCALABILITY** antes de llamar [**a**](/windows/desktop/api/winsock/nf-winsock-bind) la función de enlace. A continuación se describe un ejemplo de cómo se usaría en un equipo con dos direcciones:

-   Un [**proceso**](/windows/desktop/api/Winsock2/nf-winsock2-socket) llama a la función de socket para crear un socket.
-   Se [**llama a la función setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para habilitar la opción de socket SO PORT **\_ \_ SCALABILITY** en el socket recién creado.
-   Se [**llama a**](/windows/desktop/api/winsock/nf-winsock-bind) la función bind para realizar un enlace en una de las direcciones IP y el puerto 0 del equipo local.
-   A [**continuación,**](/windows/desktop/api/Winsock2/nf-winsock2-connect) se llama a la función connect para conectarse a una dirección IP remota. La aplicación usa el socket según sea necesario.
-   El [**mismo**](/windows/desktop/api/Winsock2/nf-winsock2-socket) proceso llama a una función de socket (posiblemente un subproceso diferente) para crear un segundo socket.
-   Se [**llama a la función setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para habilitar la opción de socket SO PORT **\_ \_ SCALABILITY** en el segundo socket recién creado.
-   Se [**llama a**](/windows/desktop/api/winsock/nf-winsock-bind) la función de enlace con la segunda dirección IP y el puerto 0 del equipo local. Incluso cuando se han asignado previamente todos los puertos, esta llamada se realiza correctamente porque hay varias direcciones IP disponibles en el equipo local y la opción de socket **SO \_ PORT \_ SCALABILITY** se estableció en ambos sockets en el mismo proceso.
-   A [**continuación,**](/windows/desktop/api/Winsock2/nf-winsock2-connect) se llama a la función connect para conectarse a una dirección IP remota. La aplicación usa el segundo socket según sea necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Ws2def.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**Opciones de socket DE SOL \_**](sol-socket-socket-options.md)
</dt> <dt>

[**Opciones de socket**](socket-options.md)
</dt> </dl>

 

 




