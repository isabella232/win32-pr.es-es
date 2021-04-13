---
description: El <simpleLocation> elemento especifica la ubicación de los conectores de búsqueda basados en el sistema de archivos o en el controlador de protocolo. Este elemento tiene dos elementos secundarios y ningún atributo.
ms.assetid: 04ffc178-0a76-4870-a075-a2ecd31937a1
title: Elemento simpleLocation (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12c17ace36314ceb180f14b6de0eb7a890a385b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360179"
---
# <a name="simplelocation-element-search-connector-schema"></a>Elemento simpleLocation (esquema del conector de búsqueda)

El <simpleLocation> elemento especifica la ubicación de los conectores de búsqueda basados en el sistema de archivos o en el controlador de protocolo. Este elemento tiene dos elementos secundarios y ningún atributo.

## <a name="syntax"></a>Sintaxis


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
| [Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)](search-schema-searchconnectordescription.md) | [simpleLocation URL (elemento) (esquema del conector de búsqueda)](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | serializado: este elemento contiene la ShellLink con codificación Base64 que apunta a la ubicación definida en el <url> elemento. Windows 7 crea el ShellLink a partir del valor del <url> elemento y actualiza correctamente este campo en la primera carga de esta biblioteca, por lo que el autor debe dejarlo vacío. |



 

## <a name="remarks"></a>Observaciones

Este elemento se puede usar en lugar de <locationProvider> cuando la ubicación está en el sistema de archivos o el conector es un controlador de protocolo conocido (como MAPI:). Si <simpleLocation> está presente, no debe haber un <locationProvider> elemento. En el caso de los conectores de búsqueda de proveedores de servicios Web, use el [<locationProvider>](search-schema-sconn-locationprovider.md) elemento en su lugar.

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



 

 



