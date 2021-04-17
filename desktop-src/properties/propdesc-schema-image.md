---
description: .
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: Elemento Image (esquema de descripción de propiedad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb519d5f8104d114734e1f12676f213312e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666862"
---
# <a name="image"></a>imagen

Solo debe haber un elemento de [imagen]() para cada elemento primario.

## <a name="syntax"></a>Sintaxis


```
<!-- image -->
<xs:element name="image">
    <xs:complexType>
        <xs:attribute name="res" use="required">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:maxLength value="260"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Información de elemento



| Elementos primarios                                                                  | Elementos secundarios |
|----------------------------------------------------------------------------------|----------------|
| [enumeración](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md) | None           |



 

## <a name="attributes"></a>Atributos



| Atributo | Descripción       |
|-----------|-------------------|
| res       | Público. Obligatorio. |



 

 

 
