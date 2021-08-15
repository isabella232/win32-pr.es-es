---
description: El elemento especifica la ubicación de los conectores de búsqueda basados en el sistema de archivos <simpleLocation> o en el controlador de protocolos. Este elemento tiene dos elementos secundarios y ningún atributo.
ms.assetid: 04ffc178-0a76-4870-a075-a2ecd31937a1
title: elemento simpleLocation (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82731c5a230f8dd12b9d73cafd75dfc7d3cdd66bf1e57120701ed3ca0ba54b07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862466"
---
# <a name="simplelocation-element-search-connector-schema"></a>elemento simpleLocation (esquema del conector de búsqueda)

El elemento especifica la ubicación de los conectores de búsqueda basados en el sistema de archivos <simpleLocation> o en el controlador de protocolos. Este elemento tiene dos elementos secundarios y ningún atributo.

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
| [Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)](search-schema-searchconnectordescription.md) | [Elemento simpleLocation url (esquema del conector de búsqueda)](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | serialized: este elemento contiene el shellLink codificado en base64 que apunta a la ubicación definida en el <url> elemento . Windows 7 crea ShellLink a partir del valor del elemento y actualiza correctamente este campo en la primera carga de esta biblioteca, por lo que el autor debe dejarla <url> vacía. |



 

## <a name="remarks"></a>Comentarios

Este elemento se puede usar en lugar de cuando la ubicación está en el sistema de archivos o el conector es un controlador de <locationProvider> protocolo conocido (como mapi:). Si <simpleLocation> está presente, NO DEBE haber un <locationProvider> elemento . Para los conectores de búsqueda del proveedor de servicios web, use el [<locationProvider>](search-schema-sconn-locationprovider.md) elemento en su lugar.

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



 

 



