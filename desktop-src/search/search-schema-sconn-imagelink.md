---
description: El elemento <imageLink> opcional especifica una miniatura para este conector de búsqueda. Este elemento tiene un elemento secundario obligatorio y ningún atributo.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: Elemento imageLink (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007ad8c2500e2739210646c446d9f906d5a83571ea4ac9780ab9136b73805c83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711095"
---
# <a name="imagelink-element-search-connector-schema"></a>Elemento imageLink (esquema del conector de búsqueda)

El elemento <imageLink> opcional especifica una miniatura para este conector de búsqueda. Este elemento tiene un elemento secundario obligatorio y ningún atributo.

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



 

 



