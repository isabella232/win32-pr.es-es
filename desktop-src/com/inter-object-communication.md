---
title: Comunicación Inter-Object
description: COM está diseñado para permitir que los clientes se comuniquen de forma transparente con objetos de, independientemente de dónde se ejecuten en el mismo proceso, en el mismo equipo o en un equipo diferente.
ms.assetid: dd4adafb-a7e4-44ba-ae4a-80585875ecb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9356ba2bcb9dd3a6a56ac16c354f3abcb752d717
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149646"
---
# <a name="inter-object-communication"></a>Comunicación Inter-Object

COM está diseñado para permitir que los clientes se comuniquen de forma transparente con objetos de, independientemente de dónde se runningÂ esos objetos en el mismo proceso, en el mismo equipo o en un equipo diferente. Esto proporciona un modelo de programación único para todos los tipos de objetos y para los clientes de objetos y los servidores de objetos.

Desde el punto de vista de un cliente, se tiene acceso a todos los objetos a través de punteros de interfaz. Un puntero debe estar en proceso. De hecho, cualquier llamada a una función de interfaz siempre llega a parte del código en proceso en primer lugar. Si el objeto está en proceso, la llamada lo alcanza directamente, sin código de infraestructura del sistema intermedio. Si el objeto está fuera de proceso, la llamada primero alcanza lo que se denomina un objeto "proxy" proporcionado por COM o por el objeto (si el implementador lo desea). Los paquetes de proxy llaman a los parámetros (incluidos los punteros de interfaz) y generan la llamada a procedimiento remoto adecuada (u otro mecanismo de comunicación en el caso de los proxies generados de forma personalizada) en el otro proceso o en el otro equipo en el que se encuentra la implementación del objeto. Este proceso de empaquetado de punteros para la transmisión a través de los límites del proceso se denomina *serialización*.

Desde el punto de vista de un servidor, todas las llamadas a las funciones de interfaz de un objeto se realizan a través de un puntero a esa interfaz. De nuevo, un puntero solo tiene contexto en un único proceso, y el llamador siempre debe ser parte del código en proceso. Si el objeto está en proceso, el llamador es el propio cliente. De lo contrario, el llamador es un objeto "stub" proporcionado por COM o por el propio objeto. El código auxiliar recibe la llamada a procedimiento remoto (u otro mecanismo de comunicación en el caso de los proxies generados de forma personalizada) del "proxy" en el proceso del cliente, anula las referencias de los parámetros y llama a la interfaz adecuada en el objeto de servidor. Desde los puntos de vista de los clientes y servidores, siempre se comunican directamente con otro código en proceso.

COM proporciona una implementación de serialización, denominada *serialización estándar*. Esta implementación funciona muy bien para la mayoría de los objetos y reduce en gran medida los requisitos de programación, lo que hace que el proceso de cálculo de referencias sea transparente eficazmente.

Sin embargo, la separación clara de la interfaz de la implementación de la transparencia del proceso de COM puede obtenerse en algunas situaciones. En ocasiones, el diseño de una interfaz que se centra en su función desde el punto de vista del cliente puede dar lugar a decisiones de diseño que entran en conflicto con la implementación eficaz de la interfaz a través de una red. En casos como este, lo que se necesita no es una transparencia de proceso pura, sino "transparencia del proceso, a menos que tenga que preocuparse". COM proporciona esta funcionalidad, ya que permite que un implementador de objeto admita el *cálculo de referencias personalizado* (también denominado deserialización de [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) ). La serialización estándar es, de hecho, una instancia de cálculo de referencias personalizado; es la implementación predeterminada que se usa cuando un objeto no requiere cálculo de referencias personalizado.

Puede implementar el cálculo de referencias personalizado para permitir que un objeto tome acciones diferentes cuando se usa desde una red que toma en el acceso local y es completamente transparente para el cliente. Esta arquitectura permite diseñar interfaces de cliente/objeto sin tener en cuenta los problemas de rendimiento de la red y, posteriormente, tratar los problemas de rendimiento de la red sin interrumpir el diseño establecido.

COM no especifica cómo se estructuran los componentes; Especifica cómo interactúan. COM deja el interés de la estructura interna de un componente en lenguajes de programación y entornos de desarrollo. Por el contrario, los entornos de programación no tienen ningún estándar establecido para trabajar con objetos fuera de la aplicación inmediata. Microsoft Visual C++, por ejemplo, funciona muy bien para manipular objetos dentro de una aplicación, pero no tiene compatibilidad para trabajar con objetos fuera de la aplicación. Por lo general, el resto de lenguajes de programación son los mismos en este sentido. Por lo tanto, para proporcionar interoperabilidad de networkwide, COM, a través de interfaces independientes del lenguaje, recoge dónde salen los lenguajes de programación.

El doble direccionamiento indirecto de la estructura VTBL significa que los punteros de la tabla de punteros de función no necesitan apuntar directamente a la implementación real en el objeto real. Este es el corazón de la transparencia del proceso.

En el caso de los servidores en proceso, donde el objeto se carga directamente en el proceso del cliente, los punteros de función de la tabla apuntan directamente a la implementación real. En este caso, una llamada de función desde el cliente a un método de interfaz transfiere directamente el control de ejecución al método. Sin embargo, esto no se puede usar para los objetos locales, los que son independientes, ya que los punteros a la memoria no se pueden compartir entre los procesos. Sin embargo, el cliente debe poder llamar a los métodos de interfaz como si estuviera llamando a la implementación real. Por lo tanto, el cliente transfiere uniformemente el control a un método de algún objeto mediante la realización de la llamada.

Un cliente siempre llama a los métodos de interfaz en algún objeto en proceso. Si el objeto real es local o remoto, la llamada se realiza a un objeto proxy, que luego realiza una llamada a procedimiento remoto al objeto real.

¿Qué método se ejecuta realmente? La respuesta es que, cada vez que haya una llamada a una interfaz fuera de proceso, cada método de interfaz se implementa mediante un objeto proxy. El objeto proxy es siempre un objeto en proceso que actúa en nombre del objeto al que se está llamando. Este objeto proxy sabe que el objeto real se está ejecutando en un servidor local o remoto.

El objeto proxy empaqueta los parámetros de función en algunos paquetes de datos y genera una llamada RPC al objeto local o remoto. Un objeto stub selecciona dicho paquete en el proceso del servidor en el equipo local o remoto, que desempaqueta los parámetros y realiza la llamada a la implementación real del método. Cuando la función devuelve, el código auxiliar empaqueta cualquier parámetro out y el valor devuelto y lo envía de vuelta al proxy, que los desempaqueta y los devuelve al cliente original.

Por lo tanto, el cliente y el servidor siempre se comunican entre sí como si todo estuviera en proceso. Todas las llamadas del cliente y todas las llamadas al servidor son, en algún momento, en proceso. Sin embargo, dado que la estructura VTBL permite que algún agente, como COM, intercepte todas las llamadas de función y todas las devoluciones de las funciones, ese agente puede redirigir dichas llamadas a una llamada RPC según sea necesario. Aunque las llamadas en proceso son más rápidas que las llamadas fuera de proceso, las diferencias de proceso son completamente transparentes para el cliente y el servidor.

Para obtener más información, vea los temas siguientes:

-   [Detalles de serialización](marshaling-details.md)
-   [Proxy](proxy.md)
-   [Stub](stub.md)
-   [Canal](channel.md)
-   [Microsoft RPC](microsoft-rpc.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clientes y servidores COM](com-clients-and-servers.md)
</dt> <dt>

[Serialización de interfaces](interface-marshaling.md)
</dt> </dl>

 

 