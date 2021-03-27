---
description: El <property> elemento especifica una propiedad utilizada por la biblioteca. Estas propiedades son específicas de la biblioteca, por lo que no hay ningún conjunto predefinido de nombres de propiedad para usar. Este elemento es opcional y no tiene elementos secundarios.
ms.assetid: 8BF6EC7A-A87E-45fe-A8F0-4B49594E9E7B
title: Property (elemento, esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b269e8914cf1f5da92d96e1922f7347a161daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997249"
---
# <a name="property-element-library-schema"></a>Property (elemento, esquema de biblioteca)

El <property> elemento especifica una propiedad utilizada por la biblioteca. Estas propiedades son específicas de la biblioteca, por lo que no hay ningún conjunto predefinido de nombres de propiedad para usar. Este elemento es opcional y no tiene elementos secundarios.

## <a name="syntax"></a>Sintaxis

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
| [Elemento propertyStore (esquema de biblioteca)](schema-library-propertystore.md) | Ninguno           |



 

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
<th>Valores</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>name</td>
<td>Público. Obligatorio. El nombre para mostrar de la propiedad.</td>

</tr>
<tr class="even">
<td>tipo</td>
<td>Público. Obligatorio. El tipo de propiedad.</td>
<td><ul>
<li>Any: valor predeterminado. El subsistema de propiedades no convertirá el valor. GetPropertyType devolverá VT_NULL.</li>
<li>NULL: no hay ningún valor para esta propiedad. GetPropertyType devolverá VT_NULL.</li>
<li>Cadena: el valor debe ser un VT_LPWSTR.</li>
<li>Booleano: el valor debe ser un VT_BOOL.</li>
<li>Byte: el valor debe ser un VT_UI1.</li>
<li>Buffer: el valor debe ser un VT_UI1 | VT_VECTOR búfer de bytes.</li>
<li>Int16: el valor debe ser un VT_I2.</li>
<li>UInt16: el valor debe ser un VT_UI2.</li>
<li>Int32: el valor debe ser un VT_I4.</li>
<li>UInt32: el valor debe ser un VT_UI4.</li>
<li>Int64: el valor debe ser un VT_I8.</li>
<li>UInt64: el valor debe ser un VT_UI8.</li>
<li>Double: el valor debe ser un VT_R8.</li>
<li>DateTime: el valor debe ser un VT_FILETIME.</li>
<li>GUID: el valor debe ser un VT_CLSID.</li>
<li>BLOB: el valor debe ser un VT_BLOB.</li>
<li>Objeto: el valor debe ser un VT_UNKNOWN.</li>
<li>Stream: el valor debe ser un VT_STREAM.</li>
<li>Clipboard: el valor debe ser un VT_CF.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Los requisitos para el elemento <nombre canónico> coinciden con los requisitos de Windows Search y del sistema de propiedades de Windows. La cadena debe ser de tipo canónico-Type.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquemas de propiedades](../properties/building-property-handlers-property-schemas.md)
</dt> <dt>

[Esquema de Descripción del conector de búsqueda](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
