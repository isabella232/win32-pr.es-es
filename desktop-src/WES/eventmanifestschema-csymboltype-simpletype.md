---
title: Tipo simple CSymbolType (registro de eventos de Windows)
description: Define un nombre de símbolo de C/C++ válido.
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- CSymbolType de tipo simple de registro
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67b0ccb7c573aa4d71c038f9133cea7c95cdfbd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695925"
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

El tipo simple **CSymbolType** es **xs: String** , que está restringido por el patrón siguiente:

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    El nombre del símbolo puede estar vacío o contener caracteres alfanuméricos y caracteres de subrayado. Si el nombre está vacío, el compilador de mensajes generará el nombre del símbolo. Si especifica un nombre, el nombre debe comenzar con un carácter de subrayado ( \_ ) o alfabético.

## <a name="remarks"></a>Observaciones

Si el nombre del símbolo está vacío, el compilador de mensajes utiliza el atributo de **nombre** del elemento que está definiendo para generar el nombre del símbolo. El compilador reemplaza los caracteres no alfanuméricos y los dígitos iniciales por caracteres de subrayado. Por ejemplo, si el atributo de **nombre** del canal es Microsoft-Windows-SampleProvider/Operational, el compilador usaría Microsoft \_ Windows \_ SampleProvider \_ Operational como el nombre del símbolo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



 

 





