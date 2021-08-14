---
description: El esquema de perfil de digitalización define un formato XML que se puede usar para almacenar las propiedades de los elementos de adquisición de imágenes de Windows (WIA), como escáneres y cámaras.
ms.assetid: e0848db3-652a-45be-a18b-99b82420c586
title: Esquema de perfil de examen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81091e75269206b6b3b5a89f86c6f92da5c1d2080d90382ac6af48c6d1cc32ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208021"
---
# <a name="scan-profile-schema"></a>Esquema de perfil de examen

El esquema de perfil de digitalización define un formato XML que se puede usar para almacenar las propiedades de los elementos de adquisición de imágenes de Windows (WIA), como escáneres y cámaras. Estos archivos persistentes permiten a las aplicaciones proporcionar análisis automático sin necesidad de que los usuarios recuerden la configuración de propiedades de los elementos.

Cualquier [**dispositivo IWiaItem2**](-wia-iwiaitem2.md) puede tener un perfil de examen. Sin embargo, **los elementos IWiaItem2** de los tipos WIA CATEGORY FINISHED FILE y \_ \_ \_ WIA CATEGORY ROOT no pueden \_ tener \_ perfiles.

Los perfiles de examen se crean y administran a través de las interfaces [**IScanProfile,**](-wia-iscanprofile.md) [**IScanProfileMgr**](-wia-iscanprofilemgr.md)e [**IScanProfileUI.**](-wia-iscanprofileui.md) Los usuarios de la aplicación pueden modificar perfiles de maneras limitadas mediante el [**método IScanProfileUI::ScanProfileDialog.**](-wia-iscanprofileui-scanprofiledialog.md)

Todos los perfiles de examen tienen los siguientes elementos: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , y `<Properties>` . El perfil predeterminado de un dispositivo también tiene un `<Default>` elemento .

El `<ProfileGUID>` elemento y el elemento no se pueden cambiar después de crear el perfil de `<DeviceID>` examen. Los valores del `<ProfileName>` elemento y del elemento se pueden `<WiaItem>` modificar. El `<Default>` elemento se puede agregar o eliminar. Esto se puede hacer mediante programación mediante los métodos [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md)e [**IScanProfileMgr::SetDefault.**](-wia-iscanprofilemgr-setdefault.md) Los usuarios también pueden cambiar estas propiedades mediante el [**método IScanProfileUI::ScanProfileDialog.**](-wia-iscanprofileui-scanprofiledialog.md)

El `<Properties>` elemento contiene elementos `<Property>` secundarios. Úselos para agregar cualquier elemento de WIA o propiedad de dispositivo al perfil. También puede desarrollar sus propios hijos de `<Property>` imagen. Esto hace que el esquema de perfil de examen sea extensible. (Para obtener más información sobre cómo extender el esquema, vea [Definición](-wia-defining-custom-properties.md)de propiedades personalizadas , [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md)e [**IScanProfile::SetProperty).**](-wia-iscanprofile-setproperty.md)

Este es el esquema de perfil de examen completo. A continuación se muestra un perfil de ejemplo.


```
<?xml version="1.0"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema"
            targetNamespace="https://www.microsoft.com"
            xmlns="https://www.microsoft.com"
            elementFormDefault="qualified">

<xs:element name="ScanProfile">
            <xs:complexType>
            <xs:sequence>
                        <xs:element name="ProfileGUID" type="xs:string"/>
                        <xs:element name="DeviceID" type="xs:string"/>
<xs:element name="ProfileName" type="xs:string"/>
                        <xs:element name="Default" minOccurs="0">
                                    <xs:complexType>
                                    </xs:complexType>
                        </xs:element>
                        <xs:element name="WiaItem" type="xs:string"/>
                        <xs:element name="Properties" type="Properties"/>
            </xs:sequence>
            </xs:complexType>
</xs:element>
 
<xs:complexType name="Properties">
<xs:sequence>
            <xs:element name="Property" maxOccurs="unbounded" minOccurs="0">
            <xs:complexType>
            <xs:simpleContent>
                        <xs:extension base="xs:string">
                                    <xs:attribute name="id" type="xs:integer" use="required"/>
                                    <xs:attribute name="type" type="xs:integer" use="required"/>
                        </xs:extension>
            </xs:simpleContent>
            </xs:complexType>
            </xs:element>
</xs:sequence>
</xs:complexType>
 
</xs:schema>
```



Haga **clic en Mostrar ejemplo** para ver un perfil de ejemplo.


```
<ScanProfile>
    <ProfileGUID>
        {F862E217-32B0-4396-987A-2191224925CD}
    </ProfileGUID>
    <DeviceID>
        {6BDD1FC6-810F-11D0-BEC7-08002BE2092F}\0001
    </DeviceID>
    <ProfileName>
        Last used settings
    </ProfileName>
    <WiaItem>
        {FB607B1F-43F3-488B-855B-FB703EC342A6}
    </WiaItem>
    <Properties>
        <Property id="4103" type="3">
            3
        </Property>
        <Property id="4106" type="72">
            {B96B3CAB-0728-11D3-9D7B-0000F81EF32E}
        </Property>
        <Property id="6147" type="3">
            300
        </Property>
        <Property id="6154" type="3">
            0
        </Property>
        <Property id="6155" type="3">
            0
        </Property>
    </Properties>
</ScanProfile>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Constantes de propiedad WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Definir propiedades personalizadas](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



