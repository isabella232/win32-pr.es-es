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
ms.openlocfilehash: 661306cf53b1ae4c7c9cd49a295afe5b84dabd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154472"
---
# <a name="profilecreationtype-mbnprofile-element"></a>Elemento ProfileCreationType (MBNProfile)

El elemento **ProfileCreationType (MBNProfile)** contiene información sobre el creador del perfil.

Este elemento puede tener uno de los valores siguientes.



| Value                 | Significado                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| "UserProvisioned"     | Este perfil se crea con la información proporcionada por el usuario del dispositivo.                                                     |
| "AdminProvisioned"    | Este perfil lo crean los administradores de ti y se distribuyen a los usuarios.                                                     |
| "OperatorProvisioned" | Este perfil lo crea un operador de red y se distribuye a los usuarios.                                                    |
| "DeviceProvisioned"   | El servicio de banda ancha móvil crea este perfil mediante la información almacenada en el contexto aprovisionado del dispositivo. |



 

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

El elemento **ProfileCreationType** se define mediante el elemento [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
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

 

 




