---
description: Normalmente, la latencia entre los niveles de una aplicación distribuida difiere en gran medida.
ms.assetid: 4780a9fd-5940-4b10-a596-22214b17c033
title: Optimizar las interacciones entre el nivel de lógica empresarial de COM+ y el nivel de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe6094cb12cc7875d8a18dea3d28ac55bf8d6ae2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705363"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-presentation-tier"></a>Optimizar las interacciones entre el nivel de lógica empresarial de COM+ y el nivel de presentación

Normalmente, la latencia entre los niveles de una aplicación distribuida difiere en gran medida. Las llamadas entre el nivel de presentación y el nivel de lógica de negocios suelen ser un orden de magnitud más lento que las llamadas entre el nivel de negocio y la capa de datos. Como resultado, el estado de retención es más costoso cuando se llama al nivel de lógica de negocios.

En los temas siguientes se describen las distintas formas de pasar datos entre los niveles de presentación y lógica de negocios:

-   [Pasar parámetros](#passing-parameters)
-   [Opciones de paso de datos](#data-passing-options)
-   [Uso de un patrón de fábrica para pasar datos](#using-a-factory-pattern-to-pass-data)
-   [Temas relacionados](#related-topics)

## <a name="passing-parameters"></a>Pasar parámetros

Para que un conjunto determinado de información se pase entre el nivel de presentación y el nivel de lógica de negocios, puede tener una sola fila, varias filas o una combinación de una sola fila (por ejemplo, un encabezado) y varias filas de datos de detalles. La manera más eficaz de pasar esta información entre los niveles es mediante una única llamada al método. Esta única llamada administraría todo el conjunto de información que se va a pasar. Esto es necesario a menos que decida controlar la transacción desde el nivel de presentación (y hacer que todo el tratamiento de las transacciones en el nivel de presentación sea idéntico en la función). Microsoft no recomienda la realización de transacciones desde el nivel de presentación, ya que las llamadas entre este nivel y el nivel de lógica de negocios suelen ser las más lentas que las llamadas en una aplicación de niveles múltiples.

Una manera de crear este tipo de método es pasar filas únicas de información como parámetros y pasar varias filas como conjuntos de registros ADO. Los conjuntos de registros son el núcleo de la metodología de acceso a datos ADO de Microsoft y el uso de conjuntos de registros ADO permite pasar toda la información relacionada con una sola transacción en un solo paso.

## <a name="data-passing-options"></a>Opciones de paso de datos

Hay otras opciones que hay que tener en cuenta al pasar datos. Entre ellas se incluye el uso de una lista de parámetros y conjuntos de registros ADO (como se explicó anteriormente), simplemente conjuntos de registros ADO, cadenas codificadas XML o matrices de estructuras. En esta sección se describe cada una de estas opciones.

En la tabla siguiente se muestran las áreas en las que es necesario prestar atención adicional al usar cualquiera de las cuatro posibilidades de pasar argumentos diferentes. Una "X" representa áreas en las que es necesario entender y comparar los pros y las necesidades de cada proyecto. Intente no tomar decisiones de pasar argumentos por componente. Las ventajas de un modelo de programación coherente a lo largo de un proyecto superan las ventajas de la optimización por cada método o por componente en todas las circunstancias, excepto en las más extremas. Las columnas se describen en la lista que sigue a la tabla.



|                       | Simultaneidad  | WAN          | Implementación   | Complejidad   |
|-----------------------|--------------|--------------|--------------|--------------|
| Entrada | Value |
| Conjuntos<br/> |              | X<br/> | X<br/> | X<br/> |
| XML<br/>        | X<br/> |              | X<br/> | X<br/> |
| Matrices<br/>     | X<br/> |              | X<br/> | X<br/> |



 

Las cuatro columnas definen las áreas que se deben ver al usar esta opción para pasar parámetros.

-   **La columna de simultaneidad** representa la necesidad de codificar o proporcionar un mecanismo que administre las condiciones de bloqueo en las operaciones de actualización. Dado que los métodos que realizan tareas de guardar pueden representar actualizaciones, pueden surgir problemas de simultaneidad. Dos tipos de bloqueo son optimistas y pesimistas. Los bloqueos pesimistas impiden que un usuario Obtenga datos para su actualización mientras otro usuario tiene la posibilidad de realizar una actualización. El bloqueo optimista es compatible con muchos más usuarios mediante la negociación de la probabilidad de que dos usuarios cualesquiera estén actualizando el mismo documento al mismo tiempo. Las llamadas de bloqueo optimista para comprobar que los datos almacenados coinciden con los datos en el momento en que se tuvo acceso a una copia de los datos para su modificación. Los conjuntos de registros ADO proporcionan compatibilidad automática con el bloqueo optimista. Los escenarios de actualización que implican listas de parámetros de una sola fila no proporcionan suficiente compatibilidad para la comprobación de simultaneidad. XML se ve afectado por este mismo problema, en el que no hay ningún conocimiento de bloqueo presente en los datos XML.
-   **La columna WAN** representa las condiciones en las que puede haber contención de la transmisión en una red de área extensa (WAN). Cuando la WAN no tiene suficiente capacidad para administrar todos los datos que se mueven en un momento dado, los usuarios de la aplicación experimentan retrasos en el tiempo de respuesta. Para admitir la simultaneidad optimista, los conjuntos de registros ADO desconectados pasan dos copias de los datos del servidor al cliente. El cliente utiliza la segunda copia para determinar el conjunto de filas de actualización más pequeño que se va a devolver cuando se confirme un cambio. Aunque esto reduce el tráfico del nivel de presentación a los datos, la carga adicional de la segunda copia puede ser significativa. El uso de conjuntos de registros como el único medio para pasar toda la información provoca que se pasen dos veces tantos datos entre niveles como sea necesario, excepto cuando el conjunto de filas de actualización se pasa de nuevo a la capa de datos desde un nivel de presentación.
-   **La columna implementación representa los** problemas asociados con los datos que pasan cuando se requiere una tecnología especial tanto en el lado del autor de la llamada como en el componente de la red. Por ejemplo, el uso de conjuntos de registros ADO requiere que los componentes de ADO estén presentes tanto en el cliente como en el servidor. Los analizadores XML deben estar presentes también en ambos lados para evitar tener que realizar analizadores de código en las aplicaciones.
-   **La columna complejidad** se indica para las cuatro opciones y es una cuestión de preferencia o la experiencia del modelo de programación anterior que puede estar ya establecida en la organización de desarrollo. Algunas personas buscan que el paso de los parámetros sea engorroso y se sienta que agrega demasiada complejidad al problema de programación. La realización de un seguimiento de los parámetros que se están controlando y de todos ellos visibles en una ventana de edición puede crear una complejidad logística que algunos desarrolladores encuentren no administrables.

El método de paso de parámetros también puede tener equilibrios, como los siguientes:

-   Los parámetros pueden implicar la administración de varios argumentos y tipos de argumento, así como tener que decidir cuándo es adecuado convertir un parámetro en un conjunto de registros.
-   Los conjuntos de registros ADO pueden cortar relaciones jerárquicas en parámetros de método hasta uno o dos argumentos. Esto simplifica considerablemente el modelo de programación y permite agregar columnas en otro momento, pero también oculta la jerarquía de información. La información sobre el contenido de un conjunto de registros ADO y su extracción posterior implica conocer los nombres de cada columna o conocer el orden de las columnas. Esta situación puede Agregar complejidad a otros desarrolladores de componentes o aplicaciones en el proyecto.
-   XML es un giro diferente en la complejidad de la jerarquía oculta mencionada anteriormente. El programador debe comprender el uso de un analizador XML para obtener acceso a la información y, a menudo, debe conocer los nombres de cada elemento del conjunto de datos antes de que se pueda encontrar el conjunto de datos.
-   Las matrices de estructuras presentan la necesidad de una comprensión común de la información que se pasa en la parte del autor de la llamada y del componente. Esta necesidad de una asignación que se comparte entre dos elementos del sistema puede dar lugar a dificultades cuando se trabaja con versiones diferentes de los componentes. Aunque la firma del método podría no cambiar, los cambios en la información esperada pueden representar programas que llaman incompatibles.

Dado que los problemas de complejidad asociados con los cuatro métodos de paso de parámetros son tan similares, es cuestionable que hay una oportunidad de simplificación importante asociada a cualquier selección.

## <a name="using-a-factory-pattern-to-pass-data"></a>Uso de un patrón de fábrica para pasar datos

Un punto de diseño importante es la facilidad de uso. El momento en que decidió usar conjuntos de registros ADO para pasar un conjunto estructurado de detalles de nuevo al nivel de presentación, ha introducido un problema de complejidad. Los programadores de nivel de presentación deben comprender la estructura de esos conjuntos de registros. Se puede producir un problema de complejidad mayor cuando se requieren varios detalles para un conjunto de datos que se va a pasar en un conjunto de registros. Para simplificar las cosas, considere la posibilidad de crear un conjunto de registros Factory Method siempre que pretenda requerir que los datos se pasen en conjuntos de registros ADO estructurados.

El generador de registros debe devolver un conjunto de registros desconectado sin conexión que se pueda escribir al llamador. Este conjunto de registros debe tener los campos adecuados (nombres y tipos de datos) ya configurados para que el cliente que realiza la llamada no necesite saber cómo fabricar el conjunto de registros. Este enfoque se conoce a menudo como el *patrón de fábrica* y es un patrón de solución común que resuelve la necesidad de crear un objeto de una determinada complejidad sin tener que conocer los matices de la creación.

Las opciones de diseño simples, como elegir el mismo nombre de parámetro para los mismos datos en cada método en el que se pasa esa información, facilitan la búsqueda de un método y saben lo que se espera. Asegurarse de que el orden en el que se pasan los argumentos es coherente en toda una familia de métodos proporciona un punto de confort que aplica un modelo coherente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Optimizar las interacciones entre el nivel de lógica empresarial de COM+ y el nivel de datos](optimizing-interactions-between-the-com--business-logic-tier-and-the-data-tier.md)
</dt> </dl>

 

 




