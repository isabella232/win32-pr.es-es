---
description: El <url> elemento especifica una dirección URL a la miniatura de este conector de búsqueda. Si <imageLink> existe, este elemento es obligatorio. No tiene elementos secundarios ni atributos.
ms.assetid: addb2614-9f4f-4cab-a678-b6020b8c4648
title: imageLink URL (elemento) (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97daaafcbf6336dd4d88c3c92315e656d137b1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696269"
---
# <a name="imagelink-url-element-search-connector-schema"></a>imageLink URL (elemento) (esquema del conector de búsqueda)

El <url> elemento especifica una dirección URL a la miniatura de este conector de búsqueda. Si <imageLink> existe, este elemento es obligatorio. No tiene elementos secundarios ni atributos.

## <a name="syntax"></a>Sintaxis


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



 

## <a name="remarks"></a>Observaciones

El valor puede ser una ruta de acceso del sistema de archivos local o una dirección URL. El archivo de imagen puede ser cualquiera de los tipos de imagen básicos compatibles con Windows 7 (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelinkurl-element"></a>Ejemplo de un elemento imageLinkurl


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



