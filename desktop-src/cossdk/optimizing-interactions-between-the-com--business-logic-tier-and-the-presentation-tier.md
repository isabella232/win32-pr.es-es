---
description: Normalmente, la latencia entre los niveles de una aplicación distribuida difiere mucho.
ms.assetid: 4780a9fd-5940-4b10-a596-22214b17c033
title: Optimización de interacciones entre el nivel de lógica de negocios de COM+ y el nivel de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ca519c6aa7f1585648b0def6530b7f224f12a98961193e4f6f7cc490a747b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306107"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-presentation-tier"></a>Optimización de interacciones entre el nivel de lógica de negocios de COM+ y el nivel de presentación

Normalmente, la latencia entre los niveles de una aplicación distribuida difiere mucho. Las llamadas entre el nivel de presentación y el nivel de lógica de negocios suelen ser un orden de magnitud más lento que las llamadas entre el nivel de negocio y el nivel de datos. Como resultado, el estado mantenido es más costoso al llamar al nivel de lógica de negocios.

En los temas siguientes se tratan formas de pasar datos entre los niveles de presentación y lógica de negocios:

-   [Pasar parámetros](#passing-parameters)
-   [Opciones de paso de datos](#data-passing-options)
-   [Usar un patrón de fábrica para pasar datos](#using-a-factory-pattern-to-pass-data)
-   [Temas relacionados](#related-topics)

## <a name="passing-parameters"></a>Pasar parámetros

Para que un conjunto determinado de información se pase entre el nivel de presentación y el nivel de lógica de negocios, puede tener una sola fila, varias filas o una combinación de una sola fila (por ejemplo, un encabezado) y varias filas de detalles de datos. La manera más eficaz de pasar esta información entre niveles es mediante una sola llamada de método. Esta única llamada administraría todo el conjunto de información que se va a pasar. Esto es necesario a menos que decida controlar la transacción desde el nivel de presentación (y hacer que todo el tratamiento de transacciones en el nivel de presentación sea idéntico en función). Microsoft no recomienda realizar transacciones desde el nivel de presentación porque las llamadas entre este nivel y el nivel de lógica de negocios suelen ser las más lentas de las llamadas en una aplicación de varios niveles.

Una manera de crear este tipo de método es pasar filas únicas de información como parámetros y pasar varias filas como conjuntos de registros de ADO. Los conjuntos de registros son el núcleo de la metodología de acceso a datos ADO de Microsoft y el uso de conjuntos de registros de ADO permite pasar toda la información relacionada con una única transacción en un solo paso.

## <a name="data-passing-options"></a>Opciones de paso de datos

Hay otras opciones que se deben tener en cuenta al pasar datos. Estos incluyen el uso de una lista de parámetros y conjuntos de registros de ADO (como se explicó anteriormente), solo conjuntos de registros ADO, cadenas codificadas XML o matrices de estructuras. En esta sección se describe cada una de estas opciones.

En la tabla siguiente se muestran las áreas en las que es necesario tener más cuidado al usar cualquiera de las cuatro posibilidades de paso de argumentos diferentes. Una "X" representa áreas en las que es necesario comprender y ponderar los puntos de acuerdo con las necesidades de cada proyecto. Intente no tomar decisiones de paso de argumentos por componente. Las ventajas de un modelo de programación coherente en un proyecto superan con creces cualquier ventaja de la optimización por método o por componente en todas las circunstancias menos en las más extremas. Las columnas se describen en la lista que sigue a la tabla.



|     &nbsp;                  | Simultaneidad  | WAN          | Implementación   | Complejidad   |
|-----------------------|--------------|--------------|--------------|--------------|
| Entrada | Valor |
| Registros<br/> |              | X<br/> | X<br/> | X<br/> |
| XML<br/>        | X<br/> |              | X<br/> | X<br/> |
| Matrices<br/>     | X<br/> |              | X<br/> | X<br/> |



 

Las cuatro columnas definen las áreas que se deben tener en cuenta al usar esa opción para pasar parámetros.

-   **La columna Simultaneidad** representa la necesidad de codificar o proporcionar un mecanismo que administre las condiciones de bloqueo en las operaciones de actualización. Puesto que los métodos que realizan guardados pueden representar actualizaciones, pueden surgir problemas de simultaneidad. Dos tipos de bloqueo son optimistas y pesimistas frecuentes. Los bloqueos pesimistas impiden que un usuario pueda obtener datos para la actualización, mientras que otro usuario tiene la posibilidad de realizar una actualización. El bloqueo optimista admite muchos más usuarios al negociar con la probabilidad de que dos usuarios puedan actualizar el mismo documento al mismo tiempo. El bloqueo optimista llama a comprobar que los datos almacenados coinciden con los datos en el momento en que se tuvo acceso a una copia de los datos para su modificación. Los conjuntos de registros de ADO proporcionan compatibilidad automática con el bloqueo optimista. Los escenarios de actualización que implican listas de parámetros de fila única no proporcionan compatibilidad suficiente para la comprobación de simultaneidad. XML sufre este mismo problema, ya que no hay ningún reconocimiento de bloqueo en los datos XML.
-   **La columna WAN representa** las condiciones en las que puede haber contención de transmisión en una red de área extensa (WAN). Cuando la WAN no tiene capacidad suficiente para administrar todos los datos que se mueven en cualquier momento, los usuarios de la aplicación experimentan retrasos en el tiempo de respuesta. Para admitir la simultaneidad optimista, los conjuntos de registros de ADO desconectados pasan dos copias de los datos del servidor al cliente. El cliente usa la segunda copia para determinar el conjunto de filas de actualización más pequeño que se va a devolver cuando se confirma un cambio. Aunque esto reduce el tráfico desde el nivel de presentación a los datos, la carga adicional de la segunda copia puede ser significativa. El uso de conjuntos de registros como único medio para pasar toda la información hace que se pasen el doble de datos entre los niveles necesarios, excepto cuando el conjunto de filas de actualización se pasa de vuelta a la capa de datos desde un nivel de presentación.
-   **La columna Implementación representa** los problemas asociados con el paso de datos cuando se requiere tecnología especial en el lado del autor de la llamada y del componente de la red. Por ejemplo, el uso de conjuntos de registros de ADO requiere que los componentes de ADO se presenten tanto en el cliente como en el servidor. Los analizadores XML también deben estar presentes en ambos lados, para evitar tener que codificar analizadores en las aplicaciones.
-   **La columna Complejidad se** indica para las cuatro opciones y es una cuestión de preferencias o experiencia del modelo de programación anterior que puede que ya esté establecida en la organización de desarrollo. Algunas personas encuentran que el paso de parámetros es complicado y se da la sensación de que agrega demasiada complejidad al problema de programación. Realizar un seguimiento del parámetro que está controlando y hacer que todos sean visibles en una ventana de edición puede crear una complejidad logística que algunos desarrolladores no pueden administrar.

El método de paso de parámetros también puede tener contras, como los siguientes:

-   Los parámetros pueden implicar la administración de varios argumentos y tipos de argumentos, así como tener que decidir cuándo es adecuado convertir un conjunto de registros en un parámetro.
-   Los conjuntos de registros de ADO pueden reducir las relaciones jerárquicas de los parámetros de método a uno o dos argumentos. Esto simplifica drásticamente el modelo de programación y admite la adición de columnas más adelante, pero también oculta la jerarquía de información. El relleno de información en un conjunto de registros de ADO y su posterior extracción implica conocer los nombres de cada columna o conocer el orden de las columnas. Esta situación puede agregar complejidad para otros desarrolladores de componentes o aplicaciones en el proyecto.
-   XML es un giro diferente en la complicación de jerarquía oculta mencionada anteriormente. El programador debe comprender el uso de un analizador XML para obtener acceso a la información y, a menudo, debe conocer los nombres de cada elemento del conjunto de datos para poder encontrar el conjunto de datos.
-   Las matrices de estructuras presentan la necesidad de un conocimiento común de la información que se pasa por parte del autor de la llamada y del componente. Esta necesidad de un mapa que se comparte entre dos elementos del sistema puede dar lugar a dificultades al tratar con diferentes versiones de componentes. Aunque es posible que la firma del método no cambie, los cambios en la información esperada pueden hacer que los programas de llamada sean incompatibles.

Dado que los problemas de complejidad asociados con los cuatro métodos de paso de parámetros son tan similares, es debatible que haya una oportunidad de simplificación significativa asociada a cualquier selección.

## <a name="using-a-factory-pattern-to-pass-data"></a>Usar un patrón de fábrica para pasar datos

Un punto de diseño importante es la facilidad de uso. En el momento en que decidió usar conjuntos de registros de ADO para volver a pasar un conjunto estructurado de detalles al nivel de presentación, introdujo un problema de complejidad. Los programadores del nivel de presentación deben comprender la estructura de esos conjuntos de registros. Puede surgir un problema de mayor complejidad cuando se requieren varios detalles para que un conjunto de datos se pase en un conjunto de registros. Para simplificar las cosas, debe considerar la posibilidad de crear un método de generador de conjuntos de registros siempre que quiera requerir que los datos se pasen en conjuntos de registros de ADO estructurados.

El generador de conjuntos de registros debe devolver un conjunto de registros desconectado vacío pero grabable al autor de la llamada. Este conjunto de registros debe tener ya configurados los campos adecuados (nombres y tipos de datos) para que el cliente que realiza la llamada no necesite saber cómo fabricación del conjunto de registros. Este enfoque se conoce a  menudo como patrón de fábrica y es un patrón de solución común que resuelve la necesidad de crear un objeto de una complejidad determinada sin tener que conocer los matices de su creación.

Las opciones de diseño sencillas, como elegir el mismo nombre de parámetro para el mismo fragmento de datos en todos los métodos en los que se pasa esa información, hacen que sea fácil ver un método y saber lo que se espera. Asegurarse de que el orden en el que se pasan argumentos like es coherente en toda una familia de métodos proporciona un punto de confort que exige un modelo coherente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Optimización de interacciones entre el nivel de lógica de negocios de COM+ y el nivel de datos](optimizing-interactions-between-the-com--business-logic-tier-and-the-data-tier.md)
</dt> </dl>

 

 




