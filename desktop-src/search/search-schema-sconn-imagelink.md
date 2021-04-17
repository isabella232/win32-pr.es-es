---
description: El <imageLink> elemento opcional especifica una miniatura para este conector de búsqueda. Este elemento tiene un elemento secundario obligatorio y ningún atributo.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: Elemento imageLink (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b2e5cbbfc8bbd98557ebd0405a09cf998e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696268"
---
# <a name="imagelink-element-search-connector-schema"></a>Elemento imageLink (esquema del conector de búsqueda)

El <imageLink> elemento opcional especifica una miniatura para este conector de búsqueda. Este elemento tiene un elemento secundario obligatorio y ningún atributo.

## <a name="syntax"></a>Sintaxis


```
<!-- imageLink -->
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



| Elemento primario                                                                                                   | Elementos secundarios                                                                           |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)](search-schema-searchconnectordescription.md) | [imageLink URL (elemento) (esquema del conector de búsqueda)](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a>Observaciones

El valor de imageLink puede ser una ruta de acceso del sistema de archivos local o una dirección URL. El archivo de imagen puede ser cualquiera de los tipos de imagen básicos compatibles con Windows 7 (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelink-element"></a>Ejemplo de un elemento imageLink


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



