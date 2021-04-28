---
description: 'Tipo simple CSymbolType (contadores de rendimiento): define un nombre de símbolo de C/C++ válido.'
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Tipo simple CSymbolType (contadores de rendimiento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0771bb1dffc006abf8e02e6c391278f7d0b03f11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084233"
---
# <a name="csymboltype-simple-type-performance-counters"></a>Tipo simple CSymbolType (contadores de rendimiento)

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

El **tipo simple CSymbolType** es **un xs:string** que está restringido por el siguiente patrón:

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    El nombre del símbolo puede estar vacío o contener caracteres alfanuméricos y caracteres de subrayado. Si especifica un nombre, el nombre debe comenzar con un carácter de subrayado ( \_ ) o un carácter alfabético.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




