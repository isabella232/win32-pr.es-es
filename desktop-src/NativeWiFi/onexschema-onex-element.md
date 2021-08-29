---
description: Especifica información de configuración 802.1X para un perfil de LAN cableada o inalámbrica.
ms.assetid: 4528fcb5-ee8e-4824-a69e-8d67622c4b4d
title: Elemento OneX
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2a0a58d4f06b30004620f7e222cdbf8a439c9bb57ab4f7ca97e3b86eaacb2e3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684875"
---
# <a name="onex-element"></a>Elemento OneX

El elemento OneX especifica información de configuración 802.1X para un perfil de LAN cableada o inalámbrica. Este elemento es el elemento raíz único para un perfil 802.1X.

El espacio de nombres de destino para el elemento OneX es `https://www.microsoft.com/networking/OneX/v1` . La mayoría de los elementos secundarios del elemento OneX están en el espacio de `OneX` nombres . Hay una excepción: el [**elemento EAPConfig**](onexschema-eapconfig-onex-element.md) está en el espacio de `https://www.microsoft.com/provisioning/EapHostConfig` nombres .

**Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** Solo se [**admite el elemento EAPConfig.**](onexschema-eapconfig-onex-element.md) Se omitirán otros elementos, si están presentes en un perfil.

``` syntax
<xs:element name="OneX">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="cacheUserData"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="heldPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="startPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxStart"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxAuthFailures"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="supplicantMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="inhibitTransmission"
                         />
                        <xs:enumeration
                            value="includeLearning"
                         />
                        <xs:enumeration
                            value="compliant"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authMode"
                minOccurs="0"
            >
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
            <xs:element name="singleSignOn"
                minOccurs="0"
            >
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
            <xs:element name="EAPConfig">
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            minOccurs="1"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                            | Tipo    | Descripción                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authMode**](onexschema-authmode-onex-element.md)                               |         | Especifica el tipo de credenciales usadas para la autenticación.<br/>                                                                                                                                                        |
| [**authPeriod**](onexschema-authperiod-onex-element.md)                           |         | Especifica el tiempo máximo, en segundos, en el que un cliente espera una respuesta del autenticador.<br/>                                                                                                  |
| [**cacheUserData**](onexschema-cacheuserdata-onex-element.md)                     | boolean | Especifica si las credenciales de usuario se almacenan en caché para las conexiones posteriores.<br/>                                                                                                                                     |
| [**EAPConfig**](onexschema-eapconfig-onex-element.md)                             |         | Especifica la configuración de EAPHost.<br/>                                                                                                                                                                              |
| [**heldPeriod**](onexschema-heldperiod-onex-element.md)                           |         | Especifica el período de tiempo, en segundos, en el que un cliente no volverá a intentar la autenticación después de un intento de autenticación con errores.<br/>                                                                             |
| [**maxAuthFailures**](onexschema-maxauthfailures-onex-element.md)                 |         | Especifica el número máximo de errores de autenticación permitidos para un conjunto de credenciales.<br/>                                                                                                                         |
| [**maxDelay**](onexschema-maxdelay-singlesignon-element.md)                       |         | Especifica, en segundos, el retraso máximo antes de que se produce un error en el intento de conexión de inicio de sesión único.<br/>                                                                                                                      |
| [**maxStart**](onexschema-maxstart-onex-element.md)                               |         | Especifica el número máximo de mensajes EAPOL-Start enviados.<br/>                                                                                                                                                        |
| [**singleSignOn**](onexschema-singlesignon-onex-element.md)                       |         | Especifica la información de configuración de red de inicio de sesión único.<br/>                                                                                                                                                       |
| [**startPeriod**](onexschema-startperiod-onex-element.md)                         |         | Especifica el período de tiempo, en segundos, que se debe esperar antes de EAPOL-Start se envía una aplicación.<br/>                                                                                                                                  |
| [**supplicantMode**](onexschema-supplicantmode-onex-element.md)                   |         | Especifica el método de transmisión utilizado para los paquetes EAPOL.<br/>                                                                                                                                                      |
| [**tipo**](onexschema-type-singlesignon-element.md)                               |         | Especifica cuándo se realiza el inicio de sesión único. Cuando se establece en `preLogon` , el inicio de sesión único se realiza antes de que el usuario inicie sesión. Cuando se establece en `postLogon` , el inicio de sesión único se realiza inmediatamente después de que el usuario inicie sesión.<br/> |
| [**userBasedVirtualLan**](onexschema-userbasedvirtuallan-singlesignon-element.md) | boolean | Especifica si la LAN virtual (VLAN) usada por el dispositivo cambia en función de las credenciales del usuario.<br/>                                                                                                                   |



## <a name="remarks"></a>Comentarios

Para ver la lista de elementos secundarios en una estructura similar a un árbol, vea [OneX Schema Elements](onexschema-elements.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio SP3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



 

 




