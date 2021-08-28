---
title: Propiedades y conjuntos de propiedades
description: Aunque los tipos de propiedades en tiempo de ejecución que ofrecen Automation y Microsoft ActiveX Controls son importantes, no abordan directamente la necesidad de almacenar información con objetos almacenados de forma persistente en el sistema de archivos.
ms.assetid: 350cfb84-2f8e-46e7-a70d-09beb14a8eee
keywords:
- Structured Storage Strctd Stg ,fundamentals,properties and property sets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df2ef4b3e4d91cc908d82b58a0ec0156a60de23208cfd8dde2718fa62eaab60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662265"
---
# <a name="properties-and-property-sets"></a>Propiedades y conjuntos de propiedades

Aunque los tipos de propiedades en tiempo de ejecución que ofrecen Automation y Microsoft ActiveX Controls son importantes, no abordan directamente la necesidad de almacenar información con objetos almacenados de forma persistente en el sistema de archivos. Estas entidades pueden incluir archivos (estructurados, compuestos, etc.), directorios y catálogos de resumen. COM proporciona un formato serializado estándar para estas propiedades persistentes y un conjunto de interfaces y funciones que permiten crear y manipular los conjuntos de propiedades y sus propiedades.

Las propiedades persistentes se almacenan como conjuntos y uno o varios conjuntos pueden estar asociados a una entidad del sistema de archivos. Estos conjuntos de propiedades persistentes están diseñados para usarse para almacenar datos adecuados para representarse como una colección de valores más completos. No están diseñados para usarse como una base de datos grande. Se pueden usar para almacenar información de resumen sobre un objeto en el sistema, al que puede acceder cualquier otro objeto que entienda cómo interpretar ese conjunto de propiedades.

Las versiones anteriores de COM especificaban muy poco con respecto a las propiedades y su uso, pero sí definen un formato serializado que permitía a los desarrolladores almacenar propiedades y conjuntos de propiedades en una instancia [**de IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage) También se definieron los identificadores de propiedad y la semántica de un único conjunto de propiedades, que se usan para obtener información de resumen sobre un documento. En ese momento, era necesario crear y manipular esa estructura directamente como un flujo de datos. Vea [Structured Storage Serialized Property Set Format](structured-storage-serialized-property-set-format.md).

Sin embargo, COM define dos interfaces principales para administrar conjuntos de propiedades:

-   [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
-   [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

Ya no es necesario tratar el formato serializado directamente cuando estas interfaces se implementan en un objeto que admite la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) (por ejemplo, archivos compuestos). Al escribir propiedades [**a través de IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) se crean datos que se ajustan exactamente al formato del conjunto de propiedades COM, como se ve a través de los **métodos IStorage.** Lo contrario también es cierto: las propiedades escritas en el formato de conjunto de propiedades COM mediante **IStorage** son visibles a través de **IPropertySetStorage** e **IPropertyStorage** (aunque no puede esperar escribir en [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) y tener las propiedades a través de **IPropertyStorage** inmediatamente disponibles, o viceversa).

La [**interfaz IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) define métodos que crean y administran conjuntos de propiedades. La [**interfaz IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) manipula directamente las propiedades dentro de un conjunto de propiedades. Al llamar a los métodos de estas interfaces, un desarrollador de aplicaciones puede administrar los conjuntos de propiedades que sean adecuados para una entidad del sistema de archivos determinada. El uso de estas interfaces proporciona una implementación de lectura y escritura ajustada para las propiedades, en lugar de tener una implementación en cada aplicación, donde podría haber cuellos de botella de rendimiento, como búsquedas incesantes. Puede implementar las interfaces para mejorar el rendimiento, de modo que las propiedades se puedan leer y escribir más rápidamente mediante, por ejemplo, un almacenamiento en caché más eficaz. Además, **IPropertyStorage** e **IPropertySetStorage** hacen posible manipular propiedades en entidades que no admiten [**IStorage,**](/windows/desktop/api/Objidl/nn-objidl-istorage)aunque en general, la mayoría de las aplicaciones no lo harán.

Esta sección contiene los siguientes temas:

-   [Conjunto de propiedades Demmary Information](the-summary-information-property-set.md)
-   [Identificadores de formato de conjunto de propiedades predefinidos](predefined-property-set-format-identifiers.md)
-   [Conjuntos de propiedades DocumentSummaryInformation y UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Implementaciones de conjunto de propiedades en COM](property-set-implementations-in-com.md)
</dt> <dt>

[Consideraciones sobre el conjunto de propiedades](property-set-considerations.md)
</dt> <dt>

[Administrar propiedades](managing-properties.md)
</dt> <dt>

[Administración de conjuntos de propiedades](managing-property-sets.md)
</dt> <dt>

[Almacenar conjuntos de propiedades](storing-property-sets.md)
</dt> <dt>

[Características de rendimiento](performance-characteristics.md)
</dt> </dl>

 

 




