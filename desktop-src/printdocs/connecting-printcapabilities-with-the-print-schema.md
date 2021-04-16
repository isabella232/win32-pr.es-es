---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 2f6c51a3-003c-4d68-9e4d-9be5d325a477
title: Conectar PrintCapabilities con el esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d2f5a34421dba2402bce1d6699f208fd58c799
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105678665"
---
# <a name="connecting-printcapabilities-with-the-print-schema"></a>Conectar PrintCapabilities con el esquema de impresión

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El esquema de PrintCapabilities general cubre la estructura, el propósito y el uso de los distintos tipos de elemento. Especifica el atributo de nombre que se usa para definir instancias específicas de cada tipo de elemento. Especifica que los autores de PrintCapabilities pueden usar instancias de elementos definidos por las palabras clave del esquema de impresión o que pueden introducir sus propias instancias definidas de forma privada, siempre que estas instancias definidas de forma privada se definan en un espacio de nombres que se identifique claramente como su propia. (Los autores de PrintCapabilities también pueden usar instancias definidas previamente en otro espacio de nombres privado).

En el documento imprimir palabras clave del esquema se definen las instancias específicas de cada tipo de elemento disponible para su uso en documentos de PrintCapabilities y en elementos PrintTicket. También documenta su finalidad y uso. El documento imprimir palabras clave del esquema también define instancias de varios tipos de elemento, como se indica a continuación:

-   Instancias de propiedad y subpropiedad que residen en la raíz del documento de PrintCapabilities

    -   Estos elementos describen los distintos aspectos y capacidades del dispositivo, y proporcionan un vocabulario común para la descripción de los dispositivos.

-   Instancias de propiedades y subpropiedades que son elementos secundarios de elementos de característica

    -   Estos elementos describen diversos aspectos relacionados con una característica específica.

-   Instancias de propiedad y subpropiedad que son elementos secundarios de elementos de opción

    -   Estos elementos describen los distintos aspectos y capacidades del dispositivo que dependen de la opción seleccionada para una característica específica. Estos podrían reemplazarse por instancias de propiedad ubicadas en la raíz del documento de PrintCapabilities, pero ofrecen más comodidad en algunos casos. Para obtener más información, vea [Agregar instancias de propiedad](adding-property-instances.md).

<!-- -->

-   Instancias de ScoredProperty

    -   Las instancias de ScoredProperty definen el lenguaje que se usa para caracterizar una opción. Las instancias de ScoredProperty definidas en las palabras clave del esquema de impresión permiten que las instancias de opciones escritas por muchas partes diferentes para muchos dispositivos sean portátiles y que sean entendidas por cualquier otro controlador de dispositivo, PrintCapabilities o proveedor de PrintTicket.

-   Instancias de valor ScoredProperty

    -   Estas instancias de valor se proporcionan por la misma razón que se proporcionan las instancias de ScoredProperty.

-   Instancias de características

    -   Cada opción debe pertenecer a una característica específica, lo que requiere que se defina la propia característica.

-   Instancias de ParameterDef

    -   Una instancia de ParameterDef proporcionada por palabras clave del esquema de impresión también define un valor para cada propiedad que contiene. El proveedor de PrintCapabilities es libre de modificar las instancias de valor de las instancias de propiedad que se pueden cambiar. Para obtener información sobre qué instancias de propiedad se pueden cambiar y cuáles no se pueden cambiar (son inmutables), vea [elementos ParameterDef y ParameterInit](parameterdef-and-parameterinit-elements.md).

Es importante tener en cuenta que el esquema de PrintCapabilities no denomina ninguna instancia de opción. Las instancias de opción se caracterizan únicamente por sus instancias de ScoredProperty tomadas en conjunto. Una idea equivocada habitual es que el uso del atributo ' name ' para definir una opción identifica las instancias de opción, pero esto es incorrecto. Los elementos de opción no deben ser únicos para las instancias de opción del mismo nivel, ni tampoco usar el atributo ' name ' para definir una opción necesaria.

En el documento imprimir palabras clave del esquema se define un espacio de nombres estándar al que pertenecen todos los atributos de nombre de instancia en los esquemas de PrintCapabilities y PrintTicket. Todas las etiquetas de tipo de elemento y los atributos XML que usan los tipos de elemento también pertenecen a este espacio de nombres.

Para cada instancia definida en el esquema de PrintCapabilities, el esquema de PrintCapabilities especifica tanto el atributo de nombre como la ubicación de la instancia. El proveedor y el cliente deben conservar ambos al usar esta instancia en su documento PrintCapabilities o PrintTicket.

El documento imprimir palabras clave del esquema designa algunas instancias como obligatorias. Estas instancias deben aparecer en cada documento de PrintCapabilities y deben inicializarse correctamente con valores válidos. Todas las instancias de las palabras clave del esquema de impresión que no están designadas como obligatorias son opcionales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



