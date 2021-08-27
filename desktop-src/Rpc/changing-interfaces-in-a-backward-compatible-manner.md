---
title: Cambiar interfaces de una manera compatible con versiones anteriores
description: Los métodos explicados en The Versioning Theory for RPC and COM pueden ser inaceptables por muchas razones.
ms.assetid: 7dec4b67-3d50-453f-b0ef-290d091186fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbe06be3106b4c599baed2d625eefa1f9c7d035c70ef89ac325406bb8c2037d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022965"
---
# <a name="changing-interfaces-in-a-backward-compatible-manner"></a>Cambiar interfaces de una manera compatible con versiones anteriores

Los métodos explicados [en The Versioning Theory for RPC and COM](the-versioning-theory-for-rpc-and-com.md) pueden ser inaceptables por muchas razones. El cambio de una versión de interfaz según las reglas requiere básicamente que los clientes nuevos no se comuniquen con servidores antiguos. Esto suele ser imposible con el software comercial implementado en el campo. A veces, Windows ha introducido cambios en la interfaz que no tienen en cuenta las versiones o GUID modificados. Esto se debe a que los nuevos clientes necesitan comunicarse con servidores heredados y porque la solución que un nuevo cliente admitiría tanto las interfaces antiguas como las nuevas se consideró no deseada.

## <a name="best-practice"></a>Procedimiento recomendado

Estos son los métodos razonables para resolver el problema de incompatibilidad de la conexión cuando no se pueden cambiar el GUID de la interfaz y la versión.

1.  Hacer que la aplicación tenga en cuenta las funcionalidades del otro lado.

    El cliente y el servidor tienen un protocolo que permite a cada uno (o al menos al nuevo cliente) establecer la identidad del asociado. Normalmente, basta con que el nuevo cliente tenga en cuenta las características compatibles con los servidores antiguos y los nuevos. Esto puede hacerse fácilmente cuando una aplicación se mantiene en un contexto de conexión y se admite a través de un tipo *XxxGetInfo* de llamada de función ejecutado por el cliente antes de realizar cualquier operación RPC. Cuando una aplicación administra las características en una versión por servidor, nunca se puede producir una llamada con una incompatibilidad con el servidor o cliente antiguo, ya que la aplicación controla qué llamadas se emiten a cada servidor. La conclusión es que la aplicación es proactiva para evitar que se desajuste. Esto puede realizarse junto con el segundo procedimiento.

2.  Presenta una nueva API remota.

    Un nuevo método remoto no colisiona con los métodos existentes si se agrega al final de la interfaz. Los clientes antiguos pueden llamar a servidores nuevos como siempre lo han hecho. El nuevo cliente puede llamar al nuevo método sin conocer la identidad del servidor, siempre que esté al tanto de los errores procedentes del servidor al que se llama. El tiempo de ejecución de RPC siempre comprueba el número de método de cada interfaz antes de una distribución para asegurarse de que el método se encuentra dentro de una tabla v adecuada. Para un método desconocido para un servidor, el tiempo de ejecución de RPC genera la excepción RPC \_ S \_ PROCNUM \_ OUT OF \_ \_ RANGE. Esta excepción solo se produce en esta situación concreta. Por lo tanto, un nuevo cliente puede observar la excepción como un signo de que la llamada se ha producido en un servidor antiguo y puede modificar su comportamiento correctamente.

3.  Introduzca nuevos parámetros o nuevos tipos de datos solo en los nuevos métodos.

    Una razón para introducir un nuevo método es evitar la incompatibilidad de datos. Si se introduce un nuevo tipo de datos o simplemente se modifica, en principio solo se debe usar en un nuevo método (o métodos). Vea [Ejemplos de cambios incompatibles para](examples-of-incompatible-changes.md) obtener ejemplos de cambios de tipos de datos incompatibles. La única excepción importante a esta regla se describe en el elemento cuatro.

