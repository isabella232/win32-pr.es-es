---
description: La interfaz IScanProfile representa un único perfil de examen y permite a las aplicaciones establecer y obtener las propiedades del perfil.
ms.assetid: 5cd76256-d64e-4934-8cc2-0a467c7e34a9
title: Interfaz IScanProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile
api_type:
- COM
api_location:
- Scanprofiles.idl
ms.openlocfilehash: 1de80ac23ffa3e2687e2e6d0449f7a273067d5899204c479f9b62e8571190d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450835"
---
# <a name="iscanprofile-interface"></a>Interfaz IScanProfile

La **interfaz IScanProfile** representa un único perfil de examen y permite a las aplicaciones establecer y obtener las propiedades del perfil.

## <a name="members"></a>Miembros

La **interfaz IScanProfile** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IScanProfile** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IScanProfile** tiene estos métodos.



| Método                                                     | Descripción                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAllPropIDs**](-wia-iscanprofile-getallpropids.md)   | Obtiene todos los iDs de propiedad disponibles en un perfil.<br/>                                                                                            |
| [**GetDeviceID**](-wia-iscanprofile-getdeviceid.md)       | Devuelve el identificador del dispositivo.<br/>                                                                                                            |
| [**GetGUID**](-wia-iscanprofile-getguid.md)               | Devuelve el GUID del perfil.<br/>                                                                                                         |
| [**GetItem**](-wia-iscanprofile-getitem.md)               | Obtiene el GUID de la categoría del elemento de WIA 2.0 al que está asociado el perfil.<br/>                                                   |
| [**GetName**](-wia-iscanprofile-getname.md)               | Obtiene el nombre descriptivo del perfil.<br/>                                                                                                   |
| [**GetNumPropIDS**](-wia-iscanprofile-getnumpropids.md)   | Obtiene el número de identificaciónes de propiedad de un perfil.<br/>                                                                                            |
| [**Getproperty**](-wia-iscanprofile-getproperty.md)       | Obtiene el valor de las propiedades secundarias especificadas en el `<Properties>` elemento de un perfil de examen.<br/>                                            |
| [**IsDefault**](-wia-iscanprofile-isdefault.md)           | Obtiene un valor que indica si el perfil es el perfil de examen predeterminado de un [**dispositivo IWiaItem2**](-wia-iwiaitem2.md) asociado.<br/> |
| [**RemoveProperty**](-wia-iscanprofile-removeproperty.md) | Quita una lista especificada de propiedades secundarias en el `<Properties>` elemento de un perfil de examen.<br/>                                            |
| [**Guardar**](-wia-iscanprofile-save.md)                     | Guarda los cambios en un perfil en el disco.<br/>                                                                                                      |
| [**SetItem**](-wia-iscanprofile-setitem.md)               | Establece el GUID de la categoría del elemento de WIA 2.0 al que está asociado el perfil.<br/>                                                       |
| [**SetName**](-wia-iscanprofile-setname.md)               | Establece el nombre descriptivo del perfil.<br/>                                                                                                   |
| [**Setproperty**](-wia-iscanprofile-setproperty.md)       | Establece el valor de las propiedades secundarias especificadas en el `<Properties>` elemento de un perfil de examen.<br/>                                            |



 

## <a name="remarks"></a>Comentarios

Cualquier [**dispositivo IWiaItem2**](-wia-iwiaitem2.md) puede tener un perfil de examen. Sin embargo, **los elementos IWiaItem2** de los tipos WIA CATEGORY FINISHED FILE y \_ \_ \_ WIA CATEGORY ROOT no pueden \_ tener \_ perfiles.

Si un perfil de examen se guarda mediante el método [**IScanProfile::Save,**](-wia-iscanprofile-save.md) se almacena como un archivo XML en %USERPROFILE% \\ Application Data Microsoft Document Center \\ \\ \\ UserScanProfiles.

Para crear una instancia de un **objeto IScanProfile,** use el [**método IScanProfileMgr::CreateProfile.**](-wia-iscanprofilemgr-createprofile.md) Para obtener una referencia a un perfil de examen que ya se ha guardado en el disco, use el [**método IScanProfileMgr::OpenProfile.**](-wia-iscanprofilemgr-openprofile.md)

Todos los perfiles de examen tienen los siguientes elementos: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , y `<Properties>` . El perfil predeterminado de un dispositivo también tiene un `<Default>` elemento .

Los `<ProfileGUID>` elementos y no se pueden cambiar después de crear el `<DeviceID>` perfil. Los valores del elemento `<ProfileName>` y del elemento se pueden cambiar después de crear el `<WiaItem>` perfil. El `<Default>` elemento se puede agregar o eliminar. Esto se puede hacer mediante programación con los métodos [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md)e [**IScanProfileMgr::SetDefault.**](-wia-iscanprofilemgr-setdefault.md) Los usuarios también pueden cambiar estas propiedades mediante el [**método IScanProfileUI::ScanProfileDialog.**](-wia-iscanprofileui-scanprofiledialog.md)

El `<Properties>` elemento contiene elementos `<Property>` secundarios. Úselos para agregar cualquier propiedad de dispositivo o elemento de WIA 2.0 al perfil. También puede desarrollar sus propios hijos de aducción de `<Property>` imágenes. Esto hace que el esquema de perfil de examen sea extensible. (Para obtener más información sobre cómo extender el esquema, vea [Definición](-wia-defining-custom-properties.md)de propiedades personalizadas , [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md)e [**IScanProfile::SetProperty).**](-wia-iscanprofile-setproperty.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                        |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Esquema de perfil de examen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
