---
description: El elemento simpleLocation especifica la ubicación de los conectores de búsqueda basados en el sistema de archivos &lt; o en el controlador de &gt; protocolos. Este elemento tiene dos elementos secundarios y ningún atributo.
ms.assetid: 04ffc178-0a76-4870-a075-a2ecd31937a1
title: elemento simpleLocation (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d266d44659fab85958cb9b4f494223d4d02d5231
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880456"
---
# <a name="simplelocation-element-search-connector-schema"></a>elemento simpleLocation (esquema del conector de búsqueda)

El elemento simpleLocation especifica la ubicación de los conectores de búsqueda basados en el sistema de archivos &lt; o en el controlador de &gt; protocolos. Este elemento tiene dos elementos secundarios y ningún atributo.

## <a name="syntax"></a>Syntax


```
<!-- simpleLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0">
                <xs:all>
                    <xs:element name="url" type="xs:anyURI"/>
                    <xs:element name="serialized" minOccurs="0"/>
                </xs:all>
                
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                                                                   | Elementos secundarios                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)](search-schema-searchconnectordescription.md) | [elemento simpleLocation url (esquema del conector de búsqueda)](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | serialized: este elemento contiene el shellLink codificado en base64 que apunta a la ubicación definida en el elemento &lt; &gt; url. Windows 7 crea ShellLink a partir del valor del elemento url y actualiza correctamente este campo en la primera carga de esta biblioteca, por lo que el autor debe dejarla &lt; &gt; vacía. |



 

## <a name="remarks"></a>Comentarios

Este elemento se puede usar en lugar de locationProvider cuando la ubicación está en el sistema de archivos o el conector es un controlador de protocolo conocido &lt; &gt; (como mapi:). Si &lt; simpleLocation &gt; está presente, NO DEBE haber un elemento &lt; &gt; locationProvider. Para los conectores de búsqueda del proveedor de servicios web, use el [ &lt; elemento locationProvider &gt; ](search-schema-sconn-locationprovider.md) en su lugar.

## <a name="examples"></a>Ejemplos


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```



 

 



