---
description: El <locationProvider> elemento opcional especifica el proveedor de búsquedas que va a usar el conector de búsqueda del proveedor de servicios Web. Este elemento contiene un atributo obligatorio y un elemento secundario opcional.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: Elemento locationProvider (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c68732300c190b44b984bbe64ca031a81ced84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705473"
---
# <a name="locationprovider-element-search-connector-schema"></a>Elemento locationProvider (esquema del conector de búsqueda)

El <locationProvider> elemento opcional especifica el proveedor de búsquedas que va a usar el conector de búsqueda del proveedor de servicios Web. Este elemento contiene un atributo obligatorio y un elemento secundario opcional.

## <a name="syntax"></a>Sintaxis


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
| [Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)](search-schema-searchconnectordescription.md) | [Elemento propertyBag (esquema del conector de búsqueda)](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a>Atributos



| Atributo | Descripción                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | Obligatorio. Identificador de clase (CLSID) del proveedor de búsquedas. |
| codebase  | Opcional.                                                      |



 

## <a name="remarks"></a>Observaciones

El @clsid valor de atributo para el proveedor de OpenSearch es {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.

El sistema de archivos y los conectores de búsqueda basados en el controlador de protocolo pueden usar el [<simpleLocation>](search-schema-sconn-simplelocation.md) elemento en su lugar. Si <locationProvider> está presente, no debe haber un <simpleLocation> elemento en la descripción del conector de búsqueda.

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



 

 



