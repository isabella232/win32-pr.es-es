---
title: Tipo simple CSymbolType (registro de eventos de Windows)
description: 'Tipo simple CSymbolType (registro de eventos de Windows): define un nombre de símbolo de C/C++ válido.'
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- Tipo simple EventLog de CSymbolType
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
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090623"
---
# <a name="csymboltype-simple-type-windows-event-log"></a>Tipo simple CSymbolType (registro de eventos de Windows)

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

## <a name="remarks"></a>Comentarios

Si el nombre del símbolo está vacío, el compilador del mensaje usa el atributo **name** del elemento que se va a definir para generar el nombre del símbolo. El compilador reemplaza los caracteres no alfanuméricos y los dígitos iniciales por caracteres de subrayado. Por ejemplo, si el  atributo name del canal es Microsoft-Windows-SampleProvider/Operational, el compilador usaría Microsoft Windows SampleProvider Operational como \_ nombre del \_ \_ símbolo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]<br/> |



 

 





