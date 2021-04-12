---
description: Permisos de la API WiFi nativa
ms.assetid: cfea9f7d-a069-497b-8138-b3949002fa5d
title: Permisos de la API WiFi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afafec7619e0920a17e3769a430c8c79aeff3828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276706"
---
# <a name="native-wifi-api-permissions"></a>Permisos de la API WiFi nativa

Se puede producir un error en una llamada de la API WiFi nativa cuando un autor de llamada no tiene los permisos adecuados para realizar la operación solicitada.

Los permisos se almacenan en [listas de control de acceso discrecional (DACL)](../secauthz/access-control-lists.md) asociadas a un [**\_ \_ objeto protegible de WLAN**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object). Para obtener más información sobre las DACL y los objetos protegibles, vea [Cómo control de DACL el acceso a un objeto](../secauthz/how-dacls-control-access-to-an-object.md).

En la tabla siguiente se muestran las funciones WiFi nativas que usan objetos protegibles para determinar si el autor de la llamada tiene permisos suficientes para realizar la operación solicitada. También se muestran los objetos protegibles utilizados por cada función.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Función</th>
<th>Objeto protegible</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>WlanSetFilterList</strong></a><br/></td>
<td><ul>
<li>wlan_secure_deny_list</li>
<li>wlan_secure_permit_list</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a><br/></td>
<td><ul>
<li>wlan_secure_ihv_control</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>WlanSetAutoConfigParameter</strong></a><br/></td>
<td><ul>
<li>wlan_secure_show_denied</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>WlanSetInterface</strong></a><br/></td>
<td><ul>
<li>wlan_secure_ac_enabled</li>
<li>wlan_secure_bc_scan_enabled</li>
<li>wlan_secure_bss_type</li>
<li>wlan_secure_current_operation_mode</li>
<li>wlan_secure_interface_properties</li>
<li>wlan_secure_media_streaming_mode_enabled</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a><br/></td>
<td><ul>
<li>wlan_secure_add_new_all_user_profiles</li>
<li>wlan_secure_add_new_per_user_profiles</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>WlanSetProfilePosition</strong></a><br/></td>
<td><ul>
<li>wlan_secure_all_user_profiles_order</li>
</ul></td>
</tr>
</tbody>
</table>



 

Antes de que una de las funciones con nombre anterior complete su funcionamiento, la función recupera la DACL almacenada en el objeto protegible adecuado. A continuación, la función comprueba la DACL para ver si el autor de la llamada tiene permisos suficientes. Las \* funciones WlanGet y WlanQuery \* requieren que la DACL contenga una [entrada de control de acceso (ACE)](../secauthz/access-control-entries.md) que conceda al [token de acceso](../secauthz/access-tokens.md) del subproceso de llamada \_ acceso de lectura \_ a la función. Las \* funciones WlanSet requieren una ACE que conceda el token de acceso del acceso de escritura de la WLAN del subproceso que realiza la llamada \_ \_ . Si el autor de la llamada no tiene permisos suficientes, se produce un error en la llamada a la función con el error \_ acceso \_ denegado.

Cada objeto protegible tiene una DACL asociada de forma predeterminada. Los permisos predeterminados almacenados en la DACL se pueden cambiar mediante la función [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) . Para determinar los derechos de usuario efectivos necesarios para realizar una operación en un sistema determinado, llame a [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).

Los perfiles de todos los usuarios tienen permisos adicionales asociados al propio perfil. Los permisos en un perfil de todos los usuarios se establecen cuando se crea o se modifica el perfil mediante [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) o [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile). El parámetro *strAllUserProfileSecurity* especifica los permisos necesarios para modificar un perfil, eliminar un perfil o conectarse a una red mediante un perfil. La eliminación o modificación de un perfil requiere el \_ permiso de acceso de escritura de WLAN \_ . La conexión a una red mediante un perfil requiere el permiso de acceso de ejecución de WLAN \_ \_ .

* * Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2: * * no se admiten las funciones [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) y [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) . No se usa el parámetro *strAllUserProfileSecurity* .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo controlan el acceso a un objeto las DACL](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**\_objeto protegible de WLAN \_**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
