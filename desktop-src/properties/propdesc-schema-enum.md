---
description: Se usa para asignar texto enumerado a valores discretos.
ms.assetid: c8cc040e-fcce-43a0-98c1-db2b2c616ac3
title: enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b615697e669f8d02e0530a1763309cfe74113467
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268268"
---
# <a name="enum"></a>enum

Se usa para asignar texto enumerado a valores discretos. Cualquier número de estos elementos puede existir en [enumeratedList.](./propdesc-schema-enumeratedlist.md) Mediante programación, se representan como objetos IPropertyEnumType, cuyo método [**IPropertyEnumType::GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) devuelve PET \_ DISCRETEVALUE.

## <a name="syntax"></a>Sintaxis


```
<!-- enum -->
<xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="value" type="xs:string" use="required"/>
        <xs:attribute name="text" type="xs:string" use="required"/>
        <xs:attribute name="mnemonics" type="xs:string"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                         | Elementos secundarios |
|--------------------------------------------------------|----------------|
| [enumeratedList](./propdesc-schema-enumeratedlist.md) | ninguno           |



 

## <a name="attributes"></a>Atributos



| Atributo | Descripción                                                                                                                                                                                                          |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| value     | Público. Necesario. Valor discreto (cadena o número) al que se va a asignar texto enumerado.                                                                                                                           |
| text      | Público. Necesario. Texto utilizado para mostrar el valor enumerado. La sintaxis permite una cadena de presentación directa o una referencia de cadena de presentación indirecta; use la cadena de presentación indirecta para que se pueda localizar. |
| teclas de acceso | **Windows 7 y versiones posteriores.** Público. Opcional. Lista de valores mnemotécnicos que se pueden usar para hacer referencia a la propiedad en las consultas de búsqueda. La lista está delimitada por el carácter \| ''.                                     |



 

 

 
