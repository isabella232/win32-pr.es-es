---
description: El <property> elemento opcional especifica las propiedades que utiliza el proveedor de ubicación.
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: Elemento Property de locationProvider (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71081b8b04ec999daa90958a29708b8efc64bee0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105707717"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a>Elemento Property de locationProvider (esquema del conector de búsqueda)

El <property> elemento opcional especifica las propiedades que utiliza el proveedor de ubicación. Estas propiedades son específicas de este proveedor de ubicación, por lo que no hay ningún conjunto de nombres predefinido que usar. El <property> elemento tiene dos atributos, tal y como se describe en este tema.

## <a name="syntax"></a>Sintaxis


```
<!-- property element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension base="xs:anyType">
                        <xs:attribute name="name" type="canonical-name" use="required"/>
                        <xs:attribute name="type"/>
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:element>
```



## <a name="property-element-information"></a><property> Información del elemento



| Elemento primario                                                                                 | Elementos secundarios                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [Elemento locationProvider (esquema del conector de búsqueda)](search-schema-sconn-locationprovider.md) | , que se describe en este tema. |



 


## <a name="property-attributes"></a><property> Sus



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
<td>Necesario. El nombre para mostrar de la propiedad.</td>
<td> </td>
</tr>
<tr class="even">
<td>type</td>
<td>Obligatorio. El tipo de propiedad.</td>
<td>Any: valor predeterminado. El subsistema de propiedades no convertirá el valor. GetPropertyType devolverá VT_NULL.
<ul>
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
<li>UInt64: el valor debe ser un VT_UI8</li>
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

Para el proveedor de OpenSearch, se usan las siguientes propiedades:

-   OpenSearchShortName: nombre corto del servicio de búsqueda
-   OpenSearchQueryTemplate: plantilla, con el formato que sigue la Convención de plantilla de OpenSearch, para el servicio de consulta
-   MaximumResultCount: (número) número máximo de resultados devueltos por el servicio de búsqueda
-   LinkIsFilePath: (booleano) si es true, el proveedor intenta interpretar los elementos devueltos como archivos, mediante sus extensiones para crear el ShellItem adecuado en la vista. Si es false, los elementos se tratan como métodos abreviados de dirección URL.

 

 



