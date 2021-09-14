---
description: Especifica el tipo de credenciales usadas para la autenticación.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169462"
---
# <a name="authmode-onex-element"></a>Elemento authMode (OneX)

El elemento authMode (OneX) especifica el tipo de credenciales usadas para la autenticación. La siguiente tabla describe los posibles valores.



| Value         | Descripción                                                                                                                                                             |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| machineOrUser | Use credenciales de equipo o usuario. Cuando un usuario ha iniciado sesión, las credenciales del usuario se usan para la autenticación. Cuando ningún usuario ha iniciado sesión, se usan las credenciales del equipo. |
| equipo       | Use solo credenciales de máquina.                                                                                                                                           |
| usuario          | Use solo credenciales de usuario.                                                                                                                                              |
| guest         | Use solo credenciales de invitado (vacías).                                                                                                                                     |



 

Este elemento es opcional. Cuando no se especifica authMode en un perfil, se usa `machineOrUser` un valor de .

**Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.

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

El **elemento authMode** se define mediante el [**elemento OneX.**](onexschema-onex-element.md)

## <a name="remarks"></a>Observaciones

Este parámetro se puede establecer en la línea de comandos mediante el **comando netsh wlan set profileparameter.** Para obtener más información, [vea Netsh Commands for Wireless Local Area Network (wlan) (Comandos netsh para redes inalámbricas de área local [wlan]).](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 
