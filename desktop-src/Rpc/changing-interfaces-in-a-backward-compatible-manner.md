---
title: Cambiar las interfaces de una manera compatible con versiones anteriores
description: Los métodos que se explican en la teoría de control de versiones de RPC y COM pueden ser inaceptables por muchas razones.
ms.assetid: 7dec4b67-3d50-453f-b0ef-290d091186fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314daecc6b55aaf4a348411010eb578149f86921
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793503"
---
# <a name="changing-interfaces-in-a-backward-compatible-manner"></a>Cambiar las interfaces de una manera compatible con versiones anteriores

Los métodos que se explican en [la teoría de control de versiones de RPC y com](the-versioning-theory-for-rpc-and-com.md) pueden ser inaceptables por muchas razones. El cambio de una versión de interfaz de acuerdo con las reglas requiere básicamente que los nuevos clientes no se comuniquen con los servidores antiguos. Esto suele ser imposible con el software comercial implementado en el campo. A veces, Windows ha introducido cambios en la interfaz ausentes de las versiones o los GUID modificados. Esto fue el resultado de la necesidad de que los nuevos clientes se comuniquen con los servidores heredados, y porque la solución que el cliente nuevo admitiría era no deseable.

## <a name="best-practice"></a>Procedimiento recomendado

Estos son los métodos razonables para solucionar el problema de incompatibilidad de la conexión cuando no se puede cambiar la versión y el GUID de la interfaz.

1.  Haga que la aplicación tenga en cuenta las capacidades del otro lado.

    El cliente y el servidor tienen un protocolo que permite que cada (o al menos el cliente nuevo) establezca la identidad del socio. Normalmente es suficiente para que el nuevo cliente tenga en cuenta las características compatibles con los servidores antiguos y nuevos. Esto se puede hacer fácilmente cuando una aplicación se mantiene en un contexto de conexión y se admite a través de un tipo *XxxGetInfo* de llamada de función ejecutada por el cliente antes de realizar cualquier operación de RPC. Cuando una aplicación administra las características en una versión por servidor, nunca se puede realizar una llamada a una incompatibilidad con el servidor o cliente anterior, ya que la aplicación controla qué llamadas se emiten a cada servidor. La línea inferior es que la aplicación es proactiva para evitar que se produzca una falta de coincidencia. Esto puede realizarse junto con la segunda práctica.

2.  Introduzca una nueva API remota.

    Un nuevo método remoto no entra en conflicto con los métodos existentes si se agrega al final de la interfaz. Los clientes antiguos pueden llamar a los nuevos servidores como siempre lo tienen. El nuevo cliente puede llamar al nuevo método sin conocer la identidad del servidor, siempre que inspeccione los errores procedentes del servidor al que se está llamando. El tiempo de ejecución de RPC siempre comprueba el número de método de cada interfaz antes de un envío para asegurarse de que el método está dentro de una tabla v adecuada. En el caso de un método desconocido para un servidor, el tiempo de ejecución de RPC produce la excepción RPC \_ S \_ PROCNUM \_ fuera \_ del \_ intervalo. Esta excepción solo se desencadena en esta situación concreta. Por lo tanto, un cliente nuevo puede ver la excepción como un signo de que la llamada pasó a un servidor anterior y puede modificar su comportamiento correctamente.

3.  Introduzca nuevos parámetros o nuevos tipos de datos solo en los nuevos métodos.

    Una razón para introducir un nuevo método es evitar la incompatibilidad de los datos. Si se introduce un nuevo tipo de datos o simplemente se modifica, en principio solo debe usarse en un nuevo método (o métodos). Vea [ejemplos de cambios incompatibles](examples-of-incompatible-changes.md) para ver ejemplos de cambios de tipos de datos incompatibles. La única excepción importante a esta regla se describe en el elemento cuatro.

