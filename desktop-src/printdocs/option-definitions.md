---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: e81068db-ab8e-420c-a0be-93bc92f3df6f
title: Definiciones de opciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10016b295cc2da7ede4e6a4f8944f279a25f6f9b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279887"
---
# <a name="option-definitions"></a>Definiciones de opciones

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

La consideración clave al definir una opción es hacerlo de manera que pueda compararse de forma significativa con otras instancias de opciones contenidas en la misma característica. La comparación debe ser significativa porque la instancia de la opción se usa para definir la configuración no solo del dispositivo, sino del trabajo, independientemente del dispositivo o PrintCapabilities que se usaron para crear la configuración. Las demás instancias de opción de la característica pueden aparecer en el mismo documento de PrintCapabilities o en otro documento de PrintCapabilities que represente un dispositivo diferente, un documento de PrintCapabilities definido por otra parte que trabaje de forma independiente. Después de que un cliente selecciona la configuración del dispositivo que se va a usar para representar un trabajo o un documento, esa configuración se guarda normalmente, junto con el trabajo o documento, en forma de un PrintTicket. El PrintTicket contiene un conjunto de instancias de opción, normalmente una para cada característica definida en el documento de PrintCapabilities. Las instancias de opción deben ser portátiles y deben conservar el intento de impresión, de modo que la intención se pueda comunicar cuando este PrintTicket se proporcione a un dispositivo diferente, incluso a uno que tenga un documento de PrintCapabilities diferente escrito por otro autor. La principal ventaja de esta portabilidad es que si un dispositivo diferente no admite específicamente una opción incluida en el PrintTicket, el controlador de dispositivo o el subsistema puede identificar y seleccionar la opción que sea la más cercana.

Una de las funciones principales de PrintTicket del controlador es identificar la opción de dispositivo en el documento de PrintCapabilities que más se aproxime a una opción determinada incluida en el PrintTicket. Durante este proceso de puntuación definido por el controlador de dispositivo, se hace referencia a la opción del PrintTicket como opción de *referencia* , mientras que la opción del documento de PrintCapabilities se conoce como la opción *candidato* . La métrica de coincidencia general es el número de instancias de ScoredProperty coincidentes en las instancias de opción candidata y de referencia; un mayor número de coincidencias suele indicar una mejor conservación de la intención de impresión. En el proceso de puntuación, puede elegir dar mayor peso a algunos elementos ScoredProperty que a otros.

Puede crear instancias de opciones portables asegurándose de que todas las instancias de opción que pertenecen a la misma característica tienen uno o más *elementos ScoredProperty en común*. Esto significa que hay un conjunto de elementos ScoredProperty que aparece en cada instancia de opción (que pertenece a la misma característica). Por ejemplo, las instancias de opción de la característica PageMediaSize pueden ser portátiles si cada instancia de opción contiene elementos ScoredProperty que definen las propiedades intrínsecas de PageMediaSize: MediaSizeWidth y MediaSizeHeight. A continuación, el código de controlador de dispositivo o subsistema puede determinar el grado de aceptación de dos instancias de opción comparando las diferencias en estos valores de ScoredProperty. Si no hay ninguna opción en el documento de PrintCapabilities que coincida exactamente con la del PrintTicket, el controlador de dispositivo puede determinar fácilmente y seleccionar la opción que tiene las dimensiones de medios que coinciden más.

En este caso, se dice que dos objetos (instancias de opción) tienen *elementos en común*, o equivalentes, que tienen *elementos correspondientes*, si se cumplen las tres condiciones siguientes.

1.  Los dos elementos son del mismo tipo de elemento.

2.  Los atributos de nombre de los dos elementos son idénticos (o ningún elemento contiene un atributo name).

3.  La cadena de elementos primarios de los elementos que se van a comparar, hasta los dos objetos en cuestión, debe cumplir las condiciones 1 y 2.

Por ejemplo, considere una situación en la que hay dos instancias de opción, donde cada una contiene una instancia de ScoredProperty y que cada una de estas instancias de ScoredProperty contiene una instancia de propiedad. Claramente, se cumple la primera condición (las dos instancias de propiedad son del mismo tipo) y se cumple parte de la tercera condición (los elementos primarios de las instancias de propiedad son del mismo tipo, ScoredProperty, y los elementos primarios de esos elementos son las instancias de opción, que también son del mismo tipo). Si los atributos de nombre de, respectivamente, las instancias de propiedad, las instancias de ScoredProperty y las instancias de opción son idénticas o no se suministran, las dos instancias de opción tienen elementos en común.

