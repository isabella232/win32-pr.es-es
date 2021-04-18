---
description: Especifica el tipo de credenciales utilizado para la autenticación.
ms.assetid: a56ce888-ec07-4ce8-a540-6d1890cb338d
title: Elemento authMode (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d699b27746226c3eb1550cfd9250e229b40a22e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687432"
---
# <a name="authmode-onex-element"></a>Elemento authMode (OneX)

El elemento authMode (OneX) especifica el tipo de credenciales que se usan para la autenticación. La siguiente tabla describe los posibles valores.



| Value         | Descripción                                                                                                                                                             |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| machineOrUser | Usar credenciales de equipo o de usuario. Cuando un usuario ha iniciado sesión, se usan las credenciales del usuario para la autenticación. Cuando ningún usuario ha iniciado sesión, se usan las credenciales del equipo. |
| equipo       | Usar solo credenciales de equipo.                                                                                                                                           |
| usuario          | Usar solo credenciales de usuario.                                                                                                                                              |
| guest         | Usar solo credenciales de invitado (vacío).                                                                                                                                     |



 

Este elemento es opcional. Cuando authMode no se especifica en un perfil, se usa un valor de `machineOrUser` .

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.

``` syntax
<xs:element name="authMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="machineOrUser"
             />
            <xs:enumeration
                value="machine"
             />
            <xs:enumeration
                value="user"
             />
            <xs:enumeration
                value="guest"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento **authMode** se define mediante el elemento [**Onex**](onexschema-onex-element.md) .

## <a name="remarks"></a>Observaciones

Este parámetro se puede establecer en la línea de comandos mediante el comando **netsh wlan set ProfileParameter** Para obtener más información, consulte [comandos Netsh para red de área local inalámbrica (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Onex-**](onexschema-onex-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Onex-**](onexschema-onex-element.md)
</dt> </dl>

 

 
