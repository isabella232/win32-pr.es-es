---
description: Este <templateInfo> elemento opcional especifica un tipo de carpeta para mostrar los resultados de una consulta sobre este conector de búsqueda. Este elemento no tiene atributos y solo un elemento secundario obligatorio.
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: Elemento templateInfo (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fd28780689b4d544f251bbaf1542bc379ecdaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696258"
---
# <a name="templateinfo-element-search-connector-schema"></a>Elemento templateInfo (esquema del conector de búsqueda)

Este <templateInfo> elemento opcional especifica un tipo de carpeta para mostrar los resultados de una consulta sobre este conector de búsqueda. Este elemento no tiene atributos y solo un elemento secundario obligatorio.

## <a name="syntax"></a>Sintaxis


```
<!-- templateInfo -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="templateInfo" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="folderType" minOccurs="0"/>
                    </xs:all>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                                                                   | Elementos secundarios                                                                     |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)](search-schema-searchconnectordescription.md) | [Elemento folderType (esquema del conector de búsqueda)](search-schema-sconn-foldertype.md) |



 

## <a name="remarks"></a>Observaciones

Si no especifica un tipo de carpeta determinado en el <templateInfo> elemento, Windows usa el tipo de carpeta conector de búsqueda general {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.

## <a name="example-of-a-templateinfo-element"></a>Ejemplo de un elemento templateInfo


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



