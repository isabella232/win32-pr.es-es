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
ms.openlocfilehash: d2d517143a55c2bd732bb8f9c642697a7d50151ddb72fcffd13d978caef597b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593095"
---
# <a name="iscanprofilemgr-interface"></a>Interfaz IScanProfileMgr

La **interfaz IScanProfileMgr** proporciona métodos para crear, abrir, eliminar y administrar perfiles de examen.

## <a name="members"></a>Miembros

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
| [**GetNumProfilesforDeviceID**](-wia-iscanprofilemgr-getnumprofilesfordeviceid.md) | Obtiene el número de perfiles de examen para el dispositivo.<br/>                                                            |
| [**GetProfiles**](-wia-iscanprofilemgr-getprofiles.md)                             | Obtiene todos los perfiles de examen disponibles para el usuario en el sistema en el que se ejecuta la aplicación.<br/>     |
| [**GetProfilesforDeviceID**](-wia-iscanprofilemgr-getprofilesfordeviceid.md)       | Obtiene todos los perfiles de examen asociados a un dispositivo.<br/>                                                        |
| [**OpenProfile**](-wia-iscanprofilemgr-openprofile.md)                             | Abre un perfil de examen que se ha guardado en el disco como un archivo XML.<br/>                                            |
| [**Actualizar**](-wia-iscanprofilemgr-refresh.md)                                     | Vuelve a enumerar todos los perfiles de examen del sistema.<br/>                                                          |
| [**SetDefault**](-wia-iscanprofilemgr-setdefault.md)                               | Establece el perfil de examen especificado como perfil predeterminado.<br/>                                                     |



 

## <a name="remarks"></a>Comentarios

Para crear un **objeto IScanProfileMgr,** use el [método CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con los parámetros siguientes:

``` syntax
CoCreateInstance(CLSID_ScanProfileMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IScanProfileMgr, ppv)
```

Si un perfil de examen se guarda mediante el método [**IScanProfile::Save,**](-wia-iscanprofile-save.md) se almacena como un archivo XML en %USERPROFILE% \\ Application Data Microsoft Document Center \\ \\ \\ UserScanProfiles.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofilemgr.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Esquema de perfil de examen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
