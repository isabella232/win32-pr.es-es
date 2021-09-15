---
description: Especifica si un usuario puede crear un perfil de usuario único.
ms.assetid: b9bdfe85-b9d5-4dcc-a7f8-05cce9702ec3
title: elemento allowEveryoneToCreateAllUserProfiles (globalFlags)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowEveryoneToCreateAllUserProfiles
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 63bc4c76ccecd8c7f774dc0e73621ef3f9b19877
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473715"
---
# <a name="alloweveryonetocreatealluserprofiles-globalflags-element"></a>elemento allowEveryoneToCreateAllUserProfiles (globalFlags)

El **elemento allowEveryoneToCreateAllUserProfiles** (globalFlags) especifica si un usuario puede crear un perfil de usuario completo. Cualquier usuario de la máquina puede usar un perfil de todos los usuarios para conectarse a la red inalámbrica asociada al perfil.

Si **allowEveryoneToCreateAllUserProfiles** es TRUE, cualquier usuario puede crear un perfil de todos los usuarios. Si **allowEveryoneToCreateAllUserProfiles** es FALSE, no todos los usuarios pueden crear un perfil de usuario completo y hay una DACL asociada con el objeto de seguridad agregar todos los perfiles de usuario nuevos que especifique los usuarios o grupos de usuarios con permiso para crear perfiles de todos los \_ \_ \_ \_ \_ \_ usuarios. La DACL predeterminada especifica que solo los usuarios que han iniciado sesión como miembros del grupo Administradores pueden crear un perfil de todos los usuarios. La configuración de seguridad predeterminada se puede cambiar mediante una llamada [**a WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings). Para obtener la configuración de seguridad actual, llame [**a WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).

Este elemento es obligatorio. Cuando el servicio AutoConfig crea un perfil, este elemento tendrá el valor predeterminado TRUE.

``` syntax
<xs:element name="allowEveryoneToCreateAllUserProfiles"
    type="boolean"
 />
```

El elemento [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) define el elemento **allowEveryoneToCreateAllUserProfiles.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




