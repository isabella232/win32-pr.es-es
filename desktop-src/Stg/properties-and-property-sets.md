---
title: Propiedades y conjuntos de propiedades
description: Aunque los tipos de propiedades de tiempo de ejecución que ofrecen Automation y los controles ActiveX de Microsoft son importantes, no solucionan directamente la necesidad de almacenar información con objetos almacenados de forma persistente en el sistema de archivos.
ms.assetid: 350cfb84-2f8e-46e7-a70d-09beb14a8eee
keywords:
- Almacenamiento estructurado Strctd STG, aspectos básicos, propiedades y conjuntos de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fdafcbef0e92479aa628ab119b6d961abb74d82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419194"
---
# <a name="properties-and-property-sets"></a>Propiedades y conjuntos de propiedades

Aunque los tipos de propiedades de tiempo de ejecución que ofrecen Automation y los controles ActiveX de Microsoft son importantes, no solucionan directamente la necesidad de almacenar información con objetos almacenados de forma persistente en el sistema de archivos. Estas entidades podrían incluir archivos (estructurados, compuestos, etc.), directorios y catálogos de resumen. COM proporciona tanto un formato serializado estándar para estas propiedades persistentes como un conjunto de interfaces y funciones que permiten crear y manipular los conjuntos de propiedades y sus propiedades.

Las propiedades persistentes se almacenan como conjuntos y uno o más conjuntos pueden estar asociados a una entidad del sistema de archivos. Estos conjuntos de propiedades persistentes están diseñados para almacenar datos que se pueden representar como una colección de valores específicos. No están diseñados para usarse como base de datos de gran tamaño. Se pueden usar para almacenar información de resumen sobre un objeto en el sistema, al que puede tener acceso cualquier otro objeto que entienda cómo interpretar ese conjunto de propiedades.

En las versiones anteriores de COM se especificaba muy poco con respecto a las propiedades y su uso, pero se definió un formato serializado que permitía a los desarrolladores almacenar propiedades y conjuntos de propiedades en una instancia de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . También se definieron los identificadores de propiedad y la semántica de un único conjunto de propiedades, que se usa para obtener información de resumen sobre un documento. En ese momento, era necesario crear y manipular directamente esa estructura como un flujo de datos. Consulte [formato del conjunto de propiedades serializado de almacenamiento estructurado](structured-storage-serialized-property-set-format.md).

Sin embargo, ahora COM define dos interfaces principales para administrar los conjuntos de propiedades:

-   [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
-   [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

Ya no es necesario tratar el formato serializado directamente cuando estas interfaces se implementan en un objeto que admite la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) (como archivos compuestos). La escritura de propiedades a través de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) y [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) crea datos que se ajustan exactamente al formato del conjunto de propiedades com, tal como se ve a través de métodos **IStorage** . Lo contrario también es cierto: las propiedades escritas en el formato del conjunto de propiedades COM mediante **IStorage** son visibles a través de **IPropertySetStorage** y **IPropertyStorage** (aunque no se puede esperar escribir en [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) y tener las propiedades a través de **IPropertyStorage** disponibles de inmediato, o viceversa).

La interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) define métodos que crean y administran conjuntos de propiedades. La interfaz [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) manipula directamente las propiedades dentro de un conjunto de propiedades. Al llamar a los métodos de estas interfaces, un desarrollador de aplicaciones puede administrar los conjuntos de propiedades que sean adecuados para una entidad del sistema de archivos determinada. El uso de estas interfaces proporciona una implementación optimizada de lectura y escritura para las propiedades, en lugar de tener una implementación en cada aplicación, donde podría haber cuellos de botella de rendimiento como la búsqueda de incessant. Puede implementar las interfaces para mejorar el rendimiento, por lo que las propiedades se pueden leer y escribir más rápidamente mediante, por ejemplo, un almacenamiento en caché más eficaz. Además, **IPropertyStorage** y **IPropertySetStorage** permiten manipular propiedades en entidades que no admiten [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), aunque en general, la mayoría de las aplicaciones no lo harán.

Esta sección contiene los siguientes temas:

-   [Conjunto de propiedades de información de Resumen](the-summary-information-property-set.md)
-   [Identificadores de formato del conjunto de propiedades predefinido](predefined-property-set-format-identifiers.md)
-   [Los conjuntos de propiedades DocumentSummaryInformation y UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Implementaciones de conjuntos de propiedades en COM](property-set-implementations-in-com.md)
</dt> <dt>

[Consideraciones sobre los conjuntos de propiedades](property-set-considerations.md)
</dt> <dt>

[Administrar propiedades](managing-properties.md)
</dt> <dt>

[Administrar conjuntos de propiedades](managing-property-sets.md)
</dt> <dt>

[Almacenar conjuntos de propiedades](storing-property-sets.md)
</dt> <dt>

[Características de rendimiento](performance-characteristics.md)
</dt> </dl>

 

 




