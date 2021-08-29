---
description: El &lt; elemento url especifica una dirección URL a la miniatura de este conector de &gt; búsqueda. Si &lt; imageLink &gt; existe, este elemento es obligatorio. No tiene elementos secundarios ni atributos.
ms.assetid: addb2614-9f4f-4cab-a678-b6020b8c4648
title: Elemento imageLink url (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011142e509d34f4942027b90625c9692c7aa87ff
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882403"
---
# <a name="imagelink-url-element-search-connector-schema"></a>Elemento imageLink url (esquema del conector de búsqueda)

El &lt; elemento url especifica una dirección URL a la miniatura de este conector de &gt; búsqueda. Si &lt; imageLink &gt; existe, este elemento es obligatorio. No tiene elementos secundarios ni atributos.

## <a name="syntax"></a>Syntax


```
<!-- url -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="imageLink" minOccurs="0">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="url" type="xs:anyURI"/>
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                                   | Elementos secundarios |
|----------------------------------------------------------------------------------|----------------|
| [Elemento imageLink (esquema del conector de búsqueda)](search-schema-sconn-imagelink.md) |                |



 

## <a name="remarks"></a>Comentarios

El valor puede ser una ruta de acceso del sistema de archivos local o una dirección URL. El archivo de imagen puede ser cualquiera de los tipos de imagen básicos admitidos por Windows 7 (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelinkurl-element"></a>Ejemplo de un elemento imageLinkurl


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



