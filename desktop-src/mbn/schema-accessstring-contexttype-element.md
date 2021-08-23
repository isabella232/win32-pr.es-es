---
description: Identifica el APN o la cadena de marcado que se va a usar para establecer una conexión de datos.
ms.assetid: e791ffa1-b417-480c-adb8-b1dda7547d89
title: Elemento AccessString (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AccessString
api_type:
- Schema
ms.openlocfilehash: 603c4aa04bb3e86891ec121233474fa96ffd792cbcb6880bad9e76599003d979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975284"
---
# <a name="accessstring-contexttype-element"></a>Elemento AccessString (contextType)

El **elemento AccessString (contextType)** identifica el APN o la cadena de marcado que se va a usar para establecer una conexión de datos.

Este elemento puede tener una longitud máxima de 100 caracteres.

Este elemento es opcional.

``` syntax
<xs:element name="AccessString">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El **elemento AccessString** se define mediante el [**tipo complejo contextType.**](schema-contexttype-complextype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Contexto (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




