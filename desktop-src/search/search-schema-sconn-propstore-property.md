---
description: El elemento &lt; de propiedad opcional especifica una propiedad utilizada por el conector de &gt; búsqueda. Estas propiedades son específicas de este conector de búsqueda, por lo que no hay ningún conjunto predefinido de nombres para usar. Este elemento no tiene elementos secundarios.
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: elemento property de propertyStore (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ad97c22ac87d67fdec0d007d4333bffe16aad1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886780"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a>elemento property de propertyStore (esquema del conector de búsqueda)

El elemento &lt; de propiedad opcional especifica una propiedad utilizada por el conector de &gt; búsqueda. Estas propiedades son específicas de este conector de búsqueda, por lo que no hay ningún conjunto predefinido de nombres para usar. Este elemento no tiene elementos secundarios.

## <a name="syntax"></a>Syntax


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
| [elemento propertyStore (esquema del conector de búsqueda)](search-schema-sconn-propertystore.md) |                |



 

## <a name="attributes"></a>Atributos




| Atributo | Descripción | Valores | 
|-----------|-------------|--------|
| name | Público. Obligatorio. El nombre para mostrar de la propiedad. |   | 
| type | Público. Obligatorio. El tipo de propiedad. | Cualquiera: valor predeterminado. El subsistema de propiedades no coercirá el valor. VT_NULL getPropertyType lo devolverá.<ul><li>Null: no hay ningún valor para esta propiedad. VT_NULL getPropertyType lo devolverá.</li><li>Cadena: el valor debe ser un VT_LPWSTR.</li><li>Booleano: el valor debe ser VT_BOOL.</li><li>Byte: el valor debe ser un VT_UI1.</li><li>Búfer: el valor debe ser un VT_UI1 | VT_VECTOR búfer de bytes.</li><li>Int16: el valor debe ser un VT_I2.</li><li>UInt16: el valor debe ser un VT_UI2.</li><li>Int32: el valor debe ser un VT_I4.</li><li>UInt32: el valor debe ser un VT_UI4.</li><li>Int64: el valor debe ser un VT_I8.</li><li>UInt64: el valor debe ser un VT_UI8</li><li>Double: el valor debe ser un VT_R8.</li><li>DateTime: el valor debe ser un VT_FILETIME.</li><li>Guid: el valor debe ser un VT_CLSID.</li><li>Blob: el valor debe ser un VT_BLOB.</li><li>Object: el valor debe ser un VT_UNKNOWN.</li><li>Secuencia: el valor debe ser un VT_STREAM.</li><li>Portapapeles: el valor debe ser un VT_CF.</li></ul> | 
| esquema | Público. Opcional. Esquema donde se define la propiedad. |   | 




 

## <a name="remarks"></a>Comentarios

OpenSearch los conectores de búsqueda pueden usar la propiedad OpenSearchHTMLRolloverTemplate. Esta propiedad identifica una plantilla con el formato siguiente a la convención OpenSearch plantilla. La plantilla OpenSearchHTMLRolloverTemplate se usa cuando el usuario hace clic en el botón "Buscar en el sitio web" de la barra de comandos.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra &lt; un elemento propertyStore &gt; con dos elementos de &lt; &gt; propiedad.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



