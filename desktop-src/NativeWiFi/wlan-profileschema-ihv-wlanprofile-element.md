---
description: Contiene diversos valores para los proveedores de hardware independientes.
ms.assetid: 4ad8c991-7849-41d6-9852-1ecadc372a2d
title: Elemento IHV (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IHV
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d2d2902522c84ebe2939d42301a491521ac8a70f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687128"
---
# <a name="ihv-wlanprofile-element"></a>Elemento IHV (WLANProfile)

El elemento IHV (WLANProfile) contiene varias opciones de configuración para los proveedores de hardware independientes. Si un perfil incluye la configuración de seguridad de IHV, invalidará cualquier seguridad definida por Microsoft.

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.

``` syntax
<xs:element name="IHV"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUIHeader">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUI">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="3"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="type">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="1"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
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
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="security"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="useMSOneX"
                type="boolean"
                minOccurs="0"
             />
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

El elemento se define mediante el elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                             | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Conectividad**](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | Contiene la configuración de conectividad relacionada con IHV.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**OUI**](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | Contiene un hexBinary de 3 bytes que identifica el IHV.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | Identifica el IHV.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**bursátil**](wlan-profileschema-security-ihv-element.md)         |                                                                   | Contiene la configuración de seguridad específica de IHV. La configuración de seguridad de Microsoft y la configuración de seguridad de IHV son mutuamente excluyentes. El perfil completo no es válido si ambas opciones de seguridad están presentes.<br/>                                                                                                                                                                                            |
| [**automáticamente**](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | Contiene un hexBinary de 1 byte que se usa para diferenciar las NIC del mismo IHV.<br/>                                                                                                                                                                                                                                                                                                        |
| [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md)       | [boolean](/dotnet/api/system.boolean) | Especifica el origen de la configuración de seguridad de 802.1 X usada por un componente de seguridad IHV. Cuando [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) es true, los componentes de seguridad de IHV usan la configuración de 802.1 x definida por Microsoft. Cuando **useMSOneX** es false, los componentes de seguridad de IHV usan la configuración de 802.1 x suministrada por el proveedor. De forma predeterminada, **useMSOneX** es false. Este elemento es opcional.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
