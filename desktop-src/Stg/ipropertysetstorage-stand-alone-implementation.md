---
title: 'IPropertySetStorage: implementación independiente'
description: La implementación independiente proporcionada por el sistema de IPropertySetStorage incluye una implementación de IPropertyStorage y IPropertySetStorage.
ms.assetid: 0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2
keywords:
- IPropertySetStorage Strctd STG, implementaciones
- IPropertySetStorage Strctd STG, implementaciones, independiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9fd0afe31775b06b3a5f61f4c79939be976e98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077859"
---
# <a name="ipropertysetstorage-stand-alone-implementation"></a>IPropertySetStorage: implementación independiente

La implementación independiente proporcionada por el sistema de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) incluye una implementación de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) y **IPropertySetStorage**. [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) es la interfaz que lee y escribe propiedades en un almacenamiento de conjunto de propiedades. [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) es la interfaz que crea y abre conjuntos de propiedades en un almacenamiento. Las interfaces [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) y [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) también se proporcionan en la implementación independiente.

Para usar la implementación independiente de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), obtenga primero un puntero a la implementación independiente proporcionada por el sistema y asocie la implementación proporcionada por el sistema con el objeto de almacenamiento. Para obtener un puntero a la implementación independiente de **IPropertySetStorage**, llame a la función [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) y proporcione el parámetro *pStorage* que especifica el objeto de almacenamiento que contendrá el conjunto de propiedades. Esta función proporciona un puntero a la nueva interfaz **IPropertySetStorage** para el objeto de almacenamiento especificado.

La implementación independiente de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) crea conjuntos de propiedades en cualquier objeto de almacenamiento, no solo en almacenamientos de archivos compuestos. La implementación independiente no depende de archivos compuestos y se puede usar con cualquier implementación de almacenamiento estructurado. Las restricciones en los almacenamientos estructurados proporcionados por el llamador se aplican a esta implementación de conjuntos de propiedades. Por ejemplo, si proporciona un almacenamiento de modo simple a [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), el [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)proporcionado restringirá el **IPropertySetStorage** resultante.

Para obtener más información sobre la implementación de archivos compuestos de esta interfaz, vea la sección [implementación de archivos compuestos IPropertySetStorage](ipropertysetstorage-compound-file-implementation.md).

## <a name="when-to-use"></a>Cuándo usar

Llame a los métodos de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para crear, abrir y eliminar conjuntos de propiedades en cualquier almacenamiento estructurado. También hay un método que proporciona un puntero al enumerador [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) que se puede usar para enumerar los conjuntos de propiedades en el almacenamiento.

La implementación independiente también proporciona las funciones auxiliares [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) y [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) , además de los métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) y [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , para crear y abrir conjuntos de propiedades. Estas dos funciones agregan compatibilidad para el \_ valor no almacenado en búfer de PROPSETFLAG, por lo que puede escribir cambios directamente en el conjunto de propiedades en lugar de almacenarlos en búfer en una memoria caché. Para obtener más información, vea [**constantes PROPSETFLAG**](propsetflag-constants.md).

## <a name="methods"></a>Métodos

La implementación independiente de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) admite los siguientes métodos.

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

Crea un nuevo conjunto de propiedades en el almacenamiento y devuelve un puntero a la interfaz [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) en el conjunto de propiedades.

Si tiene previsto usar el valor de PROPSETFLAG no \_ almacenado en búfer, utilice en su lugar la función [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) para crear y abrir el nuevo conjunto de propiedades y para obtener un puntero a la implementación independiente de la interfaz [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) en el conjunto de propiedades.

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

Abre un conjunto de propiedades existente en el almacenamiento y devuelve un puntero a la interfaz [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) en el conjunto de propiedades.

Si tiene previsto usar el valor de PROPSETFLAG no \_ almacenado en búfer, utilice en su lugar la función [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) para obtener un puntero a la implementación independiente de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) en el conjunto de propiedades especificado.

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D iminar**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

Elimina un conjunto de propiedades en este almacenamiento de conjunto de propiedades.

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

Crea un objeto que se puede utilizar para enumerar las estructuras [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Cada estructura **STATPROPSETSTG** proporciona datos sobre un conjunto de propiedades único.

> [!Note]  
> El conjunto de propiedades DocumentSummaryInformation y UserDefined es único en el sentido de que puede tener dos secciones set de propiedad en una única secuencia subyacente. Para obtener más información, vea [los conjuntos de propiedades DocumentSummaryInformation y UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md) .

 

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IPropertyStorage: implementación independiente](ipropertystorage-stand-alone-implementation.md)
</dt> <dt>

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage:: EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[**Constantes de PROPSETFLAG**](propsetflag-constants.md)
</dt> <dt>

[**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dt>

[**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> <dt>

[**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**Constantes de STGM**](stgm-constants.md)
</dt> </dl>

 

 