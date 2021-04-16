---
title: Administrar la duración de los objetos mediante el recuento de referencias
description: Administrar la duración de los objetos mediante el recuento de referencias
ms.assetid: 7f9da5a9-0435-431c-8f90-56e2e489c431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aac184baea9198721e6cdf9c0444a8c6431db08
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "105656319"
---
# <a name="managing-object-lifetimes-through-reference-counting"></a>Administrar la duración de los objetos mediante el recuento de referencias

En los sistemas de objetos tradicionales, el ciclo de vida de los objetos (es decir, los problemas relacionados con la creación y la eliminación de objetos) se controla implícitamente mediante el lenguaje (o el tiempo de ejecución del lenguaje) o explícitamente por los programadores de aplicaciones.

En un sistema que se desarrolla de forma descentralizada y que se compone de componentes reutilizados, ya no es cierto que cualquier cliente, o incluso cualquier programador, siempre "sabe" cómo tratar la duración de un componente. Para un cliente con los privilegios de seguridad correctos, sigue siendo relativamente fácil crear objetos a través de una solicitud simple, pero la eliminación de objetos es otra cuestión por completo. No es necesariamente evidente cuando un objeto ya no se necesita y se debe eliminar. (Los lectores familiarizados con los entornos de programación de recolección de elementos no utilizados, como Java, pueden estar en modo de desacuerdo; sin embargo, los objetos de Java no abarcan los límites del equipo ni siquiera los procesan, por lo que la recolección de elementos no utilizados está restringida a los objetos que viven dentro de un espacio de Además, Java fuerza el uso de un lenguaje de programación único). Incluso cuando el cliente original se realiza con el objeto, no puede simplemente apagar el objeto, ya que otros clientes o clientes todavía pueden tener una referencia a él.

Una manera de asegurarse de que un objeto ya no se necesita es depender por completo de un canal de comunicación subyacente para informar al sistema cuando todas las conexiones a un objeto entre procesos o entre canales han desaparecido. Sin embargo, los esquemas que utilizan este método son inaceptables por varias razones. Un problema es que podría requerir una diferencia importante entre el modelo de programación entre procesos y entre redes y el modelo de programación de un solo proceso. En el modelo de programación entre procesos y redes, el sistema de comunicación proporcionaría los enlaces necesarios para la administración de la duración de los objetos, mientras que en el modelo de programación de un solo proceso, los objetos se conectan directamente sin ningún canal de comunicaciones que intervenga. Otro problema es que este esquema también podría dar lugar a una capa de software proporcionado por el sistema que interferiría con el rendimiento de los componentes en el caso en proceso. Además, un mecanismo basado en la supervisión explícita no tiende a escalar hacia muchos miles o millones de objetos.

COM ofrece un enfoque escalable y distribuido a este conjunto de problemas. Los clientes indican a un objeto Cuándo lo están usando y cuándo lo hacen, y los objetos se eliminan cuando ya no son necesarios. Este enfoque tiene en cuenta que todos los objetos cuentan las referencias a ellos mismos. Los lenguajes de programación, como Java, que, de forma inherente, tienen sus propios esquemas de administración de la duración, como la recolección de elementos no utilizados, pueden usar el recuento de referencias de COM para implementar y usar objetos COM internamente, lo que permite al programador evitar trabajar con él.

Del mismo modo que una aplicación debe liberar la memoria que se ha asignado una vez que esa memoria ya no se utiliza, un cliente de un objeto es responsable de liberar sus referencias al objeto cuando ese objeto ya no se necesita. En un sistema orientado a objetos, el cliente solo puede hacer esto si asigna al objeto una instrucción para que se libere.

Es importante desasignar un objeto cuando ya no se usa. La dificultad radica en determinar cuándo es adecuado desasignar un objeto. Esto es fácil con las variables automáticas (las asignadas en la pila): no se pueden usar fuera del bloque en el que se declaran, por lo que el compilador las desasigna cuando se alcanza el final del bloque. En el caso de los objetos COM, que se asignan dinámicamente, depende de los clientes de un objeto decidir si ya no necesitan usar el objeto, especialmente los objetos locales o remotos que pueden estar usando varios clientes al mismo tiempo. El objeto debe esperar hasta que todos los clientes finalicen con él antes de liberarse. Dado que los objetos COM se manipulan a través de punteros de interfaz y pueden ser utilizados por objetos en procesos diferentes o en otros equipos, el sistema no puede realizar un seguimiento de los clientes de un objeto.

El método de COM para determinar cuándo es adecuado desasignar un objeto es el recuento de referencias manual. Cada objeto mantiene un recuento de referencias que realiza un seguimiento del número de clientes que están conectados a él; es decir, el número de punteros a cualquiera de sus interfaces en cualquier cliente.

Para obtener más información, vea los temas siguientes:

-   [Implementación del recuento de referencias](implementing-reference-counting.md)
-   [Reglas para administrar recuentos de referencias](rules-for-managing-reference-counts.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar e implementar IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




