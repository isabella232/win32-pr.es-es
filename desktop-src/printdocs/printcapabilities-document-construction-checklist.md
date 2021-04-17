---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 4b8fa1a4-6461-4722-861b-354f206b2a73
title: Lista de comprobación de construcción de documentos de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f730a426bb787104e08f879ecccd357fd3102b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105660011"
---
# <a name="printcapabilities-document-construction-checklist"></a>Lista de comprobación de construcción de documentos de PrintCapabilities

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

En el [Resumen de tipos de elementos](summary-of-element-types.md) se describen los distintos elementos que componen un documento de PrintCapabilities. En esta sección se proporciona una lista de comprobación que los autores de documentos de PrintCapabilities pueden utilizar para crear un documento de PrintCapabilities que describa un dispositivo.

1.  Identifique todos los atributos de dispositivo que contribuyan a la configuración del dispositivo. Para cada atributo de dispositivo, determine si se debe representar como una construcción de característica/opción o como una construcción de parámetro.

2.  Para cada característica de dispositivo, determine si se puede representar mediante una característica definida en las palabras clave del esquema de impresión. Si no es así, deberá introducir una nueva característica definida de forma privada (y un atributo name correspondiente).

    -   En el caso de las instancias de características definidas por palabras clave del esquema de impresión, identifique cada uno de los Estados disponibles en los que se puede establecer esta característica. Cada Estado corresponde a una opción de la instancia de la característica. Determine cuál de estos Estados corresponde a las instancias de opciones definidas por el esquema de impresión asociadas a esta característica y qué Estados requieren una instancia de opción personalizada. El tema [definiciones de opciones](option-definitions.md) presenta información sobre cómo construir nuevas instancias de opciones y cómo derivar nuevas instancias de opciones a partir de instancias de opciones existentes.

    -   En el caso de instancias de características no estándar, identifique las características que se pueden usar para distinguir una opción de otra. Representa cada una de estas características mediante un elemento ScoredProperty y, en cada instancia de la opción, asigna cada ScoredProperty un valor que es específico de esa opción. Asegúrese de que hay suficientes elementos ScoredProperty para que cada opción de una característica determinada sea única. Las instancias de característica y de opción no estándar son por su naturaleza no portable. Es decir, otro controlador no podrá encontrar ninguna característica o opción equivalente para que coincida con una característica o opción no estándar especificada en el PrintTicket que crea el controlador.

3.  Determine si cualquier opción debe contener elementos ParameterRef. Para obtener más información, vea [construcciones de parámetros](parameter-constructs.md) y elementos de referencia de [parámetro](parameter-reference-elements.md).

4.  En el caso de los parámetros, determine si una de las instancias de ParameterDef definidas en las palabras clave del esquema de impresión es una coincidencia adecuada. Si es así, copie la instancia de ParameterDef de las palabras clave del esquema de impresión y ajuste el valor de cada instancia de propiedad mutable para obtener el mejor ajuste. Si ninguna de las instancias de ParameterDef de las palabras clave del esquema de impresión es una coincidencia adecuada, cree su propia instancia de ParameterDef. Para obtener más información, vea [parámetros en el documento de PrintCapabilities](parameters-in-the-printcapabilities-document.md).

5.  Asegúrese de que todas las instancias de Property y ScoredProperty requeridas por el documento de palabras clave del esquema de impresión se encuentran en el documento de PrintCapabilities y que se han inicializado correctamente.

6.  Agregue instancias adicionales de propiedades y subpropiedades según sea necesario. Puede introducir instancias de propiedad definidas de forma privada si hay aspectos del dispositivo que debe caracterizar que no están incluidos en las instancias de propiedad definidas en las palabras clave del esquema de impresión.

7.  Observe la Convención de espacio de nombres para los atributos de nombre. Esto se aplica a los atributos de nombre definidos de forma privada, así como a los definidos en las palabras clave del esquema de impresión.

8.  Los elementos secundarios del mismo tipo de elemento no se pueden anidar en una profundidad de más de 10 elementos. Esta regla se aplica de forma independiente a cada tipo de elemento que se puede definir.

Tenga en cuenta que la funcionalidad de impresión documentar el contenido XML debe codificarse con UTF-8 o UTF-16.

Tenga en cuenta que el conjunto de instancias de Feature, Option y ParameterDef indicado no debe cambiar, independientemente de la instantánea. Las instancias de ScoredProperty que componen cada instancia de opción y el valor asignado a cada elemento ScoredProperty tampoco deben cambiar. Lo mismo se aplica a las instancias de propiedad que componen cada instancia de ParameterDef.

Para obtener una lista de instancias de propiedades adicionales que se deben proporcionar para definir completamente construcciones y parámetros de características/opciones, vea [ParameterDef](parameterdef.md) y [ParameterInit](parameterinit.md). Por ejemplo, cada característica debe especificar el comportamiento de la interfaz de usuario (IU), específicamente si se pueden seleccionar exactamente una o varias instancias de opción para cada característica al mismo tiempo. En el documento imprimir palabras clave del esquema se definen estas instancias de propiedad, donde deben aparecer en el documento de PrintCapabilities y las instancias de valor definidas en las palabras clave del esquema de impresión.

El proveedor de PrintCapabilities es responsable de emitir el valor adecuado para todas las instancias de propiedades dependientes de la configuración. Por ejemplo, si la tasa de impresión depende del modo de color y de la resolución utilizada, el proveedor de PrintCapabilities debe anotar el modo de color y la configuración de resolución especificados en el PrintTicket proporcionado por el cliente, y debe notificar el valor adecuado para la tasa de impresión. Tenga en cuenta que cada instancia de ScoredProperty debe tener un valor único; su instancia de valor no puede cambiar cuando cambia la configuración del dispositivo.

Tenga en cuenta también que las instancias de propiedades definidas en las palabras clave del esquema de impresión deben aparecer en la ubicación especificada en ella. No pueden aparecer en ubicaciones arbitrarias dentro de un documento de PrintCapabilities. Las instancias de propiedades definidas de forma privada pueden aparecer en cualquier parte, incluso como subpropiedades dentro de instancias de propiedades definidas por el esquema.

Tenga en cuenta que un conflicto funcional entre las opciones de configuración se define como dos elementos de esquema de impresión no conflictivos que tienen una función similar pero que son características diferentes. Un ejemplo sería JobDuplexAllDocumentsContiguously y DocumentDuplex; Ambos representan la función dúplex del dispositivo, pero difieren en la aplicación de la función, una que se aplica a todo el trabajo de forma contigua y otra a documentos. En el caso de que se especifiquen dos elementos de este tipo, el productor de PrintCapabilities y el consumidor de PrintTicket determinan la prioridad. Es responsabilidad del productor de PrintCapabilities indicar correctamente las restricciones entre los elementos conflictivos mediante el atributo "Constrained". Los elementos del esquema de impresión público que muestran este conflicto semántico se identifican en su definición.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



