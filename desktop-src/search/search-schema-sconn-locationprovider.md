---
description: El elemento <locationProvider> opcional especifica el proveedor de búsqueda que usará el conector de búsqueda del proveedor de servicios web. Este elemento contiene un atributo obligatorio y un elemento secundario opcional.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: Elemento locationProvider (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21101fd0e7c57b73af7bc9de525baaca9583d11e425b168d806f750063ac7203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711045"
---
# <a name="locationprovider-element-search-connector-schema"></a>Elemento locationProvider (esquema del conector de búsqueda)

El elemento <locationProvider> opcional especifica el proveedor de búsqueda que usará el conector de búsqueda del proveedor de servicios web. Este elemento contiene un atributo obligatorio y un elemento secundario opcional.

## <a name="syntax"></a>Syntax


```
<!-- locationProvider -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
                    </xs:all>
                <xs:attribute name="clsid" use="required"/>
                <xs:attribute name="codebase" type="xs:string"/>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                                                                   | Elementos secundarios                                                                       |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)](search-schema-searchconnectordescription.md) | [elemento propertyBag (esquema del conector de búsqueda)](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a>Atributos



| Atributo | Descripción                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | Obligatorio. Identificador de clase (CLSID) del proveedor de búsqueda. |
| codebase  | Opcional.                                                      |



 

## <a name="remarks"></a>Comentarios

El valor del atributo @clsid para el proveedor OpenSearch es {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.

Los conectores de búsqueda basados en el sistema de archivos y el controlador de protocolos pueden usar [<simpleLocation>](search-schema-sconn-simplelocation.md) el elemento en su lugar. Si <locationProvider> está presente, NO DEBE haber un <simpleLocation> elemento en la descripción del conector de búsqueda.

## <a name="example-of-a-locationprovider-element"></a>Ejemplo de un elemento locationProvider


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



