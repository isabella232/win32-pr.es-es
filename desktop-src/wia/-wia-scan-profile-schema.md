---
description: El esquema del perfil de digitalización define un formato XML que se puede utilizar para almacenar las propiedades de los elementos de adquisición de imágenes de Windows (WIA), como escáneres y cámaras.
ms.assetid: e0848db3-652a-45be-a18b-99b82420c586
title: Esquema de análisis de perfil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331c52e933e1e6b771c477bdc8a38f1c5f749448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696514"
---
# <a name="scan-profile-schema"></a>Esquema de análisis de perfil

El esquema del perfil de digitalización define un formato XML que se puede utilizar para almacenar las propiedades de los elementos de adquisición de imágenes de Windows (WIA), como escáneres y cámaras. Estos archivos persistentes permiten a las aplicaciones proporcionar análisis automáticos sin necesidad de que los usuarios recuerden la configuración de las propiedades de los elementos.

Cualquier dispositivo de [**IWiaItem2**](-wia-iwiaitem2.md) puede tener un perfil de digitalización. Sin embargo, los elementos de **IWiaItem2** de tipos de la \_ categoría WIA \_ Finished \_ File y WIA \_ Category \_ root no pueden tener perfiles.

Los perfiles de examen se crean y se administran a través de las interfaces [**IScanProfile**](-wia-iscanprofile.md), [**IScanProfileMgr**](-wia-iscanprofilemgr.md)y [**IScanProfileUI**](-wia-iscanprofileui.md) . Los usuarios de la aplicación pueden modificar los perfiles de maneras limitadas mediante el método [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

Todos los perfiles de examen tienen los siguientes elementos: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , y `<Properties>` . El perfil predeterminado de un dispositivo también tiene un `<Default>` elemento.

El `<ProfileGUID>` elemento y el `<DeviceID>` elemento no se pueden cambiar una vez creado el perfil de digitalización. `<ProfileName>`Se pueden modificar los valores del elemento y el `<WiaItem>` elemento. `<Default>`Se puede Agregar o eliminar el elemento. Esto se puede hacer mediante programación con los métodos [**IScanProfile:: setName**](-wia-iscanprofile-setname.md), [**IScanProfile:: SetItem**](-wia-iscanprofile-setitem.md)y [**IScanProfileMgr:: SetDefault**](-wia-iscanprofilemgr-setdefault.md) . Los usuarios también pueden cambiar estas propiedades a través del método [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

El `<Properties>` elemento contiene `<Property>` elementos secundarios. Úselos para agregar cualquier elemento WIA o propiedad de dispositivo al perfil. También puede desarrollar su propia imagen adquisiciones `<Property>` elementos secundarios. Esto hace que el esquema de Perfil de análisis sea extensible. (Para obtener más información sobre cómo extender el esquema, vea [definir propiedades personalizadas](-wia-defining-custom-properties.md), [**IScanProfile:: GetProperty**](-wia-iscanprofile-getproperty.md)y [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md)).

Este es el esquema de Perfil de examen completo. A continuación se muestra un perfil de ejemplo.


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



Haga clic en **Mostrar ejemplo** para ver un perfil de ejemplo.


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

[**IScanProfile:: GetProperty**](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Constantes de propiedad de WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Definir propiedades personalizadas](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



