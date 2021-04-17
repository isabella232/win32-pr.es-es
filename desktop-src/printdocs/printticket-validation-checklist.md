---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 4698f151-2237-4d16-b32f-4d15024cd063
title: Lista de comprobación de validación de PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a0e9f3eb71b1e9a3b670456e04e2efa3c8b15
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717418"
---
# <a name="printticket-validation-checklist"></a>Lista de comprobación de validación de PrintTicket

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Los proveedores de PrintTicket deben validar el objeto PrintTicket antes de usarlo con cualquier fin. Una vez validado el PrintTicket, se puede devolver al cliente o se puede descartar después del uso. Esta lista de comprobación cubre las tareas que el proveedor debe realizar durante la validación. El proceso de validación modificará con frecuencia el contenido del PrintTicket, aunque no modificará un PrintTicket validado previamente.

La validación siempre se realiza en un dispositivo específico que tiene un conjunto de instancias de Feature, Option y ParameterDef definidas en un documento de PrintCapabilities. El código de validación debe tener acceso al conjunto de instancias de características (y a las instancias de las opciones contenidas) e instancias de ParameterDef para el dispositivo específico, y no debe tener acceso a la PrintCapabilities. La información de las instancias de Feature, Option y ParameterDef es necesaria en determinadas partes del proceso de validación.

1.  Durante los intentos de buscar elementos correspondientes o coincidentes, tenga en cuenta que los espacios de nombres de los elementos deben coincidir antes de que cualquier nombre completo pueda considerarse una coincidencia. Todos los nombres de elemento, nombres de atributo y nombres de instancia están calificados con el espacio de nombres. En el caso de los elementos que están anidados, sus ubicaciones deben coincidir antes de que los elementos se consideren una coincidencia.

2.  Compruebe que todas las etiquetas de elemento están en el espacio de nombres público, que están definidas por el esquema PrintTicket, contienen los atributos XML y los valores de atributo adecuados, y que la ubicación de cada tipo de elemento cumple el uso definido por el esquema PrintTicket.

3.  Determinar todos los espacios de nombres informados por el documento de PrintCapabilities. Quite todos los elementos (y sus descendientes) del PrintTicket cuyos nombres de instancia pertenezcan a los espacios de nombres no comunicados por el documento de PrintCapabilities. Observe la diferencia entre este caso y el siguiente, que incluye nombres de instancia no reconocidos dentro de un espacio de nombres conocido.

4.  Debido al hecho de que los esquemas se amplían continuamente con la adición de nuevas definiciones de instancia de elemento, el código de validación no debe escribirse bajo la suposición de que se conoce cada nombre de instancia en un espacio de nombres determinado. El código de validación no puede tratar nombres de instancia no reconocidos en un espacio de nombres conocido como errores, ni puede eliminarlos del PrintTicket.

5.  Si alguna instancia de elemento tiene un elemento relacionado duplicado no permitido por el esquema PrintTicket, mantenga solo la primera aparición y elimine los duplicados, incluido el contenido del elemento duplicado.

6.  Quite de la característica o subcaracterística de PrintTicket (y de todos sus elementos secundarios) que no tenga ninguna característica correspondiente en el documento de PrintCapabilities.

7.  Compruebe la propiedad SelectionType definida en el documento PrintCapabilities para cada una de las instancias de características restantes en PrintTicket. Cualquier característica cuya propiedad SelectionType esté establecida en PickOne debe tener exactamente una instancia de opción presente en el PrintTicket, mientras que una característica cuya propiedad SelectionType es PickMany puede tener más de una. Si una característica de PrintTicket no tiene ninguna instancia de opción, proporcione la instancia de la opción predeterminada. Como es el proveedor, sabe qué opción es la opción predeterminada para cada característica.

    En el caso de una característica cuya propiedad SelectionType es PickMany, con más de una opción seleccionada en el PrintTicket, compruebe que ninguna opción está designada como IdentityOption. En caso de que haya, elimine todas las demás opciones, y solo la IdentityOption designada.

8.  Quite cualquier instancia de ParameterInit del PrintTicket que no tenga ninguna instancia de ParameterDef correspondiente en el documento de PrintCapabilities.

    Para cualquier otra instancia de ParameterInit del PrintTicket, compruebe que el valor de cada se ajusta a la instancia de ParameterDef del documento PrintCapabilities. Si falta un valor, proporcione el valor predeterminado que se proporciona en ParameterDef.

