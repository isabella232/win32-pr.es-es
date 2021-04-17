---
title: Formato de conjunto de propiedades serializado de almacenamiento estructurado
description: Los conjuntos de propiedades persistentes proporcionan una opción para almacenar los datos dentro de las entidades del sistema de archivos. Se recomienda que, para crearlos y administrarlos, use las interfaces IPropertySetStorage y IPropertyStorage descritas en propiedades y conjuntos de propiedades.
ms.assetid: f22abe40-535f-4178-9460-59bbe26ff178
keywords:
- Strctd de almacenamiento estructurado STG, Fundamentals, formato de conjunto de propiedades serializado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea03d5ccab337897be801840080e83a6fa86880
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665843"
---
# <a name="structured-storage-serialized-property-set-format"></a>Formato de conjunto de propiedades serializado de almacenamiento estructurado

Los conjuntos de propiedades persistentes proporcionan una opción para almacenar los datos dentro de las entidades del sistema de archivos. Se recomienda que, para crearlos y administrarlos, use las interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) y [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) descritas en [propiedades y conjuntos de propiedades](properties-and-property-sets.md).

Los conjuntos de propiedades se componen de una sección etiquetada de valores, con la sección identificada de forma única mediante un identificador de formato (FMTID). Cada propiedad está formada por un identificador de propiedad y un indicador de tipo que representa un valor. Cada valor almacenado en un conjunto de propiedades tiene un identificador de propiedad único que distingue la propiedad. El indicador de tipo describe la representación de los datos en el valor.

Cuando se utilizan las interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) y [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , no es necesario controlar la estructura de formato del conjunto de propiedades serializadas en com. Para obtener más información, vea los temas de la lista:

Todos los elementos de datos dentro de un conjunto de propiedades se almacenan en la representación de Intel (es decir, en un orden de bytes Little-endian).

COM define un formato de datos serializado y estándar para los conjuntos de propiedades. Al controlar el formato serializado, y no con las interfaces, los conjuntos de propiedades tienen las siguientes características:

-   Los conjuntos de propiedades permiten que distintas aplicaciones creen sus propios conjuntos de propiedades independientes para atender a la aplicación.
-   Los conjuntos de propiedades se pueden almacenar en una única instancia de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) o en una instancia de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) que contiene varias secuencias. Los conjuntos de propiedades son simplemente otro tipo de datos que se puede almacenar en muchas formas diferentes de almacenamiento en memoria o en disco. Para obtener más información y las convenciones recomendadas para crear el nombre de cadena para el objeto de almacenamiento, vea [Storage Object naming Conventions](storage-object-naming-conventions.md).
-   Los conjuntos de propiedades permiten incluir un diccionario de nombres para mostrar que describan el contenido. Se recomienda un conjunto de convenciones para elegir los nombres de propiedad. Para obtener más información sobre este diccionario opcional, vea [identificadores de propiedad reservados](reserved-property-identifiers.md), incluido el [identificador de propiedad 0](/windows/desktop/Stg/reserved-property-identifiers).

La secuencia del conjunto de propiedades se divide en tres partes principales:

-   Encabezado
-   Par de hiperdesplazamiento/FORMATID
-   Sección que contiene los valores reales del conjunto de propiedades

La longitud total de la secuencia del conjunto de propiedades debe ser menor o igual que 256 k. En las secciones siguientes, el [encabezado del conjunto de propiedades](property-set-header.md), el par de identificador de [formato/desplazamiento](format-identifier-offset-pair.md)y la [sección](section.md) (incluidos los [pares de identificadores de propiedad y desplazamiento](property-identifiers-offset-pairs.md)), con los temas de soporte, se describen los componentes individuales que componen el formato de datos del conjunto de propiedades.

> [!Note]  
> En las versiones anteriores de este documento se describen las extensiones para la secuencia del conjunto de propiedades con más de una sección permitida, pero que se ha revisado para proporcionar una sección en la secuencia de propiedades. La única excepción son [los conjuntos de propiedades DocumentSummaryInformation y UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

 

 