4.  Asignar nuevos parámetros o nuevos tipos de datos a través de un contenedor.

    Esta solución se aplica cuando un nuevo parámetro o tipo de datos debe exponerse a un usuario, pero realmente no tiene que estar remoto por separado o se puede asignar a los parámetros o tipos de datos antiguos. Por ejemplo, muchas API del sistema giran y ejecutan una llamada remota. Es posible que esté realizando algún tipo de asignación de los tipos de datos conocidos del usuario a los tipos de datos que se usan realmente en la llamada RPC subyacente. Por lo tanto, siempre merece la pena examinar si el cambio en la interfaz de usuario debe propagarse como un cambio a una interfaz remota.

    Puede ocurrir una situación similar cuando el usuario llama directamente a una API remota, pero se podría introducir un contenedor para realizar una nueva asignación de tipos o algunas otras acciones adicionales que se han hecho necesarias. El lenguaje de definición de interfaz (IDL) tiene varias maneras de facilitar dicha reapping, es decir, llamar a como , transmitir como \[ [**\_**](/windows/desktop/Midl/call-as) \] y \[ [**\_**](/windows/desktop/Midl/transmit-as) \] \[ [**\_ serializar la conexión.**](/windows/desktop/Midl/wire-marshal) \] La \[ **llamada \_ como** \] atributo introduce un contenedor de funciones en el cliente y el servidor. Ambos se colocan entre el código de usuario y el serializador. Los demás atributos se tratan con la asignación de tipos directos. En el caso de los problemas de extensión, llame a como se usa con más frecuencia y es más fácil de entender y manipular sin \[ **\_** \] problemas.

5.  Modifique los tipos de datos mediante una unión sin valores predeterminados.

    El cambio de un atributo o un tipo de datos suele dar lugar a incompatibilidades de conexión. Vea [Ejemplos de cambios incompatibles](examples-of-incompatible-changes.md) para obtener ejemplos. Sin embargo, en el caso de una unión sin una cláusula predeterminada, la incompatibilidad se puede administrar de forma similar al caso de un procedimiento fuera del intervalo, como se describió anteriormente. Este esquema es fácilmente aplicable a los tipos *XxxINFO* populares que usan uniones.

    Por ejemplo, una llamada como esta

    ```C++
    XxxGetInfo( [in] level, [out] XxxINFO  * pInfo );
    ```

    

    podría devolver información en los niveles 1, 2 o 3, siendo *XxxINFO* una unión con tres ramas: 1, 2 y 3.

6.  Use el \[ [**atributo range**](/windows/desktop/Midl/range) \] para especificar range.

    Puede especificar el atributo \[ [**range en**](/windows/desktop/Midl/range) \] un tipo de escala simple sin romper la compatibilidad con versiones anteriores. Este atributo no afecta al formato de conexión, pero durante la desmarshalling RPC comprueba el valor de la conexión para confirmar que se encuentra dentro del intervalo especificado en el archivo .idl. Si no es así, se produce \_ una excepción RPC X \_ INVALID \_ BOUND. Esto es especialmente útil si el servidor conoce el tamaño máximo de una matriz de tamaño.

    Por ejemplo:

    ```C++
    HRESULT Method1( [in, range(0,100)] ULONG m, [size_is(m)] ULONG *plong); 
    ```

    

El comportamiento de RPC cuando el nivel indicado es 4 y falta el arm, depende de la definición de la unión. Para una unión con la cláusula predeterminada definida, RPC transmite un tipo indicado en la cláusula default para cualquier cosa distinta de las etiquetas arm conocidas (en este caso, cualquier otro valor distinto de 1, 2 o 3). En el caso de una unión sin valores predeterminados, el elemento unmarserror genera una excepción porque, por definición, no hay ningún valor predeterminado al que volver. La excepción es RPC \_ S \_ INVALID \_ TAG.

De nuevo, un nuevo cliente puede ajustar su comportamiento al detectar que llamó a un servidor antiguo.

Lo que sigue a estos procedimientos recomendados es que, si se debe diseñar un tipo de datos remotable que se pueda extender en el futuro, use una unión sin valores predeterminados en el archivo IDL. Dada una opción, una unión encapsulada es ligeramente más limpia.

Debido a las peculiaridades de la representación interna del protocolo de conexión MBI64, la recomendación para agregar las manos proporcionadas anteriormente en esta sección debe calificarse de la siguiente manera: El nuevo arm que se agrega no puede cambiar la alineación de la unión y, en particular, la alineación más importante de los manos no debe cambiar. Esto no suele ser un problema, ya que un puntero en un arm fuerza la alineación a 8. Un diseño en el que cada arm es un puntero a un tipo de arm es una manera limpia de satisfacer el requisito.

 

 