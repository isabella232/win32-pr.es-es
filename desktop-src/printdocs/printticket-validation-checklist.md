---
description: Revise la lista de comprobación de validación de PrintTicket. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 4698f151-2237-4d16-b32f-4d15024cd063
title: Lista de comprobación de validación de PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6154b7cabb5825a0f0edcc8f90b8294557001f1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570553"
---
# <a name="printticket-validation-checklist"></a>Lista de comprobación de validación de PrintTicket

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Los proveedores de PrintTicket deben validar PrintTicket antes de usarlo para cualquier propósito. Una vez validado PrintTicket, se puede devolver al cliente o se puede descartar después de su uso. Esta lista de comprobación cubre las tareas que el proveedor debe realizar durante la validación. El proceso de validación modificará con frecuencia el contenido de PrintTicket, aunque no modificará un PrintTicket validado previamente.

La validación siempre se realiza en un dispositivo específico que tiene un conjunto de instancias de Feature, Option y ParameterDef definidas en un documento PrintCapabilities. El código de validación debe tener acceso al conjunto de instancias de características (y a las instancias de Option contenidas) y ParameterDef para el dispositivo específico, y no debe tener acceso a PrintCapabilities. La información de las instancias Feature, Option y ParameterDef es necesaria en determinadas partes del proceso de validación.

1.  Durante los intentos de buscar elementos correspondientes o correspondientes, tenga en cuenta que los espacios de nombres de los elementos deben coincidir antes de que cualquier nombre calificado se pueda considerar una coincidencia. Todos los nombres de elemento, los nombres de atributo y los nombres de instancia están calificados por el espacio de nombres. Para los elementos anidados, sus ubicaciones deben coincidir antes de que los elementos se consideren una coincidencia.

2.  Compruebe que todas las etiquetas de elemento están en el espacio de nombres público, están definidas por el esquema PrintTicket, contienen los atributos XML y los valores de atributo adecuados, y que la ubicación de cada tipo de elemento se ajusta al uso definido por el esquema PrintTicket.

3.  Determine todos los espacios de nombres notificados por el documento PrintCapabilities. Quite todos los elementos (y sus descendientes) de PrintTicket cuyos nombres de instancia pertenecen a espacios de nombres no notificados por el documento PrintCapabilities. Tenga en cuenta la diferencia entre este caso y el siguiente, que implica nombres de instancia no reconocidos dentro de un espacio de nombres conocido.

4.  Debido al hecho de que los esquemas se extienden continuamente con la adición de nuevas definiciones de instancia de elemento, el código de validación no debe escribirse bajo la suposición de que se conoce cada nombre de instancia de un espacio de nombres determinado. El código de validación no puede tratar los nombres de instancia no reconocidos dentro de un espacio de nombres conocido como errores, ni puede eliminarlos de PrintTicket.

5.  Si alguna instancia de elemento tiene un elemento relacionado duplicado que no está permitido por el esquema PrintTicket, mantenga solo la primera aparición y elimine los duplicados, incluido el contenido del elemento duplicado.

6.  Quite de PrintTicket cualquier característica o subfeature (y todos sus elementos secundarios) que no tenga ninguna característica correspondiente en el documento PrintCapabilities.

7.  Compruebe la propiedad SelectionType definida en el documento PrintCapabilities para cada una de las instancias de Feature restantes en PrintTicket. Cualquier característica cuya propiedad SelectionType esté establecida en PickOne debe tener exactamente una instancia de Option presente en PrintTicket, mientras que una característica cuya propiedad SelectionType sea PickMany puede tener más de una. Si una característica PrintTicket no tiene ninguna instancia de Option, proporcione la instancia predeterminada de Option. Puesto que es el proveedor, sabe qué opción es la opción predeterminada para cada característica.

    Para una característica cuya propiedad SelectionType es PickMany, con más de una opción seleccionada en PrintTicket, compruebe que no se designa ninguna opción como IdentityOption. Si lo hay, elimine todas las demás opciones, dejando solo la opción IdentityOption designada.

8.  Quite cualquier instancia parameterInit del objeto PrintTicket que no tenga ninguna instancia de ParameterDef correspondiente en el documento PrintCapabilities.

    Para cualquier otra instancia de ParameterInit en PrintTicket, compruebe que value for each se ajusta a la instancia ParameterDef del documento PrintCapabilities. Si falta un valor, proporcione el valor predeterminado que se proporciona en ParameterDef.

