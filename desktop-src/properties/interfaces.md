---
description: En esta sección se describen las Windows del sistema de propiedades.
ms.assetid: d81fe8df-9fd6-4ace-a47f-214cbba6f30c
title: Interfaces (Windows property system)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d608e1b994541667847d755e95966b6ea2770c2d0c73ce86ef8fbd79b8c9dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600125"
---
# <a name="interfaces-windows-property-system"></a>Interfaces (Windows property system)

En esta sección se describen las Windows del sistema de propiedades.



| Tema                                                                                        | Contenido                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPropertyChange**](/windows/win32/api/propsys/nn-propsys-ipropertychange)                                                 | Expone un método que encapsula un cambio en una sola propiedad.                                                                                                                                                                                                                                                                                                                          |
| [**IPropertyChangeArray**](/windows/win32/api/propsys/nn-propsys-ipropertychangearray)                                       | Expone métodos para varias operaciones de cambio que se pueden pasar a [**IFileOperation.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileoperation)                                                                                                                                                                                                                                                                   |
| [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                       | Expone métodos que enumeran y recuperan detalles de descripción de propiedades individuales.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescription2**](/windows/win32/api/propsys/nn-propsys-ipropertydescription2)                                     | Expone métodos que enumeran y recuperan detalles de descripción de propiedades individuales.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionAliasInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionaliasinfo)                     | Expone métodos para obtener las propiedades de las columnas "ordenar por" para un elemento. Esta interfaz la usan los objetos de interfaz de usuario que desean recuperar las columnas de ordenación principal o secundaria para una propiedad determinada.                                                                                                                                                                                                |
| [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)                               | Expone métodos que extraen información de una colección de descripciones de propiedades que se presentan como una lista.                                                                                                                                                                                                                                                                                   |
| [**IPropertyDescriptionRelatedPropertyInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionrelatedpropertyinfo) | Proporciona un método que reinterio una [**interfaz IPropertyDescription.**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionSearchInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionsearchinfo)                   | Expone información relacionada con la búsqueda de una propiedad. La información proporcionada por esta interfaz procede del esquema [propertyDescription,](./propdesc-schema-propertydescription.md) [el elemento searchInfo](./propdesc-schema-searchinfo.md) de una propiedad determinada. El indexador de búsqueda de Windows utiliza esta información. La mayoría de las aplicaciones que llaman no tendrán que llamar a esta interfaz. |
| [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype)                                             | Expone métodos que extraen datos de la información de enumeración. [**IPropertyEnumType proporciona**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype) acceso a los elementos [enum](./propdesc-schema-enum.md) y [enumRange](./propdesc-schema-enumrange.md) en el esquema de propiedades de forma programática en tiempo de ejecución. [](./propdesc-schema-entry.md)                                                                 |
| [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2)                                           | Expone métodos que extraen datos de la información de enumeración. [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2) extiende [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype).                                                                                                                                                                                                               |
| [**IPropertyEnumTypeList**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtypelist)                                     | Expone métodos que enumeran los valores posibles de una propiedad.                                                                                                                                                                                                                                                                                                                         |
| [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                   | Expone métodos para enumerar, obtener y establecer valores de propiedad.                                                                                                                                                                                                                                                                                                                     |
| [**IPropertyStoreCache**](/windows/win32/api/propsys/nn-propsys-ipropertystorecache)                                         | Expone métodos que permiten a un controlador administrar varios estados para cada propiedad.                                                                                                                                                                                                                                                                                                           |
| [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)                           | Expone un método que determina si el usuario puede editar una propiedad en la interfaz de usuario.                                                                                                                                                                                                                                                                                                   |
| [**IPropertyStoreFactory**](/windows/win32/api/propsys/nn-propsys-ipropertystorefactory)                                     | Expone métodos para obtener un [**objeto IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                                                                                                                                                                                                                                                                               |
| [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem)                                                 | Expone métodos que obtienen descripciones de propiedades, registran y anulan el registro de esquemas de propiedades, enumeran las descripciones de propiedades y formatea los valores de propiedad de forma estricta de tipos.                                                                                                                                                                                                                |
| [**IPropertyUI**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipropertyui)                                                         | En su lugar, [**los desarrolladores deben usar IPropertyDescription.**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de Windows](props.md)
</dt> <dt>

[Esquema de descripción de propiedad](property-description-schema.md)
</dt> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> <dt>

[Funciones](functions.md)
</dt> <dt>

[Estructuras](structures.md)
</dt> <dt>

[Constantes, enumeraciones y marcas](constants--enumerations--and-flags.md)
</dt> </dl>

 

 
