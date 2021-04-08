---
title: Tratamiento de la pérdida de conectividad
description: Tratamiento de la pérdida de conectividad
ms.assetid: a90fcb5a-773e-4c21-bf6c-c3519ec13a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8e7a8088cfe09a4c4026c16cc3dc5ea36b3430
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792801"
---
# <a name="dealing-with-loss-of-connectivity"></a>Tratamiento de la pérdida de conectividad

Una vez finalizada una llamada RPC, la conexión no está cerrada; está marcado como libre. Como tal, el servidor puede quedar inactivo o se puede perder la conectividad de red durante o entre llamadas, mientras que una conexión se encuentra en el grupo. Como cuestión de la Directiva, el tiempo de ejecución de RPC vuelve a intentar esas llamadas solo si se cumplen las dos condiciones siguientes:

-   Es posible que el servidor no pueda ejecutar la llamada o que la llamada sea idempotente.
-   El cliente puede implementar reintentos de una manera eficaz.

Los párrafos siguientes expanden y aclaran las dos condiciones.

Una llamada idempotente es una llamada que se puede ejecutar más de una vez en el servidor sin efectos secundarios no deseados. Por ejemplo, tener una llamada RPC que consulta el saldo en el Banco para una cuenta determinada es idempotente. Si esta llamada se ejecuta dos veces debido a la pérdida de conectividad, no se produce ningún daño. Otro ejemplo de una llamada idempotente es el cambio de la dirección de un cliente en una base de datos. La ejecución dos veces es correcta, ya que la segunda ejecución reemplaza simplemente la dirección actual con la misma dirección. Una operación como "reste 50 dólares de la cuenta XYZ" no es idempotente. La pérdida de conectividad de red no debe producir varias ejecuciones de este tipo de llamada.

Para que sea segura, el tiempo de ejecución de RPC trata todas las llamadas como no idempotente. El \[ \] atributo idempotente no es compatible con [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp)y se omite. Como tal, la primera condición de la lista anterior se reduce al *servidor que no puede ejecutar la llamada*.

En muchos casos, el tiempo de ejecución de RPC no puede determinar de forma concluyente que la llamada no se ha ejecutado en el servidor. En estos casos, el cliente no volverá a intentar ejecutar la llamada.

En los siguientes ejemplos se muestra Cuándo el tiempo de ejecución de RPC o no vuelve a intentar una llamada:

-   Se reiniciará un servidor.

    Se realiza una llamada RPC sencilla sin seguridad en una interfaz en la que no se ha realizado ninguna llamada anterior después del reinicio. Dado que no se realizó ninguna llamada en esta interfaz, el tiempo de ejecución de RPC intenta negociar primero el uso de la interfaz. Envía un paquete mediante una conexión en el grupo. Desde que se reinició el servidor y la conexión ya no es válida, devuelve un error. Dado que el tiempo de ejecución de RPC del cliente todavía no ha empezado a enviar los datos para la llamada real, el cliente determina que el servidor no pudo haberse ejecutado en esos datos. Por lo tanto, cierra la conexión y busca otra conexión en el grupo. Si no encuentra una conexión, se abre una nueva conexión y se intenta negociar de nuevo el uso de la interfaz. Si esto se realiza correctamente, se realiza la llamada (es decir, se realiza un reintento, porque el error se detectó antes de que se iniciara la llamada).

-   Se realiza una llamada RPC con seguridad de nivel de privacidad (cifrado) en una conexión con un contexto de seguridad ya negociado.

    Para garantizar un rendimiento eficaz, el tiempo de ejecución de RPC cifra el paquete serializado insertado (sobre los datos de texto no cifrado). Si se produce un error al intentar enviar los datos, el tiempo de ejecución de RPC no puede reintentar la llamada, ya que los datos de texto no cifrados se han sobrescrito con los datos cifrados y no pueden volver a cifrar los datos con un nuevo contexto de seguridad. Por lo tanto, no se realiza ningún reintento.

-   Se produce un error en el envío de un fragmento que no es el primero.

    No se realiza el reintento, ya que el tiempo de ejecución de RPC puede optar por descartar el contenido del primer fragmento una vez que se ha completado y no tiene forma de reintentar el envío del primer fragmento.

-   Se envía la solicitud RPC.

    El servidor anula la conexión. No se intenta ningún reintento, ya que RPC no puede discernir si el servidor recibió la llamada y comenzó a ejecutarla.

Si el servidor utiliza un extremo dinámico, RPC no volverá a resolver el punto de conexión durante los reintentos. Esto significa que, si un servidor se apaga y vuelve a aparecer, puede residir en un punto de conexión diferente, y RPC no volverá a resolver de forma transparente el punto de conexión cuando se vuelva a intentar una llamada. Para forzar la nueva resolución del punto de conexión, el cliente RPC debe llamar a [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) antes de Reintentar una llamada.

En muchos de estos casos, si un cliente RPC puede determinar si una llamada es idempotente o si mantiene los datos descartados por RPC, puede optar por crear un mecanismo de reintento en la parte superior de RPC.

> [!Note]  
> Si el servidor es un clúster y los distintos nodos del clúster ejecutan versiones diferentes del software de servidor, un reintento de RPC puede destinar la llamada en un nodo diferente del clúster en caso de conmutación por error y potencialmente en una versión diferente del servidor. En estos escenarios de implementación, asegúrese de que el cliente no se base en una versión concreta del software de servidor para ejecutar una llamada determinada. Si lo hace, el cliente debe crear un mecanismo sobre RPC que detecte y controle dichas condiciones.

 

 

 