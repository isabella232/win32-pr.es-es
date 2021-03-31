---
description: En esta sección se describen las constantes, las enumeraciones y las marcas del sistema de propiedades de Windows.
ms.assetid: ff735b9c-e444-4e6f-8e80-0b2a5d770386
title: Constantes, enumeraciones y marcas (sistema de propiedades de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8681c773181b69b24b1fe2d01d380d730c33e220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277064"
---
# <a name="constants-enumerations-and-flags"></a>Constantes, enumeraciones y marcas

En esta sección se describen las constantes, las enumeraciones y las marcas del sistema de propiedades de Windows.



| Tema                                                                              | Contenido                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GETPROPERTYSTOREFLAGS**](/windows/desktop/api/Propsys/ne-propsys-getpropertystoreflags)                             | Indica las marcas que modifican el objeto de almacén de propiedades recuperado por métodos que crean un almacén de propiedades, como [**IShellItem2:: GetPropertyStore**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore) o [**IPropertyStoreFactory:: GetPropertyStore**](/windows/win32/api/propsys/nf-propsys-ipropertystorefactory-getpropertystore).<br/>                                                                                        |
| [**PDOPSTATUS**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-pdopstatus)                                                 | Proporciona marcas de estado de la operación.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**marcas de PKA \_**](/windows/win32/api/propsys/ne-propsys-pka_flags)                                                  | Describe el comportamiento de la matriz de cambios de propiedades.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**\_tipo de agregación PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type)                 | Describe cómo se muestran los valores de propiedad cuando se seleccionan varios elementos. En el caso de una propiedad determinada, \_ el tipo de agregación PROPDESC \_ describe cómo se debe mostrar la propiedad cuando se seleccionan varios elementos que tienen un valor para la propiedad, por ejemplo, si los valores se deben sumar o promediar o simplemente mostrar con la cadena predeterminada "varios valores".<br/> |
| [**PROPDESC \_ COLUMNINDEX ( \_ tipo)**](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)                 | Indica si se puede indizar una propiedad o cómo hacerlo.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**\_tipo de condición PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_condition_type)                     | Describe el tipo de condición que se va a usar al mostrar la propiedad en la interfaz de usuario del generador de consultas en Windows Vista, pero no en Windows 7 y versiones posteriores.<br/>                                                                                                                                                                                                                                      |
| [**PROPDESC \_ ENUMFILTER**](/windows/win32/api/propsys/ne-propsys-propdesc_enumfilter)                              | Describe la lista filtrada de descripciones de propiedad que se devuelve.<br/>                                                                                                                                                                                                                                                                                                          |
| [**\_marcas de formato PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_format_flags)                         | Lo usan las funciones auxiliares de la descripción de propiedad, como [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay), para indicar el formato de una cadena de propiedad.<br/>                                                                                                                                                                                                                         |
| [**\_tipo de RELATIVEDESCRIPTION de PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_relativedescription_type) | Describe el tipo de descripción relativa para una descripción de propiedad, según lo determinado por el atributo *relativeDescriptionType* del elemento [displayInfo](./propdesc-schema-displayinfo.md) .<br/>                                                                                                                                                                                   |
| [**PROPDESC \_ \_ marcas SEARCHINFO**](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)                 | Determina si una propiedad está indizada por Windows Search.<br/>                                                                                                                                                                                                                                                                                                             |
| [**\_marcas de tipo PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_type_flags)                             | Describe los atributos del elemento [typeInfo](./propdesc-schema-typeinfo.md) en el archivo. propDesc de la propiedad.<br/>                                                                                                                                                                                                                                                                |
| [**PROPDESC \_ Ver \_ marcas**](/windows/win32/api/propsys/ne-propsys-propdesc_view_flags)                             | Estas marcas describen las propiedades de las cadenas de lista de descripción de propiedad.<br/>                                                                                                                                                                                                                                                                                                           |
| [**marcas de PROPERTYUI \_**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_propertyui_flags)                                    | Especifica las características de propiedad.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**\_unidad de comparación de PROPVAR \_**](/windows/win32/api/propvarutil/ne-propvarutil-propvar_compare_unit)                           | Estas marcas están asociadas a determinadas comparaciones de la estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .<br/>                                                                                                                                                                                                                                                                               |
| [**Estado de PSC \_**](/windows/win32/api/propsys/ne-propsys-psc_state)                                                  | Especifica el estado de una propiedad. Los establece manualmente el código que hospeda la caché del almacén de propiedades en memoria.<br/>                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de Windows](props.md)
</dt> <dt>

[Esquema de descripción de propiedad](property-description-schema.md)
</dt> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> <dt>

[Interfaces](interfaces.md)
</dt> <dt>

[Funciones](functions.md)
</dt> <dt>

[Estructuras](structures.md)
</dt> </dl>

 

 
