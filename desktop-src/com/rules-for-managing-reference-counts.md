---
title: Reglas para administrar recuentos de referencias
description: El uso de un recuento de referencias para administrar la duración de un objeto permite que varios clientes obtengan y liberen el acceso a un único objeto sin tener que coordinarse entre sí en la administración de la duración del objeto.
ms.assetid: bbe7d16c-fcb7-474d-a22d-5a3b33dd800e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9520cbbc88cb73c6e2abbd7908bed3754bb3945
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421443"
---
# <a name="rules-for-managing-reference-counts"></a>Reglas para administrar recuentos de referencias

El uso de un recuento de referencias para administrar la duración de un objeto permite que varios clientes obtengan y liberen el acceso a un único objeto sin tener que coordinarse entre sí en la administración de la duración del objeto. Siempre que el objeto de cliente se ajuste a ciertas reglas de uso, el objeto, en efecto, proporciona esta administración. Estas reglas especifican cómo administrar las referencias entre objetos. (COM no especifica implementaciones internas de objetos, aunque estas reglas son un punto de partida razonable para una directiva dentro de un objeto).

Conceptualmente, los punteros de interfaz se pueden considerar como residentes en variables de puntero que incluyen todo el estado de cálculo interno que contiene un puntero de interfaz. Esto incluiría las variables en las ubicaciones de memoria, en los registros internos del procesador y en las variables generadas por el programador y las generadas por el compilador. La asignación o inicialización de una variable de puntero implica la creación de una nueva copia de un puntero ya existente. Cuando haya una copia del puntero en alguna variable (el valor usado en la asignación/inicialización), ahora habrá dos. Una asignación a una variable de puntero destruye la copia del puntero en la variable, al igual que la destrucción de la propia variable. (Es decir, se destruye el ámbito en el que se encuentra la variable, como el marco de pila).

Desde la perspectiva del cliente COM, siempre se realiza el recuento de referencias para cada interfaz. Los clientes nunca deben suponer que un objeto utiliza el mismo contador para todas las interfaces.

El caso predeterminado es que se debe llamar a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) para cada nueva copia de un puntero de interfaz y se debe llamar a la [**versión**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para cada destrucción de un puntero de interfaz, excepto en los casos en los que las siguientes reglas permiten lo contrario:

-   **Parámetros de salida a funciones.** El autor de la llamada debe llamar a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) en el parámetro porque se liberará (con una llamada a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)) en el código de implementación cuando el valor de salida se almacena encima de él.
-   **Obteniendo una variable global.** Al crear una copia local de un puntero de interfaz a partir de una copia existente del puntero en una variable global, debe llamar a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) en la copia local, ya que otra función puede destruir la copia en la variable global mientras la copia local sigue siendo válida.
-   **Nuevos punteros sintetizados de "finos".** Una función que sintetiza un puntero de interfaz mediante un conocimiento interno especial en lugar de obtenerlo de otro origen debe llamar a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) inicialmente en el puntero recién sintetizado. Entre los ejemplos importantes de estas rutinas se incluyen las rutinas de creación de instancias, las implementaciones de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), etc.
-   **Recuperar una copia de un puntero almacenado internamente.** Cuando una función recupera una copia de un puntero almacenado internamente por el objeto denominado, el código de ese objeto debe llamar a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) en el puntero antes de que se devuelva la función. Una vez que se ha recuperado el puntero, el objeto de origen no tiene ninguna otra manera de determinar cómo se relaciona su duración con la de la copia almacenada internamente del puntero.

Las únicas excepciones a los casos predeterminados requieren que el código de administración Conozca las relaciones de las duraciones de dos o más copias de un puntero a la misma interfaz en un objeto y, simplemente, asegúrese de que el objeto no se destruya permitiendo que su recuento de referencias vaya a cero. Normalmente hay dos casos, como se indica a continuación:

-   Cuando ya existe una copia de un puntero y se crea un segundo posteriormente y se destruye mientras la primera copia sigue existiendo, se pueden omitir las llamadas a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)para la segunda copia.
-   Cuando existe una copia de un puntero y se crea un segundo y, a continuación, el primero se destruye antes del segundo, se pueden omitir las llamadas a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)para la segunda copia y a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para la primera copia.

A continuación se muestran ejemplos específicos de estas situaciones, las dos primeras son especialmente comunes:

-   **En parámetros de funciones.** La duración de la copia de un puntero de interfaz que se pasa como un parámetro a una función está anidada en la del puntero que se usa para inicializar el valor, por lo que no es necesario contar con un recuento de referencias independiente en el parámetro.
-   **Parámetros out de funciones, incluidos los valores devueltos.** Para establecer el parámetro de salida, la función debe tener una copia estable del puntero de interfaz. En la devolución, el llamador es responsable de liberar el puntero. Por lo tanto, el parámetro out no necesita un recuento de referencias independiente.
-   **Variables locales.** Una implementación de método tiene el control de la duración de cada una de las variables de puntero asignadas en el marco de pila y puede usarla para determinar cómo se deben omitir los pares de versiones [**redundantes**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) / [](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .
-   **Punteros al extremo.** Algunas estructuras de datos contienen dos objetos, cada uno con un puntero al otro. Si se sabe que la duración del primer objeto contiene la duración del segundo, no es necesario tener un recuento de referencias en el puntero del segundo objeto al primer objeto. A menudo, evitar este ciclo es importante para mantener el comportamiento de desasignación adecuado. Sin embargo, los punteros descontados deben usarse con sumo cuidado porque la parte del sistema operativo que controla el procesamiento remoto no tiene forma de conocer esta relación. Por lo tanto, en casi todos los casos, tener el puntero hacia arriba ve un segundo objeto "Friend" del primer puntero (lo que evita la circularidad) es la solución preferida. La arquitectura de los objetos conectables de COM, por ejemplo, usa este enfoque.

Al implementar o usar objetos con recuento de referencias, puede resultar útil aplicar *recuentos de referencias artificiales*, que garantizan la estabilidad del objeto durante el procesamiento de una función. Al implementar un método de una interfaz, puede llamar a funciones que tienen la posibilidad de reducir el recuento de referencias a un objeto, lo que provoca una liberación prematura del objeto y el error de la implementación. Una manera eficaz de evitarlo es insertar una llamada a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) al principio de la implementación del método y emparejarla con una llamada a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) justo antes de que el método devuelva.

En algunas situaciones, los valores devueltos de [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pueden ser inestables y no se deben confiar en ellos; solo se deben usar con fines de depuración o diagnóstico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrar la duración de los objetos mediante el recuento de referencias](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 