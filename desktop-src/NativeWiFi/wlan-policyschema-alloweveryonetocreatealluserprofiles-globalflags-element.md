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
# <a name="alloweveryonetocreatealluserprofiles-globalflags-element"></a><span data-ttu-id="65eac-103">Elemento allowEveryoneToCreateAllUserProfiles (Indicadores_globales)</span><span class="sxs-lookup"><span data-stu-id="65eac-103">allowEveryoneToCreateAllUserProfiles (globalFlags) Element</span></span>

<span data-ttu-id="65eac-104">El elemento **allowEveryoneToCreateAllUserProfiles** (indicadores_globales) especifica si un usuario puede crear un perfil de todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="65eac-104">The **allowEveryoneToCreateAllUserProfiles** (globalFlags) element specifies whether any user can create an all-user profile.</span></span> <span data-ttu-id="65eac-105">Cualquier usuario del equipo puede usar un perfil de todos los usuarios para conectarse a la red inalámbrica asociada al perfil.</span><span class="sxs-lookup"><span data-stu-id="65eac-105">An all-user profile can be used by any user on the machine to connect to the wireless network associated with the profile.</span></span>

<span data-ttu-id="65eac-106">Si **allowEveryoneToCreateAllUserProfiles** es true, el usuario puede crear un perfil de todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="65eac-106">If **allowEveryoneToCreateAllUserProfiles** is TRUE, than any user can create an all-user profile.</span></span> <span data-ttu-id="65eac-107">Si **allowEveryoneToCreateAllUserProfiles** es false, no todos los usuarios pueden crear un perfil de todos los usuarios y existe una DACL asociada al \_ \_ objeto de seguridad agregar nuevo todos los perfiles de usuario de la WLAN \_ \_ \_ \_ que especifica los usuarios o grupos de usuarios con permiso para crear perfiles de todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="65eac-107">If **allowEveryoneToCreateAllUserProfiles** is FALSE, then not all users can create an all-user profile, and there is a DACL associated with the wlan\_secure\_add\_new\_all\_user\_profiles security object that specifies the users or user groups with permission to create all-user profiles.</span></span> <span data-ttu-id="65eac-108">La DACL predeterminada especifica que solo los usuarios que han iniciado sesión como miembro del grupo administradores pueden crear un perfil de todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="65eac-108">The default DACL specifies that only users that are logged on as a member of the Administrators group can create an all-user profile.</span></span> <span data-ttu-id="65eac-109">La configuración de seguridad predeterminada se puede cambiar mediante una llamada a [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="65eac-109">The default security settings can be changed by calling [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings).</span></span> <span data-ttu-id="65eac-110">Para obtener la configuración de seguridad actual, llame a [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="65eac-110">To get the current security settings, call [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span></span>

<span data-ttu-id="65eac-111">Este elemento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="65eac-111">This element is mandatory.</span></span> <span data-ttu-id="65eac-112">Cuando el servicio de configuración automática crea un perfil, este elemento tendrá el valor predeterminado TRUE.</span><span class="sxs-lookup"><span data-stu-id="65eac-112">When a profile is created by the AutoConfig service, this element will have the default value of TRUE.</span></span>

``` syntax
<xs:element name="allowEveryoneToCreateAllUserProfiles"
    type="boolean"
 />
```

<span data-ttu-id="65eac-113">El elemento **allowEveryoneToCreateAllUserProfiles** se define mediante el elemento [**indicadores_globales**](wlan-policyschema-globalflags-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="65eac-113">The **allowEveryoneToCreateAllUserProfiles** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="65eac-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65eac-114">Requirements</span></span>



| <span data-ttu-id="65eac-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="65eac-115">Requirement</span></span> | <span data-ttu-id="65eac-116">Value</span><span class="sxs-lookup"><span data-stu-id="65eac-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="65eac-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65eac-117">Minimum supported client</span></span><br/> | <span data-ttu-id="65eac-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="65eac-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="65eac-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65eac-119">Minimum supported server</span></span><br/> | <span data-ttu-id="65eac-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="65eac-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65eac-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="65eac-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="65eac-122">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="65eac-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="65eac-123">**Indicadores**</span><span class="sxs-lookup"><span data-stu-id="65eac-123">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="65eac-124">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="65eac-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="65eac-125">**Indicadores_globales (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="65eac-125">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




