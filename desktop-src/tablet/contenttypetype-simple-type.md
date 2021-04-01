---
description: Define el tipo que define los valores válidos para el atributo de tipo del lector de diario del elemento de contenido \[ \] .
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: Tipo simple de ContentTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContentTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 55297be38dfd75f9ca11bfb6213cd99d52d2a7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082804"
---
# <a name="contenttypetype-simple-type"></a>Tipo simple de ContentTypeType

Define el tipo que define los valores válidos para el atributo de *tipo* del [ \[ lector \] de diario del elemento de contenido](content-element--journal-reader.md).

``` syntax
<xs:simpleType name="ContentTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Normal|Inert"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El tipo simple **ContentTypeType** es una cadena restringida por el siguiente patrón:

-   `Normal|Inert`

## <a name="remarks"></a>Observaciones

Los valores válidos son "normal" y "inerte".

Si el tipo es "inerte", el contenido contenido es una página de diario que es el "fondo" de solo lectura/no editable para el documento. Esto ocurre cuando se crea un documento con el controlador de impresora Escritura de notas de Journal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



 

 




