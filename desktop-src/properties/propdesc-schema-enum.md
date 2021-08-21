---
description: Se usa para asignar texto enumerado a valores discretos.
ms.assetid: c8cc040e-fcce-43a0-98c1-db2b2c616ac3
title: enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1336a690fe7ac1e19a8606912a4f7d538d3842ab6a490d17b89f90f64bbfbc13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970984"
---
# <a name="enum"></a>enum

Se usa para asignar texto enumerado a valores discretos. Cualquier número de estos elementos puede existir en [enumeratedList.](./propdesc-schema-enumeratedlist.md) Mediante programación, se representan como objetos IPropertyEnumType, cuyo método [**IPropertyEnumType::GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) devuelve PET \_ DISCRETEVALUE.

## <a name="syntax"></a>Syntax


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
| value     | Público. Obligatorio. Valor discreto (cadena o número) al que se va a asignar texto enumerado.                                                                                                                           |
| texto      | Público. Obligatorio. Texto utilizado para mostrar el valor enumerado. La sintaxis permite una cadena de presentación directa o una referencia de cadena de presentación indirecta; use la cadena de presentación indirecta para que se pueda localizar. |
| teclas de acceso | **Windows 7 y versiones posteriores.** Público. Opcional. Lista de valores mnemotécnicos que se pueden usar para hacer referencia a la propiedad en las consultas de búsqueda. La lista está delimitada por el carácter \| ''.                                     |



 

 

 
