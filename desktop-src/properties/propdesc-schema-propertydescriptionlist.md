---
description: Contenedor de uno o varios elementos propertyDescription individuales.
ms.assetid: b54aaa85-6928-470e-9630-44b094205106
title: propertyDescriptionList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd0beaf4dbbd8b71c7f4b3335c169754c704d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648285"
---
# <a name="propertydescriptionlist"></a>propertyDescriptionList

Contenedor de uno o varios elementos [propertyDescription](./propdesc-schema-propertydescription.md) individuales. Un archivo de esquema de descripción de la propiedad. propDesc debe contener al menos un elemento [propertyDescriptionList]() .

## <a name="syntax"></a>Sintaxis


```
<!-- propertyDescriptionList -->
<xs:element name="propertyDescriptionList">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="s:propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string" use="required"/>
        <xs:attribute name="product"   type="xs:string" use="required"/>
    </xs:complexType>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_formatid_and_propid">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@formatID"/>
        <xs:field    xpath="@propID"/>
    </xs:unique>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_canonical_name">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@name"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                        | Elementos secundarios                                                   |
|---------------------------------------|------------------------------------------------------------------|
| [schema](./propdesc-schema-entry.md) | [propertyDescription](./propdesc-schema-propertydescription.md) |



 

## <a name="attributes"></a>Atributos



| Atributo | Descripción                                                               |
|-----------|---------------------------------------------------------------------------|
| publisher | Público. Obligatorio. El nombre para mostrar del publicador que proporciona el esquema. |
| product   | Público. Obligatorio. Nombre para mostrar del producto que proporciona el esquema.   |



 

## <a name="remarks"></a>Observaciones

[PropertyDescriptionList]() no se debe confundir con "listas de propiedades" y [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), que son completamente independientes.

 

 
