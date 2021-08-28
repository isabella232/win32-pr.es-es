---
description: El elemento &lt; de propiedad opcional especifica las propiedades &gt; utilizadas por el proveedor de ubicación.
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: elemento property de locationProvider (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad478fd1d1c00ad5c7f866831cdfdf898557546b
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883332"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a>elemento property de locationProvider (esquema del conector de búsqueda)

El elemento &lt; de propiedad opcional especifica las propiedades &gt; utilizadas por el proveedor de ubicación. Estas propiedades son específicas de este proveedor de ubicación, por lo que no hay ningún conjunto predefinido de nombres para usar. El &lt; elemento de propiedad tiene dos &gt; atributos, como se describe en este tema.

## <a name="syntax"></a>Syntax


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



## <a name="ltpropertygt-element-information"></a>&lt;información &gt; del elemento property



| Elemento primario                                                                                 | Elementos secundarios                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [elemento locationProvider (esquema del conector de búsqueda)](search-schema-sconn-locationprovider.md) | property, que se describe en este tema. |



 


## <a name="ltpropertygt-attributes"></a>&lt;atributos de &gt; propiedad




| Atributo | Descripción | Valores | 
|-----------|-------------|--------|
| name | Necesario. El nombre para mostrar de la propiedad. |   | 
| type | Obligatorio. El tipo de propiedad. | Cualquiera: valor predeterminado. El subsistema de propiedades no coercirá el valor. VT_NULL getPropertyType lo devolverá.<ul><li>Null: no hay ningún valor para esta propiedad. VT_NULL getPropertyType lo devolverá.</li><li>Cadena: el valor debe ser un VT_LPWSTR.</li><li>Booleano: el valor debe ser VT_BOOL.</li><li>Byte: el valor debe ser un VT_UI1.</li><li>Búfer: el valor debe ser un VT_UI1 | VT_VECTOR búfer de bytes.</li><li>Int16: el valor debe ser un VT_I2.</li><li>UInt16: el valor debe ser un VT_UI2.</li><li>Int32: el valor debe ser un VT_I4.</li><li>UInt32: el valor debe ser un VT_UI4.</li><li>Int64: el valor debe ser un VT_I8.</li><li>UInt64: el valor debe ser un VT_UI8</li><li>Double: el valor debe ser un VT_R8.</li><li>DateTime: el valor debe ser un VT_FILETIME.</li><li>Guid: el valor debe ser un VT_CLSID.</li><li>Blob: el valor debe ser un VT_BLOB.</li><li>Object: el valor debe ser un VT_UNKNOWN.</li><li>Secuencia: el valor debe ser un VT_STREAM.</li><li>Portapapeles: el valor debe ser un VT_CF.</li></ul> | 




 

## <a name="remarks"></a>Comentarios

Para el OpenSearch, se usan las siguientes propiedades:

-   OpenSearchShortName: nombre corto del servicio de búsqueda
-   OpenSearchQueryTemplate: plantilla, con el formato siguiente a OpenSearch convención de plantilla, para el servicio de consulta
-   MaximumResultCount: (number) Número máximo de resultados devueltos por el servicio de búsqueda
-   LinkIsFilePath: (booleano) Si es true, el proveedor intenta interpretar los elementos devueltos como archivos, usando sus extensiones para crear el shellItem adecuado en la vista. Si es false, los elementos se tratan como métodos abreviados de dirección URL.

 

 



