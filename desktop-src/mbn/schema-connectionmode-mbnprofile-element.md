---
description: Especifica la configuración de conexión automática que se usará para un dispositivo de banda ancha móvil.
ms.assetid: 789016d5-47f1-4506-bcb9-1a4019d236fd
title: Elemento ConnectionMode (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectionMode
api_type:
- Schema
ms.openlocfilehash: d0f2290928fba4be65d39129017a171fbd3d1e66e6ebab715f616e4edec9b13e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607145"
---
# <a name="connectionmode-mbnprofile-element"></a>Elemento ConnectionMode (MBNProfile)

El **elemento ConnectionMode (MBNProfile)** especifica la configuración de conexión automática que se usará para un dispositivo de banda ancha móvil.

Este elemento puede tener uno de los siguientes valores.



| Valor       | Significado                                                                |
|-------------|------------------------------------------------------------------------|
| "manual"    | Nunca se conecte automáticamente a la red.                            |
| "auto"      | Conéctese siempre automáticamente a la red.                           |
| "inicio automático" | Conéctese automáticamente a la red, excepto cuando se encuentra en una red móvil. |



 

Este elemento puede tener un máximo de una repetición.

Esto es un elemento requerido.

``` syntax
<xs:element name="ConnectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="manual"
             />
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="auto-home"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El **elemento ConnectionMode** se define mediante el [**elemento MBNProfile.**](schema-mbnprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio aplicaciones para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




