---
description: El elemento &lt; iconReference &gt; opcional especifica un icono personalizado para esta ubicación. Este elemento no tiene atributos ni elementos secundarios.
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: elemento iconReference (Esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ff41d6dfd37e5e3fe780171701886b08b195ac
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882418"
---
# <a name="iconreference-element-search-connector-schema"></a>elemento iconReference (Esquema del conector de búsqueda)

El elemento &lt; iconReference &gt; opcional especifica un icono personalizado para esta ubicación. Este elemento no tiene atributos ni elementos secundarios.

## <a name="syntax"></a>Syntax


```
<!-- iconReference -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                                                                   | Elementos secundarios |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a>Comentarios

El formato de la referencia debe especificarse en un formato adecuado para la función [PathParseIconLocation:](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) (por ejemplo, <dll file name> , <icon index> ).

## <a name="example"></a>Ejemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 
