---
title: Tipo simple de LengthType
description: Define un tipo de longitud que se usa para especificar el número de bytes o caracteres de un elemento de datos de longitud variable, como datos binarios o una cadena ANSI o Unicode.
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- LengthType de tipo simple de registro
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dbb0720c2e26fa73056ccffdd17392e93e491c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359839"
---
# <a name="lengthtype-simple-type"></a>Tipo simple de LengthType

Define un tipo de longitud que se usa para especificar el número de bytes o caracteres de un elemento de datos de longitud variable, como datos binarios o una cadena ANSI o Unicode. El valor se puede especificar como un valor XS: unsignedShort o como una cadena que hace referencia al nombre del nodo elemento de datos que contiene el valor Short sin signo.

``` syntax
<xs:simpleType name="LengthType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





