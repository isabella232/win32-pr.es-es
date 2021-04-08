---
description: Define un nombre de símbolo de C/C++ válido.
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Tipo simple de CSymbolType (contadores de rendimiento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 418b5119046a89d93814ed8ac8bd427dc554bf26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001968"
---
# <a name="csymboltype-simple-type-performance-counters"></a>Tipo simple de CSymbolType (contadores de rendimiento)

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

    El nombre del símbolo puede estar vacío o contener caracteres alfanuméricos y caracteres de subrayado. Si especifica un nombre, el nombre debe comenzar con un carácter de subrayado ( \_ ) o alfabético.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




