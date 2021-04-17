---
description: Especifica la información de configuración de red de inicio de sesión único (SSO).
ms.assetid: c0a26f15-77fd-43e9-a6af-54e9b46f03fa
title: Elemento singleSignOn (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- singleSignOn
api_type:
- Schema
api_location: ''
ms.openlocfilehash: fd25767ed311e9a6f0e75f8dec090d4b80d3f0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677749"
---
# <a name="singlesignon-onex-element"></a>Elemento singleSignOn (OneX)

El elemento singleSignOn (OneX) especifica la información de configuración de red de inicio de sesión único (SSO).

Este elemento es opcional. No use el elemento singleSignOn en un perfil si la red no lo requiere.

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.

``` syntax
<xs:element name="singleSignOn">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="type"
                minOccurs="1"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="preLogon"
                         />
                        <xs:enumeration
                            value="postLogon"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxDelay"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="0"
                         />
                        <xs:enumeration
                            value="120"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="userBasedVirtualLan"
                type="boolean"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

El elemento **singleSignOn** se define mediante el elemento [**Onex**](onexschema-onex-element.md) .

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                            | Tipo    | Descripción                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**maxDelay**](onexschema-maxdelay-singlesignon-element.md)                       |         | Especifica, en segundos, el retraso máximo antes de que se produzca un error en el intento de conexión de inicio de sesión único.<br/>                                                                                                                      |
| [**automáticamente**](onexschema-type-singlesignon-element.md)                               |         | Especifica cuándo se realiza el inicio de sesión único. Cuando se establece en `preLogon` , se realiza el inicio de sesión único antes de que el usuario inicie sesión. Cuando se establece en `postLogon` , el inicio de sesión único se realiza inmediatamente después de que el usuario inicie sesión.<br/> |
| [**userBasedVirtualLan**](onexschema-userbasedvirtuallan-singlesignon-element.md) | boolean | Especifica si la LAN virtual (VLAN) usada por el dispositivo cambia en función de las credenciales del usuario.<br/>                                                                                                                   |



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

 

 
