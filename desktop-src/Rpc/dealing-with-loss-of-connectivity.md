---
title: Tratar con la pérdida de conectividad
description: Tratar con la pérdida de conectividad
ms.assetid: a90fcb5a-773e-4c21-bf6c-c3519ec13a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eac02c4440cb2e31a29e810d78dfd51764be3ba0ed5a6dc32f8c3e10824bd70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101685"
---
# <a name="dealing-with-loss-of-connectivity"></a>Tratar con la pérdida de conectividad

Una vez completada una llamada RPC, la conexión no se cierra; se marca como gratis. Por lo tanto, el servidor puede bajar o la conectividad de red se puede perder durante o entre llamadas, mientras una conexión está en el grupo. Como cuestión de directiva, el tiempo de ejecución de RPC vuelve a intentar esas llamadas solo si se cumplen las dos condiciones siguientes:

-   El servidor no puede ejecutar la llamada o la llamada es idempotente.
-   El cliente puede implementar reintentos de una manera eficaz para el rendimiento.

Los párrafos siguientes amplían y aclaran las dos condiciones.

Una llamada idempotente es una llamada que se puede ejecutar más de una vez en el servidor sin efectos secundarios no deseados. Por ejemplo, tener una llamada RPC que consulta el saldo del banco para una cuenta determinada es idempotente. Si esta llamada se ejecuta dos veces debido a la pérdida de conectividad, no se realiza ningún daño. Otro ejemplo de una llamada idempotente es cambiar la dirección de un cliente en una base de datos. La ejecución dos veces es correcta, ya que la segunda ejecución simplemente reemplaza la dirección ya actual por la misma dirección. Una operación como "restar cincuenta dólares de la cuenta xyz" no es idempotente. La pérdida de conectividad de red no debería dar lugar a varias ejecuciones de dicha llamada.

Para que sea seguro, el tiempo de ejecución de RPC trata todas las llamadas como no idempotentes. El \[ atributo idempotente \] no se admite para [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp)y se omite. Por lo tanto, la primera condición de la lista anterior se reduce *al servidor que posiblemente no pueda ejecutar la llamada a*.

En muchos casos, el tiempo de ejecución de RPC no puede determinar de forma concluyente que la llamada aún no se ejecutó en el servidor. En tales casos, el cliente no volverá a intentar ejecutar la llamada.

En los ejemplos siguientes se muestra cuándo el tiempo de ejecución de RPC realiza o no vuelve a intentar una llamada:

-   Se reinicia un servidor.

    Se realiza una llamada RPC sencilla sin seguridad en una interfaz en la que no se ha realizado ninguna llamada anterior después del reinicio. Puesto que no se realizó ninguna llamada en esta interfaz, el tiempo de ejecución rpc intenta primero negociar el uso de la interfaz. Envía un paquete mediante una conexión en el grupo. Puesto que el servidor se ha reiniciado y la conexión ya no es válida, devuelve un error. Dado que el tiempo de ejecución rpc del lado cliente aún no ha empezado a enviar los datos de la llamada real, el cliente determina que el servidor no podría haber ejecutado posiblemente en esos datos. Por lo tanto, cierra la conexión y busca otra conexión en el grupo. Si no encuentra una conexión, abre una nueva conexión e intenta negociar de nuevo el uso de la interfaz. Si esto se realiza correctamente, se realiza la llamada (es decir, se realiza un reintento, porque el error se detectó antes de que se iniciara la llamada).

-   Se realiza una llamada RPC con seguridad de nivel de privacidad (cifrado) en una conexión con un contexto de seguridad ya negociado.

    Para garantizar un rendimiento eficaz, el tiempo de ejecución de RPC cifra el paquete serializado en línea (sobre los datos de texto no cifrado). Si se produce un error en el intento de enviar los datos, el tiempo de ejecución rpc no puede volver a intentar la llamada, ya que los datos de texto no cifrado se han sobrescrito con los datos cifrados y no puede volver a cifrar los datos con un nuevo contexto de seguridad. Por lo tanto, no se realiza ningún reintento.

-   Se produce un error en el envío de un fragmento que no es el primero.

    No se realiza el reintento, ya que el tiempo de ejecución de RPC puede optar por descartar el contenido del primer fragmento una vez completado y no tiene ninguna manera de volver a intentar enviar el primer fragmento.

-   Se envía la solicitud RPC.

    El servidor anula la conexión. No se intenta realizar ningún reintento, ya que RPC no puede distinguir si el servidor recibió la llamada y comenzó a ejecutarla.

Si el servidor usa un punto de conexión dinámico, RPC no volverá a resolver el punto de conexión durante los reintentos. Esto significa que si un servidor se vuelve a cerrar y se vuelve a intentar, puede residir en un punto de conexión diferente y RPC no volverá a resolver el punto de conexión de forma transparente cuando se vuelva a intentar una llamada. Para forzar la re resolución del punto de conexión, el cliente RPC debe llamar a [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) antes de volver a realizar una llamada.

En muchos de estos casos, si un cliente RPC puede determinar si una llamada es idempotente o si mantiene los datos que RPC descarta, puede optar por crear un mecanismo de reintento sobre RPC.

> [!Note]  
> Si el servidor es un clúster y los distintos nodos del clúster ejecutan versiones diferentes del software del servidor, un reintento RPC puede realizar la llamada en un nodo diferente del clúster en caso de conmutación por error y, potencialmente, en una versión diferente del servidor. En estos escenarios de implementación, asegúrese de que el cliente no se base en una versión determinada del software del servidor para ejecutar una llamada determinada. Si es así, el cliente debe crear un mecanismo sobre RPC que detecte y controle dichas condiciones.

 

 

 