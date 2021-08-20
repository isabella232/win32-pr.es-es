---
title: Reglas para administrar recuentos de referencias
description: El uso de un recuento de referencias para administrar la duración de un objeto permite que varios clientes obtengan y liberen acceso a un único objeto sin tener que coordinarse entre sí para administrar la duración del objeto.
ms.assetid: bbe7d16c-fcb7-474d-a22d-5a3b33dd800e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64babd09a28babedffe7e4078076c0554d1b4e2832503909287f2643ab7e4877
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104357"
---
# <a name="rules-for-managing-reference-counts"></a>Reglas para administrar recuentos de referencias

El uso de un recuento de referencias para administrar la duración de un objeto permite que varios clientes obtengan y liberen acceso a un único objeto sin tener que coordinarse entre sí para administrar la duración del objeto. Siempre que el objeto de cliente se ajuste a ciertas reglas de uso, el objeto, en efecto, proporciona esta administración. Estas reglas especifican cómo administrar las referencias entre objetos. (COM no especifica implementaciones internas de objetos, aunque estas reglas son un punto de partida razonable para una directiva dentro de un objeto).

Conceptualmente, se puede pensar que los punteros de interfaz residen dentro de variables de puntero que incluyen todo el estado de cálculo interno que contiene un puntero de interfaz. Esto incluiría variables en ubicaciones de memoria, en registros internos del procesador y variables generadas por el programador y generadas por el compilador. La asignación o inicialización de una variable de puntero implica la creación de una nueva copia de un puntero ya existente. Donde había una copia del puntero en alguna variable (el valor usado en la asignación o inicialización), ahora hay dos. Una asignación a una variable de puntero destruye la copia del puntero actualmente en la variable, al igual que la destrucción de la propia variable. (Es decir, se destruye el ámbito en el que se encuentra la variable, como el marco de pila).

Desde la perspectiva de un cliente COM, el recuento de referencias siempre se realiza para cada interfaz. Los clientes nunca deben suponer que un objeto usa el mismo contador para todas las interfaces.

El caso predeterminado es que se debe llamar a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) para cada nueva copia de un puntero de interfaz y se debe llamar a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para cada destrucción de un puntero de interfaz, excepto cuando las reglas siguientes permiten lo contrario:

-   **Parámetros de entrada y salida para funciones.** El autor de la llamada debe llamar a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) en el parámetro porque se liberará (con una llamada a [**Release)**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)en el código de implementación cuando el valor out se almacene encima de él.
-   **Captura de una variable global.** Al crear una copia local de un puntero de interfaz a partir de una copia existente del puntero en una variable global, debe llamar a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) en la copia local porque otra función podría destruir la copia en la variable global mientras la copia local sigue siendo válida.
-   **Nuevos punteros sintetizados de "aire fino".** Una función que sintetiza un puntero de interfaz mediante conocimiento interno especial en lugar de obtenerlo de otro origen debe llamar a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) inicialmente en el puntero recién sintetizado. Algunos ejemplos importantes de estas rutinas son las rutinas de creación de instancias, las implementaciones de [**QueryInterface,**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))y así sucesivamente.
-   **Recuperar una copia de un puntero almacenado internamente.** Cuando una función recupera una copia de un puntero almacenado internamente por el objeto llamado, el código de ese objeto debe llamar a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) en el puntero antes de que se devuelva la función. Una vez recuperado el puntero, el objeto de origen no tiene ninguna otra manera de determinar cómo se relaciona su duración con la de la copia almacenada internamente del puntero.

Las únicas excepciones al caso predeterminado requieren que el código de administración conozca las relaciones de las duraciones de dos o más copias de un puntero a la misma interfaz en un objeto y simplemente asegúrese de que el objeto no se destruye al permitir que su recuento de referencias vaya a cero. Por lo general, hay dos casos, como se muestra a continuación:

-   Cuando ya existe una copia de un puntero y se crea una segunda posteriormente y, a continuación, se destruye mientras la primera copia sigue existiendo, se pueden omitir las llamadas a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)para la segunda copia.
-   Cuando existe una copia de un puntero y se crea un segundo y, a continuación, se destruye la primera antes de la segunda, se pueden omitir las llamadas a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)para la segunda copia y a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para la primera copia.

A continuación se muestran ejemplos específicos de estas situaciones, siendo las dos primeras especialmente comunes:

-   **En parámetros para funciones.** La duración de la copia de un puntero de interfaz pasado como parámetro a una función está anidada en la del puntero utilizado para inicializar el valor, por lo que no es necesario un recuento de referencias independiente en el parámetro.
-   **Parámetros out de las funciones, incluidos los valores devueltos.** Para establecer el parámetro out, la función debe tener una copia estable del puntero de interfaz. En la devolución, el autor de la llamada es responsable de liberar el puntero. Por lo tanto, el parámetro out no necesita un recuento de referencias independiente.
-   **Variables locales.** Una implementación de método tiene el control de la duración de cada una de las variables de puntero asignadas en el marco de pila y puede usarla para determinar cómo omitir pares [**de versión**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) / [**AddRef redundantes.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
-   **Backpointers.** Algunas estructuras de datos contienen dos objetos, cada uno con un puntero al otro. Si se sabe que la duración del primer objeto contiene la duración del segundo, no es necesario tener un recuento de referencias en el puntero del segundo objeto al primer objeto. A menudo, evitar este ciclo es importante para mantener el comportamiento de desasignación adecuado. Sin embargo, los punteros sin contar deben usarse con mucha precaución, ya que la parte del sistema operativo que controla el procesamiento remoto no tiene forma de conocer esta relación. Por lo tanto, en casi todos los casos, hacer que el backpointer vea un segundo objeto "friend" del primer puntero (evitando así la circularidad) es la solución preferida. La arquitectura de objetos conectables de COM, por ejemplo, usa este enfoque.

Al implementar o usar objetos con recuento de referencias, puede ser útil aplicar recuentos de referencias *artificiales,* lo que garantiza la estabilidad de los objetos durante el procesamiento de una función. Al implementar un método de una interfaz, puede llamar a funciones que tienen la posibilidad de disminuir el recuento de referencias a un objeto, lo que provoca una liberación prematura del objeto y un error en la implementación. Una manera sólida de evitar esto es insertar una llamada a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) al principio de la implementación del método y emparejar con una llamada a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) justo antes de que el método vuelva.

En algunas situaciones, los valores devueltos [**de AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pueden ser inestables y no deben basarse en ellos. solo se deben usar con fines de depuración o diagnóstico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de duraciones de objetos mediante el recuento de referencias](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 