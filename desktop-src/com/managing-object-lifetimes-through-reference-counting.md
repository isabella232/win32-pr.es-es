---
title: Administración de duraciones de objetos mediante el recuento de referencias
description: Administración de duraciones de objetos mediante el recuento de referencias
ms.assetid: 7f9da5a9-0435-431c-8f90-56e2e489c431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f2c75352eef5680eb9a4d8367f76f88c19138dd834b71068740bee18f2315
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310565"
---
# <a name="managing-object-lifetimes-through-reference-counting"></a>Administración de duraciones de objetos mediante el recuento de referencias

En los sistemas de objetos tradicionales, el ciclo de vida de los objetos (es decir, los problemas relacionados con la creación y eliminación de objetos) se controla implícitamente por el lenguaje (o el tiempo de ejecución del lenguaje) o explícitamente por los programadores de la aplicación.

En un sistema en constante evolución y construido de forma descentralizada que se comprima con componentes reutilizados, ya no es cierto que ningún cliente, o incluso cualquier programador, siempre "sepa" cómo tratar con la duración de un componente. Para un cliente con los privilegios de seguridad adecuados, todavía es relativamente fácil crear objetos a través de una solicitud simple, pero la eliminación de objetos es otra cuestión por completo. No es necesariamente claro cuando ya no se necesita un objeto y se debe eliminar. (Es posible que los lectores familiarizados con los entornos de programación recopilados por elementos no utilizados, como Java, no estén de acuerdo; sin embargo, los objetos java no abarcan los límites de la máquina o del proceso y, por tanto, la recolección de elementos no utilizados está restringida a los objetos que se encuentran dentro de un espacio de un solo proceso. Además, Java fuerza el uso de un solo lenguaje de programación). Incluso cuando el cliente original se realiza con el objeto , no puede simplemente apagar el objeto, ya que es posible que algún otro cliente o cliente todavía tenga una referencia a él.

Una manera de asegurarse de que un objeto ya no es necesario es depender completamente de un canal de comunicación subyacente para informar al sistema cuando todas las conexiones a un objeto entre procesos o entre canales han desaparecido. Sin embargo, los esquemas que usan este método son inaceptables por varias razones. Un problema es que podría requerir una diferencia importante entre el modelo de programación entre procesos y redes y el modelo de programación de un solo proceso. En el modelo de programación entre procesos y redes, el sistema de comunicación proporcionaría los enlaces necesarios para la administración de la duración de los objetos, mientras que en el modelo de programación de un solo proceso, los objetos se conectan directamente sin ningún canal de comunicaciones que intervengan. Otro problema es que este esquema también podría dar lugar a una capa de software proporcionado por el sistema que interferiría con el rendimiento de los componentes en el caso en proceso. Además, un mecanismo basado en la supervisión explícita no tiende a escalarse hacia muchos miles o millones de objetos.

COM ofrece un enfoque escalable y distribuido para este conjunto de problemas. Los clientes le dicen a un objeto cuándo lo usan y cuándo han terminado, y los objetos se eliminan cuando ya no son necesarios. Este enfoque exige que todos los objetos cuenten referencias a sí mismos. Los lenguajes de programación como Java, que tienen de forma inherente sus propios esquemas de administración de duración, como la recolección de elementos no utilizados, pueden usar el recuento de referencias de COM para implementar y usar objetos COM internamente, lo que permite al programador evitar tratar con ellos.

Al igual que una aplicación debe liberar memoria que ha asignado una vez que esa memoria ya no está en uso, un cliente de un objeto es responsable de liberar sus referencias al objeto cuando ese objeto ya no es necesario. En un sistema orientado a objetos, el cliente solo puede hacerlo si proporciona al objeto una instrucción para liberarse.

Es importante que un objeto se desasigne cuando ya no se esté utilizando. La dificultad radica en determinar cuándo es adecuado desasignar un objeto. Esto es fácil con las variables automáticas (las asignadas en la pila): no se pueden usar fuera del bloque en el que se declaran, por lo que el compilador las desasigna cuando se alcanza el final del bloque. En el caso de los objetos COM, que se asignan dinámicamente, es decisión de los clientes de un objeto decidir cuándo ya no necesitan usar el objeto, especialmente los objetos locales o remotos que pueden estar en uso por varios clientes al mismo tiempo. El objeto debe esperar hasta que todos los clientes terminen con él antes de liberarse. Dado que los objetos COM se manipulan a través de punteros de interfaz y pueden ser utilizados por objetos en procesos diferentes o en otros equipos, el sistema no puede realizar un seguimiento de los clientes de un objeto.

El método de COM para determinar cuándo es adecuado desasignar un objeto es el recuento manual de referencias. Cada objeto mantiene un recuento de referencias que realiza un seguimiento de cuántos clientes están conectados a él, es decir, cuántos punteros existen a cualquiera de sus interfaces en cualquier cliente.

Para obtener más información, vea los temas siguientes:

-   [Implementar el recuento de referencias](implementing-reference-counting.md)
-   [Reglas para administrar recuentos de referencias](rules-for-managing-reference-counts.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso e implementación de IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




