---
description: En este artículo se proporciona una lista de comprobación que los autores de documentos PrintCapabilities pueden usar para crear un documento PrintCapabilities que describa un dispositivo.
ms.assetid: 4b8fa1a4-6461-4722-861b-354f206b2a73
title: Lista de comprobación de construcción de documentos PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a5284a480f73151750926d975535ea799457a1ce2cd4c14f197a4fc6519b646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867967"
---
# <a name="printcapabilities-document-construction-checklist"></a>Lista de comprobación de construcción de documentos PrintCapabilities

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El [resumen de tipos de elementos](summary-of-element-types.md) describe los distintos elementos que forma un documento PrintCapabilities. En esta sección se proporciona una lista de comprobación que los autores de documentos PrintCapabilities pueden usar para crear un documento PrintCapabilities que describa un dispositivo.

1.  Identifique todos los atributos de dispositivo que contribuyen a la configuración del dispositivo. Para cada atributo de dispositivo de este tipo, determine si debe representarse como una construcción feature/option o como una construcción de parámetros.

2.  Para cada característica de dispositivo, determine si se puede representar mediante una característica definida en las palabras clave de esquema de impresión. Si no es así, deberá introducir una nueva característica definida de forma privada (y un atributo de nombre correspondiente).

    -   Para las instancias de características definidas por palabras clave de esquema de impresión, identifique cada uno de los estados disponibles en los que se puede establecer esta característica. Cada estado corresponde a una opción de la instancia de característica. Determine cuál de estos estados corresponde a las instancias de opción definidas por el esquema de impresión asociadas a esta característica y qué estados requieren una instancia de opción personalizada. En [el tema Definiciones de](option-definitions.md) opciones se presenta información sobre cómo construir nuevas instancias de Option y cómo derivar nuevas instancias de Option a partir de instancias de Option existentes.

    -   En el caso de las instancias de características no estándar, identifique las características que se pueden usar para distinguir una opción de otra. Represente cada una de estas características mediante un elemento ScoredProperty y, en cada instancia de Option, asigne a cada ScoredProperty un valor específico de esa opción. Asegúrese de que hay suficientes elementos ScoredProperty para que cada opción de una característica determinada sea única. Por su naturaleza, las instancias de característica y opción no estándar son noportables. Es decir, otro controlador no podrá encontrar ninguna característica u opción equivalente para que coincida con una característica o opción no estándar especificada en el PrintTicket que crea el controlador.

3.  Determine si alguna opción debe contener elementos ParameterRef. Para obtener más información, vea [Construcciones de parámetros y](parameter-constructs.md) [Elementos de referencia de parámetros](parameter-reference-elements.md).

4.  Para los parámetros, determine si una de las instancias de ParameterDef definidas en las palabras clave de esquema de impresión es una coincidencia adecuada. Si es así, copie la instancia parameterDef de las palabras clave de esquema de impresión y ajuste el valor de cada instancia de propiedad mutable para el mejor ajuste. Si ninguna de las instancias de ParameterDef de las palabras clave de esquema de impresión es una coincidencia adecuada, cree su propia instancia de ParameterDef. Para obtener más información, [vea Parámetros en el documento PrintCapabilities](parameters-in-the-printcapabilities-document.md).

5.  Asegúrese de que todas las instancias de Property y ScoredProperty requeridas por el documento Print Schema Keywords están presentes en el documento PrintCapabilities y que se inicializan correctamente.

6.  Agregue instancias de propiedad y subpropiedad adicionales según sea necesario. Puede introducir instancias de propiedad definidas de forma privada si hay aspectos del dispositivo que necesita caracterizar que no están cubiertos por las instancias de propiedad definidas en las palabras clave de esquema de impresión.

7.  Observe la Convención de espacio de nombres para los atributos de nombre. Esto se aplica a los atributos de nombre definidos de forma privada, así como a los definidos en las palabras clave de esquema de impresión.

8.  Los elementos secundarios del mismo tipo de elemento no pueden anidar en una profundidad de más de 10 elementos. Esta regla se aplica de forma independiente a cada tipo de elemento que se puede definir.

Tenga en cuenta que el contenido XML del documento Capacidades de impresión debe codificarse mediante UTF-8 o UTF-16.

Tenga en cuenta que el conjunto de instancias de Feature, Option y ParameterDef notificadas no debe cambiar, independientemente de la instantánea. Las instancias de ScoredProperty que son cada instancia de Option y el valor asignado a cada elemento ScoredProperty tampoco deben cambiar. Lo mismo se aplica a las instancias de propiedad que conste de cada instancia de ParameterDef.

Para obtener una lista de instancias de propiedad adicionales que se deben proporcionar para definir completamente las construcciones y los parámetros Feature/Option, vea [ParameterDef](parameterdef.md) y [ParameterInit.](parameterinit.md) Por ejemplo, cada característica debe especificar su comportamiento de interfaz de usuario (UI), en concreto si se pueden seleccionar exactamente una o varias instancias de opción para cada característica a la vez. El documento Palabras clave de esquema de impresión define estas instancias de propiedad, donde deben aparecer en el documento PrintCapabilities y qué instancias de Value definidas en las palabras clave de esquema de impresión están disponibles.

El proveedor PrintCapabilities es responsable de emitir el valor adecuado para todas las instancias de propiedad dependientes de la configuración. Por ejemplo, si la velocidad de impresión depende del modo de color y de la resolución utilizada, el proveedor PrintCapabilities debe tener en cuenta el modo de color y la configuración de resolución especificados en el PrintTicket proporcionado por el cliente y debe notificar el valor adecuado para la velocidad de impresión. Tenga en cuenta que cada instancia de ScoredProperty debe tener un solo valor; su instancia de valor no puede cambiar cuando cambia la configuración del dispositivo.

Tenga en cuenta también que las instancias de propiedad definidas en las palabras clave de esquema de impresión deben aparecer en la ubicación especificada. No pueden aparecer en ubicaciones arbitrarias dentro de un documento PrintCapabilities. Las instancias de propiedad definidas de forma privada pueden aparecer en cualquier lugar, incluso como subpropiedades dentro de las instancias de propiedad definidas por el esquema.

Tenga en cuenta que un conflicto funcional entre la configuración se define como dos elementos de esquema de impresión no conflictivo que tienen una función similar pero son características diferentes. Un ejemplo sería JobDuplexAllDocumentsContiguously y DocumentDuplex; ambos representan la función dúplex del dispositivo, pero difieren en la aplicación de la función, una que se aplica a todo el trabajo de forma contigua y otra a los documentos. En el caso de que se especifiquen dos elementos de este tipo, la prioridad viene determinada por el productor PrintCapabilities y el consumidor PrintTicket. Es responsabilidad del productor PrintCapabilities indicar correctamente las restricciones entre elementos en conflicto a través del atributo "constrained". Los elementos del esquema de impresión público que muestran este conflicto semántico se identifican en su definición.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



