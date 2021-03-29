---
description: Especifica si un usuario puede crear un perfil de todos los usuarios.
ms.assetid: b9bdfe85-b9d5-4dcc-a7f8-05cce9702ec3
title: Elemento allowEveryoneToCreateAllUserProfiles (Indicadores_globales)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541046"
---
# <a name="alloweveryonetocreatealluserprofiles-globalflags-element"></a>Elemento allowEveryoneToCreateAllUserProfiles (Indicadores_globales)

El elemento **allowEveryoneToCreateAllUserProfiles** (indicadores_globales) especifica si un usuario puede crear un perfil de todos los usuarios. Cualquier usuario del equipo puede usar un perfil de todos los usuarios para conectarse a la red inalámbrica asociada al perfil.

Si **allowEveryoneToCreateAllUserProfiles** es true, el usuario puede crear un perfil de todos los usuarios. Si **allowEveryoneToCreateAllUserProfiles** es false, no todos los usuarios pueden crear un perfil de todos los usuarios y existe una DACL asociada al \_ \_ objeto de seguridad agregar nuevo todos los perfiles de usuario de la WLAN \_ \_ \_ \_ que especifica los usuarios o grupos de usuarios con permiso para crear perfiles de todos los usuarios. La DACL predeterminada especifica que solo los usuarios que han iniciado sesión como miembro del grupo administradores pueden crear un perfil de todos los usuarios. La configuración de seguridad predeterminada se puede cambiar mediante una llamada a [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings). Para obtener la configuración de seguridad actual, llame a [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).

Este elemento es obligatorio. Cuando el servicio de configuración automática crea un perfil, este elemento tendrá el valor predeterminado TRUE.

``` syntax
<xs:element name="allowEveryoneToCreateAllUserProfiles"
    type="boolean"
 />
```

El elemento **allowEveryoneToCreateAllUserProfiles** se define mediante el elemento [**indicadores_globales**](wlan-policyschema-globalflags-wlanpolicy-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Indicadores**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Indicadores_globales (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




