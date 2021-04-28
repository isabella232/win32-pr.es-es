---
description: imagen
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: elemento image (esquema de descripción de propiedad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24ecb1b88b8b724ce299a81281f926972180743
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104993"
---
# <a name="image"></a>imagen

Solo debe haber un elemento [image]() para cada elemento primario.

## <a name="syntax"></a>Syntax


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
| [enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md) | None           |



 

## <a name="attributes"></a>Atributos



| Atributo | Descripción       |
|-----------|-------------------|
| res       | Público. Necesario. |



 

 

 
