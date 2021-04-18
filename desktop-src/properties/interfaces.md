---
description: En esta sección se describen las interfaces del sistema de propiedades de Windows.
ms.assetid: d81fe8df-9fd6-4ace-a47f-214cbba6f30c
title: Interfaces (sistema de propiedades de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5003458683fb9b2443df0301676b601901817d54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716083"
---
# <a name="interfaces-windows-property-system"></a>Interfaces (sistema de propiedades de Windows)

En esta sección se describen las interfaces del sistema de propiedades de Windows.



| Tema                                                                                        | Contenido                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPropertyChange**](/windows/win32/api/propsys/nn-propsys-ipropertychange)                                                 | Expone un método que encapsula un cambio en una propiedad única.                                                                                                                                                                                                                                                                                                                          |
| [**IPropertyChangeArray**](/windows/win32/api/propsys/nn-propsys-ipropertychangearray)                                       | Expone métodos para varias operaciones de cambio que se pueden pasar a [**IFileOperation**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileoperation).                                                                                                                                                                                                                                                                   |
| [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                       | Expone métodos que enumeran y recuperan detalles de descripción de propiedades individuales.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescription2**](/windows/win32/api/propsys/nn-propsys-ipropertydescription2)                                     | Expone métodos que enumeran y recuperan detalles de descripción de propiedades individuales.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionAliasInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionaliasinfo)                     | Expone métodos para obtener las propiedades de columnas "ordenar por" para un elemento. Esta interfaz la utilizan los objetos de interfaz de usuario que desean recuperar las columnas de ordenación principal o secundaria para una propiedad determinada.                                                                                                                                                                                                |
| [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)                               | Expone métodos que extraen información de una colección de descripciones de propiedades que se presentan como una lista.                                                                                                                                                                                                                                                                                   |
| [**IPropertyDescriptionRelatedPropertyInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionrelatedpropertyinfo) | Proporciona un método que recupera una interfaz [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription) .                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionSearchInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionsearchinfo)                   | Expone información relacionada con la búsqueda de una propiedad. La información proporcionada por esta interfaz procede del esquema [propertyDescription](./propdesc-schema-propertydescription.md) , elemento [searchInfo](./propdesc-schema-searchinfo.md) para una propiedad determinada. El indizador de Windows Search usa esta información. La mayoría de las aplicaciones de llamada no tendrán que llamar a esta interfaz. |
| [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype)                                             | Expone métodos que extraen datos de la información de enumeración. [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype) proporciona acceso a los elementos [enum](./propdesc-schema-enum.md) y [enumRange](./propdesc-schema-enumrange.md) en el [esquema de propiedades](./propdesc-schema-entry.md) mediante programación en tiempo de ejecución.                                                                 |
| [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2)                                           | Expone métodos que extraen datos de la información de enumeración. [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2) extiende [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype).                                                                                                                                                                                                               |
| [**IPropertyEnumTypeList**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtypelist)                                     | Expone métodos que enumeran los posibles valores de una propiedad.                                                                                                                                                                                                                                                                                                                         |
| [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                   | Expone métodos para enumerar, obtener y establecer valores de propiedad.                                                                                                                                                                                                                                                                                                                     |
| [**IPropertyStoreCache**](/windows/win32/api/propsys/nn-propsys-ipropertystorecache)                                         | Expone métodos que permiten a un controlador administrar varios Estados para cada propiedad.                                                                                                                                                                                                                                                                                                           |
| [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)                           | Expone un método que determina si el usuario puede editar una propiedad en la interfaz de usuario.                                                                                                                                                                                                                                                                                                   |
| [**IPropertyStoreFactory**](/windows/win32/api/propsys/nn-propsys-ipropertystorefactory)                                     | Expone métodos para obtener un objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .                                                                                                                                                                                                                                                                                                               |
| [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem)                                                 | Expone métodos que obtienen descripciones de propiedad, registran y anulan el registro de esquemas de propiedades, enumeran descripciones de propiedades y aplican formato a los valores de propiedad de un modo estricto.                                                                                                                                                                                                                |
| [**IPropertyUI**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipropertyui)                                                         | Los desarrolladores deben usar [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription) en su lugar.                                                                                                                                                                                                                                                                                                      |



 

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

 

 
