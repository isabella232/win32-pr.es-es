---
description: Define el tipo que define los valores válidos para el atributo Type del elemento Content \[ Lector de \] diario.
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: Tipo simple ContentTypeType
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579493"
---
# <a name="contenttypetype-simple-type"></a>Tipo simple ContentTypeType

Define el tipo que define los valores válidos para el *atributo Type* del elemento Content Lector [de \[ diario. \]](content-element--journal-reader.md)

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

El **tipo simple ContentTypeType** es una cadena que está restringida por el siguiente patrón:

-   `Normal|Inert`

## <a name="remarks"></a>Observaciones

Los valores válidos son "Normal" e "Inert".

Si el tipo es "Inert", el contenido contenido es una página de diario que es el "fondo" de solo lectura o no editable del documento. Esto sucede cuando se crea un documento mediante el controlador Escritura de notas de Journal impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



 

 