9.  Empareje cada instancia de opción en el PrintTicket con una opción que se muestra en la característica correspondiente del documento de PrintCapabilities, en función de los resultados del proceso de puntuación. La puntuación es el proceso de encontrar la opción en el documento de PrintCapabilities que mejor coincida con la opción indicada en el PrintTicket. Para obtener una descripción de lo que se tiene en cuenta durante el proceso de puntuación, vea [definiciones de opciones](option-definitions.md). Reemplace cada opción de referencia en el PrintTicket por la opción correspondiente del documento de PrintCapabilities de candidato mejor coincidente. También puede clasificar todos los candidatos por puntuación y pasar esta información a la fase de resolución en caso de que se produzca un conflicto de restricción que evite que se utilice el mejor candidato coincidente. En tales casos, el proceso de resolución puede usar el segundo candidato mejor en lugar de elegir otro candidato de forma aleatoria.

10. En el caso de una característica cuya propiedad SelectionType esté establecida en PickMany y que tenga más de una opción seleccionada en el PrintTicket, compruebe que ninguna opción está designada como IdentityOption. Si existe una opción de este tipo, elimine todas las demás opciones, dejándoa solo la IdentityOption designada. Este paso debe realizarse antes y después de aplicar el proceso de puntuación.

    La razón por la que este paso debe realizarse dos veces es que es posible que el proceso de puntuación asigne varias instancias de opción de referencia a la misma opción candidata. Si esto ocurre, elimine las instancias de opción duplicadas para que las opciones enumeradas para una determinada característica de PickMany sean únicas.

11. Agregue al PrintTicket cualquier característica presente en el documento de PrintCapabilities que no aparezca en el PrintTicket. Para esta característica, designe la opción predeterminada como la opción seleccionada.

12. Determine si hay instancias de ParameterDef que cumplan todos los criterios siguientes:

    -   La instancia de ParameterDef aparece en el documento de PrintCapabilities, pero no en el PrintTicket.

    -   La propiedad obligatoria de la instancia de ParameterDef se establece en incondicional o en condicional.

    -   Se hace referencia a la instancia de ParameterDef mediante una instancia de ParameterRef en el PrintTicket dentro de una instancia de la opción.

    Para cada instancia de ParameterDef del documento PrintCapabilities, agregue al PrintTicket una instancia ParameterInit correspondiente. Establezca el valor de las instancias de ParameterInit recién agregadas en el valor predeterminado especificado por las instancias de ParameterDef correspondientes.

13. Realice la detección de conflictos de restricciones y modifique la configuración para eliminar estos conflictos. En este tema no se define un proceso concreto que se utiliza para resolver conflictos de restricción. Debe decidir qué característica o instancia de ParameterInit se puede cambiar y una opción o valor adecuado, respectivamente, para seleccionar que tenga el menor impacto en el intento general de la configuración especificada en el PrintTicket. Como se mencionó anteriormente, puede que desee usar la puntuación de asignación de cada opción y usar la opción con la segunda puntuación más alta. Para determinar qué característica o ParameterInit cambiar, puede que desee definir una propiedad privada que el cliente pueda agregar al PrintTicket. Esta propiedad puede definir una prioridad para las instancias de Feature y ParameterInit, de modo que el proceso de resolución esté informado de qué instancias de características o ParameterInit son importantes para el cliente (y deben conservarse en el PrintTicket) y cuáles son menos importantes.

14. Si el proceso de resolución de restricciones ha provocado cambios en el PrintTicket en cualquier instancia de ParameterRef para la que la propiedad Mandatory esté establecida en Conditional, agregue instancias de ParameterInit con valores predeterminados para los que ahora aparecen y quite cualquier instancia de ParameterInit para una instancia de ParameterRef que ya no aparezca.

15. Quite todas las instancias de propiedad y su contenido que aparecen dentro de las instancias de opción en el PrintTicket. Los elementos de propiedad no tienen ningún rol en el PrintTicket. Si la opción validada para una característica determinada coincide perfectamente con la opción prevalidada, transfiera todas las instancias de propiedad de esa opción desde el PrintTicket de prevalidación al PrintTicket validado ahora, en función de la condición en la que se registran los espacios de nombres de las instancias de propiedad en el documento de PrintCapabilities. Tenga en cuenta que para que dos instancias de opciones se consideren una coincidencia perfecta, para cada ScoredProperty que se encuentre en una opción, debe haber un ScoredProperty correspondiente en la otra opción y los valores de ambas instancias de ScoredProperty deben ser iguales.

16. Si el proveedor de PrintTicket reconoce y admite cualquier instancia de propiedad pública o privada que haya sobrevivido a este punto, realice la validación en ellos. No elimine una propiedad en este momento, ya que no la reconoce, podría estar pensada para otra fase de procesamiento de documentos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



