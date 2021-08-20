---
title: Implementaciones de conjunto de propiedades en COM
description: Implementaciones de conjunto de propiedades en COM
ms.assetid: 52d7b534-f81a-4cc9-b5ea-9538bfff056c
keywords:
- Structured Storage Strctd Stg ,using,property set uses in COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d582699d398a69a0f24bee18ede362569f529de098fe49310fb93254314b1feb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960734"
---
# <a name="property-set-implementations-in-com"></a>Implementaciones de conjunto de propiedades en COM

Aunque la posibilidad de usos de conjuntos de propiedades persistentes no está totalmente aprovechada, actualmente hay dos usos principales:

-   Almacenamiento de información de resumen con un objeto como un documento
-   Transferencia de datos de propiedad entre objetos

Los conjuntos de propiedades COM se diseñaron para almacenar datos adecuados para la representación como una colección de tamaño moderado de valores más pequeños. Los conjuntos de datos que son demasiado grandes para que esto sea factible deben dividirse en secuencias, almacenamientos o conjuntos de propiedades independientes. El formato de datos del conjunto de propiedades COM no estaba pensado para proporcionar un sustituto de una base de datos de muchos objetos pequeños.

COM proporciona implementaciones de las interfaces del conjunto de propiedades para varios objetos, junto con tres funciones auxiliares. En la sección siguiente se describen algunas características de rendimiento de estas implementaciones. Para obtener más información sobre interfaces específicas y cómo obtener un puntero a estas interfaces, consulte lo siguiente en la sección referencia COM:

-   [IPropertySetStorage: implementación de archivos compuestos](ipropertysetstorage-compound-file-implementation.md)

    La implementación de archivo compuesto, que proporciona las interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream,**](/windows/desktop/api/Objidl/nn-objidl-istream) también proporciona las interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) [**e IPropertyStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) Dada una implementación de archivo compuesto de **IStorage**, la interfaz **IPropertySetStorage** se puede obtener llamando a [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

-   [Implementación del sistema de archivos IPropertySetStorage–NTFS](ipropertysetstorage-ntfs-file-system-implementation.md)

    Las [**interfaces IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) [**e IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) también se pueden obtener para archivos NTFS que no son archivos compuestos. Por lo tanto, es posible obtener estas interfaces para todos los archivos de un volumen NTFS.

-   [IPropertySetStorage: implementación independiente](ipropertysetstorage-stand-alone-implementation.md)

    Cuando se crea una instancia de esta implementación de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) se le asigna un puntero a un objeto que admite la [**interfaz IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage) A continuación, manipula los almacenamientos del conjunto de propiedades dentro de ese objeto de almacenamiento. Por lo tanto, es posible tener acceso y manipular conjuntos de propiedades en cualquier objeto que admita .

-   [Consideraciones sobre la implementación de IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)

    Hay varios problemas que se deben tener en cuenta al proporcionar una implementación de la [**interfaz IPropertySetStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) Consulte estas consideraciones *de implementación en* la sección Referencia com.

Además, hay cuatro funciones auxiliares, diseñadas para ayudar a tratar con propiedades que se han leído de una propiedad establecida en memoria (en una [**estructura PROPVARIANT):**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

-   [**PropVariantInit**](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [**PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [**FreePropVariantArray**](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [**PropVariantCopy**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)

En las secciones siguientes se deba a las implementaciones de conjunto de propiedades en COM con más detalle:

-   [Administración de conjuntos de propiedades](managing-property-sets.md)
-   [Consideraciones sobre el conjunto de propiedades](property-set-considerations.md)
-   [Almacenar conjuntos de propiedades](storing-property-sets.md)
-   [Características de rendimiento](performance-characteristics.md)
-   [Implementar el conjunto de propiedades Demmary Information](implementing-the-summary-information-property-set.md)
-   [Consideraciones sobre la implementación de IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)

 

 