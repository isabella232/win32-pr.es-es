---
description: El <property> elemento especifica una propiedad utilizada por la biblioteca. Estas propiedades son específicas de la biblioteca, por lo que no hay ningún conjunto predefinido de nombres de propiedad que usar. Este elemento es opcional y no tiene elementos secundarios.
ms.assetid: 8BF6EC7A-A87E-45fe-A8F0-4B49594E9E7B
title: elemento property (Esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481122db633750b042172561eedace81fe1d752e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468642"
---
# <a name="property-element-library-schema"></a>elemento property (Esquema de biblioteca)

El <property> elemento especifica una propiedad utilizada por la biblioteca. Estas propiedades son específicas de la biblioteca, por lo que no hay ningún conjunto predefinido de nombres de propiedad que usar. Este elemento es opcional y no tiene elementos secundarios.

## <a name="syntax"></a>Syntax

``` syntax
<!-- property -->
<xs:element name="property" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension base="xs:anyType">
                <xs:attribute name="name" type="canonical-name" use="required"/>
                    <xs:simpleType name="canonical-name">
                        <xs:restriction base="xs:string">
                            <xs:maxLength value="63"/>
                            <xs:pattern value="[0-9A-Za-z.]*"/>
                        </xs:restriction>
                    </xs:simpleType>
                <xs:attribute name="type"/>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Información de elemento



| Elemento primario                                                             | Elementos secundarios |
|----------------------------------------------------------------------------|----------------|
| [elemento propertyStore (esquema de biblioteca)](schema-library-propertystore.md) | Ninguno           |



 

## <a name="attributes"></a>Atributos




| Atributo | Descripción | Valores | 
|-----------|-------------|--------|
| name | Público. Necesario. El nombre para mostrar de la propiedad. | 
| tipo | Público. Necesario. El tipo de propiedad. | <ul><li>Cualquiera: valor predeterminado. El subsistema de propiedades no coercirá el valor. VT_NULL getPropertyType lo devolverá.</li><li>Null: no hay ningún valor para esta propiedad. VT_NULL getPropertyType lo devolverá.</li><li>Cadena: el valor debe ser un VT_LPWSTR.</li><li>Booleano: el valor debe ser VT_BOOL.</li><li>Byte: el valor debe ser un VT_UI1.</li><li>Búfer: el valor debe ser un VT_UI1 | VT_VECTOR búfer de bytes.</li><li>Int16: el valor debe ser un VT_I2.</li><li>UInt16: el valor debe ser un VT_UI2.</li><li>Int32: el valor debe ser un VT_I4.</li><li>UInt32: el valor debe ser un VT_UI4.</li><li>Int64: el valor debe ser un VT_I8.</li><li>UInt64: el valor debe ser un VT_UI8.</li><li>Double: el valor debe ser un VT_R8.</li><li>DateTime: el valor debe ser un VT_FILETIME.</li><li>Guid: el valor debe ser un VT_CLSID.</li><li>Blob: el valor debe ser un VT_BLOB.</li><li>Objeto: el valor debe ser un VT_UNKNOWN.</li><li>Secuencia: el valor debe ser un VT_STREAM.</li><li>Portapapeles: el valor debe ser un VT_CF.</li></ul> | 




 

## <a name="remarks"></a>Comentarios

Los requisitos para el <de nombre canónico> coinciden con los requisitos de Windows Search y el Windows de propiedades. La cadena debe ser de tipo canonical-type.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquemas de propiedades](../properties/building-property-handlers-property-schemas.md)
</dt> <dt>

[Esquema de descripción del conector de búsqueda](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
