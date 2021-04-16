---
description: La interfaz IScanProfile representa un único Perfil de examen y permite a las aplicaciones establecer y obtener las propiedades del perfil.
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
ms.openlocfilehash: 2e02352eef16a9b899e4c635f11c5d10b3ab5113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706320"
---
# <a name="iscanprofile-interface"></a>Interfaz IScanProfile

La interfaz **IScanProfile** representa un único Perfil de examen y permite a las aplicaciones establecer y obtener las propiedades del perfil.

## <a name="members"></a>Miembros

La interfaz **IScanProfile** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IScanProfile** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IScanProfile** tiene estos métodos.



| Método                                                     | Descripción                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAllPropIDs**](-wia-iscanprofile-getallpropids.md)   | Obtiene todos los identificadores de propiedad disponibles en un perfil.<br/>                                                                                            |
| [**GetDeviceID**](-wia-iscanprofile-getdeviceid.md)       | Devuelve el identificador del dispositivo.<br/>                                                                                                            |
| [**GetGUID**](-wia-iscanprofile-getguid.md)               | Devuelve el GUID del perfil.<br/>                                                                                                         |
| [**GetItem**](-wia-iscanprofile-getitem.md)               | Obtiene el GUID de la categoría del elemento de WIA 2,0 con el que está asociado el perfil.<br/>                                                   |
| [**GetName**](-wia-iscanprofile-getname.md)               | Obtiene el nombre descriptivo del perfil.<br/>                                                                                                   |
| [**GetNumPropIDS**](-wia-iscanprofile-getnumpropids.md)   | Obtiene el número de identificadores de propiedad de un perfil.<br/>                                                                                            |
| [**GetProperty**](-wia-iscanprofile-getproperty.md)       | Obtiene el valor de las propiedades secundarias especificadas en el `<Properties>` elemento de un perfil de digitalización.<br/>                                            |
| [**IsDefault**](-wia-iscanprofile-isdefault.md)           | Obtiene un valor que indica si el perfil es el perfil de detección predeterminado de un dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) asociado.<br/> |
| [**RemoveProperty**](-wia-iscanprofile-removeproperty.md) | Quita una lista especificada de propiedades secundarias en el `<Properties>` elemento de un perfil de digitalización.<br/>                                            |
| [**Guardar**](-wia-iscanprofile-save.md)                     | Guarda los cambios en un perfil en el disco.<br/>                                                                                                      |
| [**SetItem**](-wia-iscanprofile-setitem.md)               | Establece el GUID de la categoría del elemento de WIA 2,0 al que está asociado el perfil.<br/>                                                       |
| [**SetName**](-wia-iscanprofile-setname.md)               | Establece el nombre descriptivo del perfil.<br/>                                                                                                   |
| [**SetProperty**](-wia-iscanprofile-setproperty.md)       | Establece el valor de las propiedades secundarias especificadas en el `<Properties>` elemento de un perfil de digitalización.<br/>                                            |



 

## <a name="remarks"></a>Observaciones

Cualquier dispositivo de [**IWiaItem2**](-wia-iwiaitem2.md) puede tener un perfil de digitalización. Sin embargo, los elementos de **IWiaItem2** de tipos de la \_ categoría WIA \_ Finished \_ File y WIA \_ Category \_ root no pueden tener perfiles.

Si un perfil de digitalización se guarda con el método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) , se almacena como un archivo XML en% userprofile% \\ Application Data \\ Microsoft \\ Document Center \\ UserScanProfiles.

Para crear una instancia de un objeto **IScanProfile** , use el método [**IScanProfileMgr:: CreateProfile**](-wia-iscanprofilemgr-createprofile.md) . Para obtener una referencia a un perfil de digitalización que ya se ha guardado en el disco, use el método [**IScanProfileMgr:: OpenProfile**](-wia-iscanprofilemgr-openprofile.md) .

Todos los perfiles de examen tienen los siguientes elementos: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , y `<Properties>` . El perfil predeterminado de un dispositivo también tiene un `<Default>` elemento.

Los `<ProfileGUID>` `<DeviceID>` elementos y no se pueden cambiar una vez creado el perfil. Los valores del `<ProfileName>` elemento y el `<WiaItem>` elemento se pueden cambiar una vez creado el perfil. `<Default>`Se puede Agregar o eliminar el elemento. Esto se puede hacer mediante programación con los métodos [**IScanProfile:: setName**](-wia-iscanprofile-setname.md), [**IScanProfile:: SetItem**](-wia-iscanprofile-setitem.md)y [**IScanProfileMgr:: SetDefault**](-wia-iscanprofilemgr-setdefault.md) . Los usuarios también pueden cambiar estas propiedades a través del método [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

El `<Properties>` elemento contiene `<Property>` elementos secundarios. Úselos para agregar cualquier propiedad de dispositivo o elemento de WIA 2,0 al perfil. También puede desarrollar su propia imagen adquisiciones `<Property>` elementos secundarios. Esto hace que el esquema de Perfil de análisis sea extensible. (Para obtener más información sobre cómo extender el esquema, vea [definir propiedades personalizadas](-wia-defining-custom-properties.md), [**IScanProfile:: GetProperty**](-wia-iscanprofile-getproperty.md)y [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                        |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Esquema de análisis de perfil](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
