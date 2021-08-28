---
description: Este elemento &lt; templateInfo opcional especifica un tipo de carpeta para mostrar los &gt; resultados de una consulta a través de este conector de búsqueda. Este elemento no tiene atributos y solo un elemento secundario obligatorio.
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: elemento templateInfo (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c815d04e23f1e1af9582ad93ba08d118855676
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880386"
---
# <a name="templateinfo-element-search-connector-schema"></a>elemento templateInfo (esquema del conector de búsqueda)

Este elemento &lt; templateInfo opcional especifica un tipo de carpeta para mostrar los &gt; resultados de una consulta a través de este conector de búsqueda. Este elemento no tiene atributos y solo un elemento secundario obligatorio.

## <a name="syntax"></a>Syntax


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



 

## <a name="remarks"></a>Comentarios

Si no especifica un tipo de carpeta determinado en el elemento templateInfo, Windows usa el tipo de carpeta del conector de búsqueda &lt; &gt; general {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.

## <a name="example-of-a-templateinfo-element"></a>Ejemplo de un elemento templateInfo


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