4.  Asigne nuevos parámetros o nuevos tipos de datos a través de un contenedor.

    Esta solución se aplica cuando un nuevo parámetro o tipo de datos debe exponerse a un usuario, pero realmente no tiene que ser remoto de forma independiente o se puede asignar a los tipos de datos o parámetros antiguos. Por ejemplo, muchas API del sistema se activan y ejecutan una llamada remota. Pueden o no realizar algún tipo de asignación de los tipos de datos conocidos del usuario a los tipos de datos que se usan realmente en la llamada RPC subyacente. Por lo tanto, siempre merece la pena examinar si el cambio en la interfaz de usuario debe propagarse como un cambio en una interfaz remota.

    Se puede producir una situación similar cuando el usuario llama directamente a una API remota, pero se puede introducir un contenedor para realizar una nueva asignación de tipos o algunas otras acciones adicionales que se han hecho necesarias. El lenguaje de definición de interfaz (IDL) tiene varias formas de facilitar la reasignación, \[ [**llamar a \_ como**](/windows/desktop/Midl/call-as) \] , \[ [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) \] y \[ [**calcular las \_ referencias**](/windows/desktop/Midl/wire-marshal) \] . El \[ atributo **Call \_ as** \] introduce un contenedor de funciones en el cliente y en el servidor. Ambos se colocan entre el código de usuario y el serializador. Los demás atributos tratan con la asignación de tipos directos. En el caso de los problemas de extensión, \[ **llamar a \_ como** \] es el que se usa con más frecuencia y es más fácil de entender y manipular sin problemas.

5.  Modifique los tipos de datos a través de una uniónless predeterminada.

    Cambiar un tipo de atributo o de datos normalmente conduce a la incompatibilidad de la conexión. Vea [ejemplos de cambios incompatibles](examples-of-incompatible-changes.md) para obtener ejemplos. Sin embargo, en el caso de una Unión sin una cláusula default, la incompatibilidad se puede administrar de forma similar a como se indica en el caso de un procedimiento fuera del intervalo, tal y como se ha descrito anteriormente. Este esquema es aplicable fácilmente a los tipos de *XxxINFO* populares que usan uniones.

    Por ejemplo, una llamada como esta

    ```C++
    XxxGetInfo( [in] level, [out] XxxINFO  * pInfo );
    ```

    

    podría devolver información en el nivel 1, 2 o 3, donde *XxxINFO* es una unión con tres ramas: 1, 2 y 3.

6.  Use el \[ atributo de [**intervalo**](/windows/desktop/Midl/range) \] para especificar el intervalo.

    Puede especificar el \[ [](/windows/desktop/Midl/range) \] atributo de intervalo en un tipo de escala simple sin interrumpir la compatibilidad con versiones anteriores. Este atributo no afecta al formato de conexión, pero durante la desserialización de RPC comprueba el valor de conexión para confirmar que se encuentra dentro del intervalo especificado en el archivo. idl. Si no es así, \_ \_ \_ se produce una excepción enlazada no válida de RPC X. Esto es especialmente útil si el servidor conoce el tamaño máximo de una matriz de tamaño.

    Por ejemplo:

    ```C++
    HRESULT Method1( [in, range(0,100)] ULONG m, [size_is(m)] ULONG *plong); 
    ```

    

El comportamiento de RPC cuando el nivel indicado es 4 y falta el brazo, depende de la definición de la Unión. En el caso de una unión con la cláusula default definida, RPC transmite un tipo indicado en la cláusula default para cualquier elemento diferente de las etiquetas de ARM conocidas (en este caso, algo distinto de 1, 2 o 3). En el caso de una Unión sin valor predeterminado, el cálculo de referencias genera una excepción porque, por definición, no hay ningún valor predeterminado para revertir a. La excepción es una \_ \_ etiqueta no válida de RPC S \_ .

De nuevo, un nuevo cliente puede ajustar su comportamiento al detectar que llamó a un servidor antiguo.

Lo que se muestra a continuación de estas prácticas recomendadas es que si se debe diseñar un tipo de datos remoto que se pueda extender en el futuro, use una Unión sin valor predeterminado en el archivo IDL. Dada una opción, una Unión encapsulada es ligeramente más limpia.

Debido a las peculiaridades de la representación interna del Protocolo de conexión de NDR64, la recomendación para agregar los brazos que se han proporcionado anteriormente en esta sección debe calificarse de la siguiente manera: el nuevo ARM que se va a agregar no puede cambiar la alineación de la Unión y, en particular, la alineación más grande de los brazos no debe cambiar. Normalmente no es un problema, ya que un puntero en un ARM fuerza la alineación a 8. Un diseño en el que cada ARM es un puntero a un tipo ARM es un método limpio para satisfacer el requisito.

 

 