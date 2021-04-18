---
description: El <property> elemento opcional especifica una propiedad utilizada por el conector de búsqueda. Estas propiedades son específicas de este conector de búsqueda, por lo que no hay ningún conjunto de nombres predefinido que usar. Este elemento no tiene elementos secundarios.
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: Elemento Property de propertyStore (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2e4cee6f26ee65ba03d9225eafcea4a03a7c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540627"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a>Elemento Property de propertyStore (esquema del conector de búsqueda)

El <property> elemento opcional especifica una propiedad utilizada por el conector de búsqueda. Estas propiedades son específicas de este conector de búsqueda, por lo que no hay ningún conjunto de nombres predefinido que usar. Este elemento no tiene elementos secundarios.

## <a name="syntax"></a>Sintaxis


```
<!-- property for propertyStore element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded">
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



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                                           | Elementos secundarios |
|------------------------------------------------------------------------------------------|----------------|
| [Elemento propertyStore (esquema del conector de búsqueda)](search-schema-sconn-propertystore.md) |                |



 

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
<td> </td>
</tr>
<tr class="even">
<td>type</td>
<td>Público. Obligatorio. El tipo de propiedad.</td>
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
<tr class="odd">
<td>esquema</td>
<td>Público. Opcional. Esquema en el que se define la propiedad.</td>
<td> </td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Los conectores de búsqueda de OpenSearch pueden usar la propiedad OpenSearchHTMLRolloverTemplate. Esta propiedad identifica una plantilla a la que se da formato siguiendo la Convención de plantilla de OpenSearch. La plantilla OpenSearchHTMLRolloverTemplate se usa cuando el usuario hace clic en el botón "Buscar en el sitio web" de la barra de comandos.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra un <propertyStore> elemento con dos <property> elementos.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



