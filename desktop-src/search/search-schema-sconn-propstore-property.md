---
description: El elemento <property> opcional especifica una propiedad utilizada por el conector de búsqueda. Estas propiedades son específicas de este conector de búsqueda, por lo que no hay ningún conjunto predefinido de nombres para usar. Este elemento no tiene elementos secundarios.
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: elemento property de propertyStore (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0319e86674eb91bf8915ce6218bb387ac9d79e87
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465002"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a>elemento property de propertyStore (esquema del conector de búsqueda)

El elemento <property> opcional especifica una propiedad utilizada por el conector de búsqueda. Estas propiedades son específicas de este conector de búsqueda, por lo que no hay ningún conjunto predefinido de nombres para usar. Este elemento no tiene elementos secundarios.

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
| name | Público. Necesario. El nombre para mostrar de la propiedad. |   | 
| tipo | Público. Necesario. El tipo de propiedad. | Cualquiera: valor predeterminado. El subsistema de propiedades no coercirá el valor. VT_NULL getPropertyType lo devolverá.<ul><li>Null: no hay ningún valor para esta propiedad. VT_NULL getPropertyType lo devolverá.</li><li>Cadena: el valor debe ser un VT_LPWSTR.</li><li>Booleano: el valor debe ser VT_BOOL.</li><li>Byte: el valor debe ser un VT_UI1.</li><li>Búfer: el valor debe ser un VT_UI1 | VT_VECTOR búfer de bytes.</li><li>Int16: el valor debe ser un VT_I2.</li><li>UInt16: el valor debe ser un VT_UI2.</li><li>Int32: el valor debe ser un VT_I4.</li><li>UInt32: el valor debe ser un VT_UI4.</li><li>Int64: el valor debe ser un VT_I8.</li><li>UInt64: el valor debe ser un VT_UI8</li><li>Double: el valor debe ser un VT_R8.</li><li>DateTime: el valor debe ser un VT_FILETIME.</li><li>Guid: el valor debe ser un VT_CLSID.</li><li>Blob: el valor debe ser un VT_BLOB.</li><li>Object: el valor debe ser un VT_UNKNOWN.</li><li>Secuencia: el valor debe ser un VT_STREAM.</li><li>Portapapeles: el valor debe ser un VT_CF.</li></ul> | 
| esquema | Público. Opcional. Esquema donde se define la propiedad. |   | 




 

## <a name="remarks"></a>Comentarios

OpenSearch conectores de búsqueda pueden usar la propiedad OpenSearchHTMLRolloverTemplate. Esta propiedad identifica una plantilla con el formato siguiente a la convención OpenSearch plantilla. La plantilla OpenSearchHTMLRolloverTemplate se usa cuando el usuario hace clic en el botón "Buscar en el sitio web" de la barra de comandos.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra <propertyStore> un elemento con dos elementos <property> .


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



