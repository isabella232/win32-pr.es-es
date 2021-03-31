---
title: Implementaciones de conjuntos de propiedades en COM
description: Implementaciones de conjuntos de propiedades en COM
ms.assetid: 52d7b534-f81a-4cc9-b5ea-9538bfff056c
keywords:
- Almacenamiento estructurado Strctd STG, usar, conjunto de propiedades en COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8ee68fcd36958e0b7b0648e40f6e3c480f31d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995357"
---
# <a name="property-set-implementations-in-com"></a>Implementaciones de conjuntos de propiedades en COM

Aunque la posibilidad de usar conjuntos de propiedades persistentes no se ha aprovechado por completo, actualmente hay dos usos principales:

-   Almacenar información de resumen con un objeto como un documento
-   Transferir datos de propiedad entre objetos

Los conjuntos de propiedades COM se diseñaron para almacenar datos que son adecuados para su representación como una colección de tamaño moderado de valores específicos. Los conjuntos de datos que son demasiado grandes para que esto sea factible deben dividirse en flujos independientes, almacenamientos o conjuntos de propiedades. El formato de datos del conjunto de propiedades COM no se ha diseñado para proporcionar un sustituto para una base de datos de muchos objetos diminutos.

COM proporciona implementaciones de las interfaces de conjunto de propiedades para varios objetos, junto con tres funciones auxiliares. En la siguiente sección se describen algunas características de rendimiento de estas implementaciones. Para obtener más información sobre interfaces específicas y cómo obtener un puntero a estas interfaces, consulte lo siguiente en la sección de referencia de COM:

-   [IPropertySetStorage: implementación de archivo compuesto](ipropertysetstorage-compound-file-implementation.md)

    La implementación de archivos compuestos, que proporciona las interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) y [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) , también proporciona las interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) y [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . Dada una implementación de archivo compuesto de **IStorage**, la interfaz **IPropertySetStorage** se puede obtener llamando a [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

-   [IPropertySetStorage: implementación del sistema de archivos NTFS](ipropertysetstorage-ntfs-file-system-implementation.md)

    También se pueden obtener las interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) y [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) para los archivos NTFS que no son archivos compuestos. Por lo tanto, es posible obtener estas interfaces para todos los archivos de un volumen NTFS.

-   [IPropertySetStorage: implementación independiente](ipropertysetstorage-stand-alone-implementation.md)

    Cuando se crea una instancia de esta implementación de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) y [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , se le proporciona un puntero a un objeto que admite la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Después, manipula los almacenamientos del conjunto de propiedades dentro de ese objeto de almacenamiento. Por lo tanto, es posible tener acceso a los conjuntos de propiedades y manipularlos en cualquier objeto que admita.

-   [Consideraciones de implementación de IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)

    Hay varios problemas que se deben tener en cuenta a la hora de proporcionar una implementación de la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) . Consulte estas consideraciones de *implementación* en la sección de referencia com.

Además, hay cuatro funciones auxiliares, diseñadas para ayudar a trabajar con propiedades que se han leído de una propiedad establecida en la memoria (en una estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) ):

-   [**PropVariantInit**](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [**PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [**FreePropVariantArray**](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [**PropVariantCopy**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)

En las secciones siguientes se describen las implementaciones de conjuntos de propiedades en COM con mayor detalle:

-   [Administrar conjuntos de propiedades](managing-property-sets.md)
-   [Consideraciones sobre los conjuntos de propiedades](property-set-considerations.md)
-   [Almacenar conjuntos de propiedades](storing-property-sets.md)
-   [Características de rendimiento](performance-characteristics.md)
-   [Implementar el conjunto de propiedades de información de Resumen](implementing-the-summary-information-property-set.md)
-   [Consideraciones de implementación de IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)

 

 