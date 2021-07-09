---
description: Obtenga información sobre las definiciones de opciones en el esquema PrintCapabilities. Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: e81068db-ab8e-420c-a0be-93bc92f3df6f
title: Definiciones de opciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc7dddb4840de8bc91c7f9ab127fd31319e5399
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549373"
---
# <a name="option-definitions"></a>Definiciones de opciones

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

La consideración clave al definir una opción es hacerlo de forma que se pueda comparar significativamente con otras instancias de option contenidas en la misma característica. La comparación debe ser significativa porque la instancia de Option se usa para definir la configuración no solo del dispositivo, sino del trabajo, independientemente del dispositivo o PrintCapabilities que se usaron para crear la configuración. Las otras instancias de Opción de la característica pueden aparecer en el mismo documento PrintCapabilities o en otro documento PrintCapabilities que represente un dispositivo diferente, un documento PrintCapabilities definido por otra parte que trabaje de forma independiente. Una vez que un cliente selecciona la configuración del dispositivo que se va a usar para representar un trabajo o documento, esa configuración normalmente se guarda, junto con el trabajo o documento, en forma de PrintTicket. PrintTicket contiene un conjunto de instancias de Option, normalmente una para cada característica definida en el documento PrintCapabilities. Las instancias de opción deben ser portátiles y conservar la intención de impresión, de modo que la intención se pueda comunicar cuando este PrintTicket se proporciona a un dispositivo diferente, incluso a uno que tenga un documento PrintCapabilities diferente escrito por otro autor. La principal ventaja de esta portabilidad es que si un dispositivo diferente no admite específicamente una opción contenida en PrintTicket, el controlador o subsistema del dispositivo puede identificar y seleccionar la opción más cercana en la funcionalidad.

Una de las funciones principales de PrintTicket del controlador es identificar la opción del dispositivo en el documento PrintCapabilities que coincida más estrechamente con una opción determinada que aparece en PrintTicket. Durante este proceso de puntuación definido por el controlador de dispositivo o  de coincidencia, la opción de PrintTicket se conoce  como opción de referencia, mientras que la opción del documento PrintCapabilities se conoce como opción candidata. La métrica de coincidencia general es el número de instancias scoredProperty que coinciden en las instancias de opción candidatas y de referencia. un mayor número de coincidencias suele indicar una mejor conservación de la intención de impresión. En el proceso de puntuación, puede optar por dar mayor peso a algunos elementos ScoredProperty que a otros.

Puede hacer que las instancias de Option se puedan convertir en portables asegurándose de que todas las instancias de Option que pertenecen a la misma característica tienen uno o varios elementos ScoredProperty *en común.* Esto significa que hay un conjunto de elementos ScoredProperty que aparece en cada instancia de Option (que pertenece a la misma característica). Por ejemplo, las instancias option de la característica PageMediaSize pueden ser portables si cada instancia de Option contiene elementos ScoredProperty que definen las propiedades intrínsecas PageMediaSize: MediaSizeWidth y MediaSizeHeight. A continuación, el código del controlador o subsistema del dispositivo puede determinar si dos instancias de Option coinciden comparando las diferencias en estos valores scoredProperty. Si no hay ninguna opción en el documento PrintCapabilities que coincida exactamente con la de PrintTicket, el controlador del dispositivo puede determinar y seleccionar fácilmente la opción que tenga las dimensiones de medios que coincidan más.

Se dice que dos objetos (instancias de opción en este caso) tienen elementos en común o, de forma equivalente, tienen elementos correspondientes *,* si se cumplen las tres condiciones siguientes.

1.  Los dos elementos son del mismo tipo de elemento.

2.  Los atributos de nombre de los dos elementos son idénticos (o ninguno de los elementos contiene un atributo name).

3.  La cadena de elementos principales de los elementos que se comparan, hasta los dos objetos en consideración, debe cumplir las condiciones 1 y 2.

Por ejemplo, considere una situación en la que hay dos instancias de Option, donde cada una contiene una instancia scoredProperty y cada una de estas instancias de ScoredProperty contiene una instancia property. Claramente, se cumple la primera condición (las dos instancias de propiedad son del mismo tipo) y se cumple parte de la tercera condición (los elementos principales de las instancias property son del mismo tipo, ScoredProperty, y los elementos principales de esos elementos son las instancias option, que también son del mismo tipo). Si los atributos de nombre de, respectivamente, las instancias property, scoredProperty y option son idénticos o no se proporcionan, las dos instancias de Option tienen elementos en común.

