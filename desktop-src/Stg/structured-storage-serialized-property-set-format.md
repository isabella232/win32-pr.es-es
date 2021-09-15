---
title: Formato Storage conjunto de propiedades serializados estructurado
description: Los conjuntos de propiedades persistentes proporcionan una opción para almacenar datos en entidades del sistema de archivos. Se recomienda que, para crearlas y administrarlas, use las interfaces IPropertySetStorage e IPropertyStorage descritas en Propiedades y conjuntos de propiedades.
ms.assetid: f22abe40-535f-4178-9460-59bbe26ff178
keywords:
- Structured Storage Strctd Stg , fundamentals, serialized property set format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea03d5ccab337897be801840080e83a6fa86880
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270628"
---
# <a name="structured-storage-serialized-property-set-format"></a>Formato Storage conjunto de propiedades serializados estructurado

Los conjuntos de propiedades persistentes proporcionan una opción para almacenar datos en entidades del sistema de archivos. Se recomienda que, para crearlas y administrarlas, use las interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) descritas en [Propiedades y conjuntos de propiedades](properties-and-property-sets.md).

Los conjuntos de propiedades se componen de una sección etiquetada de valores, con la sección identificada de forma única por un identificador de formato (FMTID). Cada propiedad consta de un identificador de propiedad y un indicador de tipo que representa un valor. Cada valor almacenado en un conjunto de propiedades tiene un identificador de propiedad único que distingue la propiedad. El indicador de tipo describe la representación de los datos en el valor.

Cuando se usan las [**interfaces IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) no es necesario controlar la estructura de formato del conjunto de propiedades serializadas COM. Para obtener más información, vea los temas enumerados:

Todos los elementos de datos de un conjunto de propiedades se almacenan en la representación de Intel (es decir, en orden de bytes little-endian).

COM define un formato de datos estándar serializado para conjuntos de propiedades. Al controlar el formato serializado, y no con las interfaces, los conjuntos de propiedades tienen las siguientes características:

-   Los conjuntos de propiedades permiten que distintas aplicaciones creen sus propios conjuntos de propiedades independientes para atender a la aplicación.
-   Los conjuntos de propiedades se pueden almacenar en una única [**instancia de IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) o en una [**instancia de IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) que contiene varias secuencias. Los conjuntos de propiedades son simplemente otro tipo de datos que se puede almacenar en muchas formas diferentes de almacenamiento en memoria o en disco. Para obtener más información y las convenciones recomendadas para crear el nombre de cadena para el objeto de almacenamiento, [vea Storage convenciones de nomenclatura de objetos](storage-object-naming-conventions.md).
-   Los conjuntos de propiedades permiten incluir un diccionario de nombres para mostrar que describen el contenido. Se recomienda un conjunto de convenciones para elegir nombres de propiedad. Para obtener más información sobre este diccionario opcional, vea [Reserved Property Identifiers](reserved-property-identifiers.md), including [Property ID 0](/windows/desktop/Stg/reserved-property-identifiers).

La secuencia del conjunto de propiedades se divide en tres partes principales:

-   Encabezado
-   PAR FORMATID/offset
-   Sección que contiene los valores reales del conjunto de propiedades

La longitud total de la secuencia del conjunto de propiedades debe ser menor o igual que 256 K. En las secciones [siguientes,](property-set-header.md)Encabezado del conjunto de propiedades, Identificador de [formato/Par](format-identifier-offset-pair.md)de desplazamiento y Sección [](section.md) (incluidos identificadores de [propiedad/pares](property-identifiers-offset-pairs.md)de desplazamiento), con temas de compatibilidad, se describen los componentes individuales que componen el formato de datos del conjunto de propiedades.

> [!Note]  
> En versiones anteriores de este documento se describen las extensiones de la secuencia del conjunto de propiedades con más de una sección permitida, pero que se ha revisado para proporcionar una sección en el flujo de propiedades. La única excepción son [Los conjuntos de propiedades DocumentSummaryInformation y UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

 

 