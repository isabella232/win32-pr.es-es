---
description: Contiene información sobre el creador del perfil.
ms.assetid: a3adb323-d1de-4026-976e-a106007f4cc2
title: Elemento ProfileCreationType (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProfileCreationType
api_type:
- Schema
ms.openlocfilehash: ddf3e70607cedbaed45da19651ec73736a54bfafab197e95d2cd634d8e3833f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959845"
---
# <a name="profilecreationtype-mbnprofile-element"></a>Elemento ProfileCreationType (MBNProfile)

El **elemento ProfileCreationType (MBNProfile)** contiene información sobre el creador del perfil.

Este elemento puede tener uno de los siguientes valores.



| Value                 | Significado                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| "UserProvisioned"     | Este perfil se crea mediante la información proporcionada por el usuario del dispositivo.                                                     |
| "AdminProvisioned"    | Los administradores de TI crean este perfil y se distribuyen a los usuarios.                                                     |
| "OperatorProvisioned" | Este perfil lo crea un operador de red y se distribuye a los usuarios.                                                    |
| "DeviceProvisioned"   | El servicio banda ancha móvil crea este perfil mediante la información almacenada en el contexto aprovisionado del dispositivo. |



 

Este elemento es opcional.

``` syntax
<xs:element name="ProfileCreationType">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="UserProvisioned"
             />
            <xs:enumeration
                value="AdminProvisioned"
             />
            <xs:enumeration
                value="OperatorProvisioned"
             />
            <xs:enumeration
                value="DeviceProvisioned"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El **elemento ProfileCreationType** se define mediante el [**elemento MBNProfile.**](schema-mbnprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/> |
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

 

 