9.  Empareje cada instancia de Option en PrintTicket con una opción enumerada en la característica correspondiente del documento PrintCapabilities, en función de los resultados del proceso de puntuación. La puntuación es el proceso de buscar la opción en el documento PrintCapabilities que mejor coincida con la opción denominada en PrintTicket. Para obtener una descripción de lo que se tiene en cuenta durante el proceso de puntuación, vea [Definiciones de opciones](option-definitions.md). Reemplace cada opción de referencia de PrintTicket por la opción de documento PrintCapabilities candidata correspondiente. También puede clasificar todos los candidatos por puntuación y pasar esta información a la fase de resolución en caso de que un conflicto de restricción impida que se utilice el mejor candidato de coincidencia. En tales casos, el proceso de resolución puede usar el segundo mejor candidato en lugar de elegir otro candidato de forma aleatoria.

10. Para una característica cuya propiedad SelectionType esté establecida en PickMany y que tenga más de una opción seleccionada en PrintTicket, compruebe que no se designe ninguna opción como IdentityOption. Si existe esta opción, elimine todas las demás opciones, dejando solo la opción IdentityOption designada. Este paso debe realizarse antes y después de aplicar el proceso de puntuación.

    La razón por la que este paso debe realizarse dos veces es que es posible que el proceso de puntuación asigne varias instancias de opción de referencia a la misma opción candidata. Si esto sucede, elimine las instancias de Option duplicadas para que las opciones enumeradas para una característica PickMany determinada sean únicas.

11. Agregue a PrintTicket cualquier característica presente en el documento PrintCapabilities que no aparezca en PrintTicket. Para este tipo de característica, designe la opción predeterminada como opción seleccionada.

12. Determine si hay alguna instancia de ParameterDef que cumpla todos los criterios siguientes:

    -   La instancia de ParameterDef aparece en el documento PrintCapabilities, pero no en PrintTicket.

    -   La propiedad Mandatory de la instancia parameterDef se establece en Incondicional o Condicional.

    -   Una instancia de ParameterRef hace referencia a la instancia de ParameterDef en PrintTicket dentro de una instancia de Option.

    Para cada instancia de ParameterDef del documento PrintCapabilities, agregue a PrintTicket una instancia de ParameterInit correspondiente. Establezca el valor de las instancias de ParameterInit recién agregadas en el valor predeterminado especificado por las instancias de ParameterDef correspondientes.

13. Realice la detección de conflictos de restricción y modifique la configuración para eliminar dichos conflictos. En este tema no se define un proceso determinado que se usará para resolver conflictos de restricción. Debe decidir qué instancia de Feature o ParameterInit se puede cambiar y una opción o valor adecuada, respectivamente, para seleccionar que tenga el menor impacto en la intención general de la configuración especificada en PrintTicket. Como se mencionó anteriormente, es posible que quiera usar la puntuación de asignación de cada opción y usar la opción con la segunda puntuación más alta. Para determinar qué Característica o ParameterInit se va a cambiar, es posible que desee definir una propiedad privada que el cliente puede agregar a PrintTicket. Esta propiedad puede definir una prioridad para las instancias Feature y ParameterInit para que se informe al proceso de resolución de qué instancias de Feature o ParameterInit son importantes para el cliente (y deben conservarse en PrintTicket) y cuáles son menos importantes.

14. Si el proceso de resolución de restricciones ha provocado cambios en PrintTicket en cualquier instancia parameterRef para la que la propiedad Mandatory esté establecida en Condicional, agregue instancias ParameterInit con valores predeterminados para las que aparecen ahora y quite cualquier instancia ParameterInit de una instancia parameterRef que ya no aparezca.

15. Quite todas las instancias de propiedad y su contenido que aparecen dentro de las instancias de Option en PrintTicket. Los elementos property no tienen ningún rol en PrintTicket. Si la opción validada para una característica determinada coincide perfectamente con la opción prevalidada, transfiera todas las instancias de Propiedad de esa opción de la prevalidación PrintTicket al printTicket ahora validado, sujeto a la condición de que los espacios de nombres de las instancias de propiedad estén registrados en el documento PrintCapabilities. Tenga en cuenta que para que dos instancias de Option se consideren una coincidencia perfecta, para cada ScoredProperty que se encuentra en una opción, debe haber una scoredProperty correspondiente en la otra opción y los valores de ambas instancias de ScoredProperty deben ser los mismos.

16. Si el proveedor PrintTicket reconoce y admite cualquier instancia de propiedad pública o privada que haya sobrevivedo hasta este punto, realice la validación en ellas. No elimine una propiedad en este momento solo porque no la reconozca, podría estar pensada para otra fase del procesamiento de documentos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



