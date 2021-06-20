---
description: Obtenga información sobre el esquema de PrintCapabilities general, que abarca la estructura, el propósito y el uso de los distintos tipos de elementos.
ms.assetid: 2f6c51a3-003c-4d68-9e4d-9be5d325a477
title: Conexión de PrintCapabilities con el esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661a8eb93c6f788381713c0c6620e8a09a53648f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409648"
---
# <a name="connecting-printcapabilities-with-the-print-schema"></a>Conexión de PrintCapabilities con el esquema de impresión

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El esquema printCapabilities general cubre la estructura, el propósito y el uso de los distintos tipos de elementos. Especifica el atributo name que se usa para definir instancias específicas de cada tipo de elemento. Especifica que los autores de PrintCapabilities pueden usar instancias de elementos definidos por las palabras clave de esquema de impresión, o pueden introducir sus propias instancias definidas de forma privada, siempre y cuando estas instancias definidas de forma privada se definan en un espacio de nombres que se identifique claramente como suyo. (Los autores de PrintCapabilities también pueden usar instancias definidas previamente en otro espacio de nombres privado).

El documento Palabras clave de esquema de impresión define las instancias específicas de cada tipo de elemento disponibles para su uso en documentos PrintCapabilities y en PrintTickets. También documenta su propósito y uso. El documento Palabras clave de esquema de impresión también define instancias de varios tipos de elementos, como se indica a continuación:

-   Instancias de propiedad y subpropiedad que residen en la raíz del documento PrintCapabilities

    -   Estos elementos describen los distintos aspectos y funcionalidades del dispositivo, y proporcionan un vocabulario común para describir los dispositivos.

-   Instancias de propiedad y subpropiedad que son elementos secundarios de elementos Feature

    -   Estos elementos describen varios aspectos relacionados con una característica específica.

-   Instancias de propiedad y subpropiedad que son elementos secundarios de elementos Option

    -   Estos elementos describen los distintos aspectos y funcionalidades del dispositivo que dependen de la opción seleccionada para una característica específica. Estas instancias podrían reemplazarse por instancias de propiedad ubicadas en la raíz del documento PrintCapabilities, pero ofrecen mayor comodidad en algunos casos. Para obtener más información, vea [Adding Property Instances](adding-property-instances.md).

<!-- -->

-   Instancias de ScoredProperty

    -   Las instancias de ScoredProperty definen el idioma que se usa para caracterizar una opción. Las instancias scoredProperty definidas en las palabras clave de esquema de impresión hacen posible que las instancias de option escritas por muchas partes diferentes para muchos dispositivos sean portátiles y que cualquier otro controlador de dispositivo o proveedor PrintCapabilities o PrintTicket puedan entenderlo.

-   Instancias de ScoredProperty Value

    -   Estas instancias value se proporcionan por el mismo motivo por el que se proporcionan las instancias de ScoredProperty.

-   Instancias de características

    -   Cada opción debe pertenecer a una característica específica, lo que requiere que se defina la propia característica.

-   Instancias de ParameterDef

    -   Una instancia de ParameterDef proporcionada por palabras clave de esquema de impresión también define un valor para cada propiedad contenida en ella. El proveedor PrintCapabilities es libre de modificar las instancias value de las instancias de propiedad que se pueden cambiar. Para obtener información sobre qué instancias de propiedad se pueden cambiar y cuáles no se pueden cambiar (son inmutables), vea [Elementos ParameterDef y ParameterInit](parameterdef-and-parameterinit-elements.md).

Es importante tener en cuenta que el esquema PrintCapabilities no asigna un nombre a ninguna instancia de Option. Las instancias de opción se caracterizan únicamente por sus instancias scoredProperty tomadas como un todo. Una idea errónea común es que el uso del atributo "name" para definir una opción identifica instancias de Option, pero esto es incorrecto. No es necesario que los elementos option sean únicos para las instancias de Option del mismo nivel, ni que se use el atributo 'name' para definir una opción necesaria.

El documento Palabras clave de esquema de impresión define un espacio de nombres estándar al que pertenecen todos los atributos de nombre de instancia de los esquemas PrintCapabilities e PrintTicket. Todas las etiquetas de tipo de elemento y los atributos XML utilizados por los tipos de elemento también pertenecen a este espacio de nombres.

Para cada instancia definida en el esquema PrintCapabilities, el esquema PrintCapabilities especifica el atributo name y la ubicación de la instancia. El proveedor y el cliente deben conservar ambos al usar esta instancia en su documento PrintCapabilities o PrintTicket.

El documento Palabras clave de esquema de impresión designa algunas instancias como obligatorias. Estas instancias deben aparecer en cada documento PrintCapabilities y deben inicializarse correctamente con valores válidos. Todas las instancias de las palabras clave de esquema de impresión que no se designan como obligatorias son opcionales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



