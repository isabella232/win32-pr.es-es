---
title: Tipo simple CSymbolType (Windows de eventos)
description: 'Tipo simple CSymbolType (Windows de eventos): define un nombre de símbolo de C/C++ válido.'
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- CSymbolType de tipo simple EventLog
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0c8c17a9f4bb7e86b573d60187ffffd55c6cb96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967919"
---
# <a name="csymboltype-simple-type-windows-event-log"></a>Tipo simple CSymbolType (Windows de eventos)

Define un nombre de símbolo de C/C++ válido.

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El **tipo simple CSymbolType** es **un xs:string** restringido por el siguiente patrón:

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    El nombre del símbolo puede estar vacío o contener caracteres alfanuméricos y caracteres de subrayado. Si el nombre está vacío, el compilador del mensaje generará el nombre del símbolo. Si especifica un nombre, el nombre debe comenzar con un carácter de subrayado ( \_ ) o un carácter alfabético.

## <a name="remarks"></a>Observaciones

Si el nombre del símbolo está vacío, el compilador del mensaje usa el atributo **name** del elemento que se va a definir para generar el nombre del símbolo. El compilador reemplaza los caracteres no alfanuméricos y los dígitos iniciales por caracteres de subrayado. Por ejemplo, si el  atributo name del canal es Microsoft-Windows-SampleProvider/Operational, el compilador usaría Microsoft Windows SampleProvider Operational como nombre del \_ \_ \_ símbolo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



 

 





