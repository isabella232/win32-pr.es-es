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
# <a name="native-wifi-api-permissions"></a><span data-ttu-id="bb963-103">Permisos de la API WiFi nativa</span><span class="sxs-lookup"><span data-stu-id="bb963-103">Native Wifi API Permissions</span></span>

<span data-ttu-id="bb963-104">Se puede producir un error en una llamada de la API WiFi nativa cuando un autor de llamada no tiene los permisos adecuados para realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="bb963-104">A Native Wifi API call may fail with when a caller does not have adequate permissions to perform the requested operation.</span></span>

<span data-ttu-id="bb963-105">Los permisos se almacenan en [listas de control de acceso discrecional (DACL)](../secauthz/access-control-lists.md) asociadas a un [**\_ \_ objeto protegible de WLAN**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object).</span><span class="sxs-lookup"><span data-stu-id="bb963-105">Permissions are stored in a [discretionary access control lists (DACL)](../secauthz/access-control-lists.md) associated with a [**WLAN\_SECURABLE\_OBJECT**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object).</span></span> <span data-ttu-id="bb963-106">Para obtener más información sobre las DACL y los objetos protegibles, vea [Cómo control de DACL el acceso a un objeto](../secauthz/how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="bb963-106">For more information about DACLs and securable objects, see [How DACLs Control Access to an Object](../secauthz/how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="bb963-107">En la tabla siguiente se muestran las funciones WiFi nativas que usan objetos protegibles para determinar si el autor de la llamada tiene permisos suficientes para realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="bb963-107">The following table shows the Native Wifi functions that use securable objects to determine if the caller has sufficient permissions to perform the requested operation.</span></span> <span data-ttu-id="bb963-108">También se muestran los objetos protegibles utilizados por cada función.</span><span class="sxs-lookup"><span data-stu-id="bb963-108">It also shows the securable objects used by each function.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb963-109">Función</span><span class="sxs-lookup"><span data-stu-id="bb963-109">Function</span></span></th>
<th><span data-ttu-id="bb963-110">Objeto protegible</span><span class="sxs-lookup"><span data-stu-id="bb963-110">Securable object</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb963-111"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>WlanSetFilterList</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb963-111"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"><strong>WlanSetFilterList</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="bb963-112">wlan_secure_deny_list</span><span class="sxs-lookup"><span data-stu-id="bb963-112">wlan_secure_deny_list</span></span></li>
<li><span data-ttu-id="bb963-113">wlan_secure_permit_list</span><span class="sxs-lookup"><span data-stu-id="bb963-113">wlan_secure_permit_list</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb963-114"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb963-114"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="bb963-115">wlan_secure_ihv_control</span><span class="sxs-lookup"><span data-stu-id="bb963-115">wlan_secure_ihv_control</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb963-116"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>WlanSetAutoConfigParameter</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb963-116"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"><strong>WlanSetAutoConfigParameter</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="bb963-117">wlan_secure_show_denied</span><span class="sxs-lookup"><span data-stu-id="bb963-117">wlan_secure_show_denied</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb963-118"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>WlanSetInterface</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb963-118"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"><strong>WlanSetInterface</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="bb963-119">wlan_secure_ac_enabled</span><span class="sxs-lookup"><span data-stu-id="bb963-119">wlan_secure_ac_enabled</span></span></li>
<li><span data-ttu-id="bb963-120">wlan_secure_bc_scan_enabled</span><span class="sxs-lookup"><span data-stu-id="bb963-120">wlan_secure_bc_scan_enabled</span></span></li>
<li><span data-ttu-id="bb963-121">wlan_secure_bss_type</span><span class="sxs-lookup"><span data-stu-id="bb963-121">wlan_secure_bss_type</span></span></li>
<li><span data-ttu-id="bb963-122">wlan_secure_current_operation_mode</span><span class="sxs-lookup"><span data-stu-id="bb963-122">wlan_secure_current_operation_mode</span></span></li>
<li><span data-ttu-id="bb963-123">wlan_secure_interface_properties</span><span class="sxs-lookup"><span data-stu-id="bb963-123">wlan_secure_interface_properties</span></span></li>
<li><span data-ttu-id="bb963-124">wlan_secure_media_streaming_mode_enabled</span><span class="sxs-lookup"><span data-stu-id="bb963-124">wlan_secure_media_streaming_mode_enabled</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb963-125"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb963-125"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="bb963-126">wlan_secure_add_new_all_user_profiles</span><span class="sxs-lookup"><span data-stu-id="bb963-126">wlan_secure_add_new_all_user_profiles</span></span></li>
<li><span data-ttu-id="bb963-127">wlan_secure_add_new_per_user_profiles</span><span class="sxs-lookup"><span data-stu-id="bb963-127">wlan_secure_add_new_per_user_profiles</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb963-128"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>WlanSetProfilePosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb963-128"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"><strong>WlanSetProfilePosition</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="bb963-129">wlan_secure_all_user_profiles_order</span><span class="sxs-lookup"><span data-stu-id="bb963-129">wlan_secure_all_user_profiles_order</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bb963-130">Antes de que una de las funciones con nombre anterior complete su funcionamiento, la función recupera la DACL almacenada en el objeto protegible adecuado.</span><span class="sxs-lookup"><span data-stu-id="bb963-130">Before one of the above-named functions completes its operation, the function retrieves the DACL stored in the appropriate securable object.</span></span> <span data-ttu-id="bb963-131">A continuación, la función comprueba la DACL para ver si el autor de la llamada tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="bb963-131">The function then checks the DACL to see if the caller has sufficient permissions.</span></span> <span data-ttu-id="bb963-132">Las \* funciones WlanGet y WlanQuery \* requieren que la DACL contenga una [entrada de control de acceso (ACE)](../secauthz/access-control-entries.md) que conceda al [token de acceso](../secauthz/access-tokens.md) del subproceso de llamada \_ acceso de lectura \_ a la función.</span><span class="sxs-lookup"><span data-stu-id="bb963-132">The WlanGet\* and WlanQuery\* functions require that the DACL contains an [access control entry (ACE)](../secauthz/access-control-entries.md) that grants the [access token](../secauthz/access-tokens.md) of the calling thread WLAN\_READ\_ACCESS to the function.</span></span> <span data-ttu-id="bb963-133">Las \* funciones WlanSet requieren una ACE que conceda el token de acceso del acceso de escritura de la WLAN del subproceso que realiza la llamada \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bb963-133">The WlanSet\* functions require an ACE that grants the access token of the calling thread WLAN\_WRITE\_ACCESS.</span></span> <span data-ttu-id="bb963-134">Si el autor de la llamada no tiene permisos suficientes, se produce un error en la llamada a la función con el error \_ acceso \_ denegado.</span><span class="sxs-lookup"><span data-stu-id="bb963-134">If the caller does not have sufficient permissions, the function call fails with the error ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="bb963-135">Cada objeto protegible tiene una DACL asociada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="bb963-135">Each securable object has a DACL associated with it by default.</span></span> <span data-ttu-id="bb963-136">Los permisos predeterminados almacenados en la DACL se pueden cambiar mediante la función [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) .</span><span class="sxs-lookup"><span data-stu-id="bb963-136">The default permissions stored in the DACL can be changed using the [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) function.</span></span> <span data-ttu-id="bb963-137">Para determinar los derechos de usuario efectivos necesarios para realizar una operación en un sistema determinado, llame a [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="bb963-137">To determine the effective user rights required to perform an operation on a particular system, call [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span></span>

<span data-ttu-id="bb963-138">Los perfiles de todos los usuarios tienen permisos adicionales asociados al propio perfil.</span><span class="sxs-lookup"><span data-stu-id="bb963-138">All-user profiles have additional permissions associated with the profile itself.</span></span> <span data-ttu-id="bb963-139">Los permisos en un perfil de todos los usuarios se establecen cuando se crea o se modifica el perfil mediante [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) o [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile).</span><span class="sxs-lookup"><span data-stu-id="bb963-139">The permissions on an all-user profile are established when the profile is created or modified using [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) or [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile).</span></span> <span data-ttu-id="bb963-140">El parámetro *strAllUserProfileSecurity* especifica los permisos necesarios para modificar un perfil, eliminar un perfil o conectarse a una red mediante un perfil.</span><span class="sxs-lookup"><span data-stu-id="bb963-140">The *strAllUserProfileSecurity* parameter specifies the required permissions for modifying a profile, deleting a profile, or connecting to a network using a profile.</span></span> <span data-ttu-id="bb963-141">La eliminación o modificación de un perfil requiere el \_ permiso de acceso de escritura de WLAN \_ .</span><span class="sxs-lookup"><span data-stu-id="bb963-141">Deleting or modifying a profile requires WLAN\_WRITE\_ACCESS permission.</span></span> <span data-ttu-id="bb963-142">La conexión a una red mediante un perfil requiere el permiso de acceso de ejecución de WLAN \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bb963-142">Connecting to a network using a profile requires WLAN\_EXECUTE\_ACCESS permission.</span></span>

<span data-ttu-id="bb963-143">\* \* Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2: \* \* no se admiten las funciones [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) y [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) .</span><span class="sxs-lookup"><span data-stu-id="bb963-143">\*\*Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  \*\* The [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) and [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) functions are not supported.</span></span> <span data-ttu-id="bb963-144">No se usa el parámetro *strAllUserProfileSecurity* .</span><span class="sxs-lookup"><span data-stu-id="bb963-144">The *strAllUserProfileSecurity* parameter is not used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb963-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bb963-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb963-146">Cómo controlan el acceso a un objeto las DACL</span><span class="sxs-lookup"><span data-stu-id="bb963-146">How DACLs Control Access to an Object</span></span>](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="bb963-147">**\_objeto protegible de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="bb963-147">**WLAN\_SECURABLE\_OBJECT**</span></span>](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
