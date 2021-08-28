---
description: El elemento opcional locationProvider especifica el proveedor de búsqueda que usará el conector de búsqueda del &lt; &gt; proveedor de servicios web. Este elemento contiene un atributo obligatorio y un elemento secundario opcional.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: Elemento locationProvider (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f049a01cc0c51075c147918a2f43b740000f2e36
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883370"
---
# <a name="locationprovider-element-search-connector-schema"></a>Elemento locationProvider (esquema del conector de búsqueda)

El elemento opcional locationProvider especifica el proveedor de búsqueda que usará el conector de búsqueda del &lt; &gt; proveedor de servicios web. Este elemento contiene un atributo obligatorio y un elemento secundario opcional.

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

Los conectores de búsqueda basados en el sistema de archivos y el controlador de protocolos pueden usar el [ &lt; elemento simpleLocation &gt; ](search-schema-sconn-simplelocation.md) en su lugar. Si &lt; locationProvider &gt; está presente, NO DEBE haber un elemento &lt; simpleLocation en la descripción del conector de &gt; búsqueda.

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



 

 



