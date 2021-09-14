---
description: La interfaz IScanProfileMgr proporciona métodos para crear, abrir, eliminar y administrar perfiles de examen.
ms.assetid: f57a71b7-750c-42a8-be73-229f0145d9d5
title: Interfaz de IScanProfileMgr (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 9f0762befdda272b91451dcca67c3f9560ad354e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251822"
---
# <a name="iscanprofilemgr-interface"></a>Interfaz de IScanProfileMgr

La **interfaz IScanProfileMgr** proporciona métodos para crear, abrir, eliminar y administrar perfiles de examen.

## <a name="members"></a>Members

La **interfaz IScanProfileMgr** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IScanProfileMgr también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IScanProfileMgr** tiene estos métodos.



| Método                                                                              | Descripción                                                                                                            |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md)                         | Crea un perfil de examen vacío y lo asocia a un analizador u otro elemento de WIA 2.0.<br/>                       |
| [**DeleteAllProfiles**](-wia-iscanprofilemgr-deleteallprofiles.md)                 | Elimina todos los perfiles de examen asociados al dispositivo especificado.<br/>                                         |
| [**DeleteAllProfilesForUser**](-wia-iscanprofilemgr-deleteallprofilesforuser.md)   | Elimina todos los perfiles de examen disponibles para el usuario en el sistema en el que se ejecuta la aplicación. <br/> |
| [**DeleteProfile**](-wia-iscanprofilemgr-deleteprofile.md)                         | Elimina el perfil de examen especificado.<br/>                                                                         |
| [**GetDefaultProfile**](-wia-iscanprofilemgr-getdefaultprofile.md)                 | Obtiene el perfil de examen predeterminado.<br/>                                                                              |
| [**GetNumProfiles**](-wia-iscanprofilemgr-getnumprofiles.md)                       | Obtiene el número de perfiles de examen creados para el usuario en el sistema en el que se ejecuta la aplicación.<br/> |
| [**GetNumProfilesforDeviceID**](-wia-iscanprofilemgr-getnumprofilesfordeviceid.md) | Obtiene el número de perfiles de examen del dispositivo.<br/>                                                            |
| [**GetProfiles**](-wia-iscanprofilemgr-getprofiles.md)                             | Obtiene todos los perfiles de examen disponibles para el usuario en el sistema en el que se ejecuta la aplicación.<br/>     |
| [**GetProfilesforDeviceID**](-wia-iscanprofilemgr-getprofilesfordeviceid.md)       | Obtiene todos los perfiles de examen asociados a un dispositivo.<br/>                                                        |
| [**OpenProfile**](-wia-iscanprofilemgr-openprofile.md)                             | Abre un perfil de examen que se ha guardado en el disco como un archivo XML.<br/>                                            |
| [**Actualizar**](-wia-iscanprofilemgr-refresh.md)                                     | Vuelve a enumerar todos los perfiles de examen del sistema.<br/>                                                          |
| [**SetDefault**](-wia-iscanprofilemgr-setdefault.md)                               | Establece el perfil de examen especificado como perfil predeterminado.<br/>                                                     |



 

## <a name="remarks"></a>Observaciones

Para crear un **objeto IScanProfileMgr,** use el [método CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con los parámetros siguientes:

``` syntax
CoCreateInstance(CLSID_ScanProfileMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IScanProfileMgr, ppv)
```

Si un perfil de examen se guarda mediante el método [**IScanProfile::Save,**](-wia-iscanprofile-save.md) se almacena como un archivo XML en %USERPROFILE% \\ Application Data Microsoft Document Center \\ \\ \\ UserScanProfiles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Scanprofilemgr.h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Esquema de perfil de examen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
