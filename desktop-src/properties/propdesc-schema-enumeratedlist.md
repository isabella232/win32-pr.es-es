---
description: 'Especifica cómo IPropertyDescription:: FormatForDisplay debe formatear el valor de la propiedad como una cadena.'
ms.assetid: 49ba57b8-3e08-425f-98b2-52ed2c41a488
title: enumeratedList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d098b47463b65c483be68eb7750da929df43cee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706348"
---
# <a name="enumeratedlist"></a>enumeratedList

Especifica cómo [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) debe formatear el valor de la propiedad como una cadena. También influye en cómo se puede agrupar la propiedad o en qué valores se muestran en la lista si "editControl" es un listblox. Esto solo es aplicable si <displayInfo displayType="Enumerated"> . Solo debe haber un elemento [enumeratedList]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .

Si hay varios elementos, se usa el último. Si no se proporciona ningún elemento [enumeratedList]() , los valores de atributo predeterminados se aplican a la descripción de la propiedad.

## <a name="syntax"></a>Sintaxis


```
<!-- enumeratedList -->
<xs:element name="enumeratedList"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="value" type="xs:string" use="required"/>
                    <xs:attribute name="text" type="xs:string" use="required"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="minValue" type="xs:integer" use="required"/>
                    <xs:attribute name="setValue" type="xs:integer"/>
                    <xs:attribute name="text" type="xs:string"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
        <xs:attribute name="defaultText" type="xs:string"/>
        <xs:attribute name="useValueForDefault" type="xs:boolean"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                   | Elementos secundarios                               |
|--------------------------------------------------|----------------------------------------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | [enum](./propdesc-schema-enum.md)           |
|                                                  | [enumRange](./propdesc-schema-enumrange.md) |



 

## <a name="attributes"></a>Atributos



| Atributo          | Descripción                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| defaultText        | Público. Opcional. Especifique el texto predeterminado que se va a usar si se asigna un valor a [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) que no se asigna a uno de los elementos enumerados de la lista. La sintaxis permite una cadena de presentación directa o una referencia de cadena de presentación indirecta; Use la referencia para que se pueda localizar.                              |
| useValueForDefault | Público. Opcional. Si se establece en "true", se informará a [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) de usar el valor tal cual si el valor no se asigna a uno de los elementos enumerados de la lista. En el caso de **IPropertyDescription:: FormatForDisplay**, si se establece en "true" tiene prioridad sobre la configuración de "defaultText". El valor predeterminado es "false". |



 

 

 
