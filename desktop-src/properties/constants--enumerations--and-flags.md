---
description: En esta sección se describen las Windows del sistema de propiedades, enumeraciones y marcas.
ms.assetid: ff735b9c-e444-4e6f-8e80-0b2a5d770386
title: Constantes, enumeraciones y marcas (Windows de propiedades)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8681c773181b69b24b1fe2d01d380d730c33e220
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360674"
---
# <a name="constants-enumerations-and-flags"></a>Constantes, enumeraciones y marcas

En esta sección se describen las Windows del sistema de propiedades, enumeraciones y marcas.



| Tema                                                                              | Contenido                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GETPROPERTYSTOREFLAGS**](/windows/desktop/api/Propsys/ne-propsys-getpropertystoreflags)                             | Indica marcas que modifican el objeto de almacén de propiedades recuperado por los métodos que crean un almacén de propiedades, como [**IShellItem2::GetPropertyStore**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore) o [**IPropertyStoreFactory::GetPropertyStore**](/windows/win32/api/propsys/nf-propsys-ipropertystorefactory-getpropertystore).<br/>                                                                                        |
| [**PDOPSTATUS**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-pdopstatus)                                                 | Proporciona marcas de estado de la operación.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**MARCAS \_ PKA**](/windows/win32/api/propsys/ne-propsys-pka_flags)                                                  | Describe el comportamiento de la matriz de cambios de propiedad.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**TIPO DE \_ AGREGACIÓN \_ PROPDESC**](/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type)                 | Describe cómo se muestran los valores de propiedad cuando se seleccionan varios elementos. Para una propiedad determinada, PROPDESC AGGREGATION TYPE describe cómo se debe mostrar la propiedad cuando se seleccionan varios elementos que tienen un valor para la propiedad, como si los valores se deben sumar o promediar, o simplemente mostrarse con la cadena \_ \_ predeterminada "Varios valores".<br/> |
| [**PROPDESC \_ COLUMNINDEX \_ TYPE**](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)                 | Indica si una propiedad se puede indexar o cómo se puede indexar.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**TIPO DE CONDICIÓN \_ PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_condition_type)                     | Describe el tipo de condición que se va a usar al mostrar la propiedad en la interfaz de usuario del generador de consultas en Windows Vista, pero no en Windows 7 y versiones posteriores.<br/>                                                                                                                                                                                                                                      |
| [**PROPDESC \_ ENUMFILTER**](/windows/win32/api/propsys/ne-propsys-propdesc_enumfilter)                              | Describe la lista filtrada de descripciones de propiedades que se devuelven.<br/>                                                                                                                                                                                                                                                                                                          |
| [**MARCAS DE \_ FORMATO PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_format_flags)                         | Usado por las funciones auxiliares de descripción de propiedades, [**como PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay), para indicar el formato de una cadena de propiedad.<br/>                                                                                                                                                                                                                         |
| [**PROPDESC \_ RELATIVEDESCRIPTION \_ TYPE**](/windows/win32/api/propsys/ne-propsys-propdesc_relativedescription_type) | Describe el tipo de descripción relativa de una descripción de propiedad, determinado por el atributo *relativeDescriptionType* del [elemento displayInfo.](./propdesc-schema-displayinfo.md)<br/>                                                                                                                                                                                   |
| [**MARCAS \_ SEARCHINFO DE PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)                 | Determina si y cómo se indexa una propiedad mediante Windows Search.<br/>                                                                                                                                                                                                                                                                                                             |
| [**MARCAS DE TIPO PROPDESC \_ \_**](/windows/win32/api/propsys/ne-propsys-propdesc_type_flags)                             | Describe los atributos del [elemento typeInfo](./propdesc-schema-typeinfo.md) en el archivo .propdesc de la propiedad.<br/>                                                                                                                                                                                                                                                                |
| [**MARCAS DE \_ VISTA PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_view_flags)                             | Estas marcas describen las propiedades de las cadenas de lista de descripción de propiedades.<br/>                                                                                                                                                                                                                                                                                                           |
| [**MARCAS \_ PROPERTYUI**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_propertyui_flags)                                    | Especifica las características de propiedad.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**UNIDAD DE COMPARACIÓN DE PROPVAR \_ \_**](/windows/win32/api/propvarutil/ne-propvarutil-propvar_compare_unit)                           | Estas marcas están asociadas a determinadas comparaciones de estructura [**PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)<br/>                                                                                                                                                                                                                                                                               |
| [**PSC \_ STATE**](/windows/win32/api/propsys/ne-propsys-psc_state)                                                  | Especifica el estado de una propiedad. Se establecen manualmente mediante el código que hospeda la memoria caché del almacén de propiedades en memoria.<br/>                                                                                                                                                                                                                                                        |



 

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

 

 
