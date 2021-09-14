---
description: Permisos nativos de la API Wifi
ms.assetid: cfea9f7d-a069-497b-8138-b3949002fa5d
title: Permisos nativos de la API Wifi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da56faac08b40ace46ef1e33c5d5644be87b45c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069466"
---
# <a name="native-wifi-api-permissions"></a>Permisos nativos de la API Wifi

Se puede producir un error en una llamada a la API De Wifi nativa cuando un autor de la llamada no tiene los permisos adecuados para realizar la operación solicitada.

Los permisos se almacenan en una lista de control de acceso [discrecional (DACL)](../secauthz/access-control-lists.md) asociada a [**un objeto \_ SECURABLE \_ OBJECT de WLAN.**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object) Para obtener más información sobre las DACL y los objetos protegibles, vea Cómo controlan las [DACL el acceso a un objeto](../secauthz/how-dacls-control-access-to-an-object.md).

En la tabla siguiente se muestran las funciones wi-fi nativas que usan objetos protegibles para determinar si el autor de la llamada tiene permisos suficientes para realizar la operación solicitada. También muestra los objetos protegibles utilizados por cada función.




| Función | Objeto protegible | 
|----------|------------------|
| <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>WlanSetFilterList</strong></a><br /> | <ul><li>wlan_secure_deny_list</li><li>wlan_secure_permit_list</li></ul> | 
| <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a><br /> | <ul><li>wlan_secure_ihv_control</li></ul> | 
| <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>WlanSetAutoConfigParameter</strong></a><br /> | <ul><li>wlan_secure_show_denied</li></ul> | 
| <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>WlanSetInterface</strong></a><br /> | <ul><li>wlan_secure_ac_enabled</li><li>wlan_secure_bc_scan_enabled</li><li>wlan_secure_bss_type</li><li>wlan_secure_current_operation_mode</li><li>wlan_secure_interface_properties</li><li>wlan_secure_media_streaming_mode_enabled</li></ul> | 
| <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a><br /> | <ul><li>wlan_secure_add_new_all_user_profiles</li><li>wlan_secure_add_new_per_user_profiles</li></ul> | 
| <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>WlanSetProfilePosition</strong></a><br /> | <ul><li>wlan_secure_all_user_profiles_order</li></ul> | 




 

Antes de que una de las funciones con nombre anterior complete su operación, la función recupera la DACL almacenada en el objeto protegible adecuado. A continuación, la función comprueba la DACL para ver si el autor de la llamada tiene permisos suficientes. Las funciones WlanGet y WlanQuery requieren que la DACL contenga una entrada de control de acceso \* \* [(ACE)](../secauthz/access-control-entries.md) [](../secauthz/access-tokens.md) que conceda el token de acceso del subproceso de llamada WLAN READ ACCESS a \_ la \_ función. Las funciones WlanSet requieren una ACE que conceda el token de acceso del subproceso de llamada \* WLAN \_ WRITE \_ ACCESS. Si el autor de la llamada no tiene permisos suficientes, se produce el error ERROR ACCESS DENIED en la llamada de \_ \_ función.

Cada objeto protegible tiene una DACL asociada de forma predeterminada. Los permisos predeterminados almacenados en dacl se pueden cambiar mediante la [**función WlanSetSecuritySettings.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) Para determinar los derechos de usuario efectivos necesarios para realizar una operación en un sistema determinado, llame a [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).

Todos los perfiles de usuario tienen permisos adicionales asociados al propio perfil. Los permisos en un perfil de usuario completo se establecen cuando se crea o modifica el perfil mediante [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) o [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile). El *parámetro strAllUserProfileSecurity* especifica los permisos necesarios para modificar un perfil, eliminar un perfil o conectarse a una red mediante un perfil. La eliminación o modificación de un perfil requiere el permiso WLAN \_ WRITE \_ ACCESS. La conexión a una red mediante un perfil requiere el permiso WLAN \_ EXECUTE \_ ACCESS.

**Windows XP con SP3 e API de LAN inalámbrica para Windows XP con SP2: ** No se admiten las funciones [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) y [**WlanSetSecuritySettings.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) No se usa el parámetro *strAllUserProfileSecurity.*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo controlan las DACL el acceso a un objeto](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**OBJETO \_ PROTEGIBLE DE WLAN \_**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