Desde lo anterior, el primer paso en la creación de instancias de opción es definir un conjunto de elementos ScoredProperty presentes en la mayoría o en todas las instancias de opción. Si el atributo de configuración del dispositivo se puede representar mediante una característica estándar (una que aparece en las palabras clave del esquema de impresión), tenga en cuenta los elementos de ScoredProperty en común en las instancias de la opción estándar. Debe asegurarse de que todas las instancias de opciones nuevas que introduzca también contengan estos elementos ScoredProperty. Siempre puede agregar elementos ScoredProperty adicionales según sea necesario para diferenciar las instancias de opción de las instancias de opción estándar. Incluso puede eliminar uno o varios de los elementos de ScoredProperty en común si hay una buena razón, aunque esto reduce la portabilidad de dicha opción. Por supuesto, las consideraciones de portabilidad sugieren el uso de las instancias de la opción estándar sin modificar, a menos que haya una diferencia intrínseca entre su opción y la instancia de la opción estándar que se debe reflejar en la nueva instancia de la opción.

En el ejemplo siguiente se muestra una situación en la que podría querer agregar un elemento ScoredProperty a una instancia de la opción. Todas las instancias de opción estándar de la característica PageMediaSize tienen los elementos ScoredProperty y MediaSizeHeight en común. Supongamos que el dispositivo puede admitir uno de los tamaños de medio de la letra estándar alimentando el papel de forma inversa (LongEdgeFirst) o longitudinalmente (ShortEdgeFirst). Suponiendo que no desea incluir una nueva característica de dirección de fuente para exponer este grado de libertad, puede modificar en su lugar las dos instancias de la opción PageMediaSize para que Letter incorpore la orientación del avance de papel. Para estas dos instancias de opción de dos letras, empiece con la instancia de la opción PageMediaSize estándar y agregue un nuevo elemento ScoredProperty para representar FeedDirection. En una instancia de opción, establezca FeedDirection ScoredProperty en LongEdgeFirst; en la otra instancia de la opción, establezca FeedDirection en ShortEdgeFirst. Tenga en cuenta que estas nuevas instancias de opción mantienen su portabilidad. Si la opción que representa la letra, ShortEdgeFirst se guarda en un PrintTicket y se selecciona un dispositivo diferente que admite solo la opción de carta estándar para representar el trabajo, el código de coincidencia de opciones puede determinar rápidamente que la letra de opción estándar es la mejor coincidencia con la letra de opción, ShortEdgeFirst. La razón por la que esta es la mejor coincidencia es que todas las instancias de ScoredProperty coinciden, con la excepción de FeedDirection ScoredProperty, que no existe en la opción Letter Standard.

También puede encontrarse con casos en los que las modificaciones de la opción realmente cambian el significado, de modo que la opción modificada ya no se puede considerar como un caso especializado del original. En tales casos, debe cambiar el nombre de la opción para que refleje la diferencia entre la instancia de la opción modificada y la no modificada. Solo el autor del documento de PrintCapabilities para un dispositivo determinado puede decidir si la opción ofrecida por el dispositivo es lo suficientemente distinta de una instancia de opción estándar para garantizar una definición incompatible.

Ahora considere el caso en el que el dispositivo tiene un atributo de configuración de dispositivo que no se corresponde con ninguna de las instancias de características estándar. En este caso, no se puede confiar en las instancias de opción estándar para proporcionar la lista de elementos ScoredProperty en común. Al crear una instancia de ScoredProperty, el objetivo principal es diferenciar cada opción de las demás de la característica y describir por qué un usuario seleccionaría una opción sobre otra. La línea de base consiste en caracterizar cada opción con un atributo de nombre único y el ScoredProperty que contiene el atributo de nombre se convierte en el que se usa para determinar los elementos en común.

Una vez establecido un conjunto de elementos ScoredProperty en común, es muy sencillo asignar los valores adecuados a cada ScoredProperty para crear cada opción. Como en el ejemplo anterior, para determinadas instancias de opción, puede que necesite agregar instancias de ScoredProperty adicionales o eliminar algunos de los elementos en común para crear una instancia de opción adecuada.

Se debe observar que el esquema de impresión requiere que el conjunto de instancias de ScoredProperty, sus ubicaciones y los valores asignados a cada ScoredProperty en una opción permanezcan constantes, independientemente de la configuración. Todo el concepto de esquema de impresión se basa en instancias de opción que tienen instancias fijas, de propiedades identificables y de ScoredProperty que se comparten entre varios dispositivos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



