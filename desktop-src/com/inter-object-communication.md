---
title: Inter-Object comunicación
description: COM está diseñado para permitir que los clientes se comuniquen de forma transparente con objetos, independientemente de dónde se ejecuten esos objetos en el mismo proceso, en el mismo equipo o en un equipo diferente.
ms.assetid: dd4adafb-a7e4-44ba-ae4a-80585875ecb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9356ba2bcb9dd3a6a56ac16c354f3abcb752d717
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060903"
---
# <a name="inter-object-communication"></a>Inter-Object comunicación

COM está diseñado para permitir que los clientes se comuniquen de forma transparente con objetos, independientemente de dónde se ejecuten esos objetos en el mismo proceso, en el mismo equipo o en otro equipo. Esto proporciona un modelo de programación único para todos los tipos de objetos y para clientes de objetos y servidores de objetos.

Desde el punto de vista de un cliente, se accede a todos los objetos a través de punteros de interfaz. Un puntero debe estar en proceso. De hecho, cualquier llamada a una función de interfaz siempre llega primero a algún fragmento de código en proceso. Si el objeto está en proceso, la llamada lo alcanza directamente, sin código de infraestructura del sistema que intervena. Si el objeto está fuera de proceso, la llamada alcanza primero lo que se denomina un objeto "proxy" proporcionado por COM o por el objeto (si el implementador lo desea). Los paquetes de proxy llaman a parámetros (incluidos los punteros de interfaz) y generan la llamada a procedimiento remoto adecuada (u otro mecanismo de comunicación en el caso de servidores proxy generados personalizados) al otro proceso o al otro equipo donde se encuentra la implementación del objeto. Este proceso de empaquetado de punteros para la transmisión a través de los límites del proceso se denomina *serialización*.

Desde el punto de vista de un servidor, todas las llamadas a las funciones de interfaz de un objeto se realizan a través de un puntero a esa interfaz. De nuevo, un puntero solo tiene contexto en un único proceso y el autor de la llamada siempre debe ser parte del código en proceso. Si el objeto está en proceso, el autor de la llamada es el propio cliente. De lo contrario, el autor de la llamada es un objeto "stub" proporcionado por COM o por el propio objeto. El código auxiliar recibe la llamada a procedimiento remoto (u otro mecanismo de comunicación en el caso de servidores proxy generados personalizados) desde el "proxy" en el proceso de cliente, desmarshals los parámetros y llama a la interfaz adecuada en el objeto de servidor. Desde los puntos de vista de los clientes y servidores, siempre se comunican directamente con algún otro código en proceso.

COM proporciona una implementación de serialización, denominada *serialización estándar.* Esta implementación funciona muy bien para la mayoría de los objetos y reduce considerablemente los requisitos de programación, lo que hace que el proceso de serialización sea transparente de forma eficaz.

Sin embargo, la separación clara de la interfaz de la implementación de la transparencia del proceso de COM puede interpelarse en algunas situaciones. El diseño de una interfaz que se centra en su función desde el punto de vista del cliente a veces puede dar lugar a decisiones de diseño que entren en conflicto con la implementación eficaz de esa interfaz a través de una red. En casos como este, lo que se necesita no es transparencia pura del proceso, sino "transparencia de procesos, a menos que sea necesario tener cuidado". COM proporciona esta funcionalidad al permitir que un implementador de objetos admita la serialización personalizada *(también* denominada serialización [**IMarshal).**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) La serialización estándar es, de hecho, una instancia de serialización personalizada; es la implementación predeterminada que se usa cuando un objeto no requiere serialización personalizada.

Puede implementar la serialización personalizada para permitir que un objeto lleve a cabo acciones diferentes cuando se usa desde a través de una red de la que toma en el acceso local y es completamente transparente para el cliente. Esta arquitectura permite diseñar interfaces de cliente/objeto sin tener en cuenta los problemas de rendimiento de red y, posteriormente, solucionar los problemas de rendimiento de red sin interrumpir el diseño establecido.

COM no especifica cómo se estructuran los componentes; especifica cómo interactúan. COM deja la preocupación sobre la estructura interna de un componente a los lenguajes de programación y los entornos de desarrollo. Por el contrario, los entornos de programación no tienen ningún estándar establecido para trabajar con objetos fuera de la aplicación inmediata. Microsoft Visual C++, por ejemplo, funciona muy bien para manipular objetos dentro de una aplicación, pero no tiene compatibilidad para trabajar con objetos fuera de la aplicación. Por lo general, todos los demás lenguajes de programación son los mismos en este sentido. Por lo tanto, para proporcionar interoperabilidad en toda la red, COM, a través de interfaces independientes del lenguaje, recoge dónde dejan de estar los lenguajes de programación.

El direccionamiento indirecto doble de la estructura vtbl significa que los punteros de la tabla de punteros de función no necesitan apuntar directamente a la implementación real en el objeto real. Este es el núcleo de la transparencia del proceso.

Para los servidores en proceso, donde el objeto se carga directamente en el proceso de cliente, los punteros de función de la tabla apuntan directamente a la implementación real. En este caso, una llamada de función desde el cliente a un método de interfaz transfiere directamente el control de ejecución al método . Sin embargo, esto no puede funcionar para objetos locales, y mucho menos remotos, porque los punteros a la memoria no se pueden compartir entre procesos. No obstante, el cliente debe poder llamar a métodos de interfaz como si llamara a la implementación real. Por lo tanto, el cliente transfiere el control uniformemente a un método en algún objeto realizando la llamada.

Un cliente siempre llama a métodos de interfaz en algún objeto en proceso. Si el objeto real es local o remoto, la llamada se realiza a un objeto proxy, que, a continuación, realiza una llamada de procedimiento remoto al objeto real.

¿Qué método se ejecuta realmente? La respuesta es que cada vez que se llama a una interfaz fuera de proceso, cada método de interfaz se implementa mediante un objeto proxy. El objeto proxy siempre es un objeto en proceso que actúa en nombre del objeto al que se llama. Este objeto proxy sabe que el objeto real se ejecuta en un servidor local o remoto.

El objeto de proxy empaqueta los parámetros de función en algunos paquetes de datos y genera una llamada RPC al objeto local o remoto. Ese paquete lo recoge un objeto de código auxiliar en el proceso del servidor en el equipo local o remoto, que desempaquete los parámetros y realiza la llamada a la implementación real del método. Cuando esa función devuelve un resultado, el código auxiliar empaqueta los parámetros de salida y el valor devuelto y los envía de vuelta al proxy, que los desempaquete y los devuelve al cliente original.

Por lo tanto, el cliente y el servidor siempre se hablan entre sí como si todo fuera en proceso. Todas las llamadas del cliente y todas las llamadas al servidor están, en algún momento, en proceso. Pero como la estructura vtbl permite a algún agente, como COM, interceptar todas las llamadas de función y todas las devoluciones de funciones, ese agente puede redirigir esas llamadas a una llamada RPC según sea necesario. Aunque las llamadas en proceso son más rápidas que las llamadas fuera de proceso, las diferencias de proceso son completamente transparentes para el cliente y el servidor.

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

 

 