---
description: El elemento &lt; imageLink &gt; opcional especifica una miniatura para este conector de búsqueda. Este elemento tiene un elemento secundario obligatorio y ningún atributo.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: Elemento imageLink (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6030f44e74f8f8441b3a6cd0835df9c5969619
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882401"
---
# <a name="imagelink-element-search-connector-schema"></a>Elemento imageLink (esquema del conector de búsqueda)

El elemento &lt; imageLink &gt; opcional especifica una miniatura para este conector de búsqueda. Este elemento tiene un elemento secundario obligatorio y ningún atributo.

## <a name="syntax"></a>Syntax


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
| [Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)](search-schema-searchconnectordescription.md) | [Elemento imageLink url (esquema del conector de búsqueda)](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a>Comentarios

El valor imageLink puede ser una ruta de acceso del sistema de archivos local o una dirección URL. El archivo de imagen puede ser cualquiera de los tipos de imagen básicos admitidos por Windows 7 (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelink-element"></a>Ejemplo de un elemento imageLink


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