Desde el principio, el primer paso para crear instancias de Option es definir un conjunto de elementos ScoredProperty que están presentes en la mayoría o en todas las instancias de Option. Si el atributo de configuración del dispositivo se puede representar mediante una característica estándar (que aparece en las palabras clave de esquema de impresión), tenga en cuenta los elementos ScoredProperty en común en las instancias de option estándar. Debe asegurarse de que las nuevas instancias de Option que introduzca también contengan estos elementos ScoredProperty. Siempre puede agregar elementos ScoredProperty adicionales según sea necesario para diferenciar las instancias de Option de las instancias estándar de Option. Incluso puede eliminar uno o varios de los elementos ScoredProperty en común si hay una buena razón, aunque esto reduce la portabilidad de este tipo de opción. Por supuesto, las consideraciones de portabilidad sugieren el uso de las instancias de option estándar sin modificar a menos que haya alguna diferencia intrínseca entre la opción y la instancia de opción estándar que se debe reflejar en la nueva instancia de Option.

En el ejemplo siguiente se muestra una situación para la que es posible que desee agregar un elemento ScoredProperty a una instancia de Option. Todas las instancias de option estándar de la característica PageMediaSize tienen los elementos MediaSizeWidth y MediaSizeHeight ScoredProperty en común. Supongamos que el dispositivo puede admitir uno de los tamaños de medios letter estándar alimentando el papel de forma transversal (LongEdgeFirst) o de forma inversa (ShortEdgeFirst). Suponiendo que no desea introducir una nueva característica de dirección de fuente para exponer este grado de libertad, en su lugar puede modificar las dos instancias de la opción PageMediaSize para Letter para incorporar la orientación de la fuente de papel. Para estas dos instancias de Letter Option, comience con la instancia estándar PageMediaSize Option y agregue un nuevo elemento ScoredProperty para representar FeedDirection. En una instancia de Option, establezca FeedDirection ScoredProperty en LongEdgeFirst; en la otra instancia de Option, establezca FeedDirection en ShortEdgeFirst. Observe que estas nuevas instancias de Option mantienen su portabilidad. Si la opción que representa Letter, ShortEdgeFirst se guarda en un PrintTicket y se selecciona un dispositivo diferente que solo admite la opción estándar Letter para representar el trabajo, el código de coincidencia de opciones puede determinar rápidamente que la letra de opción estándar es la mejor coincidencia con la letra de opción, ShortEdgeFirst. La razón por la que esta es la mejor coincidencia es que todas las instancias de ScoredProperty coinciden, a excepción de FeedDirection ScoredProperty, que no existe en la opción estándar Letter.

También puede encontrar casos en los que las modificaciones realizadas en la opción cambian realmente el significado tanto que la opción modificada ya no se puede considerar un caso especializado del original. En tales casos, debe cambiar el nombre de la opción para reflejar la diferencia entre la instancia de Option modificada y la no modificada. Solo el autor del documento PrintCapabilities para un dispositivo determinado puede decidir si la opción que ofrece el dispositivo difiere lo suficiente de una instancia de opción estándar para garantizar una definición incompatible.

Ahora considere el caso en el que el dispositivo tiene un atributo de configuración de dispositivo que no se corresponde con ninguna de las instancias de características estándar. En este caso, no puede confiar en las instancias de Option estándar para proporcionar la lista de elementos ScoredProperty en común. Al crear una instancia de ScoredProperty, el objetivo principal es diferenciar cada opción de las demás de la característica y describir por qué un usuario seleccionaría una opción sobre otra. La línea de base es caracterizar cada opción con un atributo de nombre único y ScoredProperty que contiene el atributo name se convierte en la que se usa para determinar los elementos en común.

Una vez establecido un conjunto de elementos ScoredProperty en común, es una cuestión sencilla asignar los valores adecuados a cada ScoredProperty para crear cada opción. Como en el ejemplo anterior, para determinadas instancias de Option, es posible que tenga que agregar instancias de ScoredProperty adicionales o eliminar algunos de los elementos en común para crear una instancia de Option adecuada.

Debe tenerse en cuenta que el esquema de impresión requiere que el conjunto de instancias scoredProperty, sus ubicaciones y los valores asignados a cada ScoredProperty en una opción deben permanecer constantes, independientemente de la configuración. El concepto completo del esquema de impresión se basa en instancias de opción que tienen instancias de Property y ScoredProperty fijas y identificables que se comparten entre muchos dispositivos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



